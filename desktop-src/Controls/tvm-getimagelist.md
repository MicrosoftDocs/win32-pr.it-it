---
title: Messaggio TVM_GETIMAGELIST (COMmctrl. h)
description: Recupera l'handle per l'elenco di immagini normale o di stato associato a un controllo di visualizzazione albero. È possibile inviare questo messaggio in modo esplicito o utilizzando la \_ macro TreeView Getimagine.
ms.assetid: bcf5eac8-cb07-4cf8-ad93-47319fc915a5
keywords:
- Controlli di Windows Message TVM_GETIMAGELIST
topic_type:
- apiref
api_name:
- TVM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e4e2503d9c6d57743059ee1da3049a36ed17f2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743391"
---
# <a name="tvm_getimagelist-message"></a><span data-ttu-id="51c77-105">Messaggio macchina virtuale TVM \_</span><span class="sxs-lookup"><span data-stu-id="51c77-105">TVM\_GETIMAGELIST message</span></span>

<span data-ttu-id="51c77-106">Recupera l'handle per l'elenco di immagini normale o di stato associato a un controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="51c77-106">Retrieves the handle to the normal or state image list associated with a tree-view control.</span></span> <span data-ttu-id="51c77-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**TreeView \_ getimagine**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist) .</span><span class="sxs-lookup"><span data-stu-id="51c77-107">You can send this message explicitly or by using the [**TreeView\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="51c77-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="51c77-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51c77-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="51c77-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="51c77-110">Tipo di elenco di immagini da recuperare.</span><span class="sxs-lookup"><span data-stu-id="51c77-110">Type of image list to retrieve.</span></span> <span data-ttu-id="51c77-111">Questo parametro può essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="51c77-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="51c77-112">Valore</span><span class="sxs-lookup"><span data-stu-id="51c77-112">Value</span></span>                                                                                                                                                      | <span data-ttu-id="51c77-113">Significato</span><span class="sxs-lookup"><span data-stu-id="51c77-113">Meaning</span></span>                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TVSIL_NORMAL"></span><span id="tvsil_normal"></span><dl> <span data-ttu-id="51c77-114"><dt>**TVSIL \_ normale**</dt></span><span class="sxs-lookup"><span data-stu-id="51c77-114"><dt>**TVSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="51c77-115">Indica l'elenco di immagini normale, che contiene immagini selezionate, non selezionate e sovrapposte per gli elementi di un controllo di visualizzazione albero.</span><span class="sxs-lookup"><span data-stu-id="51c77-115">Indicates the normal image list, which contains selected, nonselected, and overlay images for the items of a tree-view control.</span></span><br/>                                                          |
| <span id="TVSIL_STATE"></span><span id="tvsil_state"></span><dl> <span data-ttu-id="51c77-116"><dt>**\_stato TVSIL**</dt></span><span class="sxs-lookup"><span data-stu-id="51c77-116"><dt>**TVSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="51c77-117">Indica l'elenco di immagini di stato.</span><span class="sxs-lookup"><span data-stu-id="51c77-117">Indicates the state image list.</span></span> <span data-ttu-id="51c77-118">È possibile usare le immagini di stato per indicare gli Stati degli elementi definiti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="51c77-118">You can use state images to indicate application-defined item states.</span></span> <span data-ttu-id="51c77-119">Viene visualizzata un'immagine di stato a sinistra dell'immagine selezionata o non selezionata di un elemento.</span><span class="sxs-lookup"><span data-stu-id="51c77-119">A state image is displayed to the left of an item's selected or nonselected image.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="51c77-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="51c77-120">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="51c77-121">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="51c77-121">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51c77-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="51c77-122">Return value</span></span>

<span data-ttu-id="51c77-123">Restituisce un handle HIMAGELIST per l'elenco di immagini specificato.</span><span class="sxs-lookup"><span data-stu-id="51c77-123">Returns an HIMAGELIST handle to the specified image list.</span></span>

## <a name="requirements"></a><span data-ttu-id="51c77-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51c77-124">Requirements</span></span>



| <span data-ttu-id="51c77-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="51c77-125">Requirement</span></span> | <span data-ttu-id="51c77-126">Valore</span><span class="sxs-lookup"><span data-stu-id="51c77-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="51c77-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51c77-127">Minimum supported client</span></span><br/> | <span data-ttu-id="51c77-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="51c77-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="51c77-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51c77-129">Minimum supported server</span></span><br/> | <span data-ttu-id="51c77-130">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="51c77-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="51c77-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="51c77-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="51c77-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="51c77-132"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51c77-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51c77-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51c77-134">**\_SEimagine TVM**</span><span class="sxs-lookup"><span data-stu-id="51c77-134">**TVM\_SETIMAGELIST**</span></span>](tvm-setimagelist.md)
</dt> </dl>

 

 





