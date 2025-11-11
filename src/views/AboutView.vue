<template>
  <div class="about container">
    <h1 class="header">About page</h1>
    <div class="about-con">
      <p>
        <span> Location:</span> Provided upon request, we work on drop off and
        pick up but we also do picks and drop offs at an extra charge to
        customers in Cape Town. Charge won’t exceed R200 depending on the
        distance.
      </p>
      <p>
        <span>Rotation:</span> this is where we clean up to 8 pairs of your
        sneakers for the set price given.
      </p>
    </div>
    <div class="about-icon-con">
      <h4>Restoring</h4>
      <div class="about-icon-list">
        <div class="about-icon">
          <img
            class="d-block w-100"
            src="../assets/img/painting.svg"
            alt="Second slide"
          />
          <p>Painting</p>
        </div>
        <div class="about-icon">
          <img
            class="d-block w-100"
            src="../assets/img/gluebottle.svg"
            alt="Second slide"
          />
          <p>Glueing</p>
        </div>
        <div class="about-icon">
          <img class="d-block w-100" src="../assets/img/dye.svg" alt="" />
          <p>De-yellowing</p>
        </div>
        <div class="about-icon">
          <img class="d-block w-100" src="../assets/img/dye.svg" alt="" />
          <p>Dyeing</p>
        </div>
      </div>
    </div>
    <div class="about-icon-txt">
      <span> Basic clean:</span> our basic clean will attack all the basic
      elements in order for your shoe to return to its clean best. Price: Price
      may differ depending on what you want done, we also running many different
      specials which we communicate on WhatsApp. <br /><span> More:</span>
      This is our 2nd year in business, which has allowed for growth in the ways
      we are able to satisfy different customer needs.
    </div>
  </div>
</template>

<style>
.about {
  color: #fff;
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.about-icon-txt {
  width: 70%;
  margin-bottom: 40px;
}

.about-icon img {
  width: 20% !important;
  margin: 10px;
}

.about p {
  margin: 0;
}

.about-icon-con {
  margin: 40px 0 40px;
}

.about-icon-list {
  display: flex;
  justify-content: center;
}

.about-con {
  padding: 20px;
  margin: 40px 0 40px;
  width: 70%;
}

.about-icon {
  display: flex;
  align-items: center;
  padding: 20px;
}

span {
  background: linear-gradient(90deg, #8d7ecf, #cd47da);
}

@media (max-width: 780px) {
  .about-icon-list {
    flex-wrap: wrap;
  }

  .about-icon {
    width: 60%;
  }

  .about-con,
  .about-icon-txt {
    width: 100%;
  }

  .about-icon-con {
    margin: 10px 0 10px;
  }

  .about-con {
    margin: 20px 0 20px;
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
