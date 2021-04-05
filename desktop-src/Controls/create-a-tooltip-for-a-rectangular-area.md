---
title: Come creare una descrizione comando per un'area rettangolare
description: Nell'esempio seguente viene illustrato come creare un controllo ToolTip standard per l'intera area client di una finestra.
ms.assetid: 6AF1CE6E-AD63-4F84-9759-14FE4F16092B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f8daf62bf2ba85c8750fd07a1b9122b0360fc11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708653"
---
# <a name="how-to-create-a-tooltip-for-a-rectangular-area"></a><span data-ttu-id="997d3-103">Come creare una descrizione comando per un'area rettangolare</span><span class="sxs-lookup"><span data-stu-id="997d3-103">How to Create a Tooltip for a Rectangular Area</span></span>

<span data-ttu-id="997d3-104">Nell'esempio seguente viene illustrato come creare un controllo ToolTip standard per l'intera area client di una finestra.</span><span class="sxs-lookup"><span data-stu-id="997d3-104">The following example demonstrates how to create a standard tooltip control for a window's entire client area.</span></span>

<span data-ttu-id="997d3-105">Nella figura seguente viene illustrata la descrizione comando visualizzata quando il puntatore del mouse si trova all'interno della finestra client di una finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="997d3-105">The following illustration shows the tooltip that is displayed when the mouse pointer is within the client window of a dialog box.</span></span> <span data-ttu-id="997d3-106">L'handle della finestra di dialogo è stato passato alla funzione illustrata nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="997d3-106">The handle of the dialog box was passed to the function shown in the preceding example.</span></span>

![Screenshot di una finestra di dialogo; il puntatore del mouse si trova all'interno della finestra client e una descrizione comando è visibile](images/tt-rectangle.png)

## <a name="what-you-need-to-know"></a><span data-ttu-id="997d3-108">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="997d3-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="997d3-109">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="997d3-109">Technologies</span></span>

-   [<span data-ttu-id="997d3-110">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="997d3-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="997d3-111">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="997d3-111">Prerequisites</span></span>

-   <span data-ttu-id="997d3-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="997d3-112">C/C++</span></span>
-   <span data-ttu-id="997d3-113">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="997d3-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="997d3-114">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="997d3-114">Instructions</span></span>

### <a name="create-a-tooltip-for-a-rectangular-area"></a><span data-ttu-id="997d3-115">Creare una descrizione comando per un'area rettangolare</span><span class="sxs-lookup"><span data-stu-id="997d3-115">Create a Tooltip for a Rectangular Area</span></span>

<span data-ttu-id="997d3-116">Nell'esempio seguente viene illustrato come creare un controllo ToolTip standard per l'intera area client di una finestra.</span><span class="sxs-lookup"><span data-stu-id="997d3-116">The following example demonstrates how to create a standard tooltip control for a window's entire client area.</span></span>


```C++
void CreateToolTipForRect(HWND hwndParent)
{
    // Create a tooltip.
    HWND hwndTT = CreateWindowEx(WS_EX_TOPMOST, TOOLTIPS_CLASS, NULL, 
                                 WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP, 
                                 CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
                                 hwndParent, NULL, g_hInst,NULL);

    SetWindowPos(hwndTT, HWND_TOPMOST, 0, 0, 0, 0, 
                 SWP_NOMOVE | SWP_NOSIZE | SWP_NOACTIVATE);

    // Set up "tool" information. In this case, the "tool" is the entire parent window.
    
    TOOLINFO ti = { 0 };
    ti.cbSize   = sizeof(TOOLINFO);
    ti.uFlags   = TTF_SUBCLASS;
    ti.hwnd     = hwndParent;
    ti.hinst    = g_hInst;
    ti.lpszText = TEXT("This is your tooltip string.");;
    
    GetClientRect (hwndParent, &ti.rect);

    // Associate the tooltip with the "tool" window.
    SendMessage(hwndTT, TTM_ADDTOOL, 0, (LPARAM) (LPTOOLINFO) &ti); 
} 
```



## <a name="related-topics"></a><span data-ttu-id="997d3-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="997d3-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="997d3-118">Uso di controlli ToolTip</span><span class="sxs-lookup"><span data-stu-id="997d3-118">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 




