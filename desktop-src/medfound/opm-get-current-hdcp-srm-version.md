---
description: Restituisce il numero di versione del messaggio di rinnovabilità del sistema (SRM) attualmente utilizzato dall'output del video.
ms.assetid: 65d4b98b-369f-4863-a28c-f9e3b4c2b55d
title: OPM_GET_CURRENT_HDCP_SRM_VERSION (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e05ad53ae58e2141c63179c84a90f90cea86fb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309058"
---
# <a name="opm_get_current_hdcp_srm_version"></a><span data-ttu-id="5c26d-103">OPM \_ ottenere \_ la \_ versione corrente di HDCP \_ SRM \_</span><span class="sxs-lookup"><span data-stu-id="5c26d-103">OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION</span></span>

<span data-ttu-id="5c26d-104">Restituisce il numero di versione del messaggio di rinnovabilità del sistema (SRM) attualmente utilizzato dall'output del video.</span><span class="sxs-lookup"><span data-stu-id="5c26d-104">Returns the version number of the system renewability message (SRM) currently used by the video output.</span></span>



| <span data-ttu-id="5c26d-105">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c26d-105">Requirement</span></span> | <span data-ttu-id="5c26d-106">Valore</span><span class="sxs-lookup"><span data-stu-id="5c26d-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="5c26d-107">GUID richiesta</span><span class="sxs-lookup"><span data-stu-id="5c26d-107">Request GUID</span></span> | <span data-ttu-id="5c26d-108">OPM \_ ottenere \_ la \_ versione corrente di HDCP \_ SRM \_</span><span class="sxs-lookup"><span data-stu-id="5c26d-108">OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION</span></span>                                       |
| <span data-ttu-id="5c26d-109">Dati di input</span><span class="sxs-lookup"><span data-stu-id="5c26d-109">Input data</span></span>   | <span data-ttu-id="5c26d-110">nessuno</span><span class="sxs-lookup"><span data-stu-id="5c26d-110">None</span></span>                                                                        |
| <span data-ttu-id="5c26d-111">Restituisce i dati</span><span class="sxs-lookup"><span data-stu-id="5c26d-111">Return data</span></span>  | <span data-ttu-id="5c26d-112">Struttura [**di \_ \_ informazioni standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="5c26d-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="5c26d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c26d-113">Remarks</span></span>

<span data-ttu-id="5c26d-114">Se la query ha esito positivo, il membro **ulInformation** della struttura di [**\_ \_ informazioni standard di OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) contiene il numero di versione SRM, in formato little-endian.</span><span class="sxs-lookup"><span data-stu-id="5c26d-114">If this query succeeds, the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure contains the SRM version number, in little-endian format.</span></span>

<span data-ttu-id="5c26d-115">SRM vengono usati per aggiornare l'elenco dei dispositivi High-Bandwidth Digital protezione del contenuto (HDCP) revocati.</span><span class="sxs-lookup"><span data-stu-id="5c26d-115">SRMs are used to update the list of revoked High-Bandwidth Digital Content Protection (HDCP) devices.</span></span> <span data-ttu-id="5c26d-116">SRM vengono forniti con il contenuto video.</span><span class="sxs-lookup"><span data-stu-id="5c26d-116">SRMs are delivered with the video content.</span></span> <span data-ttu-id="5c26d-117">Per impostare SRM, inviare il comando [**OPM \_ set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) .</span><span class="sxs-lookup"><span data-stu-id="5c26d-117">To set the SRM, send the [**OPM\_SET\_HDCP\_SRM**](opm-set-hdcp-srm.md) command.</span></span>

<span data-ttu-id="5c26d-118">Questa query può causare il metodo [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) per restituire uno dei codici di errore seguenti.</span><span class="sxs-lookup"><span data-stu-id="5c26d-118">This query can cause the [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) method to return any of the following error codes.</span></span>



| <span data-ttu-id="5c26d-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5c26d-119">Return code</span></span>                                            | <span data-ttu-id="5c26d-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c26d-120">Description</span></span>                             |
|--------------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="5c26d-121">ERRORE \_ grafica \_ OPM \_ HDCP \_ SRM \_ mai \_ impostato</span><span class="sxs-lookup"><span data-stu-id="5c26d-121">ERROR\_GRAPHICS\_OPM\_HDCP\_SRM\_NEVER\_SET</span></span>            | <span data-ttu-id="5c26d-122">L'applicazione non ha impostato un SRM.</span><span class="sxs-lookup"><span data-stu-id="5c26d-122">The application did not set an SRM.</span></span>     |
| <span data-ttu-id="5c26d-123">ERRORE \_ l' \_ output OPM della grafica non \_ \_ \_ \_ supporta \_ HDCP</span><span class="sxs-lookup"><span data-stu-id="5c26d-123">ERROR\_GRAPHICS\_OPM\_OUTPUT\_DOES\_NOT\_SUPPORT\_HDCP</span></span> | <span data-ttu-id="5c26d-124">L'output del video non supporta la HDCP.</span><span class="sxs-lookup"><span data-stu-id="5c26d-124">The video output does not support HDCP.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="5c26d-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c26d-125">Requirements</span></span>



| <span data-ttu-id="5c26d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c26d-126">Requirement</span></span> | <span data-ttu-id="5c26d-127">Valore</span><span class="sxs-lookup"><span data-stu-id="5c26d-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5c26d-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c26d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5c26d-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5c26d-129">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5c26d-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c26d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5c26d-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5c26d-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5c26d-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c26d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c26d-133"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c26d-133"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c26d-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c26d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c26d-135">**IOPMVideoOutput:: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="5c26d-135">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="5c26d-136">Richieste di stato di OPM</span><span class="sxs-lookup"><span data-stu-id="5c26d-136">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




