---
title: Come inizializzare l'elenco di immagini
description: A ogni elemento di un controllo di visualizzazione albero possono essere associate due immagini.
ms.assetid: 3683DB35-D70F-4181-9181-95354599B9FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 011d789da4eec39febae9d93436e23c23fa59507
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104117395"
---
# <a name="how-to-initialize-the-image-list"></a><span data-ttu-id="8a4dc-103">Come inizializzare l'elenco di immagini</span><span class="sxs-lookup"><span data-stu-id="8a4dc-103">How to Initialize the Image List</span></span>

<span data-ttu-id="8a4dc-104">A ogni elemento di un controllo di visualizzazione albero possono essere associate due immagini.</span><span class="sxs-lookup"><span data-stu-id="8a4dc-104">Every item in a tree-view control can have two images associated with it.</span></span> <span data-ttu-id="8a4dc-105">Un elemento Visualizza un'immagine quando è selezionata e l'altra in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="8a4dc-105">An item displays one image when it is selected and the other when it is not.</span></span> <span data-ttu-id="8a4dc-106">Per includere immagini con elementi della visualizzazione albero, utilizzare innanzitutto le funzioni [elenchi immagini](image-lists.md) per creare un elenco di immagini e aggiungervi immagini.</span><span class="sxs-lookup"><span data-stu-id="8a4dc-106">To include images with tree-view items, first use the [Image Lists](image-lists.md) functions to create an image list and add images to it.</span></span> <span data-ttu-id="8a4dc-107">Associare quindi l'elenco di immagini al controllo di visualizzazione ad albero usando il messaggio macchina virtuale [**TVM \_**](tvm-setimagelist.md) .</span><span class="sxs-lookup"><span data-stu-id="8a4dc-107">Then associate the image list with the tree-view control by using the [**TVM\_SETIMAGELIST**](tvm-setimagelist.md) message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="8a4dc-108">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="8a4dc-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="8a4dc-109">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="8a4dc-109">Technologies</span></span>

-   [<span data-ttu-id="8a4dc-110">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="8a4dc-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="8a4dc-111">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="8a4dc-111">Prerequisites</span></span>

-   <span data-ttu-id="8a4dc-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="8a4dc-112">C/C++</span></span>
-   <span data-ttu-id="8a4dc-113">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="8a4dc-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="8a4dc-114">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="8a4dc-114">Instructions</span></span>

### <a name="initialize-the-image-list"></a><span data-ttu-id="8a4dc-115">Inizializzare l'elenco di immagini</span><span class="sxs-lookup"><span data-stu-id="8a4dc-115">Initialize the Image List</span></span>

<span data-ttu-id="8a4dc-116">Nell'esempio seguente viene creato un elenco di immagini, vengono aggiunte tre bitmap all'elenco e l'elenco di immagini viene associato a un controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="8a4dc-116">The following example creates an image list, adds three bitmaps to the list, and associates the image list with a tree-view control.</span></span>


```C++
// InitTreeViewImageLists - creates an image list, adds three bitmaps 
// to it, and associates the image list with a tree-view control. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwndTV - handle to the tree-view control. 
//
// Global variables and constants: 
// g_hInst - the global instance handle.
// g_nOpen, g_nClosed, and g_nDocument - global indexes of the images. 
// CX_BITMAP and CY_BITMAP - width and height of an icon. 
// NUM_BITMAPS - number of bitmaps to add to the image list. 
// IDB_OPEN_FILE, IDB_CLOSED_FILE, IDB_DOCUMENT -
//     resource identifiers of the bitmaps.

BOOL InitTreeViewImageLists(HWND hwndTV) 
{ 
    HIMAGELIST himl;  // handle to image list 
    HBITMAP hbmp;     // handle to bitmap 

    // Create the image list. 
    if ((himl = ImageList_Create(CX_BITMAP, 
                                 CY_BITMAP,
                                 FALSE, 
                                 NUM_BITMAPS, 0)) == NULL) 
        return FALSE; 

    // Add the open file, closed file, and document bitmaps. 
    hbmp = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_OPEN_FILE)); 
    g_nOpen = ImageList_Add(himl, hbmp, (HBITMAP)NULL); 
    DeleteObject(hbmp); 

    hbmp = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_CLOSED_FILE)); 
    g_nClosed = ImageList_Add(himl, hbmp, (HBITMAP)NULL); 
    DeleteObject(hbmp); 

    hbmp = LoadBitmap(g_hInst, MAKEINTRESOURCE(IDB_DOCUMENT)); 
    g_nDocument = ImageList_Add(himl, hbmp, (HBITMAP)NULL); 
    DeleteObject(hbmp); 

    // Fail if not all of the images were added. 
    if (ImageList_GetImageCount(himl) < 3) 
        return FALSE; 

    // Associate the image list with the tree-view control. 
    TreeView_SetImageList(hwndTV, himl, TVSIL_NORMAL); 

    return TRUE; 
} 
```



## <a name="related-topics"></a><span data-ttu-id="8a4dc-117">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8a4dc-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a4dc-118">Uso di controlli Tree-View</span><span class="sxs-lookup"><span data-stu-id="8a4dc-118">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="8a4dc-119">L'esempio CustDTv illustra il progetto personalizzato in un controllo Tree-View</span><span class="sxs-lookup"><span data-stu-id="8a4dc-119">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




