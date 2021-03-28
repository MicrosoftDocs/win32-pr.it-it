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
# <a name="drawing-with-the-mouse"></a><span data-ttu-id="ed19b-103">Disegno con il mouse</span><span class="sxs-lookup"><span data-stu-id="ed19b-103">Drawing with the Mouse</span></span>

<span data-ttu-id="ed19b-104">È possibile consentire all'utente di creare linee con il mouse facendo in modo che la routine della finestra venga disegnato durante l'elaborazione del messaggio di [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md) .</span><span class="sxs-lookup"><span data-stu-id="ed19b-104">You can permit the user to draw lines with the mouse by having your window procedure draw while processing the [**WM\_MOUSEMOVE**](../inputdev/wm-mousemove.md) message.</span></span> <span data-ttu-id="ed19b-105">Il sistema invia il messaggio di **WM \_ MOUSEMOVE** alla routine della finestra ogni volta che l'utente sposta il cursore all'interno della finestra.</span><span class="sxs-lookup"><span data-stu-id="ed19b-105">The system sends the **WM\_MOUSEMOVE** message to the window procedure whenever the user moves the cursor within the window.</span></span> <span data-ttu-id="ed19b-106">Per creare linee, la routine della finestra può recuperare un contesto di dispositivo di visualizzazione e creare una linea nella finestra tra le posizioni correnti e precedenti del cursore.</span><span class="sxs-lookup"><span data-stu-id="ed19b-106">To draw lines, the window procedure can retrieve a display device context and draw a line in the window between the current and previous cursor positions.</span></span>

<span data-ttu-id="ed19b-107">Nell'esempio seguente, la procedura finestra viene preparata per il disegno quando l'utente preme e tiene premuto il pulsante sinistro del mouse (invio del messaggio [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) ).</span><span class="sxs-lookup"><span data-stu-id="ed19b-107">In the following example, the window procedure prepares for drawing when the user presses and holds the left mouse button (sending the [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) message).</span></span> <span data-ttu-id="ed19b-108">Quando l'utente sposta il cursore all'interno della finestra, la routine della finestra riceve una serie di messaggi di [**WM \_ MOUSEMOVE**](../inputdev/wm-mousemove.md) .</span><span class="sxs-lookup"><span data-stu-id="ed19b-108">As the user moves the cursor within the window, the window procedure receives a series of [**WM\_MOUSEMOVE**](../inputdev/wm-mousemove.md) messages.</span></span> <span data-ttu-id="ed19b-109">Per ogni messaggio, la routine della finestra Disegna una linea che connette la posizione precedente e quella corrente.</span><span class="sxs-lookup"><span data-stu-id="ed19b-109">For each message, the window procedure draws a line connecting the previous position and the current position.</span></span> <span data-ttu-id="ed19b-110">Per creare la riga, la procedura usa [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) per recuperare un contesto di dispositivo di visualizzazione. quindi, non appena il disegno è completo e prima di restituire il messaggio, la procedura usa la funzione [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) per rilasciare il contesto del dispositivo di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="ed19b-110">To draw the line, the procedure uses [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) to retrieve a display device context; then, as soon as drawing is complete and before returning from the message, the procedure uses the [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) function to release the display device context.</span></span> <span data-ttu-id="ed19b-111">Non appena l'utente rilascia il pulsante del mouse, la routine della finestra Cancella il flag e il disegno viene arrestato (che invia il messaggio [**WM \_ LBUTTONUP**](../inputdev/wm-lbuttonup.md) ).</span><span class="sxs-lookup"><span data-stu-id="ed19b-111">As soon as the user releases the mouse button, the window procedure clears the flag, and the drawing stops (which sends the [**WM\_LBUTTONUP**](../inputdev/wm-lbuttonup.md) message).</span></span>


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



<span data-ttu-id="ed19b-112">Un'applicazione che consente il disegno, come in questo esempio, in genere registra i punti o le righe in modo che le linee possano essere ridisegnate ogni volta che la finestra viene aggiornata.</span><span class="sxs-lookup"><span data-stu-id="ed19b-112">An application that enables drawing, as in this example, typically records either the points or lines so that the lines can be redrawn whenever the window is updated.</span></span> <span data-ttu-id="ed19b-113">Il disegno di applicazioni spesso utilizza un contesto di dispositivo di memoria e una bitmap associata per archiviare le linee disegnate utilizzando un mouse.</span><span class="sxs-lookup"><span data-stu-id="ed19b-113">Drawing applications often use a memory device context and an associated bitmap to store lines that were drawn by using a mouse.</span></span>

 

 
