---
title: Come aggiungere elementi di Tree-View
description: Aggiungere un elemento a un controllo di visualizzazione albero inviando il \_ messaggio di INSERTITEM INSERTITEM al controllo.
ms.assetid: CD6376F4-8B1A-489D-8538-6C1620E98F76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a7da0846b57f422de83984b197df0770286882
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104398642"
---
# <a name="how-to-add-tree-view-items"></a>Come aggiungere elementi di Tree-View

Aggiungere un elemento a un controllo di visualizzazione albero inviando il messaggio [**di \_ INSERTITEM INSERTITEM**](tvm-insertitem.md) al controllo. Il messaggio include l'indirizzo di una struttura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) , specificando l'elemento padre, l'elemento dopo il quale viene inserito il nuovo elemento e una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che definisce gli attributi dell'elemento. Gli attributi includono l'etichetta dell'elemento, le immagini selezionate e non selezionate e un valore definito dall'applicazione a 32 bit.

## <a name="what-you-need-to-know"></a>Informazioni importanti

### <a name="technologies"></a>Tecnologie

-   [Controlli Windows](window-controls.md)

### <a name="prerequisites"></a>Prerequisiti

-   C/C++
-   Programmazione dell'interfaccia utente di Windows

## <a name="instructions"></a>Istruzioni

### <a name="add-items-to-the-tree-view"></a>Aggiungere elementi al Tree-View

Nell'esempio riportato in questa sezione viene illustrato come creare una tabella di contenuti in base alle informazioni sull'intestazione del documento fornite in una matrice definita dall'applicazione. Ogni elemento della matrice è costituito da una stringa di intestazione e da un numero intero che indica il livello di intestazione. L'esempio supporta tre livelli di intestazione (1, 2 e 3).

Nell'esempio sono incluse due funzioni. La prima funzione estrae ogni intestazione e il livello di intestazione associato, quindi li passa alla seconda funzione.

La seconda funzione aggiunge un elemento a un controllo di visualizzazione albero. Usa il testo dell'intestazione come etichetta dell'elemento e usa il livello di intestazione per determinare l'elemento padre per il nuovo elemento. Viene aggiunta un'intestazione Level One alla radice del controllo di visualizzazione ad albero, viene aggiunta un'intestazione di livello due come elemento figlio del livello precedente e così via. La funzione assegna un'immagine a un elemento a seconda che disponga di elementi figlio. Se un elemento ha elementi figlio, ottiene un'immagine che rappresenta una cartella chiusa. In caso contrario, ottiene un'immagine che rappresenta un documento. Un elemento usa la stessa immagine per gli Stati selezionato e non selezionato.


```C++
// Adds items to a tree-view control. 
// Returns the handle to the newly added item. 
// hwndTV - handle to the tree-view control. 
// lpszItem - text of the item to add. 
// nLevel - level at which to add the item. 
//
// g_nClosed, and g_nDocument - global indexes of the images.

HTREEITEM AddItemToTree(HWND hwndTV, LPTSTR lpszItem, int nLevel)
{ 
    TVITEM tvi; 
    TVINSERTSTRUCT tvins; 
    static HTREEITEM hPrev = (HTREEITEM)TVI_FIRST; 
    static HTREEITEM hPrevRootItem = NULL; 
    static HTREEITEM hPrevLev2Item = NULL; 
    HTREEITEM hti; 

    tvi.mask = TVIF_TEXT | TVIF_IMAGE 
               | TVIF_SELECTEDIMAGE | TVIF_PARAM; 

    // Set the text of the item. 
    tvi.pszText = lpszItem; 
    tvi.cchTextMax = sizeof(tvi.pszText)/sizeof(tvi.pszText[0]); 

    // Assume the item is not a parent item, so give it a 
    // document image. 
    tvi.iImage = g_nDocument; 
    tvi.iSelectedImage = g_nDocument; 

    // Save the heading level in the item's application-defined 
    // data area. 
    tvi.lParam = (LPARAM)nLevel; 
    tvins.item = tvi; 
    tvins.hInsertAfter = hPrev; 

    // Set the parent item based on the specified level. 
    if (nLevel == 1) 
        tvins.hParent = TVI_ROOT; 
    else if (nLevel == 2) 
        tvins.hParent = hPrevRootItem; 
    else 
        tvins.hParent = hPrevLev2Item; 

    // Add the item to the tree-view control. 
    hPrev = (HTREEITEM)SendMessage(hwndTV, TVM_INSERTITEM, 
        0, (LPARAM)(LPTVINSERTSTRUCT)&tvins); 

    if (hPrev == NULL)
        return NULL;

    // Save the handle to the item. 
    if (nLevel == 1) 
        hPrevRootItem = hPrev; 
    else if (nLevel == 2) 
        hPrevLev2Item = hPrev; 

    // The new item is a child item. Give the parent item a 
    // closed folder bitmap to indicate it now has child items. 
    if (nLevel > 1)
    { 
        hti = TreeView_GetParent(hwndTV, hPrev); 
        tvi.mask = TVIF_IMAGE | TVIF_SELECTEDIMAGE; 
        tvi.hItem = hti; 
        tvi.iImage = g_nClosed; 
        tvi.iSelectedImage = g_nClosed; 
        TreeView_SetItem(hwndTV, &tvi); 
    } 

    return hPrev; 
} 

// Extracts heading text and heading levels from a global 
// array and passes them to a function that adds them as
// parent and child items to a tree-view control. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwndTV - handle to the tree-view control. 

BOOL InitTreeViewItems(HWND hwndTV)
{ 
    HTREEITEM hti;

    // g_rgDocHeadings is an application-defined global array of 
    // the following structures: 
    //     typedef struct 
    //       { 
    //         TCHAR tchHeading[MAX_HEADING_LEN]; 
    //         int tchLevel; 
    //     } Heading; 
    for (int i = 0; i < ARRAYSIZE(g_rgDocHeadings); i++) 
    { 
        // Add the item to the tree-view control. 
        hti = AddItemToTree(hwndTV, g_rgDocHeadings[i].tchHeading, 
            g_rgDocHeadings[i].tchLevel); 

        if (hti == NULL)
            return FALSE;
    } 
           
    return TRUE; 
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di controlli Tree-View](using-treeview.md)
</dt> <dt>

[L'esempio CustDTv illustra il progetto personalizzato in un controllo Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




