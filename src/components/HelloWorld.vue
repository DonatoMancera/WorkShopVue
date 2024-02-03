<template>
  <div class="hello">
    <h1 class="title">{{ msg }}</h1>
    <div class="container">
      <div v-for="(card, index) in cards" :key="index" class="row mb-4">
        <div class="col-md-12">
          <div class="card">
            <div class="row no-gutters">
              <div class="col-md-1 d-flex justify-content-center align-items-center">
                <img :src="card.image" alt="Imagen" class="card-img" style="width: 70px; height: 70px; object-fit: cover;">
              </div>
              <div class="card-body col-md-11">
                  <div class="mb-2 d-flex">
                    <a class="mb-0 pb-0 text-left bold" href="#" style="text-decoration: none; color: black ;">
                      <h5 class="d-md-inline-flex">{{card.title}}</h5>
                    </a>
                  </div>
                  <div class="row">
                    <div class="col-2 d-flex">
                      <p>{{card.company}}</p>
                    </div>
                    <div class="col-2">
                      <p>{{card.country}}</p>
                    </div>
                    <div class="col-2 ">
                      <p>{{card.salary}}</p>
                    </div>
                    <div class="col-2 ">
                      <p>{{card.vacancies}}</p>
                    </div>
                    <div class="col-2 ">
                      <p>{{card.date}}</p>
                    </div>
                  </div>
                </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    return {
      cards: [
      { 
        title: 'Ingeniero de Calidad', 
        company:"OFFIMEDICAS SAS",
        country: "Bogota",
        salary: "$ 1.4M - 1.6M COP",
        vacancies: "1 vacante",
        date: 'hace 2 horas', 
        image: 'https://images.pexels.com/photos/681467/pexels-photo-681467.jpeg' 
      },
      { 
        title: 'IT Sales Consultant', 
        company: "INTEXUS",
        country: "Medellin",
        salary: "$ 1.8M - 2M COP",
        vacancies: "1 vacante",
        date: 'hace dos minutos', 
        image: 'https://images.pexels.com/photos/1563355/pexels-photo-1563355.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1' 
      },
      { 
        title: 'Senior Full Stack Developer', 
        company: "20 MOVES",
        country: "Barranquilla",
        salary: "$ 8M - 10M COP",
        vacancies: "1 vacante",
        date: 'hace dos meses', 
        image: 'https://images.pexels.com/photos/2101187/pexels-photo-2101187.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1' },
    ]
    }
  },  
  
}
</script>


<style scoped>
  .card {
  transition: box-shadow 0.3s;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}


.card:hover {
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}
</style>
