<template>
    <div>
            <router-link class="event-link" :to="{ name: 'event-show', params: { id: event.id } }" 
            v-for="event in events" :key="event.id">
                <div class="event-card -shadow">
                <span class="eyebrow">@{{ event.time }} on {{ event.date }}</span>
                <h4 class="title">{{ event.title }}</h4>
                {{ event.attendees.length }} attending
                </div>
            </router-link>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                events:
                [
                    {
                        id: 1,
                        date:"Tue Aug 30 2019",
                        time:"06:30",
                        attendees:[
                            { id:'abc1234',name:'Samit' },
                            { id:'def456',name:'Johny' }
                        ]
                    },
                     {
                        id: 2,
                        date:"Fri Sep 11 2019",
                        time:"10:30",
                        attendees:[
                            { id:'abc1234',name:'Bobby' },
                            { id:'def456',name:'Eellbe' }
                        ]
                    },
                ]
            }
        },
    }
</script>

<style  scoped>
.event-card {
  padding: 20px;
  margin-bottom: 24px;
  transition: all 0.2s linear;
  cursor: pointer;
}
.event-card:hover {
  transform: scale(1.01);
  box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2), 0 1px 15px 0 rgba(0, 0, 0, 0.19);
}
.event-card > .title {
  margin: 0;
}
.event-link {
  color: black;
  text-decoration: none;
  font-weight: 100;
}
</style>