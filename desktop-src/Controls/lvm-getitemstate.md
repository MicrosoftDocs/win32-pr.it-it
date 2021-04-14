---
title: Messaggio LVM_GETITEMSTATE (COMmctrl. h)
description: Recupera lo stato di un elemento della visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro GetItemState di ListView.
ms.assetid: 862960ed-a64a-4d66-b384-9228932eae6f
keywords:
- Controlli di Windows Message LVM_GETITEMSTATE
topic_type:
- apiref
api_name:
- LVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b355e78f22c01c289f681d256ee6b4d0aa882
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478520"
---
# <a name="lvm_getitemstate-message"></a><span data-ttu-id="42fdd-105">\_Messaggio GETITEMSTATE LVM</span><span class="sxs-lookup"><span data-stu-id="42fdd-105">LVM\_GETITEMSTATE message</span></span>

<span data-ttu-id="42fdd-106">Recupera lo stato di un elemento della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="42fdd-106">Retrieves the state of a list-view item.</span></span> <span data-ttu-id="42fdd-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ GetItemState di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate) .</span><span class="sxs-lookup"><span data-stu-id="42fdd-107">You can send this message explicitly or by using the [**ListView\_GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="42fdd-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="42fdd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42fdd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="42fdd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42fdd-110">Indice dell'elemento della visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="42fdd-110">Index of the list-view item.</span></span>

</dd> <dt>

<span data-ttu-id="42fdd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="42fdd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="42fdd-112">Informazioni sullo stato da recuperare.</span><span class="sxs-lookup"><span data-stu-id="42fdd-112">State information to retrieve.</span></span> <span data-ttu-id="42fdd-113">Questo parametro può essere una combinazione dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="42fdd-113">This parameter can be a combination of the following values:</span></span>



| <span data-ttu-id="42fdd-114">Valore</span><span class="sxs-lookup"><span data-stu-id="42fdd-114">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="42fdd-115">Significato</span><span class="sxs-lookup"><span data-stu-id="42fdd-115">Meaning</span></span>                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <span data-ttu-id="42fdd-116"><dt>**\_taglia lvis**</dt></span><span class="sxs-lookup"><span data-stu-id="42fdd-116"><dt>**LVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="42fdd-117">L'elemento è contrassegnato per un'operazione di taglia e incolla.</span><span class="sxs-lookup"><span data-stu-id="42fdd-117">The item is marked for a cut-and-paste operation.</span></span><br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <span data-ttu-id="42fdd-118"><dt>**\_DROPHILITED lvis**</dt></span><span class="sxs-lookup"><span data-stu-id="42fdd-118"><dt>**LVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="42fdd-119">L'elemento è evidenziato come destinazione di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="42fdd-119">The item is highlighted as a drag-and-drop target.</span></span><br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <span data-ttu-id="42fdd-120"><dt>**LVIS con stato \_ attivo**</dt></span><span class="sxs-lookup"><span data-stu-id="42fdd-120"><dt>**LVIS\_FOCUSED**</dt></span></span> </dl>                      | <span data-ttu-id="42fdd-121">L'elemento ha lo stato attivo, quindi è racchiuso da un rettangolo di attivazione standard.</span><span class="sxs-lookup"><span data-stu-id="42fdd-121">The item has the focus, so it is surrounded by a standard focus rectangle.</span></span> <span data-ttu-id="42fdd-122">Sebbene sia possibile selezionare più di un elemento, solo un elemento può avere lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="42fdd-122">Although more than one item may be selected, only one item can have the focus.</span></span><br/> |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <span data-ttu-id="42fdd-123"><dt>**LVIS \_ selezionato**</dt></span><span class="sxs-lookup"><span data-stu-id="42fdd-123"><dt>**LVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="42fdd-124">L'elemento è selezionato.</span><span class="sxs-lookup"><span data-stu-id="42fdd-124">The item is selected.</span></span> <span data-ttu-id="42fdd-125">L'aspetto di un elemento selezionato dipende dal fatto che abbia lo stato attivo e anche sui colori di sistema usati per la selezione.</span><span class="sxs-lookup"><span data-stu-id="42fdd-125">The appearance of a selected item depends on whether it has the focus and also on the system colors used for selection.</span></span><br/>             |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <span data-ttu-id="42fdd-126"><dt>**\_OVERLAYMASK lvis**</dt></span><span class="sxs-lookup"><span data-stu-id="42fdd-126"><dt>**LVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="42fdd-127">Usare questa maschera per recuperare l'indice dell'immagine sovrapposta dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="42fdd-127">Use this mask to retrieve the item's overlay image index.</span></span><br/>                                                                                                 |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <span data-ttu-id="42fdd-128"><dt>**\_STATEIMAGEMASK lvis**</dt></span><span class="sxs-lookup"><span data-stu-id="42fdd-128"><dt>**LVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="42fdd-129">Usare questa maschera per recuperare l'indice dell'immagine di stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="42fdd-129">Use this mask to retrieve the item's state image index.</span></span><br/>                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42fdd-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42fdd-130">Return value</span></span>

<span data-ttu-id="42fdd-131">Restituisce lo stato corrente per l'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="42fdd-131">Returns the current state for the specified item.</span></span> <span data-ttu-id="42fdd-132">Gli unici bit validi nel valore restituito sono quelli che corrispondono al set di bit nel parametro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="42fdd-132">The only valid bits in the return value are those that correspond to the bits set in the *lParam* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="42fdd-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="42fdd-133">Remarks</span></span>

<span data-ttu-id="42fdd-134">Le informazioni sullo stato di un elemento includono un set di flag di bit, nonché gli indici dell'elenco di immagini che indicano l'immagine di stato e l'immagine sovrapposta dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="42fdd-134">An item's state information includes a set of bit flags as well as image list indexes that indicate the item's state image and overlay image.</span></span>

## <a name="requirements"></a><span data-ttu-id="42fdd-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42fdd-135">Requirements</span></span>



| <span data-ttu-id="42fdd-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="42fdd-136">Requirement</span></span> | <span data-ttu-id="42fdd-137">Valore</span><span class="sxs-lookup"><span data-stu-id="42fdd-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42fdd-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42fdd-138">Minimum supported client</span></span><br/> | <span data-ttu-id="42fdd-139">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="42fdd-139">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="42fdd-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42fdd-140">Minimum supported server</span></span><br/> | <span data-ttu-id="42fdd-141">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="42fdd-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="42fdd-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42fdd-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="42fdd-143"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="42fdd-143"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42fdd-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42fdd-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42fdd-145">**\_SETITEMSTATE LVM**</span><span class="sxs-lookup"><span data-stu-id="42fdd-145">**LVM\_SETITEMSTATE**</span></span>](lvm-setitemstate.md)
</dt> </dl>

 

 





