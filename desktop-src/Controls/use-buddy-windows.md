---
title: Come usare le finestre di Buddy
description: Impostando altri controlli come finestre Buddy per un TrackBar, è possibile posizionare automaticamente tali controlli alle estremità del TrackBar come etichette.
ms.assetid: 5797AA55-BD8D-407A-8896-08EE0DDC7E30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eca9a4e3b3049f8d4cf7515879d91a096f5a9e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044548"
---
# <a name="how-to-use-buddy-windows"></a><span data-ttu-id="593fc-103">Come usare le finestre di Buddy</span><span class="sxs-lookup"><span data-stu-id="593fc-103">How to Use Buddy Windows</span></span>

<span data-ttu-id="593fc-104">Impostando altri controlli come finestre Buddy per un TrackBar, è possibile posizionare automaticamente tali controlli alle estremità del TrackBar come etichette.</span><span class="sxs-lookup"><span data-stu-id="593fc-104">By setting other controls as buddy windows for a trackbar, you can automatically position those controls at the ends of the trackbar as labels.</span></span>

<span data-ttu-id="593fc-105">Nella figura seguente vengono mostrati un TrackBar orizzontale e un TrackBar verticale, entrambi con controlli statici come finestre di contatto.</span><span class="sxs-lookup"><span data-stu-id="593fc-105">The following illustration shows a horizontal and a vertical trackbar, both with static controls as buddy windows.</span></span>

![screenshot che mostra una finestra di dialogo con un TrackBar orizzontale e un TrackBar verticale](images/tkb-buddy.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="593fc-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="593fc-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="593fc-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="593fc-108">Technologies</span></span>

-   [<span data-ttu-id="593fc-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="593fc-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="593fc-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="593fc-110">Prerequisites</span></span>

-   <span data-ttu-id="593fc-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="593fc-111">C/C++</span></span>
-   <span data-ttu-id="593fc-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="593fc-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="593fc-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="593fc-113">Instructions</span></span>

### <a name="use-buddy-windows"></a><span data-ttu-id="593fc-114">Usare le finestre di Buddy</span><span class="sxs-lookup"><span data-stu-id="593fc-114">Use Buddy Windows</span></span>

<span data-ttu-id="593fc-115">Nell'esempio di codice seguente vengono create le finestre di Buddy visualizzate nell'illustrazione.</span><span class="sxs-lookup"><span data-stu-id="593fc-115">The following code example creates the buddy windows shown in the illustration.</span></span>


```
void LabelTrackbarsWithBuddies(HWND hDlg)
{
    HWND hwndTrackbar;
    HWND hwndBuddy;
    
    const int staticWidth   = 50;
    const int staticHeight  = 20;

//======================================================
// For horizontal Trackbar.

    hwndTrackbar = GetDlgItem(hDlg, IDC_SLIDER1);

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Left", SS_RIGHT | WS_CHILD | WS_VISIBLE, 
                                    0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                                    
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)TRUE, (LPARAM)hwndBuddy);
    
    //-------------------------------------------------

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Right", SS_LEFT | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                                
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)FALSE, (LPARAM)hwndBuddy);
    
//======================================================    
// For vertical Trackbar.
    
    hwndTrackbar = GetDlgItem(hDlg, IDC_SLIDER2);

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Top", SS_CENTER | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                               
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)TRUE, (LPARAM)hwndBuddy);

    //-------------------------------------------------

    hwndBuddy = CreateWindowEx(0, L"STATIC", L"Bottom", SS_CENTER | WS_CHILD | WS_VISIBLE, 
                               0, 0, staticWidth, staticHeight, hDlg, NULL, g_hInst, NULL);
                               
    SendMessage(hwndTrackbar, TBM_SETBUDDY, (WPARAM)FALSE, (LPARAM)hwndBuddy);
}
```



## <a name="remarks"></a><span data-ttu-id="593fc-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="593fc-116">Remarks</span></span>

<span data-ttu-id="593fc-117">**IDC \_ SLIDER1** e **IDC \_ SLIDER2** sono trackbars creati nell'editor risorse.</span><span class="sxs-lookup"><span data-stu-id="593fc-117">**IDC\_SLIDER1** and **IDC\_SLIDER2** are trackbars created in the resource editor.</span></span>

## <a name="related-topics"></a><span data-ttu-id="593fc-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="593fc-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="593fc-119">Uso di controlli TrackBar</span><span class="sxs-lookup"><span data-stu-id="593fc-119">Using Trackbar Controls</span></span>](using-trackbar-controls.md)
</dt> </dl>

 

 




