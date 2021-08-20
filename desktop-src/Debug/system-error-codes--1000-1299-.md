---
description: Descrive i codici di errore 1000-1299 definiti nel file di intestazione WinError.h ed è destinato agli sviluppatori.
ms.assetid: 0061feb6-e1a0-4fcd-8f80-954087c799d7
title: Codici di errore di sistema (1000-1299) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: dfda2e29a6b75acd683842509229f3bc52d7e8d3599855b01d8376f5a7daf2ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076335"
---
# <a name="system-error-codes-1000-1299"></a>Codici di errore di sistema (1000-1299)

> [!NOTE]
> Queste informazioni sono destinate agli sviluppatori che ese tracciano errori di sistema. Per altri errori, ad esempio problemi con Windows Update, è disponibile un elenco di risorse nella [pagina Codici di](system-error-codes.md) errore.

Nell'elenco seguente vengono descritti [i codici di errore di](system-error-codes.md) sistema per gli errori da 1000 a 1299. Vengono restituiti dalla funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo. Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la [**funzione FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il flag **FORMAT MESSAGE FROM \_ \_ \_ SYSTEM.**

<dl> <dt>

<span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**OVERFLOW \_ DELLO STACK DI \_ ERRORI**
</dt> <dd> <dl> <dt>

1001 (0x3E9)
</dt> <dt>



Ricorsione troppo profonda; overflow dello stack.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**MESSAGGIO \_ DI ERRORE NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1002 (0x3EA)
</dt> <dt>



La finestra non può agire sul messaggio inviato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**IMPOSSIBILE \_ \_ COMPLETARE \_ L'ERRORE**
</dt> <dd> <dl> <dt>

1003 (0x3EB)
</dt> <dt>



Impossibile completare questa funzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**FLAG \_ DI ERRORE NON \_ VALIDI**
</dt> <dd> <dl> <dt>

1004 (0x3EC)
</dt> <dt>



Flag non validi.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**ERRORE \_ VOLUME NON \_ RICONOSCIUTO**
</dt> <dd> <dl> <dt>

1005 (0x3ED)
</dt> <dt>



Il volume non contiene un file system. Assicurarsi che tutti i driver file system siano caricati e che il volume non sia danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**FILE \_ DEGLI ERRORI NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1006 (0x3EE)
</dt> <dt>



Il volume per un file è stato modificato esternamente in modo che il file aperto non sia più valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**ERRORE \_ MODALITÀ SCHERMO \_ INTERO**
</dt> <dd> <dl> <dt>

1007 (0x3EF)
</dt> <dt>



L'operazione richiesta non può essere eseguita in modalità schermo intero.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**ERRORE \_ NESSUN \_ TOKEN**
</dt> <dd> <dl> <dt>

1008 (0x3F0)
</dt> <dt>



Si è tentato di fare riferimento a un token che non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADDB"></span><span id="error_baddb"></span>**ERRORE \_ BADDB**
</dt> <dd> <dl> <dt>

1009 (0x3F1)
</dt> <dt>



Il database del Registro di sistema di configurazione è danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**ERRORE \_ BADKEY**
</dt> <dd> <dl> <dt>

1010 (0x3F2)
</dt> <dt>



La chiave del Registro di sistema di configurazione non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**ERRORE \_ CANTOPEN**
</dt> <dd> <dl> <dt>

1011 (0x3F3)
</dt> <dt>



Impossibile aprire la chiave del Registro di sistema di configurazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**ERRORE \_ CANTREAD**
</dt> <dd> <dl> <dt>

1012 (0x3F4)
</dt> <dt>



Impossibile leggere la chiave del Registro di sistema di configurazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**ERRORE \_ CANTWRITE**
</dt> <dd> <dl> <dt>

1013 (0x3F5)
</dt> <dt>



Impossibile scrivere la chiave del Registro di sistema di configurazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**REGISTRO \_ ERRORI \_ RIPRISTINATO**
</dt> <dd> <dl> <dt>

1014 (0x3F6)
</dt> <dt>



Uno dei file nel database del Registro di sistema deve essere recuperato usando un log o una copia alternativa. Il ripristino è riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**ERRORE NEL \_ REGISTRO DI \_ SISTEMA DANNEGGIATO**
</dt> <dd> <dl> <dt>

1015 (0x3F7)
</dt> <dt>



Il Registro di sistema è danneggiato. La struttura di uno dei file contenenti i dati del Registro di sistema è danneggiata oppure l'immagine di memoria del sistema del file è danneggiata oppure non è stato possibile recuperare il file perché la copia o il log alternativo è assente o danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**ERRORE DI \_ \_ I/O DEL REGISTRO \_ DI SISTEMA NON RIUSCITO**
</dt> <dd> <dl> <dt>

1016 (0x3F8)
</dt> <dt>



Un'operazione di I/O avviata dal Registro di sistema non è riuscita in modo irreversibile. Il Registro di sistema non è stato in grado di leggere, scrivere o scaricare uno dei file che contengono l'immagine del sistema del Registro di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**ERRORE \_ NON FILE DEL REGISTRO DI \_ \_ SISTEMA**
</dt> <dd> <dl> <dt>

1017 (0x3F9)
</dt> <dt>



Il sistema ha tentato di caricare o ripristinare un file nel Registro di sistema, ma il file specificato non è in un formato di file del Registro di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**CHIAVE \_ DI ERRORE \_ ELIMINATA**
</dt> <dd> <dl> <dt>

1018 (0x3FA)
</dt> <dt>



Tentativo di operazione non valida su una chiave del Registro di sistema contrassegnata per l'eliminazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**ERRORE \_ SENZA SPAZIO DI \_ \_ LOG**
</dt> <dd> <dl> <dt>

1019 (0x3FB)
</dt> <dt>



Impossibile allocare lo spazio necessario in un registro del Registro di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**LA CHIAVE \_ DI ERRORE HA ELEMENTI \_ \_ FIGLIO**
</dt> <dd> <dl> <dt>

1020 (0x3FC)
</dt> <dt>



Impossibile creare un collegamento simbolico in una chiave del Registro di sistema che dispone già di sottochiavi o valori.


</dt> </dl> </dd> <dt>

<span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**\_L'ELEMENTO FIGLIO ERROR DEVE ESSERE \_ \_ \_ VOLATILE**
</dt> <dd> <dl> <dt>

1021 (0x3FD)
</dt> <dt>



Impossibile creare una sottochiave stabile in una chiave padre volatile.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**ERRORE \_ NOTIFY \_ ENUM \_ DIR**
</dt> <dd> <dl> <dt>

1022 (0x3FE)
</dt> <dt>



È in corso il completamento di una richiesta di modifica di notifica e le informazioni non vengono restituite nel buffer del chiamante. Il chiamante deve ora enumerare i file per trovare le modifiche.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**ERRORE DURANTE \_ \_ L'ESECUZIONE DEI SERVIZI \_ DIPENDENTI**
</dt> <dd> <dl> <dt>

1051 (0x41B)
</dt> <dt>



È stato inviato un controllo di arresto a un servizio da cui dipendono altri servizi in esecuzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**ERRORE CONTROLLO \_ DEL \_ SERVIZIO NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1052 (0x41C)
</dt> <dt>



Il controllo richiesto non è valido per questo servizio.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**ERROR \_ SERVICE REQUEST TIMEOUT (TIMEOUT RICHIESTA SERVIZIO \_ \_ ERRORI)**
</dt> <dd> <dl> <dt>

1053 (0x41D)
</dt> <dt>



Il servizio non ha risposto in tempo utile alla richiesta di avvio o di controllo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**SERVIZIO \_ ERRORI \_ NESSUN \_ THREAD**
</dt> <dd> <dl> <dt>

1054 (0x41E)
</dt> <dt>



Non è stato possibile creare un thread per il servizio.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**DATABASE \_ DEL SERVIZIO ERRORI \_ \_ BLOCCATO**
</dt> <dd> <dl> <dt>

1055 (0x41F)
</dt> <dt>



Il database del servizio è bloccato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**SERVIZIO \_ ERRORI GIÀ IN \_ \_ ESECUZIONE**
</dt> <dd> <dl> <dt>

1056 (0x420)
</dt> <dt>



Un'istanza del servizio è già in esecuzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**ERRORE ACCOUNT \_ \_ DEL SERVIZIO NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1057 (0x421)
</dt> <dt>



Il nome dell'account non è valido o non esiste oppure la password non è valida per il nome account specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DISABLED"></span><span id="error_service_disabled"></span>**SERVIZIO \_ ERRORI \_ DISABILITATO**
</dt> <dd> <dl> <dt>

1058 (0x422)
</dt> <dt>



Non è possibile avviare il servizio perché è disabilitato o perché ad esso non è associato alcun dispositivo abilitato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CIRCULAR_DEPENDENCY"></span><span id="error_circular_dependency"></span>**ERRORE \_ DI \_ DIPENDENZA CIRCOLARE**
</dt> <dd> <dl> <dt>

1059 (0x423)
</dt> <dt>



È stata specificata una dipendenza circolare del servizio.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DOES_NOT_EXIST"></span><span id="error_service_does_not_exist"></span>**IL \_ SERVIZIO ERRORI NON \_ \_ \_ ESISTE**
</dt> <dd> <dl> <dt>

1060 (0x424)
</dt> <dt>



Il servizio specificato non esiste come servizio installato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_CANNOT_ACCEPT_CTRL"></span><span id="error_service_cannot_accept_ctrl"></span>**IL SERVIZIO \_ ERRORI NON PUÒ ACCETTARE \_ \_ \_ CTRL**
</dt> <dd> <dl> <dt>

1061 (0x425)
</dt> <dt>



Il servizio non può accettare messaggi di controllo in questo momento.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_ACTIVE"></span><span id="error_service_not_active"></span>**SERVIZIO \_ ERRORI \_ NON \_ ATTIVO**
</dt> <dd> <dl> <dt>

1062 (0x426)
</dt> <dt>



Il servizio non è stato avviato.


</dt> </dl> </dd> <dt>

<span id="ERROR_FAILED_SERVICE_CONTROLLER_CONNECT"></span><span id="error_failed_service_controller_connect"></span>**ERRORE DURANTE \_ LA CONNESSIONE DEL CONTROLLER DEL \_ \_ \_ SERVIZIO**
</dt> <dd> <dl> <dt>

1063 (0x427)
</dt> <dt>



Il processo del servizio non è stato in grado di connettersi al controller del servizio.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXCEPTION_IN_SERVICE"></span><span id="error_exception_in_service"></span>**ECCEZIONE \_ DI ERRORE NEL \_ \_ SERVIZIO**
</dt> <dd> <dl> <dt>

1064 (0x428)
</dt> <dt>



Si è verificata un'eccezione nel servizio durante la gestione della richiesta di controllo.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATABASE_DOES_NOT_EXIST"></span><span id="error_database_does_not_exist"></span>**DATABASE \_ DEGLI \_ ERRORI \_ \_ INESISTENTE**
</dt> <dd> <dl> <dt>

1065 (0x429)
</dt> <dt>



Il database specificato non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_SPECIFIC_ERROR"></span><span id="error_service_specific_error"></span>**ERRORE \_ SPECIFICO \_ DEL \_ SERVIZIO**
</dt> <dd> <dl> <dt>

1066 (0x42A)
</dt> <dt>



Il servizio ha restituito un codice di errore specifico del servizio.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_ABORTED"></span><span id="error_process_aborted"></span>**PROCESSO \_ DI \_ ERRORE INTERROTTO**
</dt> <dd> <dl> <dt>

1067 (0x42B)
</dt> <dt>



Il processo è stato terminato in modo imprevisto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DEPENDENCY_FAIL"></span><span id="error_service_dependency_fail"></span>**ERRORE \_ DI DIPENDENZA DEL SERVIZIO NON \_ \_ RIUSCITA**
</dt> <dd> <dl> <dt>

1068 (0x42C)
</dt> <dt>



Impossibile avviare il servizio di dipendenza o il gruppo.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_LOGON_FAILED"></span><span id="error_service_logon_failed"></span>**ERRORE DURANTE \_ \_ L'ACCESSO AL \_ SERVIZIO**
</dt> <dd> <dl> <dt>

1069 (0x42D)
</dt> <dt>



il servizio non è stato avviato a causa di un errore in fase di accesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_START_HANG"></span><span id="error_service_start_hang"></span>**ERRORE DI \_ BLOCCO \_ DELL'AVVIO DEL \_ SERVIZIO**
</dt> <dd> <dl> <dt>

1070 (0x42E)
</dt> <dt>



Dopo l'avvio, il servizio si è bloccato in uno stato di avvio in sospeso.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICE_LOCK"></span><span id="error_invalid_service_lock"></span>**ERRORE BLOCCO \_ \_ DEL SERVIZIO NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1071 (0x42F)
</dt> <dt>



Il blocco del database del servizio specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_MARKED_FOR_DELETE"></span><span id="error_service_marked_for_delete"></span>**SERVIZIO \_ ERRORI \_ CONTRASSEGNATO PER \_ \_ L'ELIMINAZIONE**
</dt> <dd> <dl> <dt>

1072 (0x430)
</dt> <dt>



Il servizio specificato è stato contrassegnato per l'eliminazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_EXISTS"></span><span id="error_service_exists"></span>**ERRORE \_ SERVIZIO \_ ESISTENTE**
</dt> <dd> <dl> <dt>

1073 (0x431)
</dt> <dt>



Il servizio specificato esiste già.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_RUNNING_LKG"></span><span id="error_already_running_lkg"></span>**ERRORE DURANTE \_ \_ \_ L'ESECUZIONE DEL LKG**
</dt> <dd> <dl> <dt>

1074 (0x432)
</dt> <dt>



Il sistema è attualmente in esecuzione con l'ultima configurazione valida nota.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_DEPENDENCY_DELETED"></span><span id="error_service_dependency_deleted"></span>**ERRORE \_ DIPENDENZA \_ SERVIZIO \_ ELIMINATA**
</dt> <dd> <dl> <dt>

1075 (0x433)
</dt> <dt>



Il servizio di dipendenza non esiste o è stato contrassegnato per l'eliminazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_BOOT_ALREADY_ACCEPTED"></span><span id="error_boot_already_accepted"></span>**ERRORE \_ AVVIO \_ GIÀ \_ ACCETTATO**
</dt> <dd> <dl> <dt>

1076 (0x434)
</dt> <dt>



L'avvio corrente è già stato accettato per l'uso come ultimo set di controlli noto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NEVER_STARTED"></span><span id="error_service_never_started"></span>**SERVIZIO \_ ERRORI \_ MAI \_ AVVIATO**
</dt> <dd> <dl> <dt>

1077 (0x435)
</dt> <dt>



Non sono stati effettuati tentativi di avvio del servizio dall'ultimo avvio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUPLICATE_SERVICE_NAME"></span><span id="error_duplicate_service_name"></span>**ERRORE NOME \_ \_ SERVIZIO \_ DUPLICATO**
</dt> <dd> <dl> <dt>

1078 (0x436)
</dt> <dt>



Il nome è già in uso come nome del servizio o come nome visualizzato del servizio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIFFERENT_SERVICE_ACCOUNT"></span><span id="error_different_service_account"></span>**ERRORE \_ ACCOUNT DEL SERVIZIO \_ \_ DIVERSO**
</dt> <dd> <dl> <dt>

1079 (0x437)
</dt> <dt>



L'account specificato per questo servizio è diverso dall'account specificato per gli altri servizi in esecuzione nello stesso processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_DETECT_DRIVER_FAILURE"></span><span id="error_cannot_detect_driver_failure"></span>**ERRORE NON \_ È POSSIBILE \_ \_ RILEVARE L'ERRORE DEL \_ DRIVER**
</dt> <dd> <dl> <dt>

1080 (0x438)
</dt> <dt>



Le azioni di errore possono essere impostate solo per i servizi Win32, non per i driver.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_DETECT_PROCESS_ABORT"></span><span id="error_cannot_detect_process_abort"></span>**ERRORE NON \_ È POSSIBILE \_ RILEVARE \_ L'INTERRUZIONE \_ DEL PROCESSO**
</dt> <dd> <dl> <dt>

1081 (0x439)
</dt> <dt>



Questo servizio viene eseguito nello stesso processo di Gestione controllo servizi. Pertanto, il gestore di controllo del servizio non può eseguire alcuna azione se il processo del servizio termina in modo imprevisto.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RECOVERY_PROGRAM"></span><span id="error_no_recovery_program"></span>**ERRORE \_ NESSUN PROGRAMMA DI \_ \_ RIPRISTINO**
</dt> <dd> <dl> <dt>

1082 (0x43A)
</dt> <dt>



Per questo servizio non è stato configurato alcun programma di ripristino.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_IN_EXE"></span><span id="error_service_not_in_exe"></span>**SERVIZIO \_ ERRORI NON IN \_ \_ \_ EXE**
</dt> <dd> <dl> <dt>

1083 (0x43B)
</dt> <dt>



Il programma eseguibile in cui questo servizio è configurato per l'esecuzione non implementa il servizio.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SAFEBOOT_SERVICE"></span><span id="error_not_safeboot_service"></span>**ERRORE \_ NON DEL SERVIZIO \_ \_ SAFEBOOT**
</dt> <dd> <dl> <dt>

1084 (0x43C)
</dt> <dt>



Questo servizio non può essere avviato in Cassaforte predefinita.


</dt> </dl> </dd> <dt>

<span id="ERROR_END_OF_MEDIA"></span><span id="error_end_of_media"></span>**FINE \_ ERRORE \_ DEL \_ SUPPORTO**
</dt> <dd> <dl> <dt>

1100 (0x44C)
</dt> <dt>



È stata raggiunta l'estremità fisica del nastro.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILEMARK_DETECTED"></span><span id="error_filemark_detected"></span>**RILEVATO \_ FILEMARK \_ DI ERRORE**
</dt> <dd> <dl> <dt>

1101 (0x44D)
</dt> <dt>



L'accesso a un nastro ha raggiunto un contrassegno di file.


</dt> </dl> </dd> <dt>

<span id="ERROR_BEGINNING_OF_MEDIA"></span><span id="error_beginning_of_media"></span>**ERRORE \_ \_ ALL'INIZIO DEL \_ SUPPORTO**
</dt> <dd> <dl> <dt>

1102 (0x44E)
</dt> <dt>



È stato rilevato l'inizio del nastro o di una partizione.


</dt> </dl> </dd> <dt>

<span id="ERROR_SETMARK_DETECTED"></span><span id="error_setmark_detected"></span>**RILEVATO \_ ERRORE SETMARK \_**
</dt> <dd> <dl> <dt>

1103 (0x44F)
</dt> <dt>



L'accesso a un nastro ha raggiunto la fine di un set di file.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_DATA_DETECTED"></span><span id="error_no_data_detected"></span>**ERRORE \_ NESSUN \_ DATO \_ RILEVATO**
</dt> <dd> <dl> <dt>

1104 (0x450)
</dt> <dt>



Sul nastro non sono presenti altri dati.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARTITION_FAILURE"></span><span id="error_partition_failure"></span>**ERRORE DI \_ PARTIZIONE \_**
</dt> <dd> <dl> <dt>

1105 (0x451)
</dt> <dt>



Impossibile partizionare il nastro.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_BLOCK_LENGTH"></span><span id="error_invalid_block_length"></span>**ERRORE LUNGHEZZA \_ \_ BLOCCO NON \_ VALIDA**
</dt> <dd> <dl> <dt>

1106 (0x452)
</dt> <dt>



Quando si accede a un nuovo nastro di una partizione multivolume, la dimensione del blocco corrente non è corretta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_PARTITIONED"></span><span id="error_device_not_partitioned"></span>**ERRORE \_ DISPOSITIVO \_ NON \_ PARTIZIONATO**
</dt> <dd> <dl> <dt>

1107 (0x453)
</dt> <dt>



Impossibile trovare le informazioni sulla partizione del nastro durante il caricamento di un nastro.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_LOCK_MEDIA"></span><span id="error_unable_to_lock_media"></span>**ERRORE DURANTE \_ IL \_ BLOCCO DEI \_ \_ SUPPORTI**
</dt> <dd> <dl> <dt>

1108 (0x454)
</dt> <dt>



Impossibile bloccare il meccanismo di inserimento dei supporti.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_UNLOAD_MEDIA"></span><span id="error_unable_to_unload_media"></span>**ERRORE \_ DURANTE \_ LO \_ SCARICAMENTO DEI \_ SUPPORTI**
</dt> <dd> <dl> <dt>

1109 (0x455)
</dt> <dt>



Impossibile scaricare il supporto.


</dt> </dl> </dd> <dt>

<span id="ERROR_MEDIA_CHANGED"></span><span id="error_media_changed"></span>**SUPPORTO \_ DI \_ ERRORE MODIFICATO**
</dt> <dd> <dl> <dt>

1110 (0x456)
</dt> <dt>



Il supporto nell'unità potrebbe essere stato modificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_BUS_RESET"></span><span id="error_bus_reset"></span>**REIMPOSTAZIONE \_ DEL BUS DI \_ ERRORE**
</dt> <dd> <dl> <dt>

1111 (0x457)
</dt> <dt>



Il bus di I/O è stato reimpostato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MEDIA_IN_DRIVE"></span><span id="error_no_media_in_drive"></span>**ERRORE \_ NESSUN \_ SUPPORTO \_ \_ NELL'UNITÀ**
</dt> <dd> <dl> <dt>

1112 (0x458)
</dt> <dt>



Nessun supporto nell'unità.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_UNICODE_TRANSLATION"></span><span id="error_no_unicode_translation"></span>**ERRORE \_ NESSUNA \_ CONVERSIONE \_ UNICODE**
</dt> <dd> <dl> <dt>

1113 (0x459)
</dt> <dt>



Nella tabella codici multi byte di destinazione non esiste alcun mapping per il carattere Unicode.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_INIT_FAILED"></span><span id="error_dll_init_failed"></span>**ERRORE \_ DLL \_ INIT \_ FAILED**
</dt> <dd> <dl> <dt>

1114 (0x45A)
</dt> <dt>



Routine di inizializzazione della libreria di collegamento dinamico (DLL) non riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="error_shutdown_in_progress"></span>**ARRESTO \_ DEGLI ERRORI IN \_ \_ CORSO**
</dt> <dd> <dl> <dt>

1115 (0x45B)
</dt> <dt>



È in corso un arresto del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SHUTDOWN_IN_PROGRESS"></span><span id="error_no_shutdown_in_progress"></span>**ERRORE \_ NESSUN ARRESTO IN \_ \_ \_ CORSO**
</dt> <dd> <dl> <dt>

1116 (0x45C)
</dt> <dt>



Impossibile interrompere l'arresto del sistema perché non è in corso alcun arresto.


</dt> </dl> </dd> <dt>

<span id="ERROR_IO_DEVICE"></span><span id="error_io_device"></span>**ERRORE \_ DEL DISPOSITIVO DI \_ I/O**
</dt> <dd> <dl> <dt>

1117 (0x45D)
</dt> <dt>



Impossibile eseguire la richiesta a causa di un errore del dispositivo di I/O.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERIAL_NO_DEVICE"></span><span id="error_serial_no_device"></span>**ERRORE \_ \_ SERIALE NO \_ DISPOSITIVO**
</dt> <dd> <dl> <dt>

1118 (0x45E)
</dt> <dt>



Nessun dispositivo seriale è stato inizializzato correttamente. Il driver seriale verrà scaricato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IRQ_BUSY"></span><span id="error_irq_busy"></span>**ERRORE \_ IRQ \_ OCCUPATO**
</dt> <dd> <dl> <dt>

1119 (0x45F)
</dt> <dt>



Impossibile aprire un dispositivo che condivide una richiesta di interrupt (IRQ) con altri dispositivi. Almeno un altro dispositivo che usa tale IRQ è già aperto.


</dt> </dl> </dd> <dt>

<span id="ERROR_MORE_WRITES"></span><span id="error_more_writes"></span>**ERROR \_ MORE \_ WRITES**
</dt> <dd> <dl> <dt>

1120 (0x460)
</dt> <dt>



Un'operazione di I/O seriale è stata completata da un'altra operazione di scrittura sulla porta seriale. IL CONTATORE \_ \_ XOFF SERIALE IOCTL \_ ha raggiunto lo zero.


</dt> </dl> </dd> <dt>

<span id="ERROR_COUNTER_TIMEOUT"></span><span id="error_counter_timeout"></span>**TIMEOUT \_ CONTATORE \_ ERRORI**
</dt> <dd> <dl> <dt>

1121 (0x461)
</dt> <dt>



Operazione di I/O seriale completata perché il periodo di timeout è scaduto. IOCTL \_ SERIAL \_ XOFF \_ COUNTER non ha raggiunto lo zero.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_ID_MARK_NOT_FOUND"></span><span id="error_floppy_id_mark_not_found"></span>**ERRORE \_ CONTRASSEGNO \_ ID FLOPPY NON \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

1122 (0x462)
</dt> <dt>



Nessun contrassegno di indirizzo ID trovato nel disco floppy.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_WRONG_CYLINDER"></span><span id="error_floppy_wrong_cylinder"></span>**ERRORE \_ FLOPPY \_ \_ ERRATO CILINDRO**
</dt> <dd> <dl> <dt>

1123 (0x463)
</dt> <dt>



Mancata corrispondenza tra il campo ID settore disco floppy e l'indirizzo di traccia del controller del disco floppy.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_UNKNOWN_ERROR"></span><span id="error_floppy_unknown_error"></span>**ERRORE \_ FLOPPY \_ SCONOSCIUTO \_**
</dt> <dd> <dl> <dt>

1124 (0x464)
</dt> <dt>



Il controller del disco floppy ha segnalato un errore non riconosciuto dal driver del disco floppy.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOPPY_BAD_REGISTERS"></span><span id="error_floppy_bad_registers"></span>**ERRORE \_ NEI REGISTRI \_ FLOPPY NON \_ ERRE**
</dt> <dd> <dl> <dt>

1125 (0x465)
</dt> <dt>



Il controller del disco floppy ha restituito risultati incoerenti nei registri.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RECALIBRATE_FAILED"></span><span id="error_disk_recalibrate_failed"></span>**ERRORE \_ DI \_ RICALIBRAZIONE DEL DISCO \_ NON RIUSCITA**
</dt> <dd> <dl> <dt>

1126 (0x466)
</dt> <dt>



Durante l'accesso al disco rigido, un'operazione di ricalibrazione non è riuscita, anche dopo i tentativi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_OPERATION_FAILED"></span><span id="error_disk_operation_failed"></span>**ERRORE DURANTE \_ \_ L'OPERAZIONE SU DISCO NON \_ RIUSCITA**
</dt> <dd> <dl> <dt>

1127 (0x467)
</dt> <dt>



Durante l'accesso al disco rigido, un'operazione su disco non è riuscita anche dopo i tentativi.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_RESET_FAILED"></span><span id="error_disk_reset_failed"></span>**ERRORE DI \_ \_ REIMPOSTAZIONE DEL \_ DISCO NON RIUSCITA**
</dt> <dd> <dl> <dt>

1128 (0x468)
</dt> <dt>



Durante l'accesso al disco rigido, era necessaria una reimpostazione del controller del disco, ma anche questa operazione non è riuscita.


</dt> </dl> </dd> <dt>

<span id="ERROR_EOM_OVERFLOW"></span><span id="error_eom_overflow"></span>**ERROR \_ EOM \_ OVERFLOW**
</dt> <dd> <dl> <dt>

1129 (0x469)
</dt> <dt>



Fine fisica del nastro rilevata.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_ENOUGH_SERVER_MEMORY"></span><span id="error_not_enough_server_memory"></span>**ERRORE \_ MEMORIA \_ SERVER \_ \_ INSUFFICIENTE**
</dt> <dd> <dl> <dt>

1130 (0x46A)
</dt> <dt>



Memoria insufficiente nel server per eseguire il comando.


</dt> </dl> </dd> <dt>

<span id="ERROR_POSSIBLE_DEADLOCK"></span><span id="error_possible_deadlock"></span>**ERRORE \_ POSSIBILE \_ DEADLOCK**
</dt> <dd> <dl> <dt>

1131 (0x46B)
</dt> <dt>



È stata rilevata una potenziale condizione di deadlock.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAPPED_ALIGNMENT"></span><span id="error_mapped_alignment"></span>**ERRORE DURANTE \_ IL MAPPING \_ DELL'ALLINEAMENTO**
</dt> <dd> <dl> <dt>

1132 (0x46C)
</dt> <dt>



L'indirizzo di base o l'offset di file specificato non ha l'allineamento corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_POWER_STATE_VETOED"></span><span id="error_set_power_state_vetoed"></span>**ERROR \_ SET \_ POWER \_ STATE \_ VETOED**
</dt> <dd> <dl> <dt>

1140 (0x474)
</dt> <dt>



Un tentativo di modificare lo stato di alimentazione del sistema è stato effettuato da un'altra applicazione o driver.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_POWER_STATE_FAILED"></span><span id="error_set_power_state_failed"></span>**ERRORE \_ DURANTE L'IMPOSTAZIONE \_ DELLO STATO DI ALIMENTAZIONE NON \_ \_ RIUSCITO**
</dt> <dd> <dl> <dt>

1141 (0x475)
</dt> <dt>



Il BIOS di sistema non è riuscito a modificare lo stato di alimentazione del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_TOO_MANY_LINKS"></span><span id="error_too_many_links"></span>**ERRORE \_ TROPPI \_ \_ COLLEGAMENTI**
</dt> <dd> <dl> <dt>

1142 (0x476)
</dt> <dt>



È stato effettuato un tentativo di creare più collegamenti in un file rispetto file system supporta.


</dt> </dl> </dd> <dt>

<span id="ERROR_OLD_WIN_VERSION"></span><span id="error_old_win_version"></span>**ERRORE \_ VERSIONE \_ PRECEDENTE \_ WIN**
</dt> <dd> <dl> <dt>

1150 (0x47E)
</dt> <dt>



Il programma specificato richiede una versione più recente di Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_WRONG_OS"></span><span id="error_app_wrong_os"></span>**ERRORE \_ DEL SISTEMA OPERATIVO \_ \_ ERRATO DELL'APP**
</dt> <dd> <dl> <dt>

1151 (0x47F)
</dt> <dt>



Il programma specificato non è un programma Windows o MS-DOS.


</dt> </dl> </dd> <dt>

<span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**ERRORE \_ APP A ISTANZA \_ \_ SINGOLA**
</dt> <dd> <dl> <dt>

1152 (0x480)
</dt> <dt>



Impossibile avviare più di un'istanza del programma specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**ERRORE \_ NELL'APP RMODE \_**
</dt> <dd> <dl> <dt>

1153 (0x481)
</dt> <dt>



Il programma specificato è stato scritto per una versione precedente di Windows.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**ERRORE \_ DLL NON \_ VALIDA**
</dt> <dd> <dl> <dt>

1154 (0x482)
</dt> <dt>



Uno dei file di libreria necessari per eseguire l'applicazione è danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**ERRORE \_ NESSUNA \_ ASSOCIAZIONE**
</dt> <dd> <dl> <dt>

1155 (0x483)
</dt> <dt>



Nessuna applicazione è associata al file specificato per questa operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**ERRORE \_ DDE \_ FAIL**
</dt> <dd> <dl> <dt>

1156 (0x484)
</dt> <dt>



Si è verificato un errore durante l'invio del comando all'applicazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**ERRORE \_ DLL \_ NON \_ TROVATA**
</dt> <dd> <dl> <dt>

1157 (0x485)
</dt> <dt>



Impossibile trovare uno dei file di libreria necessari per eseguire l'applicazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**ERRORE \_ NESSUN ALTRO HANDLE \_ \_ \_ UTENTE**
</dt> <dd> <dl> <dt>

1158 (0x486)
</dt> <dt>



Il processo corrente ha usato tutti i relativi handle di sistema per gli oggetti di Gestione finestre.


</dt> </dl> </dd> <dt>

<span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**SOLO \_ SINCRONIZZAZIONE \_ DEI MESSAGGI DI \_ ERRORE**
</dt> <dd> <dl> <dt>

1159 (0x487)
</dt> <dt>



Il messaggio può essere usato solo con operazioni sincrone.


</dt> </dl> </dd> <dt>

<span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**ELEMENTO \_ ORIGINE \_ ERRORE \_ VUOTO**
</dt> <dd> <dl> <dt>

1160 (0x488)
</dt> <dt>



L'elemento di origine indicato non dispone di supporti.


</dt> </dl> </dd> <dt>

<span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**ERROR \_ DESTINATION \_ ELEMENT \_ FULL**
</dt> <dd> <dl> <dt>

1161 (0x489)
</dt> <dt>



L'elemento di destinazione indicato contiene già supporti.


</dt> </dl> </dd> <dt>

<span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**ERRORE INDIRIZZO \_ ELEMENTO \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1162 (0x48A)
</dt> <dt>



L'elemento indicato non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**ERRORE \_ MAGAZINE \_ NON \_ PRESENTE**
</dt> <dd> <dl> <dt>

1163 (0x48B)
</dt> <dt>



L'elemento indicato fa parte di una rivista che non è presente.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**ERRORE \_ DI \_ REINIZIALIZZAZIONE DEL \_ DISPOSITIVO NECESSARIA**
</dt> <dd> <dl> <dt>

1164 (0x48C)
</dt> <dt>



Il dispositivo indicato richiede la reinizializzazione a causa di errori hardware.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**ERRORE DISPOSITIVO \_ \_ RICHIEDE \_ PULIZIA**
</dt> <dd> <dl> <dt>

1165 (0x48D)
</dt> <dt>



Il dispositivo ha indicato che è necessaria la pulizia prima di eseguire altre operazioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**ERRORE \_ DI APERTURA DELLA PORTA DEL \_ \_ DISPOSITIVO**
</dt> <dd> <dl> <dt>

1166 (0x48E)
</dt> <dt>



Il dispositivo ha indicato che la porta è aperta.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**ERRORE \_ DISPOSITIVO \_ NON \_ CONNESSO**
</dt> <dd> <dl> <dt>

1167 (0x48F)
</dt> <dt>



Il dispositivo non è connesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**ERRORE \_ NON \_ TROVATO**
</dt> <dd> <dl> <dt>

1168 (0x490)
</dt> <dt>



Element not found.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**ERRORE \_ NESSUNA \_ CORRISPONDENZA**
</dt> <dd> <dl> <dt>

1169 (0x491)
</dt> <dt>



Non è stata trovata alcuna corrispondenza per la chiave specificata nell'indice.


</dt> </dl> </dd> <dt>

<span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**SET \_ DI ERRORI NON \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

1170 (0x492)
</dt> <dt>



Il set di proprietà specificato non esiste nell'oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**PUNTO \_ DI ERRORE NON \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

1171 (0x493)
</dt> <dt>



Il punto passato a GetMouseMovePoints non si trova nel buffer.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**ERROR \_ NO \_ TRACKING \_ SERVICE**
</dt> <dd> <dl> <dt>

1172 (0x494)
</dt> <dt>



Il servizio di rilevamento (workstation) non è in esecuzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**ERRORE \_ NESSUN \_ ID \_ VOLUME**
</dt> <dd> <dl> <dt>

1173 (0x495)
</dt> <dt>



Impossibile trovare l'ID volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**ERRORE IMPOSSIBILE \_ \_ RIMUOVERE \_ \_ SOSTITUITO**
</dt> <dd> <dl> <dt>

1175 (0x497)
</dt> <dt>



Impossibile rimuovere il file da sostituire.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**ERRORE IMPOSSIBILE \_ \_ SPOSTARE LA \_ \_ SOSTITUZIONE**
</dt> <dd> <dl> <dt>

1176 (0x498)
</dt> <dt>



Impossibile spostare il file sostitutivo nel file da sostituire. Il file da sostituire ha mantenuto il nome originale.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**ERRORE \_ IMPOSSIBILE SPOSTARE LA SOSTITUZIONE \_ \_ \_ \_ 2**
</dt> <dd> <dl> <dt>

1177 (0x499)
</dt> <dt>



Impossibile spostare il file sostitutivo nel file da sostituire. Il file da sostituire è stato rinominato usando il nome del backup.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**ELIMINAZIONE \_ JOURNAL ERRORI IN \_ \_ \_ CORSO**
</dt> <dd> <dl> <dt>

1178 (0x49A)
</dt> <dt>



È in corso l'eliminazione del journal delle modifiche al volume.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**JOURNAL \_ ERRORI \_ NON \_ ATTIVO**
</dt> <dd> <dl> <dt>

1179 (0x49B)
</dt> <dt>



Il journal delle modifiche al volume non è attivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**È STATO \_ RILEVATO UN ERRORE NEL FILE \_ \_ POTENZIALE**
</dt> <dd> <dl> <dt>

1180 (0x49C)
</dt> <dt>



È stato trovato un file, ma potrebbe non essere il file corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**ERROR \_ JOURNAL \_ ENTRY \_ DELETED**
</dt> <dd> <dl> <dt>

1181 (0x49D)
</dt> <dt>



La voce del journal è stata eliminata dal journal.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**\_L'ARRESTO DEGLI ERRORI È \_ \_ PIANIFICATO**
</dt> <dd> <dl> <dt>

1190 (0x4A6)
</dt> <dt>



È già stato pianificato un arresto del sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**ERRORE DI \_ ARRESTO \_ DEGLI UTENTI \_ \_ CONNESSI**
</dt> <dd> <dl> <dt>

1191 (0x4A7)
</dt> <dt>



Non è possibile avviare l'arresto del sistema perché sono presenti altri utenti connessi al computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**ERRORE \_ DISPOSITIVO \_ NON GRAVE**
</dt> <dd> <dl> <dt>

1200 (0x4B0)
</dt> <dt>



Il nome del dispositivo specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**ERRORE \_ DI CONNESSIONE NON \_ INVAIL**
</dt> <dd> <dl> <dt>

1201 (0x4B1)
</dt> <dt>



Il dispositivo non è attualmente connesso, ma è una connessione memorizzata.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**ERRORE \_ DISPOSITIVO \_ GIÀ \_ MEMORIZZATA**
</dt> <dd> <dl> <dt>

1202 (0x4B2)
</dt> <dt>



Il nome del dispositivo locale ha una connessione memorizzata a un'altra risorsa di rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**ERRORE \_ NESSUN PERCORSO DI RETE O NON \_ \_ \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

1203 (0x4B3)
</dt> <dt>



Il percorso di rete è stato digitato in modo non corretto, non esiste o il provider di rete non è attualmente disponibile. Provare a creare nuovamente il percorso o contattare l'amministratore di rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**ERRORE \_ PROVIDER \_ NON ERATO**
</dt> <dd> <dl> <dt>

1204 (0x4B4)
</dt> <dt>



Il nome del provider di rete specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**ERRORE: \_ IMPOSSIBILE \_ APRIRE IL \_ PROFILO**
</dt> <dd> <dl> <dt>

1205 (0x4B5)
</dt> <dt>



Impossibile aprire il profilo di connessione di rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**ERRORE \_ PROFILO \_ NON ERTA**
</dt> <dd> <dl> <dt>

1206 (0x4B6)
</dt> <dt>



Il profilo di connessione di rete è danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**ERRORE \_ NON \_ CONTENITORE**
</dt> <dd> <dl> <dt>

1207 (0x4B7)
</dt> <dt>



Impossibile enumerare un non contenitore.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**ERRORE \_ ESTESO \_ ERRORE**
</dt> <dd> <dl> <dt>

1208 (0x4B8)
</dt> <dt>



Si è verificato un errore esteso.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**ERRORE \_ \_ GROUPNAME NON VALIDO**
</dt> <dd> <dl> <dt>

1209 (0x4B9)
</dt> <dt>



Il formato del nome del gruppo specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**ERRORE \_ \_ NOMECOMPUTER NON VALIDO**
</dt> <dd> <dl> <dt>

1210 (0x4BA)
</dt> <dt>



Il formato del nome computer specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**ERRORE \_ NOME EVENTO NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1211 (0x4BB)
</dt> <dt>



Il formato del nome dell'evento specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**ERRORE \_ \_ NOMEDOMINIO NON VALIDO**
</dt> <dd> <dl> <dt>

1212 (0x4BC)
</dt> <dt>



Il formato del nome di dominio specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**ERRORE \_ NOME SERVIZIO NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1213 (0x4BD)
</dt> <dt>



Il formato del nome del servizio specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**ERRORE \_ \_ NETNAME NON VALIDO**
</dt> <dd> <dl> <dt>

1214 (0x4BE)
</dt> <dt>



Il formato del nome di rete specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**ERRORE \_ NOME CONDIVISIONE NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1215 (0x4BF)
</dt> <dt>



Il formato del nome di condivisione specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**ERRORE \_ NOME PASSWORD NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1216 (0x4C0)
</dt> <dt>



Il formato della password specificata non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**ERRORE \_ NOME MESSAGGIO NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1217 (0x4C1)
</dt> <dt>



Il formato del nome del messaggio specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**ERRORE \_ \_ MESSAGEDEST NON VALIDO**
</dt> <dd> <dl> <dt>

1218 (0x4C2)
</dt> <dt>



Il formato della destinazione del messaggio specificata non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**ERRORE DURANTE \_ IL CONFLITTO DI CREDENZIALI DELLA \_ \_ SESSIONE**
</dt> <dd> <dl> <dt>

1219 (0x4C3)
</dt> <dt>



Non sono consentite più connessioni a un server o a una risorsa condivisa da parte dello stesso utente, che usano più di un nome utente. Disconnettere tutte le connessioni precedenti al server o alla risorsa condivisa e riprovare.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**SI È \_ VERIFICATO UN ERRORE DURANTE IL \_ \_ \_ SUPERAMENTO DEL LIMITE DI SESSIONI REMOTE**
</dt> <dd> <dl> <dt>

1220 (0x4C4)
</dt> <dt>



È stato effettuato un tentativo di stabilire una sessione con un server di rete, ma sono già state stabilite troppe sessioni per tale server.


</dt> </dl> </dd> <dt>

<span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**ERRORE \_ DUP \_ DOMAINNAME**
</dt> <dd> <dl> <dt>

1221 (0x4C5)
</dt> <dt>



Il nome del gruppo di lavoro o del dominio è già utilizzato da un altro computer in rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**ERRORE \_ NESSUNA \_ RETE**
</dt> <dd> <dl> <dt>

1222 (0x4C6)
</dt> <dt>



La rete non è presente o non è stata avviata.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**ERRORE \_ ANNULLATO**
</dt> <dd> <dl> <dt>

1223 (0x4C7)
</dt> <dt>



L'operazione è stata annullata dall'utente.


</dt> </dl> </dd> <dt>

<span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**ERRORE \_ FILE \_ MAPPATO DALL'UTENTE \_**
</dt> <dd> <dl> <dt>

1224 (0x4C8)
</dt> <dt>



L'operazione richiesta non può essere eseguita su un file con una sezione mappata all'utente aperta.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**ERRORE \_ CONNESSIONE \_ RIFIUTATA**
</dt> <dd> <dl> <dt>

1225 (0x4C9)
</dt> <dt>



Il computer remoto ha rifiutato la connessione di rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**ERRORE \_ DI DISCONNESSIONE \_ CON TOLLERANZA**
</dt> <dd> <dl> <dt>

1226 (0x4CA)
</dt> <dt>



La connessione di rete è stata chiusa normalmente.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**INDIRIZZO \_ DI ERRORE GIÀ \_ \_ ASSOCIATO**
</dt> <dd> <dl> <dt>

1227 (0x4CB)
</dt> <dt>



All'endpoint di trasporto di rete è già associato un indirizzo.


</dt> </dl> </dd> <dt>

<span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**INDIRIZZO \_ DI ERRORE NON \_ \_ ASSOCIATO**
</dt> <dd> <dl> <dt>

1228 (0x4CC)
</dt> <dt>



Un indirizzo non è ancora stato associato all'endpoint di rete.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**ERRORE CONNESSIONE \_ \_ NON VALIDA**
</dt> <dd> <dl> <dt>

1229 (0x4CD)
</dt> <dt>



È stata tentata un'operazione su una connessione di rete inesistente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**ERRORE \_ DI CONNESSIONE \_ ATTIVA**
</dt> <dd> <dl> <dt>

1230 (0x4CE)
</dt> <dt>



È stata tentata un'operazione non valida in una connessione di rete attiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**ERRORE \_ RETE \_ NON RAGGIUNGIBILE**
</dt> <dd> <dl> <dt>

1231 (0x4CF)
</dt> <dt>



Impossibile raggiungere il percorso di rete. Per informazioni sulla risoluzione dei problemi di rete, Windows Guida.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**ERRORE \_ HOST \_ NON RAGGIUNGIBILE**
</dt> <dd> <dl> <dt>

1232 (0x4D0)
</dt> <dt>



Impossibile raggiungere il percorso di rete. Per informazioni sulla risoluzione dei problemi di rete, Windows Guida.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**PROTOCOLLO \_ DI ERRORE NON \_ RAGGIUNGIBILE**
</dt> <dd> <dl> <dt>

1233 (0x4D1)
</dt> <dt>



Impossibile raggiungere il percorso di rete. Per informazioni sulla risoluzione dei problemi di rete, vedere Windows Guida.


</dt> </dl> </dd> <dt>

<span id="ERROR_PORT_UNREACHABLE"></span><span id="error_port_unreachable"></span>**PORTA \_ DI ERRORE NON \_ RAGGIUNGIBILE**
</dt> <dd> <dl> <dt>

1234 (0x4D2)
</dt> <dt>



Nessun servizio funziona nell'endpoint di rete di destinazione nel sistema remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_REQUEST_ABORTED"></span><span id="error_request_aborted"></span>**RICHIESTA \_ DI ERRORE \_ INTERROTTA**
</dt> <dd> <dl> <dt>

1235 (0x4D3)
</dt> <dt>



La richiesta è stata interrotta.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_ABORTED"></span><span id="error_connection_aborted"></span>**ERRORE \_ DI \_ CONNESSIONE INTERROTTA**
</dt> <dd> <dl> <dt>

1236 (0x4D4)
</dt> <dt>



La connessione di rete è stata interrotta dal sistema locale.


</dt> </dl> </dd> <dt>

<span id="ERROR_RETRY"></span><span id="error_retry"></span>**NUOVO \_ TENTATIVO DI ERRORE**
</dt> <dd> <dl> <dt>

1237 (0x4D5)
</dt> <dt>



Impossibile completare l'operazione. Deve essere eseguito un nuovo tentativo.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONNECTION_COUNT_LIMIT"></span><span id="error_connection_count_limit"></span>**LIMITE \_ CONTEGGIO \_ CONNESSIONI \_ ERRORI**
</dt> <dd> <dl> <dt>

1238 (0x4D6)
</dt> <dt>



Impossibile stabilire una connessione al server perché è stato raggiunto il limite per il numero di connessioni simultanee per questo account.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGIN_TIME_RESTRICTION"></span><span id="error_login_time_restriction"></span>**RESTRIZIONE \_ DELL'ORA \_ DI ACCESSO DEGLI \_ ERRORI**
</dt> <dd> <dl> <dt>

1239 (0x4D7)
</dt> <dt>



Tentativo di accesso durante un'ora del giorno non autorizzata per questo account.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOGIN_WKSTA_RESTRICTION"></span><span id="error_login_wksta_restriction"></span>**RESTRIZIONE \_ WKSTA DI ACCESSO \_ \_ ERRORE**
</dt> <dd> <dl> <dt>

1240 (0x4D8)
</dt> <dt>



L'account non è autorizzato ad accedere da questa stazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCORRECT_ADDRESS"></span><span id="error_incorrect_address"></span>**ERRORE \_ INDIRIZZO NON \_ CORRETTO**
</dt> <dd> <dl> <dt>

1241 (0x4D9)
</dt> <dt>



Impossibile usare l'indirizzo di rete per l'operazione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_REGISTERED"></span><span id="error_already_registered"></span>**ERRORE \_ GIÀ \_ REGISTRATO**
</dt> <dd> <dl> <dt>

1242 (0x4DA)
</dt> <dt>



Il servizio è già registrato.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOT_FOUND"></span><span id="error_service_not_found"></span>**SERVIZIO \_ ERRORI \_ NON \_ TROVATO**
</dt> <dd> <dl> <dt>

1243 (0x4DB)
</dt> <dt>



Il servizio specificato non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_AUTHENTICATED"></span><span id="error_not_authenticated"></span>**ERRORE \_ NON \_ AUTENTICATO**
</dt> <dd> <dl> <dt>

1244 (0x4DC)
</dt> <dt>



L'operazione richiesta non è stata eseguita perché l'utente non è stato autenticato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_LOGGED_ON"></span><span id="error_not_logged_on"></span>**ERRORE \_ NON \_ \_ CONNESSO**
</dt> <dd> <dl> <dt>

1245 (0x4DD)
</dt> <dt>



L'operazione richiesta non è stata eseguita perché l'utente non ha eseguito l'accesso alla rete. Il servizio specificato non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTINUE"></span><span id="error_continue"></span>**CONTINUARE CON \_ L'ERRORE**
</dt> <dd> <dl> <dt>

1246 (0x4DE)
</dt> <dt>



Continuare con il lavoro in corso.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_INITIALIZED"></span><span id="error_already_initialized"></span>**ERRORE \_ GIÀ \_ INIZIALIZZATO**
</dt> <dd> <dl> <dt>

1247 (0x4DF)
</dt> <dt>



È stato effettuato un tentativo di eseguire un'operazione di inizializzazione quando l'inizializzazione è già stata completata.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_MORE_DEVICES"></span><span id="error_no_more_devices"></span>**ERRORE \_ NESSUN \_ ALTRO \_ DISPOSITIVO**
</dt> <dd> <dl> <dt>

1248 (0x4E0)
</dt> <dt>



Nessun altro dispositivo locale.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SUCH_SITE"></span><span id="error_no_such_site"></span>**ERRORE \_ NESSUN SITO DI QUESTO \_ \_ TIPO**
</dt> <dd> <dl> <dt>

1249 (0x4E1)
</dt> <dt>



Il sito specificato non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOMAIN_CONTROLLER_EXISTS"></span><span id="error_domain_controller_exists"></span>**ERRORE \_ CONTROLLER DI DOMINIO \_ \_ ESISTENTE**
</dt> <dd> <dl> <dt>

1250 (0x4E2)
</dt> <dt>



Esiste già un controller di dominio con il nome specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_ONLY_IF_CONNECTED"></span><span id="error_only_if_connected"></span>**ERRORE \_ SOLO \_ SE \_ CONNESSO**
</dt> <dd> <dl> <dt>

1251 (0x4E3)
</dt> <dt>



Questa operazione è supportata solo quando si è connessi al server.


</dt> </dl> </dd> <dt>

<span id="ERROR_OVERRIDE_NOCHANGES"></span><span id="error_override_nochanges"></span>**ERRORE \_ OVERRIDE \_ NOCHANGES**
</dt> <dd> <dl> <dt>

1252 (0x4E4)
</dt> <dt>



Il framework di Criteri di gruppo deve chiamare l'estensione anche se non sono presenti modifiche.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_USER_PROFILE"></span><span id="error_bad_user_profile"></span>**ERRORE \_ PROFILO UTENTE NON \_ \_ GRAVE**
</dt> <dd> <dl> <dt>

1253 (0x4E5)
</dt> <dt>



L'utente specificato non ha un profilo valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SUPPORTED_ON_SBS"></span><span id="error_not_supported_on_sbs"></span>**ERRORE \_ NON SUPPORTATO IN \_ \_ \_ SBS**
</dt> <dd> <dl> <dt>

1254 (0x4E6)
</dt> <dt>



Questa operazione non è supportata in un computer che esegue Windows Server 2003 per Small Business Server.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVER_SHUTDOWN_IN_PROGRESS"></span><span id="error_server_shutdown_in_progress"></span>**ARRESTO \_ DEL SERVER DEGLI ERRORI IN \_ \_ \_ CORSO**
</dt> <dd> <dl> <dt>

1255 (0x4E7)
</dt> <dt>



Il computer server è in fase di arresto.


</dt> </dl> </dd> <dt>

<span id="ERROR_HOST_DOWN"></span><span id="error_host_down"></span>**ERRORE \_ HOST \_ IN GIÙ**
</dt> <dd> <dl> <dt>

1256 (0x4E8)
</dt> <dt>



Il sistema remoto non è disponibile. Per informazioni sulla risoluzione dei problemi di rete, vedere Windows Guida.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_ACCOUNT_SID"></span><span id="error_non_account_sid"></span>**ERRORE \_ \_ SID NON \_ ACCOUNT**
</dt> <dd> <dl> <dt>

1257 (0x4E9)
</dt> <dt>



L'identificatore di sicurezza fornito non è di un dominio dell'account.


</dt> </dl> </dd> <dt>

<span id="ERROR_NON_DOMAIN_SID"></span><span id="error_non_domain_sid"></span>**ERRORE \_ NON \_ \_ SID DI DOMINIO**
</dt> <dd> <dl> <dt>

1258 (0x4EA)
</dt> <dt>



L'identificatore di sicurezza fornito non dispone di un componente di dominio.


</dt> </dl> </dd> <dt>

<span id="ERROR_APPHELP_BLOCK"></span><span id="error_apphelp_block"></span>**ERRORE \_ BLOCCO APPHELP \_**
</dt> <dd> <dl> <dt>

1259 (0x4EB)
</dt> <dt>



La finestra di dialogo AppHelp è stata annullata impedendo l'avvio dell'applicazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_BY_POLICY"></span><span id="error_access_disabled_by_policy"></span>**ERRORE \_ DI ACCESSO DISABILITATO DAI \_ \_ \_ CRITERI**
</dt> <dd> <dl> <dt>

1260 (0x4EC)
</dt> <dt>



Questo programma è bloccato da Criteri di gruppo. Per altre informazioni, contattare l'amministratore di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_REG_NAT_CONSUMPTION"></span><span id="error_reg_nat_consumption"></span>**ERRORE DURANTE \_ L'UTILIZZO \_ DI NAT \_ REG**
</dt> <dd> <dl> <dt>

1261 (0x4ED)
</dt> <dt>



Un programma tenta di usare un valore di registro non valido. In genere causato da un registro non inizializzato. Questo errore è specifico di Itanium.


</dt> </dl> </dd> <dt>

<span id="ERROR_CSCSHARE_OFFLINE"></span><span id="error_cscshare_offline"></span>**ERRORE \_ CSCSHARE \_ OFFLINE**
</dt> <dd> <dl> <dt>

1262 (0x4EE)
</dt> <dt>



La condivisione è attualmente offline o non esiste.


</dt> </dl> </dd> <dt>

<span id="ERROR_PKINIT_FAILURE"></span><span id="error_pkinit_failure"></span>**ERRORE \_ PKINIT \_ FAILURE**
</dt> <dd> <dl> <dt>

1263 (0x4EF)
</dt> <dt>



Il protocollo Kerberos ha rilevato un errore durante la convalida del certificato KDC durante l'accesso con smart card. Sono disponibili altre informazioni nel registro eventi di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_SMARTCARD_SUBSYSTEM_FAILURE"></span><span id="error_smartcard_subsystem_failure"></span>**ERRORE \_ DEL \_ SOTTOSISTEMA SMART \_ CARD**
</dt> <dd> <dl> <dt>

1264 (0x4F0)
</dt> <dt>



Il protocollo Kerberos ha rilevato un errore durante il tentativo di utilizzare il sottosistema smart card.


</dt> </dl> </dd> <dt>

<span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**RILEVATO \_ DOWNGRADE DEGLI \_ ERRORI**
</dt> <dd> <dl> <dt>

1265 (0x4F1)
</dt> <dt>



Il sistema non è in grado di contattare un controller di dominio per eseguire la richiesta di autenticazione. Riprova più tardi.


</dt> </dl> </dd> <dt>

<span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**ERRORE \_ COMPUTER \_ BLOCCATO**
</dt> <dd> <dl> <dt>

1271 (0x4F7)
</dt> <dt>



Il computer è bloccato e non può essere arrestato senza l'opzione force.


</dt> </dl> </dd> <dt>

<span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**DATI \_ NON VALIDI FORNITI DAL CALLBACK DI \_ \_ \_ ERRORE**
</dt> <dd> <dl> <dt>

1273 (0x4F9)
</dt> <dt>



Quando viene chiamato, un callback definito dall'applicazione ha fornito dati non validi.


</dt> </dl> </dd> <dt>

<span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**AGGIORNAMENTO IN \_ \_ PRIMO PIANO DELLA \_ SINCRONIZZAZIONE DEGLI ERRORI \_ OBBLIGATORIO**
</dt> <dd> <dl> <dt>

1274 (0x4FA)
</dt> <dt>



Il framework di Criteri di gruppo deve chiamare l'estensione nell'aggiornamento sincrono dei criteri in primo piano.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**DRIVER \_ DI ERRORE \_ BLOCCATO**
</dt> <dd> <dl> <dt>

1275 (0x4FB)
</dt> <dt>



Il caricamento di questo driver è stato bloccato.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**ERRORE DURANTE \_ \_ L'IMPORTAZIONE \_ NON VALIDA DI NON \_ \_ DLL**
</dt> <dd> <dl> <dt>

1276 (0x4FC)
</dt> <dt>



Una libreria di collegamento dinamico (DLL) fa riferimento a un modulo che non era né una DLL né l'immagine eseguibile del processo.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**ERRORE \_ DI \_ ACCESSO \_ WEBBLADE DISABILITATO**
</dt> <dd> <dl> <dt>

1277 (0x4FD)
</dt> <dt>



Windows possibile aprire il programma perché è stato disabilitato.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**MANOMISSIONE \_ \_ \_ WEBBLADE DISABILITATA PER \_ L'ACCESSO AGLI ERRORI**
</dt> <dd> <dl> <dt>

1278 (0x4FE)
</dt> <dt>



Windows possibile aprire il programma perché il sistema di imposizione delle licenze è stato manomesso o danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**ERRORE DURANTE \_ IL \_ RIPRISTINO**
</dt> <dd> <dl> <dt>

1279 (0x4FF)
</dt> <dt>



Recupero della transazione non riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**ERRORE \_ GIÀ \_ FIBER**
</dt> <dd> <dl> <dt>

1280 (0x500)
</dt> <dt>



Il thread corrente è già stato convertito in un fiber.


</dt> </dl> </dd> <dt>

<span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**ERRORE \_ GIÀ \_ THREAD**
</dt> <dd> <dl> <dt>

1281 (0x501)
</dt> <dt>



Il thread corrente è già stato convertito da un fiber.


</dt> </dl> </dd> <dt>

<span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**SOVRACCARICO \_ DEL BUFFER DELLO STACK DI \_ \_ ERRORI**
</dt> <dd> <dl> <dt>

1282 (0x502)
</dt> <dt>



Il sistema ha rilevato un sovraccarico di un buffer basato su stack in questa applicazione. Questo sovraccarico potrebbe potenzialmente consentire a un utente malintenzionato di ottenere il controllo di questa applicazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**QUOTA \_ DEL PARAMETRO DI ERRORE \_ \_ SUPERATA**
</dt> <dd> <dl> <dt>

1283 (0x503)
</dt> <dt>



I dati presenti in uno dei parametri sono più di quelli su cui la funzione può operare.


</dt> </dl> </dd> <dt>

<span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**\_DEBUGGER DEGLI ERRORI \_ INATTIVO**
</dt> <dd> <dl> <dt>

1284 (0x504)
</dt> <dt>



Tentativo di eseguire un'operazione su un oggetto di debug non riuscito perché è in corso l'eliminazione dell'oggetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**ERRORE CARICAMENTO \_ \_ RITARDATO \_ NON RIUSCITO**
</dt> <dd> <dl> <dt>

1285 (0x505)
</dt> <dt>



Tentativo di ritardare il caricamento di un .dll o ottenere un indirizzo di funzione in un .dll caricamento ritardato non riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**ERRORE \_ VDM \_ NON CONSENTITO**
</dt> <dd> <dl> <dt>

1286 (0x506)
</dt> <dt>



%1 è un'applicazione a 16 bit. Non si dispone delle autorizzazioni per eseguire applicazioni a 16 bit. Controllare le autorizzazioni con l'amministratore di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**ERRORE \_ NON \_ IDENTIFICATO**
</dt> <dd> <dl> <dt>

1287 (0x507)
</dt> <dt>



Informazioni insufficienti per identificare la causa dell'errore.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**ERRORE \_ PARAMETRO \_ CRUNTIME NON \_ VALIDO**
</dt> <dd> <dl> <dt>

1288 (0x508)
</dt> <dt>



Il parametro passato a una funzione di runtime C non è corretto.


</dt> </dl> </dd> <dt>

<span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**ERRORE \_ OLTRE \_ VDL**
</dt> <dd> <dl> <dt>

1289 (0x509)
</dt> <dt>



L'operazione si è verificata oltre la lunghezza dei dati valida del file.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**ERRORE TIPO \_ DI \_ \_ SID SERVIZIO INCOMPATIBILE \_**
</dt> <dd> <dl> <dt>

1290 (0x50A)
</dt> <dt>



L'avvio del servizio non è riuscito perché uno o più servizi nello stesso processo hanno un'impostazione del tipo di SID del servizio incompatibile. Un servizio con tipo di SID del servizio con restrizioni può coesistere nello stesso processo solo con altri servizi con un tipo di SID con restrizioni. Se il tipo di SID del servizio per questo servizio è stato appena configurato, è necessario riavviare il processo di hosting per avviare il servizio.

In Windows Server 2003 e Windows XP, un servizio senza restrizioni non può coesistere nello stesso processo con altri servizi. Il servizio con il tipo di SID del servizio senza restrizioni deve essere spostato in un processo di proprietà per avviare il servizio.


</dt> </dl> </dd> <dt>

<span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**PROCESSO \_ DEL DRIVER DI ERRORE \_ \_ TERMINATO**
</dt> <dd> <dl> <dt>

1291 (0x50B)
</dt> <dt>



Il processo che ospita il driver per questo dispositivo è stato terminato.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**LIMITE \_ IMPLEMENTAZIONE \_ ERRORI**
</dt> <dd> <dl> <dt>

1292 (0x50C)
</dt> <dt>



Un'operazione ha tentato di superare un limite definito dall'implementazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**IL \_ PROCESSO DI ERRORE È \_ \_ PROTETTO**
</dt> <dd> <dl> <dt>

1293 (0x50D)
</dt> <dt>



Il processo di destinazione o il processo contenitore del thread di destinazione è un processo protetto.


</dt> </dl> </dd> <dt>

<span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**ERRORE \_ DEL SERVIZIO DI NOTIFICA DEL RITARDO \_ \_ DEL CLIENT \_**
</dt> <dd> <dl> <dt>

1294 (0x50E)
</dt> <dt>



Il client di notifica del servizio è troppo indietro rispetto allo stato corrente dei servizi nel computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**ERRORE \_ QUOTA \_ DISCO \_ SUPERATA**
</dt> <dd> <dl> <dt>

1295 (0x50F)
</dt> <dt>



L'operazione file richiesta non è riuscita perché è stata superata la quota di archiviazione. Per liberare spazio su disco, spostare i file in un percorso diverso o eliminare i file non necessari. Per altre informazioni, contattare l'amministratore di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**CONTENUTO \_ \_ DELL'ERRORE BLOCCATO**
</dt> <dd> <dl> <dt>

1296 (0x510)
</dt> <dt>



L'operazione di file richiesta non è riuscita perché i criteri di archiviazione bloccano il tipo di file. Per altre informazioni, contattare l'amministratore di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**ERRORE \_ PRIVILEGIO DEL \_ SERVIZIO INCOMPATIBILE \_**
</dt> <dd> <dl> <dt>

1297 (0x511)
</dt> <dt>



Un privilegio necessario per il corretto funzionamento del servizio non esiste nella configurazione dell'account del servizio. È possibile utilizzare lo snap-in Servizi Microsoft Management Console (MMC) (services.msc Impostazioni) e lo snap-in MMC (secpol.msc) per visualizzare la configurazione del servizio e la configurazione dell'account.


</dt> </dl> </dd> <dt>

<span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**ERRORE DI \_ BLOCCO \_ DELL'APP**
</dt> <dd> <dl> <dt>

1298 (0x512)
</dt> <dt>



Un thread coinvolto in questa operazione sembra non rispondere.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**ERRORE ETICHETTA \_ NON \_ VALIDA**
</dt> <dd> <dl> <dt>

1299 (0x513)
</dt> <dt>



Indica che un ID di sicurezza specifico non può essere assegnato come etichetta di un oggetto.


</dt> </dl> </dd> </dl>


## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Winerror</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di errore di sistema](system-error-codes.md)
</dt> </dl>

 

 




