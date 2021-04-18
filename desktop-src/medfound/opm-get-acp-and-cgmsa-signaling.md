---
description: 'Altre informazioni su: OPM_GET_ACP_AND_CGMSA_SIGNALING'
ms.assetid: d477fe3e-4498-450b-93b7-ce74ae9ed005
title: OPM_GET_ACP_AND_CGMSA_SIGNALING (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bf6294c3f1d90ac8a2292c65b3c1b8558e69220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309064"
---
# <a name="opm_get_acp_and_cgmsa_signaling"></a><span data-ttu-id="8eadc-103">\_per la \_ \_ segnalazione di ACP e \_ CGMSA \_</span><span class="sxs-lookup"><span data-stu-id="8eadc-103">OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>

<span data-ttu-id="8eadc-104">Restituisce le informazioni seguenti su un output video:</span><span class="sxs-lookup"><span data-stu-id="8eadc-104">Returns the following information about a video output:</span></span>

-   <span data-ttu-id="8eadc-105">Elenco di standard di protezione della televisione supportati dal driver.</span><span class="sxs-lookup"><span data-stu-id="8eadc-105">A list of television protection standards supported by the driver.</span></span>
-   <span data-ttu-id="8eadc-106">Standard attualmente attivo.</span><span class="sxs-lookup"><span data-stu-id="8eadc-106">The standard that is currently active.</span></span>
-   <span data-ttu-id="8eadc-107">Proporzioni correnti o altri dati di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="8eadc-107">The current aspect ratio or other signaling data.</span></span>



| <span data-ttu-id="8eadc-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="8eadc-108">Requirement</span></span> | <span data-ttu-id="8eadc-109">Valore</span><span class="sxs-lookup"><span data-stu-id="8eadc-109">Value</span></span> |
|--------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8eadc-110">GUID richiesta</span><span class="sxs-lookup"><span data-stu-id="8eadc-110">Request GUID</span></span> | <span data-ttu-id="8eadc-111">\_per la \_ \_ segnalazione di ACP e \_ CGMSA \_</span><span class="sxs-lookup"><span data-stu-id="8eadc-111">OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING</span></span>                                                |
| <span data-ttu-id="8eadc-112">Dati di input</span><span class="sxs-lookup"><span data-stu-id="8eadc-112">Input data</span></span>   | <span data-ttu-id="8eadc-113">nessuno</span><span class="sxs-lookup"><span data-stu-id="8eadc-113">None</span></span>                                                                                |
| <span data-ttu-id="8eadc-114">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="8eadc-114">Return data</span></span>  | <span data-ttu-id="8eadc-115">Struttura [**di \_ \_ \_ \_ segnalazione ACP e CGMSA di OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling)</span><span class="sxs-lookup"><span data-stu-id="8eadc-115">An [**OPM\_ACP\_AND\_CGMSA\_SIGNALING**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="8eadc-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="8eadc-116">Remarks</span></span>

<span data-ttu-id="8eadc-117">Questa query equivale alla \_ query DXVA COPPQuerySignaling utilizzata in Certified Output Protocol (Copp).</span><span class="sxs-lookup"><span data-stu-id="8eadc-117">This query is equivalent to the DXVA\_COPPQuerySignaling query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="8eadc-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8eadc-118">Requirements</span></span>



| <span data-ttu-id="8eadc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="8eadc-119">Requirement</span></span> | <span data-ttu-id="8eadc-120">Valore</span><span class="sxs-lookup"><span data-stu-id="8eadc-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8eadc-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8eadc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8eadc-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8eadc-122">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="8eadc-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8eadc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8eadc-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8eadc-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8eadc-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8eadc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8eadc-126"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8eadc-126"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8eadc-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8eadc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eadc-128">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="8eadc-128">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="8eadc-129">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="8eadc-129">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="8eadc-130">Richieste di stato di OPM</span><span class="sxs-lookup"><span data-stu-id="8eadc-130">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




