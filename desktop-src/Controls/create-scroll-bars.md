---
title: Come creare barre di scorrimento
description: Quando si crea una finestra sovrapposta, popup o figlio, è possibile aggiungere barre di scorrimento standard usando la funzione CreateWindowEx e specificando WS \_ HSCROLL, WS \_ VSCROLL o entrambi gli stili.
ms.assetid: 58353030-DCF5-4368-9658-BB282B8B5EF0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b27e3e6d9495492f46567633cc53b0f3f7c5bd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474430"
---
# <a name="how-to-create-scroll-bars"></a><span data-ttu-id="c8ecd-103">Come creare barre di scorrimento</span><span class="sxs-lookup"><span data-stu-id="c8ecd-103">How to Create Scroll Bars</span></span>

<span data-ttu-id="c8ecd-104">Quando si crea una finestra sovrapposta, popup o figlio, è possibile aggiungere barre di scorrimento standard usando la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e specificando WS \_ HSCROLL, WS \_ VSCROLL o entrambi gli stili.</span><span class="sxs-lookup"><span data-stu-id="c8ecd-104">When creating an overlapped, pop-up, or child window, you can add standard scroll bars by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specifying WS\_HSCROLL, WS\_VSCROLL, or both styles.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c8ecd-105">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="c8ecd-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c8ecd-106">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="c8ecd-106">Technologies</span></span>

-   [<span data-ttu-id="c8ecd-107">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="c8ecd-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="c8ecd-108">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="c8ecd-108">Prerequisites</span></span>

-   <span data-ttu-id="c8ecd-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="c8ecd-109">C/C++</span></span>
-   <span data-ttu-id="c8ecd-110">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="c8ecd-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="c8ecd-111">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="c8ecd-111">Instructions</span></span>

### <a name="create-a-scroll-bar"></a><span data-ttu-id="c8ecd-112">Creare una barra di scorrimento</span><span class="sxs-lookup"><span data-stu-id="c8ecd-112">Create a Scroll Bar</span></span>

<span data-ttu-id="c8ecd-113">Nell'esempio seguente viene creata una finestra con barre di scorrimento orizzontali e verticali standard.</span><span class="sxs-lookup"><span data-stu-id="c8ecd-113">The following example creates a window with standard horizontal and vertical scroll bars.</span></span>


```C++
    hwnd = CreateWindowEx( 
        0,                     // no extended styles 
        g_szWindowClass,       // global string containing name of window class
        g_szTitle,             // global string containing title bar text 
        WS_OVERLAPPEDWINDOW |  
            WS_HSCROLL | WS_VSCROLL, // window styles 
        CW_USEDEFAULT,         // default horizontal position 
        CW_USEDEFAULT,         // default vertical position 
        CW_USEDEFAULT,         // default width 
        CW_USEDEFAULT,         // default height 
        (HWND) NULL,           // no parent for overlapped windows 
        (HMENU) NULL,          // use the window class menu 
        g_hInst,               // global instance handle  
        (PVOID) NULL           // pointer not needed 
    ); 
```



<span data-ttu-id="c8ecd-114">Per elaborare i messaggi della barra di scorrimento per queste barre di scorrimento, è necessario includere il codice appropriato nella procedura della finestra principale.</span><span class="sxs-lookup"><span data-stu-id="c8ecd-114">To process scroll bar messages for these scroll bars, you must include appropriate code in the main window procedure.</span></span>

<span data-ttu-id="c8ecd-115">È possibile utilizzare la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare una barra di scorrimento specificando la classe della finestra della barra di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="c8ecd-115">You can use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create a scroll bar by specifying the SCROLLBAR window class.</span></span> <span data-ttu-id="c8ecd-116">In questo modo viene creata una barra di scorrimento orizzontale o verticale, a seconda che [**SBS \_ orizzontalmente**](scroll-bar-control-styles.md) o [**SBS \_ Vert**](scroll-bar-control-styles.md) sia specificato come stile della finestra.</span><span class="sxs-lookup"><span data-stu-id="c8ecd-116">This creates a horizontal or vertical scroll bar, depending on whether [**SBS\_HORZ**](scroll-bar-control-styles.md) or [**SBS\_VERT**](scroll-bar-control-styles.md) is specified as the window style.</span></span> <span data-ttu-id="c8ecd-117">È possibile specificare anche le dimensioni della barra di scorrimento e la relativa posizione rispetto alla finestra padre.</span><span class="sxs-lookup"><span data-stu-id="c8ecd-117">The scroll bar size and its position relative to its parent window can also be specified.</span></span>

<span data-ttu-id="c8ecd-118">Nell'esempio seguente viene creata una barra di scorrimento orizzontale posizionata lungo la parte inferiore dell'area client della finestra padre.</span><span class="sxs-lookup"><span data-stu-id="c8ecd-118">The following example creates a horizontal scroll bar that is positioned along the bottom of the parent window's client area.</span></span>


```C++
// Description:
//   Creates a horizontal scroll bar along the bottom of the parent 
//   window's area.
// Parameters:
//   hwndParent - handle to the parent window.
//   sbHeight - height, in pixels, of the scroll bar.
// Returns:
//   The handle to the scroll bar.
HWND CreateAHorizontalScrollBar(HWND hwndParent, int sbHeight)
{
    RECT rect;

    // Get the dimensions of the parent window's client area;
    if (!GetClientRect(hwndParent, &rect))
        return NULL;

    // Create the scroll bar.
    return (CreateWindowEx( 
            0,                      // no extended styles 
            L"SCROLLBAR",           // scroll bar control class 
            (PTSTR) NULL,           // no window text 
            WS_CHILD | WS_VISIBLE   // window styles  
                | SBS_HORZ,         // horizontal scroll bar style 
            rect.left,              // horizontal position 
            rect.bottom - sbHeight, // vertical position 
            rect.right,             // width of the scroll bar 
            sbHeight,               // height of the scroll bar
            hwndParent,             // handle to main window 
            (HMENU) NULL,           // no menu 
            g_hInst,                // instance owning this window 
            (PVOID) NULL            // pointer not needed 
        )); 
}
```



## <a name="related-topics"></a><span data-ttu-id="c8ecd-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c8ecd-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8ecd-120">Uso delle barre di scorrimento</span><span class="sxs-lookup"><span data-stu-id="c8ecd-120">Using Scroll Bars</span></span>](using-scroll-bars.md)
</dt> <dt>

<span data-ttu-id="c8ecd-121">[Demo sui controlli comuni di Windows (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="c8ecd-121">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 