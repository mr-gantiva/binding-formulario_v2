<script setup>
import { ref, computed } from 'vue'
import HelloWorld from './components/HelloWorld.vue'

const text = ref('')
const selected = ref('')
const picked = ref('')
const checkedLearnedSkills = ref([''])
const textArea = ref('')


// Función para obtener emoji
const emojiSelector = computed(() => imagenEmoji[emoji.value]);
</script>

<template>

  <div class="container">
    <div class="row">

      <!-- Left Section Form -->
      <div class="col-12 col-md-6 mb-5">
        <div class="left__side">

          <!-- Input Text -->
          <div class="mb-3 py-2 d-flex align-items-center">
            <label for="exampleFormControlInput1" class="form-label px-2">Titulo:</label>
            <input v-model="text" type="text" class="form-control" id="exampleFormControlInput1"
              placeholder="Estoy aprendiendo...">
          </div>

          <hr>

          <!-- Select -->
          <div class="box__option d-flex align-items-center">
            <label for="" class="px-2">Emoji</label>
            <select v-model="selected" class="form-select py-2" aria-label="Default select example">
              <option disabled value="">Please select one</option>
              <option value="😎">😎</option>
              <option value="🧑‍💻">🧑‍💻</option>
              <option value="👍">👍</option>
            </select>
          </div>

          <hr>

          <!-- Radio -->
          <div class="box__radio d-flex flex-wrap justify-content-between align-items-center py-2">
            <span>Apreciación:</span>
            <div class="form-check">
              <input v-model="picked" class="form-check-input" type="radio" value="Regular" id="flexRadioDefault1"
                checked>
              <label class="form-check-label" for="flexRadioDefault1">
                Regular
              </label>
            </div>
            <div class="form-check">
              <input v-model="picked" class="form-check-input" type="radio" value="Bien" id="flexRadioDefault2">
              <label class="form-check-label" for="flexRadioDefault2">
                Bien
              </label>
            </div>
            <div class="form-check">
              <input v-model="picked" class="form-check-input" type="radio" value="Muy bien" id="flexRadioDefault3">
              <label class="form-check-label" for="flexRadioDefault3">
                Muy bien
              </label>
            </div>
            <div class="form-check">
              <input v-model="picked" class="form-check-input" type="radio" value="Increible" id="flexRadioDefault4">
              <label class="form-check-label" for="flexRadioDefault4">
                Increible
              </label>
            </div>
          </div>

          <hr>

          <!-- Checkbox -->
          <div class="box__check py-2">

            <div class="row">
              <div class="col-12 col-md-4 text-start">
                <span>Competencias aprendidas:</span>
              </div>
              <div class="col-12 col-md-4 text-start">
                <div class="form-check">
                  <input v-model="checkedLearnedSkills" class="form-check-input" type="checkbox"
                    value="Morfología de un componente" id="morfologia" checked>
                  <label class="form-check-label" for="morfologia">
                    Morfología de un componente
                  </label>
                </div>

                <div class="form-check">
                  <input v-model="checkedLearnedSkills" class="form-check-input" type="checkbox"
                    value="One-Way y Two-Way data binding" id="OneWayTwoWay">
                  <label class="form-check-label" for="OneWayTwoWay">
                    One-Way y Two-Way data binding
                  </label>
                </div>

                <div class="form-check">
                  <input v-model="checkedLearnedSkills" class="form-check-input" type="checkbox"
                    value="El patrón de diseño MVVM" id="patronMVVM">
                  <label class="form-check-label" for="patronMVVM">
                    El patrón de diseño MVVM
                  </label>
                </div>
              </div>

              <div class="col-12 col-md-4 text-start">
                <div class="form-check">
                  <input v-model="checkedLearnedSkills" class="form-check-input" type="checkbox" value="Directivas"
                    id="directivas">
                  <label class="form-check-label" for="directivas">
                    Directivas
                  </label>
                </div>

                <div class="form-check">
                  <input v-model="checkedLearnedSkills" class="form-check-input" type="checkbox" value="Estado"
                    id="estado">
                  <label class="form-check-label" for="estado">
                    Estado
                  </label>
                </div>
              </div>
            </div>
          </div>

          <hr>

          <!-- Text area -->
          <div class="mb-3 py-2 text-start">
            <label for="exampleFormControlTextarea1" class="form-label">Opinión</label>
            <textarea v-model="textArea" class="form-control" id="exampleFormControlTextarea1" rows="3"></textarea>
          </div>
        </div>
      </div>

      <!--Right Section -->

      <div class="col-12 col-md-6 mb-5">
        <div class="right__side">
          <p>{{ selected }}</p>
          <p>{{ text }}</p>
          <p>Y me parece {{ picked }}</p>
          <p>{{ checkedLearnedSkills }}</p>
          <p>{{ textArea }}</p>
        </div>
      </div>
    </div>
  </div>

</template>

<style scoped>
.container {
  color: #fff;
}

.left__side {
  background: rgba(255, 255, 255, 0.2);
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(5px);
  -webkit-backdrop-filter: blur(5px);
  border: 1px solid rgba(255, 255, 255, 0.3);
}

:is(.left__side, .right__side) {
  border-radius: 10px;
  padding: 20px;
}

.right__side {
  background-color: #fff;
  color: #202b38;
}
</style>
