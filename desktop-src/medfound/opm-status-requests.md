---
description: Richieste di stato di OPM
ms.assetid: 428d08c6-e9f0-49fb-9ef9-d0f95416669d
title: Richieste di stato di OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd994d7cb8d43db23fe59352dba830e741b74b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753914"
---
# <a name="opm-status-requests"></a><span data-ttu-id="cd6d2-103">Richieste di stato di OPM</span><span class="sxs-lookup"><span data-stu-id="cd6d2-103">OPM Status Requests</span></span>

<span data-ttu-id="cd6d2-104">In questa sezione sono elencate le richieste di stato disponibili per l' [Output Protection Manager](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="cd6d2-104">This section lists the available status requests for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span> <span data-ttu-id="cd6d2-105">Per inviare una richiesta di stato di OPM, chiamare [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation).</span><span class="sxs-lookup"><span data-stu-id="cd6d2-105">To send an OPM status request, call [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation).</span></span> <span data-ttu-id="cd6d2-106">Per ogni richiesta sono elencate le informazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="cd6d2-106">For each request, the following information is listed.</span></span>



|              |                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd6d2-107">GUID richiesta</span><span class="sxs-lookup"><span data-stu-id="cd6d2-107">Request GUID</span></span> | <span data-ttu-id="cd6d2-108">Identifica la richiesta.</span><span class="sxs-lookup"><span data-stu-id="cd6d2-108">Identifies the request.</span></span> <span data-ttu-id="cd6d2-109">Impostare il membro **guidSetting** della struttura [**OPM \_ get \_ info \_ Parameters**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) uguale a questo valore.</span><span class="sxs-lookup"><span data-stu-id="cd6d2-109">Set the **guidSetting** member of the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="cd6d2-110">Dati di input</span><span class="sxs-lookup"><span data-stu-id="cd6d2-110">Input data</span></span>   | <span data-ttu-id="cd6d2-111">Specifica come interpretare la matrice **abParameters** nella struttura [**del \_ \_ \_ parametro OPM Get Info**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) .</span><span class="sxs-lookup"><span data-stu-id="cd6d2-111">Specifies how to interpret the **abParameters** array in the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure.</span></span>                      |
| <span data-ttu-id="cd6d2-112">Dati di output</span><span class="sxs-lookup"><span data-stu-id="cd6d2-112">Output data</span></span>  | <span data-ttu-id="cd6d2-113">Specifica come interpretare la matrice **abRequestedInformation** nella struttura [**di \_ \_ informazioni richiesta da OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) .</span><span class="sxs-lookup"><span data-stu-id="cd6d2-113">Specifies how to interpret the **abRequestedInformation** array in the [**OPM\_REQUESTED\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) structure.</span></span>         |



 

<span data-ttu-id="cd6d2-114">Sono definite le seguenti richieste di stato:</span><span class="sxs-lookup"><span data-stu-id="cd6d2-114">The following status requests are defined:</span></span>



| <span data-ttu-id="cd6d2-115">Richiesta di stato</span><span class="sxs-lookup"><span data-stu-id="cd6d2-115">Status request</span></span>                                                                                      | <span data-ttu-id="cd6d2-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd6d2-116">Description</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd6d2-117">**\_per la \_ \_ segnalazione di ACP e \_ CGMSA \_**</span><span class="sxs-lookup"><span data-stu-id="cd6d2-117">**OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-get-acp-and-cgmsa-signaling.md)                     | <span data-ttu-id="cd6d2-118">Restituisce le informazioni seguenti su un output video:</span><span class="sxs-lookup"><span data-stu-id="cd6d2-118">Returns the following information about a video output:</span></span>                                                                                               |
| [<span data-ttu-id="cd6d2-119">**\_formato di \_ \_ output effettivo \_ per OPM Get**</span><span class="sxs-lookup"><span data-stu-id="cd6d2-119">**OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT**</span></span>](opm-get-actual-output-format.md)                            | <span data-ttu-id="cd6d2-120">Restituisce una descrizione del segnale video trasmesso sul connettore.</span><span class="sxs-lookup"><span data-stu-id="cd6d2-120">Returns a description of the video signal that is being transmitted over the connector.</span></span>                                                               |
| [<span data-ttu-id="cd6d2-121">**OPM \_ ottenere \_ il \_ livello di protezione effettivo \_**</span><span class="sxs-lookup"><span data-stu-id="cd6d2-121">**OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-actual-protection-level.md)                      | <span data-ttu-id="cd6d2-122">Restituisce il livello di protezione globale per un meccanismo di protezione specificato.</span><span class="sxs-lookup"><span data-stu-id="cd6d2-122">Returns the global protection level for a specified protection mechanism.</span></span>                                                                             |
| [<span data-ttu-id="cd6d2-123">**\_tipo di \_ bus di adapter \_ \_ per OPM Get**</span><span class="sxs-lookup"><span data-stu-id="cd6d2-123">**OPM\_GET\_ADAPTER\_BUS\_TYPE**</span></span>](opm-get-adapter-bus-type.md)                                    | <span data-ttu-id="cd6d2-124">Restituisce il tipo di bus di I/O usato dall'output del video.</span><span class="sxs-lookup"><span data-stu-id="cd6d2-124">Returns the type of I/O bus used by the video output.</span></span>                                                                                                 |
| [<span data-ttu-id="cd6d2-125">**\_informazioni sul \_ codec di Get di OPM \_**</span><span class="sxs-lookup"><span data-stu-id="cd6d2-125">**OPM\_GET\_CODEC\_INFO**</span></span>](opm-get-codec-info.md)                                                 | <span data-ttu-id="cd6d2-126">Ottiene il valore di Merit di un codec hardware.</span><span class="sxs-lookup"><span data-stu-id="cd6d2-126">Gets the merit value of a hardware codec.</span></span>                                                                                                             |
| [<span data-ttu-id="cd6d2-127">**\_ \_ \_ \_ informazioni sul dispositivo HDCP connesso \_ ad OPM**</span><span class="sxs-lookup"><span data-stu-id="cd6d2-127">**OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION**</span></span>](opm-get-connected-hdcp-device-information.md) | <span data-ttu-id="cd6d2-128">Ottiene informazioni su un dispositivo High-Bandwidth Digital protezione del contenuto (HDCP) collegato all'output del video.</span><span class="sxs-lookup"><span data-stu-id="cd6d2-128">Gets information about a High-Bandwidth Digital Content Protection (HDCP) device attached to the video output.</span></span> <span data-ttu-id="cd6d2-129">Vengono restituite le seguenti informazioni:</span><span class="sxs-lookup"><span data-stu-id="cd6d2-129">The following information is returned:</span></span> |
| [<span data-ttu-id="cd6d2-130">**\_tipo di \_ connettore OPM Get \_**</span><span class="sxs-lookup"><span data-stu-id="cd6d2-130">**OPM\_GET\_CONNECTOR\_TYPE**</span></span>](opm-get-connector-type.md)                                         | <span data-ttu-id="cd6d2-131">Restituisce il tipo di connettore fisico dell'output del video.</span><span class="sxs-lookup"><span data-stu-id="cd6d2-131">Returns the physical connector type of the video output.</span></span>                                                                                              |
| [<span data-ttu-id="cd6d2-132">**OPM \_ ottenere \_ la \_ versione corrente di HDCP \_ SRM \_**</span><span class="sxs-lookup"><span data-stu-id="cd6d2-132">**OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION**</span></span>](opm-get-current-hdcp-srm-version.md)                   | <span data-ttu-id="cd6d2-133">Restituisce il numero di versione del messaggio di rinnovabilità del sistema (SRM) attualmente utilizzato dall'output del video.</span><span class="sxs-lookup"><span data-stu-id="cd6d2-133">Returns the version number of the system renewability message (SRM) currently used by the video output.</span></span>                                               |
| [<span data-ttu-id="cd6d2-134">**\_caratteristiche di Get \_ DVI \_ per OPM**</span><span class="sxs-lookup"><span data-stu-id="cd6d2-134">**OPM\_GET\_DVI\_CHARACTERISTICS**</span></span>](opm-get-dvi-characteristics.md)                               | <span data-ttu-id="cd6d2-135">Esegue una query se un connettore DVI (Digital Video Interface) supporta la versione DVI 1,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="cd6d2-135">Queries whether a digital video interface (DVI) connector supports DVI version 1.1 or later.</span></span>                                                          |
| [<span data-ttu-id="cd6d2-136">**\_ID di \_ output \_ Get di OPM**</span><span class="sxs-lookup"><span data-stu-id="cd6d2-136">**OPM\_GET\_OUTPUT\_ID**</span></span>](opm-get-output-id.md)                                                   | <span data-ttu-id="cd6d2-137">Restituisce l'identificatore univoco del monitoraggio associato a questo output del video.</span><span class="sxs-lookup"><span data-stu-id="cd6d2-137">Returns the unique identifier of the monitor associated with this video output.</span></span>                                                                       |
| [<span data-ttu-id="cd6d2-138">**OPM \_ ottenere \_ i \_ tipi di protezione supportati \_**</span><span class="sxs-lookup"><span data-stu-id="cd6d2-138">**OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES**</span></span>](opm-get-supported-protection-types.md)                | <span data-ttu-id="cd6d2-139">Restituisce l'elenco dei meccanismi di protezione supportati dal connettore.</span><span class="sxs-lookup"><span data-stu-id="cd6d2-139">Returns the list of protection mechanisms that are supported by the connector.</span></span>                                                                        |
| [<span data-ttu-id="cd6d2-140">**\_livello di \_ \_ protezione virtuale \_ di OPM Get**</span><span class="sxs-lookup"><span data-stu-id="cd6d2-140">**OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-virtual-protection-level.md)                    | <span data-ttu-id="cd6d2-141">Restituisce il livello di protezione virtuale per un meccanismo di protezione specificato.</span><span class="sxs-lookup"><span data-stu-id="cd6d2-141">Returns the virtual protection level for a specified protection mechanism.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="cd6d2-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cd6d2-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd6d2-143">Guida di riferimento alla programmazione di OPM</span><span class="sxs-lookup"><span data-stu-id="cd6d2-143">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="cd6d2-144">Gestione protezione output</span><span class="sxs-lookup"><span data-stu-id="cd6d2-144">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



