---
description: In questo argomento viene illustrato come creare una linea utilizzando GDI Plus.
ms.assetid: 2e7444f8-94a6-40d6-b243-0764e245eec4
title: Disegno di una linea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5284a178baab624633dd427cad84b35933a72fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979047"
---
# <a name="drawing-a-line"></a>Disegno di una linea

In questo argomento viene illustrato come creare una linea utilizzando GDI Plus.

Per creare una linea in GDI+ Windows sono necessari un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , un oggetto [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e un oggetto [**color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) . L'oggetto **Graphics** fornisce il metodo [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) e l'oggetto **Pen** contiene gli attributi della riga, ad esempio il colore e la larghezza. L'indirizzo dell'oggetto **Pen** viene passato come argomento al metodo **DrawLine** .

Il programma seguente, che disegna una riga da (0,0) a (200, 100), è costituito da tre funzioni: **WinMain**, **WndProc** e **OnPaint**. Le funzioni **WinMain** e **WndProc** forniscono il codice fondamentale comune alla maggior parte delle applicazioni Windows. Nella funzione **WndProc** non è presente alcun codice GDI+. La funzione **WinMain** presenta una piccola quantità di codice GDI+, ovvero le chiamate obbligatorie a [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) e [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown). Il codice GDI+ che crea effettivamente un oggetto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e disegna una riga si trova nella funzione **OnPaint** .

La funzione **OnPaint** riceve un handle per un contesto di dispositivo e passa tale handle a un costruttore di [**grafica**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . L'argomento passato al costruttore [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) è un riferimento a un oggetto [**color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) . I quattro numeri passati al costruttore di colore rappresentano i componenti alfa, rosso, verde e blu del colore. Il componente alfa determina la trasparenza del colore. 0 è completamente trasparente e 255 è completamente opaco. I quattro numeri passati al metodo [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)) rappresentano il punto iniziale (0, 0) e il punto finale (200, 100) della riga.


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



Si noti la chiamata a [**GdiplusStartup**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusstartup) nella funzione **WinMain** . Il primo parametro della funzione **GdiplusStartup** è l'indirizzo di un PTR ULONG \_ . **GdiplusStartup** riempie la variabile con un token che viene passato successivamente alla funzione [**GdiplusShutdown**](/windows/win32/api/Gdiplusinit/nf-gdiplusinit-gdiplusshutdown) . Il secondo parametro della funzione **GdiplusStartup** è l'indirizzo di una struttura [**GdiplusStartupInput**](/windows/win32/api/Gdiplusinit/ns-gdiplusinit-gdiplusstartupinput) . Il codice precedente si basa sul costruttore **GdiplusStartupInput** predefinito per impostare i membri della struttura in modo appropriato.

 

 



