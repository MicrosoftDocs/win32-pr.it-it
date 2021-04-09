---
title: Come usare le visualizzazioni affiancate
description: In questo argomento viene illustrato come impostare la visualizzazione affiancata per un controllo visualizzazione elenco.
ms.assetid: BDE17F4B-3A15-48BB-8160-036AD0DC3B41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616a9bb8a2c1707d903f0ebe2b6de86511dc6ce4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963572"
---
# <a name="how-to-use-tile-views"></a><span data-ttu-id="11c8e-103">Come usare le visualizzazioni affiancate</span><span class="sxs-lookup"><span data-stu-id="11c8e-103">How to Use Tile Views</span></span>

<span data-ttu-id="11c8e-104">In questo argomento viene illustrato come impostare la visualizzazione affiancata per un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="11c8e-104">This topic demonstrates how to set the tile view for a list-view control.</span></span> <span data-ttu-id="11c8e-105">Nella visualizzazione affiancata ogni elemento è rappresentato da un'icona grande con una o più righe di testo associato.</span><span class="sxs-lookup"><span data-stu-id="11c8e-105">In tile view, each item is represented by a large icon with one or more lines of accompanying text.</span></span> <span data-ttu-id="11c8e-106">Per un'illustrazione, vedere [informazioni sui controlli List-View](list-view-controls-overview.md).</span><span class="sxs-lookup"><span data-stu-id="11c8e-106">For an illustration, see [About List-View Controls](list-view-controls-overview.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="11c8e-107">Informazioni importanti</span><span class="sxs-lookup"><span data-stu-id="11c8e-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="11c8e-108">Tecnologie</span><span class="sxs-lookup"><span data-stu-id="11c8e-108">Technologies</span></span>

-   [<span data-ttu-id="11c8e-109">Controlli Windows</span><span class="sxs-lookup"><span data-stu-id="11c8e-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="11c8e-110">Prerequisiti</span><span class="sxs-lookup"><span data-stu-id="11c8e-110">Prerequisites</span></span>

-   <span data-ttu-id="11c8e-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="11c8e-111">C/C++</span></span>
-   <span data-ttu-id="11c8e-112">Programmazione dell'interfaccia utente di Windows</span><span class="sxs-lookup"><span data-stu-id="11c8e-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="11c8e-113">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="11c8e-113">Instructions</span></span>


<span data-ttu-id="11c8e-114">Impostare i parametri di visualizzazione generali per la visualizzazione affiancata utilizzando la macro [**\_ SetTileViewInfo di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileviewinfo) .</span><span class="sxs-lookup"><span data-stu-id="11c8e-114">Set the general display parameters for tile view by using the [**ListView\_SetTileViewInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileviewinfo) macro.</span></span> <span data-ttu-id="11c8e-115">Utilizzare la struttura [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo) passata a questa macro per specificare la posizione del testo in relazione all'icona, le dimensioni di ogni riquadro (incluso il testo associato) e il numero massimo di righe di testo.</span><span class="sxs-lookup"><span data-stu-id="11c8e-115">Use the [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo) structure that is passed to this macro to specify the position of the text in relation to the icon, the size of each tile (including accompanying text), and the maximum number of lines of text.</span></span>

<span data-ttu-id="11c8e-116">Se non si desidera che i riquadri vengano ridimensionati automaticamente, è necessario impostare **LVTVIF \_ FIXEDSIZE** nel membro **dwFlags** e **LVTVIM \_ TILESIZE** nel membro **dwMask** di [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo), oltre a fornire le dimensioni nel membro **sizeTile** .</span><span class="sxs-lookup"><span data-stu-id="11c8e-116">If you do not want tiles to be automatically sized, you must set **LVTVIF\_FIXEDSIZE** in the **dwFlags** member and **LVTVIM\_TILESIZE** in the **dwMask** member of [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo), as well as providing the dimensions in the **sizeTile** member.</span></span>

<span data-ttu-id="11c8e-117">L'esempio di codice C++ seguente imposta le informazioni sulla visualizzazione affiancata per un controllo di visualizzazione elenco in modo da visualizzare un massimo di due elementi secondari per ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="11c8e-117">The following C++ code example sets the tile view info for a list-view control so that a maximum of two subitems are displayed for each item.</span></span> <span data-ttu-id="11c8e-118">Imposta anche le dimensioni di ogni sezione.</span><span class="sxs-lookup"><span data-stu-id="11c8e-118">It also sets the size of each tile.</span></span>


```C++
    SIZE size = { 100, 50 };
    LVTILEVIEWINFO tileViewInfo = {0};

    tileViewInfo.cbSize   = sizeof(tileViewInfo);
    tileViewInfo.dwFlags  = LVTVIF_FIXEDSIZE;
    tileViewInfo.dwMask   = LVTVIM_COLUMNS | LVTVIM_TILESIZE;
    tileViewInfo.cLines   = 2;
    tileViewInfo.sizeTile = size;

    ListView_SetTileViewInfo(hWndListView, &tileViewInfo);

```



<span data-ttu-id="11c8e-119">Per ogni elemento dell'elenco, è possibile impostare altri parametri quando l'elemento viene inserito nell'elenco o in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="11c8e-119">For each item in the list, you can set further parameters when the item is inserted in the list, or later.</span></span> <span data-ttu-id="11c8e-120">La struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) usata con [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) contiene membri che specificano le colonne di dati da visualizzare sotto l'elemento e il relativo allineamento.</span><span class="sxs-lookup"><span data-stu-id="11c8e-120">The [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that is used with [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) contains members that specify which columns of data to display below the item, and their alignment.</span></span> <span data-ttu-id="11c8e-121">Questi stessi parametri di visualizzazione sono disponibili anche nella struttura [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) usata con [**ListView \_ SetTileInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileinfo).</span><span class="sxs-lookup"><span data-stu-id="11c8e-121">These same display parameters are also found in the [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) structure used with [**ListView\_SetTileInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileinfo).</span></span>

> [!Note]  
> <span data-ttu-id="11c8e-122">"Columns" si riferisce a non visualizzare le colonne nella visualizzazione affiancata, ma piuttosto agli elementi secondari, che vengono visualizzati in colonne nella visualizzazione dettagli.</span><span class="sxs-lookup"><span data-stu-id="11c8e-122">"Columns" here refers not to display columns in tile view but rather to subitems, which are displayed in columns in details view.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="11c8e-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="11c8e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11c8e-124">Riferimento al controllo visualizzazione elenco</span><span class="sxs-lookup"><span data-stu-id="11c8e-124">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="11c8e-125">Informazioni sui controlli List-View</span><span class="sxs-lookup"><span data-stu-id="11c8e-125">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="11c8e-126">Uso di controlli List-View</span><span class="sxs-lookup"><span data-stu-id="11c8e-126">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




