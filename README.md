# Bulk-Image-Downloader
It is a JavaScript Code Snippet which also acts as extension into your browser.Just add the code Snippet into your browser's bookmark and give any name you want and save it.Now, whenever you will search any images into google's images section just click the bookmark and scroll the script will automatically select all the image's link and append one after the other in the popup in the right side bottom. You can unselect the image just by clicking it.     

![Screenshot (157)](https://user-images.githubusercontent.com/42734141/62005617-8f887f00-b153-11e9-85b4-0327b02a186a.png)


## Adding a bookmark
![Screenshot (158)](https://user-images.githubusercontent.com/42734141/62006216-4a684b00-b15b-11e9-871b-23dba4211074.png)

Add This Code in the area shown in the pic above.
```javascript

(function()%7B(function(e%2C%20s)%20%7Be.src%20%3D%20s%3Be.onload%20%3D%20function()%20%7BjQuery.noConflict()%3BjQuery('%3Cstyle%20type%3D%22text%2Fcss%22%3E%20.remove%20%7B%20opacity%3A0.3%3B%7D%5Cn%20.urlmodal%20%7Bpadding%3A%2010px%3B%20background-color%3A%20%23eee%3B%20position%3A%20fixed%3B%20bottom%3A%200%3B%20right%3A%200%3B%20height%3A%20100px%3B%20width%3A%20300px%3B%20z-index%3A%201000%3B%7D%20.urlmodal%20textarea%20%7Bwidth%3A%20100%25%3B%20height%3A%20250px%3B%7D%3C%2Fstyle%3E').appendTo('head')%3BjQuery('%3Cdiv%20class%3D%22urlmodal%22%3E%3Ch3%3ELet%5C's%20create%20a%20dataset%3C%2Fh3%3E%3Ctextarea%3EScoll%20all%20the%20way%20down%5CnClick%20%22Show%20more%20images%22%5CnScroll%20more%5CnClick%20on%20the%20images%20you%20want%20to%20remove%20from%20the%20dataset%5CnThe%20urls%20will%20appear%20in%20this%20box%20for%20you%20to%20copy.%3C%2Ftextarea%3E%3C%2Fdiv%3E').appendTo('body')%3BjQuery('%23rg').on('click'%2C%20'.rg_di'%2C%20function()%20%7BjQuery(this).toggleClass('remove')%3BupdateUrls()%3Breturn%20false%3B%7D)%3BjQuery(window).scroll(updateUrls)%3BjQuery('.urlmodal%20textarea').focus(function()%20%7BupdateUrls()%3B%20setTimeout(selectText%2C%20100)%7D).mouseup(function()%20%7Breturn%20false%3B%7D)%3Bfunction%20updateUrls()%20%7Bvar%20urls%20%3D%20Array.from(document.querySelectorAll('.rg_di%3Anot(.remove)%20.rg_meta')).map(el%3D%3EJSON.parse(el.textContent).ou)%3Bvar%20search_term%20%3D%20jQuery('.gsfi').val()%3BjQuery('.urlmodal%20textarea').val(urls.join(%22%5Cn%22))%3BjQuery('.urlmodal%20h3').html(search_term%20%2B%20%22%3A%20%22%20%2B%20urls.length)%3B%7Dfunction%20selectText()%20%7BjQuery('.urlmodal%20textarea').select()%3B%7D%7D%3Bdocument.head.appendChild(e)%3B%7D)(document.createElement('script')%2C%20'%2F%2Fcode.jquery.com%2Fjquery-latest.min.js')%7D)()
```

## Reference
Inspiration comes from this years[https://www.fast.ai/] course (v3). The course is available to the public since January 2019
 




