<template>
	<div id='contacts'>
		<ul>
			<li v-for="contact in contacts" v-on:click="contact.show =!contact.show">
				<div class="card">
		      <div class="row">
		        <div class="col-2">
		          <!-- <div>
		            <img class="image":src="img" alt="Profile" height="90" width="90">
		          </div> -->
		        </div>
		        <div class="col-10">
		          <div><p class="name">{{ contact.name }}</p></div>
		          <div class="address"><span>{{ contact.streetAddress }}<br/>{{contact.city}}, {{contact.state}} {{contact.zipCode}}</span></div>
		          <div class="number"><span>{{contact.phoneNumber}}</span></div>
		          <div class="email"><span>{{ contact.email }}</span></div>
		          <div v-show="contact.show">
		          	<ul>
		          		<li class="comonality" v-for="comonality in contact.commonalities">{{comonality}}</li>
		          	</ul>
		          </div>
		        </div>
		      </div>
		    </div>
			</li>
		</ul>
	</div>

</template>

<script>
export default {

  data () {
    return {
    	contacts:[
		{
			"name" : "Contact 1",
			"streetAddress" : "123 1st Ave.",
			"city": "Lexington",
			"state" : "KY",
			"zipCode" : "40515",
			"phoneNumber" : "(859) 234-5433",
			"email" : "contact1@mail.com",
			"show" : false,
			"commonalities" : [
				"Sports",
				"Cars",
				"Kentucky Basketball"
			]
		},
		{
			"name" : "Contact 2",
			"streetAddress" : "123 2nd Ave.",
			"city": "Lexington",
			"state" : "KY",
			"zipCode" : "40515",
			"phoneNumber" : "(859) 154-7986",
			"email" : "contact2@mail.com",
			"show" : false,
			"commonalities" : [
				"Fantasy Football",
				"Music",
				"Word working"
			]			
		},
		{
			"name" : "Contact 3",
			"streetAddress" : "890 Hover St.",
			"city": "Fargo",
			"state" : "ND",
			"zipCode" : "58402",
			"phoneNumber" : "(701) 276-2301",
			"email" : "contact3@mail.com",
			"show" : false,
			"commonalities" : [
				"Weighlifting",
				"Minnesota Vikings",
				"Ice Fishing"
			]
		},
		{
			"name" : "Contact 4",
			"streetAddress" : "27 1st St.",
			"city": "Norman",
			"state" : "OK",
			"zipCode" : "70415",
			"phoneNumber" : "(605) 546-1984",
			"email" : "contact4@mail.com",
			"show" : false,
			"commonalities" : [
				"Oklahoma Football",
				"Kite Flying",
				"Golf"
			]
		},
		{
			"name" : "Contact 5",
			"streetAddress" : "7644 147th St.",
			"city": "New York",
			"state" : "NY",
			"zipCode" : "10013",
			"phoneNumber" : "(917) 989-2316",
			"email" : "contact5@mail.com",
			"show" : false,
			"commonalities" : [
				"Tennis",
				"Food"
			]
		},
		{
			"name" : "Contact 6",
			"streetAddress" : "456 Waylan Blvd.",
			"city": "Chicago",
			"state" : "IL",
			"zipCode" : "60067",
			"phoneNumber" : "(773) 962-4978",
			"email" : "contact6@mail.com",
			"show" : false,
			"commonalities" : [
				"Wind",
				"Complaining about the weather"
			]
		},
		{
			"name" : "Contact 7",
			"streetAddress" : "654 Mesedona Way.",
			"city": "San Diego",
			"state" : "CA",
			"zipCode" : "92029",
			"phoneNumber" : "(858) 173-6490",
			"email" : "contact7@mail.com",
			"show" : false,
			"commonalities" : [
				"Beaches",
				"Vacationing"
			]
		},
		{
			"name" : "Contact 8",
			"streetAddress" : "23 Beaumont St.",
			"city": "Las Vegas",
			"state" : "NV",
			"zipCode" : "10013",
			"phoneNumber" : "(702)473-5400",
			"email" : "contact8@mail.com",
			"show" : false,
			"commonalities" : [
				"Gambling",
				"Blue Man Group"
			]
		},
		{
			"name" : "Contact 9",
			"streetAddress" : "4528 Kirby Puckett Pl.",
			"city": "Minneapolis",
			"state" : "MN",
			"zipCode" : "55408",
			"phoneNumber" : "(613) 459-2006",
			"email" : "contact9@mail.com",
			"show" : false,
			"commonalities" : [
				"Minnesota Twins",
				"Baseball Stadiums"
			]
		},
		{
			"name" : "Contact 10",
			"streetAddress" : "243 1st Ave N.",
			"city": "Streeter",
			"state" : "ND",
			"zipCode" : "58483",
			"phoneNumber" : "(701) 424-3317",
			"email" : "contact10@mail.com",
			"show" : false,
			"commonalities" : [
				"Small Towns",
				"History"
			]
		}
	]

    }
  }
}
</script>

<style scoped>
#contacts{
	width: 100%;
	max-width: 1200px;
	margin-top: 40px auto;
	padding:0 20px;
	box-sizing:border-box;
}

/*.card {
  position: absolute;
  border: solid 1px #000;
  height: 100px;
  width: 280px;
  border-radius: 4px;
  margin:5px;
}*/
.image {
  border: solid 1px #ccc;
  height: 90px;
  width: 90px;
  margin: 3px 10px;
  font-size: 12px;
  text-align: center;
  border-radius: 4px;
  background-color: #eee;
}
.name{
  /*width: 200px;
  height: 18px;*/
  margin: 3px 20px;
  font-size: 32px;
  font-weight: 600;
  text-align: center;
}
.address{
/*  width: 200px;
  height: 30px;*/
  margin: 4px 20px;
  font-size: 12px;
  text-align: center;
}
.number {
 /* width: 200px;
  height: 14px;*/
  margin: 3px 20px;
  font-size: 14px;
  font-weight: 600;
  text-align: center;
}
.email{
  /*width: 200px;
  height: 30px;*/
  margin: 3px 20px;
  font-size: 14px;
  text-align: center;
}
ul{
	display: flex;
	flex-wrap: wrap;
	list-style-type: none;
	padding: 0;
}
li{
	flex-grow:2;
	flex-basis: 220px;
	text-align: center;
	padding: 30px;
	border: 1px solid #222;
	margin:50px;
}
li .comonality{
	text-shadow: 1px 2px #ccc;
	text-align: center;
	padding: 0px;
	border: none;
	margin:0px;
}
</style>
