---
description: Descrive i codici di errore 0-499 definiti nel file di intestazione WinError. h ed è destinato agli sviluppatori.
ms.assetid: cacb0aec-d438-4875-a96e-4e0239fdc6ba
title: Codici di errore di sistema (0-499) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 413d9674f511bd49df12267b60d6c6c3dac366aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877849"
---
# <a name="system-error-codes-0-499"></a><span data-ttu-id="31ee0-103">Codici di errore di sistema (0-499)</span><span class="sxs-lookup"><span data-stu-id="31ee0-103">System Error Codes (0-499)</span></span>

> [!NOTE]
> <span data-ttu-id="31ee0-104">Queste informazioni sono destinate agli sviluppatori che effettuano il debug degli errori di sistema.</span><span class="sxs-lookup"><span data-stu-id="31ee0-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="31ee0-105">Per altri errori, ad esempio problemi con Windows Update, è disponibile un elenco di risorse nella pagina [codici di errore](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="31ee0-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="31ee0-106">Nell'elenco seguente vengono descritti i [codici di errore di sistema](system-error-codes.md) (errori da 0 a 499).</span><span class="sxs-lookup"><span data-stu-id="31ee0-106">The following list describes [system error codes](system-error-codes.md) (errors 0 to 499).</span></span> <span data-ttu-id="31ee0-107">Vengono restituiti dalla funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="31ee0-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="31ee0-108">Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la funzione [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il **formato \_ Message from flag \_ di \_ sistema** .</span><span class="sxs-lookup"><span data-stu-id="31ee0-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="31ee0-109"><span id="ERROR_SUCCESS"></span><span id="error_success"></span>**ERRORE \_ riuscito**</span><span class="sxs-lookup"><span data-stu-id="31ee0-109"><span id="ERROR_SUCCESS"></span><span id="error_success"></span>**ERROR\_SUCCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-110">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="31ee0-110">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-111">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="31ee0-111">The operation completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-112"><span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**ERRORE \_ funzione non valida \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-112"><span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**ERROR\_INVALID\_FUNCTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-113">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="31ee0-113">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-114">Funzione non corretta.</span><span class="sxs-lookup"><span data-stu-id="31ee0-114">Incorrect function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-115"><span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**FILE di errore \_ \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-115"><span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**ERROR\_FILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-116">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="31ee0-116">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-117">Non è possibile trovare il file specificato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-117">The system cannot find the file specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-118"><span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**il percorso dell'errore non è stato \_ \_ \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-118"><span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**ERROR\_PATH\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-119">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="31ee0-119">3 (0x3)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-120">impossibile trovare il percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-120">The system cannot find the path specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-121"><span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**ERRORE di \_ troppi \_ \_ \_ file aperti**</span><span class="sxs-lookup"><span data-stu-id="31ee0-121"><span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**ERROR\_TOO\_MANY\_OPEN\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-122">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="31ee0-122">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-123">Il sistema non è in grado di aprire il file.</span><span class="sxs-lookup"><span data-stu-id="31ee0-123">The system cannot open the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-124"><span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**ERRORE di \_ accesso \_ negato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-124"><span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-125">5 (0x5)</span><span class="sxs-lookup"><span data-stu-id="31ee0-125">5 (0x5)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-126">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-126">Access is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-127"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERRORE \_ handle non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-127"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR\_INVALID\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-128">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="31ee0-128">6 (0x6)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-129">Handle non valido.</span><span class="sxs-lookup"><span data-stu-id="31ee0-129">The handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-130"><span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**ERRORE nell' \_ Arena \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-130"><span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**ERROR\_ARENA\_TRASHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-131">7 (0x7)</span><span class="sxs-lookup"><span data-stu-id="31ee0-131">7 (0x7)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-132">I blocchi di controllo dell'archiviazione sono stati eliminati definitivamente.</span><span class="sxs-lookup"><span data-stu-id="31ee0-132">The storage control blocks were destroyed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-133"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERRORE \_ di \_ memoria insufficiente \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-133"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-134">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="31ee0-134">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-135">Risorse di memoria insufficienti per elaborare il comando.</span><span class="sxs-lookup"><span data-stu-id="31ee0-135">Not enough memory resources are available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-136"><span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**ERRORE \_ blocco non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-136"><span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**ERROR\_INVALID\_BLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-137">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="31ee0-137">9 (0x9)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-138">L'indirizzo del blocco di controllo dell'archiviazione non è valido.</span><span class="sxs-lookup"><span data-stu-id="31ee0-138">The storage control block address is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-139"><span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**ERRORE \_ ambiente non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-139"><span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**ERROR\_BAD\_ENVIRONMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-140">10 (0xA)</span><span class="sxs-lookup"><span data-stu-id="31ee0-140">10 (0xA)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-141">L'ambiente non è corretto.</span><span class="sxs-lookup"><span data-stu-id="31ee0-141">The environment is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-142"><span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**\_formato errore errato \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-142"><span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**ERROR\_BAD\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-143">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="31ee0-143">11 (0xB)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-144">Tentativo di caricare un programma con un formato non corretto.</span><span class="sxs-lookup"><span data-stu-id="31ee0-144">An attempt was made to load a program with an incorrect format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-145"><span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**ERRORE \_ di \_ accesso non valido**</span><span class="sxs-lookup"><span data-stu-id="31ee0-145"><span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**ERROR\_INVALID\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-146">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="31ee0-146">12 (0xC)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-147">Il codice di accesso non è valido.</span><span class="sxs-lookup"><span data-stu-id="31ee0-147">The access code is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-148"><span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**ERRORE \_ dati non validi \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-148"><span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**ERROR\_INVALID\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-149">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="31ee0-149">13 (0xD)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-150">I dati non sono validi.</span><span class="sxs-lookup"><span data-stu-id="31ee0-150">The data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-151"><span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**ERRORE \_ OutOfMemory**</span><span class="sxs-lookup"><span data-stu-id="31ee0-151"><span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**ERROR\_OUTOFMEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-152">14 (0xE)</span><span class="sxs-lookup"><span data-stu-id="31ee0-152">14 (0xE)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-153">Lo spazio di archiviazione disponibile non è sufficiente per completare questa operazione.</span><span class="sxs-lookup"><span data-stu-id="31ee0-153">Not enough storage is available to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-154"><span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**ERRORE \_ unità non valida \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-154"><span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**ERROR\_INVALID\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-155">15 (0xF)</span><span class="sxs-lookup"><span data-stu-id="31ee0-155">15 (0xF)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-156">Il sistema non è in grado di trovare l'unità specificata.</span><span class="sxs-lookup"><span data-stu-id="31ee0-156">The system cannot find the drive specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-157"><span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**ERRORE \_ \_ directory corrente**</span><span class="sxs-lookup"><span data-stu-id="31ee0-157"><span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**ERROR\_CURRENT\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-158">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="31ee0-158">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-159">La directory non può essere rimossa.</span><span class="sxs-lookup"><span data-stu-id="31ee0-159">The directory cannot be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-160"><span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**ERRORE \_ non \_ stesso \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="31ee0-160"><span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**ERROR\_NOT\_SAME\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-161">17 (0x11)</span><span class="sxs-lookup"><span data-stu-id="31ee0-161">17 (0x11)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-162">Il sistema non è in grado di spostare il file in un'unità disco diversa.</span><span class="sxs-lookup"><span data-stu-id="31ee0-162">The system cannot move the file to a different disk drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-163"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERRORE \_ nessun \_ altro \_ file**</span><span class="sxs-lookup"><span data-stu-id="31ee0-163"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR\_NO\_MORE\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-164">18 (0x12)</span><span class="sxs-lookup"><span data-stu-id="31ee0-164">18 (0x12)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-165">Non sono presenti altri file.</span><span class="sxs-lookup"><span data-stu-id="31ee0-165">There are no more files.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-166"><span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**\_protezione scrittura \_ errore**</span><span class="sxs-lookup"><span data-stu-id="31ee0-166"><span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**ERROR\_WRITE\_PROTECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-167">19 (0x13)</span><span class="sxs-lookup"><span data-stu-id="31ee0-167">19 (0x13)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-168">Il supporto è protetto da scrittura.</span><span class="sxs-lookup"><span data-stu-id="31ee0-168">The media is write protected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-169"><span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**ERRORE \_ unità non valida \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-169"><span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**ERROR\_BAD\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-170">20 (0x14)</span><span class="sxs-lookup"><span data-stu-id="31ee0-170">20 (0x14)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-171">Il sistema non è in grado di trovare il dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-171">The system cannot find the device specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-172"><span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**ERRORE \_ non \_ pronto**</span><span class="sxs-lookup"><span data-stu-id="31ee0-172"><span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**ERROR\_NOT\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-173">21 (0x15)</span><span class="sxs-lookup"><span data-stu-id="31ee0-173">21 (0x15)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-174">Il dispositivo non è pronto.</span><span class="sxs-lookup"><span data-stu-id="31ee0-174">The device is not ready.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-175"><span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**ERRORE \_ \_ comando errato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-175"><span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**ERROR\_BAD\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-176">22 (0x16)</span><span class="sxs-lookup"><span data-stu-id="31ee0-176">22 (0x16)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-177">Il dispositivo non riconosce il comando.</span><span class="sxs-lookup"><span data-stu-id="31ee0-177">The device does not recognize the command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-178"><span id="ERROR_CRC"></span><span id="error_crc"></span>**ERRORE \_ CRC**</span><span class="sxs-lookup"><span data-stu-id="31ee0-178"><span id="ERROR_CRC"></span><span id="error_crc"></span>**ERROR\_CRC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-179">23 (0x17)</span><span class="sxs-lookup"><span data-stu-id="31ee0-179">23 (0x17)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-180">Errore dei dati (controllo della ridondanza ciclica).</span><span class="sxs-lookup"><span data-stu-id="31ee0-180">Data error (cyclic redundancy check).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-181"><span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**ERRORE \_ di \_ lunghezza errata**</span><span class="sxs-lookup"><span data-stu-id="31ee0-181"><span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**ERROR\_BAD\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-182">24 (0x18)</span><span class="sxs-lookup"><span data-stu-id="31ee0-182">24 (0x18)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-183">Il programma ha emesso un comando ma la lunghezza del comando non è corretta.</span><span class="sxs-lookup"><span data-stu-id="31ee0-183">The program issued a command but the command length is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-184"><span id="ERROR_SEEK"></span><span id="error_seek"></span>**\_ricerca errori**</span><span class="sxs-lookup"><span data-stu-id="31ee0-184"><span id="ERROR_SEEK"></span><span id="error_seek"></span>**ERROR\_SEEK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-185">25 (0x19)</span><span class="sxs-lookup"><span data-stu-id="31ee0-185">25 (0x19)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-186">L'unità non è in grado di individuare un'area o una traccia specifica sul disco.</span><span class="sxs-lookup"><span data-stu-id="31ee0-186">The drive cannot locate a specific area or track on the disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-187"><span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**ERRORE \_ non \_ \_ disco DOS**</span><span class="sxs-lookup"><span data-stu-id="31ee0-187"><span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**ERROR\_NOT\_DOS\_DISK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-188">26 (0x1A)</span><span class="sxs-lookup"><span data-stu-id="31ee0-188">26 (0x1A)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-189">Non è possibile accedere al disco o al dischetto specificato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-189">The specified disk or diskette cannot be accessed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-190"><span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**\_ \_ Impossibile trovare il settore degli errori \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-190"><span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**ERROR\_SECTOR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-191">27 (0x1B)</span><span class="sxs-lookup"><span data-stu-id="31ee0-191">27 (0x1B)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-192">L'unità non è in grado di trovare il settore richiesto.</span><span class="sxs-lookup"><span data-stu-id="31ee0-192">The drive cannot find the sector requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-193"><span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**ERRORE \_ \_ di \_ carta esaurita**</span><span class="sxs-lookup"><span data-stu-id="31ee0-193"><span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**ERROR\_OUT\_OF\_PAPER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-194">28 (0x1C)</span><span class="sxs-lookup"><span data-stu-id="31ee0-194">28 (0x1C)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-195">La stampante ha esaurito la carta.</span><span class="sxs-lookup"><span data-stu-id="31ee0-195">The printer is out of paper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-196"><span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**errore di \_ scrittura errore \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-196"><span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**ERROR\_WRITE\_FAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-197">29 (0x1D)</span><span class="sxs-lookup"><span data-stu-id="31ee0-197">29 (0x1D)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-198">Il sistema non è in grado di scrivere sul dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-198">The system cannot write to the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-199"><span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**errore di \_ lettura errore \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-199"><span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**ERROR\_READ\_FAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-200">30 (0x1E)</span><span class="sxs-lookup"><span data-stu-id="31ee0-200">30 (0x1E)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-201">Il sistema non è in grado di leggere dal dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-201">The system cannot read from the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-202"><span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**ERRORE \_ gen \_ errore**</span><span class="sxs-lookup"><span data-stu-id="31ee0-202"><span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**ERROR\_GEN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-203">31 (0x1F)</span><span class="sxs-lookup"><span data-stu-id="31ee0-203">31 (0x1F)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-204">Un dispositivo collegato al sistema non funziona.</span><span class="sxs-lookup"><span data-stu-id="31ee0-204">A device attached to the system is not functioning.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-205"><span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**\_violazione di condivisione degli errori \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-205"><span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**ERROR\_SHARING\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-206">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="31ee0-206">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-207">Il processo non può accedere al file perché è in uso da un altro processo.</span><span class="sxs-lookup"><span data-stu-id="31ee0-207">The process cannot access the file because it is being used by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-208"><span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**\_violazione blocco \_ errori**</span><span class="sxs-lookup"><span data-stu-id="31ee0-208"><span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**ERROR\_LOCK\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-209">33 (0x21)</span><span class="sxs-lookup"><span data-stu-id="31ee0-209">33 (0x21)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-210">Il processo non può accedere al file perché un altro processo ne ha bloccato una parte.</span><span class="sxs-lookup"><span data-stu-id="31ee0-210">The process cannot access the file because another process has locked a portion of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-211"><span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**ERRORE \_ \_ disco errato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-211"><span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**ERROR\_WRONG\_DISK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-212">34 (0x22)</span><span class="sxs-lookup"><span data-stu-id="31ee0-212">34 (0x22)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-213">Il dischetto errato si trova nell'unità.</span><span class="sxs-lookup"><span data-stu-id="31ee0-213">The wrong diskette is in the drive.</span></span> <span data-ttu-id="31ee0-214">Inserisci %2 (numero di serie volume: %3) nell'unità %1.</span><span class="sxs-lookup"><span data-stu-id="31ee0-214">Insert %2 (Volume Serial Number: %3) into drive %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-215"><span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**è \_ stato \_ superato il buffer di condivisione errori \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-215"><span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**ERROR\_SHARING\_BUFFER\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-216">36 (0x24)</span><span class="sxs-lookup"><span data-stu-id="31ee0-216">36 (0x24)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-217">Troppi file aperti per la condivisione.</span><span class="sxs-lookup"><span data-stu-id="31ee0-217">Too many files opened for sharing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-218"><span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**HANDLE di errore \_ \_ EOF**</span><span class="sxs-lookup"><span data-stu-id="31ee0-218"><span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**ERROR\_HANDLE\_EOF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-219">38 (0x26)</span><span class="sxs-lookup"><span data-stu-id="31ee0-219">38 (0x26)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-220">È stata raggiunta la fine del file.</span><span class="sxs-lookup"><span data-stu-id="31ee0-220">Reached the end of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-221"><span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**ERRORE di \_ gestione del \_ disco \_ completo**</span><span class="sxs-lookup"><span data-stu-id="31ee0-221"><span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**ERROR\_HANDLE\_DISK\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-222">39 (0x27)</span><span class="sxs-lookup"><span data-stu-id="31ee0-222">39 (0x27)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-223">Disco pieno.</span><span class="sxs-lookup"><span data-stu-id="31ee0-223">The disk is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-224"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERRORE \_ non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-224"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERROR\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-225">50 (0x32)</span><span class="sxs-lookup"><span data-stu-id="31ee0-225">50 (0x32)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-226">La richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="31ee0-226">The request is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-227"><span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**ERRORE \_ REM \_ non \_ elenco**</span><span class="sxs-lookup"><span data-stu-id="31ee0-227"><span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**ERROR\_REM\_NOT\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-228">51 (0x33)</span><span class="sxs-lookup"><span data-stu-id="31ee0-228">51 (0x33)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-229">Impossibile trovare il percorso di rete.</span><span class="sxs-lookup"><span data-stu-id="31ee0-229">Windows cannot find the network path.</span></span> <span data-ttu-id="31ee0-230">Verificare che il percorso di rete sia corretto e che il computer di destinazione non sia occupato o disattivato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-230">Verify that the network path is correct and the destination computer is not busy or turned off.</span></span> <span data-ttu-id="31ee0-231">Se Windows non è ancora in grado di trovare il percorso di rete, contattare l'amministratore di rete.</span><span class="sxs-lookup"><span data-stu-id="31ee0-231">If Windows still cannot find the network path, contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-232"><span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**\_nome duplicato errore \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-232"><span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**ERROR\_DUP\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-233">52 (0x34)</span><span class="sxs-lookup"><span data-stu-id="31ee0-233">52 (0x34)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-234">La connessione non è stata stabilita perché nella rete è presente un nome duplicato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-234">You were not connected because a duplicate name exists on the network.</span></span> <span data-ttu-id="31ee0-235">Se si aggiunge un dominio, passare a sistema nel pannello di controllo per modificare il nome del computer e riprovare.</span><span class="sxs-lookup"><span data-stu-id="31ee0-235">If joining a domain, go to System in Control Panel to change the computer name and try again.</span></span> <span data-ttu-id="31ee0-236">Se si aggiunge un gruppo di lavoro, scegliere un altro nome del gruppo di lavoro.</span><span class="sxs-lookup"><span data-stu-id="31ee0-236">If joining a workgroup, choose another workgroup name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-237"><span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**ERRORE \_ \_ NETPATH errato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-237"><span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**ERROR\_BAD\_NETPATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-238">53 (0x35)</span><span class="sxs-lookup"><span data-stu-id="31ee0-238">53 (0x35)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-239">Impossibile trovare il percorso di rete.</span><span class="sxs-lookup"><span data-stu-id="31ee0-239">The network path was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-240"><span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**ERRORE \_ rete \_ occupato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-240"><span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**ERROR\_NETWORK\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-241">54 (0x36)</span><span class="sxs-lookup"><span data-stu-id="31ee0-241">54 (0x36)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-242">La rete è occupata.</span><span class="sxs-lookup"><span data-stu-id="31ee0-242">The network is busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-243"><span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**ERRORE \_ dev \_ non \_ esiste**</span><span class="sxs-lookup"><span data-stu-id="31ee0-243"><span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**ERROR\_DEV\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-244">55 (0x37)</span><span class="sxs-lookup"><span data-stu-id="31ee0-244">55 (0x37)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-245">La risorsa o il dispositivo di rete specificato non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="31ee0-245">The specified network resource or device is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-246"><span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**ERRORE di un \_ numero eccessivo di \_ \_ cmds**</span><span class="sxs-lookup"><span data-stu-id="31ee0-246"><span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**ERROR\_TOO\_MANY\_CMDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-247">56 (0x38)</span><span class="sxs-lookup"><span data-stu-id="31ee0-247">56 (0x38)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-248">È stato raggiunto il limite di comandi BIOS di rete.</span><span class="sxs-lookup"><span data-stu-id="31ee0-248">The network BIOS command limit has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-249"><span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**ERRORE di \_ adattamento \_ HDW \_ Err**</span><span class="sxs-lookup"><span data-stu-id="31ee0-249"><span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**ERROR\_ADAP\_HDW\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-250">57 (0x39)</span><span class="sxs-lookup"><span data-stu-id="31ee0-250">57 (0x39)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-251">Si è verificato un errore hardware della scheda di rete.</span><span class="sxs-lookup"><span data-stu-id="31ee0-251">A network adapter hardware error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-252"><span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**ERRORE \_ \_ net \_ resp errato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-252"><span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**ERROR\_BAD\_NET\_RESP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-253">58 (0x3A)</span><span class="sxs-lookup"><span data-stu-id="31ee0-253">58 (0x3A)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-254">Il server specificato non può effettuare l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="31ee0-254">The specified server cannot perform the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-255"><span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**ERRORE \_ UNEXP \_ net \_ Err**</span><span class="sxs-lookup"><span data-stu-id="31ee0-255"><span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**ERROR\_UNEXP\_NET\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-256">59 (0x3B)</span><span class="sxs-lookup"><span data-stu-id="31ee0-256">59 (0x3B)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-257">Si è verificato un errore di rete imprevisto.</span><span class="sxs-lookup"><span data-stu-id="31ee0-257">An unexpected network error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-258"><span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**ERRORE \_ di \_ adattamento REM errato \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-258"><span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**ERROR\_BAD\_REM\_ADAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-259">60 (0x3C)</span><span class="sxs-lookup"><span data-stu-id="31ee0-259">60 (0x3C)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-260">La scheda remota non è compatibile.</span><span class="sxs-lookup"><span data-stu-id="31ee0-260">The remote adapter is not compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-261"><span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**ERRORE \_ printq \_ completo**</span><span class="sxs-lookup"><span data-stu-id="31ee0-261"><span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**ERROR\_PRINTQ\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-262">61 (0x3D)</span><span class="sxs-lookup"><span data-stu-id="31ee0-262">61 (0x3D)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-263">Coda della stampante piena.</span><span class="sxs-lookup"><span data-stu-id="31ee0-263">The printer queue is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-264"><span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**ERRORE \_ senza \_ \_ spazio dello spooler**</span><span class="sxs-lookup"><span data-stu-id="31ee0-264"><span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**ERROR\_NO\_SPOOL\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-265">62 (0x3E)</span><span class="sxs-lookup"><span data-stu-id="31ee0-265">62 (0x3E)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-266">Lo spazio per archiviare il file in attesa di stampa non è disponibile nel server.</span><span class="sxs-lookup"><span data-stu-id="31ee0-266">Space to store the file waiting to be printed is not available on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-267"><span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**ERRORE di \_ stampa \_ annullato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-267"><span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**ERROR\_PRINT\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-268">63 (0x3F)</span><span class="sxs-lookup"><span data-stu-id="31ee0-268">63 (0x3F)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-269">Il file in attesa di stampa è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-269">Your file waiting to be printed was deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-270"><span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**ERRORE \_ NETNAME \_ eliminato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-270"><span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**ERROR\_NETNAME\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-271">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="31ee0-271">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-272">Il nome di rete specificato non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="31ee0-272">The specified network name is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-273"><span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**ERRORE \_ di \_ accesso alla rete \_ negato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-273"><span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**ERROR\_NETWORK\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-274">65 (0x41)</span><span class="sxs-lookup"><span data-stu-id="31ee0-274">65 (0x41)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-275">Accesso alla rete negato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-275">Network access is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-276"><span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**ERRORE \_ di \_ tipo dev errato \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-276"><span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**ERROR\_BAD\_DEV\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-277">66 (0x42)</span><span class="sxs-lookup"><span data-stu-id="31ee0-277">66 (0x42)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-278">Il tipo di risorsa di rete non è corretto.</span><span class="sxs-lookup"><span data-stu-id="31ee0-278">The network resource type is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-279"><span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**ERRORE \_ \_ nome rete non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-279"><span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**ERROR\_BAD\_NET\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-280">67 (0x43)</span><span class="sxs-lookup"><span data-stu-id="31ee0-280">67 (0x43)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-281">Impossibile trovare il nome della rete.</span><span class="sxs-lookup"><span data-stu-id="31ee0-281">The network name cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-282"><span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**ERRORE di un \_ numero eccessivo di \_ \_ nomi**</span><span class="sxs-lookup"><span data-stu-id="31ee0-282"><span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**ERROR\_TOO\_MANY\_NAMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-283">68 (0x44)</span><span class="sxs-lookup"><span data-stu-id="31ee0-283">68 (0x44)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-284">È stato superato il limite del nome per la scheda della scheda di rete del computer locale.</span><span class="sxs-lookup"><span data-stu-id="31ee0-284">The name limit for the local computer network adapter card was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-285"><span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**ERRORE di un \_ numero eccessivo di \_ \_ sess**</span><span class="sxs-lookup"><span data-stu-id="31ee0-285"><span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**ERROR\_TOO\_MANY\_SESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-286">69 (0x45)</span><span class="sxs-lookup"><span data-stu-id="31ee0-286">69 (0x45)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-287">È stato superato il limite della sessione BIOS di rete.</span><span class="sxs-lookup"><span data-stu-id="31ee0-287">The network BIOS session limit was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-288"><span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**condivisione degli errori \_ \_ sospesa**</span><span class="sxs-lookup"><span data-stu-id="31ee0-288"><span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**ERROR\_SHARING\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-289">70 (0x46)</span><span class="sxs-lookup"><span data-stu-id="31ee0-289">70 (0x46)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-290">Il server remoto è stato sospeso o è in fase di avvio.</span><span class="sxs-lookup"><span data-stu-id="31ee0-290">The remote server has been paused or is in the process of being started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-291"><span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**ERRORE \_ req \_ non \_ definit**</span><span class="sxs-lookup"><span data-stu-id="31ee0-291"><span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**ERROR\_REQ\_NOT\_ACCEP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-292">71 (0x47)</span><span class="sxs-lookup"><span data-stu-id="31ee0-292">71 (0x47)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-293">Al momento non è possibile eseguire altre connessioni a questo computer remoto perché sono già presenti tutte le connessioni che il computer può accettare.</span><span class="sxs-lookup"><span data-stu-id="31ee0-293">No more connections can be made to this remote computer at this time because there are already as many connections as the computer can accept.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-294"><span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**ERRORE \_ redir in \_ pausa**</span><span class="sxs-lookup"><span data-stu-id="31ee0-294"><span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**ERROR\_REDIR\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-295">72 (0x48)</span><span class="sxs-lookup"><span data-stu-id="31ee0-295">72 (0x48)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-296">La stampante o il dispositivo disco specificato è stato sospeso.</span><span class="sxs-lookup"><span data-stu-id="31ee0-296">The specified printer or disk device has been paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-297"><span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**il \_ file degli errori \_ esiste**</span><span class="sxs-lookup"><span data-stu-id="31ee0-297"><span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**ERROR\_FILE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-298">80 (0x50)</span><span class="sxs-lookup"><span data-stu-id="31ee0-298">80 (0x50)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-299">File esistente.</span><span class="sxs-lookup"><span data-stu-id="31ee0-299">The file exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-300"><span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**l'errore \_ non può \_ essere**</span><span class="sxs-lookup"><span data-stu-id="31ee0-300"><span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**ERROR\_CANNOT\_MAKE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-301">82 (0x52)</span><span class="sxs-lookup"><span data-stu-id="31ee0-301">82 (0x52)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-302">Impossibile creare la directory o il file.</span><span class="sxs-lookup"><span data-stu-id="31ee0-302">The directory or file cannot be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-303"><span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**ERRORE \_ \_ I24**</span><span class="sxs-lookup"><span data-stu-id="31ee0-303"><span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**ERROR\_FAIL\_I24**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-304">83 (0x53)</span><span class="sxs-lookup"><span data-stu-id="31ee0-304">83 (0x53)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-305">Errore in INT 24.</span><span class="sxs-lookup"><span data-stu-id="31ee0-305">Fail on INT 24.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-306"><span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**ERRORE \_ \_ di \_ strutture**</span><span class="sxs-lookup"><span data-stu-id="31ee0-306"><span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**ERROR\_OUT\_OF\_STRUCTURES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-307">84 (0x54)</span><span class="sxs-lookup"><span data-stu-id="31ee0-307">84 (0x54)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-308">Lo spazio di archiviazione per elaborare la richiesta non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="31ee0-308">Storage to process this request is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-309"><span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**ERRORE \_ già \_ assegnato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-309"><span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**ERROR\_ALREADY\_ASSIGNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-310">85 (0x55)</span><span class="sxs-lookup"><span data-stu-id="31ee0-310">85 (0x55)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-311">Il nome del dispositivo locale è già in uso.</span><span class="sxs-lookup"><span data-stu-id="31ee0-311">The local device name is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-312"><span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**ERRORE \_ di \_ password non valida**</span><span class="sxs-lookup"><span data-stu-id="31ee0-312"><span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**ERROR\_INVALID\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-313">86 (0x56)</span><span class="sxs-lookup"><span data-stu-id="31ee0-313">86 (0x56)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-314">La password di rete specificata non è corretta.</span><span class="sxs-lookup"><span data-stu-id="31ee0-314">The specified network password is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-315"><span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**ERRORE \_ parametro non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-315"><span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-316">87 (0x57)</span><span class="sxs-lookup"><span data-stu-id="31ee0-316">87 (0x57)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-317">Parametro non corretto.</span><span class="sxs-lookup"><span data-stu-id="31ee0-317">The parameter is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-318"><span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**errore errore di \_ scrittura in rete \_ \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-318"><span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**ERROR\_NET\_WRITE\_FAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-319">88 (0x58)</span><span class="sxs-lookup"><span data-stu-id="31ee0-319">88 (0x58)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-320">Si è verificato un errore di scrittura sulla rete.</span><span class="sxs-lookup"><span data-stu-id="31ee0-320">A write fault occurred on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-321"><span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**ERRORE \_ nessun \_ \_ slot proc**</span><span class="sxs-lookup"><span data-stu-id="31ee0-321"><span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**ERROR\_NO\_PROC\_SLOTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-322">89 (0x59)</span><span class="sxs-lookup"><span data-stu-id="31ee0-322">89 (0x59)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-323">Il sistema non può avviare un altro processo in questo momento.</span><span class="sxs-lookup"><span data-stu-id="31ee0-323">The system cannot start another process at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-324"><span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**ERRORE di un \_ numero eccessivo di \_ \_ semafori**</span><span class="sxs-lookup"><span data-stu-id="31ee0-324"><span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**ERROR\_TOO\_MANY\_SEMAPHORES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-325">100 (0x64)</span><span class="sxs-lookup"><span data-stu-id="31ee0-325">100 (0x64)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-326">Non è possibile creare un altro semaforo di sistema.</span><span class="sxs-lookup"><span data-stu-id="31ee0-326">Cannot create another system semaphore.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-327"><span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**ERRORE \_ escl. \_ SEM è \_ già \_ proprietario**</span><span class="sxs-lookup"><span data-stu-id="31ee0-327"><span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**ERROR\_EXCL\_SEM\_ALREADY\_OWNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-328">101 (0x65)</span><span class="sxs-lookup"><span data-stu-id="31ee0-328">101 (0x65)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-329">Il semaforo esclusivo è di proprietà di un altro processo.</span><span class="sxs-lookup"><span data-stu-id="31ee0-329">The exclusive semaphore is owned by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-330"><span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**ERRORE \_ sem \_ \_ impostato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-330"><span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**ERROR\_SEM\_IS\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-331">102 (0x66)</span><span class="sxs-lookup"><span data-stu-id="31ee0-331">102 (0x66)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-332">Il semaforo è impostato e non può essere chiuso.</span><span class="sxs-lookup"><span data-stu-id="31ee0-332">The semaphore is set and cannot be closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-333"><span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**ERRORE di un \_ numero eccessivo di \_ \_ \_ richieste SEM**</span><span class="sxs-lookup"><span data-stu-id="31ee0-333"><span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**ERROR\_TOO\_MANY\_SEM\_REQUESTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-334">103 (0x67)</span><span class="sxs-lookup"><span data-stu-id="31ee0-334">103 (0x67)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-335">Non è possibile impostare di nuovo il semaforo.</span><span class="sxs-lookup"><span data-stu-id="31ee0-335">The semaphore cannot be set again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-336"><span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**ERRORE \_ non valido \_ in fase di \_ interrupt \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-336"><span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**ERROR\_INVALID\_AT\_INTERRUPT\_TIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-337">104 (0x68)</span><span class="sxs-lookup"><span data-stu-id="31ee0-337">104 (0x68)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-338">Non è possibile richiedere semafori esclusivi in fase di interrupt.</span><span class="sxs-lookup"><span data-stu-id="31ee0-338">Cannot request exclusive semaphores at interrupt time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-339"><span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**ERRORE \_ \_ proprietario sem \_ morto**</span><span class="sxs-lookup"><span data-stu-id="31ee0-339"><span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**ERROR\_SEM\_OWNER\_DIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-340">105 (0x69)</span><span class="sxs-lookup"><span data-stu-id="31ee0-340">105 (0x69)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-341">La proprietà precedente di questo semaforo è terminata.</span><span class="sxs-lookup"><span data-stu-id="31ee0-341">The previous ownership of this semaphore has ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-342"><span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**\_ \_ limite utente sem \_ errore**</span><span class="sxs-lookup"><span data-stu-id="31ee0-342"><span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**ERROR\_SEM\_USER\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-343">106 (0x6A)</span><span class="sxs-lookup"><span data-stu-id="31ee0-343">106 (0x6A)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-344">Inserire il dischetto per l'unità %1.</span><span class="sxs-lookup"><span data-stu-id="31ee0-344">Insert the diskette for drive %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-345"><span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**\_modifica disco \_ errore**</span><span class="sxs-lookup"><span data-stu-id="31ee0-345"><span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**ERROR\_DISK\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-346">107 (0x6B)</span><span class="sxs-lookup"><span data-stu-id="31ee0-346">107 (0x6B)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-347">Il programma è stato interrotto perché non è stato inserito un dischetto alternativo.</span><span class="sxs-lookup"><span data-stu-id="31ee0-347">The program stopped because an alternate diskette was not inserted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-348"><span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**unità di errore \_ \_ bloccata**</span><span class="sxs-lookup"><span data-stu-id="31ee0-348"><span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**ERROR\_DRIVE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-349">108 (0x6C)</span><span class="sxs-lookup"><span data-stu-id="31ee0-349">108 (0x6C)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-350">Il disco è in uso o è bloccato da un altro processo.</span><span class="sxs-lookup"><span data-stu-id="31ee0-350">The disk is in use or locked by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-351"><span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**ERRORE \_ con \_ pipe interrotta**</span><span class="sxs-lookup"><span data-stu-id="31ee0-351"><span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**ERROR\_BROKEN\_PIPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-352">109 (0x6D)</span><span class="sxs-lookup"><span data-stu-id="31ee0-352">109 (0x6D)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-353">Pipe terminata.</span><span class="sxs-lookup"><span data-stu-id="31ee0-353">The pipe has been ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-354"><span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**ERRORE di \_ apertura \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="31ee0-354"><span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**ERROR\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-355">110 (0x6E)</span><span class="sxs-lookup"><span data-stu-id="31ee0-355">110 (0x6E)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-356">Il sistema non è in grado di aprire il dispositivo o il file specificato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-356">The system cannot open the device or file specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-357"><span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**\_overflow del buffer di errore \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-357"><span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**ERROR\_BUFFER\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-358">111 (0x6F)</span><span class="sxs-lookup"><span data-stu-id="31ee0-358">111 (0x6F)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-359">Il nome del file è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="31ee0-359">The file name is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-360"><span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**\_disco errore \_ pieno**</span><span class="sxs-lookup"><span data-stu-id="31ee0-360"><span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**ERROR\_DISK\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-361">112 (0x70)</span><span class="sxs-lookup"><span data-stu-id="31ee0-361">112 (0x70)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-362">Lo spazio su disco è insufficiente.</span><span class="sxs-lookup"><span data-stu-id="31ee0-362">There is not enough space on the disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-363"><span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**ERRORE \_ nessun \_ altro \_ handle di ricerca \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-363"><span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**ERROR\_NO\_MORE\_SEARCH\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-364">113 (0x71)</span><span class="sxs-lookup"><span data-stu-id="31ee0-364">113 (0x71)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-365">Non sono disponibili altri identificatori di file interni.</span><span class="sxs-lookup"><span data-stu-id="31ee0-365">No more internal file identifiers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-366"><span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**ERRORE \_ dell' \_ handle di destinazione non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-366"><span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**ERROR\_INVALID\_TARGET\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-367">114 (0x72)</span><span class="sxs-lookup"><span data-stu-id="31ee0-367">114 (0x72)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-368">L'identificatore del file interno di destinazione non è corretto.</span><span class="sxs-lookup"><span data-stu-id="31ee0-368">The target internal file identifier is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-369"><span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**ERRORE \_ categoria non valida \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-369"><span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**ERROR\_INVALID\_CATEGORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-370">117 (0x75)</span><span class="sxs-lookup"><span data-stu-id="31ee0-370">117 (0x75)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-371">La chiamata IOCTL eseguita dal programma dell'applicazione non è corretta.</span><span class="sxs-lookup"><span data-stu-id="31ee0-371">The IOCTL call made by the application program is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-372"><span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**ERRORE \_ di \_ verifica \_ opzione non valida**</span><span class="sxs-lookup"><span data-stu-id="31ee0-372"><span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**ERROR\_INVALID\_VERIFY\_SWITCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-373">118 (0x76)</span><span class="sxs-lookup"><span data-stu-id="31ee0-373">118 (0x76)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-374">Il valore del parametro dell'opzione verify-on-Write non è corretto.</span><span class="sxs-lookup"><span data-stu-id="31ee0-374">The verify-on-write switch parameter value is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-375"><span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**ERRORE \_ \_ livello driver non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-375"><span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**ERROR\_BAD\_DRIVER\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-376">119 (0x77)</span><span class="sxs-lookup"><span data-stu-id="31ee0-376">119 (0x77)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-377">Il sistema non supporta il comando richiesto.</span><span class="sxs-lookup"><span data-stu-id="31ee0-377">The system does not support the command requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-378"><span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**chiamata di errore \_ \_ non \_ implementata**</span><span class="sxs-lookup"><span data-stu-id="31ee0-378"><span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**ERROR\_CALL\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-379">120 (0x78)</span><span class="sxs-lookup"><span data-stu-id="31ee0-379">120 (0x78)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-380">Questa funzione non è supportata in questo sistema.</span><span class="sxs-lookup"><span data-stu-id="31ee0-380">This function is not supported on this system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-381"><span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**\_timeout sem \_ errore**</span><span class="sxs-lookup"><span data-stu-id="31ee0-381"><span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**ERROR\_SEM\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-382">121 (0x79)</span><span class="sxs-lookup"><span data-stu-id="31ee0-382">121 (0x79)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-383">Il periodo di timeout del semaforo è scaduto.</span><span class="sxs-lookup"><span data-stu-id="31ee0-383">The semaphore timeout period has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-384"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERRORE \_ buffer insufficiente \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-384"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-385">122 (0x7A)</span><span class="sxs-lookup"><span data-stu-id="31ee0-385">122 (0x7A)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-386">L'area dati passata a una chiamata di sistema è troppo piccola.</span><span class="sxs-lookup"><span data-stu-id="31ee0-386">The data area passed to a system call is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-387"><span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**ERRORE \_ nome non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-387"><span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**ERROR\_INVALID\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-388">123 (0x7B)</span><span class="sxs-lookup"><span data-stu-id="31ee0-388">123 (0x7B)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-389">La sintassi del nome file, della directory o dell'etichetta di volume non è corretta.</span><span class="sxs-lookup"><span data-stu-id="31ee0-389">The filename, directory name, or volume label syntax is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-390"><span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**ERRORE \_ livello non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-390"><span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**ERROR\_INVALID\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-391">124 (0x7C)</span><span class="sxs-lookup"><span data-stu-id="31ee0-391">124 (0x7C)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-392">Il livello della chiamata di sistema non è corretto.</span><span class="sxs-lookup"><span data-stu-id="31ee0-392">The system call level is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-393"><span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**ERRORE \_ senza \_ \_ etichetta volume**</span><span class="sxs-lookup"><span data-stu-id="31ee0-393"><span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**ERROR\_NO\_VOLUME\_LABEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-394">125 (0x7D)</span><span class="sxs-lookup"><span data-stu-id="31ee0-394">125 (0x7D)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-395">Il disco non ha un'etichetta di volume.</span><span class="sxs-lookup"><span data-stu-id="31ee0-395">The disk has no volume label.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-396"><span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**ERRORE \_ mod \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-396"><span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**ERROR\_MOD\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-397">126 (0x7E)</span><span class="sxs-lookup"><span data-stu-id="31ee0-397">126 (0x7E)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-398">The specified module could not be found. (E_CSC_SYSTEM_INTERNAL: errore interno. Impossibile caricare il file o l'assembly 'ScopeEngineManaged.dll' o una delle sue dipendenze. Impossibile trovare il modulo specificato.)</span><span class="sxs-lookup"><span data-stu-id="31ee0-398">The specified module could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-399"><span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**ERRORE di \_ proc \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-399"><span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**ERROR\_PROC\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-400">127 (0x7F)</span><span class="sxs-lookup"><span data-stu-id="31ee0-400">127 (0x7F)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-401">Impossibile trovare la procedura specificata.</span><span class="sxs-lookup"><span data-stu-id="31ee0-401">The specified procedure could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-402"><span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**ERRORE di \_ attesa \_ senza \_ figli**</span><span class="sxs-lookup"><span data-stu-id="31ee0-402"><span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**ERROR\_WAIT\_NO\_CHILDREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-403">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="31ee0-403">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-404">Nessun processo figlio da attendere.</span><span class="sxs-lookup"><span data-stu-id="31ee0-404">There are no child processes to wait for.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-405"><span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**ERRORE \_ figlio \_ non \_ completato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-405"><span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**ERROR\_CHILD\_NOT\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-406">129 (0x81)</span><span class="sxs-lookup"><span data-stu-id="31ee0-406">129 (0x81)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-407">Impossibile eseguire l'applicazione %1 in modalità Win32.</span><span class="sxs-lookup"><span data-stu-id="31ee0-407">The %1 application cannot be run in Win32 mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-408"><span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**\_handle di \_ accesso \_ diretto errore**</span><span class="sxs-lookup"><span data-stu-id="31ee0-408"><span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**ERROR\_DIRECT\_ACCESS\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-409">130 (0x82)</span><span class="sxs-lookup"><span data-stu-id="31ee0-409">130 (0x82)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-410">Tentativo di utilizzare un handle di file per una partizione del disco aperta per un'operazione diversa dall'I/O del disco non elaborato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-410">Attempt to use a file handle to an open disk partition for an operation other than raw disk I/O.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-411"><span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**\_ricerca negativa \_ errore**</span><span class="sxs-lookup"><span data-stu-id="31ee0-411"><span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**ERROR\_NEGATIVE\_SEEK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-412">131 (0x83)</span><span class="sxs-lookup"><span data-stu-id="31ee0-412">131 (0x83)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-413">È stato effettuato un tentativo di spostare il puntatore del file prima dell'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="31ee0-413">An attempt was made to move the file pointer before the beginning of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-414"><span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**ERRORE \_ durante la ricerca \_ nel \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="31ee0-414"><span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**ERROR\_SEEK\_ON\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-415">132 (0x84)</span><span class="sxs-lookup"><span data-stu-id="31ee0-415">132 (0x84)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-416">Il puntatore del file non può essere impostato sul dispositivo o sul file specificato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-416">The file pointer cannot be set on the specified device or file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-417"><span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**ERRORE \_ di \_ \_ destinazione join**</span><span class="sxs-lookup"><span data-stu-id="31ee0-417"><span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**ERROR\_IS\_JOIN\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-418">133 (0x85)</span><span class="sxs-lookup"><span data-stu-id="31ee0-418">133 (0x85)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-419">Non è possibile usare un comando JOIN o SUBSt per un'unità che contiene unità precedentemente unite in join.</span><span class="sxs-lookup"><span data-stu-id="31ee0-419">A JOIN or SUBST command cannot be used for a drive that contains previously joined drives.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-420"><span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**ERRORE \_ \_ aggiunto**</span><span class="sxs-lookup"><span data-stu-id="31ee0-420"><span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**ERROR\_IS\_JOINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-421">134 (0x86)</span><span class="sxs-lookup"><span data-stu-id="31ee0-421">134 (0x86)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-422">È stato effettuato un tentativo di usare un comando JOIN o SUBSt in un'unità che è già stata unita in join.</span><span class="sxs-lookup"><span data-stu-id="31ee0-422">An attempt was made to use a JOIN or SUBST command on a drive that has already been joined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-423"><span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**l'errore \_ è \_ SUBST**</span><span class="sxs-lookup"><span data-stu-id="31ee0-423"><span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**ERROR\_IS\_SUBSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-424">135 (0x87)</span><span class="sxs-lookup"><span data-stu-id="31ee0-424">135 (0x87)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-425">È stato effettuato un tentativo di usare un comando JOIN o SUBSt in un'unità che è già stata sostituita.</span><span class="sxs-lookup"><span data-stu-id="31ee0-425">An attempt was made to use a JOIN or SUBST command on a drive that has already been substituted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-426"><span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**ERRORE \_ non \_ Unito in join**</span><span class="sxs-lookup"><span data-stu-id="31ee0-426"><span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**ERROR\_NOT\_JOINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-427">136 (0x88)</span><span class="sxs-lookup"><span data-stu-id="31ee0-427">136 (0x88)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-428">Il sistema ha tentato di eliminare il JOIN di un'unità non unita in JOIN.</span><span class="sxs-lookup"><span data-stu-id="31ee0-428">The system tried to delete the JOIN of a drive that is not joined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-429"><span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**ERRORE \_ non \_ subsd**</span><span class="sxs-lookup"><span data-stu-id="31ee0-429"><span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**ERROR\_NOT\_SUBSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-430">137 (0x89)</span><span class="sxs-lookup"><span data-stu-id="31ee0-430">137 (0x89)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-431">Il sistema ha tentato di eliminare la sostituzione di un'unità che non viene sostituita.</span><span class="sxs-lookup"><span data-stu-id="31ee0-431">The system tried to delete the substitution of a drive that is not substituted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-432"><span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**errore \_ durante il join \_ \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-432"><span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**ERROR\_JOIN\_TO\_JOIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-433">138 (0x8A)</span><span class="sxs-lookup"><span data-stu-id="31ee0-433">138 (0x8A)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-434">Il sistema ha tentato di aggiungere un'unità a una directory in un'unità unita in join.</span><span class="sxs-lookup"><span data-stu-id="31ee0-434">The system tried to join a drive to a directory on a joined drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-435"><span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**ERRORE \_ da SUBST \_ a \_ SUBST**</span><span class="sxs-lookup"><span data-stu-id="31ee0-435"><span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**ERROR\_SUBST\_TO\_SUBST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-436">139 (0x8B)</span><span class="sxs-lookup"><span data-stu-id="31ee0-436">139 (0x8B)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-437">Il sistema ha tentato di sostituire un'unità con una directory in un'unità sostituita.</span><span class="sxs-lookup"><span data-stu-id="31ee0-437">The system tried to substitute a drive to a directory on a substituted drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-438"><span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**errore durante il \_ join \_ a \_ SUBST**</span><span class="sxs-lookup"><span data-stu-id="31ee0-438"><span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**ERROR\_JOIN\_TO\_SUBST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-439">140 (0x8C)</span><span class="sxs-lookup"><span data-stu-id="31ee0-439">140 (0x8C)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-440">Il sistema ha tentato di aggiungere un'unità a una directory in un'unità sostituita.</span><span class="sxs-lookup"><span data-stu-id="31ee0-440">The system tried to join a drive to a directory on a substituted drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-441"><span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**ERRORE \_ SUBST \_ da \_ unire**</span><span class="sxs-lookup"><span data-stu-id="31ee0-441"><span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**ERROR\_SUBST\_TO\_JOIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-442">141 (0x8D)</span><span class="sxs-lookup"><span data-stu-id="31ee0-442">141 (0x8D)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-443">Il sistema ha tentato di eseguire il SUBSt di un'unità in una directory in un'unità unita in join.</span><span class="sxs-lookup"><span data-stu-id="31ee0-443">The system tried to SUBST a drive to a directory on a joined drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-444"><span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**ERRORE \_ nell' \_ unità occupata**</span><span class="sxs-lookup"><span data-stu-id="31ee0-444"><span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**ERROR\_BUSY\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-445">142 (0x8E)</span><span class="sxs-lookup"><span data-stu-id="31ee0-445">142 (0x8E)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-446">Il sistema non è in grado di eseguire un JOIN o un oggetto Subs in questo momento.</span><span class="sxs-lookup"><span data-stu-id="31ee0-446">The system cannot perform a JOIN or SUBST at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-447"><span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**ERRORE della \_ stessa \_ unità**</span><span class="sxs-lookup"><span data-stu-id="31ee0-447"><span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**ERROR\_SAME\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-448">143 (0x8F)</span><span class="sxs-lookup"><span data-stu-id="31ee0-448">143 (0x8F)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-449">Il sistema non è in grado di aggiungere o sostituire un'unità con o per una directory nella stessa unità.</span><span class="sxs-lookup"><span data-stu-id="31ee0-449">The system cannot join or substitute a drive to or for a directory on the same drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-450"><span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**ERRORE \_ dir \_ non \_ radice**</span><span class="sxs-lookup"><span data-stu-id="31ee0-450"><span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**ERROR\_DIR\_NOT\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-451">144 (0x90)</span><span class="sxs-lookup"><span data-stu-id="31ee0-451">144 (0x90)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-452">La directory non è una sottodirectory della directory radice.</span><span class="sxs-lookup"><span data-stu-id="31ee0-452">The directory is not a subdirectory of the root directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-453"><span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**\_dir errore \_ non \_ vuota**</span><span class="sxs-lookup"><span data-stu-id="31ee0-453"><span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**ERROR\_DIR\_NOT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-454">145 (0x91)</span><span class="sxs-lookup"><span data-stu-id="31ee0-454">145 (0x91)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-455">La directory non è vuota.</span><span class="sxs-lookup"><span data-stu-id="31ee0-455">The directory is not empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-456"><span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**ERRORE \_ è \_ un \_ percorso SUBST**</span><span class="sxs-lookup"><span data-stu-id="31ee0-456"><span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**ERROR\_IS\_SUBST\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-457">146 (0x92)</span><span class="sxs-lookup"><span data-stu-id="31ee0-457">146 (0x92)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-458">Il percorso specificato è in uso in un sostituto.</span><span class="sxs-lookup"><span data-stu-id="31ee0-458">The path specified is being used in a substitute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-459"><span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**ERRORE \_ nel \_ percorso di join \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-459"><span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**ERROR\_IS\_JOIN\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-460">147 (0x93)</span><span class="sxs-lookup"><span data-stu-id="31ee0-460">147 (0x93)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-461">Sono disponibili risorse insufficienti per elaborare il comando.</span><span class="sxs-lookup"><span data-stu-id="31ee0-461">Not enough resources are available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-462"><span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**\_percorso errore \_ occupato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-462"><span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**ERROR\_PATH\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-463">148 (0x94)</span><span class="sxs-lookup"><span data-stu-id="31ee0-463">148 (0x94)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-464">Impossibile utilizzare il percorso specificato in questo momento.</span><span class="sxs-lookup"><span data-stu-id="31ee0-464">The path specified cannot be used at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-465"><span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**ERRORE \_ è \_ la \_ destinazione SUBST**</span><span class="sxs-lookup"><span data-stu-id="31ee0-465"><span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**ERROR\_IS\_SUBST\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-466">149 (0x95)</span><span class="sxs-lookup"><span data-stu-id="31ee0-466">149 (0x95)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-467">È stato effettuato un tentativo di aggiunta o sostituzione di un'unità per la quale una directory nell'unità è la destinazione di un sostituto precedente.</span><span class="sxs-lookup"><span data-stu-id="31ee0-467">An attempt was made to join or substitute a drive for which a directory on the drive is the target of a previous substitute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-468"><span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**\_traccia di sistema degli errori \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-468"><span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**ERROR\_SYSTEM\_TRACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-469">150 (0x96)</span><span class="sxs-lookup"><span data-stu-id="31ee0-469">150 (0x96)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-470">Le informazioni di traccia di sistema non sono state specificate nel file di CONFIG.SYS o la traccia non è consentita.</span><span class="sxs-lookup"><span data-stu-id="31ee0-470">System trace information was not specified in your CONFIG.SYS file, or tracing is disallowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-471"><span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**ERRORE \_ \_ numero eventi non validi \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-471"><span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**ERROR\_INVALID\_EVENT\_COUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-472">151 (0x97)</span><span class="sxs-lookup"><span data-stu-id="31ee0-472">151 (0x97)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-473">Il numero di eventi semaforo specificati per DosMuxSemWait non è corretto.</span><span class="sxs-lookup"><span data-stu-id="31ee0-473">The number of specified semaphore events for DosMuxSemWait is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-474"><span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**ERRORE di un \_ numero eccessivo di \_ \_ MUXWAITERS**</span><span class="sxs-lookup"><span data-stu-id="31ee0-474"><span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**ERROR\_TOO\_MANY\_MUXWAITERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-475">152 (0x98)</span><span class="sxs-lookup"><span data-stu-id="31ee0-475">152 (0x98)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-476">DosMuxSemWait non è stato eseguito; troppi semafori sono già impostati.</span><span class="sxs-lookup"><span data-stu-id="31ee0-476">DosMuxSemWait did not execute; too many semaphores are already set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-477"><span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**ERRORE \_ di \_ formato elenco non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-477"><span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**ERROR\_INVALID\_LIST\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-478">153 (0x99)</span><span class="sxs-lookup"><span data-stu-id="31ee0-478">153 (0x99)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-479">L'elenco DosMuxSemWait non è corretto.</span><span class="sxs-lookup"><span data-stu-id="31ee0-479">The DosMuxSemWait list is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-480"><span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**\_etichetta errore \_ troppo \_ lungo**</span><span class="sxs-lookup"><span data-stu-id="31ee0-480"><span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**ERROR\_LABEL\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-481">154 (0x9A)</span><span class="sxs-lookup"><span data-stu-id="31ee0-481">154 (0x9A)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-482">L'etichetta di volume immessa supera il limite di caratteri dell'etichetta della file system di destinazione.</span><span class="sxs-lookup"><span data-stu-id="31ee0-482">The volume label you entered exceeds the label character limit of the target file system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-483"><span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**ERRORE di un \_ numero eccessivo di \_ \_ TCBs**</span><span class="sxs-lookup"><span data-stu-id="31ee0-483"><span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**ERROR\_TOO\_MANY\_TCBS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-484">155 (0x9B)</span><span class="sxs-lookup"><span data-stu-id="31ee0-484">155 (0x9B)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-485">Non è possibile creare un altro thread.</span><span class="sxs-lookup"><span data-stu-id="31ee0-485">Cannot create another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-486"><span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**\_segnalazione errori \_ rifiutata**</span><span class="sxs-lookup"><span data-stu-id="31ee0-486"><span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**ERROR\_SIGNAL\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-487">156 (0x9C)</span><span class="sxs-lookup"><span data-stu-id="31ee0-487">156 (0x9C)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-488">Il processo del destinatario ha rifiutato il segnale.</span><span class="sxs-lookup"><span data-stu-id="31ee0-488">The recipient process has refused the signal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-489"><span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**ERRORE \_ eliminato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-489"><span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**ERROR\_DISCARDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-490">157 (0x9D)</span><span class="sxs-lookup"><span data-stu-id="31ee0-490">157 (0x9D)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-491">Il segmento è già stato scartato e non può essere bloccato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-491">The segment is already discarded and cannot be locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-492"><span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**ERRORE \_ non \_ bloccato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-492"><span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**ERROR\_NOT\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-493">158 (0x9E)</span><span class="sxs-lookup"><span data-stu-id="31ee0-493">158 (0x9E)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-494">Il segmento è già sbloccato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-494">The segment is already unlocked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-495"><span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**ERRORE \_ \_ addr THREADID \_ errato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-495"><span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**ERROR\_BAD\_THREADID\_ADDR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-496">159 (0x9F)</span><span class="sxs-lookup"><span data-stu-id="31ee0-496">159 (0x9F)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-497">L'indirizzo per l'ID del thread non è corretto.</span><span class="sxs-lookup"><span data-stu-id="31ee0-497">The address for the thread ID is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-498"><span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**ERRORI \_ argomenti non validi \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-498"><span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**ERROR\_BAD\_ARGUMENTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-499">160 (messaggi 0XA0)</span><span class="sxs-lookup"><span data-stu-id="31ee0-499">160 (0xA0)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-500">Uno o più argomenti non sono corretti.</span><span class="sxs-lookup"><span data-stu-id="31ee0-500">One or more arguments are not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-501"><span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**\_ \_ nome percorso errato errore**</span><span class="sxs-lookup"><span data-stu-id="31ee0-501"><span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**ERROR\_BAD\_PATHNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-502">161 (0xA1)</span><span class="sxs-lookup"><span data-stu-id="31ee0-502">161 (0xA1)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-503">Il percorso specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="31ee0-503">The specified path is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-504"><span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**\_segnalazione errori \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="31ee0-504"><span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**ERROR\_SIGNAL\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-505">162 (0xA2)</span><span class="sxs-lookup"><span data-stu-id="31ee0-505">162 (0xA2)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-506">Un segnale è già in sospeso.</span><span class="sxs-lookup"><span data-stu-id="31ee0-506">A signal is already pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-507"><span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**ERRORE \_ massimo \_ THRDS \_ raggiunto**</span><span class="sxs-lookup"><span data-stu-id="31ee0-507"><span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**ERROR\_MAX\_THRDS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-508">164 (0xA4)</span><span class="sxs-lookup"><span data-stu-id="31ee0-508">164 (0xA4)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-509">Non è possibile creare altri thread nel sistema.</span><span class="sxs-lookup"><span data-stu-id="31ee0-509">No more threads can be created in the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-510"><span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**\_blocco errore \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="31ee0-510"><span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**ERROR\_LOCK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-511">167 (0xA7)</span><span class="sxs-lookup"><span data-stu-id="31ee0-511">167 (0xA7)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-512">Non è possibile bloccare un'area di un file.</span><span class="sxs-lookup"><span data-stu-id="31ee0-512">Unable to lock a region of a file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-513"><span id="ERROR_BUSY"></span><span id="error_busy"></span>**ERRORE \_ occupato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-513"><span id="ERROR_BUSY"></span><span id="error_busy"></span>**ERROR\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-514">170 (0xAA)</span><span class="sxs-lookup"><span data-stu-id="31ee0-514">170 (0xAA)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-515">La risorsa richiesta è in uso.</span><span class="sxs-lookup"><span data-stu-id="31ee0-515">The requested resource is in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-516"><span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**\_supporto dei dispositivi \_ con errori \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="31ee0-516"><span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**ERROR\_DEVICE\_SUPPORT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-517">171 (0xAB)</span><span class="sxs-lookup"><span data-stu-id="31ee0-517">171 (0xAB)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-518">Il rilevamento del supporto del comando del dispositivo è in corso.</span><span class="sxs-lookup"><span data-stu-id="31ee0-518">Device's command support detection is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-519"><span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**ERRORE di \_ annullamento della \_ violazione**</span><span class="sxs-lookup"><span data-stu-id="31ee0-519"><span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**ERROR\_CANCEL\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-520">173 (0xAD)</span><span class="sxs-lookup"><span data-stu-id="31ee0-520">173 (0xAD)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-521">Richiesta di blocco non in attesa per l'area di annullamento specificata.</span><span class="sxs-lookup"><span data-stu-id="31ee0-521">A lock request was not outstanding for the supplied cancel region.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-522"><span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**ERRORE \_ blocchi atomici \_ \_ non \_ supportati**</span><span class="sxs-lookup"><span data-stu-id="31ee0-522"><span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**ERROR\_ATOMIC\_LOCKS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-523">174 (0xAE)</span><span class="sxs-lookup"><span data-stu-id="31ee0-523">174 (0xAE)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-524">Il file system non supporta le modifiche atomiche al tipo di blocco.</span><span class="sxs-lookup"><span data-stu-id="31ee0-524">The file system does not support atomic changes to the lock type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-525"><span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**ERRORE \_ \_ numero di segmento non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-525"><span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**ERROR\_INVALID\_SEGMENT\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-526">180 (0xB4)</span><span class="sxs-lookup"><span data-stu-id="31ee0-526">180 (0xB4)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-527">Il sistema ha rilevato un numero di segmento non corretto.</span><span class="sxs-lookup"><span data-stu-id="31ee0-527">The system detected a segment number that was not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-528"><span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**ERRORE \_ \_ ordinale non valido**</span><span class="sxs-lookup"><span data-stu-id="31ee0-528"><span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**ERROR\_INVALID\_ORDINAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-529">182 (0xB6)</span><span class="sxs-lookup"><span data-stu-id="31ee0-529">182 (0xB6)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-530">Il sistema operativo non è in grado di eseguire %1.</span><span class="sxs-lookup"><span data-stu-id="31ee0-530">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-531"><span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**ERRORE \_ già \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="31ee0-531"><span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**ERROR\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-532">183 (0xB7)</span><span class="sxs-lookup"><span data-stu-id="31ee0-532">183 (0xB7)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-533">Impossibile creare un file, se il file esiste già.</span><span class="sxs-lookup"><span data-stu-id="31ee0-533">Cannot create a file when that file already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-534"><span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**ERRORE \_ \_ numero di flag non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-534"><span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**ERROR\_INVALID\_FLAG\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-535">186 (0xBA)</span><span class="sxs-lookup"><span data-stu-id="31ee0-535">186 (0xBA)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-536">Il flag passato non è corretto.</span><span class="sxs-lookup"><span data-stu-id="31ee0-536">The flag passed is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-537"><span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**ERRORE \_ sem \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-537"><span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**ERROR\_SEM\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-538">187 (0xBB)</span><span class="sxs-lookup"><span data-stu-id="31ee0-538">187 (0xBB)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-539">Il nome del semaforo di sistema specificato non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-539">The specified system semaphore name was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-540"><span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**ERRORE \_ di \_ avvio di CODESEG non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-540"><span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**ERROR\_INVALID\_STARTING\_CODESEG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-541">188 (0xBC)</span><span class="sxs-lookup"><span data-stu-id="31ee0-541">188 (0xBC)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-542">Il sistema operativo non è in grado di eseguire %1.</span><span class="sxs-lookup"><span data-stu-id="31ee0-542">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-543"><span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**ERRORE \_ STACKSEG non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-543"><span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**ERROR\_INVALID\_STACKSEG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-544">189 (0xBD)</span><span class="sxs-lookup"><span data-stu-id="31ee0-544">189 (0xBD)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-545">Il sistema operativo non è in grado di eseguire %1.</span><span class="sxs-lookup"><span data-stu-id="31ee0-545">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-546"><span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**ERRORE \_ MODULETYPE non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-546"><span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**ERROR\_INVALID\_MODULETYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-547">190 (0xBE)</span><span class="sxs-lookup"><span data-stu-id="31ee0-547">190 (0xBE)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-548">Il sistema operativo non è in grado di eseguire %1.</span><span class="sxs-lookup"><span data-stu-id="31ee0-548">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-549"><span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**ERRORE \_ di \_ firma exe non valida \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-549"><span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**ERROR\_INVALID\_EXE\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-550">191 (0xBF)</span><span class="sxs-lookup"><span data-stu-id="31ee0-550">191 (0xBF)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-551">Impossibile eseguire %1 in modalità Win32.</span><span class="sxs-lookup"><span data-stu-id="31ee0-551">Cannot run %1 in Win32 mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-552"><span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**ERRORE del file \_ exe \_ contrassegnato come \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="31ee0-552"><span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**ERROR\_EXE\_MARKED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-553">192 (0xC0)</span><span class="sxs-lookup"><span data-stu-id="31ee0-553">192 (0xC0)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-554">Il sistema operativo non è in grado di eseguire %1.</span><span class="sxs-lookup"><span data-stu-id="31ee0-554">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-555"><span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**ERRORE \_ nel \_ formato exe errato \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-555"><span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**ERROR\_BAD\_EXE\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-556">193 (0xC1)</span><span class="sxs-lookup"><span data-stu-id="31ee0-556">193 (0xC1)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-557">%1 non è un'applicazione Win32 valida.</span><span class="sxs-lookup"><span data-stu-id="31ee0-557">%1 is not a valid Win32 application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-558"><span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**Errore durante l' \_ iterazione \_ dei dati \_ supera \_ 64K**</span><span class="sxs-lookup"><span data-stu-id="31ee0-558"><span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**ERROR\_ITERATED\_DATA\_EXCEEDS\_64k**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-559">194 (0xC2)</span><span class="sxs-lookup"><span data-stu-id="31ee0-559">194 (0xC2)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-560">Il sistema operativo non è in grado di eseguire %1.</span><span class="sxs-lookup"><span data-stu-id="31ee0-560">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-561"><span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**ERRORE \_ MINALLOCSIZE non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-561"><span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**ERROR\_INVALID\_MINALLOCSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-562">195 (0xC3)</span><span class="sxs-lookup"><span data-stu-id="31ee0-562">195 (0xC3)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-563">Il sistema operativo non è in grado di eseguire %1.</span><span class="sxs-lookup"><span data-stu-id="31ee0-563">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-564"><span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**ERRORE \_ DYNLINK \_ dall' \_ anello non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-564"><span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**ERROR\_DYNLINK\_FROM\_INVALID\_RING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-565">196 (0xC4)</span><span class="sxs-lookup"><span data-stu-id="31ee0-565">196 (0xC4)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-566">Il sistema operativo non è in grado di eseguire questo programma applicativo.</span><span class="sxs-lookup"><span data-stu-id="31ee0-566">The operating system cannot run this application program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-567"><span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**ERRORE \_ IOPL \_ non \_ abilitato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-567"><span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**ERROR\_IOPL\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-568">197 (0xC5)</span><span class="sxs-lookup"><span data-stu-id="31ee0-568">197 (0xC5)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-569">Il sistema operativo non è attualmente configurato per l'esecuzione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="31ee0-569">The operating system is not presently configured to run this application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-570"><span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**ERRORE \_ SEGDPL non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-570"><span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**ERROR\_INVALID\_SEGDPL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-571">198 (0xC6)</span><span class="sxs-lookup"><span data-stu-id="31ee0-571">198 (0xC6)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-572">Il sistema operativo non è in grado di eseguire %1.</span><span class="sxs-lookup"><span data-stu-id="31ee0-572">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-573"><span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**ERRORE \_ AUTODATASEG \_ supera \_ 64K**</span><span class="sxs-lookup"><span data-stu-id="31ee0-573"><span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**ERROR\_AUTODATASEG\_EXCEEDS\_64k**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-574">199 (0xC7)</span><span class="sxs-lookup"><span data-stu-id="31ee0-574">199 (0xC7)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-575">Il sistema operativo non è in grado di eseguire questo programma applicativo.</span><span class="sxs-lookup"><span data-stu-id="31ee0-575">The operating system cannot run this application program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-576"><span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**Il \_ RING2SEG di errore \_ deve \_ essere \_ mobile**</span><span class="sxs-lookup"><span data-stu-id="31ee0-576"><span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**ERROR\_RING2SEG\_MUST\_BE\_MOVABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-577">200 (0xC8)</span><span class="sxs-lookup"><span data-stu-id="31ee0-577">200 (0xC8)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-578">Il segmento di codice non può essere maggiore o uguale a 64K.</span><span class="sxs-lookup"><span data-stu-id="31ee0-578">The code segment cannot be greater than or equal to 64K.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-579"><span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**ERRORE \_ \_ XEEDS catena \_ reloc \_ SEGLIM**</span><span class="sxs-lookup"><span data-stu-id="31ee0-579"><span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**ERROR\_RELOC\_CHAIN\_XEEDS\_SEGLIM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-580">201 (0xC9)</span><span class="sxs-lookup"><span data-stu-id="31ee0-580">201 (0xC9)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-581">Il sistema operativo non è in grado di eseguire %1.</span><span class="sxs-lookup"><span data-stu-id="31ee0-581">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-582"><span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**ERRORE \_ INFLOOP \_ nella \_ \_ catena reloc**</span><span class="sxs-lookup"><span data-stu-id="31ee0-582"><span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**ERROR\_INFLOOP\_IN\_RELOC\_CHAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-583">202 (0xCA)</span><span class="sxs-lookup"><span data-stu-id="31ee0-583">202 (0xCA)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-584">Il sistema operativo non è in grado di eseguire %1.</span><span class="sxs-lookup"><span data-stu-id="31ee0-584">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-585"><span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**ERRORE \_ ENVVAR \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-585"><span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**ERROR\_ENVVAR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-586">203 (0xCB)</span><span class="sxs-lookup"><span data-stu-id="31ee0-586">203 (0xCB)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-587">Il sistema non è riuscito a trovare l'opzione di ambiente immessa.</span><span class="sxs-lookup"><span data-stu-id="31ee0-587">The system could not find the environment option that was entered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-588"><span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**ERRORE \_ nessun \_ segnale \_ inviato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-588"><span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**ERROR\_NO\_SIGNAL\_SENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-589">205 (0xCD)</span><span class="sxs-lookup"><span data-stu-id="31ee0-589">205 (0xCD)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-590">Nessun processo nel sottoalbero dei comandi dispone di un gestore di segnale.</span><span class="sxs-lookup"><span data-stu-id="31ee0-590">No process in the command subtree has a signal handler.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-591"><span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**ERRORE del \_ nome file \_ EXCED \_ Range**</span><span class="sxs-lookup"><span data-stu-id="31ee0-591"><span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**ERROR\_FILENAME\_EXCED\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-592">206 (0xCE)</span><span class="sxs-lookup"><span data-stu-id="31ee0-592">206 (0xCE)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-593">Il nome file o l'estensione è troppo lungo.</span><span class="sxs-lookup"><span data-stu-id="31ee0-593">The filename or extension is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-594"><span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**ERRORE \_ RING2 \_ Stack \_ in \_ uso**</span><span class="sxs-lookup"><span data-stu-id="31ee0-594"><span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**ERROR\_RING2\_STACK\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-595">207 (0xCF)</span><span class="sxs-lookup"><span data-stu-id="31ee0-595">207 (0xCF)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-596">Lo stack Ring 2 è in uso.</span><span class="sxs-lookup"><span data-stu-id="31ee0-596">The ring 2 stack is in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-597"><span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**ERRORE \_ meta di \_ espansione \_ troppo \_ lungo**</span><span class="sxs-lookup"><span data-stu-id="31ee0-597"><span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**ERROR\_META\_EXPANSION\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-598">208 (0xD0)</span><span class="sxs-lookup"><span data-stu-id="31ee0-598">208 (0xD0)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-599">I caratteri di nome file globali, \* o?, vengono immessi in modo errato o sono stati specificati troppi caratteri di nome file globali.</span><span class="sxs-lookup"><span data-stu-id="31ee0-599">The global filename characters, \* or ?, are entered incorrectly or too many global filename characters are specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-600"><span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**ERRORE \_ \_ numero segnale non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-600"><span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**ERROR\_INVALID\_SIGNAL\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-601">209 (0xD1)</span><span class="sxs-lookup"><span data-stu-id="31ee0-601">209 (0xD1)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-602">Il segnale inviato non è corretto.</span><span class="sxs-lookup"><span data-stu-id="31ee0-602">The signal being posted is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-603"><span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**THREAD di errore \_ \_ 1 \_ inattivo**</span><span class="sxs-lookup"><span data-stu-id="31ee0-603"><span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**ERROR\_THREAD\_1\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-604">210 (0xD2)</span><span class="sxs-lookup"><span data-stu-id="31ee0-604">210 (0xD2)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-605">Impossibile impostare il gestore del segnale.</span><span class="sxs-lookup"><span data-stu-id="31ee0-605">The signal handler cannot be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-606"><span id="ERROR_LOCKED"></span><span id="error_locked"></span>**ERRORE \_ bloccato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-606"><span id="ERROR_LOCKED"></span><span id="error_locked"></span>**ERROR\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-607">212 (0xD4)</span><span class="sxs-lookup"><span data-stu-id="31ee0-607">212 (0xD4)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-608">Il segmento è bloccato e non può essere riallocato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-608">The segment is locked and cannot be reallocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-609"><span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**ERRORE di un \_ numero eccessivo di \_ \_ moduli**</span><span class="sxs-lookup"><span data-stu-id="31ee0-609"><span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**ERROR\_TOO\_MANY\_MODULES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-610">214 (0xD6)</span><span class="sxs-lookup"><span data-stu-id="31ee0-610">214 (0xD6)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-611">Troppi moduli di collegamento dinamico collegati al programma o al modulo a collegamento dinamico.</span><span class="sxs-lookup"><span data-stu-id="31ee0-611">Too many dynamic-link modules are attached to this program or dynamic-link module.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-612"><span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**\_annidamento errori \_ non \_ consentito**</span><span class="sxs-lookup"><span data-stu-id="31ee0-612"><span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**ERROR\_NESTING\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-613">215 (0xD7)</span><span class="sxs-lookup"><span data-stu-id="31ee0-613">215 (0xD7)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-614">Impossibile annidare le chiamate a LoadModule.</span><span class="sxs-lookup"><span data-stu-id="31ee0-614">Cannot nest calls to LoadModule.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-615"><span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**\_tipo di computer exe errore non \_ \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="31ee0-615"><span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**ERROR\_EXE\_MACHINE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-616">216 (0xD8)</span><span class="sxs-lookup"><span data-stu-id="31ee0-616">216 (0xD8)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-617">Questa versione di %1 non è compatibile con la versione di Windows in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="31ee0-617">This version of %1 is not compatible with the version of Windows you're running.</span></span> <span data-ttu-id="31ee0-618">Controllare le informazioni di sistema del computer e contattare l'autore del software.</span><span class="sxs-lookup"><span data-stu-id="31ee0-618">Check your computer's system information and then contact the software publisher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-619"><span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**ERRORE \_ exe \_ non è possibile \_ modificare il \_ \_ file binario firmato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-619"><span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**ERROR\_EXE\_CANNOT\_MODIFY\_SIGNED\_BINARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-620">217 (0xD9)</span><span class="sxs-lookup"><span data-stu-id="31ee0-620">217 (0xD9)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-621">Il file di immagine %1 è firmato. Impossibile modificarlo.</span><span class="sxs-lookup"><span data-stu-id="31ee0-621">The image file %1 is signed, unable to modify.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-622"><span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**ERRORE \_ exe \_ non è possibile \_ modificare il \_ \_ \_ file binario con firma complessa**</span><span class="sxs-lookup"><span data-stu-id="31ee0-622"><span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**ERROR\_EXE\_CANNOT\_MODIFY\_STRONG\_SIGNED\_BINARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-623">218 (0xDA)</span><span class="sxs-lookup"><span data-stu-id="31ee0-623">218 (0xDA)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-624">Il file di immagine %1 è firmato con firma sicura, non è possibile modificarlo.</span><span class="sxs-lookup"><span data-stu-id="31ee0-624">The image file %1 is strong signed, unable to modify.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-625"><span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**FILE di errore \_ \_ Estratto \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-625"><span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**ERROR\_FILE\_CHECKED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-626">220 (0xDC)</span><span class="sxs-lookup"><span data-stu-id="31ee0-626">220 (0xDC)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-627">Il file è stato estratto o bloccato per la modifica da un altro utente.</span><span class="sxs-lookup"><span data-stu-id="31ee0-627">This file is checked out or locked for editing by another user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-628"><span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**ERRORE di \_ checkout \_ obbligatorio**</span><span class="sxs-lookup"><span data-stu-id="31ee0-628"><span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**ERROR\_CHECKOUT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-629">221 (0xDD)</span><span class="sxs-lookup"><span data-stu-id="31ee0-629">221 (0xDD)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-630">Il file deve essere estratto prima di salvare le modifiche.</span><span class="sxs-lookup"><span data-stu-id="31ee0-630">The file must be checked out before saving changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-631"><span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**ERRORE \_ \_ tipo di file non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-631"><span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**ERROR\_BAD\_FILE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-632">222 (0xDE)</span><span class="sxs-lookup"><span data-stu-id="31ee0-632">222 (0xDE)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-633">Il tipo di file salvato o recuperato è stato bloccato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-633">The file type being saved or retrieved has been blocked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-634"><span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**FILE di errore \_ \_ troppo \_ grande**</span><span class="sxs-lookup"><span data-stu-id="31ee0-634"><span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**ERROR\_FILE\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-635">223 (0xDF)</span><span class="sxs-lookup"><span data-stu-id="31ee0-635">223 (0xDF)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-636">Le dimensioni del file superano il limite consentito e non possono essere salvate.</span><span class="sxs-lookup"><span data-stu-id="31ee0-636">The file size exceeds the limit allowed and cannot be saved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-637"><span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**\_autorizzazione moduli di errore \_ \_ obbligatoria**</span><span class="sxs-lookup"><span data-stu-id="31ee0-637"><span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**ERROR\_FORMS\_AUTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-638">224 (0xE0)</span><span class="sxs-lookup"><span data-stu-id="31ee0-638">224 (0xE0)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-639">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-639">Access Denied.</span></span> <span data-ttu-id="31ee0-640">Prima di aprire i file in questo percorso, è necessario innanzitutto aggiungere il sito Web all'elenco siti attendibili, passare al sito Web e selezionare l'opzione per l'accesso automatico.</span><span class="sxs-lookup"><span data-stu-id="31ee0-640">Before opening files in this location, you must first add the web site to your trusted sites list, browse to the web site, and select the option to login automatically.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-641"><span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**ERRORE \_ virus \_ infetto**</span><span class="sxs-lookup"><span data-stu-id="31ee0-641"><span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**ERROR\_VIRUS\_INFECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-642">225 (0xE1)</span><span class="sxs-lookup"><span data-stu-id="31ee0-642">225 (0xE1)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-643">L'operazione non è stata completata perché il file contiene un virus o software potenzialmente indesiderato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-643">Operation did not complete successfully because the file contains a virus or potentially unwanted software.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-644"><span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**ERRORE \_ virus \_ eliminato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-644"><span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**ERROR\_VIRUS\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-645">226 (0xE2)</span><span class="sxs-lookup"><span data-stu-id="31ee0-645">226 (0xE2)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-646">Questo file contiene un virus o software potenzialmente indesiderato e non può essere aperto.</span><span class="sxs-lookup"><span data-stu-id="31ee0-646">This file contains a virus or potentially unwanted software and cannot be opened.</span></span> <span data-ttu-id="31ee0-647">A causa della natura di questo virus o di software potenzialmente indesiderato, il file è stato rimosso da questo percorso.</span><span class="sxs-lookup"><span data-stu-id="31ee0-647">Due to the nature of this virus or potentially unwanted software, the file has been removed from this location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-648"><span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**PIPE di errore \_ \_ locale**</span><span class="sxs-lookup"><span data-stu-id="31ee0-648"><span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**ERROR\_PIPE\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-649">229 (0xE5)</span><span class="sxs-lookup"><span data-stu-id="31ee0-649">229 (0xE5)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-650">La pipe è locale.</span><span class="sxs-lookup"><span data-stu-id="31ee0-650">The pipe is local.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-651"><span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**PIPE errore non \_ valida \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-651"><span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**ERROR\_BAD\_PIPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-652">230 (0xE6)</span><span class="sxs-lookup"><span data-stu-id="31ee0-652">230 (0xE6)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-653">Lo stato della pipe non è valido.</span><span class="sxs-lookup"><span data-stu-id="31ee0-653">The pipe state is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-654"><span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**PIPE di errore \_ \_ occupata**</span><span class="sxs-lookup"><span data-stu-id="31ee0-654"><span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**ERROR\_PIPE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-655">231 (0xE7)</span><span class="sxs-lookup"><span data-stu-id="31ee0-655">231 (0xE7)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-656">Tutte le istanze di pipe sono occupate.</span><span class="sxs-lookup"><span data-stu-id="31ee0-656">All pipe instances are busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-657"><span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**ERRORE \_ nessun \_ dato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-657"><span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**ERROR\_NO\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-658">232 (0xE8)</span><span class="sxs-lookup"><span data-stu-id="31ee0-658">232 (0xE8)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-659">La pipe verrà chiusa.</span><span class="sxs-lookup"><span data-stu-id="31ee0-659">The pipe is being closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-660"><span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**PIPE degli errori \_ \_ non \_ connessa**</span><span class="sxs-lookup"><span data-stu-id="31ee0-660"><span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**ERROR\_PIPE\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-661">233 (0xE9)</span><span class="sxs-lookup"><span data-stu-id="31ee0-661">233 (0xE9)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-662">Nessun processo è sull'altra estremità della pipe.</span><span class="sxs-lookup"><span data-stu-id="31ee0-662">No process is on the other end of the pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-663"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERRORE di \_ più \_ dati**</span><span class="sxs-lookup"><span data-stu-id="31ee0-663"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERROR\_MORE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-664">234 (0xEA)</span><span class="sxs-lookup"><span data-stu-id="31ee0-664">234 (0xEA)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-665">sono disponibili più dati.</span><span class="sxs-lookup"><span data-stu-id="31ee0-665">More data is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-666"><span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**ERRORE \_ VC \_ disconnesso**</span><span class="sxs-lookup"><span data-stu-id="31ee0-666"><span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**ERROR\_VC\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-667">240 (0xF0)</span><span class="sxs-lookup"><span data-stu-id="31ee0-667">240 (0xF0)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-668">La sessione è stata annullata.</span><span class="sxs-lookup"><span data-stu-id="31ee0-668">The session was canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-669"><span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**ERRORE \_ \_ nome EA non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-669"><span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**ERROR\_INVALID\_EA\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-670">254 (0xFE)</span><span class="sxs-lookup"><span data-stu-id="31ee0-670">254 (0xFE)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-671">Il nome dell'attributo esteso specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="31ee0-671">The specified extended attribute name was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-672"><span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**\_elenco EA \_ errore \_ incoerente**</span><span class="sxs-lookup"><span data-stu-id="31ee0-672"><span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**ERROR\_EA\_LIST\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-673">255 (0xFF)</span><span class="sxs-lookup"><span data-stu-id="31ee0-673">255 (0xFF)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-674">Gli attributi estesi sono incoerenti.</span><span class="sxs-lookup"><span data-stu-id="31ee0-674">The extended attributes are inconsistent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-675"><span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**TIMEOUT di attesa \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-675"><span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**WAIT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-676">258 (0x102)</span><span class="sxs-lookup"><span data-stu-id="31ee0-676">258 (0x102)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-677">Tempo di attesa scaduto.</span><span class="sxs-lookup"><span data-stu-id="31ee0-677">The wait operation timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-678"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERRORE \_ nessun \_ altro \_ elemento**</span><span class="sxs-lookup"><span data-stu-id="31ee0-678"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERROR\_NO\_MORE\_ITEMS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-679">259 (0x103)</span><span class="sxs-lookup"><span data-stu-id="31ee0-679">259 (0x103)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-680">Dati disponibili esauriti.</span><span class="sxs-lookup"><span data-stu-id="31ee0-680">No more data is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-681"><span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**ERRORE \_ di \_ copia**</span><span class="sxs-lookup"><span data-stu-id="31ee0-681"><span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**ERROR\_CANNOT\_COPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-682">266 (0x10A)</span><span class="sxs-lookup"><span data-stu-id="31ee0-682">266 (0x10A)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-683">Impossibile utilizzare le funzioni di copia.</span><span class="sxs-lookup"><span data-stu-id="31ee0-683">The copy functions cannot be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-684"><span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**Directory degli errori \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-684"><span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**ERROR\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-685">267 (0x10B)</span><span class="sxs-lookup"><span data-stu-id="31ee0-685">267 (0x10B)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-686">Il nome della directory non è valido.</span><span class="sxs-lookup"><span data-stu-id="31ee0-686">The directory name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-687"><span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**ERRORE \_ EAS non \_ \_ adatto**</span><span class="sxs-lookup"><span data-stu-id="31ee0-687"><span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**ERROR\_EAS\_DIDNT\_FIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-688">275 (0x113)</span><span class="sxs-lookup"><span data-stu-id="31ee0-688">275 (0x113)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-689">Gli attributi estesi non rientravano nel buffer.</span><span class="sxs-lookup"><span data-stu-id="31ee0-689">The extended attributes did not fit in the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-690"><span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**ERRORE \_ \_ file EA \_ danneggiato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-690"><span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**ERROR\_EA\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-691">276 (0x114)</span><span class="sxs-lookup"><span data-stu-id="31ee0-691">276 (0x114)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-692">Il file di attributo esteso nel file system montato è danneggiato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-692">The extended attribute file on the mounted file system is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-693"><span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**ERRORE \_ \_ tabella EA \_ completa**</span><span class="sxs-lookup"><span data-stu-id="31ee0-693"><span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**ERROR\_EA\_TABLE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-694">277 (0x115)</span><span class="sxs-lookup"><span data-stu-id="31ee0-694">277 (0x115)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-695">Il file di tabella dell'attributo esteso è pieno.</span><span class="sxs-lookup"><span data-stu-id="31ee0-695">The extended attribute table file is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-696"><span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**ERRORE \_ \_ handle EA non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-696"><span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**ERROR\_INVALID\_EA\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-697">278 (0x116)</span><span class="sxs-lookup"><span data-stu-id="31ee0-697">278 (0x116)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-698">L'handle di attributo esteso specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="31ee0-698">The specified extended attribute handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-699"><span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**ERRORE \_ EAS \_ non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-699"><span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**ERROR\_EAS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-700">282 (0x11A)</span><span class="sxs-lookup"><span data-stu-id="31ee0-700">282 (0x11A)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-701">Il file system montato non supporta gli attributi estesi.</span><span class="sxs-lookup"><span data-stu-id="31ee0-701">The mounted file system does not support extended attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-702"><span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**ERRORE \_ non \_ proprietario**</span><span class="sxs-lookup"><span data-stu-id="31ee0-702"><span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**ERROR\_NOT\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-703">288 (0x120)</span><span class="sxs-lookup"><span data-stu-id="31ee0-703">288 (0x120)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-704">Tentativo di rilascio di mutex non di proprietà del chiamante.</span><span class="sxs-lookup"><span data-stu-id="31ee0-704">Attempt to release mutex not owned by caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-705"><span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**ERRORE di un \_ numero eccessivo di \_ \_ post**</span><span class="sxs-lookup"><span data-stu-id="31ee0-705"><span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**ERROR\_TOO\_MANY\_POSTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-706">298 (0x12A)</span><span class="sxs-lookup"><span data-stu-id="31ee0-706">298 (0x12A)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-707">Sono stati apportati troppi post a un semaforo.</span><span class="sxs-lookup"><span data-stu-id="31ee0-707">Too many posts were made to a semaphore.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-708"><span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**ERRORE \_ di \_ copia parziale**</span><span class="sxs-lookup"><span data-stu-id="31ee0-708"><span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**ERROR\_PARTIAL\_COPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-709">299 (0x12B)</span><span class="sxs-lookup"><span data-stu-id="31ee0-709">299 (0x12B)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-710">Solo una parte di una richiesta ReadProcessMemory o WriteProcessMemory è stata completata.</span><span class="sxs-lookup"><span data-stu-id="31ee0-710">Only part of a ReadProcessMemory or WriteProcessMemory request was completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-711"><span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**ERRORE \_ blocco opportunistico \_ non \_ concesso**</span><span class="sxs-lookup"><span data-stu-id="31ee0-711"><span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**ERROR\_OPLOCK\_NOT\_GRANTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-712">300 (0x12C)</span><span class="sxs-lookup"><span data-stu-id="31ee0-712">300 (0x12C)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-713">La richiesta blocco opportunistico è stata negata.</span><span class="sxs-lookup"><span data-stu-id="31ee0-713">The oplock request is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-714"><span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**ERRORE \_ del \_ protocollo blocco opportunistico non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-714"><span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**ERROR\_INVALID\_OPLOCK\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-715">301 (0x12D)</span><span class="sxs-lookup"><span data-stu-id="31ee0-715">301 (0x12D)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-716">Il sistema ha ricevuto un riconoscimento blocco opportunistico non valido.</span><span class="sxs-lookup"><span data-stu-id="31ee0-716">An invalid oplock acknowledgment was received by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-717"><span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**disco di errore \_ \_ troppo \_ frammentato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-717"><span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**ERROR\_DISK\_TOO\_FRAGMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-718">302 (0x12E)</span><span class="sxs-lookup"><span data-stu-id="31ee0-718">302 (0x12E)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-719">Il volume è troppo frammentato per completare questa operazione.</span><span class="sxs-lookup"><span data-stu-id="31ee0-719">The volume is too fragmented to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-720"><span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**ERRORE di \_ eliminazione \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="31ee0-720"><span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**ERROR\_DELETE\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-721">303 (0x12F)</span><span class="sxs-lookup"><span data-stu-id="31ee0-721">303 (0x12F)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-722">Non è possibile aprire il file perché è in fase di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="31ee0-722">The file cannot be opened because it is in the process of being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-723"><span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**ERRORE \_ incompatibile \_ con \_ l' \_ \_ \_ impostazione del registro di sistema nome breve globale \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-723"><span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**ERROR\_INCOMPATIBLE\_WITH\_GLOBAL\_SHORT\_NAME\_REGISTRY\_SETTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-724">304 (0x130)</span><span class="sxs-lookup"><span data-stu-id="31ee0-724">304 (0x130)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-725">Le impostazioni nome breve potrebbero non essere modificate in questo volume a causa dell'impostazione globale del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="31ee0-725">Short name settings may not be changed on this volume due to the global registry setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-726"><span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**\_nomi brevi \_ \_ di errore non \_ abilitati \_ nel \_ volume**</span><span class="sxs-lookup"><span data-stu-id="31ee0-726"><span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**ERROR\_SHORT\_NAMES\_NOT\_ENABLED\_ON\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-727">305 (0x131)</span><span class="sxs-lookup"><span data-stu-id="31ee0-727">305 (0x131)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-728">I nomi brevi non sono abilitati in questo volume.</span><span class="sxs-lookup"><span data-stu-id="31ee0-728">Short names are not enabled on this volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-729"><span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**il \_ flusso di sicurezza degli errori \_ \_ è \_ incoerente**</span><span class="sxs-lookup"><span data-stu-id="31ee0-729"><span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**ERROR\_SECURITY\_STREAM\_IS\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-730">306 (0x132)</span><span class="sxs-lookup"><span data-stu-id="31ee0-730">306 (0x132)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-731">Il flusso di sicurezza per il volume specificato è in uno stato incoerente.</span><span class="sxs-lookup"><span data-stu-id="31ee0-731">The security stream for the given volume is in an inconsistent state.</span></span> <span data-ttu-id="31ee0-732">Eseguire CHKDSK nel volume.</span><span class="sxs-lookup"><span data-stu-id="31ee0-732">Please run CHKDSK on the volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-733"><span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**ERRORE \_ di \_ intervallo di blocco non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-733"><span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**ERROR\_INVALID\_LOCK\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-734">307 (0x133)</span><span class="sxs-lookup"><span data-stu-id="31ee0-734">307 (0x133)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-735">Impossibile elaborare un'operazione di blocco file richiesta a causa di un intervallo di byte non valido.</span><span class="sxs-lookup"><span data-stu-id="31ee0-735">A requested file lock operation cannot be processed due to an invalid byte range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-736"><span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**\_sottosistema immagine errore \_ \_ non \_ presente**</span><span class="sxs-lookup"><span data-stu-id="31ee0-736"><span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**ERROR\_IMAGE\_SUBSYSTEM\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-737">308 (0x134)</span><span class="sxs-lookup"><span data-stu-id="31ee0-737">308 (0x134)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-738">Il sottosistema necessario per supportare il tipo di immagine non è presente.</span><span class="sxs-lookup"><span data-stu-id="31ee0-738">The subsystem needed to support the image type is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-739"><span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**GUID della notifica di errore \_ \_ \_ già \_ definito**</span><span class="sxs-lookup"><span data-stu-id="31ee0-739"><span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**ERROR\_NOTIFICATION\_GUID\_ALREADY\_DEFINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-740">309 (0x135)</span><span class="sxs-lookup"><span data-stu-id="31ee0-740">309 (0x135)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-741">Al file specificato è già associato un GUID di notifica.</span><span class="sxs-lookup"><span data-stu-id="31ee0-741">The specified file already has a notification GUID associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-742"><span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**ERRORE \_ del \_ gestore di eccezioni non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-742"><span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**ERROR\_INVALID\_EXCEPTION\_HANDLER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-743">310 (0x136)</span><span class="sxs-lookup"><span data-stu-id="31ee0-743">310 (0x136)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-744">È stata rilevata una routine del gestore di eccezioni non valida.</span><span class="sxs-lookup"><span data-stu-id="31ee0-744">An invalid exception handler routine has been detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-745"><span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**\_privilegi duplicati errore \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-745"><span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**ERROR\_DUPLICATE\_PRIVILEGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-746">311 (0x137)</span><span class="sxs-lookup"><span data-stu-id="31ee0-746">311 (0x137)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-747">Sono stati specificati privilegi duplicati per il token.</span><span class="sxs-lookup"><span data-stu-id="31ee0-747">Duplicate privileges were specified for the token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-748"><span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**ERRORE \_ nessun \_ intervallo \_ elaborato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-748"><span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**ERROR\_NO\_RANGES\_PROCESSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-749">312 (0x138)</span><span class="sxs-lookup"><span data-stu-id="31ee0-749">312 (0x138)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-750">Non è stato possibile elaborare intervalli per l'operazione specificata.</span><span class="sxs-lookup"><span data-stu-id="31ee0-750">No ranges for the specified operation were able to be processed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-751"><span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**ERRORE \_ non \_ consentito \_ nel \_ file di sistema \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-751"><span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**ERROR\_NOT\_ALLOWED\_ON\_SYSTEM\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-752">313 (0x139)</span><span class="sxs-lookup"><span data-stu-id="31ee0-752">313 (0x139)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-753">Operazione non consentita su un file interno file system.</span><span class="sxs-lookup"><span data-stu-id="31ee0-753">Operation is not allowed on a file system internal file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-754"><span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**\_risorse disco di errore \_ \_ esaurite**</span><span class="sxs-lookup"><span data-stu-id="31ee0-754"><span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**ERROR\_DISK\_RESOURCES\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-755">314 (0x13A)</span><span class="sxs-lookup"><span data-stu-id="31ee0-755">314 (0x13A)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-756">Le risorse fisiche di questo disco sono esaurite.</span><span class="sxs-lookup"><span data-stu-id="31ee0-756">The physical resources of this disk have been exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-757"><span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**ERRORE \_ di \_ token non valido**</span><span class="sxs-lookup"><span data-stu-id="31ee0-757"><span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**ERROR\_INVALID\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-758">315 (0x13B)</span><span class="sxs-lookup"><span data-stu-id="31ee0-758">315 (0x13B)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-759">Il token che rappresenta i dati non è valido.</span><span class="sxs-lookup"><span data-stu-id="31ee0-759">The token representing the data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-760"><span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**funzionalità del dispositivo di errore \_ \_ \_ non \_ supportata**</span><span class="sxs-lookup"><span data-stu-id="31ee0-760"><span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**ERROR\_DEVICE\_FEATURE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-761">316 (0x13C)</span><span class="sxs-lookup"><span data-stu-id="31ee0-761">316 (0x13C)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-762">Il dispositivo non supporta la funzionalità comando.</span><span class="sxs-lookup"><span data-stu-id="31ee0-762">The device does not support the command feature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-763"><span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**ERRORE \_ il \_ Mid \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-763"><span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**ERROR\_MR\_MID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-764">317 (0x13D)</span><span class="sxs-lookup"><span data-stu-id="31ee0-764">317 (0x13D)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-765">Impossibile trovare il testo del messaggio per il numero di messaggio 0x %1 nel file di messaggio per %2.</span><span class="sxs-lookup"><span data-stu-id="31ee0-765">The system cannot find message text for message number 0x%1 in the message file for %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-766"><span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**\_ambito errore \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-766"><span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**ERROR\_SCOPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-767">318 (0x13E)</span><span class="sxs-lookup"><span data-stu-id="31ee0-767">318 (0x13E)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-768">L'ambito specificato non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-768">The scope specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-769"><span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**ERRORE \_ ambito non definito \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-769"><span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**ERROR\_UNDEFINED\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-770">319 (0x13F)</span><span class="sxs-lookup"><span data-stu-id="31ee0-770">319 (0x13F)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-771">Il criterio di accesso centrale specificato non è definito nel computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="31ee0-771">The Central Access Policy specified is not defined on the target machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-772"><span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**ERRORE \_ limite non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-772"><span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**ERROR\_INVALID\_CAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-773">320 (0x140)</span><span class="sxs-lookup"><span data-stu-id="31ee0-773">320 (0x140)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-774">I criteri di accesso centrale ottenuti da Active Directory non sono validi.</span><span class="sxs-lookup"><span data-stu-id="31ee0-774">The Central Access Policy obtained from Active Directory is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-775"><span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**ERRORE \_ dispositivo non \_ raggiungibile**</span><span class="sxs-lookup"><span data-stu-id="31ee0-775"><span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**ERROR\_DEVICE\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-776">321 (0x141)</span><span class="sxs-lookup"><span data-stu-id="31ee0-776">321 (0x141)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-777">Il dispositivo è irraggiungibile.</span><span class="sxs-lookup"><span data-stu-id="31ee0-777">The device is unreachable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-778"><span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**ERRORE \_ dispositivo \_ Nessuna \_ risorsa**</span><span class="sxs-lookup"><span data-stu-id="31ee0-778"><span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**ERROR\_DEVICE\_NO\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-779">322 (0x142)</span><span class="sxs-lookup"><span data-stu-id="31ee0-779">322 (0x142)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-780">Il dispositivo di destinazione non dispone di risorse sufficienti per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="31ee0-780">The target device has insufficient resources to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-781"><span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**errore di \_ checksum dei dati errore \_ \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-781"><span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**ERROR\_DATA\_CHECKSUM\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-782">323 (0x143)</span><span class="sxs-lookup"><span data-stu-id="31ee0-782">323 (0x143)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-783">Si è verificato un errore di checksum di integrità dei dati.</span><span class="sxs-lookup"><span data-stu-id="31ee0-783">A data integrity checksum error occurred.</span></span> <span data-ttu-id="31ee0-784">I dati nel flusso di file sono danneggiati.</span><span class="sxs-lookup"><span data-stu-id="31ee0-784">Data in the file stream is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-785"><span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**ERRORE \_ \_ \_ operazione EA kernel intermista \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-785"><span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**ERROR\_INTERMIXED\_KERNEL\_EA\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-786">324 (0x144)</span><span class="sxs-lookup"><span data-stu-id="31ee0-786">324 (0x144)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-787">È stato effettuato un tentativo di modificare un KERNEL e un attributo esteso normale (EA) nella stessa operazione.</span><span class="sxs-lookup"><span data-stu-id="31ee0-787">An attempt was made to modify both a KERNEL and normal Extended Attribute (EA) in the same operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-788"><span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**Trim a livello di file di errore \_ \_ \_ \_ non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-788"><span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**ERROR\_FILE\_LEVEL\_TRIM\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-789">326 (0x146)</span><span class="sxs-lookup"><span data-stu-id="31ee0-789">326 (0x146)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-790">Il dispositivo non supporta il TRIM a livello di file.</span><span class="sxs-lookup"><span data-stu-id="31ee0-790">Device does not support file-level TRIM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-791"><span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**\_violazione di \_ allineamento \_ offset errori**</span><span class="sxs-lookup"><span data-stu-id="31ee0-791"><span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**ERROR\_OFFSET\_ALIGNMENT\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-792">327 (0x147)</span><span class="sxs-lookup"><span data-stu-id="31ee0-792">327 (0x147)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-793">Il comando ha specificato un offset dei dati non allineato alla granularità/allineamento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="31ee0-793">The command specified a data offset that does not align to the device's granularity/alignment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-794"><span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**ERRORE \_ \_ nel campo \_ dell' \_ \_ elenco dei parametri**</span><span class="sxs-lookup"><span data-stu-id="31ee0-794"><span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**ERROR\_INVALID\_FIELD\_IN\_PARAMETER\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-795">328 (0x148)</span><span class="sxs-lookup"><span data-stu-id="31ee0-795">328 (0x148)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-796">Il comando ha specificato un campo non valido nell'elenco di parametri.</span><span class="sxs-lookup"><span data-stu-id="31ee0-796">The command specified an invalid field in its parameter list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-797"><span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**\_operazione \_ di errore in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="31ee0-797"><span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**ERROR\_OPERATION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-798">329 (0x149)</span><span class="sxs-lookup"><span data-stu-id="31ee0-798">329 (0x149)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-799">È attualmente in corso un'operazione con il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="31ee0-799">An operation is currently in progress with the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-800"><span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**ERRORE \_ nel \_ percorso del dispositivo errato \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-800"><span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**ERROR\_BAD\_DEVICE\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-801">330 (0x14A)</span><span class="sxs-lookup"><span data-stu-id="31ee0-801">330 (0x14A)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-802">È stato effettuato un tentativo di inviare il comando tramite un percorso non valido al dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="31ee0-802">An attempt was made to send down the command via an invalid path to the target device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-803"><span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**ERRORE di un \_ numero eccessivo di \_ \_ descrittori**</span><span class="sxs-lookup"><span data-stu-id="31ee0-803"><span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**ERROR\_TOO\_MANY\_DESCRIPTORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-804">331 (0x14B)</span><span class="sxs-lookup"><span data-stu-id="31ee0-804">331 (0x14B)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-805">Il comando ha specificato un numero di descrittori che hanno superato il valore massimo supportato dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="31ee0-805">The command specified a number of descriptors that exceeded the maximum supported by the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-806"><span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**ERRORE di \_ pulizia \_ dati \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-806"><span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**ERROR\_SCRUB\_DATA\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-807">332 (0x14C)</span><span class="sxs-lookup"><span data-stu-id="31ee0-807">332 (0x14C)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-808">Lo scrub è disabilitato nel file specificato.</span><span class="sxs-lookup"><span data-stu-id="31ee0-808">Scrub is disabled on the specified file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-809"><span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**ERRORE \_ di \_ archiviazione non ridondante \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-809"><span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**ERROR\_NOT\_REDUNDANT\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-810">333 (0x14D)</span><span class="sxs-lookup"><span data-stu-id="31ee0-810">333 (0x14D)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-811">Il dispositivo di archiviazione non fornisce ridondanza.</span><span class="sxs-lookup"><span data-stu-id="31ee0-811">The storage device does not provide redundancy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-812"><span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**il \_ file residente di errore \_ \_ non è \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-812"><span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**ERROR\_RESIDENT\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-813">334 (0x14E)</span><span class="sxs-lookup"><span data-stu-id="31ee0-813">334 (0x14E)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-814">Un'operazione non è supportata in un file residente.</span><span class="sxs-lookup"><span data-stu-id="31ee0-814">An operation is not supported on a resident file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-815"><span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**ERRORE \_ \_ file compresso \_ non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="31ee0-815"><span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**ERROR\_COMPRESSED\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-816">335 (0x14F)</span><span class="sxs-lookup"><span data-stu-id="31ee0-816">335 (0x14F)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-817">Un'operazione non è supportata in un file compresso.</span><span class="sxs-lookup"><span data-stu-id="31ee0-817">An operation is not supported on a compressed file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-818"><span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**Directory degli errori \_ \_ non \_ supportata**</span><span class="sxs-lookup"><span data-stu-id="31ee0-818"><span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**ERROR\_DIRECTORY\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-819">336 (0x150)</span><span class="sxs-lookup"><span data-stu-id="31ee0-819">336 (0x150)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-820">Un'operazione non è supportata in una directory.</span><span class="sxs-lookup"><span data-stu-id="31ee0-820">An operation is not supported on a directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-821"><span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**ERRORE \_ \_ di lettura \_ dalla \_ copia**</span><span class="sxs-lookup"><span data-stu-id="31ee0-821"><span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**ERROR\_NOT\_READ\_FROM\_COPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-822">337 (0x151)</span><span class="sxs-lookup"><span data-stu-id="31ee0-822">337 (0x151)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-823">Impossibile leggere la copia specificata dei dati richiesti.</span><span class="sxs-lookup"><span data-stu-id="31ee0-823">The specified copy of the requested data could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-824"><span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**errore durante il \_ \_ riavvio di NoAction \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-824"><span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**ERROR\_FAIL\_NOACTION\_REBOOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-825">350 (0x15E)</span><span class="sxs-lookup"><span data-stu-id="31ee0-825">350 (0x15E)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-826">Non è stata eseguita alcuna azione perché è necessario riavviare il sistema.</span><span class="sxs-lookup"><span data-stu-id="31ee0-826">No action was taken as a system reboot is required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-827"><span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**ERRORE \_ di \_ arresto**</span><span class="sxs-lookup"><span data-stu-id="31ee0-827"><span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**ERROR\_FAIL\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-828">351 (0x15F)</span><span class="sxs-lookup"><span data-stu-id="31ee0-828">351 (0x15F)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-829">L'operazione di arresto non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="31ee0-829">The shutdown operation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-830"><span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**errore durante il \_ \_ riavvio**</span><span class="sxs-lookup"><span data-stu-id="31ee0-830"><span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**ERROR\_FAIL\_RESTART**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-831">352 (0x160)</span><span class="sxs-lookup"><span data-stu-id="31ee0-831">352 (0x160)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-832">Operazione di riavvio non riuscita.</span><span class="sxs-lookup"><span data-stu-id="31ee0-832">The restart operation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-833"><span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**\_numero massimo di sessioni di errore \_ \_ raggiunto**</span><span class="sxs-lookup"><span data-stu-id="31ee0-833"><span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**ERROR\_MAX\_SESSIONS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-834">353 (0x161)</span><span class="sxs-lookup"><span data-stu-id="31ee0-834">353 (0x161)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-835">È stato raggiunto il numero massimo di sessioni.</span><span class="sxs-lookup"><span data-stu-id="31ee0-835">The maximum number of sessions has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-836"><span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**\_modalità thread di errore \_ già in \_ \_ background**</span><span class="sxs-lookup"><span data-stu-id="31ee0-836"><span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**ERROR\_THREAD\_MODE\_ALREADY\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-837">400 (0x190)</span><span class="sxs-lookup"><span data-stu-id="31ee0-837">400 (0x190)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-838">Il thread è già in modalità di elaborazione in background.</span><span class="sxs-lookup"><span data-stu-id="31ee0-838">The thread is already in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-839"><span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**\_modalità thread di errore \_ non in \_ \_ background**</span><span class="sxs-lookup"><span data-stu-id="31ee0-839"><span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**ERROR\_THREAD\_MODE\_NOT\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-840">401 (0x191)</span><span class="sxs-lookup"><span data-stu-id="31ee0-840">401 (0x191)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-841">Il thread non è in modalità di elaborazione in background.</span><span class="sxs-lookup"><span data-stu-id="31ee0-841">The thread is not in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-842"><span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**modalità di elaborazione degli errori \_ \_ già in \_ \_ background**</span><span class="sxs-lookup"><span data-stu-id="31ee0-842"><span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**ERROR\_PROCESS\_MODE\_ALREADY\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-843">402 (0x192)</span><span class="sxs-lookup"><span data-stu-id="31ee0-843">402 (0x192)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-844">Il processo è già in modalità di elaborazione in background.</span><span class="sxs-lookup"><span data-stu-id="31ee0-844">The process is already in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-845"><span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**\_modalità elaborazione \_ errori \_ non in \_ background**</span><span class="sxs-lookup"><span data-stu-id="31ee0-845"><span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**ERROR\_PROCESS\_MODE\_NOT\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-846">403 (0x193)</span><span class="sxs-lookup"><span data-stu-id="31ee0-846">403 (0x193)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-847">Il processo non è in modalità di elaborazione in background.</span><span class="sxs-lookup"><span data-stu-id="31ee0-847">The process is not in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="31ee0-848"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERRORE \_ indirizzo non valido \_**</span><span class="sxs-lookup"><span data-stu-id="31ee0-848"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR\_INVALID\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="31ee0-849">487 (0x1E7)</span><span class="sxs-lookup"><span data-stu-id="31ee0-849">487 (0x1E7)</span></span>
</dt> <dt>



<span data-ttu-id="31ee0-850">Tentativo di accedere a un indirizzo non valido.</span><span class="sxs-lookup"><span data-stu-id="31ee0-850">Attempt to access invalid address.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="31ee0-851">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31ee0-851">Requirements</span></span>



| <span data-ttu-id="31ee0-852">Requisito</span><span class="sxs-lookup"><span data-stu-id="31ee0-852">Requirement</span></span> | <span data-ttu-id="31ee0-853">Valore</span><span class="sxs-lookup"><span data-stu-id="31ee0-853">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31ee0-854">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31ee0-854">Minimum supported client</span></span><br/> | <span data-ttu-id="31ee0-855">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="31ee0-855">Windows XP \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="31ee0-856">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31ee0-856">Minimum supported server</span></span><br/> | <span data-ttu-id="31ee0-857">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="31ee0-857">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="31ee0-858">Intestazione</span><span class="sxs-lookup"><span data-stu-id="31ee0-858">Header</span></span><br/>                   | <dl> <span data-ttu-id="31ee0-859"><dt>WinError. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31ee0-859"><dt>WinError.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31ee0-860">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31ee0-860">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31ee0-861">Codici di errore di sistema</span><span class="sxs-lookup"><span data-stu-id="31ee0-861">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




