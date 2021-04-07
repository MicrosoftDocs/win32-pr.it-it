---
title: Messaggio di EM_SETPAGEROTATE (RichEdit. h)
description: Imposta il layout del testo per un controllo Rich Edit.
ms.assetid: 3c2a37fe-ee9f-4b34-87bf-7ac27d010afc
keywords:
- Controlli di Windows Message EM_SETPAGEROTATE
topic_type:
- apiref
api_name:
- EM_SETPAGEROTATE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eb595456bca444c92b536b0e428ee56a5903ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964119"
---
# <a name="em_setpagerotate-message"></a><span data-ttu-id="d54d0-104">\_Messaggio SETPAGEROTATE em</span><span class="sxs-lookup"><span data-stu-id="d54d0-104">EM\_SETPAGEROTATE message</span></span>

<span data-ttu-id="d54d0-105">\[**Em \_ SETPAGEROTATE** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="d54d0-105">\[**EM\_SETPAGEROTATE** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d54d0-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]</span><span class="sxs-lookup"><span data-stu-id="d54d0-106">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="d54d0-107">Imposta il layout del testo per un controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="d54d0-107">Sets the text layout for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d54d0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d54d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d54d0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d54d0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d54d0-110">Valore del layout del testo.</span><span class="sxs-lookup"><span data-stu-id="d54d0-110">Text layout value.</span></span> <span data-ttu-id="d54d0-111">Può corrispondere a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d54d0-111">This can be one of the following values.</span></span>



| <span data-ttu-id="d54d0-112">Valore</span><span class="sxs-lookup"><span data-stu-id="d54d0-112">Value</span></span>                                                                                                                                       | <span data-ttu-id="d54d0-113">Significato</span><span class="sxs-lookup"><span data-stu-id="d54d0-113">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="EPR_0"></span><span id="epr_0"></span><dl> <span data-ttu-id="d54d0-114"><dt>**EPR \_ 0**</dt></span><span class="sxs-lookup"><span data-stu-id="d54d0-114"><dt>**EPR\_0**</dt></span></span> </dl>       | <span data-ttu-id="d54d0-115">Il testo scorre da sinistra verso destra e dall'alto verso il basso.</span><span class="sxs-lookup"><span data-stu-id="d54d0-115">Text flows from left to right and from top to bottom.</span></span><br/>                              |
| <span id="EPR_90"></span><span id="epr_90"></span><dl> <span data-ttu-id="d54d0-116"><dt>**EPR \_ 90**</dt></span><span class="sxs-lookup"><span data-stu-id="d54d0-116"><dt>**EPR\_90**</dt></span></span> </dl>    | <span data-ttu-id="d54d0-117">Il testo scorre dal basso verso l'alto e da sinistra a destra.</span><span class="sxs-lookup"><span data-stu-id="d54d0-117">Text flows from bottom to top and from left to right.</span></span><br/>                              |
| <span id="EPR_180"></span><span id="epr_180"></span><dl> <span data-ttu-id="d54d0-118"><dt>**EPR \_ 180**</dt></span><span class="sxs-lookup"><span data-stu-id="d54d0-118"><dt>**EPR\_180**</dt></span></span> </dl> | <span data-ttu-id="d54d0-119">Il testo scorre da destra a sinistra e dal basso verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="d54d0-119">Text flows from right to left and from bottom to top.</span></span><br/>                              |
| <span id="EPR_270"></span><span id="epr_270"></span><dl> <span data-ttu-id="d54d0-120"><dt>**EPR \_ 270**</dt></span><span class="sxs-lookup"><span data-stu-id="d54d0-120"><dt>**EPR\_270**</dt></span></span> </dl> | <span data-ttu-id="d54d0-121">Il testo scorre dall'alto verso il basso e da destra a sinistra.</span><span class="sxs-lookup"><span data-stu-id="d54d0-121">Text flows from top to bottom and from right to left.</span></span><br/>                              |
| <span id="EPR_SE"></span><span id="epr_se"></span><dl> <span data-ttu-id="d54d0-122"><dt>**EPR \_ se**</dt></span><span class="sxs-lookup"><span data-stu-id="d54d0-122"><dt>**EPR\_SE**</dt></span></span> </dl>    | <span data-ttu-id="d54d0-123">**Windows 8:** Il testo scorre dall'alto verso il basso e da sinistra verso destra (layout di testo mongolo).</span><span class="sxs-lookup"><span data-stu-id="d54d0-123">**Windows 8:** Text flows top to bottom and left to right (Mongolian text layout).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d54d0-124">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d54d0-124">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d54d0-125">Non utilizzato; deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="d54d0-125">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d54d0-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d54d0-126">Return value</span></span>

<span data-ttu-id="d54d0-127">Il valore restituito è il nuovo valore del layout del testo.</span><span class="sxs-lookup"><span data-stu-id="d54d0-127">Return value is the new text layout value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d54d0-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="d54d0-128">Remarks</span></span>

<span data-ttu-id="d54d0-129">Questo messaggio consente di impostare il layout del testo per l'intero documento.</span><span class="sxs-lookup"><span data-stu-id="d54d0-129">This message sets the text layout for the entire document.</span></span> <span data-ttu-id="d54d0-130">Tuttavia, il contenuto incorporato non viene ruotato e deve essere ruotato separatamente dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d54d0-130">However, embedded contents are not rotated and must be rotated separately by the application.</span></span>

## <a name="requirements"></a><span data-ttu-id="d54d0-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d54d0-131">Requirements</span></span>



| <span data-ttu-id="d54d0-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d54d0-132">Requirement</span></span> | <span data-ttu-id="d54d0-133">Valore</span><span class="sxs-lookup"><span data-stu-id="d54d0-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d54d0-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d54d0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="d54d0-135">Solo app desktop Windows XP con SP1 \[\]</span><span class="sxs-lookup"><span data-stu-id="d54d0-135">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d54d0-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d54d0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="d54d0-137">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d54d0-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d54d0-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d54d0-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="d54d0-139"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d54d0-139"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d54d0-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d54d0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d54d0-141">**\_GETPAGEROTATE em**</span><span class="sxs-lookup"><span data-stu-id="d54d0-141">**EM\_GETPAGEROTATE**</span></span>](em-getpagerotate.md)
</dt> </dl>

 

 





