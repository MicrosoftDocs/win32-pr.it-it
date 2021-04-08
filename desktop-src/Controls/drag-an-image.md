---
title: Come trascinare un'immagine
description: In questo argomento viene illustrato come trascinare un'immagine sullo schermo. Le funzioni di trascinamento spostano un'immagine in modo uniforme, in colore e senza lampeggiare del cursore. È possibile trascinare le immagini mascherate e non mascherate.
ms.assetid: 84AFA770-F495-4312-9631-3335BA8CC799
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da495ef9ee0895c04a856f456fcda3e3125f2957
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730666"
---
# <a name="how-to-drag-an-image"></a><span data-ttu-id="2eae7-105">Come trascinare un'immagine</span><span class="sxs-lookup"><span data-stu-id="2eae7-105">How to Drag an Image</span></span>

<span data-ttu-id="2eae7-106">In questo argomento viene illustrato come trascinare un'immagine sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="2eae7-106">This topic demonstrates how to drag an image on the screen.</span></span> <span data-ttu-id="2eae7-107">Le funzioni di trascinamento spostano un'immagine in modo uniforme, in colore e senza lampeggiare del cursore.</span><span class="sxs-lookup"><span data-stu-id="2eae7-107">The dragging functions move an image smoothly, in color, and without any flashing of the cursor.</span></span> <span data-ttu-id="2eae7-108">È possibile trascinare le immagini mascherate e non mascherate.</span><span class="sxs-lookup"><span data-stu-id="2eae7-108">Both masked and unmasked images can be dragged.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="2eae7-109">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="2eae7-109">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="2eae7-110">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="2eae7-110">Technologies</span></span>

-   [<span data-ttu-id="2eae7-111">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="2eae7-111">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="2eae7-112">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="2eae7-112">Prerequisites</span></span>

-   <span data-ttu-id="2eae7-113">C/C++</span><span class="sxs-lookup"><span data-stu-id="2eae7-113">C/C++</span></span>
-   <span data-ttu-id="2eae7-114">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="2eae7-114">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="2eae7-115">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="2eae7-115">Instructions</span></span>

### <a name="step-1-begin-the-drag-operation"></a><span data-ttu-id="2eae7-116">Passaggio 1: avviare l'operazione di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="2eae7-116">Step 1: Begin the drag operation.</span></span>

<span data-ttu-id="2eae7-117">Usare la [**funzione \_ BeginDrag di ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) per iniziare un'operazione di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="2eae7-117">Use the [**ImageList\_BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) function to begin a drag operation.</span></span>

<span data-ttu-id="2eae7-118">La funzione definita dall'utente nell'esempio di codice C++ seguente è progettata per essere chiamata in risposta a un messaggio di pulsante del mouse, ad esempio [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown).</span><span class="sxs-lookup"><span data-stu-id="2eae7-118">The user-defined function in the following C++ code example is intended to be called in response to a mouse button-down message, such as [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown).</span></span> <span data-ttu-id="2eae7-119">La funzione determina se l'utente ha fatto clic all'interno del rettangolo di delimitazione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2eae7-119">The function determines whether the user has clicked within the bounding rectangle of the image.</span></span> <span data-ttu-id="2eae7-120">Se l'utente ha fatto clic, la funzione acquisisce l'input del mouse, cancella l'immagine dall'area client e calcola la posizione per l'area sensibile all'interno dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="2eae7-120">If the user has clicked, the function captures the mouse input, erases the image from the client area, and calculates the position for the hot spot within the image.</span></span> <span data-ttu-id="2eae7-121">La funzione imposta l'area sensibile in modo che coincida con l'area sensibile del cursore del mouse.</span><span class="sxs-lookup"><span data-stu-id="2eae7-121">The function sets the hot spot to coincide with the hot spot of the mouse cursor.</span></span> <span data-ttu-id="2eae7-122">Quindi, la funzione inizia l'operazione di trascinamento chiamando [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag).</span><span class="sxs-lookup"><span data-stu-id="2eae7-122">Then the function begins the drag operation by calling [**ImageList\_BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag).</span></span>


```C++
// StartDragging - begins dragging a bitmap. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window in which the bitmap is dragged. 
// ptCur - coordinates of the cursor. 
// himl - handle to the image list. 
// 
// Global variables 
//     g_rcImage - bounding rectangle of the image to drag. 
//     g_nImage - index of the image. 
//     g_ptHotSpot - location of the image's hot spot. 
//     g_cxBorder and g_cyBorder - width and height of border. 
//     g_cyCaption and g_cyMenu - height of title bar and menu bar. 
extern RECT g_rcImage; 
extern int g_nImage; 
extern POINT g_ptHotSpot; 
 
BOOL StartDragging(HWND hwnd, POINT ptCur, HIMAGELIST himl) 
{ 
    // Return if the cursor is not in the bounding rectangle of 
    // the image. 
    if (!PtInRect(&g_rcImage, ptCur)) 
        return FALSE; 
 
    // Capture the mouse input. 
    SetCapture(hwnd); 
 
    // Erase the image from the client area. 
    InvalidateRect(hwnd, &g_rcImage, TRUE); 
    UpdateWindow(hwnd); 
 
    // Calculate the location of the hot spot, and save it. 
    g_ptHotSpot.x = ptCur.x - g_rcImage.left; 
    g_ptHotSpot.y = ptCur.y - g_rcImage.top; 
 
    // Begin the drag operation. 
    if (!ImageList_BeginDrag(himl, g_nImage, 
            g_ptHotSpot.x, g_ptHotSpot.y)) 
        return FALSE; 
 
    // Set the initial location of the image, and make it visible. 
    // Because the ImageList_DragEnter function expects coordinates to 
    // be relative to the upper-left corner of the given window, the 
    // width of the border, title bar, and menu bar need to be taken 
    // into account. 
    
    ImageList_DragEnter(hwnd, ptCur.x + g_cxBorder, 
        ptCur.y + g_cyBorder + g_cyCaption + g_cyMenu); 
 
    g_fDragging = TRUE; 
 
    return TRUE; 
} 
```



### <a name="step-2-move-the-image"></a><span data-ttu-id="2eae7-123">Passaggio 2: spostare l'immagine.</span><span class="sxs-lookup"><span data-stu-id="2eae7-123">Step 2: Move the image.</span></span>

<span data-ttu-id="2eae7-124">La [**funzione \_ DragMove di ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) sposta l'immagine in una nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="2eae7-124">The [**ImageList\_DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) function moves the image to a new location.</span></span>

<span data-ttu-id="2eae7-125">La funzione definita dall'utente nel seguente esempio di codice C++ è progettata per essere chiamata in risposta al messaggio di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) .</span><span class="sxs-lookup"><span data-stu-id="2eae7-125">The user-defined function in the following C++ code example is intended to be called in response to the [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message.</span></span> <span data-ttu-id="2eae7-126">Trascina l'immagine in una nuova posizione.</span><span class="sxs-lookup"><span data-stu-id="2eae7-126">It drags the image to a new location.</span></span>


```C++
// MoveTheImage - drags an image to the specified coordinates. 
// Returns TRUE if successful, or FALSE otherwise. 
// ptCur - new coordinates for the image. 
BOOL MoveTheImage(POINT ptCur) 
{ 
    if (!ImageList_DragMove(ptCur.x, ptCur.y)) 
        return FALSE; 
 
    return TRUE; 
} 

```



### <a name="step-3-end-the-drag-operation"></a><span data-ttu-id="2eae7-127">Passaggio 3: terminare l'operazione di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="2eae7-127">Step 3: End the drag operation.</span></span>

<span data-ttu-id="2eae7-128">La funzione definita dall'utente nell'esempio di codice C++ seguente chiama la [**funzione \_ EndDrag di ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) per terminare l'operazione di trascinamento.</span><span class="sxs-lookup"><span data-stu-id="2eae7-128">The user-defined function in the following C++ code example calls the [**ImageList\_EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) function to end the drag operation.</span></span> <span data-ttu-id="2eae7-129">Chiama quindi la funzione [**ImageList \_ DragLeave**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragleave) per sbloccare la finestra e nascondere l'immagine di trascinamento, consentendo di aggiornare la finestra.</span><span class="sxs-lookup"><span data-stu-id="2eae7-129">It then calls the [**ImageList\_DragLeave**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragleave) function to unlock the window and hide the drag image, allowing the window to be updated.</span></span>


```C++
// StopDragging - ends a drag operation and draws the image 
// at its final location. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwnd - handle to the window in which the bitmap is dragged. 
// himl - handle to the image list. 
// ptCur - coordinates of the cursor. 
// 
// Global variable 
//     g_ptHotSpot - location of the image's hot spot. 
 
extern POINT g_ptHotSpot; 
 
BOOL StopDragging(HWND hwnd, HIMAGELIST himl, POINT ptCur) 
{ 
    ImageList_EndDrag(); 
    ImageList_DragLeave(hwnd); 
 
    g_fDragging = FALSE; 
 
    DrawTheImage(hwnd, himl, ptCur.x - g_ptHotSpot.x, 
        ptCur.y - g_ptHotSpot.y); 
 
    ReleaseCapture(); 
    return TRUE; 
} 

```



## <a name="related-topics"></a><span data-ttu-id="2eae7-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2eae7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2eae7-131">Informazioni di riferimento sugli elenchi di immagini</span><span class="sxs-lookup"><span data-stu-id="2eae7-131">Image Lists Reference</span></span>](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[<span data-ttu-id="2eae7-132">Informazioni sugli elenchi di immagini</span><span class="sxs-lookup"><span data-stu-id="2eae7-132">About Image Lists</span></span>](image-lists.md)
</dt> <dt>

[<span data-ttu-id="2eae7-133">Uso degli elenchi di immagini</span><span class="sxs-lookup"><span data-stu-id="2eae7-133">Using Image Lists</span></span>](using-image-lists.md)
</dt> </dl>

 

 