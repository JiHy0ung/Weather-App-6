# CoNoo Second React Project

**Weather App**

![image](https://i.pinimg.com/736x/03/1a/a6/031aa6aaa96c468485d3d8b381593b97.jpg)

### **[날씨 앱 바로가기~🌦](https://jihyoung-weather-app-6.netlify.app/)**

<br>

## 사용 언어
* react

<br>

## **느낀점 & 개선사항**
deploy를 시키는데 계속해서 failed가 떠서 무슨 문제인가 싶었는데

useEffect에서 배열이 비어있어 의존성 문제가 생겼음.

```js
useEffect(() => {
  getCurrentLocation();
}, []);

/* 이렇게 바꿈. */
useEffect(() => {
  getCurrentLocation();
}, [getCurrentLocation]);
```

그리고 함수 위에

```// eslint-disable-next-line react-hooks/exhaustive-deps```

오류를 막아주는 주석문으로 해결을 함.
