---
title: Come trascinare un Tree-View elemento
description: In questo argomento viene illustrato il codice per la gestione del trascinamento degli elementi della visualizzazione albero.
ms.assetid: 989BBC27-C025-4C54-9972-4725F04A5E95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23ee7cfc9d4fa7a6e73abd042df583ae9175de8583b050ff9621b7d2789e0d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413115"
---
# <a name="how-to-drag-a-tree-view-item"></a>Come trascinare un Tree-View elemento

In questo argomento viene illustrato il codice per la gestione del trascinamento degli elementi della visualizzazione albero. Il codice di esempio è costituito da tre funzioni. La prima funzione inizia l'operazione di trascinamento, la seconda funzione trascina l'immagine e la terza funzione termina l'operazione di trascinamento.

> [!Note]  
> Il trascinamento di un elemento della visualizzazione albero comporta in genere l'elaborazione del codice di notifica [TVN \_ BEGINDRAG](tvn-begindrag.md) (o [TVN \_ BEGINRDRAG),](tvn-beginrdrag.md)del messaggio [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) e del messaggio [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) (o [**WM \_ RBUTTONUP).**](/windows/desktop/inputdev/wm-rbuttonup) Implica anche l'uso delle [funzioni Elenchi](image-lists.md) immagini per disegnare l'elemento mentre viene trascinato.

 

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Windows Controlli](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Windows Interfaccia utente programmazione

## <a name="instructions"></a>Istruzioni

### <a name="step-1-beginning-the-tree-view-drag-operation"></a>Passaggio 1: Inizio dell'operazione di trascinamento della visualizzazione albero

Un controllo di visualizzazione albero invia alla finestra padre un codice di notifica [TVN \_ BEGINDRAG](tvn-begindrag.md) (o [TVN \_ BEGINRDRAG)](tvn-beginrdrag.md)ogni volta che l'utente inizia a trascinare un elemento. La finestra padre riceve la notifica sotto forma di messaggio [**WM \_ NOTIFY**](wm-notify.md) il cui *parametro lParam* è l'indirizzo di una [**struttura NMTREEVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) I membri di questa struttura includono le coordinate dello schermo del puntatore del mouse e una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che contiene informazioni sull'elemento da trascinare.

Nell'esempio seguente viene illustrato come elaborare il [**messaggio WM \_ NOTIFY**](wm-notify.md) per ottenere [TVN \_ BEGINDRAG.](tvn-begindrag.md)


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



L'avvio dell'operazione di trascinamento comporta [**l'uso della \_ funzione ImageList BeginDrag.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) I parametri della funzione includono l'handle per l'elenco di immagini che contiene l'immagine da usare durante l'operazione di trascinamento e l'indice dell'immagine. È possibile specificare un elenco di immagini e un'immagine personalizzati oppure è possibile fare in modo che il controllo di visualizzazione albero le crei automaticamente usando il messaggio [**TVM \_ CREATEDRAGIMAGE.**](tvm-createdragimage.md)

Poiché l'immagine di trascinamento sostituisce il puntatore del mouse per la durata dell'operazione di trascinamento, [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) richiede di specificare un'area sensibile all'interno dell'immagine. Le coordinate dell'area sensibile sono relative all'angolo superiore sinistro dell'immagine. **ImageList \_ BeginDrag** richiede anche di specificare la posizione iniziale dell'immagine di trascinamento. Un'applicazione imposta in genere la posizione iniziale in modo che l'area sensibile dell'immagine di trascinamento corrisponda a quella del puntatore del mouse nel momento in cui l'utente ha iniziato l'operazione di trascinamento.

La funzione seguente illustra come iniziare a trascinare un elemento della visualizzazione albero. Usa l'immagine di trascinamento fornita dal controllo di visualizzazione albero e ottiene il rettangolo di delimitazione dell'elemento per determinare il punto appropriato per l'area sensibile. Le dimensioni del rettangolo di delimitazione sono le stesse dell'immagine.

La funzione acquisisce l'input del mouse, causando l'invio di messaggi del mouse alla finestra padre. La finestra padre richiede i messaggi [**\_ WM MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) successivi per determinare dove trascinare l'immagine e il messaggio [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) per determinare quando terminare l'operazione di trascinamento.


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



### <a name="step-2-dragging-the-tree-view-item"></a>Passaggio 2: Trascinamento dell'elemento della visualizzazione albero

Trascinare un elemento della visualizzazione albero chiamando la funzione [**\_ ImageList DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) quando la finestra padre riceve un messaggio [**WM \_ MOUSEMOVE,**](/windows/desktop/inputdev/wm-mousemove) come illustrato nell'esempio seguente. L'esempio illustra anche come eseguire l'hit testing durante l'operazione di trascinamento per determinare se evidenziare altri elementi nella visualizzazione albero come destinazioni di un'operazione di trascinamento della selezione.


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



### <a name="step-3-ending-the-tree-view-drag-operation"></a>Passaggio 3: Terminazione dell'operazione di trascinamento della visualizzazione albero

Nell'esempio seguente viene illustrato come terminare un'operazione di trascinamento. La [**funzione \_ ImageList EndDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_enddrag) viene chiamata quando la finestra padre riceve un [**messaggio WM \_ LBUTTONUP.**](/windows/desktop/inputdev/wm-lbuttonup) L'handle del controllo di visualizzazione albero viene passato alla funzione .


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Tree-View personalizzati](using-treeview.md)
</dt> <dt>

[L'esempio CustDTv illustra il disegno personalizzato in un controllo Tree-View personalizzato](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 