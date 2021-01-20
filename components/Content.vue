<template>
  <div>
    <content1 class="bg-gray-300 flex pt-0">
      <div
        class="container md:flex md:items-center md:justify-between mx-auto px-4 pt-3 space-x-4"
      >
        <!-- <h1 class="mb-4 md:mb-0 text-2xl">logo here</h1> -->
        <div class="mb-3 pt-0 pl-4">
          <input
            type="text"
            placeholder="Placeholder1"
            class="px-3 py-3 placeholder-gray-400 text-gray-700 relative bg-white bg-white rounded text-sm shadow outline-none focus:outline-none focus:shadow-outline w-full"
          />
        </div>
        <div class="mb-3 pt-0">
          <input
            type="text"
            placeholder="Placeholder2"
            class="px-3 py-3 placeholder-gray-400 text-gray-700 relative bg-white bg-white rounded text-sm shadow outline-none focus:outline-none focus:shadow-outline w-full"
          />
        </div>
        <div class="mb-3 pt-0">
          <input
            type="text"
            placeholder="Placeholder3"
            class="px-3 py-3 placeholder-gray-400 text-gray-700 relative bg-white bg-white rounded text-sm shadow outline-none focus:outline-none focus:shadow-outline w-full"
          />
        </div>
        <div class="mb-3 pt-0">
          <input
            type="text"
            placeholder="Placeholder4"
            class="px-3 py-3 placeholder-gray-400 text-gray-700 relative bg-white bg-white rounded text-sm shadow outline-none focus:outline-none focus:shadow-outline w-full"
          />
        </div>
        <div class="mb-3 pt-0">
          <input
            type="text"
            placeholder="Placeholder5"
            class="px-3 py-3 placeholder-gray-400 text-gray-700 relative bg-white bg-white rounded text-sm shadow outline-none focus:outline-none focus:shadow-outline w-full"
          />
        </div>
        <div class="mb-3 pt-0">
          <input
            type="text"
            placeholder="Placeholder6"
            class="px-3 py-3 placeholder-gray-400 text-gray-700 relative bg-white bg-white rounded text-sm shadow outline-none focus:outline-none focus:shadow-outline w-full"
          />
        </div>
      </div>
    </content1>
    <!-- <content2 class=" bg-gray-300" style="flex">
      <div class="flex">
        <div class="flex-1 ...">1</div>
        <div class="contents">
          <div class="flex-1 ...">2</div>
          <div class="flex-1 ...">3</div>
        </div>
        <div class="flex-1 ...">4</div>
      </div>
    </content2> -->
    <!-- <content3 class="grid grid-cols-4 grid-rows-6">
      <v-card>
        <v-card-title>
          Food Data
          <v-spacer></v-spacer>
          <v-text-field
            v-model="search"
            append-icon="mdi-magnify"
            label="Search"
            single-line
            hide-details
          ></v-text-field>
        </v-card-title>
        <v-data-table
          :headers="headers"
          :items="food"
          :search="search"
        ></v-data-table>
      </v-card>
    </content3> -->
    <content2>
      <v-simple-table>
        <template v-slot:default>
          <thead>
            <tr>
              <th class="text-left">Name</th>
              <th class="text-left">Calories</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="food in FOOD" :key="food.name">
              <td>{{ food.name }}</td>
              <td>{{ food.calories }}</td>
            </tr>
          </tbody>
        </template>
      </v-simple-table>
    </content2>
  </div>
</template>

<script>
export default {
  data() {
    return {
      FOOD: [
        {
          name: 'Burger',
          calories: 660,
        },
        {
          name: 'Sandwich',
          calories: 660,
        },
        {
          name: 'Cheese Whopper',
          calories: 790,
        },
        {
          name: 'Bacon King',
          calories: 1150,
        },
        {
          name: 'Farmhouse',
          calories: 1220,
        },
        {
          name: 'Grilled Chicken',
          calories: 470,
        },
        {
          name: 'Snickers Pie',
          calories: 300,
        },
        {
          name: 'Veggie Burger',
          calories: 390,
        },
        {
          name: 'Donut',
          calories: 500,
        },
        {
          name: 'Grilled Hot Dog',
          calories: 310,
        },
        {
          name: 'French Fry',
          calories: 380,
        },
      ],
    }
  },
}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
@apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/

/* .container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
} */
</style>
