# O'Kitchen
> skill :
Swiper, Map, PWA ![JavaScript](https://img.shields.io/badge/-JavaScript-dc8d2d?style=flat-square&logo=javascript&logoColor=ffffff) ![HTML](https://img.shields.io/badge/-HTML-F05032?style=flat-square&logo=html5&logoColor=ffffff) ![CSS](https://img.shields.io/badge/-CSS-007ACC?style=flat-square&logo=css3)
> 
> 반응형 : 데스크탑, 탭, 모바일
> 
> https://o-kitchen-git-main-yeongjis-projects.vercel.app/  


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

> 위 슬라이드를 구현하는 스크립트입니다. navigation 옵션을 사용하여 이전 및 다음 버튼을 설정합니다.  
> prevEl과 nextEl 속성에 각각 이전 버튼(.swiper-button-prev)과 다음 버튼(.swiper-button-next)의 선택자를 지정합니다.  
> pagination 옵션을 통해 슬라이더의 페이지네이션을 설정합니다.
> el 속성에는 페이지네이션이 표시될 요소의 선택자를 지정하며,    
> type을 "fraction"으로 설정하여  현재 슬라이드 번호와 총 슬라이드 수를 보여줍니다.

-------------------------------------------
## 2. SubSlider


![Image](https://github.com/user-attachments/assets/e7f6cfb5-8f30-42b3-b720-a3767f885bae)



```
	const subSwiper=new Swiper("#sub_slider .swiper-container", {
		slidesPerView: 1.5,
		spaceBetween: 10,
		breakpoints: {
			640: {
				slidesPerView: 3.5,
				spaceBetween: 5
			}
		}
	});

```

> subslider는 MainSlider와 다르게 한 번에 1.5개 슬라이드가 표시되어 미리보기가 가능합니다.  
> breakpoints 옵션을 통해 다양한 화면 크기에 맞춰 슬라이드 수와 간격을 조정합니다.  
> 화면 너비가 640픽셀 이상일 경우, slidesPerView를 3.5로 변경하고, spaceBetween을 5로 설정하여 더 많은 슬라이드를 보여줍니다.
















-------------------------------------------------

## 3. Map

![Image](https://github.com/user-attachments/assets/f8e1b61a-9a58-467a-afd5-c187c4e3a9e6) 

> 맵을 넣으려면 먼저 구글 맵에 들어가 위치 검색 -> 위치 클릭 -> 위치 공유-> 위도와 경도 대입을  
> 순서로 해야 map을 사용할 수 있습니다. 또한 zoom, center 등으로 상황에 맞게 커스텀 할 수 있습니다.
```
let map;

function initMap(){
	let myLatLng={lat: 37.390141551118695, lng: 126.97151846772532};

	let map=new google.maps.Map(document.getElementById("map"), {
		center: myLatLng,
		zoom: 16,
		mapTypeControl: false,
		zoomControl: false,
		fullscreenControl: false,
		rotateControl: false
	});

	let marker=new google.maps.Marker({
		position: myLatLng,
		map: map,
		title: "(주)오뚜기"
	});
}
```












