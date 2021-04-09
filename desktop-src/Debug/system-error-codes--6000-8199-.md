---
description: Descrive i codici di errore 6000-8199 definiti nel file di intestazione WinError. h ed è destinato agli sviluppatori.
ms.assetid: eaaf9f65-e8ff-4e54-90a9-04252cdd773a
title: Codici di errore di sistema (6000-8199) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 0660009411224673481e9b65bcb62d7b194ab71f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878021"
---
# <a name="system-error-codes-6000-8199"></a>Codici di errore di sistema (6000-8199)

> [!NOTE]
> Queste informazioni sono destinate agli sviluppatori che effettuano il debug degli errori di sistema. Per altri errori, ad esempio problemi con Windows Update, è disponibile un elenco di risorse nella pagina [codici di errore](system-error-codes.md) .

Nell'elenco seguente vengono descritti i [codici di errore di sistema](system-error-codes.md) (errori da 6000 a 8199). Vengono restituiti dalla funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo. Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la funzione [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il **formato \_ Message from flag \_ di \_ sistema** .

<dl> <dt>

<span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**crittografia degli errori \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

6000 (0x1770)
</dt> <dt>



Impossibile crittografare il file specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**\_decrittografia errore \_ non riuscita**
</dt> <dd> <dl> <dt>

6001 (0x1771)
</dt> <dt>



Non è stato possibile decrittografare il file specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**FILE di errore \_ \_ crittografato**
</dt> <dd> <dl> <dt>

6002 (0x1772)
</dt> <dt>



Il file specificato è crittografato e l'utente non è in grado di decrittografarlo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**ERRORE \_ nessun \_ criterio di ripristino \_**
</dt> <dd> <dl> <dt>

6003 (0x1773)
</dt> <dt>



Non sono stati configurati criteri di recupero della crittografia validi per questo sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**ERRORE \_ senza \_ EFS**
</dt> <dd> <dl> <dt>

6004 (0x1774)
</dt> <dt>



Il driver di crittografia necessario non è stato caricato per questo sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**ERRORE \_ \_ EFS errato**
</dt> <dd> <dl> <dt>

6005 (0x1775)
</dt> <dt>



Il file è stato crittografato con un driver di crittografia diverso da quello attualmente caricato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**ERRORE \_ nessun \_ \_ tasto utente**
</dt> <dd> <dl> <dt>

6006 (0x1776)
</dt> <dt>



Non sono state definite chiavi EFS per l'utente.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**FILE di errore \_ \_ non \_ crittografato**
</dt> <dd> <dl> <dt>

6007 (0x1777)
</dt> <dt>



Il file specificato non è crittografato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**ERRORE \_ di \_ esportazione del \_ formato**
</dt> <dd> <dl> <dt>

6008 (0x1778)
</dt> <dt>



Il file specificato non è nel formato di esportazione EFS definito.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**FILE di errore di sola \_ \_ lettura \_**
</dt> <dd> <dl> <dt>

6009 (0x1779)
</dt> <dt>



Il file specificato è di sola lettura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**ERRORE \_ dir \_ non \_ consentito di EFS**
</dt> <dd> <dl> <dt>

6010 (0x177A)
</dt> <dt>



La directory è stata disabilitata per la crittografia.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**ERRORE \_ del \_ Server EFS \_ non \_ attendibile**
</dt> <dd> <dl> <dt>

6011 (0x177B)
</dt> <dt>



Il server non è considerato attendibile per l'operazione di crittografia remota.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**ERRORE \_ \_ criterio di recupero errato \_**
</dt> <dd> <dl> <dt>

6012 (0x177C)
</dt> <dt>



I criteri di ripristino configurati per questo sistema contengono un certificato di ripristino non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**ERRORE \_ EFS \_ ALG \_ BLOB \_ troppo \_ grande**
</dt> <dd> <dl> <dt>

6013 (0x177D)
</dt> <dt>



L'algoritmo di crittografia utilizzato nel file di origine richiede un buffer di chiave più grande rispetto a quello del file di destinazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**il \_ volume degli errori \_ non \_ supporta \_ EFS**
</dt> <dd> <dl> <dt>

6014 (0x177E)
</dt> <dt>



La partizione del disco non supporta la crittografia dei file.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**ERRORE \_ EFS \_ disabilitato**
</dt> <dd> <dl> <dt>

6015 (0x177F)
</dt> <dt>



Questo computer è disabilitato per la crittografia dei file.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**ERRORE \_ della \_ versione EFS \_ non \_ supportata**
</dt> <dd> <dl> <dt>

6016 (0x1780)
</dt> <dt>



Per decrittografare il file crittografato, è necessario un sistema più recente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**ERRORE \_ di \_ crittografia cs- \_ \_ risposta server non valida \_**
</dt> <dd> <dl> <dt>

6017 (0x1781)
</dt> <dt>



Il server remoto ha inviato una risposta non valida per un file aperto con la crittografia lato client.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**ERRORE \_ di \_ crittografia cs \_ Server non supportato \_**
</dt> <dd> <dl> <dt>

6018 (0x1782)
</dt> <dt>



La crittografia lato client non è supportata dal server remoto anche se attesta per supportarla.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**ERRORE \_ di \_ crittografia CS crittografia \_ esistente \_ file crittografato \_**
</dt> <dd> <dl> <dt>

6019 (0x1783)
</dt> <dt>



Il file è crittografato e deve essere aperto nella modalità di crittografia lato client.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**ERRORE \_ di \_ crittografia \_ cs \_ nuovo \_ file crittografato**
</dt> <dd> <dl> <dt>

6020 (0x1784)
</dt> <dt>



È in corso la creazione di un nuovo file crittografato ed è necessario fornire un $EFS.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**ERRORE \_ \_ file di crittografia cs \_ \_ non \_ CSE**
</dt> <dd> <dl> <dt>

6021 (0x1785)
</dt> <dt>



Il client SMB ha richiesto un FSCTL CSE in un file non CSE.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**il \_ criterio di crittografia degli errori \_ Nega l' \_ \_ operazione**
</dt> <dd> <dl> <dt>

6022 (0x1786)
</dt> <dt>



L'operazione richiesta è stata bloccata dai criteri. Per ulteriori informazioni, contattare l'amministratore di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**ERRORE \_ non sono stati \_ \_ trovati server browser \_**
</dt> <dd> <dl> <dt>

6118 (0x17E6)
</dt> <dt>



L'elenco dei server per questo gruppo di lavoro non è attualmente disponibile.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**Pianifica \_ E \_ servizio \_ non \_ LocalSystem**
</dt> <dd> <dl> <dt>

6200 (0x1838)
</dt> <dt>



Per il corretto funzionamento, è necessario configurare il servizio Utilità di pianificazione per l'esecuzione nell'account di sistema. Le singole attività possono essere configurate per l'esecuzione in altri account.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**\_settore log degli errori \_ \_ non valido**
</dt> <dd> <dl> <dt>

6600 (0x19C8)
</dt> <dt>



Il servizio di log ha rilevato un settore di log non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**\_parità di settore log degli errori \_ \_ \_ non valida**
</dt> <dd> <dl> <dt>

6601 (0x19C9)
</dt> <dt>



Il servizio di log ha rilevato un settore di log con parità di blocco non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**\_RImappato il settore log degli errori \_ \_**
</dt> <dd> <dl> <dt>

6602 (0x19CA)
</dt> <dt>



Il servizio di log ha rilevato un settore di log rimappato.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**blocco del log degli errori \_ \_ \_ incompleto**
</dt> <dd> <dl> <dt>

6603 (0x19CB)
</dt> <dt>



Il servizio di log ha rilevato un blocco di log parziale o incompleto.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**\_ \_ intervallo non valido per il log degli errori \_**
</dt> <dd> <dl> <dt>

6604 (0x19CC)
</dt> <dt>



Il servizio di log ha rilevato un tentativo di accesso ai dati al di fuori dell'intervallo di log attivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**\_blocchi log degli errori \_ \_ esauriti**
</dt> <dd> <dl> <dt>

6605 (0x19CD)
</dt> <dt>



I buffer di marshalling degli utenti del servizio di log sono esauriti.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**\_contesto di lettura log degli errori \_ \_ \_ non valido**
</dt> <dd> <dl> <dt>

6606 (0x19CE)
</dt> <dt>



Il servizio di log ha rilevato un tentativo di lettura da un'area di marshalling con un contesto di lettura non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**riavvio del log degli errori \_ \_ \_ non valido**
</dt> <dd> <dl> <dt>

6607 (0x19CF)
</dt> <dt>



Il servizio di log ha rilevato un'area di riavvio del log non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**\_versione del \_ blocco del log degli errori \_**
</dt> <dd> <dl> <dt>

6608 (0x19D0)
</dt> <dt>



Il servizio di log ha rilevato una versione non valida del blocco del log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**blocco del log degli errori \_ \_ \_ non valido**
</dt> <dd> <dl> <dt>

6609 (0x19D1)
</dt> <dt>



Il servizio di log ha rilevato un blocco del log non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**\_modalità di lettura log degli errori \_ \_ \_ non valida**
</dt> <dd> <dl> <dt>

6610 (0x19D2)
</dt> <dt>



Il servizio di log ha rilevato un tentativo di lettura del log con una modalità di lettura non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**LOG degli errori \_ \_ senza \_ riavvio**
</dt> <dd> <dl> <dt>

6611 (0x19D3)
</dt> <dt>



Il servizio di log ha rilevato un flusso di log senza area di riavvio.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**metadati del log degli errori \_ \_ \_ danneggiati**
</dt> <dd> <dl> <dt>

6612 (0x19D4)
</dt> <dt>



Il servizio di log ha rilevato un file di metadati danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**metadati del log degli errori \_ \_ \_ non validi**
</dt> <dd> <dl> <dt>

6613 (0x19D5)
</dt> <dt>



Il servizio di log ha rilevato un file di metadati che non è stato possibile creare tramite il file system di log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**metadati del log degli errori \_ \_ \_ incoerenti**
</dt> <dd> <dl> <dt>

6614 (0x19D6)
</dt> <dt>



Il servizio di log ha rilevato un file di metadati con dati incoerenti.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**\_prenotazione log degli errori \_ \_ non valida**
</dt> <dd> <dl> <dt>

6615 (0x19D7)
</dt> <dt>



Il servizio di log ha rilevato un tentativo di allocare o eliminare uno spazio di prenotazione errato.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**\_ \_ Impossibile eliminare il log degli errori \_**
</dt> <dd> <dl> <dt>

6616 (0x19D8)
</dt> <dt>



Il servizio log non è in grado di eliminare il file di log o il contenitore file system


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**limite del contenitore del log degli errori \_ \_ \_ \_ superato**
</dt> <dd> <dl> <dt>

6617 (0x19D9)
</dt> <dt>



Il servizio di log ha raggiunto il numero massimo consentito di contenitori allocati a un file di log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**\_inizio log \_ degli errori \_ di \_ log**
</dt> <dd> <dl> <dt>

6618 (0x19DA)
</dt> <dt>



Il servizio di log ha eseguito un tentativo di lettura o scrittura indietro oltre l'inizio del log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**criterio del log degli errori \_ \_ \_ già \_ installato**
</dt> <dd> <dl> <dt>

6619 (0x19DB)
</dt> <dt>



Impossibile installare i criteri di log perché è già presente un criterio dello stesso tipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**criterio del log degli errori \_ \_ \_ non \_ installato**
</dt> <dd> <dl> <dt>

6620 (0x19DC)
</dt> <dt>



Il criterio di log in questione non è stato installato al momento della richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**criterio del log degli errori \_ \_ \_ non valido**
</dt> <dd> <dl> <dt>

6621 (0x19DD)
</dt> <dt>



Il set di criteri installato nel log non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**\_conflitto del \_ criterio del log degli errori \_**
</dt> <dd> <dl> <dt>

6622 (0x19DE)
</dt> <dt>



Un criterio per il log in questione ha impedito il completamento dell'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**\_coda di \_ \_ archiviazione bloccata nel log \_ degli errori**
</dt> <dd> <dl> <dt>

6623 (0x19DF)
</dt> <dt>



Non è possibile recuperare lo spazio del log perché il log è bloccato dalla coda di archiviazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**RECORD del log degli errori \_ \_ \_ inesistente**
</dt> <dd> <dl> <dt>

6624 (0x19E0)
</dt> <dt>



Il record del log non è un record nel file di log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**record del log degli errori \_ \_ \_ riservati \_ non validi**
</dt> <dd> <dl> <dt>

6625 (0x19E1)
</dt> <dt>



Il numero di record di log riservati o la modifica del numero di record di log riservati non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**spazio del log degli errori \_ \_ \_ riservato \_ non valido**
</dt> <dd> <dl> <dt>

6626 (0x19E2)
</dt> <dt>



Lo spazio del log riservato o la modifica dello spazio del log non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**coda del log degli errori \_ \_ \_ non valida**
</dt> <dd> <dl> <dt>

6627 (0x19E3)
</dt> <dt>



Una coda o una base di archivio nuova o esistente del log attivo non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**LOG degli errori \_ \_ completo**
</dt> <dd> <dl> <dt>

6628 (0x19E4)
</dt> <dt>



Lo spazio del log è esaurito.


</dt> </dl> </dd> <dt>

<span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**errore durante il \_ \_ \_ ridimensionamento del \_ log**
</dt> <dd> <dl> <dt>

6629 (0x19E5)
</dt> <dt>



Impossibile impostare il log sulla dimensione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**LOG degli errori \_ \_ multiplexed**
</dt> <dd> <dl> <dt>

6630 (0x19E6)
</dt> <dt>



Il log è multiplexato, non sono consentite Scritture dirette nel log fisico.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**LOG degli errori \_ \_ dedicato**
</dt> <dd> <dl> <dt>

6631 (0x19E7)
</dt> <dt>



L'operazione non è riuscita perché il log è un log dedicato.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**\_archivio log degli errori \_ \_ non \_ in \_ corso**
</dt> <dd> <dl> <dt>

6632 (0x19E8)
</dt> <dt>



Per l'operazione è necessario un contesto di archiviazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**\_archivio log degli errori \_ \_ in \_ corso**
</dt> <dd> <dl> <dt>

6633 (0x19E9)
</dt> <dt>



Archiviazione del log in corso.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**LOG degli errori \_ \_ effimero**
</dt> <dd> <dl> <dt>

6634 (0x19EA)
</dt> <dt>



Per l'operazione è necessario un log non temporaneo, ma il log è temporaneo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**LOG degli errori \_ \_ non sufficiente per i \_ \_ contenitori**
</dt> <dd> <dl> <dt>

6635 (0x19EB)
</dt> <dt>



Il log deve avere almeno due contenitori per poter essere letto o scritto.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**\_client log degli errori \_ \_ già \_ registrato**
</dt> <dd> <dl> <dt>

6636 (0x19EC)
</dt> <dt>



Un client di log è già registrato nel flusso.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**\_client log degli errori \_ \_ non \_ registrato**
</dt> <dd> <dl> <dt>

6637 (0x19ED)
</dt> <dt>



Un client di log non è stato registrato nel flusso.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**\_gestore completo log degli errori \_ \_ \_ in \_ corso**
</dt> <dd> <dl> <dt>

6638 (0x19EE)
</dt> <dt>



È già stata effettuata una richiesta per gestire la condizione di log full.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**lettura del contenitore del log degli errori \_ \_ \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

6639 (0x19EF)
</dt> <dt>



Si è verificato un errore del servizio log durante il tentativo di lettura da un contenitore di log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**scrittura del contenitore del log degli errori \_ \_ \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

6640 (0x19F0)
</dt> <dt>



Il servizio di log ha rilevato un errore durante il tentativo di scrittura in un contenitore di log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**apertura del contenitore del log degli errori \_ \_ \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

6641 (0x19F1)
</dt> <dt>



Si è verificato un errore del servizio log durante il tentativo di aprire un contenitore di log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**stato del contenitore del log degli errori \_ \_ \_ \_ non valido**
</dt> <dd> <dl> <dt>

6642 (0x19F2)
</dt> <dt>



Il servizio di log ha rilevato uno stato del contenitore non valido quando si tenta di eseguire un'azione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**stato del log degli errori \_ \_ \_ non valido**
</dt> <dd> <dl> <dt>

6643 (0x19F3)
</dt> <dt>



Il servizio di log non è nello stato corretto per eseguire un'azione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**LOG degli errori \_ \_ aggiunto**
</dt> <dd> <dl> <dt>

6644 (0x19F4)
</dt> <dt>



Non è possibile recuperare lo spazio del log perché il log è bloccato.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**\_scaricamento metadati del log degli errori \_ \_ \_ non riuscito**
</dt> <dd> <dl> <dt>

6645 (0x19F5)
</dt> <dt>



Scaricamento metadati del log non riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**\_ \_ sicurezza incoerente log degli errori \_**
</dt> <dd> <dl> <dt>

6646 (0x19F6)
</dt> <dt>



La sicurezza nel log e nei relativi contenitori è incoerente.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**svuotamento del log degli errori \_ \_ accodato \_ \_ non riuscito**
</dt> <dd> <dl> <dt>

6647 (0x19F7)
</dt> <dt>



I record sono stati accodati al log o sono state apportate modifiche alla prenotazione, ma non è stato possibile scaricare il log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**\_ \_ prenotazione bloccata log degli errori \_**
</dt> <dd> <dl> <dt>

6648 (0x19F8)
</dt> <dt>



Il log è bloccato a causa di una prenotazione che utilizza la maggior parte dello spazio di log. Liberare alcuni record riservati per rendere disponibile spazio.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**ERRORE \_ transazione non valida \_**
</dt> <dd> <dl> <dt>

6700 (0x1A2C)
</dt> <dt>



L'handle di transazione associato a questa operazione non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**transazione di errore \_ \_ non \_ attiva**
</dt> <dd> <dl> <dt>

6701 (0x1A2D)
</dt> <dt>



L'operazione richiesta è stata eseguita nel contesto di una transazione che non è più attiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**\_richiesta transazione di errore \_ \_ non \_ valida**
</dt> <dd> <dl> <dt>

6702 (0x1A2E)
</dt> <dt>



L'operazione richiesta non è valida per l'oggetto transazione nello stato corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**transazione di errore \_ \_ non \_ richiesta**
</dt> <dd> <dl> <dt>

6703 (0x1A2F)
</dt> <dt>



Il chiamante ha chiamato un'API di risposta, ma la risposta non è prevista perché la TM non ha emesso la richiesta corrispondente al chiamante.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**transazione di errore \_ \_ già \_ interrotta**
</dt> <dd> <dl> <dt>

6704 (0x1A30)
</dt> <dt>



È troppo tardi per eseguire l'operazione richiesta, perché la transazione è già stata interrotta.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**transazione di errore già sottoposta a \_ \_ \_ commit**
</dt> <dd> <dl> <dt>

6705 (0x1A31)
</dt> <dt>



È troppo tardi per eseguire l'operazione richiesta, perché è già stato eseguito il commit della transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**\_ \_ inizializzazione TM errore \_ non riuscita**
</dt> <dd> <dl> <dt>

6706 (0x1A32)
</dt> <dt>



Impossibile inizializzare la gestione transazioni. Le operazioni transazionali non sono supportate.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**ERRORE \_ RESOURCEMANAGER di \_ sola lettura \_**
</dt> <dd> <dl> <dt>

6707 (0x1A33)
</dt> <dt>



Il ResourceManager specificato non ha apportato modifiche o aggiornamenti alla risorsa in questa transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**transazione di errore \_ \_ non \_ unita in join**
</dt> <dd> <dl> <dt>

6708 (0x1A34)
</dt> <dt>



Resource Manager ha tentato di preparare una transazione a cui non è stato aggiunto correttamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**ERRORE di \_ transazione \_ superiore \_ esistente**
</dt> <dd> <dl> <dt>

6709 (0x1A35)
</dt> <dt>



L'oggetto transazione dispone già di un elenco superiore e il chiamante ha tentato di eseguire un'operazione che avrebbe creato un nuovo livello superiore. È consentita solo una singola integrazione superiore.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**il \_ protocollo CRM con errori \_ \_ \_ esiste già**
</dt> <dd> <dl> <dt>

6710 (0x1A36)
</dt> <dt>



Il RM ha tentato di registrare un protocollo già esistente.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**ERRORE \_ \_ propagazione transazioni \_ non riuscita**
</dt> <dd> <dl> <dt>

6711 (0x1A37)
</dt> <dt>



Il tentativo di propagare la transazione non è riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**ERRORE \_ del \_ protocollo CRM \_ non \_ trovato**
</dt> <dd> <dl> <dt>

6712 (0x1A38)
</dt> <dt>



Il protocollo di propagazione richiesto non è stato registrato come CRM.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**ERRORE di \_ transazione del \_ \_ buffer Marshall non valido \_**
</dt> <dd> <dl> <dt>

6713 (0x1A39)
</dt> <dt>



Il buffer passato a PushTransaction o PullTransaction non è in un formato valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**ERRORE \_ \_ transazione corrente \_ non \_ valida**
</dt> <dd> <dl> <dt>

6714 (0x1A3A)
</dt> <dt>



Il contesto di transazione corrente associato al thread non è un handle valido per un oggetto transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**transazione di errore \_ \_ non \_ trovata**
</dt> <dd> <dl> <dt>

6715 (0x1A3B)
</dt> <dt>



Impossibile aprire l'oggetto transazione specificato perché non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**ERRORE \_ RESOURCEMANAGER \_ non \_ trovato**
</dt> <dd> <dl> <dt>

6716 (0x1A3C)
</dt> <dt>



Non è stato possibile aprire l'oggetto ResourceManager specificato perché non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**\_ \_ Impossibile trovare l'elenco errori \_**
</dt> <dd> <dl> <dt>

6717 (0x1A3D)
</dt> <dt>



Non è stato possibile aprire l'oggetto di integrazione specificato perché non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**ERRORE \_ TRANSACTIONMANAGER \_ non \_ trovato**
</dt> <dd> <dl> <dt>

6718 (0x1A3E)
</dt> <dt>



Non è stato possibile aprire l'oggetto TransactionManager specificato perché non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**ERRORE \_ TRANSACTIONMANAGER \_ non in \_ linea**
</dt> <dd> <dl> <dt>

6719 (0x1A3F)
</dt> <dt>



Impossibile creare o aprire l'oggetto specificato perché il TransactionManager associato non è online. TransactionManager deve essere portato completamente online chiamando RecoverTransactionManager per il ripristino fino alla fine del relativo file di log prima di poter aprire gli oggetti nella relativa transazione o negli spazi dei nomi ResourceManager. Inoltre, gli errori di scrittura dei record nel file di log possono causare la disconnessione di un TransactionManager.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**ERRORE \_ TRANSACTIONMANAGER il \_ ripristino del \_ nome \_**
</dt> <dd> <dl> <dt>

6720 (0x1A40)
</dt> <dt>



Il TransactionManager specificato non è riuscito a creare gli oggetti contenuti nel file di log nello spazio dei nomi ob. Di conseguenza, TransactionManager non è stato in grado di recuperare.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**transazione di errore \_ \_ non \_ radice**
</dt> <dd> <dl> <dt>

6721 (0x1A41)
</dt> <dt>



Non è stato possibile completare la chiamata per creare un'integrazione superiore in questo oggetto transazione perché l'oggetto transazione specificato per l'integrazione è un ramo subordinato della transazione. Solo la radice della transazione può essere integrata come superiore.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**\_oggetto transazione \_ errore \_ scaduto**
</dt> <dd> <dl> <dt>

6722 (0x1A42)
</dt> <dt>



Poiché la gestione transazioni associata o Resource Manager è stato chiuso, l'handle non è più valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**\_risposta transazione di errore \_ \_ non \_ integrata**
</dt> <dd> <dl> <dt>

6723 (0x1A43)
</dt> <dt>



Non è stato possibile eseguire l'operazione specificata in questa integrazione superiore perché l'integrazione non è stata creata con la risposta di completamento corrispondente in NotificationMask.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**\_record transazioni \_ errore \_ troppo \_ lungo**
</dt> <dd> <dl> <dt>

6724 (0x1A44)
</dt> <dt>



Non è stato possibile eseguire l'operazione specificata perché il record che verrebbe registrato era troppo lungo. Questo problema può verificarsi a causa di due condizioni: sono presenti troppe integrazioni in questa transazione o il RecoveryInformation combinato per conto di tali integrazioni è troppo lungo.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**\_transazione implicita errore \_ \_ non \_ supportata**
</dt> <dd> <dl> <dt>

6725 (0x1A45)
</dt> <dt>



Transazione implicita non supportata.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**ERRORE \_ di \_ integrità transazioni \_ violato**
</dt> <dd> <dl> <dt>

6726 (0x1A46)
</dt> <dt>



Il gestore delle transazioni kernel ha dovuto interrompere o dimenticare la transazione perché blocca lo stato di avanzamento.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**ERRORE \_ TRANSACTIONMANAGER \_ identità non \_ corrispondente**
</dt> <dd> <dl> <dt>

6727 (0x1A47)
</dt> <dt>



L'identità TransactionManager fornita non corrisponde a quella registrata nel file di log di TransactionManager.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**ERRORE \_ RM \_ non può \_ essere \_ bloccato per lo \_ \_ snapshot**
</dt> <dd> <dl> <dt>

6728 (0x1A48)
</dt> <dt>



Questa operazione di snapshot non può continuare perché un gestore di risorse transazionale non può essere bloccato nello stato corrente. Riprova.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**la \_ transazione di errore \_ deve \_ WRITETHROUGH**
</dt> <dd> <dl> <dt>

6729 (0x1A49)
</dt> <dt>



La transazione non può essere integrata con il EnlistmentMask specificato, perché la transazione ha già completato la fase di prepreparazione. Per garantire la correttezza, ResourceManager deve passare a una modalità Write-through e interrompere la memorizzazione nella cache dei dati all'interno di questa transazione. L'integrazione solo per le fasi successive delle transazioni può comunque avere esito positivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**transazione di errore \_ \_ non \_ superiore**
</dt> <dd> <dl> <dt>

6730 (0x1A4A)
</dt> <dt>



La transazione non ha un elenco superiore.


</dt> </dl> </dd> <dt>

<span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**ERRORE \_ euristico di errore \_ \_ possibile**
</dt> <dd> <dl> <dt>

6731 (0x1A4B)
</dt> <dt>



Il tentativo di eseguire il commit della transazione è stato completato, ma è possibile che non sia stato eseguito il commit di una parte dell'albero delle transazioni a causa dell'euristica. È pertanto possibile che alcuni dati modificati nella transazione non abbiano eseguito il commit, causando un'incoerenza transazionale. Se possibile, verificare la coerenza dei dati associati.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**ERRORE di \_ transazione TRANSazionale \_**
</dt> <dd> <dl> <dt>

6800 (0x1A90)
</dt> <dt>



La funzione ha tentato di utilizzare un nome riservato per l'utilizzo da parte di un'altra transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**ERRORE \_ RM \_ non \_ attivo**
</dt> <dd> <dl> <dt>

6801 (0x1A91)
</dt> <dt>



Il supporto delle transazioni all'interno del gestore di risorse specificato non è stato avviato o è stato arrestato a causa di un errore.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**ERRORE \_ \_ dei metadati RM \_ danneggiati**
</dt> <dd> <dl> <dt>

6802 (0x1A92)
</dt> <dt>



I metadati di RM sono stati danneggiati. RM non funzionerà.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**Directory degli errori \_ \_ non \_ RM**
</dt> <dd> <dl> <dt>

6803 (0x1A93)
</dt> <dt>



La directory specificata non contiene un gestore di risorse.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**transazioni di errore \_ \_ remote non supportate \_**
</dt> <dd> <dl> <dt>

6805 (0x1A95)
</dt> <dt>



Il server o la condivisione remota non supporta le operazioni di file transazionali.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**dimensioni del log degli errori \_ \_ \_ non valide \_**
</dt> <dd> <dl> <dt>

6806 (0x1A96)
</dt> <dt>



Dimensioni del log richieste non valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**\_oggetto errore \_ non \_ più \_ esistente**
</dt> <dd> <dl> <dt>

6807 (0x1A97)
</dt> <dt>



L'oggetto (file, flusso, collegamento) corrispondente all'handle è stato eliminato da un rollback della transazione salvataggio.


</dt> </dl> </dd> <dt>

<span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**\_ \_ \_ Impossibile trovare il flusso di errore miniversione \_**
</dt> <dd> <dl> <dt>

6808 (0x1A98)
</dt> <dt>



Impossibile trovare il file specificato miniversione per il file transazionale aperto.


</dt> </dl> </dd> <dt>

<span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**il \_ flusso di errore \_ miniversione \_ non è \_ valido**
</dt> <dd> <dl> <dt>

6809 (0x1A99)
</dt> <dt>



Il file specificato miniversione è stato trovato ma è stato invalidato. La causa più probabile è il rollback della transazione salvataggio.


</dt> </dl> </dd> <dt>

<span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**ERRORE \_ miniversione \_ inaccessibile \_ dalla \_ \_ transazione specificata**
</dt> <dd> <dl> <dt>

6810 (0x1A9A)
</dt> <dt>



Un miniversione può essere aperto solo nel contesto della transazione che l'ha creata.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**errore durante l' \_ \_ apertura \_ \_ di miniversione con \_ modifica \_ finalità**
</dt> <dd> <dl> <dt>

6811 (0x1A9B)
</dt> <dt>



Non è possibile aprire un miniversione con modifica accesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**errore durante la creazione di un \_ \_ \_ altro \_ flusso \_ miniversioni**
</dt> <dd> <dl> <dt>

6812 (0x1A9C)
</dt> <dt>



Non è possibile creare altri miniversioni per questo flusso.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**ERRORE \_ di \_ versione del file remoto non \_ \_ corrispondente**
</dt> <dd> <dl> <dt>

6814 (0x1A9E)
</dt> <dt>



Il server remoto ha inviato un numero di versione o un FID non corrispondente per un file aperto con le transazioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**HANDLE di errore \_ \_ non \_ più \_ valido**
</dt> <dd> <dl> <dt>

6815 (0x1A9F)
</dt> <dt>



L'handle è stato invalidato da una transazione. La causa più probabile è la presenza di un mapping di memoria su un file o un handle aperto quando la transazione è terminata o ne è stato eseguito il rollback a salvataggio.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**ERRORE \_ nessun \_ \_ metadati TXF**
</dt> <dd> <dl> <dt>

6816 (0x1AA0)
</dt> <dt>



Non sono presenti metadati di transazione per il file.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**\_ \_ rilevato danneggiamento del log degli errori \_**
</dt> <dd> <dl> <dt>

6817 (0x1AA1)
</dt> <dt>



I dati del log sono danneggiati.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**errore durante il \_ \_ ripristino \_ con \_ handle \_ aperto**
</dt> <dd> <dl> <dt>

6818 (0x1AA2)
</dt> <dt>



Il file non può essere recuperato perché è ancora aperto un handle.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**ERRORE \_ RM \_ disconnesso**
</dt> <dd> <dl> <dt>

6819 (0x1AA3)
</dt> <dt>



Il risultato della transazione non è disponibile perché il gestore di risorse è stato disconnesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**\_Elenco errori \_ non \_ superiore**
</dt> <dd> <dl> <dt>

6820 (0x1AA4)
</dt> <dt>



La richiesta è stata rifiutata perché l'integrazione in questione non è un elenco superiore.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**\_Ripristino errori \_ non \_ necessario**
</dt> <dd> <dl> <dt>

6821 (0x1AA5)
</dt> <dt>



Il gestore di risorse transazionale è già coerente. Il ripristino non è necessario.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**ERRORE \_ RM \_ già \_ avviato**
</dt> <dd> <dl> <dt>

6822 (0x1AA6)
</dt> <dt>



Il gestore di risorse transazionale è già stato avviato.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**\_identità file di errore \_ \_ non \_ persistente**
</dt> <dd> <dl> <dt>

6823 (0x1AA7)
</dt> <dt>



Il file non può essere aperto in modo transazionale, perché la relativa identità dipende dal risultato di una transazione non risolta.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**errore durante la \_ \_ \_ dipendenza transazionale \_**
</dt> <dd> <dl> <dt>

6824 (0x1AA8)
</dt> <dt>



Non è possibile eseguire l'operazione perché un'altra transazione dipende dal fatto che questa proprietà non verrà modificata.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**ERRORE \_ di \_ limite incrociato tra \_ RM \_**
</dt> <dd> <dl> <dt>

6825 (0x1AA9)
</dt> <dt>



L'operazione comporterebbe un singolo file con due gestori di risorse transazionali e pertanto non è consentito.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**ERRORE \_ TXF \_ dir \_ non \_ vuoto**
</dt> <dd> <dl> <dt>

6826 (0x1AAA)
</dt> <dt>



Per eseguire questa operazione, è necessario che la directory $Txf sia vuota.


</dt> </dl> </dd> <dt>

<span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**sono \_ presenti transazioni INdubbie sull'errore \_ \_**
</dt> <dd> <dl> <dt>

6827 (0x1AAB)
</dt> <dt>



L'operazione lascia un gestore di risorse transazionale in uno stato incoerente e pertanto non è consentito.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**ERRORE \_ TM \_ volatile**
</dt> <dd> <dl> <dt>

6828 (0x1AAC)
</dt> <dt>



Non è stato possibile completare l'operazione perché la gestione transazioni non contiene un log.


</dt> </dl> </dd> <dt>

<span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**ERRORE di \_ rollback \_ timer \_ scaduto**
</dt> <dd> <dl> <dt>

6829 (0x1AAD)
</dt> <dt>



Non è stato possibile pianificare un rollback perché un rollback pianificato in precedenza è già stato eseguito o è stato accodato per l'esecuzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**ERRORE \_ TXF \_ attributo \_ danneggiato**
</dt> <dd> <dl> <dt>

6830 (0x1AAE)
</dt> <dt>



L'attributo transazionale dei metadati nel file o nella directory è danneggiato e illeggibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**ERRORE \_ EFS \_ non \_ consentito \_ nella \_ transazione**
</dt> <dd> <dl> <dt>

6831 (0x1AAF)
</dt> <dt>



Non è stato possibile completare l'operazione di crittografia perché è attiva una transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**ERRORE di \_ apertura TRANSazionale \_ \_ non \_ consentito**
</dt> <dd> <dl> <dt>

6832 (0x1AB0)
</dt> <dt>



Questo oggetto non può essere aperto in una transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**\_crescita log degli errori \_ \_ non riuscita**
</dt> <dd> <dl> <dt>

6833 (0x1AB1)
</dt> <dt>



Il tentativo di creare lo spazio nel log di Transactional Resource Manager non è riuscito. Lo stato di errore è stato registrato nel registro eventi.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**ERRORE di \_ mapping transazionale non \_ \_ supportato \_**
</dt> <dd> <dl> <dt>

6834 (0x1AB2)
</dt> <dt>



Mapping di memoria (creazione di una sezione mappata) un file remoto in una transazione non è supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**ERRORE \_ TXF \_ metadati \_ già \_ presenti**
</dt> <dd> <dl> <dt>

6835 (0x1AB3)
</dt> <dt>



I metadati della transazione sono già presenti nel file e non possono essere sostituiti.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**callback dell'ambito della transazione di errore \_ \_ \_ \_ non \_ impostati**
</dt> <dd> <dl> <dt>

6836 (0x1AB4)
</dt> <dt>



Impossibile immettere un ambito di transazione perché il gestore dell'ambito non è stato inizializzato.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**\_Promozione della transazione di errore \_ obbligatoria \_**
</dt> <dd> <dl> <dt>

6837 (0x1AB5)
</dt> <dt>



La promozione è stata necessaria per consentire l'integrazione di Resource Manager, ma la transazione è stata impostata in modo da non consentirla.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**ERRORE \_ non è possibile \_ eseguire il \_ file \_ nella \_ transazione**
</dt> <dd> <dl> <dt>

6838 (0x1AB6)
</dt> <dt>



Questo file è aperto per la modifica in una transazione non risolta e può essere aperto per l'esecuzione solo da un lettore transazionale.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**transazioni di errore \_ \_ non \_ bloccate**
</dt> <dd> <dl> <dt>

6839 (0x1AB7)
</dt> <dt>



La richiesta di scongelamento delle transazioni bloccate è stata ignorata perché le transazioni non erano state precedentemente bloccate.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**ERRORE \_ \_ blocco transazioni \_ in \_ corso**
</dt> <dd> <dl> <dt>

6840 (0x1AB8)
</dt> <dt>



Le transazioni non possono essere bloccate perché è già in corso un blocco.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**ERRORE \_ non \_ \_ volume snapshot**
</dt> <dd> <dl> <dt>

6841 (0x1AB9)
</dt> <dt>



Il volume di destinazione non è un volume snapshot. Questa operazione è valida solo su un volume montato come snapshot.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**ERRORE \_ nessun \_ salvataggio \_ con \_ \_ file aperti**
</dt> <dd> <dl> <dt>

6842 (0x1ABA)
</dt> <dt>



L'operazione salvataggio non è riuscita perché i file sono aperti nella transazione. Questa operazione non è consentita.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**\_ripristino dati di errore \_ perso \_**
</dt> <dd> <dl> <dt>

6843 (0x1ABB)
</dt> <dt>



Windows ha individuato un danneggiamento in un file e il file è stato ripristinato. Potrebbe essersi verificata una perdita di dati.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**ERRORE \_ sparse \_ non \_ consentito \_ nella \_ transazione**
</dt> <dd> <dl> <dt>

6844 (0x1ABC)
</dt> <dt>



Non è stato possibile completare l'operazione di tipo sparse perché una transazione è attiva sul file.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**ERRORE \_ TM \_ identità non \_ corrispondente**
</dt> <dd> <dl> <dt>

6845 (0x1ABD)
</dt> <dt>



La chiamata per la creazione di un oggetto TransactionManager non è riuscita perché l'identità TM archiviata nel file di log non corrisponde all'identità TM passata come argomento.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**sezione con errore \_ Floated \_**
</dt> <dd> <dl> <dt>

6846 (0x1ABE)
</dt> <dt>



Si è tentato di eseguire operazioni di I/O su un oggetto Section che è stato spostato a causa di una transazione che termina. Nessun dato valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**ERRORE \_ non può \_ accettare il \_ lavoro transazionale \_**
</dt> <dd> <dl> <dt>

6847 (0x1ABF)
</dt> <dt>



Il gestore di risorse transazionale non è attualmente in grado di accettare il lavoro transazionale a causa di una condizione temporanea, ad esempio risorse insufficienti.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**ERRORE \_ non è possibile \_ interrompere \_ le transazioni**
</dt> <dd> <dl> <dt>

6848 (0x1AC0)
</dt> <dt>



Il gestore di risorse transazionale ha troppi transazioni in attesa che non possono essere interrotti. Il gestore di risorse transazionale è stato arrestato.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**ERRORI \_ di \_ cluster danneggiati**
</dt> <dd> <dl> <dt>

6849 (0x1AC1)
</dt> <dt>



Non è stato possibile completare l'operazione a causa di cluster danneggiati sul disco.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**compressione degli errori \_ \_ non \_ consentita \_ nella \_ transazione**
</dt> <dd> <dl> <dt>

6850 (0x1AC2)
</dt> <dt>



Non è stato possibile completare l'operazione di compressione perché nel file è attiva una transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**VOLUME di errore \_ \_ Dirty**
</dt> <dd> <dl> <dt>

6851 (0x1AC3)
</dt> <dt>



Non è stato possibile completare l'operazione perché il volume è modificato. Eseguire CHKDSK e riprovare.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**ERRORE \_ nessun \_ rilevamento dei collegamenti \_ \_ nella \_ transazione**
</dt> <dd> <dl> <dt>

6852 (0x1AC4)
</dt> <dt>



Non è stato possibile completare l'operazione di rilevamento dei collegamenti perché è attiva una transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**\_operazione \_ di errore non \_ supportata \_ nella \_ transazione**
</dt> <dd> <dl> <dt>

6853 (0x1AC5)
</dt> <dt>



Questa operazione non può essere eseguita in una transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**HANDLE di errore \_ scaduto \_**
</dt> <dd> <dl> <dt>

6854 (0x1AC6)
</dt> <dt>



L'handle non è più associato correttamente alla relativa transazione. Potrebbe essere stata aperta in un gestore di risorse transazionale che in seguito è stato forzato a riavviare. Chiudere l'handle e aprirne uno nuovo.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**transazione di errore \_ \_ non \_ integrata**
</dt> <dd> <dl> <dt>

6855 (0x1AC7)
</dt> <dt>



Non è stato possibile eseguire l'operazione specificata perché Resource Manager non è integrato nella transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**ERRORE \_ ctx \_ WINSTATION \_ nome \_ non valido**
</dt> <dd> <dl> <dt>

7001 (0x1B59)
</dt> <dt>



Il nome della sessione specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**ERRORE \_ ctx \_ non valido \_**
</dt> <dd> <dl> <dt>

7002 (0x1B5A)
</dt> <dt>



Il driver di protocollo specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**ERRORE \_ ctx \_ PD \_ non \_ trovato**
</dt> <dd> <dl> <dt>

7003 (0x1B5B)
</dt> <dt>



Il driver di protocollo specificato non è stato trovato nel percorso di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**ERRORE \_ ctx \_ WD \_ non \_ trovato**
</dt> <dd> <dl> <dt>

7004 (0x1B5C)
</dt> <dt>



Il driver della connessione terminal specificato non è stato trovato nel percorso di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**ERRORE \_ ctx \_ Impossibile \_ creare la \_ voce del log eventi \_**
</dt> <dd> <dl> <dt>

7005 (0x1B5D)
</dt> <dt>



Non è stato possibile creare una chiave del registro di sistema per la registrazione eventi per questa sessione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**ERRORE \_ ctx \_ nome servizio in \_ \_ conflitto**
</dt> <dd> <dl> <dt>

7006 (0x1B5E)
</dt> <dt>



Nel sistema esiste già un servizio con lo stesso nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**ERRORE \_ ctx di \_ chiusura \_ in sospeso**
</dt> <dd> <dl> <dt>

7007 (0x1B5F)
</dt> <dt>



Operazione di chiusura in sospeso per la sessione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**ERRORE \_ ctx \_ nessun \_ OUTBUF**
</dt> <dd> <dl> <dt>

7008 (0x1B60)
</dt> <dt>



Non sono disponibili buffer di output gratuiti.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**ERRORE \_ ctx \_ modem \_ inf \_ non \_ trovato**
</dt> <dd> <dl> <dt>

7009 (0x1B61)
</dt> <dt>



MODEM. Il file INF non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**ERRORE \_ ctx \_ . \_ modem non valido**
</dt> <dd> <dl> <dt>

7010 (0x1B62)
</dt> <dt>



Il nome del modem non è stato trovato in MODEM. INF.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**errore \_ di \_ risposta del modem CTX \_ \_**
</dt> <dd> <dl> <dt>

7011 (0x1B63)
</dt> <dt>



Il modem non ha accettato il comando inviato. Verificare che il nome del modem configurato corrisponda al modem collegato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**ERRORE \_ ctx \_ \_ risposta modem \_ timeout**
</dt> <dd> <dl> <dt>

7012 (0x1B64)
</dt> <dt>



Il modem non ha risposto al comando inviato. Verificare che il modem sia cablato e acceso correttamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**ERRORE \_ di \_ risposta modem CTX \_ \_ senza \_ gestore**
</dt> <dd> <dl> <dt>

7013 (0x1B65)
</dt> <dt>



Il rilevamento del vettore non è riuscito o il vettore è stato eliminato a causa di una disconnessione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**ERRORE \_ ctx \_ modem \_ risposta \_ senza \_ Dialtone**
</dt> <dd> <dl> <dt>

7014 (0x1B66)
</dt> <dt>



Il tono di connessione non è stato rilevato entro il tempo richiesto. Verificare che il cavo telefonico sia correttamente collegato e funzionante.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**ERRORE \_ ctx \_ \_ risposta modem \_ occupato**
</dt> <dd> <dl> <dt>

7015 (0x1B67)
</dt> <dt>



Segnale occupato rilevato nel sito remoto sul callback.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**ERRORE \_ ctx \_ \_ risposta modem \_ voce**
</dt> <dd> <dl> <dt>

7016 (0x1B68)
</dt> <dt>



Voce rilevata nel sito remoto su callback.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**errore \_ ctx \_ TD \_**
</dt> <dd> <dl> <dt>

7017 (0x1B69)
</dt> <dt>



Errore del driver di trasporto.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**ERRORE \_ ctx \_ WINSTATION \_ non \_ trovato**
</dt> <dd> <dl> <dt>

7022 (0x1B6E)
</dt> <dt>



Impossibile trovare la sessione specificata.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**ERRORE \_ ctx \_ WINSTATION \_ già \_ esistente**
</dt> <dd> <dl> <dt>

7023 (0x1B6F)
</dt> <dt>



Il nome della sessione specificato è già in uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**ERRORE \_ ctx \_ WINSTATION \_ occupato**
</dt> <dd> <dl> <dt>

7024 (0x1B70)
</dt> <dt>



Non è possibile completare l'attività che si sta tentando di eseguire perché Servizi Desktop remoto è attualmente occupata. Riprovare tra alcuni minuti. Gli altri utenti dovrebbero comunque essere in grado di accedere.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**ERRORE \_ ctx \_ \_ modalità video non valida \_**
</dt> <dd> <dl> <dt>

7025 (0x1B71)
</dt> <dt>



È stato effettuato un tentativo di connessione a una sessione la cui modalità video non è supportata dal client corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**ERRORE \_ ctx \_ Graphics \_ non valido**
</dt> <dd> <dl> <dt>

7035 (0x1B7B)
</dt> <dt>



L'applicazione ha tentato di abilitare la modalità grafica DOS. La modalità grafica DOS non è supportata.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**ERRORE \_ ctx \_ Logon \_ disabilitato**
</dt> <dd> <dl> <dt>

7037 (0x1B7D)
</dt> <dt>



Il privilegio di accesso interattivo è stato disabilitato. Contatta l'amministratore.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**ERRORE \_ ctx \_ non \_ console**
</dt> <dd> <dl> <dt>

7038 (0x1B7E)
</dt> <dt>



L'operazione richiesta può essere eseguita solo nella console di sistema. Questo è spesso il risultato di un driver o di una DLL di sistema che richiede l'accesso diretto alla console.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**ERRORE \_ di \_ query client CTX \_ \_ timeout**
</dt> <dd> <dl> <dt>

7040 (0x1B80)
</dt> <dt>



Il client non è riuscito a rispondere al messaggio di connessione al server.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**errore durante la \_ \_ disconnessione della console CTX \_**
</dt> <dd> <dl> <dt>

7041 (0x1B81)
</dt> <dt>



La disconnessione della sessione della console non è supportata.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**ERRORE \_ di \_ connessione console CTX \_**
</dt> <dd> <dl> <dt>

7042 (0x1B82)
</dt> <dt>



La riconnessione di una sessione disconnessa alla console non è supportata.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**ERRORE \_ ctx \_ shadow \_ negato**
</dt> <dd> <dl> <dt>

7044 (0x1B84)
</dt> <dt>



La richiesta di controllo di un'altra sessione in modalità remota è stata negata.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**ERRORE \_ ctx \_ WINSTATION \_ accesso \_ negato**
</dt> <dd> <dl> <dt>

7045 (0x1B85)
</dt> <dt>



L'accesso alla sessione richiesto è stato negato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**ERRORE \_ ctx \_ non valido \_**
</dt> <dd> <dl> <dt>

7049 (0x1B89)
</dt> <dt>



Il driver della connessione terminal specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**ERRORE \_ ctx \_ ombreggiatura \_ non valida**
</dt> <dd> <dl> <dt>

7050 (0x1B8A)
</dt> <dt>



La sessione richiesta non può essere controllata in modalità remota. Questo potrebbe essere dovuto al fatto che la sessione è disconnessa o che attualmente non dispone di un utente connesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**ERRORE \_ ctx \_ ombreggiato \_ disabilitato**
</dt> <dd> <dl> <dt>

7051 (0x1B8B)
</dt> <dt>



La sessione richiesta non è configurata per consentire il controllo remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**ERRORE \_ ctx \_ client \_ License \_ in \_ uso**
</dt> <dd> <dl> <dt>

7052 (0x1B8C)
</dt> <dt>



La richiesta di connessione a questo Terminal Server è stata rifiutata. Il numero di licenza del client Terminal Server è attualmente in uso da parte di un altro utente. Per ottenere un numero di licenza univoco, rivolgersi all'amministratore di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**ERRORE per la \_ \_ licenza client CTX \_ \_ non \_ impostata**
</dt> <dd> <dl> <dt>

7053 (0x1B8D)
</dt> <dt>



La richiesta di connessione a questo Terminal Server è stata rifiutata. Il numero di licenza del client Terminal Server non è stato immesso per questa copia del client Terminal Server. Contattare l'amministratore di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**ERRORE \_ ctx \_ licenza \_ non \_ disponibile**
</dt> <dd> <dl> <dt>

7054 (0x1B8E)
</dt> <dt>



Il numero di connessioni a questo computer è limitato e tutte le connessioni sono in uso al momento. Provare a connettersi in un secondo momento o contattare l'amministratore di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**ERRORE \_ ctx \_ \_ client licenze \_ non valido**
</dt> <dd> <dl> <dt>

7055 (0x1B8F)
</dt> <dt>



Il client in uso non dispone di una licenza per l'uso di questo sistema. La richiesta di accesso è stata negata.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**ERRORE \_ ctx \_ licenza \_ scaduto**
</dt> <dd> <dl> <dt>

7056 (0x1B90)
</dt> <dt>



La licenza di sistema è scaduta. La richiesta di accesso è stata negata.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**ERRORE \_ dell' \_ ombreggiatura CTX \_ non \_ in esecuzione**
</dt> <dd> <dl> <dt>

7057 (0x1B91)
</dt> <dt>



Non è stato possibile terminare il controllo remoto perché la sessione specificata non è attualmente controllata in modalità remota.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**ERRORE \_ ctx \_ dell'ombreggiatura \_ terminata \_ in base alla \_ modalità \_**
</dt> <dd> <dl> <dt>

7058 (0x1B92)
</dt> <dt>



Il controllo remoto della console è stato terminato perché la modalità di visualizzazione è stata modificata. La modifica della modalità di visualizzazione in una sessione di controllo remoto non è supportata.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**il \_ numero di attivazioni errori è stato \_ \_ superato**
</dt> <dd> <dl> <dt>

7059 (0x1B93)
</dt> <dt>



L'attivazione è già stata reimpostata per il numero massimo di volte per questa installazione. Il timer di attivazione non verrà cancellato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**ERRORE \_ ctx \_ WINSTATIONS \_ disabilitato**
</dt> <dd> <dl> <dt>

7060 (0x1B94)
</dt> <dt>



Gli account di accesso remoto sono attualmente disabilitati.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**ERRORE \_ ctx \_ livello di crittografia \_ \_ obbligatorio**
</dt> <dd> <dl> <dt>

7061 (0x1B95)
</dt> <dt>



Non si dispone del livello di crittografia appropriato per accedere a questa sessione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**ERRORE \_ ctx \_ sessione \_ in \_ uso**
</dt> <dd> <dl> <dt>

7062 (0x1B96)
</dt> <dt>



L'utente% s \\ \\ % s è attualmente connesso al computer. Solo l'utente corrente o un amministratore può accedere a questo computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**ERRORE \_ ctx \_ Nessuna \_ forza \_ disconnessione**
</dt> <dd> <dl> <dt>

7063 (0x1B97)
</dt> <dt>



L'utente% s \\ \\ % s è già connesso alla console di questo computer. Non si è autorizzati ad accedere in questo momento. Per risolvere il problema, contattare% s \\ \\ % s e disconnettersi.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**ERRORE \_ di \_ restrizione dell'account CTX \_**
</dt> <dd> <dl> <dt>

7064 (0x1B98)
</dt> <dt>



Non è possibile eseguire l'accesso a causa di una restrizione dell'account.


</dt> </dl> </dd> <dt>

<span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**errore \_ del \_ protocollo RDP errore \_**
</dt> <dd> <dl> <dt>

7065 (0x1B99)
</dt> <dt>



Il componente protocollo RDP %2 ha rilevato un errore nel flusso del protocollo e ha disconnesso il client.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**ERRORE \_ ctx \_ CDM \_ Connect**
</dt> <dd> <dl> <dt>

7066 (0x1B9A)
</dt> <dt>



Il servizio Mapping unità client si è connesso alla connessione Terminal.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**ERRORE \_ ctx \_ CDM \_ Disconnect**
</dt> <dd> <dl> <dt>

7067 (0x1B9B)
</dt> <dt>



Il servizio Mapping unità client si è disconnesso sulla connessione Terminal.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**errore \_ ctx \_ livello di sicurezza \_ \_ errore**
</dt> <dd> <dl> <dt>

7068 (0x1B9C)
</dt> <dt>



Il livello di sicurezza Terminal Server ha rilevato un errore nel flusso del protocollo e ha disconnesso il client.


</dt> </dl> </dd> <dt>

<span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**\_sessioni non \_ compatibili con errore TS \_**
</dt> <dd> <dl> <dt>

7069 (0x1B9D)
</dt> <dt>



La sessione di destinazione non è compatibile con la sessione corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**errore \_ del \_ \_ sottosistema video \_ TS errore**
</dt> <dd> <dl> <dt>

7070 (0x1B9E)
</dt> <dt>



Windows non è in grado di connettersi alla sessione perché si è verificato un problema nel sottosistema video di Windows. Provare a connettersi di nuovo in un secondo momento oppure rivolgersi all'amministratore del server per assistenza.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**\_ \_ sequenza API non valida FRS ERR \_ \_**
</dt> <dd> <dl> <dt>

8001 (0x1F41)
</dt> <dt>



L'API del servizio Replica file è stata chiamata in modo errato.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**servizio di avvio di FRS \_ Err \_ \_**
</dt> <dd> <dl> <dt>

8002 (0x1F42)
</dt> <dt>



Impossibile avviare il servizio Replica file.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**\_servizio FRS ERR \_ Stop \_**
</dt> <dd> <dl> <dt>

8003 (0x1F43)
</dt> <dt>



Impossibile arrestare il servizio Replica file.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**\_ \_ API interna di FRS ERR \_**
</dt> <dd> <dl> <dt>

8004 (0x1F44)
</dt> <dt>



La richiesta è stata terminata dall'API del servizio Replica file. È possibile che nel registro eventi siano disponibili ulteriori informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**FRS \_ Err \_ interno**
</dt> <dd> <dl> <dt>

8005 (0x1F45)
</dt> <dt>



Il servizio Replica file ha terminato la richiesta. È possibile che nel registro eventi siano disponibili ulteriori informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**\_comunicazione del \_ servizio FRS ERR \_**
</dt> <dd> <dl> <dt>

8006 (0x1F46)
</dt> <dt>



Impossibile contattare il servizio Replica file. È possibile che nel registro eventi siano disponibili ulteriori informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**\_ \_ priv sufficiente per FRS ERR \_**
</dt> <dd> <dl> <dt>

8007 (0x1F47)
</dt> <dt>



Il servizio Replica file non è in grado di soddisfare la richiesta perché l'utente non dispone di privilegi sufficienti. È possibile che nel registro eventi siano disponibili ulteriori informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**\_autenticazione FRS ERR \_**
</dt> <dd> <dl> <dt>

8008 (0x1F48)
</dt> <dt>



Il servizio Replica file non è in grado di soddisfare la richiesta perché la RPC autenticata non è disponibile. È possibile che nel registro eventi siano disponibili ulteriori informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**\_priv di elemento padre di FRS ERR \_ \_ insufficiente \_**
</dt> <dd> <dl> <dt>

8009 (0x1F49)
</dt> <dt>



Il servizio Replica file non è in grado di soddisfare la richiesta perché l'utente non dispone di privilegi sufficienti per il controller di dominio. È possibile che nel registro eventi siano disponibili ulteriori informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**\_ \_ autenticazione padre ERR \_ FRS**
</dt> <dd> <dl> <dt>

8010 (0x1F4A)
</dt> <dt>



Il servizio Replica file non è in grado di soddisfare la richiesta perché la RPC autenticata non è disponibile nel controller di dominio. È possibile che nel registro eventi siano disponibili ulteriori informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**\_da FRS \_ Err \_ figlio \_ a \_ comunicazione padre**
</dt> <dd> <dl> <dt>

8011 (0x1F4B)
</dt> <dt>



Il servizio Replica file non è in grado di comunicare con il servizio Replica file sul controller di dominio. È possibile che nel registro eventi siano disponibili ulteriori informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**\_errore \_ di FRS \_ da padre a \_ \_ comm figlio**
</dt> <dd> <dl> <dt>

8012 (0x1F4C)
</dt> <dt>



Il servizio Replica file del controller di dominio non è in grado di comunicare con il servizio Replica file di questo computer. È possibile che nel registro eventi siano disponibili ulteriori informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**\_popolamento di \_ SYSVOL Err ERR \_**
</dt> <dd> <dl> <dt>

8013 (0x1F4D)
</dt> <dt>



Il servizio Replica file non è in grado di popolare il volume di sistema a causa di un errore interno. È possibile che nel registro eventi siano disponibili ulteriori informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**\_ \_ \_ timeout popolare SYSVOL ERR \_**
</dt> <dd> <dl> <dt>

8014 (0x1F4E)
</dt> <dt>



Il servizio Replica file non è in grado di popolare il volume di sistema a causa di un timeout interno. È possibile che nel registro eventi siano disponibili ulteriori informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**il servizio FRS \_ Err \_ SYSVOL \_ è \_ occupato**
</dt> <dd> <dl> <dt>

8015 (0x1F4F)
</dt> <dt>



Il servizio Replica file non è in grado di elaborare la richiesta. Il volume di sistema è occupato con una richiesta precedente.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**abbassamento di volume \_ SYSVOL Err di FRS \_ \_**
</dt> <dd> <dl> <dt>

8016 (0x1F50)
</dt> <dt>



Il servizio Replica file non è in grado di arrestare la replica del volume di sistema a causa di un errore interno. È possibile che nel registro eventi siano disponibili ulteriori informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**\_parametro servizio FRS ERR \_ non valido \_ \_**
</dt> <dd> <dl> <dt>

8017 (0x1F51)
</dt> <dt>



Il servizio Replica file ha rilevato un parametro non valido.


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

 

 




