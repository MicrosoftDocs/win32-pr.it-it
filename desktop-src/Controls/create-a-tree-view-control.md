---
title: Come creare un controllo Tree-View
description: Per creare un controllo di visualizzazione albero, usare la funzione CreateWindowEx, specificando il \_ valore di TreeView del WC per la classe Window.
ms.assetid: FEC3BF62-3085-47D4-B82E-7BD7B34B397D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136ec22cc4f3f88e57266a4c2ac88df542a39429
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118542"
---
# <a name="how-to-create-a-tree-view-control"></a><span data-ttu-id="c02fd-103">Come creare un controllo Tree-View</span><span class="sxs-lookup"><span data-stu-id="c02fd-103">How to Create a Tree-View Control</span></span>

<span data-ttu-id="c02fd-104">Per creare un controllo di visualizzazione albero, usare la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , specificando il valore di [**\_ TreeView del WC**](common-control-window-classes.md) per la classe Window.</span><span class="sxs-lookup"><span data-stu-id="c02fd-104">To create a tree-view control, use the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, specifying the [**WC\_TREEVIEW**](common-control-window-classes.md) value for the window class.</span></span> <span data-ttu-id="c02fd-105">La classe della finestra visualizzazione albero viene registrata nello spazio degli indirizzi dell'applicazione quando viene caricata la DLL del controllo comune.</span><span class="sxs-lookup"><span data-stu-id="c02fd-105">The tree-view window class is registered in the application's address space when the common control DLL is loaded.</span></span> <span data-ttu-id="c02fd-106">Per assicurarsi che la DLL venga caricata, utilizzare la funzione [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) .</span><span class="sxs-lookup"><span data-stu-id="c02fd-106">To ensure that the DLL is loaded, use the [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) function.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c02fd-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="c02fd-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c02fd-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="c02fd-108">Technologies</span></span>

-   [<span data-ttu-id="c02fd-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="c02fd-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="c02fd-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="c02fd-110">Prerequisites</span></span>

-   <span data-ttu-id="c02fd-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="c02fd-111">C/C++</span></span>
-   <span data-ttu-id="c02fd-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="c02fd-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="c02fd-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="c02fd-113">Instructions</span></span>

### <a name="create-an-instance-of-a-tree-view-control"></a><span data-ttu-id="c02fd-114">Creare un'istanza di un controllo Tree-View</span><span class="sxs-lookup"><span data-stu-id="c02fd-114">Create an Instance of a Tree-View Control</span></span>

<span data-ttu-id="c02fd-115">Nell'esempio seguente viene creato un controllo di visualizzazione albero che viene ridimensionato per adattarsi all'area client della finestra padre.</span><span class="sxs-lookup"><span data-stu-id="c02fd-115">The following example creates a tree-view control that is sized to fit the client area of the parent window.</span></span> <span data-ttu-id="c02fd-116">USA anche funzioni definite dall'applicazione per associare un elenco di immagini al controllo e aggiungere elementi al controllo.</span><span class="sxs-lookup"><span data-stu-id="c02fd-116">It also uses application-defined functions to associate an image list with the control and add items to the control.</span></span>


```C++
// Create a tree-view control. 
// Returns the handle to the new control if successful,
// or NULL otherwise. 
// hwndParent - handle to the control's parent window. 
// lpszFileName - name of the file to parse for tree-view items.
// g_hInst - the global instance handle.
// ID_TREEVIEW - the resource ID of the control.

HWND CreateATreeView(HWND hwndParent)
{ 
    RECT rcClient;  // dimensions of client area 
    HWND hwndTV;    // handle to tree-view control 

    // Ensure that the common control DLL is loaded. 
    InitCommonControls(); 

    // Get the dimensions of the parent window's client area, and create 
    // the tree-view control. 
    GetClientRect(hwndParent, &rcClient); 
    hwndTV = CreateWindowEx(0,
                            WC_TREEVIEW,
                            TEXT("Tree View"),
                            WS_VISIBLE | WS_CHILD | WS_BORDER | TVS_HASLINES, 
                            0, 
                            0, 
                            rcClient.right, 
                            rcClient.bottom,
                            hwndParent, 
                            (HMENU)ID_TREEVIEW, 
                            g_hInst, 
                            NULL); 

    // Initialize the image list, and add items to the control. 
    // InitTreeViewImageLists and InitTreeViewItems are application- 
    // defined functions, shown later. 
    if (!InitTreeViewImageLists(hwndTV) || 
                !InitTreeViewItems(hwndTV))
    { 
        DestroyWindow(hwndTV); 
        return FALSE; 
    } 
    return hwndTV;
} 
```



## <a name="remarks"></a><span data-ttu-id="c02fd-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="c02fd-117">Remarks</span></span>

<span data-ttu-id="c02fd-118">Quando si crea un controllo di visualizzazione struttura ad albero, è possibile inviare anche un messaggio [**WM \_ sefont**](/windows/desktop/winmsg/wm-setfont) per impostare il tipo di carattere da utilizzare per il testo.</span><span class="sxs-lookup"><span data-stu-id="c02fd-118">When you create a tree-view control, you can also send it a [**WM\_SETFONT**](/windows/desktop/winmsg/wm-setfont) message to set the font to be used for the text.</span></span> <span data-ttu-id="c02fd-119">È necessario inviare questo messaggio prima di inserire elementi.</span><span class="sxs-lookup"><span data-stu-id="c02fd-119">You should send this message before inserting any items.</span></span> <span data-ttu-id="c02fd-120">Per impostazione predefinita, una visualizzazione albero utilizza il carattere del titolo dell'icona.</span><span class="sxs-lookup"><span data-stu-id="c02fd-120">By default, a tree view uses the icon title font.</span></span> <span data-ttu-id="c02fd-121">Anche se è possibile personalizzare il tipo di carattere per elemento utilizzando [disegno personalizzato](custom-draw.md), il controllo di visualizzazione albero utilizza le dimensioni del tipo di carattere specificato dal messaggio **WM \_ sefont** per determinare la spaziatura e il layout.</span><span class="sxs-lookup"><span data-stu-id="c02fd-121">Although you can customize the font per-item by using [Custom Draw](custom-draw.md), the tree-view control uses the dimensions of the font specified by the **WM\_SETFONT** message to determine spacing and layout.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c02fd-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c02fd-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c02fd-123">Uso di controlli Tree-View</span><span class="sxs-lookup"><span data-stu-id="c02fd-123">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="c02fd-124">L'esempio CustDTv illustra il progetto personalizzato in un controllo Tree-View</span><span class="sxs-lookup"><span data-stu-id="c02fd-124">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 