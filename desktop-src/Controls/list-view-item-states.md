---
title: Stati degli elementi List-View (CommCtrl. h)
description: Il valore dello stato di un elemento è costituito dallo stato dell'elemento, da un indice della maschera di sovrapposizione facoltativo e da un indice facoltativo della maschera di immagine di stato.
ms.assetid: 21827f4a-f133-489b-bbd2-6979d1928b40
topic_type:
- apiref
api_name:
- LVIS_ACTIVATING
- LVIS_CUT
- LVIS_DROPHILITED
- LVIS_FOCUSED
- LVIS_OVERLAYMASK
- LVIS_SELECTED
- LVIS_STATEIMAGEMASK
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8432760dd4cc7efde30700f837864ddcf04aac31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327862"
---
# <a name="list-view-item-states"></a><span data-ttu-id="affa8-103">Stati elemento List-View</span><span class="sxs-lookup"><span data-stu-id="affa8-103">List-View Item States</span></span>

<span data-ttu-id="affa8-104">Il valore dello stato di un elemento è costituito dallo stato dell'elemento, da un indice della maschera di sovrapposizione facoltativo e da un indice facoltativo della maschera di immagine di stato.</span><span class="sxs-lookup"><span data-stu-id="affa8-104">An item's state value consists of the item's state, an optional overlay mask index, and an optional state image mask index.</span></span>

<span data-ttu-id="affa8-105">Lo stato di un elemento ne determina l'aspetto e le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="affa8-105">An item's state determines its appearance and functionality.</span></span> <span data-ttu-id="affa8-106">Lo stato può essere zero o uno o più dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="affa8-106">The state can be zero or one or more of the following values:</span></span>



| <span data-ttu-id="affa8-107">Costante</span><span class="sxs-lookup"><span data-stu-id="affa8-107">Constant</span></span>                                                                                                                                                                        | <span data-ttu-id="affa8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="affa8-108">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_ACTIVATING"></span><span id="lvis_activating"></span><dl> <span data-ttu-id="affa8-109"><dt>**attivazione di LVIS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="affa8-109"><dt>**LVIS\_ACTIVATING**</dt></span></span> </dl>             | <span data-ttu-id="affa8-110">Non è attualmente supportato.</span><span class="sxs-lookup"><span data-stu-id="affa8-110">Not currently supported.</span></span><br/>                                                                                                                                  |
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <span data-ttu-id="affa8-111"><dt>**\_taglia lvis**</dt></span><span class="sxs-lookup"><span data-stu-id="affa8-111"><dt>**LVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="affa8-112">L'elemento è contrassegnato per un'operazione di taglia e incolla.</span><span class="sxs-lookup"><span data-stu-id="affa8-112">The item is marked for a cut-and-paste operation.</span></span><br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <span data-ttu-id="affa8-113"><dt>**\_DROPHILITED lvis**</dt></span><span class="sxs-lookup"><span data-stu-id="affa8-113"><dt>**LVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="affa8-114">L'elemento è evidenziato come destinazione di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="affa8-114">The item is highlighted as a drag-and-drop target.</span></span><br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <span data-ttu-id="affa8-115"><dt>**LVIS con stato \_ attivo**</dt></span><span class="sxs-lookup"><span data-stu-id="affa8-115"><dt>**LVIS\_FOCUSED**</dt></span></span> </dl>                      | <span data-ttu-id="affa8-116">L'elemento ha lo stato attivo, quindi è racchiuso da un rettangolo di attivazione standard.</span><span class="sxs-lookup"><span data-stu-id="affa8-116">The item has the focus, so it is surrounded by a standard focus rectangle.</span></span> <span data-ttu-id="affa8-117">Sebbene sia possibile selezionare più di un elemento, solo un elemento può avere lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="affa8-117">Although more than one item may be selected, only one item can have the focus.</span></span><br/> |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <span data-ttu-id="affa8-118"><dt>**\_OVERLAYMASK lvis**</dt></span><span class="sxs-lookup"><span data-stu-id="affa8-118"><dt>**LVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="affa8-119">L'indice dell'immagine sovrapposta dell'elemento viene recuperato da una maschera.</span><span class="sxs-lookup"><span data-stu-id="affa8-119">The item's overlay image index is retrieved by a mask.</span></span><br/>                                                                                                    |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <span data-ttu-id="affa8-120"><dt>**LVIS \_ selezionato**</dt></span><span class="sxs-lookup"><span data-stu-id="affa8-120"><dt>**LVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="affa8-121">L'elemento è selezionato.</span><span class="sxs-lookup"><span data-stu-id="affa8-121">The item is selected.</span></span> <span data-ttu-id="affa8-122">L'aspetto di un elemento selezionato dipende dal fatto che abbia lo stato attivo e anche sui colori di sistema usati per la selezione.</span><span class="sxs-lookup"><span data-stu-id="affa8-122">The appearance of a selected item depends on whether it has the focus and also on the system colors used for selection.</span></span><br/>             |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <span data-ttu-id="affa8-123"><dt>**\_STATEIMAGEMASK lvis**</dt></span><span class="sxs-lookup"><span data-stu-id="affa8-123"><dt>**LVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="affa8-124">L'indice dell'immagine di stato dell'elemento viene recuperato da una maschera.</span><span class="sxs-lookup"><span data-stu-id="affa8-124">The item's state image index is retrieved by a mask.</span></span><br/>                                                                                                      |



## <a name="remarks"></a><span data-ttu-id="affa8-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="affa8-125">Remarks</span></span>

<span data-ttu-id="affa8-126">È possibile usare **lvis \_ OVERLAYMASK** mask per isolare l'indice in base uno dell'immagine sovrapposta.</span><span class="sxs-lookup"><span data-stu-id="affa8-126">You can use the **LVIS\_OVERLAYMASK** mask to isolate the one-based index of the overlay image.</span></span> <span data-ttu-id="affa8-127">È possibile usare **lvis \_ STATEIMAGEMASK** mask per isolare l'indice in base uno dell'immagine di stato.</span><span class="sxs-lookup"><span data-stu-id="affa8-127">You can use the **LVIS\_STATEIMAGEMASK** mask to isolate the one-based index of the state image.</span></span>

## <a name="requirements"></a><span data-ttu-id="affa8-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="affa8-128">Requirements</span></span>



| <span data-ttu-id="affa8-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="affa8-129">Requirement</span></span> | <span data-ttu-id="affa8-130">Valore</span><span class="sxs-lookup"><span data-stu-id="affa8-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="affa8-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="affa8-131">Header</span></span><br/> | <dl> <span data-ttu-id="affa8-132"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="affa8-132"><dt>CommCtrl.h</dt></span></span> </dl> |



 

 





