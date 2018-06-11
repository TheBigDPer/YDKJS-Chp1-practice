# YDKJS-Chp1-practice

var TAX_RATE = 0.10;
var PHONE_PRICE = 5.00;
var ACCESSORY_PRICE = 1.00;
var SPENDING_THRESHOLD = 25.00;

var bankAccountBalance = 100.00;

var purchaseAmount = 0.00;

function calculateTax (amt) {
amt = (amt * TAX_RATE) + amt;
return amt;
}

function formatAmount (amt) {
return "$" + amt.toFixed(2);
}

function printAmount (amt) {
console.log(amt);
}


for (bankAccountBalance; purchaseAmount < bankAccountBalance; bankAccountBalance - purchaseAmount) {
purchaseAmount = purchaseAmount + PHONE_PRICE;
if (purchaseAmount < SPENDING_THRESHOLD) {
purchaseAmount = purchaseAmount + ACCESSORY_PRICE;
};

purchaseAmount = calculateTax(purchaseAmount);
formatAmount(purchaseAmount);
printAmount(purchaseAmount);
}
