<template>
  <div class="main">
    <section class="hero jumbotron jumbotron-fluid p-5 d-flex flex-column justify-content-center">
      <h2 class="w-75">INDULGE YOUR FANTASY</h2>
      <p
        class="w-75"
      >We are Landscapers in Haliburton and Minden Ontario with over 25 years of experience</p>
    </section>
    <section class="container">
      <div class="row justify-content-center">
        <div class="service col-12 p-5 m-2">
          <img class="img-fluid" src="../assets/stonework.jpg" alt="service" />
          <div class="promo m-5">
            <h3>STONEWORK</h3>
            <p>We are capable of building many beautiful features for your property, such as: patios, stepping paths, outdoor kitchens...</p>
            <a class="btn">view more</a>
          </div>
        </div>

        <div class="service col-12 p-5 m-2">
          <img class="img-fluid" src="../assets/hardscape.jpg" alt="service" />
          <div class="promo m-5">
            <h3>HARDSCAPE</h3>
            <p>We are capable of building many beautiful features for your property, such as: patios, stepping paths, outdoor kitchens...</p>
            <a class="btn">view more</a>
          </div>
        </div>

        <div class="service col-12 p-5 m-2">
          <img class="img-fluid" src="../assets/softscape.jpg" alt="service" />
          <div class="promo m-5">
            <h3>SOFTSCAPE</h3>
            <p>We are capable of building many beautiful features for your property, such as: patios, stepping paths, outdoor kitchens...</p>
            <a class="btn">view more</a>
          </div>
        </div>
      </div>
    </section>
    <section class="whyus p-5 my-5 text-center">
      <h3 class="pt-5">WHY US</h3>
      <p
        class="m-auto"
      >Northern Ontario provides a beautiful natural landscape, with that comes many challenges such as: steep slopes, massive rocks, grading and water issues. We have been landscaping Haliburton and landscaping Minden Ontario for over 25 years, giving us the experience and knowledge to transform difficult terrains into the property of your dreams. Visit our Portfolio section to see some of our work</p>
      <a class="btn my-5">view more</a>
    </section>
  </div>
</template>

<script>
export default {};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hero {
  background: url(../assets/hero.jpg) no-repeat center;
  background-size: cover;
}

p {
  font-weight: 300;
}

h2 {
  font-weight: 700;
  font-size: 40px;
}

.service {
  position: relative;
}

.service img {
  position: absolute;
  width: 100%;
  height: 100%;
  z-index: -100;
  object-fit: cover;
  top: 0;
  left: 0;
}

.service h3 {
  font-size: 20px;
  font-weight: 700;
}

.service p {
  font-size: 15px;
  font-weight: 100;
  width: 100%;
}

.service .promo {
  z-index: 200;
}

.btn {
  border: 1px solid white;
  border-radius: 0px;
  padding: 10px 40px;
  color: white;
}

.btn:hover {
  background: white;
  color: #464646;
}

.service:nth-child(even) {
  text-align: right;
}

.service:nth-child(even) p {
  margin-left: auto;
}

.whyus {
  background: #44ad96;
}

.whyus h3 {
  font-size: 50px;
  font-weight: 700;
}

@media only screen and (min-width: 768px) {
  h2 {
    font-size: 80px;
  }

  p {
    font-size: 20px;
  }

  .hero {
    height: 50vw;
  }

  .service h3 {
    font-size: 80px;
  }
}

@media only screen and (min-width: 1440px) {
  h2 {
    font-size: 100px;
  }
}
</style>
