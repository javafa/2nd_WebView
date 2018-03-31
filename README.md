# 2nd_WebView
웹뷰 사용법을 알아봅니다

## WebView Client 사용
* 기본 설정
```java
    // 1. 화면과 연결
    WebView webView = findViewById(R.id.webView);

```
* 클라이언트 설정
```java
    // 2. 웹뷰 클라이언트 지정
    // 웹뷰클라이언트 - 일반적인 웹페이지 처리, 링크, 이미지 표시
    webView.setWebViewClient(new WebViewClient());     
    // 웹크롬클라이언트 - 자바스크립트 얼럿, favicon, 프로그래스처리...
    webView.setWebChromeClient(new WebChromeClient()); 
```
* 옵션설정
```java
    webView.getSettings().setJavaScriptEnabled(true);   // 내가 호출한 웹페이지에서 javascript가 동작
    webView.getSettings().setSupportZoom(true);         // 줌 가능
    webView.getSettings().setBuiltInZoomControls(true); // 줌인아웃을 할 수 있는 - + 버튼을 화면에 표시
```
* url 호출 기본함수
```java
    // url 이동
    webView.loadUrl(url);
    // 뒤로가기
    webView.goBack();
```
