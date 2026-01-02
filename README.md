# 모바일프로그래밍 6주차 과제 - 나의 깃허브

<img src="https://user-images.githubusercontent.com/62374317/80569251-7ccd0e80-8a33-11ea-9413-f7919f56313c.jpg" width="90%"></img>

package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Context;
import android.os.Bundle;
import android.webkit.WebSettings;
import android.webkit.WebView;
import android.webkit.WebViewClient;

import com.example.myapplication.ui.main.MainFragment;

public class MainActivity extends AppCompatActivity{

    private WebView mWebView;
    private WebSettings mWebSettings;

    @Override
    protected void onCreate(Bundle savedInstanceState){
        super.onCreate(savedInstanceState);
        setContentView(R.layout.main_activity);

        mWebView = (WebView)findViewById(R.id.webview_login);
        mWebView.setWebViewClient(new WebViewClient());
        mWebSettings = mWebView.getSettings();
        mWebSettings.setJavaScriptEnabled(true);

        mWebView.loadUrl("https://github.com/jungin-kim/rkrkrk24.github.io");
    }
}
