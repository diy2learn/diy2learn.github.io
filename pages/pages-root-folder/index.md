---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
header:
  image_fullwidth: header_unsplash_12.jpg
widget1:
  title: "Bababi"
  url: 'http://diy2learn.github.io/chamcon/blog/'
  image: widget1_papapi_babyOnRose_302x181.jpg
  text: '<em>Bababi</em> là tổng hợp những ghi chép và kinh nghiệm chăm con của một cặp vợ chồng trẻ người việt đang sống và làm việc ở nước ngoài. Papapi và Mamami hy vọng những ghi chép này sẽ giúp ích cho cac gia đình tương lai.'

widget2:
  title: "Mamami"
  url: 'http://diy2learn.github.io/chamcon/mamami/'
  image: widget3_mamami_birthday-cake_302x182.jpg
  text: '<em> Mamami</em> là nơi mẹ Mamami chia sẻ những công thức làm bánh Pháp và những món ăn Việt–đã được điều chỉnh để thích ứng với nguyên vật liệu ở nơi xa xứ.'

widget3:
  title: "Papapi"
  url: 'http://diy2learn.github.io/chamcon/papapi/'
  image: widget2_pathToSuccess.jpg
  text: '<em>Papapi</em> là nơi Papapi ghi chép lại những kiến thức và kinh nghiệm hữu ích cho bản thân trên con đường tìm kiếm một cuộc sống tốt hơn.'




#
# Use the call for action to show a button on the frontpage
#
# To make internal links, just use a permalink like this
# url: /getting-started/
#
# To style the button in different colors, use no value
# to use the main color or success, alert or secondary.
# To change colors see sass/_01_settings_colors.scss
#
callforaction:
  url: http://tinyletter.com/papapi
  text: Inform me about new updates and features ›
  style: alert
permalink: /index.html
#
# This is a nasty hack to make the navigation highlight
# this page as active in the topbar navigation
#
homepage: true
---

<div id="videoModal" class="reveal-modal large" data-reveal="">
  <div class="flex-video widescreen vimeo" style="display: block;">
    <iframe width="1280" height="720" src="https://www.youtube.com/embed/3b5zCFSmVvU" frameborder="0" allowfullscreen></iframe>
  </div>
  <a class="close-reveal-modal">&#215;</a>
</div>
