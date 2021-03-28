---
description: È possibile creare lo sfondo della finestra, anziché fare in che il sistema lo disegni.
ms.assetid: 72a342dc-2766-4ec9-b4c6-5ac3c550ea25
title: Disegno di uno sfondo personalizzato della finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437a88bec680a6f35e84f5444fc90a45f98da533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978650"
---
# <a name="drawing-a-custom-window-background"></a>Disegno di uno sfondo personalizzato della finestra

È possibile creare lo sfondo della finestra, anziché fare in che il sistema lo disegni. La maggior parte delle applicazioni specifica un handle di pennello o un valore di colore di sistema per il pennello di sfondo della classe durante la registrazione della classe della finestra; il sistema usa il pennello o il colore per creare lo sfondo. Se si imposta il pennello per lo sfondo della classe su **null**, tuttavia, il sistema invia un messaggio [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) alla routine della finestra ogni volta che è necessario disegnare lo sfondo della finestra, consentendo di disegnare uno sfondo personalizzato.

Nell'esempio seguente, la routine della finestra Disegna un modello a scacchi di grandi dimensioni che si adegua perfettamente alla finestra. La procedura riempie l'area client con un pennello bianco, quindi disegna rettangoli 13 20 per 20 utilizzando un pennello grigio. Il contesto del dispositivo di visualizzazione da utilizzare per il disegno dello sfondo viene specificato nel parametro *wParam* per il messaggio.


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



Se l'applicazione disegna la propria finestra ridotta a icona, il sistema invia anche il messaggio [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) alla routine della finestra per disegnare lo sfondo della finestra ridotta a icona. È possibile usare la stessa tecnica usata da [**WM \_ Paint**](wm-paint.md) per determinare se la finestra è ridotta [**a icona, chiamare la funzione**](/windows/win32/api/winuser/nf-winuser-isiconic) IsTrue e verificare la presenza del valore restituito **true**.

 

 
