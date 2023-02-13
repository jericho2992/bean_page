<script>
  let rotation=0;
  let flip = false;
   window.onload = (event) => {
    setInterval(()=>{
      if(!flip) {
        rotation+=1;
      } else {
        rotation-=1;
      }
      const trans = "rotate("+rotation+"deg)";
      const el = document.getElementById("wave");
      el.style.transform = trans;
      if(rotation>44) {
        flip=true;
      } else if(rotation<1) {
        flip=false;
      }
    }, 50);
   };
  
  function handleClick() {
    alert("This button doesn't do anything. Maybe one day...");
  }
</script>

<main>
  <div class="meet-div row-content">
    <div class="page-head row-content">
      <img src="./images/engTech.png" id="icon" alt="engTech Icon">
      <h1>
        hello engtech!
      </h1>
    </div>
    <div class="wave" id="wave" style="padding-bottom: 20px;">
      <h1>
        👋
      </h1>
    </div>
  </div>
  <div class="chart-video row-content">
    <div class="chart1" style="margin-right: 2vw;">
      <table>
        <tr><td class="left-td"><h2>📊 Industry</h2></td><td><h2>:</h2></td><td><h2>Engineering</h2></td></tr>
        <tr><td class="left-td"><h2>❤️ Passion</h2></td><td><h2>:</h2></td><td><h2>Diversity</h2></td></tr>
        <tr><td class="left-td"><h2>✏️ Hiring</h2></td><td><h2>:</h2></td><td><h2>Summer Interns</h2></td></tr>
      </table>
    </div>
    <div class="video-wrap">
      <iframe width="560" height="315" src="https://www.youtube.com/embed/KBMWeWvz6vQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" style="border-radius: 10px;" allowfullscreen></iframe>
    </div>
  </div>
  <div class="culture">
    <div class="culture-head">
      <h1>our culture</h1>
    </div>
    <div class="culture-body">
      <ul>
        <li><h2>We Believe in <span>Learning by Doing!</span></h2></li>
        <li><h2>People First</h2></li>
        <li><h2>Work / Life Balance</h2></li>
      </ul>
    </div>
  </div>
  <div class="roles">
    <div class='roles-head'>
      <h1>open roles</h1>
      <div class="roles-head-sub">
        <h2>NYC</h2>
        <h2>🔥 Summer Internship!</h2>
      </div>
    </div>
    <div class="roles-content">
      <ul>
        <li><h3>10 Weeks</h3></li>
        <li><h3>Hybrid (3 days in office)</h3></li>
        <li><h3>Interest in career in engineering</h3></li>
      </ul>
      <button id="apply-button" on:click={handleClick}>Apply Now!</button>
    </div>
  </div>
</main>

<style>
  main{
    display: flex;
    flex-direction: column;
    flex-wrap: nowrap;
    background-color: #ffffff;
    min-height: 100vh;
    min-width: 100vw;
    margin: 0;
  }
  .row-content {
    display: flex;
    flex-direction: row;
  }
  .meet-div {
    justify-content: flex-start;
    align-items: flex-end;
  }
  h1 {
    font-weight: 600;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    color: #ffbe33;
  }
  .page-head {
    margin:0 1vw 0 2vw;
    align-items: flex-end;
  }
  .page-head h1 {
    padding-bottom: 12px;
  }
  #icon {
    height: 10em;
    width: 6em;
  }
  .chart-video {
    background-color: #82b2b9;
    color: #ffffff;
    padding: 2vh 0;
    justify-content: center;
  }
  .chart1 {
    display: flex;
    flex-direction: column;
    align-items: center;
    background-image: linear-gradient(#1f1f1f, rgb(50, 50, 50), #1f1f1f);
    min-height: 315px;;
    min-width: 560px;
    max-width: 560px;
    border-radius: 10px;
    text-align: left;
  }
  .chart1 h2 {
    margin: 1.5em 0.2em;
  }
  td {
    text-align: center;
    width: 7em;
  }
  .culture-head {
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    margin: 0 2vw;
  }
  .culture-body {
    display: flex;
    flex-direction: column;
    align-items: center;
    max-width: 60vw;
    margin: 0 20vw;
    background-image: linear-gradient(#1f1f1f, rgb(50, 50, 50), #1f1f1f);
    color: #ffffff;
    border-radius: 1.5vh;
  }
  li {
    text-align: left;
    margin: 1.5em 0;
  }
  .roles {
    background-color: #1f1f1f;
    margin: 5vh 0;
    color: #ffffff;
    text-align: left;
  }
  .roles h1 {
    color: #ffffff;
    margin-left: 2vw;
    font-weight: 600;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
  .roles-head-sub {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .roles-head-sub h2 {
    font-family: cursive;
    font-size: 1.8em;
    color: #82b2b9;
    margin-top: 0;
  }
  .roles-content {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  #apply-button {
    background-color: #ffbe33;
    margin-bottom: 2vh;
  }
  #apply-button:hover {
    background-color: #82b2b9;
  }
  @media (max-width: 768px) {
    .row-content {
      flex-direction: column;
    }
    iframe {
      max-width: 96vw;
      height: 96vw;
      height: auto;
    }
    .chart1 {
    min-height: auto;
    min-width: 96vw;
    max-width: 96vw;
    margin-bottom: 5vh;
    margin-right: 0;
    }
    .meet-div {
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    .page-head {
      align-items: center;
    }
    .chart-video {
      align-items: center;
    }
    .culture-head {
      justify-content: center;
    }
    .roles-head {
      text-align: center;
    }
  }
</style>
