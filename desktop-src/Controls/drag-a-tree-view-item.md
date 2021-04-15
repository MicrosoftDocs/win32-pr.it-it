---
title: Come trascinare un elemento di Tree-View
description: In questo argomento viene illustrato il codice per la gestione del trascinamento e dell'eliminazione di elementi della visualizzazione albero.
ms.assetid: 989BBC27-C025-4C54-9972-4725F04A5E95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80cedc5f7ec750270ec5d9fb6f567bf473f8c13b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474478"
---
# <a name="how-to-drag-a-tree-view-item"></a><span data-ttu-id="58f14-103">Come trascinare un elemento di Tree-View</span><span class="sxs-lookup"><span data-stu-id="58f14-103">How to Drag a Tree-View Item</span></span>

<span data-ttu-id="58f14-104">In questo argomento viene illustrato il codice per la gestione del trascinamento e dell'eliminazione di elementi della visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="58f14-104">This topic demonstrates code for handling dragging and dropping of tree-view items.</span></span> <span data-ttu-id="58f14-105">Il codice di esempio è costituito da tre funzioni.</span><span class="sxs-lookup"><span data-stu-id="58f14-105">The sample code consists of three functions.</span></span> <span data-ttu-id="58f14-106">La prima funzione inizia l'operazione di trascinamento, la seconda funzione trascina l'immagine e la terza funzione termina l'operazione di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="58f14-106">The first function begins the drag operation, the second function drags the image, and the third function ends the drag operation.</span></span>

> [!Note]  
> <span data-ttu-id="58f14-107">Il trascinamento di un elemento della visualizzazione albero comporta in genere l'elaborazione del codice di notifica di [TVN \_ BEGINDRAG](tvn-begindrag.md) (o [TVN \_ BEGINRDRAG](tvn-beginrdrag.md)), del messaggio [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) e del messaggio [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (o [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)).</span><span class="sxs-lookup"><span data-stu-id="58f14-107">Dragging a tree-view item typically involves processing the [TVN\_BEGINDRAG](tvn-begindrag.md) (or [TVN\_BEGINRDRAG](tvn-beginrdrag.md)) notification code, the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message, and the [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (or [**WM\_RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)) message.</span></span> <span data-ttu-id="58f14-108">Comporta anche l'uso delle funzioni [elenchi di immagini](image-lists.md) per tracciare l'elemento durante il trascinamento.</span><span class="sxs-lookup"><span data-stu-id="58f14-108">It also involves using the [Image Lists](image-lists.md) functions to draw the item as it is being dragged.</span></span>

 

## <a name="what-you-need-to-know"></a><span data-ttu-id="58f14-109">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="58f14-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="58f14-110">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="58f14-110">Technologies</span></span>

-   [<span data-ttu-id="58f14-111">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="58f14-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="58f14-112">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="58f14-112">Prerequisites</span></span>

-   <span data-ttu-id="58f14-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="58f14-113">C/C++</span></span>
-   <span data-ttu-id="58f14-114">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="58f14-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="58f14-115">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="58f14-115">Instructions</span></span>

### <a name="step-1-beginning-the-tree-view-drag-operation"></a><span data-ttu-id="58f14-116">Passaggio 1: inizio dell'operazione di trascinamento della visualizzazione albero</span><span class="sxs-lookup"><span data-stu-id="58f14-116">Step 1: Beginning the tree-view drag operation</span></span>

<span data-ttu-id="58f14-117">Un controllo di visualizzazione albero invia alla finestra padre un codice di notifica di [TVN \_ BEGINDRAG](tvn-begindrag.md) (o [TVN \_ BEGINRDRAG](tvn-beginrdrag.md)) ogni volta che l'utente inizia a trascinare un elemento.</span><span class="sxs-lookup"><span data-stu-id="58f14-117">A tree-view control sends the parent window a [TVN\_BEGINDRAG](tvn-begindrag.md) (or [TVN\_BEGINRDRAG](tvn-beginrdrag.md)) notification code whenever the user starts to drag an item.</span></span> <span data-ttu-id="58f14-118">La finestra padre riceve la notifica nel formato di un messaggio [**di \_ notifica WM**](wm-notify.md) il cui parametro *lParam* è l'indirizzo di una struttura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="58f14-118">The parent window receives the notification in the form of a [**WM\_NOTIFY**](wm-notify.md) message whose *lParam* parameter is the address of an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="58f14-119">I membri di questa struttura includono le coordinate dello schermo del puntatore del mouse e una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che contiene informazioni sull'elemento da trascinare.</span><span class="sxs-lookup"><span data-stu-id="58f14-119">The members of this structure include the screen coordinates of the mouse pointer and a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains information about the item to be dragged.</span></span>

<span data-ttu-id="58f14-120">Nell'esempio seguente viene illustrato come elaborare il messaggio di [**\_ notifica WM**](wm-notify.md) per ottenere [TVN \_ BEGINDRAG](tvn-begindrag.md).</span><span class="sxs-lookup"><span data-stu-id="58f14-120">The following example shows how to process the [**WM\_NOTIFY**](wm-notify.md) message to obtain [TVN\_BEGINDRAG](tvn-begindrag.md).</span></span>


```C++
    case WM_NOTIFY: 
        switch (((LPNMHDR)lParam)->code) 
        {
            case TVN_BEGINDRAG:
                Main_OnBeginDrag(((LPNMHDR)lParam)->hwndFrom, (LPNMTREEVIEW)lParam);
                break;
        
            // Handle other cases here. 
        }
        break; 
```



<span data-ttu-id="58f14-121">L'inizio dell'operazione di trascinamento prevede l'uso della funzione [**\_ BeginDrag di ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) .</span><span class="sxs-lookup"><span data-stu-id="58f14-121">Beginning the drag operation involves using the [**ImageList\_BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) function.</span></span> <span data-ttu-id="58f14-122">I parametri della funzione includono l'handle per l'elenco di immagini che contiene l'immagine da usare durante l'operazione di trascinamento e l'indice dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="58f14-122">The function's parameters include the handle to the image list that contains the image to use during the drag operation and the index of the image.</span></span> <span data-ttu-id="58f14-123">È possibile specificare un elenco di immagini e un'immagine personalizzati oppure è possibile creare un controllo di visualizzazione albero usando il messaggio [**TVM \_ CREATEDRAGIMAGE**](tvm-createdragimage.md) .</span><span class="sxs-lookup"><span data-stu-id="58f14-123">You can either provide your own image list and image, or you can have the tree-view control create them for you by using the [**TVM\_CREATEDRAGIMAGE**](tvm-createdragimage.md) message.</span></span>

<span data-ttu-id="58f14-124">Poiché l'immagine di trascinamento sostituisce il puntatore del mouse per la durata dell'operazione di trascinamento, [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) richiede di specificare un'area sensibile all'interno dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="58f14-124">Because the drag image replaces the mouse pointer for the duration of the drag operation, [**ImageList\_BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) requires you to specify a hot spot within the image.</span></span> <span data-ttu-id="58f14-125">Le coordinate dell'area sensibile sono relative all'angolo superiore sinistro dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="58f14-125">The coordinates of the hot spot are relative to the upper left corner of the image.</span></span> <span data-ttu-id="58f14-126">**ImageList \_ Per BeginDrag** è inoltre necessario specificare la posizione iniziale dell'immagine di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="58f14-126">**ImageList\_BeginDrag** also requires you to specify the initial location of the drag image.</span></span> <span data-ttu-id="58f14-127">Un'applicazione in genere imposta la posizione iniziale in modo che l'area sensibile dell'immagine di trascinamento corrisponda a quella del puntatore del mouse nel momento in cui l'utente ha iniziato l'operazione di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="58f14-127">An application typically sets the initial location so that the hot spot of the drag image corresponds to that of the mouse pointer at the time the user began the drag operation.</span></span>

<span data-ttu-id="58f14-128">La funzione seguente illustra come iniziare a trascinare un elemento della visualizzazione struttura ad albero.</span><span class="sxs-lookup"><span data-stu-id="58f14-128">The following function demonstrates how to begin dragging a tree-view item.</span></span> <span data-ttu-id="58f14-129">Usa l'immagine di trascinamento fornita dal controllo di visualizzazione albero e ottiene il rettangolo delimitatore dell'elemento per determinare il punto appropriato per l'area sensibile.</span><span class="sxs-lookup"><span data-stu-id="58f14-129">It uses the drag image provided by the tree-view control and obtains the bounding rectangle of the item to determine the appropriate point for the hot spot.</span></span> <span data-ttu-id="58f14-130">Le dimensioni del rettangolo di delimitazione corrispondono a quelle dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="58f14-130">The dimensions of the bounding rectangle are the same as those of the image.</span></span>

<span data-ttu-id="58f14-131">La funzione acquisisce l'input del mouse, causando l'invio dei messaggi del mouse alla finestra padre.</span><span class="sxs-lookup"><span data-stu-id="58f14-131">The function captures mouse input, causing mouse messages to be sent to the parent window.</span></span> <span data-ttu-id="58f14-132">La finestra padre necessita dei messaggi di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) successivi per determinare dove trascinare l'immagine e il messaggio [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) per determinare quando terminare l'operazione di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="58f14-132">The parent window needs the subsequent [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages to determine where to drag the image and the [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) message to determine when to end the drag operation.</span></span>


```C++
// Begin dragging an item in a tree-view control. 
// hwndTV - handle to the image list. 
// lpnmtv - address of information about the item being dragged.
//
// g_fDragging -- global BOOL that specifies whether dragging is underway.

void Main_OnBeginDrag(HWND hwndTV, LPNMTREEVIEW lpnmtv)
{ 
    HIMAGELIST himl;    // handle to image list 
    RECT rcItem;        // bounding rectangle of item 

    // Tell the tree-view control to create an image to use 
    // for dragging. 
    himl = TreeView_CreateDragImage(hwndTV, lpnmtv->itemNew.hItem); 

    // Get the bounding rectangle of the item being dragged. 
    TreeView_GetItemRect(hwndTV, lpnmtv->itemNew.hItem, &rcItem, TRUE); 

    // Start the drag operation. 
    ImageList_BeginDrag(himl, 0, 0, 0);
    ImageList_DragEnter(hwndTV, lpnmtv->ptDrag.x, lpnmtv->ptDrag.x); 

    // Hide the mouse pointer, and direct mouse input to the 
    // parent window. 
    ShowCursor(FALSE); 
    SetCapture(GetParent(hwndTV)); 
    g_fDragging = TRUE; 

    return; 

} 
```



### <a name="step-2-dragging-the-tree-view-item"></a><span data-ttu-id="58f14-133">Passaggio 2: trascinamento dell'elemento della visualizzazione struttura ad albero</span><span class="sxs-lookup"><span data-stu-id="58f14-133">Step 2: Dragging the tree-view item</span></span>

<span data-ttu-id="58f14-134">Si trascina un elemento della visualizzazione struttura ad albero chiamando la funzione [**ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) quando la finestra padre riceve un messaggio di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) , come illustrato nell'esempio riportato di seguito.</span><span class="sxs-lookup"><span data-stu-id="58f14-134">You drag a tree-view item by calling the [**ImageList\_DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) function when the parent window receives a [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message, as the following example shows.</span></span> <span data-ttu-id="58f14-135">Nell'esempio viene inoltre illustrato come eseguire l'hit testing durante l'operazione di trascinamento per determinare se evidenziare altri elementi nella visualizzazione albero come destinazioni di un'operazione di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="58f14-135">The example also demonstrates how to perform hit testing during the drag operation to determine whether to highlight other items in the tree view as targets of a drag-and-drop operation.</span></span>


```C++
// Drag an item in a tree-view control, 
// highlighting the item that is the target. 
// hwndParent - handle to the parent window. 
// hwndTV - handle to the tree-view control.
// xCur and yCur - coordinates of the mouse pointer,
//     relative to the parent window. 
//
// g_fDragging - global BOOL that specifies whether dragging is underway.

void Main_OnMouseMove(HWND hwndParent, HWND hwndTV, LONG xCur, LONG yCur) 
{ 
    HTREEITEM htiTarget;  // Handle to target item. 
    TVHITTESTINFO tvht;   // Hit test information. 

    if (g_fDragging) 
    { 
       // Drag the item to the current position of the mouse pointer. 
       // First convert the dialog coordinates to control coordinates. 
       POINT point;
       point.x = xCur;
       point.y = yCur;
       ClientToScreen(hwndParent, &point);
       ScreenToClient(hwndTV, &point);
       ImageList_DragMove(point.x, point.y);
       // Turn off the dragged image so the background can be refreshed.
       ImageList_DragShowNolock(FALSE); 
                
        // Find out if the pointer is on the item. If it is, 
        // highlight the item as a drop target. 
        tvht.pt.x = point.x; 
        tvht.pt.y = point.y; 
        if ((htiTarget = TreeView_HitTest(hwndTV, &tvht)) != NULL) 
        { 
            TreeView_SelectDropTarget(hwndTV, htiTarget); 
        } 
        ImageList_DragShowNolock(TRUE);
    } 
    return; 
}
```



### <a name="step-3-ending-the-tree-view-drag-operation"></a><span data-ttu-id="58f14-136">Passaggio 3: fine dell'operazione di trascinamento della visualizzazione albero</span><span class="sxs-lookup"><span data-stu-id="58f14-136">Step 3: Ending the tree-view drag operation</span></span>

<span data-ttu-id="58f14-137">Nell'esempio seguente viene illustrato come terminare un'operazione di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="58f14-137">The following example shows how to end a drag operation.</span></span> <span data-ttu-id="58f14-138">La [**funzione \_ EndDrag di ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) viene chiamata quando la finestra padre riceve un messaggio [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) .</span><span class="sxs-lookup"><span data-stu-id="58f14-138">The [**ImageList\_EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) function is called when the parent window receives a [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) message.</span></span> <span data-ttu-id="58f14-139">L'handle del controllo di visualizzazione albero viene passato alla funzione.</span><span class="sxs-lookup"><span data-stu-id="58f14-139">The handle of the tree-view control is passed to the function.</span></span>


```C++
// Stops dragging a tree-view item, releases the 
// mouse capture, and shows the mouse pointer.
//
// g_fDragging - global BOOL that specifies whether dragging is underway.

void Main_OnLButtonUp(HWND hwndTV) 
{ 
    if (g_fDragging) 
    { 
        // Get destination item.
        HTREEITEM htiDest = TreeView_GetDropHilight(hwndTV);
        if (htiDest != NULL)
        {
            // To do: handle the actual moving of the dragged node.
        }
        ImageList_EndDrag(); 
        TreeView_SelectDropTarget(hwndTV, NULL);
        ReleaseCapture(); 
        ShowCursor(TRUE); 
        g_fDragging = FALSE; 
    } 
    return; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="58f14-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="58f14-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58f14-141">Uso di controlli Tree-View</span><span class="sxs-lookup"><span data-stu-id="58f14-141">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="58f14-142">L'esempio CustDTv illustra il progetto personalizzato in un controllo Tree-View</span><span class="sxs-lookup"><span data-stu-id="58f14-142">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 