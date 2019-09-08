<template lang="pug">
  h1.display-3.subheading.grey--text Home 
      v-container.my-5
        v-layout( row wrap )
          v-carousel(hide-delimiter-background show-arrows-on-hover dark )
            v-carousel-item(v-for="day in rasp" :key="day.day")
              .black--text {{day.day}}
              v-card(light).text-center()
                v-card-text(v-for="lesson in day.lessons" :key="lesson.name")
                    .black--text {{lesson.name}}
                    .black--text {{lesson.time}}
                    .black--text {{lesson.aud}}
                    .black--text {{lesson.teacher}}
                    .black--text {{lesson.type}}                    

                
</template>

<script>


export default {
  data() {
    return {
      rasp: [
          {day: 'Понедельник', lessons: [
          {name: 'test lesson 1', time: '9:00', aud: 'Аудитория 1', teacher: 'TEACHER', type: 'Лекция'},
          {name: 'test lesson 2', time: '10:00', aud: 'Аудитория 2', teacher: 'TEACHER', type: 'Лекция'},
           {name: 'test lesson 1', time: '9:00', aud: 'Аудитория 1', teacher: 'TEACHER', type: 'Лекция'}
        
        ]},
        {day: 'Вторник', lessons: [
          {name: 'test lesson 1', time: '9:00', aud: 'Аудитория 1', teacher: 'TEACHER', type: 'Лекция'},
          {name: 'test lesson 3', time: '10:00', aud: 'Аудитория 2', teacher: 'TEACHER', type: 'Лекция'}
        ]},
        {day: 'Среда', lessons: [
          {name: 'test lesson 1', time: '9:00', aud: 'Аудитория 1', teacher: 'TEACHER', type: 'Лекция'},
          {name: 'test lesson 3', time: '10:00', aud: 'Аудитория 2', teacher: 'TEACHER', type: 'Лекция'}
        ]},
        {day: 'Четверг', lessons: [
          {name: 'test lesson 1', time: '9:00', aud: 'Аудитория 1', teacher: 'TEACHER', type: 'Лекция'},
          {name: 'test lesson 3', time: '10:00', aud: 'Аудитория 2', teacher: 'TEACHER', type: 'Лекция'}
        ]} ]
    }
  },
  components: {

  }
};
</script>
