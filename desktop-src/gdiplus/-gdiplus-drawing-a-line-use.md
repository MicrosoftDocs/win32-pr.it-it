---
description: Questo argomento illustra come disegnare una linea usando GDI Plus.
ms.assetid: 2e7444f8-94a6-40d6-b243-0764e245eec4
title: Disegno di una linea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1e2a330f24cd0d1771458d02b264cdaa493835477b40c95d05ca4bf71c8a1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036809"
---
# <a name="drawing-a-line"></a>Disegno di una linea

Questo argomento illustra come disegnare una linea usando GDI Plus.

Per disegnare una linea in Windows GDI+ sono necessari un [**oggetto Graphics,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) un [**oggetto Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e un [**oggetto Color.**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) **L'oggetto Graphics** fornisce il [metodo DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) e l'oggetto **Pen** contiene gli attributi della linea, ad esempio colore e larghezza. L'indirizzo **dell'oggetto Pen** viene passato come argomento al **metodo DrawLine.**

Il programma seguente, che disegna una linea da (0, 0) a (200, 100), è costituito da tre funzioni: **WinMain**, **WndProc** e **OnPaint**. Le **funzioni WinMain** **e WndProc** forniscono il codice fondamentale comune alla maggior parte Windows applicazioni. Non è presente GDI+ codice nella **funzione WndProc.** La **funzione WinMain** ha una piccola quantità di codice GDI+, in modo che le chiamate necessarie a [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) e [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown). Il GDI+ codice che crea effettivamente un [**oggetto Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e disegna una linea si trova nella **funzione OnPaint.**

La **funzione OnPaint** riceve un handle per un contesto di dispositivo e lo passa a un [**costruttore Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) L'argomento passato al [**costruttore Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) è un riferimento a un [**oggetto Color.**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) I quattro numeri passati al costruttore del colore rappresentano i componenti alfa, rosso, verde e blu del colore. Il componente alfa determina la trasparenza del colore; 0 è completamente trasparente e 255 è completamente opaco. I quattro numeri passati al metodo [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) rappresentano il punto iniziale (0, 0) e il punto finale (200, 100) della riga.


```C++
#include <stdafx.h>
#include <windows.h>
#include <objidl.h>
#include <gdiplus.h>
using namespace Gdiplus;
#pragma comment (lib,"Gdiplus.lib")

VOID OnPaint(HDC hdc)
{
   Graphics graphics(hdc);
   Pen      pen(Color(255, 0, 0, 255));
   graphics.DrawLine(&pen, 0, 0, 200, 100);
}

LRESULT CALLBACK WndProc(HWND, UINT, WPARAM, LPARAM);

INT WINAPI WinMain(HINSTANCE hInstance, HINSTANCE, PSTR, INT iCmdShow)
{
   HWND                hWnd;
   MSG                 msg;
   WNDCLASS            wndClass;
   GdiplusStartupInput gdiplusStartupInput;
   ULONG_PTR           gdiplusToken;
   
   // Initialize GDI+.
   GdiplusStartup(&gdiplusToken, &gdiplusStartupInput, NULL);
   
   wndClass.style          = CS_HREDRAW | CS_VREDRAW;
   wndClass.lpfnWndProc    = WndProc;
   wndClass.cbClsExtra     = 0;
   wndClass.cbWndExtra     = 0;
   wndClass.hInstance      = hInstance;
   wndClass.hIcon          = LoadIcon(NULL, IDI_APPLICATION);
   wndClass.hCursor        = LoadCursor(NULL, IDC_ARROW);
   wndClass.hbrBackground  = (HBRUSH)GetStockObject(WHITE_BRUSH);
   wndClass.lpszMenuName   = NULL;
   wndClass.lpszClassName  = TEXT("GettingStarted");
   
   RegisterClass(&wndClass);
   
   hWnd = CreateWindow(
      TEXT("GettingStarted"),   // window class name
      TEXT("Getting Started"),  // window caption
      WS_OVERLAPPEDWINDOW,      // window style
      CW_USEDEFAULT,            // initial x position
      CW_USEDEFAULT,            // initial y position
      CW_USEDEFAULT,            // initial x size
      CW_USEDEFAULT,            // initial y size
      NULL,                     // parent window handle
      NULL,                     // window menu handle
      hInstance,                // program instance handle
      NULL);                    // creation parameters
      
   ShowWindow(hWnd, iCmdShow);
   UpdateWindow(hWnd);
   
   while(GetMessage(&msg, NULL, 0, 0))
   {
      TranslateMessage(&msg);
      DispatchMessage(&msg);
   }
   
   GdiplusShutdown(gdiplusToken);
   return msg.wParam;
}  // WinMain

LRESULT CALLBACK WndProc(HWND hWnd, UINT message, 
   WPARAM wParam, LPARAM lParam)
{
   HDC          hdc;
   PAINTSTRUCT  ps;
   
   switch(message)
   {
   case WM_PAINT:
      hdc = BeginPaint(hWnd, &ps);
      OnPaint(hdc);
      EndPaint(hWnd, &ps);
      return 0;
   case WM_DESTROY:
      PostQuitMessage(0);
      return 0;
   default:
      return DefWindowProc(hWnd, message, wParam, lParam);
   }
} // WndProc
```



Si noti la chiamata a [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) nella **funzione WinMain.** Il primo parametro della **funzione GdiplusStartup** è l'indirizzo di un ULONG \_ PTR. **GdiplusStartup** riempie la variabile con un token che viene passato successivamente alla [**funzione GdiplusShutdown.**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) Il secondo parametro della **funzione GdiplusStartup** è l'indirizzo di una [**struttura GdiplusStartupInput.**](/windows/win32/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupinput) Il codice precedente si basa sul costruttore **GdiplusStartupInput** predefinito per impostare i membri della struttura in modo appropriato.

 

 



