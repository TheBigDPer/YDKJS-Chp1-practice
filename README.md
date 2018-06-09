# YDKJS-Chp1-practice

var TAX_RATE = 0.10;
var PHONE_PRICE = 5.00;
var ACCESSORY_PRICE = 1.00;
var SPENDING_THRESHOLD = 25.00;

var bankAccountBalance = 100.00;

var purchaseAmount

function calculateTax (amt) {
amt = amt + TAX_RATE;
return amt;
}

function formatAmount (amt) {
return "$" + amt.toFixed(2);
}


while (bankAccountBalance > 0) {
purchaseAmount = purchaseAmount + PHONE_PRICE;
if (purchaseAmount < SPENDING_THRESHOLD) {
purchaseAmount = purchaseAmount + ACCESSORY_PRICE;
};
purchaseAmount = calculateTax(purchaseAmount);
bankAccountBalance = bankAccountBalance - purchaseAmount;
if (bankAccountBalance == 0) {
return formatAmount(purchaseAmount);
};
}
