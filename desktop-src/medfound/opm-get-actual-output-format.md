---
description: Restituisce una descrizione del segnale video trasmesso sul connettore.
ms.assetid: 8464470f-49db-4559-80b2-02cfc473e30e
title: OPM_GET_ACTUAL_OUTPUT_FORMAT (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12eeca9bcf8fde670447afe4268a86ffa31b6a94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344421"
---
# <a name="opm_get_actual_output_format"></a><span data-ttu-id="e8685-103">\_formato di \_ \_ output effettivo \_ per OPM Get</span><span class="sxs-lookup"><span data-stu-id="e8685-103">OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT</span></span>

<span data-ttu-id="e8685-104">Restituisce una descrizione del segnale video trasmesso sul connettore.</span><span class="sxs-lookup"><span data-stu-id="e8685-104">Returns a description of the video signal that is being transmitted over the connector.</span></span>



| <span data-ttu-id="e8685-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8685-105">Requirement</span></span> | <span data-ttu-id="e8685-106">Valore</span><span class="sxs-lookup"><span data-stu-id="e8685-106">Value</span></span> |
|--------------|------------------------------------------------------------------------------|
| <span data-ttu-id="e8685-107">GUID richiesta</span><span class="sxs-lookup"><span data-stu-id="e8685-107">Request GUID</span></span> | <span data-ttu-id="e8685-108">\_formato di \_ \_ output effettivo \_ per OPM Get</span><span class="sxs-lookup"><span data-stu-id="e8685-108">OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT</span></span>                                             |
| <span data-ttu-id="e8685-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="e8685-109">Input data</span></span>   | <span data-ttu-id="e8685-110">nessuno</span><span class="sxs-lookup"><span data-stu-id="e8685-110">None</span></span>                                                                         |
| <span data-ttu-id="e8685-111">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="e8685-111">Return data</span></span>  | <span data-ttu-id="e8685-112">Struttura [**del \_ \_ \_ formato di output effettivo di OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format)</span><span class="sxs-lookup"><span data-stu-id="e8685-112">An [**OPM\_ACTUAL\_OUTPUT\_FORMAT**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e8685-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8685-113">Remarks</span></span>

<span data-ttu-id="e8685-114">Il segnale video trasmesso sul connettore non ha necessariamente lo stesso formato della modalità di visualizzazione del desktop.</span><span class="sxs-lookup"><span data-stu-id="e8685-114">The video signal that is transmitted over the connector does not necessarily have the same format as the desktop display mode.</span></span> <span data-ttu-id="e8685-115">La modalità di visualizzazione desktop, ad esempio, potrebbe essere 1024 x 768 pixel a 85 Hz, mentre il connettore potrebbe essere un connettore S-video che trasmette un segnale video a 720 x 480 pixel, 60/1.01 Hz interlacciato.</span><span class="sxs-lookup"><span data-stu-id="e8685-115">For example, the desktop display mode might be 1024 x 768 pixels at 85 Hz, while the connector might be an S-Video connector that transmits a video signal at 720 x 480 pixels, 60/1.01 Hz interlaced.</span></span> <span data-ttu-id="e8685-116">In tal caso, il driver restituirà la risoluzione del segnale S-video, non la risoluzione del desktop.</span><span class="sxs-lookup"><span data-stu-id="e8685-116">In that case, the driver would return the resolution of the S-Video signal, not the desktop resolution.</span></span>

<span data-ttu-id="e8685-117">Questa query equivale alla \_ query DXVA COPPQueryDisplayData utilizzata in Certified Output Protocol (Copp).</span><span class="sxs-lookup"><span data-stu-id="e8685-117">This query is equivalent to the DXVA\_COPPQueryDisplayData query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8685-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8685-118">Requirements</span></span>



| <span data-ttu-id="e8685-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8685-119">Requirement</span></span> | <span data-ttu-id="e8685-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e8685-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e8685-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8685-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e8685-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e8685-122">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="e8685-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8685-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e8685-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e8685-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e8685-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8685-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8685-126"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8685-126"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8685-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8685-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8685-128">**IOPMVideoOutput:: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="e8685-128">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="e8685-129">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="e8685-129">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="e8685-130">Richieste di stato di OPM</span><span class="sxs-lookup"><span data-stu-id="e8685-130">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




