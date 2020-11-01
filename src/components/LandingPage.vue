<template>
    <div class="mainFlex">
    <!-- Parralax Image -->
    <div class="parallax">
      <v-parallax src="../assets/poster.jpg"></v-parallax>
      <div class="buttonDiv">
        <v-btn id="posterButton" @click.stop="rmDial = true" dark>READ MORE</v-btn>
      </div>
    </div>
    <!-- Paragraph cum poster -->
    <div class="rowFlex mt-12 mx-4">
      <div>
        <p>Indian law now requires companies to give 2% of their profits to charity. After all, a bone to the dog is not charity. Charity is the bone shared with the dog, when you are just as hungry as the dog. So, a corporate can donate either with a bitter feeling that they are being forced or with open arms, as an opportunity to make a difference. Dream Girl Foundation has made charity easier than ever. A corporate can partner with Dream Girl Foundation and in turn help needy children by using one (or more) of the following partnership.</p>
      </div>
      <div>
        <img src="../assets/para1.jpg" />
      </div>
    </div>
      <v-dialog v-model="rmDial">
        <v-card>
            <v-card-title>
                <p>“We make a living by what we get,
                    But we make a life by what we give.”<br>
                    -Winston Churchill
                </p>
                <p>
                  “The life of a man consists not in seeing visions and in dreaming dreams, but in active charity and in willing service”<br>
                  -Henry Wadsworth Longfellow
                </p>
                <p>
                  “He who wished to secure the good of others,
                  Has already secured his own.”<br>
                  -Confucius
                </p>
                <p>
                  “Every good act is charity. A man's true wealth hereafter is the good that he does in this world to his fellows.”<br>
                  -Moliere
                </p>
            </v-card-title>
        </v-card>
    </v-dialog>
  </div>
</template>

<script>
  export default {
    name: 'LandingPage',
    data: () => ({
      rmDial: false
    })
  }
</script>

<style scoped>
.mainFlex {
  display: flex;
  flex-flow: column;
  justify-content: space-evenly;
}
.parallax {
  position: relative;
  text-align: center;
}
.buttonDiv {
  position: absolute;
  top: 85%;
  left: 45%;
}
#posterButton{
  background-color: transparent;
  box-shadow: none;
  border: 1px solid white;
}
.rowFlex {
  display: flex;
  flex-flow: row;
  justify-content: space-evenly;
}
.rowFlex div {
  padding: 10px;
}
.rowFlex div p {
  text-align: justify;
}
.rowFlex div img {
  width: 50vw;
  height: auto;
}
</style>
