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
# <a name="how-to-add-tree-view-items"></a><span data-ttu-id="be994-103">Come aggiungere elementi di Tree-View</span><span class="sxs-lookup"><span data-stu-id="be994-103">How to Add Tree-View Items</span></span>

<span data-ttu-id="be994-104">Aggiungere un elemento a un controllo di visualizzazione albero inviando il messaggio [**di \_ INSERTITEM INSERTITEM**](tvm-insertitem.md) al controllo.</span><span class="sxs-lookup"><span data-stu-id="be994-104">You add an item to a tree-view control by sending the [**TVM\_INSERTITEM**](tvm-insertitem.md) message to the control.</span></span> <span data-ttu-id="be994-105">Il messaggio include l'indirizzo di una struttura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) , specificando l'elemento padre, l'elemento dopo il quale viene inserito il nuovo elemento e una struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) che definisce gli attributi dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="be994-105">The message includes the address of a [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) structure, specifying the parent item, the item after which the new item is inserted, and a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that defines the attributes of the item.</span></span> <span data-ttu-id="be994-106">Gli attributi includono l'etichetta dell'elemento, le immagini selezionate e non selezionate e un valore definito dall'applicazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="be994-106">The attributes include the item's label, its selected and nonselected images, and a 32-bit application-defined value.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="be994-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="be994-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="be994-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="be994-108">Technologies</span></span>

-   [<span data-ttu-id="be994-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="be994-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="be994-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="be994-110">Prerequisites</span></span>

-   <span data-ttu-id="be994-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="be994-111">C/C++</span></span>
-   <span data-ttu-id="be994-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="be994-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="be994-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="be994-113">Instructions</span></span>

### <a name="add-items-to-the-tree-view"></a><span data-ttu-id="be994-114">Aggiungere elementi al Tree-View</span><span class="sxs-lookup"><span data-stu-id="be994-114">Add Items to the Tree-View</span></span>

<span data-ttu-id="be994-115">Nell'esempio riportato in questa sezione viene illustrato come creare una tabella di contenuti in base alle informazioni sull'intestazione del documento fornite in una matrice definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="be994-115">The example in this section demonstrates how to create a table of contents based on document heading information that is provided in an application-defined array.</span></span> <span data-ttu-id="be994-116">Ogni elemento della matrice è costituito da una stringa di intestazione e da un numero intero che indica il livello di intestazione.</span><span class="sxs-lookup"><span data-stu-id="be994-116">Each array element consists of a heading string and an integer that indicates the heading level.</span></span> <span data-ttu-id="be994-117">L'esempio supporta tre livelli di intestazione (1, 2 e 3).</span><span class="sxs-lookup"><span data-stu-id="be994-117">The example supports three heading levels (1, 2, and 3).</span></span>

<span data-ttu-id="be994-118">Nell'esempio sono incluse due funzioni.</span><span class="sxs-lookup"><span data-stu-id="be994-118">The example includes two functions.</span></span> <span data-ttu-id="be994-119">La prima funzione estrae ogni intestazione e il livello di intestazione associato, quindi li passa alla seconda funzione.</span><span class="sxs-lookup"><span data-stu-id="be994-119">The first function extracts each heading and accompanying heading level and then passes them to the second function.</span></span>

<span data-ttu-id="be994-120">La seconda funzione aggiunge un elemento a un controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="be994-120">The second function adds an item to a tree-view control.</span></span> <span data-ttu-id="be994-121">Usa il testo dell'intestazione come etichetta dell'elemento e usa il livello di intestazione per determinare l'elemento padre per il nuovo elemento.</span><span class="sxs-lookup"><span data-stu-id="be994-121">It uses the heading text as the item's label, and it uses the heading level to determine the parent item for the new item.</span></span> <span data-ttu-id="be994-122">Viene aggiunta un'intestazione Level One alla radice del controllo di visualizzazione ad albero, viene aggiunta un'intestazione di livello due come elemento figlio del livello precedente e così via.</span><span class="sxs-lookup"><span data-stu-id="be994-122">A level one heading is added to the root of the tree-view control, a level two heading is added as a child item of the previous level one item, and so on.</span></span> <span data-ttu-id="be994-123">La funzione assegna un'immagine a un elemento a seconda che disponga di elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="be994-123">The function assigns an image to an item based on whether it has child items.</span></span> <span data-ttu-id="be994-124">Se un elemento ha elementi figlio, ottiene un'immagine che rappresenta una cartella chiusa.</span><span class="sxs-lookup"><span data-stu-id="be994-124">If an item has child items, it gets an image that represents a closed folder.</span></span> <span data-ttu-id="be994-125">In caso contrario, ottiene un'immagine che rappresenta un documento.</span><span class="sxs-lookup"><span data-stu-id="be994-125">Otherwise, it gets an image that represents a document.</span></span> <span data-ttu-id="be994-126">Un elemento usa la stessa immagine per gli Stati selezionato e non selezionato.</span><span class="sxs-lookup"><span data-stu-id="be994-126">An item uses the same image for both the selected and nonselected states.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="be994-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="be994-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be994-128">Uso di controlli Tree-View</span><span class="sxs-lookup"><span data-stu-id="be994-128">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="be994-129">L'esempio CustDTv illustra il progetto personalizzato in un controllo Tree-View</span><span class="sxs-lookup"><span data-stu-id="be994-129">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




