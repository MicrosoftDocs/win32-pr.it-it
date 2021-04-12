---
title: Introduzione con i movimenti tocco di Windows
description: In questa sezione vengono descritti i passaggi di base per l'utilizzo di movimenti multitouch.
ms.assetid: 0ffe222a-a0ac-498b-a4ca-85cfb1caba93
keywords:
- Windows Touch, movimenti
- Windows Touch, messaggi
- movimenti, informazioni
- movimenti, messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506fee0667e6eb38469bda10af9ded0ea6d3439f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395390"
---
# <a name="getting-started-with-windows-touch-gestures"></a>Introduzione con i movimenti tocco di Windows

In questa sezione vengono descritti i passaggi di base per l'utilizzo di movimenti multitouch.

I passaggi seguenti vengono in genere eseguiti quando si utilizzano i movimenti tocco di Windows:

1.  Configurare una finestra per la ricezione dei movimenti.
2.  Gestire i messaggi di movimento.
3.  Interpretare i messaggi di movimento.

## <a name="setting-up-a-window-to-receive-gestures"></a>Impostazione di una finestra per la ricezione di movimenti

Per impostazione predefinita, si ricevono messaggi di [**\_ movimento WM**](wm-gesture.md) .

> [!Note]  
> Se si chiama [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), si smette di ricevere messaggi di [**\_ movimento WM**](wm-gesture.md) . Se non si ricevono messaggi **di \_ movimento WM** , assicurarsi che non sia stato chiamato **RegisterTouchWindow**.

 

Nel codice seguente viene illustrata un'implementazione di InitInstance semplice.


```C++
#include <windows.h>


BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
   HWND hWnd;

   hInst = hInstance; // Store instance handle in our global variable

   hWnd = CreateWindow(szWindowClass, szTitle, WS_OVERLAPPEDWINDOW,
      CW_USEDEFAULT, 0, CW_USEDEFAULT, 0, NULL, NULL, hInstance, NULL);

   if (!hWnd)
   {
      return FALSE;
   }

   ShowWindow(hWnd, nCmdShow);
   UpdateWindow(hWnd);

   return TRUE;
}
```



## <a name="handling-gesture-messages"></a>Gestione dei messaggi di movimento

Analogamente alla gestione dei messaggi di input Windows Touch, è possibile gestire i messaggi di movimento in molti modi. Se si usa Win32, è possibile cercare il messaggio di [**\_ movimento WM**](wm-gesture.md) in WndProc. Se si sta creando un altro tipo di applicazione, è possibile aggiungere il messaggio di **\_ movimento WM** alla mappa messaggi e quindi implementare un gestore personalizzato.

Nel codice seguente viene illustrato come gestire i messaggi di movimento.


```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {    
    case WM_GESTURE:
            // Insert handler code here to interpret the gesture.            
            return DecodeGesture(hWnd, message, wParam, lParam);            
```



## <a name="interpreting-the-gesture-messages"></a>Interpretazione dei messaggi di movimento

La funzione [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) viene usata per interpretare un messaggio di movimento in una struttura che descrive il movimento. La struttura, [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo), contiene informazioni sul movimento, ad esempio la posizione in cui è stato eseguito il movimento e il tipo di movimento. Nel codice seguente viene illustrato come è possibile recuperare e interpretare un messaggio di movimento.


```C++
  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &gi);
    BOOL bHandled = FALSE;

    if (bResult){
        // now interpret the gesture
        switch (gi.dwID){
           case GID_ZOOM:
               // Code for zooming goes here     
               bHandled = TRUE;
               break;
           case GID_PAN:
               // Code for panning goes here
               bHandled = TRUE;
               break;
           case GID_ROTATE:
               // Code for rotation goes here
               bHandled = TRUE;
               break;
           case GID_TWOFINGERTAP:
               // Code for two-finger tap goes here
               bHandled = TRUE;
               break;
           case GID_PRESSANDTAP:
               // Code for roll over goes here
               bHandled = TRUE;
               break;
           default:
               // A gesture was not recognized
               break;
        }
    }else{
        DWORD dwErr = GetLastError();
        if (dwErr > 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Movimenti tocco di Windows](guide-multi-touch-gestures.md)
</dt> </dl>

 

 




