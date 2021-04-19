---
description: Le API DLP (Endpoint Data Loss Prevention) consentono alle applicazioni di inviare una notifica al sistema operativo prima e dopo determinate operazioni, ad esempio l'apertura o il salvataggio di un file.
title: Prevenzione della perdita di dati degli endpoint
ms.topic: article
ms.date: 03/18/2021
ms.openlocfilehash: 867e059e0accfc1208c96394c3065d69cf9f576c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495591"
---
# <a name="endpoint-data-loss-prevention"></a><span data-ttu-id="aebf4-103">Prevenzione della perdita di dati degli endpoint</span><span class="sxs-lookup"><span data-stu-id="aebf4-103">Endpoint data loss prevention</span></span>

<span data-ttu-id="aebf4-104">Windows 10 implementa meccanismi che consentono di evitare la perdita di dati per i file sensibili.</span><span class="sxs-lookup"><span data-stu-id="aebf4-104">Windows 10 implements mechanisms that help to prevent data loss for sensitive files.</span></span> <span data-ttu-id="aebf4-105">Le API DLP (Endpoint Data Loss Prevention) consentono alle applicazioni di inviare una notifica al sistema operativo prima e dopo determinate operazioni, ad esempio l'apertura o il salvataggio di un file.</span><span class="sxs-lookup"><span data-stu-id="aebf4-105">The endpoint data loss prevention (DLP) APIs allow applications to notify the OS before and after certain operations, such as opening or saving a file.</span></span> <span data-ttu-id="aebf4-106">Queste notifiche fungono da "hint" che consentono al sistema di ottimizzare le operazioni di perdita dei dati.</span><span class="sxs-lookup"><span data-stu-id="aebf4-106">These notifications serve as "hints" that allow the system to optimize data loss operations.</span></span>

## <a name="location-of-the-dlp-dll"></a><span data-ttu-id="aebf4-107">Percorso della DLL DLP</span><span class="sxs-lookup"><span data-stu-id="aebf4-107">Location of the DLP dll</span></span>

<span data-ttu-id="aebf4-108">Poiché la DLL DLP dell'endpoint non è in bundle con il Windows SDK, le applicazioni dovranno caricare manualmente la DLL in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="aebf4-108">Since the endpoint DLP dll isn't bundled with the Windows SDK, applications will need to load the dll manually at runtime.</span></span> <span data-ttu-id="aebf4-109">Il percorso della DLL viene archiviato nel Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="aebf4-109">The path to the dll location is stored in the registry.</span></span> <span data-ttu-id="aebf4-110">Nella tabella seguente sono elencate le chiavi e i valori del Registro di sistema in cui sono archiviate queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="aebf4-110">The following table lists the registry keys and values that store this information.</span></span> <span data-ttu-id="aebf4-111">Questi percorsi sono definiti come costanti nell'elenco di codice endpointdlp.h di esempio fornito di seguito per praticità per gli sviluppatori.</span><span class="sxs-lookup"><span data-stu-id="aebf4-111">These paths are defined as constants in the sample endpointdlp.h code listing provided below as a convenience for developers.</span></span>

| <span data-ttu-id="aebf4-112">Costante</span><span class="sxs-lookup"><span data-stu-id="aebf4-112">Constant</span></span> | <span data-ttu-id="aebf4-113">Valore</span><span class="sxs-lookup"><span data-stu-id="aebf4-113">Value</span></span> | <span data-ttu-id="aebf4-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aebf4-114">Description</span></span>   |
|----------|-------|---------------|
| <span data-ttu-id="aebf4-115">ENDPOINTDLP_DLL_NAME</span><span class="sxs-lookup"><span data-stu-id="aebf4-115">ENDPOINTDLP_DLL_NAME</span></span> | <span data-ttu-id="aebf4-116">"EndpointDlp.dll"</span><span class="sxs-lookup"><span data-stu-id="aebf4-116">"EndpointDlp.dll"</span></span> | <span data-ttu-id="aebf4-117">Nome della DLL DLP dell'endpoint che fornisce l'API</span><span class="sxs-lookup"><span data-stu-id="aebf4-117">The name of the Endpoint DLP DLL that provides the API</span></span> |
| <span data-ttu-id="aebf4-118">ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span><span class="sxs-lookup"><span data-stu-id="aebf4-118">ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span></span> | <span data-ttu-id="aebf4-119">"SOFTWARE \\ Microsoft \\ Windows Defender"</span><span class="sxs-lookup"><span data-stu-id="aebf4-119">"SOFTWARE\\Microsoft\\Windows Defender"</span></span> | <span data-ttu-id="aebf4-120">Windows Defender chiave del Registro di sistema in HKLM in cui sono archiviate alcune impostazioni DLP dell'endpoint</span><span class="sxs-lookup"><span data-stu-id="aebf4-120">Windows Defender registry key under HKLM where some Endpoint DLP settings are stored</span></span> |
| <span data-ttu-id="aebf4-121">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY</span><span class="sxs-lookup"><span data-stu-id="aebf4-121">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY</span></span> | <span data-ttu-id="aebf4-122">Valore di ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span><span class="sxs-lookup"><span data-stu-id="aebf4-122">Value of ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span></span> |  <span data-ttu-id="aebf4-123">Percorso del Registro di sistema nella chiave HKLM da cui è possibile EndpointDlp.dll percorso di installazione</span><span class="sxs-lookup"><span data-stu-id="aebf4-123">The registry path under HKLM key from which the EndpointDlp.dll install location can be obtained</span></span> |
| <span data-ttu-id="aebf4-124">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE</span><span class="sxs-lookup"><span data-stu-id="aebf4-124">ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE</span></span> | <span data-ttu-id="aebf4-125">"InstallLocation"</span><span class="sxs-lookup"><span data-stu-id="aebf4-125">"InstallLocation"</span></span> | <span data-ttu-id="aebf4-126">Valore del Registro di sistema in ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY in cui è archiviato il EndpointDlp.dll di installazione</span><span class="sxs-lookup"><span data-stu-id="aebf4-126">The registry value under ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY in which the EndpointDlp.dll install location is stored</span></span> |
| <span data-ttu-id="aebf4-127">ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX</span><span class="sxs-lookup"><span data-stu-id="aebf4-127">ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX</span></span> | <span data-ttu-id="aebf4-128">"x86"</span><span class="sxs-lookup"><span data-stu-id="aebf4-128">"x86"</span></span> | <span data-ttu-id="aebf4-129">Nelle piattaforme x64 concatenare questa directory per ottenere la versione x86 di EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="aebf4-129">On x64 platforms, concatenate this directory to obtain the x86 version of EndpointDlp.dll</span></span> |

## <a name="check-if-endpoint-dlp-is-enabled"></a><span data-ttu-id="aebf4-130">Controllare se la prevenzione della perdita dei dati dell'endpoint è abilitata</span><span class="sxs-lookup"><span data-stu-id="aebf4-130">Check if endpoint DLP is enabled</span></span>

<span data-ttu-id="aebf4-131">Per determinare se la prevenzione della perdita dei dati dell'endpoint è abilitata nel sistema, controllare il valore della chiave del Registro di sistema seguente.</span><span class="sxs-lookup"><span data-stu-id="aebf4-131">To determine if endpoint DLP is enabled on the system, check the following registry key value.</span></span> 

| <span data-ttu-id="aebf4-132">Costante</span><span class="sxs-lookup"><span data-stu-id="aebf4-132">Constant</span></span> | <span data-ttu-id="aebf4-133">Valore</span><span class="sxs-lookup"><span data-stu-id="aebf4-133">Value</span></span> | <span data-ttu-id="aebf4-134">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aebf4-134">Description</span></span>   |
|----------|-------|---------------|
| <span data-ttu-id="aebf4-135">ENDPOINTDLP_ENABLED_FLAG_REGKEY</span><span class="sxs-lookup"><span data-stu-id="aebf4-135">ENDPOINTDLP_ENABLED_FLAG_REGKEY</span></span> |  <span data-ttu-id="aebf4-136">\\"Funzionalità"</span><span class="sxs-lookup"><span data-stu-id="aebf4-136">"\\Features"</span></span> | <span data-ttu-id="aebf4-137">Percorso della chiave del flag abilitata per la prevenzione della perdita dei dati dell'endpoint in (HKLM) ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span><span class="sxs-lookup"><span data-stu-id="aebf4-137">The path to the Endpoint DLP enabled flag key under (HKLM) ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY</span></span> |
| <span data-ttu-id="aebf4-138">ENDPOINTDLP_ENABLED_FLAG_REGVALUE</span><span class="sxs-lookup"><span data-stu-id="aebf4-138">ENDPOINTDLP_ENABLED_FLAG_REGVALUE</span></span> | <span data-ttu-id="aebf4-139">"SenseDlpEnabled"</span><span class="sxs-lookup"><span data-stu-id="aebf4-139">"SenseDlpEnabled"</span></span> | <span data-ttu-id="aebf4-140">Valore del Registro di sistema in ENDPOINTDLP_ENABLED_FLAG_REGKEY contenente la chiave del Registro di sistema del flag DLP abilitato</span><span class="sxs-lookup"><span data-stu-id="aebf4-140">The registry value under ENDPOINTDLP_ENABLED_FLAG_REGKEY containing the DLP enabled flag registry key</span></span>

## <a name="endpoint-dlp-apis"></a><span data-ttu-id="aebf4-141">API DLP degli endpoint</span><span class="sxs-lookup"><span data-stu-id="aebf4-141">Endpoint DLP APIs</span></span>

<span data-ttu-id="aebf4-142">Le tabelle seguenti elencano le API fornite dalla DLL DLP dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="aebf4-142">The following tables list the APIs provided by the endpoint DLP dll.</span></span>

### <a name="initialization-and-versioning"></a><span data-ttu-id="aebf4-143">Inizializzazione e controllo delle versioni</span><span class="sxs-lookup"><span data-stu-id="aebf4-143">Initialization and versioning</span></span>

| <span data-ttu-id="aebf4-144">API</span><span class="sxs-lookup"><span data-stu-id="aebf4-144">API</span></span> | <span data-ttu-id="aebf4-145">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aebf4-145">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="aebf4-146">DlpInitializeEnforcementMode</span><span class="sxs-lookup"><span data-stu-id="aebf4-146">DlpInitializeEnforcementMode</span></span>](endpointdlp-dlpinitializeenforcementmode.md)                       | <span data-ttu-id="aebf4-147">Notifica al sistema le modalità di imposizione desiderate per un set di operazioni dlp (Data Loss Prevention) dell'endpoint.</span><span class="sxs-lookup"><span data-stu-id="aebf4-147">Notifies the system of the desired enforcement modes for a set of endpoint Data Loss Prevention (DLP) operations.</span></span>                                  |
| [<span data-ttu-id="aebf4-148">DlpGetEnforcementApiVersion</span><span class="sxs-lookup"><span data-stu-id="aebf4-148">DlpGetEnforcementApiVersion</span></span>](endpointdlp-dlpgetenforcementapiversion.md)                       | <span data-ttu-id="aebf4-149">Recupera la versione dell'API prevenzione della perdita dei dati (DLP) dell'endpoint nel dispositivo corrente.</span><span class="sxs-lookup"><span data-stu-id="aebf4-149">Retrieves the version of the endpoint Data Loss Prevention (DLP) API on the current device.</span></span>                                  |


### <a name="document-operations"></a><span data-ttu-id="aebf4-150">Operazioni relative ai documenti</span><span class="sxs-lookup"><span data-stu-id="aebf4-150">Document operations</span></span>

| <span data-ttu-id="aebf4-151">API</span><span class="sxs-lookup"><span data-stu-id="aebf4-151">API</span></span> | <span data-ttu-id="aebf4-152">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aebf4-152">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="aebf4-153">DlpNotifyPreOpenDocument</span><span class="sxs-lookup"><span data-stu-id="aebf4-153">DlpNotifyPreOpenDocument</span></span>](endpointdlp-dlpnotifypreopendocument.md) | <span data-ttu-id="aebf4-154">Fornisce al sistema informazioni su un documento prima dell'avvio dell'operazione di apertura.</span><span class="sxs-lookup"><span data-stu-id="aebf4-154">Provides the system with information about a document before the open operation is initiated.</span></span> |
| [<span data-ttu-id="aebf4-155">DlpNotifyPostOpenDocument</span><span class="sxs-lookup"><span data-stu-id="aebf4-155">DlpNotifyPostOpenDocument</span></span>](endpointdlp-dlpnotifypostopendocument.md) | <span data-ttu-id="aebf4-156">Fornisce al sistema informazioni su un documento dopo il completamento dell'operazione di apertura.</span><span class="sxs-lookup"><span data-stu-id="aebf4-156">Provides the system with information about a document after the open operation is completed.</span></span>  |
| [<span data-ttu-id="aebf4-157">DlpNotifyCloseDocument</span><span class="sxs-lookup"><span data-stu-id="aebf4-157">DlpNotifyCloseDocument</span></span>](endpointdlp-dlpnotifyclosedocument.md)                       | <span data-ttu-id="aebf4-158">Fornisce al sistema informazioni su un documento prima che venga avviata l'operazione di chiusura del documento.</span><span class="sxs-lookup"><span data-stu-id="aebf4-158">Provides the system with information about a document before the document close operation is initiated.</span></span>                                  |
| [<span data-ttu-id="aebf4-159">DlpNotifyPreOpenDocumentFile</span><span class="sxs-lookup"><span data-stu-id="aebf4-159">DlpNotifyPreOpenDocumentFile</span></span>](endpointdlp-dlpnotifypreopendocumentfile.md)                         | <span data-ttu-id="aebf4-160">Fornisce al sistema informazioni su un documento prima dell'avvio dell'operazione di apertura.</span><span class="sxs-lookup"><span data-stu-id="aebf4-160">Provides the system with information about a document before the open operation is initiated.</span></span>  |
| [<span data-ttu-id="aebf4-161">DlpNotifyPostOpenDocumentFile</span><span class="sxs-lookup"><span data-stu-id="aebf4-161">DlpNotifyPostOpenDocumentFile</span></span>](endpointdlp-dlpnotifypostopendocumentfile.md)                       | <span data-ttu-id="aebf4-162">Fornisce al sistema informazioni su un documento dopo il completamento dell'operazione di apertura.</span><span class="sxs-lookup"><span data-stu-id="aebf4-162">Provides the system with information about a document after the open operation is completed.</span></span>                                  |
| [<span data-ttu-id="aebf4-163">DlpNotifyCloseDocumentFile</span><span class="sxs-lookup"><span data-stu-id="aebf4-163">DlpNotifyCloseDocumentFile</span></span>](endpointdlp-dlpnotifyclosedocumentfile.md)                       | <span data-ttu-id="aebf4-164">Fornisce al sistema informazioni su un documento prima che venga avviata l'operazione di chiusura del documento.</span><span class="sxs-lookup"><span data-stu-id="aebf4-164">Provides the system with information about a document before the document close operation is initiated.</span></span>                                  |

### <a name="save-as-operations"></a><span data-ttu-id="aebf4-165">Salvare come operazioni</span><span class="sxs-lookup"><span data-stu-id="aebf4-165">Save as operations</span></span>
| <span data-ttu-id="aebf4-166">API</span><span class="sxs-lookup"><span data-stu-id="aebf4-166">API</span></span> | <span data-ttu-id="aebf4-167">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aebf4-167">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="aebf4-168">DlpNotifyPreSaveAsDocument</span><span class="sxs-lookup"><span data-stu-id="aebf4-168">DlpNotifyPreSaveAsDocument</span></span>](endpointdlp-dlpnotifypresaveasdocument.md)                       | <span data-ttu-id="aebf4-169">Fornisce al sistema informazioni su un documento prima che venga avviata un'operazione di salvataggio con nome.</span><span class="sxs-lookup"><span data-stu-id="aebf4-169">Provides the system with information about a document before a save as operation is initiated.</span></span>                                  |
| [<span data-ttu-id="aebf4-170">DlpNotifyPostSaveAsDocument</span><span class="sxs-lookup"><span data-stu-id="aebf4-170">DlpNotifyPostSaveAsDocument</span></span>](endpointdlp-dlpnotifypostsaveasdocument.md)                       | <span data-ttu-id="aebf4-171">Fornisce al sistema informazioni su un documento dopo il completamento dell'operazione di salvataggio con nome.</span><span class="sxs-lookup"><span data-stu-id="aebf4-171">Provides the system with information about a document after the save as operation is completed.</span></span>                                  |


### <a name="drag-and-drop-operations"></a><span data-ttu-id="aebf4-172">Operazioni di trascinamento della selezione</span><span class="sxs-lookup"><span data-stu-id="aebf4-172">Drag and drop operations</span></span>

| <span data-ttu-id="aebf4-173">API</span><span class="sxs-lookup"><span data-stu-id="aebf4-173">API</span></span> | <span data-ttu-id="aebf4-174">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aebf4-174">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="aebf4-175">DlpNotifyEnterDropTarget</span><span class="sxs-lookup"><span data-stu-id="aebf4-175">DlpNotifyEnterDropTarget</span></span>](endpointdlp-dlpnotifyenterdroptarget.md)                       | <span data-ttu-id="aebf4-176">Fornisce al sistema informazioni su un documento quando viene immessa una destinazione di rilascio.</span><span class="sxs-lookup"><span data-stu-id="aebf4-176">Provides the system with information about a document when a drop target is entered.</span></span>                                  |
| [<span data-ttu-id="aebf4-177">DlpNotifyLeaveDropTarget</span><span class="sxs-lookup"><span data-stu-id="aebf4-177">DlpNotifyLeaveDropTarget</span></span>](endpointdlp-dlpnotifyleavedroptarget.md)                       | <span data-ttu-id="aebf4-178">Fornisce al sistema informazioni su un documento quando un obiettivo di rilascio viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="aebf4-178">Provides the system with information about a document when a drop target is exited.</span></span>                                  |
| [<span data-ttu-id="aebf4-179">DlpNotifyPreDragDrop</span><span class="sxs-lookup"><span data-stu-id="aebf4-179">DlpNotifyPreDragDrop</span></span>](endpointdlp-dlpnotifypredragdrop.md)                         | <span data-ttu-id="aebf4-180">Fornisce al sistema informazioni su un documento prima dell'avvio di un'operazione di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="aebf4-180">Provides the system with information about a document before a drag drop operation is initiated.</span></span>  |
| [<span data-ttu-id="aebf4-181">DlpNotifyPostDragDrop</span><span class="sxs-lookup"><span data-stu-id="aebf4-181">DlpNotifyPostDragDrop</span></span>](endpointdlp-dlpnotifypostdragdrop.md)                         | <span data-ttu-id="aebf4-182">Fornisce al sistema informazioni su un documento dopo il completamento di un'operazione di trascinamento della selezione.</span><span class="sxs-lookup"><span data-stu-id="aebf4-182">Provides the system with information about a document after a drag drop operation is completed.</span></span>  |


### <a name="clipboard-operations"></a><span data-ttu-id="aebf4-183">operazioni relative agli Appunti</span><span class="sxs-lookup"><span data-stu-id="aebf4-183">Clipboard operations</span></span>

| <span data-ttu-id="aebf4-184">API</span><span class="sxs-lookup"><span data-stu-id="aebf4-184">API</span></span> | <span data-ttu-id="aebf4-185">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aebf4-185">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="aebf4-186">DlpNotifyPreCopyToClipboard</span><span class="sxs-lookup"><span data-stu-id="aebf4-186">DlpNotifyPreCopyToClipboard</span></span>](endpointdlp-dlpnotifyprecopytoclipboard.md)                         | <span data-ttu-id="aebf4-187">Fornisce al sistema informazioni su un documento prima dell'avvio di un'operazione di copia negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="aebf4-187">Provides the system with information about a document before a copy to clipboard operation is initiated.</span></span>  |
| [<span data-ttu-id="aebf4-188">DlpNotifyPostCopyToClipboard</span><span class="sxs-lookup"><span data-stu-id="aebf4-188">DlpNotifyPostCopyToClipboard</span></span>](endpointdlp-dlpnotifypostcopytoclipboard.md)                         | <span data-ttu-id="aebf4-189">Fornisce al sistema informazioni su un documento dopo il completamento di un'operazione di copia negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="aebf4-189">Provides the system with information about a document after a copy to clipboard operation is completed.</span></span>  |
| [<span data-ttu-id="aebf4-190">DlpNotifyPrePasteFromClipboard</span><span class="sxs-lookup"><span data-stu-id="aebf4-190">DlpNotifyPrePasteFromClipboard</span></span>](endpointdlp-dlpnotifyprepastefromclipboard.md)                         | <span data-ttu-id="aebf4-191">Fornisce al sistema informazioni su un documento prima che venga avviata un'operazione Incolla dagli Appunti.</span><span class="sxs-lookup"><span data-stu-id="aebf4-191">Provides the system with information about a document before a paste from clipboard operation is initiated.</span></span>  |
| [<span data-ttu-id="aebf4-192">DlpNotifyPostPasteFromClipboard</span><span class="sxs-lookup"><span data-stu-id="aebf4-192">DlpNotifyPostPasteFromClipboard</span></span>](endpointdlp-dlpnotifypostpastefromclipboard.md)                       | <span data-ttu-id="aebf4-193">Fornisce al sistema informazioni su un documento dopo il completamento di un'operazione Incolla dagli Appunti.</span><span class="sxs-lookup"><span data-stu-id="aebf4-193">Provides the system with information about a document after a paste from clipboard operation has completed.</span></span>                                  |
| [<span data-ttu-id="aebf4-194">DlpNotifyPostStashClipboard</span><span class="sxs-lookup"><span data-stu-id="aebf4-194">DlpNotifyPostStashClipboard</span></span>](endpointdlp-dlpnotifypoststashclipboard.md)                       | <span data-ttu-id="aebf4-195">Fornisce al sistema informazioni sullo stato dopo il completamento di un'operazione di stash clipboard.</span><span class="sxs-lookup"><span data-stu-id="aebf4-195">Provides the system with status information after a stash clipboard operation is completed.</span></span>                                  |
| [<span data-ttu-id="aebf4-196">DlpNotifyPreStashClipboard</span><span class="sxs-lookup"><span data-stu-id="aebf4-196">DlpNotifyPreStashClipboard</span></span>](endpointdlp-dlpnotifyprestashclipboard.md)                       | <span data-ttu-id="aebf4-197">Notifica al sistema prima che venga avviata un'operazione di stash clipboard.</span><span class="sxs-lookup"><span data-stu-id="aebf4-197">Notifies the system before a stash clipboard operation is initiated.</span></span>                                  |
| [<span data-ttu-id="aebf4-198">DlpMustPasteFromSystemClipboard</span><span class="sxs-lookup"><span data-stu-id="aebf4-198">DlpMustPasteFromSystemClipboard</span></span>](endpointdlp-dlpmustpastefromsystemclipboard.md)                       | <span data-ttu-id="aebf4-199">Determina se l'app deve eseguire il pull dei dati dagli Appunti di sistema anziché dalla cache interna.</span><span class="sxs-lookup"><span data-stu-id="aebf4-199">Determines whether the app must pull the data from the system clipboard rather than taking it from its internal cache.</span></span>                                  |

### <a name="print-operations"></a><span data-ttu-id="aebf4-200">Operazioni di stampa</span><span class="sxs-lookup"><span data-stu-id="aebf4-200">Print operations</span></span>

| <span data-ttu-id="aebf4-201">API</span><span class="sxs-lookup"><span data-stu-id="aebf4-201">API</span></span> | <span data-ttu-id="aebf4-202">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aebf4-202">Description</span></span> |
|-----|-------------|
| [<span data-ttu-id="aebf4-203">DlpNotifyPrePrint</span><span class="sxs-lookup"><span data-stu-id="aebf4-203">DlpNotifyPrePrint</span></span>](endpointdlp-dlpnotifypreprint.md)                         | <span data-ttu-id="aebf4-204">Fornisce al sistema informazioni su un documento prima che venga avviata un'operazione di stampa.</span><span class="sxs-lookup"><span data-stu-id="aebf4-204">Provides the system with information about a document before a print operation is initiated.</span></span>  |
| [<span data-ttu-id="aebf4-205">DlpNotifyPostStartPrint</span><span class="sxs-lookup"><span data-stu-id="aebf4-205">DlpNotifyPostStartPrint</span></span>](endpointdlp-dlpnotifypoststartprint.md)                       | <span data-ttu-id="aebf4-206">Fornisce al sistema informazioni su un documento dopo l'avvio di un'operazione di stampa.</span><span class="sxs-lookup"><span data-stu-id="aebf4-206">Provides the system with information about a document after an print operation has started.</span></span>                                  |
| [<span data-ttu-id="aebf4-207">DlpNotifyPostPrint</span><span class="sxs-lookup"><span data-stu-id="aebf4-207">DlpNotifyPostPrint</span></span>](endpointdlp-dlpnotifypostprint.md)                       | <span data-ttu-id="aebf4-208">Fornisce al sistema informazioni su un documento al termine di un'operazione di stampa.</span><span class="sxs-lookup"><span data-stu-id="aebf4-208">Provides the system with information about a document after a print operation has completed.</span></span>                                  |

## <a name="endpoint-dlp-example-header"></a><span data-ttu-id="aebf4-209">Intestazione di esempio DLP dell'endpoint</span><span class="sxs-lookup"><span data-stu-id="aebf4-209">Endpoint DLP example header</span></span>

<span data-ttu-id="aebf4-210">Poiché l'intestazione DLP dell'endpoint non è inclusa nel Windows SDK, è necessario creare manualmente il file di intestazione per ottenere le firme API da usare nell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="aebf4-210">Because the endpoint DLP header is not included in the Windows SDK, you must create the header file yourself to get API signatures to use in your implementation.</span></span> <span data-ttu-id="aebf4-211">Per praticità, viene fornito codice di esempio che è possibile copiare e incollare nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="aebf4-211">For your convenience we're providing example code that you can copy and paste into your application.</span></span> <span data-ttu-id="aebf4-212">Oltre alle dichiarazioni di funzione, questo elenco di codice definisce anche costanti utili come le informazioni sul controllo delle versioni e i percorsi delle chiavi del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="aebf4-212">In addition to function declarations, this code listing also defines useful constants such as versioning information and registry key paths.</span></span>

```cpp
//
// EndpointDlp DLL name containing the Endpoint DLP API
//

#define ENDPOINTDLP_DLL_NAME L"EndpointDlp.dll"

//
// Windows Defender registry key under HKLM where some Endpoint DLP settings are stored
//

#define ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"SOFTWARE\\Microsoft\\Windows Defender"

//
// EndpointDlp.dll install location can be obtained from the registry under the following HKLM key
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY

//
// EndpointDlp.dll install location is stored under ENDPOINTDLP_DLL_INSTALL_LOCATION_REGKEY in the following registry value
//

#define ENDPOINTDLP_DLL_INSTALL_LOCATION_REGVALUE L"InstallLocation"

//
// On x64 platforms, concatanate the following directory to obtain the x86 version of EndpointDlp.dll
//

#define ENDPOINTDLP_DLL_WOW64_X86_INSTALL_LOCATION_SUFFIX L"x86"

//
// Endpoint DLP enabled flag can be found under the following HKLM key
//

#define ENDPOINTDLP_ENABLED_FLAG_REGKEY ENDPOINTDLP_WINDOWS_DEFENDER_REGKEY L"\\Features"

//
// Endpoint DLP enabled flag can be found under ENDPOINTDLP_ENABLED_REGKEY in the following registry value
//

#define ENDPOINTDLP_ENABLED_FLAG_REGVALUE L"SenseDlpEnabled"


#define DLP_DOCUMENT_INFO_V_1 0x1     

#define DLP_DOCUMENT_INFO_V_LATEST DLP_DOCUMENT_INFO_V_1


//
//  Enlightened app enforcement capablities.
//

typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, // No enforcement, DLP enforces operation.
    DlpAppEnforceLevelNotify,   // App send notifications on operation, DLP enforces operation.
    DlpAppEnforceLevelPrevent,  // Currently not supported (App allows or blocks operation, DLP enforces warning, eventing and UI). 
    DlpAppEnforceLevelFull,     // Currently not supported (App handles all enforcement (blocks operation, enforces warning, UI), DLP will only handle auditing.)
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;

typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
    
//
//  The stucture describes the enforcement level for each operation.
//
    
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;


/*
Function description:
     The application calls this functio to declares the enforcement level for each operation.

Parameters:
    _In_ DWORD Count - Number of operations. 
    _In_reads_opt_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL* OperationEnforcement - Array indicating operations
    supported by the application and enforcement level:
        DlpAppEnforceLevelNone - No enforcement, DLP enforces operation.
        DlpAppEnforceLevelNotify -  App send notifications on operation, DLP enforces operation.

Return:
    S_OK - Function completed successfully.
    E_INVALIDARG - Invalid parameters passed to function.
    E_OUTOFMEMORY - Memory allocation failed.
    E_XXX - Varius error codes.
*/       
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);


/*
Function description:
    Returns the version of the enforcement API.
    MajorVersion indicates a new interfaces/API.
    MinorVersion indicates changes to existing interfaces/API-s.
   
Parameters:
    None.

Return:
    S_OK - Function completed successfully
    E_XXX - Varius error codes.
*/
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);


typedef struct _DLP_DOCUMENT_INFO {

    //
    //  Information version. Always set it to DLP_DOCUMENT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Original path of the document.
    //  
    
    LPCWSTR PersistentFileName;

    //
    //  Path to the real backing file.
    //
    
    LPCWSTR LocalFileName;

}DLP_DOCUMENT_INFO, *PDLP_DOCUMENT_INFO;

//
//  Post operation status information.
//
    
#define DLP_POSTOP_STATUS_V_1 0x1     
        
#define DLP_POSTOP_STATUS_V_LATEST DLP_POSTOP_STATUS_V_1;
    
       
typedef struct _DLP_POSTOP_STATUS {

    //
    //  Information version. Always set it to DLP_POSTOP_STATUS_V_LATEST
    //
    
    DWORD Version;

    //
    //  Set to TRUE if app's operation succeeded, FALSE otherwise. 
    //
    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS;    


#define DLP_PRINT_INFO_V_1 0x1     
    
#define DLP_PRINT_INFO_V_LATEST DLP_PRINT_INFO_V_1;

typedef struct _DLP_PRINT_INFO {

    //
    //  Information version. Always set it to DLP_PRINT_INFO_V_LATEST
    //
    
    DWORD Version;

    //
    //  Destination printer.
    //
    
    LPCWSTR PrinterName;

    //
    //  Print job name.
    //
    
    LPCWSTR JobName;

    //
    //  Output file, if printing to file.
    //

    LPCWSTR OutputFileName;
    
}DLP_PRINT_INFO, *PDLP_PRINT_INFO;

    
void WINAPI DlpNotifyPreOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostOpenDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyCloseDocumentFile(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);

void WINAPI DlpNotifyPreSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination);
void WINAPI DlpNotifyPostSaveAsDocument(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ LPCWSTR Destination, _In_ const PDLP_POSTOP_STATUS OpStatus); 

void WINAPI DlpNotifyPrePrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostStartPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo);
void WINAPI DlpNotifyPostPrint(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_PRINT_INFO PrintInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostCopyToClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPrePasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostPasteFromClipboard(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreStashClipboard();
void WINAPI DlpNotifyPostStashClipboard(_In_ const PDLP_POSTOP_STATUS OpStatus);

void WINAPI DlpNotifyPreDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyPostDragDrop(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus);
    
void WINAPI DlpNotifyEnterDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo);
void WINAPI DlpNotifyLeaveDropTarget(_In_ const PDLP_DOCUMENT_INFO DocumentInfo, _In_ const PDLP_POSTOP_STATUS OpStatus); 


```


