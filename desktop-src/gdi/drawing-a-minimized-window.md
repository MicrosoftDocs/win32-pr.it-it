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
# <a name="drawing-a-minimized-window"></a><span data-ttu-id="9ec89-103">Disegno di una finestra ridotta a icona</span><span class="sxs-lookup"><span data-stu-id="9ec89-103">Drawing a Minimized Window</span></span>

<span data-ttu-id="9ec89-104">È possibile creare finestre ridotte a icona anziché fare in modo che il sistema li disegni.</span><span class="sxs-lookup"><span data-stu-id="9ec89-104">You can draw your own minimized windows rather than having the system draw them for you.</span></span> <span data-ttu-id="9ec89-105">La maggior parte delle applicazioni definisce un'icona di classe durante la registrazione della classe di finestra per la finestra e il sistema disegna l'icona quando la finestra è ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="9ec89-105">Most applications define a class icon when registering the window class for the window, and the system draws the icon when the window is minimized.</span></span> <span data-ttu-id="9ec89-106">Se si imposta l'icona della classe su **null**, tuttavia, il sistema invia un messaggio di [**\_ disegno WM**](wm-paint.md) alla routine della finestra ogni volta che la finestra è ridotta a icona, consentendo alla routine della finestra di disegnare nella finestra ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="9ec89-106">If you set the class icon to **NULL**, however, the system sends a [**WM\_PAINT**](wm-paint.md) message to your window procedure whenever the window is minimized, enabling the window procedure to draw in the minimized window.</span></span>

<span data-ttu-id="9ec89-107">Nell'esempio seguente, la routine della finestra Disegna una stella nella finestra ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="9ec89-107">In the following example, the window procedure draws a star in the minimized window.</span></span> <span data-ttu-id="9ec89-108">Per determinare quando la finestra è ridotta a icona, nella procedura viene utilizzata la funzione l' [**icona**](/windows/win32/api/winuser/nf-winuser-isiconic) .</span><span class="sxs-lookup"><span data-stu-id="9ec89-108">The procedure uses the [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) function to determine when the window is minimized.</span></span> <span data-ttu-id="9ec89-109">Ciò garantisce che la stella venga disegnata solo quando la finestra è ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="9ec89-109">This ensures that the star is drawn only when the window is minimized.</span></span>


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



<span data-ttu-id="9ec89-110">Impostare l'icona della classe su **null** impostando il membro **HIcon** della struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) su **null** prima di chiamare la funzione [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) per la classe Window.</span><span class="sxs-lookup"><span data-stu-id="9ec89-110">You set the class icon to **NULL** by setting the **hIcon** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure to **NULL** before calling the [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) function for the window class.</span></span>

 

 
