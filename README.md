# inventory-Item
function createInventoryItem(name, category, price) {  
    return {  
  name: name,  
  category: category,  
  price: price,  
  describeItem: function() {  
  console.log(`Item Name: ${this.name}, Category: ${this.category}, Price: $${this.price}`);  
  },  
  addItemDiscount: function(discountPercent) {  
  this.discountedPrice = this.price - (this.price * (discountPercent / 100));  
  },  
  applyDiscount: function() {  
  console.log(`Discounted Price: $${this.discountedPrice.toFixed(2)}`);  
}  
};  
}  
const item = createInventoryItem("Laptop", "Electronics", 1000);  
item.describeItem();   
item.addItemDiscount(10);  
item.applyDiscount(); 
