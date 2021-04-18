---
description: Restituisce il livello di protezione virtuale per un meccanismo di protezione specificato.
ms.assetid: 635d54de-2735-4390-8bac-ba63b9503909
title: OPM_GET_VIRTUAL_PROTECTION_LEVEL (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7ac36abd0a043a74a18401205bbb5e661ac17d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309056"
---
# <a name="opm_get_virtual_protection_level"></a><span data-ttu-id="da432-103">\_livello di \_ \_ protezione virtuale \_ di OPM Get</span><span class="sxs-lookup"><span data-stu-id="da432-103">OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="da432-104">Restituisce il livello di protezione virtuale per un meccanismo di protezione specificato.</span><span class="sxs-lookup"><span data-stu-id="da432-104">Returns the virtual protection level for a specified protection mechanism.</span></span>

<span data-ttu-id="da432-105">Il livello di protezione *virtuale* è il livello richiesto dall'applicazione durante la sessione di output Protection Manager (OPM) corrente.</span><span class="sxs-lookup"><span data-stu-id="da432-105">The *virtual* protection level is the level requested by the application during the current Output Protection Manager (OPM) session.</span></span> <span data-ttu-id="da432-106">Il driver potrebbe applicare un livello superiore, a causa di eventi esterni a questa sessione di OPM.</span><span class="sxs-lookup"><span data-stu-id="da432-106">The driver might apply a higher level, due to events outside of this OPM session.</span></span> <span data-ttu-id="da432-107">Per individuare il livello di protezione effettivo attivo, inviare la query del [**\_ livello di \_ \_ protezione effettivo \_ dell'OPM**](opm-get-actual-protection-level.md) .</span><span class="sxs-lookup"><span data-stu-id="da432-107">To find the actual protection level that is in effect, send the [**OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL**](opm-get-actual-protection-level.md) query.</span></span>



| <span data-ttu-id="da432-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="da432-108">Requirement</span></span> | <span data-ttu-id="da432-109">Valore</span><span class="sxs-lookup"><span data-stu-id="da432-109">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da432-110">GUID richiesta</span><span class="sxs-lookup"><span data-stu-id="da432-110">Request GUID</span></span> | <span data-ttu-id="da432-111">\_livello di \_ \_ protezione virtuale \_ di OPM Get</span><span class="sxs-lookup"><span data-stu-id="da432-111">OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL</span></span>                                                                                                                                          |
| <span data-ttu-id="da432-112">Dati di input</span><span class="sxs-lookup"><span data-stu-id="da432-112">Input data</span></span>   | <span data-ttu-id="da432-113">Meccanismo di protezione per la query, specificato come intero a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="da432-113">The protection mechanism to query, specified as a 32-bit integer.</span></span> <span data-ttu-id="da432-114">Il valore viene interpretato come un membro dei [**flag del tipo di protezione OPM**](opm-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="da432-114">The value is interpreted as a member of the [**OPM Protection Type Flags**](opm-protection-type-flags.md).</span></span> |
| <span data-ttu-id="da432-115">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="da432-115">Return data</span></span>  | <span data-ttu-id="da432-116">Struttura [**di \_ \_ informazioni standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="da432-116">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span>                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="da432-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="da432-117">Remarks</span></span>

<span data-ttu-id="da432-118">Il livello di protezione viene restituito nel membro **ulInformation** della struttura [**di \_ \_ informazioni standard di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="da432-118">The protection level is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="da432-119">Il significato di questo valore dipende dal meccanismo di protezione su cui viene eseguita una query.</span><span class="sxs-lookup"><span data-stu-id="da432-119">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="da432-120">Per ogni meccanismo di protezione, il valore di **ulInformation** è un flag di un'enumerazione diversa, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="da432-120">For each protection mechanism, the value of **ulInformation** is a flag from a different enumeration, as shown in the following table.</span></span>



| <span data-ttu-id="da432-121">Meccanismo di protezione</span><span class="sxs-lookup"><span data-stu-id="da432-121">Protection mechanism</span></span> | <span data-ttu-id="da432-122">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="da432-122">Enumeration</span></span>                                                       |
|----------------------|-------------------------------------------------------------------|
| <span data-ttu-id="da432-123">ACP</span><span class="sxs-lookup"><span data-stu-id="da432-123">ACP</span></span>                  | [<span data-ttu-id="da432-124">**\_livello di \_ protezione \_ ACP di OPM**</span><span class="sxs-lookup"><span data-stu-id="da432-124">**OPM\_ACP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| <span data-ttu-id="da432-125">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="da432-125">CGMS-A</span></span>               | [<span data-ttu-id="da432-126">**CGMS-flag di protezione**</span><span class="sxs-lookup"><span data-stu-id="da432-126">**CGMS-A Protection Flags**</span></span>](cgms-a-protection-flags.md)        |
| <span data-ttu-id="da432-127">DPCP</span><span class="sxs-lookup"><span data-stu-id="da432-127">DPCP</span></span>                 | [<span data-ttu-id="da432-128">**\_livello di \_ protezione \_ DPCP OPM**</span><span class="sxs-lookup"><span data-stu-id="da432-128">**OPM\_DPCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| <span data-ttu-id="da432-129">PROTOCOLLO HDCP</span><span class="sxs-lookup"><span data-stu-id="da432-129">HDCP</span></span>                 | [<span data-ttu-id="da432-130">**\_livello di \_ protezione \_ HDCP di OPM**</span><span class="sxs-lookup"><span data-stu-id="da432-130">**OPM\_HDCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

<span data-ttu-id="da432-131">Questa query equivale alla \_ query DXVA COPPQueryLocalProtectionLevel utilizzata in Certified Output Protocol (Copp).</span><span class="sxs-lookup"><span data-stu-id="da432-131">This query is equivalent to the DXVA\_COPPQueryLocalProtectionLevel query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="da432-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da432-132">Requirements</span></span>



| <span data-ttu-id="da432-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="da432-133">Requirement</span></span> | <span data-ttu-id="da432-134">Valore</span><span class="sxs-lookup"><span data-stu-id="da432-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="da432-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da432-135">Minimum supported client</span></span><br/> | <span data-ttu-id="da432-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="da432-136">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="da432-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="da432-137">Minimum supported server</span></span><br/> | <span data-ttu-id="da432-138">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="da432-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="da432-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da432-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="da432-140"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="da432-140"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da432-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da432-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da432-142">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="da432-142">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="da432-143">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="da432-143">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="da432-144">Richieste di stato di OPM</span><span class="sxs-lookup"><span data-stu-id="da432-144">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




