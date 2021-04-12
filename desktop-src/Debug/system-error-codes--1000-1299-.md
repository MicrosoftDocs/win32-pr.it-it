---
description: Descrive i codici di errore 1000-1299 definiti nel file di intestazione WinError. h ed è destinato agli sviluppatori.
ms.assetid: 0061feb6-e1a0-4fcd-8f80-954087c799d7
title: Codici di errore di sistema (1000-1299) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 592bd5c6653526d87fed05d6ec76f739355ae359
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523714"
---
# <a name="system-error-codes-1000-1299"></a><span data-ttu-id="84126-103">Codici di errore di sistema (1000-1299)</span><span class="sxs-lookup"><span data-stu-id="84126-103">System Error Codes (1000-1299)</span></span>

> [!NOTE]
> <span data-ttu-id="84126-104">Queste informazioni sono destinate agli sviluppatori che effettuano il debug degli errori di sistema.</span><span class="sxs-lookup"><span data-stu-id="84126-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="84126-105">Per altri errori, ad esempio problemi con Windows Update, è disponibile un elenco di risorse nella pagina [codici di errore](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="84126-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="84126-106">Nell'elenco seguente vengono descritti i [codici di errore di sistema](system-error-codes.md) per gli errori da 1000 a 1299.</span><span class="sxs-lookup"><span data-stu-id="84126-106">The following list describes [system error codes](system-error-codes.md) for errors 1000 to 1299.</span></span> <span data-ttu-id="84126-107">Vengono restituiti dalla funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="84126-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="84126-108">Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la funzione [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il **formato \_ Message from flag \_ di \_ sistema** .</span><span class="sxs-lookup"><span data-stu-id="84126-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="84126-109"><span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**\_overflow dello stack di errori \_**</span><span class="sxs-lookup"><span data-stu-id="84126-109"><span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**ERROR\_STACK\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-110">1001 (0x3E9)</span><span class="sxs-lookup"><span data-stu-id="84126-110">1001 (0x3E9)</span></span>
</dt> <dt>



<span data-ttu-id="84126-111">Ricorsione troppo profonda; overflow dello stack.</span><span class="sxs-lookup"><span data-stu-id="84126-111">Recursion too deep; the stack overflowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-112"><span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**messaggio di errore \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="84126-112"><span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**ERROR\_INVALID\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-113">1002 (0x3EA)</span><span class="sxs-lookup"><span data-stu-id="84126-113">1002 (0x3EA)</span></span>
</dt> <dt>



<span data-ttu-id="84126-114">La finestra non può agire sul messaggio inviato.</span><span class="sxs-lookup"><span data-stu-id="84126-114">The window cannot act on the sent message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-115"><span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**\_non è \_ possibile \_ completare l'errore**</span><span class="sxs-lookup"><span data-stu-id="84126-115"><span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**ERROR\_CAN\_NOT\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-116">1003 (0x3EB)</span><span class="sxs-lookup"><span data-stu-id="84126-116">1003 (0x3EB)</span></span>
</dt> <dt>



<span data-ttu-id="84126-117">Non è possibile completare questa funzione.</span><span class="sxs-lookup"><span data-stu-id="84126-117">Cannot complete this function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-118"><span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**flag di errore \_ non validi \_**</span><span class="sxs-lookup"><span data-stu-id="84126-118"><span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**ERROR\_INVALID\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-119">1004 (0x3EC)</span><span class="sxs-lookup"><span data-stu-id="84126-119">1004 (0x3EC)</span></span>
</dt> <dt>



<span data-ttu-id="84126-120">Flag non validi.</span><span class="sxs-lookup"><span data-stu-id="84126-120">Invalid flags.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-121"><span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**ERRORE \_ volume non riconosciuto \_**</span><span class="sxs-lookup"><span data-stu-id="84126-121"><span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**ERROR\_UNRECOGNIZED\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-122">1005 (0x3ED)</span><span class="sxs-lookup"><span data-stu-id="84126-122">1005 (0x3ED)</span></span>
</dt> <dt>



<span data-ttu-id="84126-123">Il volume non contiene un file system riconosciuto.</span><span class="sxs-lookup"><span data-stu-id="84126-123">The volume does not contain a recognized file system.</span></span> <span data-ttu-id="84126-124">Verificare che tutti i driver di file system necessari siano caricati e che il volume non sia danneggiato.</span><span class="sxs-lookup"><span data-stu-id="84126-124">Please make sure that all required file system drivers are loaded and that the volume is not corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-125"><span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**FILE degli errori \_ \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="84126-125"><span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**ERROR\_FILE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-126">1006 (0x3EE)</span><span class="sxs-lookup"><span data-stu-id="84126-126">1006 (0x3EE)</span></span>
</dt> <dt>



<span data-ttu-id="84126-127">Il volume di un file è stato modificato esternamente in modo che il file aperto non sia più valido.</span><span class="sxs-lookup"><span data-stu-id="84126-127">The volume for a file has been externally altered so that the opened file is no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-128"><span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**\_modalità a schermo intero errore \_**</span><span class="sxs-lookup"><span data-stu-id="84126-128"><span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**ERROR\_FULLSCREEN\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-129">1007 (0x3EF)</span><span class="sxs-lookup"><span data-stu-id="84126-129">1007 (0x3EF)</span></span>
</dt> <dt>



<span data-ttu-id="84126-130">L'operazione richiesta non può essere eseguita in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="84126-130">The requested operation cannot be performed in full-screen mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-131"><span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**ERRORE \_ nessun \_ token**</span><span class="sxs-lookup"><span data-stu-id="84126-131"><span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**ERROR\_NO\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-132">1008 (0x3F0)</span><span class="sxs-lookup"><span data-stu-id="84126-132">1008 (0x3F0)</span></span>
</dt> <dt>



<span data-ttu-id="84126-133">È stato effettuato un tentativo di fare riferimento a un token che non esiste.</span><span class="sxs-lookup"><span data-stu-id="84126-133">An attempt was made to reference a token that does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-134"><span id="ERROR_BADDB"></span><span id="error_baddb"></span>**ERRORE \_ BADDB**</span><span class="sxs-lookup"><span data-stu-id="84126-134"><span id="ERROR_BADDB"></span><span id="error_baddb"></span>**ERROR\_BADDB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-135">1009 (0x3F1)</span><span class="sxs-lookup"><span data-stu-id="84126-135">1009 (0x3F1)</span></span>
</dt> <dt>



<span data-ttu-id="84126-136">Il database del registro di sistema di configurazione è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="84126-136">The configuration registry database is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-137"><span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**ERRORE \_ BADKEY**</span><span class="sxs-lookup"><span data-stu-id="84126-137"><span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**ERROR\_BADKEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-138">1010 (0x3F2)</span><span class="sxs-lookup"><span data-stu-id="84126-138">1010 (0x3F2)</span></span>
</dt> <dt>



<span data-ttu-id="84126-139">La chiave del registro di sistema di configurazione non è valida.</span><span class="sxs-lookup"><span data-stu-id="84126-139">The configuration registry key is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-140"><span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**ERRORE \_ CANTOPEN**</span><span class="sxs-lookup"><span data-stu-id="84126-140"><span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**ERROR\_CANTOPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-141">1011 (0x3F3)</span><span class="sxs-lookup"><span data-stu-id="84126-141">1011 (0x3F3)</span></span>
</dt> <dt>



<span data-ttu-id="84126-142">Non è stato possibile aprire la chiave del registro di sistema per la configurazione.</span><span class="sxs-lookup"><span data-stu-id="84126-142">The configuration registry key could not be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-143"><span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**ERRORE \_ CANTREAD**</span><span class="sxs-lookup"><span data-stu-id="84126-143"><span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**ERROR\_CANTREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-144">1012 (0x3F4)</span><span class="sxs-lookup"><span data-stu-id="84126-144">1012 (0x3F4)</span></span>
</dt> <dt>



<span data-ttu-id="84126-145">Impossibile leggere la chiave del registro di sistema per la configurazione.</span><span class="sxs-lookup"><span data-stu-id="84126-145">The configuration registry key could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-146"><span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**ERRORE \_ CANTWRITE**</span><span class="sxs-lookup"><span data-stu-id="84126-146"><span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**ERROR\_CANTWRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-147">1013 (0x3F5)</span><span class="sxs-lookup"><span data-stu-id="84126-147">1013 (0x3F5)</span></span>
</dt> <dt>



<span data-ttu-id="84126-148">Impossibile scrivere la chiave del registro di sistema per la configurazione.</span><span class="sxs-lookup"><span data-stu-id="84126-148">The configuration registry key could not be written.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-149"><span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**\_registro errori \_ recuperato**</span><span class="sxs-lookup"><span data-stu-id="84126-149"><span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**ERROR\_REGISTRY\_RECOVERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-150">1014 (0x3F6)</span><span class="sxs-lookup"><span data-stu-id="84126-150">1014 (0x3F6)</span></span>
</dt> <dt>



<span data-ttu-id="84126-151">Uno dei file nel database del registro di sistema deve essere recuperato tramite un log o una copia alternativa.</span><span class="sxs-lookup"><span data-stu-id="84126-151">One of the files in the registry database had to be recovered by use of a log or alternate copy.</span></span> <span data-ttu-id="84126-152">Il ripristino è stato completato correttamente.</span><span class="sxs-lookup"><span data-stu-id="84126-152">The recovery was successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-153"><span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**\_registro errori \_ danneggiato**</span><span class="sxs-lookup"><span data-stu-id="84126-153"><span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**ERROR\_REGISTRY\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-154">1015 (0x3F7)</span><span class="sxs-lookup"><span data-stu-id="84126-154">1015 (0x3F7)</span></span>
</dt> <dt>



<span data-ttu-id="84126-155">Il registro di sistema è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="84126-155">The registry is corrupted.</span></span> <span data-ttu-id="84126-156">La struttura di uno dei file contenenti i dati del registro di sistema è danneggiata oppure l'immagine di memoria del sistema del file è danneggiata oppure il file non può essere recuperato perché la copia o il registro alternativo è assente o danneggiato.</span><span class="sxs-lookup"><span data-stu-id="84126-156">The structure of one of the files containing registry data is corrupted, or the system's memory image of the file is corrupted, or the file could not be recovered because the alternate copy or log was absent or corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-157"><span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**ERRORE i/o \_ Registro di sistema \_ \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="84126-157"><span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**ERROR\_REGISTRY\_IO\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-158">1016 (0x3F8)</span><span class="sxs-lookup"><span data-stu-id="84126-158">1016 (0x3F8)</span></span>
</dt> <dt>



<span data-ttu-id="84126-159">Un'operazione di I/O avviata dal registro di sistema non è riuscita in modo irreversibile.</span><span class="sxs-lookup"><span data-stu-id="84126-159">An I/O operation initiated by the registry failed unrecoverably.</span></span> <span data-ttu-id="84126-160">Il registro di sistema non è stato in grado di leggere o scrivere o scaricare uno dei file che contiene l'immagine del sistema del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="84126-160">The registry could not read in, or write out, or flush, one of the files that contain the system's image of the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-161"><span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**ERRORE \_ nel \_ file del registro di sistema \_**</span><span class="sxs-lookup"><span data-stu-id="84126-161"><span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**ERROR\_NOT\_REGISTRY\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-162">1017 (0x3F9)</span><span class="sxs-lookup"><span data-stu-id="84126-162">1017 (0x3F9)</span></span>
</dt> <dt>



<span data-ttu-id="84126-163">Il sistema ha tentato di caricare o ripristinare un file nel registro di sistema, ma il file specificato non è in un formato di file del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="84126-163">The system has attempted to load or restore a file into the registry, but the specified file is not in a registry file format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-164"><span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**chiave di errore \_ \_ eliminata**</span><span class="sxs-lookup"><span data-stu-id="84126-164"><span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**ERROR\_KEY\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-165">1018 (0x3FA)</span><span class="sxs-lookup"><span data-stu-id="84126-165">1018 (0x3FA)</span></span>
</dt> <dt>



<span data-ttu-id="84126-166">Si è tentato di eseguire un'operazione non valida su una chiave del registro di sistema contrassegnata per l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="84126-166">Illegal operation attempted on a registry key that has been marked for deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-167"><span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**ERRORE \_ senza \_ spazio di log \_**</span><span class="sxs-lookup"><span data-stu-id="84126-167"><span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**ERROR\_NO\_LOG\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-168">1019 (0x3FB)</span><span class="sxs-lookup"><span data-stu-id="84126-168">1019 (0x3FB)</span></span>
</dt> <dt>



<span data-ttu-id="84126-169">Impossibile allocare lo spazio richiesto in un registro del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="84126-169">System could not allocate the required space in a registry log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-170"><span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**chiave di errore \_ \_ con \_ elementi figlio**</span><span class="sxs-lookup"><span data-stu-id="84126-170"><span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**ERROR\_KEY\_HAS\_CHILDREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-171">1020 (0x3FC)</span><span class="sxs-lookup"><span data-stu-id="84126-171">1020 (0x3FC)</span></span>
</dt> <dt>



<span data-ttu-id="84126-172">Non è possibile creare un collegamento simbolico in una chiave del registro di sistema in cui sono già presenti sottochiavi o valori.</span><span class="sxs-lookup"><span data-stu-id="84126-172">Cannot create a symbolic link in a registry key that already has subkeys or values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-173"><span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**il \_ figlio di errore \_ deve \_ essere \_ volatile**</span><span class="sxs-lookup"><span data-stu-id="84126-173"><span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**ERROR\_CHILD\_MUST\_BE\_VOLATILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-174">1021 (0x3FD)</span><span class="sxs-lookup"><span data-stu-id="84126-174">1021 (0x3FD)</span></span>
</dt> <dt>



<span data-ttu-id="84126-175">Non è possibile creare una sottochiave stabile in una chiave padre volatile.</span><span class="sxs-lookup"><span data-stu-id="84126-175">Cannot create a stable subkey under a volatile parent key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-176"><span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**ERRORE di \_ notifica dell' \_ enumerazione \_ dir**</span><span class="sxs-lookup"><span data-stu-id="84126-176"><span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**ERROR\_NOTIFY\_ENUM\_DIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-177">1022 (0x3FE)</span><span class="sxs-lookup"><span data-stu-id="84126-177">1022 (0x3FE)</span></span>
</dt> <dt>



<span data-ttu-id="84126-178">Viene completata una richiesta di modifica della notifica e le informazioni non vengono restituite nel buffer del chiamante.</span><span class="sxs-lookup"><span data-stu-id="84126-178">A notify change request is being completed and the information is not being returned in the caller's buffer.</span></span> <span data-ttu-id="84126-179">Il chiamante deve ora enumerare i file per individuare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="84126-179">The caller now needs to enumerate the files to find the changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-180"><span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**\_servizi dipendenti dall'errore \_ \_ in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="84126-180"><span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**ERROR\_DEPENDENT\_SERVICES\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-181">1051 (0x41B)</span><span class="sxs-lookup"><span data-stu-id="84126-181">1051 (0x41B)</span></span>
</dt> <dt>



<span data-ttu-id="84126-182">Un controllo stop è stato inviato a un servizio da cui dipendono altri servizi in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="84126-182">A stop control has been sent to a service that other running services are dependent on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-183"><span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**ERRORE \_ di \_ controllo del servizio non valido \_**</span><span class="sxs-lookup"><span data-stu-id="84126-183"><span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**ERROR\_INVALID\_SERVICE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-184">1052 (0x41C)</span><span class="sxs-lookup"><span data-stu-id="84126-184">1052 (0x41C)</span></span>
</dt> <dt>



<span data-ttu-id="84126-185">Il controllo richiesto non è valido per questo servizio.</span><span class="sxs-lookup"><span data-stu-id="84126-185">The requested control is not valid for this service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-186"><span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**\_timeout della \_ richiesta del servizio di errore \_**</span><span class="sxs-lookup"><span data-stu-id="84126-186"><span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**ERROR\_SERVICE\_REQUEST\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-187">1053 (0x41D)</span><span class="sxs-lookup"><span data-stu-id="84126-187">1053 (0x41D)</span></span>
</dt> <dt>



<span data-ttu-id="84126-188">Il servizio non ha risposto in tempo utile alla richiesta di avvio o di controllo.</span><span class="sxs-lookup"><span data-stu-id="84126-188">The service did not respond to the start or control request in a timely fashion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-189"><span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**ERRORE \_ servizio \_ senza \_ thread**</span><span class="sxs-lookup"><span data-stu-id="84126-189"><span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**ERROR\_SERVICE\_NO\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-190">1054 (0x41E)</span><span class="sxs-lookup"><span data-stu-id="84126-190">1054 (0x41E)</span></span>
</dt> <dt>



<span data-ttu-id="84126-191">Non è stato possibile creare un thread per il servizio.</span><span class="sxs-lookup"><span data-stu-id="84126-191">A thread could not be created for the service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-192"><span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**DATABASE del servizio di errore \_ \_ \_ bloccato**</span><span class="sxs-lookup"><span data-stu-id="84126-192"><span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**ERROR\_SERVICE\_DATABASE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-193">1055 (0x41F)</span><span class="sxs-lookup"><span data-stu-id="84126-193">1055 (0x41F)</span></span>
</dt> <dt>



<span data-ttu-id="84126-194">Il database del servizio è bloccato.</span><span class="sxs-lookup"><span data-stu-id="84126-194">The service database is locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-195"><span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**\_servizio errori \_ già \_ in esecuzione**</span><span class="sxs-lookup"><span data-stu-id="84126-195"><span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**ERROR\_SERVICE\_ALREADY\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-196">1056 (0x420)</span><span class="sxs-lookup"><span data-stu-id="84126-196">1056 (0x420)</span></span>
</dt> <dt>



<span data-ttu-id="84126-197">Un'istanza del servizio è già in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="84126-197">An instance of the service is already running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-198"><span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**ERRORE \_ dell' \_ account del servizio non valido \_**</span><span class="sxs-lookup"><span data-stu-id="84126-198"><span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**ERROR\_INVALID\_SERVICE\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-199">1057 (0x421)</span><span class="sxs-lookup"><span data-stu-id="84126-199">1057 (0x421)</span></span>
</dt> <dt>



<span data-ttu-id="84126-200">Il nome dell'account non è valido o non esiste oppure la password non è valida per il nome dell'account specificato.</span><span class="sxs-lookup"><span data-stu-id="84126-200">The account name is invalid or does not exist, or the password is invalid for the account name specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-201"><span id="ERROR_SERVICE_DISABLED"></span><span id="error_service_disabled"></span>**\_servizio errori \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="84126-201"><span id="ERROR_SERVICE_DISABLED"></span><span id="error_service_disabled"></span>**ERROR\_SERVICE\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-202">1058 (0x422)</span><span class="sxs-lookup"><span data-stu-id="84126-202">1058 (0x422)</span></span>
</dt> <dt>



<span data-ttu-id="84126-203">Non è possibile avviare il servizio perché è disabilitato o perché ad esso non è associato alcun dispositivo abilitato.</span><span class="sxs-lookup"><span data-stu-id="84126-203">The service cannot be started, either because it is disabled or because it has no enabled devices associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-204"><span id="ERROR_CIRCULAR_DEPENDENCY"></span><span id="error_circular_dependency"></span>**\_dipendenza circolare degli errori \_**</span><span class="sxs-lookup"><span data-stu-id="84126-204"><span id="ERROR_CIRCULAR_DEPENDENCY"></span><span id="error_circular_dependency"></span>**ERROR\_CIRCULAR\_DEPENDENCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-205">1059 (0x423)</span><span class="sxs-lookup"><span data-stu-id="84126-205">1059 (0x423)</span></span>
</dt> <dt>



<span data-ttu-id="84126-206">È stata specificata la dipendenza circolare del servizio.</span><span class="sxs-lookup"><span data-stu-id="84126-206">Circular service dependency was specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-207"><span id="ERROR_SERVICE_DOES_NOT_EXIST"></span><span id="error_service_does_not_exist"></span>**\_il servizio errori non \_ \_ \_ esiste**</span><span class="sxs-lookup"><span data-stu-id="84126-207"><span id="ERROR_SERVICE_DOES_NOT_EXIST"></span><span id="error_service_does_not_exist"></span>**ERROR\_SERVICE\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-208">1060 (0x424)</span><span class="sxs-lookup"><span data-stu-id="84126-208">1060 (0x424)</span></span>
</dt> <dt>



<span data-ttu-id="84126-209">Il servizio specificato non esiste come servizio installato.</span><span class="sxs-lookup"><span data-stu-id="84126-209">The specified service does not exist as an installed service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-210"><span id="ERROR_SERVICE_CANNOT_ACCEPT_CTRL"></span><span id="error_service_cannot_accept_ctrl"></span>**il \_ servizio di errore \_ non può \_ accettare \_ CTRL**</span><span class="sxs-lookup"><span data-stu-id="84126-210"><span id="ERROR_SERVICE_CANNOT_ACCEPT_CTRL"></span><span id="error_service_cannot_accept_ctrl"></span>**ERROR\_SERVICE\_CANNOT\_ACCEPT\_CTRL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-211">1061 (0x425)</span><span class="sxs-lookup"><span data-stu-id="84126-211">1061 (0x425)</span></span>
</dt> <dt>



<span data-ttu-id="84126-212">Il servizio non può accettare messaggi di controllo in questo momento.</span><span class="sxs-lookup"><span data-stu-id="84126-212">The service cannot accept control messages at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-213"><span id="ERROR_SERVICE_NOT_ACTIVE"></span><span id="error_service_not_active"></span>**\_servizio errori \_ non \_ attivo**</span><span class="sxs-lookup"><span data-stu-id="84126-213"><span id="ERROR_SERVICE_NOT_ACTIVE"></span><span id="error_service_not_active"></span>**ERROR\_SERVICE\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-214">1062 (0x426)</span><span class="sxs-lookup"><span data-stu-id="84126-214">1062 (0x426)</span></span>
</dt> <dt>



<span data-ttu-id="84126-215">Il servizio non è stato avviato.</span><span class="sxs-lookup"><span data-stu-id="84126-215">The service has not been started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-216"><span id="ERROR_FAILED_SERVICE_CONTROLLER_CONNECT"></span><span id="error_failed_service_controller_connect"></span>**ERRORE \_ di \_ \_ connessione del controller di servizio non riuscito \_**</span><span class="sxs-lookup"><span data-stu-id="84126-216"><span id="ERROR_FAILED_SERVICE_CONTROLLER_CONNECT"></span><span id="error_failed_service_controller_connect"></span>**ERROR\_FAILED\_SERVICE\_CONTROLLER\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-217">1063 (0x427)</span><span class="sxs-lookup"><span data-stu-id="84126-217">1063 (0x427)</span></span>
</dt> <dt>



<span data-ttu-id="84126-218">Il processo del servizio non è stato in grado di connettersi al controller del servizio.</span><span class="sxs-lookup"><span data-stu-id="84126-218">The service process could not connect to the service controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-219"><span id="ERROR_EXCEPTION_IN_SERVICE"></span><span id="error_exception_in_service"></span>**\_eccezione \_ di errore nel \_ servizio**</span><span class="sxs-lookup"><span data-stu-id="84126-219"><span id="ERROR_EXCEPTION_IN_SERVICE"></span><span id="error_exception_in_service"></span>**ERROR\_EXCEPTION\_IN\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-220">1064 (0x428)</span><span class="sxs-lookup"><span data-stu-id="84126-220">1064 (0x428)</span></span>
</dt> <dt>



<span data-ttu-id="84126-221">Si è verificata un'eccezione nel servizio durante la gestione della richiesta di controllo.</span><span class="sxs-lookup"><span data-stu-id="84126-221">An exception occurred in the service when handling the control request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-222"><span id="ERROR_DATABASE_DOES_NOT_EXIST"></span><span id="error_database_does_not_exist"></span>**il database degli errori non \_ \_ \_ \_ esiste**</span><span class="sxs-lookup"><span data-stu-id="84126-222"><span id="ERROR_DATABASE_DOES_NOT_EXIST"></span><span id="error_database_does_not_exist"></span>**ERROR\_DATABASE\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-223">1065 (0x429)</span><span class="sxs-lookup"><span data-stu-id="84126-223">1065 (0x429)</span></span>
</dt> <dt>



<span data-ttu-id="84126-224">Il database specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="84126-224">The database specified does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-225"><span id="ERROR_SERVICE_SPECIFIC_ERROR"></span><span id="error_service_specific_error"></span>**errore \_ specifico del servizio di errore \_ \_**</span><span class="sxs-lookup"><span data-stu-id="84126-225"><span id="ERROR_SERVICE_SPECIFIC_ERROR"></span><span id="error_service_specific_error"></span>**ERROR\_SERVICE\_SPECIFIC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-226">1066 (0x42A)</span><span class="sxs-lookup"><span data-stu-id="84126-226">1066 (0x42A)</span></span>
</dt> <dt>



<span data-ttu-id="84126-227">Il servizio ha restituito un codice di errore specifico del servizio.</span><span class="sxs-lookup"><span data-stu-id="84126-227">The service has returned a service-specific error code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-228"><span id="ERROR_PROCESS_ABORTED"></span><span id="error_process_aborted"></span>**processo di errore \_ \_ interrotto**</span><span class="sxs-lookup"><span data-stu-id="84126-228"><span id="ERROR_PROCESS_ABORTED"></span><span id="error_process_aborted"></span>**ERROR\_PROCESS\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-229">1067 (0x42B)</span><span class="sxs-lookup"><span data-stu-id="84126-229">1067 (0x42B)</span></span>
</dt> <dt>



<span data-ttu-id="84126-230">Il processo è stato terminato in modo imprevisto.</span><span class="sxs-lookup"><span data-stu-id="84126-230">The process terminated unexpectedly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-231"><span id="ERROR_SERVICE_DEPENDENCY_FAIL"></span><span id="error_service_dependency_fail"></span>**errore di \_ dipendenza del servizio errori \_ \_**</span><span class="sxs-lookup"><span data-stu-id="84126-231"><span id="ERROR_SERVICE_DEPENDENCY_FAIL"></span><span id="error_service_dependency_fail"></span>**ERROR\_SERVICE\_DEPENDENCY\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-232">1068 (0x42C)</span><span class="sxs-lookup"><span data-stu-id="84126-232">1068 (0x42C)</span></span>
</dt> <dt>



<span data-ttu-id="84126-233">Impossibile avviare il servizio o il gruppo di dipendenze.</span><span class="sxs-lookup"><span data-stu-id="84126-233">The dependency service or group failed to start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-234"><span id="ERROR_SERVICE_LOGON_FAILED"></span><span id="error_service_logon_failed"></span>**accesso al servizio di errore \_ \_ \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="84126-234"><span id="ERROR_SERVICE_LOGON_FAILED"></span><span id="error_service_logon_failed"></span>**ERROR\_SERVICE\_LOGON\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-235">1069 (0x42D)</span><span class="sxs-lookup"><span data-stu-id="84126-235">1069 (0x42D)</span></span>
</dt> <dt>



<span data-ttu-id="84126-236">il servizio non è stato avviato a causa di un errore in fase di accesso.</span><span class="sxs-lookup"><span data-stu-id="84126-236">The service did not start due to a logon failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-237"><span id="ERROR_SERVICE_START_HANG"></span><span id="error_service_start_hang"></span>**\_ \_ blocco avvio servizio \_ errori**</span><span class="sxs-lookup"><span data-stu-id="84126-237"><span id="ERROR_SERVICE_START_HANG"></span><span id="error_service_start_hang"></span>**ERROR\_SERVICE\_START\_HANG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-238">1070 (0x42E)</span><span class="sxs-lookup"><span data-stu-id="84126-238">1070 (0x42E)</span></span>
</dt> <dt>



<span data-ttu-id="84126-239">Dopo l'avvio, il servizio è stato bloccato in uno stato di avvio in sospeso.</span><span class="sxs-lookup"><span data-stu-id="84126-239">After starting, the service hung in a start-pending state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-240"><span id="ERROR_INVALID_SERVICE_LOCK"></span><span id="error_invalid_service_lock"></span>**ERRORE \_ \_ Blocco servizio non valido \_**</span><span class="sxs-lookup"><span data-stu-id="84126-240"><span id="ERROR_INVALID_SERVICE_LOCK"></span><span id="error_invalid_service_lock"></span>**ERROR\_INVALID\_SERVICE\_LOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-241">1071 (0x42F)</span><span class="sxs-lookup"><span data-stu-id="84126-241">1071 (0x42F)</span></span>
</dt> <dt>



<span data-ttu-id="84126-242">Il blocco del database del servizio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="84126-242">The specified service database lock is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-243"><span id="ERROR_SERVICE_MARKED_FOR_DELETE"></span><span id="error_service_marked_for_delete"></span>**\_servizio \_ di errore contrassegnato per l' \_ \_ eliminazione**</span><span class="sxs-lookup"><span data-stu-id="84126-243"><span id="ERROR_SERVICE_MARKED_FOR_DELETE"></span><span id="error_service_marked_for_delete"></span>**ERROR\_SERVICE\_MARKED\_FOR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-244">1072 (0x430)</span><span class="sxs-lookup"><span data-stu-id="84126-244">1072 (0x430)</span></span>
</dt> <dt>



<span data-ttu-id="84126-245">Il servizio specificato è stato contrassegnato per l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="84126-245">The specified service has been marked for deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-246"><span id="ERROR_SERVICE_EXISTS"></span><span id="error_service_exists"></span>**il \_ servizio di errore \_ esiste**</span><span class="sxs-lookup"><span data-stu-id="84126-246"><span id="ERROR_SERVICE_EXISTS"></span><span id="error_service_exists"></span>**ERROR\_SERVICE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-247">1073 (0x431)</span><span class="sxs-lookup"><span data-stu-id="84126-247">1073 (0x431)</span></span>
</dt> <dt>



<span data-ttu-id="84126-248">Il servizio specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="84126-248">The specified service already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-249"><span id="ERROR_ALREADY_RUNNING_LKG"></span><span id="error_already_running_lkg"></span>**errore durante l' \_ \_ esecuzione di \_ Ultima**</span><span class="sxs-lookup"><span data-stu-id="84126-249"><span id="ERROR_ALREADY_RUNNING_LKG"></span><span id="error_already_running_lkg"></span>**ERROR\_ALREADY\_RUNNING\_LKG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-250">1074 (0x432)</span><span class="sxs-lookup"><span data-stu-id="84126-250">1074 (0x432)</span></span>
</dt> <dt>



<span data-ttu-id="84126-251">Il sistema è attualmente in esecuzione con l'ultima configurazione ben nota.</span><span class="sxs-lookup"><span data-stu-id="84126-251">The system is currently running with the last-known-good configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-252"><span id="ERROR_SERVICE_DEPENDENCY_DELETED"></span><span id="error_service_dependency_deleted"></span>**dipendenza del servizio di errore \_ \_ \_ eliminata**</span><span class="sxs-lookup"><span data-stu-id="84126-252"><span id="ERROR_SERVICE_DEPENDENCY_DELETED"></span><span id="error_service_dependency_deleted"></span>**ERROR\_SERVICE\_DEPENDENCY\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-253">1075 (0x433)</span><span class="sxs-lookup"><span data-stu-id="84126-253">1075 (0x433)</span></span>
</dt> <dt>



<span data-ttu-id="84126-254">Il servizio di dipendenza non esiste o è stato contrassegnato per l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="84126-254">The dependency service does not exist or has been marked for deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-255"><span id="ERROR_BOOT_ALREADY_ACCEPTED"></span><span id="error_boot_already_accepted"></span>**ERRORE di \_ avvio \_ già \_ accettato**</span><span class="sxs-lookup"><span data-stu-id="84126-255"><span id="ERROR_BOOT_ALREADY_ACCEPTED"></span><span id="error_boot_already_accepted"></span>**ERROR\_BOOT\_ALREADY\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-256">1076 (0x434)</span><span class="sxs-lookup"><span data-stu-id="84126-256">1076 (0x434)</span></span>
</dt> <dt>



<span data-ttu-id="84126-257">L'avvio corrente è già stato accettato per l'uso come ultimo set di controlli valido.</span><span class="sxs-lookup"><span data-stu-id="84126-257">The current boot has already been accepted for use as the last-known-good control set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-258"><span id="ERROR_SERVICE_NEVER_STARTED"></span><span id="error_service_never_started"></span>**il \_ servizio di errore \_ non è mai stato \_ avviato**</span><span class="sxs-lookup"><span data-stu-id="84126-258"><span id="ERROR_SERVICE_NEVER_STARTED"></span><span id="error_service_never_started"></span>**ERROR\_SERVICE\_NEVER\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-259">1077 (0x435)</span><span class="sxs-lookup"><span data-stu-id="84126-259">1077 (0x435)</span></span>
</dt> <dt>



<span data-ttu-id="84126-260">Nessun tentativo di avviare il servizio è stato eseguito dopo l'ultimo avvio.</span><span class="sxs-lookup"><span data-stu-id="84126-260">No attempts to start the service have been made since the last boot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-261"><span id="ERROR_DUPLICATE_SERVICE_NAME"></span><span id="error_duplicate_service_name"></span>**\_nome del \_ servizio DUPLICAto errore \_**</span><span class="sxs-lookup"><span data-stu-id="84126-261"><span id="ERROR_DUPLICATE_SERVICE_NAME"></span><span id="error_duplicate_service_name"></span>**ERROR\_DUPLICATE\_SERVICE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-262">1078 (0x436)</span><span class="sxs-lookup"><span data-stu-id="84126-262">1078 (0x436)</span></span>
</dt> <dt>



<span data-ttu-id="84126-263">Il nome è già in uso come nome del servizio o nome visualizzato del servizio.</span><span class="sxs-lookup"><span data-stu-id="84126-263">The name is already in use as either a service name or a service display name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-264"><span id="ERROR_DIFFERENT_SERVICE_ACCOUNT"></span><span id="error_different_service_account"></span>**ERRORE \_ dell' \_ account del servizio diverso \_**</span><span class="sxs-lookup"><span data-stu-id="84126-264"><span id="ERROR_DIFFERENT_SERVICE_ACCOUNT"></span><span id="error_different_service_account"></span>**ERROR\_DIFFERENT\_SERVICE\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-265">1079 (0x437)</span><span class="sxs-lookup"><span data-stu-id="84126-265">1079 (0x437)</span></span>
</dt> <dt>



<span data-ttu-id="84126-266">L'account specificato per questo servizio è diverso dall'account specificato per altri servizi in esecuzione nello stesso processo.</span><span class="sxs-lookup"><span data-stu-id="84126-266">The account specified for this service is different from the account specified for other services running in the same process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-267"><span id="ERROR_CANNOT_DETECT_DRIVER_FAILURE"></span><span id="error_cannot_detect_driver_failure"></span>**errore durante il rilevamento dell'errore del \_ \_ \_ driver \_**</span><span class="sxs-lookup"><span data-stu-id="84126-267"><span id="ERROR_CANNOT_DETECT_DRIVER_FAILURE"></span><span id="error_cannot_detect_driver_failure"></span>**ERROR\_CANNOT\_DETECT\_DRIVER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-268">1080 (nell'0x438)</span><span class="sxs-lookup"><span data-stu-id="84126-268">1080 (0x438)</span></span>
</dt> <dt>



<span data-ttu-id="84126-269">Le azioni di errore possono essere impostate solo per i servizi Win32, non per i driver.</span><span class="sxs-lookup"><span data-stu-id="84126-269">Failure actions can only be set for Win32 services, not for drivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-270"><span id="ERROR_CANNOT_DETECT_PROCESS_ABORT"></span><span id="error_cannot_detect_process_abort"></span>**ERRORE \_ non è in grado di \_ rilevare l' \_ interruzione del processo \_**</span><span class="sxs-lookup"><span data-stu-id="84126-270"><span id="ERROR_CANNOT_DETECT_PROCESS_ABORT"></span><span id="error_cannot_detect_process_abort"></span>**ERROR\_CANNOT\_DETECT\_PROCESS\_ABORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-271">1081 (0x439)</span><span class="sxs-lookup"><span data-stu-id="84126-271">1081 (0x439)</span></span>
</dt> <dt>



<span data-ttu-id="84126-272">Questo servizio viene eseguito nello stesso processo di gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="84126-272">This service runs in the same process as the service control manager.</span></span> <span data-ttu-id="84126-273">Pertanto, gestione controllo servizi non può intervenire se il processo del servizio viene terminato in modo imprevisto.</span><span class="sxs-lookup"><span data-stu-id="84126-273">Therefore, the service control manager cannot take action if this service's process terminates unexpectedly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-274"><span id="ERROR_NO_RECOVERY_PROGRAM"></span><span id="error_no_recovery_program"></span>**ERRORE \_ nessun \_ programma di ripristino \_**</span><span class="sxs-lookup"><span data-stu-id="84126-274"><span id="ERROR_NO_RECOVERY_PROGRAM"></span><span id="error_no_recovery_program"></span>**ERROR\_NO\_RECOVERY\_PROGRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-275">1082 (0x43A)</span><span class="sxs-lookup"><span data-stu-id="84126-275">1082 (0x43A)</span></span>
</dt> <dt>



<span data-ttu-id="84126-276">Nessun programma di ripristino configurato per questo servizio.</span><span class="sxs-lookup"><span data-stu-id="84126-276">No recovery program has been configured for this service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-277"><span id="ERROR_SERVICE_NOT_IN_EXE"></span><span id="error_service_not_in_exe"></span>**\_servizio errori \_ non presente nel file \_ \_ exe**</span><span class="sxs-lookup"><span data-stu-id="84126-277"><span id="ERROR_SERVICE_NOT_IN_EXE"></span><span id="error_service_not_in_exe"></span>**ERROR\_SERVICE\_NOT\_IN\_EXE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-278">1083 (0x43B)</span><span class="sxs-lookup"><span data-stu-id="84126-278">1083 (0x43B)</span></span>
</dt> <dt>



<span data-ttu-id="84126-279">Il programma eseguibile che questo servizio è configurato per l'esecuzione in non implementa il servizio.</span><span class="sxs-lookup"><span data-stu-id="84126-279">The executable program that this service is configured to run in does not implement the service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-280"><span id="ERROR_NOT_SAFEBOOT_SERVICE"></span><span id="error_not_safeboot_service"></span>**ERRORE \_ non è il \_ \_ servizio SafeBoot**</span><span class="sxs-lookup"><span data-stu-id="84126-280"><span id="ERROR_NOT_SAFEBOOT_SERVICE"></span><span id="error_not_safeboot_service"></span>**ERROR\_NOT\_SAFEBOOT\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-281">1084 (0x43C)</span><span class="sxs-lookup"><span data-stu-id="84126-281">1084 (0x43C)</span></span>
</dt> <dt>



<span data-ttu-id="84126-282">Impossibile avviare il servizio in modalità provvisoria.</span><span class="sxs-lookup"><span data-stu-id="84126-282">This service cannot be started in Safe Mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-283"><span id="ERROR_END_OF_MEDIA"></span><span id="error_end_of_media"></span>**\_fine errore \_ del \_ supporto**</span><span class="sxs-lookup"><span data-stu-id="84126-283"><span id="ERROR_END_OF_MEDIA"></span><span id="error_end_of_media"></span>**ERROR\_END\_OF\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-284">1100 (0x44C)</span><span class="sxs-lookup"><span data-stu-id="84126-284">1100 (0x44C)</span></span>
</dt> <dt>



<span data-ttu-id="84126-285">È stata raggiunta la fine fisica del nastro.</span><span class="sxs-lookup"><span data-stu-id="84126-285">The physical end of the tape has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-286"><span id="ERROR_FILEMARK_DETECTED"></span><span id="error_filemark_detected"></span>**\_rilevato errore FILEmark \_**</span><span class="sxs-lookup"><span data-stu-id="84126-286"><span id="ERROR_FILEMARK_DETECTED"></span><span id="error_filemark_detected"></span>**ERROR\_FILEMARK\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-287">1101 (0x44D)</span><span class="sxs-lookup"><span data-stu-id="84126-287">1101 (0x44D)</span></span>
</dt> <dt>



<span data-ttu-id="84126-288">Un accesso al nastro ha raggiunto un oggetto filemark.</span><span class="sxs-lookup"><span data-stu-id="84126-288">A tape access reached a filemark.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-289"><span id="ERROR_BEGINNING_OF_MEDIA"></span><span id="error_beginning_of_media"></span>**ERRORE \_ \_ di inizio del \_ supporto**</span><span class="sxs-lookup"><span data-stu-id="84126-289"><span id="ERROR_BEGINNING_OF_MEDIA"></span><span id="error_beginning_of_media"></span>**ERROR\_BEGINNING\_OF\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-290">1102 (0x44E)</span><span class="sxs-lookup"><span data-stu-id="84126-290">1102 (0x44E)</span></span>
</dt> <dt>



<span data-ttu-id="84126-291">È stato rilevato l'inizio del nastro o di una partizione.</span><span class="sxs-lookup"><span data-stu-id="84126-291">The beginning of the tape or a partition was encountered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-292"><span id="ERROR_SETMARK_DETECTED"></span><span id="error_setmark_detected"></span>**\_indicatore di errore \_ rilevato**</span><span class="sxs-lookup"><span data-stu-id="84126-292"><span id="ERROR_SETMARK_DETECTED"></span><span id="error_setmark_detected"></span>**ERROR\_SETMARK\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-293">1103 (0x44F)</span><span class="sxs-lookup"><span data-stu-id="84126-293">1103 (0x44F)</span></span>
</dt> <dt>



<span data-ttu-id="84126-294">Un accesso al nastro ha raggiunto la fine di un set di file.</span><span class="sxs-lookup"><span data-stu-id="84126-294">A tape access reached the end of a set of files.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-295"><span id="ERROR_NO_DATA_DETECTED"></span><span id="error_no_data_detected"></span>**ERRORE \_ nessun \_ dato \_ rilevato**</span><span class="sxs-lookup"><span data-stu-id="84126-295"><span id="ERROR_NO_DATA_DETECTED"></span><span id="error_no_data_detected"></span>**ERROR\_NO\_DATA\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-296">1104 (0x450)</span><span class="sxs-lookup"><span data-stu-id="84126-296">1104 (0x450)</span></span>
</dt> <dt>



<span data-ttu-id="84126-297">Nessun altro dato sul nastro.</span><span class="sxs-lookup"><span data-stu-id="84126-297">No more data is on the tape.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-298"><span id="ERROR_PARTITION_FAILURE"></span><span id="error_partition_failure"></span>**errore \_ partizione \_ errore**</span><span class="sxs-lookup"><span data-stu-id="84126-298"><span id="ERROR_PARTITION_FAILURE"></span><span id="error_partition_failure"></span>**ERROR\_PARTITION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-299">1105 (0x451)</span><span class="sxs-lookup"><span data-stu-id="84126-299">1105 (0x451)</span></span>
</dt> <dt>



<span data-ttu-id="84126-300">Non è stato possibile partizionare il nastro.</span><span class="sxs-lookup"><span data-stu-id="84126-300">Tape could not be partitioned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-301"><span id="ERROR_INVALID_BLOCK_LENGTH"></span><span id="error_invalid_block_length"></span>**ERRORE \_ \_ Lunghezza blocco non valida \_**</span><span class="sxs-lookup"><span data-stu-id="84126-301"><span id="ERROR_INVALID_BLOCK_LENGTH"></span><span id="error_invalid_block_length"></span>**ERROR\_INVALID\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-302">1106 (0x452)</span><span class="sxs-lookup"><span data-stu-id="84126-302">1106 (0x452)</span></span>
</dt> <dt>



<span data-ttu-id="84126-303">Quando si accede a un nuovo nastro di una partizione multivolume, le dimensioni correnti del blocco non sono corrette.</span><span class="sxs-lookup"><span data-stu-id="84126-303">When accessing a new tape of a multivolume partition, the current block size is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-304"><span id="ERROR_DEVICE_NOT_PARTITIONED"></span><span id="error_device_not_partitioned"></span>**ERRORE \_ dispositivo \_ non \_ partizionato**</span><span class="sxs-lookup"><span data-stu-id="84126-304"><span id="ERROR_DEVICE_NOT_PARTITIONED"></span><span id="error_device_not_partitioned"></span>**ERROR\_DEVICE\_NOT\_PARTITIONED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-305">1107 (0x453)</span><span class="sxs-lookup"><span data-stu-id="84126-305">1107 (0x453)</span></span>
</dt> <dt>



<span data-ttu-id="84126-306">Impossibile trovare le informazioni sulla partizione del nastro durante il caricamento di un nastro.</span><span class="sxs-lookup"><span data-stu-id="84126-306">Tape partition information could not be found when loading a tape.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-307"><span id="ERROR_UNABLE_TO_LOCK_MEDIA"></span><span id="error_unable_to_lock_media"></span>**ERRORE \_ non è possibile \_ \_ bloccare i \_ supporti**</span><span class="sxs-lookup"><span data-stu-id="84126-307"><span id="ERROR_UNABLE_TO_LOCK_MEDIA"></span><span id="error_unable_to_lock_media"></span>**ERROR\_UNABLE\_TO\_LOCK\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-308">1108 (0x454)</span><span class="sxs-lookup"><span data-stu-id="84126-308">1108 (0x454)</span></span>
</dt> <dt>



<span data-ttu-id="84126-309">Impossibile bloccare il meccanismo di espulsione dei supporti.</span><span class="sxs-lookup"><span data-stu-id="84126-309">Unable to lock the media eject mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-310"><span id="ERROR_UNABLE_TO_UNLOAD_MEDIA"></span><span id="error_unable_to_unload_media"></span>**errore durante lo \_ \_ \_ scaricamento del \_ supporto**</span><span class="sxs-lookup"><span data-stu-id="84126-310"><span id="ERROR_UNABLE_TO_UNLOAD_MEDIA"></span><span id="error_unable_to_unload_media"></span>**ERROR\_UNABLE\_TO\_UNLOAD\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-311">1109 (0x455)</span><span class="sxs-lookup"><span data-stu-id="84126-311">1109 (0x455)</span></span>
</dt> <dt>



<span data-ttu-id="84126-312">Impossibile scaricare il supporto.</span><span class="sxs-lookup"><span data-stu-id="84126-312">Unable to unload the media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-313"><span id="ERROR_MEDIA_CHANGED"></span><span id="error_media_changed"></span>**\_supporto errori \_ modificato**</span><span class="sxs-lookup"><span data-stu-id="84126-313"><span id="ERROR_MEDIA_CHANGED"></span><span id="error_media_changed"></span>**ERROR\_MEDIA\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-314">1110 (0x456)</span><span class="sxs-lookup"><span data-stu-id="84126-314">1110 (0x456)</span></span>
</dt> <dt>



<span data-ttu-id="84126-315">È possibile che il supporto nell'unità sia stato modificato.</span><span class="sxs-lookup"><span data-stu-id="84126-315">The media in the drive may have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-316"><span id="ERROR_BUS_RESET"></span><span id="error_bus_reset"></span>**reimpostazione del bus di errore \_ \_**</span><span class="sxs-lookup"><span data-stu-id="84126-316"><span id="ERROR_BUS_RESET"></span><span id="error_bus_reset"></span>**ERROR\_BUS\_RESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-317">1111 (0x457)</span><span class="sxs-lookup"><span data-stu-id="84126-317">1111 (0x457)</span></span>
</dt> <dt>



<span data-ttu-id="84126-318">Il bus di I/O è stato reimpostato.</span><span class="sxs-lookup"><span data-stu-id="84126-318">The I/O bus was reset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-319"><span id="ERROR_NO_MEDIA_IN_DRIVE"></span><span id="error_no_media_in_drive"></span>**ERRORE \_ nessun \_ supporto \_ nell' \_ unità**</span><span class="sxs-lookup"><span data-stu-id="84126-319"><span id="ERROR_NO_MEDIA_IN_DRIVE"></span><span id="error_no_media_in_drive"></span>**ERROR\_NO\_MEDIA\_IN\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-320">1112 (0x458)</span><span class="sxs-lookup"><span data-stu-id="84126-320">1112 (0x458)</span></span>
</dt> <dt>



<span data-ttu-id="84126-321">Nessun supporto nell'unità.</span><span class="sxs-lookup"><span data-stu-id="84126-321">No media in drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-322"><span id="ERROR_NO_UNICODE_TRANSLATION"></span><span id="error_no_unicode_translation"></span>**ERRORE \_ Nessuna \_ \_ conversione Unicode**</span><span class="sxs-lookup"><span data-stu-id="84126-322"><span id="ERROR_NO_UNICODE_TRANSLATION"></span><span id="error_no_unicode_translation"></span>**ERROR\_NO\_UNICODE\_TRANSLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-323">1113 (0x459)</span><span class="sxs-lookup"><span data-stu-id="84126-323">1113 (0x459)</span></span>
</dt> <dt>



<span data-ttu-id="84126-324">Non esiste alcun mapping per il carattere Unicode nella tabella codici multibyte di destinazione.</span><span class="sxs-lookup"><span data-stu-id="84126-324">No mapping for the Unicode character exists in the target multi-byte code page.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-325"><span id="ERROR_DLL_INIT_FAILED"></span><span id="error_dll_init_failed"></span>**ERRORE \_ di \_ inizializzazione DLL \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="84126-325"><span id="ERROR_DLL_INIT_FAILED"></span><span id="error_dll_init_failed"></span>**ERROR\_DLL\_INIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-326">1114 (0x45A)</span><span class="sxs-lookup"><span data-stu-id="84126-326">1114 (0x45A)</span></span>
</dt> <dt>



<span data-ttu-id="84126-327">Routine di inizializzazione DLL (Dynamic Link Library) non riuscita.</span><span class="sxs-lookup"><span data-stu-id="84126-327">A dynamic link library (DLL) initialization routine failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-328"><span id="ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="error_shutdown_in_progress"></span>**ERRORE \_ \_ di arresto in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="84126-328"><span id="ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="error_shutdown_in_progress"></span>**ERROR\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-329">1115 (0x45B)</span><span class="sxs-lookup"><span data-stu-id="84126-329">1115 (0x45B)</span></span>
</dt> <dt>



<span data-ttu-id="84126-330">È in corso l'arresto del sistema.</span><span class="sxs-lookup"><span data-stu-id="84126-330">A system shutdown is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-331"><span id="ERROR_NO_SHUTDOWN_IN_PROGRESS"></span><span id="error_no_shutdown_in_progress"></span>**ERRORE \_ nessun \_ arresto \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="84126-331"><span id="ERROR_NO_SHUTDOWN_IN_PROGRESS"></span><span id="error_no_shutdown_in_progress"></span>**ERROR\_NO\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-332">1116 (0x45C)</span><span class="sxs-lookup"><span data-stu-id="84126-332">1116 (0x45C)</span></span>
</dt> <dt>



<span data-ttu-id="84126-333">Impossibile interrompere l'arresto del sistema perché non è in corso l'arresto.</span><span class="sxs-lookup"><span data-stu-id="84126-333">Unable to abort the system shutdown because no shutdown was in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-334"><span id="ERROR_IO_DEVICE"></span><span id="error_io_device"></span>**ERRORE \_ io \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="84126-334"><span id="ERROR_IO_DEVICE"></span><span id="error_io_device"></span>**ERROR\_IO\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-335">1117 (0x45D)</span><span class="sxs-lookup"><span data-stu-id="84126-335">1117 (0x45D)</span></span>
</dt> <dt>



<span data-ttu-id="84126-336">Impossibile eseguire la richiesta a causa di un errore del dispositivo di I/O.</span><span class="sxs-lookup"><span data-stu-id="84126-336">The request could not be performed because of an I/O device error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-337"><span id="ERROR_SERIAL_NO_DEVICE"></span><span id="error_serial_no_device"></span>**ERRORE \_ seriale \_ nessun \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="84126-337"><span id="ERROR_SERIAL_NO_DEVICE"></span><span id="error_serial_no_device"></span>**ERROR\_SERIAL\_NO\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-338">1118 (0x45E)</span><span class="sxs-lookup"><span data-stu-id="84126-338">1118 (0x45E)</span></span>
</dt> <dt>



<span data-ttu-id="84126-339">Nessun dispositivo seriale inizializzato correttamente.</span><span class="sxs-lookup"><span data-stu-id="84126-339">No serial device was successfully initialized.</span></span> <span data-ttu-id="84126-340">Il driver seriale viene scaricato.</span><span class="sxs-lookup"><span data-stu-id="84126-340">The serial driver will unload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-341"><span id="ERROR_IRQ_BUSY"></span><span id="error_irq_busy"></span>**ERRORE \_ IRQ \_ occupato**</span><span class="sxs-lookup"><span data-stu-id="84126-341"><span id="ERROR_IRQ_BUSY"></span><span id="error_irq_busy"></span>**ERROR\_IRQ\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-342">1119 (0x45F)</span><span class="sxs-lookup"><span data-stu-id="84126-342">1119 (0x45F)</span></span>
</dt> <dt>



<span data-ttu-id="84126-343">Non è possibile aprire un dispositivo che condivide una richiesta di interrupt (IRQ) con altri dispositivi.</span><span class="sxs-lookup"><span data-stu-id="84126-343">Unable to open a device that was sharing an interrupt request (IRQ) with other devices.</span></span> <span data-ttu-id="84126-344">Almeno un altro dispositivo che usa tale IRQ è già stato aperto.</span><span class="sxs-lookup"><span data-stu-id="84126-344">At least one other device that uses that IRQ was already opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-345"><span id="ERROR_MORE_WRITES"></span><span id="error_more_writes"></span>**\_ulteriori \_ SCRITTURe errore**</span><span class="sxs-lookup"><span data-stu-id="84126-345"><span id="ERROR_MORE_WRITES"></span><span id="error_more_writes"></span>**ERROR\_MORE\_WRITES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-346">1120 (0x460)</span><span class="sxs-lookup"><span data-stu-id="84126-346">1120 (0x460)</span></span>
</dt> <dt>



<span data-ttu-id="84126-347">Un'operazione di I/O seriale è stata completata da un'altra scrittura sulla porta seriale.</span><span class="sxs-lookup"><span data-stu-id="84126-347">A serial I/O operation was completed by another write to the serial port.</span></span> <span data-ttu-id="84126-348">Il \_ contatore XOFF seriale IOCTL ha \_ raggiunto lo \_ zero.</span><span class="sxs-lookup"><span data-stu-id="84126-348">The IOCTL\_SERIAL\_XOFF\_COUNTER reached zero.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-349"><span id="ERROR_COUNTER_TIMEOUT"></span><span id="error_counter_timeout"></span>**\_timeout contatore \_ errori**</span><span class="sxs-lookup"><span data-stu-id="84126-349"><span id="ERROR_COUNTER_TIMEOUT"></span><span id="error_counter_timeout"></span>**ERROR\_COUNTER\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-350">1121 (0x461)</span><span class="sxs-lookup"><span data-stu-id="84126-350">1121 (0x461)</span></span>
</dt> <dt>



<span data-ttu-id="84126-351">Un'operazione di I/O seriale è stata completata perché il periodo di timeout è scaduto.</span><span class="sxs-lookup"><span data-stu-id="84126-351">A serial I/O operation completed because the timeout period expired.</span></span> <span data-ttu-id="84126-352">Il \_ \_ contatore XOFF seriale IOCTL \_ non ha raggiunto lo zero.</span><span class="sxs-lookup"><span data-stu-id="84126-352">The IOCTL\_SERIAL\_XOFF\_COUNTER did not reach zero.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-353"><span id="ERROR_FLOPPY_ID_MARK_NOT_FOUND"></span><span id="error_floppy_id_mark_not_found"></span>**\_ \_ contrassegno ID floppy \_ errore \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="84126-353"><span id="ERROR_FLOPPY_ID_MARK_NOT_FOUND"></span><span id="error_floppy_id_mark_not_found"></span>**ERROR\_FLOPPY\_ID\_MARK\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-354">1122 (0x462)</span><span class="sxs-lookup"><span data-stu-id="84126-354">1122 (0x462)</span></span>
</dt> <dt>



<span data-ttu-id="84126-355">Non è stato trovato alcun contrassegno di indirizzo ID nel disco floppy.</span><span class="sxs-lookup"><span data-stu-id="84126-355">No ID address mark was found on the floppy disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-356"><span id="ERROR_FLOPPY_WRONG_CYLINDER"></span><span id="error_floppy_wrong_cylinder"></span>**ERRORE \_ del \_ cilindro floppy errato \_**</span><span class="sxs-lookup"><span data-stu-id="84126-356"><span id="ERROR_FLOPPY_WRONG_CYLINDER"></span><span id="error_floppy_wrong_cylinder"></span>**ERROR\_FLOPPY\_WRONG\_CYLINDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-357">1123 (0x463)</span><span class="sxs-lookup"><span data-stu-id="84126-357">1123 (0x463)</span></span>
</dt> <dt>



<span data-ttu-id="84126-358">Mancata corrispondenza tra il campo ID settore disco floppy e l'indirizzo di rilevamento del controller del disco floppy.</span><span class="sxs-lookup"><span data-stu-id="84126-358">Mismatch between the floppy disk sector ID field and the floppy disk controller track address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-359"><span id="ERROR_FLOPPY_UNKNOWN_ERROR"></span><span id="error_floppy_unknown_error"></span>**errore \_ sconosciuto del floppy di errore \_ \_**</span><span class="sxs-lookup"><span data-stu-id="84126-359"><span id="ERROR_FLOPPY_UNKNOWN_ERROR"></span><span id="error_floppy_unknown_error"></span>**ERROR\_FLOPPY\_UNKNOWN\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-360">1124 (0x464)</span><span class="sxs-lookup"><span data-stu-id="84126-360">1124 (0x464)</span></span>
</dt> <dt>



<span data-ttu-id="84126-361">Il controller del disco floppy ha segnalato un errore non riconosciuto dal driver del disco floppy.</span><span class="sxs-lookup"><span data-stu-id="84126-361">The floppy disk controller reported an error that is not recognized by the floppy disk driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-362"><span id="ERROR_FLOPPY_BAD_REGISTERS"></span><span id="error_floppy_bad_registers"></span>**\_registro errori floppy \_ errato \_**</span><span class="sxs-lookup"><span data-stu-id="84126-362"><span id="ERROR_FLOPPY_BAD_REGISTERS"></span><span id="error_floppy_bad_registers"></span>**ERROR\_FLOPPY\_BAD\_REGISTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-363">1125 (0x465)</span><span class="sxs-lookup"><span data-stu-id="84126-363">1125 (0x465)</span></span>
</dt> <dt>



<span data-ttu-id="84126-364">Il controller del disco floppy ha restituito risultati incoerenti nei propri registri.</span><span class="sxs-lookup"><span data-stu-id="84126-364">The floppy disk controller returned inconsistent results in its registers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-365"><span id="ERROR_DISK_RECALIBRATE_FAILED"></span><span id="error_disk_recalibrate_failed"></span>**\_RIcalibrazione disco errore \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="84126-365"><span id="ERROR_DISK_RECALIBRATE_FAILED"></span><span id="error_disk_recalibrate_failed"></span>**ERROR\_DISK\_RECALIBRATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-366">1126 (0x466)</span><span class="sxs-lookup"><span data-stu-id="84126-366">1126 (0x466)</span></span>
</dt> <dt>



<span data-ttu-id="84126-367">Durante l'accesso al disco rigido, un'operazione di ricalibrazione non è riuscita, anche dopo i tentativi.</span><span class="sxs-lookup"><span data-stu-id="84126-367">While accessing the hard disk, a recalibrate operation failed, even after retries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-368"><span id="ERROR_DISK_OPERATION_FAILED"></span><span id="error_disk_operation_failed"></span>**\_operazione disco \_ errore \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="84126-368"><span id="ERROR_DISK_OPERATION_FAILED"></span><span id="error_disk_operation_failed"></span>**ERROR\_DISK\_OPERATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-369">1127 (0x467)</span><span class="sxs-lookup"><span data-stu-id="84126-369">1127 (0x467)</span></span>
</dt> <dt>



<span data-ttu-id="84126-370">Durante l'accesso al disco rigido, un'operazione su disco non è riuscita anche dopo i tentativi.</span><span class="sxs-lookup"><span data-stu-id="84126-370">While accessing the hard disk, a disk operation failed even after retries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-371"><span id="ERROR_DISK_RESET_FAILED"></span><span id="error_disk_reset_failed"></span>**ERRORE \_ di \_ reimpostazione del disco \_**</span><span class="sxs-lookup"><span data-stu-id="84126-371"><span id="ERROR_DISK_RESET_FAILED"></span><span id="error_disk_reset_failed"></span>**ERROR\_DISK\_RESET\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-372">1128 (0x468)</span><span class="sxs-lookup"><span data-stu-id="84126-372">1128 (0x468)</span></span>
</dt> <dt>



<span data-ttu-id="84126-373">Durante l'accesso al disco rigido, era necessaria una reimpostazione del controller del disco, ma anche tale operazione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="84126-373">While accessing the hard disk, a disk controller reset was needed, but even that failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-374"><span id="ERROR_EOM_OVERFLOW"></span><span id="error_eom_overflow"></span>**ERRORE \_ di \_ overflow EOM**</span><span class="sxs-lookup"><span data-stu-id="84126-374"><span id="ERROR_EOM_OVERFLOW"></span><span id="error_eom_overflow"></span>**ERROR\_EOM\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-375">1129 (0x469)</span><span class="sxs-lookup"><span data-stu-id="84126-375">1129 (0x469)</span></span>
</dt> <dt>



<span data-ttu-id="84126-376">Fine fisica del nastro rilevata.</span><span class="sxs-lookup"><span data-stu-id="84126-376">Physical end of tape encountered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-377"><span id="ERROR_NOT_ENOUGH_SERVER_MEMORY"></span><span id="error_not_enough_server_memory"></span>**ERRORE \_ \_ memoria del \_ server insufficiente \_**</span><span class="sxs-lookup"><span data-stu-id="84126-377"><span id="ERROR_NOT_ENOUGH_SERVER_MEMORY"></span><span id="error_not_enough_server_memory"></span>**ERROR\_NOT\_ENOUGH\_SERVER\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-378">1130 (0x46A)</span><span class="sxs-lookup"><span data-stu-id="84126-378">1130 (0x46A)</span></span>
</dt> <dt>



<span data-ttu-id="84126-379">Memoria insufficiente nel server per eseguire il comando.</span><span class="sxs-lookup"><span data-stu-id="84126-379">Not enough server storage is available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-380"><span id="ERROR_POSSIBLE_DEADLOCK"></span><span id="error_possible_deadlock"></span>**ERRORE \_ possibile \_ deadlock**</span><span class="sxs-lookup"><span data-stu-id="84126-380"><span id="ERROR_POSSIBLE_DEADLOCK"></span><span id="error_possible_deadlock"></span>**ERROR\_POSSIBLE\_DEADLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-381">1131 (0x46B)</span><span class="sxs-lookup"><span data-stu-id="84126-381">1131 (0x46B)</span></span>
</dt> <dt>



<span data-ttu-id="84126-382">È stata rilevata una potenziale condizione di deadlock.</span><span class="sxs-lookup"><span data-stu-id="84126-382">A potential deadlock condition has been detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-383"><span id="ERROR_MAPPED_ALIGNMENT"></span><span id="error_mapped_alignment"></span>**\_allineamento con mapping degli errori \_**</span><span class="sxs-lookup"><span data-stu-id="84126-383"><span id="ERROR_MAPPED_ALIGNMENT"></span><span id="error_mapped_alignment"></span>**ERROR\_MAPPED\_ALIGNMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-384">1132 (0x46C)</span><span class="sxs-lookup"><span data-stu-id="84126-384">1132 (0x46C)</span></span>
</dt> <dt>



<span data-ttu-id="84126-385">L'indirizzo di base o l'offset del file specificato non dispone dell'allineamento appropriato.</span><span class="sxs-lookup"><span data-stu-id="84126-385">The base address or the file offset specified does not have the proper alignment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-386"><span id="ERROR_SET_POWER_STATE_VETOED"></span><span id="error_set_power_state_vetoed"></span>**errore durante il \_ reimpostazione \_ \_ dello stato di alimentazione \_**</span><span class="sxs-lookup"><span data-stu-id="84126-386"><span id="ERROR_SET_POWER_STATE_VETOED"></span><span id="error_set_power_state_vetoed"></span>**ERROR\_SET\_POWER\_STATE\_VETOED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-387">1140 (0x474)</span><span class="sxs-lookup"><span data-stu-id="84126-387">1140 (0x474)</span></span>
</dt> <dt>



<span data-ttu-id="84126-388">Il tentativo di modificare lo stato di alimentazione del sistema è stato bloccato da un'altra applicazione o da un altro driver.</span><span class="sxs-lookup"><span data-stu-id="84126-388">An attempt to change the system power state was vetoed by another application or driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-389"><span id="ERROR_SET_POWER_STATE_FAILED"></span><span id="error_set_power_state_failed"></span>**errore durante l' \_ impostazione \_ \_ dello stato di alimentazione \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="84126-389"><span id="ERROR_SET_POWER_STATE_FAILED"></span><span id="error_set_power_state_failed"></span>**ERROR\_SET\_POWER\_STATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-390">1141 (0x475)</span><span class="sxs-lookup"><span data-stu-id="84126-390">1141 (0x475)</span></span>
</dt> <dt>



<span data-ttu-id="84126-391">Il BIOS di sistema non è riuscito a modificare lo stato di alimentazione del sistema.</span><span class="sxs-lookup"><span data-stu-id="84126-391">The system BIOS failed an attempt to change the system power state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-392"><span id="ERROR_TOO_MANY_LINKS"></span><span id="error_too_many_links"></span>**ERRORE di un \_ numero eccessivo di \_ \_ collegamenti**</span><span class="sxs-lookup"><span data-stu-id="84126-392"><span id="ERROR_TOO_MANY_LINKS"></span><span id="error_too_many_links"></span>**ERROR\_TOO\_MANY\_LINKS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-393">1142 (0x476)</span><span class="sxs-lookup"><span data-stu-id="84126-393">1142 (0x476)</span></span>
</dt> <dt>



<span data-ttu-id="84126-394">È stato effettuato un tentativo di creare altri collegamenti in un file rispetto al file system supportato da.</span><span class="sxs-lookup"><span data-stu-id="84126-394">An attempt was made to create more links on a file than the file system supports.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-395"><span id="ERROR_OLD_WIN_VERSION"></span><span id="error_old_win_version"></span>**ERRORE \_ versione precedente di \_ Win \_**</span><span class="sxs-lookup"><span data-stu-id="84126-395"><span id="ERROR_OLD_WIN_VERSION"></span><span id="error_old_win_version"></span>**ERROR\_OLD\_WIN\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-396">1150 (0x47E)</span><span class="sxs-lookup"><span data-stu-id="84126-396">1150 (0x47E)</span></span>
</dt> <dt>



<span data-ttu-id="84126-397">Il programma specificato richiede una versione più recente di Windows.</span><span class="sxs-lookup"><span data-stu-id="84126-397">The specified program requires a newer version of Windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-398"><span id="ERROR_APP_WRONG_OS"></span><span id="error_app_wrong_os"></span>**ERRORE \_ del \_ \_ sistema operativo app errato**</span><span class="sxs-lookup"><span data-stu-id="84126-398"><span id="ERROR_APP_WRONG_OS"></span><span id="error_app_wrong_os"></span>**ERROR\_APP\_WRONG\_OS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-399">1151 (0x47F)</span><span class="sxs-lookup"><span data-stu-id="84126-399">1151 (0x47F)</span></span>
</dt> <dt>



<span data-ttu-id="84126-400">Il programma specificato non è un programma Windows o MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="84126-400">The specified program is not a Windows or MS-DOS program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-401"><span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**ERRORE \_ \_ app a istanza singola \_**</span><span class="sxs-lookup"><span data-stu-id="84126-401"><span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**ERROR\_SINGLE\_INSTANCE\_APP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-402">1152 (0x480)</span><span class="sxs-lookup"><span data-stu-id="84126-402">1152 (0x480)</span></span>
</dt> <dt>



<span data-ttu-id="84126-403">Impossibile avviare più di un'istanza del programma specificato.</span><span class="sxs-lookup"><span data-stu-id="84126-403">Cannot start more than one instance of the specified program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-404"><span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**ERRORE \_ \_ app RMODE**</span><span class="sxs-lookup"><span data-stu-id="84126-404"><span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**ERROR\_RMODE\_APP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-405">1153 (0x481)</span><span class="sxs-lookup"><span data-stu-id="84126-405">1153 (0x481)</span></span>
</dt> <dt>



<span data-ttu-id="84126-406">Il programma specificato è stato scritto per una versione precedente di Windows.</span><span class="sxs-lookup"><span data-stu-id="84126-406">The specified program was written for an earlier version of Windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-407"><span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**ERRORE \_ di \_ dll non valida**</span><span class="sxs-lookup"><span data-stu-id="84126-407"><span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**ERROR\_INVALID\_DLL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-408">1154 (0x482)</span><span class="sxs-lookup"><span data-stu-id="84126-408">1154 (0x482)</span></span>
</dt> <dt>



<span data-ttu-id="84126-409">Uno dei file di libreria necessari per eseguire l'applicazione è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="84126-409">One of the library files needed to run this application is damaged.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-410"><span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**ERRORE \_ Nessuna \_ associazione**</span><span class="sxs-lookup"><span data-stu-id="84126-410"><span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**ERROR\_NO\_ASSOCIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-411">1155 (0x483)</span><span class="sxs-lookup"><span data-stu-id="84126-411">1155 (0x483)</span></span>
</dt> <dt>



<span data-ttu-id="84126-412">Nessuna applicazione associata al file specificato per questa operazione.</span><span class="sxs-lookup"><span data-stu-id="84126-412">No application is associated with the specified file for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-413"><span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**ERRORE \_ DDE \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="84126-413"><span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**ERROR\_DDE\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-414">1156 (0x484)</span><span class="sxs-lookup"><span data-stu-id="84126-414">1156 (0x484)</span></span>
</dt> <dt>



<span data-ttu-id="84126-415">Si è verificato un errore durante l'invio del comando all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="84126-415">An error occurred in sending the command to the application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-416"><span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**DLL di errore \_ \_ non \_ trovata**</span><span class="sxs-lookup"><span data-stu-id="84126-416"><span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**ERROR\_DLL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-417">1157 (0x485)</span><span class="sxs-lookup"><span data-stu-id="84126-417">1157 (0x485)</span></span>
</dt> <dt>



<span data-ttu-id="84126-418">Impossibile trovare uno dei file di libreria necessari per eseguire l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="84126-418">One of the library files needed to run this application cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-419"><span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**ERRORE \_ di \_ altri \_ \_ handle utente**</span><span class="sxs-lookup"><span data-stu-id="84126-419"><span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**ERROR\_NO\_MORE\_USER\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-420">1158 (0x486)</span><span class="sxs-lookup"><span data-stu-id="84126-420">1158 (0x486)</span></span>
</dt> <dt>



<span data-ttu-id="84126-421">Il processo corrente ha utilizzato tutta la relativa tolleranza di sistema degli handle per gli oggetti di Window Manager.</span><span class="sxs-lookup"><span data-stu-id="84126-421">The current process has used all of its system allowance of handles for Window Manager objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-422"><span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**\_ \_ solo sincronizzazione messaggi di errore \_**</span><span class="sxs-lookup"><span data-stu-id="84126-422"><span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**ERROR\_MESSAGE\_SYNC\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-423">1159 (0x487)</span><span class="sxs-lookup"><span data-stu-id="84126-423">1159 (0x487)</span></span>
</dt> <dt>



<span data-ttu-id="84126-424">Il messaggio può essere utilizzato solo con le operazioni sincrone.</span><span class="sxs-lookup"><span data-stu-id="84126-424">The message can be used only with synchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-425"><span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**\_elemento di origine errore \_ \_ vuoto**</span><span class="sxs-lookup"><span data-stu-id="84126-425"><span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**ERROR\_SOURCE\_ELEMENT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-426">1160 (0x488)</span><span class="sxs-lookup"><span data-stu-id="84126-426">1160 (0x488)</span></span>
</dt> <dt>



<span data-ttu-id="84126-427">L'elemento di origine indicato non contiene supporti.</span><span class="sxs-lookup"><span data-stu-id="84126-427">The indicated source element has no media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-428"><span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**ERRORE \_ \_ elemento destinazione \_ completo**</span><span class="sxs-lookup"><span data-stu-id="84126-428"><span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**ERROR\_DESTINATION\_ELEMENT\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-429">1161 (0x489)</span><span class="sxs-lookup"><span data-stu-id="84126-429">1161 (0x489)</span></span>
</dt> <dt>



<span data-ttu-id="84126-430">L'elemento di destinazione indicato contiene già un supporto.</span><span class="sxs-lookup"><span data-stu-id="84126-430">The indicated destination element already contains media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-431"><span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**ERRORE \_ di \_ Indirizzo elemento non valido \_**</span><span class="sxs-lookup"><span data-stu-id="84126-431"><span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**ERROR\_ILLEGAL\_ELEMENT\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-432">1162 (0x48A)</span><span class="sxs-lookup"><span data-stu-id="84126-432">1162 (0x48A)</span></span>
</dt> <dt>



<span data-ttu-id="84126-433">L'elemento indicato non esiste.</span><span class="sxs-lookup"><span data-stu-id="84126-433">The indicated element does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-434"><span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**rivista di errore \_ \_ non \_ presente**</span><span class="sxs-lookup"><span data-stu-id="84126-434"><span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**ERROR\_MAGAZINE\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-435">1163 (0x48B)</span><span class="sxs-lookup"><span data-stu-id="84126-435">1163 (0x48B)</span></span>
</dt> <dt>



<span data-ttu-id="84126-436">L'elemento indicato fa parte di una rivista che non è presente.</span><span class="sxs-lookup"><span data-stu-id="84126-436">The indicated element is part of a magazine that is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-437"><span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**ERRORE \_ di \_ reinizializzazione del dispositivo \_ necessario**</span><span class="sxs-lookup"><span data-stu-id="84126-437"><span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**ERROR\_DEVICE\_REINITIALIZATION\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-438">1164 (0x48C)</span><span class="sxs-lookup"><span data-stu-id="84126-438">1164 (0x48C)</span></span>
</dt> <dt>



<span data-ttu-id="84126-439">Il dispositivo indicato richiede la reinizializzazione a causa di errori hardware.</span><span class="sxs-lookup"><span data-stu-id="84126-439">The indicated device requires reinitialization due to hardware errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-440"><span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**il \_ dispositivo di errore \_ richiede la \_ pulizia**</span><span class="sxs-lookup"><span data-stu-id="84126-440"><span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**ERROR\_DEVICE\_REQUIRES\_CLEANING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-441">1165 (0x48D)</span><span class="sxs-lookup"><span data-stu-id="84126-441">1165 (0x48D)</span></span>
</dt> <dt>



<span data-ttu-id="84126-442">Il dispositivo ha indicato che è necessaria la pulizia prima di eseguire altre operazioni.</span><span class="sxs-lookup"><span data-stu-id="84126-442">The device has indicated that cleaning is required before further operations are attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-443"><span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**ERRORE \_ \_ sportello dispositivo \_ aperto**</span><span class="sxs-lookup"><span data-stu-id="84126-443"><span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**ERROR\_DEVICE\_DOOR\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-444">1166 (0x48E)</span><span class="sxs-lookup"><span data-stu-id="84126-444">1166 (0x48E)</span></span>
</dt> <dt>



<span data-ttu-id="84126-445">Il dispositivo ha indicato che lo sportello è aperto.</span><span class="sxs-lookup"><span data-stu-id="84126-445">The device has indicated that its door is open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-446"><span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**ERRORE \_ dispositivo \_ non \_ connesso**</span><span class="sxs-lookup"><span data-stu-id="84126-446"><span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**ERROR\_DEVICE\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-447">1167 (0x48F)</span><span class="sxs-lookup"><span data-stu-id="84126-447">1167 (0x48F)</span></span>
</dt> <dt>



<span data-ttu-id="84126-448">Il dispositivo non è connesso.</span><span class="sxs-lookup"><span data-stu-id="84126-448">The device is not connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-449"><span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**ERRORE \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="84126-449"><span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**ERROR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-450">1168 (0x490)</span><span class="sxs-lookup"><span data-stu-id="84126-450">1168 (0x490)</span></span>
</dt> <dt>



<span data-ttu-id="84126-451">Element not found.</span><span class="sxs-lookup"><span data-stu-id="84126-451">Element not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-452"><span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**ERRORE \_ Nessuna \_ corrispondenza**</span><span class="sxs-lookup"><span data-stu-id="84126-452"><span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**ERROR\_NO\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-453">1169 (0x491)</span><span class="sxs-lookup"><span data-stu-id="84126-453">1169 (0x491)</span></span>
</dt> <dt>



<span data-ttu-id="84126-454">Non è stata trovata alcuna corrispondenza per la chiave specificata nell'indice.</span><span class="sxs-lookup"><span data-stu-id="84126-454">There was no match for the specified key in the index.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-455"><span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**\_ \_ Impossibile trovare il set di errori \_**</span><span class="sxs-lookup"><span data-stu-id="84126-455"><span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**ERROR\_SET\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-456">1170 (0x492)</span><span class="sxs-lookup"><span data-stu-id="84126-456">1170 (0x492)</span></span>
</dt> <dt>



<span data-ttu-id="84126-457">Il set di proprietà specificato non esiste nell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="84126-457">The property set specified does not exist on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-458"><span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**il punto di errore non è stato \_ \_ \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="84126-458"><span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**ERROR\_POINT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-459">1171 (0x493)</span><span class="sxs-lookup"><span data-stu-id="84126-459">1171 (0x493)</span></span>
</dt> <dt>



<span data-ttu-id="84126-460">Il punto passato a GetMouseMovePoints non è presente nel buffer.</span><span class="sxs-lookup"><span data-stu-id="84126-460">The point passed to GetMouseMovePoints is not in the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-461"><span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**ERRORE \_ nessun \_ servizio di rilevamento \_**</span><span class="sxs-lookup"><span data-stu-id="84126-461"><span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**ERROR\_NO\_TRACKING\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-462">1172 (0x494)</span><span class="sxs-lookup"><span data-stu-id="84126-462">1172 (0x494)</span></span>
</dt> <dt>



<span data-ttu-id="84126-463">Il servizio di rilevamento (workstation) non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="84126-463">The tracking (workstation) service is not running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-464"><span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**ERRORE \_ nessun \_ \_ ID volume**</span><span class="sxs-lookup"><span data-stu-id="84126-464"><span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**ERROR\_NO\_VOLUME\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-465">1173 (0x495)</span><span class="sxs-lookup"><span data-stu-id="84126-465">1173 (0x495)</span></span>
</dt> <dt>



<span data-ttu-id="84126-466">Impossibile trovare l'ID volume.</span><span class="sxs-lookup"><span data-stu-id="84126-466">The Volume ID could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-467"><span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**ERRORE \_ non è possibile \_ \_ rimuovere \_ sostituito**</span><span class="sxs-lookup"><span data-stu-id="84126-467"><span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**ERROR\_UNABLE\_TO\_REMOVE\_REPLACED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-468">1175 (0x497)</span><span class="sxs-lookup"><span data-stu-id="84126-468">1175 (0x497)</span></span>
</dt> <dt>



<span data-ttu-id="84126-469">Impossibile rimuovere il file da sostituire.</span><span class="sxs-lookup"><span data-stu-id="84126-469">Unable to remove the file to be replaced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-470"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**ERRORE \_ non è possibile \_ \_ spostare la \_ sostituzione**</span><span class="sxs-lookup"><span data-stu-id="84126-470"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**ERROR\_UNABLE\_TO\_MOVE\_REPLACEMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-471">1176 (0x498)</span><span class="sxs-lookup"><span data-stu-id="84126-471">1176 (0x498)</span></span>
</dt> <dt>



<span data-ttu-id="84126-472">Impossibile spostare il file di sostituzione nel file da sostituire.</span><span class="sxs-lookup"><span data-stu-id="84126-472">Unable to move the replacement file to the file to be replaced.</span></span> <span data-ttu-id="84126-473">Il file da sostituire ha mantenuto il nome originale.</span><span class="sxs-lookup"><span data-stu-id="84126-473">The file to be replaced has retained its original name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-474"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**ERRORE \_ non è possibile \_ \_ spostare la \_ sostituzione \_ 2**</span><span class="sxs-lookup"><span data-stu-id="84126-474"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**ERROR\_UNABLE\_TO\_MOVE\_REPLACEMENT\_2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-475">1177 (0x499)</span><span class="sxs-lookup"><span data-stu-id="84126-475">1177 (0x499)</span></span>
</dt> <dt>



<span data-ttu-id="84126-476">Impossibile spostare il file di sostituzione nel file da sostituire.</span><span class="sxs-lookup"><span data-stu-id="84126-476">Unable to move the replacement file to the file to be replaced.</span></span> <span data-ttu-id="84126-477">Il file da sostituire è stato rinominato usando il nome del backup.</span><span class="sxs-lookup"><span data-stu-id="84126-477">The file to be replaced has been renamed using the backup name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-478"><span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**\_eliminazione Journal degli errori \_ \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="84126-478"><span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**ERROR\_JOURNAL\_DELETE\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-479">1178 (0x49A)</span><span class="sxs-lookup"><span data-stu-id="84126-479">1178 (0x49A)</span></span>
</dt> <dt>



<span data-ttu-id="84126-480">È in corso l'eliminazione del journal delle modifiche del volume.</span><span class="sxs-lookup"><span data-stu-id="84126-480">The volume change journal is being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-481"><span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**Journal degli errori \_ \_ non \_ attivo**</span><span class="sxs-lookup"><span data-stu-id="84126-481"><span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**ERROR\_JOURNAL\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-482">1179 (0x49B)</span><span class="sxs-lookup"><span data-stu-id="84126-482">1179 (0x49B)</span></span>
</dt> <dt>



<span data-ttu-id="84126-483">Il Journal delle modifiche del volume non è attivo.</span><span class="sxs-lookup"><span data-stu-id="84126-483">The volume change journal is not active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-484"><span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**ERRORE \_ possibile \_ file \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="84126-484"><span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**ERROR\_POTENTIAL\_FILE\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-485">1180 (0x49C)</span><span class="sxs-lookup"><span data-stu-id="84126-485">1180 (0x49C)</span></span>
</dt> <dt>



<span data-ttu-id="84126-486">È stato trovato un file, ma potrebbe non essere il file corretto.</span><span class="sxs-lookup"><span data-stu-id="84126-486">A file was found, but it may not be the correct file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-487"><span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**\_voce journal degli errori \_ \_ eliminata**</span><span class="sxs-lookup"><span data-stu-id="84126-487"><span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**ERROR\_JOURNAL\_ENTRY\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-488">1181 (0x49D)</span><span class="sxs-lookup"><span data-stu-id="84126-488">1181 (0x49D)</span></span>
</dt> <dt>



<span data-ttu-id="84126-489">La voce del journal è stata eliminata dal Journal.</span><span class="sxs-lookup"><span data-stu-id="84126-489">The journal entry has been deleted from the journal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-490"><span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**ERRORE \_ di \_ arresto \_ pianificato**</span><span class="sxs-lookup"><span data-stu-id="84126-490"><span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**ERROR\_SHUTDOWN\_IS\_SCHEDULED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-491">1190 (0x4A6)</span><span class="sxs-lookup"><span data-stu-id="84126-491">1190 (0x4A6)</span></span>
</dt> <dt>



<span data-ttu-id="84126-492">Un arresto del sistema è già stato pianificato.</span><span class="sxs-lookup"><span data-stu-id="84126-492">A system shutdown has already been scheduled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-493"><span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**ERRORE \_ \_ di arresto degli utenti \_ connessi \_**</span><span class="sxs-lookup"><span data-stu-id="84126-493"><span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**ERROR\_SHUTDOWN\_USERS\_LOGGED\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-494">1191 (0x4A7)</span><span class="sxs-lookup"><span data-stu-id="84126-494">1191 (0x4A7)</span></span>
</dt> <dt>



<span data-ttu-id="84126-495">Impossibile avviare l'arresto del sistema perché sono presenti altri utenti connessi al computer.</span><span class="sxs-lookup"><span data-stu-id="84126-495">The system shutdown cannot be initiated because there are other users logged on to the computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-496"><span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**ERRORE \_ \_ dispositivo errato**</span><span class="sxs-lookup"><span data-stu-id="84126-496"><span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**ERROR\_BAD\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-497">1200 (0x4B0)</span><span class="sxs-lookup"><span data-stu-id="84126-497">1200 (0x4B0)</span></span>
</dt> <dt>



<span data-ttu-id="84126-498">Il nome del dispositivo specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="84126-498">The specified device name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-499"><span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**ERRORE di \_ connessione non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="84126-499"><span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**ERROR\_CONNECTION\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-500">1201 (0x4B1)</span><span class="sxs-lookup"><span data-stu-id="84126-500">1201 (0x4B1)</span></span>
</dt> <dt>



<span data-ttu-id="84126-501">Il dispositivo non è attualmente connesso, ma è una connessione memorizzata.</span><span class="sxs-lookup"><span data-stu-id="84126-501">The device is not currently connected but it is a remembered connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-502"><span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**dispositivo con errori \_ \_ già \_ memorizzato**</span><span class="sxs-lookup"><span data-stu-id="84126-502"><span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**ERROR\_DEVICE\_ALREADY\_REMEMBERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-503">1202 (0x4B2)</span><span class="sxs-lookup"><span data-stu-id="84126-503">1202 (0x4B2)</span></span>
</dt> <dt>



<span data-ttu-id="84126-504">Il nome del dispositivo locale ha una connessione memorizzata a un'altra risorsa di rete.</span><span class="sxs-lookup"><span data-stu-id="84126-504">The local device name has a remembered connection to another network resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-505"><span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**ERRORE \_ nessun \_ \_ percorso NET o \_ errato \_**</span><span class="sxs-lookup"><span data-stu-id="84126-505"><span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**ERROR\_NO\_NET\_OR\_BAD\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-506">1203 (0x4B3)</span><span class="sxs-lookup"><span data-stu-id="84126-506">1203 (0x4B3)</span></span>
</dt> <dt>



<span data-ttu-id="84126-507">Il percorso di rete non è stato tipizzato correttamente, non esiste oppure il provider di rete non è attualmente disponibile.</span><span class="sxs-lookup"><span data-stu-id="84126-507">The network path was either typed incorrectly, does not exist, or the network provider is not currently available.</span></span> <span data-ttu-id="84126-508">Provare a ridigitare il percorso o a contattare l'amministratore di rete.</span><span class="sxs-lookup"><span data-stu-id="84126-508">Please try retyping the path or contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-509"><span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**ERRORE \_ del \_ provider errato**</span><span class="sxs-lookup"><span data-stu-id="84126-509"><span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**ERROR\_BAD\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-510">1204 (0x4B4)</span><span class="sxs-lookup"><span data-stu-id="84126-510">1204 (0x4B4)</span></span>
</dt> <dt>



<span data-ttu-id="84126-511">Il nome del provider di rete specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="84126-511">The specified network provider name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-512"><span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**ERRORE \_ non è possibile \_ aprire \_ il profilo**</span><span class="sxs-lookup"><span data-stu-id="84126-512"><span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**ERROR\_CANNOT\_OPEN\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-513">1205 (0x4B5)</span><span class="sxs-lookup"><span data-stu-id="84126-513">1205 (0x4B5)</span></span>
</dt> <dt>



<span data-ttu-id="84126-514">Non è possibile aprire il profilo di connessione di rete.</span><span class="sxs-lookup"><span data-stu-id="84126-514">Unable to open the network connection profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-515"><span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**ERRORE \_ \_ profilo errato**</span><span class="sxs-lookup"><span data-stu-id="84126-515"><span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**ERROR\_BAD\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-516">1206 (0x4B6)</span><span class="sxs-lookup"><span data-stu-id="84126-516">1206 (0x4B6)</span></span>
</dt> <dt>



<span data-ttu-id="84126-517">Il profilo di connessione di rete è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="84126-517">The network connection profile is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-518"><span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**ERRORE \_ non \_ contenitore**</span><span class="sxs-lookup"><span data-stu-id="84126-518"><span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**ERROR\_NOT\_CONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-519">1207 (0x4B7)</span><span class="sxs-lookup"><span data-stu-id="84126-519">1207 (0x4B7)</span></span>
</dt> <dt>



<span data-ttu-id="84126-520">Impossibile enumerare un non contenitore.</span><span class="sxs-lookup"><span data-stu-id="84126-520">Cannot enumerate a noncontainer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-521"><span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**errore \_ esteso \_ errore**</span><span class="sxs-lookup"><span data-stu-id="84126-521"><span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**ERROR\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-522">1208 (0x4B8)</span><span class="sxs-lookup"><span data-stu-id="84126-522">1208 (0x4B8)</span></span>
</dt> <dt>



<span data-ttu-id="84126-523">Si è verificato un errore esteso.</span><span class="sxs-lookup"><span data-stu-id="84126-523">An extended error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-524"><span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**ERRORE \_ \_ GroupName non valido**</span><span class="sxs-lookup"><span data-stu-id="84126-524"><span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**ERROR\_INVALID\_GROUPNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-525">1209 (0x4B9)</span><span class="sxs-lookup"><span data-stu-id="84126-525">1209 (0x4B9)</span></span>
</dt> <dt>



<span data-ttu-id="84126-526">Il formato del nome del gruppo specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="84126-526">The format of the specified group name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-527"><span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**ERRORE \_ nomecomputer non valido \_**</span><span class="sxs-lookup"><span data-stu-id="84126-527"><span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**ERROR\_INVALID\_COMPUTERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-528">1210 (0x4BA)</span><span class="sxs-lookup"><span data-stu-id="84126-528">1210 (0x4BA)</span></span>
</dt> <dt>



<span data-ttu-id="84126-529">Il formato del nome computer specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="84126-529">The format of the specified computer name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-530"><span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**ERRORE \_ \_ EventName non valido**</span><span class="sxs-lookup"><span data-stu-id="84126-530"><span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**ERROR\_INVALID\_EVENTNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-531">1211 (0x4BB)</span><span class="sxs-lookup"><span data-stu-id="84126-531">1211 (0x4BB)</span></span>
</dt> <dt>



<span data-ttu-id="84126-532">Il formato del nome di evento specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="84126-532">The format of the specified event name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-533"><span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**ERRORE \_ \_ DomainName non valido**</span><span class="sxs-lookup"><span data-stu-id="84126-533"><span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**ERROR\_INVALID\_DOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-534">1212 (0x4BC)</span><span class="sxs-lookup"><span data-stu-id="84126-534">1212 (0x4BC)</span></span>
</dt> <dt>



<span data-ttu-id="84126-535">Il formato del nome di dominio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="84126-535">The format of the specified domain name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-536"><span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**ERRORE \_ \_ ServiceName non valido**</span><span class="sxs-lookup"><span data-stu-id="84126-536"><span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**ERROR\_INVALID\_SERVICENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-537">1213 (0x4BD)</span><span class="sxs-lookup"><span data-stu-id="84126-537">1213 (0x4BD)</span></span>
</dt> <dt>



<span data-ttu-id="84126-538">Il formato del nome del servizio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="84126-538">The format of the specified service name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-539"><span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**ERRORE \_ NETNAME non valido \_**</span><span class="sxs-lookup"><span data-stu-id="84126-539"><span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**ERROR\_INVALID\_NETNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-540">1214 (0x4BE)</span><span class="sxs-lookup"><span data-stu-id="84126-540">1214 (0x4BE)</span></span>
</dt> <dt>



<span data-ttu-id="84126-541">Il formato del nome di rete specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="84126-541">The format of the specified network name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-542"><span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**ERRORE \_ condivisione non valida \_**</span><span class="sxs-lookup"><span data-stu-id="84126-542"><span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**ERROR\_INVALID\_SHARENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-543">1215 (0x4BF)</span><span class="sxs-lookup"><span data-stu-id="84126-543">1215 (0x4BF)</span></span>
</dt> <dt>



<span data-ttu-id="84126-544">Il formato del nome di condivisione specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="84126-544">The format of the specified share name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-545"><span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**ERRORE \_ \_ passwordname non valida**</span><span class="sxs-lookup"><span data-stu-id="84126-545"><span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**ERROR\_INVALID\_PASSWORDNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-546">1216 (0x4C0)</span><span class="sxs-lookup"><span data-stu-id="84126-546">1216 (0x4C0)</span></span>
</dt> <dt>



<span data-ttu-id="84126-547">Il formato della password specificata non è valido.</span><span class="sxs-lookup"><span data-stu-id="84126-547">The format of the specified password is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-548"><span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**ERRORE \_ \_ MessageName non valido**</span><span class="sxs-lookup"><span data-stu-id="84126-548"><span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**ERROR\_INVALID\_MESSAGENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-549">1217 (0x4C1)</span><span class="sxs-lookup"><span data-stu-id="84126-549">1217 (0x4C1)</span></span>
</dt> <dt>



<span data-ttu-id="84126-550">Il formato del nome del messaggio specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="84126-550">The format of the specified message name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-551"><span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**ERRORE \_ MESSAGEDEST non valido \_**</span><span class="sxs-lookup"><span data-stu-id="84126-551"><span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**ERROR\_INVALID\_MESSAGEDEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-552">1218 (0x4C2)</span><span class="sxs-lookup"><span data-stu-id="84126-552">1218 (0x4C2)</span></span>
</dt> <dt>



<span data-ttu-id="84126-553">Il formato della destinazione del messaggio specificata non è valido.</span><span class="sxs-lookup"><span data-stu-id="84126-553">The format of the specified message destination is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-554"><span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**\_conflitto di \_ credenziali della sessione di errore \_**</span><span class="sxs-lookup"><span data-stu-id="84126-554"><span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**ERROR\_SESSION\_CREDENTIAL\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-555">1219 (0x4C3)</span><span class="sxs-lookup"><span data-stu-id="84126-555">1219 (0x4C3)</span></span>
</dt> <dt>



<span data-ttu-id="84126-556">Non sono consentite più connessioni a un server o a una risorsa condivisa dallo stesso utente, usando più di un nome utente.</span><span class="sxs-lookup"><span data-stu-id="84126-556">Multiple connections to a server or shared resource by the same user, using more than one user name, are not allowed.</span></span> <span data-ttu-id="84126-557">Disconnettere tutte le connessioni precedenti al server o alla risorsa condivisa e riprovare.</span><span class="sxs-lookup"><span data-stu-id="84126-557">Disconnect all previous connections to the server or shared resource and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-558"><span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**\_ \_ \_ superato limite sessione remota \_ errore**</span><span class="sxs-lookup"><span data-stu-id="84126-558"><span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**ERROR\_REMOTE\_SESSION\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-559">1220 (0x4C4)</span><span class="sxs-lookup"><span data-stu-id="84126-559">1220 (0x4C4)</span></span>
</dt> <dt>



<span data-ttu-id="84126-560">È stato effettuato un tentativo di stabilire una sessione in un server di rete, ma sono già state stabilite troppe sessioni per tale server.</span><span class="sxs-lookup"><span data-stu-id="84126-560">An attempt was made to establish a session to a network server, but there are already too many sessions established to that server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-561"><span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**ERRORE \_ DUP \_ NomeDominio**</span><span class="sxs-lookup"><span data-stu-id="84126-561"><span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**ERROR\_DUP\_DOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-562">1221 (0x4C5)</span><span class="sxs-lookup"><span data-stu-id="84126-562">1221 (0x4C5)</span></span>
</dt> <dt>



<span data-ttu-id="84126-563">Il gruppo di lavoro o il nome di dominio è già in uso da un altro computer della rete.</span><span class="sxs-lookup"><span data-stu-id="84126-563">The workgroup or domain name is already in use by another computer on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-564"><span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**ERRORE \_ Nessuna \_ rete**</span><span class="sxs-lookup"><span data-stu-id="84126-564"><span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**ERROR\_NO\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-565">1222 (0x4C6)</span><span class="sxs-lookup"><span data-stu-id="84126-565">1222 (0x4C6)</span></span>
</dt> <dt>



<span data-ttu-id="84126-566">La rete non è presente o non è stata avviata.</span><span class="sxs-lookup"><span data-stu-id="84126-566">The network is not present or not started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-567"><span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**ERRORE \_ annullato**</span><span class="sxs-lookup"><span data-stu-id="84126-567"><span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**ERROR\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-568">1223 (0x4C7)</span><span class="sxs-lookup"><span data-stu-id="84126-568">1223 (0x4C7)</span></span>
</dt> <dt>



<span data-ttu-id="84126-569">L'operazione è stata annullata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="84126-569">The operation was canceled by the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-570"><span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**\_file con \_ mapping \_ utente errore**</span><span class="sxs-lookup"><span data-stu-id="84126-570"><span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**ERROR\_USER\_MAPPED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-571">1224 (0x4C8)</span><span class="sxs-lookup"><span data-stu-id="84126-571">1224 (0x4C8)</span></span>
</dt> <dt>



<span data-ttu-id="84126-572">Impossibile eseguire l'operazione richiesta su un file con una sezione mappata all'utente aperta.</span><span class="sxs-lookup"><span data-stu-id="84126-572">The requested operation cannot be performed on a file with a user-mapped section open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-573"><span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**\_connessione errore \_ rifiutata**</span><span class="sxs-lookup"><span data-stu-id="84126-573"><span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**ERROR\_CONNECTION\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-574">1225 (0x4C9)</span><span class="sxs-lookup"><span data-stu-id="84126-574">1225 (0x4C9)</span></span>
</dt> <dt>



<span data-ttu-id="84126-575">Il computer remoto ha rifiutato la connessione di rete.</span><span class="sxs-lookup"><span data-stu-id="84126-575">The remote computer refused the network connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-576"><span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**ERRORE \_ di \_ disconnessione normale**</span><span class="sxs-lookup"><span data-stu-id="84126-576"><span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**ERROR\_GRACEFUL\_DISCONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-577">1226 (0x4CA)</span><span class="sxs-lookup"><span data-stu-id="84126-577">1226 (0x4CA)</span></span>
</dt> <dt>



<span data-ttu-id="84126-578">La connessione di rete è stata chiusa correttamente.</span><span class="sxs-lookup"><span data-stu-id="84126-578">The network connection was gracefully closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-579"><span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**\_indirizzo errore \_ già \_ associato**</span><span class="sxs-lookup"><span data-stu-id="84126-579"><span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**ERROR\_ADDRESS\_ALREADY\_ASSOCIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-580">1227 (0x4CB)</span><span class="sxs-lookup"><span data-stu-id="84126-580">1227 (0x4CB)</span></span>
</dt> <dt>



<span data-ttu-id="84126-581">All'endpoint di trasporto di rete è già associato un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="84126-581">The network transport endpoint already has an address associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-582"><span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**\_indirizzo errore \_ non \_ associato**</span><span class="sxs-lookup"><span data-stu-id="84126-582"><span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**ERROR\_ADDRESS\_NOT\_ASSOCIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-583">1228 (0x4CC)</span><span class="sxs-lookup"><span data-stu-id="84126-583">1228 (0x4CC)</span></span>
</dt> <dt>



<span data-ttu-id="84126-584">Un indirizzo non è ancora stato associato all'endpoint di rete.</span><span class="sxs-lookup"><span data-stu-id="84126-584">An address has not yet been associated with the network endpoint.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-585"><span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**ERRORE di \_ connessione \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="84126-585"><span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**ERROR\_CONNECTION\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-586">1229 (0x4CD)</span><span class="sxs-lookup"><span data-stu-id="84126-586">1229 (0x4CD)</span></span>
</dt> <dt>



<span data-ttu-id="84126-587">Si è tentato di eseguire un'operazione su una connessione di rete inesistente.</span><span class="sxs-lookup"><span data-stu-id="84126-587">An operation was attempted on a nonexistent network connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-588"><span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**ERRORE di \_ connessione \_ attivo**</span><span class="sxs-lookup"><span data-stu-id="84126-588"><span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**ERROR\_CONNECTION\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-589">1230 (0x4CE)</span><span class="sxs-lookup"><span data-stu-id="84126-589">1230 (0x4CE)</span></span>
</dt> <dt>



<span data-ttu-id="84126-590">Si è tentato di eseguire un'operazione non valida su una connessione di rete attiva.</span><span class="sxs-lookup"><span data-stu-id="84126-590">An invalid operation was attempted on an active network connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-591"><span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**ERRORE di \_ rete \_ irraggiungibile**</span><span class="sxs-lookup"><span data-stu-id="84126-591"><span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**ERROR\_NETWORK\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-592">1231 (0x4CF)</span><span class="sxs-lookup"><span data-stu-id="84126-592">1231 (0x4CF)</span></span>
</dt> <dt>



<span data-ttu-id="84126-593">Impossibile raggiungere il percorso di rete.</span><span class="sxs-lookup"><span data-stu-id="84126-593">The network location cannot be reached.</span></span> <span data-ttu-id="84126-594">Per informazioni sulla risoluzione dei problemi di rete, vedere la Guida di Windows.</span><span class="sxs-lookup"><span data-stu-id="84126-594">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-595"><span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**ERRORE \_ host non \_ raggiungibile**</span><span class="sxs-lookup"><span data-stu-id="84126-595"><span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**ERROR\_HOST\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-596">1232 (0x4D0)</span><span class="sxs-lookup"><span data-stu-id="84126-596">1232 (0x4D0)</span></span>
</dt> <dt>



<span data-ttu-id="84126-597">Impossibile raggiungere il percorso di rete.</span><span class="sxs-lookup"><span data-stu-id="84126-597">The network location cannot be reached.</span></span> <span data-ttu-id="84126-598">Per informazioni sulla risoluzione dei problemi di rete, vedere la Guida di Windows.</span><span class="sxs-lookup"><span data-stu-id="84126-598">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-599"><span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**protocollo di errore \_ \_ irraggiungibile**</span><span class="sxs-lookup"><span data-stu-id="84126-599"><span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**ERROR\_PROTOCOL\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-600">1233 (0x4D1)</span><span class="sxs-lookup"><span data-stu-id="84126-600">1233 (0x4D1)</span></span>
</dt> <dt>



<span data-ttu-id="84126-601">Impossibile raggiungere il percorso di rete.</span><span class="sxs-lookup"><span data-stu-id="84126-601">The network location cannot be reached.</span></span> <span data-ttu-id="84126-602">Per informazioni sulla risoluzione dei problemi di rete, vedere la Guida di Windows.</span><span class="sxs-lookup"><span data-stu-id="84126-602">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-603"><span id="ERROR_PORT_UNREACHABLE"></span><span id="error_port_unreachable"></span>**porta di errore \_ \_ irraggiungibile**</span><span class="sxs-lookup"><span data-stu-id="84126-603"><span id="ERROR_PORT_UNREACHABLE"></span><span id="error_port_unreachable"></span>**ERROR\_PORT\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-604">1234 (0x4D2)</span><span class="sxs-lookup"><span data-stu-id="84126-604">1234 (0x4D2)</span></span>
</dt> <dt>



<span data-ttu-id="84126-605">Nessun servizio sta operando sull'endpoint di rete di destinazione nel sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="84126-605">No service is operating at the destination network endpoint on the remote system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-606"><span id="ERROR_REQUEST_ABORTED"></span><span id="error_request_aborted"></span>**richiesta di errore \_ \_ interrotta**</span><span class="sxs-lookup"><span data-stu-id="84126-606"><span id="ERROR_REQUEST_ABORTED"></span><span id="error_request_aborted"></span>**ERROR\_REQUEST\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-607">1235 (0x4D3)</span><span class="sxs-lookup"><span data-stu-id="84126-607">1235 (0x4D3)</span></span>
</dt> <dt>



<span data-ttu-id="84126-608">La richiesta è stata interrotta.</span><span class="sxs-lookup"><span data-stu-id="84126-608">The request was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-609"><span id="ERROR_CONNECTION_ABORTED"></span><span id="error_connection_aborted"></span>**ERRORE di \_ connessione \_ interrotto**</span><span class="sxs-lookup"><span data-stu-id="84126-609"><span id="ERROR_CONNECTION_ABORTED"></span><span id="error_connection_aborted"></span>**ERROR\_CONNECTION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-610">1236 (0x4D4)</span><span class="sxs-lookup"><span data-stu-id="84126-610">1236 (0x4D4)</span></span>
</dt> <dt>



<span data-ttu-id="84126-611">La connessione di rete è stata interrotta dal sistema locale.</span><span class="sxs-lookup"><span data-stu-id="84126-611">The network connection was aborted by the local system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-612"><span id="ERROR_RETRY"></span><span id="error_retry"></span>**tentativo di errore \_**</span><span class="sxs-lookup"><span data-stu-id="84126-612"><span id="ERROR_RETRY"></span><span id="error_retry"></span>**ERROR\_RETRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-613">1237 (0x4D5)</span><span class="sxs-lookup"><span data-stu-id="84126-613">1237 (0x4D5)</span></span>
</dt> <dt>



<span data-ttu-id="84126-614">Impossibile completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="84126-614">The operation could not be completed.</span></span> <span data-ttu-id="84126-615">È necessario eseguire un nuovo tentativo.</span><span class="sxs-lookup"><span data-stu-id="84126-615">A retry should be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-616"><span id="ERROR_CONNECTION_COUNT_LIMIT"></span><span id="error_connection_count_limit"></span>**\_ \_ limite numero connessioni \_ errore**</span><span class="sxs-lookup"><span data-stu-id="84126-616"><span id="ERROR_CONNECTION_COUNT_LIMIT"></span><span id="error_connection_count_limit"></span>**ERROR\_CONNECTION\_COUNT\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-617">1238 (0x4D6)</span><span class="sxs-lookup"><span data-stu-id="84126-617">1238 (0x4D6)</span></span>
</dt> <dt>



<span data-ttu-id="84126-618">Non è stato possibile stabilire una connessione al server perché è stato raggiunto il limite per il numero di connessioni simultanee per l'account.</span><span class="sxs-lookup"><span data-stu-id="84126-618">A connection to the server could not be made because the limit on the number of concurrent connections for this account has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-619"><span id="ERROR_LOGIN_TIME_RESTRICTION"></span><span id="error_login_time_restriction"></span>**\_ \_ limitazione tempo di accesso errore \_**</span><span class="sxs-lookup"><span data-stu-id="84126-619"><span id="ERROR_LOGIN_TIME_RESTRICTION"></span><span id="error_login_time_restriction"></span>**ERROR\_LOGIN\_TIME\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-620">1239 (0x4D7)</span><span class="sxs-lookup"><span data-stu-id="84126-620">1239 (0x4D7)</span></span>
</dt> <dt>



<span data-ttu-id="84126-621">Tentativo di accesso durante un'ora del giorno non autorizzata per l'account.</span><span class="sxs-lookup"><span data-stu-id="84126-621">Attempting to log in during an unauthorized time of day for this account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-622"><span id="ERROR_LOGIN_WKSTA_RESTRICTION"></span><span id="error_login_wksta_restriction"></span>**\_ \_ restrizione WKSTA login errore \_**</span><span class="sxs-lookup"><span data-stu-id="84126-622"><span id="ERROR_LOGIN_WKSTA_RESTRICTION"></span><span id="error_login_wksta_restriction"></span>**ERROR\_LOGIN\_WKSTA\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-623">1240 (0x4D8)</span><span class="sxs-lookup"><span data-stu-id="84126-623">1240 (0x4D8)</span></span>
</dt> <dt>



<span data-ttu-id="84126-624">L'account non è autorizzato ad accedere da questa stazione.</span><span class="sxs-lookup"><span data-stu-id="84126-624">The account is not authorized to log in from this station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-625"><span id="ERROR_INCORRECT_ADDRESS"></span><span id="error_incorrect_address"></span>**ERRORE \_ di \_ indirizzo errato**</span><span class="sxs-lookup"><span data-stu-id="84126-625"><span id="ERROR_INCORRECT_ADDRESS"></span><span id="error_incorrect_address"></span>**ERROR\_INCORRECT\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-626">1241 (0x4D9)</span><span class="sxs-lookup"><span data-stu-id="84126-626">1241 (0x4D9)</span></span>
</dt> <dt>



<span data-ttu-id="84126-627">Impossibile utilizzare l'indirizzo di rete per l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="84126-627">The network address could not be used for the operation requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-628"><span id="ERROR_ALREADY_REGISTERED"></span><span id="error_already_registered"></span>**ERRORE \_ già \_ registrato**</span><span class="sxs-lookup"><span data-stu-id="84126-628"><span id="ERROR_ALREADY_REGISTERED"></span><span id="error_already_registered"></span>**ERROR\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-629">1242 (0x4DA)</span><span class="sxs-lookup"><span data-stu-id="84126-629">1242 (0x4DA)</span></span>
</dt> <dt>



<span data-ttu-id="84126-630">Il servizio è già registrato.</span><span class="sxs-lookup"><span data-stu-id="84126-630">The service is already registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-631"><span id="ERROR_SERVICE_NOT_FOUND"></span><span id="error_service_not_found"></span>**\_ \_ Impossibile trovare il servizio di errore \_**</span><span class="sxs-lookup"><span data-stu-id="84126-631"><span id="ERROR_SERVICE_NOT_FOUND"></span><span id="error_service_not_found"></span>**ERROR\_SERVICE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-632">1243 (0x4DB)</span><span class="sxs-lookup"><span data-stu-id="84126-632">1243 (0x4DB)</span></span>
</dt> <dt>



<span data-ttu-id="84126-633">Il servizio specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="84126-633">The specified service does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-634"><span id="ERROR_NOT_AUTHENTICATED"></span><span id="error_not_authenticated"></span>**ERRORE \_ non \_ autenticato**</span><span class="sxs-lookup"><span data-stu-id="84126-634"><span id="ERROR_NOT_AUTHENTICATED"></span><span id="error_not_authenticated"></span>**ERROR\_NOT\_AUTHENTICATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-635">1244 (0x4DC)</span><span class="sxs-lookup"><span data-stu-id="84126-635">1244 (0x4DC)</span></span>
</dt> <dt>



<span data-ttu-id="84126-636">L'operazione richiesta non è stata eseguita perché l'utente non è stato autenticato.</span><span class="sxs-lookup"><span data-stu-id="84126-636">The operation being requested was not performed because the user has not been authenticated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-637"><span id="ERROR_NOT_LOGGED_ON"></span><span id="error_not_logged_on"></span>**ERRORE \_ non \_ connesso \_**</span><span class="sxs-lookup"><span data-stu-id="84126-637"><span id="ERROR_NOT_LOGGED_ON"></span><span id="error_not_logged_on"></span>**ERROR\_NOT\_LOGGED\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-638">1245 (0x4DD)</span><span class="sxs-lookup"><span data-stu-id="84126-638">1245 (0x4DD)</span></span>
</dt> <dt>



<span data-ttu-id="84126-639">L'operazione richiesta non è stata eseguita perché l'utente non ha eseguito l'accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="84126-639">The operation being requested was not performed because the user has not logged on to the network.</span></span> <span data-ttu-id="84126-640">Il servizio specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="84126-640">The specified service does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-641"><span id="ERROR_CONTINUE"></span><span id="error_continue"></span>**ERRORE \_ continuo**</span><span class="sxs-lookup"><span data-stu-id="84126-641"><span id="ERROR_CONTINUE"></span><span id="error_continue"></span>**ERROR\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-642">1246 (0x4DE)</span><span class="sxs-lookup"><span data-stu-id="84126-642">1246 (0x4DE)</span></span>
</dt> <dt>



<span data-ttu-id="84126-643">Continuare con il lavoro in corso.</span><span class="sxs-lookup"><span data-stu-id="84126-643">Continue with work in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-644"><span id="ERROR_ALREADY_INITIALIZED"></span><span id="error_already_initialized"></span>**ERRORE \_ già \_ inizializzato**</span><span class="sxs-lookup"><span data-stu-id="84126-644"><span id="ERROR_ALREADY_INITIALIZED"></span><span id="error_already_initialized"></span>**ERROR\_ALREADY\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-645">1247 (0x4DF)</span><span class="sxs-lookup"><span data-stu-id="84126-645">1247 (0x4DF)</span></span>
</dt> <dt>



<span data-ttu-id="84126-646">È stato effettuato un tentativo di eseguire un'operazione di inizializzazione quando l'inizializzazione è già stata completata.</span><span class="sxs-lookup"><span data-stu-id="84126-646">An attempt was made to perform an initialization operation when initialization has already been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-647"><span id="ERROR_NO_MORE_DEVICES"></span><span id="error_no_more_devices"></span>**ERRORE \_ nessun \_ altro \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="84126-647"><span id="ERROR_NO_MORE_DEVICES"></span><span id="error_no_more_devices"></span>**ERROR\_NO\_MORE\_DEVICES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-648">1248 (0x4E0)</span><span class="sxs-lookup"><span data-stu-id="84126-648">1248 (0x4E0)</span></span>
</dt> <dt>



<span data-ttu-id="84126-649">Non sono più presenti dispositivi locali.</span><span class="sxs-lookup"><span data-stu-id="84126-649">No more local devices.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-650"><span id="ERROR_NO_SUCH_SITE"></span><span id="error_no_such_site"></span>**ERRORE \_ nessun \_ sito di questo tipo \_**</span><span class="sxs-lookup"><span data-stu-id="84126-650"><span id="ERROR_NO_SUCH_SITE"></span><span id="error_no_such_site"></span>**ERROR\_NO\_SUCH\_SITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-651">1249 (0x4E1)</span><span class="sxs-lookup"><span data-stu-id="84126-651">1249 (0x4E1)</span></span>
</dt> <dt>



<span data-ttu-id="84126-652">Il sito specificato non esiste.</span><span class="sxs-lookup"><span data-stu-id="84126-652">The specified site does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-653"><span id="ERROR_DOMAIN_CONTROLLER_EXISTS"></span><span id="error_domain_controller_exists"></span>**il \_ controller di dominio dell'errore \_ \_ esiste**</span><span class="sxs-lookup"><span data-stu-id="84126-653"><span id="ERROR_DOMAIN_CONTROLLER_EXISTS"></span><span id="error_domain_controller_exists"></span>**ERROR\_DOMAIN\_CONTROLLER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-654">1250 (0x4E2)</span><span class="sxs-lookup"><span data-stu-id="84126-654">1250 (0x4E2)</span></span>
</dt> <dt>



<span data-ttu-id="84126-655">Un controller di dominio con il nome specificato esiste già.</span><span class="sxs-lookup"><span data-stu-id="84126-655">A domain controller with the specified name already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-656"><span id="ERROR_ONLY_IF_CONNECTED"></span><span id="error_only_if_connected"></span>**ERRORE \_ solo \_ se \_ connesso**</span><span class="sxs-lookup"><span data-stu-id="84126-656"><span id="ERROR_ONLY_IF_CONNECTED"></span><span id="error_only_if_connected"></span>**ERROR\_ONLY\_IF\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-657">1251 (0x4E3)</span><span class="sxs-lookup"><span data-stu-id="84126-657">1251 (0x4E3)</span></span>
</dt> <dt>



<span data-ttu-id="84126-658">Questa operazione è supportata solo quando si è connessi al server.</span><span class="sxs-lookup"><span data-stu-id="84126-658">This operation is supported only when you are connected to the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-659"><span id="ERROR_OVERRIDE_NOCHANGES"></span><span id="error_override_nochanges"></span>**ERRORE \_ override \_ NoChanges**</span><span class="sxs-lookup"><span data-stu-id="84126-659"><span id="ERROR_OVERRIDE_NOCHANGES"></span><span id="error_override_nochanges"></span>**ERROR\_OVERRIDE\_NOCHANGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-660">1252 (0x4E4)</span><span class="sxs-lookup"><span data-stu-id="84126-660">1252 (0x4E4)</span></span>
</dt> <dt>



<span data-ttu-id="84126-661">Il Framework di criteri di gruppo deve chiamare l'estensione anche se non sono state apportate modifiche.</span><span class="sxs-lookup"><span data-stu-id="84126-661">The group policy framework should call the extension even if there are no changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-662"><span id="ERROR_BAD_USER_PROFILE"></span><span id="error_bad_user_profile"></span>**ERRORE \_ nel \_ profilo utente errato \_**</span><span class="sxs-lookup"><span data-stu-id="84126-662"><span id="ERROR_BAD_USER_PROFILE"></span><span id="error_bad_user_profile"></span>**ERROR\_BAD\_USER\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-663">1253 (0x4E5)</span><span class="sxs-lookup"><span data-stu-id="84126-663">1253 (0x4E5)</span></span>
</dt> <dt>



<span data-ttu-id="84126-664">Il profilo dell'utente specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="84126-664">The specified user does not have a valid profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-665"><span id="ERROR_NOT_SUPPORTED_ON_SBS"></span><span id="error_not_supported_on_sbs"></span>**ERRORE \_ non \_ supportato \_ in \_ SBS**</span><span class="sxs-lookup"><span data-stu-id="84126-665"><span id="ERROR_NOT_SUPPORTED_ON_SBS"></span><span id="error_not_supported_on_sbs"></span>**ERROR\_NOT\_SUPPORTED\_ON\_SBS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-666">1254 (0x4E6)</span><span class="sxs-lookup"><span data-stu-id="84126-666">1254 (0x4E6)</span></span>
</dt> <dt>



<span data-ttu-id="84126-667">Questa operazione non è supportata in un computer che esegue Windows Server 2003 per Small Business Server.</span><span class="sxs-lookup"><span data-stu-id="84126-667">This operation is not supported on a computer running Windows Server 2003 for Small Business Server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-668"><span id="ERROR_SERVER_SHUTDOWN_IN_PROGRESS"></span><span id="error_server_shutdown_in_progress"></span>**\_ \_ arresto del server \_ di errore in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="84126-668"><span id="ERROR_SERVER_SHUTDOWN_IN_PROGRESS"></span><span id="error_server_shutdown_in_progress"></span>**ERROR\_SERVER\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-669">1255 (0x4E7)</span><span class="sxs-lookup"><span data-stu-id="84126-669">1255 (0x4E7)</span></span>
</dt> <dt>



<span data-ttu-id="84126-670">Il computer server si sta arrestando.</span><span class="sxs-lookup"><span data-stu-id="84126-670">The server machine is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-671"><span id="ERROR_HOST_DOWN"></span><span id="error_host_down"></span>**ERRORE \_ host \_ inattivo**</span><span class="sxs-lookup"><span data-stu-id="84126-671"><span id="ERROR_HOST_DOWN"></span><span id="error_host_down"></span>**ERROR\_HOST\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-672">1256 (0x4E8)</span><span class="sxs-lookup"><span data-stu-id="84126-672">1256 (0x4E8)</span></span>
</dt> <dt>



<span data-ttu-id="84126-673">Il sistema remoto non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="84126-673">The remote system is not available.</span></span> <span data-ttu-id="84126-674">Per informazioni sulla risoluzione dei problemi di rete, vedere la Guida di Windows.</span><span class="sxs-lookup"><span data-stu-id="84126-674">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-675"><span id="ERROR_NON_ACCOUNT_SID"></span><span id="error_non_account_sid"></span>**\_SID errore non \_ account \_**</span><span class="sxs-lookup"><span data-stu-id="84126-675"><span id="ERROR_NON_ACCOUNT_SID"></span><span id="error_non_account_sid"></span>**ERROR\_NON\_ACCOUNT\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-676">1257 (0x4E9)</span><span class="sxs-lookup"><span data-stu-id="84126-676">1257 (0x4E9)</span></span>
</dt> <dt>



<span data-ttu-id="84126-677">L'identificatore di sicurezza specificato non si trova in un dominio dell'account.</span><span class="sxs-lookup"><span data-stu-id="84126-677">The security identifier provided is not from an account domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-678"><span id="ERROR_NON_DOMAIN_SID"></span><span id="error_non_domain_sid"></span>**ERRORE \_ non \_ dominio \_ SID**</span><span class="sxs-lookup"><span data-stu-id="84126-678"><span id="ERROR_NON_DOMAIN_SID"></span><span id="error_non_domain_sid"></span>**ERROR\_NON\_DOMAIN\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-679">1258 (0x4EA)</span><span class="sxs-lookup"><span data-stu-id="84126-679">1258 (0x4EA)</span></span>
</dt> <dt>



<span data-ttu-id="84126-680">L'identificatore di sicurezza fornito non dispone di un componente di dominio.</span><span class="sxs-lookup"><span data-stu-id="84126-680">The security identifier provided does not have a domain component.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-681"><span id="ERROR_APPHELP_BLOCK"></span><span id="error_apphelp_block"></span>**ERRORE \_ APPHELP \_ blocco**</span><span class="sxs-lookup"><span data-stu-id="84126-681"><span id="ERROR_APPHELP_BLOCK"></span><span id="error_apphelp_block"></span>**ERROR\_APPHELP\_BLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-682">1259 (0x4EB)</span><span class="sxs-lookup"><span data-stu-id="84126-682">1259 (0x4EB)</span></span>
</dt> <dt>



<span data-ttu-id="84126-683">La finestra di dialogo AppHelp è stata annullata impedendo l'avvio dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="84126-683">AppHelp dialog canceled thus preventing the application from starting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-684"><span id="ERROR_ACCESS_DISABLED_BY_POLICY"></span><span id="error_access_disabled_by_policy"></span>**\_accesso agli errori \_ disabilitato \_ dal \_ criterio**</span><span class="sxs-lookup"><span data-stu-id="84126-684"><span id="ERROR_ACCESS_DISABLED_BY_POLICY"></span><span id="error_access_disabled_by_policy"></span>**ERROR\_ACCESS\_DISABLED\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-685">1260 (0x4EC)</span><span class="sxs-lookup"><span data-stu-id="84126-685">1260 (0x4EC)</span></span>
</dt> <dt>



<span data-ttu-id="84126-686">Questo programma è bloccato da criteri di gruppo.</span><span class="sxs-lookup"><span data-stu-id="84126-686">This program is blocked by group policy.</span></span> <span data-ttu-id="84126-687">Per ulteriori informazioni, contattare l'amministratore di sistema.</span><span class="sxs-lookup"><span data-stu-id="84126-687">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-688"><span id="ERROR_REG_NAT_CONSUMPTION"></span><span id="error_reg_nat_consumption"></span>**ERRORE \_ reg \_ \_ consumo NAT**</span><span class="sxs-lookup"><span data-stu-id="84126-688"><span id="ERROR_REG_NAT_CONSUMPTION"></span><span id="error_reg_nat_consumption"></span>**ERROR\_REG\_NAT\_CONSUMPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-689">1261 (0x4ED)</span><span class="sxs-lookup"><span data-stu-id="84126-689">1261 (0x4ED)</span></span>
</dt> <dt>



<span data-ttu-id="84126-690">Un programma tenta di utilizzare un valore di registro non valido.</span><span class="sxs-lookup"><span data-stu-id="84126-690">A program attempt to use an invalid register value.</span></span> <span data-ttu-id="84126-691">Normalmente causato da un registro non inizializzato.</span><span class="sxs-lookup"><span data-stu-id="84126-691">Normally caused by an uninitialized register.</span></span> <span data-ttu-id="84126-692">Questo errore è specifico di Itanium.</span><span class="sxs-lookup"><span data-stu-id="84126-692">This error is Itanium specific.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-693"><span id="ERROR_CSCSHARE_OFFLINE"></span><span id="error_cscshare_offline"></span>**ERRORE \_ CSCSHARE \_ offline**</span><span class="sxs-lookup"><span data-stu-id="84126-693"><span id="ERROR_CSCSHARE_OFFLINE"></span><span id="error_cscshare_offline"></span>**ERROR\_CSCSHARE\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-694">1262 (0x4EE)</span><span class="sxs-lookup"><span data-stu-id="84126-694">1262 (0x4EE)</span></span>
</dt> <dt>



<span data-ttu-id="84126-695">La condivisione è attualmente offline o non esiste.</span><span class="sxs-lookup"><span data-stu-id="84126-695">The share is currently offline or does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-696"><span id="ERROR_PKINIT_FAILURE"></span><span id="error_pkinit_failure"></span>**ERRORE \_ PKINIT non \_ riuscito**</span><span class="sxs-lookup"><span data-stu-id="84126-696"><span id="ERROR_PKINIT_FAILURE"></span><span id="error_pkinit_failure"></span>**ERROR\_PKINIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-697">1263 (0x4EF)</span><span class="sxs-lookup"><span data-stu-id="84126-697">1263 (0x4EF)</span></span>
</dt> <dt>



<span data-ttu-id="84126-698">Il protocollo Kerberos ha rilevato un errore durante la convalida del certificato KDC durante l'accesso alla smart card.</span><span class="sxs-lookup"><span data-stu-id="84126-698">The Kerberos protocol encountered an error while validating the KDC certificate during smartcard logon.</span></span> <span data-ttu-id="84126-699">Sono disponibili ulteriori informazioni nel registro eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="84126-699">There is more information in the system event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-700"><span id="ERROR_SMARTCARD_SUBSYSTEM_FAILURE"></span><span id="error_smartcard_subsystem_failure"></span>**errore \_ del \_ sottosistema Smart Card errore \_**</span><span class="sxs-lookup"><span data-stu-id="84126-700"><span id="ERROR_SMARTCARD_SUBSYSTEM_FAILURE"></span><span id="error_smartcard_subsystem_failure"></span>**ERROR\_SMARTCARD\_SUBSYSTEM\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-701">1264 (0x4F0)</span><span class="sxs-lookup"><span data-stu-id="84126-701">1264 (0x4F0)</span></span>
</dt> <dt>



<span data-ttu-id="84126-702">Il protocollo Kerberos ha rilevato un errore durante il tentativo di utilizzare il sottosistema smart card.</span><span class="sxs-lookup"><span data-stu-id="84126-702">The Kerberos protocol encountered an error while attempting to utilize the smartcard subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-703"><span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**il downgrade dell'errore è stato \_ \_ rilevato**</span><span class="sxs-lookup"><span data-stu-id="84126-703"><span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**ERROR\_DOWNGRADE\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-704">1265 (0x4F1)</span><span class="sxs-lookup"><span data-stu-id="84126-704">1265 (0x4F1)</span></span>
</dt> <dt>



<span data-ttu-id="84126-705">Il sistema non è in grado di contattare un controller di dominio per il servizio della richiesta di autenticazione.</span><span class="sxs-lookup"><span data-stu-id="84126-705">The system cannot contact a domain controller to service the authentication request.</span></span> <span data-ttu-id="84126-706">Riprova più tardi.</span><span class="sxs-lookup"><span data-stu-id="84126-706">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-707"><span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**computer con errori \_ \_ bloccato**</span><span class="sxs-lookup"><span data-stu-id="84126-707"><span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**ERROR\_MACHINE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-708">1271 (0x4F7)</span><span class="sxs-lookup"><span data-stu-id="84126-708">1271 (0x4F7)</span></span>
</dt> <dt>



<span data-ttu-id="84126-709">Il computer è bloccato e non può essere arrestato senza l'opzione Force.</span><span class="sxs-lookup"><span data-stu-id="84126-709">The machine is locked and cannot be shut down without the force option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-710"><span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**CALLBACK di errore \_ \_ fornito \_ dati non validi \_**</span><span class="sxs-lookup"><span data-stu-id="84126-710"><span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**ERROR\_CALLBACK\_SUPPLIED\_INVALID\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-711">1273 (0x4F9)</span><span class="sxs-lookup"><span data-stu-id="84126-711">1273 (0x4F9)</span></span>
</dt> <dt>



<span data-ttu-id="84126-712">Un callback definito dall'applicazione ha dato dati non validi quando viene chiamato.</span><span class="sxs-lookup"><span data-stu-id="84126-712">An application-defined callback gave invalid data when called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-713"><span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**\_aggiornamento in \_ primo piano della sincronizzazione errori \_ \_ obbligatorio**</span><span class="sxs-lookup"><span data-stu-id="84126-713"><span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**ERROR\_SYNC\_FOREGROUND\_REFRESH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-714">1274 (0x4FA)</span><span class="sxs-lookup"><span data-stu-id="84126-714">1274 (0x4FA)</span></span>
</dt> <dt>



<span data-ttu-id="84126-715">Il Framework di criteri di gruppo deve chiamare l'estensione nell'aggiornamento dei criteri di primo piano sincrono.</span><span class="sxs-lookup"><span data-stu-id="84126-715">The group policy framework should call the extension in the synchronous foreground policy refresh.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-716"><span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**DRIVER di errore \_ \_ bloccato**</span><span class="sxs-lookup"><span data-stu-id="84126-716"><span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**ERROR\_DRIVER\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-717">1275 (0x4FB)</span><span class="sxs-lookup"><span data-stu-id="84126-717">1275 (0x4FB)</span></span>
</dt> <dt>



<span data-ttu-id="84126-718">Il caricamento del driver è stato bloccato.</span><span class="sxs-lookup"><span data-stu-id="84126-718">This driver has been blocked from loading.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-719"><span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**errore durante l' \_ \_ importazione \_ di \_ non \_ dll**</span><span class="sxs-lookup"><span data-stu-id="84126-719"><span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**ERROR\_INVALID\_IMPORT\_OF\_NON\_DLL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-720">1276 (0x4FC)</span><span class="sxs-lookup"><span data-stu-id="84126-720">1276 (0x4FC)</span></span>
</dt> <dt>



<span data-ttu-id="84126-721">Una libreria a collegamento dinamico (DLL) fa riferimento a un modulo che non è né una DLL né l'immagine eseguibile del processo.</span><span class="sxs-lookup"><span data-stu-id="84126-721">A dynamic link library (DLL) referenced a module that was neither a DLL nor the process's executable image.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-722"><span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**ERRORE di \_ accesso al pannello \_ \_ WebBlade disabilitato**</span><span class="sxs-lookup"><span data-stu-id="84126-722"><span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**ERROR\_ACCESS\_DISABLED\_WEBBLADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-723">1277 (0x4FD)</span><span class="sxs-lookup"><span data-stu-id="84126-723">1277 (0x4FD)</span></span>
</dt> <dt>



<span data-ttu-id="84126-724">Windows non è in grado di aprire il programma perché è stato disabilitato.</span><span class="sxs-lookup"><span data-stu-id="84126-724">Windows cannot open this program since it has been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-725"><span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**ERRORE di \_ accesso al \_ \_ WebBlade disabilitato per l'accesso \_**</span><span class="sxs-lookup"><span data-stu-id="84126-725"><span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**ERROR\_ACCESS\_DISABLED\_WEBBLADE\_TAMPER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-726">1278 (0x4FE)</span><span class="sxs-lookup"><span data-stu-id="84126-726">1278 (0x4FE)</span></span>
</dt> <dt>



<span data-ttu-id="84126-727">Windows non è in grado di aprire il programma perché il sistema di imposizione delle licenze è stato manomesso o danneggiato.</span><span class="sxs-lookup"><span data-stu-id="84126-727">Windows cannot open this program because the license enforcement system has been tampered with or become corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-728"><span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**ERRORE di \_ ripristino \_**</span><span class="sxs-lookup"><span data-stu-id="84126-728"><span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**ERROR\_RECOVERY\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-729">1279 (0x4FF)</span><span class="sxs-lookup"><span data-stu-id="84126-729">1279 (0x4FF)</span></span>
</dt> <dt>



<span data-ttu-id="84126-730">Ripristino transazione non riuscito.</span><span class="sxs-lookup"><span data-stu-id="84126-730">A transaction recover failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-731"><span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**ERRORE \_ già \_ Fiber**</span><span class="sxs-lookup"><span data-stu-id="84126-731"><span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**ERROR\_ALREADY\_FIBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-732">1280 (0x500)</span><span class="sxs-lookup"><span data-stu-id="84126-732">1280 (0x500)</span></span>
</dt> <dt>



<span data-ttu-id="84126-733">Il thread corrente è già stato convertito in Fiber.</span><span class="sxs-lookup"><span data-stu-id="84126-733">The current thread has already been converted to a fiber.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-734"><span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**ERRORE \_ già \_ thread**</span><span class="sxs-lookup"><span data-stu-id="84126-734"><span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**ERROR\_ALREADY\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-735">1281 (0x501)</span><span class="sxs-lookup"><span data-stu-id="84126-735">1281 (0x501)</span></span>
</dt> <dt>



<span data-ttu-id="84126-736">Il thread corrente è già stato convertito da Fiber.</span><span class="sxs-lookup"><span data-stu-id="84126-736">The current thread has already been converted from a fiber.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-737"><span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**\_sovraccarico buffer dello stack di errori \_ \_**</span><span class="sxs-lookup"><span data-stu-id="84126-737"><span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**ERROR\_STACK\_BUFFER\_OVERRUN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-738">1282 (0x502)</span><span class="sxs-lookup"><span data-stu-id="84126-738">1282 (0x502)</span></span>
</dt> <dt>



<span data-ttu-id="84126-739">Il sistema ha rilevato un sovraccarico di un buffer basato su stack in questa applicazione.</span><span class="sxs-lookup"><span data-stu-id="84126-739">The system detected an overrun of a stack-based buffer in this application.</span></span> <span data-ttu-id="84126-740">Questo sovraccarico potrebbe potenzialmente consentire a un utente malintenzionato di ottenere il controllo di questa applicazione.</span><span class="sxs-lookup"><span data-stu-id="84126-740">This overrun could potentially allow a malicious user to gain control of this application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-741"><span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**QUOTA del parametro di errore \_ \_ \_ superata**</span><span class="sxs-lookup"><span data-stu-id="84126-741"><span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**ERROR\_PARAMETER\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-742">1283 (0x503)</span><span class="sxs-lookup"><span data-stu-id="84126-742">1283 (0x503)</span></span>
</dt> <dt>



<span data-ttu-id="84126-743">I dati presenti in uno dei parametri sono maggiori di quelli che la funzione può utilizzare.</span><span class="sxs-lookup"><span data-stu-id="84126-743">Data present in one of the parameters is more than the function can operate on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-744"><span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**\_debugger errori \_ inattivo**</span><span class="sxs-lookup"><span data-stu-id="84126-744"><span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**ERROR\_DEBUGGER\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-745">1284 (0x504)</span><span class="sxs-lookup"><span data-stu-id="84126-745">1284 (0x504)</span></span>
</dt> <dt>



<span data-ttu-id="84126-746">Il tentativo di eseguire un'operazione su un oggetto di debug non è riuscito perché è in corso l'eliminazione dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="84126-746">An attempt to do an operation on a debug object failed because the object is in the process of being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-747"><span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**ERRORE \_ di \_ caricamento ritardato \_**</span><span class="sxs-lookup"><span data-stu-id="84126-747"><span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**ERROR\_DELAY\_LOAD\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-748">1285 (0x505)</span><span class="sxs-lookup"><span data-stu-id="84126-748">1285 (0x505)</span></span>
</dt> <dt>



<span data-ttu-id="84126-749">Tentativo di ritardare il caricamento di un file con estensione dll o di ottenere un indirizzo di funzione in un file con estensione dll a caricamento ritardato non riuscito.</span><span class="sxs-lookup"><span data-stu-id="84126-749">An attempt to delay-load a .dll or get a function address in a delay-loaded .dll failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-750"><span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**ERRORE \_ VDM non \_ consentito**</span><span class="sxs-lookup"><span data-stu-id="84126-750"><span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**ERROR\_VDM\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-751">1286 (0x506)</span><span class="sxs-lookup"><span data-stu-id="84126-751">1286 (0x506)</span></span>
</dt> <dt>



<span data-ttu-id="84126-752">%1 è un'applicazione a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="84126-752">%1 is a 16-bit application.</span></span> <span data-ttu-id="84126-753">Non si dispone delle autorizzazioni per l'esecuzione di applicazioni a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="84126-753">You do not have permissions to execute 16-bit applications.</span></span> <span data-ttu-id="84126-754">Verificare le autorizzazioni con l'amministratore di sistema.</span><span class="sxs-lookup"><span data-stu-id="84126-754">Check your permissions with your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-755"><span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**errore non \_ identificato \_**</span><span class="sxs-lookup"><span data-stu-id="84126-755"><span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**ERROR\_UNIDENTIFIED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-756">1287 (0x507)</span><span class="sxs-lookup"><span data-stu-id="84126-756">1287 (0x507)</span></span>
</dt> <dt>



<span data-ttu-id="84126-757">Informazioni insufficienti per identificare la cause dell'errore.</span><span class="sxs-lookup"><span data-stu-id="84126-757">Insufficient information exists to identify the cause of failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-758"><span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**ERRORE \_ \_ parametro CRUNTIME non valido \_**</span><span class="sxs-lookup"><span data-stu-id="84126-758"><span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**ERROR\_INVALID\_CRUNTIME\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-759">1288 (0x508)</span><span class="sxs-lookup"><span data-stu-id="84126-759">1288 (0x508)</span></span>
</dt> <dt>



<span data-ttu-id="84126-760">Il parametro passato a una funzione di runtime C non è corretto.</span><span class="sxs-lookup"><span data-stu-id="84126-760">The parameter passed to a C runtime function is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-761"><span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**ERRORE \_ oltre \_ VDL**</span><span class="sxs-lookup"><span data-stu-id="84126-761"><span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**ERROR\_BEYOND\_VDL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-762">1289 (0x509)</span><span class="sxs-lookup"><span data-stu-id="84126-762">1289 (0x509)</span></span>
</dt> <dt>



<span data-ttu-id="84126-763">L'operazione si è verificata oltre la lunghezza dei dati valida del file.</span><span class="sxs-lookup"><span data-stu-id="84126-763">The operation occurred beyond the valid data length of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-764"><span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**ERRORE \_ tipo di \_ SID del servizio non compatibile \_ \_**</span><span class="sxs-lookup"><span data-stu-id="84126-764"><span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**ERROR\_INCOMPATIBLE\_SERVICE\_SID\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-765">1290 (0x50A)</span><span class="sxs-lookup"><span data-stu-id="84126-765">1290 (0x50A)</span></span>
</dt> <dt>



<span data-ttu-id="84126-766">L'avvio del servizio non è riuscito perché uno o più servizi nello stesso processo hanno un'impostazione del tipo di SID del servizio incompatibile.</span><span class="sxs-lookup"><span data-stu-id="84126-766">The service start failed since one or more services in the same process have an incompatible service SID type setting.</span></span> <span data-ttu-id="84126-767">Un servizio con tipo di SID servizio con restrizioni può coesistere solo nello stesso processo con altri servizi con un tipo di SID con restrizioni.</span><span class="sxs-lookup"><span data-stu-id="84126-767">A service with restricted service SID type can only coexist in the same process with other services with a restricted SID type.</span></span> <span data-ttu-id="84126-768">Se il tipo di SID del servizio è stato appena configurato, è necessario riavviare il processo di hosting per poter avviare il servizio.</span><span class="sxs-lookup"><span data-stu-id="84126-768">If the service SID type for this service was just configured, the hosting process must be restarted in order to start this service.</span></span>

<span data-ttu-id="84126-769">In Windows Server 2003 e Windows XP un servizio senza restrizioni non può coesistere nello stesso processo con altri servizi.</span><span class="sxs-lookup"><span data-stu-id="84126-769">On Windows Server 2003 and Windows XP, an unrestricted service cannot coexist in the same process with other services.</span></span> <span data-ttu-id="84126-770">Il servizio con il tipo di SID servizio senza restrizioni deve essere spostato in un processo di proprietà per poter avviare il servizio.</span><span class="sxs-lookup"><span data-stu-id="84126-770">The service with the unrestricted service SID type must be moved to an owned process in order to start this service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-771"><span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**processo del driver di errore \_ \_ \_ terminato**</span><span class="sxs-lookup"><span data-stu-id="84126-771"><span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**ERROR\_DRIVER\_PROCESS\_TERMINATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-772">1291 (0x50B)</span><span class="sxs-lookup"><span data-stu-id="84126-772">1291 (0x50B)</span></span>
</dt> <dt>



<span data-ttu-id="84126-773">Il processo che ospita il driver per questo dispositivo è stato terminato.</span><span class="sxs-lookup"><span data-stu-id="84126-773">The process hosting the driver for this device has been terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-774"><span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**\_limite di implementazione degli errori \_**</span><span class="sxs-lookup"><span data-stu-id="84126-774"><span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**ERROR\_IMPLEMENTATION\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-775">1292 (0x50C)</span><span class="sxs-lookup"><span data-stu-id="84126-775">1292 (0x50C)</span></span>
</dt> <dt>



<span data-ttu-id="84126-776">Un'operazione ha tentato di superare un limite definito dall'implementazione.</span><span class="sxs-lookup"><span data-stu-id="84126-776">An operation attempted to exceed an implementation-defined limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-777"><span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**il \_ processo di errore \_ è \_ protetto**</span><span class="sxs-lookup"><span data-stu-id="84126-777"><span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**ERROR\_PROCESS\_IS\_PROTECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-778">1293 (0x50D)</span><span class="sxs-lookup"><span data-stu-id="84126-778">1293 (0x50D)</span></span>
</dt> <dt>



<span data-ttu-id="84126-779">Il processo di destinazione o il processo contenitore del thread di destinazione è un processo protetto.</span><span class="sxs-lookup"><span data-stu-id="84126-779">Either the target process, or the target thread's containing process, is a protected process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-780"><span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**notifica del servizio di errore \_ \_ \_ ritardo del client \_**</span><span class="sxs-lookup"><span data-stu-id="84126-780"><span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**ERROR\_SERVICE\_NOTIFY\_CLIENT\_LAGGING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-781">1294 (0x50E)</span><span class="sxs-lookup"><span data-stu-id="84126-781">1294 (0x50E)</span></span>
</dt> <dt>



<span data-ttu-id="84126-782">Il client di notifica del servizio è troppo indietro per lo stato corrente dei servizi nel computer.</span><span class="sxs-lookup"><span data-stu-id="84126-782">The service notification client is lagging too far behind the current state of services in the machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-783"><span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**\_quota disco di errore \_ \_ superata**</span><span class="sxs-lookup"><span data-stu-id="84126-783"><span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**ERROR\_DISK\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-784">1295 (0x50F)</span><span class="sxs-lookup"><span data-stu-id="84126-784">1295 (0x50F)</span></span>
</dt> <dt>



<span data-ttu-id="84126-785">L'operazione di file richiesta non è riuscita perché è stata superata la quota di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="84126-785">The requested file operation failed because the storage quota was exceeded.</span></span> <span data-ttu-id="84126-786">Per liberare spazio su disco, spostare i file in un percorso diverso o eliminare i file non necessari.</span><span class="sxs-lookup"><span data-stu-id="84126-786">To free up disk space, move files to a different location or delete unnecessary files.</span></span> <span data-ttu-id="84126-787">Per ulteriori informazioni, contattare l'amministratore di sistema.</span><span class="sxs-lookup"><span data-stu-id="84126-787">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-788"><span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**\_contenuto errore \_ bloccato**</span><span class="sxs-lookup"><span data-stu-id="84126-788"><span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**ERROR\_CONTENT\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-789">1296 (0x510)</span><span class="sxs-lookup"><span data-stu-id="84126-789">1296 (0x510)</span></span>
</dt> <dt>



<span data-ttu-id="84126-790">L'operazione di file richiesta non è riuscita perché i criteri di archiviazione bloccano il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="84126-790">The requested file operation failed because the storage policy blocks that type of file.</span></span> <span data-ttu-id="84126-791">Per ulteriori informazioni, contattare l'amministratore di sistema.</span><span class="sxs-lookup"><span data-stu-id="84126-791">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-792"><span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**ERRORE di \_ servizio INcompatibile \_ \_**</span><span class="sxs-lookup"><span data-stu-id="84126-792"><span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**ERROR\_INCOMPATIBLE\_SERVICE\_PRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-793">1297 (0x511)</span><span class="sxs-lookup"><span data-stu-id="84126-793">1297 (0x511)</span></span>
</dt> <dt>



<span data-ttu-id="84126-794">Un privilegio richiesto dal servizio per il corretto funzionamento non esiste nella configurazione dell'account del servizio.</span><span class="sxs-lookup"><span data-stu-id="84126-794">A privilege that the service requires to function properly does not exist in the service account configuration.</span></span> <span data-ttu-id="84126-795">È possibile utilizzare lo snap-in servizi di Microsoft Management Console (MMC) (Services. msc) e lo snap-in MMC Impostazioni di sicurezza locali (secpol. msc) per visualizzare la configurazione del servizio e la configurazione dell'account.</span><span class="sxs-lookup"><span data-stu-id="84126-795">You may use the Services Microsoft Management Console (MMC) snap-in (services.msc) and the Local Security Settings MMC snap-in (secpol.msc) to view the service configuration and the account configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-796"><span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**ERRORE \_ \_ blocco app**</span><span class="sxs-lookup"><span data-stu-id="84126-796"><span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**ERROR\_APP\_HANG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-797">1298 (0x512)</span><span class="sxs-lookup"><span data-stu-id="84126-797">1298 (0x512)</span></span>
</dt> <dt>



<span data-ttu-id="84126-798">Un thread incluso in questa operazione sembra non rispondere.</span><span class="sxs-lookup"><span data-stu-id="84126-798">A thread involved in this operation appears to be unresponsive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="84126-799"><span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**\_etichetta errore non valida \_**</span><span class="sxs-lookup"><span data-stu-id="84126-799"><span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**ERROR\_INVALID\_LABEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="84126-800">1299 (0x513)</span><span class="sxs-lookup"><span data-stu-id="84126-800">1299 (0x513)</span></span>
</dt> <dt>



<span data-ttu-id="84126-801">Indica che un determinato ID di sicurezza non può essere assegnato come etichetta di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="84126-801">Indicates a particular Security ID may not be assigned as the label of an object.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="84126-802">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84126-802">Requirements</span></span>



| <span data-ttu-id="84126-803">Requisito</span><span class="sxs-lookup"><span data-stu-id="84126-803">Requirement</span></span> | <span data-ttu-id="84126-804">Valore</span><span class="sxs-lookup"><span data-stu-id="84126-804">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84126-805">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84126-805">Minimum supported client</span></span><br/> | <span data-ttu-id="84126-806">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="84126-806">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="84126-807">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="84126-807">Minimum supported server</span></span><br/> | <span data-ttu-id="84126-808">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="84126-808">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="84126-809">Intestazione</span><span class="sxs-lookup"><span data-stu-id="84126-809">Header</span></span><br/>                   | <dl> <span data-ttu-id="84126-810"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="84126-810"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84126-811">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84126-811">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84126-812">Codici di errore di sistema</span><span class="sxs-lookup"><span data-stu-id="84126-812">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




