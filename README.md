Mgt Lazy Image Loader For Magento
====================================

## FEATURES
-----------------

There are many ways to improve the performance of your magento store. 
All shop owners will know that product images play an important part. 
However, there is one problem with this. 
The more images you have, the slower the site loads and utilizes more bandwidth. 
A very good solution to this is to load your images on demand, or what is most commonly known as lazy loading.

Conclusion
Lazy loading is a additional way to improve the page's loading time and overall performance. 
You only need 1-2 minutes to install this magento extension.

## MORE INFORMATION

[http://www.mgt-commerce.com/magento-lazy-load-images.html](http://www.mgt-commerce.com/magento-lazy-load-images.html)

## INSTALLATION
-----------------

1. Extract zip archive and copy contents to the app/folder of your Magento installation
2. Open the file "app/design/frontend/default/default/catalog/product/list.phtml"

search for

<pre>
<code>
 &lt;img src="<?php echo $this->helper('catalog/image')->init($_product, 'small_image')->resize(135); ?>"
 width="135" height="135" alt="<?php echo $this->stripTags($this->getImageLabel($_product, 'small_image'), null, true) ?>" /&gt;
</code>
</pre>

replace with
<pre>
<code>
&lt;img class="lazy" src="<?php echo $this->getSkinUrl('images/mgt_lazy_image_loader/loader.gif'); ?>" data-src="<?php echo $this->helper('catalog/image')->init($_product, 'small_image')->resize(135); ?>" width="135" height="135" alt="<?php echo $this->stripTags($this->getImageLabel($_product, 'small_image'), null, true) ?>" /&gt;
  </cody>
</pre>
    
3. Clear the cache in Admin > System > Cache Management

## CHANGELOG

1.0.4

* Add newest jquery version
* Change namespace to Mgt

1.0.3

* Fixed typo in template

1.0.1

* Add lazy loading in catalog search results

1.0.0

* Fix typo
