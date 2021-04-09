---
title: Come creare un controllo Header
description: In questo argomento viene illustrato come creare un controllo intestazione e posizionarlo all'interno dell'area client della finestra padre.
ms.assetid: 094AF70C-2761-439E-A1E3-0FD04212FE87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bce9bf9d7b117f5f61766ca326b91b0d19a2c903
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104047623"
---
# <a name="how-to-create-a-header-control"></a><span data-ttu-id="37a52-103">Come creare un controllo Header</span><span class="sxs-lookup"><span data-stu-id="37a52-103">How to Create a Header Control</span></span>

<span data-ttu-id="37a52-104">In questo argomento viene illustrato come creare un controllo intestazione e posizionarlo all'interno dell'area client della finestra padre.</span><span class="sxs-lookup"><span data-stu-id="37a52-104">This topic demonstrates how to create a header control and position it within the parent window's client area.</span></span> <span data-ttu-id="37a52-105">È possibile creare un controllo Header usando la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e specificando la classe della finestra di [**\_ intestazione WC**](common-control-window-classes.md) e gli stili appropriati del [controllo intestazione](header-control-styles.md).</span><span class="sxs-lookup"><span data-stu-id="37a52-105">You can create a header control by using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function and specifying the [**WC\_HEADER**](common-control-window-classes.md) window class and the appropriate [header control styles](header-control-styles.md).</span></span> <span data-ttu-id="37a52-106">Questa classe della finestra viene registrata quando viene caricata la DLL del controllo comune.</span><span class="sxs-lookup"><span data-stu-id="37a52-106">This window class is registered when the common control DLL is loaded.</span></span> <span data-ttu-id="37a52-107">Per assicurarsi che questa DLL venga caricata, utilizzare la funzione [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) .</span><span class="sxs-lookup"><span data-stu-id="37a52-107">To ensure that this DLL is loaded, use the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="37a52-108">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="37a52-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="37a52-109">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="37a52-109">Technologies</span></span>

-   [<span data-ttu-id="37a52-110">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="37a52-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="37a52-111">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="37a52-111">Prerequisites</span></span>

-   <span data-ttu-id="37a52-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="37a52-112">C/C++</span></span>
-   <span data-ttu-id="37a52-113">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="37a52-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="37a52-114">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="37a52-114">Instructions</span></span>


<span data-ttu-id="37a52-115">Nell'esempio di codice C++ riportato di seguito viene prima chiamata la funzione [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) per caricare la dll del controllo comune.</span><span class="sxs-lookup"><span data-stu-id="37a52-115">The following C++ code example first calls the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function to load the common control DLL.</span></span> <span data-ttu-id="37a52-116">Chiama quindi la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) per creare un controllo Header.</span><span class="sxs-lookup"><span data-stu-id="37a52-116">It then calls the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function to create a header control.</span></span> <span data-ttu-id="37a52-117">Il controllo viene inizialmente nascosto.</span><span class="sxs-lookup"><span data-stu-id="37a52-117">The control is initially hidden.</span></span> <span data-ttu-id="37a52-118">Il messaggio di [**\_ layout HDM**](hdm-layout.md) viene utilizzato per calcolare le dimensioni e la posizione del controllo all'interno della finestra padre.</span><span class="sxs-lookup"><span data-stu-id="37a52-118">The [**HDM\_LAYOUT**](hdm-layout.md) message is used to calculate the size and position of the control within the parent window.</span></span> <span data-ttu-id="37a52-119">Il controllo viene quindi riposizionato e reso visibile.</span><span class="sxs-lookup"><span data-stu-id="37a52-119">The control is then repositioned and made visible.</span></span>



```C++
// DoCreateHeader - creates a header control that is positioned along 
//     the top of the parent window's client area. 
// Returns the handle to the header control. 
// hwndParent - handle to the parent window. 
// 
// Global variable 
//    g_hinst - handle to the application instance 
extern HINSTANCE g_hinst; 
//
// child-window identifier
int ID_HEADER;
//
HWND DoCreateHeader(HWND hwndParent) 
{ 
        HWND hwndHeader; 
        RECT rcParent; 
        HDLAYOUT hdl; 
        WINDOWPOS wp; 
 
        // Ensure that the common control DLL is loaded, and then create 
        // the header control. 
        INITCOMMONCONTROLSEX icex;  //declare an INITCOMMONCONTROLSEX Structure
        icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
        icex.dwICC = ICC_LISTVIEW_CLASSES;   //set dwICC member to ICC_LISTVIEW_CLASSES    
                                             // this loads list-view and header control classes.
    InitCommonControlsEx(&icex); 
 
        if ((hwndHeader = CreateWindowEx(0, WC_HEADER, (LPCTSTR) NULL, 
                WS_CHILD | WS_BORDER | HDS_BUTTONS | HDS_HORZ, 
                0, 0, 0, 0, hwndParent, (HMENU) ID_HEADER, g_hinst, 
                (LPVOID) NULL)) == NULL) 
            return (HWND) NULL; 
 
        // Retrieve the bounding rectangle of the parent window's 
        // client area, and then request size and position values 
        // from the header control. 
        GetClientRect(hwndParent, &rcParent); 
 
        hdl.prc = &rcParent; 
        hdl.pwpos = &wp; 
        if (!SendMessage(hwndHeader, HDM_LAYOUT, 0, (LPARAM) &hdl)) 
            return (HWND) NULL; 
 
        // Set the size, position, and visibility of the header control. 
        SetWindowPos(hwndHeader, wp.hwndInsertAfter, wp.x, wp.y, 
            wp.cx, wp.cy, wp.flags | SWP_SHOWWINDOW); 
 
        return hwndHeader; 
}
```



## <a name="related-topics"></a><span data-ttu-id="37a52-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="37a52-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37a52-121">Informazioni sui controlli intestazione</span><span class="sxs-lookup"><span data-stu-id="37a52-121">About Header Controls</span></span>](header-controls.md)
</dt> <dt>

[<span data-ttu-id="37a52-122">Riferimento al controllo intestazione</span><span class="sxs-lookup"><span data-stu-id="37a52-122">Header Control Reference</span></span>](bumper-header-control-header-control-reference.md)
</dt> <dt>

[<span data-ttu-id="37a52-123">Uso di controlli Header</span><span class="sxs-lookup"><span data-stu-id="37a52-123">Using Header Controls</span></span>](using-header-controls.md)
</dt> </dl>

 

 