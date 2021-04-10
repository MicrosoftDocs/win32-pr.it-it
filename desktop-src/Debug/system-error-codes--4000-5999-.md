---
description: Descrive i codici di errore 4000-5999 definiti nel file di intestazione WinError. h ed è destinato agli sviluppatori.
ms.assetid: 1d2f7160-6322-4c75-abbc-4a882bbdf7ce
title: Codici di errore di sistema (4000-5999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: bfd39042489f2a92ff2eb13df92a22e392c5405e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126891"
---
# <a name="system-error-codes-4000-5999"></a><span data-ttu-id="0a486-103">Codici di errore di sistema (4000-5999)</span><span class="sxs-lookup"><span data-stu-id="0a486-103">System Error Codes (4000-5999)</span></span>

> [!NOTE]
> <span data-ttu-id="0a486-104">Queste informazioni sono destinate agli sviluppatori che effettuano il debug degli errori di sistema.</span><span class="sxs-lookup"><span data-stu-id="0a486-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="0a486-105">Per altri errori, ad esempio problemi con Windows Update, è disponibile un elenco di risorse nella pagina [codici di errore](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="0a486-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="0a486-106">Nell'elenco seguente vengono descritti i [codici di errore di sistema](system-error-codes.md) per gli errori da 4000 a 5999.</span><span class="sxs-lookup"><span data-stu-id="0a486-106">The following list describes [system error codes](system-error-codes.md) for errors 4000 to 5999.</span></span> <span data-ttu-id="0a486-107">Vengono restituiti dalla funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="0a486-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="0a486-108">Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la funzione [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il **formato \_ Message from flag \_ di \_ sistema** .</span><span class="sxs-lookup"><span data-stu-id="0a486-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="0a486-109"><span id="ERROR_WINS_INTERNAL"></span><span id="error_wins_internal"></span>**ERRORE \_ \_ interno WINS**</span><span class="sxs-lookup"><span data-stu-id="0a486-109"><span id="ERROR_WINS_INTERNAL"></span><span id="error_wins_internal"></span>**ERROR\_WINS\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-110">4000 (0xFA0)</span><span class="sxs-lookup"><span data-stu-id="0a486-110">4000 (0xFA0)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-111">WINS ha rilevato un errore durante l'elaborazione del comando.</span><span class="sxs-lookup"><span data-stu-id="0a486-111">WINS encountered an error while processing the command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-112"><span id="ERROR_CAN_NOT_DEL_LOCAL_WINS"></span><span id="error_can_not_del_local_wins"></span>**l'errore \_ non può essere il \_ \_ del \_ \_ WINS locale**</span><span class="sxs-lookup"><span data-stu-id="0a486-112"><span id="ERROR_CAN_NOT_DEL_LOCAL_WINS"></span><span id="error_can_not_del_local_wins"></span>**ERROR\_CAN\_NOT\_DEL\_LOCAL\_WINS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-113">4001 (0xFA1)</span><span class="sxs-lookup"><span data-stu-id="0a486-113">4001 (0xFA1)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-114">Non è possibile eliminare la WINS locale.</span><span class="sxs-lookup"><span data-stu-id="0a486-114">The local WINS cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-115"><span id="ERROR_STATIC_INIT"></span><span id="error_static_init"></span>**ERRORE \_ \_ init statico**</span><span class="sxs-lookup"><span data-stu-id="0a486-115"><span id="ERROR_STATIC_INIT"></span><span id="error_static_init"></span>**ERROR\_STATIC\_INIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-116">4002 (0xFA2)</span><span class="sxs-lookup"><span data-stu-id="0a486-116">4002 (0xFA2)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-117">L'importazione dal file non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="0a486-117">The importation from the file failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-118"><span id="ERROR_INC_BACKUP"></span><span id="error_inc_backup"></span>**ERRORE \_ di \_ backup Inc**</span><span class="sxs-lookup"><span data-stu-id="0a486-118"><span id="ERROR_INC_BACKUP"></span><span id="error_inc_backup"></span>**ERROR\_INC\_BACKUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-119">4003 (0xFA3)</span><span class="sxs-lookup"><span data-stu-id="0a486-119">4003 (0xFA3)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-120">Il backup non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="0a486-120">The backup failed.</span></span> <span data-ttu-id="0a486-121">È stato eseguito un backup completo prima?</span><span class="sxs-lookup"><span data-stu-id="0a486-121">Was a full backup done before?</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-122"><span id="ERROR_FULL_BACKUP"></span><span id="error_full_backup"></span>**ERRORE \_ \_ backup completo**</span><span class="sxs-lookup"><span data-stu-id="0a486-122"><span id="ERROR_FULL_BACKUP"></span><span id="error_full_backup"></span>**ERROR\_FULL\_BACKUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-123">4004 (0xFA4)</span><span class="sxs-lookup"><span data-stu-id="0a486-123">4004 (0xFA4)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-124">Il backup non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="0a486-124">The backup failed.</span></span> <span data-ttu-id="0a486-125">Controllare la directory in cui si sta eseguendo il backup del database.</span><span class="sxs-lookup"><span data-stu-id="0a486-125">Check the directory to which you are backing the database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-126"><span id="ERROR_REC_NON_EXISTENT"></span><span id="error_rec_non_existent"></span>**ERRORE \_ REC \_ non \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="0a486-126"><span id="ERROR_REC_NON_EXISTENT"></span><span id="error_rec_non_existent"></span>**ERROR\_REC\_NON\_EXISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-127">4005 (0xFA5)</span><span class="sxs-lookup"><span data-stu-id="0a486-127">4005 (0xFA5)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-128">Il nome non esiste nel database WINS.</span><span class="sxs-lookup"><span data-stu-id="0a486-128">The name does not exist in the WINS database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-129"><span id="ERROR_RPL_NOT_ALLOWED"></span><span id="error_rpl_not_allowed"></span>**ERRORE \_ RPL \_ non \_ consentito**</span><span class="sxs-lookup"><span data-stu-id="0a486-129"><span id="ERROR_RPL_NOT_ALLOWED"></span><span id="error_rpl_not_allowed"></span>**ERROR\_RPL\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-130">4006 (0xFA6)</span><span class="sxs-lookup"><span data-stu-id="0a486-130">4006 (0xFA6)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-131">La replica con un partner non configurato non è consentita.</span><span class="sxs-lookup"><span data-stu-id="0a486-131">Replication with a nonconfigured partner is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-132"><span id="PEERDIST_ERROR_CONTENTINFO_VERSION_UNSUPPORTED"></span><span id="peerdist_error_contentinfo_version_unsupported"></span>**\_errore PEERDIST \_ versione CONTENTINFO non \_ \_ supportata**</span><span class="sxs-lookup"><span data-stu-id="0a486-132"><span id="PEERDIST_ERROR_CONTENTINFO_VERSION_UNSUPPORTED"></span><span id="peerdist_error_contentinfo_version_unsupported"></span>**PEERDIST\_ERROR\_CONTENTINFO\_VERSION\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-133">4050 (0xFD2)</span><span class="sxs-lookup"><span data-stu-id="0a486-133">4050 (0xFD2)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-134">La versione delle informazioni sul contenuto fornite non è supportata.</span><span class="sxs-lookup"><span data-stu-id="0a486-134">The version of the supplied content information is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-135"><span id="PEERDIST_ERROR_CANNOT_PARSE_CONTENTINFO"></span><span id="peerdist_error_cannot_parse_contentinfo"></span>**\_errore PEERDIST \_ non è possibile \_ analizzare \_ CONTENTINFO**</span><span class="sxs-lookup"><span data-stu-id="0a486-135"><span id="PEERDIST_ERROR_CANNOT_PARSE_CONTENTINFO"></span><span id="peerdist_error_cannot_parse_contentinfo"></span>**PEERDIST\_ERROR\_CANNOT\_PARSE\_CONTENTINFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-136">4051 (0xFD3)</span><span class="sxs-lookup"><span data-stu-id="0a486-136">4051 (0xFD3)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-137">Le informazioni sul contenuto fornite non sono valide.</span><span class="sxs-lookup"><span data-stu-id="0a486-137">The supplied content information is malformed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-138"><span id="PEERDIST_ERROR_MISSING_DATA"></span><span id="peerdist_error_missing_data"></span>**\_ \_ mancano i dati nell'errore PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-138"><span id="PEERDIST_ERROR_MISSING_DATA"></span><span id="peerdist_error_missing_data"></span>**PEERDIST\_ERROR\_MISSING\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-139">4052 (0xFD4)</span><span class="sxs-lookup"><span data-stu-id="0a486-139">4052 (0xFD4)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-140">I dati richiesti non sono stati trovati nelle cache locali o peer.</span><span class="sxs-lookup"><span data-stu-id="0a486-140">The requested data cannot be found in local or peer caches.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-141"><span id="PEERDIST_ERROR_NO_MORE"></span><span id="peerdist_error_no_more"></span>**\_errore PEERDIST \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-141"><span id="PEERDIST_ERROR_NO_MORE"></span><span id="peerdist_error_no_more"></span>**PEERDIST\_ERROR\_NO\_MORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-142">4053 (0xFD5)</span><span class="sxs-lookup"><span data-stu-id="0a486-142">4053 (0xFD5)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-143">Nessun altro dato disponibile o richiesto.</span><span class="sxs-lookup"><span data-stu-id="0a486-143">No more data is available or required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-144"><span id="PEERDIST_ERROR_NOT_INITIALIZED"></span><span id="peerdist_error_not_initialized"></span>**\_errore PEERDIST \_ non \_ inizializzato**</span><span class="sxs-lookup"><span data-stu-id="0a486-144"><span id="PEERDIST_ERROR_NOT_INITIALIZED"></span><span id="peerdist_error_not_initialized"></span>**PEERDIST\_ERROR\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-145">4054 (0xFD6)</span><span class="sxs-lookup"><span data-stu-id="0a486-145">4054 (0xFD6)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-146">L'oggetto fornito non è stato inizializzato.</span><span class="sxs-lookup"><span data-stu-id="0a486-146">The supplied object has not been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-147"><span id="PEERDIST_ERROR_ALREADY_INITIALIZED"></span><span id="peerdist_error_already_initialized"></span>**\_errore PEERDIST \_ già \_ inizializzato**</span><span class="sxs-lookup"><span data-stu-id="0a486-147"><span id="PEERDIST_ERROR_ALREADY_INITIALIZED"></span><span id="peerdist_error_already_initialized"></span>**PEERDIST\_ERROR\_ALREADY\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-148">4055 (0xFD7)</span><span class="sxs-lookup"><span data-stu-id="0a486-148">4055 (0xFD7)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-149">L'oggetto fornito è già stato inizializzato.</span><span class="sxs-lookup"><span data-stu-id="0a486-149">The supplied object has already been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-150"><span id="PEERDIST_ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="peerdist_error_shutdown_in_progress"></span>**\_arresto errore \_ PEERDIST \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="0a486-150"><span id="PEERDIST_ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="peerdist_error_shutdown_in_progress"></span>**PEERDIST\_ERROR\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-151">4056 (0xFD8)</span><span class="sxs-lookup"><span data-stu-id="0a486-151">4056 (0xFD8)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-152">È già in corso un'operazione di arresto.</span><span class="sxs-lookup"><span data-stu-id="0a486-152">A shutdown operation is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-153"><span id="PEERDIST_ERROR_INVALIDATED"></span><span id="peerdist_error_invalidated"></span>**\_errore PEERDIST \_ invalidato**</span><span class="sxs-lookup"><span data-stu-id="0a486-153"><span id="PEERDIST_ERROR_INVALIDATED"></span><span id="peerdist_error_invalidated"></span>**PEERDIST\_ERROR\_INVALIDATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-154">4057 (0xFD9)</span><span class="sxs-lookup"><span data-stu-id="0a486-154">4057 (0xFD9)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-155">L'oggetto fornito è già stato invalidato.</span><span class="sxs-lookup"><span data-stu-id="0a486-155">The supplied object has already been invalidated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-156"><span id="PEERDIST_ERROR_ALREADY_EXISTS"></span><span id="peerdist_error_already_exists"></span>**l' \_ errore \_ PEERDIST \_ esiste già**</span><span class="sxs-lookup"><span data-stu-id="0a486-156"><span id="PEERDIST_ERROR_ALREADY_EXISTS"></span><span id="peerdist_error_already_exists"></span>**PEERDIST\_ERROR\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-157">4058 (0xFDA)</span><span class="sxs-lookup"><span data-stu-id="0a486-157">4058 (0xFDA)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-158">Un elemento esiste già e non è stato sostituito.</span><span class="sxs-lookup"><span data-stu-id="0a486-158">An element already exists and was not replaced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-159"><span id="PEERDIST_ERROR_OPERATION_NOTFOUND"></span><span id="peerdist_error_operation_notfound"></span>**\_operazione di errore PEERDIST \_ \_ NotFound**</span><span class="sxs-lookup"><span data-stu-id="0a486-159"><span id="PEERDIST_ERROR_OPERATION_NOTFOUND"></span><span id="peerdist_error_operation_notfound"></span>**PEERDIST\_ERROR\_OPERATION\_NOTFOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-160">4059 (0xFDB)</span><span class="sxs-lookup"><span data-stu-id="0a486-160">4059 (0xFDB)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-161">Non è possibile annullare l'operazione richiesta perché è già stata completata.</span><span class="sxs-lookup"><span data-stu-id="0a486-161">Can not cancel the requested operation as it has already been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-162"><span id="PEERDIST_ERROR_ALREADY_COMPLETED"></span><span id="peerdist_error_already_completed"></span>**\_errore PEERDIST \_ già \_ completato**</span><span class="sxs-lookup"><span data-stu-id="0a486-162"><span id="PEERDIST_ERROR_ALREADY_COMPLETED"></span><span id="peerdist_error_already_completed"></span>**PEERDIST\_ERROR\_ALREADY\_COMPLETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-163">4060 (0xFDC)</span><span class="sxs-lookup"><span data-stu-id="0a486-163">4060 (0xFDC)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-164">Non è possibile eseguire l'operazione variante richiesta perché è già stata eseguita.</span><span class="sxs-lookup"><span data-stu-id="0a486-164">Can not perform the reqested operation because it has already been carried out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-165"><span id="PEERDIST_ERROR_OUT_OF_BOUNDS"></span><span id="peerdist_error_out_of_bounds"></span>**\_errore PEERDIST \_ fuori \_ \_ limite**</span><span class="sxs-lookup"><span data-stu-id="0a486-165"><span id="PEERDIST_ERROR_OUT_OF_BOUNDS"></span><span id="peerdist_error_out_of_bounds"></span>**PEERDIST\_ERROR\_OUT\_OF\_BOUNDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-166">4061 (0xFDD)</span><span class="sxs-lookup"><span data-stu-id="0a486-166">4061 (0xFDD)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-167">Un'operazione ha eseguito l'accesso ai dati oltre i limiti dei dati validi.</span><span class="sxs-lookup"><span data-stu-id="0a486-167">An operation accessed data beyond the bounds of valid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-168"><span id="PEERDIST_ERROR_VERSION_UNSUPPORTED"></span><span id="peerdist_error_version_unsupported"></span>**versione dell'errore PEERDIST non \_ \_ \_ supportata**</span><span class="sxs-lookup"><span data-stu-id="0a486-168"><span id="PEERDIST_ERROR_VERSION_UNSUPPORTED"></span><span id="peerdist_error_version_unsupported"></span>**PEERDIST\_ERROR\_VERSION\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-169">4062 (0xFDE)</span><span class="sxs-lookup"><span data-stu-id="0a486-169">4062 (0xFDE)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-170">La versione richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="0a486-170">The requested version is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-171"><span id="PEERDIST_ERROR_INVALID_CONFIGURATION"></span><span id="peerdist_error_invalid_configuration"></span>**\_configurazione errore PEERDIST \_ non valida \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-171"><span id="PEERDIST_ERROR_INVALID_CONFIGURATION"></span><span id="peerdist_error_invalid_configuration"></span>**PEERDIST\_ERROR\_INVALID\_CONFIGURATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-172">4063 (0xFDF)</span><span class="sxs-lookup"><span data-stu-id="0a486-172">4063 (0xFDF)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-173">Valore di configurazione non valido.</span><span class="sxs-lookup"><span data-stu-id="0a486-173">A configuration value is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-174"><span id="PEERDIST_ERROR_NOT_LICENSED"></span><span id="peerdist_error_not_licensed"></span>**\_errore PEERDIST \_ non \_ concesso in licenza**</span><span class="sxs-lookup"><span data-stu-id="0a486-174"><span id="PEERDIST_ERROR_NOT_LICENSED"></span><span id="peerdist_error_not_licensed"></span>**PEERDIST\_ERROR\_NOT\_LICENSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-175">4064 (0xFE0)</span><span class="sxs-lookup"><span data-stu-id="0a486-175">4064 (0xFE0)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-176">Lo SKU non è concesso in licenza.</span><span class="sxs-lookup"><span data-stu-id="0a486-176">The SKU is not licensed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-177"><span id="PEERDIST_ERROR_SERVICE_UNAVAILABLE"></span><span id="peerdist_error_service_unavailable"></span>**\_servizio errori PEERDIST non \_ \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="0a486-177"><span id="PEERDIST_ERROR_SERVICE_UNAVAILABLE"></span><span id="peerdist_error_service_unavailable"></span>**PEERDIST\_ERROR\_SERVICE\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-178">4065 (0xFE1)</span><span class="sxs-lookup"><span data-stu-id="0a486-178">4065 (0xFE1)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-179">Il servizio PeerDist è ancora in fase di inizializzazione e sarà disponibile a breve.</span><span class="sxs-lookup"><span data-stu-id="0a486-179">PeerDist Service is still initializing and will be available shortly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-180"><span id="PEERDIST_ERROR_TRUST_FAILURE"></span><span id="peerdist_error_trust_failure"></span>**\_errore di \_ ATTENDIBILità PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-180"><span id="PEERDIST_ERROR_TRUST_FAILURE"></span><span id="peerdist_error_trust_failure"></span>**PEERDIST\_ERROR\_TRUST\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-181">4066 (0xFE2)</span><span class="sxs-lookup"><span data-stu-id="0a486-181">4066 (0xFE2)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-182">La comunicazione con uno o più computer verrà temporaneamente bloccata a causa di errori recenti.</span><span class="sxs-lookup"><span data-stu-id="0a486-182">Communication with one or more computers will be temporarily blocked due to recent errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-183"><span id="ERROR_DHCP_ADDRESS_CONFLICT"></span><span id="error_dhcp_address_conflict"></span>**ERRORE \_ in \_ conflitto di indirizzi DHCP \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-183"><span id="ERROR_DHCP_ADDRESS_CONFLICT"></span><span id="error_dhcp_address_conflict"></span>**ERROR\_DHCP\_ADDRESS\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-184">4100 (0x1004)</span><span class="sxs-lookup"><span data-stu-id="0a486-184">4100 (0x1004)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-185">Il client DHCP ha ottenuto un indirizzo IP già in uso nella rete.</span><span class="sxs-lookup"><span data-stu-id="0a486-185">The DHCP client has obtained an IP address that is already in use on the network.</span></span> <span data-ttu-id="0a486-186">L'interfaccia locale verrà disabilitata fino a quando il client DHCP non potrà ottenere un nuovo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="0a486-186">The local interface will be disabled until the DHCP client can obtain a new address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-187"><span id="ERROR_WMI_GUID_NOT_FOUND"></span><span id="error_wmi_guid_not_found"></span>**ERRORE \_ \_ GUID WMI \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="0a486-187"><span id="ERROR_WMI_GUID_NOT_FOUND"></span><span id="error_wmi_guid_not_found"></span>**ERROR\_WMI\_GUID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-188">4200 (0x1068)</span><span class="sxs-lookup"><span data-stu-id="0a486-188">4200 (0x1068)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-189">Il GUID passato non è stato riconosciuto come valido da un provider di dati WMI.</span><span class="sxs-lookup"><span data-stu-id="0a486-189">The GUID passed was not recognized as valid by a WMI data provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-190"><span id="ERROR_WMI_INSTANCE_NOT_FOUND"></span><span id="error_wmi_instance_not_found"></span>**ERRORE \_ dell' \_ istanza WMI \_ non \_ trovata**</span><span class="sxs-lookup"><span data-stu-id="0a486-190"><span id="ERROR_WMI_INSTANCE_NOT_FOUND"></span><span id="error_wmi_instance_not_found"></span>**ERROR\_WMI\_INSTANCE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-191">4201 (0x1069)</span><span class="sxs-lookup"><span data-stu-id="0a486-191">4201 (0x1069)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-192">Il nome dell'istanza passato non è stato riconosciuto come valido da un provider di dati WMI.</span><span class="sxs-lookup"><span data-stu-id="0a486-192">The instance name passed was not recognized as valid by a WMI data provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-193"><span id="ERROR_WMI_ITEMID_NOT_FOUND"></span><span id="error_wmi_itemid_not_found"></span>**ERRORE \_ ID elemento WMI \_ \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="0a486-193"><span id="ERROR_WMI_ITEMID_NOT_FOUND"></span><span id="error_wmi_itemid_not_found"></span>**ERROR\_WMI\_ITEMID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-194">4202 (0x106A)</span><span class="sxs-lookup"><span data-stu-id="0a486-194">4202 (0x106A)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-195">L'ID dell'elemento dati passato non è stato riconosciuto come valido da un provider di dati WMI.</span><span class="sxs-lookup"><span data-stu-id="0a486-195">The data item ID passed was not recognized as valid by a WMI data provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-196"><span id="ERROR_WMI_TRY_AGAIN"></span><span id="error_wmi_try_again"></span>**ERRORE \_ WMI \_ Riprova \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-196"><span id="ERROR_WMI_TRY_AGAIN"></span><span id="error_wmi_try_again"></span>**ERROR\_WMI\_TRY\_AGAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-197">4203 (0x106B)</span><span class="sxs-lookup"><span data-stu-id="0a486-197">4203 (0x106B)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-198">Non è stato possibile completare la richiesta WMI ed è necessario riprovare.</span><span class="sxs-lookup"><span data-stu-id="0a486-198">The WMI request could not be completed and should be retried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-199"><span id="ERROR_WMI_DP_NOT_FOUND"></span><span id="error_wmi_dp_not_found"></span>**ERRORE \_ WMI \_ DP \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="0a486-199"><span id="ERROR_WMI_DP_NOT_FOUND"></span><span id="error_wmi_dp_not_found"></span>**ERROR\_WMI\_DP\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-200">4204 (0x106C)</span><span class="sxs-lookup"><span data-stu-id="0a486-200">4204 (0x106C)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-201">Impossibile trovare il provider di dati WMI.</span><span class="sxs-lookup"><span data-stu-id="0a486-201">The WMI data provider could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-202"><span id="ERROR_WMI_UNRESOLVED_INSTANCE_REF"></span><span id="error_wmi_unresolved_instance_ref"></span>**ERRORE \_ di \_ riferimento dell'istanza non risolta WMI \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-202"><span id="ERROR_WMI_UNRESOLVED_INSTANCE_REF"></span><span id="error_wmi_unresolved_instance_ref"></span>**ERROR\_WMI\_UNRESOLVED\_INSTANCE\_REF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-203">4205 (0x106D)</span><span class="sxs-lookup"><span data-stu-id="0a486-203">4205 (0x106D)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-204">Il provider di dati WMI fa riferimento a un set di istanze che non è stato registrato.</span><span class="sxs-lookup"><span data-stu-id="0a486-204">The WMI data provider references an instance set that has not been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-205"><span id="ERROR_WMI_ALREADY_ENABLED"></span><span id="error_wmi_already_enabled"></span>**ERRORE \_ WMI \_ già \_ abilitato**</span><span class="sxs-lookup"><span data-stu-id="0a486-205"><span id="ERROR_WMI_ALREADY_ENABLED"></span><span id="error_wmi_already_enabled"></span>**ERROR\_WMI\_ALREADY\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-206">4206 (0x106E)</span><span class="sxs-lookup"><span data-stu-id="0a486-206">4206 (0x106E)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-207">Il blocco di dati WMI o la notifica degli eventi è già stata abilitata.</span><span class="sxs-lookup"><span data-stu-id="0a486-207">The WMI data block or event notification has already been enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-208"><span id="ERROR_WMI_GUID_DISCONNECTED"></span><span id="error_wmi_guid_disconnected"></span>**ERRORE \_ \_ GUID WMI \_ disconnesso**</span><span class="sxs-lookup"><span data-stu-id="0a486-208"><span id="ERROR_WMI_GUID_DISCONNECTED"></span><span id="error_wmi_guid_disconnected"></span>**ERROR\_WMI\_GUID\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-209">4207 (0x106F)</span><span class="sxs-lookup"><span data-stu-id="0a486-209">4207 (0x106F)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-210">Il blocco di dati WMI non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="0a486-210">The WMI data block is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-211"><span id="ERROR_WMI_SERVER_UNAVAILABLE"></span><span id="error_wmi_server_unavailable"></span>**ERRORE \_ server WMI non \_ \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="0a486-211"><span id="ERROR_WMI_SERVER_UNAVAILABLE"></span><span id="error_wmi_server_unavailable"></span>**ERROR\_WMI\_SERVER\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-212">4208 (0x1070)</span><span class="sxs-lookup"><span data-stu-id="0a486-212">4208 (0x1070)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-213">Il servizio dati WMI non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="0a486-213">The WMI data service is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-214"><span id="ERROR_WMI_DP_FAILED"></span><span id="error_wmi_dp_failed"></span>**ERRORE \_ WMI \_ DP \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="0a486-214"><span id="ERROR_WMI_DP_FAILED"></span><span id="error_wmi_dp_failed"></span>**ERROR\_WMI\_DP\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-215">4209 (0x1071)</span><span class="sxs-lookup"><span data-stu-id="0a486-215">4209 (0x1071)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-216">Il provider di dati WMI non è riuscito a eseguire la richiesta.</span><span class="sxs-lookup"><span data-stu-id="0a486-216">The WMI data provider failed to carry out the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-217"><span id="ERROR_WMI_INVALID_MOF"></span><span id="error_wmi_invalid_mof"></span>**ERRORE \_ \_ MOF WMI non valido \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-217"><span id="ERROR_WMI_INVALID_MOF"></span><span id="error_wmi_invalid_mof"></span>**ERROR\_WMI\_INVALID\_MOF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-218">4210 (0x1072)</span><span class="sxs-lookup"><span data-stu-id="0a486-218">4210 (0x1072)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-219">Le informazioni MOF WMI non sono valide.</span><span class="sxs-lookup"><span data-stu-id="0a486-219">The WMI MOF information is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-220"><span id="ERROR_WMI_INVALID_REGINFO"></span><span id="error_wmi_invalid_reginfo"></span>**ERRORE \_ WMI \_ REGINFO non valido \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-220"><span id="ERROR_WMI_INVALID_REGINFO"></span><span id="error_wmi_invalid_reginfo"></span>**ERROR\_WMI\_INVALID\_REGINFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-221">4211 (0x1073)</span><span class="sxs-lookup"><span data-stu-id="0a486-221">4211 (0x1073)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-222">Le informazioni di registrazione WMI non sono valide.</span><span class="sxs-lookup"><span data-stu-id="0a486-222">The WMI registration information is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-223"><span id="ERROR_WMI_ALREADY_DISABLED"></span><span id="error_wmi_already_disabled"></span>**ERRORE \_ WMI \_ già \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="0a486-223"><span id="ERROR_WMI_ALREADY_DISABLED"></span><span id="error_wmi_already_disabled"></span>**ERROR\_WMI\_ALREADY\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-224">4212 (0x1074)</span><span class="sxs-lookup"><span data-stu-id="0a486-224">4212 (0x1074)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-225">Il blocco di dati WMI o la notifica degli eventi è già stata disabilitata.</span><span class="sxs-lookup"><span data-stu-id="0a486-225">The WMI data block or event notification has already been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-226"><span id="ERROR_WMI_READ_ONLY"></span><span id="error_wmi_read_only"></span>**ERRORE \_ WMI di sola \_ lettura \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-226"><span id="ERROR_WMI_READ_ONLY"></span><span id="error_wmi_read_only"></span>**ERROR\_WMI\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-227">4213 (0x1075)</span><span class="sxs-lookup"><span data-stu-id="0a486-227">4213 (0x1075)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-228">Il blocco di dati o l'elemento di dati WMI è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="0a486-228">The WMI data item or data block is read only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-229"><span id="ERROR_WMI_SET_FAILURE"></span><span id="error_wmi_set_failure"></span>**ERRORE \_ set WMI Error \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-229"><span id="ERROR_WMI_SET_FAILURE"></span><span id="error_wmi_set_failure"></span>**ERROR\_WMI\_SET\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-230">4214 (0x1076)</span><span class="sxs-lookup"><span data-stu-id="0a486-230">4214 (0x1076)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-231">Impossibile modificare l'elemento di dati WMI o il blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="0a486-231">The WMI data item or data block could not be changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-232"><span id="ERROR_NOT_APPCONTAINER"></span><span id="error_not_appcontainer"></span>**ERRORE \_ non \_ appcontainer**</span><span class="sxs-lookup"><span data-stu-id="0a486-232"><span id="ERROR_NOT_APPCONTAINER"></span><span id="error_not_appcontainer"></span>**ERROR\_NOT\_APPCONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-233">4250 (0x109A)</span><span class="sxs-lookup"><span data-stu-id="0a486-233">4250 (0x109A)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-234">Questa operazione è valida solo nel contesto di un contenitore di app.</span><span class="sxs-lookup"><span data-stu-id="0a486-234">This operation is only valid in the context of an app container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-235"><span id="ERROR_APPCONTAINER_REQUIRED"></span><span id="error_appcontainer_required"></span>**ERRORE \_ appcontainer \_ obbligatorio**</span><span class="sxs-lookup"><span data-stu-id="0a486-235"><span id="ERROR_APPCONTAINER_REQUIRED"></span><span id="error_appcontainer_required"></span>**ERROR\_APPCONTAINER\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-236">4251 (0x109B)</span><span class="sxs-lookup"><span data-stu-id="0a486-236">4251 (0x109B)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-237">Questa applicazione può essere eseguita solo nel contesto di un contenitore di app.</span><span class="sxs-lookup"><span data-stu-id="0a486-237">This application can only run in the context of an app container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-238"><span id="ERROR_NOT_SUPPORTED_IN_APPCONTAINER"></span><span id="error_not_supported_in_appcontainer"></span>**ERRORE \_ non \_ supportato \_ in \_ appcontainer**</span><span class="sxs-lookup"><span data-stu-id="0a486-238"><span id="ERROR_NOT_SUPPORTED_IN_APPCONTAINER"></span><span id="error_not_supported_in_appcontainer"></span>**ERROR\_NOT\_SUPPORTED\_IN\_APPCONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-239">4252 (0x109C)</span><span class="sxs-lookup"><span data-stu-id="0a486-239">4252 (0x109C)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-240">Questa funzionalità non è supportata nel contesto di un contenitore di app.</span><span class="sxs-lookup"><span data-stu-id="0a486-240">This functionality is not supported in the context of an app container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-241"><span id="ERROR_INVALID_PACKAGE_SID_LENGTH"></span><span id="error_invalid_package_sid_length"></span>**ERRORE \_ di \_ \_ lunghezza SID \_ pacchetto non valido**</span><span class="sxs-lookup"><span data-stu-id="0a486-241"><span id="ERROR_INVALID_PACKAGE_SID_LENGTH"></span><span id="error_invalid_package_sid_length"></span>**ERROR\_INVALID\_PACKAGE\_SID\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-242">4253 (0x109D)</span><span class="sxs-lookup"><span data-stu-id="0a486-242">4253 (0x109D)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-243">La lunghezza del SID specificato non è una lunghezza valida per i SID del contenitore di app.</span><span class="sxs-lookup"><span data-stu-id="0a486-243">The length of the SID supplied is not a valid length for app container SIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-244"><span id="ERROR_INVALID_MEDIA"></span><span id="error_invalid_media"></span>**ERRORE \_ supporto non valido \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-244"><span id="ERROR_INVALID_MEDIA"></span><span id="error_invalid_media"></span>**ERROR\_INVALID\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-245">4300 (0x10CC)</span><span class="sxs-lookup"><span data-stu-id="0a486-245">4300 (0x10CC)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-246">L'identificatore del supporto non rappresenta un supporto valido.</span><span class="sxs-lookup"><span data-stu-id="0a486-246">The media identifier does not represent a valid medium.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-247"><span id="ERROR_INVALID_LIBRARY"></span><span id="error_invalid_library"></span>**ERRORE \_ di \_ libreria non valida**</span><span class="sxs-lookup"><span data-stu-id="0a486-247"><span id="ERROR_INVALID_LIBRARY"></span><span id="error_invalid_library"></span>**ERROR\_INVALID\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-248">4301 (0x10CD)</span><span class="sxs-lookup"><span data-stu-id="0a486-248">4301 (0x10CD)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-249">L'identificatore della libreria non rappresenta una libreria valida.</span><span class="sxs-lookup"><span data-stu-id="0a486-249">The library identifier does not represent a valid library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-250"><span id="ERROR_INVALID_MEDIA_POOL"></span><span id="error_invalid_media_pool"></span>**ERRORE \_ nel \_ pool di supporti non valido \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-250"><span id="ERROR_INVALID_MEDIA_POOL"></span><span id="error_invalid_media_pool"></span>**ERROR\_INVALID\_MEDIA\_POOL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-251">4302 (0x10CE)</span><span class="sxs-lookup"><span data-stu-id="0a486-251">4302 (0x10CE)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-252">L'identificatore del pool di supporti non rappresenta un pool di supporti valido.</span><span class="sxs-lookup"><span data-stu-id="0a486-252">The media pool identifier does not represent a valid media pool.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-253"><span id="ERROR_DRIVE_MEDIA_MISMATCH"></span><span id="error_drive_media_mismatch"></span>**supporto dell'unità di errore non \_ \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="0a486-253"><span id="ERROR_DRIVE_MEDIA_MISMATCH"></span><span id="error_drive_media_mismatch"></span>**ERROR\_DRIVE\_MEDIA\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-254">4303 (0x10CF)</span><span class="sxs-lookup"><span data-stu-id="0a486-254">4303 (0x10CF)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-255">L'unità e il supporto non sono compatibili o sono presenti in librerie diverse.</span><span class="sxs-lookup"><span data-stu-id="0a486-255">The drive and medium are not compatible or exist in different libraries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-256"><span id="ERROR_MEDIA_OFFLINE"></span><span id="error_media_offline"></span>**\_supporto errori \_ offline**</span><span class="sxs-lookup"><span data-stu-id="0a486-256"><span id="ERROR_MEDIA_OFFLINE"></span><span id="error_media_offline"></span>**ERROR\_MEDIA\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-257">4304 (0x10D0)</span><span class="sxs-lookup"><span data-stu-id="0a486-257">4304 (0x10D0)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-258">Il supporto attualmente esiste in una libreria offline e deve essere online per eseguire questa operazione.</span><span class="sxs-lookup"><span data-stu-id="0a486-258">The medium currently exists in an offline library and must be online to perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-259"><span id="ERROR_LIBRARY_OFFLINE"></span><span id="error_library_offline"></span>**\_libreria errori \_ offline**</span><span class="sxs-lookup"><span data-stu-id="0a486-259"><span id="ERROR_LIBRARY_OFFLINE"></span><span id="error_library_offline"></span>**ERROR\_LIBRARY\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-260">4305 (0x10D1)</span><span class="sxs-lookup"><span data-stu-id="0a486-260">4305 (0x10D1)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-261">Impossibile eseguire l'operazione su una libreria offline.</span><span class="sxs-lookup"><span data-stu-id="0a486-261">The operation cannot be performed on an offline library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-262"><span id="ERROR_EMPTY"></span><span id="error_empty"></span>**ERRORE \_ vuoto**</span><span class="sxs-lookup"><span data-stu-id="0a486-262"><span id="ERROR_EMPTY"></span><span id="error_empty"></span>**ERROR\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-263">4306 (0x10D2)</span><span class="sxs-lookup"><span data-stu-id="0a486-263">4306 (0x10D2)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-264">La libreria, l'unità o il pool di supporti è vuoto.</span><span class="sxs-lookup"><span data-stu-id="0a486-264">The library, drive, or media pool is empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-265"><span id="ERROR_NOT_EMPTY"></span><span id="error_not_empty"></span>**ERRORE \_ non \_ vuoto**</span><span class="sxs-lookup"><span data-stu-id="0a486-265"><span id="ERROR_NOT_EMPTY"></span><span id="error_not_empty"></span>**ERROR\_NOT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-266">4307 (0x10D3)</span><span class="sxs-lookup"><span data-stu-id="0a486-266">4307 (0x10D3)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-267">Per eseguire questa operazione, è necessario che la libreria, l'unità o il pool di supporti sia vuoto.</span><span class="sxs-lookup"><span data-stu-id="0a486-267">The library, drive, or media pool must be empty to perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-268"><span id="ERROR_MEDIA_UNAVAILABLE"></span><span id="error_media_unavailable"></span>**supporto errori non \_ \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="0a486-268"><span id="ERROR_MEDIA_UNAVAILABLE"></span><span id="error_media_unavailable"></span>**ERROR\_MEDIA\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-269">4308 (0x10D4)</span><span class="sxs-lookup"><span data-stu-id="0a486-269">4308 (0x10D4)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-270">Nessun supporto è attualmente disponibile in questo pool di supporti o nella libreria.</span><span class="sxs-lookup"><span data-stu-id="0a486-270">No media is currently available in this media pool or library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-271"><span id="ERROR_RESOURCE_DISABLED"></span><span id="error_resource_disabled"></span>**\_risorsa errore \_ disabilitata**</span><span class="sxs-lookup"><span data-stu-id="0a486-271"><span id="ERROR_RESOURCE_DISABLED"></span><span id="error_resource_disabled"></span>**ERROR\_RESOURCE\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-272">4309 (0x10D5)</span><span class="sxs-lookup"><span data-stu-id="0a486-272">4309 (0x10D5)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-273">Una risorsa necessaria per questa operazione è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="0a486-273">A resource required for this operation is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-274"><span id="ERROR_INVALID_CLEANER"></span><span id="error_invalid_cleaner"></span>**ERRORE \_ di \_ pulizia non valido**</span><span class="sxs-lookup"><span data-stu-id="0a486-274"><span id="ERROR_INVALID_CLEANER"></span><span id="error_invalid_cleaner"></span>**ERROR\_INVALID\_CLEANER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-275">4310 (0x10D6)</span><span class="sxs-lookup"><span data-stu-id="0a486-275">4310 (0x10D6)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-276">L'identificatore del supporto non rappresenta una pulitura valida.</span><span class="sxs-lookup"><span data-stu-id="0a486-276">The media identifier does not represent a valid cleaner.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-277"><span id="ERROR_UNABLE_TO_CLEAN"></span><span id="error_unable_to_clean"></span>**ERRORE \_ \_ di \_ pulizia**</span><span class="sxs-lookup"><span data-stu-id="0a486-277"><span id="ERROR_UNABLE_TO_CLEAN"></span><span id="error_unable_to_clean"></span>**ERROR\_UNABLE\_TO\_CLEAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-278">4311 (0x10D7)</span><span class="sxs-lookup"><span data-stu-id="0a486-278">4311 (0x10D7)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-279">L'unità non può essere pulita o non supporta la pulizia.</span><span class="sxs-lookup"><span data-stu-id="0a486-279">The drive cannot be cleaned or does not support cleaning.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-280"><span id="ERROR_OBJECT_NOT_FOUND"></span><span id="error_object_not_found"></span>**\_ \_ Impossibile trovare l'oggetto errore \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-280"><span id="ERROR_OBJECT_NOT_FOUND"></span><span id="error_object_not_found"></span>**ERROR\_OBJECT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-281">4312 (0x10D8)</span><span class="sxs-lookup"><span data-stu-id="0a486-281">4312 (0x10D8)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-282">L'identificatore di oggetto non rappresenta un oggetto valido.</span><span class="sxs-lookup"><span data-stu-id="0a486-282">The object identifier does not represent a valid object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-283"><span id="ERROR_DATABASE_FAILURE"></span><span id="error_database_failure"></span>**ERRORE nel \_ database \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-283"><span id="ERROR_DATABASE_FAILURE"></span><span id="error_database_failure"></span>**ERROR\_DATABASE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-284">4313 (0x10D9)</span><span class="sxs-lookup"><span data-stu-id="0a486-284">4313 (0x10D9)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-285">Impossibile leggere o scrivere nel database.</span><span class="sxs-lookup"><span data-stu-id="0a486-285">Unable to read from or write to the database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-286"><span id="ERROR_DATABASE_FULL"></span><span id="error_database_full"></span>**DATABASE con errori \_ \_ completo**</span><span class="sxs-lookup"><span data-stu-id="0a486-286"><span id="ERROR_DATABASE_FULL"></span><span id="error_database_full"></span>**ERROR\_DATABASE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-287">4314 (0x10DA)</span><span class="sxs-lookup"><span data-stu-id="0a486-287">4314 (0x10DA)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-288">Il database è pieno.</span><span class="sxs-lookup"><span data-stu-id="0a486-288">The database is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-289"><span id="ERROR_MEDIA_INCOMPATIBLE"></span><span id="error_media_incompatible"></span>**\_supporti errori \_ incompatibili**</span><span class="sxs-lookup"><span data-stu-id="0a486-289"><span id="ERROR_MEDIA_INCOMPATIBLE"></span><span id="error_media_incompatible"></span>**ERROR\_MEDIA\_INCOMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-290">4315 (0x10DB)</span><span class="sxs-lookup"><span data-stu-id="0a486-290">4315 (0x10DB)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-291">Il supporto non è compatibile con il dispositivo o il pool di supporti.</span><span class="sxs-lookup"><span data-stu-id="0a486-291">The medium is not compatible with the device or media pool.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-292"><span id="ERROR_RESOURCE_NOT_PRESENT"></span><span id="error_resource_not_present"></span>**\_risorsa errore \_ non \_ presente**</span><span class="sxs-lookup"><span data-stu-id="0a486-292"><span id="ERROR_RESOURCE_NOT_PRESENT"></span><span id="error_resource_not_present"></span>**ERROR\_RESOURCE\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-293">4316 (0x10DC)</span><span class="sxs-lookup"><span data-stu-id="0a486-293">4316 (0x10DC)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-294">La risorsa necessaria per questa operazione non esiste.</span><span class="sxs-lookup"><span data-stu-id="0a486-294">The resource required for this operation does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-295"><span id="ERROR_INVALID_OPERATION"></span><span id="error_invalid_operation"></span>**ERRORE \_ operazione non valida \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-295"><span id="ERROR_INVALID_OPERATION"></span><span id="error_invalid_operation"></span>**ERROR\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-296">4317 (0x10DD)</span><span class="sxs-lookup"><span data-stu-id="0a486-296">4317 (0x10DD)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-297">Identificatore dell'operazione non valido.</span><span class="sxs-lookup"><span data-stu-id="0a486-297">The operation identifier is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-298"><span id="ERROR_MEDIA_NOT_AVAILABLE"></span><span id="error_media_not_available"></span>**\_supporto errori \_ non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="0a486-298"><span id="ERROR_MEDIA_NOT_AVAILABLE"></span><span id="error_media_not_available"></span>**ERROR\_MEDIA\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-299">4318 (0x10DE)</span><span class="sxs-lookup"><span data-stu-id="0a486-299">4318 (0x10DE)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-300">Il supporto non è montato o pronto per l'uso.</span><span class="sxs-lookup"><span data-stu-id="0a486-300">The media is not mounted or ready for use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-301"><span id="ERROR_DEVICE_NOT_AVAILABLE"></span><span id="error_device_not_available"></span>**dispositivo di errore \_ \_ non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="0a486-301"><span id="ERROR_DEVICE_NOT_AVAILABLE"></span><span id="error_device_not_available"></span>**ERROR\_DEVICE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-302">4319 (0x10DF)</span><span class="sxs-lookup"><span data-stu-id="0a486-302">4319 (0x10DF)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-303">Il dispositivo non è pronto per l'uso.</span><span class="sxs-lookup"><span data-stu-id="0a486-303">The device is not ready for use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-304"><span id="ERROR_REQUEST_REFUSED"></span><span id="error_request_refused"></span>**richiesta di errore \_ \_ rifiutata**</span><span class="sxs-lookup"><span data-stu-id="0a486-304"><span id="ERROR_REQUEST_REFUSED"></span><span id="error_request_refused"></span>**ERROR\_REQUEST\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-305">4320 (0x10E0)</span><span class="sxs-lookup"><span data-stu-id="0a486-305">4320 (0x10E0)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-306">L'operatore o l'amministratore ha rifiutato la richiesta.</span><span class="sxs-lookup"><span data-stu-id="0a486-306">The operator or administrator has refused the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-307"><span id="ERROR_INVALID_DRIVE_OBJECT"></span><span id="error_invalid_drive_object"></span>**ERRORE \_ dell' \_ oggetto unità non valido \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-307"><span id="ERROR_INVALID_DRIVE_OBJECT"></span><span id="error_invalid_drive_object"></span>**ERROR\_INVALID\_DRIVE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-308">4321 (0x10E1)</span><span class="sxs-lookup"><span data-stu-id="0a486-308">4321 (0x10E1)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-309">L'identificatore dell'unità non rappresenta un'unità valida.</span><span class="sxs-lookup"><span data-stu-id="0a486-309">The drive identifier does not represent a valid drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-310"><span id="ERROR_LIBRARY_FULL"></span><span id="error_library_full"></span>**\_libreria errori \_ completa**</span><span class="sxs-lookup"><span data-stu-id="0a486-310"><span id="ERROR_LIBRARY_FULL"></span><span id="error_library_full"></span>**ERROR\_LIBRARY\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-311">4322 (0x10E2)</span><span class="sxs-lookup"><span data-stu-id="0a486-311">4322 (0x10E2)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-312">La libreria è piena.</span><span class="sxs-lookup"><span data-stu-id="0a486-312">Library is full.</span></span> <span data-ttu-id="0a486-313">Nessun slot disponibile per l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="0a486-313">No slot is available for use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-314"><span id="ERROR_MEDIUM_NOT_ACCESSIBLE"></span><span id="error_medium_not_accessible"></span>**ERRORE \_ medio \_ non \_ accessibile**</span><span class="sxs-lookup"><span data-stu-id="0a486-314"><span id="ERROR_MEDIUM_NOT_ACCESSIBLE"></span><span id="error_medium_not_accessible"></span>**ERROR\_MEDIUM\_NOT\_ACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-315">4323 (0x10E3)</span><span class="sxs-lookup"><span data-stu-id="0a486-315">4323 (0x10E3)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-316">Il trasporto non può accedere al supporto.</span><span class="sxs-lookup"><span data-stu-id="0a486-316">The transport cannot access the medium.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-317"><span id="ERROR_UNABLE_TO_LOAD_MEDIUM"></span><span id="error_unable_to_load_medium"></span>**ERRORE \_ non è possibile \_ \_ caricare il \_ supporto**</span><span class="sxs-lookup"><span data-stu-id="0a486-317"><span id="ERROR_UNABLE_TO_LOAD_MEDIUM"></span><span id="error_unable_to_load_medium"></span>**ERROR\_UNABLE\_TO\_LOAD\_MEDIUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-318">4324 (0x10E4)</span><span class="sxs-lookup"><span data-stu-id="0a486-318">4324 (0x10E4)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-319">Impossibile caricare il supporto nell'unità.</span><span class="sxs-lookup"><span data-stu-id="0a486-319">Unable to load the medium into the drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-320"><span id="ERROR_UNABLE_TO_INVENTORY_DRIVE"></span><span id="error_unable_to_inventory_drive"></span>**ERRORE \_ \_ nell' \_ inventario dell' \_ unità**</span><span class="sxs-lookup"><span data-stu-id="0a486-320"><span id="ERROR_UNABLE_TO_INVENTORY_DRIVE"></span><span id="error_unable_to_inventory_drive"></span>**ERROR\_UNABLE\_TO\_INVENTORY\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-321">4325 (0x10E5)</span><span class="sxs-lookup"><span data-stu-id="0a486-321">4325 (0x10E5)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-322">Impossibile recuperare lo stato dell'unità.</span><span class="sxs-lookup"><span data-stu-id="0a486-322">Unable to retrieve the drive status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-323"><span id="ERROR_UNABLE_TO_INVENTORY_SLOT"></span><span id="error_unable_to_inventory_slot"></span>**ERRORE \_ \_ di \_ inventario dello \_ slot**</span><span class="sxs-lookup"><span data-stu-id="0a486-323"><span id="ERROR_UNABLE_TO_INVENTORY_SLOT"></span><span id="error_unable_to_inventory_slot"></span>**ERROR\_UNABLE\_TO\_INVENTORY\_SLOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-324">4326 (0x10E6)</span><span class="sxs-lookup"><span data-stu-id="0a486-324">4326 (0x10E6)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-325">Non è possibile recuperare lo stato dello slot.</span><span class="sxs-lookup"><span data-stu-id="0a486-325">Unable to retrieve the slot status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-326"><span id="ERROR_UNABLE_TO_INVENTORY_TRANSPORT"></span><span id="error_unable_to_inventory_transport"></span>**ERRORE \_ non è possibile \_ eseguire l' \_ inventario del \_ trasporto**</span><span class="sxs-lookup"><span data-stu-id="0a486-326"><span id="ERROR_UNABLE_TO_INVENTORY_TRANSPORT"></span><span id="error_unable_to_inventory_transport"></span>**ERROR\_UNABLE\_TO\_INVENTORY\_TRANSPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-327">4327 (0x10E7)</span><span class="sxs-lookup"><span data-stu-id="0a486-327">4327 (0x10E7)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-328">Impossibile recuperare lo stato del trasporto.</span><span class="sxs-lookup"><span data-stu-id="0a486-328">Unable to retrieve status about the transport.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-329"><span id="ERROR_TRANSPORT_FULL"></span><span id="error_transport_full"></span>**\_trasporto errori \_ completo**</span><span class="sxs-lookup"><span data-stu-id="0a486-329"><span id="ERROR_TRANSPORT_FULL"></span><span id="error_transport_full"></span>**ERROR\_TRANSPORT\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-330">4328 (0x10E8)</span><span class="sxs-lookup"><span data-stu-id="0a486-330">4328 (0x10E8)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-331">Impossibile utilizzare il trasporto perché è già in uso.</span><span class="sxs-lookup"><span data-stu-id="0a486-331">Cannot use the transport because it is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-332"><span id="ERROR_CONTROLLING_IEPORT"></span><span id="error_controlling_ieport"></span>**errore durante il \_ controllo di \_ inserimento/espulsione**</span><span class="sxs-lookup"><span data-stu-id="0a486-332"><span id="ERROR_CONTROLLING_IEPORT"></span><span id="error_controlling_ieport"></span>**ERROR\_CONTROLLING\_IEPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-333">4329 (0x10E9)</span><span class="sxs-lookup"><span data-stu-id="0a486-333">4329 (0x10E9)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-334">Non è possibile aprire o chiudere la porta di inserimento/espulsione.</span><span class="sxs-lookup"><span data-stu-id="0a486-334">Unable to open or close the inject/eject port.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-335"><span id="ERROR_UNABLE_TO_EJECT_MOUNTED_MEDIA"></span><span id="error_unable_to_eject_mounted_media"></span>**ERRORE \_ non è possibile \_ \_ rimuovere il \_ \_ supporto montato**</span><span class="sxs-lookup"><span data-stu-id="0a486-335"><span id="ERROR_UNABLE_TO_EJECT_MOUNTED_MEDIA"></span><span id="error_unable_to_eject_mounted_media"></span>**ERROR\_UNABLE\_TO\_EJECT\_MOUNTED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-336">4330 (0x10EA)</span><span class="sxs-lookup"><span data-stu-id="0a486-336">4330 (0x10EA)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-337">Impossibile estrarre il supporto perché si trova in un'unità.</span><span class="sxs-lookup"><span data-stu-id="0a486-337">Unable to eject the medium because it is in a drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-338"><span id="ERROR_CLEANER_SLOT_SET"></span><span id="error_cleaner_slot_set"></span>**SET di slot per la pulizia degli errori \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-338"><span id="ERROR_CLEANER_SLOT_SET"></span><span id="error_cleaner_slot_set"></span>**ERROR\_CLEANER\_SLOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-339">4331 (0x10EB)</span><span class="sxs-lookup"><span data-stu-id="0a486-339">4331 (0x10EB)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-340">Uno slot di pulitura è già riservato.</span><span class="sxs-lookup"><span data-stu-id="0a486-340">A cleaner slot is already reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-341"><span id="ERROR_CLEANER_SLOT_NOT_SET"></span><span id="error_cleaner_slot_not_set"></span>**lo slot per la pulizia degli errori \_ \_ non è \_ \_ impostato**</span><span class="sxs-lookup"><span data-stu-id="0a486-341"><span id="ERROR_CLEANER_SLOT_NOT_SET"></span><span id="error_cleaner_slot_not_set"></span>**ERROR\_CLEANER\_SLOT\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-342">4332 (0x10EC)</span><span class="sxs-lookup"><span data-stu-id="0a486-342">4332 (0x10EC)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-343">Uno slot di pulitura non è riservato.</span><span class="sxs-lookup"><span data-stu-id="0a486-343">A cleaner slot is not reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-344"><span id="ERROR_CLEANER_CARTRIDGE_SPENT"></span><span id="error_cleaner_cartridge_spent"></span>**\_pulitura della \_ cartuccia di \_ errore**</span><span class="sxs-lookup"><span data-stu-id="0a486-344"><span id="ERROR_CLEANER_CARTRIDGE_SPENT"></span><span id="error_cleaner_cartridge_spent"></span>**ERROR\_CLEANER\_CARTRIDGE\_SPENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-345">4333 (0x10ED)</span><span class="sxs-lookup"><span data-stu-id="0a486-345">4333 (0x10ED)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-346">La cartuccia Cleaner ha eseguito il numero massimo di operazioni di pulizia delle unità.</span><span class="sxs-lookup"><span data-stu-id="0a486-346">The cleaner cartridge has performed the maximum number of drive cleanings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-347"><span id="ERROR_UNEXPECTED_OMID"></span><span id="error_unexpected_omid"></span>**errore di un errore \_ imprevisto. \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-347"><span id="ERROR_UNEXPECTED_OMID"></span><span id="error_unexpected_omid"></span>**ERROR\_UNEXPECTED\_OMID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-348">4334 (0x10EE)</span><span class="sxs-lookup"><span data-stu-id="0a486-348">4334 (0x10EE)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-349">Identificatore medio imprevisto.</span><span class="sxs-lookup"><span data-stu-id="0a486-349">Unexpected on-medium identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-350"><span id="ERROR_CANT_DELETE_LAST_ITEM"></span><span id="error_cant_delete_last_item"></span>**errore \_ durante \_ l'eliminazione dell' \_ ultimo \_ elemento**</span><span class="sxs-lookup"><span data-stu-id="0a486-350"><span id="ERROR_CANT_DELETE_LAST_ITEM"></span><span id="error_cant_delete_last_item"></span>**ERROR\_CANT\_DELETE\_LAST\_ITEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-351">4335 (0x10EF)</span><span class="sxs-lookup"><span data-stu-id="0a486-351">4335 (0x10EF)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-352">L'ultimo elemento rimanente in questo gruppo o risorsa non può essere eliminato.</span><span class="sxs-lookup"><span data-stu-id="0a486-352">The last remaining item in this group or resource cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-353"><span id="ERROR_MESSAGE_EXCEEDS_MAX_SIZE"></span><span id="error_message_exceeds_max_size"></span>**il \_ messaggio di errore \_ supera le \_ dimensioni massime \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-353"><span id="ERROR_MESSAGE_EXCEEDS_MAX_SIZE"></span><span id="error_message_exceeds_max_size"></span>**ERROR\_MESSAGE\_EXCEEDS\_MAX\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-354">4336 (0x10F0)</span><span class="sxs-lookup"><span data-stu-id="0a486-354">4336 (0x10F0)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-355">Il messaggio specificato supera la dimensione massima consentita per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="0a486-355">The message provided exceeds the maximum size allowed for this parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-356"><span id="ERROR_VOLUME_CONTAINS_SYS_FILES"></span><span id="error_volume_contains_sys_files"></span>**il \_ volume degli errori \_ contiene \_ \_ i file sys**</span><span class="sxs-lookup"><span data-stu-id="0a486-356"><span id="ERROR_VOLUME_CONTAINS_SYS_FILES"></span><span id="error_volume_contains_sys_files"></span>**ERROR\_VOLUME\_CONTAINS\_SYS\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-357">4337 (0x10F1)</span><span class="sxs-lookup"><span data-stu-id="0a486-357">4337 (0x10F1)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-358">Il volume contiene file di sistema o di paging.</span><span class="sxs-lookup"><span data-stu-id="0a486-358">The volume contains system or paging files.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-359"><span id="ERROR_INDIGENOUS_TYPE"></span><span id="error_indigenous_type"></span>**tipo di errore \_ nativo \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-359"><span id="ERROR_INDIGENOUS_TYPE"></span><span id="error_indigenous_type"></span>**ERROR\_INDIGENOUS\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-360">4338 (0x10F2)</span><span class="sxs-lookup"><span data-stu-id="0a486-360">4338 (0x10F2)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-361">Non è possibile rimuovere il tipo di supporto da questa libreria perché almeno un'unità nella libreria segnala che è in grado di supportare questo tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="0a486-361">The media type cannot be removed from this library since at least one drive in the library reports it can support this media type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-362"><span id="ERROR_NO_SUPPORTING_DRIVES"></span><span id="error_no_supporting_drives"></span>**ERRORE \_ senza \_ unità di supporto \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-362"><span id="ERROR_NO_SUPPORTING_DRIVES"></span><span id="error_no_supporting_drives"></span>**ERROR\_NO\_SUPPORTING\_DRIVES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-363">4339 (0x10F3)</span><span class="sxs-lookup"><span data-stu-id="0a486-363">4339 (0x10F3)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-364">Non è possibile montare questo supporto offline sul sistema perché non sono presenti unità abilitate che possono essere usate.</span><span class="sxs-lookup"><span data-stu-id="0a486-364">This offline media cannot be mounted on this system since no enabled drives are present which can be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-365"><span id="ERROR_CLEANER_CARTRIDGE_INSTALLED"></span><span id="error_cleaner_cartridge_installed"></span>**\_cartuccia di pulitura errori \_ \_ installata**</span><span class="sxs-lookup"><span data-stu-id="0a486-365"><span id="ERROR_CLEANER_CARTRIDGE_INSTALLED"></span><span id="error_cleaner_cartridge_installed"></span>**ERROR\_CLEANER\_CARTRIDGE\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-366">4340 (0x10F4)</span><span class="sxs-lookup"><span data-stu-id="0a486-366">4340 (0x10F4)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-367">Nella libreria di nastri è presente una cartuccia di pulitura.</span><span class="sxs-lookup"><span data-stu-id="0a486-367">A cleaner cartridge is present in the tape library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-368"><span id="ERROR_IEPORT_FULL"></span><span id="error_ieport_full"></span>**ERRORE \_ inserimento/espulsione \_ completo**</span><span class="sxs-lookup"><span data-stu-id="0a486-368"><span id="ERROR_IEPORT_FULL"></span><span id="error_ieport_full"></span>**ERROR\_IEPORT\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-369">4341 (0x10F5)</span><span class="sxs-lookup"><span data-stu-id="0a486-369">4341 (0x10F5)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-370">Impossibile utilizzare la porta di inserimento/espulsione perché non è vuota.</span><span class="sxs-lookup"><span data-stu-id="0a486-370">Cannot use the inject/eject port because it is not empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-371"><span id="ERROR_FILE_OFFLINE"></span><span id="error_file_offline"></span>**FILE degli errori \_ \_ offline**</span><span class="sxs-lookup"><span data-stu-id="0a486-371"><span id="ERROR_FILE_OFFLINE"></span><span id="error_file_offline"></span>**ERROR\_FILE\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-372">4350 (0x10FE)</span><span class="sxs-lookup"><span data-stu-id="0a486-372">4350 (0x10FE)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-373">Il file non è attualmente disponibile per l'utilizzo in questo computer.</span><span class="sxs-lookup"><span data-stu-id="0a486-373">This file is currently not available for use on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-374"><span id="ERROR_REMOTE_STORAGE_NOT_ACTIVE"></span><span id="error_remote_storage_not_active"></span>**ERRORE \_ di \_ archiviazione remota \_ non \_ attivo**</span><span class="sxs-lookup"><span data-stu-id="0a486-374"><span id="ERROR_REMOTE_STORAGE_NOT_ACTIVE"></span><span id="error_remote_storage_not_active"></span>**ERROR\_REMOTE\_STORAGE\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-375">4351 (0x10FF)</span><span class="sxs-lookup"><span data-stu-id="0a486-375">4351 (0x10FF)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-376">Il servizio di archiviazione remoto non è operativo in questo momento.</span><span class="sxs-lookup"><span data-stu-id="0a486-376">The remote storage service is not operational at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-377"><span id="ERROR_REMOTE_STORAGE_MEDIA_ERROR"></span><span id="error_remote_storage_media_error"></span>**errore \_ del \_ supporto di archiviazione remota \_ errore \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-377"><span id="ERROR_REMOTE_STORAGE_MEDIA_ERROR"></span><span id="error_remote_storage_media_error"></span>**ERROR\_REMOTE\_STORAGE\_MEDIA\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-378">4352 (0x1100)</span><span class="sxs-lookup"><span data-stu-id="0a486-378">4352 (0x1100)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-379">Il servizio di archiviazione remota ha rilevato un errore del supporto.</span><span class="sxs-lookup"><span data-stu-id="0a486-379">The remote storage service encountered a media error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-380"><span id="ERROR_NOT_A_REPARSE_POINT"></span><span id="error_not_a_reparse_point"></span>**ERRORE \_ non è \_ un punto di \_ analisi \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-380"><span id="ERROR_NOT_A_REPARSE_POINT"></span><span id="error_not_a_reparse_point"></span>**ERROR\_NOT\_A\_REPARSE\_POINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-381">4390 (0x1126)</span><span class="sxs-lookup"><span data-stu-id="0a486-381">4390 (0x1126)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-382">Il file o la directory non è un punto di analisi.</span><span class="sxs-lookup"><span data-stu-id="0a486-382">The file or directory is not a reparse point.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-383"><span id="ERROR_REPARSE_ATTRIBUTE_CONFLICT"></span><span id="error_reparse_attribute_conflict"></span>**ERRORE di \_ RIanalisi dell' \_ attributo \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-383"><span id="ERROR_REPARSE_ATTRIBUTE_CONFLICT"></span><span id="error_reparse_attribute_conflict"></span>**ERROR\_REPARSE\_ATTRIBUTE\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-384">4391 (0x1127)</span><span class="sxs-lookup"><span data-stu-id="0a486-384">4391 (0x1127)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-385">Non è possibile impostare l'attributo reparse point perché è in conflitto con un attributo esistente.</span><span class="sxs-lookup"><span data-stu-id="0a486-385">The reparse point attribute cannot be set because it conflicts with an existing attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-386"><span id="ERROR_INVALID_REPARSE_DATA"></span><span id="error_invalid_reparse_data"></span>**ERRORE \_ di \_ analisi \_ dei dati non validi**</span><span class="sxs-lookup"><span data-stu-id="0a486-386"><span id="ERROR_INVALID_REPARSE_DATA"></span><span id="error_invalid_reparse_data"></span>**ERROR\_INVALID\_REPARSE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-387">4392 (0x1128)</span><span class="sxs-lookup"><span data-stu-id="0a486-387">4392 (0x1128)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-388">I dati presenti nel buffer del reparse point non sono validi.</span><span class="sxs-lookup"><span data-stu-id="0a486-388">The data present in the reparse point buffer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-389"><span id="ERROR_REPARSE_TAG_INVALID"></span><span id="error_reparse_tag_invalid"></span>**ERRORE di \_ reparse \_ tag \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="0a486-389"><span id="ERROR_REPARSE_TAG_INVALID"></span><span id="error_reparse_tag_invalid"></span>**ERROR\_REPARSE\_TAG\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-390">4393 (0x1129)</span><span class="sxs-lookup"><span data-stu-id="0a486-390">4393 (0x1129)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-391">Il tag presente nel buffer del reparse point non è valido.</span><span class="sxs-lookup"><span data-stu-id="0a486-391">The tag present in the reparse point buffer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-392"><span id="ERROR_REPARSE_TAG_MISMATCH"></span><span id="error_reparse_tag_mismatch"></span>**ERRORE di \_ reparse \_ tag non \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="0a486-392"><span id="ERROR_REPARSE_TAG_MISMATCH"></span><span id="error_reparse_tag_mismatch"></span>**ERROR\_REPARSE\_TAG\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-393">4394 (0x112A)</span><span class="sxs-lookup"><span data-stu-id="0a486-393">4394 (0x112A)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-394">Mancata corrispondenza tra il tag specificato nella richiesta e il tag presente nel reparse point.</span><span class="sxs-lookup"><span data-stu-id="0a486-394">There is a mismatch between the tag specified in the request and the tag present in the reparse point.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-395"><span id="ERROR_APP_DATA_NOT_FOUND"></span><span id="error_app_data_not_found"></span>**ERRORE \_ \_ dati app \_ non \_ trovati**</span><span class="sxs-lookup"><span data-stu-id="0a486-395"><span id="ERROR_APP_DATA_NOT_FOUND"></span><span id="error_app_data_not_found"></span>**ERROR\_APP\_DATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-396">4400 (0x1130)</span><span class="sxs-lookup"><span data-stu-id="0a486-396">4400 (0x1130)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-397">Dati della cache veloce non trovati.</span><span class="sxs-lookup"><span data-stu-id="0a486-397">Fast Cache data not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-398"><span id="ERROR_APP_DATA_EXPIRED"></span><span id="error_app_data_expired"></span>**ERRORE \_ \_ dati app \_ scaduti**</span><span class="sxs-lookup"><span data-stu-id="0a486-398"><span id="ERROR_APP_DATA_EXPIRED"></span><span id="error_app_data_expired"></span>**ERROR\_APP\_DATA\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-399">4401 (0x1131)</span><span class="sxs-lookup"><span data-stu-id="0a486-399">4401 (0x1131)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-400">I dati della cache veloce sono scaduti.</span><span class="sxs-lookup"><span data-stu-id="0a486-400">Fast Cache data expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-401"><span id="ERROR_APP_DATA_CORRUPT"></span><span id="error_app_data_corrupt"></span>**ERRORE \_ \_ dati app \_ danneggiati**</span><span class="sxs-lookup"><span data-stu-id="0a486-401"><span id="ERROR_APP_DATA_CORRUPT"></span><span id="error_app_data_corrupt"></span>**ERROR\_APP\_DATA\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-402">4402 (0x1132)</span><span class="sxs-lookup"><span data-stu-id="0a486-402">4402 (0x1132)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-403">Dati della cache veloce danneggiati.</span><span class="sxs-lookup"><span data-stu-id="0a486-403">Fast Cache data corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-404"><span id="ERROR_APP_DATA_LIMIT_EXCEEDED"></span><span id="error_app_data_limit_exceeded"></span>**ERRORE \_ \_ limite dati \_ app \_ superato**</span><span class="sxs-lookup"><span data-stu-id="0a486-404"><span id="ERROR_APP_DATA_LIMIT_EXCEEDED"></span><span id="error_app_data_limit_exceeded"></span>**ERROR\_APP\_DATA\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-405">4403 (0x1133)</span><span class="sxs-lookup"><span data-stu-id="0a486-405">4403 (0x1133)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-406">I dati della cache veloce hanno superato le dimensioni massime e non possono essere aggiornati.</span><span class="sxs-lookup"><span data-stu-id="0a486-406">Fast Cache data has exceeded its max size and cannot be updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-407"><span id="ERROR_APP_DATA_REBOOT_REQUIRED"></span><span id="error_app_data_reboot_required"></span>**ERRORE \_ è \_ \_ necessario riavviare i dati dell'app \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-407"><span id="ERROR_APP_DATA_REBOOT_REQUIRED"></span><span id="error_app_data_reboot_required"></span>**ERROR\_APP\_DATA\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-408">4404 (0x1134)</span><span class="sxs-lookup"><span data-stu-id="0a486-408">4404 (0x1134)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-409">La cache veloce è stata riarmata e richiede un riavvio fino a quando non può essere aggiornata.</span><span class="sxs-lookup"><span data-stu-id="0a486-409">Fast Cache has been ReArmed and requires a reboot until it can be updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-410"><span id="ERROR_SECUREBOOT_ROLLBACK_DETECTED"></span><span id="error_secureboot_rollback_detected"></span>**ERRORE \_ \_ rilevato rollback \_ SECUREBOOT**</span><span class="sxs-lookup"><span data-stu-id="0a486-410"><span id="ERROR_SECUREBOOT_ROLLBACK_DETECTED"></span><span id="error_secureboot_rollback_detected"></span>**ERROR\_SECUREBOOT\_ROLLBACK\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-411">4420 (0x1144)</span><span class="sxs-lookup"><span data-stu-id="0a486-411">4420 (0x1144)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-412">L'avvio protetto ha rilevato un tentativo di rollback dei dati protetti.</span><span class="sxs-lookup"><span data-stu-id="0a486-412">Secure Boot detected that rollback of protected data has been attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-413"><span id="ERROR_SECUREBOOT_POLICY_VIOLATION"></span><span id="error_secureboot_policy_violation"></span>**ERRORE \_ di \_ violazione dei criteri di SECUREBOOT \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-413"><span id="ERROR_SECUREBOOT_POLICY_VIOLATION"></span><span id="error_secureboot_policy_violation"></span>**ERROR\_SECUREBOOT\_POLICY\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-414">4421 (0x1145)</span><span class="sxs-lookup"><span data-stu-id="0a486-414">4421 (0x1145)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-415">Il valore è protetto da criteri di avvio protetto e non può essere modificato o eliminato.</span><span class="sxs-lookup"><span data-stu-id="0a486-415">The value is protected by Secure Boot policy and cannot be modified or deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-416"><span id="ERROR_SECUREBOOT_INVALID_POLICY"></span><span id="error_secureboot_invalid_policy"></span>**ERRORE \_ SECUREBOOT \_ criterio non valido \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-416"><span id="ERROR_SECUREBOOT_INVALID_POLICY"></span><span id="error_secureboot_invalid_policy"></span>**ERROR\_SECUREBOOT\_INVALID\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-417">4422 (0x1146)</span><span class="sxs-lookup"><span data-stu-id="0a486-417">4422 (0x1146)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-418">Il criterio di avvio protetto non è valido.</span><span class="sxs-lookup"><span data-stu-id="0a486-418">The Secure Boot policy is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-419"><span id="ERROR_SECUREBOOT_POLICY_PUBLISHER_NOT_FOUND"></span><span id="error_secureboot_policy_publisher_not_found"></span>**ERRORE \_ SECUREBOOT di \_ pubblicazione del criterio \_ \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="0a486-419"><span id="ERROR_SECUREBOOT_POLICY_PUBLISHER_NOT_FOUND"></span><span id="error_secureboot_policy_publisher_not_found"></span>**ERROR\_SECUREBOOT\_POLICY\_PUBLISHER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-420">4423 (0x1147)</span><span class="sxs-lookup"><span data-stu-id="0a486-420">4423 (0x1147)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-421">Un nuovo criterio di avvio protetto non contiene il server di pubblicazione corrente nell'elenco di aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="0a486-421">A new Secure Boot policy did not contain the current publisher on its update list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-422"><span id="ERROR_SECUREBOOT_POLICY_NOT_SIGNED"></span><span id="error_secureboot_policy_not_signed"></span>**ERRORE \_ SECUREBOOT \_ criterio \_ non \_ firmato**</span><span class="sxs-lookup"><span data-stu-id="0a486-422"><span id="ERROR_SECUREBOOT_POLICY_NOT_SIGNED"></span><span id="error_secureboot_policy_not_signed"></span>**ERROR\_SECUREBOOT\_POLICY\_NOT\_SIGNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-423">4424 (0x1148)</span><span class="sxs-lookup"><span data-stu-id="0a486-423">4424 (0x1148)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-424">I criteri di avvio protetto non sono firmati o sono firmati da un firmatario non attendibile.</span><span class="sxs-lookup"><span data-stu-id="0a486-424">The Secure Boot policy is either not signed or is signed by a non-trusted signer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-425"><span id="ERROR_SECUREBOOT_NOT_ENABLED"></span><span id="error_secureboot_not_enabled"></span>**ERRORE \_ SECUREBOOT \_ non \_ abilitato**</span><span class="sxs-lookup"><span data-stu-id="0a486-425"><span id="ERROR_SECUREBOOT_NOT_ENABLED"></span><span id="error_secureboot_not_enabled"></span>**ERROR\_SECUREBOOT\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-426">4425 (0x1149)</span><span class="sxs-lookup"><span data-stu-id="0a486-426">4425 (0x1149)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-427">L'avvio protetto non è abilitato in questo computer.</span><span class="sxs-lookup"><span data-stu-id="0a486-427">Secure Boot is not enabled on this machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-428"><span id="ERROR_SECUREBOOT_FILE_REPLACED"></span><span id="error_secureboot_file_replaced"></span>**ERRORE \_ SECUREBOOT \_ file \_ sostituito**</span><span class="sxs-lookup"><span data-stu-id="0a486-428"><span id="ERROR_SECUREBOOT_FILE_REPLACED"></span><span id="error_secureboot_file_replaced"></span>**ERROR\_SECUREBOOT\_FILE\_REPLACED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-429">4426 (0x114A)</span><span class="sxs-lookup"><span data-stu-id="0a486-429">4426 (0x114A)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-430">Per l'avvio protetto è necessario che determinati file e driver non vengano sostituiti da altri file o driver.</span><span class="sxs-lookup"><span data-stu-id="0a486-430">Secure Boot requires that certain files and drivers are not replaced by other files or drivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-431"><span id="ERROR_OFFLOAD_READ_FLT_NOT_SUPPORTED"></span><span id="error_offload_read_flt_not_supported"></span>**ERRORE di \_ OFFLOAD \_ Read \_ flt \_ non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="0a486-431"><span id="ERROR_OFFLOAD_READ_FLT_NOT_SUPPORTED"></span><span id="error_offload_read_flt_not_supported"></span>**ERROR\_OFFLOAD\_READ\_FLT\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-432">4440 (0x1158)</span><span class="sxs-lookup"><span data-stu-id="0a486-432">4440 (0x1158)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-433">L'operazione di lettura dell'offload di copia non è supportata da un filtro.</span><span class="sxs-lookup"><span data-stu-id="0a486-433">The copy offload read operation is not supported by a filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-434"><span id="ERROR_OFFLOAD_WRITE_FLT_NOT_SUPPORTED"></span><span id="error_offload_write_flt_not_supported"></span>**ERRORE di \_ OFFLOAD \_ scrittura \_ flt \_ non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="0a486-434"><span id="ERROR_OFFLOAD_WRITE_FLT_NOT_SUPPORTED"></span><span id="error_offload_write_flt_not_supported"></span>**ERROR\_OFFLOAD\_WRITE\_FLT\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-435">4441 (0x1159)</span><span class="sxs-lookup"><span data-stu-id="0a486-435">4441 (0x1159)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-436">L'operazione di scrittura dell'offload di copia non è supportata da un filtro.</span><span class="sxs-lookup"><span data-stu-id="0a486-436">The copy offload write operation is not supported by a filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-437"><span id="ERROR_OFFLOAD_READ_FILE_NOT_SUPPORTED"></span><span id="error_offload_read_file_not_supported"></span>**ERRORE di \_ OFFLOAD \_ file di lettura \_ \_ non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="0a486-437"><span id="ERROR_OFFLOAD_READ_FILE_NOT_SUPPORTED"></span><span id="error_offload_read_file_not_supported"></span>**ERROR\_OFFLOAD\_READ\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-438">4442 (0x115A)</span><span class="sxs-lookup"><span data-stu-id="0a486-438">4442 (0x115A)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-439">L'operazione di lettura dell'offload di copia non è supportata per il file.</span><span class="sxs-lookup"><span data-stu-id="0a486-439">The copy offload read operation is not supported for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-440"><span id="ERROR_OFFLOAD_WRITE_FILE_NOT_SUPPORTED"></span><span id="error_offload_write_file_not_supported"></span>**errore durante l' \_ OFFLOAD del \_ file di scrittura \_ \_ non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="0a486-440"><span id="ERROR_OFFLOAD_WRITE_FILE_NOT_SUPPORTED"></span><span id="error_offload_write_file_not_supported"></span>**ERROR\_OFFLOAD\_WRITE\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-441">4443 (0x115B)</span><span class="sxs-lookup"><span data-stu-id="0a486-441">4443 (0x115B)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-442">L'operazione di scrittura dell'offload di copia non è supportata per il file.</span><span class="sxs-lookup"><span data-stu-id="0a486-442">The copy offload write operation is not supported for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-443"><span id="ERROR_VOLUME_NOT_SIS_ENABLED"></span><span id="error_volume_not_sis_enabled"></span>**VOLUME di errore \_ \_ non \_ abilitato per SIS \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-443"><span id="ERROR_VOLUME_NOT_SIS_ENABLED"></span><span id="error_volume_not_sis_enabled"></span>**ERROR\_VOLUME\_NOT\_SIS\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-444">4500 (0x1194)</span><span class="sxs-lookup"><span data-stu-id="0a486-444">4500 (0x1194)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-445">L'archiviazione a istanza singola non è disponibile in questo volume.</span><span class="sxs-lookup"><span data-stu-id="0a486-445">Single Instance Storage is not available on this volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-446"><span id="ERROR_DEPENDENT_RESOURCE_EXISTS"></span><span id="error_dependent_resource_exists"></span>**\_risorsa dipendente dall'errore \_ \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="0a486-446"><span id="ERROR_DEPENDENT_RESOURCE_EXISTS"></span><span id="error_dependent_resource_exists"></span>**ERROR\_DEPENDENT\_RESOURCE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-447">5001 (0X1389)</span><span class="sxs-lookup"><span data-stu-id="0a486-447">5001 (0x1389)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-448">Non è possibile completare l'operazione perché altre risorse dipendono da questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a486-448">The operation cannot be completed because other resources are dependent on this resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-449"><span id="ERROR_DEPENDENCY_NOT_FOUND"></span><span id="error_dependency_not_found"></span>**\_dipendenza errore \_ non \_ trovata**</span><span class="sxs-lookup"><span data-stu-id="0a486-449"><span id="ERROR_DEPENDENCY_NOT_FOUND"></span><span id="error_dependency_not_found"></span>**ERROR\_DEPENDENCY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-450">5002 (0x138A)</span><span class="sxs-lookup"><span data-stu-id="0a486-450">5002 (0x138A)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-451">Impossibile trovare la dipendenza della risorsa cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-451">The cluster resource dependency cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-452"><span id="ERROR_DEPENDENCY_ALREADY_EXISTS"></span><span id="error_dependency_already_exists"></span>**dipendenza di errore \_ \_ già \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="0a486-452"><span id="ERROR_DEPENDENCY_ALREADY_EXISTS"></span><span id="error_dependency_already_exists"></span>**ERROR\_DEPENDENCY\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-453">5003 (0x138B)</span><span class="sxs-lookup"><span data-stu-id="0a486-453">5003 (0x138B)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-454">La risorsa cluster non può essere resa dipendente dalla risorsa specificata perché è già dipendente.</span><span class="sxs-lookup"><span data-stu-id="0a486-454">The cluster resource cannot be made dependent on the specified resource because it is already dependent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-455"><span id="ERROR_RESOURCE_NOT_ONLINE"></span><span id="error_resource_not_online"></span>**\_risorsa errore \_ non in \_ linea**</span><span class="sxs-lookup"><span data-stu-id="0a486-455"><span id="ERROR_RESOURCE_NOT_ONLINE"></span><span id="error_resource_not_online"></span>**ERROR\_RESOURCE\_NOT\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-456">5004 (0x138C)</span><span class="sxs-lookup"><span data-stu-id="0a486-456">5004 (0x138C)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-457">La risorsa cluster non è online.</span><span class="sxs-lookup"><span data-stu-id="0a486-457">The cluster resource is not online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-458"><span id="ERROR_HOST_NODE_NOT_AVAILABLE"></span><span id="error_host_node_not_available"></span>**\_nodo host di errore \_ \_ non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="0a486-458"><span id="ERROR_HOST_NODE_NOT_AVAILABLE"></span><span id="error_host_node_not_available"></span>**ERROR\_HOST\_NODE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-459">5005 (0x138D)</span><span class="sxs-lookup"><span data-stu-id="0a486-459">5005 (0x138D)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-460">Un nodo del cluster non è disponibile per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="0a486-460">A cluster node is not available for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-461"><span id="ERROR_RESOURCE_NOT_AVAILABLE"></span><span id="error_resource_not_available"></span>**\_risorsa errore \_ non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="0a486-461"><span id="ERROR_RESOURCE_NOT_AVAILABLE"></span><span id="error_resource_not_available"></span>**ERROR\_RESOURCE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-462">5006 (0x138E)</span><span class="sxs-lookup"><span data-stu-id="0a486-462">5006 (0x138E)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-463">La risorsa cluster non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="0a486-463">The cluster resource is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-464"><span id="ERROR_RESOURCE_NOT_FOUND"></span><span id="error_resource_not_found"></span>**\_risorsa errore \_ non \_ trovata**</span><span class="sxs-lookup"><span data-stu-id="0a486-464"><span id="ERROR_RESOURCE_NOT_FOUND"></span><span id="error_resource_not_found"></span>**ERROR\_RESOURCE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-465">5007 (0x138F)</span><span class="sxs-lookup"><span data-stu-id="0a486-465">5007 (0x138F)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-466">Impossibile trovare la risorsa cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-466">The cluster resource could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-467"><span id="ERROR_SHUTDOWN_CLUSTER"></span><span id="error_shutdown_cluster"></span>**ERRORE di \_ arresto del \_ cluster**</span><span class="sxs-lookup"><span data-stu-id="0a486-467"><span id="ERROR_SHUTDOWN_CLUSTER"></span><span id="error_shutdown_cluster"></span>**ERROR\_SHUTDOWN\_CLUSTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-468">5008 (0x1390)</span><span class="sxs-lookup"><span data-stu-id="0a486-468">5008 (0x1390)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-469">È in corso l'arresto del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-469">The cluster is being shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-470"><span id="ERROR_CANT_EVICT_ACTIVE_NODE"></span><span id="error_cant_evict_active_node"></span>**errore durante la \_ \_ rimozione del \_ \_ nodo attivo**</span><span class="sxs-lookup"><span data-stu-id="0a486-470"><span id="ERROR_CANT_EVICT_ACTIVE_NODE"></span><span id="error_cant_evict_active_node"></span>**ERROR\_CANT\_EVICT\_ACTIVE\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-471">5009 (0x1391)</span><span class="sxs-lookup"><span data-stu-id="0a486-471">5009 (0x1391)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-472">Un nodo del cluster non può essere rimosso dal cluster, a meno che il nodo non sia attivo o sia l'ultimo nodo.</span><span class="sxs-lookup"><span data-stu-id="0a486-472">A cluster node cannot be evicted from the cluster unless the node is down or it is the last node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-473"><span id="ERROR_OBJECT_ALREADY_EXISTS"></span><span id="error_object_already_exists"></span>**l' \_ oggetto \_ Error \_ esiste già**</span><span class="sxs-lookup"><span data-stu-id="0a486-473"><span id="ERROR_OBJECT_ALREADY_EXISTS"></span><span id="error_object_already_exists"></span>**ERROR\_OBJECT\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-474">5010 (0x1392)</span><span class="sxs-lookup"><span data-stu-id="0a486-474">5010 (0x1392)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-475">L'oggetto esiste già.</span><span class="sxs-lookup"><span data-stu-id="0a486-475">The object already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-476"><span id="ERROR_OBJECT_IN_LIST"></span><span id="error_object_in_list"></span>**\_oggetto Error \_ nell' \_ elenco**</span><span class="sxs-lookup"><span data-stu-id="0a486-476"><span id="ERROR_OBJECT_IN_LIST"></span><span id="error_object_in_list"></span>**ERROR\_OBJECT\_IN\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-477">5011 (0x1393)</span><span class="sxs-lookup"><span data-stu-id="0a486-477">5011 (0x1393)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-478">L'oggetto è già presente nell'elenco.</span><span class="sxs-lookup"><span data-stu-id="0a486-478">The object is already in the list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-479"><span id="ERROR_GROUP_NOT_AVAILABLE"></span><span id="error_group_not_available"></span>**\_gruppo errori \_ non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="0a486-479"><span id="ERROR_GROUP_NOT_AVAILABLE"></span><span id="error_group_not_available"></span>**ERROR\_GROUP\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-480">5012 (0x1394)</span><span class="sxs-lookup"><span data-stu-id="0a486-480">5012 (0x1394)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-481">Il gruppo cluster non è disponibile per le nuove richieste.</span><span class="sxs-lookup"><span data-stu-id="0a486-481">The cluster group is not available for any new requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-482"><span id="ERROR_GROUP_NOT_FOUND"></span><span id="error_group_not_found"></span>**\_ \_ Impossibile trovare il gruppo di errori \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-482"><span id="ERROR_GROUP_NOT_FOUND"></span><span id="error_group_not_found"></span>**ERROR\_GROUP\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-483">5013 (0x1395)</span><span class="sxs-lookup"><span data-stu-id="0a486-483">5013 (0x1395)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-484">Impossibile trovare il gruppo cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-484">The cluster group could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-485"><span id="ERROR_GROUP_NOT_ONLINE"></span><span id="error_group_not_online"></span>**\_gruppo errori \_ non in \_ linea**</span><span class="sxs-lookup"><span data-stu-id="0a486-485"><span id="ERROR_GROUP_NOT_ONLINE"></span><span id="error_group_not_online"></span>**ERROR\_GROUP\_NOT\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-486">5014 (0x1396)</span><span class="sxs-lookup"><span data-stu-id="0a486-486">5014 (0x1396)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-487">Non è stato possibile completare l'operazione perché il gruppo cluster non è online.</span><span class="sxs-lookup"><span data-stu-id="0a486-487">The operation could not be completed because the cluster group is not online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-488"><span id="ERROR_HOST_NODE_NOT_RESOURCE_OWNER"></span><span id="error_host_node_not_resource_owner"></span>**\_nodo host \_ errore \_ non \_ \_ proprietario risorsa**</span><span class="sxs-lookup"><span data-stu-id="0a486-488"><span id="ERROR_HOST_NODE_NOT_RESOURCE_OWNER"></span><span id="error_host_node_not_resource_owner"></span>**ERROR\_HOST\_NODE\_NOT\_RESOURCE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-489">5015 (0x1397)</span><span class="sxs-lookup"><span data-stu-id="0a486-489">5015 (0x1397)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-490">L'operazione non è riuscita perché il nodo del cluster specificato non è il proprietario della risorsa o il nodo non è un possibile proprietario della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a486-490">The operation failed because either the specified cluster node is not the owner of the resource, or the node is not a possible owner of the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-491"><span id="ERROR_HOST_NODE_NOT_GROUP_OWNER"></span><span id="error_host_node_not_group_owner"></span>**ERRORE \_ del \_ nodo \_ host \_ non \_ proprietario del gruppo**</span><span class="sxs-lookup"><span data-stu-id="0a486-491"><span id="ERROR_HOST_NODE_NOT_GROUP_OWNER"></span><span id="error_host_node_not_group_owner"></span>**ERROR\_HOST\_NODE\_NOT\_GROUP\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-492">5016 (0x1398)</span><span class="sxs-lookup"><span data-stu-id="0a486-492">5016 (0x1398)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-493">Operazione non riuscita. Il gruppo non è di proprietà del nodo di cluster specificato o il nodo non è un possibile proprietario del gruppo.</span><span class="sxs-lookup"><span data-stu-id="0a486-493">The operation failed because either the specified cluster node is not the owner of the group, or the node is not a possible owner of the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-494"><span id="ERROR_RESMON_CREATE_FAILED"></span><span id="error_resmon_create_failed"></span>**ERRORE \_ di \_ creazione resmon \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="0a486-494"><span id="ERROR_RESMON_CREATE_FAILED"></span><span id="error_resmon_create_failed"></span>**ERROR\_RESMON\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-495">5017 (0x1399)</span><span class="sxs-lookup"><span data-stu-id="0a486-495">5017 (0x1399)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-496">Impossibile creare la risorsa cluster nel monitoraggio risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="0a486-496">The cluster resource could not be created in the specified resource monitor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-497"><span id="ERROR_RESMON_ONLINE_FAILED"></span><span id="error_resmon_online_failed"></span>**ERRORE \_ resmon \_ online \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="0a486-497"><span id="ERROR_RESMON_ONLINE_FAILED"></span><span id="error_resmon_online_failed"></span>**ERROR\_RESMON\_ONLINE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-498">5018 (0x139A)</span><span class="sxs-lookup"><span data-stu-id="0a486-498">5018 (0x139A)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-499">Impossibile portare in linea la risorsa cluster dal monitoraggio risorse.</span><span class="sxs-lookup"><span data-stu-id="0a486-499">The cluster resource could not be brought online by the resource monitor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-500"><span id="ERROR_RESOURCE_ONLINE"></span><span id="error_resource_online"></span>**\_risorsa errore \_ online**</span><span class="sxs-lookup"><span data-stu-id="0a486-500"><span id="ERROR_RESOURCE_ONLINE"></span><span id="error_resource_online"></span>**ERROR\_RESOURCE\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-501">5019 (0x139B)</span><span class="sxs-lookup"><span data-stu-id="0a486-501">5019 (0x139B)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-502">Non è stato possibile completare l'operazione perché la risorsa cluster è online.</span><span class="sxs-lookup"><span data-stu-id="0a486-502">The operation could not be completed because the cluster resource is online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-503"><span id="ERROR_QUORUM_RESOURCE"></span><span id="error_quorum_resource"></span>**ERRORE \_ di \_ risorsa quorum**</span><span class="sxs-lookup"><span data-stu-id="0a486-503"><span id="ERROR_QUORUM_RESOURCE"></span><span id="error_quorum_resource"></span>**ERROR\_QUORUM\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-504">5020 (0x139C)</span><span class="sxs-lookup"><span data-stu-id="0a486-504">5020 (0x139C)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-505">Non è stato possibile eliminare o portare offline la risorsa cluster perché è la risorsa quorum.</span><span class="sxs-lookup"><span data-stu-id="0a486-505">The cluster resource could not be deleted or brought offline because it is the quorum resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-506"><span id="ERROR_NOT_QUORUM_CAPABLE"></span><span id="error_not_quorum_capable"></span>**ERRORE \_ non \_ idoneo per il quorum \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-506"><span id="ERROR_NOT_QUORUM_CAPABLE"></span><span id="error_not_quorum_capable"></span>**ERROR\_NOT\_QUORUM\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-507">5021 (0x139D)</span><span class="sxs-lookup"><span data-stu-id="0a486-507">5021 (0x139D)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-508">Il cluster non è riuscito a rendere la risorsa specificata una risorsa quorum perché non è in grado di essere una risorsa quorum.</span><span class="sxs-lookup"><span data-stu-id="0a486-508">The cluster could not make the specified resource a quorum resource because it is not capable of being a quorum resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-509"><span id="ERROR_CLUSTER_SHUTTING_DOWN"></span><span id="error_cluster_shutting_down"></span>**ERRORE \_ di \_ arresto del \_ cluster**</span><span class="sxs-lookup"><span data-stu-id="0a486-509"><span id="ERROR_CLUSTER_SHUTTING_DOWN"></span><span id="error_cluster_shutting_down"></span>**ERROR\_CLUSTER\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-510">5022 (0x139E)</span><span class="sxs-lookup"><span data-stu-id="0a486-510">5022 (0x139E)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-511">È in corso l'arresto del software del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-511">The cluster software is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-512"><span id="ERROR_INVALID_STATE"></span><span id="error_invalid_state"></span>**ERRORE \_ di \_ stato non valido**</span><span class="sxs-lookup"><span data-stu-id="0a486-512"><span id="ERROR_INVALID_STATE"></span><span id="error_invalid_state"></span>**ERROR\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-513">5023 (0x139F)</span><span class="sxs-lookup"><span data-stu-id="0a486-513">5023 (0x139F)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-514">Il gruppo o la risorsa non si trova nello stato corretto per eseguire l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="0a486-514">The group or resource is not in the correct state to perform the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-515"><span id="ERROR_RESOURCE_PROPERTIES_STORED"></span><span id="error_resource_properties_stored"></span>**\_proprietà delle risorse di errore \_ \_ archiviate**</span><span class="sxs-lookup"><span data-stu-id="0a486-515"><span id="ERROR_RESOURCE_PROPERTIES_STORED"></span><span id="error_resource_properties_stored"></span>**ERROR\_RESOURCE\_PROPERTIES\_STORED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-516">5024 (0x13A0)</span><span class="sxs-lookup"><span data-stu-id="0a486-516">5024 (0x13A0)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-517">Le proprietà sono state archiviate, ma non tutte le modifiche saranno effettive fino alla successiva porta online della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a486-517">The properties were stored but not all changes will take effect until the next time the resource is brought online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-518"><span id="ERROR_NOT_QUORUM_CLASS"></span><span id="error_not_quorum_class"></span>**ERRORE \_ di \_ classe del quorum \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-518"><span id="ERROR_NOT_QUORUM_CLASS"></span><span id="error_not_quorum_class"></span>**ERROR\_NOT\_QUORUM\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-519">5025 (0x13A1)</span><span class="sxs-lookup"><span data-stu-id="0a486-519">5025 (0x13A1)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-520">Il cluster non è riuscito a rendere la risorsa specificata una risorsa quorum perché non appartiene a una classe di archiviazione condivisa.</span><span class="sxs-lookup"><span data-stu-id="0a486-520">The cluster could not make the specified resource a quorum resource because it does not belong to a shared storage class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-521"><span id="ERROR_CORE_RESOURCE"></span><span id="error_core_resource"></span>**\_risorsa principale \_ errore**</span><span class="sxs-lookup"><span data-stu-id="0a486-521"><span id="ERROR_CORE_RESOURCE"></span><span id="error_core_resource"></span>**ERROR\_CORE\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-522">5026 (0x13A2)</span><span class="sxs-lookup"><span data-stu-id="0a486-522">5026 (0x13A2)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-523">Non è stato possibile eliminare la risorsa cluster perché è una risorsa principale.</span><span class="sxs-lookup"><span data-stu-id="0a486-523">The cluster resource could not be deleted since it is a core resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-524"><span id="ERROR_QUORUM_RESOURCE_ONLINE_FAILED"></span><span id="error_quorum_resource_online_failed"></span>**ERRORE \_ di \_ risorsa quorum \_ online \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="0a486-524"><span id="ERROR_QUORUM_RESOURCE_ONLINE_FAILED"></span><span id="error_quorum_resource_online_failed"></span>**ERROR\_QUORUM\_RESOURCE\_ONLINE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-525">5027 (0x13A3)</span><span class="sxs-lookup"><span data-stu-id="0a486-525">5027 (0x13A3)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-526">La risorsa quorum non è riuscita a tornare in linea.</span><span class="sxs-lookup"><span data-stu-id="0a486-526">The quorum resource failed to come online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-527"><span id="ERROR_QUORUMLOG_OPEN_FAILED"></span><span id="error_quorumlog_open_failed"></span>**ERRORE \_ QUORUMLOG \_ apertura \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="0a486-527"><span id="ERROR_QUORUMLOG_OPEN_FAILED"></span><span id="error_quorumlog_open_failed"></span>**ERROR\_QUORUMLOG\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-528">5028 (0x13A4)</span><span class="sxs-lookup"><span data-stu-id="0a486-528">5028 (0x13A4)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-529">Impossibile creare o montare correttamente il registro quorum.</span><span class="sxs-lookup"><span data-stu-id="0a486-529">The quorum log could not be created or mounted successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-530"><span id="ERROR_CLUSTERLOG_CORRUPT"></span><span id="error_clusterlog_corrupt"></span>**ERRORE \_ CLUSTERLOG \_ danneggiato**</span><span class="sxs-lookup"><span data-stu-id="0a486-530"><span id="ERROR_CLUSTERLOG_CORRUPT"></span><span id="error_clusterlog_corrupt"></span>**ERROR\_CLUSTERLOG\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-531">5029 (0x13A5)</span><span class="sxs-lookup"><span data-stu-id="0a486-531">5029 (0x13A5)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-532">Il log del cluster è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="0a486-532">The cluster log is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-533"><span id="ERROR_CLUSTERLOG_RECORD_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_record_exceeds_maxsize"></span>**ERRORE \_ \_ record CLUSTERLOG \_ superiore a \_ MaxSize**</span><span class="sxs-lookup"><span data-stu-id="0a486-533"><span id="ERROR_CLUSTERLOG_RECORD_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_record_exceeds_maxsize"></span>**ERROR\_CLUSTERLOG\_RECORD\_EXCEEDS\_MAXSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-534">5030 (0x13A6)</span><span class="sxs-lookup"><span data-stu-id="0a486-534">5030 (0x13A6)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-535">Impossibile scrivere il record nel log del cluster perché supera le dimensioni massime.</span><span class="sxs-lookup"><span data-stu-id="0a486-535">The record could not be written to the cluster log since it exceeds the maximum size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-536"><span id="ERROR_CLUSTERLOG_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_exceeds_maxsize"></span>**ERRORE \_ CLUSTERLOG \_ superiore a \_ MaxSize**</span><span class="sxs-lookup"><span data-stu-id="0a486-536"><span id="ERROR_CLUSTERLOG_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_exceeds_maxsize"></span>**ERROR\_CLUSTERLOG\_EXCEEDS\_MAXSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-537">5031 (0x13A7)</span><span class="sxs-lookup"><span data-stu-id="0a486-537">5031 (0x13A7)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-538">Il log del cluster supera le dimensioni massime.</span><span class="sxs-lookup"><span data-stu-id="0a486-538">The cluster log exceeds its maximum size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-539"><span id="ERROR_CLUSTERLOG_CHKPOINT_NOT_FOUND"></span><span id="error_clusterlog_chkpoint_not_found"></span>**ERRORE \_ CLUSTERLOG \_ CHKPOINT \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="0a486-539"><span id="ERROR_CLUSTERLOG_CHKPOINT_NOT_FOUND"></span><span id="error_clusterlog_chkpoint_not_found"></span>**ERROR\_CLUSTERLOG\_CHKPOINT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-540">5032 (0x13A8)</span><span class="sxs-lookup"><span data-stu-id="0a486-540">5032 (0x13A8)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-541">Nessun record del checkpoint trovato nel log del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-541">No checkpoint record was found in the cluster log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-542"><span id="ERROR_CLUSTERLOG_NOT_ENOUGH_SPACE"></span><span id="error_clusterlog_not_enough_space"></span>**ERRORE \_ CLUSTERLOG \_ \_ spazio insufficiente \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-542"><span id="ERROR_CLUSTERLOG_NOT_ENOUGH_SPACE"></span><span id="error_clusterlog_not_enough_space"></span>**ERROR\_CLUSTERLOG\_NOT\_ENOUGH\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-543">5033 (0x13A9)</span><span class="sxs-lookup"><span data-stu-id="0a486-543">5033 (0x13A9)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-544">Lo spazio su disco minimo necessario per la registrazione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="0a486-544">The minimum required disk space needed for logging is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-545"><span id="ERROR_QUORUM_OWNER_ALIVE"></span><span id="error_quorum_owner_alive"></span>**ERRORE \_ \_ proprietario quorum \_ attivo**</span><span class="sxs-lookup"><span data-stu-id="0a486-545"><span id="ERROR_QUORUM_OWNER_ALIVE"></span><span id="error_quorum_owner_alive"></span>**ERROR\_QUORUM\_OWNER\_ALIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-546">5034 (0x13AA)</span><span class="sxs-lookup"><span data-stu-id="0a486-546">5034 (0x13AA)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-547">Il nodo del cluster non è riuscito a assumere il controllo della risorsa quorum perché la risorsa è di proprietà di un altro nodo attivo.</span><span class="sxs-lookup"><span data-stu-id="0a486-547">The cluster node failed to take control of the quorum resource because the resource is owned by another active node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-548"><span id="ERROR_NETWORK_NOT_AVAILABLE"></span><span id="error_network_not_available"></span>**ERRORE di \_ rete \_ non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="0a486-548"><span id="ERROR_NETWORK_NOT_AVAILABLE"></span><span id="error_network_not_available"></span>**ERROR\_NETWORK\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-549">5035 (0x13AB)</span><span class="sxs-lookup"><span data-stu-id="0a486-549">5035 (0x13AB)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-550">Una rete cluster non è disponibile per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="0a486-550">A cluster network is not available for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-551"><span id="ERROR_NODE_NOT_AVAILABLE"></span><span id="error_node_not_available"></span>**\_nodo errore \_ non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="0a486-551"><span id="ERROR_NODE_NOT_AVAILABLE"></span><span id="error_node_not_available"></span>**ERROR\_NODE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-552">5036 (0x13AC)</span><span class="sxs-lookup"><span data-stu-id="0a486-552">5036 (0x13AC)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-553">Un nodo del cluster non è disponibile per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="0a486-553">A cluster node is not available for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-554"><span id="ERROR_ALL_NODES_NOT_AVAILABLE"></span><span id="error_all_nodes_not_available"></span>**ERRORE \_ tutti i \_ nodi \_ non \_ disponibili**</span><span class="sxs-lookup"><span data-stu-id="0a486-554"><span id="ERROR_ALL_NODES_NOT_AVAILABLE"></span><span id="error_all_nodes_not_available"></span>**ERROR\_ALL\_NODES\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-555">5037 (0x13AD)</span><span class="sxs-lookup"><span data-stu-id="0a486-555">5037 (0x13AD)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-556">Per eseguire questa operazione, è necessario che tutti i nodi del cluster siano in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="0a486-556">All cluster nodes must be running to perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-557"><span id="ERROR_RESOURCE_FAILED"></span><span id="error_resource_failed"></span>**ERRORE di \_ risorsa \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="0a486-557"><span id="ERROR_RESOURCE_FAILED"></span><span id="error_resource_failed"></span>**ERROR\_RESOURCE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-558">5038 (0x13AE)</span><span class="sxs-lookup"><span data-stu-id="0a486-558">5038 (0x13AE)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-559">Errore di una risorsa cluster</span><span class="sxs-lookup"><span data-stu-id="0a486-559">A cluster resource failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-560"><span id="ERROR_CLUSTER_INVALID_NODE"></span><span id="error_cluster_invalid_node"></span>**nodo del cluster di errore \_ \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-560"><span id="ERROR_CLUSTER_INVALID_NODE"></span><span id="error_cluster_invalid_node"></span>**ERROR\_CLUSTER\_INVALID\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-561">5039 (0x13AF)</span><span class="sxs-lookup"><span data-stu-id="0a486-561">5039 (0x13AF)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-562">Il nodo del cluster non è valido.</span><span class="sxs-lookup"><span data-stu-id="0a486-562">The cluster node is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-563"><span id="ERROR_CLUSTER_NODE_EXISTS"></span><span id="error_cluster_node_exists"></span>**nodo del cluster di errore \_ \_ \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="0a486-563"><span id="ERROR_CLUSTER_NODE_EXISTS"></span><span id="error_cluster_node_exists"></span>**ERROR\_CLUSTER\_NODE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-564">5040 (0x13B0)</span><span class="sxs-lookup"><span data-stu-id="0a486-564">5040 (0x13B0)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-565">Il nodo del cluster esiste già.</span><span class="sxs-lookup"><span data-stu-id="0a486-565">The cluster node already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-566"><span id="ERROR_CLUSTER_JOIN_IN_PROGRESS"></span><span id="error_cluster_join_in_progress"></span>**ERRORE \_ \_ di join \_ del cluster in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="0a486-566"><span id="ERROR_CLUSTER_JOIN_IN_PROGRESS"></span><span id="error_cluster_join_in_progress"></span>**ERROR\_CLUSTER\_JOIN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-567">5041 (0x13B1)</span><span class="sxs-lookup"><span data-stu-id="0a486-567">5041 (0x13B1)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-568">Un nodo è in corso di aggiunta al cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-568">A node is in the process of joining the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-569"><span id="ERROR_CLUSTER_NODE_NOT_FOUND"></span><span id="error_cluster_node_not_found"></span>**nodo del cluster di errore \_ \_ \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="0a486-569"><span id="ERROR_CLUSTER_NODE_NOT_FOUND"></span><span id="error_cluster_node_not_found"></span>**ERROR\_CLUSTER\_NODE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-570">5042 (0x13B2)</span><span class="sxs-lookup"><span data-stu-id="0a486-570">5042 (0x13B2)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-571">Impossibile trovare il nodo del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-571">The cluster node was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-572"><span id="ERROR_CLUSTER_LOCAL_NODE_NOT_FOUND"></span><span id="error_cluster_local_node_not_found"></span>**\_ \_ nodo locale del cluster di errore \_ \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="0a486-572"><span id="ERROR_CLUSTER_LOCAL_NODE_NOT_FOUND"></span><span id="error_cluster_local_node_not_found"></span>**ERROR\_CLUSTER\_LOCAL\_NODE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-573">5043 (0x13B3)</span><span class="sxs-lookup"><span data-stu-id="0a486-573">5043 (0x13B3)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-574">Impossibile trovare le informazioni sul nodo locale del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-574">The cluster local node information was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-575"><span id="ERROR_CLUSTER_NETWORK_EXISTS"></span><span id="error_cluster_network_exists"></span>**ERRORE \_ \_ rete cluster \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="0a486-575"><span id="ERROR_CLUSTER_NETWORK_EXISTS"></span><span id="error_cluster_network_exists"></span>**ERROR\_CLUSTER\_NETWORK\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-576">5044 (0x13B4)</span><span class="sxs-lookup"><span data-stu-id="0a486-576">5044 (0x13B4)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-577">La rete cluster esiste già.</span><span class="sxs-lookup"><span data-stu-id="0a486-577">The cluster network already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-578"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND"></span><span id="error_cluster_network_not_found"></span>**ERRORE \_ di \_ rete cluster \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="0a486-578"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND"></span><span id="error_cluster_network_not_found"></span>**ERROR\_CLUSTER\_NETWORK\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-579">5045 (0x13B5)</span><span class="sxs-lookup"><span data-stu-id="0a486-579">5045 (0x13B5)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-580">Impossibile trovare la rete cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-580">The cluster network was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-581"><span id="ERROR_CLUSTER_NETINTERFACE_EXISTS"></span><span id="error_cluster_netinterface_exists"></span>**ERRORE del \_ cluster \_ NETINTERFACE \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="0a486-581"><span id="ERROR_CLUSTER_NETINTERFACE_EXISTS"></span><span id="error_cluster_netinterface_exists"></span>**ERROR\_CLUSTER\_NETINTERFACE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-582">5046 (0x13B6)</span><span class="sxs-lookup"><span data-stu-id="0a486-582">5046 (0x13B6)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-583">L'interfaccia di rete del cluster esiste già.</span><span class="sxs-lookup"><span data-stu-id="0a486-583">The cluster network interface already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-584"><span id="ERROR_CLUSTER_NETINTERFACE_NOT_FOUND"></span><span id="error_cluster_netinterface_not_found"></span>**ERRORE \_ cluster \_ NETINTERFACE \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="0a486-584"><span id="ERROR_CLUSTER_NETINTERFACE_NOT_FOUND"></span><span id="error_cluster_netinterface_not_found"></span>**ERROR\_CLUSTER\_NETINTERFACE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-585">5047 (0x13B7)</span><span class="sxs-lookup"><span data-stu-id="0a486-585">5047 (0x13B7)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-586">Impossibile trovare l'interfaccia di rete cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-586">The cluster network interface was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-587"><span id="ERROR_CLUSTER_INVALID_REQUEST"></span><span id="error_cluster_invalid_request"></span>**\_ \_ richiesta non valida del cluster di errori \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-587"><span id="ERROR_CLUSTER_INVALID_REQUEST"></span><span id="error_cluster_invalid_request"></span>**ERROR\_CLUSTER\_INVALID\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-588">5048 (0x13B8)</span><span class="sxs-lookup"><span data-stu-id="0a486-588">5048 (0x13B8)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-589">La richiesta del cluster non è valida per questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="0a486-589">The cluster request is not valid for this object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-590"><span id="ERROR_CLUSTER_INVALID_NETWORK_PROVIDER"></span><span id="error_cluster_invalid_network_provider"></span>**ERRORE \_ cluster \_ \_ provider di rete non valido \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-590"><span id="ERROR_CLUSTER_INVALID_NETWORK_PROVIDER"></span><span id="error_cluster_invalid_network_provider"></span>**ERROR\_CLUSTER\_INVALID\_NETWORK\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-591">5049 (0x13B9)</span><span class="sxs-lookup"><span data-stu-id="0a486-591">5049 (0x13B9)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-592">Il provider di rete cluster non è valido.</span><span class="sxs-lookup"><span data-stu-id="0a486-592">The cluster network provider is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-593"><span id="ERROR_CLUSTER_NODE_DOWN"></span><span id="error_cluster_node_down"></span>**nodo del cluster di errore \_ \_ \_ inattivo**</span><span class="sxs-lookup"><span data-stu-id="0a486-593"><span id="ERROR_CLUSTER_NODE_DOWN"></span><span id="error_cluster_node_down"></span>**ERROR\_CLUSTER\_NODE\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-594">5050 (0x13BA)</span><span class="sxs-lookup"><span data-stu-id="0a486-594">5050 (0x13BA)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-595">Il nodo del cluster è inattivo.</span><span class="sxs-lookup"><span data-stu-id="0a486-595">The cluster node is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-596"><span id="ERROR_CLUSTER_NODE_UNREACHABLE"></span><span id="error_cluster_node_unreachable"></span>**ERRORE del \_ nodo del cluster non \_ \_ raggiungibile**</span><span class="sxs-lookup"><span data-stu-id="0a486-596"><span id="ERROR_CLUSTER_NODE_UNREACHABLE"></span><span id="error_cluster_node_unreachable"></span>**ERROR\_CLUSTER\_NODE\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-597">5051 (0x13BB)</span><span class="sxs-lookup"><span data-stu-id="0a486-597">5051 (0x13BB)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-598">Il nodo del cluster non è raggiungibile.</span><span class="sxs-lookup"><span data-stu-id="0a486-598">The cluster node is not reachable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-599"><span id="ERROR_CLUSTER_NODE_NOT_MEMBER"></span><span id="error_cluster_node_not_member"></span>**nodo del cluster di errore \_ \_ \_ non \_ membro**</span><span class="sxs-lookup"><span data-stu-id="0a486-599"><span id="ERROR_CLUSTER_NODE_NOT_MEMBER"></span><span id="error_cluster_node_not_member"></span>**ERROR\_CLUSTER\_NODE\_NOT\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-600">5052 (0x13BC)</span><span class="sxs-lookup"><span data-stu-id="0a486-600">5052 (0x13BC)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-601">Il nodo del cluster non è un membro del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-601">The cluster node is not a member of the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-602"><span id="ERROR_CLUSTER_JOIN_NOT_IN_PROGRESS"></span><span id="error_cluster_join_not_in_progress"></span>**ERRORE \_ \_ di join \_ del cluster non \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="0a486-602"><span id="ERROR_CLUSTER_JOIN_NOT_IN_PROGRESS"></span><span id="error_cluster_join_not_in_progress"></span>**ERROR\_CLUSTER\_JOIN\_NOT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-603">5053 (0x13BD)</span><span class="sxs-lookup"><span data-stu-id="0a486-603">5053 (0x13BD)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-604">Un'operazione di join del cluster non è in corso.</span><span class="sxs-lookup"><span data-stu-id="0a486-604">A cluster join operation is not in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-605"><span id="ERROR_CLUSTER_INVALID_NETWORK"></span><span id="error_cluster_invalid_network"></span>**ERRORE \_ cluster \_ rete non valida \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-605"><span id="ERROR_CLUSTER_INVALID_NETWORK"></span><span id="error_cluster_invalid_network"></span>**ERROR\_CLUSTER\_INVALID\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-606">5054 (0x13BE)</span><span class="sxs-lookup"><span data-stu-id="0a486-606">5054 (0x13BE)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-607">Rete cluster non valida.</span><span class="sxs-lookup"><span data-stu-id="0a486-607">The cluster network is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-608"><span id="ERROR_CLUSTER_NODE_UP"></span><span id="error_cluster_node_up"></span>**nodo del cluster di errore \_ \_ \_ attivo**</span><span class="sxs-lookup"><span data-stu-id="0a486-608"><span id="ERROR_CLUSTER_NODE_UP"></span><span id="error_cluster_node_up"></span>**ERROR\_CLUSTER\_NODE\_UP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-609">5056 (0x13C0)</span><span class="sxs-lookup"><span data-stu-id="0a486-609">5056 (0x13C0)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-610">Il nodo del cluster è attivo.</span><span class="sxs-lookup"><span data-stu-id="0a486-610">The cluster node is up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-611"><span id="ERROR_CLUSTER_IPADDR_IN_USE"></span><span id="error_cluster_ipaddr_in_use"></span>**ERRORE \_ \_ del cluster IPADDR \_ in \_ uso**</span><span class="sxs-lookup"><span data-stu-id="0a486-611"><span id="ERROR_CLUSTER_IPADDR_IN_USE"></span><span id="error_cluster_ipaddr_in_use"></span>**ERROR\_CLUSTER\_IPADDR\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-612">5057 (0x13C1)</span><span class="sxs-lookup"><span data-stu-id="0a486-612">5057 (0x13C1)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-613">L'indirizzo IP del cluster è già in uso.</span><span class="sxs-lookup"><span data-stu-id="0a486-613">The cluster IP address is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-614"><span id="ERROR_CLUSTER_NODE_NOT_PAUSED"></span><span id="error_cluster_node_not_paused"></span>**nodo del cluster di errore \_ \_ \_ non \_ sospeso**</span><span class="sxs-lookup"><span data-stu-id="0a486-614"><span id="ERROR_CLUSTER_NODE_NOT_PAUSED"></span><span id="error_cluster_node_not_paused"></span>**ERROR\_CLUSTER\_NODE\_NOT\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-615">5058 (0x13C2)</span><span class="sxs-lookup"><span data-stu-id="0a486-615">5058 (0x13C2)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-616">Il nodo del cluster non è sospeso.</span><span class="sxs-lookup"><span data-stu-id="0a486-616">The cluster node is not paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-617"><span id="ERROR_CLUSTER_NO_SECURITY_CONTEXT"></span><span id="error_cluster_no_security_context"></span>**ERRORE \_ nel \_ cluster \_ senza \_ contesto di sicurezza**</span><span class="sxs-lookup"><span data-stu-id="0a486-617"><span id="ERROR_CLUSTER_NO_SECURITY_CONTEXT"></span><span id="error_cluster_no_security_context"></span>**ERROR\_CLUSTER\_NO\_SECURITY\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-618">5059 (0x13C3)</span><span class="sxs-lookup"><span data-stu-id="0a486-618">5059 (0x13C3)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-619">Non è disponibile alcun contesto di sicurezza del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-619">No cluster security context is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-620"><span id="ERROR_CLUSTER_NETWORK_NOT_INTERNAL"></span><span id="error_cluster_network_not_internal"></span>**ERRORE \_ di \_ rete del cluster \_ non \_ interno**</span><span class="sxs-lookup"><span data-stu-id="0a486-620"><span id="ERROR_CLUSTER_NETWORK_NOT_INTERNAL"></span><span id="error_cluster_network_not_internal"></span>**ERROR\_CLUSTER\_NETWORK\_NOT\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-621">5060 (0x13C4)</span><span class="sxs-lookup"><span data-stu-id="0a486-621">5060 (0x13C4)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-622">La rete cluster non è configurata per la comunicazione interna del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-622">The cluster network is not configured for internal cluster communication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-623"><span id="ERROR_CLUSTER_NODE_ALREADY_UP"></span><span id="error_cluster_node_already_up"></span>**nodo del cluster di errore \_ \_ \_ già \_ attivo**</span><span class="sxs-lookup"><span data-stu-id="0a486-623"><span id="ERROR_CLUSTER_NODE_ALREADY_UP"></span><span id="error_cluster_node_already_up"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_UP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-624">5061 (0x13C5)</span><span class="sxs-lookup"><span data-stu-id="0a486-624">5061 (0x13C5)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-625">Il nodo del cluster è già attivo.</span><span class="sxs-lookup"><span data-stu-id="0a486-625">The cluster node is already up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-626"><span id="ERROR_CLUSTER_NODE_ALREADY_DOWN"></span><span id="error_cluster_node_already_down"></span>**nodo del cluster di errore \_ \_ \_ già \_ attivo**</span><span class="sxs-lookup"><span data-stu-id="0a486-626"><span id="ERROR_CLUSTER_NODE_ALREADY_DOWN"></span><span id="error_cluster_node_already_down"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-627">5062 (0x13C6)</span><span class="sxs-lookup"><span data-stu-id="0a486-627">5062 (0x13C6)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-628">Il nodo del cluster è già inattivo.</span><span class="sxs-lookup"><span data-stu-id="0a486-628">The cluster node is already down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-629"><span id="ERROR_CLUSTER_NETWORK_ALREADY_ONLINE"></span><span id="error_cluster_network_already_online"></span>**\_rete cluster di errore \_ \_ già \_ online**</span><span class="sxs-lookup"><span data-stu-id="0a486-629"><span id="ERROR_CLUSTER_NETWORK_ALREADY_ONLINE"></span><span id="error_cluster_network_already_online"></span>**ERROR\_CLUSTER\_NETWORK\_ALREADY\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-630">5063 (0x13C7)</span><span class="sxs-lookup"><span data-stu-id="0a486-630">5063 (0x13C7)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-631">La rete cluster è già online.</span><span class="sxs-lookup"><span data-stu-id="0a486-631">The cluster network is already online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-632"><span id="ERROR_CLUSTER_NETWORK_ALREADY_OFFLINE"></span><span id="error_cluster_network_already_offline"></span>**\_rete cluster di errore \_ \_ già \_ offline**</span><span class="sxs-lookup"><span data-stu-id="0a486-632"><span id="ERROR_CLUSTER_NETWORK_ALREADY_OFFLINE"></span><span id="error_cluster_network_already_offline"></span>**ERROR\_CLUSTER\_NETWORK\_ALREADY\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-633">5064 (0x13C8)</span><span class="sxs-lookup"><span data-stu-id="0a486-633">5064 (0x13C8)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-634">La rete cluster è già offline.</span><span class="sxs-lookup"><span data-stu-id="0a486-634">The cluster network is already offline.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-635"><span id="ERROR_CLUSTER_NODE_ALREADY_MEMBER"></span><span id="error_cluster_node_already_member"></span>**nodo del cluster di errore \_ \_ \_ già \_ membro**</span><span class="sxs-lookup"><span data-stu-id="0a486-635"><span id="ERROR_CLUSTER_NODE_ALREADY_MEMBER"></span><span id="error_cluster_node_already_member"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-636">5065 (0x13C9)</span><span class="sxs-lookup"><span data-stu-id="0a486-636">5065 (0x13C9)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-637">Il nodo del cluster è già membro del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-637">The cluster node is already a member of the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-638"><span id="ERROR_CLUSTER_LAST_INTERNAL_NETWORK"></span><span id="error_cluster_last_internal_network"></span>**\_ \_ Ultima \_ rete interna cluster \_ errori**</span><span class="sxs-lookup"><span data-stu-id="0a486-638"><span id="ERROR_CLUSTER_LAST_INTERNAL_NETWORK"></span><span id="error_cluster_last_internal_network"></span>**ERROR\_CLUSTER\_LAST\_INTERNAL\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-639">5066 (0x13CA)</span><span class="sxs-lookup"><span data-stu-id="0a486-639">5066 (0x13CA)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-640">La rete cluster è l'unico configurato per la comunicazione interna del cluster tra due o più nodi del cluster attivi.</span><span class="sxs-lookup"><span data-stu-id="0a486-640">The cluster network is the only one configured for internal cluster communication between two or more active cluster nodes.</span></span> <span data-ttu-id="0a486-641">Impossibile rimuovere dalla rete la funzionalità di comunicazione interna.</span><span class="sxs-lookup"><span data-stu-id="0a486-641">The internal communication capability cannot be removed from the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-642"><span id="ERROR_CLUSTER_NETWORK_HAS_DEPENDENTS"></span><span id="error_cluster_network_has_dependents"></span>**ERRORE \_ della \_ rete cluster \_ con \_ dipendenti**</span><span class="sxs-lookup"><span data-stu-id="0a486-642"><span id="ERROR_CLUSTER_NETWORK_HAS_DEPENDENTS"></span><span id="error_cluster_network_has_dependents"></span>**ERROR\_CLUSTER\_NETWORK\_HAS\_DEPENDENTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-643">5067 (0x13CB)</span><span class="sxs-lookup"><span data-stu-id="0a486-643">5067 (0x13CB)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-644">Una o più risorse cluster dipendono dalla rete per fornire il servizio ai client.</span><span class="sxs-lookup"><span data-stu-id="0a486-644">One or more cluster resources depend on the network to provide service to clients.</span></span> <span data-ttu-id="0a486-645">Non è possibile rimuovere la funzionalità di accesso client dalla rete.</span><span class="sxs-lookup"><span data-stu-id="0a486-645">The client access capability cannot be removed from the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-646"><span id="ERROR_INVALID_OPERATION_ON_QUORUM"></span><span id="error_invalid_operation_on_quorum"></span>**ERRORE \_ operazione non valida \_ \_ sul \_ quorum**</span><span class="sxs-lookup"><span data-stu-id="0a486-646"><span id="ERROR_INVALID_OPERATION_ON_QUORUM"></span><span id="error_invalid_operation_on_quorum"></span>**ERROR\_INVALID\_OPERATION\_ON\_QUORUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-647">5068 (0x13CC)</span><span class="sxs-lookup"><span data-stu-id="0a486-647">5068 (0x13CC)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-648">Questa operazione non può essere eseguita sulla risorsa cluster come risorsa quorum.</span><span class="sxs-lookup"><span data-stu-id="0a486-648">This operation cannot be performed on the cluster resource as it the quorum resource.</span></span> <span data-ttu-id="0a486-649">Non è possibile portare offline la risorsa quorum o modificare il relativo elenco di proprietari.</span><span class="sxs-lookup"><span data-stu-id="0a486-649">You may not bring the quorum resource offline or modify its possible owners list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-650"><span id="ERROR_DEPENDENCY_NOT_ALLOWED"></span><span id="error_dependency_not_allowed"></span>**\_dipendenza errore \_ non \_ consentita**</span><span class="sxs-lookup"><span data-stu-id="0a486-650"><span id="ERROR_DEPENDENCY_NOT_ALLOWED"></span><span id="error_dependency_not_allowed"></span>**ERROR\_DEPENDENCY\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-651">5069 (0x13CD)</span><span class="sxs-lookup"><span data-stu-id="0a486-651">5069 (0x13CD)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-652">La risorsa quorum del cluster non può avere alcuna dipendenza.</span><span class="sxs-lookup"><span data-stu-id="0a486-652">The cluster quorum resource is not allowed to have any dependencies.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-653"><span id="ERROR_CLUSTER_NODE_PAUSED"></span><span id="error_cluster_node_paused"></span>**nodo del cluster di errore \_ \_ \_ sospeso**</span><span class="sxs-lookup"><span data-stu-id="0a486-653"><span id="ERROR_CLUSTER_NODE_PAUSED"></span><span id="error_cluster_node_paused"></span>**ERROR\_CLUSTER\_NODE\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-654">5070 (0x13CE)</span><span class="sxs-lookup"><span data-stu-id="0a486-654">5070 (0x13CE)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-655">Il nodo del cluster è sospeso.</span><span class="sxs-lookup"><span data-stu-id="0a486-655">The cluster node is paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-656"><span id="ERROR_NODE_CANT_HOST_RESOURCE"></span><span id="error_node_cant_host_resource"></span>**\_ \_ \_ risorsa host cant del nodo errore \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-656"><span id="ERROR_NODE_CANT_HOST_RESOURCE"></span><span id="error_node_cant_host_resource"></span>**ERROR\_NODE\_CANT\_HOST\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-657">5071 (0x13CF)</span><span class="sxs-lookup"><span data-stu-id="0a486-657">5071 (0x13CF)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-658">Impossibile portare in linea la risorsa cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-658">The cluster resource cannot be brought online.</span></span> <span data-ttu-id="0a486-659">Il nodo proprietario non è in grado di eseguire questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a486-659">The owner node cannot run this resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-660"><span id="ERROR_CLUSTER_NODE_NOT_READY"></span><span id="error_cluster_node_not_ready"></span>**nodo del cluster di errore \_ \_ \_ non \_ pronto**</span><span class="sxs-lookup"><span data-stu-id="0a486-660"><span id="ERROR_CLUSTER_NODE_NOT_READY"></span><span id="error_cluster_node_not_ready"></span>**ERROR\_CLUSTER\_NODE\_NOT\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-661">5072 (0x13D0)</span><span class="sxs-lookup"><span data-stu-id="0a486-661">5072 (0x13D0)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-662">Il nodo del cluster non è pronto per eseguire l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="0a486-662">The cluster node is not ready to perform the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-663"><span id="ERROR_CLUSTER_NODE_SHUTTING_DOWN"></span><span id="error_cluster_node_shutting_down"></span>**ERRORE \_ di \_ arresto del nodo cluster \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-663"><span id="ERROR_CLUSTER_NODE_SHUTTING_DOWN"></span><span id="error_cluster_node_shutting_down"></span>**ERROR\_CLUSTER\_NODE\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-664">5073 (0x13D1)</span><span class="sxs-lookup"><span data-stu-id="0a486-664">5073 (0x13D1)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-665">È in corso l'arresto del nodo del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-665">The cluster node is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-666"><span id="ERROR_CLUSTER_JOIN_ABORTED"></span><span id="error_cluster_join_aborted"></span>**ERRORE \_ di \_ join del cluster \_ interrotto**</span><span class="sxs-lookup"><span data-stu-id="0a486-666"><span id="ERROR_CLUSTER_JOIN_ABORTED"></span><span id="error_cluster_join_aborted"></span>**ERROR\_CLUSTER\_JOIN\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-667">5074 (0x13D2)</span><span class="sxs-lookup"><span data-stu-id="0a486-667">5074 (0x13D2)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-668">L'operazione di join del cluster è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="0a486-668">The cluster join operation was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-669"><span id="ERROR_CLUSTER_INCOMPATIBLE_VERSIONS"></span><span id="error_cluster_incompatible_versions"></span>**\_ \_ versioni incompatibili del cluster di errori \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-669"><span id="ERROR_CLUSTER_INCOMPATIBLE_VERSIONS"></span><span id="error_cluster_incompatible_versions"></span>**ERROR\_CLUSTER\_INCOMPATIBLE\_VERSIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-670">5075 (0x13D3)</span><span class="sxs-lookup"><span data-stu-id="0a486-670">5075 (0x13D3)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-671">L'operazione di join del cluster non è riuscita a causa di versioni software incompatibili tra il nodo di join e il relativo sponsor.</span><span class="sxs-lookup"><span data-stu-id="0a486-671">The cluster join operation failed due to incompatible software versions between the joining node and its sponsor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-672"><span id="ERROR_CLUSTER_MAXNUM_OF_RESOURCES_EXCEEDED"></span><span id="error_cluster_maxnum_of_resources_exceeded"></span>**\_ \_ MAXNUM del cluster \_ di errore delle \_ risorse \_ superato**</span><span class="sxs-lookup"><span data-stu-id="0a486-672"><span id="ERROR_CLUSTER_MAXNUM_OF_RESOURCES_EXCEEDED"></span><span id="error_cluster_maxnum_of_resources_exceeded"></span>**ERROR\_CLUSTER\_MAXNUM\_OF\_RESOURCES\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-673">5076 (0x13D4)</span><span class="sxs-lookup"><span data-stu-id="0a486-673">5076 (0x13D4)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-674">Non è possibile creare questa risorsa perché il cluster ha raggiunto il limite al numero di risorse che può monitorare.</span><span class="sxs-lookup"><span data-stu-id="0a486-674">This resource cannot be created because the cluster has reached the limit on the number of resources it can monitor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-675"><span id="ERROR_CLUSTER_SYSTEM_CONFIG_CHANGED"></span><span id="error_cluster_system_config_changed"></span>**ERRORE \_ di \_ configurazione del sistema cluster \_ \_ modificato**</span><span class="sxs-lookup"><span data-stu-id="0a486-675"><span id="ERROR_CLUSTER_SYSTEM_CONFIG_CHANGED"></span><span id="error_cluster_system_config_changed"></span>**ERROR\_CLUSTER\_SYSTEM\_CONFIG\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-676">5077 (0x13D5)</span><span class="sxs-lookup"><span data-stu-id="0a486-676">5077 (0x13D5)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-677">La configurazione di sistema è stata modificata durante l'operazione di join o modulo del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-677">The system configuration changed during the cluster join or form operation.</span></span> <span data-ttu-id="0a486-678">L'operazione di join o modulo è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="0a486-678">The join or form operation was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-679"><span id="ERROR_CLUSTER_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_cluster_resource_type_not_found"></span>**\_ \_ \_ \_ Impossibile trovare il tipo di risorsa cluster di errore \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-679"><span id="ERROR_CLUSTER_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_cluster_resource_type_not_found"></span>**ERROR\_CLUSTER\_RESOURCE\_TYPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-680">5078 (0x13D6)</span><span class="sxs-lookup"><span data-stu-id="0a486-680">5078 (0x13D6)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-681">Il tipo di risorsa specificato non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="0a486-681">The specified resource type was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-682"><span id="ERROR_CLUSTER_RESTYPE_NOT_SUPPORTED"></span><span id="error_cluster_restype_not_supported"></span>**ERRORE del \_ cluster \_ restype \_ non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="0a486-682"><span id="ERROR_CLUSTER_RESTYPE_NOT_SUPPORTED"></span><span id="error_cluster_restype_not_supported"></span>**ERROR\_CLUSTER\_RESTYPE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-683">5079 (0x13D7)</span><span class="sxs-lookup"><span data-stu-id="0a486-683">5079 (0x13D7)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-684">Il nodo specificato non supporta una risorsa di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="0a486-684">The specified node does not support a resource of this type.</span></span> <span data-ttu-id="0a486-685">Ciò può essere dovuto a incoerenze di versione o a causa dell'assenza della DLL di risorse in questo nodo.</span><span class="sxs-lookup"><span data-stu-id="0a486-685">This may be due to version inconsistencies or due to the absence of the resource DLL on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-686"><span id="ERROR_CLUSTER_RESNAME_NOT_FOUND"></span><span id="error_cluster_resname_not_found"></span>**ERRORE \_ cluster \_ RESNAME \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="0a486-686"><span id="ERROR_CLUSTER_RESNAME_NOT_FOUND"></span><span id="error_cluster_resname_not_found"></span>**ERROR\_CLUSTER\_RESNAME\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-687">5080 (0x13D8)</span><span class="sxs-lookup"><span data-stu-id="0a486-687">5080 (0x13D8)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-688">Il nome di risorsa specificato non è supportato da questa DLL di risorse.</span><span class="sxs-lookup"><span data-stu-id="0a486-688">The specified resource name is not supported by this resource DLL.</span></span> <span data-ttu-id="0a486-689">Questo potrebbe essere dovuto a un nome non valido (o modificato) fornito alla DLL della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a486-689">This may be due to a bad (or changed) name supplied to the resource DLL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-690"><span id="ERROR_CLUSTER_NO_RPC_PACKAGES_REGISTERED"></span><span id="error_cluster_no_rpc_packages_registered"></span>**ERRORE \_ del \_ cluster \_ nessun \_ pacchetto RPC \_ registrato**</span><span class="sxs-lookup"><span data-stu-id="0a486-690"><span id="ERROR_CLUSTER_NO_RPC_PACKAGES_REGISTERED"></span><span id="error_cluster_no_rpc_packages_registered"></span>**ERROR\_CLUSTER\_NO\_RPC\_PACKAGES\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-691">5081 (0x13D9)</span><span class="sxs-lookup"><span data-stu-id="0a486-691">5081 (0x13D9)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-692">Non è stato possibile registrare alcun pacchetto di autenticazione con il server RPC.</span><span class="sxs-lookup"><span data-stu-id="0a486-692">No authentication package could be registered with the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-693"><span id="ERROR_CLUSTER_OWNER_NOT_IN_PREFLIST"></span><span id="error_cluster_owner_not_in_preflist"></span>**ERRORE \_ \_ del proprietario \_ del cluster non \_ in \_ PREFLIST**</span><span class="sxs-lookup"><span data-stu-id="0a486-693"><span id="ERROR_CLUSTER_OWNER_NOT_IN_PREFLIST"></span><span id="error_cluster_owner_not_in_preflist"></span>**ERROR\_CLUSTER\_OWNER\_NOT\_IN\_PREFLIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-694">5082 (0x13DA)</span><span class="sxs-lookup"><span data-stu-id="0a486-694">5082 (0x13DA)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-695">Non è possibile portare il gruppo online perché il proprietario del gruppo non è presente nell'elenco preferito per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="0a486-695">You cannot bring the group online because the owner of the group is not in the preferred list for the group.</span></span> <span data-ttu-id="0a486-696">Per modificare il nodo proprietario per il gruppo, spostare il gruppo.</span><span class="sxs-lookup"><span data-stu-id="0a486-696">To change the owner node for the group, move the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-697"><span id="ERROR_CLUSTER_DATABASE_SEQMISMATCH"></span><span id="error_cluster_database_seqmismatch"></span>**ERRORE \_ del \_ database cluster \_ SEQMISMATCH**</span><span class="sxs-lookup"><span data-stu-id="0a486-697"><span id="ERROR_CLUSTER_DATABASE_SEQMISMATCH"></span><span id="error_cluster_database_seqmismatch"></span>**ERROR\_CLUSTER\_DATABASE\_SEQMISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-698">5083 (0x13DB)</span><span class="sxs-lookup"><span data-stu-id="0a486-698">5083 (0x13DB)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-699">L'operazione di join non è riuscita perché il numero di sequenza del database cluster è stato modificato o non è compatibile con il nodo del blocco.</span><span class="sxs-lookup"><span data-stu-id="0a486-699">The join operation failed because the cluster database sequence number has changed or is incompatible with the locker node.</span></span> <span data-ttu-id="0a486-700">Questo problema può verificarsi durante un'operazione di join se il database del cluster è stato modificato durante il join.</span><span class="sxs-lookup"><span data-stu-id="0a486-700">This may happen during a join operation if the cluster database was changing during the join.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-701"><span id="ERROR_RESMON_INVALID_STATE"></span><span id="error_resmon_invalid_state"></span>**ERRORE \_ resmon \_ stato non valido \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-701"><span id="ERROR_RESMON_INVALID_STATE"></span><span id="error_resmon_invalid_state"></span>**ERROR\_RESMON\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-702">5084 (0x13DC)</span><span class="sxs-lookup"><span data-stu-id="0a486-702">5084 (0x13DC)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-703">Il monitoraggio risorse non consentirà l'esecuzione dell'operazione di errore mentre la risorsa si trova nello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="0a486-703">The resource monitor will not allow the fail operation to be performed while the resource is in its current state.</span></span> <span data-ttu-id="0a486-704">Questo problema può verificarsi se la risorsa è in uno stato in sospeso.</span><span class="sxs-lookup"><span data-stu-id="0a486-704">This may happen if the resource is in a pending state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-705"><span id="ERROR_CLUSTER_GUM_NOT_LOCKER"></span><span id="error_cluster_gum_not_locker"></span>**ERRORE \_ di \_ \_ blocco del \_ cluster**</span><span class="sxs-lookup"><span data-stu-id="0a486-705"><span id="ERROR_CLUSTER_GUM_NOT_LOCKER"></span><span id="error_cluster_gum_not_locker"></span>**ERROR\_CLUSTER\_GUM\_NOT\_LOCKER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-706">5085 (0x13DD)</span><span class="sxs-lookup"><span data-stu-id="0a486-706">5085 (0x13DD)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-707">Un codice non di blocco ha ricevuto una richiesta di riservare il blocco per la creazione di aggiornamenti globali.</span><span class="sxs-lookup"><span data-stu-id="0a486-707">A non locker code got a request to reserve the lock for making global updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-708"><span id="ERROR_QUORUM_DISK_NOT_FOUND"></span><span id="error_quorum_disk_not_found"></span>**\_disco quorum \_ errore \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="0a486-708"><span id="ERROR_QUORUM_DISK_NOT_FOUND"></span><span id="error_quorum_disk_not_found"></span>**ERROR\_QUORUM\_DISK\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-709">5086 (0x13DE)</span><span class="sxs-lookup"><span data-stu-id="0a486-709">5086 (0x13DE)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-710">Il disco quorum non è stato trovato dal servizio cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-710">The quorum disk could not be located by the cluster service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-711"><span id="ERROR_DATABASE_BACKUP_CORRUPT"></span><span id="error_database_backup_corrupt"></span>**BACKUP del database di errore \_ \_ \_ danneggiato**</span><span class="sxs-lookup"><span data-stu-id="0a486-711"><span id="ERROR_DATABASE_BACKUP_CORRUPT"></span><span id="error_database_backup_corrupt"></span>**ERROR\_DATABASE\_BACKUP\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-712">5087 (0x13DF)</span><span class="sxs-lookup"><span data-stu-id="0a486-712">5087 (0x13DF)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-713">È possibile che il database del cluster di cui è stato eseguito il backup sia danneggiato.</span><span class="sxs-lookup"><span data-stu-id="0a486-713">The backed up cluster database is possibly corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-714"><span id="ERROR_CLUSTER_NODE_ALREADY_HAS_DFS_ROOT"></span><span id="error_cluster_node_already_has_dfs_root"></span>**il \_ nodo del cluster di errore \_ dispone già di una \_ \_ \_ \_ radice DFS**</span><span class="sxs-lookup"><span data-stu-id="0a486-714"><span id="ERROR_CLUSTER_NODE_ALREADY_HAS_DFS_ROOT"></span><span id="error_cluster_node_already_has_dfs_root"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_HAS\_DFS\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-715">5088 (0x13E0)</span><span class="sxs-lookup"><span data-stu-id="0a486-715">5088 (0x13E0)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-716">Una radice DFS esiste già nel nodo del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-716">A DFS root already exists in this cluster node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-717"><span id="ERROR_RESOURCE_PROPERTY_UNCHANGEABLE"></span><span id="error_resource_property_unchangeable"></span>**Proprietà della risorsa di errore non \_ \_ \_ modificabile**</span><span class="sxs-lookup"><span data-stu-id="0a486-717"><span id="ERROR_RESOURCE_PROPERTY_UNCHANGEABLE"></span><span id="error_resource_property_unchangeable"></span>**ERROR\_RESOURCE\_PROPERTY\_UNCHANGEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-718">5089 (0x13E1)</span><span class="sxs-lookup"><span data-stu-id="0a486-718">5089 (0x13E1)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-719">Il tentativo di modificare una proprietà della risorsa non è riuscito perché è in conflitto con un'altra proprietà esistente.</span><span class="sxs-lookup"><span data-stu-id="0a486-719">An attempt to modify a resource property failed because it conflicts with another existing property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-720"><span id="ERROR_CLUSTER_MEMBERSHIP_INVALID_STATE"></span><span id="error_cluster_membership_invalid_state"></span>**ERRORE \_ appartenenza cluster a \_ \_ stato non valido \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-720"><span id="ERROR_CLUSTER_MEMBERSHIP_INVALID_STATE"></span><span id="error_cluster_membership_invalid_state"></span>**ERROR\_CLUSTER\_MEMBERSHIP\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-721">5890 (0x1702)</span><span class="sxs-lookup"><span data-stu-id="0a486-721">5890 (0x1702)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-722">Si è tentato di eseguire un'operazione incompatibile con lo stato di appartenenza corrente del nodo.</span><span class="sxs-lookup"><span data-stu-id="0a486-722">An operation was attempted that is incompatible with the current membership state of the node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-723"><span id="ERROR_CLUSTER_QUORUMLOG_NOT_FOUND"></span><span id="error_cluster_quorumlog_not_found"></span>**ERRORE \_ cluster \_ QUORUMLOG \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="0a486-723"><span id="ERROR_CLUSTER_QUORUMLOG_NOT_FOUND"></span><span id="error_cluster_quorumlog_not_found"></span>**ERROR\_CLUSTER\_QUORUMLOG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-724">5891 (0x1703)</span><span class="sxs-lookup"><span data-stu-id="0a486-724">5891 (0x1703)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-725">La risorsa quorum non contiene il registro quorum.</span><span class="sxs-lookup"><span data-stu-id="0a486-725">The quorum resource does not contain the quorum log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-726"><span id="ERROR_CLUSTER_MEMBERSHIP_HALT"></span><span id="error_cluster_membership_halt"></span>**\_ \_ interruzione appartenenza cluster di errore \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-726"><span id="ERROR_CLUSTER_MEMBERSHIP_HALT"></span><span id="error_cluster_membership_halt"></span>**ERROR\_CLUSTER\_MEMBERSHIP\_HALT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-727">5892 (0x1704)</span><span class="sxs-lookup"><span data-stu-id="0a486-727">5892 (0x1704)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-728">Il motore di appartenenza ha richiesto l'arresto del servizio cluster in questo nodo.</span><span class="sxs-lookup"><span data-stu-id="0a486-728">The membership engine requested shutdown of the cluster service on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-729"><span id="ERROR_CLUSTER_INSTANCE_ID_MISMATCH"></span><span id="error_cluster_instance_id_mismatch"></span>**\_ID istanza cluster di errore non \_ \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="0a486-729"><span id="ERROR_CLUSTER_INSTANCE_ID_MISMATCH"></span><span id="error_cluster_instance_id_mismatch"></span>**ERROR\_CLUSTER\_INSTANCE\_ID\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-730">5893 (0x1705)</span><span class="sxs-lookup"><span data-stu-id="0a486-730">5893 (0x1705)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-731">L'operazione di join non è riuscita perché l'ID istanza del cluster del nodo di join non corrisponde all'ID istanza del cluster del nodo sponsor.</span><span class="sxs-lookup"><span data-stu-id="0a486-731">The join operation failed because the cluster instance ID of the joining node does not match the cluster instance ID of the sponsor node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-732"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND_FOR_IP"></span><span id="error_cluster_network_not_found_for_ip"></span>**ERRORE \_ \_ di rete cluster \_ non \_ trovato per l' \_ \_ indirizzo IP**</span><span class="sxs-lookup"><span data-stu-id="0a486-732"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND_FOR_IP"></span><span id="error_cluster_network_not_found_for_ip"></span>**ERROR\_CLUSTER\_NETWORK\_NOT\_FOUND\_FOR\_IP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-733">5894 (0x1706)</span><span class="sxs-lookup"><span data-stu-id="0a486-733">5894 (0x1706)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-734">Impossibile trovare una rete cluster corrispondente per l'indirizzo IP specificato.</span><span class="sxs-lookup"><span data-stu-id="0a486-734">A matching cluster network for the specified IP address could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-735"><span id="ERROR_CLUSTER_PROPERTY_DATA_TYPE_MISMATCH"></span><span id="error_cluster_property_data_type_mismatch"></span>**ERRORE \_ del \_ tipo di dati della proprietà cluster non \_ \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="0a486-735"><span id="ERROR_CLUSTER_PROPERTY_DATA_TYPE_MISMATCH"></span><span id="error_cluster_property_data_type_mismatch"></span>**ERROR\_CLUSTER\_PROPERTY\_DATA\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-736">5895 (0x1707)</span><span class="sxs-lookup"><span data-stu-id="0a486-736">5895 (0x1707)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-737">Il tipo di dati effettivo della proprietà non corrisponde al tipo di dati previsto della proprietà.</span><span class="sxs-lookup"><span data-stu-id="0a486-737">The actual data type of the property did not match the expected data type of the property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-738"><span id="ERROR_CLUSTER_EVICT_WITHOUT_CLEANUP"></span><span id="error_cluster_evict_without_cleanup"></span>**ERRORE \_ di \_ rimozione del cluster \_ senza \_ pulizia**</span><span class="sxs-lookup"><span data-stu-id="0a486-738"><span id="ERROR_CLUSTER_EVICT_WITHOUT_CLEANUP"></span><span id="error_cluster_evict_without_cleanup"></span>**ERROR\_CLUSTER\_EVICT\_WITHOUT\_CLEANUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-739">5896 (0x1708)</span><span class="sxs-lookup"><span data-stu-id="0a486-739">5896 (0x1708)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-740">Il nodo del cluster è stato rimosso dal cluster, ma il nodo non è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="0a486-740">The cluster node was evicted from the cluster successfully, but the node was not cleaned up.</span></span> <span data-ttu-id="0a486-741">Per determinare i passaggi di pulizia non riusciti e come eseguire il ripristino, vedere il registro eventi dell'applicazione clustering di failover con Visualizzatore eventi.</span><span class="sxs-lookup"><span data-stu-id="0a486-741">To determine what cleanup steps failed and how to recover, see the Failover Clustering application event log using Event Viewer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-742"><span id="ERROR_CLUSTER_PARAMETER_MISMATCH"></span><span id="error_cluster_parameter_mismatch"></span>**ERRORE \_ parametro cluster non \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="0a486-742"><span id="ERROR_CLUSTER_PARAMETER_MISMATCH"></span><span id="error_cluster_parameter_mismatch"></span>**ERROR\_CLUSTER\_PARAMETER\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-743">5897 (0x1709)</span><span class="sxs-lookup"><span data-stu-id="0a486-743">5897 (0x1709)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-744">Due o più valori di parametro specificati per le proprietà di una risorsa sono in conflitto.</span><span class="sxs-lookup"><span data-stu-id="0a486-744">Two or more parameter values specified for a resource's properties are in conflict.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-745"><span id="ERROR_NODE_CANNOT_BE_CLUSTERED"></span><span id="error_node_cannot_be_clustered"></span>**\_ \_ Impossibile \_ \_ RAGGRUPPAre il nodo errore**</span><span class="sxs-lookup"><span data-stu-id="0a486-745"><span id="ERROR_NODE_CANNOT_BE_CLUSTERED"></span><span id="error_node_cannot_be_clustered"></span>**ERROR\_NODE\_CANNOT\_BE\_CLUSTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-746">5898 (0x170A)</span><span class="sxs-lookup"><span data-stu-id="0a486-746">5898 (0x170A)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-747">Questo computer non può essere membro di un cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-747">This computer cannot be made a member of a cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-748"><span id="ERROR_CLUSTER_WRONG_OS_VERSION"></span><span id="error_cluster_wrong_os_version"></span>**ERRORE \_ del \_ cluster \_ versione del sistema operativo \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-748"><span id="ERROR_CLUSTER_WRONG_OS_VERSION"></span><span id="error_cluster_wrong_os_version"></span>**ERROR\_CLUSTER\_WRONG\_OS\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-749">5899 (0x170B)</span><span class="sxs-lookup"><span data-stu-id="0a486-749">5899 (0x170B)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-750">Il computer non può essere membro di un cluster perché non è installata la versione corretta di Windows.</span><span class="sxs-lookup"><span data-stu-id="0a486-750">This computer cannot be made a member of a cluster because it does not have the correct version of Windows installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-751"><span id="ERROR_CLUSTER_CANT_CREATE_DUP_CLUSTER_NAME"></span><span id="error_cluster_cant_create_dup_cluster_name"></span>**\_ \_ Impossibile creare il \_ \_ \_ nome cluster DUPLICAto \_ del cluster di errori**</span><span class="sxs-lookup"><span data-stu-id="0a486-751"><span id="ERROR_CLUSTER_CANT_CREATE_DUP_CLUSTER_NAME"></span><span id="error_cluster_cant_create_dup_cluster_name"></span>**ERROR\_CLUSTER\_CANT\_CREATE\_DUP\_CLUSTER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-752">5900 (0x170C)</span><span class="sxs-lookup"><span data-stu-id="0a486-752">5900 (0x170C)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-753">Non è possibile creare un cluster con il nome del cluster specificato perché il nome del cluster è già in uso.</span><span class="sxs-lookup"><span data-stu-id="0a486-753">A cluster cannot be created with the specified cluster name because that cluster name is already in use.</span></span> <span data-ttu-id="0a486-754">Specificare un nome diverso per il cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-754">Specify a different name for the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-755"><span id="ERROR_CLUSCFG_ALREADY_COMMITTED"></span><span id="error_cluscfg_already_committed"></span>**ERRORE \_ CLUSCFG \_ già \_ eseguito**</span><span class="sxs-lookup"><span data-stu-id="0a486-755"><span id="ERROR_CLUSCFG_ALREADY_COMMITTED"></span><span id="error_cluscfg_already_committed"></span>**ERROR\_CLUSCFG\_ALREADY\_COMMITTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-756">5901 (0x170D)</span><span class="sxs-lookup"><span data-stu-id="0a486-756">5901 (0x170D)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-757">È già stato eseguito il commit dell'azione di configurazione del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-757">The cluster configuration action has already been committed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-758"><span id="ERROR_CLUSCFG_ROLLBACK_FAILED"></span><span id="error_cluscfg_rollback_failed"></span>**ERRORE \_ \_ rollback CLUSCFG \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="0a486-758"><span id="ERROR_CLUSCFG_ROLLBACK_FAILED"></span><span id="error_cluscfg_rollback_failed"></span>**ERROR\_CLUSCFG\_ROLLBACK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-759">5902 (0x170E)</span><span class="sxs-lookup"><span data-stu-id="0a486-759">5902 (0x170E)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-760">Non è stato possibile eseguire il rollback dell'azione di configurazione del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-760">The cluster configuration action could not be rolled back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-761"><span id="ERROR_CLUSCFG_SYSTEM_DISK_DRIVE_LETTER_CONFLICT"></span><span id="error_cluscfg_system_disk_drive_letter_conflict"></span>**ERRORE \_ nella \_ \_ lettera di \_ unità \_ disco \_ di sistema CLUSCFG**</span><span class="sxs-lookup"><span data-stu-id="0a486-761"><span id="ERROR_CLUSCFG_SYSTEM_DISK_DRIVE_LETTER_CONFLICT"></span><span id="error_cluscfg_system_disk_drive_letter_conflict"></span>**ERROR\_CLUSCFG\_SYSTEM\_DISK\_DRIVE\_LETTER\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-762">5903 (0x170F)</span><span class="sxs-lookup"><span data-stu-id="0a486-762">5903 (0x170F)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-763">La lettera di unità assegnata a un disco di sistema in un nodo è in conflitto con la lettera di unità assegnata a un disco in un altro nodo.</span><span class="sxs-lookup"><span data-stu-id="0a486-763">The drive letter assigned to a system disk on one node conflicted with the drive letter assigned to a disk on another node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-764"><span id="ERROR_CLUSTER_OLD_VERSION"></span><span id="error_cluster_old_version"></span>**ERRORE \_ nella \_ versione precedente del cluster \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-764"><span id="ERROR_CLUSTER_OLD_VERSION"></span><span id="error_cluster_old_version"></span>**ERROR\_CLUSTER\_OLD\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-765">5904 (0x1710)</span><span class="sxs-lookup"><span data-stu-id="0a486-765">5904 (0x1710)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-766">Uno o più nodi del cluster eseguono una versione di Windows che non supporta questa operazione.</span><span class="sxs-lookup"><span data-stu-id="0a486-766">One or more nodes in the cluster are running a version of Windows that does not support this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-767"><span id="ERROR_CLUSTER_MISMATCHED_COMPUTER_ACCT_NAME"></span><span id="error_cluster_mismatched_computer_acct_name"></span>**ERRORE del cluster per il \_ \_ \_ \_ nome acct del computer non corrispondente \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-767"><span id="ERROR_CLUSTER_MISMATCHED_COMPUTER_ACCT_NAME"></span><span id="error_cluster_mismatched_computer_acct_name"></span>**ERROR\_CLUSTER\_MISMATCHED\_COMPUTER\_ACCT\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-768">5905 (0x1711)</span><span class="sxs-lookup"><span data-stu-id="0a486-768">5905 (0x1711)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-769">Il nome dell'account computer corrispondente non corrisponde al nome di rete per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a486-769">The name of the corresponding computer account doesn't match the Network Name for this resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-770"><span id="ERROR_CLUSTER_NO_NET_ADAPTERS"></span><span id="error_cluster_no_net_adapters"></span>**ERRORE \_ cluster \_ nessun \_ \_ Adapter NET**</span><span class="sxs-lookup"><span data-stu-id="0a486-770"><span id="ERROR_CLUSTER_NO_NET_ADAPTERS"></span><span id="error_cluster_no_net_adapters"></span>**ERROR\_CLUSTER\_NO\_NET\_ADAPTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-771">5906 (0x1712)</span><span class="sxs-lookup"><span data-stu-id="0a486-771">5906 (0x1712)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-772">Non sono disponibili schede di rete.</span><span class="sxs-lookup"><span data-stu-id="0a486-772">No network adapters are available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-773"><span id="ERROR_CLUSTER_POISONED"></span><span id="error_cluster_poisoned"></span>**ERRORE \_ cluster non \_ elaborabile**</span><span class="sxs-lookup"><span data-stu-id="0a486-773"><span id="ERROR_CLUSTER_POISONED"></span><span id="error_cluster_poisoned"></span>**ERROR\_CLUSTER\_POISONED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-774">5907 (0x1713)</span><span class="sxs-lookup"><span data-stu-id="0a486-774">5907 (0x1713)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-775">Il nodo del cluster è stato danneggiato.</span><span class="sxs-lookup"><span data-stu-id="0a486-775">The cluster node has been poisoned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-776"><span id="ERROR_CLUSTER_GROUP_MOVING"></span><span id="error_cluster_group_moving"></span>**errore durante lo stato del \_ \_ gruppo cluster \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-776"><span id="ERROR_CLUSTER_GROUP_MOVING"></span><span id="error_cluster_group_moving"></span>**ERROR\_CLUSTER\_GROUP\_MOVING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-777">5908 (0x1714)</span><span class="sxs-lookup"><span data-stu-id="0a486-777">5908 (0x1714)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-778">Il gruppo non è in grado di accettare la richiesta perché sta per essere spostato in un altro nodo.</span><span class="sxs-lookup"><span data-stu-id="0a486-778">The group is unable to accept the request since it is moving to another node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-779"><span id="ERROR_CLUSTER_RESOURCE_TYPE_BUSY"></span><span id="error_cluster_resource_type_busy"></span>**\_tipo di risorsa cluster di errore \_ \_ \_ occupato**</span><span class="sxs-lookup"><span data-stu-id="0a486-779"><span id="ERROR_CLUSTER_RESOURCE_TYPE_BUSY"></span><span id="error_cluster_resource_type_busy"></span>**ERROR\_CLUSTER\_RESOURCE\_TYPE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-780">5909 (0x1715)</span><span class="sxs-lookup"><span data-stu-id="0a486-780">5909 (0x1715)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-781">Il tipo di risorsa non può accettare la richiesta perché è troppo occupato a eseguire un'altra operazione.</span><span class="sxs-lookup"><span data-stu-id="0a486-781">The resource type cannot accept the request since is too busy performing another operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-782"><span id="ERROR_RESOURCE_CALL_TIMED_OUT"></span><span id="error_resource_call_timed_out"></span>**\_timeout della \_ chiamata alla risorsa \_ di errore \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-782"><span id="ERROR_RESOURCE_CALL_TIMED_OUT"></span><span id="error_resource_call_timed_out"></span>**ERROR\_RESOURCE\_CALL\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-783">5910 (0x1716)</span><span class="sxs-lookup"><span data-stu-id="0a486-783">5910 (0x1716)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-784">Timeout della chiamata alla DLL della risorsa cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-784">The call to the cluster resource DLL timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-785"><span id="ERROR_INVALID_CLUSTER_IPV6_ADDRESS"></span><span id="error_invalid_cluster_ipv6_address"></span>**ERRORE \_ di \_ \_ indirizzo IPv6 del cluster non valido \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-785"><span id="ERROR_INVALID_CLUSTER_IPV6_ADDRESS"></span><span id="error_invalid_cluster_ipv6_address"></span>**ERROR\_INVALID\_CLUSTER\_IPV6\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-786">5911 (0x1717)</span><span class="sxs-lookup"><span data-stu-id="0a486-786">5911 (0x1717)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-787">Indirizzo non valido per una risorsa indirizzo IPv6.</span><span class="sxs-lookup"><span data-stu-id="0a486-787">The address is not valid for an IPv6 Address resource.</span></span> <span data-ttu-id="0a486-788">Un indirizzo IPv6 globale è obbligatorio e deve corrispondere a una rete di cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-788">A global IPv6 address is required, and it must match a cluster network.</span></span> <span data-ttu-id="0a486-789">Gli indirizzi di compatibilità non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="0a486-789">Compatibility addresses are not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-790"><span id="ERROR_CLUSTER_INTERNAL_INVALID_FUNCTION"></span><span id="error_cluster_internal_invalid_function"></span>**\_funzione interna del cluster di errore \_ \_ non valida \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-790"><span id="ERROR_CLUSTER_INTERNAL_INVALID_FUNCTION"></span><span id="error_cluster_internal_invalid_function"></span>**ERROR\_CLUSTER\_INTERNAL\_INVALID\_FUNCTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-791">5912 (0x1718)</span><span class="sxs-lookup"><span data-stu-id="0a486-791">5912 (0x1718)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-792">Si è verificato un errore interno del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-792">An internal cluster error occurred.</span></span> <span data-ttu-id="0a486-793">È stata tentata una chiamata a una funzione non valida.</span><span class="sxs-lookup"><span data-stu-id="0a486-793">A call to an invalid function was attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-794"><span id="ERROR_CLUSTER_PARAMETER_OUT_OF_BOUNDS"></span><span id="error_cluster_parameter_out_of_bounds"></span>**\_ \_ parametro del cluster \_ di errore fuori \_ \_ limite**</span><span class="sxs-lookup"><span data-stu-id="0a486-794"><span id="ERROR_CLUSTER_PARAMETER_OUT_OF_BOUNDS"></span><span id="error_cluster_parameter_out_of_bounds"></span>**ERROR\_CLUSTER\_PARAMETER\_OUT\_OF\_BOUNDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-795">5913 (0x1719)</span><span class="sxs-lookup"><span data-stu-id="0a486-795">5913 (0x1719)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-796">Il valore di un parametro non è compreso nell'intervallo accettabile.</span><span class="sxs-lookup"><span data-stu-id="0a486-796">A parameter value is out of acceptable range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-797"><span id="ERROR_CLUSTER_PARTIAL_SEND"></span><span id="error_cluster_partial_send"></span>**ERRORE \_ di \_ invio parziale del cluster \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-797"><span id="ERROR_CLUSTER_PARTIAL_SEND"></span><span id="error_cluster_partial_send"></span>**ERROR\_CLUSTER\_PARTIAL\_SEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-798">5914 (0x171A)</span><span class="sxs-lookup"><span data-stu-id="0a486-798">5914 (0x171A)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-799">Si è verificato un errore di rete durante l'invio dei dati a un altro nodo del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-799">A network error occurred while sending data to another node in the cluster.</span></span> <span data-ttu-id="0a486-800">Il numero di byte trasmessi è inferiore al necessario.</span><span class="sxs-lookup"><span data-stu-id="0a486-800">The number of bytes transmitted was less than required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-801"><span id="ERROR_CLUSTER_REGISTRY_INVALID_FUNCTION"></span><span id="error_cluster_registry_invalid_function"></span>**ERRORE \_ registro cluster- \_ \_ funzione non valida \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-801"><span id="ERROR_CLUSTER_REGISTRY_INVALID_FUNCTION"></span><span id="error_cluster_registry_invalid_function"></span>**ERROR\_CLUSTER\_REGISTRY\_INVALID\_FUNCTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-802">5915 (0x171B)</span><span class="sxs-lookup"><span data-stu-id="0a486-802">5915 (0x171B)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-803">È stata tentata un'operazione del registro cluster non valida.</span><span class="sxs-lookup"><span data-stu-id="0a486-803">An invalid cluster registry operation was attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-804"><span id="ERROR_CLUSTER_INVALID_STRING_TERMINATION"></span><span id="error_cluster_invalid_string_termination"></span>**\_ \_ interruzione stringa non valida del cluster di errori \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-804"><span id="ERROR_CLUSTER_INVALID_STRING_TERMINATION"></span><span id="error_cluster_invalid_string_termination"></span>**ERROR\_CLUSTER\_INVALID\_STRING\_TERMINATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-805">5916 (0x171C)</span><span class="sxs-lookup"><span data-stu-id="0a486-805">5916 (0x171C)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-806">Una stringa di input di caratteri non è terminata correttamente.</span><span class="sxs-lookup"><span data-stu-id="0a486-806">An input string of characters is not properly terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-807"><span id="ERROR_CLUSTER_INVALID_STRING_FORMAT"></span><span id="error_cluster_invalid_string_format"></span>**ERRORE del \_ cluster in \_ \_ formato stringa non valido \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-807"><span id="ERROR_CLUSTER_INVALID_STRING_FORMAT"></span><span id="error_cluster_invalid_string_format"></span>**ERROR\_CLUSTER\_INVALID\_STRING\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-808">5917 (0x171D)</span><span class="sxs-lookup"><span data-stu-id="0a486-808">5917 (0x171D)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-809">Una stringa di input di caratteri non è in un formato valido per i dati rappresentati.</span><span class="sxs-lookup"><span data-stu-id="0a486-809">An input string of characters is not in a valid format for the data it represents.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-810"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_IN_PROGRESS"></span><span id="error_cluster_database_transaction_in_progress"></span>**ERRORE \_ \_ \_ di transazione database cluster \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="0a486-810"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_IN_PROGRESS"></span><span id="error_cluster_database_transaction_in_progress"></span>**ERROR\_CLUSTER\_DATABASE\_TRANSACTION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-811">5918 (0x171E)</span><span class="sxs-lookup"><span data-stu-id="0a486-811">5918 (0x171E)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-812">Si è verificato un errore interno del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-812">An internal cluster error occurred.</span></span> <span data-ttu-id="0a486-813">È stata tentata una transazione del database cluster mentre era già in corso una transazione.</span><span class="sxs-lookup"><span data-stu-id="0a486-813">A cluster database transaction was attempted while a transaction was already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-814"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_NOT_IN_PROGRESS"></span><span id="error_cluster_database_transaction_not_in_progress"></span>**ERRORE \_ \_ \_ di transazione database cluster \_ non \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="0a486-814"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_NOT_IN_PROGRESS"></span><span id="error_cluster_database_transaction_not_in_progress"></span>**ERROR\_CLUSTER\_DATABASE\_TRANSACTION\_NOT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-815">5919 (0x171F)</span><span class="sxs-lookup"><span data-stu-id="0a486-815">5919 (0x171F)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-816">Si è verificato un errore interno del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-816">An internal cluster error occurred.</span></span> <span data-ttu-id="0a486-817">Si è verificato un tentativo di eseguire il commit di una transazione del database cluster mentre non è in corso alcuna transazione.</span><span class="sxs-lookup"><span data-stu-id="0a486-817">There was an attempt to commit a cluster database transaction while no transaction was in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-818"><span id="ERROR_CLUSTER_NULL_DATA"></span><span id="error_cluster_null_data"></span>**ERRORI \_ \_ dei dati null del cluster \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-818"><span id="ERROR_CLUSTER_NULL_DATA"></span><span id="error_cluster_null_data"></span>**ERROR\_CLUSTER\_NULL\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-819">5920 (0x1720)</span><span class="sxs-lookup"><span data-stu-id="0a486-819">5920 (0x1720)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-820">Si è verificato un errore interno del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-820">An internal cluster error occurred.</span></span> <span data-ttu-id="0a486-821">I dati non sono stati inizializzati correttamente.</span><span class="sxs-lookup"><span data-stu-id="0a486-821">Data was not properly initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-822"><span id="ERROR_CLUSTER_PARTIAL_READ"></span><span id="error_cluster_partial_read"></span>**ERRORE \_ di \_ lettura parziale del cluster \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-822"><span id="ERROR_CLUSTER_PARTIAL_READ"></span><span id="error_cluster_partial_read"></span>**ERROR\_CLUSTER\_PARTIAL\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-823">5921 (0x1721)</span><span class="sxs-lookup"><span data-stu-id="0a486-823">5921 (0x1721)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-824">Si è verificato un errore durante la lettura da un flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="0a486-824">An error occurred while reading from a stream of data.</span></span> <span data-ttu-id="0a486-825">È stato restituito un numero imprevisto di byte.</span><span class="sxs-lookup"><span data-stu-id="0a486-825">An unexpected number of bytes was returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-826"><span id="ERROR_CLUSTER_PARTIAL_WRITE"></span><span id="error_cluster_partial_write"></span>**ERRORE \_ di \_ scrittura parziale del cluster \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-826"><span id="ERROR_CLUSTER_PARTIAL_WRITE"></span><span id="error_cluster_partial_write"></span>**ERROR\_CLUSTER\_PARTIAL\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-827">5922 (0x1722)</span><span class="sxs-lookup"><span data-stu-id="0a486-827">5922 (0x1722)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-828">Si è verificato un errore durante la scrittura in un flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="0a486-828">An error occurred while writing to a stream of data.</span></span> <span data-ttu-id="0a486-829">Impossibile scrivere il numero di byte richiesto.</span><span class="sxs-lookup"><span data-stu-id="0a486-829">The required number of bytes could not be written.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-830"><span id="ERROR_CLUSTER_CANT_DESERIALIZE_DATA"></span><span id="error_cluster_cant_deserialize_data"></span>**ERRORE del \_ cluster di \_ \_ deserializzazione \_ dei dati**</span><span class="sxs-lookup"><span data-stu-id="0a486-830"><span id="ERROR_CLUSTER_CANT_DESERIALIZE_DATA"></span><span id="error_cluster_cant_deserialize_data"></span>**ERROR\_CLUSTER\_CANT\_DESERIALIZE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-831">5923 (0x1723)</span><span class="sxs-lookup"><span data-stu-id="0a486-831">5923 (0x1723)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-832">Si è verificato un errore durante la deserializzazione di un flusso di dati del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-832">An error occurred while deserializing a stream of cluster data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-833"><span id="ERROR_DEPENDENT_RESOURCE_PROPERTY_CONFLICT"></span><span id="error_dependent_resource_property_conflict"></span>**\_ \_ \_ conflitto proprietà risorse dipendente dall'errore \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-833"><span id="ERROR_DEPENDENT_RESOURCE_PROPERTY_CONFLICT"></span><span id="error_dependent_resource_property_conflict"></span>**ERROR\_DEPENDENT\_RESOURCE\_PROPERTY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-834">5924 (0x1724)</span><span class="sxs-lookup"><span data-stu-id="0a486-834">5924 (0x1724)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-835">Uno o più valori di proprietà per questa risorsa sono in conflitto con uno o più valori di proprietà associati alle risorse dipendenti.</span><span class="sxs-lookup"><span data-stu-id="0a486-835">One or more property values for this resource are in conflict with one or more property values associated with its dependent resource(s).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-836"><span id="ERROR_CLUSTER_NO_QUORUM"></span><span id="error_cluster_no_quorum"></span>**ERRORE del \_ cluster \_ senza \_ quorum**</span><span class="sxs-lookup"><span data-stu-id="0a486-836"><span id="ERROR_CLUSTER_NO_QUORUM"></span><span id="error_cluster_no_quorum"></span>**ERROR\_CLUSTER\_NO\_QUORUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-837">5925 (0x1725)</span><span class="sxs-lookup"><span data-stu-id="0a486-837">5925 (0x1725)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-838">Un quorum di nodi del cluster non è presente per formare un cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-838">A quorum of cluster nodes was not present to form a cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-839"><span id="ERROR_CLUSTER_INVALID_IPV6_NETWORK"></span><span id="error_cluster_invalid_ipv6_network"></span>**ERRORE \_ cluster \_ \_ rete IPv6 non valida \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-839"><span id="ERROR_CLUSTER_INVALID_IPV6_NETWORK"></span><span id="error_cluster_invalid_ipv6_network"></span>**ERROR\_CLUSTER\_INVALID\_IPV6\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-840">5926 (0x1726)</span><span class="sxs-lookup"><span data-stu-id="0a486-840">5926 (0x1726)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-841">La rete cluster non è valida per una risorsa indirizzo IPv6 o non corrisponde all'indirizzo configurato.</span><span class="sxs-lookup"><span data-stu-id="0a486-841">The cluster network is not valid for an IPv6 Address resource, or it does not match the configured address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-842"><span id="ERROR_CLUSTER_INVALID_IPV6_TUNNEL_NETWORK"></span><span id="error_cluster_invalid_ipv6_tunnel_network"></span>**ERRORE \_ cluster \_ \_ \_ rete tunnel IPv6 non valida \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-842"><span id="ERROR_CLUSTER_INVALID_IPV6_TUNNEL_NETWORK"></span><span id="error_cluster_invalid_ipv6_tunnel_network"></span>**ERROR\_CLUSTER\_INVALID\_IPV6\_TUNNEL\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-843">5927 (0x1727)</span><span class="sxs-lookup"><span data-stu-id="0a486-843">5927 (0x1727)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-844">La rete cluster non è valida per una risorsa tunnel IPv6.</span><span class="sxs-lookup"><span data-stu-id="0a486-844">The cluster network is not valid for an IPv6 Tunnel resource.</span></span> <span data-ttu-id="0a486-845">Controllare la configurazione della risorsa indirizzo IP da cui dipende la risorsa tunnel IPv6.</span><span class="sxs-lookup"><span data-stu-id="0a486-845">Check the configuration of the IP Address resource on which the IPv6 Tunnel resource depends.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-846"><span id="ERROR_QUORUM_NOT_ALLOWED_IN_THIS_GROUP"></span><span id="error_quorum_not_allowed_in_this_group"></span>**\_il quorum degli errori \_ non è \_ consentito \_ in \_ questo \_ gruppo**</span><span class="sxs-lookup"><span data-stu-id="0a486-846"><span id="ERROR_QUORUM_NOT_ALLOWED_IN_THIS_GROUP"></span><span id="error_quorum_not_allowed_in_this_group"></span>**ERROR\_QUORUM\_NOT\_ALLOWED\_IN\_THIS\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-847">5928 (0x1728)</span><span class="sxs-lookup"><span data-stu-id="0a486-847">5928 (0x1728)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-848">La risorsa quorum non può trovarsi nel gruppo di archiviazione disponibile.</span><span class="sxs-lookup"><span data-stu-id="0a486-848">Quorum resource cannot reside in the Available Storage group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-849"><span id="ERROR_DEPENDENCY_TREE_TOO_COMPLEX"></span><span id="error_dependency_tree_too_complex"></span>**\_albero delle dipendenze di errore \_ \_ troppo \_ complesso**</span><span class="sxs-lookup"><span data-stu-id="0a486-849"><span id="ERROR_DEPENDENCY_TREE_TOO_COMPLEX"></span><span id="error_dependency_tree_too_complex"></span>**ERROR\_DEPENDENCY\_TREE\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-850">5929 (0x1729)</span><span class="sxs-lookup"><span data-stu-id="0a486-850">5929 (0x1729)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-851">Le dipendenze per questa risorsa sono troppo profondamente nidificate.</span><span class="sxs-lookup"><span data-stu-id="0a486-851">The dependencies for this resource are nested too deeply.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-852"><span id="ERROR_EXCEPTION_IN_RESOURCE_CALL"></span><span id="error_exception_in_resource_call"></span>**\_eccezione \_ di errore \_ nella \_ chiamata di risorsa**</span><span class="sxs-lookup"><span data-stu-id="0a486-852"><span id="ERROR_EXCEPTION_IN_RESOURCE_CALL"></span><span id="error_exception_in_resource_call"></span>**ERROR\_EXCEPTION\_IN\_RESOURCE\_CALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-853">5930 (0x172A)</span><span class="sxs-lookup"><span data-stu-id="0a486-853">5930 (0x172A)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-854">La chiamata nella DLL della risorsa ha generato un'eccezione non gestita.</span><span class="sxs-lookup"><span data-stu-id="0a486-854">The call into the resource DLL raised an unhandled exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-855"><span id="ERROR_CLUSTER_RHS_FAILED_INITIALIZATION"></span><span id="error_cluster_rhs_failed_initialization"></span>**\_inizializzazione del cluster di errore \_ RHS \_ non riuscita \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-855"><span id="ERROR_CLUSTER_RHS_FAILED_INITIALIZATION"></span><span id="error_cluster_rhs_failed_initialization"></span>**ERROR\_CLUSTER\_RHS\_FAILED\_INITIALIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-856">5931 (0x172B)</span><span class="sxs-lookup"><span data-stu-id="0a486-856">5931 (0x172B)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-857">Impossibile inizializzare il processo RHS.</span><span class="sxs-lookup"><span data-stu-id="0a486-857">The RHS process failed to initialize.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-858"><span id="ERROR_CLUSTER_NOT_INSTALLED"></span><span id="error_cluster_not_installed"></span>**ERRORE del \_ cluster \_ non \_ installato**</span><span class="sxs-lookup"><span data-stu-id="0a486-858"><span id="ERROR_CLUSTER_NOT_INSTALLED"></span><span id="error_cluster_not_installed"></span>**ERROR\_CLUSTER\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-859">5932 (0x172C)</span><span class="sxs-lookup"><span data-stu-id="0a486-859">5932 (0x172C)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-860">La funzionalità clustering di failover non è installata in questo nodo.</span><span class="sxs-lookup"><span data-stu-id="0a486-860">The Failover Clustering feature is not installed on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-861"><span id="ERROR_CLUSTER_RESOURCES_MUST_BE_ONLINE_ON_THE_SAME_NODE"></span><span id="error_cluster_resources_must_be_online_on_the_same_node"></span>**le \_ \_ risorse cluster \_ di errore devono \_ essere \_ online nello \_ \_ \_ stesso \_ nodo**</span><span class="sxs-lookup"><span data-stu-id="0a486-861"><span id="ERROR_CLUSTER_RESOURCES_MUST_BE_ONLINE_ON_THE_SAME_NODE"></span><span id="error_cluster_resources_must_be_online_on_the_same_node"></span>**ERROR\_CLUSTER\_RESOURCES\_MUST\_BE\_ONLINE\_ON\_THE\_SAME\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-862">5933 (0x172D)</span><span class="sxs-lookup"><span data-stu-id="0a486-862">5933 (0x172D)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-863">Le risorse devono essere online nello stesso nodo per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="0a486-863">The resources must be online on the same node for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-864"><span id="ERROR_CLUSTER_MAX_NODES_IN_CLUSTER"></span><span id="error_cluster_max_nodes_in_cluster"></span>**\_ \_ numero massimo \_ di nodi \_ del cluster di errore nel \_ cluster**</span><span class="sxs-lookup"><span data-stu-id="0a486-864"><span id="ERROR_CLUSTER_MAX_NODES_IN_CLUSTER"></span><span id="error_cluster_max_nodes_in_cluster"></span>**ERROR\_CLUSTER\_MAX\_NODES\_IN\_CLUSTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-865">5934 (0x172E)</span><span class="sxs-lookup"><span data-stu-id="0a486-865">5934 (0x172E)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-866">Non è possibile aggiungere un nuovo nodo perché questo cluster è già al numero massimo di nodi.</span><span class="sxs-lookup"><span data-stu-id="0a486-866">A new node can not be added since this cluster is already at its maximum number of nodes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-867"><span id="ERROR_CLUSTER_TOO_MANY_NODES"></span><span id="error_cluster_too_many_nodes"></span>**ERRORE del \_ cluster di \_ troppi \_ \_ nodi**</span><span class="sxs-lookup"><span data-stu-id="0a486-867"><span id="ERROR_CLUSTER_TOO_MANY_NODES"></span><span id="error_cluster_too_many_nodes"></span>**ERROR\_CLUSTER\_TOO\_MANY\_NODES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-868">5935 (0x172F)</span><span class="sxs-lookup"><span data-stu-id="0a486-868">5935 (0x172F)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-869">Non è possibile creare il cluster perché il numero di nodi specificato supera il limite massimo consentito.</span><span class="sxs-lookup"><span data-stu-id="0a486-869">This cluster can not be created since the specified number of nodes exceeds the maximum allowed limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-870"><span id="ERROR_CLUSTER_OBJECT_ALREADY_USED"></span><span id="error_cluster_object_already_used"></span>**\_oggetto cluster di errore \_ già in \_ \_ uso**</span><span class="sxs-lookup"><span data-stu-id="0a486-870"><span id="ERROR_CLUSTER_OBJECT_ALREADY_USED"></span><span id="error_cluster_object_already_used"></span>**ERROR\_CLUSTER\_OBJECT\_ALREADY\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-871">5936 (0x1730)</span><span class="sxs-lookup"><span data-stu-id="0a486-871">5936 (0x1730)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-872">Il tentativo di utilizzare il nome del cluster specificato non è riuscito perché nel dominio esiste già un oggetto computer abilitato con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="0a486-872">An attempt to use the specified cluster name failed because an enabled computer object with the given name already exists in the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-873"><span id="ERROR_NONCORE_GROUPS_FOUND"></span><span id="error_noncore_groups_found"></span>**ERRORE di \_ gruppi non core \_ \_ trovati**</span><span class="sxs-lookup"><span data-stu-id="0a486-873"><span id="ERROR_NONCORE_GROUPS_FOUND"></span><span id="error_noncore_groups_found"></span>**ERROR\_NONCORE\_GROUPS\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-874">5937 (0x1731)</span><span class="sxs-lookup"><span data-stu-id="0a486-874">5937 (0x1731)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-875">Questo cluster non può essere eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="0a486-875">This cluster cannot be destroyed.</span></span> <span data-ttu-id="0a486-876">Contiene gruppi di applicazioni non core che devono essere eliminati prima che il cluster possa essere eliminato definitivamente.</span><span class="sxs-lookup"><span data-stu-id="0a486-876">It has non-core application groups which must be deleted before the cluster can be destroyed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-877"><span id="ERROR_FILE_SHARE_RESOURCE_CONFLICT"></span><span id="error_file_share_resource_conflict"></span>**\_conflitto di \_ risorse di condivisione file \_ di errore \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-877"><span id="ERROR_FILE_SHARE_RESOURCE_CONFLICT"></span><span id="error_file_share_resource_conflict"></span>**ERROR\_FILE\_SHARE\_RESOURCE\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-878">5938 (0x1732)</span><span class="sxs-lookup"><span data-stu-id="0a486-878">5938 (0x1732)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-879">La condivisione file associata alla risorsa di controllo di condivisione file non può essere ospitata da questo cluster o da uno dei relativi nodi.</span><span class="sxs-lookup"><span data-stu-id="0a486-879">File share associated with file share witness resource cannot be hosted by this cluster or any of its nodes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-880"><span id="ERROR_CLUSTER_EVICT_INVALID_REQUEST"></span><span id="error_cluster_evict_invalid_request"></span>**ERRORE del \_ cluster per \_ rimuovere la \_ richiesta non valida \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-880"><span id="ERROR_CLUSTER_EVICT_INVALID_REQUEST"></span><span id="error_cluster_evict_invalid_request"></span>**ERROR\_CLUSTER\_EVICT\_INVALID\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-881">5939 (0x1733)</span><span class="sxs-lookup"><span data-stu-id="0a486-881">5939 (0x1733)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-882">L'eliminazione di questo nodo non è valida in questo momento.</span><span class="sxs-lookup"><span data-stu-id="0a486-882">Eviction of this node is invalid at this time.</span></span> <span data-ttu-id="0a486-883">A causa dell'eliminazione del nodo dei requisiti del quorum, il cluster viene arrestato.</span><span class="sxs-lookup"><span data-stu-id="0a486-883">Due to quorum requirements node eviction will result in cluster shutdown.</span></span> <span data-ttu-id="0a486-884">Se è l'ultimo nodo del cluster, usare il comando destroy cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-884">If it is the last node in the cluster, destroy cluster command should be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-885"><span id="ERROR_CLUSTER_SINGLETON_RESOURCE"></span><span id="error_cluster_singleton_resource"></span>**\_ \_ risorsa singleton del cluster di errore \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-885"><span id="ERROR_CLUSTER_SINGLETON_RESOURCE"></span><span id="error_cluster_singleton_resource"></span>**ERROR\_CLUSTER\_SINGLETON\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-886">5940 (0x1734)</span><span class="sxs-lookup"><span data-stu-id="0a486-886">5940 (0x1734)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-887">Nel cluster è consentita una sola istanza di questo tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="0a486-887">Only one instance of this resource type is allowed in the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-888"><span id="ERROR_CLUSTER_GROUP_SINGLETON_RESOURCE"></span><span id="error_cluster_group_singleton_resource"></span>**ERRORE \_ della \_ \_ risorsa singleton del gruppo cluster \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-888"><span id="ERROR_CLUSTER_GROUP_SINGLETON_RESOURCE"></span><span id="error_cluster_group_singleton_resource"></span>**ERROR\_CLUSTER\_GROUP\_SINGLETON\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-889">5941 (0x1735)</span><span class="sxs-lookup"><span data-stu-id="0a486-889">5941 (0x1735)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-890">È consentita una sola istanza di questo tipo di risorsa per gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0a486-890">Only one instance of this resource type is allowed per resource group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-891"><span id="ERROR_CLUSTER_RESOURCE_PROVIDER_FAILED"></span><span id="error_cluster_resource_provider_failed"></span>**ERRORE \_ del \_ provider di risorse cluster \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-891"><span id="ERROR_CLUSTER_RESOURCE_PROVIDER_FAILED"></span><span id="error_cluster_resource_provider_failed"></span>**ERROR\_CLUSTER\_RESOURCE\_PROVIDER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-892">5942 (0x1736)</span><span class="sxs-lookup"><span data-stu-id="0a486-892">5942 (0x1736)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-893">La risorsa non è riuscita a tornare in linea a causa di un errore di una o più risorse del provider.</span><span class="sxs-lookup"><span data-stu-id="0a486-893">The resource failed to come online due to the failure of one or more provider resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-894"><span id="ERROR_CLUSTER_RESOURCE_CONFIGURATION_ERROR"></span><span id="error_cluster_resource_configuration_error"></span>**errore \_ di \_ configurazione della risorsa cluster \_ errore \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-894"><span id="ERROR_CLUSTER_RESOURCE_CONFIGURATION_ERROR"></span><span id="error_cluster_resource_configuration_error"></span>**ERROR\_CLUSTER\_RESOURCE\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-895">5943 (0x1737)</span><span class="sxs-lookup"><span data-stu-id="0a486-895">5943 (0x1737)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-896">La risorsa ha indicato che non è possibile passare in linea su alcun nodo.</span><span class="sxs-lookup"><span data-stu-id="0a486-896">The resource has indicated that it cannot come online on any node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-897"><span id="ERROR_CLUSTER_GROUP_BUSY"></span><span id="error_cluster_group_busy"></span>**gruppo di cluster di errore \_ \_ \_ occupato**</span><span class="sxs-lookup"><span data-stu-id="0a486-897"><span id="ERROR_CLUSTER_GROUP_BUSY"></span><span id="error_cluster_group_busy"></span>**ERROR\_CLUSTER\_GROUP\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-898">5944 (0x1738)</span><span class="sxs-lookup"><span data-stu-id="0a486-898">5944 (0x1738)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-899">Al momento non è possibile eseguire l'operazione corrente in questo gruppo.</span><span class="sxs-lookup"><span data-stu-id="0a486-899">The current operation cannot be performed on this group at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-900"><span id="ERROR_CLUSTER_NOT_SHARED_VOLUME"></span><span id="error_cluster_not_shared_volume"></span>**ERRORE \_ del \_ \_ volume condiviso del cluster \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-900"><span id="ERROR_CLUSTER_NOT_SHARED_VOLUME"></span><span id="error_cluster_not_shared_volume"></span>**ERROR\_CLUSTER\_NOT\_SHARED\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-901">5945 (0x1739)</span><span class="sxs-lookup"><span data-stu-id="0a486-901">5945 (0x1739)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-902">La directory o il file non si trova in un volume condiviso cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-902">The directory or file is not located on a cluster shared volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-903"><span id="ERROR_CLUSTER_INVALID_SECURITY_DESCRIPTOR"></span><span id="error_cluster_invalid_security_descriptor"></span>**\_ \_ \_ descrittore di sicurezza non valido del cluster di errori \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-903"><span id="ERROR_CLUSTER_INVALID_SECURITY_DESCRIPTOR"></span><span id="error_cluster_invalid_security_descriptor"></span>**ERROR\_CLUSTER\_INVALID\_SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-904">5946 (0x173A)</span><span class="sxs-lookup"><span data-stu-id="0a486-904">5946 (0x173A)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-905">Il descrittore di sicurezza non soddisfa i requisiti per un cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-905">The Security Descriptor does not meet the requirements for a cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-906"><span id="ERROR_CLUSTER_SHARED_VOLUMES_IN_USE"></span><span id="error_cluster_shared_volumes_in_use"></span>**\_ \_ volumi condivisi cluster \_ \_ di errore in \_ uso**</span><span class="sxs-lookup"><span data-stu-id="0a486-906"><span id="ERROR_CLUSTER_SHARED_VOLUMES_IN_USE"></span><span id="error_cluster_shared_volumes_in_use"></span>**ERROR\_CLUSTER\_SHARED\_VOLUMES\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-907">5947 (0x173B)</span><span class="sxs-lookup"><span data-stu-id="0a486-907">5947 (0x173B)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-908">Nel cluster sono configurate una o più risorse di volumi condivisi.</span><span class="sxs-lookup"><span data-stu-id="0a486-908">There is one or more shared volumes resources configured in the cluster.</span></span> <span data-ttu-id="0a486-909">Queste risorse devono essere spostate nello spazio di archiviazione disponibile affinché l'operazione abbia esito positivo.</span><span class="sxs-lookup"><span data-stu-id="0a486-909">Those resources must be moved to available storage in order for operation to succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-910"><span id="ERROR_CLUSTER_USE_SHARED_VOLUMES_API"></span><span id="error_cluster_use_shared_volumes_api"></span>**ERRORE del \_ cluster \_ usare l' \_ \_ API volumi condivisi \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-910"><span id="ERROR_CLUSTER_USE_SHARED_VOLUMES_API"></span><span id="error_cluster_use_shared_volumes_api"></span>**ERROR\_CLUSTER\_USE\_SHARED\_VOLUMES\_API**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-911">5948 (0x173C)</span><span class="sxs-lookup"><span data-stu-id="0a486-911">5948 (0x173C)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-912">Il gruppo o la risorsa non può essere modificato direttamente.</span><span class="sxs-lookup"><span data-stu-id="0a486-912">This group or resource cannot be directly manipulated.</span></span> <span data-ttu-id="0a486-913">Usare le API del volume condiviso per eseguire l'operazione desiderata.</span><span class="sxs-lookup"><span data-stu-id="0a486-913">Use shared volume APIs to perform desired operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-914"><span id="ERROR_CLUSTER_BACKUP_IN_PROGRESS"></span><span id="error_cluster_backup_in_progress"></span>**\_ \_ backup del cluster \_ di errore in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="0a486-914"><span id="ERROR_CLUSTER_BACKUP_IN_PROGRESS"></span><span id="error_cluster_backup_in_progress"></span>**ERROR\_CLUSTER\_BACKUP\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-915">5949 (0x173D)</span><span class="sxs-lookup"><span data-stu-id="0a486-915">5949 (0x173D)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-916">Il backup è in corso.</span><span class="sxs-lookup"><span data-stu-id="0a486-916">Back up is in progress.</span></span> <span data-ttu-id="0a486-917">Attendere il completamento del backup prima di riprovare.</span><span class="sxs-lookup"><span data-stu-id="0a486-917">Please wait for backup completion before trying this operation again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-918"><span id="ERROR_NON_CSV_PATH"></span><span id="error_non_csv_path"></span>**ERRORE \_ non \_ CSV \_ percorso**</span><span class="sxs-lookup"><span data-stu-id="0a486-918"><span id="ERROR_NON_CSV_PATH"></span><span id="error_non_csv_path"></span>**ERROR\_NON\_CSV\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-919">5950 (0x173E)</span><span class="sxs-lookup"><span data-stu-id="0a486-919">5950 (0x173E)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-920">Il percorso non appartiene a un volume condiviso cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-920">The path does not belong to a cluster shared volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-921"><span id="ERROR_CSV_VOLUME_NOT_LOCAL"></span><span id="error_csv_volume_not_local"></span>**\_volume CSV \_ errore \_ non \_ locale**</span><span class="sxs-lookup"><span data-stu-id="0a486-921"><span id="ERROR_CSV_VOLUME_NOT_LOCAL"></span><span id="error_csv_volume_not_local"></span>**ERROR\_CSV\_VOLUME\_NOT\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-922">5951 (0x173F)</span><span class="sxs-lookup"><span data-stu-id="0a486-922">5951 (0x173F)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-923">Il volume condiviso cluster non è installato localmente in questo nodo.</span><span class="sxs-lookup"><span data-stu-id="0a486-923">The cluster shared volume is not locally mounted on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-924"><span id="ERROR_CLUSTER_WATCHDOG_TERMINATING"></span><span id="error_cluster_watchdog_terminating"></span>**errore durante la chiusura del watchdog del \_ cluster \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-924"><span id="ERROR_CLUSTER_WATCHDOG_TERMINATING"></span><span id="error_cluster_watchdog_terminating"></span>**ERROR\_CLUSTER\_WATCHDOG\_TERMINATING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-925">5952 (0x1740)</span><span class="sxs-lookup"><span data-stu-id="0a486-925">5952 (0x1740)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-926">Il watchdog del cluster verrà terminato.</span><span class="sxs-lookup"><span data-stu-id="0a486-926">The cluster watchdog is terminating.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-927"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_INCOMPATIBLE_NODES"></span><span id="error_cluster_resource_vetoed_move_incompatible_nodes"></span>**ERRORE \_ di \_ spostamento della risorsa cluster di \_ \_ \_ nodi incompatibili \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-927"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_INCOMPATIBLE_NODES"></span><span id="error_cluster_resource_vetoed_move_incompatible_nodes"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_MOVE\_INCOMPATIBLE\_NODES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-928">5953 (0x1741)</span><span class="sxs-lookup"><span data-stu-id="0a486-928">5953 (0x1741)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-929">Una risorsa ha dato il veto a uno spostamento tra due nodi perché non sono compatibili.</span><span class="sxs-lookup"><span data-stu-id="0a486-929">A resource vetoed a move between two nodes because they are incompatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-930"><span id="ERROR_CLUSTER_INVALID_NODE_WEIGHT"></span><span id="error_cluster_invalid_node_weight"></span>**\_spessore nodo del cluster di errore \_ non valido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-930"><span id="ERROR_CLUSTER_INVALID_NODE_WEIGHT"></span><span id="error_cluster_invalid_node_weight"></span>**ERROR\_CLUSTER\_INVALID\_NODE\_WEIGHT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-931">5954 (0x1742)</span><span class="sxs-lookup"><span data-stu-id="0a486-931">5954 (0x1742)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-932">La richiesta non è valida perché non è possibile modificare il peso del nodo mentre il cluster si trova in modalità quorum solo disco oppure perché la modifica del peso del nodo viola i requisiti minimi del quorum del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-932">The request is invalid either because node weight cannot be changed while the cluster is in disk-only quorum mode, or because changing the node weight would violate the minimum cluster quorum requirements.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-933"><span id="ERROR_CLUSTER_RESOURCE_VETOED_CALL"></span><span id="error_cluster_resource_vetoed_call"></span>**errore durante la chiamata alla \_ \_ risorsa cluster \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-933"><span id="ERROR_CLUSTER_RESOURCE_VETOED_CALL"></span><span id="error_cluster_resource_vetoed_call"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_CALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-934">5955 (0x1743)</span><span class="sxs-lookup"><span data-stu-id="0a486-934">5955 (0x1743)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-935">La risorsa ha posto il veto alla chiamata.</span><span class="sxs-lookup"><span data-stu-id="0a486-935">The resource vetoed the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-936"><span id="ERROR_RESMON_SYSTEM_RESOURCES_LACKING"></span><span id="error_resmon_system_resources_lacking"></span>**ERRORE \_ resmon \_ risorse di sistema \_ \_ mancanti**</span><span class="sxs-lookup"><span data-stu-id="0a486-936"><span id="ERROR_RESMON_SYSTEM_RESOURCES_LACKING"></span><span id="error_resmon_system_resources_lacking"></span>**ERROR\_RESMON\_SYSTEM\_RESOURCES\_LACKING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-937">5956 (0x1744)</span><span class="sxs-lookup"><span data-stu-id="0a486-937">5956 (0x1744)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-938">Non è stato possibile avviare o eseguire la risorsa perché non è stato possibile riservare risorse di sistema sufficienti.</span><span class="sxs-lookup"><span data-stu-id="0a486-938">Resource could not start or run because it could not reserve sufficient system resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-939"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_DESTINATION"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_destination"></span>**la \_ \_ risorsa cluster \_ di errore \_ \_ non dispone \_ \_ di risorse sufficienti \_ per \_ spostare la destinazione**</span><span class="sxs-lookup"><span data-stu-id="0a486-939"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_DESTINATION"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_destination"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_MOVE\_NOT\_ENOUGH\_RESOURCES\_ON\_DESTINATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-940">5957 (0x1745)</span><span class="sxs-lookup"><span data-stu-id="0a486-940">5957 (0x1745)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-941">Una risorsa ha bloccato uno spostamento tra due nodi perché la destinazione attualmente non dispone di risorse sufficienti per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="0a486-941">A resource vetoed a move between two nodes because the destination currently does not have enough resources to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-942"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_SOURCE"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_source"></span>**la \_ \_ risorsa cluster \_ di errore \_ Sposta \_ \_ le risorse insufficienti \_ \_ nell' \_ origine**</span><span class="sxs-lookup"><span data-stu-id="0a486-942"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_SOURCE"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_source"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_MOVE\_NOT\_ENOUGH\_RESOURCES\_ON\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-943">5958 (0x1746)</span><span class="sxs-lookup"><span data-stu-id="0a486-943">5958 (0x1746)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-944">Una risorsa ha causato il veto di uno spostamento tra due nodi perché l'origine attualmente non dispone di risorse sufficienti per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="0a486-944">A resource vetoed a move between two nodes because the source currently does not have enough resources to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-945"><span id="ERROR_CLUSTER_GROUP_QUEUED"></span><span id="error_cluster_group_queued"></span>**ERRORE del \_ gruppo di cluster in \_ \_ coda**</span><span class="sxs-lookup"><span data-stu-id="0a486-945"><span id="ERROR_CLUSTER_GROUP_QUEUED"></span><span id="error_cluster_group_queued"></span>**ERROR\_CLUSTER\_GROUP\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-946">5959 (0x1747)</span><span class="sxs-lookup"><span data-stu-id="0a486-946">5959 (0x1747)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-947">Non è possibile completare l'operazione richiesta perché il gruppo è in coda per un'operazione.</span><span class="sxs-lookup"><span data-stu-id="0a486-947">The requested operation can not be completed because the group is queued for an operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-948"><span id="ERROR_CLUSTER_RESOURCE_LOCKED_STATUS"></span><span id="error_cluster_resource_locked_status"></span>**ERRORE \_ \_ \_ stato blocco risorse \_ cluster**</span><span class="sxs-lookup"><span data-stu-id="0a486-948"><span id="ERROR_CLUSTER_RESOURCE_LOCKED_STATUS"></span><span id="error_cluster_resource_locked_status"></span>**ERROR\_CLUSTER\_RESOURCE\_LOCKED\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-949">5960 (0x1748)</span><span class="sxs-lookup"><span data-stu-id="0a486-949">5960 (0x1748)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-950">L'operazione richiesta non può essere completata perché lo stato di una risorsa è bloccato.</span><span class="sxs-lookup"><span data-stu-id="0a486-950">The requested operation can not be completed because a resource has locked status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-951"><span id="ERROR_CLUSTER_SHARED_VOLUME_FAILOVER_NOT_ALLOWED"></span><span id="error_cluster_shared_volume_failover_not_allowed"></span>**ERRORE \_ \_ failover del \_ volume condiviso cluster \_ \_ non \_ consentito**</span><span class="sxs-lookup"><span data-stu-id="0a486-951"><span id="ERROR_CLUSTER_SHARED_VOLUME_FAILOVER_NOT_ALLOWED"></span><span id="error_cluster_shared_volume_failover_not_allowed"></span>**ERROR\_CLUSTER\_SHARED\_VOLUME\_FAILOVER\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-952">5961 (0x1749)</span><span class="sxs-lookup"><span data-stu-id="0a486-952">5961 (0x1749)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-953">La risorsa non può essere spostata in un altro nodo perché il volume condiviso del cluster ha consentito l'operazione.</span><span class="sxs-lookup"><span data-stu-id="0a486-953">The resource cannot move to another node because a cluster shared volume vetoed the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-954"><span id="ERROR_CLUSTER_NODE_DRAIN_IN_PROGRESS"></span><span id="error_cluster_node_drain_in_progress"></span>**ERRORE \_ \_ \_ di svuotamento del nodo cluster \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="0a486-954"><span id="ERROR_CLUSTER_NODE_DRAIN_IN_PROGRESS"></span><span id="error_cluster_node_drain_in_progress"></span>**ERROR\_CLUSTER\_NODE\_DRAIN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-955">5962 (0x174A)</span><span class="sxs-lookup"><span data-stu-id="0a486-955">5962 (0x174A)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-956">Uno svuotamento del nodo è già in corso.</span><span class="sxs-lookup"><span data-stu-id="0a486-956">A node drain is already in progress.</span></span>

<span data-ttu-id="0a486-957">Questo valore era denominato anche **errore \_ \_ \_ di evacuazione nodi cluster \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="0a486-957">This value was also named **ERROR\_CLUSTER\_NODE\_EVACUATION\_IN\_PROGRESS**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-958"><span id="ERROR_CLUSTER_DISK_NOT_CONNECTED"></span><span id="error_cluster_disk_not_connected"></span>**ERRORE \_ del \_ disco del cluster \_ non \_ connesso**</span><span class="sxs-lookup"><span data-stu-id="0a486-958"><span id="ERROR_CLUSTER_DISK_NOT_CONNECTED"></span><span id="error_cluster_disk_not_connected"></span>**ERROR\_CLUSTER\_DISK\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-959">5963 (0x174B)</span><span class="sxs-lookup"><span data-stu-id="0a486-959">5963 (0x174B)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-960">L'archiviazione in cluster non è connessa al nodo.</span><span class="sxs-lookup"><span data-stu-id="0a486-960">Clustered storage is not connected to the node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-961"><span id="ERROR_DISK_NOT_CSV_CAPABLE"></span><span id="error_disk_not_csv_capable"></span>**\_disco errore \_ non \_ compatibile con CSV \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-961"><span id="ERROR_DISK_NOT_CSV_CAPABLE"></span><span id="error_disk_not_csv_capable"></span>**ERROR\_DISK\_NOT\_CSV\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-962">5964 (0x174C)</span><span class="sxs-lookup"><span data-stu-id="0a486-962">5964 (0x174C)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-963">Il disco non è configurato in modo da essere utilizzato con CSV.</span><span class="sxs-lookup"><span data-stu-id="0a486-963">The disk is not configured in a way to be used with CSV.</span></span> <span data-ttu-id="0a486-964">I dischi CSV devono contenere almeno una partizione formattata con NTFS.</span><span class="sxs-lookup"><span data-stu-id="0a486-964">CSV disks must have at least one partition that is formatted with NTFS.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-965"><span id="ERROR_RESOURCE_NOT_IN_AVAILABLE_STORAGE"></span><span id="error_resource_not_in_available_storage"></span>**\_risorsa \_ di errore non \_ \_ presente nell' \_ archiviazione disponibile**</span><span class="sxs-lookup"><span data-stu-id="0a486-965"><span id="ERROR_RESOURCE_NOT_IN_AVAILABLE_STORAGE"></span><span id="error_resource_not_in_available_storage"></span>**ERROR\_RESOURCE\_NOT\_IN\_AVAILABLE\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-966">5965 (0x174D)</span><span class="sxs-lookup"><span data-stu-id="0a486-966">5965 (0x174D)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-967">Per completare questa azione, è necessario che la risorsa faccia parte del gruppo di archiviazione disponibile.</span><span class="sxs-lookup"><span data-stu-id="0a486-967">The resource must be part of the Available Storage group to complete this action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-968"><span id="ERROR_CLUSTER_SHARED_VOLUME_REDIRECTED"></span><span id="error_cluster_shared_volume_redirected"></span>**ERRORE \_ del \_ volume condiviso del cluster \_ \_ reindirizzato**</span><span class="sxs-lookup"><span data-stu-id="0a486-968"><span id="ERROR_CLUSTER_SHARED_VOLUME_REDIRECTED"></span><span id="error_cluster_shared_volume_redirected"></span>**ERROR\_CLUSTER\_SHARED\_VOLUME\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-969">5966 (0x174E)</span><span class="sxs-lookup"><span data-stu-id="0a486-969">5966 (0x174E)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-970">L'operazione CSVFS non è riuscita perché il volume è in modalità reindirizzato.</span><span class="sxs-lookup"><span data-stu-id="0a486-970">CSVFS failed operation as volume is in redirected mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-971"><span id="ERROR_CLUSTER_SHARED_VOLUME_NOT_REDIRECTED"></span><span id="error_cluster_shared_volume_not_redirected"></span>**ERRORE \_ del \_ volume condiviso cluster \_ \_ non \_ reindirizzato**</span><span class="sxs-lookup"><span data-stu-id="0a486-971"><span id="ERROR_CLUSTER_SHARED_VOLUME_NOT_REDIRECTED"></span><span id="error_cluster_shared_volume_not_redirected"></span>**ERROR\_CLUSTER\_SHARED\_VOLUME\_NOT\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-972">5967 (0x174F)</span><span class="sxs-lookup"><span data-stu-id="0a486-972">5967 (0x174F)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-973">L'operazione CSVFS non è riuscita perché il volume non è in modalità reindirizzata.</span><span class="sxs-lookup"><span data-stu-id="0a486-973">CSVFS failed operation as volume is not in redirected mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-974"><span id="ERROR_CLUSTER_CANNOT_RETURN_PROPERTIES"></span><span id="error_cluster_cannot_return_properties"></span>**il \_ cluster di errore \_ non può \_ restituire \_ Proprietà**</span><span class="sxs-lookup"><span data-stu-id="0a486-974"><span id="ERROR_CLUSTER_CANNOT_RETURN_PROPERTIES"></span><span id="error_cluster_cannot_return_properties"></span>**ERROR\_CLUSTER\_CANNOT\_RETURN\_PROPERTIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-975">5968 (0x1750)</span><span class="sxs-lookup"><span data-stu-id="0a486-975">5968 (0x1750)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-976">Non è possibile restituire le proprietà del cluster in questo momento.</span><span class="sxs-lookup"><span data-stu-id="0a486-976">Cluster properties cannot be returned at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-977"><span id="ERROR_CLUSTER_RESOURCE_CONTAINS_UNSUPPORTED_DIFF_AREA_FOR_SHARED_VOLUMES"></span><span id="error_cluster_resource_contains_unsupported_diff_area_for_shared_volumes"></span>**\_ \_ la risorsa cluster \_ di errore contiene un' \_ \_ area diff non supportata \_ \_ per i \_ \_ volumi condivisi**</span><span class="sxs-lookup"><span data-stu-id="0a486-977"><span id="ERROR_CLUSTER_RESOURCE_CONTAINS_UNSUPPORTED_DIFF_AREA_FOR_SHARED_VOLUMES"></span><span id="error_cluster_resource_contains_unsupported_diff_area_for_shared_volumes"></span>**ERROR\_CLUSTER\_RESOURCE\_CONTAINS\_UNSUPPORTED\_DIFF\_AREA\_FOR\_SHARED\_VOLUMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-978">5969 (0x1751)</span><span class="sxs-lookup"><span data-stu-id="0a486-978">5969 (0x1751)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-979">La risorsa disco del cluster contiene un'area di diff snapshot software non supportata per i volumi condivisi del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-979">The clustered disk resource contains software snapshot diff area that are not supported for Cluster Shared Volumes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-980"><span id="ERROR_CLUSTER_RESOURCE_IS_IN_MAINTENANCE_MODE"></span><span id="error_cluster_resource_is_in_maintenance_mode"></span>**ERRORE \_ \_ della risorsa \_ cluster \_ in \_ \_ modalità manutenzione**</span><span class="sxs-lookup"><span data-stu-id="0a486-980"><span id="ERROR_CLUSTER_RESOURCE_IS_IN_MAINTENANCE_MODE"></span><span id="error_cluster_resource_is_in_maintenance_mode"></span>**ERROR\_CLUSTER\_RESOURCE\_IS\_IN\_MAINTENANCE\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-981">5970 (0x1752)</span><span class="sxs-lookup"><span data-stu-id="0a486-981">5970 (0x1752)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-982">Non è possibile completare l'operazione perché la risorsa è in modalità di manutenzione.</span><span class="sxs-lookup"><span data-stu-id="0a486-982">The operation cannot be completed because the resource is in maintenance mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-983"><span id="ERROR_CLUSTER_AFFINITY_CONFLICT"></span><span id="error_cluster_affinity_conflict"></span>**\_conflitto di \_ affinità del cluster di errore \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-983"><span id="ERROR_CLUSTER_AFFINITY_CONFLICT"></span><span id="error_cluster_affinity_conflict"></span>**ERROR\_CLUSTER\_AFFINITY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-984">5971 (0x1753)</span><span class="sxs-lookup"><span data-stu-id="0a486-984">5971 (0x1753)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-985">Non è possibile completare l'operazione a causa di conflitti di affinità del cluster.</span><span class="sxs-lookup"><span data-stu-id="0a486-985">The operation cannot be completed because of cluster affinity conflicts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0a486-986"><span id="ERROR_CLUSTER_RESOURCE_IS_REPLICA_VIRTUAL_MACHINE"></span><span id="error_cluster_resource_is_replica_virtual_machine"></span>**\_la risorsa cluster di errore \_ è una \_ \_ \_ macchina virtuale di replica \_**</span><span class="sxs-lookup"><span data-stu-id="0a486-986"><span id="ERROR_CLUSTER_RESOURCE_IS_REPLICA_VIRTUAL_MACHINE"></span><span id="error_cluster_resource_is_replica_virtual_machine"></span>**ERROR\_CLUSTER\_RESOURCE\_IS\_REPLICA\_VIRTUAL\_MACHINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a486-987">5972 (0x1754)</span><span class="sxs-lookup"><span data-stu-id="0a486-987">5972 (0x1754)</span></span>
</dt> <dt>



<span data-ttu-id="0a486-988">Non è possibile completare l'operazione perché la risorsa è una macchina virtuale di replica.</span><span class="sxs-lookup"><span data-stu-id="0a486-988">The operation cannot be completed because the resource is a replica virtual machine.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="0a486-989">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a486-989">Requirements</span></span>



| <span data-ttu-id="0a486-990">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a486-990">Requirement</span></span> | <span data-ttu-id="0a486-991">Valore</span><span class="sxs-lookup"><span data-stu-id="0a486-991">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0a486-992">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a486-992">Minimum supported client</span></span><br/> | <span data-ttu-id="0a486-993">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0a486-993">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0a486-994">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a486-994">Minimum supported server</span></span><br/> | <span data-ttu-id="0a486-995">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0a486-995">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0a486-996">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a486-996">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a486-997"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a486-997"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a486-998">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a486-998">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a486-999">Codici di errore di sistema</span><span class="sxs-lookup"><span data-stu-id="0a486-999">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




