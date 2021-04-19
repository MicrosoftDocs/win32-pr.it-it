---
title: Stati degli elementi di controllo Tree-View (CommCtrl. h)
description: In questa sezione sono elencati i flag di stato dell'elemento utilizzati per indicare lo stato di un elemento in un controllo di visualizzazione albero.
ms.assetid: 5b11d575-6dfd-47a8-b959-b19aaeeca70e
topic_type:
- apiref
api_name:
- TVIS_BOLD
- TVIS_CUT
- TVIS_DROPHILITED
- TVIS_EXPANDED
- TVIS_EXPANDEDONCE
- TVIS_EXPANDPARTIAL
- TVIS_SELECTED
- TVIS_OVERLAYMASK
- TVIS_STATEIMAGEMASK
- TVIS_USERMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4a19306855b7f38d03aa00323b26407f108bfe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326839"
---
# <a name="tree-view-control-item-states"></a><span data-ttu-id="99995-103">Stati degli elementi di controllo Tree-View</span><span class="sxs-lookup"><span data-stu-id="99995-103">Tree-View Control Item States</span></span>

<span data-ttu-id="99995-104">In questa sezione sono elencati i flag di stato dell'elemento utilizzati per indicare lo stato di un elemento in un controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="99995-104">This section lists the item state flags used to indicate the state of an item in a tree-view control.</span></span>



| <span data-ttu-id="99995-105">Costante</span><span class="sxs-lookup"><span data-stu-id="99995-105">Constant</span></span>                                                                                                                                                                        | <span data-ttu-id="99995-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="99995-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVIS_BOLD"></span><span id="tvis_bold"></span><dl> <span data-ttu-id="99995-107"><dt>**TVIS \_ grassetto**</dt></span><span class="sxs-lookup"><span data-stu-id="99995-107"><dt>**TVIS\_BOLD**</dt></span></span> </dl>                               | <span data-ttu-id="99995-108">L'elemento è in grassetto.</span><span class="sxs-lookup"><span data-stu-id="99995-108">The item is bold.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_CUT"></span><span id="tvis_cut"></span><dl> <span data-ttu-id="99995-109"><dt>**\_taglia TVIS**</dt></span><span class="sxs-lookup"><span data-stu-id="99995-109"><dt>**TVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="99995-110">L'elemento viene selezionato come parte di un'operazione di taglia e incolla.</span><span class="sxs-lookup"><span data-stu-id="99995-110">The item is selected as part of a cut-and-paste operation.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="TVIS_DROPHILITED"></span><span id="tvis_drophilited"></span><dl> <span data-ttu-id="99995-111"><dt>**\_DROPHILITED TVIS**</dt></span><span class="sxs-lookup"><span data-stu-id="99995-111"><dt>**TVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="99995-112">L'elemento è selezionato come destinazione di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="99995-112">The item is selected as a drag-and-drop target.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_EXPANDED"></span><span id="tvis_expanded"></span><dl> <span data-ttu-id="99995-113"><dt>**TVIS \_ espansa**</dt></span><span class="sxs-lookup"><span data-stu-id="99995-113"><dt>**TVIS\_EXPANDED**</dt></span></span> </dl>                   | <span data-ttu-id="99995-114">L'elenco di elementi figlio dell'elemento è attualmente espanso; ovvero gli elementi figlio sono visibili.</span><span class="sxs-lookup"><span data-stu-id="99995-114">The item's list of child items is currently expanded; that is, the child items are visible.</span></span> <span data-ttu-id="99995-115">Questo valore si applica solo agli elementi padre.</span><span class="sxs-lookup"><span data-stu-id="99995-115">This value applies only to parent items.</span></span><br/>                                                                                                                                                                                                                                                                                                                  |
| <span id="TVIS_EXPANDEDONCE"></span><span id="tvis_expandedonce"></span><dl> <span data-ttu-id="99995-116"><dt>**\_EXPANDEDONCE TVIS**</dt></span><span class="sxs-lookup"><span data-stu-id="99995-116"><dt>**TVIS\_EXPANDEDONCE**</dt></span></span> </dl>       | <span data-ttu-id="99995-117">L'elenco di elementi figlio dell'elemento è stato espanso almeno una volta.</span><span class="sxs-lookup"><span data-stu-id="99995-117">The item's list of child items has been expanded at least once.</span></span> <span data-ttu-id="99995-118">I codici di notifica di [TVN \_ ITEMEXPANDING](tvn-itemexpanding.md) e [TVN \_ ITEMEXPANDED](tvn-itemexpanded.md) non vengono generati per gli elementi padre con questo stato impostato in risposta a un messaggio di [**\_ espansione TVM**](tvm-expand.md) .</span><span class="sxs-lookup"><span data-stu-id="99995-118">The [TVN\_ITEMEXPANDING](tvn-itemexpanding.md) and [TVN\_ITEMEXPANDED](tvn-itemexpanded.md) notification codes are not generated for parent items that have this state set in response to a [**TVM\_EXPAND**](tvm-expand.md) message.</span></span> <span data-ttu-id="99995-119">L'uso \_ di TVE Collapse e TVE \_ COLLAPSERESET con **TVM \_ expand** provocherà la reimpostazione di questo stato.</span><span class="sxs-lookup"><span data-stu-id="99995-119">Using TVE\_COLLAPSE and TVE\_COLLAPSERESET with **TVM\_EXPAND** will cause this state to be reset.</span></span> <span data-ttu-id="99995-120">Questo valore si applica solo agli elementi padre.</span><span class="sxs-lookup"><span data-stu-id="99995-120">This value applies only to parent items.</span></span> <br/> |
| <span id="TVIS_EXPANDPARTIAL"></span><span id="tvis_expandpartial"></span><dl> <span data-ttu-id="99995-121"><dt>**\_EXPANDPARTIAL TVIS**</dt></span><span class="sxs-lookup"><span data-stu-id="99995-121"><dt>**TVIS\_EXPANDPARTIAL**</dt></span></span> </dl>    | <span data-ttu-id="99995-122">**Versione 4,70**.</span><span class="sxs-lookup"><span data-stu-id="99995-122">**Version 4.70**.</span></span> <span data-ttu-id="99995-123">Elemento visualizzazione albero parzialmente espanso.</span><span class="sxs-lookup"><span data-stu-id="99995-123">A partially expanded tree-view item.</span></span> <span data-ttu-id="99995-124">In questo stato, alcuni, ma non tutti, gli elementi figlio sono visibili e viene visualizzato il simbolo più dell'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="99995-124">In this state, some, but not all, of the child items are visible and the parent item's plus symbol is displayed.</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <span id="TVIS_SELECTED"></span><span id="tvis_selected"></span><dl> <span data-ttu-id="99995-125"><dt>**TVIS \_ selezionato**</dt></span><span class="sxs-lookup"><span data-stu-id="99995-125"><dt>**TVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="99995-126">L'elemento è selezionato.</span><span class="sxs-lookup"><span data-stu-id="99995-126">The item is selected.</span></span> <span data-ttu-id="99995-127">Il relativo aspetto dipende dal fatto che abbia lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="99995-127">Its appearance depends on whether it has the focus.</span></span> <span data-ttu-id="99995-128">L'elemento verrà disegnato usando i colori di sistema per la selezione.</span><span class="sxs-lookup"><span data-stu-id="99995-128">The item will be drawn using the system colors for selection.</span></span> <br/>                                                                                                                                                                                                                                                                                                              |
| <span id="TVIS_OVERLAYMASK"></span><span id="tvis_overlaymask"></span><dl> <span data-ttu-id="99995-129"><dt>**\_OVERLAYMASK TVIS**</dt></span><span class="sxs-lookup"><span data-stu-id="99995-129"><dt>**TVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="99995-130">Maschera per i bit utilizzati per specificare l'indice dell'immagine sovrapposta dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="99995-130">Mask for the bits used to specify the item's overlay image index.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="TVIS_STATEIMAGEMASK"></span><span id="tvis_stateimagemask"></span><dl> <span data-ttu-id="99995-131"><dt>**\_STATEIMAGEMASK TVIS**</dt></span><span class="sxs-lookup"><span data-stu-id="99995-131"><dt>**TVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="99995-132">Maschera per i bit utilizzati per specificare l'indice dell'immagine di stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="99995-132">Mask for the bits used to specify the item's state image index.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="TVIS_USERMASK"></span><span id="tvis_usermask"></span><dl> <span data-ttu-id="99995-133"><dt>**\_usermask TVIS**</dt></span><span class="sxs-lookup"><span data-stu-id="99995-133"><dt>**TVIS\_USERMASK**</dt></span></span> </dl>                   | <span data-ttu-id="99995-134">Uguale a **TVIS \_ STATEIMAGEMASK**.</span><span class="sxs-lookup"><span data-stu-id="99995-134">Same as **TVIS\_STATEIMAGEMASK**.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="remarks"></a><span data-ttu-id="99995-135">Commenti</span><span class="sxs-lookup"><span data-stu-id="99995-135">Remarks</span></span>

<span data-ttu-id="99995-136">Quando si imposta o recupera l'indice dell'immagine sovrapposta o dell'immagine di stato di un elemento, è necessario specificare le maschere seguenti nel membro **stateMask** della struttura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) :</span><span class="sxs-lookup"><span data-stu-id="99995-136">When you set or retrieve an item's overlay image index or state image index, you must specify the following masks in the **stateMask** member of the [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure:</span></span>

-   <span data-ttu-id="99995-137">**\_OVERLAYMASK TVIS**</span><span class="sxs-lookup"><span data-stu-id="99995-137">**TVIS\_OVERLAYMASK**</span></span>
-   <span data-ttu-id="99995-138">**\_STATEIMAGEMASK TVIS**</span><span class="sxs-lookup"><span data-stu-id="99995-138">**TVIS\_STATEIMAGEMASK**</span></span>
-   <span data-ttu-id="99995-139">**\_usermask TVIS**</span><span class="sxs-lookup"><span data-stu-id="99995-139">**TVIS\_USERMASK**</span></span>

<span data-ttu-id="99995-140">Questi valori possono essere usati anche per mascherare i bit di stato che non sono di interesse.</span><span class="sxs-lookup"><span data-stu-id="99995-140">These values can also be used to mask off the state bits that are not of interest.</span></span>

## <a name="requirements"></a><span data-ttu-id="99995-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99995-141">Requirements</span></span>



| <span data-ttu-id="99995-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="99995-142">Requirement</span></span> | <span data-ttu-id="99995-143">Valore</span><span class="sxs-lookup"><span data-stu-id="99995-143">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="99995-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="99995-144">Header</span></span><br/> | <dl> <span data-ttu-id="99995-145"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="99995-145"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





