<template>
  <div class="sticky top-0 z-10 w-screen">
    <n-progress
        type="line"
        :percentage="10"
        :height="8"
        :border-radius="0"
        rail-color="rgba(27, 153, 139, 0.2)"
        color="#1B998B"
        :show-indicator="false"
      />
      <n-card class="px-[50px] 2xl:px-[260px] header-font bg-[#FFF] header-shadow">
        <n-space justify="space-between">
          <h1 class="text-[#212831] text-[28px] leading-[45px] font-bold tracking-[0.3px]">Some Title</h1>
          <n-button 
            class="text-[#FFF] font-extrabold text-xl leading-[22px] tracking-[0.35px] bg-[#0872BA] rounded-lg 
              border-transparent px-[22px] py-[19px]"
          >
            Nächste Frage
          </n-button>
        </n-space>
      </n-card>
  </div>

  <main class="bg-[#F8F8F9]">
    <div class="w-screen 2xl:w-[1400px] mx-auto ">
    <div class="message-font pt-[50px] pb-[42px] mx-auto flex justify-start px-[40px] 2xl:px-0">
      <img src="../../../assets/info-square.svg" alt="warning" class="w-[43px] h-[43px] mr-[25px] flex-none"/>
        <p class="text-[#121] text-[22px] leading-[33px] tracking-[0.5px] font-normal opacity-75 grow">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris dui diam, auctor sed placerat id, egestas a purus. 
          Aliquam in orci sit amet magna mattis varius
        </p>
    </div>

    <n-card class="letter bg-[#FFF] pt-[17px] rounded-t-2xl mx-[35px] 2xl:mx-auto w-screen 2xl:w-[1400px] relative lg:block px-[40px] 2xl:px-0">
      <div class="text-[22px] leading-[78px] tracking-[0.35px] text-[#121] pb-[20px] px-[46px] border-b-dashed"> 
        Liebe Claudia, <br/>
        entschuldige, dass ich mich so lange nicht bei dir gemeldet <br/>
        Wie du weißt, bin ich vor zwei Wochen
         <div 
            class="drop-zone inline-flex"
            @drop="onDrop($event, '1')"
            @dragenter.prevent
            @dragover.prevent
          >
            <div v-if="getList('1').length > 0">
              <template v-for = "item in getList('1')" :key="item.id">
                <div  
                  draggable="true"
                  @dragstart="startDrag($event, item)"
                  :class="item.class"
                  class="relative"
                >
                  {{ item.title }}
                  <img src="../../../assets/cancel.svg" alt="cancel" @click="cancelWord(item)" class="cancel" />
                </div>                
              </template>               
            </div>
            <div v-else class="empty 1" >
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
            </div>
          </div>
       Deswegen hatte ich leider keine Zeit 
          <div 
            class="drop-zone inline-flex"
            @drop="onDrop($event, '2')"
            @dragenter.prevent
            @dragover.prevent
          >
            <div v-if="getList('2').length > 0">
              <template v-for = "item in getList('2')" :key="item.id">
                <div  
                  draggable="true"
                  @dragstart="startDrag($event, item)"
                  :class="item.class"
                  class="relative"
                >
                  {{ item.title }}
                  <img src="../../../assets/cancel.svg" alt="cancel" @click="cancelWord(item)" class="cancel" />
                </div>                
              </template>               
            </div>
            <div v-else class="empty 2" >
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
            </div>
          </div>
        meine Freunde. Aber deinen Vorschlag, mal wieder gemeinsam 
          <div 
            class="drop-zone inline-flex"
            @drop="onDrop($event, '3')"
            @dragenter.prevent
            @dragover.prevent
          >
            <div v-if="getList('3').length > 0">
              <template v-for = "item in getList('3')" :key="item.id">
                <div  
                  draggable="true"
                  @dragstart="startDrag($event, item)"
                  :class="item.class"
                  class="relative"
                >
                  {{ item.title }}
                  <img src="../../../assets/cancel.svg" alt="cancel" @click="cancelWord(item)" class="cancel" />
                </div>                
              </template>               
            </div>
            <div v-else class="empty 3" >
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
            </div>
          </div>
        Tag miteinander zu verbringen, finde ich 
        sehr gut. Mir passt es auch am besten am Wochenende. Würde es bei dir schon 
          <div 
            class="drop-zone inline-flex"
            @drop="onDrop($event, '4')"
            @dragenter.prevent
            @dragover.prevent
          >
            <div v-if="getList('4').length > 0">
              <template v-for = "item in getList('4')" :key="item.id">
                <div  
                  draggable="true"
                  @dragstart="startDrag($event, item)"
                  :class="item.class"
                  class="relative"
                >
                  {{ item.title }}
                  <img src="../../../assets/cancel.svg" alt="cancel" @click="cancelWord(item)" class="cancel" />
                </div>                
              </template>               
            </div>
            <div v-else class="empty 4" >
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
            </div>
          </div>
        Samstag gehen? Da habe ich 
        noch nichts vor. Es würde 
          <div 
            class="drop-zone inline-flex"
            @drop="onDrop($event, '5')"
            @dragenter.prevent
            @dragover.prevent
          >
            <div v-if="getList('5').length > 0">
              <template v-for = "item in getList('5')" :key="item.id">
                <div  
                  draggable="true"
                  @dragstart="startDrag($event, item)"
                  :class="item.class"
                  class="relative"
                >
                  {{ item.title }}
                  <img src="../../../assets/cancel.svg" alt="cancel" @click="cancelWord(item)" class="cancel" />
                </div>                
              </template>               
            </div>
            <div v-else class="empty 5" >
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
            </div>
          </div> 
          natürlich freuen, wenn du dir bei dieser Gelegenheit 
        auch meine neue Wohnung anschaust. Es ist wunderbar, so viel zu haben. Was meinst du, wir uns bei mir treffen und dann unsere 
        Einkaufstour machen? Oder ist es dir 
          <div 
            class="drop-zone inline-flex"
            @drop="onDrop($event, '6')"
            @dragenter.prevent
            @dragover.prevent
          >
            <div v-if="getList('6').length > 0">
              <template v-for = "item in getList('6')" :key="item.id">
                <div  
                  draggable="true"
                  @dragstart="startDrag($event, item)"
                  :class="item.class"
                  class="relative"
                >
                  {{ item.title }}
                  <img src="../../../assets/cancel.svg" alt="cancel" @click="cancelWord(item)" class="cancel" />
                </div>                
              </template>               
            </div>
            <div v-else class="empty 6" >
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
            </div>
          </div> 
           , wenn wir zuerst einkaufen und am Abend zusammen kochen und essen? Übrigens, 
        können wir dein Auto nehmen? 
          <div 
            class="drop-zone inline-flex"
            @drop="onDrop($event, '7')"
            @dragenter.prevent
            @dragover.prevent
          >
            <div v-if="getList('7').length > 0">
              <template v-for = "item in getList('7')" :key="item.id">
                <div  
                  draggable="true"
                  @dragstart="startDrag($event, item)"
                  :class="item.class"
                  class="relative"
                >
                  {{ item.title }}
                  <img src="../../../assets/cancel.svg" alt="cancel" @click="cancelWord(item)" class="cancel" />
                </div>                
              </template>               
            </div>
            <div v-else class="empty 7" >
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
            </div>
          </div> 
           steht schon wieder in der Werkstatt. Schreib mir doch bald, ob du an diesem Tag Zeit hast. 
        <div 
            class="drop-zone inline-flex"
            @drop="onDrop($event, '8')"
            @dragenter.prevent
            @dragover.prevent
          >
            <div v-if="getList('8').length > 0">
              <template v-for = "item in getList('8')" :key="item.id">
                <div  
                  draggable="true"
                  @dragstart="startDrag($event, item)"
                  :class="item.class"
                  class="relative"
                >
                  {{ item.title }}
                  <img src="../../../assets/cancel.svg" alt="cancel" @click="cancelWord(item)" class="cancel" />
                </div>                
              </template>               
            </div>
            <div v-else class="empty 8" >
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
              <img src="../../../assets/green-dot.svg" alt="dot" class="mr-[7px] w-[7px] h-[7px]"/>
            </div>
          </div> 
          du keine Zeit hast, finden wir sicher einen anderen Tag. <br/>
        Marion
        </div>
        <div
          @dragenter.prevent
          @dragover.prevent
          class="words-list sticky bottom-0 lg:block"
        >
          <div v-for = "item in getList('words')"
            :key="item.id"
            :draggable="item.class === 'inactive' ? false : true"
            @dragstart="startDrag($event, item)"
            :class="item.class"
            @click="choseAnswer($event)"
          >
            {{ item.title }}
          </div>
        </div>
    </n-card>
    </div>
  </main>

</template>

<script>
import { ref } from 'vue'

export default ({
  setup() {
    const items = ref([
      {id: 1, title: 'umgezogen', list: 'words', class: 'active'}, 
      {id: 2, title: 'mich', list: 'words', class: 'active'},
      {id: 3, title: 'einen', list: 'words', class: 'active'},
      {id: 4, title: 'nächsten', list: 'words', class: 'active'},
      {id: 5, title: 'für', list: 'words', class: 'active'},
      {id: 6, title: 'lieber', list: 'words', class: 'active'},
      {id: 7, title: 'wollen', list: 'words', class: 'active'},
      {id: 8, title: 'Meines', list: 'words', class: 'active'},
    ])

    const getList = (list) => {
      return items.value.filter(item => item.list === list)
    }

    const startDrag = (event, item) => {
      event.dataTransfer.dropEffect = 'move'
      event.dataTransfer.effectAllowed = 'move'
      event.dataTransfer.setData('id', item.id)
    }

    const listValidate = (list, newItem) => {
      const id = newItem.id
      const all = items.value.filter(item => item.list === list)
      if(all.length >= 2) {
        items.value.forEach((item, index) => {
          if (item.list === list && item.id !== id) {
            const original = items.value.find(i => i.id === (item.id - 10))
            original.class="active"
            items.value.splice(index, 1)
          }

          if (item.list === list && item.id === id) {
            items.value.splice(index, 1)
          }

        })
      }
    }

    const onDrop = (event, list, id) => {
      let item = null

      if(typeof event === 'object' && event !== null) {
        const itemId = event.dataTransfer.getData('id')
        item = items.value.find(item => item.id == itemId)
      }
      
      if(id) {
        item = items.value.find(item => item.id === id)
      }

      if (item.list !== 'words') {
        item.list = list
        listValidate(list, item)
        return
      }

      const newItem = {...item}
      newItem.list = list
      newItem.id += 10
      item.class="inactive"
      newItem.class='active'
      items.value.push(newItem)
      listValidate(list, newItem)
    }

    const cancelWord = (item) => {
      const original = items.value.find(i => i.id === (item.id - 10))
      original.class="active"
      const copy = items.value.findIndex(i => i.id === item.id)
      items.value.splice(copy, 1)
    }

    const choseAnswer = (event) => { 
      if(event.srcElement.className === 'inactive') {
        return
      }

      const item = items.value.find(item => item.title === event.target.outerText)
      const dropZones = document.querySelectorAll('.drop-zone div')
      dropZones.forEach(zone => {
        zone.onclick = (event) => getAnswer(event)
      })

      function getAnswer(event) {
        const style = event.srcElement.className
        if(style.includes('empty')) {
          const list = style.slice(6)
          onDrop(_, list, item.id)
        }        
      }
    }

    const startDrop = (item) => {
      onDrop(item.event, item.listNumber)
    }

    const startDragging = (i) => {
      startDrag(i.event, i.item)
    }

    return {
      getList,
      startDrag,
      onDrop,
      cancelWord,
      choseAnswer,
      startDrop,
      startDragging
    };
  },
});
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Archivo:wght@700;800&family=Hind&family=Mulish&display=swap');

.header-font{
  font-family: 'Archivo', sans-serif;
}

.header-shadow {
  box-shadow: 0px 0px 10px 1px rgba(0, 0, 0, 0.05);
}

.message-font {
  font-family: 'Hind', sans-serif;
}

.letter {
  font-family: 'Mulish', sans-serif;
  border: 0.5px solid rgba(0, 0, 0, 0.1);
  box-shadow: 0px 8px 40px rgba(1, 33, 54, 0.05);
}

.empty {
  border: 1px solid rgba(0, 0, 0, 0.15);
  background: #FFFFFF;
  border-radius: 10px;
  display: inline-flex;
  padding: 20px 70px;
  justify-content: center;
  align-items: center;
  margin: 0 40px;
}

.cancel {
  position: absolute;
  top: -15px;
  right: -15px;
  width: 30px;
  height: 30px;
}

.words-list {
  border-top: 1px dashed #BABACC;
  border-image: url('../../../assets/line-dashed.svg') 2 fill repeat;
  padding: 82px 48px 0;
  display: flex;
  flex-flow: row wrap;
  justify-content: space-between;
  align-content: space-between;
  gap: 56px 120px;
  background-color: #FFFFFF
}

.active {
  font-family: 'Hind', sans-serif;
  width: 163px;
  height: 46px;
  background-color: #1B998B;
  border-radius: 10px;
  color: #FFF;
  letter-spacing: 0.5px;
  font-size: 18px;
  line-height: 29px;
  display: inline-flex;
  justify-content: center;
  align-items: center;
}

.drop-zone .active {
  margin: 0 40px;
}

.inactive {
  font-family: 'Hind', sans-serif;
  width: 163px;
  height: 46px;
  background: rgba(30, 165, 154, 0.2);
  border: 1px solid rgba(30, 165, 154, 0.6);
  border-radius: 10px;
  color: rgba(30, 165, 154, 0.4);
  letter-spacing: 0.5px;
  font-size: 18px;
  line-height: 29px;
  display: inline-flex;
  justify-content: center;
  align-items: center;
}

</style>
