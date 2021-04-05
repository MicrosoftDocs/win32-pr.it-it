---
title: Come creare un'interfaccia della tastiera per le barre di scorrimento standard
description: Anche se un controllo barra di scorrimento fornisce un'interfaccia di tastiera incorporata, non è presente una barra di scorrimento standard.
ms.assetid: 249D0077-6E61-479A-91D5-A4BD9752B82E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b739638d95d9f3e530718f8e9b9e6168069420
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103873005"
---
# <a name="how-to-create-a-keyboard-interface-for-standard-scroll-bars"></a><span data-ttu-id="600cd-103">Come creare un'interfaccia della tastiera per le barre di scorrimento standard</span><span class="sxs-lookup"><span data-stu-id="600cd-103">How to Create a Keyboard Interface for Standard Scroll Bars</span></span>

<span data-ttu-id="600cd-104">Anche se un controllo barra di scorrimento fornisce un'interfaccia di tastiera incorporata, non è presente una barra di scorrimento standard.</span><span class="sxs-lookup"><span data-stu-id="600cd-104">Although a scroll bar control provides a built-in keyboard interface, a standard scroll bar does not.</span></span> <span data-ttu-id="600cd-105">Per implementare un'interfaccia della tastiera per una barra di scorrimento standard, una routine della finestra deve elaborare il messaggio di [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) ed esaminare il codice della chiave virtuale specificato dal parametro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="600cd-105">To implement a keyboard interface for a standard scroll bar, a window procedure must process the [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message and examine the virtual-key code specified by the *wParam* parameter.</span></span> <span data-ttu-id="600cd-106">Se il codice della chiave virtuale corrisponde a un tasto di direzione, la routine della finestra Invia a se stessa un messaggio [**WM \_ HSCROLL**](wm-hscroll.md) o [**WM \_ VSCROLL**](wm-vscroll.md) con la parola meno ordinata del parametro *wParam* impostato sul codice di richiesta della barra di scorrimento appropriato.</span><span class="sxs-lookup"><span data-stu-id="600cd-106">If the virtual-key code corresponds to an arrow key, the window procedure sends itself a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message with the low-order word of the *wParam* parameter set to the appropriate scroll bar request code.</span></span>

<span data-ttu-id="600cd-107">Ad esempio, quando l'utente preme il tasto freccia su, la routine della finestra riceve un messaggio [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown) con *wParam* uguale a VK \_ .</span><span class="sxs-lookup"><span data-stu-id="600cd-107">For example, when the user presses the UP arrow key, the window procedure receives a [**WM\_KEYDOWN**](/windows/desktop/inputdev/wm-keydown) message with *wParam* equal to VK\_UP.</span></span> <span data-ttu-id="600cd-108">In risposta, la routine della finestra Invia a se stessa un messaggio [**WM \_ VSCROLL**](wm-vscroll.md) con la parola di ordine inferiore di *wParam* impostata sul \_ codice della richiesta di lineup SB.</span><span class="sxs-lookup"><span data-stu-id="600cd-108">In response, the window procedure sends itself a [**WM\_VSCROLL**](wm-vscroll.md) message with the low-order word of *wParam* set to the SB\_LINEUP request code.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="600cd-109">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="600cd-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="600cd-110">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="600cd-110">Technologies</span></span>

-   [<span data-ttu-id="600cd-111">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="600cd-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="600cd-112">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="600cd-112">Prerequisites</span></span>

-   <span data-ttu-id="600cd-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="600cd-113">C/C++</span></span>
-   <span data-ttu-id="600cd-114">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="600cd-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="600cd-115">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="600cd-115">Instructions</span></span>

### <a name="create-a-keyboard-interface-for-a-standard-scroll-bar"></a><span data-ttu-id="600cd-116">Creare un'interfaccia di tastiera per una barra di scorrimento standard</span><span class="sxs-lookup"><span data-stu-id="600cd-116">Create a Keyboard Interface for a Standard Scroll Bar</span></span>

<span data-ttu-id="600cd-117">Nell'esempio di codice seguente viene illustrato come includere un'interfaccia della tastiera per una barra di scorrimento standard.</span><span class="sxs-lookup"><span data-stu-id="600cd-117">The following code example demonstrates how to include a keyboard interface for a standard scroll bar.</span></span>


```C++
    case WM_KEYDOWN: 
    {
        WORD wScrollNotify = 0xFFFF;

        switch (wParam) 
        { 
            case VK_UP: 
                wScrollNotify = SB_LINEUP; 
                break; 
 
            case VK_PRIOR: 
                wScrollNotify = SB_PAGEUP; 
                break; 
 
            case VK_NEXT: 
                wScrollNotify = SB_PAGEDOWN; 
                break; 
 
            case VK_DOWN: 
                wScrollNotify = SB_LINEDOWN; 
                break; 
 
            case VK_HOME: 
                wScrollNotify = SB_TOP; 
                break; 
 
            case VK_END: 
                wScrollNotify = SB_BOTTOM; 
                break; 
        } 
 
        if (wScrollNotify != -1) 
            SendMessage(hwnd, WM_VSCROLL, MAKELONG(wScrollNotify, 0), 0L); 
 
        break; 
    }
```



## <a name="related-topics"></a><span data-ttu-id="600cd-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="600cd-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="600cd-119">Uso delle barre di scorrimento</span><span class="sxs-lookup"><span data-stu-id="600cd-119">Using Scroll Bars</span></span>](using-scroll-bars.md)
</dt> <dt>

<span data-ttu-id="600cd-120">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="600cd-120">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 