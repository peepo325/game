<template>
<div id="Select">

    <button @click="random">
        Start
    </button>

</div>
</template>

<script>
export default {
    data: function () {
        return {
            player: [{
                    name: 'Batman',
                    hp: 106,
                    image: 'https://www.google.com/url?sa=i&url=https%3A%2F%2Ftoppng.com%2Fbatman-new-52-PNG-free-PNG-Images_193405&psig=AOvVaw3JQm8ZBUX6sz5cBjAiuIhf&ust=1598675533189000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCOD4gdGIvesCFQAAAAAdAAAAABAD'
                },
                {
                    name: 'Batman',
                    hp: 106,
                    image: 'https://media1.tenor.com/images/49de17c6f21172b3abfaf5972fddf6d6/tenor.gif?itemid=10206784'
                },
                {
                    name: 'Superman',
                    hp: 120,
                    image: 'https://media1.tenor.com/images/2c38a3defb4c11e299defc216d0bc9a8/tenor.gif?itemid=11328655'
                },
                {
                    name: 'Green lantern',
                    hp: 110,
                    image: 'https://media1.tenor.com/images/cacb74825150659ec3c37d4f62c72e93/tenor.gif?itemid=8009868'
                },
                {
                    name: 'Aquaman',
                    hp: 129,
                    image: 'https://media1.tenor.com/images/94e2c69f155ef0f3dbc12c92e41ae707/tenor.gif?itemid=4884166'
                },
                {
                    name: 'Wonder Woman',
                    hp: 114,
                    image: 'https://media1.tenor.com/images/1d2edf4e8ea20b84279870923838203b/tenor.gif?itemid=10415980'
                },
                
            ],
            monster: [
                {
                    name: '',
                    hp: 140,
                    image: 'https://media2.giphy.com/media/hyBjcpooaAwuY/200.gif'
                },
                {
                    name: 'Joker',
                    hp: 140,
                    image: 'https://media1.tenor.com/images/b6a23f127d0e8307fee852b89869b6b4/tenor.gif?itemid=11637371'
                },
                {
                    name: 'Two face',
                    hp: 126,
                    image: 'https://media1.tenor.com/images/507d58a626fa15cb0b57e57f7a1cb873/tenor.gif?itemid=9698651'
                },
                {
                    name: 'The ridler',
                    hp: 110,
                    image: 'https://media.tenor.com/images/f16cdecdfa01b42dd350b6628550e211/tenor.gif'
                },
                {
                    name: 'Poison Ivy',
                    hp: 108,
                    image: 'https://media1.tenor.com/images/8412d29485948d3e7c99215f1b65b823/tenor.gif?itemid=13711257'
                },
                
                {
                    name: 'Harley quin',
                    hp: 134,
                    image: 'https://media1.tenor.com/images/2cbf1b4ac674b2834befd48a5c58a8b5/tenor.gif?itemid=9513434'
                },
                {
                    name:'Catwoman',
                    hp: 114,
                    image:'https://media1.tenor.com/images/4b37b5bd50929175e63eec3fdecd2628/tenor.gif?itemid=5262076'
                }
            ]
        }
    },
    methods: {
        pickName: function (n) {
            console.log("name :", this.player[n].name)
        },
        randomHero: function (min, max) {
            return Math.max(Math.floor(Math.random() * max) + 1, min)
        },
        random: function () {
            this.nH = this.randomHero(0, 5)
            this.nM = this.randomHero(0, 6)
            this.name_hero = this.player[this.nH].name //สุ่ม hero เก็บในตัวแปร ชื่อ
            this.hp_hero = this.player[this.nH].hp //สุ่ม hero เก็บในตัวแปร hp
            this.name_monster = this.monster[this.nM].name //สุ่ม moster เก็บในตัวแปร ชื่อ
            this.hp_monster = this.monster[this.nM].hp
            this.$emit("Heroname", this.name_hero)
            this.$emit("HeroHP", this.hp_hero)
            this.$emit("Monstername", this.name_monster)
            this.$emit("MonsterHP", this.hp_monster)
            console.log("name :", this.name_hero)
            console.log("hp :", this.hp_hero)
            console.log("name :", this.name_monster)
            console.log("hp :", this.hp_monster)
            this.imghero = this.player[this.nH].image
            this.imgmonster = this.monster[this.nM].image
            
            this.$emit("Imghero",this.imghero)
            this.$emit("Imgmonster",this.imgmonster)
          
        }
    },
}
</script>

<style>
</style>