<template>
  <div class="main">
    <div class="checkout-con">
      <div class="item-selected">
        <p>{{ selectedItem.Item }}</p>
        <p>{{ selectedItem.Time }}</p>
      </div>
      <div class="cart">
        <input
          type="text"
          id="name"
          placeholder="Name"
          required
          class="form-control"
        /><input
          type="tel"
          id="phone"
          placeholder="Phone number"
          class="form-control"
        /><input
          type="email"
          id="email"
          placeholder="Email"
          required
          class="form-control"
        />
        <p>Summary</p>
        <p>Total:R{{ selectedItem.Price }}</p>
        <button v-on:click="sendEmail()" class="btn btn-success">Email</button>
      </div>
    </div>
  </div>
</template>
<script>
import { useRoute } from "vue-router";
import Items from "@/Data";
import emailjs from "emailjs-com";

export default {
  data() {
    const route = useRoute();

    return {
      ItemList: Items,
      selectedItem: [],
      id: route.params.id,
    };
  },
  mounted() {
    this.selectedItem;
    this.ItemList.map((i) => {
      if (i.Id == this.id) {
        this.selectedItem = i;
      }
    });
    console.log(this.selectedItem);
  },
  methods: {
    async sendEmail() {
      let phone = document.getElementById("phone").value;
      let email = document.getElementById("email").value;
      let name = document.getElementById("name").value;
      let message =
        "\n Name: " +
        name +
        "\n Phone: " +
        phone +
        "\n Email: " +
        email +
        "\n Serivce selected:\n " +
        this.selectedItem.Item +
        "\n " +
        this.selectedItem.Time +
        "\n R" +
        this.selectedItem.Price;
      try {
        const result = await emailjs.send(
          "service_ky4ajza", // replace with your EmailJS service ID
          "template_bjlbx6p", // replace with your EmailJS template ID
          {
            title: name,
            name: name,
            from_name: name,
            reply_to: email,
            message: message,
          },
          "AajdHMjsIK7dS_tu-" // replace with your EmailJS public key
        );

        alert("Email sent successfully!");

        // Clear form
        this.name = "";
        this.email = "";
        this.message = "";
      } catch (error) {
        console.log(error);
        alert("Failed to send email. Please try again.");
      }
    },
  },
};
</script>
<style>
@media (max-width: 780px) {
  .packages-details-item {
    width: 40% !important;
  }

  .packages-details a {
    width: 30% !important;
  }

  .packages img {
    width: 20% !important;
  }

  .checkout-con {
    flex-direction: column !important;
    align-items: center !important;
  }

  .item-selected {
    width: 84% !important;
    margin-bottom: 15px;
    margin-top: 10px;
  }

  .cart,
  .item-selected {
    height: 300px !important;
  }

  .cart {
    width: 100% !important;
  }
}

.main {
  height: 100%;
  align-items: center;
}

.checkout-con,
.main {
  display: flex;
  justify-content: center;
}

.checkout-con {
  width: 100%;
}

.item-selected {
  width: 50%;
  background: linear-gradient(90deg, #8d7ecf, #cd47da);
}

.cart,
.item-selected {
  height: 600px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  font-size: x-large;
  color: #fff;
}

.cart {
  width: 30%;
  align-items: center;
}

.cart input {
  width: 50%;
  margin: 10px;
}

.cart button {
  width: 20%;
  border-radius: 20px;
  background: linear-gradient(90deg, #8d7ecf, #a96bd9, #cd47da);
}
</style>
