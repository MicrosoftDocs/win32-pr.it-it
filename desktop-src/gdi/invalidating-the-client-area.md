---
description: Il sistema non è l'unica origine dei messaggi WM \_ PAINT. La funzione InvalidateRect o InvalidateRgn può generare indirettamente messaggi WM \_ PAINT per le finestre. Queste funzioni contrassegnano tutta o parte di un'area client come non valida (che deve essere ridisegnata).
ms.assetid: 41c2bc07-768b-4d27-a869-69b072f3e033
title: Invalidazione dell'area client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d94a3a5b4e6903c549331788f9e81947dca44e7a699bb1a633bce46525585b2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558661"
---
# <a name="invalidating-the-client-area"></a>Invalidazione dell'area client

Il sistema non è l'unica origine dei [**messaggi WM \_ PAINT.**](wm-paint.md) La [**funzione InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) o [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) può generare indirettamente messaggi **WM \_ PAINT** per le finestre. Queste funzioni contrassegnano tutta o parte di un'area client come non valida (che deve essere ridisegnata).

Nell'esempio seguente la routine della finestra invalida l'intera area client durante l'elaborazione [**di messaggi WM \_ CHAR.**](../inputdev/wm-char.md) In questo modo l'utente può modificare la figura digitando un numero e visualizzando i risultati. questi risultati vengono disegnati non appena non sono presenti altri messaggi nella coda di messaggi dell'applicazione.


```C++
RECT rc;
POINT aptPentagon[6] = {50,2, 98,35, 79,90, 21,90, 2,35, 50,2}, 
      aptHexagon[7]  = {50,2, 93,25, 93,75, 50,98, 7,75, 7,25, 50,2}; 
POINT *ppt = aptPentagon; 
int cpt = 6; 
 
  . 
  . 
  . 
 
case WM_CHAR: 
    switch (wParam) 
    { 
        case '5': 
            ppt = aptPentagon; 
            cpt = 6; 
            break; 
        case '6': 
            ppt = aptHexagon; 
            cpt = 7; 
            break; 
    } 
    InvalidateRect(hwnd, NULL, TRUE); 
    return 0L; 
 
case WM_PAINT: 
    hdc = BeginPaint(hwnd, &ps); 
    GetClientRect(hwnd, &rc); 
    SetMapMode(hdc, MM_ANISOTROPIC); 
    SetWindowExtEx(hdc, 100, 100, NULL); 
    SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
    Polyline(hdc, ppt, cpt); 
    EndPaint(hwnd, &ps); 
    return 0L; 
```



In questo esempio **l'argomento NULL** usato da [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) specifica l'intera area client. **L'argomento TRUE** determina la cancellazione dello sfondo. Se non si vuole che l'applicazione attenda che la coda di messaggi dell'applicazione non abbia altri messaggi, usare la [**funzione UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) per forzare l'invio immediato del messaggio [**WM \_ PAINT.**](wm-paint.md) Se è presente una parte non valida dell'area client, **UpdateWindow** invia il messaggio **WM \_ PAINT** per la finestra specificata direttamente alla routine della finestra.

 

 
