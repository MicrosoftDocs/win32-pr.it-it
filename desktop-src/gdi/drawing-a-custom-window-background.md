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
# <a name="drawing-a-custom-window-background"></a><span data-ttu-id="30d41-103">Disegno di uno sfondo personalizzato della finestra</span><span class="sxs-lookup"><span data-stu-id="30d41-103">Drawing a Custom Window Background</span></span>

<span data-ttu-id="30d41-104">È possibile creare lo sfondo della finestra, anziché fare in che il sistema lo disegni.</span><span class="sxs-lookup"><span data-stu-id="30d41-104">You can draw your own window background rather than having the system draw it for you.</span></span> <span data-ttu-id="30d41-105">La maggior parte delle applicazioni specifica un handle di pennello o un valore di colore di sistema per il pennello di sfondo della classe durante la registrazione della classe della finestra; il sistema usa il pennello o il colore per creare lo sfondo.</span><span class="sxs-lookup"><span data-stu-id="30d41-105">Most applications specify a brush handle or system color value for the class background brush when registering the window class; the system uses the brush or color to draw the background.</span></span> <span data-ttu-id="30d41-106">Se si imposta il pennello per lo sfondo della classe su **null**, tuttavia, il sistema invia un messaggio [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) alla routine della finestra ogni volta che è necessario disegnare lo sfondo della finestra, consentendo di disegnare uno sfondo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="30d41-106">If you set the class background brush to **NULL**, however, the system sends a [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message to your window procedure whenever the window background must be drawn, letting you draw a custom background.</span></span>

<span data-ttu-id="30d41-107">Nell'esempio seguente, la routine della finestra Disegna un modello a scacchi di grandi dimensioni che si adegua perfettamente alla finestra.</span><span class="sxs-lookup"><span data-stu-id="30d41-107">In the following example, the window procedure draws a large checkerboard pattern that fits neatly in the window.</span></span> <span data-ttu-id="30d41-108">La procedura riempie l'area client con un pennello bianco, quindi disegna rettangoli 13 20 per 20 utilizzando un pennello grigio.</span><span class="sxs-lookup"><span data-stu-id="30d41-108">The procedure fills the client area with a white brush and then draws thirteen 20-by-20 rectangles using a gray brush.</span></span> <span data-ttu-id="30d41-109">Il contesto del dispositivo di visualizzazione da utilizzare per il disegno dello sfondo viene specificato nel parametro *wParam* per il messaggio.</span><span class="sxs-lookup"><span data-stu-id="30d41-109">The display device context to use when drawing the background is specified in the *wParam* parameter for the message.</span></span>


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



<span data-ttu-id="30d41-110">Se l'applicazione disegna la propria finestra ridotta a icona, il sistema invia anche il messaggio [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) alla routine della finestra per disegnare lo sfondo della finestra ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="30d41-110">If the application draws its own minimized window, the system also sends the [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message to the window procedure to draw the background for the minimized window.</span></span> <span data-ttu-id="30d41-111">È possibile usare la stessa tecnica usata da [**WM \_ Paint**](wm-paint.md) per determinare se la finestra è ridotta [**a icona, chiamare la funzione**](/windows/win32/api/winuser/nf-winuser-isiconic) IsTrue e verificare la presenza del valore restituito **true**.</span><span class="sxs-lookup"><span data-stu-id="30d41-111">You can use the same technique used by [**WM\_PAINT**](wm-paint.md) to determine whether the window is minimized that is, call the [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) function and check for the return value **TRUE**.</span></span>

 

 
