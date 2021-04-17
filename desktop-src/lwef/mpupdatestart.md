---
title: Funzione MpUpdateStart (MpClient. h)
description: Avvia un'operazione di aggiornamento della firma.
ms.assetid: BB056356-17E5-42F0-9636-9E1C254361E4
keywords:
- Funzionalità dell'ambiente Windows legacy della funzione MpUpdateStart
topic_type:
- apiref
api_name:
- MpUpdateStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39867525529339c6b354ae771b070589ca52acfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478736"
---
# <a name="mpupdatestart-function"></a><span data-ttu-id="391e5-104">MpUpdateStart (funzione)</span><span class="sxs-lookup"><span data-stu-id="391e5-104">MpUpdateStart function</span></span>

<span data-ttu-id="391e5-105">Avvia un'operazione di aggiornamento della firma.</span><span class="sxs-lookup"><span data-stu-id="391e5-105">Starts a signature update operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="391e5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="391e5-106">Syntax</span></span>


```C++
HRESULT WINAPI MpUpdateStart(
  _In_     MPHANDLE         hMpHandle,
  _In_     DWORD            dwUpdateOptions,
  _In_opt_ PMPCALLBACK_INFO pCallbackInfo,
  _Out_    PMPHANDLE        phUpdateHandle
);
```



## <a name="parameters"></a><span data-ttu-id="391e5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="391e5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="391e5-108">*hMpHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="391e5-108">*hMpHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="391e5-109">Tipo: **MPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="391e5-109">Type: **MPHANDLE**</span></span>

<span data-ttu-id="391e5-110">Handle per l'interfaccia di malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="391e5-110">Handle to the malware protection manager interface.</span></span> <span data-ttu-id="391e5-111">Questo handle viene restituito dalla funzione [**MpManagerOpen**](mpmanageropen.md) .</span><span class="sxs-lookup"><span data-stu-id="391e5-111">This handle is returned by the [**MpManagerOpen**](mpmanageropen.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="391e5-112">*dwUpdateOptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="391e5-112">*dwUpdateOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="391e5-113">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="391e5-113">Type: **DWORD**</span></span>

<span data-ttu-id="391e5-114">Specifica l'opzione per l'operazione di aggiornamento della firma.</span><span class="sxs-lookup"><span data-stu-id="391e5-114">Specifies the option for the signature update operation.</span></span> <span data-ttu-id="391e5-115">Può essere uno dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="391e5-115">It can be one of the following values:</span></span>



| <span data-ttu-id="391e5-116">Valore</span><span class="sxs-lookup"><span data-stu-id="391e5-116">Value</span></span>                                                                                                                                                                                              | <span data-ttu-id="391e5-117">Significato</span><span class="sxs-lookup"><span data-stu-id="391e5-117">Meaning</span></span>                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPUPDATE_OPTION_NONE"></span><span id="mpupdate_option_none"></span><dl> <span data-ttu-id="391e5-118"><dt>**\_opzione MPUPDATE \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="391e5-118"><dt>**MPUPDATE\_OPTION\_NONE**</dt></span></span> </dl>                | <span data-ttu-id="391e5-119">Non è richiesta alcuna opzione specifica.</span><span class="sxs-lookup"><span data-stu-id="391e5-119">No specific option is requested.</span></span><br/>                                                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_ASYNC"></span><span id="mpupdate_option_async"></span><dl> <span data-ttu-id="391e5-120"><dt>**\_opzione MPUPDATE \_ Async**</dt></span><span class="sxs-lookup"><span data-stu-id="391e5-120"><dt>**MPUPDATE\_OPTION\_ASYNC**</dt></span></span> </dl>             | <span data-ttu-id="391e5-121">L'operazione di aggiornamento deve essere asincrona, in cui **MpUpdateStart** viene restituito immediatamente dopo la riuscita dell'avvio dell'aggiornamento della firma.</span><span class="sxs-lookup"><span data-stu-id="391e5-121">The update operation is to be asynchronous, where **MpUpdateStart** returns immediately after the successful initiation of the signature update.</span></span> <span data-ttu-id="391e5-122">Per impostazione predefinita, l'operazione di aggiornamento è sincrona, ovvero **MpUpdateStart** restituirà solo dopo il completamento dell'aggiornamento della firma.</span><span class="sxs-lookup"><span data-stu-id="391e5-122">(By default the update operation is synchronous, meaning **MpUpdateStart** will return only after the signature update is finished.)</span></span><br/> |
| <span id="MPUPDATE_OPTION_PROGRESS"></span><span id="mpupdate_option_progress"></span><dl> <span data-ttu-id="391e5-123"><dt>**\_stato dell'opzione MPUPDATE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="391e5-123"><dt>**MPUPDATE\_OPTION\_PROGRESS**</dt></span></span> </dl>    | <span data-ttu-id="391e5-124">Il chiamante è interessato a ricevere informazioni sullo stato di aggiornamento della firma tramite un callback.</span><span class="sxs-lookup"><span data-stu-id="391e5-124">The caller is interested in receiving signature update progress information via a callback.</span></span><br/>                                                                                                                                                                                           |
| <span id="MPUPDATE_OPTION_HTTP"></span><span id="mpupdate_option_http"></span><dl> <span data-ttu-id="391e5-125"><dt>**\_opzione MPUPDATE \_ http**</dt></span><span class="sxs-lookup"><span data-stu-id="391e5-125"><dt>**MPUPDATE\_OPTION\_HTTP**</dt></span></span> </dl>                | <span data-ttu-id="391e5-126">L'aggiornamento della firma viene eseguito scaricando il pacchetto di firma completa dal sito del portale Microsoft Security.</span><span class="sxs-lookup"><span data-stu-id="391e5-126">The signature update is performed by downloading the full signature package from the Microsoft security portal site.</span></span> <span data-ttu-id="391e5-127">Può essere usata come opzione di fallback se il client sta riscontrando un problema di download della firma tramite Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="391e5-127">This can be used as a fallback option if the client is experiencing a signature download problem via Microsoft Update.</span></span><br/>                                           |
| <span id="MPUPDATE_OPTION_UNC"></span><span id="mpupdate_option_unc"></span><dl> <span data-ttu-id="391e5-128"><dt>**\_UNC option \_ MPUPDATE**</dt></span><span class="sxs-lookup"><span data-stu-id="391e5-128"><dt>**MPUPDATE\_OPTION\_UNC**</dt></span></span> </dl>                   | <span data-ttu-id="391e5-129">Esegue l'aggiornamento della firma utilizzando il download diretto da condivisioni UNC.</span><span class="sxs-lookup"><span data-stu-id="391e5-129">Performs signature update using direct download from UNC shares.</span></span><br/>                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_MANAGED"></span><span id="mpupdate_option_managed"></span><dl> <span data-ttu-id="391e5-130"><dt>**\_opzione MPUPDATE \_ gestita**</dt></span><span class="sxs-lookup"><span data-stu-id="391e5-130"><dt>**MPUPDATE\_OPTION\_MANAGED**</dt></span></span> </dl>       | <span data-ttu-id="391e5-131">Esegue l'aggiornamento della firma utilizzando il servizio gestito WSUS.</span><span class="sxs-lookup"><span data-stu-id="391e5-131">Performs signature update using the Managed Service WSUS.</span></span><br/>                                                                                                                                                                                                                             |
| <span id="MPUPDATE_OPTION_UNMANAGED"></span><span id="mpupdate_option_unmanaged"></span><dl> <span data-ttu-id="391e5-132"><dt>**\_opzione MPUPDATE \_ non gestita**</dt></span><span class="sxs-lookup"><span data-stu-id="391e5-132"><dt>**MPUPDATE\_OPTION\_UNMANAGED**</dt></span></span> </dl> | <span data-ttu-id="391e5-133">Esegue l'aggiornamento delle firme usando il servizio non gestito MU/WU.</span><span class="sxs-lookup"><span data-stu-id="391e5-133">Performs signature update using the Unmanaged Service MU/WU.</span></span><br/>                                                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="391e5-134">*pCallbackInfo* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="391e5-134">*pCallbackInfo* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="391e5-135">Tipo: **PMPCALLBACK \_ info**</span><span class="sxs-lookup"><span data-stu-id="391e5-135">Type: **PMPCALLBACK\_INFO**</span></span>

<span data-ttu-id="391e5-136">Puntatore alle informazioni di callback utilizzate per inserire il client con le modifiche dello stato di aggiornamento della firma (ad esempio, avvio e completamento) e le informazioni sullo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="391e5-136">A pointer to the callback information used to feed the client with signature update state changes (such as start and complete) and progress information.</span></span> <span data-ttu-id="391e5-137">I [**\_ dati MPCALLBACK**](mpcallback-data.md) restituiti nella funzione di callback segnalano lo stato di aggiornamento effettivo e le informazioni relative allo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="391e5-137">The [**MPCALLBACK\_DATA**](mpcallback-data.md) passed back in the callback function reports actual update state and progress-related information.</span></span> <span data-ttu-id="391e5-138">Di seguito è riportato un elenco di possibili callback:</span><span class="sxs-lookup"><span data-stu-id="391e5-138">The following is a list of possible callbacks:</span></span>



| <span data-ttu-id="391e5-139">Valore</span><span class="sxs-lookup"><span data-stu-id="391e5-139">Value</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="391e5-140">Significato</span><span class="sxs-lookup"><span data-stu-id="391e5-140">Meaning</span></span>                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span><dl> <span data-ttu-id="391e5-141"><dt>**\_inizio MPNOTIFY SIGUPDATE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="391e5-141"><dt>**MPNOTIFY\_SIGUPDATE\_START**</dt></span></span> </dl>                                      | <span data-ttu-id="391e5-142">Operazione di aggiornamento avviata.</span><span class="sxs-lookup"><span data-stu-id="391e5-142">Update operation started.</span></span><br/>                                                                                                                                  |
| <span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span><dl> <span data-ttu-id="391e5-143"><dt>**MPNOTIFY \_ SIGUPDATE \_ completata**</dt></span><span class="sxs-lookup"><span data-stu-id="391e5-143"><dt>**MPNOTIFY\_SIGUPDATE\_COMPLETE**</dt></span></span> </dl>                             | <span data-ttu-id="391e5-144">Operazione di aggiornamento completata.</span><span class="sxs-lookup"><span data-stu-id="391e5-144">Update operation completed.</span></span><br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span><dl> <span data-ttu-id="391e5-145"><dt>**\_avvio della \_ ricerca \_ SIGUPDATE di MPNOTIFY**</dt></span><span class="sxs-lookup"><span data-stu-id="391e5-145"><dt>**MPNOTIFY\_SIGUPDATE\_SEARCH\_START**</dt></span></span> </dl>                | <span data-ttu-id="391e5-146">Ricerca degli aggiornamenti avviata.</span><span class="sxs-lookup"><span data-stu-id="391e5-146">Search for updates started.</span></span><br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span><dl> <span data-ttu-id="391e5-147"><dt>**\_ricerca MPNOTIFY \_ SIGUPDATE \_ completata**</dt></span><span class="sxs-lookup"><span data-stu-id="391e5-147"><dt>**MPNOTIFY\_SIGUPDATE\_SEARCH\_COMPLETE**</dt></span></span> </dl>       | <span data-ttu-id="391e5-148">Ricerca degli aggiornamenti completata.</span><span class="sxs-lookup"><span data-stu-id="391e5-148">Search for updates completed.</span></span> <span data-ttu-id="391e5-149">Altre informazioni sono disponibili tramite la struttura [**\_ dei dati MPSIGUPDATE**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="391e5-149">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span><dl> <span data-ttu-id="391e5-150"><dt>**avvio del download di MPNOTIFY \_ SIGUPDATE \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="391e5-150"><dt>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_START**</dt></span></span> </dl>          | <span data-ttu-id="391e5-151">Download per l'aggiornamento avviato.</span><span class="sxs-lookup"><span data-stu-id="391e5-151">Download for update started.</span></span><br/>                                                                                                                               |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span><dl> <span data-ttu-id="391e5-152"><dt>**stato del download di MPNOTIFY \_ SIGUPDATE \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="391e5-152"><dt>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_PROGRESS**</dt></span></span> </dl> | <span data-ttu-id="391e5-153">Scaricare informazioni sullo stato di avanzamento.</span><span class="sxs-lookup"><span data-stu-id="391e5-153">Download progress information.</span></span> <span data-ttu-id="391e5-154">Altre informazioni sono disponibili tramite la struttura [**\_ dei dati MPSIGUPDATE**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="391e5-154">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                            |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span><dl> <span data-ttu-id="391e5-155"><dt>**Download di MPNOTIFY \_ SIGUPDATE \_ \_ completato**</dt></span><span class="sxs-lookup"><span data-stu-id="391e5-155"><dt>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_COMPLETE**</dt></span></span> </dl> | <span data-ttu-id="391e5-156">Download per l'aggiornamento completato.</span><span class="sxs-lookup"><span data-stu-id="391e5-156">Download for update complete.</span></span> <span data-ttu-id="391e5-157">Altre informazioni sono disponibili tramite la struttura [**\_ dei dati MPSIGUPDATE**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="391e5-157">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span><dl> <span data-ttu-id="391e5-158"><dt>**\_ \_ avvio installazione di MPNOTIFY SIGUPDATE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="391e5-158"><dt>**MPNOTIFY\_SIGUPDATE\_INSTALL\_START**</dt></span></span> </dl>             | <span data-ttu-id="391e5-159">Installazione dell'aggiornamento avviata.</span><span class="sxs-lookup"><span data-stu-id="391e5-159">Installation of update started.</span></span><br/>                                                                                                                            |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span><dl> <span data-ttu-id="391e5-160"><dt>**stato di installazione di MPNOTIFY \_ SIGUPDATE \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="391e5-160"><dt>**MPNOTIFY\_SIGUPDATE\_INSTALL\_PROGRESS**</dt></span></span> </dl>    | <span data-ttu-id="391e5-161">Informazioni sullo stato dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="391e5-161">Installation progress information.</span></span> <span data-ttu-id="391e5-162">Altre informazioni sono disponibili tramite la struttura [**\_ dei dati MPSIGUPDATE**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="391e5-162">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                        |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span><dl> <span data-ttu-id="391e5-163"><dt>**installazione di MPNOTIFY \_ SIGUPDATE \_ \_ completata**</dt></span><span class="sxs-lookup"><span data-stu-id="391e5-163"><dt>**MPNOTIFY\_SIGUPDATE\_INSTALL\_COMPLETE**</dt></span></span> </dl>    | <span data-ttu-id="391e5-164">L'installazione dell'aggiornamento è stata completata.</span><span class="sxs-lookup"><span data-stu-id="391e5-164">Installation of update completed.</span></span> <span data-ttu-id="391e5-165">Altre informazioni sono disponibili tramite la struttura [**\_ dei dati MPSIGUPDATE**](mpsigupdate-data.md) .</span><span class="sxs-lookup"><span data-stu-id="391e5-165">Additional information is available via [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md) structure.</span></span><br/>                         |
| <span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span><dl> <span data-ttu-id="391e5-166"><dt>**\_richiesta SIGUPDATE \_ MPNOTIFY \_ elaborata**</dt></span><span class="sxs-lookup"><span data-stu-id="391e5-166"><dt>**MPNOTIFY\_SIGUPDATE\_REQUEST\_PROCESSED**</dt></span></span> </dl> | <span data-ttu-id="391e5-167">Il servizio antimalware ha elaborato una richiesta di aggiornamento della firma.</span><span class="sxs-lookup"><span data-stu-id="391e5-167">The antimalware service processed a signature update request.</span></span> <span data-ttu-id="391e5-168">Esito negativo o esito positivo è indicato da *HRESULT* nei [**\_ dati MPCALLBACK**](mpcallback-data.md).</span><span class="sxs-lookup"><span data-stu-id="391e5-168">Failure or success is indicated by *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md).</span></span><br/> |
| <span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span><dl> <span data-ttu-id="391e5-169"><dt>**riavvio di MPNOTIFY \_ SIGUPDATE \_ \_ obbligatorio**</dt></span><span class="sxs-lookup"><span data-stu-id="391e5-169"><dt>**MPNOTIFY\_SIGUPDATE\_REBOOT\_REQUIRED**</dt></span></span> </dl>       | <span data-ttu-id="391e5-170">Per completare l'operazione di aggiornamento, è necessario riavviare il computer.</span><span class="sxs-lookup"><span data-stu-id="391e5-170">Requires reboot to complete the update operation.</span></span> <span data-ttu-id="391e5-171">Esito negativo o esito positivo è indicato da *HRESULT* nei [**\_ dati MPCALLBACK**](mpcallback-data.md).</span><span class="sxs-lookup"><span data-stu-id="391e5-171">Failure or success is indicated by *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md).</span></span><br/>             |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <span data-ttu-id="391e5-172"><dt>**\_errore interno \_ MPNOTIFY**</dt></span><span class="sxs-lookup"><span data-stu-id="391e5-172"><dt>**MPNOTIFY\_INTERNAL\_FAILURE**</dt></span></span> </dl>                                   | <span data-ttu-id="391e5-173">Si è verificato un errore generico durante l'operazione di aggiornamento della firma.</span><span class="sxs-lookup"><span data-stu-id="391e5-173">Signature update operation has encountered a generic failure.</span></span> <span data-ttu-id="391e5-174">Il codice di errore del valore *HRESULT* nei [**\_ dati MPCALLBACK**](mpcallback-data.md) è specifico.</span><span class="sxs-lookup"><span data-stu-id="391e5-174">The *hResult* in [**MPCALLBACK\_DATA**](mpcallback-data.md) has the specific error code.</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="391e5-175">*phUpdateHandle* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="391e5-175">*phUpdateHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="391e5-176">Tipo: **PMPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="391e5-176">Type: **PMPHANDLE**</span></span>

<span data-ttu-id="391e5-177">Handle di aggiornamento restituito che identifica l'operazione di aggiornamento della firma attualmente avviata.</span><span class="sxs-lookup"><span data-stu-id="391e5-177">Returned update handle which identifies the currently initiated signature update operation.</span></span> <span data-ttu-id="391e5-178">Questo handle può essere utilizzato nelle chiamate di funzione successive, ad esempio per controllare l'operazione di aggiornamento della firma.</span><span class="sxs-lookup"><span data-stu-id="391e5-178">This handle can be used in subsequent function calls, such as to control the signature update operation.</span></span> <span data-ttu-id="391e5-179">L'handle deve essere chiuso con la funzione [**MpHandleClose**](mphandleclose.md) .</span><span class="sxs-lookup"><span data-stu-id="391e5-179">The handle must be closed with the [**MpHandleClose**](mphandleclose.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="391e5-180">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="391e5-180">Return value</span></span>

<span data-ttu-id="391e5-181">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="391e5-181">Type: **HRESULT**</span></span>

<span data-ttu-id="391e5-182">Se la funzione ha esito positivo, il valore restituito è **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="391e5-182">If the function succeeds the return value is **S\_OK**.</span></span>

<span data-ttu-id="391e5-183">Se la funzione ha esito negativo, il valore restituito è un codice **HRESULT** non riuscito.</span><span class="sxs-lookup"><span data-stu-id="391e5-183">If the function fails then the return value is a failed **HRESULT** code.</span></span> <span data-ttu-id="391e5-184">Il chiamante può utilizzare la funzione [**MpErrorMessageFormat**](mperrormessageformat.md) per ottenere una descrizione generica del messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="391e5-184">The caller can use the [**MpErrorMessageFormat**](mperrormessageformat.md) function to get a generic description of the error message.</span></span>

## <a name="requirements"></a><span data-ttu-id="391e5-185">Requisiti</span><span class="sxs-lookup"><span data-stu-id="391e5-185">Requirements</span></span>



| <span data-ttu-id="391e5-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="391e5-186">Requirement</span></span> | <span data-ttu-id="391e5-187">Valore</span><span class="sxs-lookup"><span data-stu-id="391e5-187">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="391e5-188">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="391e5-188">Minimum supported client</span></span><br/> | <span data-ttu-id="391e5-189">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="391e5-189">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="391e5-190">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="391e5-190">Minimum supported server</span></span><br/> | <span data-ttu-id="391e5-191">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="391e5-191">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="391e5-192">Intestazione</span><span class="sxs-lookup"><span data-stu-id="391e5-192">Header</span></span><br/>                   | <dl> <span data-ttu-id="391e5-193"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="391e5-193"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="391e5-194">DLL</span><span class="sxs-lookup"><span data-stu-id="391e5-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="391e5-195"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="391e5-195"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="391e5-196">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="391e5-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="391e5-197">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="391e5-197">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="391e5-198">**MpHandleClose**</span><span class="sxs-lookup"><span data-stu-id="391e5-198">**MpHandleClose**</span></span>](mphandleclose.md)
</dt> <dt>

[<span data-ttu-id="391e5-199">**MpManagerOpen**</span><span class="sxs-lookup"><span data-stu-id="391e5-199">**MpManagerOpen**</span></span>](mpmanageropen.md)
</dt> <dt>

[<span data-ttu-id="391e5-200">**\_dati MPCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="391e5-200">**MPCALLBACK\_DATA**</span></span>](mpcallback-data.md)
</dt> <dt>

[<span data-ttu-id="391e5-201">**\_dati MPSIGUPDATE**</span><span class="sxs-lookup"><span data-stu-id="391e5-201">**MPSIGUPDATE\_DATA**</span></span>](mpsigupdate-data.md)
</dt> </dl>

 

 





