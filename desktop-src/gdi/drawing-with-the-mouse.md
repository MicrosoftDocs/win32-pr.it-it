---
description: È possibile consentire all'utente di creare linee con il mouse facendo in modo che la routine della finestra venga disegnato durante l'elaborazione del messaggio di WM \_ MOUSEMOVE.
ms.assetid: 5e8a54b6-05cc-4446-b82e-2b3e550d780a
title: Disegno con il mouse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ad38e7ef8af5c39918bac7231aea4dde285caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049730"
---
# <a name="drawing-with-the-mouse"></a>Disegno con il mouse

È possibile consentire all'utente di creare linee con il mouse facendo in modo che la routine della finestra venga disegnato durante l'elaborazione del messaggio di [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md) . Il sistema invia il messaggio di **WM \_ MOUSEMOVE** alla routine della finestra ogni volta che l'utente sposta il cursore all'interno della finestra. Per creare linee, la routine della finestra può recuperare un contesto di dispositivo di visualizzazione e creare una linea nella finestra tra le posizioni correnti e precedenti del cursore.

Nell'esempio seguente, la procedura finestra viene preparata per il disegno quando l'utente preme e tiene premuto il pulsante sinistro del mouse (invio del messaggio [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) ). Quando l'utente sposta il cursore all'interno della finestra, la routine della finestra riceve una serie di messaggi di [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md) . Per ogni messaggio, la routine della finestra Disegna una linea che connette la posizione precedente e quella corrente. Per creare la riga, la procedura usa [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) per recuperare un contesto di dispositivo di visualizzazione. quindi, non appena il disegno è completo e prima di restituire il messaggio, la procedura usa la funzione [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) per rilasciare il contesto del dispositivo di visualizzazione. Non appena l'utente rilascia il pulsante del mouse, la routine della finestra Cancella il flag e il disegno viene arrestato (che invia il messaggio [**WM \_ LBUTTONUP**](../inputdev/wm-lbuttonup.md) ).


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



Un'applicazione che consente il disegno, come in questo esempio, in genere registra i punti o le righe in modo che le linee possano essere ridisegnate ogni volta che la finestra viene aggiornata. Il disegno di applicazioni spesso utilizza un contesto di dispositivo di memoria e una bitmap associata per archiviare le linee disegnate utilizzando un mouse.

 

 
