<div class="jumbotron jumbotron-fluid">
  <div class="container">
    <h1 class="display-4">Barnsley Healthy Holiday Clubs</h1>
    <p class="lead">Once again we are pleased to join up with Barnsley Council for our Holiday Clubs.</p>
    <hr class="my-4">
    <p>Classes are free for children on free school meals, with the Barnsely Council Healthy Holidays code, or £18.00 otherwise, and include a meal.</p>
    <p>To register, pick your days from the list below and fill in  your. If you do not qualify for free school, we will be in touch to arrange payment. </p>


    <div class="container">
{% for club in site.data.holiday_clubs %}
  {% assign loopindex = forloop.index | modulo: 4 %}
  {% if loopindex == 1 %}
    <!-- start loop -->
    <div class="row">
  {% endif %}
        <div class="card col-sm">
          <img class="card-img-top" src="{{ site.baseurl }}/assets/img/239103681_4221236217952071_7560413288161334995_cropped.jpg" alt="Building dens at holiday club">
          <div class="card-body">
            <h5 class="card-title text-dark">{{ club.Title }}</h5>
            <h6 class="card-subtitle mb-2 text-muted">9:30am until 1:30pm</h6>
            <a href="https://my.barnsley.gov.uk/Events/BookTickets/{{ club.Number }}" target="_blank" class="card-link btn btn-primary">Book</a>
          </div>
        </div>
  {% if loopindex == 0 %}
    </div>
    <!-- end loop -->
  {% endif %}
{% endfor %}
    </div>
  </div>
</div>
