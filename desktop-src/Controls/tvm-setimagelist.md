---
title: Messaggio TVM_SETIMAGELIST (COMmctrl. h)
description: Imposta l'elenco di immagini normale o di stato per un controllo di visualizzazione albero e ridisegnato il controllo usando le nuove immagini. È possibile inviare questo messaggio in modo esplicito o usando la macro dell'oggetto TreeView \_ .
ms.assetid: 1a7bf2f8-c7db-44a8-b234-0ffc498e9000
keywords:
- Controlli di Windows Message TVM_SETIMAGELIST
topic_type:
- apiref
api_name:
- TVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f308cb8a56b2e74a5703af144bac03c271efc95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741554"
---
# <a name="tvm_setimagelist-message"></a><span data-ttu-id="eb930-105">\_Messaggio SEimagine TVM</span><span class="sxs-lookup"><span data-stu-id="eb930-105">TVM\_SETIMAGELIST message</span></span>

<span data-ttu-id="eb930-106">Imposta l'elenco di immagini normale o di stato per un controllo di visualizzazione albero e ridisegnato il controllo usando le nuove immagini.</span><span class="sxs-lookup"><span data-stu-id="eb930-106">Sets the normal or state image list for a tree-view control and redraws the control using the new images.</span></span> <span data-ttu-id="eb930-107">È possibile inviare questo messaggio in modo esplicito o usando la macro dell'oggetto [**TreeView \_**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist) .</span><span class="sxs-lookup"><span data-stu-id="eb930-107">You can send this message explicitly or by using the [**TreeView\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="eb930-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="eb930-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb930-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eb930-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb930-110">Tipo di elenco di immagini da impostare.</span><span class="sxs-lookup"><span data-stu-id="eb930-110">Type of image list to set.</span></span> <span data-ttu-id="eb930-111">Questo parametro può essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="eb930-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="eb930-112">Valore</span><span class="sxs-lookup"><span data-stu-id="eb930-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="eb930-113">Significato</span><span class="sxs-lookup"><span data-stu-id="eb930-113">Meaning</span></span>                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <span data-ttu-id="eb930-114"><dt>**TVSIL \_ normale**</dt></span><span class="sxs-lookup"><span data-stu-id="eb930-114"><dt>**TVSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="eb930-115">Indica l'elenco di immagini normale, che contiene immagini selezionate, non selezionate e sovrapposte per gli elementi di un controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="eb930-115">Indicates the normal image list, which contains selected, nonselected, and overlay images for the items of a tree-view control.</span></span><br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <span data-ttu-id="eb930-116"><dt>**\_stato TVSIL**</dt></span><span class="sxs-lookup"><span data-stu-id="eb930-116"><dt>**TVSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="eb930-117">Indica l'elenco di immagini di stato.</span><span class="sxs-lookup"><span data-stu-id="eb930-117">Indicates the state image list.</span></span> <span data-ttu-id="eb930-118">È possibile usare le immagini di stato per indicare gli Stati degli elementi definiti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="eb930-118">You can use state images to indicate application-defined item states.</span></span> <span data-ttu-id="eb930-119">Viene visualizzata un'immagine di stato a sinistra dell'immagine selezionata o non selezionata di un elemento.</span><span class="sxs-lookup"><span data-stu-id="eb930-119">A state image is displayed to the left of an item's selected or nonselected image.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="eb930-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eb930-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eb930-121">Handle per l'elenco di immagini.</span><span class="sxs-lookup"><span data-stu-id="eb930-121">Handle to the image list.</span></span> <span data-ttu-id="eb930-122">Se *lParam* è **null**, il messaggio rimuove l'elenco di immagini specificato dal controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="eb930-122">If *lParam* is **NULL**, the message removes the specified image list from the tree-view control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb930-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eb930-123">Return value</span></span>

<span data-ttu-id="eb930-124">Restituisce l'handle per l'elenco di immagini precedente, se presente, o **null** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="eb930-124">Returns the handle to the previous image list, if any, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb930-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="eb930-125">Remarks</span></span>

<span data-ttu-id="eb930-126">Il controllo di visualizzazione albero non eliminerà l'elenco di immagini specificato con questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="eb930-126">The tree-view control will not destroy the image list specified with this message.</span></span> <span data-ttu-id="eb930-127">Quando non è più necessario, l'applicazione deve eliminare l'elenco di immagini.</span><span class="sxs-lookup"><span data-stu-id="eb930-127">Your application must destroy the image list when it is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb930-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb930-128">Requirements</span></span>



| <span data-ttu-id="eb930-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb930-129">Requirement</span></span> | <span data-ttu-id="eb930-130">Valore</span><span class="sxs-lookup"><span data-stu-id="eb930-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb930-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb930-131">Minimum supported client</span></span><br/> | <span data-ttu-id="eb930-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eb930-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eb930-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb930-133">Minimum supported server</span></span><br/> | <span data-ttu-id="eb930-134">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eb930-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eb930-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eb930-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb930-136"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb930-136"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb930-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb930-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb930-138">**macchina \_ virtuale TVM**</span><span class="sxs-lookup"><span data-stu-id="eb930-138">**TVM\_GETIMAGELIST**</span></span>](tvm-getimagelist.md)
</dt> </dl>

 

 





