<template>
    <div class="card" @mouseenter="hover = true" @mouseleave="hover = false">
      <div class="compact-top">
         <img src="../assets/close_quarter.png" alt="Magazine Icon" class="icon"/>
      </div>
      <div class="compact-bottom">
        <p class="basic-title" >Basic Magazine</p>
      </div>
    </div>

    <div v-if="hover" class="detailed-view">
      <div class="card-header">
        <span class="title">Basic Magazine</span>
        <img src="../assets/basic_magazine.png" alt="Icon" class="icon"/>
      </div>
      <div class="card-body">
        <p class="price">$ 500</p>
        <ul class="stats">
          <li>+24% <span class="ammo">Ammo</span></li>
          <li>+15% <span class="damage">Weapon Damage</span></li>
        </ul>
      </div>
      <div class="card-footer">
        <p>IS COMPONENT OF:</p>
        <a href="#" class="component-link">
          <img src="../assets/titanic_magazine.png" alt="Titanic Icon" class="component-icon" /> Titanic Magazine
        </a>
      </div> 
    </div>
  </template>
  
<script>
export default {
  name: 'MagazineCard',
  data(){
    return {
      hover: false
    }
  },
  props: {
    compact: {
      type: Boolean,
      default: true,
    },
  },
}

</script>
  <style scoped>

  /* Main card styling */
  .card {
    width: 138px;
    height: 154px;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    font-family: Arial, sans-serif;
    cursor: pointer;
    transition: all 0.3s ease;
    overflow: hidden;
  }
  
  /* Basic view styling */
  .compact-top {
    display: flex;
    height: 50%;
    flex-direction: column;
    align-items: center;
    background: rgb(208,141,62);
    text-align: center;
    vertical-align: middle;
  }
  
  .compact-bottom {
    display: flex;
    height: 50%;
    flex-direction: column;
    align-items: center;
    background: rgb(240, 225, 203);
    text-align: center;
    vertical-align: middle;
  }

  .basic-title {
    text-align: center;
    vertical-align: middle;
    display: auto;
    margin: auto;
    /* position: relative;
    font-size: 14px;
    font-weight: bold;
    color: rgb(15,18,12); */
  }
  
  .icon {
    display: block;
    margin: auto;
    /* filter: blur(0px) drop-shadow(5px 5px rgb(46,33,5,1)); */
    filter: invert();
    height: 75%;
  }
  
  /* Detailed view styling */
  .detailed-view {
    width: 300px;
    background: #b76e00;
    color: white;
    padding: 10px;
    box-sizing: border-box;
  }
  
  .card-header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border-bottom: 1px solid #00000050;
  }
  
  .title {
    font-size: 18px;
    font-weight: bold;
  }
  
  .card-body {
    padding: 10px 0;
  }
  
  .price {
    font-size: 24px;
    color: #33ff99;
    margin: 0;
  }
  
  .stats {
    list-style: none;
    padding: 0;
    margin: 0;
  }
  
  .stats li {
    color: #cccccc;
    margin-bottom: 5px;
  }
  
  .ammo {
    color: #66ccff;
  }
  
  .damage {
    color: #ff6666;
  }
  
  .card-footer {
    background: #8a5a00;
    padding: 5px;
    border-radius: 5px;
    margin-top: 10px;
  }
  
  .component-link {
    color: #99ccff;
    text-decoration: none;
    display: flex;
    align-items: center;
  }
  
  .component-icon {
    width: 20px;
    height: 20px;
    margin-right: 5px;
  }
  </style>