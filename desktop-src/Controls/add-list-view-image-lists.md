---
title: Come aggiungere List-View elenchi di immagini
description: In questo argomento viene illustrato come aggiungere elenchi di immagini a un controllo visualizzazione elenco.
ms.assetid: 3C282FBC-5E37-4D8E-A2C4-B2876874E9A7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2f6f5b483ea80b412ab7638c9aceafcac4c5e6
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104339667"
---
# <a name="how-to-add-list-view-image-lists"></a><span data-ttu-id="e5649-103">Come aggiungere List-View elenchi di immagini</span><span class="sxs-lookup"><span data-stu-id="e5649-103">How to Add List-View Image Lists</span></span>

<span data-ttu-id="e5649-104">In questo argomento viene illustrato come aggiungere elenchi di immagini a un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="e5649-104">This topic demonstrates how to add image lists to a list-view control.</span></span>

<span data-ttu-id="e5649-105">Vengono creati solo gli elenchi di immagini usati dal controllo.</span><span class="sxs-lookup"><span data-stu-id="e5649-105">You create only the image lists that the control uses.</span></span> <span data-ttu-id="e5649-106">Se, ad esempio, l'applicazione non consente all'utente di passare alla visualizzazione icone, non è necessario creare e assegnare un elenco di icone di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="e5649-106">For example, if your application does not allow the user to switch to icon view, you do not need to create and assign a large icon list.</span></span> <span data-ttu-id="e5649-107">Se si creano elenchi di immagini grandi e piccole, devono contenere le stesse immagini nello stesso ordine, poiché viene usato un solo valore per identificare l'icona di un elemento della visualizzazione elenco in entrambi gli elenchi di immagini.</span><span class="sxs-lookup"><span data-stu-id="e5649-107">If you create both large and small image lists, they must contain the same images in the same order, because a single value is used to identify a list-view item's icon in both image lists.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="e5649-108">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="e5649-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="e5649-109">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="e5649-109">Technologies</span></span>

-   [<span data-ttu-id="e5649-110">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="e5649-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="e5649-111">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="e5649-111">Prerequisites</span></span>

-   <span data-ttu-id="e5649-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="e5649-112">C/C++</span></span>
-   <span data-ttu-id="e5649-113">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="e5649-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="e5649-114">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="e5649-114">Instructions</span></span>


<span data-ttu-id="e5649-115">Per visualizzare le immagini degli elementi, è necessario assegnare un elenco di immagini al controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="e5649-115">To display item images, you must assign an image list to the list-view control.</span></span> <span data-ttu-id="e5649-116">A tale scopo, usare il [**messaggio \_ LVM**](lvm-setimagelist.md) o la corrispondente macro [**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist), che specifica se l'elenco immagini contiene icone a dimensione intera, icone piccole o immagini di stato.</span><span class="sxs-lookup"><span data-stu-id="e5649-116">To do this, use the [**LVM\_SETIMAGELIST**](lvm-setimagelist.md) message or the corresponding macro [**ListView\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist), specifying whether the image list contains full-sized icons, small icons, or state images.</span></span> <span data-ttu-id="e5649-117">Per recuperare l'handle a un elenco di immagini attualmente assegnato a un controllo visualizzazione elenco, usare il messaggio [**LVM \_ getimagine**](lvm-getimagelist.md) .</span><span class="sxs-lookup"><span data-stu-id="e5649-117">To retrieve the handle to an image list that is currently assigned to a list-view control, use the [**LVM\_GETIMAGELIST**](lvm-getimagelist.md) message.</span></span> <span data-ttu-id="e5649-118">È possibile utilizzare la funzione [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) per determinare le dimensioni appropriate per le icone di dimensioni ridotte e di dimensioni ridotte.</span><span class="sxs-lookup"><span data-stu-id="e5649-118">You can use the [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) function to determine appropriate dimensions for the full-sized and small icons.</span></span>

<span data-ttu-id="e5649-119">Nell'esempio di codice C++ riportato di seguito, la funzione definita dall'applicazione crea innanzitutto elenchi di immagini e li assegna a un controllo di visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="e5649-119">In the following C++ code example, the application-defined function first creates image lists and then assigns them to a list-view control.</span></span>


```C++
// InitListViewImageLists: Creates image lists for a list-view control.
// This function only creates image lists. It does not insert the items into
// the control, which is necessary for the control to be visible.   
//
// Returns TRUE if successful, or FALSE otherwise. 
//
// hWndListView: Handle to the list-view control. 
// global variable g_hInst: The handle to the module of either a 
// dynamic-link library (DLL) or executable (.exe) that contains
// the image to be loaded. If loading a standard or system
// icon, set g_hInst to NULL.
//
BOOL InitListViewImageLists(HWND hWndListView) 
{ 
    HICON hiconItem;     // Icon for list-view items.
    HIMAGELIST hLarge;   // Image list for icon view.
    HIMAGELIST hSmall;   // Image list for other views.

    // Create the full-sized icon image lists. 
    hLarge = ImageList_Create(GetSystemMetrics(SM_CXICON), 
                              GetSystemMetrics(SM_CYICON), 
                              ILC_MASK, 1, 1); 

    hSmall = ImageList_Create(GetSystemMetrics(SM_CXSMICON), 
                              GetSystemMetrics(SM_CYSMICON), 
                              ILC_MASK, 1, 1); 
    
    // Add an icon to each image list.  
    hiconItem = LoadIcon(g_hInst, MAKEINTRESOURCE(IDI_ITEM));

    ImageList_AddIcon(hLarge, hiconItem);
    ImageList_AddIcon(hSmall, hiconItem);

    DestroyIcon(hiconItem);
 
// When you are dealing with multiple icons, you can use the previous four lines of 
// code inside a loop. The following code shows such a loop. The 
// icons are defined in the application's header file as resources, which 
// are numbered consecutively starting with IDS_FIRSTICON. The number of 
// icons is defined in the header file as C_ICONS.
/*    
    for(index = 0; index < C_ICONS; index++)
    {
        hIconItem = LoadIcon (g_hinst, MAKEINTRESOURCE(IDS_FIRSTICON + index));
        ImageList_AddIcon(hSmall, hIconItem);
        ImageList_AddIcon(hLarge, hIconItem);
        Destroy(hIconItem);
    }
*/
    
    // Assign the image lists to the list-view control. 
    ListView_SetImageList(hWndListView, hLarge, LVSIL_NORMAL); 
    ListView_SetImageList(hWndListView, hSmall, LVSIL_SMALL); 
    
    return TRUE; 
}
```



## <a name="related-topics"></a><span data-ttu-id="e5649-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e5649-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5649-121">Riferimento al controllo visualizzazione elenco</span><span class="sxs-lookup"><span data-stu-id="e5649-121">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="e5649-122">Informazioni sui controlli List-View</span><span class="sxs-lookup"><span data-stu-id="e5649-122">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="e5649-123">Uso di controlli List-View</span><span class="sxs-lookup"><span data-stu-id="e5649-123">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 