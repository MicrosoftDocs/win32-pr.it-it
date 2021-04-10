---
description: Descrive i codici di errore 500-999 definiti nel file di intestazione WinError. h ed è destinato agli sviluppatori.
ms.assetid: 8d8b427b-b761-4023-a834-a6eff96d6ba1
title: Codici di errore di sistema (500-999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 02b35374fcb68f9b416948d5e39b2182f573b60f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225719"
---
# <a name="system-error-codes-500-999"></a><span data-ttu-id="97216-103">Codici di errore di sistema (500-999)</span><span class="sxs-lookup"><span data-stu-id="97216-103">System Error Codes (500-999)</span></span>

> [!NOTE]
> <span data-ttu-id="97216-104">Queste informazioni sono destinate agli sviluppatori che effettuano il debug degli errori di sistema.</span><span class="sxs-lookup"><span data-stu-id="97216-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="97216-105">Per altri errori, ad esempio problemi con Windows Update, è disponibile un elenco di risorse nella pagina [codici di errore](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="97216-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="97216-106">Nell'elenco seguente vengono descritti i [codici di errore di sistema](system-error-codes.md) (errori da 500 a 999).</span><span class="sxs-lookup"><span data-stu-id="97216-106">The following list describes [system error codes](system-error-codes.md) (errors 500 to 999).</span></span> <span data-ttu-id="97216-107">Vengono restituiti dalla funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo.</span><span class="sxs-lookup"><span data-stu-id="97216-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="97216-108">Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la funzione [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il **formato \_ Message from flag \_ di \_ sistema** .</span><span class="sxs-lookup"><span data-stu-id="97216-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="97216-109"><span id="ERROR_USER_PROFILE_LOAD"></span><span id="error_user_profile_load"></span>**errore \_ durante \_ il caricamento del profilo utente \_**</span><span class="sxs-lookup"><span data-stu-id="97216-109"><span id="ERROR_USER_PROFILE_LOAD"></span><span id="error_user_profile_load"></span>**ERROR\_USER\_PROFILE\_LOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-110">500 (0x1F4)</span><span class="sxs-lookup"><span data-stu-id="97216-110">500 (0x1F4)</span></span>
</dt> <dt>



<span data-ttu-id="97216-111">Non è possibile caricare il profilo utente.</span><span class="sxs-lookup"><span data-stu-id="97216-111">User profile cannot be loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-112"><span id="ERROR_ARITHMETIC_OVERFLOW"></span><span id="error_arithmetic_overflow"></span>**ERRORE \_ di \_ overflow aritmetico**</span><span class="sxs-lookup"><span data-stu-id="97216-112"><span id="ERROR_ARITHMETIC_OVERFLOW"></span><span id="error_arithmetic_overflow"></span>**ERROR\_ARITHMETIC\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-113">534 (0x216)</span><span class="sxs-lookup"><span data-stu-id="97216-113">534 (0x216)</span></span>
</dt> <dt>



<span data-ttu-id="97216-114">Il risultato aritmetico ha superato 32 bit.</span><span class="sxs-lookup"><span data-stu-id="97216-114">Arithmetic result exceeded 32 bits.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-115"><span id="ERROR_PIPE_CONNECTED"></span><span id="error_pipe_connected"></span>**PIPE di errore \_ \_ connessa**</span><span class="sxs-lookup"><span data-stu-id="97216-115"><span id="ERROR_PIPE_CONNECTED"></span><span id="error_pipe_connected"></span>**ERROR\_PIPE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-116">535 (0x217)</span><span class="sxs-lookup"><span data-stu-id="97216-116">535 (0x217)</span></span>
</dt> <dt>



<span data-ttu-id="97216-117">È presente un processo sull'altra estremità della pipe.</span><span class="sxs-lookup"><span data-stu-id="97216-117">There is a process on other end of the pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-118"><span id="ERROR_PIPE_LISTENING"></span><span id="error_pipe_listening"></span>**\_ascolto pipe di errore \_**</span><span class="sxs-lookup"><span data-stu-id="97216-118"><span id="ERROR_PIPE_LISTENING"></span><span id="error_pipe_listening"></span>**ERROR\_PIPE\_LISTENING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-119">536 (0x218)</span><span class="sxs-lookup"><span data-stu-id="97216-119">536 (0x218)</span></span>
</dt> <dt>



<span data-ttu-id="97216-120">In attesa che un processo apra l'altra estremità della pipe.</span><span class="sxs-lookup"><span data-stu-id="97216-120">Waiting for a process to open the other end of the pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-121"><span id="ERROR_VERIFIER_STOP"></span><span id="error_verifier_stop"></span>**arresto di errore \_ Verifier \_**</span><span class="sxs-lookup"><span data-stu-id="97216-121"><span id="ERROR_VERIFIER_STOP"></span><span id="error_verifier_stop"></span>**ERROR\_VERIFIER\_STOP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-122">537 (0x219)</span><span class="sxs-lookup"><span data-stu-id="97216-122">537 (0x219)</span></span>
</dt> <dt>



<span data-ttu-id="97216-123">Application Verifier ha rilevato un errore nel processo corrente.</span><span class="sxs-lookup"><span data-stu-id="97216-123">Application verifier has found an error in the current process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-124"><span id="ERROR_ABIOS_ERROR"></span><span id="error_abios_error"></span>**errore \_ ABIOS \_ errore**</span><span class="sxs-lookup"><span data-stu-id="97216-124"><span id="ERROR_ABIOS_ERROR"></span><span id="error_abios_error"></span>**ERROR\_ABIOS\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-125">538 (0x21A)</span><span class="sxs-lookup"><span data-stu-id="97216-125">538 (0x21A)</span></span>
</dt> <dt>



<span data-ttu-id="97216-126">Si è verificato un errore nel sottosistema ABIOS.</span><span class="sxs-lookup"><span data-stu-id="97216-126">An error occurred in the ABIOS subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-127"><span id="ERROR_WX86_WARNING"></span><span id="error_wx86_warning"></span>**ERRORE \_ WX86 \_ avviso**</span><span class="sxs-lookup"><span data-stu-id="97216-127"><span id="ERROR_WX86_WARNING"></span><span id="error_wx86_warning"></span>**ERROR\_WX86\_WARNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-128">539 (0x21B)</span><span class="sxs-lookup"><span data-stu-id="97216-128">539 (0x21B)</span></span>
</dt> <dt>



<span data-ttu-id="97216-129">Si è verificato un avviso nel sottosistema WX86.</span><span class="sxs-lookup"><span data-stu-id="97216-129">A warning occurred in the WX86 subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-130"><span id="ERROR_WX86_ERROR"></span><span id="error_wx86_error"></span>**Errore \_ WX86 \_ errore**</span><span class="sxs-lookup"><span data-stu-id="97216-130"><span id="ERROR_WX86_ERROR"></span><span id="error_wx86_error"></span>**ERROR\_WX86\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-131">540 (0x21C)</span><span class="sxs-lookup"><span data-stu-id="97216-131">540 (0x21C)</span></span>
</dt> <dt>



<span data-ttu-id="97216-132">Si è verificato un errore nel sottosistema WX86.</span><span class="sxs-lookup"><span data-stu-id="97216-132">An error occurred in the WX86 subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-133"><span id="ERROR_TIMER_NOT_CANCELED"></span><span id="error_timer_not_canceled"></span>**TIMER di errore \_ \_ non \_ annullato**</span><span class="sxs-lookup"><span data-stu-id="97216-133"><span id="ERROR_TIMER_NOT_CANCELED"></span><span id="error_timer_not_canceled"></span>**ERROR\_TIMER\_NOT\_CANCELED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-134">541 (0x21D)</span><span class="sxs-lookup"><span data-stu-id="97216-134">541 (0x21D)</span></span>
</dt> <dt>



<span data-ttu-id="97216-135">È stato effettuato un tentativo di annullare o impostare un timer con un APC associato e il thread oggetto non è il thread che ha originariamente impostato il timer con una routine APC associata.</span><span class="sxs-lookup"><span data-stu-id="97216-135">An attempt was made to cancel or set a timer that has an associated APC and the subject thread is not the thread that originally set the timer with an associated APC routine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-136"><span id="ERROR_UNWIND"></span><span id="error_unwind"></span>**\_rimozione errore**</span><span class="sxs-lookup"><span data-stu-id="97216-136"><span id="ERROR_UNWIND"></span><span id="error_unwind"></span>**ERROR\_UNWIND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-137">542 (0x21E)</span><span class="sxs-lookup"><span data-stu-id="97216-137">542 (0x21E)</span></span>
</dt> <dt>



<span data-ttu-id="97216-138">Codice eccezione di rimozione.</span><span class="sxs-lookup"><span data-stu-id="97216-138">Unwind exception code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-139"><span id="ERROR_BAD_STACK"></span><span id="error_bad_stack"></span>**ERRORE \_ \_ stack errato**</span><span class="sxs-lookup"><span data-stu-id="97216-139"><span id="ERROR_BAD_STACK"></span><span id="error_bad_stack"></span>**ERROR\_BAD\_STACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-140">543 (0x21F)</span><span class="sxs-lookup"><span data-stu-id="97216-140">543 (0x21F)</span></span>
</dt> <dt>



<span data-ttu-id="97216-141">È stato rilevato uno stack non valido o non allineato durante un'operazione di rimozione.</span><span class="sxs-lookup"><span data-stu-id="97216-141">An invalid or unaligned stack was encountered during an unwind operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-142"><span id="ERROR_INVALID_UNWIND_TARGET"></span><span id="error_invalid_unwind_target"></span>**ERRORE \_ destinazione di rimozione non valida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="97216-142"><span id="ERROR_INVALID_UNWIND_TARGET"></span><span id="error_invalid_unwind_target"></span>**ERROR\_INVALID\_UNWIND\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-143">544 (0x220)</span><span class="sxs-lookup"><span data-stu-id="97216-143">544 (0x220)</span></span>
</dt> <dt>



<span data-ttu-id="97216-144">È stata rilevata una destinazione di rimozione non valida durante un'operazione di rimozione.</span><span class="sxs-lookup"><span data-stu-id="97216-144">An invalid unwind target was encountered during an unwind operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-145"><span id="ERROR_INVALID_PORT_ATTRIBUTES"></span><span id="error_invalid_port_attributes"></span>**ERRORE \_ \_ attributi porta non validi \_**</span><span class="sxs-lookup"><span data-stu-id="97216-145"><span id="ERROR_INVALID_PORT_ATTRIBUTES"></span><span id="error_invalid_port_attributes"></span>**ERROR\_INVALID\_PORT\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-146">545 (0x221)</span><span class="sxs-lookup"><span data-stu-id="97216-146">545 (0x221)</span></span>
</dt> <dt>



<span data-ttu-id="97216-147">Attributi di oggetto non validi specificati per NtCreatePort o attributi di porta non validi specificati in NtConnectPort</span><span class="sxs-lookup"><span data-stu-id="97216-147">Invalid Object Attributes specified to NtCreatePort or invalid Port Attributes specified to NtConnectPort</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-148"><span id="ERROR_PORT_MESSAGE_TOO_LONG"></span><span id="error_port_message_too_long"></span>**messaggio della porta di errore \_ \_ \_ troppo \_ lungo**</span><span class="sxs-lookup"><span data-stu-id="97216-148"><span id="ERROR_PORT_MESSAGE_TOO_LONG"></span><span id="error_port_message_too_long"></span>**ERROR\_PORT\_MESSAGE\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-149">546 (0x222)</span><span class="sxs-lookup"><span data-stu-id="97216-149">546 (0x222)</span></span>
</dt> <dt>



<span data-ttu-id="97216-150">La lunghezza del messaggio passato a NtRequestPort o NtRequestWaitReplyPort è più lunga del messaggio massimo consentito dalla porta.</span><span class="sxs-lookup"><span data-stu-id="97216-150">Length of message passed to NtRequestPort or NtRequestWaitReplyPort was longer than the maximum message allowed by the port.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-151"><span id="ERROR_INVALID_QUOTA_LOWER"></span><span id="error_invalid_quota_lower"></span>**ERRORE \_ di \_ quota \_ inferiore non valida**</span><span class="sxs-lookup"><span data-stu-id="97216-151"><span id="ERROR_INVALID_QUOTA_LOWER"></span><span id="error_invalid_quota_lower"></span>**ERROR\_INVALID\_QUOTA\_LOWER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-152">547 (0x223)</span><span class="sxs-lookup"><span data-stu-id="97216-152">547 (0x223)</span></span>
</dt> <dt>



<span data-ttu-id="97216-153">È stato effettuato un tentativo di abbassare un limite di quota al di sotto dell'utilizzo corrente.</span><span class="sxs-lookup"><span data-stu-id="97216-153">An attempt was made to lower a quota limit below the current usage.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-154"><span id="ERROR_DEVICE_ALREADY_ATTACHED"></span><span id="error_device_already_attached"></span>**dispositivo di errore \_ \_ già \_ collegato**</span><span class="sxs-lookup"><span data-stu-id="97216-154"><span id="ERROR_DEVICE_ALREADY_ATTACHED"></span><span id="error_device_already_attached"></span>**ERROR\_DEVICE\_ALREADY\_ATTACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-155">548 (0x224)</span><span class="sxs-lookup"><span data-stu-id="97216-155">548 (0x224)</span></span>
</dt> <dt>



<span data-ttu-id="97216-156">È stato effettuato un tentativo di connessione a un dispositivo già collegato a un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="97216-156">An attempt was made to attach to a device that was already attached to another device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-157"><span id="ERROR_INSTRUCTION_MISALIGNMENT"></span><span id="error_instruction_misalignment"></span>**ERRORE \_ di \_ allineamento delle istruzioni**</span><span class="sxs-lookup"><span data-stu-id="97216-157"><span id="ERROR_INSTRUCTION_MISALIGNMENT"></span><span id="error_instruction_misalignment"></span>**ERROR\_INSTRUCTION\_MISALIGNMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-158">549 (0x225)</span><span class="sxs-lookup"><span data-stu-id="97216-158">549 (0x225)</span></span>
</dt> <dt>



<span data-ttu-id="97216-159">È stato effettuato un tentativo di eseguire un'istruzione in un indirizzo non allineato e il sistema host non supporta riferimenti a istruzioni non allineate.</span><span class="sxs-lookup"><span data-stu-id="97216-159">An attempt was made to execute an instruction at an unaligned address and the host system does not support unaligned instruction references.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-160"><span id="ERROR_PROFILING_NOT_STARTED"></span><span id="error_profiling_not_started"></span>**ERRORE di \_ PROfilatura \_ non \_ avviato**</span><span class="sxs-lookup"><span data-stu-id="97216-160"><span id="ERROR_PROFILING_NOT_STARTED"></span><span id="error_profiling_not_started"></span>**ERROR\_PROFILING\_NOT\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-161">550 (0x226)</span><span class="sxs-lookup"><span data-stu-id="97216-161">550 (0x226)</span></span>
</dt> <dt>



<span data-ttu-id="97216-162">Profilatura non avviata.</span><span class="sxs-lookup"><span data-stu-id="97216-162">Profiling not started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-163"><span id="ERROR_PROFILING_NOT_STOPPED"></span><span id="error_profiling_not_stopped"></span>**ERRORE di \_ PROfilatura \_ non \_ arrestato**</span><span class="sxs-lookup"><span data-stu-id="97216-163"><span id="ERROR_PROFILING_NOT_STOPPED"></span><span id="error_profiling_not_stopped"></span>**ERROR\_PROFILING\_NOT\_STOPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-164">551 (0x227)</span><span class="sxs-lookup"><span data-stu-id="97216-164">551 (0x227)</span></span>
</dt> <dt>



<span data-ttu-id="97216-165">Profilatura non arrestata.</span><span class="sxs-lookup"><span data-stu-id="97216-165">Profiling not stopped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-166"><span id="ERROR_COULD_NOT_INTERPRET"></span><span id="error_could_not_interpret"></span>**\_Impossibile \_ \_ INTERPRETAre l'errore**</span><span class="sxs-lookup"><span data-stu-id="97216-166"><span id="ERROR_COULD_NOT_INTERPRET"></span><span id="error_could_not_interpret"></span>**ERROR\_COULD\_NOT\_INTERPRET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-167">552 (0x228)</span><span class="sxs-lookup"><span data-stu-id="97216-167">552 (0x228)</span></span>
</dt> <dt>



<span data-ttu-id="97216-168">L'ACL passato non contiene le informazioni minime necessarie.</span><span class="sxs-lookup"><span data-stu-id="97216-168">The passed ACL did not contain the minimum required information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-169"><span id="ERROR_PROFILING_AT_LIMIT"></span><span id="error_profiling_at_limit"></span>**ERRORE \_ di PROfilatura \_ al \_ limite**</span><span class="sxs-lookup"><span data-stu-id="97216-169"><span id="ERROR_PROFILING_AT_LIMIT"></span><span id="error_profiling_at_limit"></span>**ERROR\_PROFILING\_AT\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-170">553 (0x229)</span><span class="sxs-lookup"><span data-stu-id="97216-170">553 (0x229)</span></span>
</dt> <dt>



<span data-ttu-id="97216-171">Il numero di oggetti di profilatura attivi è massimo e non può essere avviato.</span><span class="sxs-lookup"><span data-stu-id="97216-171">The number of active profiling objects is at the maximum and no more may be started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-172"><span id="ERROR_CANT_WAIT"></span><span id="error_cant_wait"></span>**ERRORE \_ di \_ attesa del cant**</span><span class="sxs-lookup"><span data-stu-id="97216-172"><span id="ERROR_CANT_WAIT"></span><span id="error_cant_wait"></span>**ERROR\_CANT\_WAIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-173">554 (0x22A)</span><span class="sxs-lookup"><span data-stu-id="97216-173">554 (0x22A)</span></span>
</dt> <dt>



<span data-ttu-id="97216-174">Utilizzato per indicare che un'operazione non può continuare senza blocco per I/O.</span><span class="sxs-lookup"><span data-stu-id="97216-174">Used to indicate that an operation cannot continue without blocking for I/O.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-175"><span id="ERROR_CANT_TERMINATE_SELF"></span><span id="error_cant_terminate_self"></span>**ERRORE \_ di \_ terminazione \_ automatica**</span><span class="sxs-lookup"><span data-stu-id="97216-175"><span id="ERROR_CANT_TERMINATE_SELF"></span><span id="error_cant_terminate_self"></span>**ERROR\_CANT\_TERMINATE\_SELF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-176">555 (0x22B)</span><span class="sxs-lookup"><span data-stu-id="97216-176">555 (0x22B)</span></span>
</dt> <dt>



<span data-ttu-id="97216-177">Indica che un thread ha tentato di terminare se stesso per impostazione predefinita (denominato NtTerminateThread con **null**) ed è l'ultimo thread del processo corrente.</span><span class="sxs-lookup"><span data-stu-id="97216-177">Indicates that a thread attempted to terminate itself by default (called NtTerminateThread with **NULL**) and it was the last thread in the current process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-178"><span id="ERROR_UNEXPECTED_MM_CREATE_ERR"></span><span id="error_unexpected_mm_create_err"></span>**ERRORE \_ imprevisto di \_ \_ creazione \_ Err**</span><span class="sxs-lookup"><span data-stu-id="97216-178"><span id="ERROR_UNEXPECTED_MM_CREATE_ERR"></span><span id="error_unexpected_mm_create_err"></span>**ERROR\_UNEXPECTED\_MM\_CREATE\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-179">556 (0x22C)</span><span class="sxs-lookup"><span data-stu-id="97216-179">556 (0x22C)</span></span>
</dt> <dt>



<span data-ttu-id="97216-180">Se viene restituito un errore MM che non è definito nel filtro FsRtl standard, viene convertito in uno degli errori seguenti, che è sicuramente presente nel filtro.</span><span class="sxs-lookup"><span data-stu-id="97216-180">If an MM error is returned which is not defined in the standard FsRtl filter, it is converted to one of the following errors which is guaranteed to be in the filter.</span></span> <span data-ttu-id="97216-181">In questo caso, le informazioni vengono perse, tuttavia, il filtro gestisce correttamente l'eccezione.</span><span class="sxs-lookup"><span data-stu-id="97216-181">In this case information is lost, however, the filter correctly handles the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-182"><span id="ERROR_UNEXPECTED_MM_MAP_ERROR"></span><span id="error_unexpected_mm_map_error"></span>**errore \_ di \_ \_ mappa mm imprevisto \_**</span><span class="sxs-lookup"><span data-stu-id="97216-182"><span id="ERROR_UNEXPECTED_MM_MAP_ERROR"></span><span id="error_unexpected_mm_map_error"></span>**ERROR\_UNEXPECTED\_MM\_MAP\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-183">557 (0x22D)</span><span class="sxs-lookup"><span data-stu-id="97216-183">557 (0x22D)</span></span>
</dt> <dt>



<span data-ttu-id="97216-184">Se viene restituito un errore MM che non è definito nel filtro FsRtl standard, viene convertito in uno degli errori seguenti, che è sicuramente presente nel filtro.</span><span class="sxs-lookup"><span data-stu-id="97216-184">If an MM error is returned which is not defined in the standard FsRtl filter, it is converted to one of the following errors which is guaranteed to be in the filter.</span></span> <span data-ttu-id="97216-185">In questo caso, le informazioni vengono perse, tuttavia, il filtro gestisce correttamente l'eccezione.</span><span class="sxs-lookup"><span data-stu-id="97216-185">In this case information is lost, however, the filter correctly handles the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-186"><span id="ERROR_UNEXPECTED_MM_EXTEND_ERR"></span><span id="error_unexpected_mm_extend_err"></span>**ERRORE \_ imprevisto \_ mm \_ extend \_ Err**</span><span class="sxs-lookup"><span data-stu-id="97216-186"><span id="ERROR_UNEXPECTED_MM_EXTEND_ERR"></span><span id="error_unexpected_mm_extend_err"></span>**ERROR\_UNEXPECTED\_MM\_EXTEND\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-187">558 (0x22E)</span><span class="sxs-lookup"><span data-stu-id="97216-187">558 (0x22E)</span></span>
</dt> <dt>



<span data-ttu-id="97216-188">Se viene restituito un errore MM che non è definito nel filtro FsRtl standard, viene convertito in uno degli errori seguenti, che è sicuramente presente nel filtro.</span><span class="sxs-lookup"><span data-stu-id="97216-188">If an MM error is returned which is not defined in the standard FsRtl filter, it is converted to one of the following errors which is guaranteed to be in the filter.</span></span> <span data-ttu-id="97216-189">In questo caso, le informazioni vengono perse, tuttavia, il filtro gestisce correttamente l'eccezione.</span><span class="sxs-lookup"><span data-stu-id="97216-189">In this case information is lost, however, the filter correctly handles the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-190"><span id="ERROR_BAD_FUNCTION_TABLE"></span><span id="error_bad_function_table"></span>**\_tabella delle \_ funzioni ERRAta Error \_**</span><span class="sxs-lookup"><span data-stu-id="97216-190"><span id="ERROR_BAD_FUNCTION_TABLE"></span><span id="error_bad_function_table"></span>**ERROR\_BAD\_FUNCTION\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-191">559 (0x22F)</span><span class="sxs-lookup"><span data-stu-id="97216-191">559 (0x22F)</span></span>
</dt> <dt>



<span data-ttu-id="97216-192">È stata rilevata una tabella di funzioni in formato non corretto durante un'operazione di rimozione.</span><span class="sxs-lookup"><span data-stu-id="97216-192">A malformed function table was encountered during an unwind operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-193"><span id="ERROR_NO_GUID_TRANSLATION"></span><span id="error_no_guid_translation"></span>**ERRORE \_ senza \_ \_ conversione GUID**</span><span class="sxs-lookup"><span data-stu-id="97216-193"><span id="ERROR_NO_GUID_TRANSLATION"></span><span id="error_no_guid_translation"></span>**ERROR\_NO\_GUID\_TRANSLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-194">560 (0x230)</span><span class="sxs-lookup"><span data-stu-id="97216-194">560 (0x230)</span></span>
</dt> <dt>



<span data-ttu-id="97216-195">Indica che è stato effettuato un tentativo di assegnare la protezione a un file o a una directory file system e che uno dei SID del descrittore di sicurezza non può essere convertito in un GUID che può essere archiviato dall'file system.</span><span class="sxs-lookup"><span data-stu-id="97216-195">Indicates that an attempt was made to assign protection to a file system file or directory and one of the SIDs in the security descriptor could not be translated into a GUID that could be stored by the file system.</span></span> <span data-ttu-id="97216-196">In questo modo, il tentativo di protezione non riesce, che può causare un tentativo di creazione di file non riuscito.</span><span class="sxs-lookup"><span data-stu-id="97216-196">This causes the protection attempt to fail, which may cause a file creation attempt to fail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-197"><span id="ERROR_INVALID_LDT_SIZE"></span><span id="error_invalid_ldt_size"></span>**ERRORE \_ \_ dimensioni LDT non valide \_**</span><span class="sxs-lookup"><span data-stu-id="97216-197"><span id="ERROR_INVALID_LDT_SIZE"></span><span id="error_invalid_ldt_size"></span>**ERROR\_INVALID\_LDT\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-198">561 (0x231)</span><span class="sxs-lookup"><span data-stu-id="97216-198">561 (0x231)</span></span>
</dt> <dt>



<span data-ttu-id="97216-199">Indica che è stato effettuato un tentativo di espandere un LDT impostando le relative dimensioni o che la dimensione non era un numero pari di selettori.</span><span class="sxs-lookup"><span data-stu-id="97216-199">Indicates that an attempt was made to grow an LDT by setting its size, or that the size was not an even number of selectors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-200"><span id="ERROR_INVALID_LDT_OFFSET"></span><span id="error_invalid_ldt_offset"></span>**ERRORE \_ di \_ offset LDT non valido \_**</span><span class="sxs-lookup"><span data-stu-id="97216-200"><span id="ERROR_INVALID_LDT_OFFSET"></span><span id="error_invalid_ldt_offset"></span>**ERROR\_INVALID\_LDT\_OFFSET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-201">563 (0x233)</span><span class="sxs-lookup"><span data-stu-id="97216-201">563 (0x233)</span></span>
</dt> <dt>



<span data-ttu-id="97216-202">Indica che il valore iniziale delle informazioni LDT non è un multiplo integrale della dimensione del selettore.</span><span class="sxs-lookup"><span data-stu-id="97216-202">Indicates that the starting value for the LDT information was not an integral multiple of the selector size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-203"><span id="ERROR_INVALID_LDT_DESCRIPTOR"></span><span id="error_invalid_ldt_descriptor"></span>**ERRORE \_ \_ \_ descrittore LDT non valido**</span><span class="sxs-lookup"><span data-stu-id="97216-203"><span id="ERROR_INVALID_LDT_DESCRIPTOR"></span><span id="error_invalid_ldt_descriptor"></span>**ERROR\_INVALID\_LDT\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-204">564 (0x234)</span><span class="sxs-lookup"><span data-stu-id="97216-204">564 (0x234)</span></span>
</dt> <dt>



<span data-ttu-id="97216-205">Indica che l'utente ha fornito un descrittore non valido durante il tentativo di impostare i descrittori LDT.</span><span class="sxs-lookup"><span data-stu-id="97216-205">Indicates that the user supplied an invalid descriptor when trying to set up Ldt descriptors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-206"><span id="ERROR_TOO_MANY_THREADS"></span><span id="error_too_many_threads"></span>**ERRORE di un \_ numero eccessivo di \_ \_ thread**</span><span class="sxs-lookup"><span data-stu-id="97216-206"><span id="ERROR_TOO_MANY_THREADS"></span><span id="error_too_many_threads"></span>**ERROR\_TOO\_MANY\_THREADS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-207">565 (0x235)</span><span class="sxs-lookup"><span data-stu-id="97216-207">565 (0x235)</span></span>
</dt> <dt>



<span data-ttu-id="97216-208">Indica che un processo dispone di un numero eccessivo di thread per eseguire l'azione richiesta.</span><span class="sxs-lookup"><span data-stu-id="97216-208">Indicates a process has too many threads to perform the requested action.</span></span> <span data-ttu-id="97216-209">Ad esempio, l'assegnazione di un token primario può essere eseguita solo quando un processo ha zero o un thread.</span><span class="sxs-lookup"><span data-stu-id="97216-209">For example, assignment of a primary token may only be performed when a process has zero or one threads.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-210"><span id="ERROR_THREAD_NOT_IN_PROCESS"></span><span id="error_thread_not_in_process"></span>**\_thread \_ di errore non \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="97216-210"><span id="ERROR_THREAD_NOT_IN_PROCESS"></span><span id="error_thread_not_in_process"></span>**ERROR\_THREAD\_NOT\_IN\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-211">566 (0x236)</span><span class="sxs-lookup"><span data-stu-id="97216-211">566 (0x236)</span></span>
</dt> <dt>



<span data-ttu-id="97216-212">È stato effettuato un tentativo di operare su un thread all'interno di un processo specifico, ma il thread specificato non è nel processo specificato.</span><span class="sxs-lookup"><span data-stu-id="97216-212">An attempt was made to operate on a thread within a specific process, but the thread specified is not in the process specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-213"><span id="ERROR_PAGEFILE_QUOTA_EXCEEDED"></span><span id="error_pagefile_quota_exceeded"></span>**QUOTA di paging degli errori \_ \_ \_ superata**</span><span class="sxs-lookup"><span data-stu-id="97216-213"><span id="ERROR_PAGEFILE_QUOTA_EXCEEDED"></span><span id="error_pagefile_quota_exceeded"></span>**ERROR\_PAGEFILE\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-214">567 (0x237)</span><span class="sxs-lookup"><span data-stu-id="97216-214">567 (0x237)</span></span>
</dt> <dt>



<span data-ttu-id="97216-215">Quota del file di paging superata.</span><span class="sxs-lookup"><span data-stu-id="97216-215">Page file quota was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-216"><span id="ERROR_LOGON_SERVER_CONFLICT"></span><span id="error_logon_server_conflict"></span>**\_conflitto del \_ server di accesso con errori \_**</span><span class="sxs-lookup"><span data-stu-id="97216-216"><span id="ERROR_LOGON_SERVER_CONFLICT"></span><span id="error_logon_server_conflict"></span>**ERROR\_LOGON\_SERVER\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-217">568 (0x238)</span><span class="sxs-lookup"><span data-stu-id="97216-217">568 (0x238)</span></span>
</dt> <dt>



<span data-ttu-id="97216-218">Impossibile avviare il servizio Netlogon perché un altro servizio Netlogon in esecuzione nel dominio è in conflitto con il ruolo specificato.</span><span class="sxs-lookup"><span data-stu-id="97216-218">The Netlogon service cannot start because another Netlogon service running in the domain conflicts with the specified role.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-219"><span id="ERROR_SYNCHRONIZATION_REQUIRED"></span><span id="error_synchronization_required"></span>**sincronizzazione degli errori \_ \_ obbligatoria**</span><span class="sxs-lookup"><span data-stu-id="97216-219"><span id="ERROR_SYNCHRONIZATION_REQUIRED"></span><span id="error_synchronization_required"></span>**ERROR\_SYNCHRONIZATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-220">569 (0x239)</span><span class="sxs-lookup"><span data-stu-id="97216-220">569 (0x239)</span></span>
</dt> <dt>



<span data-ttu-id="97216-221">Il database SAM in un server Windows è significativamente fuori dalla sincronizzazione con la copia sul controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="97216-221">The SAM database on a Windows Server is significantly out of synchronization with the copy on the Domain Controller.</span></span> <span data-ttu-id="97216-222">È necessaria una sincronizzazione completa.</span><span class="sxs-lookup"><span data-stu-id="97216-222">A complete synchronization is required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-223"><span id="ERROR_NET_OPEN_FAILED"></span><span id="error_net_open_failed"></span>**ERRORE \_ net \_ Open \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="97216-223"><span id="ERROR_NET_OPEN_FAILED"></span><span id="error_net_open_failed"></span>**ERROR\_NET\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-224">570 (0x23A)</span><span class="sxs-lookup"><span data-stu-id="97216-224">570 (0x23A)</span></span>
</dt> <dt>



<span data-ttu-id="97216-225">L'API NtCreateFile non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="97216-225">The NtCreateFile API failed.</span></span> <span data-ttu-id="97216-226">Questo errore non dovrebbe mai essere restituito a un'applicazione. si tratta di un segnaposto che deve essere utilizzato dal redirector di gestione LAN Windows nelle routine di mapping degli errori interni.</span><span class="sxs-lookup"><span data-stu-id="97216-226">This error should never be returned to an application, it is a place holder for the Windows Lan Manager Redirector to use in its internal error mapping routines.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-227"><span id="ERROR_IO_PRIVILEGE_FAILED"></span><span id="error_io_privilege_failed"></span>**privilegio i/o errore \_ \_ \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="97216-227"><span id="ERROR_IO_PRIVILEGE_FAILED"></span><span id="error_io_privilege_failed"></span>**ERROR\_IO\_PRIVILEGE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-228">571 (0x23B)</span><span class="sxs-lookup"><span data-stu-id="97216-228">571 (0x23B)</span></span>
</dt> <dt>



<span data-ttu-id="97216-229">{Privilegio non riuscito} Impossibile modificare le autorizzazioni di I/O per il processo.</span><span class="sxs-lookup"><span data-stu-id="97216-229">{Privilege Failed} The I/O permissions for the process could not be changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-230"><span id="ERROR_CONTROL_C_EXIT"></span><span id="error_control_c_exit"></span>**\_uscita dal controllo di errore \_ C \_**</span><span class="sxs-lookup"><span data-stu-id="97216-230"><span id="ERROR_CONTROL_C_EXIT"></span><span id="error_control_c_exit"></span>**ERROR\_CONTROL\_C\_EXIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-231">572 (0x23C)</span><span class="sxs-lookup"><span data-stu-id="97216-231">572 (0x23C)</span></span>
</dt> <dt>



<span data-ttu-id="97216-232">{Applicazione uscita da CTRL + C} L'applicazione è stata terminata in seguito a una combinazione di tasti CTRL + C.</span><span class="sxs-lookup"><span data-stu-id="97216-232">{Application Exit by CTRL+C} The application terminated as a result of a CTRL+C.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-233"><span id="ERROR_MISSING_SYSTEMFILE"></span><span id="error_missing_systemfile"></span>**ERRORE \_ manca \_ SYSTEMFILE**</span><span class="sxs-lookup"><span data-stu-id="97216-233"><span id="ERROR_MISSING_SYSTEMFILE"></span><span id="error_missing_systemfile"></span>**ERROR\_MISSING\_SYSTEMFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-234">573 (0x23D)</span><span class="sxs-lookup"><span data-stu-id="97216-234">573 (0x23D)</span></span>
</dt> <dt>



<span data-ttu-id="97216-235">{File di sistema mancante} Il file di sistema richiesto% HS non è valido o è mancante.</span><span class="sxs-lookup"><span data-stu-id="97216-235">{Missing System File} The required system file %hs is bad or missing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-236"><span id="ERROR_UNHANDLED_EXCEPTION"></span><span id="error_unhandled_exception"></span>**ERRORE \_ eccezione non gestita \_**</span><span class="sxs-lookup"><span data-stu-id="97216-236"><span id="ERROR_UNHANDLED_EXCEPTION"></span><span id="error_unhandled_exception"></span>**ERROR\_UNHANDLED\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-237">574 (0x23E)</span><span class="sxs-lookup"><span data-stu-id="97216-237">574 (0x23E)</span></span>
</dt> <dt>



<span data-ttu-id="97216-238">{Errore applicazione} Si è verificata l'eccezione% s (0x% 08lx) nell'applicazione nel percorso 0x% 08lx.</span><span class="sxs-lookup"><span data-stu-id="97216-238">{Application Error} The exception %s (0x%08lx) occurred in the application at location 0x%08lx.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-239"><span id="ERROR_APP_INIT_FAILURE"></span><span id="error_app_init_failure"></span>**errore \_ di \_ inizializzazione dell'app errore \_**</span><span class="sxs-lookup"><span data-stu-id="97216-239"><span id="ERROR_APP_INIT_FAILURE"></span><span id="error_app_init_failure"></span>**ERROR\_APP\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-240">575 (0x23F)</span><span class="sxs-lookup"><span data-stu-id="97216-240">575 (0x23F)</span></span>
</dt> <dt>



<span data-ttu-id="97216-241">{Errore applicazione} Non è stato possibile avviare correttamente l'applicazione (0x% lx).</span><span class="sxs-lookup"><span data-stu-id="97216-241">{Application Error} The application was unable to start correctly (0x%lx).</span></span> <span data-ttu-id="97216-242">Fare clic su OK per chiudere l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="97216-242">Click OK to close the application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-243"><span id="ERROR_PAGEFILE_CREATE_FAILED"></span><span id="error_pagefile_create_failed"></span>**ERRORE \_ di \_ creazione del pagefile \_**</span><span class="sxs-lookup"><span data-stu-id="97216-243"><span id="ERROR_PAGEFILE_CREATE_FAILED"></span><span id="error_pagefile_create_failed"></span>**ERROR\_PAGEFILE\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-244">576 (0x240)</span><span class="sxs-lookup"><span data-stu-id="97216-244">576 (0x240)</span></span>
</dt> <dt>



<span data-ttu-id="97216-245">{Impossibile creare il file di paging} Creazione del file di paging% HS non riuscita (% LX).</span><span class="sxs-lookup"><span data-stu-id="97216-245">{Unable to Create Paging File} The creation of the paging file %hs failed (%lx).</span></span> <span data-ttu-id="97216-246">Dimensioni richieste:% LD.</span><span class="sxs-lookup"><span data-stu-id="97216-246">The requested size was %ld.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-247"><span id="ERROR_INVALID_IMAGE_HASH"></span><span id="error_invalid_image_hash"></span>**ERRORE \_ di \_ hash immagine non valido \_**</span><span class="sxs-lookup"><span data-stu-id="97216-247"><span id="ERROR_INVALID_IMAGE_HASH"></span><span id="error_invalid_image_hash"></span>**ERROR\_INVALID\_IMAGE\_HASH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-248">577 (0x241)</span><span class="sxs-lookup"><span data-stu-id="97216-248">577 (0x241)</span></span>
</dt> <dt>



<span data-ttu-id="97216-249">Windows non è in grado di verificare la firma digitale per il file.</span><span class="sxs-lookup"><span data-stu-id="97216-249">Windows cannot verify the digital signature for this file.</span></span> <span data-ttu-id="97216-250">Una modifica recente dell'hardware o del software potrebbe avere installato un file firmato in modo errato o danneggiato o che potrebbe essere un software dannoso proveniente da un'origine sconosciuta.</span><span class="sxs-lookup"><span data-stu-id="97216-250">A recent hardware or software change might have installed a file that is signed incorrectly or damaged, or that might be malicious software from an unknown source.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-251"><span id="ERROR_NO_PAGEFILE"></span><span id="error_no_pagefile"></span>**ERRORE \_ nessun \_ pagefile**</span><span class="sxs-lookup"><span data-stu-id="97216-251"><span id="ERROR_NO_PAGEFILE"></span><span id="error_no_pagefile"></span>**ERROR\_NO\_PAGEFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-252">578 (0x242)</span><span class="sxs-lookup"><span data-stu-id="97216-252">578 (0x242)</span></span>
</dt> <dt>



<span data-ttu-id="97216-253">{Nessun file di paging specificato} Nella configurazione di sistema non è stato specificato alcun file di paging.</span><span class="sxs-lookup"><span data-stu-id="97216-253">{No Paging File Specified} No paging file was specified in the system configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-254"><span id="ERROR_ILLEGAL_FLOAT_CONTEXT"></span><span id="error_illegal_float_context"></span>**ERRORE \_ \_ contesto float non valido \_**</span><span class="sxs-lookup"><span data-stu-id="97216-254"><span id="ERROR_ILLEGAL_FLOAT_CONTEXT"></span><span id="error_illegal_float_context"></span>**ERROR\_ILLEGAL\_FLOAT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-255">579 (0x243)</span><span class="sxs-lookup"><span data-stu-id="97216-255">579 (0x243)</span></span>
</dt> <dt>



<span data-ttu-id="97216-256">ECCEZIONE Un'applicazione in modalità reale ha emesso un'istruzione a virgola mobile e l'hardware a virgola mobile non è presente.</span><span class="sxs-lookup"><span data-stu-id="97216-256">{EXCEPTION} A real-mode application issued a floating-point instruction and floating-point hardware is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-257"><span id="ERROR_NO_EVENT_PAIR"></span><span id="error_no_event_pair"></span>**ERRORE \_ Nessuna \_ coppia di eventi \_**</span><span class="sxs-lookup"><span data-stu-id="97216-257"><span id="ERROR_NO_EVENT_PAIR"></span><span id="error_no_event_pair"></span>**ERROR\_NO\_EVENT\_PAIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-258">580 (0x244)</span><span class="sxs-lookup"><span data-stu-id="97216-258">580 (0x244)</span></span>
</dt> <dt>



<span data-ttu-id="97216-259">Un'operazione di sincronizzazione della coppia di eventi è stata eseguita utilizzando l'oggetto coppia di eventi client/server specifico del thread, ma al thread non è stato associato alcun oggetto coppia di eventi.</span><span class="sxs-lookup"><span data-stu-id="97216-259">An event pair synchronization operation was performed using the thread specific client/server event pair object, but no event pair object was associated with the thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-260"><span id="ERROR_DOMAIN_CTRLR_CONFIG_ERROR"></span><span id="error_domain_ctrlr_config_error"></span>**errore di configurazione del dominio di errore \_ \_ CTRLR \_ \_**</span><span class="sxs-lookup"><span data-stu-id="97216-260"><span id="ERROR_DOMAIN_CTRLR_CONFIG_ERROR"></span><span id="error_domain_ctrlr_config_error"></span>**ERROR\_DOMAIN\_CTRLR\_CONFIG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-261">581 (0x245)</span><span class="sxs-lookup"><span data-stu-id="97216-261">581 (0x245)</span></span>
</dt> <dt>



<span data-ttu-id="97216-262">Una configurazione di Windows Server non è corretta.</span><span class="sxs-lookup"><span data-stu-id="97216-262">A Windows Server has an incorrect configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-263"><span id="ERROR_ILLEGAL_CHARACTER"></span><span id="error_illegal_character"></span>**ERRORE \_ carattere non valido \_**</span><span class="sxs-lookup"><span data-stu-id="97216-263"><span id="ERROR_ILLEGAL_CHARACTER"></span><span id="error_illegal_character"></span>**ERROR\_ILLEGAL\_CHARACTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-264">582 (0x246)</span><span class="sxs-lookup"><span data-stu-id="97216-264">582 (0x246)</span></span>
</dt> <dt>



<span data-ttu-id="97216-265">È stato rilevato un carattere non valido.</span><span class="sxs-lookup"><span data-stu-id="97216-265">An illegal character was encountered.</span></span> <span data-ttu-id="97216-266">Per un set di caratteri a più byte, questo include un byte di apertura senza un byte finale positivo.</span><span class="sxs-lookup"><span data-stu-id="97216-266">For a multi-byte character set this includes a lead byte without a succeeding trail byte.</span></span> <span data-ttu-id="97216-267">Per il set di caratteri Unicode sono inclusi i caratteri 0xFFFF e 0xFFFE.</span><span class="sxs-lookup"><span data-stu-id="97216-267">For the Unicode character set this includes the characters 0xFFFF and 0xFFFE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-268"><span id="ERROR_UNDEFINED_CHARACTER"></span><span id="error_undefined_character"></span>**ERRORE \_ carattere non definito \_**</span><span class="sxs-lookup"><span data-stu-id="97216-268"><span id="ERROR_UNDEFINED_CHARACTER"></span><span id="error_undefined_character"></span>**ERROR\_UNDEFINED\_CHARACTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-269">583 (0x247)</span><span class="sxs-lookup"><span data-stu-id="97216-269">583 (0x247)</span></span>
</dt> <dt>



<span data-ttu-id="97216-270">Il carattere Unicode non è definito nel set di caratteri Unicode installato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="97216-270">The Unicode character is not defined in the Unicode character set installed on the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-271"><span id="ERROR_FLOPPY_VOLUME"></span><span id="error_floppy_volume"></span>**\_volume floppy \_ errore**</span><span class="sxs-lookup"><span data-stu-id="97216-271"><span id="ERROR_FLOPPY_VOLUME"></span><span id="error_floppy_volume"></span>**ERROR\_FLOPPY\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-272">584 (0x248)</span><span class="sxs-lookup"><span data-stu-id="97216-272">584 (0x248)</span></span>
</dt> <dt>



<span data-ttu-id="97216-273">Impossibile creare il file di paging su un dischetto floppy.</span><span class="sxs-lookup"><span data-stu-id="97216-273">The paging file cannot be created on a floppy diskette.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-274"><span id="ERROR_BIOS_FAILED_TO_CONNECT_INTERRUPT"></span><span id="error_bios_failed_to_connect_interrupt"></span>**ERRORE \_ BIOS \_ non è stato \_ possibile \_ connettere l' \_ interrupt**</span><span class="sxs-lookup"><span data-stu-id="97216-274"><span id="ERROR_BIOS_FAILED_TO_CONNECT_INTERRUPT"></span><span id="error_bios_failed_to_connect_interrupt"></span>**ERROR\_BIOS\_FAILED\_TO\_CONNECT\_INTERRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-275">585 (0x249)</span><span class="sxs-lookup"><span data-stu-id="97216-275">585 (0x249)</span></span>
</dt> <dt>



<span data-ttu-id="97216-276">Il BIOS di sistema non è riuscito a connettere un interrupt di sistema al dispositivo o al bus per il quale il dispositivo è connesso.</span><span class="sxs-lookup"><span data-stu-id="97216-276">The system BIOS failed to connect a system interrupt to the device or bus for which the device is connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-277"><span id="ERROR_BACKUP_CONTROLLER"></span><span id="error_backup_controller"></span>**\_controller di backup degli errori \_**</span><span class="sxs-lookup"><span data-stu-id="97216-277"><span id="ERROR_BACKUP_CONTROLLER"></span><span id="error_backup_controller"></span>**ERROR\_BACKUP\_CONTROLLER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-278">586 (0x24A)</span><span class="sxs-lookup"><span data-stu-id="97216-278">586 (0x24A)</span></span>
</dt> <dt>



<span data-ttu-id="97216-279">Questa operazione è consentita solo per il controller di dominio primario del dominio.</span><span class="sxs-lookup"><span data-stu-id="97216-279">This operation is only allowed for the Primary Domain Controller of the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-280"><span id="ERROR_MUTANT_LIMIT_EXCEEDED"></span><span id="error_mutant_limit_exceeded"></span>**\_limite del mutatore di errore \_ \_ superato**</span><span class="sxs-lookup"><span data-stu-id="97216-280"><span id="ERROR_MUTANT_LIMIT_EXCEEDED"></span><span id="error_mutant_limit_exceeded"></span>**ERROR\_MUTANT\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-281">587 (0x24B)</span><span class="sxs-lookup"><span data-stu-id="97216-281">587 (0x24B)</span></span>
</dt> <dt>



<span data-ttu-id="97216-282">È stato effettuato un tentativo di acquisire un mutatore in modo che sia stato superato il numero massimo di conteggi.</span><span class="sxs-lookup"><span data-stu-id="97216-282">An attempt was made to acquire a mutant such that its maximum count would have been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-283"><span id="ERROR_FS_DRIVER_REQUIRED"></span><span id="error_fs_driver_required"></span>**ERRORE \_ \_ driver FS \_ necessario**</span><span class="sxs-lookup"><span data-stu-id="97216-283"><span id="ERROR_FS_DRIVER_REQUIRED"></span><span id="error_fs_driver_required"></span>**ERROR\_FS\_DRIVER\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-284">588 (0x24C)</span><span class="sxs-lookup"><span data-stu-id="97216-284">588 (0x24C)</span></span>
</dt> <dt>



<span data-ttu-id="97216-285">È stato eseguito l'accesso a un volume per il quale è necessario un driver file system che non è ancora stato caricato.</span><span class="sxs-lookup"><span data-stu-id="97216-285">A volume has been accessed for which a file system driver is required that has not yet been loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-286"><span id="ERROR_CANNOT_LOAD_REGISTRY_FILE"></span><span id="error_cannot_load_registry_file"></span>**ERRORE \_ non è possibile \_ caricare il \_ file del registro di sistema \_**</span><span class="sxs-lookup"><span data-stu-id="97216-286"><span id="ERROR_CANNOT_LOAD_REGISTRY_FILE"></span><span id="error_cannot_load_registry_file"></span>**ERROR\_CANNOT\_LOAD\_REGISTRY\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-287">589 (0x24D)</span><span class="sxs-lookup"><span data-stu-id="97216-287">589 (0x24D)</span></span>
</dt> <dt>



<span data-ttu-id="97216-288">{Errore file registro di sistema} Il registro di sistema non è in grado di caricare l'hive (file):% HS o il relativo log o alternativa.</span><span class="sxs-lookup"><span data-stu-id="97216-288">{Registry File Failure} The registry cannot load the hive (file): %hs or its log or alternate.</span></span> <span data-ttu-id="97216-289">È danneggiato, assente o non accessibile in scrittura.</span><span class="sxs-lookup"><span data-stu-id="97216-289">It is corrupt, absent, or not writable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-290"><span id="ERROR_DEBUG_ATTACH_FAILED"></span><span id="error_debug_attach_failed"></span>**ERRORE \_ di \_ connessione di debug \_**</span><span class="sxs-lookup"><span data-stu-id="97216-290"><span id="ERROR_DEBUG_ATTACH_FAILED"></span><span id="error_debug_attach_failed"></span>**ERROR\_DEBUG\_ATTACH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-291">590 (0x24E)</span><span class="sxs-lookup"><span data-stu-id="97216-291">590 (0x24E)</span></span>
</dt> <dt>



<span data-ttu-id="97216-292">{Errore imprevisto in [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)} Si è verificato un errore imprevisto durante l'elaborazione di una richiesta dell'API **DebugActiveProcess** .</span><span class="sxs-lookup"><span data-stu-id="97216-292">{Unexpected Failure in [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)} An unexpected failure occurred while processing a **DebugActiveProcess** API request.</span></span> <span data-ttu-id="97216-293">È possibile scegliere OK per terminare il processo oppure Annulla per ignorare l'errore.</span><span class="sxs-lookup"><span data-stu-id="97216-293">You may choose OK to terminate the process, or Cancel to ignore the error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-294"><span id="ERROR_SYSTEM_PROCESS_TERMINATED"></span><span id="error_system_process_terminated"></span>**ERRORE \_ del \_ processo di sistema \_ terminato**</span><span class="sxs-lookup"><span data-stu-id="97216-294"><span id="ERROR_SYSTEM_PROCESS_TERMINATED"></span><span id="error_system_process_terminated"></span>**ERROR\_SYSTEM\_PROCESS\_TERMINATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-295">591 (0x24F)</span><span class="sxs-lookup"><span data-stu-id="97216-295">591 (0x24F)</span></span>
</dt> <dt>



<span data-ttu-id="97216-296">{Errore irreversibile del sistema} Il processo di sistema% HS è stato interrotto in modo imprevisto con lo stato 0x% 08x (0x% 08x 0x% 08x).</span><span class="sxs-lookup"><span data-stu-id="97216-296">{Fatal System Error} The %hs system process terminated unexpectedly with a status of 0x%08x (0x%08x 0x%08x).</span></span> <span data-ttu-id="97216-297">Il sistema è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="97216-297">The system has been shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-298"><span id="ERROR_DATA_NOT_ACCEPTED"></span><span id="error_data_not_accepted"></span>**\_dati errore \_ non \_ accettati**</span><span class="sxs-lookup"><span data-stu-id="97216-298"><span id="ERROR_DATA_NOT_ACCEPTED"></span><span id="error_data_not_accepted"></span>**ERROR\_DATA\_NOT\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-299">592 (0x250)</span><span class="sxs-lookup"><span data-stu-id="97216-299">592 (0x250)</span></span>
</dt> <dt>



<span data-ttu-id="97216-300">{Dati non accettati} Il client TDI non è in grado di gestire i dati ricevuti durante un'indicazione.</span><span class="sxs-lookup"><span data-stu-id="97216-300">{Data Not Accepted} The TDI client could not handle the data received during an indication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-301"><span id="ERROR_VDM_HARD_ERROR"></span><span id="error_vdm_hard_error"></span>**errore \_ hardware di VDM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="97216-301"><span id="ERROR_VDM_HARD_ERROR"></span><span id="error_vdm_hard_error"></span>**ERROR\_VDM\_HARD\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-302">593 (0x251)</span><span class="sxs-lookup"><span data-stu-id="97216-302">593 (0x251)</span></span>
</dt> <dt>



<span data-ttu-id="97216-303">NTVDM ha rilevato un errore hardware.</span><span class="sxs-lookup"><span data-stu-id="97216-303">NTVDM encountered a hard error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-304"><span id="ERROR_DRIVER_CANCEL_TIMEOUT"></span><span id="error_driver_cancel_timeout"></span>**\_ \_ timeout annullamento driver \_ errore**</span><span class="sxs-lookup"><span data-stu-id="97216-304"><span id="ERROR_DRIVER_CANCEL_TIMEOUT"></span><span id="error_driver_cancel_timeout"></span>**ERROR\_DRIVER\_CANCEL\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-305">594 (0x252)</span><span class="sxs-lookup"><span data-stu-id="97216-305">594 (0x252)</span></span>
</dt> <dt>



<span data-ttu-id="97216-306">{Annulla timeout} Il driver% HS non è riuscito a completare una richiesta di I/O annullata nel tempo assegnato.</span><span class="sxs-lookup"><span data-stu-id="97216-306">{Cancel Timeout} The driver %hs failed to complete a cancelled I/O request in the allotted time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-307"><span id="ERROR_REPLY_MESSAGE_MISMATCH"></span><span id="error_reply_message_mismatch"></span>**messaggio di risposta errore non \_ \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="97216-307"><span id="ERROR_REPLY_MESSAGE_MISMATCH"></span><span id="error_reply_message_mismatch"></span>**ERROR\_REPLY\_MESSAGE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-308">595 (0x253)</span><span class="sxs-lookup"><span data-stu-id="97216-308">595 (0x253)</span></span>
</dt> <dt>



<span data-ttu-id="97216-309">{Messaggio di risposta non corrispondente} È stato effettuato un tentativo di rispondere a un messaggio LPC, ma il thread specificato dall'ID client nel messaggio non era in attesa del messaggio.</span><span class="sxs-lookup"><span data-stu-id="97216-309">{Reply Message Mismatch} An attempt was made to reply to an LPC message, but the thread specified by the client ID in the message was not waiting on that message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-310"><span id="ERROR_LOST_WRITEBEHIND_DATA"></span><span id="error_lost_writebehind_data"></span>**errore durante la \_ perdita di \_ \_ dati WRITEBEHIND**</span><span class="sxs-lookup"><span data-stu-id="97216-310"><span id="ERROR_LOST_WRITEBEHIND_DATA"></span><span id="error_lost_writebehind_data"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-311">596 (0x254)</span><span class="sxs-lookup"><span data-stu-id="97216-311">596 (0x254)</span></span>
</dt> <dt>



<span data-ttu-id="97216-312">{Scrittura ritardata non riuscita} Windows non è riuscito a salvare tutti i dati per il file% HS.</span><span class="sxs-lookup"><span data-stu-id="97216-312">{Delayed Write Failed} Windows was unable to save all the data for the file %hs.</span></span> <span data-ttu-id="97216-313">I dati sono andati persi.</span><span class="sxs-lookup"><span data-stu-id="97216-313">The data has been lost.</span></span> <span data-ttu-id="97216-314">Questo errore può essere causato da un errore dell'hardware del computer o della connessione di rete.</span><span class="sxs-lookup"><span data-stu-id="97216-314">This error may be caused by a failure of your computer hardware or network connection.</span></span> <span data-ttu-id="97216-315">Provare a salvare il file altrove.</span><span class="sxs-lookup"><span data-stu-id="97216-315">Please try to save this file elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-316"><span id="ERROR_CLIENT_SERVER_PARAMETERS_INVALID"></span><span id="error_client_server_parameters_invalid"></span>**\_parametri del server client di errore \_ \_ \_ non validi**</span><span class="sxs-lookup"><span data-stu-id="97216-316"><span id="ERROR_CLIENT_SERVER_PARAMETERS_INVALID"></span><span id="error_client_server_parameters_invalid"></span>**ERROR\_CLIENT\_SERVER\_PARAMETERS\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-317">597 (0x255)</span><span class="sxs-lookup"><span data-stu-id="97216-317">597 (0x255)</span></span>
</dt> <dt>



<span data-ttu-id="97216-318">Il parametro o i parametri passati al server nella finestra memoria condivisa client/server non sono validi.</span><span class="sxs-lookup"><span data-stu-id="97216-318">The parameter(s) passed to the server in the client/server shared memory window were invalid.</span></span> <span data-ttu-id="97216-319">Nella finestra Shared Memory è possibile che siano stati inseriti troppi dati.</span><span class="sxs-lookup"><span data-stu-id="97216-319">Too much data may have been put in the shared memory window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-320"><span id="ERROR_NOT_TINY_STREAM"></span><span id="error_not_tiny_stream"></span>**ERRORE \_ non \_ piccolo \_ flusso**</span><span class="sxs-lookup"><span data-stu-id="97216-320"><span id="ERROR_NOT_TINY_STREAM"></span><span id="error_not_tiny_stream"></span>**ERROR\_NOT\_TINY\_STREAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-321">598 (0x256)</span><span class="sxs-lookup"><span data-stu-id="97216-321">598 (0x256)</span></span>
</dt> <dt>



<span data-ttu-id="97216-322">Il flusso non è un flusso di piccole dimensioni.</span><span class="sxs-lookup"><span data-stu-id="97216-322">The stream is not a tiny stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-323"><span id="ERROR_STACK_OVERFLOW_READ"></span><span id="error_stack_overflow_read"></span>**\_ \_ lettura Overflow stack \_ errore**</span><span class="sxs-lookup"><span data-stu-id="97216-323"><span id="ERROR_STACK_OVERFLOW_READ"></span><span id="error_stack_overflow_read"></span>**ERROR\_STACK\_OVERFLOW\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-324">599 (0x257)</span><span class="sxs-lookup"><span data-stu-id="97216-324">599 (0x257)</span></span>
</dt> <dt>



<span data-ttu-id="97216-325">La richiesta deve essere gestita dal codice di overflow dello stack.</span><span class="sxs-lookup"><span data-stu-id="97216-325">The request must be handled by the stack overflow code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-326"><span id="ERROR_CONVERT_TO_LARGE"></span><span id="error_convert_to_large"></span>**ERRORE \_ conversione \_ in \_ grande**</span><span class="sxs-lookup"><span data-stu-id="97216-326"><span id="ERROR_CONVERT_TO_LARGE"></span><span id="error_convert_to_large"></span>**ERROR\_CONVERT\_TO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-327">600 (0x258)</span><span class="sxs-lookup"><span data-stu-id="97216-327">600 (0x258)</span></span>
</dt> <dt>



<span data-ttu-id="97216-328">Codici di stato OFS interno che indicano come viene gestita un'operazione di allocazione.</span><span class="sxs-lookup"><span data-stu-id="97216-328">Internal OFS status codes indicating how an allocation operation is handled.</span></span> <span data-ttu-id="97216-329">Viene eseguito un nuovo tentativo dopo lo spostamento del oNode contenitore o il flusso di extent viene convertito in un flusso di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="97216-329">Either it is retried after the containing onode is moved or the extent stream is converted to a large stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-330"><span id="ERROR_FOUND_OUT_OF_SCOPE"></span><span id="error_found_out_of_scope"></span>**ERRORE \_ rilevato \_ dall' \_ \_ ambito**</span><span class="sxs-lookup"><span data-stu-id="97216-330"><span id="ERROR_FOUND_OUT_OF_SCOPE"></span><span id="error_found_out_of_scope"></span>**ERROR\_FOUND\_OUT\_OF\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-331">601 (0x259)</span><span class="sxs-lookup"><span data-stu-id="97216-331">601 (0x259)</span></span>
</dt> <dt>



<span data-ttu-id="97216-332">Il tentativo di trovare l'oggetto ha trovato un oggetto corrispondente in base all'ID del volume, ma non rientra nell'ambito dell'handle utilizzato per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="97216-332">The attempt to find the object found an object matching by ID on the volume but it is out of the scope of the handle used for the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-333"><span id="ERROR_ALLOCATE_BUCKET"></span><span id="error_allocate_bucket"></span>**ERRORE di \_ allocazione del \_ bucket**</span><span class="sxs-lookup"><span data-stu-id="97216-333"><span id="ERROR_ALLOCATE_BUCKET"></span><span id="error_allocate_bucket"></span>**ERROR\_ALLOCATE\_BUCKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-334">602 (0x25A)</span><span class="sxs-lookup"><span data-stu-id="97216-334">602 (0x25A)</span></span>
</dt> <dt>



<span data-ttu-id="97216-335">La matrice di bucket deve essere aumentata.</span><span class="sxs-lookup"><span data-stu-id="97216-335">The bucket array must be grown.</span></span> <span data-ttu-id="97216-336">Ripetere la transazione dopo questa operazione.</span><span class="sxs-lookup"><span data-stu-id="97216-336">Retry transaction after doing so.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-337"><span id="ERROR_MARSHALL_OVERFLOW"></span><span id="error_marshall_overflow"></span>**ERRORE \_ Marshall \_ overflow**</span><span class="sxs-lookup"><span data-stu-id="97216-337"><span id="ERROR_MARSHALL_OVERFLOW"></span><span id="error_marshall_overflow"></span>**ERROR\_MARSHALL\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-338">603 (0x25B)</span><span class="sxs-lookup"><span data-stu-id="97216-338">603 (0x25B)</span></span>
</dt> <dt>



<span data-ttu-id="97216-339">Si è verificato un overflow del buffer di marshalling utente/kernel.</span><span class="sxs-lookup"><span data-stu-id="97216-339">The user/kernel marshalling buffer has overflowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-340"><span id="ERROR_INVALID_VARIANT"></span><span id="error_invalid_variant"></span>**ERRORE \_ Variant non valido \_**</span><span class="sxs-lookup"><span data-stu-id="97216-340"><span id="ERROR_INVALID_VARIANT"></span><span id="error_invalid_variant"></span>**ERROR\_INVALID\_VARIANT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-341">604 (0x25C)</span><span class="sxs-lookup"><span data-stu-id="97216-341">604 (0x25C)</span></span>
</dt> <dt>



<span data-ttu-id="97216-342">La struttura VARIANT fornita contiene dati non validi.</span><span class="sxs-lookup"><span data-stu-id="97216-342">The supplied variant structure contains invalid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-343"><span id="ERROR_BAD_COMPRESSION_BUFFER"></span><span id="error_bad_compression_buffer"></span>**ERRORE \_ \_ buffer di compressione errato \_**</span><span class="sxs-lookup"><span data-stu-id="97216-343"><span id="ERROR_BAD_COMPRESSION_BUFFER"></span><span id="error_bad_compression_buffer"></span>**ERROR\_BAD\_COMPRESSION\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-344">605 (0x25D)</span><span class="sxs-lookup"><span data-stu-id="97216-344">605 (0x25D)</span></span>
</dt> <dt>



<span data-ttu-id="97216-345">Il buffer specificato contiene dati in formato non valido.</span><span class="sxs-lookup"><span data-stu-id="97216-345">The specified buffer contains ill-formed data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-346"><span id="ERROR_AUDIT_FAILED"></span><span id="error_audit_failed"></span>**\_controllo errori \_ non riuscito**</span><span class="sxs-lookup"><span data-stu-id="97216-346"><span id="ERROR_AUDIT_FAILED"></span><span id="error_audit_failed"></span>**ERROR\_AUDIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-347">606 (0x25E)</span><span class="sxs-lookup"><span data-stu-id="97216-347">606 (0x25E)</span></span>
</dt> <dt>



<span data-ttu-id="97216-348">{Audit non riuscito} Tentativo di generare un controllo di sicurezza non riuscito.</span><span class="sxs-lookup"><span data-stu-id="97216-348">{Audit Failed} An attempt to generate a security audit failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-349"><span id="ERROR_TIMER_RESOLUTION_NOT_SET"></span><span id="error_timer_resolution_not_set"></span>**risoluzione del timer di errore \_ \_ \_ non \_ impostata**</span><span class="sxs-lookup"><span data-stu-id="97216-349"><span id="ERROR_TIMER_RESOLUTION_NOT_SET"></span><span id="error_timer_resolution_not_set"></span>**ERROR\_TIMER\_RESOLUTION\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-350">607 (0x25F)</span><span class="sxs-lookup"><span data-stu-id="97216-350">607 (0x25F)</span></span>
</dt> <dt>



<span data-ttu-id="97216-351">La risoluzione del timer non è stata impostata in precedenza dal processo corrente.</span><span class="sxs-lookup"><span data-stu-id="97216-351">The timer resolution was not previously set by the current process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-352"><span id="ERROR_INSUFFICIENT_LOGON_INFO"></span><span id="error_insufficient_logon_info"></span>**ERRORE \_ \_ informazioni di accesso insufficienti \_**</span><span class="sxs-lookup"><span data-stu-id="97216-352"><span id="ERROR_INSUFFICIENT_LOGON_INFO"></span><span id="error_insufficient_logon_info"></span>**ERROR\_INSUFFICIENT\_LOGON\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-353">608 (0x260)</span><span class="sxs-lookup"><span data-stu-id="97216-353">608 (0x260)</span></span>
</dt> <dt>



<span data-ttu-id="97216-354">Le informazioni sull'account non sono sufficienti per l'accesso.</span><span class="sxs-lookup"><span data-stu-id="97216-354">There is insufficient account information to log you on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-355"><span id="ERROR_BAD_DLL_ENTRYPOINT"></span><span id="error_bad_dll_entrypoint"></span>**ERRORE \_ di \_ ENTRYPOINT dll non valido \_**</span><span class="sxs-lookup"><span data-stu-id="97216-355"><span id="ERROR_BAD_DLL_ENTRYPOINT"></span><span id="error_bad_dll_entrypoint"></span>**ERROR\_BAD\_DLL\_ENTRYPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-356">609 (0x261)</span><span class="sxs-lookup"><span data-stu-id="97216-356">609 (0x261)</span></span>
</dt> <dt>



<span data-ttu-id="97216-357">{EntryPoint DLL non valido} La libreria a collegamento dinamico% HS non è stata scritta correttamente.</span><span class="sxs-lookup"><span data-stu-id="97216-357">{Invalid DLL Entrypoint} The dynamic link library %hs is not written correctly.</span></span> <span data-ttu-id="97216-358">Il puntatore dello stack è stato lasciato in uno stato incoerente.</span><span class="sxs-lookup"><span data-stu-id="97216-358">The stack pointer has been left in an inconsistent state.</span></span> <span data-ttu-id="97216-359">Il EntryPoint deve essere dichiarato come WINAPI o STDCALL.</span><span class="sxs-lookup"><span data-stu-id="97216-359">The entrypoint should be declared as WINAPI or STDCALL.</span></span> <span data-ttu-id="97216-360">Selezionare Sì per interrompere il caricamento della DLL.</span><span class="sxs-lookup"><span data-stu-id="97216-360">Select YES to fail the DLL load.</span></span> <span data-ttu-id="97216-361">Selezionare NO per continuare l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="97216-361">Select NO to continue execution.</span></span> <span data-ttu-id="97216-362">Se si seleziona NO, l'applicazione potrebbe non funzionare correttamente.</span><span class="sxs-lookup"><span data-stu-id="97216-362">Selecting NO may cause the application to operate incorrectly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-363"><span id="ERROR_BAD_SERVICE_ENTRYPOINT"></span><span id="error_bad_service_entrypoint"></span>**ERRORE \_ \_ ENTRYPOINT servizio \_ errato**</span><span class="sxs-lookup"><span data-stu-id="97216-363"><span id="ERROR_BAD_SERVICE_ENTRYPOINT"></span><span id="error_bad_service_entrypoint"></span>**ERROR\_BAD\_SERVICE\_ENTRYPOINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-364">610 (0x262)</span><span class="sxs-lookup"><span data-stu-id="97216-364">610 (0x262)</span></span>
</dt> <dt>



<span data-ttu-id="97216-365">{EntryPoint di callback del servizio non valido} Il servizio% HS non è stato scritto correttamente.</span><span class="sxs-lookup"><span data-stu-id="97216-365">{Invalid Service Callback Entrypoint} The %hs service is not written correctly.</span></span> <span data-ttu-id="97216-366">Il puntatore dello stack è stato lasciato in uno stato incoerente.</span><span class="sxs-lookup"><span data-stu-id="97216-366">The stack pointer has been left in an inconsistent state.</span></span> <span data-ttu-id="97216-367">Il EntryPoint di callback deve essere dichiarato come WINAPI o STDCALL.</span><span class="sxs-lookup"><span data-stu-id="97216-367">The callback entrypoint should be declared as WINAPI or STDCALL.</span></span> <span data-ttu-id="97216-368">Se si seleziona OK, il servizio continuerà a funzionare.</span><span class="sxs-lookup"><span data-stu-id="97216-368">Selecting OK will cause the service to continue operation.</span></span> <span data-ttu-id="97216-369">Tuttavia, il processo del servizio potrebbe funzionare in modo errato.</span><span class="sxs-lookup"><span data-stu-id="97216-369">However, the service process may operate incorrectly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-370"><span id="ERROR_IP_ADDRESS_CONFLICT1"></span><span id="error_ip_address_conflict1"></span>**ERRORE \_ dell' \_ indirizzo IP \_ CONFLICT1**</span><span class="sxs-lookup"><span data-stu-id="97216-370"><span id="ERROR_IP_ADDRESS_CONFLICT1"></span><span id="error_ip_address_conflict1"></span>**ERROR\_IP\_ADDRESS\_CONFLICT1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-371">611 (0x263)</span><span class="sxs-lookup"><span data-stu-id="97216-371">611 (0x263)</span></span>
</dt> <dt>



<span data-ttu-id="97216-372">Si è verificato un conflitto di indirizzi IP con un altro sistema nella rete.</span><span class="sxs-lookup"><span data-stu-id="97216-372">There is an IP address conflict with another system on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-373"><span id="ERROR_IP_ADDRESS_CONFLICT2"></span><span id="error_ip_address_conflict2"></span>**ERRORE \_ dell' \_ indirizzo IP \_ CONFLICT2**</span><span class="sxs-lookup"><span data-stu-id="97216-373"><span id="ERROR_IP_ADDRESS_CONFLICT2"></span><span id="error_ip_address_conflict2"></span>**ERROR\_IP\_ADDRESS\_CONFLICT2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-374">612 (0x264)</span><span class="sxs-lookup"><span data-stu-id="97216-374">612 (0x264)</span></span>
</dt> <dt>



<span data-ttu-id="97216-375">Si è verificato un conflitto di indirizzi IP con un altro sistema nella rete.</span><span class="sxs-lookup"><span data-stu-id="97216-375">There is an IP address conflict with another system on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-376"><span id="ERROR_REGISTRY_QUOTA_LIMIT"></span><span id="error_registry_quota_limit"></span>**\_ \_ limite quota registro \_ errori**</span><span class="sxs-lookup"><span data-stu-id="97216-376"><span id="ERROR_REGISTRY_QUOTA_LIMIT"></span><span id="error_registry_quota_limit"></span>**ERROR\_REGISTRY\_QUOTA\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-377">613 (0x265)</span><span class="sxs-lookup"><span data-stu-id="97216-377">613 (0x265)</span></span>
</dt> <dt>



<span data-ttu-id="97216-378">{Low sullo spazio del registro di sistema} Il sistema ha raggiunto la dimensione massima consentita per la parte del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="97216-378">{Low On Registry Space} The system has reached the maximum size allowed for the system part of the registry.</span></span> <span data-ttu-id="97216-379">Le richieste di archiviazione aggiuntive verranno ignorate.</span><span class="sxs-lookup"><span data-stu-id="97216-379">Additional storage requests will be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-380"><span id="ERROR_NO_CALLBACK_ACTIVE"></span><span id="error_no_callback_active"></span>**ERRORE \_ nessun \_ callback \_ attivo**</span><span class="sxs-lookup"><span data-stu-id="97216-380"><span id="ERROR_NO_CALLBACK_ACTIVE"></span><span id="error_no_callback_active"></span>**ERROR\_NO\_CALLBACK\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-381">614 (0x266)</span><span class="sxs-lookup"><span data-stu-id="97216-381">614 (0x266)</span></span>
</dt> <dt>



<span data-ttu-id="97216-382">Non è possibile eseguire un servizio di sistema restituito di callback quando non è attivo alcun callback.</span><span class="sxs-lookup"><span data-stu-id="97216-382">A callback return system service cannot be executed when no callback is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-383"><span id="ERROR_PWD_TOO_SHORT"></span><span id="error_pwd_too_short"></span>**ERRORE \_ pwd \_ troppo \_ breve**</span><span class="sxs-lookup"><span data-stu-id="97216-383"><span id="ERROR_PWD_TOO_SHORT"></span><span id="error_pwd_too_short"></span>**ERROR\_PWD\_TOO\_SHORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-384">615 (0x267)</span><span class="sxs-lookup"><span data-stu-id="97216-384">615 (0x267)</span></span>
</dt> <dt>



<span data-ttu-id="97216-385">La password specificata è troppo breve per soddisfare i criteri dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="97216-385">The password provided is too short to meet the policy of your user account.</span></span> <span data-ttu-id="97216-386">Scegliere una password più lunga.</span><span class="sxs-lookup"><span data-stu-id="97216-386">Please choose a longer password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-387"><span id="ERROR_PWD_TOO_RECENT"></span><span id="error_pwd_too_recent"></span>**ERRORE \_ pwd \_ troppo \_ recente**</span><span class="sxs-lookup"><span data-stu-id="97216-387"><span id="ERROR_PWD_TOO_RECENT"></span><span id="error_pwd_too_recent"></span>**ERROR\_PWD\_TOO\_RECENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-388">616 (0x268)</span><span class="sxs-lookup"><span data-stu-id="97216-388">616 (0x268)</span></span>
</dt> <dt>



<span data-ttu-id="97216-389">I criteri dell'account utente non consentono di modificare le password troppo spesso.</span><span class="sxs-lookup"><span data-stu-id="97216-389">The policy of your user account does not allow you to change passwords too frequently.</span></span> <span data-ttu-id="97216-390">Questa operazione viene eseguita per impedire agli utenti di tornare a una password familiare ma potenzialmente individuata.</span><span class="sxs-lookup"><span data-stu-id="97216-390">This is done to prevent users from changing back to a familiar, but potentially discovered, password.</span></span> <span data-ttu-id="97216-391">Se si ritiene che la password sia stata compromessa, contattare immediatamente l'amministratore per fare in modo che ne venga assegnato uno nuovo.</span><span class="sxs-lookup"><span data-stu-id="97216-391">If you feel your password has been compromised then please contact your administrator immediately to have a new one assigned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-392"><span id="ERROR_PWD_HISTORY_CONFLICT"></span><span id="error_pwd_history_conflict"></span>**\_ \_ conflitto cronologia pwd \_ errore**</span><span class="sxs-lookup"><span data-stu-id="97216-392"><span id="ERROR_PWD_HISTORY_CONFLICT"></span><span id="error_pwd_history_conflict"></span>**ERROR\_PWD\_HISTORY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-393">617 (0x269)</span><span class="sxs-lookup"><span data-stu-id="97216-393">617 (0x269)</span></span>
</dt> <dt>



<span data-ttu-id="97216-394">Si è tentato di modificare la password in un computer che è stato usato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="97216-394">You have attempted to change your password to one that you have used in the past.</span></span> <span data-ttu-id="97216-395">I criteri dell'account utente non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="97216-395">The policy of your user account does not allow this.</span></span> <span data-ttu-id="97216-396">Selezionare una password che non è stata usata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="97216-396">Please select a password that you have not previously used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-397"><span id="ERROR_UNSUPPORTED_COMPRESSION"></span><span id="error_unsupported_compression"></span>**ERRORE di \_ compressione non supportata \_**</span><span class="sxs-lookup"><span data-stu-id="97216-397"><span id="ERROR_UNSUPPORTED_COMPRESSION"></span><span id="error_unsupported_compression"></span>**ERROR\_UNSUPPORTED\_COMPRESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-398">618 (0x26A)</span><span class="sxs-lookup"><span data-stu-id="97216-398">618 (0x26A)</span></span>
</dt> <dt>



<span data-ttu-id="97216-399">Il formato di compressione specificato non è supportato.</span><span class="sxs-lookup"><span data-stu-id="97216-399">The specified compression format is unsupported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-400"><span id="ERROR_INVALID_HW_PROFILE"></span><span id="error_invalid_hw_profile"></span>**ERRORE \_ del \_ profilo HW non valido \_**</span><span class="sxs-lookup"><span data-stu-id="97216-400"><span id="ERROR_INVALID_HW_PROFILE"></span><span id="error_invalid_hw_profile"></span>**ERROR\_INVALID\_HW\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-401">619 (0x26B)</span><span class="sxs-lookup"><span data-stu-id="97216-401">619 (0x26B)</span></span>
</dt> <dt>



<span data-ttu-id="97216-402">La configurazione del profilo hardware specificata non è valida.</span><span class="sxs-lookup"><span data-stu-id="97216-402">The specified hardware profile configuration is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-403"><span id="ERROR_INVALID_PLUGPLAY_DEVICE_PATH"></span><span id="error_invalid_plugplay_device_path"></span>**ERRORE \_ \_ PLUGPLAY \_ percorso dispositivo \_ non valido**</span><span class="sxs-lookup"><span data-stu-id="97216-403"><span id="ERROR_INVALID_PLUGPLAY_DEVICE_PATH"></span><span id="error_invalid_plugplay_device_path"></span>**ERROR\_INVALID\_PLUGPLAY\_DEVICE\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-404">620 (0x26C)</span><span class="sxs-lookup"><span data-stu-id="97216-404">620 (0x26C)</span></span>
</dt> <dt>



<span data-ttu-id="97216-405">Il percorso del dispositivo del registro di sistema Plug and Play specificato non è valido.</span><span class="sxs-lookup"><span data-stu-id="97216-405">The specified Plug and Play registry device path is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-406"><span id="ERROR_QUOTA_LIST_INCONSISTENT"></span><span id="error_quota_list_inconsistent"></span>**\_elenco quote \_ errori \_ incoerenti**</span><span class="sxs-lookup"><span data-stu-id="97216-406"><span id="ERROR_QUOTA_LIST_INCONSISTENT"></span><span id="error_quota_list_inconsistent"></span>**ERROR\_QUOTA\_LIST\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-407">621 (0x26D)</span><span class="sxs-lookup"><span data-stu-id="97216-407">621 (0x26D)</span></span>
</dt> <dt>



<span data-ttu-id="97216-408">L'elenco di quote specificato non è coerente internamente con il relativo descrittore.</span><span class="sxs-lookup"><span data-stu-id="97216-408">The specified quota list is internally inconsistent with its descriptor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-409"><span id="ERROR_EVALUATION_EXPIRATION"></span><span id="error_evaluation_expiration"></span>**\_scadenza valutazione \_ errore**</span><span class="sxs-lookup"><span data-stu-id="97216-409"><span id="ERROR_EVALUATION_EXPIRATION"></span><span id="error_evaluation_expiration"></span>**ERROR\_EVALUATION\_EXPIRATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-410">622 (0x26E)</span><span class="sxs-lookup"><span data-stu-id="97216-410">622 (0x26E)</span></span>
</dt> <dt>



<span data-ttu-id="97216-411">{Notifica di valutazione di Windows} Il periodo di valutazione per questa installazione di Windows è scaduto.</span><span class="sxs-lookup"><span data-stu-id="97216-411">{Windows Evaluation Notification} The evaluation period for this installation of Windows has expired.</span></span> <span data-ttu-id="97216-412">Questo sistema verrà arrestato tra 1 ora.</span><span class="sxs-lookup"><span data-stu-id="97216-412">This system will shutdown in 1 hour.</span></span> <span data-ttu-id="97216-413">Per ripristinare l'accesso a questa installazione di Windows, aggiornare questa installazione utilizzando una distribuzione con licenza del prodotto.</span><span class="sxs-lookup"><span data-stu-id="97216-413">To restore access to this installation of Windows, please upgrade this installation using a licensed distribution of this product.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-414"><span id="ERROR_ILLEGAL_DLL_RELOCATION"></span><span id="error_illegal_dll_relocation"></span>**ERRORE \_ di \_ rilocazione della dll non valida \_**</span><span class="sxs-lookup"><span data-stu-id="97216-414"><span id="ERROR_ILLEGAL_DLL_RELOCATION"></span><span id="error_illegal_dll_relocation"></span>**ERROR\_ILLEGAL\_DLL\_RELOCATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-415">623 (0x26F)</span><span class="sxs-lookup"><span data-stu-id="97216-415">623 (0x26F)</span></span>
</dt> <dt>



<span data-ttu-id="97216-416">{Rilocazione della DLL di sistema non valida} La DLL di sistema% HS è stata rilocata in memoria.</span><span class="sxs-lookup"><span data-stu-id="97216-416">{Illegal System DLL Relocation} The system DLL %hs was relocated in memory.</span></span> <span data-ttu-id="97216-417">L'applicazione non viene eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="97216-417">The application will not run properly.</span></span> <span data-ttu-id="97216-418">La rilocazione è stata eseguita perché la DLL% HS occupa un intervallo di indirizzi riservato per le DLL di sistema Windows.</span><span class="sxs-lookup"><span data-stu-id="97216-418">The relocation occurred because the DLL %hs occupied an address range reserved for Windows system DLLs.</span></span> <span data-ttu-id="97216-419">Il fornitore che fornisce la DLL deve essere contattato per una nuova DLL.</span><span class="sxs-lookup"><span data-stu-id="97216-419">The vendor supplying the DLL should be contacted for a new DLL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-420"><span id="ERROR_DLL_INIT_FAILED_LOGOFF"></span><span id="error_dll_init_failed_logoff"></span>**ERRORE \_ di \_ inizializzazione DLL \_ non riuscita \_**</span><span class="sxs-lookup"><span data-stu-id="97216-420"><span id="ERROR_DLL_INIT_FAILED_LOGOFF"></span><span id="error_dll_init_failed_logoff"></span>**ERROR\_DLL\_INIT\_FAILED\_LOGOFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-421">624 (0x270)</span><span class="sxs-lookup"><span data-stu-id="97216-421">624 (0x270)</span></span>
</dt> <dt>



<span data-ttu-id="97216-422">{Inizializzazione DLL non riuscita} L'inizializzazione dell'applicazione non è riuscita perché è in corso l'arresto della stazione di finestra.</span><span class="sxs-lookup"><span data-stu-id="97216-422">{DLL Initialization Failed} The application failed to initialize because the window station is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-423"><span id="ERROR_VALIDATE_CONTINUE"></span><span id="error_validate_continue"></span>**ERRORE di \_ convalida \_ continua**</span><span class="sxs-lookup"><span data-stu-id="97216-423"><span id="ERROR_VALIDATE_CONTINUE"></span><span id="error_validate_continue"></span>**ERROR\_VALIDATE\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-424">625 (0x271)</span><span class="sxs-lookup"><span data-stu-id="97216-424">625 (0x271)</span></span>
</dt> <dt>



<span data-ttu-id="97216-425">Il processo di convalida deve continuare con il passaggio successivo.</span><span class="sxs-lookup"><span data-stu-id="97216-425">The validation process needs to continue on to the next step.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-426"><span id="ERROR_NO_MORE_MATCHES"></span><span id="error_no_more_matches"></span>**ERRORE \_ \_ altre \_ corrispondenze**</span><span class="sxs-lookup"><span data-stu-id="97216-426"><span id="ERROR_NO_MORE_MATCHES"></span><span id="error_no_more_matches"></span>**ERROR\_NO\_MORE\_MATCHES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-427">626 (0x272)</span><span class="sxs-lookup"><span data-stu-id="97216-427">626 (0x272)</span></span>
</dt> <dt>



<span data-ttu-id="97216-428">Non sono presenti altre corrispondenze per l'enumerazione dell'indice corrente.</span><span class="sxs-lookup"><span data-stu-id="97216-428">There are no more matches for the current index enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-429"><span id="ERROR_RANGE_LIST_CONFLICT"></span><span id="error_range_list_conflict"></span>**\_ \_ conflitto elenco intervallo \_ errori**</span><span class="sxs-lookup"><span data-stu-id="97216-429"><span id="ERROR_RANGE_LIST_CONFLICT"></span><span id="error_range_list_conflict"></span>**ERROR\_RANGE\_LIST\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-430">627 (0x273)</span><span class="sxs-lookup"><span data-stu-id="97216-430">627 (0x273)</span></span>
</dt> <dt>



<span data-ttu-id="97216-431">Non è stato possibile aggiungere l'intervallo all'elenco di intervalli a causa di un conflitto.</span><span class="sxs-lookup"><span data-stu-id="97216-431">The range could not be added to the range list because of a conflict.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-432"><span id="ERROR_SERVER_SID_MISMATCH"></span><span id="error_server_sid_mismatch"></span>**\_ \_ MANCAta corrispondenza del SID del server errori \_**</span><span class="sxs-lookup"><span data-stu-id="97216-432"><span id="ERROR_SERVER_SID_MISMATCH"></span><span id="error_server_sid_mismatch"></span>**ERROR\_SERVER\_SID\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-433">628 (0x274)</span><span class="sxs-lookup"><span data-stu-id="97216-433">628 (0x274)</span></span>
</dt> <dt>



<span data-ttu-id="97216-434">Il processo server viene eseguito con un SID diverso da quello richiesto dal client.</span><span class="sxs-lookup"><span data-stu-id="97216-434">The server process is running under a SID different than that required by client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-435"><span id="ERROR_CANT_ENABLE_DENY_ONLY"></span><span id="error_cant_enable_deny_only"></span>**ERRORE \_ di \_ Abilitazione \_ \_ solo negazione**</span><span class="sxs-lookup"><span data-stu-id="97216-435"><span id="ERROR_CANT_ENABLE_DENY_ONLY"></span><span id="error_cant_enable_deny_only"></span>**ERROR\_CANT\_ENABLE\_DENY\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-436">629 (0x275)</span><span class="sxs-lookup"><span data-stu-id="97216-436">629 (0x275)</span></span>
</dt> <dt>



<span data-ttu-id="97216-437">Non è possibile abilitare un gruppo contrassegnato come use solo per Deny.</span><span class="sxs-lookup"><span data-stu-id="97216-437">A group marked use for deny only cannot be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-438"><span id="ERROR_FLOAT_MULTIPLE_FAULTS"></span><span id="error_float_multiple_faults"></span>**errore durante il \_ float di \_ più \_ errori**</span><span class="sxs-lookup"><span data-stu-id="97216-438"><span id="ERROR_FLOAT_MULTIPLE_FAULTS"></span><span id="error_float_multiple_faults"></span>**ERROR\_FLOAT\_MULTIPLE\_FAULTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-439">630 (0x276)</span><span class="sxs-lookup"><span data-stu-id="97216-439">630 (0x276)</span></span>
</dt> <dt>



<span data-ttu-id="97216-440">ECCEZIONE Più errori a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="97216-440">{EXCEPTION} Multiple floating point faults.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-441"><span id="ERROR_FLOAT_MULTIPLE_TRAPS"></span><span id="error_float_multiple_traps"></span>**errore durante il \_ float di \_ più \_ trap**</span><span class="sxs-lookup"><span data-stu-id="97216-441"><span id="ERROR_FLOAT_MULTIPLE_TRAPS"></span><span id="error_float_multiple_traps"></span>**ERROR\_FLOAT\_MULTIPLE\_TRAPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-442">631 (0x277)</span><span class="sxs-lookup"><span data-stu-id="97216-442">631 (0x277)</span></span>
</dt> <dt>



<span data-ttu-id="97216-443">ECCEZIONE Più trap a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="97216-443">{EXCEPTION} Multiple floating point traps.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-444"><span id="ERROR_NOINTERFACE"></span><span id="error_nointerface"></span>**ERRORE \_ NOinterface**</span><span class="sxs-lookup"><span data-stu-id="97216-444"><span id="ERROR_NOINTERFACE"></span><span id="error_nointerface"></span>**ERROR\_NOINTERFACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-445">632 (0x278)</span><span class="sxs-lookup"><span data-stu-id="97216-445">632 (0x278)</span></span>
</dt> <dt>



<span data-ttu-id="97216-446">L'interfaccia richiesta non è supportata.</span><span class="sxs-lookup"><span data-stu-id="97216-446">The requested interface is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-447"><span id="ERROR_DRIVER_FAILED_SLEEP"></span><span id="error_driver_failed_sleep"></span>**ERRORE \_ di \_ sospensione driver non riuscito \_**</span><span class="sxs-lookup"><span data-stu-id="97216-447"><span id="ERROR_DRIVER_FAILED_SLEEP"></span><span id="error_driver_failed_sleep"></span>**ERROR\_DRIVER\_FAILED\_SLEEP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-448">633 (0x279)</span><span class="sxs-lookup"><span data-stu-id="97216-448">633 (0x279)</span></span>
</dt> <dt>



<span data-ttu-id="97216-449">{Standby sistema non riuscito} Il driver% HS non supporta la modalità standby.</span><span class="sxs-lookup"><span data-stu-id="97216-449">{System Standby Failed} The driver %hs does not support standby mode.</span></span> <span data-ttu-id="97216-450">L'aggiornamento di questo driver può consentire al sistema di passare alla modalità standby.</span><span class="sxs-lookup"><span data-stu-id="97216-450">Updating this driver may allow the system to go to standby mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-451"><span id="ERROR_CORRUPT_SYSTEM_FILE"></span><span id="error_corrupt_system_file"></span>**ERRORE \_ \_ file di sistema danneggiato \_**</span><span class="sxs-lookup"><span data-stu-id="97216-451"><span id="ERROR_CORRUPT_SYSTEM_FILE"></span><span id="error_corrupt_system_file"></span>**ERROR\_CORRUPT\_SYSTEM\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-452">634 (0x27A)</span><span class="sxs-lookup"><span data-stu-id="97216-452">634 (0x27A)</span></span>
</dt> <dt>



<span data-ttu-id="97216-453">Il file di sistema %1 è stato danneggiato ed è stato sostituito.</span><span class="sxs-lookup"><span data-stu-id="97216-453">The system file %1 has become corrupt and has been replaced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-454"><span id="ERROR_COMMITMENT_MINIMUM"></span><span id="error_commitment_minimum"></span>**\_minimo impegno \_ errore**</span><span class="sxs-lookup"><span data-stu-id="97216-454"><span id="ERROR_COMMITMENT_MINIMUM"></span><span id="error_commitment_minimum"></span>**ERROR\_COMMITMENT\_MINIMUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-455">635 (0x27B)</span><span class="sxs-lookup"><span data-stu-id="97216-455">635 (0x27B)</span></span>
</dt> <dt>



<span data-ttu-id="97216-456">{Memoria virtuale minima troppo bassa} Memoria virtuale insufficiente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="97216-456">{Virtual Memory Minimum Too Low} Your system is low on virtual memory.</span></span> <span data-ttu-id="97216-457">Windows sta aumentando le dimensioni del file di paging della memoria virtuale.</span><span class="sxs-lookup"><span data-stu-id="97216-457">Windows is increasing the size of your virtual memory paging file.</span></span> <span data-ttu-id="97216-458">Durante questo processo, le richieste di memoria per alcune applicazioni potrebbero essere negate.</span><span class="sxs-lookup"><span data-stu-id="97216-458">During this process, memory requests for some applications may be denied.</span></span> <span data-ttu-id="97216-459">Per ulteriori informazioni, vedere la Guida di.</span><span class="sxs-lookup"><span data-stu-id="97216-459">For more information, see Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-460"><span id="ERROR_PNP_RESTART_ENUMERATION"></span><span id="error_pnp_restart_enumeration"></span>**ERRORE \_ di \_ enumerazione di riavvio PNP \_**</span><span class="sxs-lookup"><span data-stu-id="97216-460"><span id="ERROR_PNP_RESTART_ENUMERATION"></span><span id="error_pnp_restart_enumeration"></span>**ERROR\_PNP\_RESTART\_ENUMERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-461">636 (0x27C)</span><span class="sxs-lookup"><span data-stu-id="97216-461">636 (0x27C)</span></span>
</dt> <dt>



<span data-ttu-id="97216-462">Un dispositivo è stato rimosso, quindi è necessario riavviare l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="97216-462">A device was removed so enumeration must be restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-463"><span id="ERROR_SYSTEM_IMAGE_BAD_SIGNATURE"></span><span id="error_system_image_bad_signature"></span>**immagine del sistema di errore \_ \_ \_ firma non valida \_**</span><span class="sxs-lookup"><span data-stu-id="97216-463"><span id="ERROR_SYSTEM_IMAGE_BAD_SIGNATURE"></span><span id="error_system_image_bad_signature"></span>**ERROR\_SYSTEM\_IMAGE\_BAD\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-464">637 (0x27D)</span><span class="sxs-lookup"><span data-stu-id="97216-464">637 (0x27D)</span></span>
</dt> <dt>



<span data-ttu-id="97216-465">{Errore irreversibile del sistema} L'immagine di sistema% s non è firmata correttamente.</span><span class="sxs-lookup"><span data-stu-id="97216-465">{Fatal System Error} The system image %s is not properly signed.</span></span> <span data-ttu-id="97216-466">Il file è stato sostituito con il file firmato.</span><span class="sxs-lookup"><span data-stu-id="97216-466">The file has been replaced with the signed file.</span></span> <span data-ttu-id="97216-467">Il sistema è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="97216-467">The system has been shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-468"><span id="ERROR_PNP_REBOOT_REQUIRED"></span><span id="error_pnp_reboot_required"></span>**ERRORE \_ PNP \_ riavvio \_ richiesto**</span><span class="sxs-lookup"><span data-stu-id="97216-468"><span id="ERROR_PNP_REBOOT_REQUIRED"></span><span id="error_pnp_reboot_required"></span>**ERROR\_PNP\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-469">638 (0x27E)</span><span class="sxs-lookup"><span data-stu-id="97216-469">638 (0x27E)</span></span>
</dt> <dt>



<span data-ttu-id="97216-470">Il dispositivo non viene avviato senza riavvio.</span><span class="sxs-lookup"><span data-stu-id="97216-470">Device will not start without a reboot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-471"><span id="ERROR_INSUFFICIENT_POWER"></span><span id="error_insufficient_power"></span>**ERRORE \_ di \_ alimentazione insufficiente**</span><span class="sxs-lookup"><span data-stu-id="97216-471"><span id="ERROR_INSUFFICIENT_POWER"></span><span id="error_insufficient_power"></span>**ERROR\_INSUFFICIENT\_POWER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-472">639 (0x27F)</span><span class="sxs-lookup"><span data-stu-id="97216-472">639 (0x27F)</span></span>
</dt> <dt>



<span data-ttu-id="97216-473">La potenza necessaria non è sufficiente per completare l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="97216-473">There is not enough power to complete the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-474"><span id="ERROR_MULTIPLE_FAULT_VIOLATION"></span><span id="error_multiple_fault_violation"></span>**errore \_ di \_ più \_ violazioni di errore**</span><span class="sxs-lookup"><span data-stu-id="97216-474"><span id="ERROR_MULTIPLE_FAULT_VIOLATION"></span><span id="error_multiple_fault_violation"></span>**ERROR\_MULTIPLE\_FAULT\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-475">640 (0x280)</span><span class="sxs-lookup"><span data-stu-id="97216-475">640 (0x280)</span></span>
</dt> <dt>



<span data-ttu-id="97216-476">errore \_ di \_ più \_ violazioni di errore</span><span class="sxs-lookup"><span data-stu-id="97216-476">ERROR\_MULTIPLE\_FAULT\_VIOLATION</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-477"><span id="ERROR_SYSTEM_SHUTDOWN"></span><span id="error_system_shutdown"></span>**ERRORE \_ di \_ arresto del sistema**</span><span class="sxs-lookup"><span data-stu-id="97216-477"><span id="ERROR_SYSTEM_SHUTDOWN"></span><span id="error_system_shutdown"></span>**ERROR\_SYSTEM\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-478">641 (0x281)</span><span class="sxs-lookup"><span data-stu-id="97216-478">641 (0x281)</span></span>
</dt> <dt>



<span data-ttu-id="97216-479">È in corso l'arresto del sistema.</span><span class="sxs-lookup"><span data-stu-id="97216-479">The system is in the process of shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-480"><span id="ERROR_PORT_NOT_SET"></span><span id="error_port_not_set"></span>**porta di errore \_ \_ non \_ impostata**</span><span class="sxs-lookup"><span data-stu-id="97216-480"><span id="ERROR_PORT_NOT_SET"></span><span id="error_port_not_set"></span>**ERROR\_PORT\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-481">642 (0x282)</span><span class="sxs-lookup"><span data-stu-id="97216-481">642 (0x282)</span></span>
</dt> <dt>



<span data-ttu-id="97216-482">È stato eseguito un tentativo di rimuovere un processo DebugPort, ma una porta non era ancora associata al processo.</span><span class="sxs-lookup"><span data-stu-id="97216-482">An attempt to remove a processes DebugPort was made, but a port was not already associated with the process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-483"><span id="ERROR_DS_VERSION_CHECK_FAILURE"></span><span id="error_ds_version_check_failure"></span>**ERRORE \_ \_ controllo versione \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="97216-483"><span id="ERROR_DS_VERSION_CHECK_FAILURE"></span><span id="error_ds_version_check_failure"></span>**ERROR\_DS\_VERSION\_CHECK\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-484">643 (0x283)</span><span class="sxs-lookup"><span data-stu-id="97216-484">643 (0x283)</span></span>
</dt> <dt>



<span data-ttu-id="97216-485">Questa versione di Windows non è compatibile con la versione del comportamento della foresta di directory, del dominio o del controller di dominio.</span><span class="sxs-lookup"><span data-stu-id="97216-485">This version of Windows is not compatible with the behavior version of directory forest, domain or domain controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-486"><span id="ERROR_RANGE_NOT_FOUND"></span><span id="error_range_not_found"></span>**\_intervallo errori \_ non \_ trovato**</span><span class="sxs-lookup"><span data-stu-id="97216-486"><span id="ERROR_RANGE_NOT_FOUND"></span><span id="error_range_not_found"></span>**ERROR\_RANGE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-487">644 (0x284)</span><span class="sxs-lookup"><span data-stu-id="97216-487">644 (0x284)</span></span>
</dt> <dt>



<span data-ttu-id="97216-488">L'intervallo specificato non è stato trovato nell'elenco di intervalli.</span><span class="sxs-lookup"><span data-stu-id="97216-488">The specified range could not be found in the range list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-489"><span id="ERROR_NOT_SAFE_MODE_DRIVER"></span><span id="error_not_safe_mode_driver"></span>**\_driver in \_ modalità non sicura \_ \_ errore**</span><span class="sxs-lookup"><span data-stu-id="97216-489"><span id="ERROR_NOT_SAFE_MODE_DRIVER"></span><span id="error_not_safe_mode_driver"></span>**ERROR\_NOT\_SAFE\_MODE\_DRIVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-490">646 (0x286)</span><span class="sxs-lookup"><span data-stu-id="97216-490">646 (0x286)</span></span>
</dt> <dt>



<span data-ttu-id="97216-491">Il driver non è stato caricato perché il sistema viene avviato in modalità provvisoria.</span><span class="sxs-lookup"><span data-stu-id="97216-491">The driver was not loaded because the system is booting into safe mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-492"><span id="ERROR_FAILED_DRIVER_ENTRY"></span><span id="error_failed_driver_entry"></span>**ERRORE \_ \_ voce driver non riuscita \_**</span><span class="sxs-lookup"><span data-stu-id="97216-492"><span id="ERROR_FAILED_DRIVER_ENTRY"></span><span id="error_failed_driver_entry"></span>**ERROR\_FAILED\_DRIVER\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-493">647 (0x287)</span><span class="sxs-lookup"><span data-stu-id="97216-493">647 (0x287)</span></span>
</dt> <dt>



<span data-ttu-id="97216-494">Il driver non è stato caricato perché non ha superato la chiamata di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="97216-494">The driver was not loaded because it failed its initialization call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-495"><span id="ERROR_DEVICE_ENUMERATION_ERROR"></span><span id="error_device_enumeration_error"></span>**errore \_ di \_ enumerazione dispositivo errore \_**</span><span class="sxs-lookup"><span data-stu-id="97216-495"><span id="ERROR_DEVICE_ENUMERATION_ERROR"></span><span id="error_device_enumeration_error"></span>**ERROR\_DEVICE\_ENUMERATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-496">648 (0x288)</span><span class="sxs-lookup"><span data-stu-id="97216-496">648 (0x288)</span></span>
</dt> <dt>



<span data-ttu-id="97216-497">"% HS" ha rilevato un errore durante l'applicazione dell'alimentazione o la lettura della configurazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="97216-497">The "%hs" encountered an error while applying power or reading the device configuration.</span></span> <span data-ttu-id="97216-498">Ciò può essere causato da un errore dell'hardware o da una connessione scadente.</span><span class="sxs-lookup"><span data-stu-id="97216-498">This may be caused by a failure of your hardware or by a poor connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-499"><span id="ERROR_MOUNT_POINT_NOT_RESOLVED"></span><span id="error_mount_point_not_resolved"></span>**\_punto di montaggio errore \_ \_ non \_ risolto**</span><span class="sxs-lookup"><span data-stu-id="97216-499"><span id="ERROR_MOUNT_POINT_NOT_RESOLVED"></span><span id="error_mount_point_not_resolved"></span>**ERROR\_MOUNT\_POINT\_NOT\_RESOLVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-500">649 (0x289)</span><span class="sxs-lookup"><span data-stu-id="97216-500">649 (0x289)</span></span>
</dt> <dt>



<span data-ttu-id="97216-501">L'operazione di creazione non è riuscita perché il nome contiene almeno un punto di montaggio che viene risolto in un volume a cui l'oggetto dispositivo specificato non è collegato.</span><span class="sxs-lookup"><span data-stu-id="97216-501">The create operation failed because the name contained at least one mount point which resolves to a volume to which the specified device object is not attached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-502"><span id="ERROR_INVALID_DEVICE_OBJECT_PARAMETER"></span><span id="error_invalid_device_object_parameter"></span>**ERRORE \_ \_ \_ parametro oggetto dispositivo non valido \_**</span><span class="sxs-lookup"><span data-stu-id="97216-502"><span id="ERROR_INVALID_DEVICE_OBJECT_PARAMETER"></span><span id="error_invalid_device_object_parameter"></span>**ERROR\_INVALID\_DEVICE\_OBJECT\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-503">650 (0x28A)</span><span class="sxs-lookup"><span data-stu-id="97216-503">650 (0x28A)</span></span>
</dt> <dt>



<span data-ttu-id="97216-504">Il parametro dell'oggetto dispositivo non è un oggetto dispositivo valido o non è collegato al volume specificato dal nome file.</span><span class="sxs-lookup"><span data-stu-id="97216-504">The device object parameter is either not a valid device object or is not attached to the volume specified by the file name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-505"><span id="ERROR_MCA_OCCURED"></span><span id="error_mca_occured"></span>**ERRORE \_ MCA \_ eseguito**</span><span class="sxs-lookup"><span data-stu-id="97216-505"><span id="ERROR_MCA_OCCURED"></span><span id="error_mca_occured"></span>**ERROR\_MCA\_OCCURED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-506">651 (0x28B)</span><span class="sxs-lookup"><span data-stu-id="97216-506">651 (0x28B)</span></span>
</dt> <dt>



<span data-ttu-id="97216-507">Si è verificato un errore di controllo del computer.</span><span class="sxs-lookup"><span data-stu-id="97216-507">A Machine Check Error has occurred.</span></span> <span data-ttu-id="97216-508">Per ulteriori informazioni, consultare il registro eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="97216-508">Please check the system eventlog for additional information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-509"><span id="ERROR_DRIVER_DATABASE_ERROR"></span><span id="error_driver_database_error"></span>**\_errore del \_ database del driver di errore \_**</span><span class="sxs-lookup"><span data-stu-id="97216-509"><span id="ERROR_DRIVER_DATABASE_ERROR"></span><span id="error_driver_database_error"></span>**ERROR\_DRIVER\_DATABASE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-510">652 (0x28C)</span><span class="sxs-lookup"><span data-stu-id="97216-510">652 (0x28C)</span></span>
</dt> <dt>



<span data-ttu-id="97216-511">Errore \[ %2 durante \] l'elaborazione del database del driver.</span><span class="sxs-lookup"><span data-stu-id="97216-511">There was error \[%2\] processing the driver database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-512"><span id="ERROR_SYSTEM_HIVE_TOO_LARGE"></span><span id="error_system_hive_too_large"></span>**ERRORE \_ di \_ hive di sistema \_ troppo \_ grande**</span><span class="sxs-lookup"><span data-stu-id="97216-512"><span id="ERROR_SYSTEM_HIVE_TOO_LARGE"></span><span id="error_system_hive_too_large"></span>**ERROR\_SYSTEM\_HIVE\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-513">653 (0x28D)</span><span class="sxs-lookup"><span data-stu-id="97216-513">653 (0x28D)</span></span>
</dt> <dt>



<span data-ttu-id="97216-514">La dimensione dell'hive del sistema ha superato il limite.</span><span class="sxs-lookup"><span data-stu-id="97216-514">System hive size has exceeded its limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-515"><span id="ERROR_DRIVER_FAILED_PRIOR_UNLOAD"></span><span id="error_driver_failed_prior_unload"></span>**\_ \_ scaricamento precedente errore driver non riuscito \_ \_**</span><span class="sxs-lookup"><span data-stu-id="97216-515"><span id="ERROR_DRIVER_FAILED_PRIOR_UNLOAD"></span><span id="error_driver_failed_prior_unload"></span>**ERROR\_DRIVER\_FAILED\_PRIOR\_UNLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-516">654 (0x28E)</span><span class="sxs-lookup"><span data-stu-id="97216-516">654 (0x28E)</span></span>
</dt> <dt>



<span data-ttu-id="97216-517">Non è stato possibile caricare il driver perché una versione precedente del driver è ancora in memoria.</span><span class="sxs-lookup"><span data-stu-id="97216-517">The driver could not be loaded because a previous version of the driver is still in memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-518"><span id="ERROR_VOLSNAP_PREPARE_HIBERNATE"></span><span id="error_volsnap_prepare_hibernate"></span>**ERRORE \_ VolSnap preparare lo stato di \_ \_ ibernazione**</span><span class="sxs-lookup"><span data-stu-id="97216-518"><span id="ERROR_VOLSNAP_PREPARE_HIBERNATE"></span><span id="error_volsnap_prepare_hibernate"></span>**ERROR\_VOLSNAP\_PREPARE\_HIBERNATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-519">655 (0x28F)</span><span class="sxs-lookup"><span data-stu-id="97216-519">655 (0x28F)</span></span>
</dt> <dt>



<span data-ttu-id="97216-520">{Servizio Copia Shadow del volume} Attendere mentre il Servizio Copia Shadow del volume prepara il volume% HS per l'ibernazione.</span><span class="sxs-lookup"><span data-stu-id="97216-520">{Volume Shadow Copy Service} Please wait while the Volume Shadow Copy Service prepares volume %hs for hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-521"><span id="ERROR_HIBERNATION_FAILURE"></span><span id="error_hibernation_failure"></span>**errore di \_ ibernazione errore \_**</span><span class="sxs-lookup"><span data-stu-id="97216-521"><span id="ERROR_HIBERNATION_FAILURE"></span><span id="error_hibernation_failure"></span>**ERROR\_HIBERNATION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-522">656 (0x290)</span><span class="sxs-lookup"><span data-stu-id="97216-522">656 (0x290)</span></span>
</dt> <dt>



<span data-ttu-id="97216-523">Il sistema non è stato in stato di ibernazione (codice di errore% HS).</span><span class="sxs-lookup"><span data-stu-id="97216-523">The system has failed to hibernate (The error code is %hs).</span></span> <span data-ttu-id="97216-524">Lo stato di ibernazione verrà disabilitato fino al riavvio del sistema.</span><span class="sxs-lookup"><span data-stu-id="97216-524">Hibernation will be disabled until the system is restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-525"><span id="ERROR_PWD_TOO_LONG"></span><span id="error_pwd_too_long"></span>**ERRORE \_ pwd \_ troppo \_ lungo**</span><span class="sxs-lookup"><span data-stu-id="97216-525"><span id="ERROR_PWD_TOO_LONG"></span><span id="error_pwd_too_long"></span>**ERROR\_PWD\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-526">657 (0x291)</span><span class="sxs-lookup"><span data-stu-id="97216-526">657 (0x291)</span></span>
</dt> <dt>



<span data-ttu-id="97216-527">La password specificata è troppo lungo per soddisfare i criteri dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="97216-527">The password provided is too long to meet the policy of your user account.</span></span> <span data-ttu-id="97216-528">Scegliere una password più breve.</span><span class="sxs-lookup"><span data-stu-id="97216-528">Please choose a shorter password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-529"><span id="ERROR_FILE_SYSTEM_LIMITATION"></span><span id="error_file_system_limitation"></span>**\_limitazione del file \_ System \_ degli errori**</span><span class="sxs-lookup"><span data-stu-id="97216-529"><span id="ERROR_FILE_SYSTEM_LIMITATION"></span><span id="error_file_system_limitation"></span>**ERROR\_FILE\_SYSTEM\_LIMITATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-530">665 (0x299)</span><span class="sxs-lookup"><span data-stu-id="97216-530">665 (0x299)</span></span>
</dt> <dt>



<span data-ttu-id="97216-531">Impossibile completare l'operazione a causa di un limite del file system.</span><span class="sxs-lookup"><span data-stu-id="97216-531">The requested operation could not be completed due to a file system limitation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-532"><span id="ERROR_ASSERTION_FAILURE"></span><span id="error_assertion_failure"></span>**ERRORE dell' \_ asserzione di errore \_**</span><span class="sxs-lookup"><span data-stu-id="97216-532"><span id="ERROR_ASSERTION_FAILURE"></span><span id="error_assertion_failure"></span>**ERROR\_ASSERTION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-533">668 (0x29C)</span><span class="sxs-lookup"><span data-stu-id="97216-533">668 (0x29C)</span></span>
</dt> <dt>



<span data-ttu-id="97216-534">Si è verificato un errore di asserzione.</span><span class="sxs-lookup"><span data-stu-id="97216-534">An assertion failure has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-535"><span id="ERROR_ACPI_ERROR"></span><span id="error_acpi_error"></span>**errore \_ ACPI \_ errore**</span><span class="sxs-lookup"><span data-stu-id="97216-535"><span id="ERROR_ACPI_ERROR"></span><span id="error_acpi_error"></span>**ERROR\_ACPI\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-536">669 (0x29D)</span><span class="sxs-lookup"><span data-stu-id="97216-536">669 (0x29D)</span></span>
</dt> <dt>



<span data-ttu-id="97216-537">Si è verificato un errore nel sottosistema ACPI.</span><span class="sxs-lookup"><span data-stu-id="97216-537">An error occurred in the ACPI subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-538"><span id="ERROR_WOW_ASSERTION"></span><span id="error_wow_assertion"></span>**\_ \_ asserzione Wow errore**</span><span class="sxs-lookup"><span data-stu-id="97216-538"><span id="ERROR_WOW_ASSERTION"></span><span id="error_wow_assertion"></span>**ERROR\_WOW\_ASSERTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-539">670 (0x29E)</span><span class="sxs-lookup"><span data-stu-id="97216-539">670 (0x29E)</span></span>
</dt> <dt>



<span data-ttu-id="97216-540">Errore di asserzione WOW.</span><span class="sxs-lookup"><span data-stu-id="97216-540">WOW Assertion Error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-541"><span id="ERROR_PNP_BAD_MPS_TABLE"></span><span id="error_pnp_bad_mps_table"></span>**ERRORE \_ PNP \_ \_ tabella MPS non valida \_**</span><span class="sxs-lookup"><span data-stu-id="97216-541"><span id="ERROR_PNP_BAD_MPS_TABLE"></span><span id="error_pnp_bad_mps_table"></span>**ERROR\_PNP\_BAD\_MPS\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-542">671 (0x29F)</span><span class="sxs-lookup"><span data-stu-id="97216-542">671 (0x29F)</span></span>
</dt> <dt>



<span data-ttu-id="97216-543">Un dispositivo non è presente nella tabella MPS del BIOS di sistema.</span><span class="sxs-lookup"><span data-stu-id="97216-543">A device is missing in the system BIOS MPS table.</span></span> <span data-ttu-id="97216-544">Questo dispositivo non verrà usato.</span><span class="sxs-lookup"><span data-stu-id="97216-544">This device will not be used.</span></span> <span data-ttu-id="97216-545">Contattare il fornitore del sistema per l'aggiornamento del BIOS di sistema.</span><span class="sxs-lookup"><span data-stu-id="97216-545">Please contact your system vendor for system BIOS update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-546"><span id="ERROR_PNP_TRANSLATION_FAILED"></span><span id="error_pnp_translation_failed"></span>**ERRORE \_ di \_ conversione PNP \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="97216-546"><span id="ERROR_PNP_TRANSLATION_FAILED"></span><span id="error_pnp_translation_failed"></span>**ERROR\_PNP\_TRANSLATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-547">672 (0x2A0)</span><span class="sxs-lookup"><span data-stu-id="97216-547">672 (0x2A0)</span></span>
</dt> <dt>



<span data-ttu-id="97216-548">Un convertitore non è riuscito a convertire le risorse.</span><span class="sxs-lookup"><span data-stu-id="97216-548">A translator failed to translate resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-549"><span id="ERROR_PNP_IRQ_TRANSLATION_FAILED"></span><span id="error_pnp_irq_translation_failed"></span>**ERRORE \_ di \_ conversione IRQ PNP \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="97216-549"><span id="ERROR_PNP_IRQ_TRANSLATION_FAILED"></span><span id="error_pnp_irq_translation_failed"></span>**ERROR\_PNP\_IRQ\_TRANSLATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-550">673 (0x2A1)</span><span class="sxs-lookup"><span data-stu-id="97216-550">673 (0x2A1)</span></span>
</dt> <dt>



<span data-ttu-id="97216-551">Un convertitore di IRQ non è riuscito a tradurre le risorse.</span><span class="sxs-lookup"><span data-stu-id="97216-551">A IRQ translator failed to translate resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-552"><span id="ERROR_PNP_INVALID_ID"></span><span id="error_pnp_invalid_id"></span>**ERRORE \_ PNP \_ non valido \_**</span><span class="sxs-lookup"><span data-stu-id="97216-552"><span id="ERROR_PNP_INVALID_ID"></span><span id="error_pnp_invalid_id"></span>**ERROR\_PNP\_INVALID\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-553">674 (0x2A2)</span><span class="sxs-lookup"><span data-stu-id="97216-553">674 (0x2A2)</span></span>
</dt> <dt>



<span data-ttu-id="97216-554">Il driver %2 ha restituito un ID non valido per un dispositivo figlio (%3).</span><span class="sxs-lookup"><span data-stu-id="97216-554">Driver %2 returned invalid ID for a child device (%3).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-555"><span id="ERROR_WAKE_SYSTEM_DEBUGGER"></span><span id="error_wake_system_debugger"></span>**\_debugger di sistema di riattivazione errore \_ \_**</span><span class="sxs-lookup"><span data-stu-id="97216-555"><span id="ERROR_WAKE_SYSTEM_DEBUGGER"></span><span id="error_wake_system_debugger"></span>**ERROR\_WAKE\_SYSTEM\_DEBUGGER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-556">675 (0x2A3)</span><span class="sxs-lookup"><span data-stu-id="97216-556">675 (0x2A3)</span></span>
</dt> <dt>



<span data-ttu-id="97216-557">{Debugger del kernel riattivato} il debugger di sistema è stato riattivato da un interrupt.</span><span class="sxs-lookup"><span data-stu-id="97216-557">{Kernel Debugger Awakened} the system debugger was awakened by an interrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-558"><span id="ERROR_HANDLES_CLOSED"></span><span id="error_handles_closed"></span>**handle di errore \_ \_ chiusi**</span><span class="sxs-lookup"><span data-stu-id="97216-558"><span id="ERROR_HANDLES_CLOSED"></span><span id="error_handles_closed"></span>**ERROR\_HANDLES\_CLOSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-559">676 (0x2A4)</span><span class="sxs-lookup"><span data-stu-id="97216-559">676 (0x2A4)</span></span>
</dt> <dt>



<span data-ttu-id="97216-560">{Handle chiusi} Gli handle per gli oggetti sono stati chiusi automaticamente in seguito all'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="97216-560">{Handles Closed} Handles to objects have been automatically closed as a result of the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-561"><span id="ERROR_EXTRANEOUS_INFORMATION"></span><span id="error_extraneous_information"></span>**\_informazioni estranee \_ sull'errore**</span><span class="sxs-lookup"><span data-stu-id="97216-561"><span id="ERROR_EXTRANEOUS_INFORMATION"></span><span id="error_extraneous_information"></span>**ERROR\_EXTRANEOUS\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-562">677 (0x2A5)</span><span class="sxs-lookup"><span data-stu-id="97216-562">677 (0x2A5)</span></span>
</dt> <dt>



<span data-ttu-id="97216-563">{Troppe informazioni} L'elenco di controllo di accesso (ACL) specificato contiene più informazioni del previsto.</span><span class="sxs-lookup"><span data-stu-id="97216-563">{Too Much Information} The specified access control list (ACL) contained more information than was expected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-564"><span id="ERROR_RXACT_COMMIT_NECESSARY"></span><span id="error_rxact_commit_necessary"></span>**ERRORE \_ RXACT \_ commit \_ necessario**</span><span class="sxs-lookup"><span data-stu-id="97216-564"><span id="ERROR_RXACT_COMMIT_NECESSARY"></span><span id="error_rxact_commit_necessary"></span>**ERROR\_RXACT\_COMMIT\_NECESSARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-565">678 (0x2A6)</span><span class="sxs-lookup"><span data-stu-id="97216-565">678 (0x2A6)</span></span>
</dt> <dt>



<span data-ttu-id="97216-566">Questo stato indica che lo stato della transazione esiste già per il sottoalbero del registro di sistema, ma che il commit di una transazione è stato interrotto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="97216-566">This warning level status indicates that the transaction state already exists for the registry sub-tree, but that a transaction commit was previously aborted.</span></span> <span data-ttu-id="97216-567">Il commit non è stato completato, ma non ne è stato eseguito il rollback, quindi è possibile eseguirne il commit se lo si desidera.</span><span class="sxs-lookup"><span data-stu-id="97216-567">The commit has NOT been completed, but has not been rolled back either (so it may still be committed if desired).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-568"><span id="ERROR_MEDIA_CHECK"></span><span id="error_media_check"></span>**\_controllo del supporto errori \_**</span><span class="sxs-lookup"><span data-stu-id="97216-568"><span id="ERROR_MEDIA_CHECK"></span><span id="error_media_check"></span>**ERROR\_MEDIA\_CHECK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-569">679 (0x2A7)</span><span class="sxs-lookup"><span data-stu-id="97216-569">679 (0x2A7)</span></span>
</dt> <dt>



<span data-ttu-id="97216-570">{Media changed} È possibile che il supporto sia stato modificato.</span><span class="sxs-lookup"><span data-stu-id="97216-570">{Media Changed} The media may have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-571"><span id="ERROR_GUID_SUBSTITUTION_MADE"></span><span id="error_guid_substitution_made"></span>**\_sostituzione GUID \_ errore \_ eseguita**</span><span class="sxs-lookup"><span data-stu-id="97216-571"><span id="ERROR_GUID_SUBSTITUTION_MADE"></span><span id="error_guid_substitution_made"></span>**ERROR\_GUID\_SUBSTITUTION\_MADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-572">680 (0x2A8)</span><span class="sxs-lookup"><span data-stu-id="97216-572">680 (0x2A8)</span></span>
</dt> <dt>



<span data-ttu-id="97216-573">{Sostituzione GUID} Durante la conversione di un identificatore globale (GUID) in un ID di sicurezza (SID) di Windows, non è stato trovato alcun prefisso GUID definito in modo amministrativo.</span><span class="sxs-lookup"><span data-stu-id="97216-573">{GUID Substitution} During the translation of a global identifier (GUID) to a Windows security ID (SID), no administratively-defined GUID prefix was found.</span></span> <span data-ttu-id="97216-574">È stato usato un prefisso sostitutivo, che non compromette la sicurezza del sistema.</span><span class="sxs-lookup"><span data-stu-id="97216-574">A substitute prefix was used, which will not compromise system security.</span></span> <span data-ttu-id="97216-575">Tuttavia, questo può fornire un accesso più restrittivo rispetto a quello previsto.</span><span class="sxs-lookup"><span data-stu-id="97216-575">However, this may provide a more restrictive access than intended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-576"><span id="ERROR_STOPPED_ON_SYMLINK"></span><span id="error_stopped_on_symlink"></span>**ERRORE \_ interrotto \_ sul \_ collegamento simbolico**</span><span class="sxs-lookup"><span data-stu-id="97216-576"><span id="ERROR_STOPPED_ON_SYMLINK"></span><span id="error_stopped_on_symlink"></span>**ERROR\_STOPPED\_ON\_SYMLINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-577">681 (0x2A9)</span><span class="sxs-lookup"><span data-stu-id="97216-577">681 (0x2A9)</span></span>
</dt> <dt>



<span data-ttu-id="97216-578">Operazione di creazione arrestata dopo il raggiungimento di un collegamento simbolico.</span><span class="sxs-lookup"><span data-stu-id="97216-578">The create operation stopped after reaching a symbolic link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-579"><span id="ERROR_LONGJUMP"></span><span id="error_longjump"></span>**ERRORE \_ LONGJUMP**</span><span class="sxs-lookup"><span data-stu-id="97216-579"><span id="ERROR_LONGJUMP"></span><span id="error_longjump"></span>**ERROR\_LONGJUMP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-580">682 (0x2AA)</span><span class="sxs-lookup"><span data-stu-id="97216-580">682 (0x2AA)</span></span>
</dt> <dt>



<span data-ttu-id="97216-581">È stato eseguito un salto lungo.</span><span class="sxs-lookup"><span data-stu-id="97216-581">A long jump has been executed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-582"><span id="ERROR_PLUGPLAY_QUERY_VETOED"></span><span id="error_plugplay_query_vetoed"></span>**ERRORE \_ PLUGPLAY \_ query con \_ veto**</span><span class="sxs-lookup"><span data-stu-id="97216-582"><span id="ERROR_PLUGPLAY_QUERY_VETOED"></span><span id="error_plugplay_query_vetoed"></span>**ERROR\_PLUGPLAY\_QUERY\_VETOED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-583">683 (0x2AB)</span><span class="sxs-lookup"><span data-stu-id="97216-583">683 (0x2AB)</span></span>
</dt> <dt>



<span data-ttu-id="97216-584">Operazione di query Plug and Play non riuscita.</span><span class="sxs-lookup"><span data-stu-id="97216-584">The Plug and Play query operation was not successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-585"><span id="ERROR_UNWIND_CONSOLIDATE"></span><span id="error_unwind_consolidate"></span>**errore durante la \_ rimozione del \_ consolidamento**</span><span class="sxs-lookup"><span data-stu-id="97216-585"><span id="ERROR_UNWIND_CONSOLIDATE"></span><span id="error_unwind_consolidate"></span>**ERROR\_UNWIND\_CONSOLIDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-586">684 (0x2AC)</span><span class="sxs-lookup"><span data-stu-id="97216-586">684 (0x2AC)</span></span>
</dt> <dt>



<span data-ttu-id="97216-587">È stato eseguito un consolidamento dei frame.</span><span class="sxs-lookup"><span data-stu-id="97216-587">A frame consolidation has been executed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-588"><span id="ERROR_REGISTRY_HIVE_RECOVERED"></span><span id="error_registry_hive_recovered"></span>**\_ripristino hive del registro errori \_ \_**</span><span class="sxs-lookup"><span data-stu-id="97216-588"><span id="ERROR_REGISTRY_HIVE_RECOVERED"></span><span id="error_registry_hive_recovered"></span>**ERROR\_REGISTRY\_HIVE\_RECOVERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-589">685 (0x2AD)</span><span class="sxs-lookup"><span data-stu-id="97216-589">685 (0x2AD)</span></span>
</dt> <dt>



<span data-ttu-id="97216-590">{Hive del registro di sistema recuperato} Hive del registro di sistema (file):% HS è stato danneggiato ed è stato recuperato.</span><span class="sxs-lookup"><span data-stu-id="97216-590">{Registry Hive Recovered} Registry hive (file): %hs was corrupted and it has been recovered.</span></span> <span data-ttu-id="97216-591">È possibile che alcuni dati siano andati perduti.</span><span class="sxs-lookup"><span data-stu-id="97216-591">Some data might have been lost.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-592"><span id="ERROR_DLL_MIGHT_BE_INSECURE"></span><span id="error_dll_might_be_insecure"></span>**la \_ dll di errore \_ potrebbe non \_ essere \_ sicura**</span><span class="sxs-lookup"><span data-stu-id="97216-592"><span id="ERROR_DLL_MIGHT_BE_INSECURE"></span><span id="error_dll_might_be_insecure"></span>**ERROR\_DLL\_MIGHT\_BE\_INSECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-593">686 (0x2AE)</span><span class="sxs-lookup"><span data-stu-id="97216-593">686 (0x2AE)</span></span>
</dt> <dt>



<span data-ttu-id="97216-594">L'applicazione sta tentando di eseguire il codice eseguibile dal modulo% HS.</span><span class="sxs-lookup"><span data-stu-id="97216-594">The application is attempting to run executable code from the module %hs.</span></span> <span data-ttu-id="97216-595">Questa operazione potrebbe non essere sicura.</span><span class="sxs-lookup"><span data-stu-id="97216-595">This may be insecure.</span></span> <span data-ttu-id="97216-596">È disponibile un'alternativa,% HS.</span><span class="sxs-lookup"><span data-stu-id="97216-596">An alternative, %hs, is available.</span></span> <span data-ttu-id="97216-597">Se l'applicazione usa il modulo sicuro% HS?</span><span class="sxs-lookup"><span data-stu-id="97216-597">Should the application use the secure module %hs?</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-598"><span id="ERROR_DLL_MIGHT_BE_INCOMPATIBLE"></span><span id="error_dll_might_be_incompatible"></span>**la \_ dll di errore \_ potrebbe non \_ essere \_ compatibile**</span><span class="sxs-lookup"><span data-stu-id="97216-598"><span id="ERROR_DLL_MIGHT_BE_INCOMPATIBLE"></span><span id="error_dll_might_be_incompatible"></span>**ERROR\_DLL\_MIGHT\_BE\_INCOMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-599">687 (0x2AF)</span><span class="sxs-lookup"><span data-stu-id="97216-599">687 (0x2AF)</span></span>
</dt> <dt>



<span data-ttu-id="97216-600">L'applicazione sta caricando il codice eseguibile dal modulo% HS.</span><span class="sxs-lookup"><span data-stu-id="97216-600">The application is loading executable code from the module %hs.</span></span> <span data-ttu-id="97216-601">Questa operazione è sicura, ma potrebbe non essere compatibile con le versioni precedenti del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="97216-601">This is secure, but may be incompatible with previous releases of the operating system.</span></span> <span data-ttu-id="97216-602">È disponibile un'alternativa,% HS.</span><span class="sxs-lookup"><span data-stu-id="97216-602">An alternative, %hs, is available.</span></span> <span data-ttu-id="97216-603">Se l'applicazione usa il modulo sicuro% HS?</span><span class="sxs-lookup"><span data-stu-id="97216-603">Should the application use the secure module %hs?</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-604"><span id="ERROR_DBG_EXCEPTION_NOT_HANDLED"></span><span id="error_dbg_exception_not_handled"></span>**\_eccezione dbg \_ errore \_ non \_ gestita**</span><span class="sxs-lookup"><span data-stu-id="97216-604"><span id="ERROR_DBG_EXCEPTION_NOT_HANDLED"></span><span id="error_dbg_exception_not_handled"></span>**ERROR\_DBG\_EXCEPTION\_NOT\_HANDLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-605">688 (0x2B0)</span><span class="sxs-lookup"><span data-stu-id="97216-605">688 (0x2B0)</span></span>
</dt> <dt>



<span data-ttu-id="97216-606">L'eccezione non è stata gestita dal debugger.</span><span class="sxs-lookup"><span data-stu-id="97216-606">Debugger did not handle the exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-607"><span id="ERROR_DBG_REPLY_LATER"></span><span id="error_dbg_reply_later"></span>**ERRORE \_ dbg \_ risposta in un \_ secondo momento**</span><span class="sxs-lookup"><span data-stu-id="97216-607"><span id="ERROR_DBG_REPLY_LATER"></span><span id="error_dbg_reply_later"></span>**ERROR\_DBG\_REPLY\_LATER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-608">689 (0x2B1)</span><span class="sxs-lookup"><span data-stu-id="97216-608">689 (0x2B1)</span></span>
</dt> <dt>



<span data-ttu-id="97216-609">Il debugger risponderà in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="97216-609">Debugger will reply later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-610"><span id="ERROR_DBG_UNABLE_TO_PROVIDE_HANDLE"></span><span id="error_dbg_unable_to_provide_handle"></span>**ERRORE \_ dbg \_ Impossibile \_ \_ fornire \_ handle**</span><span class="sxs-lookup"><span data-stu-id="97216-610"><span id="ERROR_DBG_UNABLE_TO_PROVIDE_HANDLE"></span><span id="error_dbg_unable_to_provide_handle"></span>**ERROR\_DBG\_UNABLE\_TO\_PROVIDE\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-611">690 (0x2B2)</span><span class="sxs-lookup"><span data-stu-id="97216-611">690 (0x2B2)</span></span>
</dt> <dt>



<span data-ttu-id="97216-612">Il debugger non è in grado di fornire handle.</span><span class="sxs-lookup"><span data-stu-id="97216-612">Debugger cannot provide handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-613"><span id="ERROR_DBG_TERMINATE_THREAD"></span><span id="error_dbg_terminate_thread"></span>**ERRORE \_ dbg \_ Termina \_ thread**</span><span class="sxs-lookup"><span data-stu-id="97216-613"><span id="ERROR_DBG_TERMINATE_THREAD"></span><span id="error_dbg_terminate_thread"></span>**ERROR\_DBG\_TERMINATE\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-614">691 (0x2B3)</span><span class="sxs-lookup"><span data-stu-id="97216-614">691 (0x2B3)</span></span>
</dt> <dt>



<span data-ttu-id="97216-615">Thread terminato dal debugger.</span><span class="sxs-lookup"><span data-stu-id="97216-615">Debugger terminated thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-616"><span id="ERROR_DBG_TERMINATE_PROCESS"></span><span id="error_dbg_terminate_process"></span>**ERRORE \_ dbg \_ terminare il \_ processo**</span><span class="sxs-lookup"><span data-stu-id="97216-616"><span id="ERROR_DBG_TERMINATE_PROCESS"></span><span id="error_dbg_terminate_process"></span>**ERROR\_DBG\_TERMINATE\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-617">692 (0x2B4)</span><span class="sxs-lookup"><span data-stu-id="97216-617">692 (0x2B4)</span></span>
</dt> <dt>



<span data-ttu-id="97216-618">Processo terminato dal debugger.</span><span class="sxs-lookup"><span data-stu-id="97216-618">Debugger terminated process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-619"><span id="ERROR_DBG_CONTROL_C"></span><span id="error_dbg_control_c"></span>**ERRORE \_ dbg \_ controllo \_ C**</span><span class="sxs-lookup"><span data-stu-id="97216-619"><span id="ERROR_DBG_CONTROL_C"></span><span id="error_dbg_control_c"></span>**ERROR\_DBG\_CONTROL\_C**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-620">693 (0x2B5)</span><span class="sxs-lookup"><span data-stu-id="97216-620">693 (0x2B5)</span></span>
</dt> <dt>



<span data-ttu-id="97216-621">Il debugger ha ottenuto il controllo C.</span><span class="sxs-lookup"><span data-stu-id="97216-621">Debugger got control C.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-622"><span id="ERROR_DBG_PRINTEXCEPTION_C"></span><span id="error_dbg_printexception_c"></span>**ERRORE \_ dbg \_ PrintException \_ C**</span><span class="sxs-lookup"><span data-stu-id="97216-622"><span id="ERROR_DBG_PRINTEXCEPTION_C"></span><span id="error_dbg_printexception_c"></span>**ERROR\_DBG\_PRINTEXCEPTION\_C**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-623">694 (0x2B6)</span><span class="sxs-lookup"><span data-stu-id="97216-623">694 (0x2B6)</span></span>
</dt> <dt>



<span data-ttu-id="97216-624">Eccezione stampata dal debugger sul controllo C.</span><span class="sxs-lookup"><span data-stu-id="97216-624">Debugger printed exception on control C.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-625"><span id="ERROR_DBG_RIPEXCEPTION"></span><span id="error_dbg_ripexception"></span>**ERRORE \_ dbg \_ RIPEXCEPTION**</span><span class="sxs-lookup"><span data-stu-id="97216-625"><span id="ERROR_DBG_RIPEXCEPTION"></span><span id="error_dbg_ripexception"></span>**ERROR\_DBG\_RIPEXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-626">695 (0x2B7)</span><span class="sxs-lookup"><span data-stu-id="97216-626">695 (0x2B7)</span></span>
</dt> <dt>



<span data-ttu-id="97216-627">Eccezione RIP ricevuta dal debugger.</span><span class="sxs-lookup"><span data-stu-id="97216-627">Debugger received RIP exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-628"><span id="ERROR_DBG_CONTROL_BREAK"></span><span id="error_dbg_control_break"></span>**ERRORE \_ - \_ \_ Interrompi controllo dbg**</span><span class="sxs-lookup"><span data-stu-id="97216-628"><span id="ERROR_DBG_CONTROL_BREAK"></span><span id="error_dbg_control_break"></span>**ERROR\_DBG\_CONTROL\_BREAK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-629">696 (0x2B8)</span><span class="sxs-lookup"><span data-stu-id="97216-629">696 (0x2B8)</span></span>
</dt> <dt>



<span data-ttu-id="97216-630">Interruzione del controllo ricevuta dal debugger.</span><span class="sxs-lookup"><span data-stu-id="97216-630">Debugger received control break.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-631"><span id="ERROR_DBG_COMMAND_EXCEPTION"></span><span id="error_dbg_command_exception"></span>**\_ \_ eccezione comando dbg \_ errore**</span><span class="sxs-lookup"><span data-stu-id="97216-631"><span id="ERROR_DBG_COMMAND_EXCEPTION"></span><span id="error_dbg_command_exception"></span>**ERROR\_DBG\_COMMAND\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-632">697 (0x2B9)</span><span class="sxs-lookup"><span data-stu-id="97216-632">697 (0x2B9)</span></span>
</dt> <dt>



<span data-ttu-id="97216-633">Eccezione di comunicazione del comando del debugger.</span><span class="sxs-lookup"><span data-stu-id="97216-633">Debugger command communication exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-634"><span id="ERROR_OBJECT_NAME_EXISTS"></span><span id="error_object_name_exists"></span>**\_nome oggetto \_ errore \_ esistente**</span><span class="sxs-lookup"><span data-stu-id="97216-634"><span id="ERROR_OBJECT_NAME_EXISTS"></span><span id="error_object_name_exists"></span>**ERROR\_OBJECT\_NAME\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-635">698 (0x2BA)</span><span class="sxs-lookup"><span data-stu-id="97216-635">698 (0x2BA)</span></span>
</dt> <dt>



<span data-ttu-id="97216-636">{Object exists} È stato effettuato un tentativo di creare un oggetto e il nome dell'oggetto esisteva già.</span><span class="sxs-lookup"><span data-stu-id="97216-636">{Object Exists} An attempt was made to create an object and the object name already existed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-637"><span id="ERROR_THREAD_WAS_SUSPENDED"></span><span id="error_thread_was_suspended"></span>**\_thread di \_ errore \_ sospeso**</span><span class="sxs-lookup"><span data-stu-id="97216-637"><span id="ERROR_THREAD_WAS_SUSPENDED"></span><span id="error_thread_was_suspended"></span>**ERROR\_THREAD\_WAS\_SUSPENDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-638">699 (0x2BB)</span><span class="sxs-lookup"><span data-stu-id="97216-638">699 (0x2BB)</span></span>
</dt> <dt>



<span data-ttu-id="97216-639">{Thread sospeso} Si è verificata una chiusura del thread durante la sospensione del thread.</span><span class="sxs-lookup"><span data-stu-id="97216-639">{Thread Suspended} A thread termination occurred while the thread was suspended.</span></span> <span data-ttu-id="97216-640">Il thread è stato ripreso e la terminazione continua.</span><span class="sxs-lookup"><span data-stu-id="97216-640">The thread was resumed, and termination proceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-641"><span id="ERROR_IMAGE_NOT_AT_BASE"></span><span id="error_image_not_at_base"></span>**\_immagine \_ di errore non \_ alla \_ base**</span><span class="sxs-lookup"><span data-stu-id="97216-641"><span id="ERROR_IMAGE_NOT_AT_BASE"></span><span id="error_image_not_at_base"></span>**ERROR\_IMAGE\_NOT\_AT\_BASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-642">700 (0x2BC)</span><span class="sxs-lookup"><span data-stu-id="97216-642">700 (0x2BC)</span></span>
</dt> <dt>



<span data-ttu-id="97216-643">{Immagine rilocata} Non è stato possibile eseguire il mapping di un file di immagine all'indirizzo specificato nel file di immagine.</span><span class="sxs-lookup"><span data-stu-id="97216-643">{Image Relocated} An image file could not be mapped at the address specified in the image file.</span></span> <span data-ttu-id="97216-644">È necessario eseguire correzioni locali su questa immagine.</span><span class="sxs-lookup"><span data-stu-id="97216-644">Local fixups must be performed on this image.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-645"><span id="ERROR_RXACT_STATE_CREATED"></span><span id="error_rxact_state_created"></span>**\_stato RXACT \_ errore \_ creato**</span><span class="sxs-lookup"><span data-stu-id="97216-645"><span id="ERROR_RXACT_STATE_CREATED"></span><span id="error_rxact_state_created"></span>**ERROR\_RXACT\_STATE\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-646">701 (0x2BD)</span><span class="sxs-lookup"><span data-stu-id="97216-646">701 (0x2BD)</span></span>
</dt> <dt>



<span data-ttu-id="97216-647">Questo stato di livello informativo indica che lo stato della transazione di un sottoalbero del registro di sistema specificato non esiste ancora e deve essere creato.</span><span class="sxs-lookup"><span data-stu-id="97216-647">This informational level status indicates that a specified registry sub-tree transaction state did not yet exist and had to be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-648"><span id="ERROR_SEGMENT_NOTIFICATION"></span><span id="error_segment_notification"></span>**\_notifica del segmento di errore \_**</span><span class="sxs-lookup"><span data-stu-id="97216-648"><span id="ERROR_SEGMENT_NOTIFICATION"></span><span id="error_segment_notification"></span>**ERROR\_SEGMENT\_NOTIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-649">702 (0x2BE)</span><span class="sxs-lookup"><span data-stu-id="97216-649">702 (0x2BE)</span></span>
</dt> <dt>



<span data-ttu-id="97216-650">{Caricamento segmento} Una macchina virtuale DOS (VDM) sta caricando, scaricando o muovendo un'immagine del segmento di programma MS-DOS o Win16.</span><span class="sxs-lookup"><span data-stu-id="97216-650">{Segment Load} A virtual DOS machine (VDM) is loading, unloading, or moving an MS-DOS or Win16 program segment image.</span></span> <span data-ttu-id="97216-651">Viene generata un'eccezione in modo che un debugger possa caricare, scaricare o tenere traccia dei simboli e dei punti di interruzione all'interno di questi segmenti a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="97216-651">An exception is raised so a debugger can load, unload or track symbols and breakpoints within these 16-bit segments.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-652"><span id="ERROR_BAD_CURRENT_DIRECTORY"></span><span id="error_bad_current_directory"></span>**ERRORE \_ \_ directory corrente non valida \_**</span><span class="sxs-lookup"><span data-stu-id="97216-652"><span id="ERROR_BAD_CURRENT_DIRECTORY"></span><span id="error_bad_current_directory"></span>**ERROR\_BAD\_CURRENT\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-653">703 (0x2BF)</span><span class="sxs-lookup"><span data-stu-id="97216-653">703 (0x2BF)</span></span>
</dt> <dt>



<span data-ttu-id="97216-654">{Directory corrente non valida} Il processo non può passare alla directory corrente di avvio% HS.</span><span class="sxs-lookup"><span data-stu-id="97216-654">{Invalid Current Directory} The process cannot switch to the startup current directory %hs.</span></span> <span data-ttu-id="97216-655">Selezionare OK per impostare la directory corrente su% HS oppure selezionare Annulla per uscire.</span><span class="sxs-lookup"><span data-stu-id="97216-655">Select OK to set current directory to %hs, or select CANCEL to exit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-656"><span id="ERROR_FT_READ_RECOVERY_FROM_BACKUP"></span><span id="error_ft_read_recovery_from_backup"></span>**ERRORE \_ ft \_ lettura \_ ripristino \_ dal \_ backup**</span><span class="sxs-lookup"><span data-stu-id="97216-656"><span id="ERROR_FT_READ_RECOVERY_FROM_BACKUP"></span><span id="error_ft_read_recovery_from_backup"></span>**ERROR\_FT\_READ\_RECOVERY\_FROM\_BACKUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-657">704 (0x2C0)</span><span class="sxs-lookup"><span data-stu-id="97216-657">704 (0x2C0)</span></span>
</dt> <dt>



<span data-ttu-id="97216-658">{Lettura ridondante} Per soddisfare una richiesta di lettura, l'file system a tolleranza di errore NT leggere correttamente i dati richiesti da una copia ridondante.</span><span class="sxs-lookup"><span data-stu-id="97216-658">{Redundant Read} To satisfy a read request, the NT fault-tolerant file system successfully read the requested data from a redundant copy.</span></span> <span data-ttu-id="97216-659">Questa operazione è stata eseguita perché il file system ha rilevato un errore in un membro del volume a tolleranza di errore, ma non è stato in grado di riassegnare l'area del dispositivo non riuscita.</span><span class="sxs-lookup"><span data-stu-id="97216-659">This was done because the file system encountered a failure on a member of the fault-tolerant volume, but was unable to reassign the failing area of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-660"><span id="ERROR_FT_WRITE_RECOVERY"></span><span id="error_ft_write_recovery"></span>**errore durante il \_ \_ recupero della scrittura ft \_**</span><span class="sxs-lookup"><span data-stu-id="97216-660"><span id="ERROR_FT_WRITE_RECOVERY"></span><span id="error_ft_write_recovery"></span>**ERROR\_FT\_WRITE\_RECOVERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-661">705 (0x2C1)</span><span class="sxs-lookup"><span data-stu-id="97216-661">705 (0x2C1)</span></span>
</dt> <dt>



<span data-ttu-id="97216-662">{Scrittura ridondante} Per soddisfare una richiesta di scrittura, il file system a tolleranza di errore NT ha scritto correttamente una copia ridondante delle informazioni.</span><span class="sxs-lookup"><span data-stu-id="97216-662">{Redundant Write} To satisfy a write request, the NT fault-tolerant file system successfully wrote a redundant copy of the information.</span></span> <span data-ttu-id="97216-663">Questa operazione è stata eseguita perché il file system ha rilevato un errore in un membro del volume a tolleranza di errore, ma non è stato in grado di riassegnare l'area del dispositivo non riuscita.</span><span class="sxs-lookup"><span data-stu-id="97216-663">This was done because the file system encountered a failure on a member of the fault-tolerant volume, but was not able to reassign the failing area of the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-664"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH"></span><span id="error_image_machine_type_mismatch"></span>**\_tipo di computer immagine errore non \_ \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="97216-664"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH"></span><span id="error_image_machine_type_mismatch"></span>**ERROR\_IMAGE\_MACHINE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-665">706 (0x2C2)</span><span class="sxs-lookup"><span data-stu-id="97216-665">706 (0x2C2)</span></span>
</dt> <dt>



<span data-ttu-id="97216-666">{Tipo computer non corrispondente} Il file di immagine% HS è valido, ma è per un tipo di computer diverso dal computer corrente.</span><span class="sxs-lookup"><span data-stu-id="97216-666">{Machine Type Mismatch} The image file %hs is valid, but is for a machine type other than the current machine.</span></span> <span data-ttu-id="97216-667">Fare clic su OK per continuare oppure su Annulla per interrompere il caricamento della DLL.</span><span class="sxs-lookup"><span data-stu-id="97216-667">Select OK to continue, or CANCEL to fail the DLL load.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-668"><span id="ERROR_RECEIVE_PARTIAL"></span><span id="error_receive_partial"></span>**ERRORE di \_ ricezione \_ parziale**</span><span class="sxs-lookup"><span data-stu-id="97216-668"><span id="ERROR_RECEIVE_PARTIAL"></span><span id="error_receive_partial"></span>**ERROR\_RECEIVE\_PARTIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-669">707 (0x2C3)</span><span class="sxs-lookup"><span data-stu-id="97216-669">707 (0x2C3)</span></span>
</dt> <dt>



<span data-ttu-id="97216-670">{Dati parziali ricevuti} Il trasporto di rete ha restituito i dati parziali al client.</span><span class="sxs-lookup"><span data-stu-id="97216-670">{Partial Data Received} The network transport returned partial data to its client.</span></span> <span data-ttu-id="97216-671">I dati rimanenti verranno inviati in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="97216-671">The remaining data will be sent later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-672"><span id="ERROR_RECEIVE_EXPEDITED"></span><span id="error_receive_expedited"></span>**ERRORE di \_ ricezione \_ accelerato**</span><span class="sxs-lookup"><span data-stu-id="97216-672"><span id="ERROR_RECEIVE_EXPEDITED"></span><span id="error_receive_expedited"></span>**ERROR\_RECEIVE\_EXPEDITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-673">708 (0x2C4)</span><span class="sxs-lookup"><span data-stu-id="97216-673">708 (0x2C4)</span></span>
</dt> <dt>



<span data-ttu-id="97216-674">{Dati accelerati ricevuti} Il trasporto di rete ha restituito i dati al client contrassegnato come accelerato dal sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="97216-674">{Expedited Data Received} The network transport returned data to its client that was marked as expedited by the remote system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-675"><span id="ERROR_RECEIVE_PARTIAL_EXPEDITED"></span><span id="error_receive_partial_expedited"></span>**errore durante la ricezione di una \_ \_ \_ accelerazione parziale**</span><span class="sxs-lookup"><span data-stu-id="97216-675"><span id="ERROR_RECEIVE_PARTIAL_EXPEDITED"></span><span id="error_receive_partial_expedited"></span>**ERROR\_RECEIVE\_PARTIAL\_EXPEDITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-676">709 (0x2C5)</span><span class="sxs-lookup"><span data-stu-id="97216-676">709 (0x2C5)</span></span>
</dt> <dt>



<span data-ttu-id="97216-677">{Dati con accelerazione parziale ricevuti} Il trasporto di rete ha restituito i dati parziali al client e tali dati sono stati contrassegnati come accelerati dal sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="97216-677">{Partial Expedited Data Received} The network transport returned partial data to its client and this data was marked as expedited by the remote system.</span></span> <span data-ttu-id="97216-678">I dati rimanenti verranno inviati in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="97216-678">The remaining data will be sent later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-679"><span id="ERROR_EVENT_DONE"></span><span id="error_event_done"></span>**evento di errore \_ \_ completato**</span><span class="sxs-lookup"><span data-stu-id="97216-679"><span id="ERROR_EVENT_DONE"></span><span id="error_event_done"></span>**ERROR\_EVENT\_DONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-680">710 (0x2C6)</span><span class="sxs-lookup"><span data-stu-id="97216-680">710 (0x2C6)</span></span>
</dt> <dt>



<span data-ttu-id="97216-681">{Evento TDI completato} L'indicazione TDI è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="97216-681">{TDI Event Done} The TDI indication has completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-682"><span id="ERROR_EVENT_PENDING"></span><span id="error_event_pending"></span>**evento di errore \_ \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="97216-682"><span id="ERROR_EVENT_PENDING"></span><span id="error_event_pending"></span>**ERROR\_EVENT\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-683">711 (0x2C7)</span><span class="sxs-lookup"><span data-stu-id="97216-683">711 (0x2C7)</span></span>
</dt> <dt>



<span data-ttu-id="97216-684">{Evento TDI in sospeso} L'indicazione TDI è entrata nello stato in sospeso.</span><span class="sxs-lookup"><span data-stu-id="97216-684">{TDI Event Pending} The TDI indication has entered the pending state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-685"><span id="ERROR_CHECKING_FILE_SYSTEM"></span><span id="error_checking_file_system"></span>**errore durante \_ il controllo del \_ file \_ System**</span><span class="sxs-lookup"><span data-stu-id="97216-685"><span id="ERROR_CHECKING_FILE_SYSTEM"></span><span id="error_checking_file_system"></span>**ERROR\_CHECKING\_FILE\_SYSTEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-686">712 (0x2C8)</span><span class="sxs-lookup"><span data-stu-id="97216-686">712 (0x2C8)</span></span>
</dt> <dt>



<span data-ttu-id="97216-687">Controllo file system in% wZ.</span><span class="sxs-lookup"><span data-stu-id="97216-687">Checking file system on %wZ.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-688"><span id="ERROR_FATAL_APP_EXIT"></span><span id="error_fatal_app_exit"></span>**ERRORE \_ di \_ uscita dell'app irreversibile \_**</span><span class="sxs-lookup"><span data-stu-id="97216-688"><span id="ERROR_FATAL_APP_EXIT"></span><span id="error_fatal_app_exit"></span>**ERROR\_FATAL\_APP\_EXIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-689">713 (0x2C9)</span><span class="sxs-lookup"><span data-stu-id="97216-689">713 (0x2C9)</span></span>
</dt> <dt>



<span data-ttu-id="97216-690">{Chiusura applicazione irreversibile}% HS.</span><span class="sxs-lookup"><span data-stu-id="97216-690">{Fatal Application Exit} %hs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-691"><span id="ERROR_PREDEFINED_HANDLE"></span><span id="error_predefined_handle"></span>**\_handle predefinito dell' \_ errore**</span><span class="sxs-lookup"><span data-stu-id="97216-691"><span id="ERROR_PREDEFINED_HANDLE"></span><span id="error_predefined_handle"></span>**ERROR\_PREDEFINED\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-692">714 (0x2CA)</span><span class="sxs-lookup"><span data-stu-id="97216-692">714 (0x2CA)</span></span>
</dt> <dt>



<span data-ttu-id="97216-693">Un handle predefinito fa riferimento alla chiave del registro di sistema specificata.</span><span class="sxs-lookup"><span data-stu-id="97216-693">The specified registry key is referenced by a predefined handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-694"><span id="ERROR_WAS_UNLOCKED"></span><span id="error_was_unlocked"></span>**ERRORE \_ \_ sbloccato**</span><span class="sxs-lookup"><span data-stu-id="97216-694"><span id="ERROR_WAS_UNLOCKED"></span><span id="error_was_unlocked"></span>**ERROR\_WAS\_UNLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-695">715 (0x2CB)</span><span class="sxs-lookup"><span data-stu-id="97216-695">715 (0x2CB)</span></span>
</dt> <dt>



<span data-ttu-id="97216-696">{Pagina sbloccata} La protezione della pagina di una pagina bloccata è stata modificata in "nessun accesso" e la pagina è stata sbloccata dalla memoria e dal processo.</span><span class="sxs-lookup"><span data-stu-id="97216-696">{Page Unlocked} The page protection of a locked page was changed to 'No Access' and the page was unlocked from memory and from the process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-697"><span id="ERROR_SERVICE_NOTIFICATION"></span><span id="error_service_notification"></span>**\_notifica del servizio di errore \_**</span><span class="sxs-lookup"><span data-stu-id="97216-697"><span id="ERROR_SERVICE_NOTIFICATION"></span><span id="error_service_notification"></span>**ERROR\_SERVICE\_NOTIFICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-698">716 (0x2CC)</span><span class="sxs-lookup"><span data-stu-id="97216-698">716 (0x2CC)</span></span>
</dt> <dt>



<span data-ttu-id="97216-699">% HS</span><span class="sxs-lookup"><span data-stu-id="97216-699">%hs</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-700"><span id="ERROR_WAS_LOCKED"></span><span id="error_was_locked"></span>**ERRORE \_ \_ bloccato**</span><span class="sxs-lookup"><span data-stu-id="97216-700"><span id="ERROR_WAS_LOCKED"></span><span id="error_was_locked"></span>**ERROR\_WAS\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-701">717 (0x2CD)</span><span class="sxs-lookup"><span data-stu-id="97216-701">717 (0x2CD)</span></span>
</dt> <dt>



<span data-ttu-id="97216-702">{Pagina bloccata} Una delle pagine da bloccare è già bloccata.</span><span class="sxs-lookup"><span data-stu-id="97216-702">{Page Locked} One of the pages to lock was already locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-703"><span id="ERROR_LOG_HARD_ERROR"></span><span id="error_log_hard_error"></span>**\_ \_ errore hardware del log degli errori \_**</span><span class="sxs-lookup"><span data-stu-id="97216-703"><span id="ERROR_LOG_HARD_ERROR"></span><span id="error_log_hard_error"></span>**ERROR\_LOG\_HARD\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-704">718 (0x2CE)</span><span class="sxs-lookup"><span data-stu-id="97216-704">718 (0x2CE)</span></span>
</dt> <dt>



<span data-ttu-id="97216-705">Popup applicazione: %1: %2</span><span class="sxs-lookup"><span data-stu-id="97216-705">Application popup: %1 : %2</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-706"><span id="ERROR_ALREADY_WIN32"></span><span id="error_already_win32"></span>**ERRORE \_ già \_ Win32**</span><span class="sxs-lookup"><span data-stu-id="97216-706"><span id="ERROR_ALREADY_WIN32"></span><span id="error_already_win32"></span>**ERROR\_ALREADY\_WIN32**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-707">719 (0x2CF)</span><span class="sxs-lookup"><span data-stu-id="97216-707">719 (0x2CF)</span></span>
</dt> <dt>



<span data-ttu-id="97216-708">ERRORE \_ già \_ Win32</span><span class="sxs-lookup"><span data-stu-id="97216-708">ERROR\_ALREADY\_WIN32</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-709"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH_EXE"></span><span id="error_image_machine_type_mismatch_exe"></span>**\_tipo computer immagine errore non corrispondente al file \_ \_ \_ \_ exe**</span><span class="sxs-lookup"><span data-stu-id="97216-709"><span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH_EXE"></span><span id="error_image_machine_type_mismatch_exe"></span>**ERROR\_IMAGE\_MACHINE\_TYPE\_MISMATCH\_EXE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-710">720 (0x2D0)</span><span class="sxs-lookup"><span data-stu-id="97216-710">720 (0x2D0)</span></span>
</dt> <dt>



<span data-ttu-id="97216-711">{Tipo computer non corrispondente} Il file di immagine% HS è valido, ma è per un tipo di computer diverso dal computer corrente.</span><span class="sxs-lookup"><span data-stu-id="97216-711">{Machine Type Mismatch} The image file %hs is valid, but is for a machine type other than the current machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-712"><span id="ERROR_NO_YIELD_PERFORMED"></span><span id="error_no_yield_performed"></span>**ERRORE \_ nessun \_ rendimento \_ eseguito**</span><span class="sxs-lookup"><span data-stu-id="97216-712"><span id="ERROR_NO_YIELD_PERFORMED"></span><span id="error_no_yield_performed"></span>**ERROR\_NO\_YIELD\_PERFORMED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-713">721 (0x2D1)</span><span class="sxs-lookup"><span data-stu-id="97216-713">721 (0x2D1)</span></span>
</dt> <dt>



<span data-ttu-id="97216-714">È stata eseguita un'esecuzione del rendimento e non è disponibile alcun thread per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="97216-714">A yield execution was performed and no thread was available to run.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-715"><span id="ERROR_TIMER_RESUME_IGNORED"></span><span id="error_timer_resume_ignored"></span>**\_riavvio timer di errore \_ \_ ignorato**</span><span class="sxs-lookup"><span data-stu-id="97216-715"><span id="ERROR_TIMER_RESUME_IGNORED"></span><span id="error_timer_resume_ignored"></span>**ERROR\_TIMER\_RESUME\_IGNORED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-716">722 (0x2D2)</span><span class="sxs-lookup"><span data-stu-id="97216-716">722 (0x2D2)</span></span>
</dt> <dt>



<span data-ttu-id="97216-717">Il flag ripristinabile di un'API timer è stato ignorato.</span><span class="sxs-lookup"><span data-stu-id="97216-717">The resumable flag to a timer API was ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-718"><span id="ERROR_ARBITRATION_UNHANDLED"></span><span id="error_arbitration_unhandled"></span>**ERRORE \_ arbitrale non \_ gestito**</span><span class="sxs-lookup"><span data-stu-id="97216-718"><span id="ERROR_ARBITRATION_UNHANDLED"></span><span id="error_arbitration_unhandled"></span>**ERROR\_ARBITRATION\_UNHANDLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-719">723 (0x2D3)</span><span class="sxs-lookup"><span data-stu-id="97216-719">723 (0x2D3)</span></span>
</dt> <dt>



<span data-ttu-id="97216-720">L'arbitro ha posticipato l'arbitraggio di queste risorse al padre.</span><span class="sxs-lookup"><span data-stu-id="97216-720">The arbiter has deferred arbitration of these resources to its parent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-721"><span id="ERROR_CARDBUS_NOT_SUPPORTED"></span><span id="error_cardbus_not_supported"></span>**ERRORE \_ CardBus \_ non \_ supportato**</span><span class="sxs-lookup"><span data-stu-id="97216-721"><span id="ERROR_CARDBUS_NOT_SUPPORTED"></span><span id="error_cardbus_not_supported"></span>**ERROR\_CARDBUS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-722">724 (0x2D4)</span><span class="sxs-lookup"><span data-stu-id="97216-722">724 (0x2D4)</span></span>
</dt> <dt>



<span data-ttu-id="97216-723">Impossibile avviare il dispositivo CardBus inserito a causa di un errore di configurazione in "% HS".</span><span class="sxs-lookup"><span data-stu-id="97216-723">The inserted CardBus device cannot be started because of a configuration error on "%hs".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-724"><span id="ERROR_MP_PROCESSOR_MISMATCH"></span><span id="error_mp_processor_mismatch"></span>**ERRORE \_ processore MP non \_ \_ corrispondente**</span><span class="sxs-lookup"><span data-stu-id="97216-724"><span id="ERROR_MP_PROCESSOR_MISMATCH"></span><span id="error_mp_processor_mismatch"></span>**ERROR\_MP\_PROCESSOR\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-725">725 (0x2D5)</span><span class="sxs-lookup"><span data-stu-id="97216-725">725 (0x2D5)</span></span>
</dt> <dt>



<span data-ttu-id="97216-726">Le CPU in questo sistema multiprocessore non hanno lo stesso livello di revisione.</span><span class="sxs-lookup"><span data-stu-id="97216-726">The CPUs in this multiprocessor system are not all the same revision level.</span></span> <span data-ttu-id="97216-727">Per utilizzare tutti i processori, il sistema operativo si limita alle funzionalità del processore meno idoneo nel sistema.</span><span class="sxs-lookup"><span data-stu-id="97216-727">To use all processors the operating system restricts itself to the features of the least capable processor in the system.</span></span> <span data-ttu-id="97216-728">Se si verificano problemi con questo sistema, contattare il produttore della CPU per verificare se questa combinazione di processori è supportata.</span><span class="sxs-lookup"><span data-stu-id="97216-728">Should problems occur with this system, contact the CPU manufacturer to see if this mix of processors is supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-729"><span id="ERROR_HIBERNATED"></span><span id="error_hibernated"></span>**ERRORE \_ ibernato**</span><span class="sxs-lookup"><span data-stu-id="97216-729"><span id="ERROR_HIBERNATED"></span><span id="error_hibernated"></span>**ERROR\_HIBERNATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-730">726 (0x2D6)</span><span class="sxs-lookup"><span data-stu-id="97216-730">726 (0x2D6)</span></span>
</dt> <dt>



<span data-ttu-id="97216-731">Il sistema è stato messo in stato di ibernazione.</span><span class="sxs-lookup"><span data-stu-id="97216-731">The system was put into hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-732"><span id="ERROR_RESUME_HIBERNATION"></span><span id="error_resume_hibernation"></span>**ERRORE di \_ ripresa della \_ sospensione**</span><span class="sxs-lookup"><span data-stu-id="97216-732"><span id="ERROR_RESUME_HIBERNATION"></span><span id="error_resume_hibernation"></span>**ERROR\_RESUME\_HIBERNATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-733">727 (0x2D7)</span><span class="sxs-lookup"><span data-stu-id="97216-733">727 (0x2D7)</span></span>
</dt> <dt>



<span data-ttu-id="97216-734">Il sistema è stato ripreso dalla modalità di ibernazione.</span><span class="sxs-lookup"><span data-stu-id="97216-734">The system was resumed from hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-735"><span id="ERROR_FIRMWARE_UPDATED"></span><span id="error_firmware_updated"></span>**FIRMWARE degli errori \_ \_ aggiornato**</span><span class="sxs-lookup"><span data-stu-id="97216-735"><span id="ERROR_FIRMWARE_UPDATED"></span><span id="error_firmware_updated"></span>**ERROR\_FIRMWARE\_UPDATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-736">728 (0x2D8)</span><span class="sxs-lookup"><span data-stu-id="97216-736">728 (0x2D8)</span></span>
</dt> <dt>



<span data-ttu-id="97216-737">È stato rilevato che il firmware del sistema (BIOS) è stato aggiornato con la \[ data precedente del firmware = %2, data corrente del firmware %3 \] .</span><span class="sxs-lookup"><span data-stu-id="97216-737">Windows has detected that the system firmware (BIOS) was updated \[previous firmware date = %2, current firmware date %3\].</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-738"><span id="ERROR_DRIVERS_LEAKING_LOCKED_PAGES"></span><span id="error_drivers_leaking_locked_pages"></span>**driver di errore \_ \_ perdite \_ di \_ pagine bloccate**</span><span class="sxs-lookup"><span data-stu-id="97216-738"><span id="ERROR_DRIVERS_LEAKING_LOCKED_PAGES"></span><span id="error_drivers_leaking_locked_pages"></span>**ERROR\_DRIVERS\_LEAKING\_LOCKED\_PAGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-739">729 (0x2D9)</span><span class="sxs-lookup"><span data-stu-id="97216-739">729 (0x2D9)</span></span>
</dt> <dt>



<span data-ttu-id="97216-740">Un driver di dispositivo sta perdendo le pagine di I/O bloccate causando un calo del sistema.</span><span class="sxs-lookup"><span data-stu-id="97216-740">A device driver is leaking locked I/O pages causing system degradation.</span></span> <span data-ttu-id="97216-741">Il sistema ha attivato automaticamente il codice di rilevamento per tentare di individuare il problema.</span><span class="sxs-lookup"><span data-stu-id="97216-741">The system has automatically enabled tracking code in order to try and catch the culprit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-742"><span id="ERROR_WAKE_SYSTEM"></span><span id="error_wake_system"></span>**\_sistema di riattivazione errore \_**</span><span class="sxs-lookup"><span data-stu-id="97216-742"><span id="ERROR_WAKE_SYSTEM"></span><span id="error_wake_system"></span>**ERROR\_WAKE\_SYSTEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-743">730 (0x2DA)</span><span class="sxs-lookup"><span data-stu-id="97216-743">730 (0x2DA)</span></span>
</dt> <dt>



<span data-ttu-id="97216-744">Il sistema si è risvegliato.</span><span class="sxs-lookup"><span data-stu-id="97216-744">The system has awoken.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-745"><span id="ERROR_WAIT_1"></span><span id="error_wait_1"></span>**ERRORE di \_ attesa \_ 1**</span><span class="sxs-lookup"><span data-stu-id="97216-745"><span id="ERROR_WAIT_1"></span><span id="error_wait_1"></span>**ERROR\_WAIT\_1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-746">731 (0x2DB)</span><span class="sxs-lookup"><span data-stu-id="97216-746">731 (0x2DB)</span></span>
</dt> <dt>



<span data-ttu-id="97216-747">ERRORE di \_ attesa \_ 1</span><span class="sxs-lookup"><span data-stu-id="97216-747">ERROR\_WAIT\_1</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-748"><span id="ERROR_WAIT_2"></span><span id="error_wait_2"></span>**ERRORE di \_ attesa \_ 2**</span><span class="sxs-lookup"><span data-stu-id="97216-748"><span id="ERROR_WAIT_2"></span><span id="error_wait_2"></span>**ERROR\_WAIT\_2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-749">732 (0x2DC)</span><span class="sxs-lookup"><span data-stu-id="97216-749">732 (0x2DC)</span></span>
</dt> <dt>



<span data-ttu-id="97216-750">ERRORE di \_ attesa \_ 2</span><span class="sxs-lookup"><span data-stu-id="97216-750">ERROR\_WAIT\_2</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-751"><span id="ERROR_WAIT_3"></span><span id="error_wait_3"></span>**ERRORE di \_ attesa \_ 3**</span><span class="sxs-lookup"><span data-stu-id="97216-751"><span id="ERROR_WAIT_3"></span><span id="error_wait_3"></span>**ERROR\_WAIT\_3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-752">733 (0x2DD)</span><span class="sxs-lookup"><span data-stu-id="97216-752">733 (0x2DD)</span></span>
</dt> <dt>



<span data-ttu-id="97216-753">ERRORE di \_ attesa \_ 3</span><span class="sxs-lookup"><span data-stu-id="97216-753">ERROR\_WAIT\_3</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-754"><span id="ERROR_WAIT_63"></span><span id="error_wait_63"></span>**ERRORE di \_ attesa \_ 63**</span><span class="sxs-lookup"><span data-stu-id="97216-754"><span id="ERROR_WAIT_63"></span><span id="error_wait_63"></span>**ERROR\_WAIT\_63**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-755">734 (0x2DE)</span><span class="sxs-lookup"><span data-stu-id="97216-755">734 (0x2DE)</span></span>
</dt> <dt>



<span data-ttu-id="97216-756">ERRORE di \_ attesa \_ 63</span><span class="sxs-lookup"><span data-stu-id="97216-756">ERROR\_WAIT\_63</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-757"><span id="ERROR_ABANDONED_WAIT_0"></span><span id="error_abandoned_wait_0"></span>**ERRORE \_ di \_ attesa abbandonata \_ 0**</span><span class="sxs-lookup"><span data-stu-id="97216-757"><span id="ERROR_ABANDONED_WAIT_0"></span><span id="error_abandoned_wait_0"></span>**ERROR\_ABANDONED\_WAIT\_0**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-758">735 (0x2DF)</span><span class="sxs-lookup"><span data-stu-id="97216-758">735 (0x2DF)</span></span>
</dt> <dt>



<span data-ttu-id="97216-759">ERRORE \_ di \_ attesa abbandonata \_ 0</span><span class="sxs-lookup"><span data-stu-id="97216-759">ERROR\_ABANDONED\_WAIT\_0</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-760"><span id="ERROR_ABANDONED_WAIT_63"></span><span id="error_abandoned_wait_63"></span>**ERRORE \_ di \_ attesa abbandonata \_ 63**</span><span class="sxs-lookup"><span data-stu-id="97216-760"><span id="ERROR_ABANDONED_WAIT_63"></span><span id="error_abandoned_wait_63"></span>**ERROR\_ABANDONED\_WAIT\_63**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-761">736 (0x2E0)</span><span class="sxs-lookup"><span data-stu-id="97216-761">736 (0x2E0)</span></span>
</dt> <dt>



<span data-ttu-id="97216-762">ERRORE \_ di \_ attesa abbandonata \_ 63</span><span class="sxs-lookup"><span data-stu-id="97216-762">ERROR\_ABANDONED\_WAIT\_63</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-763"><span id="ERROR_USER_APC"></span><span id="error_user_apc"></span>**ERRORE \_ \_ APC utente**</span><span class="sxs-lookup"><span data-stu-id="97216-763"><span id="ERROR_USER_APC"></span><span id="error_user_apc"></span>**ERROR\_USER\_APC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-764">737 (0x2E1)</span><span class="sxs-lookup"><span data-stu-id="97216-764">737 (0x2E1)</span></span>
</dt> <dt>



<span data-ttu-id="97216-765">ERRORE \_ \_ APC utente</span><span class="sxs-lookup"><span data-stu-id="97216-765">ERROR\_USER\_APC</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-766"><span id="ERROR_KERNEL_APC"></span><span id="error_kernel_apc"></span>**ERRORE del \_ kernel \_ APC**</span><span class="sxs-lookup"><span data-stu-id="97216-766"><span id="ERROR_KERNEL_APC"></span><span id="error_kernel_apc"></span>**ERROR\_KERNEL\_APC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-767">738 (0x2E2)</span><span class="sxs-lookup"><span data-stu-id="97216-767">738 (0x2E2)</span></span>
</dt> <dt>



<span data-ttu-id="97216-768">ERRORE del \_ kernel \_ APC</span><span class="sxs-lookup"><span data-stu-id="97216-768">ERROR\_KERNEL\_APC</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-769"><span id="ERROR_ALERTED"></span><span id="error_alerted"></span>**avviso di errore \_**</span><span class="sxs-lookup"><span data-stu-id="97216-769"><span id="ERROR_ALERTED"></span><span id="error_alerted"></span>**ERROR\_ALERTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-770">739 (0x2E3)</span><span class="sxs-lookup"><span data-stu-id="97216-770">739 (0x2E3)</span></span>
</dt> <dt>



<span data-ttu-id="97216-771">avviso di errore \_</span><span class="sxs-lookup"><span data-stu-id="97216-771">ERROR\_ALERTED</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-772"><span id="ERROR_ELEVATION_REQUIRED"></span><span id="error_elevation_required"></span>**\_elevazione degli errori \_ obbligatoria**</span><span class="sxs-lookup"><span data-stu-id="97216-772"><span id="ERROR_ELEVATION_REQUIRED"></span><span id="error_elevation_required"></span>**ERROR\_ELEVATION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-773">740 (0x2E4)</span><span class="sxs-lookup"><span data-stu-id="97216-773">740 (0x2E4)</span></span>
</dt> <dt>



<span data-ttu-id="97216-774">L'operazione richiesta richiede l'elevazione dei privilegi.</span><span class="sxs-lookup"><span data-stu-id="97216-774">The requested operation requires elevation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-775"><span id="ERROR_REPARSE"></span><span id="error_reparse"></span>**ANALISI degli errori \_**</span><span class="sxs-lookup"><span data-stu-id="97216-775"><span id="ERROR_REPARSE"></span><span id="error_reparse"></span>**ERROR\_REPARSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-776">741 (0x2E5)</span><span class="sxs-lookup"><span data-stu-id="97216-776">741 (0x2E5)</span></span>
</dt> <dt>



<span data-ttu-id="97216-777">Un reparse deve essere eseguito dal gestore oggetti perché il nome del file ha prodotto un collegamento simbolico.</span><span class="sxs-lookup"><span data-stu-id="97216-777">A reparse should be performed by the Object Manager since the name of the file resulted in a symbolic link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-778"><span id="ERROR_OPLOCK_BREAK_IN_PROGRESS"></span><span id="error_oplock_break_in_progress"></span>**ERRORE \_ \_ di blocco opportunistico break \_ in \_ corso**</span><span class="sxs-lookup"><span data-stu-id="97216-778"><span id="ERROR_OPLOCK_BREAK_IN_PROGRESS"></span><span id="error_oplock_break_in_progress"></span>**ERROR\_OPLOCK\_BREAK\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-779">742 (0x2E6)</span><span class="sxs-lookup"><span data-stu-id="97216-779">742 (0x2E6)</span></span>
</dt> <dt>



<span data-ttu-id="97216-780">Operazione di apertura/creazione completata mentre è in corso un'blocco opportunistico.</span><span class="sxs-lookup"><span data-stu-id="97216-780">An open/create operation completed while an oplock break is underway.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-781"><span id="ERROR_VOLUME_MOUNTED"></span><span id="error_volume_mounted"></span>**VOLUME di errore \_ \_ montato**</span><span class="sxs-lookup"><span data-stu-id="97216-781"><span id="ERROR_VOLUME_MOUNTED"></span><span id="error_volume_mounted"></span>**ERROR\_VOLUME\_MOUNTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-782">743 (0x2E7)</span><span class="sxs-lookup"><span data-stu-id="97216-782">743 (0x2E7)</span></span>
</dt> <dt>



<span data-ttu-id="97216-783">Un nuovo volume è stato montato da un file system.</span><span class="sxs-lookup"><span data-stu-id="97216-783">A new volume has been mounted by a file system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-784"><span id="ERROR_RXACT_COMMITTED"></span><span id="error_rxact_committed"></span>**ERRORE \_ RXACT \_ commit**</span><span class="sxs-lookup"><span data-stu-id="97216-784"><span id="ERROR_RXACT_COMMITTED"></span><span id="error_rxact_committed"></span>**ERROR\_RXACT\_COMMITTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-785">744 (0x2E8)</span><span class="sxs-lookup"><span data-stu-id="97216-785">744 (0x2E8)</span></span>
</dt> <dt>



<span data-ttu-id="97216-786">Questo stato indica che lo stato della transazione esiste già per il sottoalbero del registro di sistema, ma che il commit di una transazione è stato interrotto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="97216-786">This success level status indicates that the transaction state already exists for the registry sub-tree, but that a transaction commit was previously aborted.</span></span> <span data-ttu-id="97216-787">Il commit è ora completato.</span><span class="sxs-lookup"><span data-stu-id="97216-787">The commit has now been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-788"><span id="ERROR_NOTIFY_CLEANUP"></span><span id="error_notify_cleanup"></span>**ERRORE \_ notifica \_ pulizia**</span><span class="sxs-lookup"><span data-stu-id="97216-788"><span id="ERROR_NOTIFY_CLEANUP"></span><span id="error_notify_cleanup"></span>**ERROR\_NOTIFY\_CLEANUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-789">745 (0x2E9)</span><span class="sxs-lookup"><span data-stu-id="97216-789">745 (0x2E9)</span></span>
</dt> <dt>



<span data-ttu-id="97216-790">Indica che una richiesta di modifica della notifica è stata completata a causa della chiusura dell'handle che ha effettuato la richiesta di modifica della notifica.</span><span class="sxs-lookup"><span data-stu-id="97216-790">This indicates that a notify change request has been completed due to closing the handle which made the notify change request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-791"><span id="ERROR_PRIMARY_TRANSPORT_CONNECT_FAILED"></span><span id="error_primary_transport_connect_failed"></span>**ERRORE \_ di \_ connessione trasporto primario \_ \_ non riuscita**</span><span class="sxs-lookup"><span data-stu-id="97216-791"><span id="ERROR_PRIMARY_TRANSPORT_CONNECT_FAILED"></span><span id="error_primary_transport_connect_failed"></span>**ERROR\_PRIMARY\_TRANSPORT\_CONNECT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-792">746 (0x2EA)</span><span class="sxs-lookup"><span data-stu-id="97216-792">746 (0x2EA)</span></span>
</dt> <dt>



<span data-ttu-id="97216-793">{Errore di connessione al trasporto primario} È stato effettuato un tentativo di connessione al server remoto% HS sul trasporto primario, ma la connessione non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="97216-793">{Connect Failure on Primary Transport} An attempt was made to connect to the remote server %hs on the primary transport, but the connection failed.</span></span> <span data-ttu-id="97216-794">Il computer è stato in grado di connettersi a un trasporto secondario.</span><span class="sxs-lookup"><span data-stu-id="97216-794">The computer WAS able to connect on a secondary transport.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-795"><span id="ERROR_PAGE_FAULT_TRANSITION"></span><span id="error_page_fault_transition"></span>**\_transizione errore pagina errori \_ \_**</span><span class="sxs-lookup"><span data-stu-id="97216-795"><span id="ERROR_PAGE_FAULT_TRANSITION"></span><span id="error_page_fault_transition"></span>**ERROR\_PAGE\_FAULT\_TRANSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-796">747 (0x2EB)</span><span class="sxs-lookup"><span data-stu-id="97216-796">747 (0x2EB)</span></span>
</dt> <dt>



<span data-ttu-id="97216-797">Errore di pagina: errore di transizione.</span><span class="sxs-lookup"><span data-stu-id="97216-797">Page fault was a transition fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-798"><span id="ERROR_PAGE_FAULT_DEMAND_ZERO"></span><span id="error_page_fault_demand_zero"></span>**errore della pagina di errore della \_ \_ \_ richiesta di errori \_**</span><span class="sxs-lookup"><span data-stu-id="97216-798"><span id="ERROR_PAGE_FAULT_DEMAND_ZERO"></span><span id="error_page_fault_demand_zero"></span>**ERROR\_PAGE\_FAULT\_DEMAND\_ZERO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-799">748 (0x2EC)</span><span class="sxs-lookup"><span data-stu-id="97216-799">748 (0x2EC)</span></span>
</dt> <dt>



<span data-ttu-id="97216-800">Errore di pagina: errore di richiesta zero.</span><span class="sxs-lookup"><span data-stu-id="97216-800">Page fault was a demand zero fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-801"><span id="ERROR_PAGE_FAULT_COPY_ON_WRITE"></span><span id="error_page_fault_copy_on_write"></span>**copia degli errori \_ \_ di pagina di errore durante la \_ \_ \_ scrittura**</span><span class="sxs-lookup"><span data-stu-id="97216-801"><span id="ERROR_PAGE_FAULT_COPY_ON_WRITE"></span><span id="error_page_fault_copy_on_write"></span>**ERROR\_PAGE\_FAULT\_COPY\_ON\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-802">749 (0x2ED)</span><span class="sxs-lookup"><span data-stu-id="97216-802">749 (0x2ED)</span></span>
</dt> <dt>



<span data-ttu-id="97216-803">Errore di pagina: errore di richiesta zero.</span><span class="sxs-lookup"><span data-stu-id="97216-803">Page fault was a demand zero fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-804"><span id="ERROR_PAGE_FAULT_GUARD_PAGE"></span><span id="error_page_fault_guard_page"></span>**\_pagina errore \_ pagina \_ protezione \_ errori**</span><span class="sxs-lookup"><span data-stu-id="97216-804"><span id="ERROR_PAGE_FAULT_GUARD_PAGE"></span><span id="error_page_fault_guard_page"></span>**ERROR\_PAGE\_FAULT\_GUARD\_PAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-805">750 (0x2EE)</span><span class="sxs-lookup"><span data-stu-id="97216-805">750 (0x2EE)</span></span>
</dt> <dt>



<span data-ttu-id="97216-806">Errore di pagina: errore di richiesta zero.</span><span class="sxs-lookup"><span data-stu-id="97216-806">Page fault was a demand zero fault.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-807"><span id="ERROR_PAGE_FAULT_PAGING_FILE"></span><span id="error_page_fault_paging_file"></span>**\_file di \_ paging degli errori di pagina errore \_ \_**</span><span class="sxs-lookup"><span data-stu-id="97216-807"><span id="ERROR_PAGE_FAULT_PAGING_FILE"></span><span id="error_page_fault_paging_file"></span>**ERROR\_PAGE\_FAULT\_PAGING\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-808">751 (0x2EF)</span><span class="sxs-lookup"><span data-stu-id="97216-808">751 (0x2EF)</span></span>
</dt> <dt>



<span data-ttu-id="97216-809">L'errore di pagina è stato soddisfatto leggendo da un dispositivo di archiviazione secondario.</span><span class="sxs-lookup"><span data-stu-id="97216-809">Page fault was satisfied by reading from a secondary storage device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-810"><span id="ERROR_CACHE_PAGE_LOCKED"></span><span id="error_cache_page_locked"></span>**\_pagina cache degli errori \_ \_ bloccata**</span><span class="sxs-lookup"><span data-stu-id="97216-810"><span id="ERROR_CACHE_PAGE_LOCKED"></span><span id="error_cache_page_locked"></span>**ERROR\_CACHE\_PAGE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-811">752 (0x2F0)</span><span class="sxs-lookup"><span data-stu-id="97216-811">752 (0x2F0)</span></span>
</dt> <dt>



<span data-ttu-id="97216-812">Pagina memorizzata nella cache bloccata durante l'operazione.</span><span class="sxs-lookup"><span data-stu-id="97216-812">Cached page was locked during operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-813"><span id="ERROR_CRASH_DUMP"></span><span id="error_crash_dump"></span>**\_dump di arresto anomalo errore \_**</span><span class="sxs-lookup"><span data-stu-id="97216-813"><span id="ERROR_CRASH_DUMP"></span><span id="error_crash_dump"></span>**ERROR\_CRASH\_DUMP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-814">753 (0x2F1)</span><span class="sxs-lookup"><span data-stu-id="97216-814">753 (0x2F1)</span></span>
</dt> <dt>



<span data-ttu-id="97216-815">Il dump di arresto anomalo esiste nel file di paging.</span><span class="sxs-lookup"><span data-stu-id="97216-815">Crash dump exists in paging file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-816"><span id="ERROR_BUFFER_ALL_ZEROS"></span><span id="error_buffer_all_zeros"></span>**BUFFER di errore \_ \_ tutti \_ zeri**</span><span class="sxs-lookup"><span data-stu-id="97216-816"><span id="ERROR_BUFFER_ALL_ZEROS"></span><span id="error_buffer_all_zeros"></span>**ERROR\_BUFFER\_ALL\_ZEROS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-817">754 (0x2F2)</span><span class="sxs-lookup"><span data-stu-id="97216-817">754 (0x2F2)</span></span>
</dt> <dt>



<span data-ttu-id="97216-818">Il buffer specificato contiene tutti gli zeri.</span><span class="sxs-lookup"><span data-stu-id="97216-818">Specified buffer contains all zeros.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-819"><span id="ERROR_REPARSE_OBJECT"></span><span id="error_reparse_object"></span>**ERRORE di \_ reparse \_ Object**</span><span class="sxs-lookup"><span data-stu-id="97216-819"><span id="ERROR_REPARSE_OBJECT"></span><span id="error_reparse_object"></span>**ERROR\_REPARSE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-820">755 (0x2F3)</span><span class="sxs-lookup"><span data-stu-id="97216-820">755 (0x2F3)</span></span>
</dt> <dt>



<span data-ttu-id="97216-821">Un reparse deve essere eseguito dal gestore oggetti perché il nome del file ha prodotto un collegamento simbolico.</span><span class="sxs-lookup"><span data-stu-id="97216-821">A reparse should be performed by the Object Manager since the name of the file resulted in a symbolic link.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-822"><span id="ERROR_RESOURCE_REQUIREMENTS_CHANGED"></span><span id="error_resource_requirements_changed"></span>**\_requisiti delle risorse di errore \_ \_ modificati**</span><span class="sxs-lookup"><span data-stu-id="97216-822"><span id="ERROR_RESOURCE_REQUIREMENTS_CHANGED"></span><span id="error_resource_requirements_changed"></span>**ERROR\_RESOURCE\_REQUIREMENTS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-823">756 (0x2F4)</span><span class="sxs-lookup"><span data-stu-id="97216-823">756 (0x2F4)</span></span>
</dt> <dt>



<span data-ttu-id="97216-824">Il dispositivo è riuscito a eseguire una query e i requisiti relativi alle risorse sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="97216-824">The device has succeeded a query-stop and its resource requirements have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-825"><span id="ERROR_TRANSLATION_COMPLETE"></span><span id="error_translation_complete"></span>**\_traduzione errore \_ completata**</span><span class="sxs-lookup"><span data-stu-id="97216-825"><span id="ERROR_TRANSLATION_COMPLETE"></span><span id="error_translation_complete"></span>**ERROR\_TRANSLATION\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-826">757 (0x2F5)</span><span class="sxs-lookup"><span data-stu-id="97216-826">757 (0x2F5)</span></span>
</dt> <dt>



<span data-ttu-id="97216-827">Il traduttore ha tradotto queste risorse nello spazio globale e non è necessario eseguire altre traduzioni.</span><span class="sxs-lookup"><span data-stu-id="97216-827">The translator has translated these resources into the global space and no further translations should be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-828"><span id="ERROR_NOTHING_TO_TERMINATE"></span><span id="error_nothing_to_terminate"></span>**\_nessun errore \_ da \_ terminare**</span><span class="sxs-lookup"><span data-stu-id="97216-828"><span id="ERROR_NOTHING_TO_TERMINATE"></span><span id="error_nothing_to_terminate"></span>**ERROR\_NOTHING\_TO\_TERMINATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-829">758 (0x2F6)</span><span class="sxs-lookup"><span data-stu-id="97216-829">758 (0x2F6)</span></span>
</dt> <dt>



<span data-ttu-id="97216-830">Un processo terminato non dispone di thread da terminare.</span><span class="sxs-lookup"><span data-stu-id="97216-830">A process being terminated has no threads to terminate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-831"><span id="ERROR_PROCESS_NOT_IN_JOB"></span><span id="error_process_not_in_job"></span>**\_processo \_ di errore non \_ nel \_ processo**</span><span class="sxs-lookup"><span data-stu-id="97216-831"><span id="ERROR_PROCESS_NOT_IN_JOB"></span><span id="error_process_not_in_job"></span>**ERROR\_PROCESS\_NOT\_IN\_JOB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-832">759 (0x2F7)</span><span class="sxs-lookup"><span data-stu-id="97216-832">759 (0x2F7)</span></span>
</dt> <dt>



<span data-ttu-id="97216-833">Il processo specificato non fa parte di un processo.</span><span class="sxs-lookup"><span data-stu-id="97216-833">The specified process is not part of a job.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-834"><span id="ERROR_PROCESS_IN_JOB"></span><span id="error_process_in_job"></span>**\_processo \_ di errore nel processo \_**</span><span class="sxs-lookup"><span data-stu-id="97216-834"><span id="ERROR_PROCESS_IN_JOB"></span><span id="error_process_in_job"></span>**ERROR\_PROCESS\_IN\_JOB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-835">760 (0x2F8)</span><span class="sxs-lookup"><span data-stu-id="97216-835">760 (0x2F8)</span></span>
</dt> <dt>



<span data-ttu-id="97216-836">Il processo specificato fa parte di un processo.</span><span class="sxs-lookup"><span data-stu-id="97216-836">The specified process is part of a job.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-837"><span id="ERROR_VOLSNAP_HIBERNATE_READY"></span><span id="error_volsnap_hibernate_ready"></span>**ERRORE \_ VolSnap \_ ibernato \_ pronto**</span><span class="sxs-lookup"><span data-stu-id="97216-837"><span id="ERROR_VOLSNAP_HIBERNATE_READY"></span><span id="error_volsnap_hibernate_ready"></span>**ERROR\_VOLSNAP\_HIBERNATE\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-838">761 (0x2F9)</span><span class="sxs-lookup"><span data-stu-id="97216-838">761 (0x2F9)</span></span>
</dt> <dt>



<span data-ttu-id="97216-839">{Servizio Copia Shadow del volume} Il sistema è ora pronto per l'ibernazione.</span><span class="sxs-lookup"><span data-stu-id="97216-839">{Volume Shadow Copy Service} The system is now ready for hibernation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-840"><span id="ERROR_FSFILTER_OP_COMPLETED_SUCCESSFULLY"></span><span id="error_fsfilter_op_completed_successfully"></span>**ERRORE \_ FSFILTER \_ op \_ completato \_ correttamente**</span><span class="sxs-lookup"><span data-stu-id="97216-840"><span id="ERROR_FSFILTER_OP_COMPLETED_SUCCESSFULLY"></span><span id="error_fsfilter_op_completed_successfully"></span>**ERROR\_FSFILTER\_OP\_COMPLETED\_SUCCESSFULLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-841">762 (0x2FA)</span><span class="sxs-lookup"><span data-stu-id="97216-841">762 (0x2FA)</span></span>
</dt> <dt>



<span data-ttu-id="97216-842">Un driver di filtro file system o file system ha completato un'operazione FsFilter.</span><span class="sxs-lookup"><span data-stu-id="97216-842">A file system or file system filter driver has successfully completed an FsFilter operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-843"><span id="ERROR_INTERRUPT_VECTOR_ALREADY_CONNECTED"></span><span id="error_interrupt_vector_already_connected"></span>**il \_ vettore di interrupt errore è \_ \_ già \_ connesso**</span><span class="sxs-lookup"><span data-stu-id="97216-843"><span id="ERROR_INTERRUPT_VECTOR_ALREADY_CONNECTED"></span><span id="error_interrupt_vector_already_connected"></span>**ERROR\_INTERRUPT\_VECTOR\_ALREADY\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-844">763 (0x2FB)</span><span class="sxs-lookup"><span data-stu-id="97216-844">763 (0x2FB)</span></span>
</dt> <dt>



<span data-ttu-id="97216-845">Il vettore di interrupt specificato è già connesso.</span><span class="sxs-lookup"><span data-stu-id="97216-845">The specified interrupt vector was already connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-846"><span id="ERROR_INTERRUPT_STILL_CONNECTED"></span><span id="error_interrupt_still_connected"></span>**ERRORE di \_ interrupt \_ ancora \_ connesso**</span><span class="sxs-lookup"><span data-stu-id="97216-846"><span id="ERROR_INTERRUPT_STILL_CONNECTED"></span><span id="error_interrupt_still_connected"></span>**ERROR\_INTERRUPT\_STILL\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-847">764 (0x2FC)</span><span class="sxs-lookup"><span data-stu-id="97216-847">764 (0x2FC)</span></span>
</dt> <dt>



<span data-ttu-id="97216-848">Il vettore di interrupt specificato è ancora connesso.</span><span class="sxs-lookup"><span data-stu-id="97216-848">The specified interrupt vector is still connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-849"><span id="ERROR_WAIT_FOR_OPLOCK"></span><span id="error_wait_for_oplock"></span>**ERRORE \_ \_ di attesa per \_ blocco opportunistico**</span><span class="sxs-lookup"><span data-stu-id="97216-849"><span id="ERROR_WAIT_FOR_OPLOCK"></span><span id="error_wait_for_oplock"></span>**ERROR\_WAIT\_FOR\_OPLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-850">765 (0x2FD)</span><span class="sxs-lookup"><span data-stu-id="97216-850">765 (0x2FD)</span></span>
</dt> <dt>



<span data-ttu-id="97216-851">Un'operazione è bloccata in attesa di un blocco opportunistico.</span><span class="sxs-lookup"><span data-stu-id="97216-851">An operation is blocked waiting for an oplock.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-852"><span id="ERROR_DBG_EXCEPTION_HANDLED"></span><span id="error_dbg_exception_handled"></span>**\_eccezione DBG di errore \_ \_ gestita**</span><span class="sxs-lookup"><span data-stu-id="97216-852"><span id="ERROR_DBG_EXCEPTION_HANDLED"></span><span id="error_dbg_exception_handled"></span>**ERROR\_DBG\_EXCEPTION\_HANDLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-853">766 (0x2FE)</span><span class="sxs-lookup"><span data-stu-id="97216-853">766 (0x2FE)</span></span>
</dt> <dt>



<span data-ttu-id="97216-854">Eccezione gestita dal debugger.</span><span class="sxs-lookup"><span data-stu-id="97216-854">Debugger handled exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-855"><span id="ERROR_DBG_CONTINUE"></span><span id="error_dbg_continue"></span>**ERRORE \_ dbg \_ continuare**</span><span class="sxs-lookup"><span data-stu-id="97216-855"><span id="ERROR_DBG_CONTINUE"></span><span id="error_dbg_continue"></span>**ERROR\_DBG\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-856">767 (0x2FF)</span><span class="sxs-lookup"><span data-stu-id="97216-856">767 (0x2FF)</span></span>
</dt> <dt>



<span data-ttu-id="97216-857">Debugger prosegue.</span><span class="sxs-lookup"><span data-stu-id="97216-857">Debugger continued.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-858"><span id="ERROR_CALLBACK_POP_STACK"></span><span id="error_callback_pop_stack"></span>**\_ \_ pop stack callback \_ errore**</span><span class="sxs-lookup"><span data-stu-id="97216-858"><span id="ERROR_CALLBACK_POP_STACK"></span><span id="error_callback_pop_stack"></span>**ERROR\_CALLBACK\_POP\_STACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-859">768 (0x300)</span><span class="sxs-lookup"><span data-stu-id="97216-859">768 (0x300)</span></span>
</dt> <dt>



<span data-ttu-id="97216-860">Si è verificata un'eccezione in un callback in modalità utente e il frame di callback del kernel deve essere rimosso.</span><span class="sxs-lookup"><span data-stu-id="97216-860">An exception occurred in a user mode callback and the kernel callback frame should be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-861"><span id="ERROR_COMPRESSION_DISABLED"></span><span id="error_compression_disabled"></span>**compressione degli errori \_ \_ disabilitata**</span><span class="sxs-lookup"><span data-stu-id="97216-861"><span id="ERROR_COMPRESSION_DISABLED"></span><span id="error_compression_disabled"></span>**ERROR\_COMPRESSION\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-862">769 (0x301)</span><span class="sxs-lookup"><span data-stu-id="97216-862">769 (0x301)</span></span>
</dt> <dt>



<span data-ttu-id="97216-863">La compressione è disabilitata per questo volume.</span><span class="sxs-lookup"><span data-stu-id="97216-863">Compression is disabled for this volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-864"><span id="ERROR_CANTFETCHBACKWARDS"></span><span id="error_cantfetchbackwards"></span>**ERRORE \_ CANTFETCHBACKWARDS**</span><span class="sxs-lookup"><span data-stu-id="97216-864"><span id="ERROR_CANTFETCHBACKWARDS"></span><span id="error_cantfetchbackwards"></span>**ERROR\_CANTFETCHBACKWARDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-865">770 (0x302)</span><span class="sxs-lookup"><span data-stu-id="97216-865">770 (0x302)</span></span>
</dt> <dt>



<span data-ttu-id="97216-866">Il provider di dati non è in grado di recuperare le versioni precedenti di un set di risultati.</span><span class="sxs-lookup"><span data-stu-id="97216-866">The data provider cannot fetch backwards through a result set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-867"><span id="ERROR_CANTSCROLLBACKWARDS"></span><span id="error_cantscrollbackwards"></span>**ERRORE \_ CANTSCROLLBACKWARDS**</span><span class="sxs-lookup"><span data-stu-id="97216-867"><span id="ERROR_CANTSCROLLBACKWARDS"></span><span id="error_cantscrollbackwards"></span>**ERROR\_CANTSCROLLBACKWARDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-868">771 (0x303)</span><span class="sxs-lookup"><span data-stu-id="97216-868">771 (0x303)</span></span>
</dt> <dt>



<span data-ttu-id="97216-869">Il provider di dati non è in grado di scorrere indietro di un set di risultati.</span><span class="sxs-lookup"><span data-stu-id="97216-869">The data provider cannot scroll backwards through a result set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-870"><span id="ERROR_ROWSNOTRELEASED"></span><span id="error_rowsnotreleased"></span>**ERRORE \_ ROWSNOTRELEASED**</span><span class="sxs-lookup"><span data-stu-id="97216-870"><span id="ERROR_ROWSNOTRELEASED"></span><span id="error_rowsnotreleased"></span>**ERROR\_ROWSNOTRELEASED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-871">772 (0x304)</span><span class="sxs-lookup"><span data-stu-id="97216-871">772 (0x304)</span></span>
</dt> <dt>



<span data-ttu-id="97216-872">Il provider di dati richiede che i dati recuperati in precedenza vengano rilasciati prima di richiedere più dati.</span><span class="sxs-lookup"><span data-stu-id="97216-872">The data provider requires that previously fetched data is released before asking for more data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-873"><span id="ERROR_BAD_ACCESSOR_FLAGS"></span><span id="error_bad_accessor_flags"></span>**\_flag della \_ funzione di accesso ERRAta Error \_**</span><span class="sxs-lookup"><span data-stu-id="97216-873"><span id="ERROR_BAD_ACCESSOR_FLAGS"></span><span id="error_bad_accessor_flags"></span>**ERROR\_BAD\_ACCESSOR\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-874">773 (0x305)</span><span class="sxs-lookup"><span data-stu-id="97216-874">773 (0x305)</span></span>
</dt> <dt>



<span data-ttu-id="97216-875">Il provider di dati non è stato in grado di interpretare i flag impostati per un'associazione di colonna in una funzione di accesso.</span><span class="sxs-lookup"><span data-stu-id="97216-875">The data provider was not able to interpret the flags set for a column binding in an accessor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-876"><span id="ERROR_ERRORS_ENCOUNTERED"></span><span id="error_errors_encountered"></span>**\_errori \_ rilevati**</span><span class="sxs-lookup"><span data-stu-id="97216-876"><span id="ERROR_ERRORS_ENCOUNTERED"></span><span id="error_errors_encountered"></span>**ERROR\_ERRORS\_ENCOUNTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-877">774 (0x306)</span><span class="sxs-lookup"><span data-stu-id="97216-877">774 (0x306)</span></span>
</dt> <dt>



<span data-ttu-id="97216-878">Si sono verificati uno o più errori durante l'elaborazione della richiesta.</span><span class="sxs-lookup"><span data-stu-id="97216-878">One or more errors occurred while processing the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-879"><span id="ERROR_NOT_CAPABLE"></span><span id="error_not_capable"></span>**ERRORE \_ non \_ idoneo**</span><span class="sxs-lookup"><span data-stu-id="97216-879"><span id="ERROR_NOT_CAPABLE"></span><span id="error_not_capable"></span>**ERROR\_NOT\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-880">775 (0x307)</span><span class="sxs-lookup"><span data-stu-id="97216-880">775 (0x307)</span></span>
</dt> <dt>



<span data-ttu-id="97216-881">L'implementazione non è in grado di eseguire la richiesta.</span><span class="sxs-lookup"><span data-stu-id="97216-881">The implementation is not capable of performing the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-882"><span id="ERROR_REQUEST_OUT_OF_SEQUENCE"></span><span id="error_request_out_of_sequence"></span>**\_richiesta \_ di errore \_ fuori \_ sequenza**</span><span class="sxs-lookup"><span data-stu-id="97216-882"><span id="ERROR_REQUEST_OUT_OF_SEQUENCE"></span><span id="error_request_out_of_sequence"></span>**ERROR\_REQUEST\_OUT\_OF\_SEQUENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-883">776 (0x308)</span><span class="sxs-lookup"><span data-stu-id="97216-883">776 (0x308)</span></span>
</dt> <dt>



<span data-ttu-id="97216-884">Il client di un componente ha richiesto un'operazione non valida in base allo stato dell'istanza del componente.</span><span class="sxs-lookup"><span data-stu-id="97216-884">The client of a component requested an operation which is not valid given the state of the component instance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-885"><span id="ERROR_VERSION_PARSE_ERROR"></span><span id="error_version_parse_error"></span>**errore di \_ analisi della versione errore \_ \_**</span><span class="sxs-lookup"><span data-stu-id="97216-885"><span id="ERROR_VERSION_PARSE_ERROR"></span><span id="error_version_parse_error"></span>**ERROR\_VERSION\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-886">777 (0x309)</span><span class="sxs-lookup"><span data-stu-id="97216-886">777 (0x309)</span></span>
</dt> <dt>



<span data-ttu-id="97216-887">Non è stato possibile analizzare un numero di versione.</span><span class="sxs-lookup"><span data-stu-id="97216-887">A version number could not be parsed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-888"><span id="ERROR_BADSTARTPOSITION"></span><span id="error_badstartposition"></span>**ERRORE \_ BADSTARTPOSITION**</span><span class="sxs-lookup"><span data-stu-id="97216-888"><span id="ERROR_BADSTARTPOSITION"></span><span id="error_badstartposition"></span>**ERROR\_BADSTARTPOSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-889">778 (0x30A)</span><span class="sxs-lookup"><span data-stu-id="97216-889">778 (0x30A)</span></span>
</dt> <dt>



<span data-ttu-id="97216-890">La posizione iniziale dell'iteratore non è valida.</span><span class="sxs-lookup"><span data-stu-id="97216-890">The iterator's start position is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-891"><span id="ERROR_MEMORY_HARDWARE"></span><span id="error_memory_hardware"></span>**\_hardware memoria \_ errore**</span><span class="sxs-lookup"><span data-stu-id="97216-891"><span id="ERROR_MEMORY_HARDWARE"></span><span id="error_memory_hardware"></span>**ERROR\_MEMORY\_HARDWARE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-892">779 (0x30B)</span><span class="sxs-lookup"><span data-stu-id="97216-892">779 (0x30B)</span></span>
</dt> <dt>



<span data-ttu-id="97216-893">L'hardware ha segnalato un errore di memoria non correggibile.</span><span class="sxs-lookup"><span data-stu-id="97216-893">The hardware has reported an uncorrectable memory error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-894"><span id="ERROR_DISK_REPAIR_DISABLED"></span><span id="error_disk_repair_disabled"></span>**ripristino del disco di errore \_ \_ \_ disabilitato**</span><span class="sxs-lookup"><span data-stu-id="97216-894"><span id="ERROR_DISK_REPAIR_DISABLED"></span><span id="error_disk_repair_disabled"></span>**ERROR\_DISK\_REPAIR\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-895">780 (0x30C)</span><span class="sxs-lookup"><span data-stu-id="97216-895">780 (0x30C)</span></span>
</dt> <dt>



<span data-ttu-id="97216-896">È stata richiesta l'abilitazione dell'operazione di correzione automatica.</span><span class="sxs-lookup"><span data-stu-id="97216-896">The attempted operation required self healing to be enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-897"><span id="ERROR_INSUFFICIENT_RESOURCE_FOR_SPECIFIED_SHARED_SECTION_SIZE"></span><span id="error_insufficient_resource_for_specified_shared_section_size"></span>**ERRORE \_ \_ di risorsa insufficiente \_ per le \_ \_ dimensioni di sezione condivise specificate \_ \_**</span><span class="sxs-lookup"><span data-stu-id="97216-897"><span id="ERROR_INSUFFICIENT_RESOURCE_FOR_SPECIFIED_SHARED_SECTION_SIZE"></span><span id="error_insufficient_resource_for_specified_shared_section_size"></span>**ERROR\_INSUFFICIENT\_RESOURCE\_FOR\_SPECIFIED\_SHARED\_SECTION\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-898">781 (0x30D)</span><span class="sxs-lookup"><span data-stu-id="97216-898">781 (0x30D)</span></span>
</dt> <dt>



<span data-ttu-id="97216-899">Si è verificato un errore nell'heap del desktop durante l'allocazione della memoria della sessione.</span><span class="sxs-lookup"><span data-stu-id="97216-899">The Desktop heap encountered an error while allocating session memory.</span></span> <span data-ttu-id="97216-900">Sono disponibili ulteriori informazioni nel registro eventi di sistema.</span><span class="sxs-lookup"><span data-stu-id="97216-900">There is more information in the system event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-901"><span id="ERROR_SYSTEM_POWERSTATE_TRANSITION"></span><span id="error_system_powerstate_transition"></span>**\_ \_ transizione PowerState sistema di errore \_**</span><span class="sxs-lookup"><span data-stu-id="97216-901"><span id="ERROR_SYSTEM_POWERSTATE_TRANSITION"></span><span id="error_system_powerstate_transition"></span>**ERROR\_SYSTEM\_POWERSTATE\_TRANSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-902">782 (0x30E)</span><span class="sxs-lookup"><span data-stu-id="97216-902">782 (0x30E)</span></span>
</dt> <dt>



<span data-ttu-id="97216-903">Lo stato di alimentazione del sistema è in fase di transizione da %2 a %3.</span><span class="sxs-lookup"><span data-stu-id="97216-903">The system power state is transitioning from %2 to %3.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-904"><span id="ERROR_SYSTEM_POWERSTATE_COMPLEX_TRANSITION"></span><span id="error_system_powerstate_complex_transition"></span>**ERRORE \_ di \_ PowerState sistema di \_ \_ transizione complessa**</span><span class="sxs-lookup"><span data-stu-id="97216-904"><span id="ERROR_SYSTEM_POWERSTATE_COMPLEX_TRANSITION"></span><span id="error_system_powerstate_complex_transition"></span>**ERROR\_SYSTEM\_POWERSTATE\_COMPLEX\_TRANSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-905">783 (0x30F)</span><span class="sxs-lookup"><span data-stu-id="97216-905">783 (0x30F)</span></span>
</dt> <dt>



<span data-ttu-id="97216-906">Lo stato di alimentazione del sistema è in fase di transizione da %2 a %3, ma è possibile immettere %4.</span><span class="sxs-lookup"><span data-stu-id="97216-906">The system power state is transitioning from %2 to %3 but could enter %4.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-907"><span id="ERROR_MCA_EXCEPTION"></span><span id="error_mca_exception"></span>**ERRORE \_ MCA \_ eccezione**</span><span class="sxs-lookup"><span data-stu-id="97216-907"><span id="ERROR_MCA_EXCEPTION"></span><span id="error_mca_exception"></span>**ERROR\_MCA\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-908">784 (0x310)</span><span class="sxs-lookup"><span data-stu-id="97216-908">784 (0x310)</span></span>
</dt> <dt>



<span data-ttu-id="97216-909">Un thread viene inviato con l'eccezione MCA a causa di MCA.</span><span class="sxs-lookup"><span data-stu-id="97216-909">A thread is getting dispatched with MCA EXCEPTION because of MCA.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-910"><span id="ERROR_ACCESS_AUDIT_BY_POLICY"></span><span id="error_access_audit_by_policy"></span>**\_ \_ controllo degli errori \_ di accesso per \_ criterio**</span><span class="sxs-lookup"><span data-stu-id="97216-910"><span id="ERROR_ACCESS_AUDIT_BY_POLICY"></span><span id="error_access_audit_by_policy"></span>**ERROR\_ACCESS\_AUDIT\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-911">785 (0x311)</span><span class="sxs-lookup"><span data-stu-id="97216-911">785 (0x311)</span></span>
</dt> <dt>



<span data-ttu-id="97216-912">L'accesso a %1 è stato monitorato dalla regola dei criteri %2.</span><span class="sxs-lookup"><span data-stu-id="97216-912">Access to %1 is monitored by policy rule %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-913"><span id="ERROR_ACCESS_DISABLED_NO_SAFER_UI_BY_POLICY"></span><span id="error_access_disabled_no_safer_ui_by_policy"></span>**\_accesso agli errori \_ disabilitato \_ senza \_ \_ interfaccia utente sicura \_ per \_ criterio**</span><span class="sxs-lookup"><span data-stu-id="97216-913"><span id="ERROR_ACCESS_DISABLED_NO_SAFER_UI_BY_POLICY"></span><span id="error_access_disabled_no_safer_ui_by_policy"></span>**ERROR\_ACCESS\_DISABLED\_NO\_SAFER\_UI\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-914">786 (0x312)</span><span class="sxs-lookup"><span data-stu-id="97216-914">786 (0x312)</span></span>
</dt> <dt>



<span data-ttu-id="97216-915">L'accesso a %1 è stato limitato dall'amministratore dalla regola dei criteri %2.</span><span class="sxs-lookup"><span data-stu-id="97216-915">Access to %1 has been restricted by your Administrator by policy rule %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-916"><span id="ERROR_ABANDON_HIBERFILE"></span><span id="error_abandon_hiberfile"></span>**errore durante l' \_ abbandono di \_ HIBERFILE**</span><span class="sxs-lookup"><span data-stu-id="97216-916"><span id="ERROR_ABANDON_HIBERFILE"></span><span id="error_abandon_hiberfile"></span>**ERROR\_ABANDON\_HIBERFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-917">787 (0x313)</span><span class="sxs-lookup"><span data-stu-id="97216-917">787 (0x313)</span></span>
</dt> <dt>



<span data-ttu-id="97216-918">Un file di ibernazione valido è stato invalidato e deve essere abbandonato.</span><span class="sxs-lookup"><span data-stu-id="97216-918">A valid hibernation file has been invalidated and should be abandoned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-919"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_DISCONNECTED"></span><span id="error_lost_writebehind_data_network_disconnected"></span>**errore durante la \_ perdita della \_ \_ rete dati WRITEBEHIND \_ \_ disconnessa**</span><span class="sxs-lookup"><span data-stu-id="97216-919"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_DISCONNECTED"></span><span id="error_lost_writebehind_data_network_disconnected"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA\_NETWORK\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-920">788 (0x314)</span><span class="sxs-lookup"><span data-stu-id="97216-920">788 (0x314)</span></span>
</dt> <dt>



<span data-ttu-id="97216-921">{Scrittura ritardata non riuscita} Windows non è riuscito a salvare tutti i dati per il file% HS; i dati sono andati persi.</span><span class="sxs-lookup"><span data-stu-id="97216-921">{Delayed Write Failed} Windows was unable to save all the data for the file %hs; the data has been lost.</span></span> <span data-ttu-id="97216-922">Questo errore può essere causato da problemi di connettività di rete.</span><span class="sxs-lookup"><span data-stu-id="97216-922">This error may be caused by network connectivity issues.</span></span> <span data-ttu-id="97216-923">Provare a salvare il file altrove.</span><span class="sxs-lookup"><span data-stu-id="97216-923">Please try to save this file elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-924"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_SERVER_ERROR"></span><span id="error_lost_writebehind_data_network_server_error"></span>**ERRORE durante la \_ perdita di \_ WRITEBEHIND \_ data \_ Network \_ server \_ Error**</span><span class="sxs-lookup"><span data-stu-id="97216-924"><span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_SERVER_ERROR"></span><span id="error_lost_writebehind_data_network_server_error"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA\_NETWORK\_SERVER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-925">789 (0x315)</span><span class="sxs-lookup"><span data-stu-id="97216-925">789 (0x315)</span></span>
</dt> <dt>



<span data-ttu-id="97216-926">{Scrittura ritardata non riuscita} Windows non è riuscito a salvare tutti i dati per il file% HS; i dati sono andati persi.</span><span class="sxs-lookup"><span data-stu-id="97216-926">{Delayed Write Failed} Windows was unable to save all the data for the file %hs; the data has been lost.</span></span> <span data-ttu-id="97216-927">Questo errore è stato restituito dal server in cui si trova il file.</span><span class="sxs-lookup"><span data-stu-id="97216-927">This error was returned by the server on which the file exists.</span></span> <span data-ttu-id="97216-928">Provare a salvare il file altrove.</span><span class="sxs-lookup"><span data-stu-id="97216-928">Please try to save this file elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-929"><span id="ERROR_LOST_WRITEBEHIND_DATA_LOCAL_DISK_ERROR"></span><span id="error_lost_writebehind_data_local_disk_error"></span>**errore durante la \_ perdita \_ \_ \_ del \_ disco locale di dati WRITEBEHIND \_**</span><span class="sxs-lookup"><span data-stu-id="97216-929"><span id="ERROR_LOST_WRITEBEHIND_DATA_LOCAL_DISK_ERROR"></span><span id="error_lost_writebehind_data_local_disk_error"></span>**ERROR\_LOST\_WRITEBEHIND\_DATA\_LOCAL\_DISK\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-930">790 (0x316)</span><span class="sxs-lookup"><span data-stu-id="97216-930">790 (0x316)</span></span>
</dt> <dt>



<span data-ttu-id="97216-931">{Scrittura ritardata non riuscita} Windows non è riuscito a salvare tutti i dati per il file% HS; i dati sono andati persi.</span><span class="sxs-lookup"><span data-stu-id="97216-931">{Delayed Write Failed} Windows was unable to save all the data for the file %hs; the data has been lost.</span></span> <span data-ttu-id="97216-932">Questo errore può essere causato dal fatto che il dispositivo è stato rimosso o il supporto è protetto da scrittura.</span><span class="sxs-lookup"><span data-stu-id="97216-932">This error may be caused if the device has been removed or the media is write-protected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-933"><span id="ERROR_BAD_MCFG_TABLE"></span><span id="error_bad_mcfg_table"></span>**ERRORE \_ nella \_ tabella MCFG non valida \_**</span><span class="sxs-lookup"><span data-stu-id="97216-933"><span id="ERROR_BAD_MCFG_TABLE"></span><span id="error_bad_mcfg_table"></span>**ERROR\_BAD\_MCFG\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-934">791 (0x317)</span><span class="sxs-lookup"><span data-stu-id="97216-934">791 (0x317)</span></span>
</dt> <dt>



<span data-ttu-id="97216-935">Le risorse necessarie per questo dispositivo sono in conflitto con la tabella MCFG.</span><span class="sxs-lookup"><span data-stu-id="97216-935">The resources required for this device conflict with the MCFG table.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-936"><span id="ERROR_DISK_REPAIR_REDIRECTED"></span><span id="error_disk_repair_redirected"></span>**ripristino del disco di errore \_ \_ \_ reindirizzato**</span><span class="sxs-lookup"><span data-stu-id="97216-936"><span id="ERROR_DISK_REPAIR_REDIRECTED"></span><span id="error_disk_repair_redirected"></span>**ERROR\_DISK\_REPAIR\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-937">792 (0x318)</span><span class="sxs-lookup"><span data-stu-id="97216-937">792 (0x318)</span></span>
</dt> <dt>



<span data-ttu-id="97216-938">Non è stato possibile eseguire il ripristino del volume mentre è in linea.</span><span class="sxs-lookup"><span data-stu-id="97216-938">The volume repair could not be performed while it is online.</span></span> <span data-ttu-id="97216-939">Pianificare per portare il volume offline in modo che possa essere ripristinato.</span><span class="sxs-lookup"><span data-stu-id="97216-939">Please schedule to take the volume offline so that it can be repaired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-940"><span id="ERROR_DISK_REPAIR_UNSUCCESSFUL"></span><span id="error_disk_repair_unsuccessful"></span>**correzione del disco di errore non \_ \_ \_ riuscita**</span><span class="sxs-lookup"><span data-stu-id="97216-940"><span id="ERROR_DISK_REPAIR_UNSUCCESSFUL"></span><span id="error_disk_repair_unsuccessful"></span>**ERROR\_DISK\_REPAIR\_UNSUCCESSFUL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-941">793 (0x319)</span><span class="sxs-lookup"><span data-stu-id="97216-941">793 (0x319)</span></span>
</dt> <dt>



<span data-ttu-id="97216-942">Il ripristino del volume non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="97216-942">The volume repair was not successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-943"><span id="ERROR_CORRUPT_LOG_OVERFULL"></span><span id="error_corrupt_log_overfull"></span>**ERRORE \_ di \_ log \_ danneggiato**</span><span class="sxs-lookup"><span data-stu-id="97216-943"><span id="ERROR_CORRUPT_LOG_OVERFULL"></span><span id="error_corrupt_log_overfull"></span>**ERROR\_CORRUPT\_LOG\_OVERFULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-944">794 (0x31A)</span><span class="sxs-lookup"><span data-stu-id="97216-944">794 (0x31A)</span></span>
</dt> <dt>



<span data-ttu-id="97216-945">Uno dei log di danneggiamento del volume è pieno.</span><span class="sxs-lookup"><span data-stu-id="97216-945">One of the volume corruption logs is full.</span></span> <span data-ttu-id="97216-946">Ulteriori danneggiamenti che potrebbero essere rilevati non verranno registrati.</span><span class="sxs-lookup"><span data-stu-id="97216-946">Further corruptions that may be detected won't be logged.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-947"><span id="ERROR_CORRUPT_LOG_CORRUPTED"></span><span id="error_corrupt_log_corrupted"></span>**ERRORE \_ del \_ log \_ danneggiato**</span><span class="sxs-lookup"><span data-stu-id="97216-947"><span id="ERROR_CORRUPT_LOG_CORRUPTED"></span><span id="error_corrupt_log_corrupted"></span>**ERROR\_CORRUPT\_LOG\_CORRUPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-948">795 (0x31B)</span><span class="sxs-lookup"><span data-stu-id="97216-948">795 (0x31B)</span></span>
</dt> <dt>



<span data-ttu-id="97216-949">Uno dei log di danneggiamento del volume è danneggiato internamente ed è necessario ricrearlo.</span><span class="sxs-lookup"><span data-stu-id="97216-949">One of the volume corruption logs is internally corrupted and needs to be recreated.</span></span> <span data-ttu-id="97216-950">Il volume può contenere danneggiamenti non rilevati e deve essere analizzato.</span><span class="sxs-lookup"><span data-stu-id="97216-950">The volume may contain undetected corruptions and must be scanned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-951"><span id="ERROR_CORRUPT_LOG_UNAVAILABLE"></span><span id="error_corrupt_log_unavailable"></span>**ERRORE \_ del \_ log danneggiato non \_ disponibile**</span><span class="sxs-lookup"><span data-stu-id="97216-951"><span id="ERROR_CORRUPT_LOG_UNAVAILABLE"></span><span id="error_corrupt_log_unavailable"></span>**ERROR\_CORRUPT\_LOG\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-952">796 (0x31C)</span><span class="sxs-lookup"><span data-stu-id="97216-952">796 (0x31C)</span></span>
</dt> <dt>



<span data-ttu-id="97216-953">Uno dei log di danneggiamento del volume non è disponibile per essere utilizzato.</span><span class="sxs-lookup"><span data-stu-id="97216-953">One of the volume corruption logs is unavailable for being operated on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-954"><span id="ERROR_CORRUPT_LOG_DELETED_FULL"></span><span id="error_corrupt_log_deleted_full"></span>**ERRORE \_ di \_ log danneggiato \_ eliminato \_**</span><span class="sxs-lookup"><span data-stu-id="97216-954"><span id="ERROR_CORRUPT_LOG_DELETED_FULL"></span><span id="error_corrupt_log_deleted_full"></span>**ERROR\_CORRUPT\_LOG\_DELETED\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-955">797 (0x31D)</span><span class="sxs-lookup"><span data-stu-id="97216-955">797 (0x31D)</span></span>
</dt> <dt>



<span data-ttu-id="97216-956">Uno dei log di danneggiamento del volume è stato eliminato mentre erano ancora presenti record di danneggiamento.</span><span class="sxs-lookup"><span data-stu-id="97216-956">One of the volume corruption logs was deleted while still having corruption records in them.</span></span> <span data-ttu-id="97216-957">Il volume contiene i danneggiamenti rilevati e deve essere analizzato.</span><span class="sxs-lookup"><span data-stu-id="97216-957">The volume contains detected corruptions and must be scanned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-958"><span id="ERROR_CORRUPT_LOG_CLEARED"></span><span id="error_corrupt_log_cleared"></span>**ERRORE \_ di \_ log danneggiato \_ cancellato**</span><span class="sxs-lookup"><span data-stu-id="97216-958"><span id="ERROR_CORRUPT_LOG_CLEARED"></span><span id="error_corrupt_log_cleared"></span>**ERROR\_CORRUPT\_LOG\_CLEARED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-959">798 (0x31E)</span><span class="sxs-lookup"><span data-stu-id="97216-959">798 (0x31E)</span></span>
</dt> <dt>



<span data-ttu-id="97216-960">Uno dei log di danneggiamento del volume è stato cancellato da CHKDSK e non contiene più i danneggiamenti reali.</span><span class="sxs-lookup"><span data-stu-id="97216-960">One of the volume corruption logs was cleared by chkdsk and no longer contains real corruptions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-961"><span id="ERROR_ORPHAN_NAME_EXHAUSTED"></span><span id="error_orphan_name_exhausted"></span>**ERRORE \_ nome orfano \_ \_ esaurito**</span><span class="sxs-lookup"><span data-stu-id="97216-961"><span id="ERROR_ORPHAN_NAME_EXHAUSTED"></span><span id="error_orphan_name_exhausted"></span>**ERROR\_ORPHAN\_NAME\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-962">799 (0x31F)</span><span class="sxs-lookup"><span data-stu-id="97216-962">799 (0x31F)</span></span>
</dt> <dt>



<span data-ttu-id="97216-963">I file orfani esistono nel volume, ma non possono essere recuperati perché non è stato possibile creare altri nuovi nomi nella directory di ripristino.</span><span class="sxs-lookup"><span data-stu-id="97216-963">Orphaned files exist on the volume but could not be recovered because no more new names could be created in the recovery directory.</span></span> <span data-ttu-id="97216-964">I file devono essere spostati dalla directory di ripristino.</span><span class="sxs-lookup"><span data-stu-id="97216-964">Files must be moved from the recovery directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-965"><span id="ERROR_OPLOCK_SWITCHED_TO_NEW_HANDLE"></span><span id="error_oplock_switched_to_new_handle"></span>**ERRORE \_ blocco opportunistico \_ passato \_ al \_ nuovo \_ handle**</span><span class="sxs-lookup"><span data-stu-id="97216-965"><span id="ERROR_OPLOCK_SWITCHED_TO_NEW_HANDLE"></span><span id="error_oplock_switched_to_new_handle"></span>**ERROR\_OPLOCK\_SWITCHED\_TO\_NEW\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-966">800 (0x320)</span><span class="sxs-lookup"><span data-stu-id="97216-966">800 (0x320)</span></span>
</dt> <dt>



<span data-ttu-id="97216-967">Il blocco opportunistico associato a questo handle è ora associato a un handle diverso.</span><span class="sxs-lookup"><span data-stu-id="97216-967">The oplock that was associated with this handle is now associated with a different handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-968"><span id="ERROR_CANNOT_GRANT_REQUESTED_OPLOCK"></span><span id="error_cannot_grant_requested_oplock"></span>**ERRORE \_ non può \_ concedere il \_ \_ blocco opportunistico richiesto**</span><span class="sxs-lookup"><span data-stu-id="97216-968"><span id="ERROR_CANNOT_GRANT_REQUESTED_OPLOCK"></span><span id="error_cannot_grant_requested_oplock"></span>**ERROR\_CANNOT\_GRANT\_REQUESTED\_OPLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-969">801 (0x321)</span><span class="sxs-lookup"><span data-stu-id="97216-969">801 (0x321)</span></span>
</dt> <dt>



<span data-ttu-id="97216-970">Non è possibile concedere un blocco opportunistico del livello richiesto.</span><span class="sxs-lookup"><span data-stu-id="97216-970">An oplock of the requested level cannot be granted.</span></span> <span data-ttu-id="97216-971">Potrebbe essere disponibile un blocco opportunistico di un livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="97216-971">An oplock of a lower level may be available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-972"><span id="ERROR_CANNOT_BREAK_OPLOCK"></span><span id="error_cannot_break_oplock"></span>**ERRORE \_ Impossibile \_ interrompere \_ blocco opportunistico**</span><span class="sxs-lookup"><span data-stu-id="97216-972"><span id="ERROR_CANNOT_BREAK_OPLOCK"></span><span id="error_cannot_break_oplock"></span>**ERROR\_CANNOT\_BREAK\_OPLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-973">802 (0x322)</span><span class="sxs-lookup"><span data-stu-id="97216-973">802 (0x322)</span></span>
</dt> <dt>



<span data-ttu-id="97216-974">L'operazione non è stata completata correttamente perché potrebbe causare l'interruzione di un blocco opportunistico.</span><span class="sxs-lookup"><span data-stu-id="97216-974">The operation did not complete successfully because it would cause an oplock to be broken.</span></span> <span data-ttu-id="97216-975">Il chiamante ha richiesto l'interruzione del oplock esistente.</span><span class="sxs-lookup"><span data-stu-id="97216-975">The caller has requested that existing oplocks not be broken.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-976"><span id="ERROR_OPLOCK_HANDLE_CLOSED"></span><span id="error_oplock_handle_closed"></span>**ERRORE \_ blocco opportunistico \_ handle \_ chiuso**</span><span class="sxs-lookup"><span data-stu-id="97216-976"><span id="ERROR_OPLOCK_HANDLE_CLOSED"></span><span id="error_oplock_handle_closed"></span>**ERROR\_OPLOCK\_HANDLE\_CLOSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-977">803 (0x323)</span><span class="sxs-lookup"><span data-stu-id="97216-977">803 (0x323)</span></span>
</dt> <dt>



<span data-ttu-id="97216-978">L'handle a cui è stato associato questo blocco opportunistico è stato chiuso.</span><span class="sxs-lookup"><span data-stu-id="97216-978">The handle with which this oplock was associated has been closed.</span></span> <span data-ttu-id="97216-979">Il blocco opportunistico è ora rotto.</span><span class="sxs-lookup"><span data-stu-id="97216-979">The oplock is now broken.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-980"><span id="ERROR_NO_ACE_CONDITION"></span><span id="error_no_ace_condition"></span>**ERRORE \_ Nessuna \_ \_ condizione ACE**</span><span class="sxs-lookup"><span data-stu-id="97216-980"><span id="ERROR_NO_ACE_CONDITION"></span><span id="error_no_ace_condition"></span>**ERROR\_NO\_ACE\_CONDITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-981">804 (0x324)</span><span class="sxs-lookup"><span data-stu-id="97216-981">804 (0x324)</span></span>
</dt> <dt>



<span data-ttu-id="97216-982">La voce di controllo di accesso (ACE) specificata non contiene una condizione.</span><span class="sxs-lookup"><span data-stu-id="97216-982">The specified access control entry (ACE) does not contain a condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-983"><span id="ERROR_INVALID_ACE_CONDITION"></span><span id="error_invalid_ace_condition"></span>**ERRORE \_ \_ condizione ACE non valida \_**</span><span class="sxs-lookup"><span data-stu-id="97216-983"><span id="ERROR_INVALID_ACE_CONDITION"></span><span id="error_invalid_ace_condition"></span>**ERROR\_INVALID\_ACE\_CONDITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-984">805 (0x325)</span><span class="sxs-lookup"><span data-stu-id="97216-984">805 (0x325)</span></span>
</dt> <dt>



<span data-ttu-id="97216-985">La voce di controllo di accesso (ACE) specificata contiene una condizione non valida.</span><span class="sxs-lookup"><span data-stu-id="97216-985">The specified access control entry (ACE) contains an invalid condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-986"><span id="ERROR_FILE_HANDLE_REVOKED"></span><span id="error_file_handle_revoked"></span>**HANDLE di file di errore \_ \_ \_ revocato**</span><span class="sxs-lookup"><span data-stu-id="97216-986"><span id="ERROR_FILE_HANDLE_REVOKED"></span><span id="error_file_handle_revoked"></span>**ERROR\_FILE\_HANDLE\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-987">806 (0x326)</span><span class="sxs-lookup"><span data-stu-id="97216-987">806 (0x326)</span></span>
</dt> <dt>



<span data-ttu-id="97216-988">L'accesso all'handle di file specificato è stato revocato.</span><span class="sxs-lookup"><span data-stu-id="97216-988">Access to the specified file handle has been revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-989"><span id="ERROR_IMAGE_AT_DIFFERENT_BASE"></span><span id="error_image_at_different_base"></span>**\_immagine \_ di errore con \_ \_ base diversa**</span><span class="sxs-lookup"><span data-stu-id="97216-989"><span id="ERROR_IMAGE_AT_DIFFERENT_BASE"></span><span id="error_image_at_different_base"></span>**ERROR\_IMAGE\_AT\_DIFFERENT\_BASE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-990">807 (0x327)</span><span class="sxs-lookup"><span data-stu-id="97216-990">807 (0x327)</span></span>
</dt> <dt>



<span data-ttu-id="97216-991">È stato eseguito il mapping di un file di immagine a un indirizzo diverso da quello specificato nel file di immagine, ma correzioni verrà ancora eseguito automaticamente nell'immagine.</span><span class="sxs-lookup"><span data-stu-id="97216-991">An image file was mapped at a different address from the one specified in the image file but fixups will still be automatically performed on the image.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-992"><span id="ERROR_EA_ACCESS_DENIED"></span><span id="error_ea_access_denied"></span>**ERRORE \_ accesso a EA \_ \_ negato**</span><span class="sxs-lookup"><span data-stu-id="97216-992"><span id="ERROR_EA_ACCESS_DENIED"></span><span id="error_ea_access_denied"></span>**ERROR\_EA\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-993">994 (0x3E2)</span><span class="sxs-lookup"><span data-stu-id="97216-993">994 (0x3E2)</span></span>
</dt> <dt>



<span data-ttu-id="97216-994">Accesso all'attributo esteso negato.</span><span class="sxs-lookup"><span data-stu-id="97216-994">Access to the extended attribute was denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-995"><span id="ERROR_OPERATION_ABORTED"></span><span id="error_operation_aborted"></span>**operazione di errore \_ \_ interrotta**</span><span class="sxs-lookup"><span data-stu-id="97216-995"><span id="ERROR_OPERATION_ABORTED"></span><span id="error_operation_aborted"></span>**ERROR\_OPERATION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-996">995 (0x3E3)</span><span class="sxs-lookup"><span data-stu-id="97216-996">995 (0x3E3)</span></span>
</dt> <dt>



<span data-ttu-id="97216-997">L'operazione di I/O è stata interrotta a causa dell'uscita di un thread o di una richiesta dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="97216-997">The I/O operation has been aborted because of either a thread exit or an application request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-998"><span id="ERROR_IO_INCOMPLETE"></span><span id="error_io_incomplete"></span>**ERRORE \_ io \_ incompleto**</span><span class="sxs-lookup"><span data-stu-id="97216-998"><span id="ERROR_IO_INCOMPLETE"></span><span id="error_io_incomplete"></span>**ERROR\_IO\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-999">996 (0x3E4)</span><span class="sxs-lookup"><span data-stu-id="97216-999">996 (0x3E4)</span></span>
</dt> <dt>



<span data-ttu-id="97216-1000">L'evento di I/O sovrapposto non è in uno stato segnalato.</span><span class="sxs-lookup"><span data-stu-id="97216-1000">Overlapped I/O event is not in a signaled state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-1001"><span id="ERROR_IO_PENDING"></span><span id="error_io_pending"></span>**ERRORE i/o \_ \_ in sospeso**</span><span class="sxs-lookup"><span data-stu-id="97216-1001"><span id="ERROR_IO_PENDING"></span><span id="error_io_pending"></span>**ERROR\_IO\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-1002">997 (0x3E5)</span><span class="sxs-lookup"><span data-stu-id="97216-1002">997 (0x3E5)</span></span>
</dt> <dt>



<span data-ttu-id="97216-1003">Operazione di I/O sovrapposta in corso.</span><span class="sxs-lookup"><span data-stu-id="97216-1003">Overlapped I/O operation is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-1004"><span id="ERROR_NOACCESS"></span><span id="error_noaccess"></span>**ERRORE \_ NOaccess**</span><span class="sxs-lookup"><span data-stu-id="97216-1004"><span id="ERROR_NOACCESS"></span><span id="error_noaccess"></span>**ERROR\_NOACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-1005">998 (0x3E6)</span><span class="sxs-lookup"><span data-stu-id="97216-1005">998 (0x3E6)</span></span>
</dt> <dt>



<span data-ttu-id="97216-1006">Accesso non valido alla posizione di memoria.</span><span class="sxs-lookup"><span data-stu-id="97216-1006">Invalid access to memory location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97216-1007"><span id="ERROR_SWAPERROR"></span><span id="error_swaperror"></span>**ERRORE \_ SWAPERROR**</span><span class="sxs-lookup"><span data-stu-id="97216-1007"><span id="ERROR_SWAPERROR"></span><span id="error_swaperror"></span>**ERROR\_SWAPERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97216-1008">999 (0x3E7)</span><span class="sxs-lookup"><span data-stu-id="97216-1008">999 (0x3E7)</span></span>
</dt> <dt>



<span data-ttu-id="97216-1009">Errore durante l'esecuzione dell'operazione di inpaginazione.</span><span class="sxs-lookup"><span data-stu-id="97216-1009">Error performing inpage operation.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="97216-1010">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97216-1010">Requirements</span></span>



| <span data-ttu-id="97216-1011">Requisito</span><span class="sxs-lookup"><span data-stu-id="97216-1011">Requirement</span></span> | <span data-ttu-id="97216-1012">Valore</span><span class="sxs-lookup"><span data-stu-id="97216-1012">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97216-1013">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97216-1013">Minimum supported client</span></span><br/> | <span data-ttu-id="97216-1014">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="97216-1014">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="97216-1015">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97216-1015">Minimum supported server</span></span><br/> | <span data-ttu-id="97216-1016">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="97216-1016">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="97216-1017">Intestazione</span><span class="sxs-lookup"><span data-stu-id="97216-1017">Header</span></span><br/>                   | <dl> <span data-ttu-id="97216-1018"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="97216-1018"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97216-1019">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97216-1019">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97216-1020">Codici di errore di sistema</span><span class="sxs-lookup"><span data-stu-id="97216-1020">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 
