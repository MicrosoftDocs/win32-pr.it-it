---
title: Come creare un TrackBar
description: Quando viene creato il TrackBar, viene inizializzato sia l'intervallo che l'intervallo di selezione. Anche le dimensioni della pagina sono impostate in questo momento.
ms.assetid: FA110B4A-D3D7-49D8-A3DC-368099F6DA1E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9468ff044b94837f54d04cda4a9105f15410692
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044290"
---
# <a name="how-to-create-a-trackbar"></a><span data-ttu-id="7895e-104">Come creare un TrackBar</span><span class="sxs-lookup"><span data-stu-id="7895e-104">How to Create a Trackbar</span></span>

<span data-ttu-id="7895e-105">Quando viene creato il TrackBar, viene inizializzato sia l'intervallo che l'intervallo di selezione.</span><span class="sxs-lookup"><span data-stu-id="7895e-105">When the trackbar is created, both its range and its selection range are initialized.</span></span> <span data-ttu-id="7895e-106">Anche le dimensioni della pagina sono impostate in questo momento.</span><span class="sxs-lookup"><span data-stu-id="7895e-106">The page size is also set at this time.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="7895e-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="7895e-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7895e-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="7895e-108">Technologies</span></span>

-   [<span data-ttu-id="7895e-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="7895e-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="7895e-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="7895e-110">Prerequisites</span></span>

-   <span data-ttu-id="7895e-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="7895e-111">C/C++</span></span>
-   <span data-ttu-id="7895e-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="7895e-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="7895e-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="7895e-113">Instructions</span></span>

### <a name="create-a-trackbar"></a><span data-ttu-id="7895e-114">Creare un TrackBar</span><span class="sxs-lookup"><span data-stu-id="7895e-114">Create a Trackbar</span></span>

<span data-ttu-id="7895e-115">Nell'esempio seguente viene illustrato come creare un TrackBar con gli [**stili \_ TBS**](trackbar-control-styles.md) [**\_ autoENABLESELRANGE e TBS**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="7895e-115">The following example shows how to create a trackbar with the [**TBS\_AUTOTICKS**](trackbar-control-styles.md) and [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) styles.</span></span>


```
// CreateTrackbar - creates and initializes a trackbar. 
// 
// Global variable
//     g_hinst - instance handle
//
HWND WINAPI CreateTrackbar( 
    HWND hwndDlg,  // handle of dialog box (parent window) 
    UINT iMin,     // minimum value in trackbar range 
    UINT iMax,     // maximum value in trackbar range 
    UINT iSelMin,  // minimum value in trackbar selection 
    UINT iSelMax)  // maximum value in trackbar selection 
{ 

    InitCommonControls(); // loads common control's DLL 

    hwndTrack = CreateWindowEx( 
        0,                               // no extended styles 
        TRACKBAR_CLASS,                  // class name 
        "Trackbar Control",              // title (caption) 
        WS_CHILD | 
        WS_VISIBLE | 
        TBS_AUTOTICKS | 
        TBS_ENABLESELRANGE,              // style 
        10, 10,                          // position 
        200, 30,                         // size 
        hwndDlg,                         // parent window 
        ID_TRACKBAR,                     // control identifier 
        g_hinst,                         // instance 
        NULL                             // no WM_CREATE parameter 
        ); 

    SendMessage(hwndTrack, TBM_SETRANGE, 
        (WPARAM) TRUE,                   // redraw flag 
        (LPARAM) MAKELONG(iMin, iMax));  // min. & max. positions
        
    SendMessage(hwndTrack, TBM_SETPAGESIZE, 
        0, (LPARAM) 4);                  // new page size 

    SendMessage(hwndTrack, TBM_SETSEL, 
        (WPARAM) FALSE,                  // redraw flag 
        (LPARAM) MAKELONG(iSelMin, iSelMax)); 
        
    SendMessage(hwndTrack, TBM_SETPOS, 
        (WPARAM) TRUE,                   // redraw flag 
        (LPARAM) iSelMin); 

    SetFocus(hwndTrack); 

    return hwndTrack; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="7895e-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7895e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7895e-117">Uso di controlli TrackBar</span><span class="sxs-lookup"><span data-stu-id="7895e-117">Using Trackbar Controls</span></span>](using-trackbar-controls.md)
</dt> </dl>

 

 




