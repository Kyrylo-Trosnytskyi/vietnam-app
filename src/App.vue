<script>
export default {
  data() {
    return {
      scenarios: [
        {
          title: "Пошук полковника Курца",
          description:
            "Ви отримали завдання від армійського командування знайти полковника Курца, який зник у джунглях В'єтнаму...",
          survivalTips: [
            "Зберіть надійну команду",
            "Будьте пильними у джунглях",
            "Дізнайтеся більше про мотиви полковника",
          ],
        },
        {
          title: "Битва за Хамбургер Гілл",
          description:
            'Вам необхідно очолити військовий загін та здійснити наступ на ворожу позицію на пагорбі, відомому як "Хамбургер Гілл"...',
          survivalTips: [
            "Налаштуйте спілкування з авіаційною підтримкою",
            "Обережно рухайтеся вгору по пагорбу",
            "Забезпечте медичну допомогу пораненим",
          ],
        },
        {
          title: "Захист Сайгону",
          description:
            "Ви повинні захищати місто Сайгон від масового вторгнення сил Північного В'єтнаму та В'єтконгу...",
          survivalTips: [
            "Розмістіть спостережні пункти",
            "Розгорніть важкі засоби вогневої підтримки",
            "Забезпечте евакуацію цивільного населення",
          ],
        },
        {
          title: "Тайний рейд",
          description:
            "Ваш загін отримав завдання просунутися на тил ворога і знищити важливий військовий об'єкт...",
          survivalTips: [
            "Вивчіть маршрут і план атаки",
            "Використовуйте прикриття ночі",
            "Дійте спільно та з координацією",
          ],
        },
      ],
    };
  },
  methods: {
    showSurvivalTips(index) {
      alert(this.scenarios[index].survivalTips.join("\n"));
    },
  },
};
</script>

<template>
  <div id="app">
    <h1 class="text-center my-5">Апокаліпсис сьогодні</h1>
    <div class="container">
      <div class="row">
        <div
          class="col-md-6 mb-4"
          v-for="(scenario, index) in scenarios"
          :key="index"
        >
          <div class="card">
            <div class="card-header">
              <h2>{{ scenario.title }}</h2>
            </div>
            <div class="card-body">
              <p>{{ scenario.description }}</p>
            </div>
            <div class="card-footer">
              <button class="btn btn-danger" @click="showSurvivalTips(index)">
                Що робити?
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
