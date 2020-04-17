# use_models_inside_template (phtml)

Lets not use object manager in template or anywhere but easiest way to get object reference of any class is:

<?php $mergedCells = ($this->helper(Magento\Tax\Helper\Data::class)->displayCartBothPrices() ? 2 : 1); ?>

for getting checkout session:
$checkoutSession = $this->helper(Magento\Checkout\Helper\Data::class)->getCheckout();

same goes for cart, customer and all other class files

$object = $this->helper(vendor\modulename\Helper\Data::class)->function();

Helper class provides objects for all types of classes.
