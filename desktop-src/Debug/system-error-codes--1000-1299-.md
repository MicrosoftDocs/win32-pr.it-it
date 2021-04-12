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
# <a name="system-error-codes-1000-1299"></a>Codici di errore di sistema (1000-1299)

> [!NOTE]
> Queste informazioni sono destinate agli sviluppatori che effettuano il debug degli errori di sistema. Per altri errori, ad esempio problemi con Windows Update, è disponibile un elenco di risorse nella pagina [codici di errore](system-error-codes.md) .

Nell'elenco seguente vengono descritti i [codici di errore di sistema](system-error-codes.md) per gli errori da 1000 a 1299. Vengono restituiti dalla funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo. Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la funzione [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il **formato \_ Message from flag \_ di \_ sistema** .

<dl> <dt>

<span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**\_overflow dello stack di errori \_**
</dt> <dd> <dl> <dt>

1001 (0x3E9)
</dt> <dt>



Ricorsione troppo profonda; overflow dello stack.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**messaggio di errore \_ non valido \_**
</dt> <dd> <dl> <dt>

1002 (0x3EA)
</dt> <dt>



La finestra non può agire sul messaggio inviato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**\_non è \_ possibile \_ completare l'errore**
</dt> <dd> <dl> <dt>

1003 (0x3EB)
</dt> <dt>



Non è possibile completare questa funzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**flag di errore \_ non validi \_**
</dt> <dd> <dl> <dt>

1004 (0x3EC)
</dt> <dt>



Flag non validi.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**ERRORE \_ volume non riconosciuto \_**
</dt> <dd> <dl> <dt>

1005 (0x3ED)
</dt> <dt>



Il volume non contiene un file system riconosciuto. Verificare che tutti i driver di file system necessari siano caricati e che il volume non sia danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**FILE degli errori \_ \_ non valido**
</dt> <dd> <dl> <dt>

1006 (0x3EE)
</dt> <dt>



Il volume di un file è stato modificato esternamente in modo che il file aperto non sia più valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**\_modalità a schermo intero errore \_**
</dt> <dd> <dl> <dt>

1007 (0x3EF)
</dt> <dt>



L'operazione richiesta non può essere eseguita in modalità schermo intero.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**ERRORE \_ nessun \_ token**
</dt> <dd> <dl> <dt>

1008 (0x3F0)
</dt> <dt>



È stato effettuato un tentativo di fare riferimento a un token che non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADDB"></span><span id="error_baddb"></span>**ERRORE \_ BADDB**
</dt> <dd> <dl> <dt>

1009 (0x3F1)
</dt> <dt>



Il database del registro di sistema di configurazione è danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**ERRORE \_ BADKEY**
</dt> <dd> <dl> <dt>

1010 (0x3F2)
</dt> <dt>



La chiave del registro di sistema di configurazione non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**ERRORE \_ CANTOPEN**
</dt> <dd> <dl> <dt>

1011 (0x3F3)
</dt> <dt>



Non è stato possibile aprire la chiave del registro di sistema per la configurazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**ERRORE \_ CANTREAD**
</dt> <dd> <dl> <dt>

1012 (0x3F4)
</dt> <dt>



Impossibile leggere la chiave del registro di sistema per la configurazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**ERRORE \_ CANTWRITE**
</dt> <dd> <dl> <dt>

1013 (0x3F5)
</dt> <dt>



Impossibile scrivere la chiave del registro di sistema per la configurazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**\_registro errori \_ recuperato**
</dt> <dd> <dl> <dt>

1014 (0x3F6)
</dt> <dt>



Uno dei file nel database del registro di sistema deve essere recuperato tramite un log o una copia alternativa. Il ripristino è stato completato correttamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**\_registro errori \_ danneggiato**
</dt> <dd> <dl> <dt>

1015 (0x3F7)
</dt> <dt>



Il registro di sistema è danneggiato. La struttura di uno dei file contenenti i dati del registro di sistema è danneggiata oppure l'immagine di memoria del sistema del file è danneggiata oppure il file non può essere recuperato perché la copia o il registro alternativo è assente o danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**ERRORE i/o \_ Registro di sistema \_ \_ non riuscito**
</dt> <dd> <dl> <dt>

1016 (0x3F8)
</dt> <dt>



Un'operazione di I/O avviata dal registro di sistema non è riuscita in modo irreversibile. Il registro di sistema non è stato in grado di leggere o scrivere o scaricare uno dei file che contiene l'immagine del sistema del registro di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**ERRORE \_ nel \_ file del registro di sistema \_**
</dt> <dd> <dl> <dt>

1017 (0x3F9)
</dt> <dt>



Il sistema ha tentato di caricare o ripristinare un file nel registro di sistema, ma il file specificato non è in un formato di file del registro di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**chiave di errore \_ \_ eliminata**
</dt> <dd> <dl> <dt>

1018 (0x3FA)
</dt> <dt>



Si è tentato di eseguire un'operazione non valida su una chiave del registro di sistema contrassegnata per l'eliminazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**ERRORE \_ senza \_ spazio di log \_**
</dt> <dd> <dl> <dt>

1019 (0x3FB)
</dt> <dt>



Impossibile allocare lo spazio richiesto in un registro del registro di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**chiave di errore \_ \_ con \_ elementi figlio**
</dt> <dd> <dl> <dt>

1020 (0x3FC)
</dt> <dt>



Non è possibile creare un collegamento simbolico in una chiave del registro di sistema in cui sono già presenti sottochiavi o valori.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**il \_ figlio di errore \_ deve \_ essere \_ volatile**
</dt> <dd> <dl> <dt>

1021 (0x3FD)
</dt> <dt>



Non è possibile creare una sottochiave stabile in una chiave padre volatile.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**ERRORE di \_ notifica dell' \_ enumerazione \_ dir**
</dt> <dd> <dl> <dt>

1022 (0x3FE)
</dt> <dt>



Viene completata una richiesta di modifica della notifica e le informazioni non vengono restituite nel buffer del chiamante. Il chiamante deve ora enumerare i file per individuare le modifiche.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**\_servizi dipendenti dall'errore \_ \_ in esecuzione**
</dt> <dd> <dl> <dt>

1051 (0x41B)
</dt> <dt>



Un controllo stop è stato inviato a un servizio da cui dipendono altri servizi in esecuzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**ERRORE \_ di \_ controllo del servizio non valido \_**
</dt> <dd> <dl> <dt>

1052 (0x41C)
</dt> <dt>



Il controllo richiesto non è valido per questo servizio.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**\_timeout della \_ richiesta del servizio di errore \_**
</dt> <dd> <dl> <dt>

1053 (0x41D)
</dt> <dt>



Il servizio non ha risposto in tempo utile alla richiesta di avvio o di controllo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**ERRORE \_ servizio \_ senza \_ thread**
</dt> <dd> <dl> <dt>

1054 (0x41E)
</dt> <dt>



Non è stato possibile creare un thread per il servizio.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**DATABASE del servizio di errore \_ \_ \_ bloccato**
</dt> <dd> <dl> <dt>

1055 (0x41F)
</dt> <dt>



Il database del servizio è bloccato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**\_servizio errori \_ già \_ in esecuzione**
</dt> <dd> <dl> <dt>

1056 (0x420)
</dt> <dt>



Un'istanza del servizio è già in esecuzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**ERRORE \_ dell' \_ account del servizio non valido \_**
</dt> <dd> <dl> <dt>

1057 (0x421)
</dt> <dt>



Il nome dell'account non è valido o non esiste oppure la password non è valida per il nome dell'account specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DISABLED"></span><span id="error_service_disabled"></span>**\_servizio errori \_ disabilitato**
</dt> <dd> <dl> <dt>

1058 (0x422)
</dt> <dt>



Non è possibile avviare il servizio perché è disabilitato o perché ad esso non è associato alcun dispositivo abilitato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CIRCULAR_DEPENDENCY"></span><span id="error_circular_dependency"></span>**\_dipendenza circolare degli errori \_**
</dt> <dd> <dl> <dt>

1059 (0x423)
</dt> <dt>



È stata specificata la dipendenza circolare del servizio.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DOES_NOT_EXIST"></span><span id="error_service_does_not_exist"></span>**\_il servizio errori non \_ \_ \_ esiste**
</dt> <dd> <dl> <dt>

1060 (0x424)
</dt> <dt>



Il servizio specificato non esiste come servizio installato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_CANNOT_ACCEPT_CTRL"></span><span id="error_service_cannot_accept_ctrl"></span>**il \_ servizio di errore \_ non può \_ accettare \_ CTRL**
</dt> <dd> <dl> <dt>

1061 (0x425)
</dt> <dt>



Il servizio non può accettare messaggi di controllo in questo momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_ACTIVE"></span><span id="error_service_not_active"></span>**\_servizio errori \_ non \_ attivo**
</dt> <dd> <dl> <dt>

1062 (0x426)
</dt> <dt>



Il servizio non è stato avviato.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAILED_SERVICE_CONTROLLER_CONNECT"></span><span id="error_failed_service_controller_connect"></span>**ERRORE \_ di \_ \_ connessione del controller di servizio non riuscito \_**
</dt> <dd> <dl> <dt>

1063 (0x427)
</dt> <dt>



Il processo del servizio non è stato in grado di connettersi al controller del servizio.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCEPTION_IN_SERVICE"></span><span id="error_exception_in_service"></span>**\_eccezione \_ di errore nel \_ servizio**
</dt> <dd> <dl> <dt>

1064 (0x428)
</dt> <dt>



Si è verificata un'eccezione nel servizio durante la gestione della richiesta di controllo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_DOES_NOT_EXIST"></span><span id="error_database_does_not_exist"></span>**il database degli errori non \_ \_ \_ \_ esiste**
</dt> <dd> <dl> <dt>

1065 (0x429)
</dt> <dt>



Il database specificato non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_SPECIFIC_ERROR"></span><span id="error_service_specific_error"></span>**errore \_ specifico del servizio di errore \_ \_**
</dt> <dd> <dl> <dt>

1066 (0x42A)
</dt> <dt>



Il servizio ha restituito un codice di errore specifico del servizio.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_ABORTED"></span><span id="error_process_aborted"></span>**processo di errore \_ \_ interrotto**
</dt> <dd> <dl> <dt>

1067 (0x42B)
</dt> <dt>



Il processo è stato terminato in modo imprevisto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DEPENDENCY_FAIL"></span><span id="error_service_dependency_fail"></span>**errore di \_ dipendenza del servizio errori \_ \_**
</dt> <dd> <dl> <dt>

1068 (0x42C)
</dt> <dt>



Impossibile avviare il servizio o il gruppo di dipendenze.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_LOGON_FAILED"></span><span id="error_service_logon_failed"></span>**accesso al servizio di errore \_ \_ \_ non riuscito**
</dt> <dd> <dl> <dt>

1069 (0x42D)
</dt> <dt>



il servizio non è stato avviato a causa di un errore in fase di accesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_START_HANG"></span><span id="error_service_start_hang"></span>**\_ \_ blocco avvio servizio \_ errori**
</dt> <dd> <dl> <dt>

1070 (0x42E)
</dt> <dt>



Dopo l'avvio, il servizio è stato bloccato in uno stato di avvio in sospeso.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_LOCK"></span><span id="error_invalid_service_lock"></span>**ERRORE \_ \_ Blocco servizio non valido \_**
</dt> <dd> <dl> <dt>

1071 (0x42F)
</dt> <dt>



Il blocco del database del servizio specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_MARKED_FOR_DELETE"></span><span id="error_service_marked_for_delete"></span>**\_servizio \_ di errore contrassegnato per l' \_ \_ eliminazione**
</dt> <dd> <dl> <dt>

1072 (0x430)
</dt> <dt>



Il servizio specificato è stato contrassegnato per l'eliminazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_EXISTS"></span><span id="error_service_exists"></span>**il \_ servizio di errore \_ esiste**
</dt> <dd> <dl> <dt>

1073 (0x431)
</dt> <dt>



Il servizio specificato esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_RUNNING_LKG"></span><span id="error_already_running_lkg"></span>**errore durante l' \_ \_ esecuzione di \_ Ultima**
</dt> <dd> <dl> <dt>

1074 (0x432)
</dt> <dt>



Il sistema è attualmente in esecuzione con l'ultima configurazione ben nota.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DEPENDENCY_DELETED"></span><span id="error_service_dependency_deleted"></span>**dipendenza del servizio di errore \_ \_ \_ eliminata**
</dt> <dd> <dl> <dt>

1075 (0x433)
</dt> <dt>



Il servizio di dipendenza non esiste o è stato contrassegnato per l'eliminazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_BOOT_ALREADY_ACCEPTED"></span><span id="error_boot_already_accepted"></span>**ERRORE di \_ avvio \_ già \_ accettato**
</dt> <dd> <dl> <dt>

1076 (0x434)
</dt> <dt>



L'avvio corrente è già stato accettato per l'uso come ultimo set di controlli valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NEVER_STARTED"></span><span id="error_service_never_started"></span>**il \_ servizio di errore \_ non è mai stato \_ avviato**
</dt> <dd> <dl> <dt>

1077 (0x435)
</dt> <dt>



Nessun tentativo di avviare il servizio è stato eseguito dopo l'ultimo avvio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_SERVICE_NAME"></span><span id="error_duplicate_service_name"></span>**\_nome del \_ servizio DUPLICAto errore \_**
</dt> <dd> <dl> <dt>

1078 (0x436)
</dt> <dt>



Il nome è già in uso come nome del servizio o nome visualizzato del servizio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIFFERENT_SERVICE_ACCOUNT"></span><span id="error_different_service_account"></span>**ERRORE \_ dell' \_ account del servizio diverso \_**
</dt> <dd> <dl> <dt>

1079 (0x437)
</dt> <dt>



L'account specificato per questo servizio è diverso dall'account specificato per altri servizi in esecuzione nello stesso processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_DETECT_DRIVER_FAILURE"></span><span id="error_cannot_detect_driver_failure"></span>**errore durante il rilevamento dell'errore del \_ \_ \_ driver \_**
</dt> <dd> <dl> <dt>

1080 (nell'0x438)
</dt> <dt>



Le azioni di errore possono essere impostate solo per i servizi Win32, non per i driver.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_DETECT_PROCESS_ABORT"></span><span id="error_cannot_detect_process_abort"></span>**ERRORE \_ non è in grado di \_ rilevare l' \_ interruzione del processo \_**
</dt> <dd> <dl> <dt>

1081 (0x439)
</dt> <dt>



Questo servizio viene eseguito nello stesso processo di gestione controllo servizi. Pertanto, gestione controllo servizi non può intervenire se il processo del servizio viene terminato in modo imprevisto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RECOVERY_PROGRAM"></span><span id="error_no_recovery_program"></span>**ERRORE \_ nessun \_ programma di ripristino \_**
</dt> <dd> <dl> <dt>

1082 (0x43A)
</dt> <dt>



Nessun programma di ripristino configurato per questo servizio.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_IN_EXE"></span><span id="error_service_not_in_exe"></span>**\_servizio errori \_ non presente nel file \_ \_ exe**
</dt> <dd> <dl> <dt>

1083 (0x43B)
</dt> <dt>



Il programma eseguibile che questo servizio è configurato per l'esecuzione in non implementa il servizio.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAFEBOOT_SERVICE"></span><span id="error_not_safeboot_service"></span>**ERRORE \_ non è il \_ \_ servizio SafeBoot**
</dt> <dd> <dl> <dt>

1084 (0x43C)
</dt> <dt>



Impossibile avviare il servizio in modalità provvisoria.


</dt> </dl> </dd> <dt>

<span id="ERROR_END_OF_MEDIA"></span><span id="error_end_of_media"></span>**\_fine errore \_ del \_ supporto**
</dt> <dd> <dl> <dt>

1100 (0x44C)
</dt> <dt>



È stata raggiunta la fine fisica del nastro.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILEMARK_DETECTED"></span><span id="error_filemark_detected"></span>**\_rilevato errore FILEmark \_**
</dt> <dd> <dl> <dt>

1101 (0x44D)
</dt> <dt>



Un accesso al nastro ha raggiunto un oggetto filemark.


</dt> </dl> </dd> <dt>

<span id="ERROR_BEGINNING_OF_MEDIA"></span><span id="error_beginning_of_media"></span>**ERRORE \_ \_ di inizio del \_ supporto**
</dt> <dd> <dl> <dt>

1102 (0x44E)
</dt> <dt>



È stato rilevato l'inizio del nastro o di una partizione.


</dt> </dl> </dd> <dt>

<span id="ERROR_SETMARK_DETECTED"></span><span id="error_setmark_detected"></span>**\_indicatore di errore \_ rilevato**
</dt> <dd> <dl> <dt>

1103 (0x44F)
</dt> <dt>



Un accesso al nastro ha raggiunto la fine di un set di file.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_DATA_DETECTED"></span><span id="error_no_data_detected"></span>**ERRORE \_ nessun \_ dato \_ rilevato**
</dt> <dd> <dl> <dt>

1104 (0x450)
</dt> <dt>



Nessun altro dato sul nastro.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARTITION_FAILURE"></span><span id="error_partition_failure"></span>**errore \_ partizione \_ errore**
</dt> <dd> <dl> <dt>

1105 (0x451)
</dt> <dt>



Non è stato possibile partizionare il nastro.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_BLOCK_LENGTH"></span><span id="error_invalid_block_length"></span>**ERRORE \_ \_ Lunghezza blocco non valida \_**
</dt> <dd> <dl> <dt>

1106 (0x452)
</dt> <dt>



Quando si accede a un nuovo nastro di una partizione multivolume, le dimensioni correnti del blocco non sono corrette.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_PARTITIONED"></span><span id="error_device_not_partitioned"></span>**ERRORE \_ dispositivo \_ non \_ partizionato**
</dt> <dd> <dl> <dt>

1107 (0x453)
</dt> <dt>



Impossibile trovare le informazioni sulla partizione del nastro durante il caricamento di un nastro.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_LOCK_MEDIA"></span><span id="error_unable_to_lock_media"></span>**ERRORE \_ non è possibile \_ \_ bloccare i \_ supporti**
</dt> <dd> <dl> <dt>

1108 (0x454)
</dt> <dt>



Impossibile bloccare il meccanismo di espulsione dei supporti.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_UNLOAD_MEDIA"></span><span id="error_unable_to_unload_media"></span>**errore durante lo \_ \_ \_ scaricamento del \_ supporto**
</dt> <dd> <dl> <dt>

1109 (0x455)
</dt> <dt>



Impossibile scaricare il supporto.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_CHANGED"></span><span id="error_media_changed"></span>**\_supporto errori \_ modificato**
</dt> <dd> <dl> <dt>

1110 (0x456)
</dt> <dt>



È possibile che il supporto nell'unità sia stato modificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUS_RESET"></span><span id="error_bus_reset"></span>**reimpostazione del bus di errore \_ \_**
</dt> <dd> <dl> <dt>

1111 (0x457)
</dt> <dt>



Il bus di I/O è stato reimpostato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MEDIA_IN_DRIVE"></span><span id="error_no_media_in_drive"></span>**ERRORE \_ nessun \_ supporto \_ nell' \_ unità**
</dt> <dd> <dl> <dt>

1112 (0x458)
</dt> <dt>



Nessun supporto nell'unità.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_UNICODE_TRANSLATION"></span><span id="error_no_unicode_translation"></span>**ERRORE \_ Nessuna \_ \_ conversione Unicode**
</dt> <dd> <dl> <dt>

1113 (0x459)
</dt> <dt>



Non esiste alcun mapping per il carattere Unicode nella tabella codici multibyte di destinazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_INIT_FAILED"></span><span id="error_dll_init_failed"></span>**ERRORE \_ di \_ inizializzazione DLL \_ non riuscito**
</dt> <dd> <dl> <dt>

1114 (0x45A)
</dt> <dt>



Routine di inizializzazione DLL (Dynamic Link Library) non riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="error_shutdown_in_progress"></span>**ERRORE \_ \_ di arresto in \_ corso**
</dt> <dd> <dl> <dt>

1115 (0x45B)
</dt> <dt>



È in corso l'arresto del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SHUTDOWN_IN_PROGRESS"></span><span id="error_no_shutdown_in_progress"></span>**ERRORE \_ nessun \_ arresto \_ in \_ corso**
</dt> <dd> <dl> <dt>

1116 (0x45C)
</dt> <dt>



Impossibile interrompere l'arresto del sistema perché non è in corso l'arresto.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_DEVICE"></span><span id="error_io_device"></span>**ERRORE \_ io \_ dispositivo**
</dt> <dd> <dl> <dt>

1117 (0x45D)
</dt> <dt>



Impossibile eseguire la richiesta a causa di un errore del dispositivo di I/O.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERIAL_NO_DEVICE"></span><span id="error_serial_no_device"></span>**ERRORE \_ seriale \_ nessun \_ dispositivo**
</dt> <dd> <dl> <dt>

1118 (0x45E)
</dt> <dt>



Nessun dispositivo seriale inizializzato correttamente. Il driver seriale viene scaricato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IRQ_BUSY"></span><span id="error_irq_busy"></span>**ERRORE \_ IRQ \_ occupato**
</dt> <dd> <dl> <dt>

1119 (0x45F)
</dt> <dt>



Non è possibile aprire un dispositivo che condivide una richiesta di interrupt (IRQ) con altri dispositivi. Almeno un altro dispositivo che usa tale IRQ è già stato aperto.


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_WRITES"></span><span id="error_more_writes"></span>**\_ulteriori \_ SCRITTURe errore**
</dt> <dd> <dl> <dt>

1120 (0x460)
</dt> <dt>



Un'operazione di I/O seriale è stata completata da un'altra scrittura sulla porta seriale. Il \_ contatore XOFF seriale IOCTL ha \_ raggiunto lo \_ zero.


</dt> </dl> </dd> <dt>

<span id="ERROR_COUNTER_TIMEOUT"></span><span id="error_counter_timeout"></span>**\_timeout contatore \_ errori**
</dt> <dd> <dl> <dt>

1121 (0x461)
</dt> <dt>



Un'operazione di I/O seriale è stata completata perché il periodo di timeout è scaduto. Il \_ \_ contatore XOFF seriale IOCTL \_ non ha raggiunto lo zero.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_ID_MARK_NOT_FOUND"></span><span id="error_floppy_id_mark_not_found"></span>**\_ \_ contrassegno ID floppy \_ errore \_ non \_ trovato**
</dt> <dd> <dl> <dt>

1122 (0x462)
</dt> <dt>



Non è stato trovato alcun contrassegno di indirizzo ID nel disco floppy.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_WRONG_CYLINDER"></span><span id="error_floppy_wrong_cylinder"></span>**ERRORE \_ del \_ cilindro floppy errato \_**
</dt> <dd> <dl> <dt>

1123 (0x463)
</dt> <dt>



Mancata corrispondenza tra il campo ID settore disco floppy e l'indirizzo di rilevamento del controller del disco floppy.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_UNKNOWN_ERROR"></span><span id="error_floppy_unknown_error"></span>**errore \_ sconosciuto del floppy di errore \_ \_**
</dt> <dd> <dl> <dt>

1124 (0x464)
</dt> <dt>



Il controller del disco floppy ha segnalato un errore non riconosciuto dal driver del disco floppy.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_BAD_REGISTERS"></span><span id="error_floppy_bad_registers"></span>**\_registro errori floppy \_ errato \_**
</dt> <dd> <dl> <dt>

1125 (0x465)
</dt> <dt>



Il controller del disco floppy ha restituito risultati incoerenti nei propri registri.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RECALIBRATE_FAILED"></span><span id="error_disk_recalibrate_failed"></span>**\_RIcalibrazione disco errore \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

1126 (0x466)
</dt> <dt>



Durante l'accesso al disco rigido, un'operazione di ricalibrazione non è riuscita, anche dopo i tentativi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_OPERATION_FAILED"></span><span id="error_disk_operation_failed"></span>**\_operazione disco \_ errore \_ non riuscita**
</dt> <dd> <dl> <dt>

1127 (0x467)
</dt> <dt>



Durante l'accesso al disco rigido, un'operazione su disco non è riuscita anche dopo i tentativi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RESET_FAILED"></span><span id="error_disk_reset_failed"></span>**ERRORE \_ di \_ reimpostazione del disco \_**
</dt> <dd> <dl> <dt>

1128 (0x468)
</dt> <dt>



Durante l'accesso al disco rigido, era necessaria una reimpostazione del controller del disco, ma anche tale operazione non è riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_EOM_OVERFLOW"></span><span id="error_eom_overflow"></span>**ERRORE \_ di \_ overflow EOM**
</dt> <dd> <dl> <dt>

1129 (0x469)
</dt> <dt>



Fine fisica del nastro rilevata.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_SERVER_MEMORY"></span><span id="error_not_enough_server_memory"></span>**ERRORE \_ \_ memoria del \_ server insufficiente \_**
</dt> <dd> <dl> <dt>

1130 (0x46A)
</dt> <dt>



Memoria insufficiente nel server per eseguire il comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_POSSIBLE_DEADLOCK"></span><span id="error_possible_deadlock"></span>**ERRORE \_ possibile \_ deadlock**
</dt> <dd> <dl> <dt>

1131 (0x46B)
</dt> <dt>



È stata rilevata una potenziale condizione di deadlock.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAPPED_ALIGNMENT"></span><span id="error_mapped_alignment"></span>**\_allineamento con mapping degli errori \_**
</dt> <dd> <dl> <dt>

1132 (0x46C)
</dt> <dt>



L'indirizzo di base o l'offset del file specificato non dispone dell'allineamento appropriato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_POWER_STATE_VETOED"></span><span id="error_set_power_state_vetoed"></span>**errore durante il \_ reimpostazione \_ \_ dello stato di alimentazione \_**
</dt> <dd> <dl> <dt>

1140 (0x474)
</dt> <dt>



Il tentativo di modificare lo stato di alimentazione del sistema è stato bloccato da un'altra applicazione o da un altro driver.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_POWER_STATE_FAILED"></span><span id="error_set_power_state_failed"></span>**errore durante l' \_ impostazione \_ \_ dello stato di alimentazione \_ non riuscito**
</dt> <dd> <dl> <dt>

1141 (0x475)
</dt> <dt>



Il BIOS di sistema non è riuscito a modificare lo stato di alimentazione del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_LINKS"></span><span id="error_too_many_links"></span>**ERRORE di un \_ numero eccessivo di \_ \_ collegamenti**
</dt> <dd> <dl> <dt>

1142 (0x476)
</dt> <dt>



È stato effettuato un tentativo di creare altri collegamenti in un file rispetto al file system supportato da.


</dt> </dl> </dd> <dt>

<span id="ERROR_OLD_WIN_VERSION"></span><span id="error_old_win_version"></span>**ERRORE \_ versione precedente di \_ Win \_**
</dt> <dd> <dl> <dt>

1150 (0x47E)
</dt> <dt>



Il programma specificato richiede una versione più recente di Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_WRONG_OS"></span><span id="error_app_wrong_os"></span>**ERRORE \_ del \_ \_ sistema operativo app errato**
</dt> <dd> <dl> <dt>

1151 (0x47F)
</dt> <dt>



Il programma specificato non è un programma Windows o MS-DOS.


</dt> </dl> </dd> <dt>

<span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**ERRORE \_ \_ app a istanza singola \_**
</dt> <dd> <dl> <dt>

1152 (0x480)
</dt> <dt>



Impossibile avviare più di un'istanza del programma specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**ERRORE \_ \_ app RMODE**
</dt> <dd> <dl> <dt>

1153 (0x481)
</dt> <dt>



Il programma specificato è stato scritto per una versione precedente di Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**ERRORE \_ di \_ dll non valida**
</dt> <dd> <dl> <dt>

1154 (0x482)
</dt> <dt>



Uno dei file di libreria necessari per eseguire l'applicazione è danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**ERRORE \_ Nessuna \_ associazione**
</dt> <dd> <dl> <dt>

1155 (0x483)
</dt> <dt>



Nessuna applicazione associata al file specificato per questa operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**ERRORE \_ DDE \_ non riuscita**
</dt> <dd> <dl> <dt>

1156 (0x484)
</dt> <dt>



Si è verificato un errore durante l'invio del comando all'applicazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**DLL di errore \_ \_ non \_ trovata**
</dt> <dd> <dl> <dt>

1157 (0x485)
</dt> <dt>



Impossibile trovare uno dei file di libreria necessari per eseguire l'applicazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**ERRORE \_ di \_ altri \_ \_ handle utente**
</dt> <dd> <dl> <dt>

1158 (0x486)
</dt> <dt>



Il processo corrente ha utilizzato tutta la relativa tolleranza di sistema degli handle per gli oggetti di Window Manager.


</dt> </dl> </dd> <dt>

<span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**\_ \_ solo sincronizzazione messaggi di errore \_**
</dt> <dd> <dl> <dt>

1159 (0x487)
</dt> <dt>



Il messaggio può essere utilizzato solo con le operazioni sincrone.


</dt> </dl> </dd> <dt>

<span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**\_elemento di origine errore \_ \_ vuoto**
</dt> <dd> <dl> <dt>

1160 (0x488)
</dt> <dt>



L'elemento di origine indicato non contiene supporti.


</dt> </dl> </dd> <dt>

<span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**ERRORE \_ \_ elemento destinazione \_ completo**
</dt> <dd> <dl> <dt>

1161 (0x489)
</dt> <dt>



L'elemento di destinazione indicato contiene già un supporto.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**ERRORE \_ di \_ Indirizzo elemento non valido \_**
</dt> <dd> <dl> <dt>

1162 (0x48A)
</dt> <dt>



L'elemento indicato non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**rivista di errore \_ \_ non \_ presente**
</dt> <dd> <dl> <dt>

1163 (0x48B)
</dt> <dt>



L'elemento indicato fa parte di una rivista che non è presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**ERRORE \_ di \_ reinizializzazione del dispositivo \_ necessario**
</dt> <dd> <dl> <dt>

1164 (0x48C)
</dt> <dt>



Il dispositivo indicato richiede la reinizializzazione a causa di errori hardware.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**il \_ dispositivo di errore \_ richiede la \_ pulizia**
</dt> <dd> <dl> <dt>

1165 (0x48D)
</dt> <dt>



Il dispositivo ha indicato che è necessaria la pulizia prima di eseguire altre operazioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**ERRORE \_ \_ sportello dispositivo \_ aperto**
</dt> <dd> <dl> <dt>

1166 (0x48E)
</dt> <dt>



Il dispositivo ha indicato che lo sportello è aperto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**ERRORE \_ dispositivo \_ non \_ connesso**
</dt> <dd> <dl> <dt>

1167 (0x48F)
</dt> <dt>



Il dispositivo non è connesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**ERRORE \_ non \_ trovato**
</dt> <dd> <dl> <dt>

1168 (0x490)
</dt> <dt>



Element not found.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**ERRORE \_ Nessuna \_ corrispondenza**
</dt> <dd> <dl> <dt>

1169 (0x491)
</dt> <dt>



Non è stata trovata alcuna corrispondenza per la chiave specificata nell'indice.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**\_ \_ Impossibile trovare il set di errori \_**
</dt> <dd> <dl> <dt>

1170 (0x492)
</dt> <dt>



Il set di proprietà specificato non esiste nell'oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**il punto di errore non è stato \_ \_ \_ trovato**
</dt> <dd> <dl> <dt>

1171 (0x493)
</dt> <dt>



Il punto passato a GetMouseMovePoints non è presente nel buffer.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**ERRORE \_ nessun \_ servizio di rilevamento \_**
</dt> <dd> <dl> <dt>

1172 (0x494)
</dt> <dt>



Il servizio di rilevamento (workstation) non è in esecuzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**ERRORE \_ nessun \_ \_ ID volume**
</dt> <dd> <dl> <dt>

1173 (0x495)
</dt> <dt>



Impossibile trovare l'ID volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**ERRORE \_ non è possibile \_ \_ rimuovere \_ sostituito**
</dt> <dd> <dl> <dt>

1175 (0x497)
</dt> <dt>



Impossibile rimuovere il file da sostituire.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**ERRORE \_ non è possibile \_ \_ spostare la \_ sostituzione**
</dt> <dd> <dl> <dt>

1176 (0x498)
</dt> <dt>



Impossibile spostare il file di sostituzione nel file da sostituire. Il file da sostituire ha mantenuto il nome originale.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**ERRORE \_ non è possibile \_ \_ spostare la \_ sostituzione \_ 2**
</dt> <dd> <dl> <dt>

1177 (0x499)
</dt> <dt>



Impossibile spostare il file di sostituzione nel file da sostituire. Il file da sostituire è stato rinominato usando il nome del backup.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**\_eliminazione Journal degli errori \_ \_ in \_ corso**
</dt> <dd> <dl> <dt>

1178 (0x49A)
</dt> <dt>



È in corso l'eliminazione del journal delle modifiche del volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**Journal degli errori \_ \_ non \_ attivo**
</dt> <dd> <dl> <dt>

1179 (0x49B)
</dt> <dt>



Il Journal delle modifiche del volume non è attivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**ERRORE \_ possibile \_ file \_ trovato**
</dt> <dd> <dl> <dt>

1180 (0x49C)
</dt> <dt>



È stato trovato un file, ma potrebbe non essere il file corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**\_voce journal degli errori \_ \_ eliminata**
</dt> <dd> <dl> <dt>

1181 (0x49D)
</dt> <dt>



La voce del journal è stata eliminata dal Journal.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**ERRORE \_ di \_ arresto \_ pianificato**
</dt> <dd> <dl> <dt>

1190 (0x4A6)
</dt> <dt>



Un arresto del sistema è già stato pianificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**ERRORE \_ \_ di arresto degli utenti \_ connessi \_**
</dt> <dd> <dl> <dt>

1191 (0x4A7)
</dt> <dt>



Impossibile avviare l'arresto del sistema perché sono presenti altri utenti connessi al computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**ERRORE \_ \_ dispositivo errato**
</dt> <dd> <dl> <dt>

1200 (0x4B0)
</dt> <dt>



Il nome del dispositivo specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**ERRORE di \_ connessione non \_ disponibile**
</dt> <dd> <dl> <dt>

1201 (0x4B1)
</dt> <dt>



Il dispositivo non è attualmente connesso, ma è una connessione memorizzata.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**dispositivo con errori \_ \_ già \_ memorizzato**
</dt> <dd> <dl> <dt>

1202 (0x4B2)
</dt> <dt>



Il nome del dispositivo locale ha una connessione memorizzata a un'altra risorsa di rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**ERRORE \_ nessun \_ \_ percorso NET o \_ errato \_**
</dt> <dd> <dl> <dt>

1203 (0x4B3)
</dt> <dt>



Il percorso di rete non è stato tipizzato correttamente, non esiste oppure il provider di rete non è attualmente disponibile. Provare a ridigitare il percorso o a contattare l'amministratore di rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**ERRORE \_ del \_ provider errato**
</dt> <dd> <dl> <dt>

1204 (0x4B4)
</dt> <dt>



Il nome del provider di rete specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**ERRORE \_ non è possibile \_ aprire \_ il profilo**
</dt> <dd> <dl> <dt>

1205 (0x4B5)
</dt> <dt>



Non è possibile aprire il profilo di connessione di rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**ERRORE \_ \_ profilo errato**
</dt> <dd> <dl> <dt>

1206 (0x4B6)
</dt> <dt>



Il profilo di connessione di rete è danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**ERRORE \_ non \_ contenitore**
</dt> <dd> <dl> <dt>

1207 (0x4B7)
</dt> <dt>



Impossibile enumerare un non contenitore.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**errore \_ esteso \_ errore**
</dt> <dd> <dl> <dt>

1208 (0x4B8)
</dt> <dt>



Si è verificato un errore esteso.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**ERRORE \_ \_ GroupName non valido**
</dt> <dd> <dl> <dt>

1209 (0x4B9)
</dt> <dt>



Il formato del nome del gruppo specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**ERRORE \_ nomecomputer non valido \_**
</dt> <dd> <dl> <dt>

1210 (0x4BA)
</dt> <dt>



Il formato del nome computer specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**ERRORE \_ \_ EventName non valido**
</dt> <dd> <dl> <dt>

1211 (0x4BB)
</dt> <dt>



Il formato del nome di evento specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**ERRORE \_ \_ DomainName non valido**
</dt> <dd> <dl> <dt>

1212 (0x4BC)
</dt> <dt>



Il formato del nome di dominio specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**ERRORE \_ \_ ServiceName non valido**
</dt> <dd> <dl> <dt>

1213 (0x4BD)
</dt> <dt>



Il formato del nome del servizio specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**ERRORE \_ NETNAME non valido \_**
</dt> <dd> <dl> <dt>

1214 (0x4BE)
</dt> <dt>



Il formato del nome di rete specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**ERRORE \_ condivisione non valida \_**
</dt> <dd> <dl> <dt>

1215 (0x4BF)
</dt> <dt>



Il formato del nome di condivisione specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**ERRORE \_ \_ passwordname non valida**
</dt> <dd> <dl> <dt>

1216 (0x4C0)
</dt> <dt>



Il formato della password specificata non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**ERRORE \_ \_ MessageName non valido**
</dt> <dd> <dl> <dt>

1217 (0x4C1)
</dt> <dt>



Il formato del nome del messaggio specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**ERRORE \_ MESSAGEDEST non valido \_**
</dt> <dd> <dl> <dt>

1218 (0x4C2)
</dt> <dt>



Il formato della destinazione del messaggio specificata non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**\_conflitto di \_ credenziali della sessione di errore \_**
</dt> <dd> <dl> <dt>

1219 (0x4C3)
</dt> <dt>



Non sono consentite più connessioni a un server o a una risorsa condivisa dallo stesso utente, usando più di un nome utente. Disconnettere tutte le connessioni precedenti al server o alla risorsa condivisa e riprovare.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**\_ \_ \_ superato limite sessione remota \_ errore**
</dt> <dd> <dl> <dt>

1220 (0x4C4)
</dt> <dt>



È stato effettuato un tentativo di stabilire una sessione in un server di rete, ma sono già state stabilite troppe sessioni per tale server.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**ERRORE \_ DUP \_ NomeDominio**
</dt> <dd> <dl> <dt>

1221 (0x4C5)
</dt> <dt>



Il gruppo di lavoro o il nome di dominio è già in uso da un altro computer della rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**ERRORE \_ Nessuna \_ rete**
</dt> <dd> <dl> <dt>

1222 (0x4C6)
</dt> <dt>



La rete non è presente o non è stata avviata.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**ERRORE \_ annullato**
</dt> <dd> <dl> <dt>

1223 (0x4C7)
</dt> <dt>



L'operazione è stata annullata dall'utente.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**\_file con \_ mapping \_ utente errore**
</dt> <dd> <dl> <dt>

1224 (0x4C8)
</dt> <dt>



Impossibile eseguire l'operazione richiesta su un file con una sezione mappata all'utente aperta.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**\_connessione errore \_ rifiutata**
</dt> <dd> <dl> <dt>

1225 (0x4C9)
</dt> <dt>



Il computer remoto ha rifiutato la connessione di rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**ERRORE \_ di \_ disconnessione normale**
</dt> <dd> <dl> <dt>

1226 (0x4CA)
</dt> <dt>



La connessione di rete è stata chiusa correttamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**\_indirizzo errore \_ già \_ associato**
</dt> <dd> <dl> <dt>

1227 (0x4CB)
</dt> <dt>



All'endpoint di trasporto di rete è già associato un indirizzo.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**\_indirizzo errore \_ non \_ associato**
</dt> <dd> <dl> <dt>

1228 (0x4CC)
</dt> <dt>



Un indirizzo non è ancora stato associato all'endpoint di rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**ERRORE di \_ connessione \_ non valido**
</dt> <dd> <dl> <dt>

1229 (0x4CD)
</dt> <dt>



Si è tentato di eseguire un'operazione su una connessione di rete inesistente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**ERRORE di \_ connessione \_ attivo**
</dt> <dd> <dl> <dt>

1230 (0x4CE)
</dt> <dt>



Si è tentato di eseguire un'operazione non valida su una connessione di rete attiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**ERRORE di \_ rete \_ irraggiungibile**
</dt> <dd> <dl> <dt>

1231 (0x4CF)
</dt> <dt>



Impossibile raggiungere il percorso di rete. Per informazioni sulla risoluzione dei problemi di rete, vedere la Guida di Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**ERRORE \_ host non \_ raggiungibile**
</dt> <dd> <dl> <dt>

1232 (0x4D0)
</dt> <dt>



Impossibile raggiungere il percorso di rete. Per informazioni sulla risoluzione dei problemi di rete, vedere la Guida di Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**protocollo di errore \_ \_ irraggiungibile**
</dt> <dd> <dl> <dt>

1233 (0x4D1)
</dt> <dt>



Impossibile raggiungere il percorso di rete. Per informazioni sulla risoluzione dei problemi di rete, vedere la Guida di Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_UNREACHABLE"></span><span id="error_port_unreachable"></span>**porta di errore \_ \_ irraggiungibile**
</dt> <dd> <dl> <dt>

1234 (0x4D2)
</dt> <dt>



Nessun servizio sta operando sull'endpoint di rete di destinazione nel sistema remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_ABORTED"></span><span id="error_request_aborted"></span>**richiesta di errore \_ \_ interrotta**
</dt> <dd> <dl> <dt>

1235 (0x4D3)
</dt> <dt>



La richiesta è stata interrotta.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_ABORTED"></span><span id="error_connection_aborted"></span>**ERRORE di \_ connessione \_ interrotto**
</dt> <dd> <dl> <dt>

1236 (0x4D4)
</dt> <dt>



La connessione di rete è stata interrotta dal sistema locale.


</dt> </dl> </dd> <dt>

<span id="ERROR_RETRY"></span><span id="error_retry"></span>**tentativo di errore \_**
</dt> <dd> <dl> <dt>

1237 (0x4D5)
</dt> <dt>



Impossibile completare l'operazione. È necessario eseguire un nuovo tentativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_COUNT_LIMIT"></span><span id="error_connection_count_limit"></span>**\_ \_ limite numero connessioni \_ errore**
</dt> <dd> <dl> <dt>

1238 (0x4D6)
</dt> <dt>



Non è stato possibile stabilire una connessione al server perché è stato raggiunto il limite per il numero di connessioni simultanee per l'account.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGIN_TIME_RESTRICTION"></span><span id="error_login_time_restriction"></span>**\_ \_ limitazione tempo di accesso errore \_**
</dt> <dd> <dl> <dt>

1239 (0x4D7)
</dt> <dt>



Tentativo di accesso durante un'ora del giorno non autorizzata per l'account.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGIN_WKSTA_RESTRICTION"></span><span id="error_login_wksta_restriction"></span>**\_ \_ restrizione WKSTA login errore \_**
</dt> <dd> <dl> <dt>

1240 (0x4D8)
</dt> <dt>



L'account non è autorizzato ad accedere da questa stazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_ADDRESS"></span><span id="error_incorrect_address"></span>**ERRORE \_ di \_ indirizzo errato**
</dt> <dd> <dl> <dt>

1241 (0x4D9)
</dt> <dt>



Impossibile utilizzare l'indirizzo di rete per l'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_REGISTERED"></span><span id="error_already_registered"></span>**ERRORE \_ già \_ registrato**
</dt> <dd> <dl> <dt>

1242 (0x4DA)
</dt> <dt>



Il servizio è già registrato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_FOUND"></span><span id="error_service_not_found"></span>**\_ \_ Impossibile trovare il servizio di errore \_**
</dt> <dd> <dl> <dt>

1243 (0x4DB)
</dt> <dt>



Il servizio specificato non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_AUTHENTICATED"></span><span id="error_not_authenticated"></span>**ERRORE \_ non \_ autenticato**
</dt> <dd> <dl> <dt>

1244 (0x4DC)
</dt> <dt>



L'operazione richiesta non è stata eseguita perché l'utente non è stato autenticato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOGGED_ON"></span><span id="error_not_logged_on"></span>**ERRORE \_ non \_ connesso \_**
</dt> <dd> <dl> <dt>

1245 (0x4DD)
</dt> <dt>



L'operazione richiesta non è stata eseguita perché l'utente non ha eseguito l'accesso alla rete. Il servizio specificato non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTINUE"></span><span id="error_continue"></span>**ERRORE \_ continuo**
</dt> <dd> <dl> <dt>

1246 (0x4DE)
</dt> <dt>



Continuare con il lavoro in corso.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_INITIALIZED"></span><span id="error_already_initialized"></span>**ERRORE \_ già \_ inizializzato**
</dt> <dd> <dl> <dt>

1247 (0x4DF)
</dt> <dt>



È stato effettuato un tentativo di eseguire un'operazione di inizializzazione quando l'inizializzazione è già stata completata.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_DEVICES"></span><span id="error_no_more_devices"></span>**ERRORE \_ nessun \_ altro \_ dispositivo**
</dt> <dd> <dl> <dt>

1248 (0x4E0)
</dt> <dt>



Non sono più presenti dispositivi locali.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_SITE"></span><span id="error_no_such_site"></span>**ERRORE \_ nessun \_ sito di questo tipo \_**
</dt> <dd> <dl> <dt>

1249 (0x4E1)
</dt> <dt>



Il sito specificato non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CONTROLLER_EXISTS"></span><span id="error_domain_controller_exists"></span>**il \_ controller di dominio dell'errore \_ \_ esiste**
</dt> <dd> <dl> <dt>

1250 (0x4E2)
</dt> <dt>



Un controller di dominio con il nome specificato esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_ONLY_IF_CONNECTED"></span><span id="error_only_if_connected"></span>**ERRORE \_ solo \_ se \_ connesso**
</dt> <dd> <dl> <dt>

1251 (0x4E3)
</dt> <dt>



Questa operazione è supportata solo quando si è connessi al server.


</dt> </dl> </dd> <dt>

<span id="ERROR_OVERRIDE_NOCHANGES"></span><span id="error_override_nochanges"></span>**ERRORE \_ override \_ NoChanges**
</dt> <dd> <dl> <dt>

1252 (0x4E4)
</dt> <dt>



Il Framework di criteri di gruppo deve chiamare l'estensione anche se non sono state apportate modifiche.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_USER_PROFILE"></span><span id="error_bad_user_profile"></span>**ERRORE \_ nel \_ profilo utente errato \_**
</dt> <dd> <dl> <dt>

1253 (0x4E5)
</dt> <dt>



Il profilo dell'utente specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_ON_SBS"></span><span id="error_not_supported_on_sbs"></span>**ERRORE \_ non \_ supportato \_ in \_ SBS**
</dt> <dd> <dl> <dt>

1254 (0x4E6)
</dt> <dt>



Questa operazione non è supportata in un computer che esegue Windows Server 2003 per Small Business Server.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_SHUTDOWN_IN_PROGRESS"></span><span id="error_server_shutdown_in_progress"></span>**\_ \_ arresto del server \_ di errore in \_ corso**
</dt> <dd> <dl> <dt>

1255 (0x4E7)
</dt> <dt>



Il computer server si sta arrestando.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_DOWN"></span><span id="error_host_down"></span>**ERRORE \_ host \_ inattivo**
</dt> <dd> <dl> <dt>

1256 (0x4E8)
</dt> <dt>



Il sistema remoto non è disponibile. Per informazioni sulla risoluzione dei problemi di rete, vedere la Guida di Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_ACCOUNT_SID"></span><span id="error_non_account_sid"></span>**\_SID errore non \_ account \_**
</dt> <dd> <dl> <dt>

1257 (0x4E9)
</dt> <dt>



L'identificatore di sicurezza specificato non si trova in un dominio dell'account.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_DOMAIN_SID"></span><span id="error_non_domain_sid"></span>**ERRORE \_ non \_ dominio \_ SID**
</dt> <dd> <dl> <dt>

1258 (0x4EA)
</dt> <dt>



L'identificatore di sicurezza fornito non dispone di un componente di dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_APPHELP_BLOCK"></span><span id="error_apphelp_block"></span>**ERRORE \_ APPHELP \_ blocco**
</dt> <dd> <dl> <dt>

1259 (0x4EB)
</dt> <dt>



La finestra di dialogo AppHelp è stata annullata impedendo l'avvio dell'applicazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_BY_POLICY"></span><span id="error_access_disabled_by_policy"></span>**\_accesso agli errori \_ disabilitato \_ dal \_ criterio**
</dt> <dd> <dl> <dt>

1260 (0x4EC)
</dt> <dt>



Questo programma è bloccato da criteri di gruppo. Per ulteriori informazioni, contattare l'amministratore di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_REG_NAT_CONSUMPTION"></span><span id="error_reg_nat_consumption"></span>**ERRORE \_ reg \_ \_ consumo NAT**
</dt> <dd> <dl> <dt>

1261 (0x4ED)
</dt> <dt>



Un programma tenta di utilizzare un valore di registro non valido. Normalmente causato da un registro non inizializzato. Questo errore è specifico di Itanium.


</dt> </dl> </dd> <dt>

<span id="ERROR_CSCSHARE_OFFLINE"></span><span id="error_cscshare_offline"></span>**ERRORE \_ CSCSHARE \_ offline**
</dt> <dd> <dl> <dt>

1262 (0x4EE)
</dt> <dt>



La condivisione è attualmente offline o non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_PKINIT_FAILURE"></span><span id="error_pkinit_failure"></span>**ERRORE \_ PKINIT non \_ riuscito**
</dt> <dd> <dl> <dt>

1263 (0x4EF)
</dt> <dt>



Il protocollo Kerberos ha rilevato un errore durante la convalida del certificato KDC durante l'accesso alla smart card. Sono disponibili ulteriori informazioni nel registro eventi di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SMARTCARD_SUBSYSTEM_FAILURE"></span><span id="error_smartcard_subsystem_failure"></span>**errore \_ del \_ sottosistema Smart Card errore \_**
</dt> <dd> <dl> <dt>

1264 (0x4F0)
</dt> <dt>



Il protocollo Kerberos ha rilevato un errore durante il tentativo di utilizzare il sottosistema smart card.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**il downgrade dell'errore è stato \_ \_ rilevato**
</dt> <dd> <dl> <dt>

1265 (0x4F1)
</dt> <dt>



Il sistema non è in grado di contattare un controller di dominio per il servizio della richiesta di autenticazione. Riprova più tardi.


</dt> </dl> </dd> <dt>

<span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**computer con errori \_ \_ bloccato**
</dt> <dd> <dl> <dt>

1271 (0x4F7)
</dt> <dt>



Il computer è bloccato e non può essere arrestato senza l'opzione Force.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**CALLBACK di errore \_ \_ fornito \_ dati non validi \_**
</dt> <dd> <dl> <dt>

1273 (0x4F9)
</dt> <dt>



Un callback definito dall'applicazione ha dato dati non validi quando viene chiamato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**\_aggiornamento in \_ primo piano della sincronizzazione errori \_ \_ obbligatorio**
</dt> <dd> <dl> <dt>

1274 (0x4FA)
</dt> <dt>



Il Framework di criteri di gruppo deve chiamare l'estensione nell'aggiornamento dei criteri di primo piano sincrono.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**DRIVER di errore \_ \_ bloccato**
</dt> <dd> <dl> <dt>

1275 (0x4FB)
</dt> <dt>



Il caricamento del driver è stato bloccato.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**errore durante l' \_ \_ importazione \_ di \_ non \_ dll**
</dt> <dd> <dl> <dt>

1276 (0x4FC)
</dt> <dt>



Una libreria a collegamento dinamico (DLL) fa riferimento a un modulo che non è né una DLL né l'immagine eseguibile del processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**ERRORE di \_ accesso al pannello \_ \_ WebBlade disabilitato**
</dt> <dd> <dl> <dt>

1277 (0x4FD)
</dt> <dt>



Windows non è in grado di aprire il programma perché è stato disabilitato.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**ERRORE di \_ accesso al \_ \_ WebBlade disabilitato per l'accesso \_**
</dt> <dd> <dl> <dt>

1278 (0x4FE)
</dt> <dt>



Windows non è in grado di aprire il programma perché il sistema di imposizione delle licenze è stato manomesso o danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**ERRORE di \_ ripristino \_**
</dt> <dd> <dl> <dt>

1279 (0x4FF)
</dt> <dt>



Ripristino transazione non riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**ERRORE \_ già \_ Fiber**
</dt> <dd> <dl> <dt>

1280 (0x500)
</dt> <dt>



Il thread corrente è già stato convertito in Fiber.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**ERRORE \_ già \_ thread**
</dt> <dd> <dl> <dt>

1281 (0x501)
</dt> <dt>



Il thread corrente è già stato convertito da Fiber.


</dt> </dl> </dd> <dt>

<span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**\_sovraccarico buffer dello stack di errori \_ \_**
</dt> <dd> <dl> <dt>

1282 (0x502)
</dt> <dt>



Il sistema ha rilevato un sovraccarico di un buffer basato su stack in questa applicazione. Questo sovraccarico potrebbe potenzialmente consentire a un utente malintenzionato di ottenere il controllo di questa applicazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**QUOTA del parametro di errore \_ \_ \_ superata**
</dt> <dd> <dl> <dt>

1283 (0x503)
</dt> <dt>



I dati presenti in uno dei parametri sono maggiori di quelli che la funzione può utilizzare.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**\_debugger errori \_ inattivo**
</dt> <dd> <dl> <dt>

1284 (0x504)
</dt> <dt>



Il tentativo di eseguire un'operazione su un oggetto di debug non è riuscito perché è in corso l'eliminazione dell'oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**ERRORE \_ di \_ caricamento ritardato \_**
</dt> <dd> <dl> <dt>

1285 (0x505)
</dt> <dt>



Tentativo di ritardare il caricamento di un file con estensione dll o di ottenere un indirizzo di funzione in un file con estensione dll a caricamento ritardato non riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**ERRORE \_ VDM non \_ consentito**
</dt> <dd> <dl> <dt>

1286 (0x506)
</dt> <dt>



%1 è un'applicazione a 16 bit. Non si dispone delle autorizzazioni per l'esecuzione di applicazioni a 16 bit. Verificare le autorizzazioni con l'amministratore di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**errore non \_ identificato \_**
</dt> <dd> <dl> <dt>

1287 (0x507)
</dt> <dt>



Informazioni insufficienti per identificare la cause dell'errore.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**ERRORE \_ \_ parametro CRUNTIME non valido \_**
</dt> <dd> <dl> <dt>

1288 (0x508)
</dt> <dt>



Il parametro passato a una funzione di runtime C non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**ERRORE \_ oltre \_ VDL**
</dt> <dd> <dl> <dt>

1289 (0x509)
</dt> <dt>



L'operazione si è verificata oltre la lunghezza dei dati valida del file.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**ERRORE \_ tipo di \_ SID del servizio non compatibile \_ \_**
</dt> <dd> <dl> <dt>

1290 (0x50A)
</dt> <dt>



L'avvio del servizio non è riuscito perché uno o più servizi nello stesso processo hanno un'impostazione del tipo di SID del servizio incompatibile. Un servizio con tipo di SID servizio con restrizioni può coesistere solo nello stesso processo con altri servizi con un tipo di SID con restrizioni. Se il tipo di SID del servizio è stato appena configurato, è necessario riavviare il processo di hosting per poter avviare il servizio.

In Windows Server 2003 e Windows XP un servizio senza restrizioni non può coesistere nello stesso processo con altri servizi. Il servizio con il tipo di SID servizio senza restrizioni deve essere spostato in un processo di proprietà per poter avviare il servizio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**processo del driver di errore \_ \_ \_ terminato**
</dt> <dd> <dl> <dt>

1291 (0x50B)
</dt> <dt>



Il processo che ospita il driver per questo dispositivo è stato terminato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**\_limite di implementazione degli errori \_**
</dt> <dd> <dl> <dt>

1292 (0x50C)
</dt> <dt>



Un'operazione ha tentato di superare un limite definito dall'implementazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**il \_ processo di errore \_ è \_ protetto**
</dt> <dd> <dl> <dt>

1293 (0x50D)
</dt> <dt>



Il processo di destinazione o il processo contenitore del thread di destinazione è un processo protetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**notifica del servizio di errore \_ \_ \_ ritardo del client \_**
</dt> <dd> <dl> <dt>

1294 (0x50E)
</dt> <dt>



Il client di notifica del servizio è troppo indietro per lo stato corrente dei servizi nel computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**\_quota disco di errore \_ \_ superata**
</dt> <dd> <dl> <dt>

1295 (0x50F)
</dt> <dt>



L'operazione di file richiesta non è riuscita perché è stata superata la quota di archiviazione. Per liberare spazio su disco, spostare i file in un percorso diverso o eliminare i file non necessari. Per ulteriori informazioni, contattare l'amministratore di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**\_contenuto errore \_ bloccato**
</dt> <dd> <dl> <dt>

1296 (0x510)
</dt> <dt>



L'operazione di file richiesta non è riuscita perché i criteri di archiviazione bloccano il tipo di file. Per ulteriori informazioni, contattare l'amministratore di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**ERRORE di \_ servizio INcompatibile \_ \_**
</dt> <dd> <dl> <dt>

1297 (0x511)
</dt> <dt>



Un privilegio richiesto dal servizio per il corretto funzionamento non esiste nella configurazione dell'account del servizio. È possibile utilizzare lo snap-in servizi di Microsoft Management Console (MMC) (Services. msc) e lo snap-in MMC Impostazioni di sicurezza locali (secpol. msc) per visualizzare la configurazione del servizio e la configurazione dell'account.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**ERRORE \_ \_ blocco app**
</dt> <dd> <dl> <dt>

1298 (0x512)
</dt> <dt>



Un thread incluso in questa operazione sembra non rispondere.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**\_etichetta errore non valida \_**
</dt> <dd> <dl> <dt>

1299 (0x513)
</dt> <dt>



Indica che un determinato ID di sicurezza non può essere assegnato come etichetta di un oggetto.


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

 

 




