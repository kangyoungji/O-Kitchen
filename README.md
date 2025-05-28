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

> 슬라이드로 움직일 뿐 아니라 페이지가 표시되고, 버튼으로도 넘어가는 슬라이드를 구현했습니다. 

![Image](https://github.com/user-attachments/assets/06ce2ea2-07ce-403c-890c-cc35397d52f8)

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

-------------------------------------------
## 2. SubSlider

![Image](https://github.com/user-attachments/assets/e7f6cfb5-8f30-42b3-b720-a3767f885bae)























-------------------------------------------------

## 3. Map

![Image](https://github.com/user-attachments/assets/f8e1b61a-9a58-467a-afd5-c187c4e3a9e6) 

> 맵을 넣으려면 먼저 구글 맵에 들어가 위치 검색 -> 위치 클릭 -> 위치 공유-> 위도와 경도 대입을  
> 순서로 해야 map을 사용할 수 있습니다. 또한 zoom, center 등으로 상황에 맞게 커스텀 할 수 있습니다.
```
// const : 변하지 않는 오브젝트 입력할 때 사용
// point : 위도 경도 좌표

const point={ lat: 37.401564, lng: 126.922195 };

function initMap(){
	// const prodSwiper=new Swiper(".product_swiper", { loop: true, autoplay: true })
	// document.getElementById("map")
	const map=new google.maps.Map(document.getElementById("map"), {
		center: point, // 타깃
		zoom: 16 // 배율
	});
}

window.initMap=initMap;
```












