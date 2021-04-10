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
# <a name="system-error-codes-500-999"></a>Codici di errore di sistema (500-999)

> [!NOTE]
> Queste informazioni sono destinate agli sviluppatori che effettuano il debug degli errori di sistema. Per altri errori, ad esempio problemi con Windows Update, è disponibile un elenco di risorse nella pagina [codici di errore](system-error-codes.md) .

Nell'elenco seguente vengono descritti i [codici di errore di sistema](system-error-codes.md) (errori da 500 a 999). Vengono restituiti dalla funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo. Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la funzione [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il **formato \_ Message from flag \_ di \_ sistema** .

<dl> <dt>

<span id="ERROR_USER_PROFILE_LOAD"></span><span id="error_user_profile_load"></span>**errore \_ durante \_ il caricamento del profilo utente \_**
</dt> <dd> <dl> <dt>

500 (0x1F4)
</dt> <dt>



Non è possibile caricare il profilo utente.


</dt> </dl> </dd> <dt>

<span id="ERROR_ARITHMETIC_OVERFLOW"></span><span id="error_arithmetic_overflow"></span>**ERRORE \_ di \_ overflow aritmetico**
</dt> <dd> <dl> <dt>

534 (0x216)
</dt> <dt>



Il risultato aritmetico ha superato 32 bit.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_CONNECTED"></span><span id="error_pipe_connected"></span>**PIPE di errore \_ \_ connessa**
</dt> <dd> <dl> <dt>

535 (0x217)
</dt> <dt>



È presente un processo sull'altra estremità della pipe.


</dt> </dl> </dd> <dt>

<span id="ERROR_PIPE_LISTENING"></span><span id="error_pipe_listening"></span>**\_ascolto pipe di errore \_**
</dt> <dd> <dl> <dt>

536 (0x218)
</dt> <dt>



In attesa che un processo apra l'altra estremità della pipe.


</dt> </dl> </dd> <dt>

<span id="ERROR_VERIFIER_STOP"></span><span id="error_verifier_stop"></span>**arresto di errore \_ Verifier \_**
</dt> <dd> <dl> <dt>

537 (0x219)
</dt> <dt>



Application Verifier ha rilevato un errore nel processo corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_ABIOS_ERROR"></span><span id="error_abios_error"></span>**errore \_ ABIOS \_ errore**
</dt> <dd> <dl> <dt>

538 (0x21A)
</dt> <dt>



Si è verificato un errore nel sottosistema ABIOS.


</dt> </dl> </dd> <dt>

<span id="ERROR_WX86_WARNING"></span><span id="error_wx86_warning"></span>**ERRORE \_ WX86 \_ avviso**
</dt> <dd> <dl> <dt>

539 (0x21B)
</dt> <dt>



Si è verificato un avviso nel sottosistema WX86.


</dt> </dl> </dd> <dt>

<span id="ERROR_WX86_ERROR"></span><span id="error_wx86_error"></span>**Errore \_ WX86 \_ errore**
</dt> <dd> <dl> <dt>

540 (0x21C)
</dt> <dt>



Si è verificato un errore nel sottosistema WX86.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_NOT_CANCELED"></span><span id="error_timer_not_canceled"></span>**TIMER di errore \_ \_ non \_ annullato**
</dt> <dd> <dl> <dt>

541 (0x21D)
</dt> <dt>



È stato effettuato un tentativo di annullare o impostare un timer con un APC associato e il thread oggetto non è il thread che ha originariamente impostato il timer con una routine APC associata.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNWIND"></span><span id="error_unwind"></span>**\_rimozione errore**
</dt> <dd> <dl> <dt>

542 (0x21E)
</dt> <dt>



Codice eccezione di rimozione.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_STACK"></span><span id="error_bad_stack"></span>**ERRORE \_ \_ stack errato**
</dt> <dd> <dl> <dt>

543 (0x21F)
</dt> <dt>



È stato rilevato uno stack non valido o non allineato durante un'operazione di rimozione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_UNWIND_TARGET"></span><span id="error_invalid_unwind_target"></span>**ERRORE \_ destinazione di rimozione non valida \_ \_**
</dt> <dd> <dl> <dt>

544 (0x220)
</dt> <dt>



È stata rilevata una destinazione di rimozione non valida durante un'operazione di rimozione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PORT_ATTRIBUTES"></span><span id="error_invalid_port_attributes"></span>**ERRORE \_ \_ attributi porta non validi \_**
</dt> <dd> <dl> <dt>

545 (0x221)
</dt> <dt>



Attributi di oggetto non validi specificati per NtCreatePort o attributi di porta non validi specificati in NtConnectPort


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_MESSAGE_TOO_LONG"></span><span id="error_port_message_too_long"></span>**messaggio della porta di errore \_ \_ \_ troppo \_ lungo**
</dt> <dd> <dl> <dt>

546 (0x222)
</dt> <dt>



La lunghezza del messaggio passato a NtRequestPort o NtRequestWaitReplyPort è più lunga del messaggio massimo consentito dalla porta.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_QUOTA_LOWER"></span><span id="error_invalid_quota_lower"></span>**ERRORE \_ di \_ quota \_ inferiore non valida**
</dt> <dd> <dl> <dt>

547 (0x223)
</dt> <dt>



È stato effettuato un tentativo di abbassare un limite di quota al di sotto dell'utilizzo corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ALREADY_ATTACHED"></span><span id="error_device_already_attached"></span>**dispositivo di errore \_ \_ già \_ collegato**
</dt> <dd> <dl> <dt>

548 (0x224)
</dt> <dt>



È stato effettuato un tentativo di connessione a un dispositivo già collegato a un altro dispositivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSTRUCTION_MISALIGNMENT"></span><span id="error_instruction_misalignment"></span>**ERRORE \_ di \_ allineamento delle istruzioni**
</dt> <dd> <dl> <dt>

549 (0x225)
</dt> <dt>



È stato effettuato un tentativo di eseguire un'istruzione in un indirizzo non allineato e il sistema host non supporta riferimenti a istruzioni non allineate.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_NOT_STARTED"></span><span id="error_profiling_not_started"></span>**ERRORE di \_ PROfilatura \_ non \_ avviato**
</dt> <dd> <dl> <dt>

550 (0x226)
</dt> <dt>



Profilatura non avviata.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_NOT_STOPPED"></span><span id="error_profiling_not_stopped"></span>**ERRORE di \_ PROfilatura \_ non \_ arrestato**
</dt> <dd> <dl> <dt>

551 (0x227)
</dt> <dt>



Profilatura non arrestata.


</dt> </dl> </dd> <dt>

<span id="ERROR_COULD_NOT_INTERPRET"></span><span id="error_could_not_interpret"></span>**\_Impossibile \_ \_ INTERPRETAre l'errore**
</dt> <dd> <dl> <dt>

552 (0x228)
</dt> <dt>



L'ACL passato non contiene le informazioni minime necessarie.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROFILING_AT_LIMIT"></span><span id="error_profiling_at_limit"></span>**ERRORE \_ di PROfilatura \_ al \_ limite**
</dt> <dd> <dl> <dt>

553 (0x229)
</dt> <dt>



Il numero di oggetti di profilatura attivi è massimo e non può essere avviato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_WAIT"></span><span id="error_cant_wait"></span>**ERRORE \_ di \_ attesa del cant**
</dt> <dd> <dl> <dt>

554 (0x22A)
</dt> <dt>



Utilizzato per indicare che un'operazione non può continuare senza blocco per I/O.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_TERMINATE_SELF"></span><span id="error_cant_terminate_self"></span>**ERRORE \_ di \_ terminazione \_ automatica**
</dt> <dd> <dl> <dt>

555 (0x22B)
</dt> <dt>



Indica che un thread ha tentato di terminare se stesso per impostazione predefinita (denominato NtTerminateThread con **null**) ed è l'ultimo thread del processo corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_CREATE_ERR"></span><span id="error_unexpected_mm_create_err"></span>**ERRORE \_ imprevisto di \_ \_ creazione \_ Err**
</dt> <dd> <dl> <dt>

556 (0x22C)
</dt> <dt>



Se viene restituito un errore MM che non è definito nel filtro FsRtl standard, viene convertito in uno degli errori seguenti, che è sicuramente presente nel filtro. In questo caso, le informazioni vengono perse, tuttavia, il filtro gestisce correttamente l'eccezione.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_MAP_ERROR"></span><span id="error_unexpected_mm_map_error"></span>**errore \_ di \_ \_ mappa mm imprevisto \_**
</dt> <dd> <dl> <dt>

557 (0x22D)
</dt> <dt>



Se viene restituito un errore MM che non è definito nel filtro FsRtl standard, viene convertito in uno degli errori seguenti, che è sicuramente presente nel filtro. In questo caso, le informazioni vengono perse, tuttavia, il filtro gestisce correttamente l'eccezione.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNEXPECTED_MM_EXTEND_ERR"></span><span id="error_unexpected_mm_extend_err"></span>**ERRORE \_ imprevisto \_ mm \_ extend \_ Err**
</dt> <dd> <dl> <dt>

558 (0x22E)
</dt> <dt>



Se viene restituito un errore MM che non è definito nel filtro FsRtl standard, viene convertito in uno degli errori seguenti, che è sicuramente presente nel filtro. In questo caso, le informazioni vengono perse, tuttavia, il filtro gestisce correttamente l'eccezione.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_FUNCTION_TABLE"></span><span id="error_bad_function_table"></span>**\_tabella delle \_ funzioni ERRAta Error \_**
</dt> <dd> <dl> <dt>

559 (0x22F)
</dt> <dt>



È stata rilevata una tabella di funzioni in formato non corretto durante un'operazione di rimozione.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_GUID_TRANSLATION"></span><span id="error_no_guid_translation"></span>**ERRORE \_ senza \_ \_ conversione GUID**
</dt> <dd> <dl> <dt>

560 (0x230)
</dt> <dt>



Indica che è stato effettuato un tentativo di assegnare la protezione a un file o a una directory file system e che uno dei SID del descrittore di sicurezza non può essere convertito in un GUID che può essere archiviato dall'file system. In questo modo, il tentativo di protezione non riesce, che può causare un tentativo di creazione di file non riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_SIZE"></span><span id="error_invalid_ldt_size"></span>**ERRORE \_ \_ dimensioni LDT non valide \_**
</dt> <dd> <dl> <dt>

561 (0x231)
</dt> <dt>



Indica che è stato effettuato un tentativo di espandere un LDT impostando le relative dimensioni o che la dimensione non era un numero pari di selettori.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_OFFSET"></span><span id="error_invalid_ldt_offset"></span>**ERRORE \_ di \_ offset LDT non valido \_**
</dt> <dd> <dl> <dt>

563 (0x233)
</dt> <dt>



Indica che il valore iniziale delle informazioni LDT non è un multiplo integrale della dimensione del selettore.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LDT_DESCRIPTOR"></span><span id="error_invalid_ldt_descriptor"></span>**ERRORE \_ \_ \_ descrittore LDT non valido**
</dt> <dd> <dl> <dt>

564 (0x234)
</dt> <dt>



Indica che l'utente ha fornito un descrittore non valido durante il tentativo di impostare i descrittori LDT.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_THREADS"></span><span id="error_too_many_threads"></span>**ERRORE di un \_ numero eccessivo di \_ \_ thread**
</dt> <dd> <dl> <dt>

565 (0x235)
</dt> <dt>



Indica che un processo dispone di un numero eccessivo di thread per eseguire l'azione richiesta. Ad esempio, l'assegnazione di un token primario può essere eseguita solo quando un processo ha zero o un thread.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_NOT_IN_PROCESS"></span><span id="error_thread_not_in_process"></span>**\_thread \_ di errore non \_ in \_ corso**
</dt> <dd> <dl> <dt>

566 (0x236)
</dt> <dt>



È stato effettuato un tentativo di operare su un thread all'interno di un processo specifico, ma il thread specificato non è nel processo specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_QUOTA_EXCEEDED"></span><span id="error_pagefile_quota_exceeded"></span>**QUOTA di paging degli errori \_ \_ \_ superata**
</dt> <dd> <dl> <dt>

567 (0x237)
</dt> <dt>



Quota del file di paging superata.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGON_SERVER_CONFLICT"></span><span id="error_logon_server_conflict"></span>**\_conflitto del \_ server di accesso con errori \_**
</dt> <dd> <dl> <dt>

568 (0x238)
</dt> <dt>



Impossibile avviare il servizio Netlogon perché un altro servizio Netlogon in esecuzione nel dominio è in conflitto con il ruolo specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYNCHRONIZATION_REQUIRED"></span><span id="error_synchronization_required"></span>**sincronizzazione degli errori \_ \_ obbligatoria**
</dt> <dd> <dl> <dt>

569 (0x239)
</dt> <dt>



Il database SAM in un server Windows è significativamente fuori dalla sincronizzazione con la copia sul controller di dominio. È necessaria una sincronizzazione completa.


</dt> </dl> </dd> <dt>

<span id="ERROR_NET_OPEN_FAILED"></span><span id="error_net_open_failed"></span>**ERRORE \_ net \_ Open \_ non riuscito**
</dt> <dd> <dl> <dt>

570 (0x23A)
</dt> <dt>



L'API NtCreateFile non è riuscita. Questo errore non dovrebbe mai essere restituito a un'applicazione. si tratta di un segnaposto che deve essere utilizzato dal redirector di gestione LAN Windows nelle routine di mapping degli errori interni.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_PRIVILEGE_FAILED"></span><span id="error_io_privilege_failed"></span>**privilegio i/o errore \_ \_ \_ non riuscito**
</dt> <dd> <dl> <dt>

571 (0x23B)
</dt> <dt>



{Privilegio non riuscito} Impossibile modificare le autorizzazioni di I/O per il processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTROL_C_EXIT"></span><span id="error_control_c_exit"></span>**\_uscita dal controllo di errore \_ C \_**
</dt> <dd> <dl> <dt>

572 (0x23C)
</dt> <dt>



{Applicazione uscita da CTRL + C} L'applicazione è stata terminata in seguito a una combinazione di tasti CTRL + C.


</dt> </dl> </dd> <dt>

<span id="ERROR_MISSING_SYSTEMFILE"></span><span id="error_missing_systemfile"></span>**ERRORE \_ manca \_ SYSTEMFILE**
</dt> <dd> <dl> <dt>

573 (0x23D)
</dt> <dt>



{File di sistema mancante} Il file di sistema richiesto% HS non è valido o è mancante.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNHANDLED_EXCEPTION"></span><span id="error_unhandled_exception"></span>**ERRORE \_ eccezione non gestita \_**
</dt> <dd> <dl> <dt>

574 (0x23E)
</dt> <dt>



{Errore applicazione} Si è verificata l'eccezione% s (0x% 08lx) nell'applicazione nel percorso 0x% 08lx.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_INIT_FAILURE"></span><span id="error_app_init_failure"></span>**errore \_ di \_ inizializzazione dell'app errore \_**
</dt> <dd> <dl> <dt>

575 (0x23F)
</dt> <dt>



{Errore applicazione} Non è stato possibile avviare correttamente l'applicazione (0x% lx). Fare clic su OK per chiudere l'applicazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGEFILE_CREATE_FAILED"></span><span id="error_pagefile_create_failed"></span>**ERRORE \_ di \_ creazione del pagefile \_**
</dt> <dd> <dl> <dt>

576 (0x240)
</dt> <dt>



{Impossibile creare il file di paging} Creazione del file di paging% HS non riuscita (% LX). Dimensioni richieste:% LD.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_IMAGE_HASH"></span><span id="error_invalid_image_hash"></span>**ERRORE \_ di \_ hash immagine non valido \_**
</dt> <dd> <dl> <dt>

577 (0x241)
</dt> <dt>



Windows non è in grado di verificare la firma digitale per il file. Una modifica recente dell'hardware o del software potrebbe avere installato un file firmato in modo errato o danneggiato o che potrebbe essere un software dannoso proveniente da un'origine sconosciuta.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_PAGEFILE"></span><span id="error_no_pagefile"></span>**ERRORE \_ nessun \_ pagefile**
</dt> <dd> <dl> <dt>

578 (0x242)
</dt> <dt>



{Nessun file di paging specificato} Nella configurazione di sistema non è stato specificato alcun file di paging.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_FLOAT_CONTEXT"></span><span id="error_illegal_float_context"></span>**ERRORE \_ \_ contesto float non valido \_**
</dt> <dd> <dl> <dt>

579 (0x243)
</dt> <dt>



ECCEZIONE Un'applicazione in modalità reale ha emesso un'istruzione a virgola mobile e l'hardware a virgola mobile non è presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_EVENT_PAIR"></span><span id="error_no_event_pair"></span>**ERRORE \_ Nessuna \_ coppia di eventi \_**
</dt> <dd> <dl> <dt>

580 (0x244)
</dt> <dt>



Un'operazione di sincronizzazione della coppia di eventi è stata eseguita utilizzando l'oggetto coppia di eventi client/server specifico del thread, ma al thread non è stato associato alcun oggetto coppia di eventi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CTRLR_CONFIG_ERROR"></span><span id="error_domain_ctrlr_config_error"></span>**errore di configurazione del dominio di errore \_ \_ CTRLR \_ \_**
</dt> <dd> <dl> <dt>

581 (0x245)
</dt> <dt>



Una configurazione di Windows Server non è corretta.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_CHARACTER"></span><span id="error_illegal_character"></span>**ERRORE \_ carattere non valido \_**
</dt> <dd> <dl> <dt>

582 (0x246)
</dt> <dt>



È stato rilevato un carattere non valido. Per un set di caratteri a più byte, questo include un byte di apertura senza un byte finale positivo. Per il set di caratteri Unicode sono inclusi i caratteri 0xFFFF e 0xFFFE.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNDEFINED_CHARACTER"></span><span id="error_undefined_character"></span>**ERRORE \_ carattere non definito \_**
</dt> <dd> <dl> <dt>

583 (0x247)
</dt> <dt>



Il carattere Unicode non è definito nel set di caratteri Unicode installato nel sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_VOLUME"></span><span id="error_floppy_volume"></span>**\_volume floppy \_ errore**
</dt> <dd> <dl> <dt>

584 (0x248)
</dt> <dt>



Impossibile creare il file di paging su un dischetto floppy.


</dt> </dl> </dd> <dt>

<span id="ERROR_BIOS_FAILED_TO_CONNECT_INTERRUPT"></span><span id="error_bios_failed_to_connect_interrupt"></span>**ERRORE \_ BIOS \_ non è stato \_ possibile \_ connettere l' \_ interrupt**
</dt> <dd> <dl> <dt>

585 (0x249)
</dt> <dt>



Il BIOS di sistema non è riuscito a connettere un interrupt di sistema al dispositivo o al bus per il quale il dispositivo è connesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_BACKUP_CONTROLLER"></span><span id="error_backup_controller"></span>**\_controller di backup degli errori \_**
</dt> <dd> <dl> <dt>

586 (0x24A)
</dt> <dt>



Questa operazione è consentita solo per il controller di dominio primario del dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_MUTANT_LIMIT_EXCEEDED"></span><span id="error_mutant_limit_exceeded"></span>**\_limite del mutatore di errore \_ \_ superato**
</dt> <dd> <dl> <dt>

587 (0x24B)
</dt> <dt>



È stato effettuato un tentativo di acquisire un mutatore in modo che sia stato superato il numero massimo di conteggi.


</dt> </dl> </dd> <dt>

<span id="ERROR_FS_DRIVER_REQUIRED"></span><span id="error_fs_driver_required"></span>**ERRORE \_ \_ driver FS \_ necessario**
</dt> <dd> <dl> <dt>

588 (0x24C)
</dt> <dt>



È stato eseguito l'accesso a un volume per il quale è necessario un driver file system che non è ancora stato caricato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_LOAD_REGISTRY_FILE"></span><span id="error_cannot_load_registry_file"></span>**ERRORE \_ non è possibile \_ caricare il \_ file del registro di sistema \_**
</dt> <dd> <dl> <dt>

589 (0x24D)
</dt> <dt>



{Errore file registro di sistema} Il registro di sistema non è in grado di caricare l'hive (file):% HS o il relativo log o alternativa. È danneggiato, assente o non accessibile in scrittura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEBUG_ATTACH_FAILED"></span><span id="error_debug_attach_failed"></span>**ERRORE \_ di \_ connessione di debug \_**
</dt> <dd> <dl> <dt>

590 (0x24E)
</dt> <dt>



{Errore imprevisto in [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess)} Si è verificato un errore imprevisto durante l'elaborazione di una richiesta dell'API **DebugActiveProcess** . È possibile scegliere OK per terminare il processo oppure Annulla per ignorare l'errore.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_PROCESS_TERMINATED"></span><span id="error_system_process_terminated"></span>**ERRORE \_ del \_ processo di sistema \_ terminato**
</dt> <dd> <dl> <dt>

591 (0x24F)
</dt> <dt>



{Errore irreversibile del sistema} Il processo di sistema% HS è stato interrotto in modo imprevisto con lo stato 0x% 08x (0x% 08x 0x% 08x). Il sistema è stato arrestato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_NOT_ACCEPTED"></span><span id="error_data_not_accepted"></span>**\_dati errore \_ non \_ accettati**
</dt> <dd> <dl> <dt>

592 (0x250)
</dt> <dt>



{Dati non accettati} Il client TDI non è in grado di gestire i dati ricevuti durante un'indicazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_VDM_HARD_ERROR"></span><span id="error_vdm_hard_error"></span>**errore \_ hardware di VDM \_ \_**
</dt> <dd> <dl> <dt>

593 (0x251)
</dt> <dt>



NTVDM ha rilevato un errore hardware.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_CANCEL_TIMEOUT"></span><span id="error_driver_cancel_timeout"></span>**\_ \_ timeout annullamento driver \_ errore**
</dt> <dd> <dl> <dt>

594 (0x252)
</dt> <dt>



{Annulla timeout} Il driver% HS non è riuscito a completare una richiesta di I/O annullata nel tempo assegnato.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPLY_MESSAGE_MISMATCH"></span><span id="error_reply_message_mismatch"></span>**messaggio di risposta errore non \_ \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

595 (0x253)
</dt> <dt>



{Messaggio di risposta non corrispondente} È stato effettuato un tentativo di rispondere a un messaggio LPC, ma il thread specificato dall'ID client nel messaggio non era in attesa del messaggio.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA"></span><span id="error_lost_writebehind_data"></span>**errore durante la \_ perdita di \_ \_ dati WRITEBEHIND**
</dt> <dd> <dl> <dt>

596 (0x254)
</dt> <dt>



{Scrittura ritardata non riuscita} Windows non è riuscito a salvare tutti i dati per il file% HS. I dati sono andati persi. Questo errore può essere causato da un errore dell'hardware del computer o della connessione di rete. Provare a salvare il file altrove.


</dt> </dl> </dd> <dt>

<span id="ERROR_CLIENT_SERVER_PARAMETERS_INVALID"></span><span id="error_client_server_parameters_invalid"></span>**\_parametri del server client di errore \_ \_ \_ non validi**
</dt> <dd> <dl> <dt>

597 (0x255)
</dt> <dt>



Il parametro o i parametri passati al server nella finestra memoria condivisa client/server non sono validi. Nella finestra Shared Memory è possibile che siano stati inseriti troppi dati.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_TINY_STREAM"></span><span id="error_not_tiny_stream"></span>**ERRORE \_ non \_ piccolo \_ flusso**
</dt> <dd> <dl> <dt>

598 (0x256)
</dt> <dt>



Il flusso non è un flusso di piccole dimensioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_STACK_OVERFLOW_READ"></span><span id="error_stack_overflow_read"></span>**\_ \_ lettura Overflow stack \_ errore**
</dt> <dd> <dl> <dt>

599 (0x257)
</dt> <dt>



La richiesta deve essere gestita dal codice di overflow dello stack.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONVERT_TO_LARGE"></span><span id="error_convert_to_large"></span>**ERRORE \_ conversione \_ in \_ grande**
</dt> <dd> <dl> <dt>

600 (0x258)
</dt> <dt>



Codici di stato OFS interno che indicano come viene gestita un'operazione di allocazione. Viene eseguito un nuovo tentativo dopo lo spostamento del oNode contenitore o il flusso di extent viene convertito in un flusso di grandi dimensioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_FOUND_OUT_OF_SCOPE"></span><span id="error_found_out_of_scope"></span>**ERRORE \_ rilevato \_ dall' \_ \_ ambito**
</dt> <dd> <dl> <dt>

601 (0x259)
</dt> <dt>



Il tentativo di trovare l'oggetto ha trovato un oggetto corrispondente in base all'ID del volume, ma non rientra nell'ambito dell'handle utilizzato per l'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALLOCATE_BUCKET"></span><span id="error_allocate_bucket"></span>**ERRORE di \_ allocazione del \_ bucket**
</dt> <dd> <dl> <dt>

602 (0x25A)
</dt> <dt>



La matrice di bucket deve essere aumentata. Ripetere la transazione dopo questa operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_MARSHALL_OVERFLOW"></span><span id="error_marshall_overflow"></span>**ERRORE \_ Marshall \_ overflow**
</dt> <dd> <dl> <dt>

603 (0x25B)
</dt> <dt>



Si è verificato un overflow del buffer di marshalling utente/kernel.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_VARIANT"></span><span id="error_invalid_variant"></span>**ERRORE \_ Variant non valido \_**
</dt> <dd> <dl> <dt>

604 (0x25C)
</dt> <dt>



La struttura VARIANT fornita contiene dati non validi.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_COMPRESSION_BUFFER"></span><span id="error_bad_compression_buffer"></span>**ERRORE \_ \_ buffer di compressione errato \_**
</dt> <dd> <dl> <dt>

605 (0x25D)
</dt> <dt>



Il buffer specificato contiene dati in formato non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_AUDIT_FAILED"></span><span id="error_audit_failed"></span>**\_controllo errori \_ non riuscito**
</dt> <dd> <dl> <dt>

606 (0x25E)
</dt> <dt>



{Audit non riuscito} Tentativo di generare un controllo di sicurezza non riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_RESOLUTION_NOT_SET"></span><span id="error_timer_resolution_not_set"></span>**risoluzione del timer di errore \_ \_ \_ non \_ impostata**
</dt> <dd> <dl> <dt>

607 (0x25F)
</dt> <dt>



La risoluzione del timer non è stata impostata in precedenza dal processo corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_LOGON_INFO"></span><span id="error_insufficient_logon_info"></span>**ERRORE \_ \_ informazioni di accesso insufficienti \_**
</dt> <dd> <dl> <dt>

608 (0x260)
</dt> <dt>



Le informazioni sull'account non sono sufficienti per l'accesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DLL_ENTRYPOINT"></span><span id="error_bad_dll_entrypoint"></span>**ERRORE \_ di \_ ENTRYPOINT dll non valido \_**
</dt> <dd> <dl> <dt>

609 (0x261)
</dt> <dt>



{EntryPoint DLL non valido} La libreria a collegamento dinamico% HS non è stata scritta correttamente. Il puntatore dello stack è stato lasciato in uno stato incoerente. Il EntryPoint deve essere dichiarato come WINAPI o STDCALL. Selezionare Sì per interrompere il caricamento della DLL. Selezionare NO per continuare l'esecuzione. Se si seleziona NO, l'applicazione potrebbe non funzionare correttamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_SERVICE_ENTRYPOINT"></span><span id="error_bad_service_entrypoint"></span>**ERRORE \_ \_ ENTRYPOINT servizio \_ errato**
</dt> <dd> <dl> <dt>

610 (0x262)
</dt> <dt>



{EntryPoint di callback del servizio non valido} Il servizio% HS non è stato scritto correttamente. Il puntatore dello stack è stato lasciato in uno stato incoerente. Il EntryPoint di callback deve essere dichiarato come WINAPI o STDCALL. Se si seleziona OK, il servizio continuerà a funzionare. Tuttavia, il processo del servizio potrebbe funzionare in modo errato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IP_ADDRESS_CONFLICT1"></span><span id="error_ip_address_conflict1"></span>**ERRORE \_ dell' \_ indirizzo IP \_ CONFLICT1**
</dt> <dd> <dl> <dt>

611 (0x263)
</dt> <dt>



Si è verificato un conflitto di indirizzi IP con un altro sistema nella rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_IP_ADDRESS_CONFLICT2"></span><span id="error_ip_address_conflict2"></span>**ERRORE \_ dell' \_ indirizzo IP \_ CONFLICT2**
</dt> <dd> <dl> <dt>

612 (0x264)
</dt> <dt>



Si è verificato un conflitto di indirizzi IP con un altro sistema nella rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_QUOTA_LIMIT"></span><span id="error_registry_quota_limit"></span>**\_ \_ limite quota registro \_ errori**
</dt> <dd> <dl> <dt>

613 (0x265)
</dt> <dt>



{Low sullo spazio del registro di sistema} Il sistema ha raggiunto la dimensione massima consentita per la parte del registro di sistema. Le richieste di archiviazione aggiuntive verranno ignorate.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_CALLBACK_ACTIVE"></span><span id="error_no_callback_active"></span>**ERRORE \_ nessun \_ callback \_ attivo**
</dt> <dd> <dl> <dt>

614 (0x266)
</dt> <dt>



Non è possibile eseguire un servizio di sistema restituito di callback quando non è attivo alcun callback.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_SHORT"></span><span id="error_pwd_too_short"></span>**ERRORE \_ pwd \_ troppo \_ breve**
</dt> <dd> <dl> <dt>

615 (0x267)
</dt> <dt>



La password specificata è troppo breve per soddisfare i criteri dell'account utente. Scegliere una password più lunga.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_RECENT"></span><span id="error_pwd_too_recent"></span>**ERRORE \_ pwd \_ troppo \_ recente**
</dt> <dd> <dl> <dt>

616 (0x268)
</dt> <dt>



I criteri dell'account utente non consentono di modificare le password troppo spesso. Questa operazione viene eseguita per impedire agli utenti di tornare a una password familiare ma potenzialmente individuata. Se si ritiene che la password sia stata compromessa, contattare immediatamente l'amministratore per fare in modo che ne venga assegnato uno nuovo.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_HISTORY_CONFLICT"></span><span id="error_pwd_history_conflict"></span>**\_ \_ conflitto cronologia pwd \_ errore**
</dt> <dd> <dl> <dt>

617 (0x269)
</dt> <dt>



Si è tentato di modificare la password in un computer che è stato usato in precedenza. I criteri dell'account utente non sono consentiti. Selezionare una password che non è stata usata in precedenza.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNSUPPORTED_COMPRESSION"></span><span id="error_unsupported_compression"></span>**ERRORE di \_ compressione non supportata \_**
</dt> <dd> <dl> <dt>

618 (0x26A)
</dt> <dt>



Il formato di compressione specificato non è supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_HW_PROFILE"></span><span id="error_invalid_hw_profile"></span>**ERRORE \_ del \_ profilo HW non valido \_**
</dt> <dd> <dl> <dt>

619 (0x26B)
</dt> <dt>



La configurazione del profilo hardware specificata non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PLUGPLAY_DEVICE_PATH"></span><span id="error_invalid_plugplay_device_path"></span>**ERRORE \_ \_ PLUGPLAY \_ percorso dispositivo \_ non valido**
</dt> <dd> <dl> <dt>

620 (0x26C)
</dt> <dt>



Il percorso del dispositivo del registro di sistema Plug and Play specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_QUOTA_LIST_INCONSISTENT"></span><span id="error_quota_list_inconsistent"></span>**\_elenco quote \_ errori \_ incoerenti**
</dt> <dd> <dl> <dt>

621 (0x26D)
</dt> <dt>



L'elenco di quote specificato non è coerente internamente con il relativo descrittore.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVALUATION_EXPIRATION"></span><span id="error_evaluation_expiration"></span>**\_scadenza valutazione \_ errore**
</dt> <dd> <dl> <dt>

622 (0x26E)
</dt> <dt>



{Notifica di valutazione di Windows} Il periodo di valutazione per questa installazione di Windows è scaduto. Questo sistema verrà arrestato tra 1 ora. Per ripristinare l'accesso a questa installazione di Windows, aggiornare questa installazione utilizzando una distribuzione con licenza del prodotto.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_DLL_RELOCATION"></span><span id="error_illegal_dll_relocation"></span>**ERRORE \_ di \_ rilocazione della dll non valida \_**
</dt> <dd> <dl> <dt>

623 (0x26F)
</dt> <dt>



{Rilocazione della DLL di sistema non valida} La DLL di sistema% HS è stata rilocata in memoria. L'applicazione non viene eseguita correttamente. La rilocazione è stata eseguita perché la DLL% HS occupa un intervallo di indirizzi riservato per le DLL di sistema Windows. Il fornitore che fornisce la DLL deve essere contattato per una nuova DLL.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_INIT_FAILED_LOGOFF"></span><span id="error_dll_init_failed_logoff"></span>**ERRORE \_ di \_ inizializzazione DLL \_ non riuscita \_**
</dt> <dd> <dl> <dt>

624 (0x270)
</dt> <dt>



{Inizializzazione DLL non riuscita} L'inizializzazione dell'applicazione non è riuscita perché è in corso l'arresto della stazione di finestra.


</dt> </dl> </dd> <dt>

<span id="ERROR_VALIDATE_CONTINUE"></span><span id="error_validate_continue"></span>**ERRORE di \_ convalida \_ continua**
</dt> <dd> <dl> <dt>

625 (0x271)
</dt> <dt>



Il processo di convalida deve continuare con il passaggio successivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_MATCHES"></span><span id="error_no_more_matches"></span>**ERRORE \_ \_ altre \_ corrispondenze**
</dt> <dd> <dl> <dt>

626 (0x272)
</dt> <dt>



Non sono presenti altre corrispondenze per l'enumerazione dell'indice corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_RANGE_LIST_CONFLICT"></span><span id="error_range_list_conflict"></span>**\_ \_ conflitto elenco intervallo \_ errori**
</dt> <dd> <dl> <dt>

627 (0x273)
</dt> <dt>



Non è stato possibile aggiungere l'intervallo all'elenco di intervalli a causa di un conflitto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_SID_MISMATCH"></span><span id="error_server_sid_mismatch"></span>**\_ \_ MANCAta corrispondenza del SID del server errori \_**
</dt> <dd> <dl> <dt>

628 (0x274)
</dt> <dt>



Il processo server viene eseguito con un SID diverso da quello richiesto dal client.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_ENABLE_DENY_ONLY"></span><span id="error_cant_enable_deny_only"></span>**ERRORE \_ di \_ Abilitazione \_ \_ solo negazione**
</dt> <dd> <dl> <dt>

629 (0x275)
</dt> <dt>



Non è possibile abilitare un gruppo contrassegnato come use solo per Deny.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOAT_MULTIPLE_FAULTS"></span><span id="error_float_multiple_faults"></span>**errore durante il \_ float di \_ più \_ errori**
</dt> <dd> <dl> <dt>

630 (0x276)
</dt> <dt>



ECCEZIONE Più errori a virgola mobile.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOAT_MULTIPLE_TRAPS"></span><span id="error_float_multiple_traps"></span>**errore durante il \_ float di \_ più \_ trap**
</dt> <dd> <dl> <dt>

631 (0x277)
</dt> <dt>



ECCEZIONE Più trap a virgola mobile.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOINTERFACE"></span><span id="error_nointerface"></span>**ERRORE \_ NOinterface**
</dt> <dd> <dl> <dt>

632 (0x278)
</dt> <dt>



L'interfaccia richiesta non è supportata.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_FAILED_SLEEP"></span><span id="error_driver_failed_sleep"></span>**ERRORE \_ di \_ sospensione driver non riuscito \_**
</dt> <dd> <dl> <dt>

633 (0x279)
</dt> <dt>



{Standby sistema non riuscito} Il driver% HS non supporta la modalità standby. L'aggiornamento di questo driver può consentire al sistema di passare alla modalità standby.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_SYSTEM_FILE"></span><span id="error_corrupt_system_file"></span>**ERRORE \_ \_ file di sistema danneggiato \_**
</dt> <dd> <dl> <dt>

634 (0x27A)
</dt> <dt>



Il file di sistema %1 è stato danneggiato ed è stato sostituito.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMMITMENT_MINIMUM"></span><span id="error_commitment_minimum"></span>**\_minimo impegno \_ errore**
</dt> <dd> <dl> <dt>

635 (0x27B)
</dt> <dt>



{Memoria virtuale minima troppo bassa} Memoria virtuale insufficiente nel sistema. Windows sta aumentando le dimensioni del file di paging della memoria virtuale. Durante questo processo, le richieste di memoria per alcune applicazioni potrebbero essere negate. Per ulteriori informazioni, vedere la Guida di.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_RESTART_ENUMERATION"></span><span id="error_pnp_restart_enumeration"></span>**ERRORE \_ di \_ enumerazione di riavvio PNP \_**
</dt> <dd> <dl> <dt>

636 (0x27C)
</dt> <dt>



Un dispositivo è stato rimosso, quindi è necessario riavviare l'enumerazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_IMAGE_BAD_SIGNATURE"></span><span id="error_system_image_bad_signature"></span>**immagine del sistema di errore \_ \_ \_ firma non valida \_**
</dt> <dd> <dl> <dt>

637 (0x27D)
</dt> <dt>



{Errore irreversibile del sistema} L'immagine di sistema% s non è firmata correttamente. Il file è stato sostituito con il file firmato. Il sistema è stato arrestato.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_REBOOT_REQUIRED"></span><span id="error_pnp_reboot_required"></span>**ERRORE \_ PNP \_ riavvio \_ richiesto**
</dt> <dd> <dl> <dt>

638 (0x27E)
</dt> <dt>



Il dispositivo non viene avviato senza riavvio.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_POWER"></span><span id="error_insufficient_power"></span>**ERRORE \_ di \_ alimentazione insufficiente**
</dt> <dd> <dl> <dt>

639 (0x27F)
</dt> <dt>



La potenza necessaria non è sufficiente per completare l'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_MULTIPLE_FAULT_VIOLATION"></span><span id="error_multiple_fault_violation"></span>**errore \_ di \_ più \_ violazioni di errore**
</dt> <dd> <dl> <dt>

640 (0x280)
</dt> <dt>



errore \_ di \_ più \_ violazioni di errore


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_SHUTDOWN"></span><span id="error_system_shutdown"></span>**ERRORE \_ di \_ arresto del sistema**
</dt> <dd> <dl> <dt>

641 (0x281)
</dt> <dt>



È in corso l'arresto del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_NOT_SET"></span><span id="error_port_not_set"></span>**porta di errore \_ \_ non \_ impostata**
</dt> <dd> <dl> <dt>

642 (0x282)
</dt> <dt>



È stato eseguito un tentativo di rimuovere un processo DebugPort, ma una porta non era ancora associata al processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DS_VERSION_CHECK_FAILURE"></span><span id="error_ds_version_check_failure"></span>**ERRORE \_ \_ controllo versione \_ DS \_**
</dt> <dd> <dl> <dt>

643 (0x283)
</dt> <dt>



Questa versione di Windows non è compatibile con la versione del comportamento della foresta di directory, del dominio o del controller di dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_RANGE_NOT_FOUND"></span><span id="error_range_not_found"></span>**\_intervallo errori \_ non \_ trovato**
</dt> <dd> <dl> <dt>

644 (0x284)
</dt> <dt>



L'intervallo specificato non è stato trovato nell'elenco di intervalli.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAFE_MODE_DRIVER"></span><span id="error_not_safe_mode_driver"></span>**\_driver in \_ modalità non sicura \_ \_ errore**
</dt> <dd> <dl> <dt>

646 (0x286)
</dt> <dt>



Il driver non è stato caricato perché il sistema viene avviato in modalità provvisoria.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAILED_DRIVER_ENTRY"></span><span id="error_failed_driver_entry"></span>**ERRORE \_ \_ voce driver non riuscita \_**
</dt> <dd> <dl> <dt>

647 (0x287)
</dt> <dt>



Il driver non è stato caricato perché non ha superato la chiamata di inizializzazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ENUMERATION_ERROR"></span><span id="error_device_enumeration_error"></span>**errore \_ di \_ enumerazione dispositivo errore \_**
</dt> <dd> <dl> <dt>

648 (0x288)
</dt> <dt>



"% HS" ha rilevato un errore durante l'applicazione dell'alimentazione o la lettura della configurazione del dispositivo. Ciò può essere causato da un errore dell'hardware o da una connessione scadente.


</dt> </dl> </dd> <dt>

<span id="ERROR_MOUNT_POINT_NOT_RESOLVED"></span><span id="error_mount_point_not_resolved"></span>**\_punto di montaggio errore \_ \_ non \_ risolto**
</dt> <dd> <dl> <dt>

649 (0x289)
</dt> <dt>



L'operazione di creazione non è riuscita perché il nome contiene almeno un punto di montaggio che viene risolto in un volume a cui l'oggetto dispositivo specificato non è collegato.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DEVICE_OBJECT_PARAMETER"></span><span id="error_invalid_device_object_parameter"></span>**ERRORE \_ \_ \_ parametro oggetto dispositivo non valido \_**
</dt> <dd> <dl> <dt>

650 (0x28A)
</dt> <dt>



Il parametro dell'oggetto dispositivo non è un oggetto dispositivo valido o non è collegato al volume specificato dal nome file.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_OCCURED"></span><span id="error_mca_occured"></span>**ERRORE \_ MCA \_ eseguito**
</dt> <dd> <dl> <dt>

651 (0x28B)
</dt> <dt>



Si è verificato un errore di controllo del computer. Per ulteriori informazioni, consultare il registro eventi di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_DATABASE_ERROR"></span><span id="error_driver_database_error"></span>**\_errore del \_ database del driver di errore \_**
</dt> <dd> <dl> <dt>

652 (0x28C)
</dt> <dt>



Errore \[ %2 durante \] l'elaborazione del database del driver.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_HIVE_TOO_LARGE"></span><span id="error_system_hive_too_large"></span>**ERRORE \_ di \_ hive di sistema \_ troppo \_ grande**
</dt> <dd> <dl> <dt>

653 (0x28D)
</dt> <dt>



La dimensione dell'hive del sistema ha superato il limite.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_FAILED_PRIOR_UNLOAD"></span><span id="error_driver_failed_prior_unload"></span>**\_ \_ scaricamento precedente errore driver non riuscito \_ \_**
</dt> <dd> <dl> <dt>

654 (0x28E)
</dt> <dt>



Non è stato possibile caricare il driver perché una versione precedente del driver è ancora in memoria.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLSNAP_PREPARE_HIBERNATE"></span><span id="error_volsnap_prepare_hibernate"></span>**ERRORE \_ VolSnap preparare lo stato di \_ \_ ibernazione**
</dt> <dd> <dl> <dt>

655 (0x28F)
</dt> <dt>



{Servizio Copia Shadow del volume} Attendere mentre il Servizio Copia Shadow del volume prepara il volume% HS per l'ibernazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_HIBERNATION_FAILURE"></span><span id="error_hibernation_failure"></span>**errore di \_ ibernazione errore \_**
</dt> <dd> <dl> <dt>

656 (0x290)
</dt> <dt>



Il sistema non è stato in stato di ibernazione (codice di errore% HS). Lo stato di ibernazione verrà disabilitato fino al riavvio del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_PWD_TOO_LONG"></span><span id="error_pwd_too_long"></span>**ERRORE \_ pwd \_ troppo \_ lungo**
</dt> <dd> <dl> <dt>

657 (0x291)
</dt> <dt>



La password specificata è troppo lungo per soddisfare i criteri dell'account utente. Scegliere una password più breve.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_SYSTEM_LIMITATION"></span><span id="error_file_system_limitation"></span>**\_limitazione del file \_ System \_ degli errori**
</dt> <dd> <dl> <dt>

665 (0x299)
</dt> <dt>



Impossibile completare l'operazione a causa di un limite del file system.


</dt> </dl> </dd> <dt>

<span id="ERROR_ASSERTION_FAILURE"></span><span id="error_assertion_failure"></span>**ERRORE dell' \_ asserzione di errore \_**
</dt> <dd> <dl> <dt>

668 (0x29C)
</dt> <dt>



Si è verificato un errore di asserzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACPI_ERROR"></span><span id="error_acpi_error"></span>**errore \_ ACPI \_ errore**
</dt> <dd> <dl> <dt>

669 (0x29D)
</dt> <dt>



Si è verificato un errore nel sottosistema ACPI.


</dt> </dl> </dd> <dt>

<span id="ERROR_WOW_ASSERTION"></span><span id="error_wow_assertion"></span>**\_ \_ asserzione Wow errore**
</dt> <dd> <dl> <dt>

670 (0x29E)
</dt> <dt>



Errore di asserzione WOW.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_BAD_MPS_TABLE"></span><span id="error_pnp_bad_mps_table"></span>**ERRORE \_ PNP \_ \_ tabella MPS non valida \_**
</dt> <dd> <dl> <dt>

671 (0x29F)
</dt> <dt>



Un dispositivo non è presente nella tabella MPS del BIOS di sistema. Questo dispositivo non verrà usato. Contattare il fornitore del sistema per l'aggiornamento del BIOS di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_TRANSLATION_FAILED"></span><span id="error_pnp_translation_failed"></span>**ERRORE \_ di \_ conversione PNP \_ non riuscita**
</dt> <dd> <dl> <dt>

672 (0x2A0)
</dt> <dt>



Un convertitore non è riuscito a convertire le risorse.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_IRQ_TRANSLATION_FAILED"></span><span id="error_pnp_irq_translation_failed"></span>**ERRORE \_ di \_ conversione IRQ PNP \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

673 (0x2A1)
</dt> <dt>



Un convertitore di IRQ non è riuscito a tradurre le risorse.


</dt> </dl> </dd> <dt>

<span id="ERROR_PNP_INVALID_ID"></span><span id="error_pnp_invalid_id"></span>**ERRORE \_ PNP \_ non valido \_**
</dt> <dd> <dl> <dt>

674 (0x2A2)
</dt> <dt>



Il driver %2 ha restituito un ID non valido per un dispositivo figlio (%3).


</dt> </dl> </dd> <dt>

<span id="ERROR_WAKE_SYSTEM_DEBUGGER"></span><span id="error_wake_system_debugger"></span>**\_debugger di sistema di riattivazione errore \_ \_**
</dt> <dd> <dl> <dt>

675 (0x2A3)
</dt> <dt>



{Debugger del kernel riattivato} il debugger di sistema è stato riattivato da un interrupt.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLES_CLOSED"></span><span id="error_handles_closed"></span>**handle di errore \_ \_ chiusi**
</dt> <dd> <dl> <dt>

676 (0x2A4)
</dt> <dt>



{Handle chiusi} Gli handle per gli oggetti sono stati chiusi automaticamente in seguito all'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXTRANEOUS_INFORMATION"></span><span id="error_extraneous_information"></span>**\_informazioni estranee \_ sull'errore**
</dt> <dd> <dl> <dt>

677 (0x2A5)
</dt> <dt>



{Troppe informazioni} L'elenco di controllo di accesso (ACL) specificato contiene più informazioni del previsto.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMIT_NECESSARY"></span><span id="error_rxact_commit_necessary"></span>**ERRORE \_ RXACT \_ commit \_ necessario**
</dt> <dd> <dl> <dt>

678 (0x2A6)
</dt> <dt>



Questo stato indica che lo stato della transazione esiste già per il sottoalbero del registro di sistema, ma che il commit di una transazione è stato interrotto in precedenza. Il commit non è stato completato, ma non ne è stato eseguito il rollback, quindi è possibile eseguirne il commit se lo si desidera.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_CHECK"></span><span id="error_media_check"></span>**\_controllo del supporto errori \_**
</dt> <dd> <dl> <dt>

679 (0x2A7)
</dt> <dt>



{Media changed} È possibile che il supporto sia stato modificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_GUID_SUBSTITUTION_MADE"></span><span id="error_guid_substitution_made"></span>**\_sostituzione GUID \_ errore \_ eseguita**
</dt> <dd> <dl> <dt>

680 (0x2A8)
</dt> <dt>



{Sostituzione GUID} Durante la conversione di un identificatore globale (GUID) in un ID di sicurezza (SID) di Windows, non è stato trovato alcun prefisso GUID definito in modo amministrativo. È stato usato un prefisso sostitutivo, che non compromette la sicurezza del sistema. Tuttavia, questo può fornire un accesso più restrittivo rispetto a quello previsto.


</dt> </dl> </dd> <dt>

<span id="ERROR_STOPPED_ON_SYMLINK"></span><span id="error_stopped_on_symlink"></span>**ERRORE \_ interrotto \_ sul \_ collegamento simbolico**
</dt> <dd> <dl> <dt>

681 (0x2A9)
</dt> <dt>



Operazione di creazione arrestata dopo il raggiungimento di un collegamento simbolico.


</dt> </dl> </dd> <dt>

<span id="ERROR_LONGJUMP"></span><span id="error_longjump"></span>**ERRORE \_ LONGJUMP**
</dt> <dd> <dl> <dt>

682 (0x2AA)
</dt> <dt>



È stato eseguito un salto lungo.


</dt> </dl> </dd> <dt>

<span id="ERROR_PLUGPLAY_QUERY_VETOED"></span><span id="error_plugplay_query_vetoed"></span>**ERRORE \_ PLUGPLAY \_ query con \_ veto**
</dt> <dd> <dl> <dt>

683 (0x2AB)
</dt> <dt>



Operazione di query Plug and Play non riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNWIND_CONSOLIDATE"></span><span id="error_unwind_consolidate"></span>**errore durante la \_ rimozione del \_ consolidamento**
</dt> <dd> <dl> <dt>

684 (0x2AC)
</dt> <dt>



È stato eseguito un consolidamento dei frame.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_HIVE_RECOVERED"></span><span id="error_registry_hive_recovered"></span>**\_ripristino hive del registro errori \_ \_**
</dt> <dd> <dl> <dt>

685 (0x2AD)
</dt> <dt>



{Hive del registro di sistema recuperato} Hive del registro di sistema (file):% HS è stato danneggiato ed è stato recuperato. È possibile che alcuni dati siano andati perduti.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_MIGHT_BE_INSECURE"></span><span id="error_dll_might_be_insecure"></span>**la \_ dll di errore \_ potrebbe non \_ essere \_ sicura**
</dt> <dd> <dl> <dt>

686 (0x2AE)
</dt> <dt>



L'applicazione sta tentando di eseguire il codice eseguibile dal modulo% HS. Questa operazione potrebbe non essere sicura. È disponibile un'alternativa,% HS. Se l'applicazione usa il modulo sicuro% HS?


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_MIGHT_BE_INCOMPATIBLE"></span><span id="error_dll_might_be_incompatible"></span>**la \_ dll di errore \_ potrebbe non \_ essere \_ compatibile**
</dt> <dd> <dl> <dt>

687 (0x2AF)
</dt> <dt>



L'applicazione sta caricando il codice eseguibile dal modulo% HS. Questa operazione è sicura, ma potrebbe non essere compatibile con le versioni precedenti del sistema operativo. È disponibile un'alternativa,% HS. Se l'applicazione usa il modulo sicuro% HS?


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_EXCEPTION_NOT_HANDLED"></span><span id="error_dbg_exception_not_handled"></span>**\_eccezione dbg \_ errore \_ non \_ gestita**
</dt> <dd> <dl> <dt>

688 (0x2B0)
</dt> <dt>



L'eccezione non è stata gestita dal debugger.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_REPLY_LATER"></span><span id="error_dbg_reply_later"></span>**ERRORE \_ dbg \_ risposta in un \_ secondo momento**
</dt> <dd> <dl> <dt>

689 (0x2B1)
</dt> <dt>



Il debugger risponderà in un secondo momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_UNABLE_TO_PROVIDE_HANDLE"></span><span id="error_dbg_unable_to_provide_handle"></span>**ERRORE \_ dbg \_ Impossibile \_ \_ fornire \_ handle**
</dt> <dd> <dl> <dt>

690 (0x2B2)
</dt> <dt>



Il debugger non è in grado di fornire handle.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_TERMINATE_THREAD"></span><span id="error_dbg_terminate_thread"></span>**ERRORE \_ dbg \_ Termina \_ thread**
</dt> <dd> <dl> <dt>

691 (0x2B3)
</dt> <dt>



Thread terminato dal debugger.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_TERMINATE_PROCESS"></span><span id="error_dbg_terminate_process"></span>**ERRORE \_ dbg \_ terminare il \_ processo**
</dt> <dd> <dl> <dt>

692 (0x2B4)
</dt> <dt>



Processo terminato dal debugger.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTROL_C"></span><span id="error_dbg_control_c"></span>**ERRORE \_ dbg \_ controllo \_ C**
</dt> <dd> <dl> <dt>

693 (0x2B5)
</dt> <dt>



Il debugger ha ottenuto il controllo C.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_PRINTEXCEPTION_C"></span><span id="error_dbg_printexception_c"></span>**ERRORE \_ dbg \_ PrintException \_ C**
</dt> <dd> <dl> <dt>

694 (0x2B6)
</dt> <dt>



Eccezione stampata dal debugger sul controllo C.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_RIPEXCEPTION"></span><span id="error_dbg_ripexception"></span>**ERRORE \_ dbg \_ RIPEXCEPTION**
</dt> <dd> <dl> <dt>

695 (0x2B7)
</dt> <dt>



Eccezione RIP ricevuta dal debugger.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTROL_BREAK"></span><span id="error_dbg_control_break"></span>**ERRORE \_ - \_ \_ Interrompi controllo dbg**
</dt> <dd> <dl> <dt>

696 (0x2B8)
</dt> <dt>



Interruzione del controllo ricevuta dal debugger.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_COMMAND_EXCEPTION"></span><span id="error_dbg_command_exception"></span>**\_ \_ eccezione comando dbg \_ errore**
</dt> <dd> <dl> <dt>

697 (0x2B9)
</dt> <dt>



Eccezione di comunicazione del comando del debugger.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NAME_EXISTS"></span><span id="error_object_name_exists"></span>**\_nome oggetto \_ errore \_ esistente**
</dt> <dd> <dl> <dt>

698 (0x2BA)
</dt> <dt>



{Object exists} È stato effettuato un tentativo di creare un oggetto e il nome dell'oggetto esisteva già.


</dt> </dl> </dd> <dt>

<span id="ERROR_THREAD_WAS_SUSPENDED"></span><span id="error_thread_was_suspended"></span>**\_thread di \_ errore \_ sospeso**
</dt> <dd> <dl> <dt>

699 (0x2BB)
</dt> <dt>



{Thread sospeso} Si è verificata una chiusura del thread durante la sospensione del thread. Il thread è stato ripreso e la terminazione continua.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_NOT_AT_BASE"></span><span id="error_image_not_at_base"></span>**\_immagine \_ di errore non \_ alla \_ base**
</dt> <dd> <dl> <dt>

700 (0x2BC)
</dt> <dt>



{Immagine rilocata} Non è stato possibile eseguire il mapping di un file di immagine all'indirizzo specificato nel file di immagine. È necessario eseguire correzioni locali su questa immagine.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_STATE_CREATED"></span><span id="error_rxact_state_created"></span>**\_stato RXACT \_ errore \_ creato**
</dt> <dd> <dl> <dt>

701 (0x2BD)
</dt> <dt>



Questo stato di livello informativo indica che lo stato della transazione di un sottoalbero del registro di sistema specificato non esiste ancora e deve essere creato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SEGMENT_NOTIFICATION"></span><span id="error_segment_notification"></span>**\_notifica del segmento di errore \_**
</dt> <dd> <dl> <dt>

702 (0x2BE)
</dt> <dt>



{Caricamento segmento} Una macchina virtuale DOS (VDM) sta caricando, scaricando o muovendo un'immagine del segmento di programma MS-DOS o Win16. Viene generata un'eccezione in modo che un debugger possa caricare, scaricare o tenere traccia dei simboli e dei punti di interruzione all'interno di questi segmenti a 16 bit.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CURRENT_DIRECTORY"></span><span id="error_bad_current_directory"></span>**ERRORE \_ \_ directory corrente non valida \_**
</dt> <dd> <dl> <dt>

703 (0x2BF)
</dt> <dt>



{Directory corrente non valida} Il processo non può passare alla directory corrente di avvio% HS. Selezionare OK per impostare la directory corrente su% HS oppure selezionare Annulla per uscire.


</dt> </dl> </dd> <dt>

<span id="ERROR_FT_READ_RECOVERY_FROM_BACKUP"></span><span id="error_ft_read_recovery_from_backup"></span>**ERRORE \_ ft \_ lettura \_ ripristino \_ dal \_ backup**
</dt> <dd> <dl> <dt>

704 (0x2C0)
</dt> <dt>



{Lettura ridondante} Per soddisfare una richiesta di lettura, l'file system a tolleranza di errore NT leggere correttamente i dati richiesti da una copia ridondante. Questa operazione è stata eseguita perché il file system ha rilevato un errore in un membro del volume a tolleranza di errore, ma non è stato in grado di riassegnare l'area del dispositivo non riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_FT_WRITE_RECOVERY"></span><span id="error_ft_write_recovery"></span>**errore durante il \_ \_ recupero della scrittura ft \_**
</dt> <dd> <dl> <dt>

705 (0x2C1)
</dt> <dt>



{Scrittura ridondante} Per soddisfare una richiesta di scrittura, il file system a tolleranza di errore NT ha scritto correttamente una copia ridondante delle informazioni. Questa operazione è stata eseguita perché il file system ha rilevato un errore in un membro del volume a tolleranza di errore, ma non è stato in grado di riassegnare l'area del dispositivo non riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH"></span><span id="error_image_machine_type_mismatch"></span>**\_tipo di computer immagine errore non \_ \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

706 (0x2C2)
</dt> <dt>



{Tipo computer non corrispondente} Il file di immagine% HS è valido, ma è per un tipo di computer diverso dal computer corrente. Fare clic su OK per continuare oppure su Annulla per interrompere il caricamento della DLL.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_PARTIAL"></span><span id="error_receive_partial"></span>**ERRORE di \_ ricezione \_ parziale**
</dt> <dd> <dl> <dt>

707 (0x2C3)
</dt> <dt>



{Dati parziali ricevuti} Il trasporto di rete ha restituito i dati parziali al client. I dati rimanenti verranno inviati in un secondo momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_EXPEDITED"></span><span id="error_receive_expedited"></span>**ERRORE di \_ ricezione \_ accelerato**
</dt> <dd> <dl> <dt>

708 (0x2C4)
</dt> <dt>



{Dati accelerati ricevuti} Il trasporto di rete ha restituito i dati al client contrassegnato come accelerato dal sistema remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECEIVE_PARTIAL_EXPEDITED"></span><span id="error_receive_partial_expedited"></span>**errore durante la ricezione di una \_ \_ \_ accelerazione parziale**
</dt> <dd> <dl> <dt>

709 (0x2C5)
</dt> <dt>



{Dati con accelerazione parziale ricevuti} Il trasporto di rete ha restituito i dati parziali al client e tali dati sono stati contrassegnati come accelerati dal sistema remoto. I dati rimanenti verranno inviati in un secondo momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENT_DONE"></span><span id="error_event_done"></span>**evento di errore \_ \_ completato**
</dt> <dd> <dl> <dt>

710 (0x2C6)
</dt> <dt>



{Evento TDI completato} L'indicazione TDI è stata completata correttamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_EVENT_PENDING"></span><span id="error_event_pending"></span>**evento di errore \_ \_ in sospeso**
</dt> <dd> <dl> <dt>

711 (0x2C7)
</dt> <dt>



{Evento TDI in sospeso} L'indicazione TDI è entrata nello stato in sospeso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHECKING_FILE_SYSTEM"></span><span id="error_checking_file_system"></span>**errore durante \_ il controllo del \_ file \_ System**
</dt> <dd> <dl> <dt>

712 (0x2C8)
</dt> <dt>



Controllo file system in% wZ.


</dt> </dl> </dd> <dt>

<span id="ERROR_FATAL_APP_EXIT"></span><span id="error_fatal_app_exit"></span>**ERRORE \_ di \_ uscita dell'app irreversibile \_**
</dt> <dd> <dl> <dt>

713 (0x2C9)
</dt> <dt>



{Chiusura applicazione irreversibile}% HS.


</dt> </dl> </dd> <dt>

<span id="ERROR_PREDEFINED_HANDLE"></span><span id="error_predefined_handle"></span>**\_handle predefinito dell' \_ errore**
</dt> <dd> <dl> <dt>

714 (0x2CA)
</dt> <dt>



Un handle predefinito fa riferimento alla chiave del registro di sistema specificata.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAS_UNLOCKED"></span><span id="error_was_unlocked"></span>**ERRORE \_ \_ sbloccato**
</dt> <dd> <dl> <dt>

715 (0x2CB)
</dt> <dt>



{Pagina sbloccata} La protezione della pagina di una pagina bloccata è stata modificata in "nessun accesso" e la pagina è stata sbloccata dalla memoria e dal processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOTIFICATION"></span><span id="error_service_notification"></span>**\_notifica del servizio di errore \_**
</dt> <dd> <dl> <dt>

716 (0x2CC)
</dt> <dt>



% HS


</dt> </dl> </dd> <dt>

<span id="ERROR_WAS_LOCKED"></span><span id="error_was_locked"></span>**ERRORE \_ \_ bloccato**
</dt> <dd> <dl> <dt>

717 (0x2CD)
</dt> <dt>



{Pagina bloccata} Una delle pagine da bloccare è già bloccata.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_HARD_ERROR"></span><span id="error_log_hard_error"></span>**\_ \_ errore hardware del log degli errori \_**
</dt> <dd> <dl> <dt>

718 (0x2CE)
</dt> <dt>



Popup applicazione: %1: %2


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_WIN32"></span><span id="error_already_win32"></span>**ERRORE \_ già \_ Win32**
</dt> <dd> <dl> <dt>

719 (0x2CF)
</dt> <dt>



ERRORE \_ già \_ Win32


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_MACHINE_TYPE_MISMATCH_EXE"></span><span id="error_image_machine_type_mismatch_exe"></span>**\_tipo computer immagine errore non corrispondente al file \_ \_ \_ \_ exe**
</dt> <dd> <dl> <dt>

720 (0x2D0)
</dt> <dt>



{Tipo computer non corrispondente} Il file di immagine% HS è valido, ma è per un tipo di computer diverso dal computer corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_YIELD_PERFORMED"></span><span id="error_no_yield_performed"></span>**ERRORE \_ nessun \_ rendimento \_ eseguito**
</dt> <dd> <dl> <dt>

721 (0x2D1)
</dt> <dt>



È stata eseguita un'esecuzione del rendimento e non è disponibile alcun thread per l'esecuzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_TIMER_RESUME_IGNORED"></span><span id="error_timer_resume_ignored"></span>**\_riavvio timer di errore \_ \_ ignorato**
</dt> <dd> <dl> <dt>

722 (0x2D2)
</dt> <dt>



Il flag ripristinabile di un'API timer è stato ignorato.


</dt> </dl> </dd> <dt>

<span id="ERROR_ARBITRATION_UNHANDLED"></span><span id="error_arbitration_unhandled"></span>**ERRORE \_ arbitrale non \_ gestito**
</dt> <dd> <dl> <dt>

723 (0x2D3)
</dt> <dt>



L'arbitro ha posticipato l'arbitraggio di queste risorse al padre.


</dt> </dl> </dd> <dt>

<span id="ERROR_CARDBUS_NOT_SUPPORTED"></span><span id="error_cardbus_not_supported"></span>**ERRORE \_ CardBus \_ non \_ supportato**
</dt> <dd> <dl> <dt>

724 (0x2D4)
</dt> <dt>



Impossibile avviare il dispositivo CardBus inserito a causa di un errore di configurazione in "% HS".


</dt> </dl> </dd> <dt>

<span id="ERROR_MP_PROCESSOR_MISMATCH"></span><span id="error_mp_processor_mismatch"></span>**ERRORE \_ processore MP non \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

725 (0x2D5)
</dt> <dt>



Le CPU in questo sistema multiprocessore non hanno lo stesso livello di revisione. Per utilizzare tutti i processori, il sistema operativo si limita alle funzionalità del processore meno idoneo nel sistema. Se si verificano problemi con questo sistema, contattare il produttore della CPU per verificare se questa combinazione di processori è supportata.


</dt> </dl> </dd> <dt>

<span id="ERROR_HIBERNATED"></span><span id="error_hibernated"></span>**ERRORE \_ ibernato**
</dt> <dd> <dl> <dt>

726 (0x2D6)
</dt> <dt>



Il sistema è stato messo in stato di ibernazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESUME_HIBERNATION"></span><span id="error_resume_hibernation"></span>**ERRORE di \_ ripresa della \_ sospensione**
</dt> <dd> <dl> <dt>

727 (0x2D7)
</dt> <dt>



Il sistema è stato ripreso dalla modalità di ibernazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_FIRMWARE_UPDATED"></span><span id="error_firmware_updated"></span>**FIRMWARE degli errori \_ \_ aggiornato**
</dt> <dd> <dl> <dt>

728 (0x2D8)
</dt> <dt>



È stato rilevato che il firmware del sistema (BIOS) è stato aggiornato con la \[ data precedente del firmware = %2, data corrente del firmware %3 \] .


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVERS_LEAKING_LOCKED_PAGES"></span><span id="error_drivers_leaking_locked_pages"></span>**driver di errore \_ \_ perdite \_ di \_ pagine bloccate**
</dt> <dd> <dl> <dt>

729 (0x2D9)
</dt> <dt>



Un driver di dispositivo sta perdendo le pagine di I/O bloccate causando un calo del sistema. Il sistema ha attivato automaticamente il codice di rilevamento per tentare di individuare il problema.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAKE_SYSTEM"></span><span id="error_wake_system"></span>**\_sistema di riattivazione errore \_**
</dt> <dd> <dl> <dt>

730 (0x2DA)
</dt> <dt>



Il sistema si è risvegliato.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_1"></span><span id="error_wait_1"></span>**ERRORE di \_ attesa \_ 1**
</dt> <dd> <dl> <dt>

731 (0x2DB)
</dt> <dt>



ERRORE di \_ attesa \_ 1


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_2"></span><span id="error_wait_2"></span>**ERRORE di \_ attesa \_ 2**
</dt> <dd> <dl> <dt>

732 (0x2DC)
</dt> <dt>



ERRORE di \_ attesa \_ 2


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_3"></span><span id="error_wait_3"></span>**ERRORE di \_ attesa \_ 3**
</dt> <dd> <dl> <dt>

733 (0x2DD)
</dt> <dt>



ERRORE di \_ attesa \_ 3


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_63"></span><span id="error_wait_63"></span>**ERRORE di \_ attesa \_ 63**
</dt> <dd> <dl> <dt>

734 (0x2DE)
</dt> <dt>



ERRORE di \_ attesa \_ 63


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDONED_WAIT_0"></span><span id="error_abandoned_wait_0"></span>**ERRORE \_ di \_ attesa abbandonata \_ 0**
</dt> <dd> <dl> <dt>

735 (0x2DF)
</dt> <dt>



ERRORE \_ di \_ attesa abbandonata \_ 0


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDONED_WAIT_63"></span><span id="error_abandoned_wait_63"></span>**ERRORE \_ di \_ attesa abbandonata \_ 63**
</dt> <dd> <dl> <dt>

736 (0x2E0)
</dt> <dt>



ERRORE \_ di \_ attesa abbandonata \_ 63


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_APC"></span><span id="error_user_apc"></span>**ERRORE \_ \_ APC utente**
</dt> <dd> <dl> <dt>

737 (0x2E1)
</dt> <dt>



ERRORE \_ \_ APC utente


</dt> </dl> </dd> <dt>

<span id="ERROR_KERNEL_APC"></span><span id="error_kernel_apc"></span>**ERRORE del \_ kernel \_ APC**
</dt> <dd> <dl> <dt>

738 (0x2E2)
</dt> <dt>



ERRORE del \_ kernel \_ APC


</dt> </dl> </dd> <dt>

<span id="ERROR_ALERTED"></span><span id="error_alerted"></span>**avviso di errore \_**
</dt> <dd> <dl> <dt>

739 (0x2E3)
</dt> <dt>



avviso di errore \_


</dt> </dl> </dd> <dt>

<span id="ERROR_ELEVATION_REQUIRED"></span><span id="error_elevation_required"></span>**\_elevazione degli errori \_ obbligatoria**
</dt> <dd> <dl> <dt>

740 (0x2E4)
</dt> <dt>



L'operazione richiesta richiede l'elevazione dei privilegi.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE"></span><span id="error_reparse"></span>**ANALISI degli errori \_**
</dt> <dd> <dl> <dt>

741 (0x2E5)
</dt> <dt>



Un reparse deve essere eseguito dal gestore oggetti perché il nome del file ha prodotto un collegamento simbolico.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_BREAK_IN_PROGRESS"></span><span id="error_oplock_break_in_progress"></span>**ERRORE \_ \_ di blocco opportunistico break \_ in \_ corso**
</dt> <dd> <dl> <dt>

742 (0x2E6)
</dt> <dt>



Operazione di apertura/creazione completata mentre è in corso un'blocco opportunistico.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_MOUNTED"></span><span id="error_volume_mounted"></span>**VOLUME di errore \_ \_ montato**
</dt> <dd> <dl> <dt>

743 (0x2E7)
</dt> <dt>



Un nuovo volume è stato montato da un file system.


</dt> </dl> </dd> <dt>

<span id="ERROR_RXACT_COMMITTED"></span><span id="error_rxact_committed"></span>**ERRORE \_ RXACT \_ commit**
</dt> <dd> <dl> <dt>

744 (0x2E8)
</dt> <dt>



Questo stato indica che lo stato della transazione esiste già per il sottoalbero del registro di sistema, ma che il commit di una transazione è stato interrotto in precedenza. Il commit è ora completato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFY_CLEANUP"></span><span id="error_notify_cleanup"></span>**ERRORE \_ notifica \_ pulizia**
</dt> <dd> <dl> <dt>

745 (0x2E9)
</dt> <dt>



Indica che una richiesta di modifica della notifica è stata completata a causa della chiusura dell'handle che ha effettuato la richiesta di modifica della notifica.


</dt> </dl> </dd> <dt>

<span id="ERROR_PRIMARY_TRANSPORT_CONNECT_FAILED"></span><span id="error_primary_transport_connect_failed"></span>**ERRORE \_ di \_ connessione trasporto primario \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

746 (0x2EA)
</dt> <dt>



{Errore di connessione al trasporto primario} È stato effettuato un tentativo di connessione al server remoto% HS sul trasporto primario, ma la connessione non è riuscita. Il computer è stato in grado di connettersi a un trasporto secondario.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_TRANSITION"></span><span id="error_page_fault_transition"></span>**\_transizione errore pagina errori \_ \_**
</dt> <dd> <dl> <dt>

747 (0x2EB)
</dt> <dt>



Errore di pagina: errore di transizione.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_DEMAND_ZERO"></span><span id="error_page_fault_demand_zero"></span>**errore della pagina di errore della \_ \_ \_ richiesta di errori \_**
</dt> <dd> <dl> <dt>

748 (0x2EC)
</dt> <dt>



Errore di pagina: errore di richiesta zero.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_COPY_ON_WRITE"></span><span id="error_page_fault_copy_on_write"></span>**copia degli errori \_ \_ di pagina di errore durante la \_ \_ \_ scrittura**
</dt> <dd> <dl> <dt>

749 (0x2ED)
</dt> <dt>



Errore di pagina: errore di richiesta zero.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_GUARD_PAGE"></span><span id="error_page_fault_guard_page"></span>**\_pagina errore \_ pagina \_ protezione \_ errori**
</dt> <dd> <dl> <dt>

750 (0x2EE)
</dt> <dt>



Errore di pagina: errore di richiesta zero.


</dt> </dl> </dd> <dt>

<span id="ERROR_PAGE_FAULT_PAGING_FILE"></span><span id="error_page_fault_paging_file"></span>**\_file di \_ paging degli errori di pagina errore \_ \_**
</dt> <dd> <dl> <dt>

751 (0x2EF)
</dt> <dt>



L'errore di pagina è stato soddisfatto leggendo da un dispositivo di archiviazione secondario.


</dt> </dl> </dd> <dt>

<span id="ERROR_CACHE_PAGE_LOCKED"></span><span id="error_cache_page_locked"></span>**\_pagina cache degli errori \_ \_ bloccata**
</dt> <dd> <dl> <dt>

752 (0x2F0)
</dt> <dt>



Pagina memorizzata nella cache bloccata durante l'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRASH_DUMP"></span><span id="error_crash_dump"></span>**\_dump di arresto anomalo errore \_**
</dt> <dd> <dl> <dt>

753 (0x2F1)
</dt> <dt>



Il dump di arresto anomalo esiste nel file di paging.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUFFER_ALL_ZEROS"></span><span id="error_buffer_all_zeros"></span>**BUFFER di errore \_ \_ tutti \_ zeri**
</dt> <dd> <dl> <dt>

754 (0x2F2)
</dt> <dt>



Il buffer specificato contiene tutti gli zeri.


</dt> </dl> </dd> <dt>

<span id="ERROR_REPARSE_OBJECT"></span><span id="error_reparse_object"></span>**ERRORE di \_ reparse \_ Object**
</dt> <dd> <dl> <dt>

755 (0x2F3)
</dt> <dt>



Un reparse deve essere eseguito dal gestore oggetti perché il nome del file ha prodotto un collegamento simbolico.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCE_REQUIREMENTS_CHANGED"></span><span id="error_resource_requirements_changed"></span>**\_requisiti delle risorse di errore \_ \_ modificati**
</dt> <dd> <dl> <dt>

756 (0x2F4)
</dt> <dt>



Il dispositivo è riuscito a eseguire una query e i requisiti relativi alle risorse sono stati modificati.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSLATION_COMPLETE"></span><span id="error_translation_complete"></span>**\_traduzione errore \_ completata**
</dt> <dd> <dl> <dt>

757 (0x2F5)
</dt> <dt>



Il traduttore ha tradotto queste risorse nello spazio globale e non è necessario eseguire altre traduzioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTHING_TO_TERMINATE"></span><span id="error_nothing_to_terminate"></span>**\_nessun errore \_ da \_ terminare**
</dt> <dd> <dl> <dt>

758 (0x2F6)
</dt> <dt>



Un processo terminato non dispone di thread da terminare.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_NOT_IN_JOB"></span><span id="error_process_not_in_job"></span>**\_processo \_ di errore non \_ nel \_ processo**
</dt> <dd> <dl> <dt>

759 (0x2F7)
</dt> <dt>



Il processo specificato non fa parte di un processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_IN_JOB"></span><span id="error_process_in_job"></span>**\_processo \_ di errore nel processo \_**
</dt> <dd> <dl> <dt>

760 (0x2F8)
</dt> <dt>



Il processo specificato fa parte di un processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLSNAP_HIBERNATE_READY"></span><span id="error_volsnap_hibernate_ready"></span>**ERRORE \_ VolSnap \_ ibernato \_ pronto**
</dt> <dd> <dl> <dt>

761 (0x2F9)
</dt> <dt>



{Servizio Copia Shadow del volume} Il sistema è ora pronto per l'ibernazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_FSFILTER_OP_COMPLETED_SUCCESSFULLY"></span><span id="error_fsfilter_op_completed_successfully"></span>**ERRORE \_ FSFILTER \_ op \_ completato \_ correttamente**
</dt> <dd> <dl> <dt>

762 (0x2FA)
</dt> <dt>



Un driver di filtro file system o file system ha completato un'operazione FsFilter.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERRUPT_VECTOR_ALREADY_CONNECTED"></span><span id="error_interrupt_vector_already_connected"></span>**il \_ vettore di interrupt errore è \_ \_ già \_ connesso**
</dt> <dd> <dl> <dt>

763 (0x2FB)
</dt> <dt>



Il vettore di interrupt specificato è già connesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_INTERRUPT_STILL_CONNECTED"></span><span id="error_interrupt_still_connected"></span>**ERRORE di \_ interrupt \_ ancora \_ connesso**
</dt> <dd> <dl> <dt>

764 (0x2FC)
</dt> <dt>



Il vettore di interrupt specificato è ancora connesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_WAIT_FOR_OPLOCK"></span><span id="error_wait_for_oplock"></span>**ERRORE \_ \_ di attesa per \_ blocco opportunistico**
</dt> <dd> <dl> <dt>

765 (0x2FD)
</dt> <dt>



Un'operazione è bloccata in attesa di un blocco opportunistico.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_EXCEPTION_HANDLED"></span><span id="error_dbg_exception_handled"></span>**\_eccezione DBG di errore \_ \_ gestita**
</dt> <dd> <dl> <dt>

766 (0x2FE)
</dt> <dt>



Eccezione gestita dal debugger.


</dt> </dl> </dd> <dt>

<span id="ERROR_DBG_CONTINUE"></span><span id="error_dbg_continue"></span>**ERRORE \_ dbg \_ continuare**
</dt> <dd> <dl> <dt>

767 (0x2FF)
</dt> <dt>



Debugger prosegue.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALLBACK_POP_STACK"></span><span id="error_callback_pop_stack"></span>**\_ \_ pop stack callback \_ errore**
</dt> <dd> <dl> <dt>

768 (0x300)
</dt> <dt>



Si è verificata un'eccezione in un callback in modalità utente e il frame di callback del kernel deve essere rimosso.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSION_DISABLED"></span><span id="error_compression_disabled"></span>**compressione degli errori \_ \_ disabilitata**
</dt> <dd> <dl> <dt>

769 (0x301)
</dt> <dt>



La compressione è disabilitata per questo volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTFETCHBACKWARDS"></span><span id="error_cantfetchbackwards"></span>**ERRORE \_ CANTFETCHBACKWARDS**
</dt> <dd> <dl> <dt>

770 (0x302)
</dt> <dt>



Il provider di dati non è in grado di recuperare le versioni precedenti di un set di risultati.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTSCROLLBACKWARDS"></span><span id="error_cantscrollbackwards"></span>**ERRORE \_ CANTSCROLLBACKWARDS**
</dt> <dd> <dl> <dt>

771 (0x303)
</dt> <dt>



Il provider di dati non è in grado di scorrere indietro di un set di risultati.


</dt> </dl> </dd> <dt>

<span id="ERROR_ROWSNOTRELEASED"></span><span id="error_rowsnotreleased"></span>**ERRORE \_ ROWSNOTRELEASED**
</dt> <dd> <dl> <dt>

772 (0x304)
</dt> <dt>



Il provider di dati richiede che i dati recuperati in precedenza vengano rilasciati prima di richiedere più dati.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_ACCESSOR_FLAGS"></span><span id="error_bad_accessor_flags"></span>**\_flag della \_ funzione di accesso ERRAta Error \_**
</dt> <dd> <dl> <dt>

773 (0x305)
</dt> <dt>



Il provider di dati non è stato in grado di interpretare i flag impostati per un'associazione di colonna in una funzione di accesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_ERRORS_ENCOUNTERED"></span><span id="error_errors_encountered"></span>**\_errori \_ rilevati**
</dt> <dd> <dl> <dt>

774 (0x306)
</dt> <dt>



Si sono verificati uno o più errori durante l'elaborazione della richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CAPABLE"></span><span id="error_not_capable"></span>**ERRORE \_ non \_ idoneo**
</dt> <dd> <dl> <dt>

775 (0x307)
</dt> <dt>



L'implementazione non è in grado di eseguire la richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_OUT_OF_SEQUENCE"></span><span id="error_request_out_of_sequence"></span>**\_richiesta \_ di errore \_ fuori \_ sequenza**
</dt> <dd> <dl> <dt>

776 (0x308)
</dt> <dt>



Il client di un componente ha richiesto un'operazione non valida in base allo stato dell'istanza del componente.


</dt> </dl> </dd> <dt>

<span id="ERROR_VERSION_PARSE_ERROR"></span><span id="error_version_parse_error"></span>**errore di \_ analisi della versione errore \_ \_**
</dt> <dd> <dl> <dt>

777 (0x309)
</dt> <dt>



Non è stato possibile analizzare un numero di versione.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADSTARTPOSITION"></span><span id="error_badstartposition"></span>**ERRORE \_ BADSTARTPOSITION**
</dt> <dd> <dl> <dt>

778 (0x30A)
</dt> <dt>



La posizione iniziale dell'iteratore non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEMORY_HARDWARE"></span><span id="error_memory_hardware"></span>**\_hardware memoria \_ errore**
</dt> <dd> <dl> <dt>

779 (0x30B)
</dt> <dt>



L'hardware ha segnalato un errore di memoria non correggibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_DISABLED"></span><span id="error_disk_repair_disabled"></span>**ripristino del disco di errore \_ \_ \_ disabilitato**
</dt> <dd> <dl> <dt>

780 (0x30C)
</dt> <dt>



È stata richiesta l'abilitazione dell'operazione di correzione automatica.


</dt> </dl> </dd> <dt>

<span id="ERROR_INSUFFICIENT_RESOURCE_FOR_SPECIFIED_SHARED_SECTION_SIZE"></span><span id="error_insufficient_resource_for_specified_shared_section_size"></span>**ERRORE \_ \_ di risorsa insufficiente \_ per le \_ \_ dimensioni di sezione condivise specificate \_ \_**
</dt> <dd> <dl> <dt>

781 (0x30D)
</dt> <dt>



Si è verificato un errore nell'heap del desktop durante l'allocazione della memoria della sessione. Sono disponibili ulteriori informazioni nel registro eventi di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_POWERSTATE_TRANSITION"></span><span id="error_system_powerstate_transition"></span>**\_ \_ transizione PowerState sistema di errore \_**
</dt> <dd> <dl> <dt>

782 (0x30E)
</dt> <dt>



Lo stato di alimentazione del sistema è in fase di transizione da %2 a %3.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYSTEM_POWERSTATE_COMPLEX_TRANSITION"></span><span id="error_system_powerstate_complex_transition"></span>**ERRORE \_ di \_ PowerState sistema di \_ \_ transizione complessa**
</dt> <dd> <dl> <dt>

783 (0x30F)
</dt> <dt>



Lo stato di alimentazione del sistema è in fase di transizione da %2 a %3, ma è possibile immettere %4.


</dt> </dl> </dd> <dt>

<span id="ERROR_MCA_EXCEPTION"></span><span id="error_mca_exception"></span>**ERRORE \_ MCA \_ eccezione**
</dt> <dd> <dl> <dt>

784 (0x310)
</dt> <dt>



Un thread viene inviato con l'eccezione MCA a causa di MCA.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_AUDIT_BY_POLICY"></span><span id="error_access_audit_by_policy"></span>**\_ \_ controllo degli errori \_ di accesso per \_ criterio**
</dt> <dd> <dl> <dt>

785 (0x311)
</dt> <dt>



L'accesso a %1 è stato monitorato dalla regola dei criteri %2.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_NO_SAFER_UI_BY_POLICY"></span><span id="error_access_disabled_no_safer_ui_by_policy"></span>**\_accesso agli errori \_ disabilitato \_ senza \_ \_ interfaccia utente sicura \_ per \_ criterio**
</dt> <dd> <dl> <dt>

786 (0x312)
</dt> <dt>



L'accesso a %1 è stato limitato dall'amministratore dalla regola dei criteri %2.


</dt> </dl> </dd> <dt>

<span id="ERROR_ABANDON_HIBERFILE"></span><span id="error_abandon_hiberfile"></span>**errore durante l' \_ abbandono di \_ HIBERFILE**
</dt> <dd> <dl> <dt>

787 (0x313)
</dt> <dt>



Un file di ibernazione valido è stato invalidato e deve essere abbandonato.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_DISCONNECTED"></span><span id="error_lost_writebehind_data_network_disconnected"></span>**errore durante la \_ perdita della \_ \_ rete dati WRITEBEHIND \_ \_ disconnessa**
</dt> <dd> <dl> <dt>

788 (0x314)
</dt> <dt>



{Scrittura ritardata non riuscita} Windows non è riuscito a salvare tutti i dati per il file% HS; i dati sono andati persi. Questo errore può essere causato da problemi di connettività di rete. Provare a salvare il file altrove.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_NETWORK_SERVER_ERROR"></span><span id="error_lost_writebehind_data_network_server_error"></span>**ERRORE durante la \_ perdita di \_ WRITEBEHIND \_ data \_ Network \_ server \_ Error**
</dt> <dd> <dl> <dt>

789 (0x315)
</dt> <dt>



{Scrittura ritardata non riuscita} Windows non è riuscito a salvare tutti i dati per il file% HS; i dati sono andati persi. Questo errore è stato restituito dal server in cui si trova il file. Provare a salvare il file altrove.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOST_WRITEBEHIND_DATA_LOCAL_DISK_ERROR"></span><span id="error_lost_writebehind_data_local_disk_error"></span>**errore durante la \_ perdita \_ \_ \_ del \_ disco locale di dati WRITEBEHIND \_**
</dt> <dd> <dl> <dt>

790 (0x316)
</dt> <dt>



{Scrittura ritardata non riuscita} Windows non è riuscito a salvare tutti i dati per il file% HS; i dati sono andati persi. Questo errore può essere causato dal fatto che il dispositivo è stato rimosso o il supporto è protetto da scrittura.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_MCFG_TABLE"></span><span id="error_bad_mcfg_table"></span>**ERRORE \_ nella \_ tabella MCFG non valida \_**
</dt> <dd> <dl> <dt>

791 (0x317)
</dt> <dt>



Le risorse necessarie per questo dispositivo sono in conflitto con la tabella MCFG.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_REDIRECTED"></span><span id="error_disk_repair_redirected"></span>**ripristino del disco di errore \_ \_ \_ reindirizzato**
</dt> <dd> <dl> <dt>

792 (0x318)
</dt> <dt>



Non è stato possibile eseguire il ripristino del volume mentre è in linea. Pianificare per portare il volume offline in modo che possa essere ripristinato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_REPAIR_UNSUCCESSFUL"></span><span id="error_disk_repair_unsuccessful"></span>**correzione del disco di errore non \_ \_ \_ riuscita**
</dt> <dd> <dl> <dt>

793 (0x319)
</dt> <dt>



Il ripristino del volume non è riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_OVERFULL"></span><span id="error_corrupt_log_overfull"></span>**ERRORE \_ di \_ log \_ danneggiato**
</dt> <dd> <dl> <dt>

794 (0x31A)
</dt> <dt>



Uno dei log di danneggiamento del volume è pieno. Ulteriori danneggiamenti che potrebbero essere rilevati non verranno registrati.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_CORRUPTED"></span><span id="error_corrupt_log_corrupted"></span>**ERRORE \_ del \_ log \_ danneggiato**
</dt> <dd> <dl> <dt>

795 (0x31B)
</dt> <dt>



Uno dei log di danneggiamento del volume è danneggiato internamente ed è necessario ricrearlo. Il volume può contenere danneggiamenti non rilevati e deve essere analizzato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_UNAVAILABLE"></span><span id="error_corrupt_log_unavailable"></span>**ERRORE \_ del \_ log danneggiato non \_ disponibile**
</dt> <dd> <dl> <dt>

796 (0x31C)
</dt> <dt>



Uno dei log di danneggiamento del volume non è disponibile per essere utilizzato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_DELETED_FULL"></span><span id="error_corrupt_log_deleted_full"></span>**ERRORE \_ di \_ log danneggiato \_ eliminato \_**
</dt> <dd> <dl> <dt>

797 (0x31D)
</dt> <dt>



Uno dei log di danneggiamento del volume è stato eliminato mentre erano ancora presenti record di danneggiamento. Il volume contiene i danneggiamenti rilevati e deve essere analizzato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CORRUPT_LOG_CLEARED"></span><span id="error_corrupt_log_cleared"></span>**ERRORE \_ di \_ log danneggiato \_ cancellato**
</dt> <dd> <dl> <dt>

798 (0x31E)
</dt> <dt>



Uno dei log di danneggiamento del volume è stato cancellato da CHKDSK e non contiene più i danneggiamenti reali.


</dt> </dl> </dd> <dt>

<span id="ERROR_ORPHAN_NAME_EXHAUSTED"></span><span id="error_orphan_name_exhausted"></span>**ERRORE \_ nome orfano \_ \_ esaurito**
</dt> <dd> <dl> <dt>

799 (0x31F)
</dt> <dt>



I file orfani esistono nel volume, ma non possono essere recuperati perché non è stato possibile creare altri nuovi nomi nella directory di ripristino. I file devono essere spostati dalla directory di ripristino.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_SWITCHED_TO_NEW_HANDLE"></span><span id="error_oplock_switched_to_new_handle"></span>**ERRORE \_ blocco opportunistico \_ passato \_ al \_ nuovo \_ handle**
</dt> <dd> <dl> <dt>

800 (0x320)
</dt> <dt>



Il blocco opportunistico associato a questo handle è ora associato a un handle diverso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_GRANT_REQUESTED_OPLOCK"></span><span id="error_cannot_grant_requested_oplock"></span>**ERRORE \_ non può \_ concedere il \_ \_ blocco opportunistico richiesto**
</dt> <dd> <dl> <dt>

801 (0x321)
</dt> <dt>



Non è possibile concedere un blocco opportunistico del livello richiesto. Potrebbe essere disponibile un blocco opportunistico di un livello inferiore.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_BREAK_OPLOCK"></span><span id="error_cannot_break_oplock"></span>**ERRORE \_ Impossibile \_ interrompere \_ blocco opportunistico**
</dt> <dd> <dl> <dt>

802 (0x322)
</dt> <dt>



L'operazione non è stata completata correttamente perché potrebbe causare l'interruzione di un blocco opportunistico. Il chiamante ha richiesto l'interruzione del oplock esistente.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPLOCK_HANDLE_CLOSED"></span><span id="error_oplock_handle_closed"></span>**ERRORE \_ blocco opportunistico \_ handle \_ chiuso**
</dt> <dd> <dl> <dt>

803 (0x323)
</dt> <dt>



L'handle a cui è stato associato questo blocco opportunistico è stato chiuso. Il blocco opportunistico è ora rotto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_ACE_CONDITION"></span><span id="error_no_ace_condition"></span>**ERRORE \_ Nessuna \_ \_ condizione ACE**
</dt> <dd> <dl> <dt>

804 (0x324)
</dt> <dt>



La voce di controllo di accesso (ACE) specificata non contiene una condizione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_ACE_CONDITION"></span><span id="error_invalid_ace_condition"></span>**ERRORE \_ \_ condizione ACE non valida \_**
</dt> <dd> <dl> <dt>

805 (0x325)
</dt> <dt>



La voce di controllo di accesso (ACE) specificata contiene una condizione non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_HANDLE_REVOKED"></span><span id="error_file_handle_revoked"></span>**HANDLE di file di errore \_ \_ \_ revocato**
</dt> <dd> <dl> <dt>

806 (0x326)
</dt> <dt>



L'accesso all'handle di file specificato è stato revocato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMAGE_AT_DIFFERENT_BASE"></span><span id="error_image_at_different_base"></span>**\_immagine \_ di errore con \_ \_ base diversa**
</dt> <dd> <dl> <dt>

807 (0x327)
</dt> <dt>



È stato eseguito il mapping di un file di immagine a un indirizzo diverso da quello specificato nel file di immagine, ma correzioni verrà ancora eseguito automaticamente nell'immagine.


</dt> </dl> </dd> <dt>

<span id="ERROR_EA_ACCESS_DENIED"></span><span id="error_ea_access_denied"></span>**ERRORE \_ accesso a EA \_ \_ negato**
</dt> <dd> <dl> <dt>

994 (0x3E2)
</dt> <dt>



Accesso all'attributo esteso negato.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_ABORTED"></span><span id="error_operation_aborted"></span>**operazione di errore \_ \_ interrotta**
</dt> <dd> <dl> <dt>

995 (0x3E3)
</dt> <dt>



L'operazione di I/O è stata interrotta a causa dell'uscita di un thread o di una richiesta dell'applicazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_INCOMPLETE"></span><span id="error_io_incomplete"></span>**ERRORE \_ io \_ incompleto**
</dt> <dd> <dl> <dt>

996 (0x3E4)
</dt> <dt>



L'evento di I/O sovrapposto non è in uno stato segnalato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_PENDING"></span><span id="error_io_pending"></span>**ERRORE i/o \_ \_ in sospeso**
</dt> <dd> <dl> <dt>

997 (0x3E5)
</dt> <dt>



Operazione di I/O sovrapposta in corso.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOACCESS"></span><span id="error_noaccess"></span>**ERRORE \_ NOaccess**
</dt> <dd> <dl> <dt>

998 (0x3E6)
</dt> <dt>



Accesso non valido alla posizione di memoria.


</dt> </dl> </dd> <dt>

<span id="ERROR_SWAPERROR"></span><span id="error_swaperror"></span>**ERRORE \_ SWAPERROR**
</dt> <dd> <dl> <dt>

999 (0x3E7)
</dt> <dt>



Errore durante l'esecuzione dell'operazione di inpaginazione.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di errore di sistema](system-error-codes.md)
</dt> </dl>

 

 
