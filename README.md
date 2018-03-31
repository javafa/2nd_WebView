# 2nd_WebView
웹뷰 사용법을 알아봅니다

## WebView Client 사용
* 기본 설정
```java
    // 1. 화면과 연결
    WebView webView = findViewById(R.id.webView);
    
    // script 사용 설정 (필수)
    webView.getSettings().setJavaScriptEnabled(true);
    // 줌사용
    webView.getSettings().setSupportZoom(true);
    webView.getSettings().setBuiltInZoomControls(true);
```
* 클라이언트 설정
```java
    // 2. 웹뷰 클라이언트 지정
    webView.setWebViewClient(new WebViewClient());     // 웹뷰클라이언트 - 일반적인 웹페이지 처리, 링크, 이미지 표시
    webView.setWebChromeClient(new WebChromeClient()); // 웹크롬클라이언트 - 자바스크립트 얼럿, favicon, 프로그래스처리...
```

* url 호출 기본함수
```java
    // url 이동
    webView.loadUrl(url);
    // 뒤로가기
    webView.goBack();
```
