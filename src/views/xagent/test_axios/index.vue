
<style scoped>
  h2{
    text-align: center;
    padding: 30px;
    font-size: 18px;
  }
  #chart_example{
    width: 50%;
    height: 500px;
    border: 1px solid red;
    margin: 0 auto;
  }
</style>
<template>
  <div>
    <h2> {{title}}</h2>

  </div>
</template>


<script>
    export default {
      data() {
            return {"title": "test-axios"}
          },
      mounted: function () {
        let url = 'http://192.168.2.227/cso/mg/jwt_login/'
        let params = {
          username: 'admin001',
          password: '112233..'
        }
        this.$ajax.post(url, params).then(function (res) {
           console.log(res)
        }).catch(function (err) {
          console.log(err)
        })
      }
    }
</script>
