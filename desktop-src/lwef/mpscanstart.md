---
title: Funzione MpScanStart (MpClient. h)
description: Avvia un'operazione di analisi.
ms.assetid: 3AF147C8-A41F-4193-AE28-72C1FBD18BA2
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpScanStart
topic_type:
- apiref
api_name:
- MpScanStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d343787edc85a18dc7471d19165999a7252d18a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964487"
---
# <a name="mpscanstart-function"></a><span data-ttu-id="4386e-104">MpScanStart (funzione)</span><span class="sxs-lookup"><span data-stu-id="4386e-104">MpScanStart function</span></span>

<span data-ttu-id="4386e-105">Avvia un'operazione di analisi.</span><span class="sxs-lookup"><span data-stu-id="4386e-105">Starts a scanning operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4386e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4386e-106">Syntax</span></span>


```C++
HRESULT WINAPI MpScanStart(
  _In_     MPHANDLE          hMpHandle,
  _In_     MPSCAN_TYPE       ScanType,
  _In_     DWORD             dwScanOptions,
  _In_opt_ PMPSCAN_RESOURCES pScanResources,
  _In_opt_ PMPCALLBACK_INFO  pCallbackInfo,
  _Out_    PMPHANDLE         phScanHandle
);
```



## <a name="parameters"></a><span data-ttu-id="4386e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4386e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4386e-108">*hMpHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4386e-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4386e-109">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="4386e-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="4386e-110">Handle per l'interfaccia di malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="4386e-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="4386e-111">Questo handle viene restituito dalla funzione [**MpManagerOpen**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="4386e-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="4386e-112">*ScanType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4386e-112">*ScanType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4386e-113">Tipo: **[ **MPSCAN \_**](mpscan-type.md)**</span><span class="sxs-lookup"><span data-stu-id="4386e-113">Type: **[**MPSCAN\_TYPE**](mpscan-type.md)**</span></span>

<span data-ttu-id="4386e-114">Specifica il tipo di analisi.</span><span class="sxs-lookup"><span data-stu-id="4386e-114">Specifies the type of scan.</span></span> <span data-ttu-id="4386e-115">Questo parametro deve essere uno dei membri del [**\_ tipo MPSCAN**](mpscan-type.md) enueration.</span><span class="sxs-lookup"><span data-stu-id="4386e-115">This parameter must be one of the members of the [**MPSCAN\_TYPE**](mpscan-type.md) enueration.</span></span>

</dd> <dt>

<span data-ttu-id="4386e-116">*dwScanOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4386e-116">*dwScanOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4386e-117">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="4386e-117">Type: **DWORD**</span></span>

<span data-ttu-id="4386e-118">Specifica varie opzioni per l'operazione di analisi.</span><span class="sxs-lookup"><span data-stu-id="4386e-118">Specifies various options for scanning operation.</span></span>



| <span data-ttu-id="4386e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="4386e-119">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="4386e-120">Significato</span><span class="sxs-lookup"><span data-stu-id="4386e-120">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPSCAN_OPTION_NONE"></span><span id="mpscan_option_none"></span><dl> <span data-ttu-id="4386e-121"><dt>**\_opzione MPSCAN \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="4386e-121"><dt>**MPSCAN\_OPTION\_NONE**</dt></span></span> </dl>                               | <span data-ttu-id="4386e-122">Non è richiesta alcuna opzione specifica.</span><span class="sxs-lookup"><span data-stu-id="4386e-122">No specific option is requested.</span></span><br/>                                                                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_ASYNC"></span><span id="mpscan_option_async"></span><dl> <span data-ttu-id="4386e-123"><dt>**\_opzione MPSCAN \_ Async**</dt></span><span class="sxs-lookup"><span data-stu-id="4386e-123"><dt>**MPSCAN\_OPTION\_ASYNC**</dt></span></span> </dl>                            | <span data-ttu-id="4386e-124">L'operazione di analisi deve essere asincrona, in cui **MpScanStart** viene restituito immediatamente dopo la corretta inizializzazione dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="4386e-124">The scan operation is to be asynchronous, where **MpScanStart** returns immediately after the successful initiation of scanning.</span></span> <span data-ttu-id="4386e-125">Per impostazione predefinita, l'operazione di analisi è sincrona, ovvero **MpScanStart** restituirà solo dopo il completamento dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="4386e-125">(By default the scan operation is synchronous, meaning **MpScanStart** will return only after the scan is finished.)</span></span><br/>      |
| <span id="MPSCAN_OPTION_PROGRESS"></span><span id="mpscan_option_progress"></span><dl> <span data-ttu-id="4386e-126"><dt>**\_stato dell'opzione MPSCAN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4386e-126"><dt>**MPSCAN\_OPTION\_PROGRESS**</dt></span></span> </dl>                   | <span data-ttu-id="4386e-127">Il chiamante è interessato a ricevere informazioni sullo stato di avanzamento dell'analisi tramite un callback.</span><span class="sxs-lookup"><span data-stu-id="4386e-127">The caller is interested in receiving scan progress information via a callback.</span></span><br/>                                                                                                                                                                            |
| <span id="MPSCAN_OPTION_LOWPRIORITY"></span><span id="mpscan_option_lowpriority"></span><dl> <span data-ttu-id="4386e-128"><dt>**\_opzione MPSCAN \_ LOWPRIORITY**</dt></span><span class="sxs-lookup"><span data-stu-id="4386e-128"><dt>**MPSCAN\_OPTION\_LOWPRIORITY**</dt></span></span> </dl>          | <span data-ttu-id="4386e-129">Eseguire l'analisi con priorità bassa.</span><span class="sxs-lookup"><span data-stu-id="4386e-129">Perform the scan with low priority.</span></span> <span data-ttu-id="4386e-130">Per impostazione predefinita, l'operazione di analisi viene eseguita con priorità normale.</span><span class="sxs-lookup"><span data-stu-id="4386e-130">(By default the scan operation is performed with normal priority.)</span></span><br/>                                                                                                                                                     |
| <span id="MPSCAN_OPTION_PACKEDEXES"></span><span id="mpscan_option_packedexes"></span><dl> <span data-ttu-id="4386e-131"><dt>**\_opzione MPSCAN \_ PACKEDEXES**</dt></span><span class="sxs-lookup"><span data-stu-id="4386e-131"><dt>**MPSCAN\_OPTION\_PACKEDEXES**</dt></span></span> </dl>             | <span data-ttu-id="4386e-132">Analizza i file eseguibili compressi per individuare possibili minacce.</span><span class="sxs-lookup"><span data-stu-id="4386e-132">Scan packed executables for possible threats.</span></span><br/>                                                                                                                                                                                                              |
| <span id="MPSCAN_OPTION_ARCHIVES"></span><span id="mpscan_option_archives"></span><dl> <span data-ttu-id="4386e-133"><dt>**\_archivi delle opzioni di MPSCAN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4386e-133"><dt>**MPSCAN\_OPTION\_ARCHIVES**</dt></span></span> </dl>                   | <span data-ttu-id="4386e-134">Analizza il contenuto dell'archivio per individuare possibili minacce.</span><span class="sxs-lookup"><span data-stu-id="4386e-134">Scan archive contents for possible threats.</span></span> <span data-ttu-id="4386e-135">Gli archivi sono file con estensioni, ad esempio zip, CAB o tar.</span><span class="sxs-lookup"><span data-stu-id="4386e-135">Archives are files with extensions such as .zip, .cab, or .tar.</span></span><br/>                                                                                                                                                |
| <span id="MPSCAN_OPTION_HEURISTICS"></span><span id="mpscan_option_heuristics"></span><dl> <span data-ttu-id="4386e-136"><dt>**\_euristica dell'opzione MPSCAN \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4386e-136"><dt>**MPSCAN\_OPTION\_HEURISTICS**</dt></span></span> </dl>             | <span data-ttu-id="4386e-137">Abilitare l'analisi basata su euristica.</span><span class="sxs-lookup"><span data-stu-id="4386e-137">Enable heuristics-based scanning.</span></span> <span data-ttu-id="4386e-138">Questa operazione analizzerà le minacce con tipo di rilevamento impostato su euristica.</span><span class="sxs-lookup"><span data-stu-id="4386e-138">This will scan for threats with detection type set to heuristics.</span></span><br/>                                                                                                                                                        |
| <span id="MPSCAN_OPTION_REPORTFRIENDLY"></span><span id="mpscan_option_reportfriendly"></span><dl> <span data-ttu-id="4386e-139"><dt>**\_opzione MPSCAN \_ REPORTFRIENDLY**</dt></span><span class="sxs-lookup"><span data-stu-id="4386e-139"><dt>**MPSCAN\_OPTION\_REPORTFRIENDLY**</dt></span></span> </dl> | <span data-ttu-id="4386e-140">Segnala elementi descrittivi in un'analisi delle risorse.</span><span class="sxs-lookup"><span data-stu-id="4386e-140">Report friendly items in a resource scan.</span></span> <span data-ttu-id="4386e-141">Questa operazione è destinata solo a un uso interno.</span><span class="sxs-lookup"><span data-stu-id="4386e-141">This is intended for internal use only.</span></span><br/>                                                                                                                                                                          |
| <span id="MPSCAN_OPTION_REPORTUNKNOWN"></span><span id="mpscan_option_reportunknown"></span><dl> <span data-ttu-id="4386e-142"><dt>**\_opzione MPSCAN \_ REPORTUNKNOWN**</dt></span><span class="sxs-lookup"><span data-stu-id="4386e-142"><dt>**MPSCAN\_OPTION\_REPORTUNKNOWN**</dt></span></span> </dl>    | <span data-ttu-id="4386e-143">Segnala elementi sconosciuti in un'analisi delle risorse.</span><span class="sxs-lookup"><span data-stu-id="4386e-143">Report unknown items in a resource scan.</span></span> <span data-ttu-id="4386e-144">Questa operazione è destinata solo a un uso interno.</span><span class="sxs-lookup"><span data-stu-id="4386e-144">This is intended for internal use only.</span></span><br/>                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_NOCONSOLIDATE"></span><span id="mpscan_option_noconsolidate"></span><dl> <span data-ttu-id="4386e-145"><dt>**\_opzione MPSCAN \_ consolidate**</dt></span><span class="sxs-lookup"><span data-stu-id="4386e-145"><dt>**MPSCAN\_OPTION\_NOCONSOLIDATE**</dt></span></span> </dl>    | <span data-ttu-id="4386e-146">Non consolidare i risultati dell'analisi con la visualizzazione minacce globali.</span><span class="sxs-lookup"><span data-stu-id="4386e-146">Do not consolidate scan results with global threat view.</span></span> <span data-ttu-id="4386e-147">Questa operazione è utile per un client, ad esempio un client di posta elettronica, che vuole controllare la pulizia dell'esperienza utente autonomamente, anziché consentire la pulizia dell'esperienza utente predefinita.</span><span class="sxs-lookup"><span data-stu-id="4386e-147">This is useful for a client (such as an email client) which wants to control cleaning UX by itself rather than allowing default anti-malware cleaning UX.</span></span> <span data-ttu-id="4386e-148">Questa operazione è destinata solo a un uso interno.</span><span class="sxs-lookup"><span data-stu-id="4386e-148">This is intended for internal use only.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4386e-149">*pScanResources* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4386e-149">*pScanResources* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4386e-150">Tipo: **\_ risorse PMPSCAN**</span><span class="sxs-lookup"><span data-stu-id="4386e-150">Type: **PMPSCAN\_RESOURCES**</span></span>

<span data-ttu-id="4386e-151">Puntatore alle informazioni sulle risorse di analisi.</span><span class="sxs-lookup"><span data-stu-id="4386e-151">A pointer to the scan resource information.</span></span> <span data-ttu-id="4386e-152">Questo parametro deve essere **null** per un'analisi veloce.</span><span class="sxs-lookup"><span data-stu-id="4386e-152">This parameter must be **NULL** for a quick scan.</span></span> <span data-ttu-id="4386e-153">Si tratta di un parametro facoltativo per un'analisi completa.</span><span class="sxs-lookup"><span data-stu-id="4386e-153">This is an optional parameter for a full scan.</span></span> <span data-ttu-id="4386e-154">Per un'analisi delle risorse, questo parametro deve essere specificato con almeno una struttura di informazioni sulle risorse.</span><span class="sxs-lookup"><span data-stu-id="4386e-154">For a resource scan this parameter must be specified with at least one resource information structure.</span></span> <span data-ttu-id="4386e-155">Per analizzare risorse specifiche, il chiamante deve disporre dell'autorizzazione di **\_ lettura generica** per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="4386e-155">To scan specific resources the caller must have **GENERIC\_READ** permission for the resource.</span></span> <span data-ttu-id="4386e-156">Vedere [**\_ risorse di MPSCAN**](mpscan-resources.md).</span><span class="sxs-lookup"><span data-stu-id="4386e-156">See [**MPSCAN\_RESOURCES**](mpscan-resources.md).</span></span>

</dd> <dt>

<span data-ttu-id="4386e-157">*pCallbackInfo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4386e-157">*pCallbackInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4386e-158">Tipo: **PMPCALLBACK \_ info**</span><span class="sxs-lookup"><span data-stu-id="4386e-158">Type: **PMPCALLBACK\_INFO**</span></span>

<span data-ttu-id="4386e-159">Puntatore alle informazioni di callback utilizzate per inserire il client con le modifiche dello stato di analisi (ad esempio, avvio e completamento) e le informazioni sullo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="4386e-159">A pointer to the callback information used to feed the client with scan state changes (such as start and complete) and progress information.</span></span> <span data-ttu-id="4386e-160">I [**\_ dati MPCALLBACK**](mpcallback-data.md) restituiti nella funzione di callback segnalano lo stato di analisi effettivo e le informazioni relative allo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="4386e-160">The [**MPCALLBACK\_DATA**](mpcallback-data.md) passed back in the callback function reports actual scan state and progress-related information.</span></span> <span data-ttu-id="4386e-161">Di seguito è riportato un elenco di possibili callback:</span><span class="sxs-lookup"><span data-stu-id="4386e-161">The following is a list of possible callbacks:</span></span>



| <span data-ttu-id="4386e-162">Valore</span><span class="sxs-lookup"><span data-stu-id="4386e-162">Value</span></span>                                                                                                                                                                                                       | <span data-ttu-id="4386e-163">Significato</span><span class="sxs-lookup"><span data-stu-id="4386e-163">Meaning</span></span>                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span><dl> <span data-ttu-id="4386e-164"><dt>**\_avvio dell'analisi MPNOTIFY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4386e-164"><dt>**MPNOTIFY\_SCAN\_START**</dt></span></span> </dl>                            | <span data-ttu-id="4386e-165">Operazione di analisi avviata.</span><span class="sxs-lookup"><span data-stu-id="4386e-165">Scan operation started.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span><dl> <span data-ttu-id="4386e-166"><dt>**\_analisi MPNOTIFY \_ completata**</dt></span><span class="sxs-lookup"><span data-stu-id="4386e-166"><dt>**MPNOTIFY\_SCAN\_COMPLETE**</dt></span></span> </dl>                   | <span data-ttu-id="4386e-167">Operazione di analisi completata.</span><span class="sxs-lookup"><span data-stu-id="4386e-167">Scan operation completed.</span></span> <span data-ttu-id="4386e-168">Altre informazioni sono disponibili tramite la struttura [**\_ dei dati MPSCAN**](mpscan-data.md) .</span><span class="sxs-lookup"><span data-stu-id="4386e-168">Additional information is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/>                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span><dl> <span data-ttu-id="4386e-169"><dt>**\_analisi MPNOTIFY \_ sospesa**</dt></span><span class="sxs-lookup"><span data-stu-id="4386e-169"><dt>**MPNOTIFY\_SCAN\_PAUSED**</dt></span></span> </dl>                         | <span data-ttu-id="4386e-170">Operazione di analisi sospesa.</span><span class="sxs-lookup"><span data-stu-id="4386e-170">Scan operation is paused.</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span><dl> <span data-ttu-id="4386e-171"><dt>**\_analisi MPNOTIFY \_ ripresa**</dt></span><span class="sxs-lookup"><span data-stu-id="4386e-171"><dt>**MPNOTIFY\_SCAN\_RESUMED**</dt></span></span> </dl>                      | <span data-ttu-id="4386e-172">Operazione di analisi ripresa dalla pausa.</span><span class="sxs-lookup"><span data-stu-id="4386e-172">Scan operation resumed from pause.</span></span><br/>                                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span><dl> <span data-ttu-id="4386e-173"><dt>**\_annullamento dell'analisi MPNOTIFY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4386e-173"><dt>**MPNOTIFY\_SCAN\_CANCEL**</dt></span></span> </dl>                         | <span data-ttu-id="4386e-174">Operazione di analisi annullata.</span><span class="sxs-lookup"><span data-stu-id="4386e-174">Scan operation was cancelled.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span><dl> <span data-ttu-id="4386e-175"><dt>**\_stato analisi \_ MPNOTIFY**</dt></span><span class="sxs-lookup"><span data-stu-id="4386e-175"><dt>**MPNOTIFY\_SCAN\_PROGRESS**</dt></span></span> </dl>                   | <span data-ttu-id="4386e-176">Informazioni sullo stato di avanzamento dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="4386e-176">Scan progress information.</span></span> <span data-ttu-id="4386e-177">Altre informazioni, ad esempio le statistiche sulle risorse, sono disponibili tramite la struttura [**\_ dei dati MPSCAN**](mpscan-data.md) .</span><span class="sxs-lookup"><span data-stu-id="4386e-177">Additional information (such as resource statistics) is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/>                                                                                                                                                               |
| <span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span><dl> <span data-ttu-id="4386e-178"><dt>**\_errore di analisi MPNOTIFY \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4386e-178"><dt>**MPNOTIFY\_SCAN\_ERROR**</dt></span></span> </dl>                            | <span data-ttu-id="4386e-179">Analizza le informazioni sugli errori per una risorsa specifica.</span><span class="sxs-lookup"><span data-stu-id="4386e-179">Scan error information for a specific resource.</span></span> <span data-ttu-id="4386e-180">Le informazioni specifiche sulle risorse sono disponibili tramite la struttura [**\_ dei dati MPSCAN**](mpscan-data.md) .</span><span class="sxs-lookup"><span data-stu-id="4386e-180">The specific resource information is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/>                                                                                                                                                             |
| <span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span><dl> <span data-ttu-id="4386e-181"><dt>**\_analisi MPNOTIFY \_ infettata**</dt></span><span class="sxs-lookup"><span data-stu-id="4386e-181"><dt>**MPNOTIFY\_SCAN\_INFECTED**</dt></span></span> </dl>                   | <span data-ttu-id="4386e-182">L'analisi ha rilevato una risorsa infetta.</span><span class="sxs-lookup"><span data-stu-id="4386e-182">Scan found an infected resource.</span></span> <span data-ttu-id="4386e-183">Si noti che nella maggior parte dei casi questo comporterà una minaccia segnalata alla fine dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="4386e-183">Note that in most of the cases this will result in some threat reported at the end of the scan.</span></span> <span data-ttu-id="4386e-184">In alcuni casi potrebbe non essere materializzata come minaccia a causa di esclusioni.</span><span class="sxs-lookup"><span data-stu-id="4386e-184">Sometimes it may not materialize as a threat because of exclusions.</span></span> <span data-ttu-id="4386e-185">Altre informazioni sulle risorse infette sono disponibili tramite la struttura [**\_ dei dati MPSCAN**](mpscan-data.md) .</span><span class="sxs-lookup"><span data-stu-id="4386e-185">Additional infected resource information is available via [**MPSCAN\_DATA**](mpscan-data.md) structure.</span></span><br/> |
| <span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span><dl> <span data-ttu-id="4386e-186"><dt>**MPNOTIFY \_ Scan \_ MEMORYSTART**</dt></span><span class="sxs-lookup"><span data-stu-id="4386e-186"><dt>**MPNOTIFY\_SCAN\_MEMORYSTART**</dt></span></span> </dl>          | <span data-ttu-id="4386e-187">È stata avviata la parte di analisi veloce dell'analisi completa.</span><span class="sxs-lookup"><span data-stu-id="4386e-187">Quick scan portion of the full scan has started.</span></span><br/>                                                                                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span><dl> <span data-ttu-id="4386e-188"><dt>**MPNOTIFY \_ Scan \_ MEMORYCOMPLETE**</dt></span><span class="sxs-lookup"><span data-stu-id="4386e-188"><dt>**MPNOTIFY\_SCAN\_MEMORYCOMPLETE**</dt></span></span> </dl> | <span data-ttu-id="4386e-189">È stata completata la parte di analisi veloce dell'analisi completa.</span><span class="sxs-lookup"><span data-stu-id="4386e-189">Quick scan portion of the full scan has completed.</span></span><br/>                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <span data-ttu-id="4386e-190"><dt>**\_errore interno \_ MPNOTIFY**</dt></span><span class="sxs-lookup"><span data-stu-id="4386e-190"><dt>**MPNOTIFY\_INTERNAL\_FAILURE**</dt></span></span> </dl>          | <span data-ttu-id="4386e-191">Si è verificato un errore generico durante l'operazione di analisi.</span><span class="sxs-lookup"><span data-stu-id="4386e-191">Scan operation has encountered a generic failure.</span></span> <span data-ttu-id="4386e-192">Il codice di errore del valore *HRESULT* nei [**\_ dati MPCALLBACK**](mpcallback-data.md) è specifico.</span><span class="sxs-lookup"><span data-stu-id="4386e-192">The *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md) has the specific error code.</span></span><br/>                                                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="4386e-193">*phScanHandle* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4386e-193">*phScanHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4386e-194">Tipo: **PMPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="4386e-194">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="4386e-195">Handle di analisi restituito che identifica l'analisi attualmente avviata.</span><span class="sxs-lookup"><span data-stu-id="4386e-195">Returned scan handle which identifies the currently initiated scan.</span></span> <span data-ttu-id="4386e-196">Questo handle può essere usato nelle chiamate di funzione successive, ad esempio per recuperare un risultato di analisi.</span><span class="sxs-lookup"><span data-stu-id="4386e-196">This handle can be used in subsequent function calls, such as to retrieve a scan result.</span></span> <span data-ttu-id="4386e-197">L'handle deve essere chiuso con la funzione [**MpHandleClose**](mphandleclose.md) .</span><span class="sxs-lookup"><span data-stu-id="4386e-197">The handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4386e-198">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4386e-198">Return value</span></span>

<span data-ttu-id="4386e-199">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4386e-199">Type: **HRESULT**</span></span>

<span data-ttu-id="4386e-200">Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4386e-200">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="4386e-201">Se la funzione ha esito negativo, il valore restituito è un codice **HRESULT** non riuscito.</span><span class="sxs-lookup"><span data-stu-id="4386e-201">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="4386e-202">Il chiamante può utilizzare la funzione [**MpErrorMessageFormat**](mperrormessageformat.md) per ottenere una descrizione generica del messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="4386e-202">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4386e-203">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4386e-203">Requirements</span></span>



| <span data-ttu-id="4386e-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="4386e-204">Requirement</span></span> | <span data-ttu-id="4386e-205">Valore</span><span class="sxs-lookup"><span data-stu-id="4386e-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4386e-206">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4386e-206">Minimum supported client</span></span><br/> | <span data-ttu-id="4386e-207">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4386e-207">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="4386e-208">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4386e-208">Minimum supported server</span></span><br/> | <span data-ttu-id="4386e-209">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4386e-209">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4386e-210">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4386e-210">Header</span></span><br/>                   | <dl> <span data-ttu-id="4386e-211"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="4386e-211"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="4386e-212">DLL</span><span class="sxs-lookup"><span data-stu-id="4386e-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4386e-213"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4386e-213"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4386e-214">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4386e-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4386e-215">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="4386e-215">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="4386e-216">**MpHandleClose**</span><span class="sxs-lookup"><span data-stu-id="4386e-216">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> <dt>

[<span data-ttu-id="4386e-217">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="4386e-217">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="4386e-218">**\_dati MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="4386e-218">**MPCALLBACK\_DATA**</span></span>](mpcallback-data.md)
</dt> <dt>

[<span data-ttu-id="4386e-219">**\_dati MPSCAN**</span><span class="sxs-lookup"><span data-stu-id="4386e-219">**MPSCAN\_DATA**</span></span>](mpscan-data.md)
</dt> <dt>

[<span data-ttu-id="4386e-220">**risorse di MPSCAN \_**</span><span class="sxs-lookup"><span data-stu-id="4386e-220">**MPSCAN\_RESOURCES**</span></span>](mpscan-resources.md)
</dt> <dt>

[<span data-ttu-id="4386e-221">**\_tipo MPSCAN**</span><span class="sxs-lookup"><span data-stu-id="4386e-221">**MPSCAN\_TYPE**</span></span>](mpscan-type.md)
</dt> </dl>

 

 





