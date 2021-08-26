---
description: È possibile disegnare uno sfondo della finestra personalizzato anziché fare in modo che il sistema la dise disegna per conto dell'utente.
ms.assetid: 72a342dc-2766-4ec9-b4c6-5ac3c550ea25
title: Disegno di uno sfondo di finestra personalizzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4248f7d7a1ae27ae09c93e95734fd72285028e1185b6d35110e5141fcbf88c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966011"
---
# <a name="drawing-a-custom-window-background"></a>Disegno di uno sfondo di finestra personalizzato

È possibile disegnare uno sfondo della finestra personalizzato anziché fare in modo che il sistema la dise disegna per conto dell'utente. La maggior parte delle applicazioni specifica un handle di pennello o un valore di colore di sistema per il pennello di sfondo della classe durante la registrazione della classe della finestra; il sistema usa il pennello o il colore per disegnare lo sfondo. Se tuttavia si imposta il pennello di sfondo della classe su **NULL,** il sistema invia un messaggio [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) alla routine della finestra ogni volta che è necessario disegnare lo sfondo della finestra, consentendo di disegnare uno sfondo personalizzato.

Nell'esempio seguente la routine della finestra disegna un modello a scacchiera di grandi dimensioni che si adatta perfettamente alla finestra. La procedura riempie l'area client con un pennello bianco e quindi disegna tre rettangoli 20 per 20 usando un pennello grigio. Il contesto di dispositivo di visualizzazione da utilizzare per disegnare lo sfondo è specificato nel *parametro wParam* per il messaggio.


```C++
HBRUSH hbrWhite, hbrGray; 
 
  . 
  . 
  . 
 
case WM_CREATE: 
    hbrWhite = GetStockObject(WHITE_BRUSH); 
    hbrGray  = GetStockObject(GRAY_BRUSH); 
    return 0L; 
 
case WM_ERASEBKGND: 
    hdc = (HDC) wParam; 
    GetClientRect(hwnd, &rc); 
    SetMapMode(hdc, MM_ANISOTROPIC); 
    SetWindowExtEx(hdc, 100, 100, NULL); 
    SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
    FillRect(hdc, &rc, hbrWhite); 
 
    for (i = 0; i < 13; i++) 
    { 
        x = (i * 40) % 100; 
        y = ((i * 40) / 100) * 20; 
        SetRect(&rc, x, y, x + 20, y + 20); 
        FillRect(hdc, &rc, hbrGray); 
    } 
  return 1L; 
```



Se l'applicazione disegna una finestra ridotta a icona, il sistema invia anche il messaggio [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) alla routine della finestra per disegnare lo sfondo per la finestra ridotta a icona. È possibile usare la stessa tecnica usata da [**WM \_ PAINT**](wm-paint.md) per determinare se la finestra è ridotta a icona, vale a dire chiamare la funzione [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) e verificare la presenza del valore restituito **TRUE.**

 

 
