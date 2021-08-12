---
description: È possibile consentire all'utente di disegnare linee con il mouse facendo disegnare la routine della finestra durante l'elaborazione del messaggio WM \_ MOUSEMOVE.
ms.assetid: 5e8a54b6-05cc-4446-b82e-2b3e550d780a
title: Disegno con il mouse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de7c75c768dcdd330e04a0877bacf59b63d59a6eeb9707011faff6a6b15055c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118250403"
---
# <a name="drawing-with-the-mouse"></a>Disegno con il mouse

È possibile consentire all'utente di disegnare linee con il mouse facendo disegnare la routine della finestra durante l'elaborazione del [**messaggio WM \_ MOUSEMOVE.**](../inputdev/wm-mousemove.md) Il sistema invia il **messaggio WM \_ MOUSEMOVE** alla routine della finestra ogni volta che l'utente sposta il cursore all'interno della finestra. Per disegnare linee, la routine della finestra può recuperare un contesto di dispositivo di visualizzazione e disegnare una linea nella finestra tra le posizioni correnti e precedenti del cursore.

Nell'esempio seguente la routine della finestra si prepara per il disegno quando l'utente preme e tiene premuto il pulsante sinistro del mouse (inviando il messaggio [**WM \_ LBUTTONDOWN).**](../inputdev/wm-lbuttondown.md) Quando l'utente sposta il cursore all'interno della finestra, la routine della finestra riceve una serie di [**messaggi WM \_ MOUSEMOVE.**](../inputdev/wm-mousemove.md) Per ogni messaggio, la routine della finestra disegna una linea che connette la posizione precedente e la posizione corrente. Per disegnare la linea, la procedura usa [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) per recuperare un contesto di dispositivo di visualizzazione. quindi, non appena il disegno è completo e prima di restituire il messaggio, la procedura usa la funzione [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) per rilasciare il contesto di dispositivo di visualizzazione. Non appena l'utente rilascia il pulsante del mouse, la routine della finestra cancella il flag e il disegno si interrompe (che invia il [**messaggio WM \_ LBUTTONUP).**](../inputdev/wm-lbuttonup.md)


```C++
BOOL fDraw = FALSE; 
POINT ptPrevious; 
 
  . 
  . 
  . 
 
case WM_LBUTTONDOWN: 
    fDraw = TRUE; 
    ptPrevious.x = LOWORD(lParam); 
    ptPrevious.y = HIWORD(lParam); 
    return 0L; 
 
case WM_LBUTTONUP: 
    if (fDraw) 
    { 
        hdc = GetDC(hwnd); 
        MoveToEx(hdc, ptPrevious.x, ptPrevious.y, NULL); 
        LineTo(hdc, LOWORD(lParam), HIWORD(lParam)); 
        ReleaseDC(hwnd, hdc); 
    } 
    fDraw = FALSE; 
    return 0L; 
 
case WM_MOUSEMOVE: 
    if (fDraw) 
    { 
        hdc = GetDC(hwnd); 
        MoveToEx(hdc, ptPrevious.x, ptPrevious.y, NULL); 
        LineTo(hdc, ptPrevious.x = LOWORD(lParam), 
          ptPrevious.y = HIWORD(lParam)); 
        ReleaseDC(hwnd, hdc); 
    } 
    return 0L; 
```



Un'applicazione che consente di disegnare, come in questo esempio, registra in genere i punti o le linee in modo che le linee possano essere ridisegnate ogni volta che la finestra viene aggiornata. Le applicazioni di disegno usano spesso un contesto di dispositivo di memoria e una bitmap associata per archiviare le linee disegnate con il mouse.

 

 
