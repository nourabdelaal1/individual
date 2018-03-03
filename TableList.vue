<template>
    <div class="row">
      <div class="col-md-12">
        <div class="card">
          <paper-table :title="table1.title" :sub-title="table1.subTitle" :data="table1.data" :columns="table1.columns">
                    </paper-table>
                  </div>
                  <div class="topnav">
</div>
<form role="form" class="" @submit.prevent="createProduct">
            <div align="center" style="max-width:400px" class="form-group">
                <br>
                <v-card class="grey lighten-4 elevation-0">
                  <v-card-text>
                    <v-container fluid>
                     <v-layout row>
                        <v-flex xs4>

                        </v-flex>
                        <v-flex xs8 style="margin:auto;max-width:100%">
                          <v-text-field
                            name="product"
                            label=" product"
                            class="input-group--focused"
                            placeholder=""
                            v-validate="{ rules: { required: true} }"
                            type="text"
                            v-model="name"
                            required='true'
                            id=""
                          ></v-text-field>
                        </v-flex>
                      </v-layout>
                      </v-container>
                  </v-card-text>
                </v-card>


                </div>

            <div>

                <div style="max-width:400px">
                    <button class="btn btn-primary btn-sm" style="height:50px">Create Product</button>
                </div>
            </div>
        </form>
<label for="promo-code">Search your Products Here</label>
<input type="text" placeholder="Search Here..">
<div>
  <button class="Update">
            <center>Search Product</center>
            </button>
            <div id = "app">
            <v-header></v-header>
            <v-button></v-button>
            </div>
            <div class="topnav">
  <input type="text"v-model ="name" placeholder="Name Here..">

<input type="text"v-model ="price" placeholder="Price Here..">

<input type="text"v-model ="createdAt" placeholder="Created at..">

<input type="text"v-model ="updatedAt" placeholder="Updated at..">
</div>
       <button addclick="createProduct()">Add</button>
       <button addclick="createProduct()">Delete</button>
       <button addclick="createProduct()">Update</button>
      </div>

                </div>


                        <div class="summary-delivery">
                          <select name="delivery-collection" class="summary-delivery-selection">
                             <option value="0" selected="selected">Nike Shoes Air Force</option>
                             <option value="collection">New Balance</option>
                             <option value="first-class">Adidas Super Star</option>
                          </select>
                        </div>
                      <html lang="en">

<head>
  <meta charset="utf-8">
  <meta http-equiv="x-ua-compatible" content="ie=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Basket</title>
</head>

<body>
  <main>
    <div class="basket">
      <div class="basket-module">
        <label for="promo-code">Enter a promotional code</label>
        <input id="promo-code" type="text" name="promo-code" maxlength="5" class="promo-code-field">
        <button class="promo-code-cta">Apply</button>
      </div>
      <div class="basket-product">
        <div class="item">
          <div class="product-image">
            <img src="http://nb.scene7.com/is/image/NB/ml574egb_nb_02_i?$dw_pgp_hd$" alt="Placholder Image 2" class="product-frame">
          </div>
          <div class="product-details">
            <h1><strong><span class="item-quantity"></span> New Balance </strong> Maroon</h1>
            <p><strong>Navy, Size 7.5</strong></p>
            <p>Product Code - 232321939</p>
          </div>
        </div>
        <div class="price">$50.60</div>
        <div class="quantity">

        </div>
        <div class="subtotal"></div>
        <input type="text" placeholder="Enter Quantity..">
        <div class="remove">
          <button>Remove</button>
        </div>
      </div>

      <div class="basket-product">
        <div class="item">
          <div class="product-image">
            <img src="https://images-na.ssl-images-amazon.com/images/I/714v5CiuL9L._UX395_.jpg" alt="Placholder Image 2" class="product-frame">
          </div>
          <div class="product-details">
            <h1><strong><span class="item-quantity"></span> Nike</strong> Air Force</h1>
            <p><strong>Navy, Size 10</strong></p>
            <p>Product Code - 232321939</p>
          </div>
        </div>
        <div class="quantity">
        </div>
        <div class="subtotal">50.60</div>
        <input type="text" placeholder="Enter Quantity..">
        <div class="remove">
          <button>Remove</button>
        </div>
      </div>
    </div>
    <aside>
      <div class="summary">
        <div class="summary-total-items"><span class="total-items"></span> Items in your Bag</div>
        <div class="summary-subtotal">
          <div class="subtotal-title">Subtotal</div>
          <div class="subtotal-value final-value" id="basket-subtotal">130.00</div>
          <div class="summary-promo hide">
            <div class="promo-title">Promotion</div>
            <div class="promo-value final-value" id="basket-promo"></div>
          </div>
        </div>
        <div class="summary-delivery">
          <select name="delivery-collection" class="summary-delivery-selection">
              <option value="0" selected="selected">Credit Card</option>
             <option value="collection">Cash on Delivery</option>

          </select>
        </div>
        <div class="summary-total">
          <div class="total-title">Total</div>
          <div class="total-value final-value" id="basket-total">130.00</div>
        </div>
        <div class="summary-checkout">
          <button class="checkout-cta">Go to Secure Checkout</button>
        </div>
      </div>
    </aside>
  </main>
</body>

</html>
    </div>
</template>
<script>
  import PaperTable from 'components/UIComponents/PaperTable.vue'
  import axios from 'axios'

  const tableColumns = ['Id', 'Name', 'Price', 'CreatedAt', 'UpdatedAt', 'SellerName']
  const tableData = [{
    id: 1,
    name: 'Nike Shoes"Air Force"',
    price: '$55.00',
    createdat: '15/2/2018',
    updatedat: '16/2/2018',
    sellername: 'Nour'
  },
  {
    id: 2,
    name: 'New Balance',
    price: '$50.60',
    createdat: '15/2/2018',
    updatedat: '16/2/2018',
    sellername: 'Nour'
  },
  {
    id: 3,
    name: 'Adidas "Super Star"',
    price: '$40.00',
    createdat: '3/2/2018',
    updatedat: '3/2/2018',
    sellername: 'Nour'

  }
  ]

  export default {

    components: {
      PaperTable
    },
    data () {
      return {
        table1: {
          title: 'Store',
          subTitle: 'A list of products',
          columns: [...tableColumns],
          data: [...tableData]
        },
        table2: {
          title: 'Table on Plain Background',
          subTitle: 'Here is a subtitle for this table',
          columns: [...tableColumns],
          data: [...tableData]
        },
        name: '',
        price: '',
        createdAt: '',
        updatedAt: ''
      }
    },
    methods: {
      createProduct: function () {
        console.log(this.name)
        console.log(this.price)
        console.log(this.createdAt)
        console.log(this.updatedAt)
        axios.post('localhost:3000/api/product/createProduct',
          {
            'name': this.name,
            'price': this.price,
            'createdAt': this.createdAt,
            'updatedAt': this.updatedAt
          })
  .then(response => {})
  .catch(e => {
  })
      }
    }
  }
</script>
<style>

</style>
