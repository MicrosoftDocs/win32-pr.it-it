---
description: Restituisce il livello di protezione globale per un meccanismo di protezione specificato.
ms.assetid: 3dd4f6f0-2305-4470-bbd4-7737fa2d8eae
title: OPM_GET_ACTUAL_PROTECTION_LEVEL (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 960d704fd44ca779f128795b26603698bb0ad622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049659"
---
# <a name="opm_get_actual_protection_level"></a><span data-ttu-id="765b5-103">OPM \_ ottenere \_ il \_ livello di protezione effettivo \_</span><span class="sxs-lookup"><span data-stu-id="765b5-103">OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="765b5-104">Restituisce il livello di protezione globale per un meccanismo di protezione specificato.</span><span class="sxs-lookup"><span data-stu-id="765b5-104">Returns the global protection level for a specified protection mechanism.</span></span>



| <span data-ttu-id="765b5-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="765b5-105">Requirement</span></span> | <span data-ttu-id="765b5-106">Valore</span><span class="sxs-lookup"><span data-stu-id="765b5-106">Value</span></span> |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="765b5-107">GUID richiesta</span><span class="sxs-lookup"><span data-stu-id="765b5-107">Request GUID</span></span> | <span data-ttu-id="765b5-108">OPM \_ ottenere \_ il \_ livello di protezione effettivo \_</span><span class="sxs-lookup"><span data-stu-id="765b5-108">OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL</span></span>                                                                                                                                       |
| <span data-ttu-id="765b5-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="765b5-109">Input data</span></span>   | <span data-ttu-id="765b5-110">Meccanismo di protezione per la query, specificato come intero a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="765b5-110">The protection mechanism to query, specified as a 32-bit integer.</span></span> <span data-ttu-id="765b5-111">Il valore viene interpretato come un membro dei [flag del tipo di protezione OPM](opm-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="765b5-111">The value is interpreted as a member of the [OPM Protection Type Flags](opm-protection-type-flags.md).</span></span> |
| <span data-ttu-id="765b5-112">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="765b5-112">Return data</span></span>  | <span data-ttu-id="765b5-113">Struttura [**di \_ \_ informazioni standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="765b5-113">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="765b5-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="765b5-114">Remarks</span></span>

<span data-ttu-id="765b5-115">Il livello di protezione globale è il livello di protezione attualmente applicato al connettore, indipendentemente dal modo in cui il driver di grafica ha richiesto di applicare la protezione.</span><span class="sxs-lookup"><span data-stu-id="765b5-115">The global protection level is the protection level that is currently being applied on the connector, regardless of how the graphics driver was instructed to apply the protection.</span></span> <span data-ttu-id="765b5-116">Ad esempio, un'applicazione può impostare il livello di protezione ACP chiamando la funzione **ChangeDisplaySettingsEx** .</span><span class="sxs-lookup"><span data-stu-id="765b5-116">For example, an application can set the ACP protection level by calling the **ChangeDisplaySettingsEx** function.</span></span> <span data-ttu-id="765b5-117">In tal caso, il livello di protezione globale rifletterebbe questa impostazione, anche se non è stata richiesta tramite output Protection Manager (OPM).</span><span class="sxs-lookup"><span data-stu-id="765b5-117">In that case, the global protection level would reflect this setting, even though it was not requested through Output Protection Manager (OPM).</span></span>

<span data-ttu-id="765b5-118">Il livello di protezione viene restituito nel membro **ulInformation** della struttura [**di \_ \_ informazioni standard di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="765b5-118">The protection level is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="765b5-119">Il significato di questo valore dipende dal meccanismo di protezione su cui viene eseguita una query.</span><span class="sxs-lookup"><span data-stu-id="765b5-119">The meaning of this value depends on the protection mechanism that is queried.</span></span> <span data-ttu-id="765b5-120">Per ogni meccanismo di protezione, il valore di **ulInformation** è un flag di un'enumerazione diversa, come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="765b5-120">For each protection mechanism, the value of **ulInformation** is a flag from a different enumeration, as shown in the following table.</span></span>



| <span data-ttu-id="765b5-121">Meccanismo di protezione</span><span class="sxs-lookup"><span data-stu-id="765b5-121">Protection mechanism</span></span> | <span data-ttu-id="765b5-122">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="765b5-122">Enumeration</span></span>                                                       |
|----------------------|-------------------------------------------------------------------|
| <span data-ttu-id="765b5-123">ACP</span><span class="sxs-lookup"><span data-stu-id="765b5-123">ACP</span></span>                  | [<span data-ttu-id="765b5-124">**\_livello di \_ protezione \_ ACP di OPM**</span><span class="sxs-lookup"><span data-stu-id="765b5-124">**OPM\_ACP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_acp_protection_level)   |
| <span data-ttu-id="765b5-125">CGMS-A</span><span class="sxs-lookup"><span data-stu-id="765b5-125">CGMS-A</span></span>               | [<span data-ttu-id="765b5-126">CGMS-flag di protezione</span><span class="sxs-lookup"><span data-stu-id="765b5-126">CGMS-A Protection Flags</span></span>](cgms-a-protection-flags.md)            |
| <span data-ttu-id="765b5-127">DPCP</span><span class="sxs-lookup"><span data-stu-id="765b5-127">DPCP</span></span>                 | [<span data-ttu-id="765b5-128">**\_livello di \_ protezione \_ DPCP OPM**</span><span class="sxs-lookup"><span data-stu-id="765b5-128">**OPM\_DPCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_dpcp_protection_level) |
| <span data-ttu-id="765b5-129">PROTOCOLLO HDCP</span><span class="sxs-lookup"><span data-stu-id="765b5-129">HDCP</span></span>                 | [<span data-ttu-id="765b5-130">**\_livello di \_ protezione \_ HDCP di OPM**</span><span class="sxs-lookup"><span data-stu-id="765b5-130">**OPM\_HDCP\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/opmapi/ne-opmapi-opm_hdcp_protection_level) |



 

<span data-ttu-id="765b5-131">Questa query equivale alla \_ query DXVA COPPQueryGlobalProtectionLevel utilizzata in Certified Output Protocol (Copp).</span><span class="sxs-lookup"><span data-stu-id="765b5-131">This query is equivalent to the DXVA\_COPPQueryGlobalProtectionLevel query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="765b5-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="765b5-132">Requirements</span></span>



| <span data-ttu-id="765b5-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="765b5-133">Requirement</span></span> | <span data-ttu-id="765b5-134">Valore</span><span class="sxs-lookup"><span data-stu-id="765b5-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="765b5-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="765b5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="765b5-136">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="765b5-136">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="765b5-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="765b5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="765b5-138">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="765b5-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="765b5-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="765b5-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="765b5-140"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="765b5-140"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="765b5-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="765b5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="765b5-142">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="765b5-142">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="765b5-143">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="765b5-143">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="765b5-144">Richieste di stato di OPM</span><span class="sxs-lookup"><span data-stu-id="765b5-144">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




