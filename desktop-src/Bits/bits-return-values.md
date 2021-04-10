---
title: Valori restituiti BITS
description: Il file Bitsmsg. h contiene le costanti del valore restituito seguenti.
ms.assetid: 8df5022a-b161-4558-9d60-efdbdf1754d6
keywords:
- BIT errori
- BIT degli errori, codici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9086de1d55bbdc9695876bd06368ab28dbbb161
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963329"
---
# <a name="bits-return-values"></a><span data-ttu-id="db0e9-105">Valori restituiti BITS</span><span class="sxs-lookup"><span data-stu-id="db0e9-105">BITS Return Values</span></span>

<span data-ttu-id="db0e9-106">Il file Bitsmsg. h contiene le costanti del valore restituito seguenti.</span><span class="sxs-lookup"><span data-stu-id="db0e9-106">The Bitsmsg.h file contains the following return value constants.</span></span> <span data-ttu-id="db0e9-107">Le costanti rappresentano i valori restituiti generati da BITS e i valori restituiti HTTP che BITS acquisisce.</span><span class="sxs-lookup"><span data-stu-id="db0e9-107">The constants represent return values that BITS generates and HTTP return values that BITS captures.</span></span> <span data-ttu-id="db0e9-108">Tutti gli altri valori restituiti che è possibile ricevere sono i valori restituiti di Windows COM, RPC o convertiti (BITS utilizza [HRESULT \_ dalla macro \_ Win32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) per convertire i valori restituiti di Windows in valori HRESULT).</span><span class="sxs-lookup"><span data-stu-id="db0e9-108">All other return values that you can receive are COM, RPC, or converted Windows return values (BITS uses the [HRESULT\_FROM\_WIN32](/windows/win32/api/winerror/nf-winerror-hresult_from_win32) macro to convert the Windows return values to HRESULT values).</span></span>

<span data-ttu-id="db0e9-109">Si noti che il file Bitsmsg. h contiene valori restituiti aggiuntivi non elencati di seguito.</span><span class="sxs-lookup"><span data-stu-id="db0e9-109">Note that the Bitsmsg.h file contains additional return values not listed below.</span></span>

<dl> <dt>

<span data-ttu-id="db0e9-110"><span id="BG_S_PARTIAL_COMPLETE__0x00200017_"></span><span id="bg_s_partial_complete__0x00200017_"></span><span id="BG_S_PARTIAL_COMPLETE__0X00200017_"></span>\_ \_ Completamento parziale di BG \_ (0x00200017)</span><span class="sxs-lookup"><span data-stu-id="db0e9-110"><span id="BG_S_PARTIAL_COMPLETE__0x00200017_"></span><span id="bg_s_partial_complete__0x00200017_"></span><span id="BG_S_PARTIAL_COMPLETE__0X00200017_"></span>BG\_S\_PARTIAL\_COMPLETE (0x00200017)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-111">Un subset dei file del processo è stato trasferito correttamente prima della chiamata al metodo [**Metodo ibackgroundcopyjob:: complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) .</span><span class="sxs-lookup"><span data-stu-id="db0e9-111">A subset of the job's files transferred successfully before the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method was called.</span></span> <span data-ttu-id="db0e9-112">Quelli che non sono stati completati sono stati eliminati.</span><span class="sxs-lookup"><span data-stu-id="db0e9-112">Those that were not complete were deleted.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-113"><span id="BG_S_UNABLE_TO_DELETE_FILES__0x0020001A_"></span><span id="bg_s_unable_to_delete_files__0x0020001a_"></span><span id="BG_S_UNABLE_TO_DELETE_FILES__0X0020001A_"></span>\_Non è \_ possibile \_ \_ eliminare i file in BG \_ (0x0020001A)</span><span class="sxs-lookup"><span data-stu-id="db0e9-113"><span id="BG_S_UNABLE_TO_DELETE_FILES__0x0020001A_"></span><span id="bg_s_unable_to_delete_files__0x0020001a_"></span><span id="BG_S_UNABLE_TO_DELETE_FILES__0X0020001A_"></span>BG\_S\_UNABLE\_TO\_DELETE\_FILES (0x0020001A)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-114">Non è possibile eliminare tutti i file temporanei associati al processo.</span><span class="sxs-lookup"><span data-stu-id="db0e9-114">Unable to delete all temporary files associated with the job.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-115"><span id="BG_S_OVERRIDDEN_BY_POLICY__0x00200055_"></span><span id="bg_s_overridden_by_policy__0x00200055_"></span><span id="BG_S_OVERRIDDEN_BY_POLICY__0X00200055_"></span>BG \_ \_ sottoposto \_ a override dai \_ criteri (0x00200055)</span><span class="sxs-lookup"><span data-stu-id="db0e9-115"><span id="BG_S_OVERRIDDEN_BY_POLICY__0x00200055_"></span><span id="bg_s_overridden_by_policy__0x00200055_"></span><span id="BG_S_OVERRIDDEN_BY_POLICY__0X00200055_"></span>BG\_S\_OVERRIDDEN\_BY\_POLICY (0x00200055)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-116">La preferenza di configurazione è stata salvata correttamente, ma la preferenza non verrà usata perché un'impostazione di Criteri di gruppo configurata sostituisce la preferenza.</span><span class="sxs-lookup"><span data-stu-id="db0e9-116">The configuration preference has been saved successfully, but the preference will not be used because a configured Group Policy setting overrides the preference.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-117"><span id="BG_E_NOT_FOUND__0x80200001_"></span><span id="bg_e_not_found__0x80200001_"></span><span id="BG_E_NOT_FOUND__0X80200001_"></span>BG \_ E \_ non \_ trovato (0x80200001)</span><span class="sxs-lookup"><span data-stu-id="db0e9-117"><span id="BG_E_NOT_FOUND__0x80200001_"></span><span id="bg_e_not_found__0x80200001_"></span><span id="BG_E_NOT_FOUND__0X80200001_"></span>BG\_E\_NOT\_FOUND (0x80200001)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-118">Il processo richiesto non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="db0e9-118">The requested job was not found.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-119"><span id="BG_E_INVALID_STATE__0x80200002_"></span><span id="bg_e_invalid_state__0x80200002_"></span><span id="BG_E_INVALID_STATE__0X80200002_"></span>Stato di BG \_ E \_ non valido \_ (0x80200002)</span><span class="sxs-lookup"><span data-stu-id="db0e9-119"><span id="BG_E_INVALID_STATE__0x80200002_"></span><span id="bg_e_invalid_state__0x80200002_"></span><span id="BG_E_INVALID_STATE__0X80200002_"></span>BG\_E\_INVALID\_STATE (0x80200002)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-120">L'azione richiesta non è consentita nello stato del processo corrente.</span><span class="sxs-lookup"><span data-stu-id="db0e9-120">The requested action is not allowed in the current job state.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-121"><span id="BG_E_EMPTY__0x80200003_"></span><span id="bg_e_empty__0x80200003_"></span><span id="BG_E_EMPTY__0X80200003_"></span>BG \_ E \_ Empty (0x80200003)</span><span class="sxs-lookup"><span data-stu-id="db0e9-121"><span id="BG_E_EMPTY__0x80200003_"></span><span id="bg_e_empty__0x80200003_"></span><span id="BG_E_EMPTY__0X80200003_"></span>BG\_E\_EMPTY (0x80200003)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-122">Prima di poter riprendere il processo, il processo deve contenere uno o più file.</span><span class="sxs-lookup"><span data-stu-id="db0e9-122">The job must contain one or more files before you can resume the job.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-123"><span id="BG_E_FILE_NOT_AVAILABLE__0x80200004_"></span><span id="bg_e_file_not_available__0x80200004_"></span><span id="BG_E_FILE_NOT_AVAILABLE__0X80200004_"></span>Il \_ file BG E \_ \_ non è \_ disponibile (0x80200004)</span><span class="sxs-lookup"><span data-stu-id="db0e9-123"><span id="BG_E_FILE_NOT_AVAILABLE__0x80200004_"></span><span id="bg_e_file_not_available__0x80200004_"></span><span id="BG_E_FILE_NOT_AVAILABLE__0X80200004_"></span>BG\_E\_FILE\_NOT\_AVAILABLE (0x80200004)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-124">Le informazioni sul file non sono disponibili perché l'errore non è associato a un file locale o remoto.</span><span class="sxs-lookup"><span data-stu-id="db0e9-124">File information is not available because the error is not associated with a local or remote file.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-125"><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0x80200005_"></span><span id="bg_e_protocol_not_available__0x80200005_"></span><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0X80200005_"></span>\_Protocollo BG \_ E \_ non \_ disponibile (0x80200005)</span><span class="sxs-lookup"><span data-stu-id="db0e9-125"><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0x80200005_"></span><span id="bg_e_protocol_not_available__0x80200005_"></span><span id="BG_E_PROTOCOL_NOT_AVAILABLE__0X80200005_"></span>BG\_E\_PROTOCOL\_NOT\_AVAILABLE (0x80200005)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-126">Le informazioni sul protocollo non sono disponibili perché l'errore non è associato al protocollo di trasferimento specificato.</span><span class="sxs-lookup"><span data-stu-id="db0e9-126">Protocol information is not available because the error is not associated with the specified transfer protocol.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-127"><span id="BG_E_DESTINATION_LOCKED__0x8020000D_"></span><span id="bg_e_destination_locked__0x8020000d_"></span><span id="BG_E_DESTINATION_LOCKED__0X8020000D_"></span>Destinazione di BG \_ E \_ \_ bloccata (0x8020000D)</span><span class="sxs-lookup"><span data-stu-id="db0e9-127"><span id="BG_E_DESTINATION_LOCKED__0x8020000D_"></span><span id="bg_e_destination_locked__0x8020000d_"></span><span id="BG_E_DESTINATION_LOCKED__0X8020000D_"></span>BG\_E\_DESTINATION\_LOCKED (0x8020000D)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-128">Il volume file system di destinazione, specificato nel nome file locale, è bloccato.</span><span class="sxs-lookup"><span data-stu-id="db0e9-128">The destination file system volume, specified in the local file name, is locked.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-129"><span id="BG_E_VOLUME_CHANGED__0x8020000E_"></span><span id="bg_e_volume_changed__0x8020000e_"></span><span id="BG_E_VOLUME_CHANGED__0X8020000E_"></span>VOLUME di BG \_ E \_ \_ modificato (0x8020000E)</span><span class="sxs-lookup"><span data-stu-id="db0e9-129"><span id="BG_E_VOLUME_CHANGED__0x8020000E_"></span><span id="bg_e_volume_changed__0x8020000e_"></span><span id="BG_E_VOLUME_CHANGED__0X8020000E_"></span>BG\_E\_VOLUME\_CHANGED (0x8020000E)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-130">Il volume di destinazione, specificato nel nome file locale, è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="db0e9-130">The destination volume, specified in the local file name, has changed.</span></span> <span data-ttu-id="db0e9-131">Il disco floppy originale, ad esempio, è stato sostituito da un altro disco floppy.</span><span class="sxs-lookup"><span data-stu-id="db0e9-131">For example, the original floppy disk has been replaced with a different floppy disk.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-132"><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0x8020000F_"></span><span id="bg_e_error_information_unavailable__0x8020000f_"></span><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0X8020000F_"></span>\_Informazioni sugli errori di BG E non \_ \_ \_ disponibili (0x8020000F)</span><span class="sxs-lookup"><span data-stu-id="db0e9-132"><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0x8020000F_"></span><span id="bg_e_error_information_unavailable__0x8020000f_"></span><span id="BG_E_ERROR_INFORMATION_UNAVAILABLE__0X8020000F_"></span>BG\_E\_ERROR\_INFORMATION\_UNAVAILABLE (0x8020000F)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-133">Le informazioni sull'errore sono disponibili solo quando lo stato del processo è \_ \_ errore stato processo BG \_ .</span><span class="sxs-lookup"><span data-stu-id="db0e9-133">Error information is only available when the state of the job is BG\_JOB\_STATE\_ERROR.</span></span> <span data-ttu-id="db0e9-134">Le informazioni sull'errore non sono disponibili dopo che BITS inizia il trasferimento dei dati del processo o il client viene chiuso.</span><span class="sxs-lookup"><span data-stu-id="db0e9-134">The error information is not available after BITS begins transferring the job's data or the client exits.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-135"><span id="BG_E_NETWORK_DISCONNECTED__0x80200010_"></span><span id="bg_e_network_disconnected__0x80200010_"></span><span id="BG_E_NETWORK_DISCONNECTED__0X80200010_"></span>BG \_ E \_ rete \_ disconnessa (0x80200010)</span><span class="sxs-lookup"><span data-stu-id="db0e9-135"><span id="BG_E_NETWORK_DISCONNECTED__0x80200010_"></span><span id="bg_e_network_disconnected__0x80200010_"></span><span id="BG_E_NETWORK_DISCONNECTED__0X80200010_"></span>BG\_E\_NETWORK\_DISCONNECTED (0x80200010)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-136">La scheda di rete è inattiva o disconnessa.</span><span class="sxs-lookup"><span data-stu-id="db0e9-136">The network adapter is inactive or disconnected.</span></span> <span data-ttu-id="db0e9-137">Tutti i processi vengono inseriti nello \_ stato di \_ errore temporaneo di stato del processo BG \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="db0e9-137">All jobs are placed in the BG\_JOB\_STATE\_TRANSIENT\_ERROR state.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-138"><span id="BG_E_MISSING_FILE_SIZE__0x80200011_"></span><span id="bg_e_missing_file_size__0x80200011_"></span><span id="BG_E_MISSING_FILE_SIZE__0X80200011_"></span>\_ \_ Dimensioni file mancanti E BG \_ \_ (0x80200011)</span><span class="sxs-lookup"><span data-stu-id="db0e9-138"><span id="BG_E_MISSING_FILE_SIZE__0x80200011_"></span><span id="bg_e_missing_file_size__0x80200011_"></span><span id="BG_E_MISSING_FILE_SIZE__0X80200011_"></span>BG\_E\_MISSING\_FILE\_SIZE (0x80200011)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-139">Il server non ha restituito le dimensioni del file.</span><span class="sxs-lookup"><span data-stu-id="db0e9-139">The server did not return the file size.</span></span> <span data-ttu-id="db0e9-140">BITS trasferisce solo contenuto statico e richiede che il server HTTP restituisca l'intestazione Content-Length.</span><span class="sxs-lookup"><span data-stu-id="db0e9-140">BITS only transfers static content and requires the HTTP server to return the Content-Length header.</span></span> <span data-ttu-id="db0e9-141">La richiesta di trasferimento ha esito negativo se l'URL punta al contenuto dinamico.</span><span class="sxs-lookup"><span data-stu-id="db0e9-141">The transfer request fails if the URL points to dynamic content.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-142"><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0x80200012_"></span><span id="bg_e_insufficient_http_support__0x80200012_"></span><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0X80200012_"></span>\_ \_ Supporto http BG E insufficiente \_ \_ (0x80200012)</span><span class="sxs-lookup"><span data-stu-id="db0e9-142"><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0x80200012_"></span><span id="bg_e_insufficient_http_support__0x80200012_"></span><span id="BG_E_INSUFFICIENT_HTTP_SUPPORT__0X80200012_"></span>BG\_E\_INSUFFICIENT\_HTTP\_SUPPORT (0x80200012)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-143">Il server non supporta il protocollo HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="db0e9-143">The server does not support the HTTP/1.1 protocol.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-144"><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0x80200013_"></span><span id="bg_e_insufficient_range_support__0x80200013_"></span><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0X80200013_"></span>Supporto per gli intervalli di BG \_ E \_ insufficiente \_ \_ (0x80200013)</span><span class="sxs-lookup"><span data-stu-id="db0e9-144"><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0x80200013_"></span><span id="bg_e_insufficient_range_support__0x80200013_"></span><span id="BG_E_INSUFFICIENT_RANGE_SUPPORT__0X80200013_"></span>BG\_E\_INSUFFICIENT\_RANGE\_SUPPORT (0x80200013)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-145">Il server non supporta l'intestazione Content-Range.</span><span class="sxs-lookup"><span data-stu-id="db0e9-145">The server does not support the Content-Range header.</span></span> <span data-ttu-id="db0e9-146">In genere, questo errore viene visualizzato quando si prova a scaricare il contenuto dinamico.</span><span class="sxs-lookup"><span data-stu-id="db0e9-146">Typically, you receive this error when you try to download dynamic content.</span></span> <span data-ttu-id="db0e9-147">Questo errore può essere visualizzato anche se un proxy intermedio sta rimuovendo l'intestazione Content-Range o Content-Length.</span><span class="sxs-lookup"><span data-stu-id="db0e9-147">You can also receive this error if an intermediate proxy is removing the Content-Range or Content-Length header.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-148"><span id="BG_E_REMOTE_NOT_SUPPORTED__0x80200014_"></span><span id="bg_e_remote_not_supported__0x80200014_"></span><span id="BG_E_REMOTE_NOT_SUPPORTED__0X80200014_"></span>BG \_ E \_ Remote \_ non \_ supportate (0x80200014)</span><span class="sxs-lookup"><span data-stu-id="db0e9-148"><span id="BG_E_REMOTE_NOT_SUPPORTED__0x80200014_"></span><span id="bg_e_remote_not_supported__0x80200014_"></span><span id="BG_E_REMOTE_NOT_SUPPORTED__0X80200014_"></span>BG\_E\_REMOTE\_NOT\_SUPPORTED (0x80200014)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-149">L'uso remoto di BITS non è supportato.</span><span class="sxs-lookup"><span data-stu-id="db0e9-149">Remote use of BITS is not supported.</span></span> <span data-ttu-id="db0e9-150">Per ulteriori informazioni, vedere [utenti e connessioni di rete](users-and-network-connections.md).</span><span class="sxs-lookup"><span data-stu-id="db0e9-150">For more information, see [Users and Network Connections](users-and-network-connections.md).</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-151"><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0x80200015_"></span><span id="bg_e_new_owner_diff_mapping__0x80200015_"></span><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0X80200015_"></span>BG \_ E \_ nuovo \_ \_ mapping diff proprietario \_ (0x80200015)</span><span class="sxs-lookup"><span data-stu-id="db0e9-151"><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0x80200015_"></span><span id="bg_e_new_owner_diff_mapping__0x80200015_"></span><span id="BG_E_NEW_OWNER_DIFF_MAPPING__0X80200015_"></span>BG\_E\_NEW\_OWNER\_DIFF\_MAPPING (0x80200015)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-152">Il mapping delle unità di rete per il file locale è diverso per il proprietario corrente rispetto al proprietario precedente.</span><span class="sxs-lookup"><span data-stu-id="db0e9-152">The network drive mapping for the local file is different for the current owner than for the previous owner.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-153"><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0x80200016_"></span><span id="bg_e_new_owner_no_file_access__0x80200016_"></span><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0X80200016_"></span>BG \_ E \_ New \_ owner \_ nessun \_ \_ accesso ai file (0x80200016)</span><span class="sxs-lookup"><span data-stu-id="db0e9-153"><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0x80200016_"></span><span id="bg_e_new_owner_no_file_access__0x80200016_"></span><span id="BG_E_NEW_OWNER_NO_FILE_ACCESS__0X80200016_"></span>BG\_E\_NEW\_OWNER\_NO\_FILE\_ACCESS (0x80200016)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-154">Le autorizzazioni del nuovo proprietario non sono sufficienti per i file temporanei dei processi.</span><span class="sxs-lookup"><span data-stu-id="db0e9-154">The new owner has insufficient permissions to the temporary job files.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-155"><span id="BG_E_PROXY_LIST_TOO_LARGE__0x80200018_"></span><span id="bg_e_proxy_list_too_large__0x80200018_"></span><span id="BG_E_PROXY_LIST_TOO_LARGE__0X80200018_"></span>\_ \_ Elenco proxy BG \_ E \_ troppo \_ grande (0x80200018)</span><span class="sxs-lookup"><span data-stu-id="db0e9-155"><span id="BG_E_PROXY_LIST_TOO_LARGE__0x80200018_"></span><span id="bg_e_proxy_list_too_large__0x80200018_"></span><span id="BG_E_PROXY_LIST_TOO_LARGE__0X80200018_"></span>BG\_E\_PROXY\_LIST\_TOO\_LARGE (0x80200018)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-156">L'elenco di proxy HTTP è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="db0e9-156">The HTTP proxy list is too long.</span></span> <span data-ttu-id="db0e9-157">L'elenco non deve superare 32 KB.</span><span class="sxs-lookup"><span data-stu-id="db0e9-157">The list must not exceed 32 KB.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-158"><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0x80200019_"></span><span id="bg_e_proxy_bypass_list_too_large__0x80200019_"></span><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0X80200019_"></span>\_Elenco di \_ bypass proxy BG E \_ \_ \_ troppo \_ grande (0x80200019)</span><span class="sxs-lookup"><span data-stu-id="db0e9-158"><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0x80200019_"></span><span id="bg_e_proxy_bypass_list_too_large__0x80200019_"></span><span id="BG_E_PROXY_BYPASS_LIST_TOO_LARGE__0X80200019_"></span>BG\_E\_PROXY\_BYPASS\_LIST\_TOO\_LARGE (0x80200019)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-159">L'elenco di bypass proxy HTTP è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="db0e9-159">The HTTP proxy bypass list is too long.</span></span> <span data-ttu-id="db0e9-160">L'elenco non deve superare 32 KB.</span><span class="sxs-lookup"><span data-stu-id="db0e9-160">The list must not exceed 32 KB.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-161"><span id="BG_E_TOO_MANY_FILES__0x8020001C_"></span><span id="bg_e_too_many_files__0x8020001c_"></span><span id="BG_E_TOO_MANY_FILES__0X8020001C_"></span>BG \_ E \_ troppi \_ \_ file (0x8020001C)</span><span class="sxs-lookup"><span data-stu-id="db0e9-161"><span id="BG_E_TOO_MANY_FILES__0x8020001C_"></span><span id="bg_e_too_many_files__0x8020001c_"></span><span id="BG_E_TOO_MANY_FILES__0X8020001C_"></span>BG\_E\_TOO\_MANY\_FILES (0x8020001C)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-162">Non è possibile aggiungere più di un file a un processo di caricamento.</span><span class="sxs-lookup"><span data-stu-id="db0e9-162">You cannot add more than one file to an upload job.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-163"><span id="BG_E_LOCAL_FILE_CHANGED__0x8020001D_"></span><span id="bg_e_local_file_changed__0x8020001d_"></span><span id="BG_E_LOCAL_FILE_CHANGED__0X8020001D_"></span>\_File locale di BG E \_ \_ \_ modificato (0x8020001D)</span><span class="sxs-lookup"><span data-stu-id="db0e9-163"><span id="BG_E_LOCAL_FILE_CHANGED__0x8020001D_"></span><span id="bg_e_local_file_changed__0x8020001d_"></span><span id="BG_E_LOCAL_FILE_CHANGED__0X8020001D_"></span>BG\_E\_LOCAL\_FILE\_CHANGED (0x8020001D)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-164">Il contenuto del file locale è stato modificato dopo l'inizio del processo di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="db0e9-164">The contents of the local file changed after the transfer process began.</span></span> <span data-ttu-id="db0e9-165">Il contenuto del file locale non può essere modificato dopo l'inizio del processo di trasferimento in un processo di caricamento o caricamento-risposta.</span><span class="sxs-lookup"><span data-stu-id="db0e9-165">The contents of the local file cannot change after the transfer process begins on an upload or upload-reply job.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-166"><span id="BG_E_TOO_LARGE__0x80200020_"></span><span id="bg_e_too_large__0x80200020_"></span><span id="BG_E_TOO_LARGE__0X80200020_"></span>BG \_ E \_ troppo \_ grande (0x80200020)</span><span class="sxs-lookup"><span data-stu-id="db0e9-166"><span id="BG_E_TOO_LARGE__0x80200020_"></span><span id="bg_e_too_large__0x80200020_"></span><span id="BG_E_TOO_LARGE__0X80200020_"></span>BG\_E\_TOO\_LARGE (0x80200020)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-167">Le dimensioni del file di caricamento superano le dimensioni massime di caricamento consentite specificate sul server.</span><span class="sxs-lookup"><span data-stu-id="db0e9-167">The size of the upload file exceeds the maximum allowed upload size specified on the server.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-168"><span id="BG_E_STRING_TOO_LONG__0x80200021_"></span><span id="bg_e_string_too_long__0x80200021_"></span><span id="BG_E_STRING_TOO_LONG__0X80200021_"></span>\_Stringa BG \_ E \_ troppo \_ lungo (0x80200021)</span><span class="sxs-lookup"><span data-stu-id="db0e9-168"><span id="BG_E_STRING_TOO_LONG__0x80200021_"></span><span id="bg_e_string_too_long__0x80200021_"></span><span id="BG_E_STRING_TOO_LONG__0X80200021_"></span>BG\_E\_STRING\_TOO\_LONG (0x80200021)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-169">La stringa specificata è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="db0e9-169">The specified string is too long.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-170"><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0x80200022_"></span><span id="bg_e_client_server_protocol_mismatch__0x80200022_"></span><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0X80200022_"></span>\_ \_ \_ Mancata corrispondenza del protocollo server client E BG \_ \_ (0x80200022)</span><span class="sxs-lookup"><span data-stu-id="db0e9-170"><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0x80200022_"></span><span id="bg_e_client_server_protocol_mismatch__0x80200022_"></span><span id="BG_E_CLIENT_SERVER_PROTOCOL_MISMATCH__0X80200022_"></span>BG\_E\_CLIENT\_SERVER\_PROTOCOL\_MISMATCH (0x80200022)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-171">Il client e il server non sono riusciti a negoziare un protocollo da usare per il processo di caricamento.</span><span class="sxs-lookup"><span data-stu-id="db0e9-171">The client and server were unable to negotiate a protocol to use for the upload job.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-172"><span id="BG_E_SERVER_EXECUTE_ENABLED__0x80200023_"></span><span id="bg_e_server_execute_enabled__0x80200023_"></span><span id="BG_E_SERVER_EXECUTE_ENABLED__0X80200023_"></span>\_Esecuzione del server BG E \_ \_ \_ abilitata (0x80200023)</span><span class="sxs-lookup"><span data-stu-id="db0e9-172"><span id="BG_E_SERVER_EXECUTE_ENABLED__0x80200023_"></span><span id="bg_e_server_execute_enabled__0x80200023_"></span><span id="BG_E_SERVER_EXECUTE_ENABLED__0X80200023_"></span>BG\_E\_SERVER\_EXECUTE\_ENABLED (0x80200023)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-173">Le autorizzazioni di scripting o di esecuzione sono abilitate nella directory virtuale IIS associata al processo.</span><span class="sxs-lookup"><span data-stu-id="db0e9-173">Scripting or execute permissions are enabled on the IIS virtual directory associated with the job.</span></span> <span data-ttu-id="db0e9-174">Per caricare i file nella directory virtuale, disabilitare le autorizzazioni di scripting ed esecuzione per la directory virtuale.</span><span class="sxs-lookup"><span data-stu-id="db0e9-174">To upload files to the virtual directory, disable the scripting and execute permissions on the virtual directory.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-175"><span id="BG_E_USERNAME_TOO_LARGE__0x80200025_"></span><span id="bg_e_username_too_large__0x80200025_"></span><span id="BG_E_USERNAME_TOO_LARGE__0X80200025_"></span>BG \_ E \_ nome utente \_ troppo \_ grande (0x80200025)</span><span class="sxs-lookup"><span data-stu-id="db0e9-175"><span id="BG_E_USERNAME_TOO_LARGE__0x80200025_"></span><span id="bg_e_username_too_large__0x80200025_"></span><span id="BG_E_USERNAME_TOO_LARGE__0X80200025_"></span>BG\_E\_USERNAME\_TOO\_LARGE (0x80200025)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-176">Il nome utente non può superare i 300 caratteri.</span><span class="sxs-lookup"><span data-stu-id="db0e9-176">The user name cannot exceed 300 characters.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-177"><span id="BG_E_PASSWORD_TOO_LARGE__0x80200026_"></span><span id="bg_e_password_too_large__0x80200026_"></span><span id="BG_E_PASSWORD_TOO_LARGE__0X80200026_"></span>\_Password BG \_ E \_ troppo \_ grande (0x80200026)</span><span class="sxs-lookup"><span data-stu-id="db0e9-177"><span id="BG_E_PASSWORD_TOO_LARGE__0x80200026_"></span><span id="bg_e_password_too_large__0x80200026_"></span><span id="BG_E_PASSWORD_TOO_LARGE__0X80200026_"></span>BG\_E\_PASSWORD\_TOO\_LARGE (0x80200026)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-178">La password non può superare i 65535 caratteri.</span><span class="sxs-lookup"><span data-stu-id="db0e9-178">The password cannot exceed 65535 characters.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-179"><span id="BG_E_INVALID_AUTH_TARGET__0x80200027_"></span><span id="bg_e_invalid_auth_target__0x80200027_"></span><span id="BG_E_INVALID_AUTH_TARGET__0X80200027_"></span>\_Destinazione di autenticazione BG E \_ non valida \_ \_ (0x80200027)</span><span class="sxs-lookup"><span data-stu-id="db0e9-179"><span id="BG_E_INVALID_AUTH_TARGET__0x80200027_"></span><span id="bg_e_invalid_auth_target__0x80200027_"></span><span id="BG_E_INVALID_AUTH_TARGET__0X80200027_"></span>BG\_E\_INVALID\_AUTH\_TARGET (0x80200027)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-180">La destinazione di autenticazione specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="db0e9-180">The specified authentication target is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-181"><span id="BG_E_INVALID_AUTH_SCHEME__0x80200028_"></span><span id="bg_e_invalid_auth_scheme__0x80200028_"></span><span id="BG_E_INVALID_AUTH_SCHEME__0X80200028_"></span>\_Schema di autenticazione BG E \_ non valido \_ \_ (0x80200028)</span><span class="sxs-lookup"><span data-stu-id="db0e9-181"><span id="BG_E_INVALID_AUTH_SCHEME__0x80200028_"></span><span id="bg_e_invalid_auth_scheme__0x80200028_"></span><span id="BG_E_INVALID_AUTH_SCHEME__0X80200028_"></span>BG\_E\_INVALID\_AUTH\_SCHEME (0x80200028)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-182">Lo schema di autenticazione specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="db0e9-182">The specified authentication scheme is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-183"><span id="BG_E_INVALID_RANGE__0x8020002B_"></span><span id="bg_e_invalid_range__0x8020002b_"></span><span id="BG_E_INVALID_RANGE__0X8020002B_"></span>\_Intervallo BG E \_ non valido \_ (0x8020002B)</span><span class="sxs-lookup"><span data-stu-id="db0e9-183"><span id="BG_E_INVALID_RANGE__0x8020002B_"></span><span id="bg_e_invalid_range__0x8020002b_"></span><span id="BG_E_INVALID_RANGE__0X8020002B_"></span>BG\_E\_INVALID\_RANGE (0x8020002B)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-184">L'intervallo di byte specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="db0e9-184">The specified byte range is invalid.</span></span> <span data-ttu-id="db0e9-185">L'intervallo di byte deve esistere all'interno del file remoto specificato.</span><span class="sxs-lookup"><span data-stu-id="db0e9-185">The byte range must exist within the specified remote file.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-186"><span id="BG_E_OVERLAPPING_RANGES__0x8020002C_"></span><span id="bg_e_overlapping_ranges__0x8020002c_"></span><span id="BG_E_OVERLAPPING_RANGES__0X8020002C_"></span>Intervalli di BG \_ E \_ sovrapposti \_ (0x8020002C)</span><span class="sxs-lookup"><span data-stu-id="db0e9-186"><span id="BG_E_OVERLAPPING_RANGES__0x8020002C_"></span><span id="bg_e_overlapping_ranges__0x8020002c_"></span><span id="BG_E_OVERLAPPING_RANGES__0X8020002C_"></span>BG\_E\_OVERLAPPING\_RANGES (0x8020002C)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-187">L'elenco di intervalli di byte contiene intervalli sovrapposti o duplicati, che non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="db0e9-187">The list of byte ranges contains overlapping or duplicate ranges, which are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-188"><span id="BG_E_BLOCKED_BY_POLICY__0x8020003E_"></span><span id="bg_e_blocked_by_policy__0x8020003e_"></span><span id="BG_E_BLOCKED_BY_POLICY__0X8020003E_"></span>BG \_ E \_ bloccato \_ dal \_ criterio (0x8020003E)</span><span class="sxs-lookup"><span data-stu-id="db0e9-188"><span id="BG_E_BLOCKED_BY_POLICY__0x8020003E_"></span><span id="bg_e_blocked_by_policy__0x8020003e_"></span><span id="BG_E_BLOCKED_BY_POLICY__0X8020003E_"></span>BG\_E\_BLOCKED\_BY\_POLICY (0x8020003E)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-189">Le impostazioni Criteri di gruppo impediscono l'esecuzione dei processi in background in questo momento.</span><span class="sxs-lookup"><span data-stu-id="db0e9-189">Group Policy settings prevent background jobs from running at this time.</span></span> <span data-ttu-id="db0e9-190">Per informazioni dettagliate, vedere il criterio [MaxInternetBandwidth](group-policies.md) .</span><span class="sxs-lookup"><span data-stu-id="db0e9-190">For details, see the [MaxInternetBandwidth](group-policies.md) policy.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-191"><span id="BG_E_INVALID_PROXY_INFO__0x8020003F_"></span><span id="bg_e_invalid_proxy_info__0x8020003f_"></span><span id="BG_E_INVALID_PROXY_INFO__0X8020003F_"></span>\_Informazioni sul proxy BG E \_ non valide \_ \_ (0x8020003F)</span><span class="sxs-lookup"><span data-stu-id="db0e9-191"><span id="BG_E_INVALID_PROXY_INFO__0x8020003F_"></span><span id="bg_e_invalid_proxy_info__0x8020003f_"></span><span id="BG_E_INVALID_PROXY_INFO__0X8020003F_"></span>BG\_E\_INVALID\_PROXY\_INFO (0x8020003F)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-192">Errore di run-time che indica che l'elenco proxy o l'elenco di bypass proxy specificato utilizzando il metodo [**Metodo ibackgroundcopyjob:: SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) non è valido.</span><span class="sxs-lookup"><span data-stu-id="db0e9-192">Run-time error that indicates the proxy list or proxy bypass list that you specified using the [**IBackgroundCopyJob::SetProxySettings**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-setproxysettings) method is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-193"><span id="BG_E_INVALID_CREDENTIALS__0x80200040_"></span><span id="bg_e_invalid_credentials__0x80200040_"></span><span id="BG_E_INVALID_CREDENTIALS__0X80200040_"></span>\_Credenziali BG E \_ non valide \_ (0x80200040)</span><span class="sxs-lookup"><span data-stu-id="db0e9-193"><span id="BG_E_INVALID_CREDENTIALS__0x80200040_"></span><span id="bg_e_invalid_credentials__0x80200040_"></span><span id="BG_E_INVALID_CREDENTIALS__0X80200040_"></span>BG\_E\_INVALID\_CREDENTIALS (0x80200040)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-194">Il formato delle credenziali di sicurezza specificate non è valido.</span><span class="sxs-lookup"><span data-stu-id="db0e9-194">The format of the supplied security credentials is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-195"><span id="BG_E_RECORD_DELETED__0x80200042_"></span><span id="bg_e_record_deleted__0x80200042_"></span><span id="BG_E_RECORD_DELETED__0X80200042_"></span>\_Record BG \_ E \_ eliminato (0x80200042)</span><span class="sxs-lookup"><span data-stu-id="db0e9-195"><span id="BG_E_RECORD_DELETED__0x80200042_"></span><span id="bg_e_record_deleted__0x80200042_"></span><span id="BG_E_RECORD_DELETED__0X80200042_"></span>BG\_E\_RECORD\_DELETED (0x80200042)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-196">Il record della cache è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="db0e9-196">The cache record has been deleted.</span></span> <span data-ttu-id="db0e9-197">Il tentativo di aggiornamento è stato abbandonato.</span><span class="sxs-lookup"><span data-stu-id="db0e9-197">The attempt to update it has been abandoned.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-198"><span id="BG_E_UPNP_ERROR__0x80200045_"></span><span id="bg_e_upnp_error__0x80200045_"></span><span id="BG_E_UPNP_ERROR__0X80200045_"></span>\_ \_ Errore UPnP E BG \_ (0x80200045)</span><span class="sxs-lookup"><span data-stu-id="db0e9-198"><span id="BG_E_UPNP_ERROR__0x80200045_"></span><span id="bg_e_upnp_error__0x80200045_"></span><span id="BG_E_UPNP_ERROR__0X80200045_"></span>BG\_E\_UPNP\_ERROR (0x80200045)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-199">Si è verificato un errore di Plug and Play universale (UPnP).</span><span class="sxs-lookup"><span data-stu-id="db0e9-199">A Universal Plug and Play (UPnP) error has occurred.</span></span> <span data-ttu-id="db0e9-200">Verificare il dispositivo gateway Internet.</span><span class="sxs-lookup"><span data-stu-id="db0e9-200">Please check your Internet Gateway Device.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-201"><span id="BG_E_PEERCACHING_DISABLED__0x80200047_"></span><span id="bg_e_peercaching_disabled__0x80200047_"></span><span id="BG_E_PEERCACHING_DISABLED__0X80200047_"></span>BG \_ E \_ peer caching \_ disabilitato (0x80200047)</span><span class="sxs-lookup"><span data-stu-id="db0e9-201"><span id="BG_E_PEERCACHING_DISABLED__0x80200047_"></span><span id="bg_e_peercaching_disabled__0x80200047_"></span><span id="BG_E_PEERCACHING_DISABLED__0X80200047_"></span>BG\_E\_PEERCACHING\_DISABLED (0x80200047)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-202">La memorizzazione nella cache peer è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="db0e9-202">Peer-caching is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-203"><span id="BG_E_BUSYCACHERECORD__0x80200048_"></span><span id="bg_e_busycacherecord__0x80200048_"></span><span id="BG_E_BUSYCACHERECORD__0X80200048_"></span>BG \_ E \_ BUSYCACHERECORD (0x80200048)</span><span class="sxs-lookup"><span data-stu-id="db0e9-203"><span id="BG_E_BUSYCACHERECORD__0x80200048_"></span><span id="bg_e_busycacherecord__0x80200048_"></span><span id="BG_E_BUSYCACHERECORD__0X80200048_"></span>BG\_E\_BUSYCACHERECORD (0x80200048)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-204">Il record della cache è in uso e non può essere modificato o eliminato.</span><span class="sxs-lookup"><span data-stu-id="db0e9-204">The cache record is in use and cannot be changed or deleted.</span></span> <span data-ttu-id="db0e9-205">Riprovare tra qualche secondo.</span><span class="sxs-lookup"><span data-stu-id="db0e9-205">Try again after a few seconds.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-206"><span id="BG_E_TOO_MANY_JOBS_PER_USER__0x80200049_"></span><span id="bg_e_too_many_jobs_per_user__0x80200049_"></span><span id="BG_E_TOO_MANY_JOBS_PER_USER__0X80200049_"></span>BG \_ E \_ troppi \_ \_ processi \_ per \_ utente (0x80200049)</span><span class="sxs-lookup"><span data-stu-id="db0e9-206"><span id="BG_E_TOO_MANY_JOBS_PER_USER__0x80200049_"></span><span id="bg_e_too_many_jobs_per_user__0x80200049_"></span><span id="BG_E_TOO_MANY_JOBS_PER_USER__0X80200049_"></span>BG\_E\_TOO\_MANY\_JOBS\_PER\_USER (0x80200049)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-207">Il numero di processi per l'utente ha superato il limite di processi per utente impostato dall'impostazione del Criteri di gruppo MaxJobsPerUser.</span><span class="sxs-lookup"><span data-stu-id="db0e9-207">The job count for the user has exceeded the per user job limit set by the MaxJobsPerUser Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-208"><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0x80200050_"></span><span id="bg_e_too_many_jobs_per_machine__0x80200050_"></span><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0X80200050_"></span>BG \_ E \_ troppi \_ \_ processi \_ per \_ computer (0x80200050)</span><span class="sxs-lookup"><span data-stu-id="db0e9-208"><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0x80200050_"></span><span id="bg_e_too_many_jobs_per_machine__0x80200050_"></span><span id="BG_E_TOO_MANY_JOBS_PER_MACHINE__0X80200050_"></span>BG\_E\_TOO\_MANY\_JOBS\_PER\_MACHINE (0x80200050)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-209">Il numero di processi per il computer ha superato il limite di processi per computer impostato dall'impostazione del Criteri di gruppo MaxJobsPerMachine.</span><span class="sxs-lookup"><span data-stu-id="db0e9-209">The job count for the computer has exceeded the per computer job limit set by the MaxJobsPerMachine Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-210"><span id="BG_E_TOO_MANY_FILES_IN_JOB__0x80200051_"></span><span id="bg_e_too_many_files_in_job__0x80200051_"></span><span id="BG_E_TOO_MANY_FILES_IN_JOB__0X80200051_"></span>BG \_ E \_ troppi \_ \_ file \_ nel \_ processo (0x80200051)</span><span class="sxs-lookup"><span data-stu-id="db0e9-210"><span id="BG_E_TOO_MANY_FILES_IN_JOB__0x80200051_"></span><span id="bg_e_too_many_files_in_job__0x80200051_"></span><span id="BG_E_TOO_MANY_FILES_IN_JOB__0X80200051_"></span>BG\_E\_TOO\_MANY\_FILES\_IN\_JOB (0x80200051)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-211">Il numero di file per il processo ha superato il limite di file per processo impostato dall'impostazione del Criteri di gruppo MaxFilesPerJob.</span><span class="sxs-lookup"><span data-stu-id="db0e9-211">The file count for the job has exceeded the per job file limit set by the MaxFilesPerJob Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-212"><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0x80200052_"></span><span id="bg_e_too_many_ranges_in_file__0x80200052_"></span><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0X80200052_"></span>BG \_ E \_ un \_ numero \_ eccessivo \_ di intervalli nel \_ file (0x80200052)</span><span class="sxs-lookup"><span data-stu-id="db0e9-212"><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0x80200052_"></span><span id="bg_e_too_many_ranges_in_file__0x80200052_"></span><span id="BG_E_TOO_MANY_RANGES_IN_FILE__0X80200052_"></span>BG\_E\_TOO\_MANY\_RANGES\_IN\_FILE (0x80200052)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-213">Il numero di intervalli per il file ha superato il limite di intervallo per file impostato dall'impostazione del Criteri di gruppo MaxRangesPerFile.</span><span class="sxs-lookup"><span data-stu-id="db0e9-213">The range count for the file has exceeded the per file range limit set by the MaxRangesPerFile Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-214"><span id="BG_E_VALIDATION_FAILED__0x80200053_"></span><span id="bg_e_validation_failed__0x80200053_"></span><span id="BG_E_VALIDATION_FAILED__0X80200053_"></span>Convalida di BG \_ E \_ \_ non riuscita (0x80200053)</span><span class="sxs-lookup"><span data-stu-id="db0e9-214"><span id="BG_E_VALIDATION_FAILED__0x80200053_"></span><span id="bg_e_validation_failed__0x80200053_"></span><span id="BG_E_VALIDATION_FAILED__0X80200053_"></span>BG\_E\_VALIDATION\_FAILED (0x80200053)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-215">L'applicazione ha richiesto i dati da un sito Web, ma la risposta non è valida.</span><span class="sxs-lookup"><span data-stu-id="db0e9-215">The application requested data from a website, but the response was not valid.</span></span> <span data-ttu-id="db0e9-216">Per informazioni dettagliate, usare Visualizzatore eventi per visualizzare i registri applicazioni \\ Microsoft \\ Windows \\ BITS-client \\ Operational log.</span><span class="sxs-lookup"><span data-stu-id="db0e9-216">For details, use Event Viewer to view the Application Logs\\Microsoft\\Windows\\Bits-client\\Operational log.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-217"><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0x80200054_"></span><span id="bg_e_maxdownload_timeout__0x80200054_"></span><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0X80200054_"></span>TIMEOUT di BG \_ E \_ MAXDOWNLOAD \_ (0x80200054)</span><span class="sxs-lookup"><span data-stu-id="db0e9-217"><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0x80200054_"></span><span id="bg_e_maxdownload_timeout__0x80200054_"></span><span id="BG_E_MAXDOWNLOAD_TIMEOUT__0X80200054_"></span>BG\_E\_MAXDOWNLOAD\_TIMEOUT (0x80200054)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-218">Timeout dei bit durante il download del processo.</span><span class="sxs-lookup"><span data-stu-id="db0e9-218">BITS timed out downloading the job.</span></span> <span data-ttu-id="db0e9-219">Il download non è stato completato entro il tempo di download massimo impostato nel processo o nell'impostazione Criteri di gruppo MaxDownloadTime.</span><span class="sxs-lookup"><span data-stu-id="db0e9-219">The download did not complete within the maximum download time set on the job or the MaxDownloadTime Group Policy setting.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-220"><span id="BG_E_HTTP_ERROR_400__0x80190190_"></span><span id="bg_e_http_error_400__0x80190190_"></span><span id="BG_E_HTTP_ERROR_400__0X80190190_"></span>\_Errore HTTP di BG E \_ \_ \_ 400 (0x80190190)</span><span class="sxs-lookup"><span data-stu-id="db0e9-220"><span id="BG_E_HTTP_ERROR_400__0x80190190_"></span><span id="bg_e_http_error_400__0x80190190_"></span><span id="BG_E_HTTP_ERROR_400__0X80190190_"></span>BG\_E\_HTTP\_ERROR\_400 (0x80190190)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-221">Il server non è riuscito a elaborare la richiesta di trasferimento perché la sintassi del nome file remoto non è valida.</span><span class="sxs-lookup"><span data-stu-id="db0e9-221">The server could not process the transfer request because the syntax of the remote file name is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-222"><span id="BG_E_HTTP_ERROR_401__0x80190191_"></span><span id="bg_e_http_error_401__0x80190191_"></span><span id="BG_E_HTTP_ERROR_401__0X80190191_"></span>\_Errore HTTP di BG E \_ \_ \_ 401 (0x80190191)</span><span class="sxs-lookup"><span data-stu-id="db0e9-222"><span id="BG_E_HTTP_ERROR_401__0x80190191_"></span><span id="bg_e_http_error_401__0x80190191_"></span><span id="BG_E_HTTP_ERROR_401__0X80190191_"></span>BG\_E\_HTTP\_ERROR\_401 (0x80190191)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-223">L'utente non dispone delle autorizzazioni necessarie per accedere al file remoto.</span><span class="sxs-lookup"><span data-stu-id="db0e9-223">The user does not have permission to access the remote file.</span></span> <span data-ttu-id="db0e9-224">La risorsa richiesta prevede l'autenticazione degli utenti.</span><span class="sxs-lookup"><span data-stu-id="db0e9-224">The requested resource requires user authentication.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-225"><span id="BG_E_HTTP_ERROR_404__0x80190194_"></span><span id="bg_e_http_error_404__0x80190194_"></span><span id="BG_E_HTTP_ERROR_404__0X80190194_"></span>\_Errore HTTP di BG E \_ \_ \_ 404 (0x80190194)</span><span class="sxs-lookup"><span data-stu-id="db0e9-225"><span id="BG_E_HTTP_ERROR_404__0x80190194_"></span><span id="bg_e_http_error_404__0x80190194_"></span><span id="BG_E_HTTP_ERROR_404__0X80190194_"></span>BG\_E\_HTTP\_ERROR\_404 (0x80190194)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-226">L'URL richiesto non esiste nel server.</span><span class="sxs-lookup"><span data-stu-id="db0e9-226">The requested URL does not exist on the server.</span></span>

<span data-ttu-id="db0e9-227">In IIS 7, questo errore può indicare</span><span class="sxs-lookup"><span data-stu-id="db0e9-227">In IIS 7, this error can indicate</span></span>

-   <span data-ttu-id="db0e9-228">I caricamenti BITS non sono abilitati nella directory virtuale (VDIR) nel server.</span><span class="sxs-lookup"><span data-stu-id="db0e9-228">That BITS uploads are not enabled on the virtual directory (vdir) on the server.</span></span>
-   <span data-ttu-id="db0e9-229">Che le dimensioni del caricamento superino il limite massimo di caricamento (per informazioni dettagliate, vedere la proprietà dell'estensione IIS [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) ).</span><span class="sxs-lookup"><span data-stu-id="db0e9-229">That the upload size exceeds the maximum upload limit (for details, see the [**BITSMaximumUploadSize**](bits-iis-extension-properties.md) IIS extension property).</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-230"><span id="BG_E_HTTP_ERROR_407__0x80190197_"></span><span id="bg_e_http_error_407__0x80190197_"></span><span id="BG_E_HTTP_ERROR_407__0X80190197_"></span>\_Errore HTTP di BG E \_ \_ \_ 407 (0x80190197)</span><span class="sxs-lookup"><span data-stu-id="db0e9-230"><span id="BG_E_HTTP_ERROR_407__0x80190197_"></span><span id="bg_e_http_error_407__0x80190197_"></span><span id="BG_E_HTTP_ERROR_407__0X80190197_"></span>BG\_E\_HTTP\_ERROR\_407 (0x80190197)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-231">L'utente non dispone delle autorizzazioni necessarie per accedere al proxy.</span><span class="sxs-lookup"><span data-stu-id="db0e9-231">The user does not have permission to access the proxy.</span></span> <span data-ttu-id="db0e9-232">Il proxy richiede l'autenticazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="db0e9-232">The proxy requires user authentication.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-233"><span id="BG_E_HTTP_ERROR_414__0x8019019E_"></span><span id="bg_e_http_error_414__0x8019019e_"></span><span id="BG_E_HTTP_ERROR_414__0X8019019E_"></span>\_Errore HTTP di BG E \_ \_ \_ 414 (0x8019019E)</span><span class="sxs-lookup"><span data-stu-id="db0e9-233"><span id="BG_E_HTTP_ERROR_414__0x8019019E_"></span><span id="bg_e_http_error_414__0x8019019e_"></span><span id="BG_E_HTTP_ERROR_414__0X8019019E_"></span>BG\_E\_HTTP\_ERROR\_414 (0x8019019E)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-234">Il server non è in grado di elaborare la richiesta di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="db0e9-234">The server cannot process the transfer request.</span></span> <span data-ttu-id="db0e9-235">Il Uniform Resource Identifier (URI) nel nome file remoto è più lungo di quello che il server è in grado di interpretare.</span><span class="sxs-lookup"><span data-stu-id="db0e9-235">The Uniform Resource Identifier (URI) in the remote file name is longer than the server can interpret.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-236"><span id="BG_E_HTTP_ERROR_501__0x801901F5_"></span><span id="bg_e_http_error_501__0x801901f5_"></span><span id="BG_E_HTTP_ERROR_501__0X801901F5_"></span>\_Errore HTTP di BG E \_ \_ \_ 501 (0x801901F5)</span><span class="sxs-lookup"><span data-stu-id="db0e9-236"><span id="BG_E_HTTP_ERROR_501__0x801901F5_"></span><span id="bg_e_http_error_501__0x801901f5_"></span><span id="BG_E_HTTP_ERROR_501__0X801901F5_"></span>BG\_E\_HTTP\_ERROR\_501 (0x801901F5)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-237">Il server non supporta la funzionalità necessaria per soddisfare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="db0e9-237">The server does not support the functionality required to fulfill the request.</span></span> <span data-ttu-id="db0e9-238">In IIS 6 questo errore indica che i caricamenti BITS non sono abilitati nella directory virtuale (VDIR) nel server.</span><span class="sxs-lookup"><span data-stu-id="db0e9-238">In IIS 6, this error indicates that BITS uploads are not enabled on the virtual directory (vdir) on the server.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-239"><span id="BG_E_HTTP_ERROR_503__0x801901F7_"></span><span id="bg_e_http_error_503__0x801901f7_"></span><span id="BG_E_HTTP_ERROR_503__0X801901F7_"></span>\_Errore HTTP di BG E \_ \_ \_ 503 (0x801901F7)</span><span class="sxs-lookup"><span data-stu-id="db0e9-239"><span id="BG_E_HTTP_ERROR_503__0x801901F7_"></span><span id="bg_e_http_error_503__0x801901f7_"></span><span id="BG_E_HTTP_ERROR_503__0X801901F7_"></span>BG\_E\_HTTP\_ERROR\_503 (0x801901F7)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-240">Il servizio è temporaneamente sovraccarico e non può elaborare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="db0e9-240">The service is temporarily overloaded and cannot process the request.</span></span> <span data-ttu-id="db0e9-241">Riprendere il processo in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="db0e9-241">Resume the job at a later time.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-242"><span id="BG_E_HTTP_ERROR_504__0x801901F8_"></span><span id="bg_e_http_error_504__0x801901f8_"></span><span id="BG_E_HTTP_ERROR_504__0X801901F8_"></span>\_Errore HTTP di BG E \_ \_ \_ 504 (0x801901F8)</span><span class="sxs-lookup"><span data-stu-id="db0e9-242"><span id="BG_E_HTTP_ERROR_504__0x801901F8_"></span><span id="bg_e_http_error_504__0x801901f8_"></span><span id="BG_E_HTTP_ERROR_504__0X801901F8_"></span>BG\_E\_HTTP\_ERROR\_504 (0x801901F8)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-243">Timeout della richiesta di trasferimento durante l'attesa di un gateway.</span><span class="sxs-lookup"><span data-stu-id="db0e9-243">The transfer request timed out while waiting for a gateway.</span></span> <span data-ttu-id="db0e9-244">Riprendere il processo in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="db0e9-244">Resume the job at a later time.</span></span>

</dd> <dt>

<span data-ttu-id="db0e9-245"><span id="BG_E_HTTP_ERROR_505__0x801901F9_"></span><span id="bg_e_http_error_505__0x801901f9_"></span><span id="BG_E_HTTP_ERROR_505__0X801901F9_"></span>\_Errore HTTP di BG E \_ \_ \_ 505 (0x801901F9)</span><span class="sxs-lookup"><span data-stu-id="db0e9-245"><span id="BG_E_HTTP_ERROR_505__0x801901F9_"></span><span id="bg_e_http_error_505__0x801901f9_"></span><span id="BG_E_HTTP_ERROR_505__0X801901F9_"></span>BG\_E\_HTTP\_ERROR\_505 (0x801901F9)</span></span>
</dt> <dd>

<span data-ttu-id="db0e9-246">Il server non supporta la versione del protocollo HTTP specificata nel nome file remoto.</span><span class="sxs-lookup"><span data-stu-id="db0e9-246">The server does not support the HTTP protocol version specified in the remote file name.</span></span>

</dd> </dl>

<span data-ttu-id="db0e9-247">Il file di intestazione Bitsmsg. h contiene valori restituiti HTTP aggiuntivi non elencati sopra che BITS usa internamente.</span><span class="sxs-lookup"><span data-stu-id="db0e9-247">The Bitsmsg.h header file contains additional HTTP return values not listed above that BITS uses internally.</span></span> <span data-ttu-id="db0e9-248">Per informazioni su questi e altri valori restituiti HTTP che è possibile ricevere, vedere la specifica RFC 2616 da Internet Engineering Task Force all'indirizzo [https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html\#sec10](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10) .</span><span class="sxs-lookup"><span data-stu-id="db0e9-248">For information on these and other HTTP return values you can receive, see the RFC 2616 specification from the Internet Engineering Task Force at [https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html\#sec10](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html#sec10).</span></span>

 

 