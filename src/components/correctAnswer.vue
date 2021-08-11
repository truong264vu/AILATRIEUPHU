<template>
  <div class="correctAsw">
       <div id="nextTrue" >
            
              <p></p>
              <div class="tich"></div>
              <p>CORRECT !</p>
              <p>Câu tiếp theo trị giá : $ {{questions[count + 1].point}}</p>
                
              <input type="submit" readonly value="OK" @mousedown="COUNT_UP()" @click="START_TIME()" >

           
        </div>
  </div>
</template>

<script>
import { mapMutations, mapState } from 'vuex';
export default {
    name: 'correctAnswer',
    computed: mapState(['questions','count','totalPoint']),
    methods: mapMutations(['START_TIME','STOP_TIME','COUNT_UP']),
}
</script>

<style scoped>

.correctAsw #nextTrue {
    height: 400px;
    width: 700px;
    background: #362da8;
    border-radius: 30px;
    border: none;

}
.correctAsw .tich {

    height: 100px;
    width: 100px;
    background: url(../../images/true.gif) no-repeat;
    background-size: 100px 100px;
    padding: 10px;
    display: block;
    line-height: 100px;
    margin: 0px 0px 0px 300px;
}
.correctAsw #nextTrue p {
    height: 25px;
    font-size: 25px;
    color: white;
    font-weight: 500;
}
.correctAsw #nextTrue input {
    margin-top: 20px;
    width: 200px;
    height: 60px;
    font-size: 30px;
    background:rgb(3, 3, 134);
    color: white;
    font-weight: 700px;
    text-align: center;
    border-radius: 20px;
    border: none;
}
.correctAsw #nextTrue input:hover {
    cursor: pointer;
    background: rgb(17, 17, 122);
}


/* RPS dien thoai */
@media (max-width: 1100px) {
    
.correctAsw #nextTrue {
    height: 300px;
    width: 500px;
    border-radius: 20px;

}
.correctAsw .tich {

    height: 70px;
    width: 70px;
    background-size: 70px 70px;
    padding: 10px;
    margin: 0px 0px 0px 220px;
}
.correctAsw #nextTrue p {
    height: 10px;
    font-size: 20px;
    color: white;
    font-weight: 200;
}
.correctAsw #nextTrue input {
    margin-top: 20px;
    width: 160px;
    height: 60px;
    font-size: 30px;
    font-weight: 500px;
    border-radius: 20px;
}

}

</style>