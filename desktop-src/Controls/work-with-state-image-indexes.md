---
title: Come lavorare con gli indici di immagini di stato
description: Spesso si confonde l'impostazione e il recupero dell'indice dell'immagine di stato in un controllo di visualizzazione albero.
ms.assetid: 2666D922-9957-4A75-BFDA-038720F1EEDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be84035907b69ba98ed60a33046f1a58fd2b47b2
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "103723686"
---
# <a name="how-to-work-with-state-image-indexes"></a><span data-ttu-id="636b1-103">Come lavorare con gli indici di immagini di stato</span><span class="sxs-lookup"><span data-stu-id="636b1-103">How to Work With State Image Indexes</span></span>

<span data-ttu-id="636b1-104">Spesso si confonde l'impostazione e il recupero dell'indice dell'immagine di stato in un controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="636b1-104">There is often confusion about how to set and retrieve the state image index in a tree-view control.</span></span> <span data-ttu-id="636b1-105">Negli esempi seguenti viene illustrato il metodo appropriato per l'impostazione e il recupero dell'indice dell'immagine di stato.</span><span class="sxs-lookup"><span data-stu-id="636b1-105">The following examples demonstrate the proper method for setting and retrieving the state image index.</span></span> <span data-ttu-id="636b1-106">Negli esempi si presuppone che esistano solo due indici di immagini di stato nel controllo di visualizzazione albero, deselezionati e controllati.</span><span class="sxs-lookup"><span data-stu-id="636b1-106">The examples assume that there are only two state image indexes in the tree-view control, unchecked and checked.</span></span> <span data-ttu-id="636b1-107">Se l'applicazione contiene più di due, sarà necessario modificare queste funzioni per gestire tale caso.</span><span class="sxs-lookup"><span data-stu-id="636b1-107">If your application contains more than two, these functions will need to be modified to handle that case.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="636b1-108">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="636b1-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="636b1-109">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="636b1-109">Technologies</span></span>

-   [<span data-ttu-id="636b1-110">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="636b1-110">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="636b1-111">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="636b1-111">Prerequisites</span></span>

-   <span data-ttu-id="636b1-112">C/C++</span><span class="sxs-lookup"><span data-stu-id="636b1-112">C/C++</span></span>
-   <span data-ttu-id="636b1-113">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="636b1-113">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="636b1-114">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="636b1-114">Instructions</span></span>

### <a name="set-a-tree-view-items-check-state"></a><span data-ttu-id="636b1-115">Imposta lo stato di selezione di un elemento di Tree-View</span><span class="sxs-lookup"><span data-stu-id="636b1-115">Set a Tree-View Item's Check State</span></span>

<span data-ttu-id="636b1-116">Nell'esempio seguente viene illustrato come impostare lo stato di selezione di un elemento della visualizzazione struttura ad albero.</span><span class="sxs-lookup"><span data-stu-id="636b1-116">The following example demonstrates how to set a tree-view item's check state.</span></span>


```C++
  BOOL TreeView_SetCheckState(HWND hwndTreeView, HTREEITEM hItem, BOOL fCheck)
  {
      TVITEM tvItem;

      tvItem.mask   = TVIF_HANDLE | TVIF_STATE;
      tvItem.hItem  = hItem;
      tvItem.stateMask  = TVIS_STATEIMAGEMASK;

      // Image 1 in the tree-view check box image list is the unchecked box. 
      // Image 2 is the checked box.

      tvItem.state = INDEXTOSTATEIMAGEMASK((fCheck ? 2 : 1));

      return TreeView_SetItem(hwndTreeView, &tvItem);
  }
```



### <a name="retrieve-a-tree-view-items-check-state"></a><span data-ttu-id="636b1-117">Recuperare lo stato di selezione di un elemento di Tree-View</span><span class="sxs-lookup"><span data-stu-id="636b1-117">Retrieve a Tree-View Item's Check State</span></span>

<span data-ttu-id="636b1-118">Nell'esempio seguente viene illustrato come recuperare lo stato di selezione di un elemento della visualizzazione struttura ad albero.</span><span class="sxs-lookup"><span data-stu-id="636b1-118">The following example demonstrates how to retrieve a tree-view item's check state.</span></span>


```C++
  BOOL TreeView_GetCheckState(HWND hwndTreeView, HTREEITEM hItem)
  {
      TVITEM tvItem;

      // Prepare to receive the desired information.
      tvItem.mask   = TVIF_HANDLE | TVIF_STATE;
      tvItem.hItem  = hItem;
      tvItem.stateMask  = TVIS_STATEIMAGEMASK;

      // Request the information.
      TreeView_GetItem(hwndTreeView, &tvItem);

      // Return zero if it's not checked, or nonzero otherwise.
      return ((BOOL)(tvItem.state >> 12) - 1);
  }
```



## <a name="related-topics"></a><span data-ttu-id="636b1-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="636b1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="636b1-120">Uso di controlli Tree-View</span><span class="sxs-lookup"><span data-stu-id="636b1-120">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="636b1-121">L'esempio CustDTv illustra il progetto personalizzato in un controllo Tree-View</span><span class="sxs-lookup"><span data-stu-id="636b1-121">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




