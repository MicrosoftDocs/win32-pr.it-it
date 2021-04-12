---
title: Messaggio LVM_SETCALLBACKMASK (COMmctrl. h)
description: Modifica la maschera di callback per un controllo visualizzazione elenco. È possibile inviare questo messaggio in modo esplicito o usando la \_ macro SetCallbackMask di ListView.
ms.assetid: d7828bab-9897-408c-99ca-fad42b431be8
keywords:
- Controlli di Windows Message LVM_SETCALLBACKMASK
topic_type:
- apiref
api_name:
- LVM_SETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef6dd46228c4e4aeada30f469a77f9e67aff3a37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119470"
---
# <a name="lvm_setcallbackmask-message"></a><span data-ttu-id="d0a7e-105">\_Messaggio SETCALLBACKMASK LVM</span><span class="sxs-lookup"><span data-stu-id="d0a7e-105">LVM\_SETCALLBACKMASK message</span></span>

<span data-ttu-id="d0a7e-106">Modifica la maschera di callback per un controllo visualizzazione elenco.</span><span class="sxs-lookup"><span data-stu-id="d0a7e-106">Changes the callback mask for a list-view control.</span></span> <span data-ttu-id="d0a7e-107">È possibile inviare questo messaggio in modo esplicito o usando la macro [**\_ SetCallbackMask di ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask) .</span><span class="sxs-lookup"><span data-stu-id="d0a7e-107">You can send this message explicitly or by using the [**ListView\_SetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="d0a7e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0a7e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0a7e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d0a7e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d0a7e-110">Valore della maschera di callback.</span><span class="sxs-lookup"><span data-stu-id="d0a7e-110">Value of the callback mask.</span></span> <span data-ttu-id="d0a7e-111">I bit della maschera indicano gli Stati degli elementi o le immagini per cui l'applicazione archivia i dati dello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="d0a7e-111">The bits of the mask indicate the item states or images for which the application stores the current state data.</span></span> <span data-ttu-id="d0a7e-112">Questo valore può essere una qualsiasi combinazione delle costanti seguenti:</span><span class="sxs-lookup"><span data-stu-id="d0a7e-112">This value can be any combination of the following constants:</span></span>



| <span data-ttu-id="d0a7e-113">Valore</span><span class="sxs-lookup"><span data-stu-id="d0a7e-113">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="d0a7e-114">Significato</span><span class="sxs-lookup"><span data-stu-id="d0a7e-114">Meaning</span></span>                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <span data-ttu-id="d0a7e-115"><dt>**\_taglia lvis**</dt></span><span class="sxs-lookup"><span data-stu-id="d0a7e-115"><dt>**LVIS\_CUT**</dt></span></span> </dl>                                  | <span data-ttu-id="d0a7e-116">L'elemento è contrassegnato per un'operazione di taglia e incolla.</span><span class="sxs-lookup"><span data-stu-id="d0a7e-116">The item is marked for a cut-and-paste operation.</span></span><br/>                                       |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <span data-ttu-id="d0a7e-117"><dt>**\_DROPHILITED lvis**</dt></span><span class="sxs-lookup"><span data-stu-id="d0a7e-117"><dt>**LVIS\_DROPHILITED**</dt></span></span> </dl>          | <span data-ttu-id="d0a7e-118">L'elemento è evidenziato come destinazione di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="d0a7e-118">The item is highlighted as a drag-and-drop target.</span></span><br/>                                      |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <span data-ttu-id="d0a7e-119"><dt>**LVIS con stato \_ attivo**</dt></span><span class="sxs-lookup"><span data-stu-id="d0a7e-119"><dt>**LVIS\_FOCUSED**</dt></span></span> </dl>                      | <span data-ttu-id="d0a7e-120">L'elemento ha lo stato attivo.</span><span class="sxs-lookup"><span data-stu-id="d0a7e-120">The item has the focus.</span></span><br/>                                                                 |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <span data-ttu-id="d0a7e-121"><dt>**LVIS \_ selezionato**</dt></span><span class="sxs-lookup"><span data-stu-id="d0a7e-121"><dt>**LVIS\_SELECTED**</dt></span></span> </dl>                   | <span data-ttu-id="d0a7e-122">L'elemento è selezionato.</span><span class="sxs-lookup"><span data-stu-id="d0a7e-122">The item is selected.</span></span> <br/>                                                                  |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <span data-ttu-id="d0a7e-123"><dt>**\_OVERLAYMASK lvis**</dt></span><span class="sxs-lookup"><span data-stu-id="d0a7e-123"><dt>**LVIS\_OVERLAYMASK**</dt></span></span> </dl>          | <span data-ttu-id="d0a7e-124">L'applicazione archivia l'indice dell'elenco immagini dell'immagine sovrapposta corrente per ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="d0a7e-124">The application stores the image list index of the current overlay image for each item.</span></span><br/> |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <span data-ttu-id="d0a7e-125"><dt>**\_STATEIMAGEMASK lvis**</dt></span><span class="sxs-lookup"><span data-stu-id="d0a7e-125"><dt>**LVIS\_STATEIMAGEMASK**</dt></span></span> </dl> | <span data-ttu-id="d0a7e-126">L'applicazione archivia l'indice dell'elenco immagini dell'immagine di stato corrente per ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="d0a7e-126">The application stores the image list index of the current state image for each item.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="d0a7e-127">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d0a7e-127">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="d0a7e-128">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d0a7e-128">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0a7e-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0a7e-129">Return value</span></span>

<span data-ttu-id="d0a7e-130">Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d0a7e-130">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0a7e-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0a7e-131">Remarks</span></span>

<span data-ttu-id="d0a7e-132">La *maschera di callback* di un controllo visualizzazione elenco è un set di flag di bit che specificano gli Stati degli elementi per i quali l'applicazione, anziché il controllo, archivia i dati correnti.</span><span class="sxs-lookup"><span data-stu-id="d0a7e-132">The *callback mask* of a list-view control is a set of bit flags that specify the item states for which the application, rather than the control, stores the current data.</span></span> <span data-ttu-id="d0a7e-133">La maschera di callback viene applicata a tutti gli elementi del controllo, a differenza della designazione dell'elemento di callback che si applica a un elemento specifico.</span><span class="sxs-lookup"><span data-stu-id="d0a7e-133">The callback mask applies to all of the control's items, unlike the callback item designation, which applies to a specific item.</span></span> <span data-ttu-id="d0a7e-134">Per impostazione predefinita, la maschera di callback è zero, il che significa che il controllo elenco-visualizzazione archivia tutte le informazioni sullo stato dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="d0a7e-134">The callback mask is zero by default, meaning that the list-view control stores all item state information.</span></span> <span data-ttu-id="d0a7e-135">Dopo aver creato un controllo visualizzazione elenco e aver inizializzato gli elementi, è possibile inviare il messaggio **LVM \_ SETCALLBACKMASK** per modificare la maschera di callback.</span><span class="sxs-lookup"><span data-stu-id="d0a7e-135">After creating a list-view control and initializing its items, you can send the **LVM\_SETCALLBACKMASK** message to change the callback mask.</span></span> <span data-ttu-id="d0a7e-136">Per recuperare la maschera di callback corrente, inviare il messaggio [**LVM \_ GETCALLBACKMASK**](lvm-getcallbackmask.md) .</span><span class="sxs-lookup"><span data-stu-id="d0a7e-136">To retrieve the current callback mask, send the [**LVM\_GETCALLBACKMASK**](lvm-getcallbackmask.md) message.</span></span>

<span data-ttu-id="d0a7e-137">Per ulteriori informazioni sulle immagini sovrapposte e le immagini di stato, vedere [aggiunta di List-View elenchi di immagini](using-list-view-controls.md).</span><span class="sxs-lookup"><span data-stu-id="d0a7e-137">For more information about overlay images and state images, see [Adding List-View Image Lists](using-list-view-controls.md).</span></span>

<span data-ttu-id="d0a7e-138">Per altre informazioni sui callback di visualizzazione elenco, vedere [elementi di callback e maschera di callback](list-view-controls-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d0a7e-138">For more information on list-view callbacks, see [Callback Items and the Callback Mask](list-view-controls-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0a7e-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0a7e-139">Requirements</span></span>



| <span data-ttu-id="d0a7e-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0a7e-140">Requirement</span></span> | <span data-ttu-id="d0a7e-141">Valore</span><span class="sxs-lookup"><span data-stu-id="d0a7e-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0a7e-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0a7e-142">Minimum supported client</span></span><br/> | <span data-ttu-id="d0a7e-143">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d0a7e-143">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d0a7e-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0a7e-144">Minimum supported server</span></span><br/> | <span data-ttu-id="d0a7e-145">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d0a7e-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d0a7e-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0a7e-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0a7e-147"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0a7e-147"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0a7e-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0a7e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0a7e-149">**\_GETDISPINFO LVN**</span><span class="sxs-lookup"><span data-stu-id="d0a7e-149">**LVN\_GETDISPINFO**</span></span>](lvn-getdispinfo.md)
</dt> </dl>

 

 





