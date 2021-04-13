---
description: Il sistema non è l'unica fonte di \_ messaggi di disegno WM. La funzione InvalidateRect o InvalidateRgn può generare indirettamente \_ messaggi di disegno WM per le finestre. Queste funzioni contrassegnano tutta o parte di un'area client come non valida (che deve essere ridisegnato).
ms.assetid: 41c2bc07-768b-4d27-a869-69b072f3e033
title: Invalidare l'area client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76fb02be44f600b80f87ec8f05c022fa3c35d827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993960"
---
# <a name="invalidating-the-client-area"></a>Invalidare l'area client

Il sistema non è l'unica fonte di messaggi di [**\_ disegno WM**](wm-paint.md) . La funzione [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) o [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) può generare indirettamente messaggi di **\_ disegno WM** per le finestre. Queste funzioni contrassegnano tutta o parte di un'area client come non valida (che deve essere ridisegnato).

Nell'esempio seguente, la routine della finestra invalida l'intera area client durante l'elaborazione dei messaggi [**WM \_ char**](../inputdev/wm-char.md) . Ciò consente all'utente di modificare la figura digitando un numero e visualizzando i risultati; Questi risultati vengono disegnati non appena non sono presenti altri messaggi nella coda di messaggi dell'applicazione.


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



In questo esempio, l'argomento **null** utilizzato da [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) specifica l'intera area client; l'argomento **true** causa la cancellazione dello sfondo. Se non si desidera che l'applicazione attenda finché la coda di messaggi dell'applicazione non dispone di altri messaggi, utilizzare la funzione [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) per forzare l'invio immediato del messaggio di [**\_ disegno WM**](wm-paint.md) . Se è presente una parte non valida dell'area client, **UpdateWindow** invia il messaggio di **\_ disegno WM** per la finestra specificata direttamente alla routine della finestra.

 

 
