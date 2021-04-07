---
title: Messaggio HDM_SETIMAGELIST (COMmctrl. h)
description: Assegna un elenco di immagini a un controllo intestazione esistente. È possibile inviare questo messaggio in modo esplicito oppure usare l'intestazione \_ SetStateImageList o la \_ macro di intestazione.
ms.assetid: 1d7f07fa-f6f4-422a-949c-97d0388343e3
keywords:
- Controlli di Windows Message HDM_SETIMAGELIST
topic_type:
- apiref
api_name:
- HDM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17fe21d64b141cf27d32e00fac0ce78228421518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964161"
---
# <a name="hdm_setimagelist-message"></a><span data-ttu-id="25e2c-105">HDM \_ messaggio di immagine</span><span class="sxs-lookup"><span data-stu-id="25e2c-105">HDM\_SETIMAGELIST message</span></span>

<span data-ttu-id="25e2c-106">Assegna un elenco di immagini a un controllo intestazione esistente.</span><span class="sxs-lookup"><span data-stu-id="25e2c-106">Assigns an image list to an existing header control.</span></span> <span data-ttu-id="25e2c-107">È possibile inviare questo messaggio in modo esplicito oppure usare l'intestazione [**\_ SetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist) o la macro di intestazione. [**\_**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist)</span><span class="sxs-lookup"><span data-stu-id="25e2c-107">You can send this message explicitly or use the [**Header\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) or [**Header\_SetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="25e2c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="25e2c-108">Parameters</span></span>

<dl> <span data-ttu-id="25e2c-109"><dt>*wParam*</dt> </span><span class="sxs-lookup"><span data-stu-id="25e2c-109"><dt>*wParam* </dt> </span></span><dd><span data-ttu-id="25e2c-110">Uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="25e2c-110">One of the following values:</span></span>

| <span data-ttu-id="25e2c-111">Valore</span><span class="sxs-lookup"><span data-stu-id="25e2c-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="25e2c-112">Significato</span><span class="sxs-lookup"><span data-stu-id="25e2c-112">Meaning</span></span>                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <span data-ttu-id="25e2c-113"><dt>**HDSIL \_ normale**</dt></span><span class="sxs-lookup"><span data-stu-id="25e2c-113"><dt>**HDSIL\_NORMAL**</dt></span></span> </dl> | <span data-ttu-id="25e2c-114">Indica che si tratta di un elenco di immagini normale.</span><span class="sxs-lookup"><span data-stu-id="25e2c-114">Indicates that this is a normal image list.</span></span><br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <span data-ttu-id="25e2c-115"><dt>**\_stato HDSIL**</dt></span><span class="sxs-lookup"><span data-stu-id="25e2c-115"><dt>**HDSIL\_STATE**</dt></span></span> </dl>    | <span data-ttu-id="25e2c-116">Indica che si tratta di un elenco di immagini di stato.</span><span class="sxs-lookup"><span data-stu-id="25e2c-116">Indicates that this is a state image list.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="25e2c-117">*lParam*</span><span class="sxs-lookup"><span data-stu-id="25e2c-117">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="25e2c-118">Handle per un elenco di immagini.</span><span class="sxs-lookup"><span data-stu-id="25e2c-118">A handle to an image list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25e2c-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25e2c-119">Return value</span></span>

<span data-ttu-id="25e2c-120">Restituisce l'handle per l'elenco di immagini precedentemente associato al controllo.</span><span class="sxs-lookup"><span data-stu-id="25e2c-120">Returns the handle to the image list previously associated with the control.</span></span> <span data-ttu-id="25e2c-121">Restituisce **null** in caso di errore o se non è stato impostato in precedenza alcun elenco di immagini.</span><span class="sxs-lookup"><span data-stu-id="25e2c-121">Returns **NULL** upon failure or if no image list was set previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="25e2c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25e2c-122">Requirements</span></span>



| <span data-ttu-id="25e2c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="25e2c-123">Requirement</span></span> | <span data-ttu-id="25e2c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="25e2c-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25e2c-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25e2c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="25e2c-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="25e2c-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="25e2c-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25e2c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="25e2c-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="25e2c-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="25e2c-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25e2c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="25e2c-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="25e2c-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





