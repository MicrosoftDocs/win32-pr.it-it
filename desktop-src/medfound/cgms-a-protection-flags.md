---
description: Specificare i livelli di protezione per il sistema di gestione della generazione della copia&\# 8212; Analogico (CGMS-A).
ms.assetid: 739e2f9e-b8f1-4ee1-8706-9a069773a3de
title: CGMS-flag di protezione (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3329ae13741490f2783d548baeead65ba59bc5ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401552"
---
# <a name="cgms-a-protection-flags"></a><span data-ttu-id="4ac3b-103">CGMS-flag di protezione</span><span class="sxs-lookup"><span data-stu-id="4ac3b-103">CGMS-A Protection Flags</span></span>

<span data-ttu-id="4ac3b-104">Le costanti nella tabella seguente specificano i livelli di protezione per l'analogico del sistema di gestione della generazione di copia (CGMS-A).</span><span class="sxs-lookup"><span data-stu-id="4ac3b-104">The constants in the following table specify the protection levels for Copy Generation Management System Analog (CGMS-A).</span></span>



| <span data-ttu-id="4ac3b-105">Costante/valore</span><span class="sxs-lookup"><span data-stu-id="4ac3b-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="4ac3b-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ac3b-106">Description</span></span>                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_CGMSA_OFF"></span><span id="opm_cgmsa_off"></span><dl> <span data-ttu-id="4ac3b-107"><dt>**OPM \_ CGMSA \_ off**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="4ac3b-107"><dt>**OPM\_CGMSA\_OFF**</dt> <dt>0x00</dt></span></span> </dl>                                                                                       | <span data-ttu-id="4ac3b-108">CGMS-A è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-108">CGMS-A is disabled.</span></span> <br/>                                                                                                   |
| <span id="OPM_CGMSA_COPY_FREELY"></span><span id="opm_cgmsa_copy_freely"></span><dl> <span data-ttu-id="4ac3b-109"><dt>**OPM \_ Copia di CGMSA \_ \_ liberamente**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="4ac3b-109"><dt>**OPM\_CGMSA\_COPY\_FREELY**</dt> <dt>0x01</dt></span></span> </dl>                                                              | <span data-ttu-id="4ac3b-110">Il livello di protezione è copy free.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-110">The protection level is Copy Freely.</span></span><br/>                                                                                   |
| <span id="OPM_CGMSA_COPY_NO_MORE"></span><span id="opm_cgmsa_copy_no_more"></span><dl> <span data-ttu-id="4ac3b-111"><dt>**OPM \_ CGMSA \_ Copia \_ non \_ più**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="4ac3b-111"><dt>**OPM\_CGMSA\_COPY\_NO\_MORE**</dt> <dt>0x02</dt></span></span> </dl>                                                          | <span data-ttu-id="4ac3b-112">Il livello di protezione non è più disponibile per la copia.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-112">The protection level is Copy No More.</span></span> <br/>                                                                                 |
| <span id="OPM_CGMSA_COPY_ONE_GENERATION"></span><span id="opm_cgmsa_copy_one_generation"></span><dl> <span data-ttu-id="4ac3b-113"><dt>**OPM \_ CGMSA \_ copia 0x03 di \_ una \_ generazione**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4ac3b-113"><dt>**OPM\_CGMSA\_COPY\_ONE\_GENERATION**</dt> <dt>0x03</dt></span></span> </dl>                                     | <span data-ttu-id="4ac3b-114">Il livello di protezione è copia di una generazione.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-114">The protection level is Copy One Generation.</span></span> <br/>                                                                          |
| <span id="OPM_CGMSA_COPY_NEVER"></span><span id="opm_cgmsa_copy_never"></span><dl> <span data-ttu-id="4ac3b-115"><dt>**OPM \_ CGMSA \_ copy \_ Never**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="4ac3b-115"><dt>**OPM\_CGMSA\_COPY\_NEVER**</dt> <dt>0x04</dt></span></span> </dl>                                                                 | <span data-ttu-id="4ac3b-116">Il livello di protezione non è mai copiato.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-116">The protection level is Copy Never.</span></span><br/>                                                                                    |
| <span id="OPM_CGMSA_REDISTRIBUTION_CONTROL_REQUIRED"></span><span id="opm_cgmsa_redistribution_control_required"></span><dl> <span data-ttu-id="4ac3b-117"><dt>**OPM \_ Il \_ controllo di ridistribuzione CGMSA è \_ \_ obbligatorio**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="4ac3b-117"><dt>**OPM\_CGMSA\_REDISTRIBUTION\_CONTROL\_REQUIRED**</dt> <dt>0x08</dt></span></span> </dl> | <span data-ttu-id="4ac3b-118">È necessario il controllo di ridistribuzione (detto anche *flag di trasmissione*).</span><span class="sxs-lookup"><span data-stu-id="4ac3b-118">Redistribution control (also called the *broadcast flag*) is required.</span></span> <span data-ttu-id="4ac3b-119">Questo flag può essere combinato con gli altri flag.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-119">This flag can be combined with the other flags.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4ac3b-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ac3b-120">Remarks</span></span>

<span data-ttu-id="4ac3b-121">Questi flag sono equivalenti alle costanti di enumerazione del **\_ livello di \_ protezione \_ Copp CGMSA** utilizzate nel protocollo di protezione output (Copp) certificato.</span><span class="sxs-lookup"><span data-stu-id="4ac3b-121">These flags are equivalent to the **COPP\_CGMSA\_Protection\_Level** enumeration constants used in the Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ac3b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ac3b-122">Requirements</span></span>



| <span data-ttu-id="4ac3b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ac3b-123">Requirement</span></span> | <span data-ttu-id="4ac3b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4ac3b-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4ac3b-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ac3b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4ac3b-126">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4ac3b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4ac3b-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ac3b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4ac3b-128">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4ac3b-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4ac3b-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4ac3b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ac3b-130"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ac3b-130"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ac3b-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ac3b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ac3b-132">Costanti Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4ac3b-132">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




