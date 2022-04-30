---
title: Create React App : Typescript
tags: [React, JavaScript, Web Development]
style: border
color: primary
description: Create React App : Typescript
---
# create - react - app : typescript



1. **npx-create-react-app 으로 폴더 생성 : typescript 프로젝트 생성** 

오늘도 안되면 죽일것이다. 
[링크](https://velog.io/@miiunii/CRACreate-React-App%EC%9C%BC%EB%A1%9C-Typescript-%EC%84%A4%EC%A0%95%ED%95%98%EA%B8%B0) npx-create-react-app 으로 폴더 생성 
localhost  3030으로 멀쩡하게 생성이 되었다. 
: 폴더 열어보면 ts파일, tsconfig.json으로 생성된것을 볼 수 있음 

```tex
npx create-react-app(프로젝트명) --template typescript
```

이 작업을 통해 CRA가 typescript를 이용할 때 필요한 기본적인 것들을 설치 및 설정을 해준다.
( babel, webpack etc... )



2. **tsconfig.json 설정**

 처음 몇번의 시도에서는 나는 이것을 조물딱 조물딱 만지고 시작을 했더랬다. 
허나 create-react-app 의 패키지는 나보다 똑똑할 것이다. 일단은 가만히 내버려 두도록 한다.  

---- npm start 가 성공적으로 진행된다. 



3. **오늘의 깨달음은**


   [react-kakao-maps-sdk](https://www.npmjs.com/package/react-kakao-maps-sdk) 와[@types/kakao-js-sdk](https://www.npmjs.com/package/@types/kakao-js-sdk)는 전혀 다른 친구라는 것이다. 

   [@types/kakao-js-sdk](https://www.npmjs.com/package/@types/kakao-js-sdk) 는 카카오에서 제공하는 api를 typescript에서도 사용할 수 있도록 
   **TypeScript definitions** for Kakao JavaScript SDK 만 제공하는 알맹이 없는 파일이고

   [react-kakao-maps-sdk](https://www.npmjs.com/package/react-kakao-maps-sdk) 는 [Kakao Maps API](https://apis.map.kakao.com/)를 react에 맞게 포팅한 라이브러리 

   +여기안에 typescript definition 패키지까지 같이 들어있는 패키지이다. 

   sdk 김범수가 만든거 아니라고 계속 깔기 싫다고 객기부렸는데 [@types/kakao-js-sdk](https://www.npmjs.com/package/@types/kakao-js-sdk) 만 설치해서 react 에서 typescript로 앱 만들려면 일단 카카오 js 라이브러리를 ts로 바꿔서... 또 리액트에 맞게 tsx로 만들었어야 한다나..
   남의말 듣는것도 실력이다. 

   **React에서 Typescript를 사용하고싶은 나는 온순하게 [react-kakao-maps-sdk](https://www.npmjs.com/package/react-kakao-maps-sdk) 를 설치하도록 한다.**

   그리고 다른것은 깔끔하게 잊도록 한다. 

   

   *역시 코딩은 차분함이 생명이다. 뭔가 필사를  시작해야겠다. 다 적혀있는데 잘 안읽었지...*



4. **eslint setting : javascript의 문제점을 수정할때 유용한 util 이라고 한다. **

​		설치 완료 후, 프로젝트 root에 '.eslintrc.js', '.eslintignore'를 만든다.
​		eslintrc.js에 아래 코드를 넣는다.
​		( eslint를 어떤 plugin으로 어떤 rule로 적용할 것인지 정하는 파일 )







# react-kakao-maps-sdk

1. https://www.npmjs.com/package/react-kakao-maps-sdk

   일단 시키는걸 다 해줬다. 
   325d93eda8c4b6345f61337aea429148
   javascript키도 안까불고 그냥 넣었다. 
   
2. 타입스크립트 사용자를 위해 [kakao.maps.d.ts](https://github.com/JaeSeoKim/kakao.maps.d.ts) 패키지를 제공합니다.

   `tsconfig.json`의 `compilerOptions.types` 속성에 `kakao.maps.d.ts` 패키지를 추가하시면 됩니다.



여기까지도 npm start가 잘 실행된다. :) 
원래 하던것처럼 app.css, index.css 밀고, 
app.tsx 의<div classname =App> 만 남겨두고 실행해봐도 잘된다. 



3. javascript 키를 숨겨준다. 

