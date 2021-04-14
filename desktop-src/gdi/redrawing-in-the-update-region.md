---
description: È possibile limitare la quantità di disegno eseguita dall'applicazione durante l'elaborazione del \_ messaggio di disegno WM determinando le dimensioni e la posizione dell'area di aggiornamento.
ms.assetid: 3407014d-6427-45e9-8be4-b8037ca5438f
title: Ridisegno nell'area di aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f90518db1a66b98fc7f4bd5961f2cfa581bb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993880"
---
# <a name="redrawing-in-the-update-region"></a>Ridisegno nell'area di aggiornamento

È possibile limitare la quantità di disegno eseguita dall'applicazione durante l'elaborazione del [**messaggio \_ di disegno WM**](wm-paint.md) determinando le dimensioni e la posizione dell'area di aggiornamento. Poiché il sistema usa l'area di aggiornamento quando si crea l'area di ridimensionamento per il contesto del dispositivo di visualizzazione della finestra, è possibile determinare indirettamente l'area di aggiornamento esaminando l'area di visualizzazione.

Nell'esempio seguente, la routine della finestra Disegna un triangolo, un rettangolo, un Pentagono e un esagono, ma solo se tutte o una parte di ogni figura si trova all'interno dell'area di aggiornamento. La procedura della finestra usa la funzione [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) e un rettangolo 100 per 100 per determinare se una figura si trova all'interno dell'area di ridimensionamento (e di conseguenza l'area di aggiornamento) per il contesto di dispositivo comune recuperato da [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint).


```C++
POINT aptTriangle[4]  = {50,2, 98,86,  2,86, 50,2}, 
      aptRectangle[5] = { 2,2, 98,2,  98,98,  2,98, 2,2}, 
      aptPentagon[6]  = {50,2, 98,35, 79,90, 21,90, 2,35, 50,2}, 
      aptHexagon[7]   = {50,2, 93,25, 93,75, 50,98, 7,75, 7,25, 50,2}; 
  . 
  . 
  . 
 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            SetRect(&rc, 0, 0, 100, 100); 
 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptTriangle, 4); 
 
            SetViewportOrgEx(hdc, 100, 0, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptRectangle, 5); 
 
            SetViewportOrgEx(hdc, 0, 100, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptPentagon, 6); 
 
            SetViewportOrgEx(hdc, 100, 100, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptHexagon, 7); 
            EndPaint(hwnd, &ps); 
            return 0L; 
 
  . 
  . 
  . 
```



Le coordinate di ogni figura in questo esempio si trovano nello stesso rettangolo 100 per 100. Prima di disegnare una figura, la routine della finestra Imposta l'origine del viewport su una parte diversa dell'area client usando la funzione [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) . In questo modo si impedisce che le cifre vengano disegnate una sopra l'altra. La modifica dell'origine del viewport non influisce sull'area di visualizzazione, ma influisce sul modo in cui vengono interpretate le coordinate del rettangolo passato a [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) . La modifica dell'origine consente inoltre di utilizzare un solo rettangolo per controllare l'area di aggiornamento anziché singoli rettangoli per ogni figura.

 

 



