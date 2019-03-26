# Win10_Visual_Studio_2017_OpenCV_4.0.1-test  


source code and how to,

```
// openCVtest1.cpp : 此檔案包含 'main' 函式。程式會於該處開始執行及結束執行。
//

/*
ref : https://blog.csdn.net/BeautyJingJing/article/details/79162988

Visual Studio 2017
opencv 4.01
xiaolaba, 2019-mar-25


下載,
https://sourceforge.net/projects/opencvlibrary/files/4.0.1/opencv-4.0.1-vc14_vc15.exe/download
解壓縮到, C:\opencv

win10 x64 繁體版 setup, [設定] [系統] [關於], 右上角 [系統資訊], 左邊 [進階系統設定], 跳出 [系統內容],
[進階] [環境變數N], 跳出 [環境變數], 
[系統變數], 編輯 [path], 加入 [C:\opencv\build\x64\vc15\bin]
[使用者變數], 編輯 [path], 加入 [C:\opencv\build\x64\vc15\bin]


隨便把一個 jpg 更名為 1.jpg, 複製到 C:\, 程序會讀並顯示5秒


Visual Studio 2017 設定
[專案] [屬性], 跳出 [openCVtest1 屬性頁], [所有組態] [平台] 選 x64, 
[VC++] [include 目錄], 加入 [C:\opencv\build\include]
[VC++] [程式庫目錄], 加入 [C:\opencv\build\x64\vc15\lib]
[連接器] [一般], [輸入] [其他相依性], [debug] 最後面, 在 % 前面加入 [opencv_world401d.lib;]
[連接器] [一般], [輸入] [其他相依性], [Release] 最後面, 在 % 前面加入 [opencv_world401.lib;]

*/

#include "pch.h"
#include <iostream>



//#include "stdafx.h"	//no uses
#include<opencv2\core\core.hpp>
#include<opencv2\highgui\highgui.hpp>

#include<opencv2\highgui\highgui_c.h> // xiaolaba, add this otherwise, otherwise not define for cvNamedWindow()


using namespace cv;
using namespace std;
int main()
{
	// 读入一张图片
	//Mat img = imread("C:\\Users\\lijing\\Pictures\\Saved Pictures\\timg.jpg");
	//Mat img = imread("C:\\Users\\User0\\Pictures\\1.jpg");
	Mat img = imread("C:\\xiaolaba_Logitech_C270_marco_mod_IMG_20190324_172511.jpg");
	// 创建一个名为 "photo"窗口  
	cvNamedWindow("photo CV_WINDOW_NORMAL", CV_WINDOW_NORMAL);	//user can change size
	cvNamedWindow("photo WINDOW_AUTOSIZE", WINDOW_AUTOSIZE);	//user cannot change size
	//cvNamedWindow("photo WINDOW_AUTOSIZE", CV_GUI_EXPANDED);	//user cannot change size
	// 在窗口中显示游戏原画  
	imshow("photo CV_WINDOW_NORMAL", img);
	imshow("photo WINDOW_AUTOSIZE", img);
	// 等待10000 ms后窗口自动关闭  
	//waitKey(10000);
	waitKey(20000);
	//waitKey(0);                                          // Wait for a keystroke in the window
	return 0;
}

/*
-------------------- -
作者：BeautyJingJing
来源：CSDN
原文：https ://blog.csdn.net/BeautyJingJing/article/details/79162988 
版权声明：本文为博主原创文章，转载请附上博文链接！
*/


// 執行程式: Ctrl + F5 或 [偵錯] > [啟動但不偵錯] 功能表
// 偵錯程式: F5 或 [偵錯] > [啟動偵錯] 功能表

// 開始使用的秘訣: 
//   1. 使用 [方案總管] 視窗，新增/管理檔案
//   2. 使用 [Team Explorer] 視窗，連線到原始檔控制
//   3. 使用 [輸出] 視窗，參閱組建輸出與其他訊息
//   4. 使用 [錯誤清單] 視窗，檢視錯誤
//   5. 前往 [專案] > [新增項目]，建立新的程式碼檔案，或是前往 [專案] > [新增現有項目]，將現有程式碼檔案新增至專案
//   6. 之後要再次開啟此專案時，請前往 [檔案] > [開啟] > [專案]，然後選取 .sln 檔案

```



The outcome

