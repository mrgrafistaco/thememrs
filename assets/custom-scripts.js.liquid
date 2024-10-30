
  // const priceSelectorDesktop = '.cart-item__totals.right.small-hide';
  const priceSelectorDesktop = 'td.cart-item__totals.right.small-hide > div.cart-item__price-wrapper > span';
  const priceSelectorMobile = 'td.cart-item__totals.right.medium-hide.large-up-hide > div.cart-item__price-wrapper > span';
  const subTotalSelector = '#main-cart-footer > div > div > div > div.js-contents > div.totals > p';

  // update totla as quantity changes
  document.addEventListener('DOMContentLoaded', () => {
      document.querySelectorAll('[id*="CartItem-"]').forEach((cartItem, index) => {
          cartItem.querySelector('.quantity__input').addEventListener('change', async (e) => {

              // hide price until update is complete
              cartItem.querySelector(priceSelectorDesktop).classList.add('isNotVisible');
              cartItem.querySelector(priceSelectorMobile).classList.add('isNotVisible');

              const newQuantity = cartItem.querySelector('.quantity__input').value;
              console.log({newQuantity});
              console.log('quantity changed');
              console.log({index});

              // get line item key
              const key = cartItem.querySelector('.quantity__input').getAttribute('data-line-item-key');
              console.log({key});

              // Ajax update
              const cartUpdateResponse = await fetch('/cart/update.js', {
                  method: 'post',
                  headers: {
                      Accept: 'application/json',
                      'Content-Type': 'application/json',
                  },
                  body: JSON.stringify({ updates: { [key]: newQuantity} }), // update quantity
              });

              const json = await cartUpdateResponse.json();
              console.log({json});

              // const res = await fetch('/?section_id=main-cart-items');
              const res = await fetch('/cart');
              if(!res.ok) {
                  console.log('could not fetch');
              }
              const text = await res.text();

              const html = document.createElement('div');
              html.innerHTML = text;

              // update cart line items
              const priceContainerDesktop = html.querySelectorAll(priceSelectorDesktop);
              if (priceContainerDesktop && priceContainerDesktop.length > 0) {
                  const updatedPriceDesktop = priceContainerDesktop[index].innerHTML;
                  if(cartItem.querySelector(priceSelectorDesktop)) {
                      cartItem.querySelector(priceSelectorDesktop).classList.remove('isNotVisible');
                      cartItem.querySelector(priceSelectorDesktop).innerHTML = updatedPriceDesktop;  
                  } 
              }

              const priceContainerMobile = html.querySelectorAll(priceSelectorMobile);
              if (priceContainerMobile && priceContainerMobile.length > 0) {
                  const updatedPriceMobile = priceContainerMobile[index].innerHTML;
                  if(cartItem.querySelector(priceSelectorMobile)) {
                      cartItem.querySelector(priceSelectorMobile).classList.remove('isNotVisible');
                      cartItem.querySelector(priceSelectorMobile).innerHTML = updatedPriceMobile;  
                  } 
              }

              // update cart subtotal
              const subTotalContainer = document.querySelector(subTotalSelector);
              document.querySelector(subTotalSelector).innerHTML = html.querySelector(subTotalSelector).innerHTML;
          })
      });

  });
