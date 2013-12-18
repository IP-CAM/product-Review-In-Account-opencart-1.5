# H1 comments2products
=================

Module for opencart 1.5 sho comments for product in customer account page

Update catalog/controller/product/product.php
For fast add First and Last name
 add:
     $firstname = $this->customer->getFirstName();
     $lastname = $this->customer->getLastName();
     $this->data['FirstName'] = isset($firstname)?$firstname:'';
     $this->data['LastName'] = isset($lastname)?$lastname:'';
     
Somewere near line 280
Also need update the views
catalog/view/theme/default/template/product/product.tpl

*found* -
`<input type="text" name="name" value="" />`--

*replace* with -
`<input type="text" name="name" value="<?php echo $FirstName.' '.$LastName; ?>" />`
