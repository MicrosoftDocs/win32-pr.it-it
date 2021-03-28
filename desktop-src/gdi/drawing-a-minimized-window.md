---
description: È possibile creare finestre ridotte a icona anziché fare in modo che il sistema li disegni.
ms.assetid: 607d987a-5bdc-46bc-bde7-6dc52745ac79
title: Disegno di una finestra ridotta a icona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced1f3205243ea098856517590d58caee851329a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401679"
---
# <a name="drawing-a-minimized-window"></a>Disegno di una finestra ridotta a icona

È possibile creare finestre ridotte a icona anziché fare in modo che il sistema li disegni. La maggior parte delle applicazioni definisce un'icona di classe durante la registrazione della classe di finestra per la finestra e il sistema disegna l'icona quando la finestra è ridotta a icona. Se si imposta l'icona della classe su **null**, tuttavia, il sistema invia un messaggio di [**\_ disegno WM**](wm-paint.md) alla routine della finestra ogni volta che la finestra è ridotta a icona, consentendo alla routine della finestra di disegnare nella finestra ridotta a icona.

Nell'esempio seguente, la routine della finestra Disegna una stella nella finestra ridotta a icona. Per determinare quando la finestra è ridotta a icona, nella procedura viene utilizzata la funzione l' [**icona**](/windows/win32/api/winuser/nf-winuser-isiconic) . Ciò garantisce che la stella venga disegnata solo quando la finestra è ridotta a icona.


```C++
POINT aptStar[6] = {50,2, 2,98, 98,33, 2,33, 98,98, 50,2}; 
 
  . 
  . 
  . 
 
case WM_PAINT: 
    hdc = BeginPaint(hwnd, &ps); 
 
    // Determine whether the window is minimized.  
 
    if (IsIconic(hwnd)) 
    { 
        GetClientRect(hwnd, &rc); 
        SetMapMode(hdc, MM_ANISOTROPIC); 
        SetWindowExtEx(hdc, 100, 100, NULL); 
        SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
        Polyline(hdc, aptStar, 6); 
    } 
    else 
    { 
        TextOut(hdc, 0,0, "Hello, Windows!", 15); 
    } 
    EndPaint(hwnd, &ps); 
    return 0L; 
```



Impostare l'icona della classe su **null** impostando il membro **HIcon** della struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) su **null** prima di chiamare la funzione [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) per la classe Window.

 

 
