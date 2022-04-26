# React로 github.io 홈페이지 만들기

1.  리액트 프로젝트 만들고 <br/> `yarn create-react-app 프로젝트명`
2.  깃헙 레포 만들고 프로젝트랑 연결하기
3.  프로젝트에 gd-pages 다운받기 <br/> `yarn add gh-pages gh-pages --dev`
4.  package.json 수정하기 <br/>
    2번 라인에 :
    ` "homepage": "https://깃헙ID.github.io/레포명" `
    scripts 안에 :

        ```
        "predeploy": "npm run build",
        "deploy": "gh-pages -d build"
        ```

5.  `yarn run deploy`하기, published 뜨면 성공.
6.  깃헙 settings > pages 에 source 부분에 dg-pages /root 로 설정되어있는지 확인. 여기서 알려주는 주소로 들어가면 확인 됨.

자꾸 뭔가 안된다면?

- yarn run deploy가 안되요,.,,;;;
  package.json 에 설정한 predeploy 코드 확인하기
  나는 첨에 predeploy 가 yarn run build 로 되어있어서 안됐음. npm run build로 바꾸니까 바로 deploy 코드 먹힘 ㅎ

- setting 에서 알려준 주소대로 들어갔는데 자꾸 리드미 내용이 떠요,,,,,
  pages 설정에 gh-pages 로 되어있는지 확인하고 좀만 기다렸다가 확인해보기. 바로 안뜰수도있음.
