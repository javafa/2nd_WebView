# 2nd_WebView
웹뷰 사용법을 알아봅니다

## WebView Client 사용
* 기본 설정
```java
    // script 사용 설정 (필수)
    webView.getSettings().setJavaScriptEnabled(true);
    // 줌사용
    webView.getSettings().setSupportZoom(true);
    webView.getSettings().setBuiltInZoomControls(true);
```
* 클라이언트 설정
```java
    // 웹뷰 클라이언트를 지정... (안하면 내장 웹브라우저가 팝업된다.)
    webView.setWebViewClient(new WebViewClient());
    // 둘다 세팅할것 : http 프로토콜을 ChromeClient 가 처리해 주지 않음 (강제 옵션이 있는지는 각자 확인)
    webView.setWebChromeClient(new WebChromeClient());
```
* url 호출 기본함수
```java
    // url 이동
    webView.loadUrl(url);
    // 뒤로가기
    webView.goBack();
```