# add

      {% comment %}
        <!--  Polishing Packaging products code start  -->

            {% if product.metafields.custom.polishing_cloth != blank %}
            {% assign products = product.metafields.custom.polishing_cloth.value %}
         {%- for product in products -%}
              <div class="question_custom_gift">
            <input type="checkbox"  class="polishing_cloth" value="{{ product.variants.first.id}}">
            <label for="vehicle1">Add Polishing cloth</label>
              </div>  
            {% endfor %}
                 <div class="custom_product_meta" style="display:none;">
                <h3 class="complementary_section_title">{{ section.settings.heading_custom }}<span>
              <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" 
              width="40" zoomAndPan="magnify" viewBox="0 0 30 30.000001" height="40" preserveAspectRatio="xMidYMid meet" 
              version="1.0"><defs><clipPath id="id1">
           <path d="M 2.847656 4.792969 L 26.796875 4.792969 L 26.796875 24.390625 L 2.847656 24.390625 Z M 2.847656 4.792969 " clip-rule="nonzero"/></clipPath></defs><g clip-path="url(#id1)"><path fill="rgb(0%, 0%, 0%)" d="M 11.078125 24.3125 L 2.847656 15.890625 L 6.128906 12.53125 L 11.078125 17.597656 L 23.519531 4.875 L 26.796875 8.230469 Z M 11.078125 24.3125 " fill-opacity="1" fill-rule="nonzero"/></g></svg></span></h3>
              <ul class="complementey_slider">
        {%- for product in products -%}
          <li class="meta_product_item" item_id="{{ product.id }}">
            <div class="content-all-customm">
            <div class="meta_container">
              <div class="image-left">
          {% if product.featured_image != blank %}
              <div class="meta-item-image">
              <img src="{{ product.featured_image | img_url:'87x87' }}" meta_id ="{{ product.variants.id }}" alt="" loading="lazy" width="100" height="100">
              </div>
            {% endif %}
              </div>
              <div class="info-right">
              <div class="meta-item-title">{{ product.title }}</div>  
             <div class="meta-item-price">
               {% if product.compare_at_price_min > product.price %}<span>{{ product.compare_at_price_min  | money_with_currency }}</span>{% endif %}{{ product.price | money_with_currency }}
             </div> 
            </div>
              
            </div>
            </div>
              </li>
          {%- endfor -%}
              </ul>
                </div>
                 {% endif %}
            <!--  Polishing Packaging products code end  -->

            <!--  Gift Packaging products code start  -->
            
            {% if product.metafields.custom.gift_wrap != blank %}
            {% assign productss = product.metafields.custom.gift_wrap.value %}
         {%- for productt in productss -%}
              <div class="question_custom_gifts">
            <input type="checkbox" class="gift_cart" value="{{ productt.variants.first.id}}">
            <label for="vehicle1">Add Gift Card</label>
              </div>  
            {% endfor %}
                 <div class="custom_product_metas" style="display:none;">
                <h3 class="complementary_section_title">Gift Card Added<span>
              <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" 
              width="40" zoomAndPan="magnify" viewBox="0 0 30 30.000001" height="40" preserveAspectRatio="xMidYMid meet" 
              version="1.0"><defs><clipPath id="id1">
           <path d="M 2.847656 4.792969 L 26.796875 4.792969 L 26.796875 24.390625 L 2.847656 24.390625 Z M 2.847656 4.792969 " clip-rule="nonzero"/></clipPath></defs><g clip-path="url(#id1)"><path fill="rgb(0%, 0%, 0%)" d="M 11.078125 24.3125 L 2.847656 15.890625 L 6.128906 12.53125 L 11.078125 17.597656 L 23.519531 4.875 L 26.796875 8.230469 Z M 11.078125 24.3125 " fill-opacity="1" fill-rule="nonzero"/></g></svg></span></h3>
              <ul class="complementey_slider">
        {%- for productt in productss -%}
          <li class="meta_product_item" item_id="{{ productt.id }}">
            <div class="content-all-customm">
            <div class="meta_container">
              <div class="image-left">
          {% if productt.featured_image != blank %}
              <div class="meta-item-image">
              <img src="{{ productt.featured_image | img_url:'87x87' }}" meta_id ="{{ productt.variants.id }}" alt="" loading="lazy" width="100" height="100">
              </div>
            {% endif %}
              </div>
              <div class="info-right">
              <div class="meta-item-title">{{ productt.title }}</div>  
             <div class="meta-item-price">
               {% if productt.compare_at_price_min > productt.price %}<span>{{ productt.compare_at_price_min  | money_with_currency }}</span>{% endif %}{{ productt.price | money_with_currency }}
             </div> 
            </div>
              
            </div>
            </div>
              </li>
          {%- endfor -%}
              </ul>
                </div>
                 {% endif %}
            <!--  Gift Packaging products code end  -->
            {% endcomment %}


            --------------------js--------------------------------



            $(document).ready(function(){
$('.testemonial-slider').slick({
  dots: false,
arrows: true,
  infinite: true,
  speed: 300,
  slidesToShow: 3,
  slidesToScroll: 1,
  centerMode: false,
     prevArrow:'<button class="slick-prev"><i class="fa fa-angle-left" aria-hidden="true"></i></button>',
  nextArrow:'<button class="slick-next"><i class="fa fa-angle-right" aria-hidden="true"></i></button>',
  responsive: [
    {
      breakpoint: 1024,
      settings: {
        slidesToShow: 2,
        slidesToScroll: 1,
        infinite: true,
        dots: true
      }
    },
    {
      breakpoint: 768,
      settings: {
        slidesToShow: 2,
        slidesToScroll: 1
      }
    },
    {
      breakpoint: 600,
      settings: {
        slidesToShow: 1,
        slidesToScroll: 1
      }
    },
    {
      breakpoint: 480,
      settings: {
        slidesToShow: 1,
        slidesToScroll: 1
      }
    }
    // You can unslick at a given breakpoint now by adding:
    // settings: "unslick"
    // instead of a settings object
  ]
});

// collection page
  $(document).on("click",".produts-listingg",function() {
    // alert('gttg');
   $("ul#product-grid").removeClass("product-grid grid--2-col-tablet-down grid--3-col-desktop");
    $("ul#product-grid").addClass("grid--2-col-tablet-down grid--2-col-desktop list-view");
   $(".product-desctription-custom").addClass("showing");
  });
 $(document).on("click",".produts-blockk",function() {
   // alert('test');
    $("ul#product-grid").removeClass("grid--2-col-tablet-down grid--2-col-desktop list-view");
    $("ul#product-grid").addClass("product-grid grid--2-col-tablet-down grid--3-col-desktop");
    $(".product-desctription-custom.showing").removeClass("showing");
  });
  $(".col-toggle").click(function () {
    $(".col-toggle").removeClass("active");
     $(this).addClass("active");  
});

  //product page vertical slider
    $(".vertical_slider").slick({
           slidesToShow: 7,
  slidesToScroll: 7,
            infinite: false,
            vertical: true,
            verticalSwiping: true,
            arrows: true,
            swipeToSlide: true,
            focusOnSelect: true,
          prevArrow:'<button class="slick-prev">More Pics<i class="fa fa-angle-up" aria-hidden="true"></i></button>',
  nextArrow:'<button class="slick-next">More Pics<i class="fa fa-angle-down" aria-hidden="true"></i></button>',
        });
  //price append product


 // Product page gift warraping js
  $(document).on("click", ".question_custom_gift", function(e) {
       var checked = $(this).find("input:checkbox").is(":checked");
       if (checked) {
         // show gift packing product
          $('.custom_product_meta').show(200);
         // get product id
          var pr_ID = $('input:checkbox').attr('value');
         // add product on cart
//          $(document).one("click", ".custom_cart_btnn", function() {
//            alert('testing');
//            var count = $('.cart-count-bubble span').html();
//            // alert(count);
//           setTimeout(function() {
//            $.ajax({ 
//           type: 'POST',
//           url: '/cart/add.js',
//           data: {
//           quantity:1,
//           id: pr_ID
//            },
//          dataType: 'json',
//          success: function() {
//          // alert('Gift Packaing Added');
        
//       }
//       });
// }, 2500);
//          });
         
       } else {
         
           $('.custom_product_meta').hide(200);
       }
    });

   // Product page gift warraping js
  $(document).on("click", ".question_custom_gifts", function(e) {
       var checked = $(this).find("input:checkbox").is(":checked");
       if (checked) {
         // show gift packing product
          $('.custom_product_metas').show(200);
         // get product id
          var pr_ID = $('input:checkbox').attr('value');
         // add product on cart
//          $(document).one("click", ".custom_cart_btnns", function() {
//            var count = $('.cart-count-bubble span').html();
//            // alert(count);
//           setTimeout(function() {
//            $.ajax({ 
//           type: 'POST',
//           url: '/cart/add.js',
//           data: {
//           quantity:1,
//           id: pr_ID
//            },
//          dataType: 'json',
//          success: function() {
//          // alert('Gift Packaing Added');
        
//       }
//       });
// }, 1500);
//          });
         
       } else {
         
           $('.custom_product_metas').hide(200);
       }
    });


     $('input.polishing_cloth').click(function(){
            if($(this).prop("checked") == true){
                console.log("Checkbox is checked.");
                var product_id = $(this).val();
                console.log('product_id',product_id);
               $.ajax({ 
              type: 'POST',
              url: '/cart/add.js',
              data: {
              quantity:1,
              id: product_id
               },
             dataType: 'json',
             success: function() {
            console.log('success');
            
          }
          });
            }
            else if($(this).prop("checked") == false){
                console.log("Checkbox is unchecked.");

                var product_id = $(this).val();
    console.log('product_id',product_id);

 var quantity = 1;
  quantity = quantity-1;
  var params = {
    type: 'POST',
    url: '/cart/change.js',
    data: 'quantity=' + quantity + '&id=' + product_id,
    dataType: 'json',
    success: function(line_item) {
        console.log('ok cart remove');
      if ((typeof callback) === 'function') {
        callback(line_item);
      }
      else {
        Shopify.cartPopap(product_id);
        Shopify.onItemAdded(line_item);
      }
    },
    error: function(XMLHttpRequest, textStatus) {
      Shopify.onError(XMLHttpRequest, textStatus);
    }
  };
  jQuery.ajax(params);
            }
        });




           $('input.gift_cart').click(function(){
            if($(this).prop("checked") == true){
                console.log("Checkbox is checked.");
                var product_id = $(this).val();
    console.log('product_id',product_id);
               $.ajax({ 
          type: 'POST',
          url: '/cart/add.js',
          data: {
          quantity:1,
          id: product_id
           },
         dataType: 'json',
         success: function() {
        console.log('success');
        
      }
      });
            }
            else if($(this).prop("checked") == false){
                console.log("Checkbox is unchecked.");
                var product_id = $(this).val();
    console.log('product_id',product_id);

 var quantity = 1;
  quantity = quantity-1;
  var params = {
    type: 'POST',
    url: '/cart/change.js',
    data: 'quantity=' + quantity + '&id=' + product_id,
    dataType: 'json',
    success: function(line_item) {
        console.log('ok cart remove');
      if ((typeof callback) === 'function') {
        callback(line_item);
      }
      else {
        Shopify.cartPopap(product_id);
        Shopify.onItemAdded(line_item);
      }
    },
    error: function(XMLHttpRequest, textStatus) {
      Shopify.onError(XMLHttpRequest, textStatus);
    }
  };
  jQuery.ajax(params);
            }
        });
  
});




