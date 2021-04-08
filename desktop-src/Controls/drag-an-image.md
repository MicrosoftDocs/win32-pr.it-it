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
# <a name="how-to-drag-an-image"></a>Come trascinare un'immagine

In questo argomento viene illustrato come trascinare un'immagine sullo schermo. Le funzioni di trascinamento spostano un'immagine in modo uniforme, in colore e senza lampeggiare del cursore. È possibile trascinare le immagini mascherate e non mascherate.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="step-1-begin-the-drag-operation"></a>Passaggio 1: avviare l'operazione di trascinamento.

Usare la [**funzione \_ BeginDrag di ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) per iniziare un'operazione di trascinamento.

La funzione definita dall'utente nell'esempio di codice C++ seguente è progettata per essere chiamata in risposta a un messaggio di pulsante del mouse, ad esempio [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown). La funzione determina se l'utente ha fatto clic all'interno del rettangolo di delimitazione dell'immagine. Se l'utente ha fatto clic, la funzione acquisisce l'input del mouse, cancella l'immagine dall'area client e calcola la posizione per l'area sensibile all'interno dell'immagine. La funzione imposta l'area sensibile in modo che coincida con l'area sensibile del cursore del mouse. Quindi, la funzione inizia l'operazione di trascinamento chiamando [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag).


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



### <a name="step-2-move-the-image"></a>Passaggio 2: spostare l'immagine.

La [**funzione \_ DragMove di ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) sposta l'immagine in una nuova posizione.

La funzione definita dall'utente nel seguente esempio di codice C++ è progettata per essere chiamata in risposta al messaggio di [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) . Trascina l'immagine in una nuova posizione.


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



### <a name="step-3-end-the-drag-operation"></a>Passaggio 3: terminare l'operazione di trascinamento.

La funzione definita dall'utente nell'esempio di codice C++ seguente chiama la [**funzione \_ EndDrag di ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) per terminare l'operazione di trascinamento. Chiama quindi la funzione [**ImageList \_ DragLeave**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragleave) per sbloccare la finestra e nascondere l'immagine di trascinamento, consentendo di aggiornare la finestra.


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sugli elenchi di immagini](bumper-image-lists-image-lists-reference.md)
</dt> <dt>

[Informazioni sugli elenchi di immagini](image-lists.md)
</dt> <dt>

[Uso degli elenchi di immagini](using-image-lists.md)
</dt> </dl>

 

 