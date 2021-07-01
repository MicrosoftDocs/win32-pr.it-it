---
description: Richieste di stato OPM
ms.assetid: 428d08c6-e9f0-49fb-9ef9-d0f95416669d
title: Richieste di stato OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbf7338fe1309feb49fd191e3f4a1a22f3639b4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120176"
---
# <a name="opm-status-requests"></a><span data-ttu-id="32320-103">Richieste di stato OPM</span><span class="sxs-lookup"><span data-stu-id="32320-103">OPM Status Requests</span></span>

<span data-ttu-id="32320-104">Questa sezione elenca le richieste di stato disponibili per [Output Protection Manager](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="32320-104">This section lists the available status requests for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span> <span data-ttu-id="32320-105">Per inviare una richiesta di stato OPM, chiamare [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation).</span><span class="sxs-lookup"><span data-stu-id="32320-105">To send an OPM status request, call [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation).</span></span> <span data-ttu-id="32320-106">Per ogni richiesta sono elencate le informazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="32320-106">For each request, the following information is listed.</span></span>



| <span data-ttu-id="32320-107">Valore</span><span class="sxs-lookup"><span data-stu-id="32320-107">Value</span></span>             | <span data-ttu-id="32320-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32320-108">Description</span></span>                                                                                                                                                           |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32320-109">GUID della richiesta</span><span class="sxs-lookup"><span data-stu-id="32320-109">Request GUID</span></span> | <span data-ttu-id="32320-110">Identifica la richiesta.</span><span class="sxs-lookup"><span data-stu-id="32320-110">Identifies the request.</span></span> <span data-ttu-id="32320-111">Impostare il **membro guidSetting** della struttura [**OPM \_ GET INFO \_ \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) su questo valore.</span><span class="sxs-lookup"><span data-stu-id="32320-111">Set the **guidSetting** member of the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="32320-112">Dati di input</span><span class="sxs-lookup"><span data-stu-id="32320-112">Input data</span></span>   | <span data-ttu-id="32320-113">Specifica come interpretare la matrice **abParameters** nella [**struttura OPM \_ GET INFO \_ \_ PARAMETERS.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters)</span><span class="sxs-lookup"><span data-stu-id="32320-113">Specifies how to interpret the **abParameters** array in the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure.</span></span>                      |
| <span data-ttu-id="32320-114">Dati di output</span><span class="sxs-lookup"><span data-stu-id="32320-114">Output data</span></span>  | <span data-ttu-id="32320-115">Specifica come interpretare la matrice **abRequestedInformation** nella [**struttura OPM \_ REQUESTED \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information)</span><span class="sxs-lookup"><span data-stu-id="32320-115">Specifies how to interpret the **abRequestedInformation** array in the [**OPM\_REQUESTED\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) structure.</span></span>         |



 

<span data-ttu-id="32320-116">Vengono definite le richieste di stato seguenti:</span><span class="sxs-lookup"><span data-stu-id="32320-116">The following status requests are defined:</span></span>



| <span data-ttu-id="32320-117">Richiesta di stato</span><span class="sxs-lookup"><span data-stu-id="32320-117">Status request</span></span>                                                                                      | <span data-ttu-id="32320-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32320-118">Description</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="32320-119">**OPM \_ GET \_ ACP E \_ \_ CGMSA \_ SIGNALING**</span><span class="sxs-lookup"><span data-stu-id="32320-119">**OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-get-acp-and-cgmsa-signaling.md)                     | <span data-ttu-id="32320-120">Restituisce le informazioni seguenti su un output video:</span><span class="sxs-lookup"><span data-stu-id="32320-120">Returns the following information about a video output:</span></span>                                                                                               |
| [<span data-ttu-id="32320-121">**OPM \_ GET \_ ACTUAL \_ OUTPUT \_ FORMAT**</span><span class="sxs-lookup"><span data-stu-id="32320-121">**OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT**</span></span>](opm-get-actual-output-format.md)                            | <span data-ttu-id="32320-122">Restituisce una descrizione del segnale video trasmesso tramite il connettore.</span><span class="sxs-lookup"><span data-stu-id="32320-122">Returns a description of the video signal that is being transmitted over the connector.</span></span>                                                               |
| [<span data-ttu-id="32320-123">**OPM \_ OTTIENE IL LIVELLO DI PROTEZIONE \_ \_ \_ EFFETTIVO**</span><span class="sxs-lookup"><span data-stu-id="32320-123">**OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-actual-protection-level.md)                      | <span data-ttu-id="32320-124">Restituisce il livello di protezione globale per un meccanismo di protezione specificato.</span><span class="sxs-lookup"><span data-stu-id="32320-124">Returns the global protection level for a specified protection mechanism.</span></span>                                                                             |
| [<span data-ttu-id="32320-125">**TIPO DI \_ \_ BUS \_ DELL'ADAPTER \_ OPM GET**</span><span class="sxs-lookup"><span data-stu-id="32320-125">**OPM\_GET\_ADAPTER\_BUS\_TYPE**</span></span>](opm-get-adapter-bus-type.md)                                    | <span data-ttu-id="32320-126">Restituisce il tipo di bus di I/O utilizzato dall'output video.</span><span class="sxs-lookup"><span data-stu-id="32320-126">Returns the type of I/O bus used by the video output.</span></span>                                                                                                 |
| [<span data-ttu-id="32320-127">**OPM \_ GET \_ CODEC \_ INFO**</span><span class="sxs-lookup"><span data-stu-id="32320-127">**OPM\_GET\_CODEC\_INFO**</span></span>](opm-get-codec-info.md)                                                 | <span data-ttu-id="32320-128">Ottiene il valore di merito di un codec hardware.</span><span class="sxs-lookup"><span data-stu-id="32320-128">Gets the merit value of a hardware codec.</span></span>                                                                                                             |
| [<span data-ttu-id="32320-129">**OPM \_ GET \_ CONNECTED \_ HDCP \_ DEVICE \_ INFORMATION**</span><span class="sxs-lookup"><span data-stu-id="32320-129">**OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION**</span></span>](opm-get-connected-hdcp-device-information.md) | <span data-ttu-id="32320-130">Ottiene informazioni su High-Bandwidth dispositivo HDCP (Digital protezione del contenuto) collegato all'output video.</span><span class="sxs-lookup"><span data-stu-id="32320-130">Gets information about a High-Bandwidth Digital Content Protection (HDCP) device attached to the video output.</span></span> <span data-ttu-id="32320-131">Vengono restituite le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="32320-131">The following information is returned:</span></span> |
| [<span data-ttu-id="32320-132">**TIPO DI CONNETTORE OPM \_ GET \_ \_**</span><span class="sxs-lookup"><span data-stu-id="32320-132">**OPM\_GET\_CONNECTOR\_TYPE**</span></span>](opm-get-connector-type.md)                                         | <span data-ttu-id="32320-133">Restituisce il tipo di connettore fisico dell'output video.</span><span class="sxs-lookup"><span data-stu-id="32320-133">Returns the physical connector type of the video output.</span></span>                                                                                              |
| [<span data-ttu-id="32320-134">**OPM \_ GET \_ CURRENT \_ HDCP \_ SRM \_ VERSION**</span><span class="sxs-lookup"><span data-stu-id="32320-134">**OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION**</span></span>](opm-get-current-hdcp-srm-version.md)                   | <span data-ttu-id="32320-135">Restituisce il numero di versione del messaggio di rinnovo del sistema (SRM) attualmente usato dall'output video.</span><span class="sxs-lookup"><span data-stu-id="32320-135">Returns the version number of the system renewability message (SRM) currently used by the video output.</span></span>                                               |
| [<span data-ttu-id="32320-136">**OPM \_ GET \_ DVI \_ CHARACTERISTICS**</span><span class="sxs-lookup"><span data-stu-id="32320-136">**OPM\_GET\_DVI\_CHARACTERISTICS**</span></span>](opm-get-dvi-characteristics.md)                               | <span data-ttu-id="32320-137">Verifica se un connettore DVI (Digital Video Interface) supporta DVI versione 1.1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="32320-137">Queries whether a digital video interface (DVI) connector supports DVI version 1.1 or later.</span></span>                                                          |
| [<span data-ttu-id="32320-138">**OPM \_ GET \_ OUTPUT \_ ID**</span><span class="sxs-lookup"><span data-stu-id="32320-138">**OPM\_GET\_OUTPUT\_ID**</span></span>](opm-get-output-id.md)                                                   | <span data-ttu-id="32320-139">Restituisce l'identificatore univoco del monitoraggio associato a questo output video.</span><span class="sxs-lookup"><span data-stu-id="32320-139">Returns the unique identifier of the monitor associated with this video output.</span></span>                                                                       |
| [<span data-ttu-id="32320-140">**OPM \_ OTTIENE I TIPI DI PROTEZIONE \_ \_ \_ SUPPORTATI**</span><span class="sxs-lookup"><span data-stu-id="32320-140">**OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES**</span></span>](opm-get-supported-protection-types.md)                | <span data-ttu-id="32320-141">Restituisce l'elenco dei meccanismi di protezione supportati dal connettore.</span><span class="sxs-lookup"><span data-stu-id="32320-141">Returns the list of protection mechanisms that are supported by the connector.</span></span>                                                                        |
| [<span data-ttu-id="32320-142">**OPM \_ GET \_ VIRTUAL \_ PROTECTION \_ LEVEL**</span><span class="sxs-lookup"><span data-stu-id="32320-142">**OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-virtual-protection-level.md)                    | <span data-ttu-id="32320-143">Restituisce il livello di protezione virtuale per un meccanismo di protezione specificato.</span><span class="sxs-lookup"><span data-stu-id="32320-143">Returns the virtual protection level for a specified protection mechanism.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="32320-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="32320-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32320-145">Informazioni di riferimento sulla programmazione OPM</span><span class="sxs-lookup"><span data-stu-id="32320-145">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="32320-146">Output Protection Manager</span><span class="sxs-lookup"><span data-stu-id="32320-146">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



