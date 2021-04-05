---
title: Come elaborare i messaggi di notifica TrackBar
description: I TrackBar inviano notifiche alla finestra padre delle azioni dell'utente inviando il messaggio padre a WM \_ HSCROLL o WM \_ VSCROLL.
ms.assetid: 83F47A3E-E607-49C2-A8B5-BC8A321D90BB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c723ad1bebb5c9f3ec8c4e7aefdc658e0881aef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709007"
---
# <a name="how-to-process-trackbar-notification-messages"></a><span data-ttu-id="1d339-103">Come elaborare i messaggi di notifica TrackBar</span><span class="sxs-lookup"><span data-stu-id="1d339-103">How to Process Trackbar Notification Messages</span></span>

<span data-ttu-id="1d339-104">I TrackBar inviano notifiche alla finestra padre delle azioni dell'utente inviando il messaggio padre a [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="1d339-104">Trackbars notify their parent window of user actions by sending the parent a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="1d339-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="1d339-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="1d339-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="1d339-106">Technologies</span></span>

-   [<span data-ttu-id="1d339-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="1d339-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="1d339-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="1d339-108">Prerequisites</span></span>

-   <span data-ttu-id="1d339-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="1d339-109">C/C++</span></span>
-   <span data-ttu-id="1d339-110">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="1d339-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="1d339-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="1d339-111">Instructions</span></span>

### <a name="process-trackbar-notification-messages"></a><span data-ttu-id="1d339-112">Messaggi di notifica del processo TrackBar</span><span class="sxs-lookup"><span data-stu-id="1d339-112">Process Trackbar Notification Messages</span></span>

<span data-ttu-id="1d339-113">L'esempio di codice seguente è una funzione che viene chiamata quando la finestra padre di TrackBar riceve un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="1d339-113">The following code example is a function that is called when the trackbar's parent window receives a [**WM\_HSCROLL**](wm-hscroll.md) message.</span></span> <span data-ttu-id="1d339-114">Il TrackBar in questo esempio ha lo stile [**TBS \_ ENABLESELRANGE**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="1d339-114">The trackbar in this example has the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span> <span data-ttu-id="1d339-115">La posizione del dispositivo di scorrimento viene confrontata con l'intervallo di selezione e il dispositivo di scorrimento viene spostato nella posizione iniziale o finale dell'intervallo di selezione, quando necessario.</span><span class="sxs-lookup"><span data-stu-id="1d339-115">The position of the slider is compared to the selection range, and the slider is moved to the starting or ending position of the selection range when necessary.</span></span>


```
// TBNotifications - handles trackbar notifications received 
// in the wParam parameter of WM_HSCROLL. This function simply 
// ensures that the slider remains within the selection range. 

VOID WINAPI TBNotifications( 
    WPARAM wParam,  // wParam of WM_HSCROLL message 
    HWND hwndTrack, // handle of trackbar window 
    UINT iSelMin,   // minimum value of trackbar selection 
    UINT iSelMax)   // maximum value of trackbar selection 
    { 
    DWORD dwPos;    // current position of slider 

    switch (LOWORD(wParam)) { 
    
        case TB_ENDTRACK:
          
            dwPos = SendMessage(hwndTrack, TBM_GETPOS, 0, 0); 
            
            if (dwPos > iSelMax) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMax); 
                    
            else if (dwPos < iSelMin) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMin); 
            
            break; 

        default: 
        
            break; 
        } 
} 
```



## <a name="remarks"></a><span data-ttu-id="1d339-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="1d339-116">Remarks</span></span>

<span data-ttu-id="1d339-117">Una finestra di dialogo che contiene un TrackBar di tipo con stile di visualizzazione di [**TBS \_**](trackbar-control-styles.md) può utilizzare questa funzione quando viene ricevuto un messaggio [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="1d339-117">A dialog box that contains a [**TBS\_VERT**](trackbar-control-styles.md) style trackbar can use this function when it receives a [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d339-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1d339-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d339-119">Uso di controlli TrackBar</span><span class="sxs-lookup"><span data-stu-id="1d339-119">Using Trackbar Controls</span></span>](using-trackbar-controls.md)
</dt> </dl>

 

 




