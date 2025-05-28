# O'Kitchen
> skill :
Swiper, Map, PWA ![JavaScript](https://img.shields.io/badge/-JavaScript-dc8d2d?style=flat-square&logo=javascript&logoColor=ffffff) ![HTML](https://img.shields.io/badge/-HTML-F05032?style=flat-square&logo=html5&logoColor=ffffff) ![CSS](https://img.shields.io/badge/-CSS-007ACC?style=flat-square&logo=css3) 

> 반응형 : 데스크탑, 탭, 모바일

✅ Point
------------
✔ MainSlider
✔ next, prev, pagination
✔ SubSlider
✔ Map

----------------------------------------

## 1. MainSlider + next, prev, pagination


```
const mainSwiper=new Swiper("#main_slider .swiper-container", {
		navigation: {
			prevEl: "#main_slider .swiper-button-prev",
			nextEl: "#main_slider .swiper-button-next"
		},
		pagination: {
			el: "#main_slider .swiper-pagination",
			type: "fraction"
		}
	});
```
