---
title: Estensione di un'immagine
description: Estensione di un'immagine
ms.assetid: 7cfd91c3-0ebd-47eb-a33d-c81a66f820e5
keywords:
- MCIWndGetDest (macro)
- MCIWndPutDest (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0296cd31988ba79aeab9221fb41b4fd150ffc09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331572"
---
# <a name="stretching-an-image"></a>Estensione di un'immagine

Nell'esempio seguente si estendono le immagini di un clip video. Aumenta le dimensioni del rettangolo di destinazione usando la macro [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) . La dimensione dell'area di riproduzione rimane invariata, quindi il risultato è un'immagine ingrandita e distorta. Negli esempi viene utilizzata la funzione **MCIWndPutDest** per riposizionare il rettangolo di destinazione rispetto all'area di riproduzione, consentendo di visualizzare parti diverse dell'immagine estesa.


```C++
extern RECT rCurrent, rDest; 
 
case WM_COMMAND: 
   switch (wParam) 
   { 
       case IDM_CREATEMCIWND: 
           g_hwndMCIWnd = MCIWndCreate(hwnd, 
               g_hinst, 
               WS_CHILD | WS_VISIBLE, 
               "sample.avi"); 
           break; 
 
       case  IDM_STRETCHIMAGE:      // stretch destination RECT 3:2, 
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rDest.top = rCurrent.top;               // new boundaries 
           rDest.right = rCurrent.right; 
           rDest.left = rCurrent.left + 
               ((rCurrent.left - rCurrent.right) * 3); 
           rDest.bottom = rCurrent.top + 
               ((rCurrent.bottom - rCurrent.top) * 2); 
           MCIWndPutDest(g_hwndMCIWnd, &rDest); // new destination 
           break; 
       case IDM_MOVEDOWN:           // move toward bottom of image 
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rCurrent.top -= 100;                    // new boundaries 
           rCurrent.bottom -= 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination
           break; 
       case IDM_MOVEUP:             // move toward top of image 
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rCurrent.top += 100;                    // new boundaries 
           rCurrent.bottom += 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination 
           break; 
       case IDM_MOVELEFT:           // move toward left edge of image
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rCurrent.right += 100;                  // new boundaries 
           rCurrent.left += 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination 
           break; 
       case  IDM_MOVERIGHT:         // move toward right edge of image
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT
           rCurrent.right -= 100;                  // new boundaries 
           rCurrent.left -= 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination 
           break; 
   } 
   break; 
 
   // Handle other messages here. 
```



 

 




