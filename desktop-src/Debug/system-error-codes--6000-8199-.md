---
description: Descrive i codici di errore 6000-8199 definiti nel file di intestazione WinError.h ed è destinato agli sviluppatori.
ms.assetid: eaaf9f65-e8ff-4e54-90a9-04252cdd773a
title: Codici di errore di sistema (6000-8199) (WinError.h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: d24a165798f0d4bf8a3ed534880cd3f9ad1f2b8b85d072e8a4d7aae8e6345508
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131661"
---
# <a name="system-error-codes-6000-8199"></a>Codici di errore di sistema (6000-8199)

> [!NOTE]
> Queste informazioni sono destinate agli sviluppatori che ese tracciano errori di sistema. Per altri errori, ad esempio problemi con Windows Update, è disponibile un elenco di risorse nella [pagina Codici di](system-error-codes.md) errore.

L'elenco seguente descrive i [codici di errore di](system-error-codes.md) sistema (errori da 6000 a 8199). Vengono restituiti dalla funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) quando molte funzioni hanno esito negativo. Per recuperare il testo della descrizione dell'errore nell'applicazione, usare la [**funzione FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con il flag **FORMAT MESSAGE FROM \_ \_ \_ SYSTEM.**

<dl> <dt>

<span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**ERRORE DI \_ CRITTOGRAFIA \_ NON RIUSCITA**
</dt> <dd> <dl> <dt>

6000 (0x1770)
</dt> <dt>



Impossibile crittografare il file specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**ERRORE DI \_ DECRITTOGRAFIA \_ NON RIUSCITA**
</dt> <dd> <dl> <dt>

6001 (0x1771)
</dt> <dt>



Impossibile decrittografare il file specificato.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**FILE \_ DEGLI ERRORI \_ CRITTOGRAFATO**
</dt> <dd> <dl> <dt>

6002 (0x1772)
</dt> <dt>



Il file specificato è crittografato e l'utente non è in grado di decrittografarlo.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**ERRORE \_ NESSUN CRITERIO DI \_ \_ RIPRISTINO**
</dt> <dd> <dl> <dt>

6003 (0x1773)
</dt> <dt>



Non sono stati configurati criteri di ripristino della crittografia validi per questo sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**ERRORE \_ NO \_ EFS**
</dt> <dd> <dl> <dt>

6004 (0x1774)
</dt> <dt>



Il driver di crittografia richiesto non è caricato per questo sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**ERRORE \_ \_ EFS ERRATO**
</dt> <dd> <dl> <dt>

6005 (0x1775)
</dt> <dt>



Il file è stato crittografato con un driver di crittografia diverso da quello attualmente caricato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**ERRORE \_ - NESSUNA CHIAVE \_ \_ UTENTE**
</dt> <dd> <dl> <dt>

6006 (0x1776)
</dt> <dt>



Non sono presenti chiavi EFS definite per l'utente.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**FILE \_ DEGLI ERRORI NON \_ \_ CRITTOGRAFATO**
</dt> <dd> <dl> <dt>

6007 (0x1777)
</dt> <dt>



Il file specificato non è crittografato.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**ERRORE \_ DURANTE \_ L'ESPORTAZIONE DEL \_ FORMATO**
</dt> <dd> <dl> <dt>

6008 (0x1778)
</dt> <dt>



Il file specificato non è nel formato di esportazione EFS definito.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**FILE \_ DEGLI ERRORI DI SOLA \_ \_ LETTURA**
</dt> <dd> <dl> <dt>

6009 (0x1779)
</dt> <dt>



Il file specificato è di sola lettura.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**ERRORE \_ DIR \_ EFS \_ NON CONSENTITO**
</dt> <dd> <dl> <dt>

6010 (0x177A)
</dt> <dt>



La directory è stata disabilitata per la crittografia.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**ERRORE \_ SERVER EFS \_ NON \_ \_ ATTENDIBILE**
</dt> <dd> <dl> <dt>

6011 (0x177B)
</dt> <dt>



Il server non è attendibile per l'operazione di crittografia remota.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**ERRORE \_ - CRITERI DI RIPRISTINO NON \_ \_ ERSI**
</dt> <dd> <dl> <dt>

6012 (0x177C)
</dt> <dt>



I criteri di ripristino configurati per questo sistema contengono un certificato di ripristino non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**ERRORE \_ BLOB \_ ALG EFS \_ TROPPO \_ \_ GRANDE**
</dt> <dd> <dl> <dt>

6013 (0x177D)
</dt> <dt>



L'algoritmo di crittografia usato nel file di origine richiede un buffer della chiave più grande di quello nel file di destinazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**ERRORE \_ VOLUME NON SUPPORTA \_ \_ \_ EFS**
</dt> <dd> <dl> <dt>

6014 (0x177E)
</dt> <dt>



La partizione del disco non supporta la crittografia dei file.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**ERRORE \_ EFS \_ DISABILITATO**
</dt> <dd> <dl> <dt>

6015 (0x177F)
</dt> <dt>



Questo computer è disabilitato per la crittografia dei file.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**ERRORE \_ VERSIONE EFS \_ NON \_ \_ SUPPORTATA**
</dt> <dd> <dl> <dt>

6016 (0x1780)
</dt> <dt>



Per decrittografare il file crittografato è necessario un sistema più recente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**ERRORE CS \_ \_ ENCRYPTION INVALID SERVER \_ \_ \_ RESPONSE**
</dt> <dd> <dl> <dt>

6017 (0x1781)
</dt> <dt>



Il server remoto ha inviato una risposta non valida per un file aperto con crittografia lato client.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**ERRORE \_ CS \_ ENCRYPTION \_ UNSUPPORTED \_ SERVER**
</dt> <dd> <dl> <dt>

6018 (0x1782)
</dt> <dt>



La crittografia lato client non è supportata dal server remoto anche se dichiara di supportarla.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**ERRORE \_ CS ENCRYPTION EXISTING \_ \_ \_ ENCRYPTED \_ FILE**
</dt> <dd> <dl> <dt>

6019 (0x1783)
</dt> <dt>



Il file è crittografato e deve essere aperto in modalità crittografia lato client.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**ERRORE \_ CS ENCRYPTION NEW \_ \_ \_ ENCRYPTED \_ FILE**
</dt> <dd> <dl> <dt>

6020 (0x1784)
</dt> <dt>



È in corso la creazione di un nuovo file crittografato $EFS deve essere specificato un nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**ERRORE \_ CS ENCRYPTION FILE NOT \_ \_ \_ \_ CSE**
</dt> <dd> <dl> <dt>

6021 (0x1785)
</dt> <dt>



Il client SMB ha richiesto un FILE CSE FSCTL in un file non CSE.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**ERRORE DURANTE \_ \_ L'OPERAZIONE \_ DI NEGAZIONE DEI CRITERI DI \_ CRITTOGRAFIA**
</dt> <dd> <dl> <dt>

6022 (0x1786)
</dt> <dt>



L'operazione richiesta è stata bloccata dai criteri. Per altre informazioni, contattare l'amministratore di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**ERRORE \_ NESSUN SERVER BROWSER \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

6118 (0x17E6)
</dt> <dt>



L'elenco dei server per questo gruppo di lavoro non è attualmente disponibile.


</dt> </dl> </dd> <dt>

<span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**SCHED \_ E \_ SERVICE \_ NOT \_ LOCALSYSTEM**
</dt> <dd> <dl> <dt>

6200 (0x1838)
</dt> <dt>



Il Utilità di pianificazione deve essere configurato per l'esecuzione nell'account di sistema per il corretto funzionamento. Le singole attività possono essere configurate per l'esecuzione in altri account.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**SETTORE \_ DEL LOG DEGLI ERRORI NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

6600 (0x19C8)
</dt> <dt>



Il servizio di log ha rilevato un settore di log non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**PARITÀ \_ DEL SETTORE DEL LOG DEGLI ERRORI NON \_ \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

6601 (0x19C9)
</dt> <dt>



Il servizio di log ha rilevato un settore di log con parità di blocco non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**RIDEFINIRE IL \_ MAPPING DEL SETTORE DEL LOG DEGLI \_ \_ ERRORI**
</dt> <dd> <dl> <dt>

6602 (0x19CA)
</dt> <dt>



Il servizio di log ha rilevato un settore di log mappato.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**BLOCCO \_ DEL LOG DEGLI ERRORI \_ \_ INCOMPLETO**
</dt> <dd> <dl> <dt>

6603 (0x19CB)
</dt> <dt>



Il servizio di log ha rilevato un blocco di log parziale o incompleto.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**INTERVALLO \_ DEL LOG DEGLI ERRORI NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

6604 (0x19CC)
</dt> <dt>



Il servizio di log ha rilevato un tentativo di accesso ai dati non compreso nell'intervallo di log attivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**BLOCCHI \_ DEL LOG DEGLI ERRORI \_ \_ ESAURITI**
</dt> <dd> <dl> <dt>

6605 (0x19CD)
</dt> <dt>



I buffer di marshalling degli utenti del servizio di log sono esauriti.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**CONTESTO DI \_ LETTURA LOG DEGLI ERRORI NON \_ \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

6606 (0x19CE)
</dt> <dt>



Il servizio di log ha rilevato un tentativo di lettura da un'area di marshalling con un contesto di lettura non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**RIAVVIO \_ DEL LOG DEGLI ERRORI NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

6607 (0x19CF)
</dt> <dt>



Il servizio di log ha rilevato un'area di riavvio del log non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**VERSIONE \_ DEL BLOCCO DEL LOG DEGLI \_ \_ ERRORI**
</dt> <dd> <dl> <dt>

6608 (0x19D0)
</dt> <dt>



Il servizio di log ha rilevato una versione del blocco di log non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**BLOCCO \_ DEL LOG DEGLI ERRORI NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

6609 (0x19D1)
</dt> <dt>



Il servizio di log ha rilevato un blocco di log non valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**MODALITÀ \_ DI LETTURA LOG DEGLI ERRORI NON \_ \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

6610 (0x19D2)
</dt> <dt>



Il servizio di log ha rilevato un tentativo di lettura del log con una modalità di lettura non valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**LOG \_ DEGLI ERRORI NESSUN \_ \_ RIAVVIO**
</dt> <dd> <dl> <dt>

6611 (0x19D3)
</dt> <dt>



Il servizio di log ha rilevato un flusso di log senza area di riavvio.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**METADATI \_ DEL LOG DEGLI ERRORI \_ \_ DANNEGGIATI**
</dt> <dd> <dl> <dt>

6612 (0x19D4)
</dt> <dt>



Il servizio di log ha rilevato un file di metadati danneggiato.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**METADATI \_ DEL LOG DEGLI ERRORI NON \_ \_ VALIDI**
</dt> <dd> <dl> <dt>

6613 (0x19D5)
</dt> <dt>



Il servizio di log ha rilevato un file di metadati che non è stato possibile creare dal log file system.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**METADATI DEL \_ LOG \_ DEGLI ERRORI \_ INCOERENTI**
</dt> <dd> <dl> <dt>

6614 (0x19D6)
</dt> <dt>



Il servizio di log ha rilevato un file di metadati con dati incoerenti.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**PRENOTAZIONE \_ LOG DEGLI ERRORI NON \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

6615 (0x19D7)
</dt> <dt>



Il servizio di log ha rilevato un tentativo eroso di allocare o eliminare lo spazio di prenotazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**LOG \_ DEGLI ERRORI \_ CANT \_ DELETE**
</dt> <dd> <dl> <dt>

6616 (0x19D8)
</dt> <dt>



Il servizio di log non può eliminare il file di log o file system contenitore.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**LIMITE \_ DEL \_ CONTENITORE DEL LOG DEGLI ERRORI \_ \_ SUPERATO**
</dt> <dd> <dl> <dt>

6617 (0x19D9)
</dt> <dt>



Il servizio di log ha raggiunto il numero massimo di contenitori consentiti allocati a un file di log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**INIZIO \_ LOG DEGLI ERRORI DEL \_ \_ \_ LOG**
</dt> <dd> <dl> <dt>

6618 (0x19DA)
</dt> <dt>



Il servizio di log ha tentato di leggere o scrivere all'indietro dopo l'avvio del log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**CRITERI \_ DEL LOG DEGLI ERRORI GIÀ \_ \_ \_ INSTALLATI**
</dt> <dd> <dl> <dt>

6619 (0x19DB)
</dt> <dt>



Impossibile installare i criteri di log perché è già presente un criterio dello stesso tipo.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**CRITERI \_ DEL LOG DEGLI ERRORI NON \_ \_ \_ INSTALLATI**
</dt> <dd> <dl> <dt>

6620 (0x19DC)
</dt> <dt>



I criteri di log in questione non sono stati installati al momento della richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**CRITERI \_ DEL LOG DEGLI ERRORI NON \_ \_ VALIDI**
</dt> <dd> <dl> <dt>

6621 (0x19DD)
</dt> <dt>



Il set di criteri installato nel log non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**CONFLITTO DEI \_ CRITERI DEL LOG DEGLI \_ \_ ERRORI**
</dt> <dd> <dl> <dt>

6622 (0x19DE)
</dt> <dt>



Un criterio nel log in questione ha impedito il completamento dell'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**CODA DI \_ ARCHIVIAZIONE BLOCCATA DEL LOG DEGLI \_ \_ \_ ERRORI**
</dt> <dd> <dl> <dt>

6623 (0x19DF)
</dt> <dt>



Non è possibile recuperare spazio del log perché il log è bloccato dalla parte finale dell'archivio.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**RECORD \_ DEL LOG DEGLI ERRORI \_ \_ INESISTENTE**
</dt> <dd> <dl> <dt>

6624 (0x19E0)
</dt> <dt>



Il record di log non è un record nel file di log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**RECORD DEL \_ LOG DEGLI ERRORI RISERVATI NON \_ \_ \_ VALIDI**
</dt> <dd> <dl> <dt>

6625 (0x19E1)
</dt> <dt>



Il numero di record di log riservati o la rettifica del numero di record di log riservati non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**SPAZIO RISERVATO \_ DEL LOG DEGLI ERRORI NON \_ \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

6626 (0x19E2)
</dt> <dt>



Lo spazio di log riservato o la regolazione dello spazio del log non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**CODA \_ LOG DEGLI ERRORI NON \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

6627 (0x19E3)
</dt> <dt>



Una coda di archiviazione nuova o esistente o una base del log attivo non è valida.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**LOG \_ DEGLI ERRORI \_ COMPLETO**
</dt> <dd> <dl> <dt>

6628 (0x19E4)
</dt> <dt>



Spazio log esaurito.


</dt> </dl> </dd> <dt>

<span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**ERRORE NON \_ \_ È STATO POSSIBILE \_ RIDIMENSIONARE IL \_ LOG**
</dt> <dd> <dl> <dt>

6629 (0x19E5)
</dt> <dt>



Non è stato possibile impostare il log sulla dimensione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**\_ \_ MULTIPLEXED LOG DEGLI ERRORI**
</dt> <dd> <dl> <dt>

6630 (0x19E6)
</dt> <dt>



Il log è con multiplex, non sono consentite scritture dirette nel log fisico.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**LOG \_ DEGLI \_ ERRORI DEDICATO**
</dt> <dd> <dl> <dt>

6631 (0x19E7)
</dt> <dt>



L'operazione non è riuscita perché il log è un log dedicato.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**\_L'ARCHIVIO DEL LOG DEGLI ERRORI NON È IN \_ \_ \_ \_ CORSO**
</dt> <dd> <dl> <dt>

6632 (0x19E8)
</dt> <dt>



L'operazione richiede un contesto di archiviazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**ARCHIVIAZIONE \_ LOG DEGLI ERRORI IN \_ \_ \_ CORSO**
</dt> <dd> <dl> <dt>

6633 (0x19E9)
</dt> <dt>



È in corso l'archiviazione dei log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**MESSAGGIO \_ \_ FFEMERAL DEL LOG DEGLI ERRORI**
</dt> <dd> <dl> <dt>

6634 (0x19EA)
</dt> <dt>



L'operazione richiede un log non phemeral, ma il log è phemeral.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**LOG \_ DEGLI \_ \_ ERRORI: \_ CONTENITORI NON SUFFICIENTI**
</dt> <dd> <dl> <dt>

6635 (0x19EB)
</dt> <dt>



Il log deve avere almeno due contenitori prima di poter essere letto o scritto.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**CLIENT \_ LOG DEGLI ERRORI GIÀ \_ \_ \_ REGISTRATO**
</dt> <dd> <dl> <dt>

6636 (0x19EC)
</dt> <dt>



Un client di log è già registrato nel flusso.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**\_CLIENT LOG DEGLI ERRORI NON \_ \_ \_ REGISTRATO**
</dt> <dd> <dl> <dt>

6637 (0x19ED)
</dt> <dt>



Un client di log non è stato registrato nel flusso.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**GESTORE \_ LOG DEGLI ERRORI COMPLETO IN \_ \_ \_ \_ CORSO**
</dt> <dd> <dl> <dt>

6638 (0x19EE)
</dt> <dt>



È già stata effettuata una richiesta per gestire la condizione di registrazione completa.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**LETTURA \_ DEL \_ CONTENITORE DEL LOG DEGLI ERRORI NON \_ \_ RIUSCITA**
</dt> <dd> <dl> <dt>

6639 (0x19EF)
</dt> <dt>



Il servizio di log ha rilevato un errore durante il tentativo di lettura da un contenitore di log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**SCRITTURA \_ DEL \_ CONTENITORE DEL LOG DEGLI ERRORI NON \_ \_ RIUSCITA**
</dt> <dd> <dl> <dt>

6640 (0x19F0)
</dt> <dt>



Il servizio di log ha rilevato un errore durante il tentativo di scrittura in un contenitore di log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**APERTURA \_ DEL \_ CONTENITORE DEL LOG DEGLI ERRORI NON \_ \_ RIUSCITA**
</dt> <dd> <dl> <dt>

6641 (0x19F1)
</dt> <dt>



Il servizio di log ha rilevato un errore durante il tentativo di apertura di un contenitore di log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**STATO \_ DEL \_ CONTENITORE DEL LOG DEGLI ERRORI NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

6642 (0x19F2)
</dt> <dt>



Il servizio di log ha rilevato uno stato del contenitore non valido durante il tentativo di un'azione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**STATO \_ DEL LOG DEGLI ERRORI NON \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

6643 (0x19F3)
</dt> <dt>



Il servizio di log non è nello stato corretto per eseguire un'azione richiesta.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**LOG \_ \_ DEGLI ERRORI AGGIUNTO**
</dt> <dd> <dl> <dt>

6644 (0x19F4)
</dt> <dt>



Non è possibile recuperare lo spazio del log perché il log è bloccato.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**SCARICAMENTO \_ DEI METADATI DEL LOG DEGLI ERRORI NON \_ \_ \_ RIUSCITO**
</dt> <dd> <dl> <dt>

6645 (0x19F5)
</dt> <dt>



Lo scaricamento dei metadati del log non è riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**SICUREZZA \_ \_ INCOERENTE DEL LOG DEGLI \_ ERRORI**
</dt> <dd> <dl> <dt>

6646 (0x19F6)
</dt> <dt>



La sicurezza nel log e nei relativi contenitori è incoerente.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**LO \_ SCARICAMENTO \_ ACCODATO DEL LOG \_ DEGLI ERRORI NON È \_ RIUSCITO**
</dt> <dd> <dl> <dt>

6647 (0x19F7)
</dt> <dt>



I record sono stati aggiunti al log o sono state apportate modifiche alla prenotazione, ma non è stato possibile svuotare il log.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**PRENOTAZIONE \_ AGGIUNTA AL LOG DEGLI \_ \_ ERRORI**
</dt> <dd> <dl> <dt>

6648 (0x19F8)
</dt> <dt>



Il log viene aggiunto a causa della prenotazione che utilizza la maggior parte dello spazio del log. Liberare alcuni record riservati per liberare spazio.


</dt> </dl> </dd> <dt>

<span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**ERRORE \_ TRANSAZIONE \_ NON VALIDA**
</dt> <dd> <dl> <dt>

6700 (0x1A2C)
</dt> <dt>



L'handle di transazione associato a questa operazione non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**TRANSAZIONE \_ DI \_ ERRORE NON \_ ATTIVA**
</dt> <dd> <dl> <dt>

6701 (0x1A2D)
</dt> <dt>



L'operazione richiesta è stata eseguita nel contesto di una transazione che non è più attiva.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**RICHIESTA \_ DI \_ TRANSAZIONE ERRORE NON \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

6702 (0x1A2E)
</dt> <dt>



L'operazione richiesta non è valida per l'oggetto Transaction nello stato corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**TRANSAZIONE \_ DI \_ ERRORE NON \_ RICHIESTA**
</dt> <dd> <dl> <dt>

6703 (0x1A2F)
</dt> <dt>



Il chiamante ha chiamato un'API di risposta, ma la risposta non è prevista perché il TM non ha emittente la richiesta corrispondente al chiamante.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**TRANSAZIONE \_ DI ERRORE \_ GIÀ \_ INTERROTTA**
</dt> <dd> <dl> <dt>

6704 (0x1A30)
</dt> <dt>



È troppo tardi per eseguire l'operazione richiesta, perché la transazione è già stata interrotta.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**TRANSAZIONE \_ DI ERRORE GIÀ DI CUI È GIÀ STATO ESEGUITO IL \_ \_ COMMIT**
</dt> <dd> <dl> <dt>

6705 (0x1A31)
</dt> <dt>



È troppo tardi per eseguire l'operazione richiesta, perché è già stato eseguito il commit della transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**ERRORE \_ DI INIZIALIZZAZIONE TM \_ NON \_ RIUSCITA**
</dt> <dd> <dl> <dt>

6706 (0x1A32)
</dt> <dt>



Impossibile inizializzare correttamente il gestore transazioni. Le operazioni transazione non sono supportate.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**ERRORE \_ RESOURCEMANAGER \_ DI SOLA \_ LETTURA**
</dt> <dd> <dl> <dt>

6707 (0x1A33)
</dt> <dt>



L'oggetto ResourceManager specificato non ha apportato modifiche o aggiornamenti alla risorsa in questa transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**TRANSAZIONE \_ DI ERRORE NON \_ \_ UNITA**
</dt> <dd> <dl> <dt>

6708 (0x1A34)
</dt> <dt>



Il gestore delle risorse ha tentato di preparare una transazione che non è stata unita correttamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**ESISTE \_ UNA \_ TRANSAZIONE DI ERRORE \_ SUPERIORE**
</dt> <dd> <dl> <dt>

6709 (0x1A35)
</dt> <dt>



L'oggetto Transaction ha già un'integrazione superiore e il chiamante ha tentato un'operazione che avrebbe creato un nuovo superiore. È consentita una sola integrazione superiore.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**ERRORE \_ DEL PROTOCOLLO CRM GIÀ \_ \_ \_ ESISTENTE**
</dt> <dd> <dl> <dt>

6710 (0x1A36)
</dt> <dt>



RM ha tentato di registrare un protocollo già esistente.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**ERRORE \_ PROPAGAZIONE \_ TRANSAZIONE \_ NON RIUSCITA**
</dt> <dd> <dl> <dt>

6711 (0x1A37)
</dt> <dt>



Tentativo di propagazione della transazione non riuscito.


</dt> </dl> </dd> <dt>

<span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**ERRORE \_ DEL PROTOCOLLO CRM NON \_ \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

6712 (0x1A38)
</dt> <dt>



Il protocollo di propagazione richiesto non è stato registrato come CRM.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**TRANSAZIONE \_ DI ERRORE BUFFER MARSHALL NON \_ \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

6713 (0x1A39)
</dt> <dt>



Il buffer passato a PushTransaction o PullTransaction non è in un formato valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**ERRORE \_ \_ TRANSAZIONE CORRENTE \_ NON \_ VALIDA**
</dt> <dd> <dl> <dt>

6714 (0x1A3A)
</dt> <dt>



Il contesto di transazione corrente associato al thread non è un handle valido per un oggetto transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**TRANSAZIONE \_ \_ DI ERRORE NON \_ TROVATA**
</dt> <dd> <dl> <dt>

6715 (0x1A3B)
</dt> <dt>



Impossibile aprire l'oggetto Transaction specificato perché non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**ERRORE \_ RESOURCEMANAGER \_ NON \_ TROVATO**
</dt> <dd> <dl> <dt>

6716 (0x1A3C)
</dt> <dt>



Impossibile aprire l'oggetto ResourceManager specificato perché non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**INTEGRAZIONE \_ DEGLI ERRORI NON \_ \_ TROVATA**
</dt> <dd> <dl> <dt>

6717 (0x1A3D)
</dt> <dt>



Impossibile aprire l'oggetto Enlistment specificato perché non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**ERRORE \_ TRANSACTIONMANAGER \_ NON \_ TROVATO**
</dt> <dd> <dl> <dt>

6718 (0x1A3E)
</dt> <dt>



Impossibile aprire l'oggetto TransactionManager specificato perché non è stato trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**ERRORE \_ TRANSACTIONMANAGER \_ NON \_ ONLINE**
</dt> <dd> <dl> <dt>

6719 (0x1A3F)
</dt> <dt>



Impossibile creare o aprire l'oggetto specificato perché l'oggetto TransactionManager associato non è online. TransactionManager deve essere portato completamente online chiamando RecoverTransactionManager per eseguire il ripristino fino alla fine del logFile prima che gli oggetti nei relativi spazi dei nomi Transaction o ResourceManager possano essere aperti. Inoltre, gli errori di scrittura dei record nel relativo LogFile possono causare la disconnessione di transactionManager.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**ERRORE DI \_ COLLISIONE DEI NOMI \_ DI RIPRISTINO \_ DI TRANSACTIONMANAGER \_**
</dt> <dd> <dl> <dt>

6720 (0x1A40)
</dt> <dt>



L'oggetto TransactionManager specificato non è stato in grado di creare gli oggetti contenuti nel relativo file di log nello spazio dei nomi Ob. Di conseguenza, TransactionManager non è stato in grado di eseguire il recupero.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**ERROR \_ TRANSACTION \_ NOT \_ ROOT**
</dt> <dd> <dl> <dt>

6721 (0x1A41)
</dt> <dt>



Impossibile completare la chiamata per creare un'integrazione superiore in questo oggetto Transaction, perché l'oggetto Transaction specificato per l'integrazione è un ramo subordinato della transazione. Solo la radice della transazione può essere integrata come livello superiore.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**ERRORE OGGETTO \_ \_ TRANSAZIONE \_ SCADUTO**
</dt> <dd> <dl> <dt>

6722 (0x1A42)
</dt> <dt>



Poiché la gestione transazioni o la gestione risorse associata è stata chiusa, l'handle non è più valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**ERRORE RISPOSTA \_ \_ TRANSAZIONE \_ NON \_ INTEGRATA**
</dt> <dd> <dl> <dt>

6723 (0x1A43)
</dt> <dt>



Non è stato possibile eseguire l'operazione specificata su questa integrazione Superiore, perché l'integrazione non è stata creata con la risposta di completamento corrispondente in NotificationMask.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**RECORD \_ DELLA \_ TRANSAZIONE DI ERRORE TROPPO \_ \_ LUNGO**
</dt> <dd> <dl> <dt>

6724 (0x1A44)
</dt> <dt>



Impossibile eseguire l'operazione specificata perché il record che verrebbe registrato era troppo lungo. Ciò può verificarsi a causa di due condizioni: sono presenti troppi integrazioni in questa transazione o la combinazione di RecoveryInformation registrata per conto di tali integrazioni è troppo lunga.


</dt> </dl> </dd> <dt>

<span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**ERRORE \_ \_ TRANSAZIONE \_ IMPLICITA NON \_ SUPPORTATA**
</dt> <dd> <dl> <dt>

6725 (0x1A45)
</dt> <dt>



La transazione implicita non è supportata.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**ERRORE DURANTE \_ LA \_ VIOLAZIONE \_ DELL'INTEGRITÀ DELLA TRANSAZIONE**
</dt> <dd> <dl> <dt>

6726 (0x1A46)
</dt> <dt>



La gestione transazioni del kernel ha dovuto interrompere o dimenticare la transazione perché ha bloccato lo stato di avanzamento in avanti.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**ERRORE \_ DI MANCATA CORRISPONDENZA \_ \_ DELL'IDENTITÀ DI TRANSACTIONMANAGER**
</dt> <dd> <dl> <dt>

6727 (0x1A47)
</dt> <dt>



L'identità TransactionManager fornita non corrisponde a quella registrata nel file di log di TransactionManager.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**ERRORE \_ RM \_ NON BLOCCATO PER LO \_ \_ \_ \_ SNAPSHOT**
</dt> <dd> <dl> <dt>

6728 (0x1A48)
</dt> <dt>



L'operazione di snapshot non può continuare perché un gestore di risorse transazionale non può essere bloccato nello stato corrente. Riprova.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**ERROR \_ TRANSACTION \_ MUST \_ WRITETHROUGH**
</dt> <dd> <dl> <dt>

6729 (0x1A49)
</dt> <dt>



La transazione non può essere integrata nell'oggetto EnlistmentMask specificato, perché la transazione ha già completato la fase PrePrepare. Per garantire la correttezza, ResourceManager deve passare a una modalità write-through e smettere di memorizzare nella cache i dati all'interno di questa transazione. L'integrazione solo per le fasi di transazione successive può comunque avere esito positivo.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**ERROR \_ TRANSACTION \_ NO \_ SUPERIOR**
</dt> <dd> <dl> <dt>

6730 (0x1A4A)
</dt> <dt>



La transazione non dispone di un'integrazione superiore.


</dt> </dl> </dd> <dt>

<span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**POSSIBILE \_ DANNEGGIAMENTO \_ EURISTICO \_ DEGLI ERRORI**
</dt> <dd> <dl> <dt>

6731 (0x1A4B)
</dt> <dt>



Il tentativo di eseguire il commit della transazione è stato completato, ma è possibile che non sia stato eseguito correttamente il commit di una parte dell'albero delle transazioni a causa dell'euristica. È pertanto possibile che non sia stato eseguito il commit di alcuni dati modificati nella transazione, con conseguente incoerenza transazionale. Se possibile, controllare la coerenza dei dati associati.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**ERRORE \_ CONFLITTO \_ TRANSAZIONALE**
</dt> <dd> <dl> <dt>

6800 (0x1A90)
</dt> <dt>



La funzione ha tentato di usare un nome riservato per l'utilizzo da parte di un'altra transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**ERRORE \_ RM \_ NON \_ ATTIVO**
</dt> <dd> <dl> <dt>

6801 (0x1A91)
</dt> <dt>



Il supporto delle transazioni all'interno del gestore di risorse specificato non è stato avviato o è stato arrestato a causa di un errore.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**ERRORE \_ METADATI RM \_ \_ DANNEGGIATI**
</dt> <dd> <dl> <dt>

6802 (0x1A92)
</dt> <dt>



I metadati dell'RM sono danneggiati. L'RM non funzionerà.


</dt> </dl> </dd> <dt>

<span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**DIRECTORY \_ DEGLI ERRORI NON \_ \_ RM**
</dt> <dd> <dl> <dt>

6803 (0x1A93)
</dt> <dt>



La directory specificata non contiene un gestore di risorse.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**TRANSAZIONI \_ DI ERRORE REMOTE NON \_ \_ SUPPORTATE**
</dt> <dd> <dl> <dt>

6805 (0x1A95)
</dt> <dt>



Il server remoto o la condivisione non supporta le operazioni su file transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**DIMENSIONI DEL \_ LOG DEGLI ERRORI NON \_ \_ \_ VALIDE**
</dt> <dd> <dl> <dt>

6806 (0x1A96)
</dt> <dt>



Le dimensioni del log richieste non sono valide.


</dt> </dl> </dd> <dt>

<span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**\_L'OGGETTO ERROR NON ESISTE \_ \_ \_ PIÙ**
</dt> <dd> <dl> <dt>

6807 (0x1A97)
</dt> <dt>



L'oggetto (file, flusso, collegamento) corrispondente all'handle è stato eliminato da un rollback del punto di salvataggio della transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**ERRORE \_ \_ MINIVERSIONE \_ FLUSSO NON \_ TROVATA**
</dt> <dd> <dl> <dt>

6808 (0x1A98)
</dt> <dt>



La miniversione di file specificata non è stata trovata per questo file transazione aperto.


</dt> </dl> </dd> <dt>

<span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**\_MINIVERSIONE DEL FLUSSO DI ERRORE NON \_ \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

6809 (0x1A99)
</dt> <dt>



La miniversione di file specificata è stata trovata ma è stata invalidata. La causa più probabile è un rollback del punto di salvataggio delle transazioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**\_MINIVERSIONE DI \_ ERRORE \_ INACCESSIBILE DALLA \_ TRANSAZIONE \_ SPECIFICATA**
</dt> <dd> <dl> <dt>

6810 (0x1A9A)
</dt> <dt>



Una miniversione può essere aperta solo nel contesto della transazione che lo ha creato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**ERRORE \_ CANT \_ OPEN \_ MINIVERSION WITH MODIFY \_ \_ \_ INTENT**
</dt> <dd> <dl> <dt>

6811 (0x1A9B)
</dt> <dt>



Non è possibile aprire una miniversione con accesso di modifica.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**ERRORE \_ DURANTE LA CREAZIONE DI ALTRE \_ \_ \_ \_ MINIVERSIONI DI FLUSSO**
</dt> <dd> <dl> <dt>

6812 (0x1A9C)
</dt> <dt>



Non è possibile creare altre miniversioni per questo flusso.


</dt> </dl> </dd> <dt>

<span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**ERRORE \_ VERSIONE FILE REMOTO NON \_ \_ \_ CORRISPONDENTE**
</dt> <dd> <dl> <dt>

6814 (0x1A9E)
</dt> <dt>



Il server remoto ha inviato un numero di versione non corrispondente o Fid per un file aperto con transazioni.


</dt> </dl> </dd> <dt>

<span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**HANDLE \_ DI ERRORE NON PIÙ \_ \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

6815 (0x1A9F)
</dt> <dt>



L'handle è stato invalidato da una transazione. La causa più probabile è la presenza del mapping della memoria in un file o in un handle aperto al termine o al rollback della transazione fino al punto di salvataggio.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**ERRORE \_ SENZA \_ METADATI \_ TXF**
</dt> <dd> <dl> <dt>

6816 (0x1AA0)
</dt> <dt>



Nel file non sono presenti metadati di transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**RILEVATO \_ DANNEGGIAMENTO DEL LOG \_ DEGLI \_ ERRORI**
</dt> <dd> <dl> <dt>

6817 (0x1AA1)
</dt> <dt>



I dati del log sono danneggiati.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**ERRORE \_ CANT \_ RECOVER WITH HANDLE \_ \_ \_ OPEN**
</dt> <dd> <dl> <dt>

6818 (0x1AA2)
</dt> <dt>



Non è possibile recuperare il file perché è ancora aperto un handle.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**ERRORE \_ RM \_ DISCONNESSO**
</dt> <dd> <dl> <dt>

6819 (0x1AA3)
</dt> <dt>



Il risultato della transazione non è disponibile perché il gestore di risorse responsabile è stato disconnesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**INTEGRAZIONE \_ DEGLI ERRORI NON \_ \_ SUPERIORE**
</dt> <dd> <dl> <dt>

6820 (0x1AA4)
</dt> <dt>



La richiesta è stata rifiutata perché l'integrazione in questione non è un'integrazione superiore.


</dt> </dl> </dd> <dt>

<span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**RIPRISTINO \_ DEGLI ERRORI NON \_ \_ NECESSARIO**
</dt> <dd> <dl> <dt>

6821 (0x1AA5)
</dt> <dt>



Il gestore delle risorse transazionali è già coerente. Il ripristino non è necessario.


</dt> </dl> </dd> <dt>

<span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**ERRORE \_ RM \_ GIÀ \_ AVVIATO**
</dt> <dd> <dl> <dt>

6822 (0x1AA6)
</dt> <dt>



Il gestore delle risorse transazionali è già stato avviato.


</dt> </dl> </dd> <dt>

<span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**IDENTITÀ \_ DEL FILE DI ERRORE NON \_ \_ \_ PERSISTENTE**
</dt> <dd> <dl> <dt>

6823 (0x1AA7)
</dt> <dt>



Il file non può essere aperto in modo transazionale, perché la relativa identità dipende dal risultato di una transazione non risolta.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**ERRORE \_ NON PUÒ INTERROMPERE LA DIPENDENZA \_ \_ \_ TRANSAZIONALE**
</dt> <dd> <dl> <dt>

6824 (0x1AA8)
</dt> <dt>



L'operazione non può essere eseguita perché un'altra transazione dipende dal fatto che questa proprietà non cambierà.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**ERRORE \_ CANT \_ CROSS \_ RM \_ BOUNDARY**
</dt> <dd> <dl> <dt>

6825 (0x1AA9)
</dt> <dt>



L'operazione comporterebbe un singolo file con due gestori delle risorse transazionali e pertanto non è consentita.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**ERRORE \_ TXF \_ DIR \_ NON \_ VUOTO**
</dt> <dd> <dl> <dt>

6826 (0x1AAA)
</dt> <dt>



La $Txf directory deve essere vuota per l'esito positivo dell'operazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**ERRORE \_ DURANTE L'INDOUBT \_ TRANSACTIONS \_ EXIST**
</dt> <dd> <dl> <dt>

6827 (0x1AAB)
</dt> <dt>



L'operazione lascia uno stato incoerente per un gestore di risorse transazionale e pertanto non è consentita.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**ERRORE \_ TM \_ VOLATILE**
</dt> <dd> <dl> <dt>

6828 (0x1AAC)
</dt> <dt>



Impossibile completare l'operazione perché il gestore transazioni non dispone di un log.


</dt> </dl> </dd> <dt>

<span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**TIMER \_ DI ROLLBACK DEGLI ERRORI \_ \_ SCADUTO**
</dt> <dd> <dl> <dt>

6829 (0x1AAD)
</dt> <dt>



Non è stato possibile pianificato un rollback perché un rollback pianificato in precedenza è già stato eseguito o è stato accodato per l'esecuzione.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**ERRORE \_ DELL'ATTRIBUTO TXF \_ \_ DANNEGGIATO**
</dt> <dd> <dl> <dt>

6830 (0x1AAE)
</dt> <dt>



L'attributo dei metadati transazionali nel file o nella directory è danneggiato e illeggibile.


</dt> </dl> </dd> <dt>

<span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**ERRORE \_ EFS \_ NON CONSENTITO \_ NELLA \_ \_ TRANSAZIONE**
</dt> <dd> <dl> <dt>

6831 (0x1AAF)
</dt> <dt>



Impossibile completare l'operazione di crittografia perché è attiva una transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**ERRORE \_ APERTURA \_ TRANSAZIONALE NON \_ \_ CONSENTITA**
</dt> <dd> <dl> <dt>

6832 (0x1AB0)
</dt> <dt>



Questo oggetto non può essere aperto in una transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**AUMENTO \_ DEL LOG DEGLI ERRORI NON \_ \_ RIUSCITO**
</dt> <dd> <dl> <dt>

6833 (0x1AB1)
</dt> <dt>



Tentativo di creare spazio nel log del gestore delle risorse transazionale non riuscito. Lo stato dell'errore è stato registrato nel registro eventi.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**ERRORE \_ DI \_ MAPPING TRANSAZIONE REMOTO NON \_ \_ SUPPORTATO**
</dt> <dd> <dl> <dt>

6834 (0x1AB2)
</dt> <dt>



Il mapping della memoria (creazione di una sezione mappata) di un file remoto in una transazione non è supportato.


</dt> </dl> </dd> <dt>

<span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**METADATI \_ TXF \_ DI ERRORE GIÀ \_ \_ PRESENTI**
</dt> <dd> <dl> <dt>

6835 (0x1AB3)
</dt> <dt>



I metadati della transazione sono già presenti in questo file e non possono essere sostituiti.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**CALLBACK \_ \_ DELL'AMBITO \_ DELLA TRANSAZIONE \_ DI ERRORE NON \_ IMPOSTATI**
</dt> <dd> <dl> <dt>

6836 (0x1AB4)
</dt> <dt>



Impossibile immettere un ambito della transazione perché il gestore dell'ambito non è stato inizializzato.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**PROMOZIONE \_ RICHIESTA \_ DELLA \_ TRANSAZIONE DI ERRORE**
</dt> <dd> <dl> <dt>

6837 (0x1AB5)
</dt> <dt>



La promozione era necessaria per consentire al gestore delle risorse di integrarsi, ma la transazione è stata impostata per non consentire l'integrazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**ERRORE: \_ IMPOSSIBILE ESEGUIRE IL FILE NELLA \_ \_ \_ \_ TRANSAZIONE**
</dt> <dd> <dl> <dt>

6838 (0x1AB6)
</dt> <dt>



Questo file è aperto per la modifica in una transazione non risolta e può essere aperto per l'esecuzione solo da un lettore transazionale.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**TRANSAZIONI \_ DI ERRORE NON \_ \_ BLOCCATE**
</dt> <dd> <dl> <dt>

6839 (0x1AB7)
</dt> <dt>



La richiesta di scosto delle transazioni bloccate è stata ignorata perché le transazioni non erano state bloccate in precedenza.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**BLOCCO \_ DELLA \_ TRANSAZIONE DI ERRORE IN \_ \_ CORSO**
</dt> <dd> <dl> <dt>

6840 (0x1AB8)
</dt> <dt>



Le transazioni non possono essere bloccate perché è già in corso un blocco.


</dt> </dl> </dd> <dt>

<span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**ERRORE \_ NON VOLUME \_ \_ SNAPSHOT**
</dt> <dd> <dl> <dt>

6841 (0x1AB9)
</dt> <dt>



Il volume di destinazione non è un volume snapshot. Questa operazione è valida solo in un volume montato come snapshot.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**ERRORE \_ NESSUN PUNTO DI SALVATAGGIO CON FILE \_ \_ \_ \_ APERTI**
</dt> <dd> <dl> <dt>

6842 (0x1ABA)
</dt> <dt>



L'operazione di salvataggio del punto di salvataggio non è riuscita perché i file sono aperti nella transazione. Questa operazione non è consentita.


</dt> </dl> </dd> <dt>

<span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**CORREZIONE \_ DEI DATI DI ERRORE \_ \_ PERSI**
</dt> <dd> <dl> <dt>

6843 (0x1ABB)
</dt> <dt>



Windows rilevato danneggiamento in un file e tale file è stato ripristinato. È possibile che si sia verificata una perdita di dati.


</dt> </dl> </dd> <dt>

<span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**SPARSE \_ DI ERRORE NON CONSENTITO NELLA \_ \_ \_ \_ TRANSAZIONE**
</dt> <dd> <dl> <dt>

6844 (0x1ABC)
</dt> <dt>



Impossibile completare l'operazione di tipo sparse perché nel file è attiva una transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**ERRORE \_ TM \_ IDENTITY \_ MISMATCH**
</dt> <dd> <dl> <dt>

6845 (0x1ABD)
</dt> <dt>



La chiamata per creare un oggetto TransactionManager non è riuscita perché l'identità Tm archiviata nel file di log non corrisponde all'identità Tm passata come argomento.


</dt> </dl> </dd> <dt>

<span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**SEZIONE \_ FLOATED \_ DEGLI ERRORI**
</dt> <dd> <dl> <dt>

6846 (0x1ABE)
</dt> <dt>



È stato effettuato un tentativo di I/O su un oggetto sezione che è stato mobile come risultato della fine di una transazione. Non sono presenti dati validi.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**\_L'ERRORE NON PUÒ ACCETTARE IL LAVORO \_ \_ \_ TRANSAZIONE**
</dt> <dd> <dl> <dt>

6847 (0x1ABF)
</dt> <dt>



Il gestore delle risorse transazionali non può attualmente accettare operazioni transazionali a causa di una condizione temporanea, ad esempio risorse limitate.


</dt> </dl> </dd> <dt>

<span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**IMPOSSIBILE \_ INTERROMPERE \_ LE \_ TRANSAZIONI**
</dt> <dd> <dl> <dt>

6848 (0x1AC0)
</dt> <dt>



Il gestore delle risorse transazionali ha troppe tranaction in sospeso che non è stato possibile interrompere. La gestione delle risorse transazionali è stata arrestata.


</dt> </dl> </dd> <dt>

<span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**ERRORE \_ CLUSTER \_ NON ERRI**
</dt> <dd> <dl> <dt>

6849 (0x1AC1)
</dt> <dt>



Impossibile completare l'operazione a causa di cluster non erri su disco.


</dt> </dl> </dd> <dt>

<span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**COMPRESSIONE \_ DEGLI ERRORI NON \_ \_ CONSENTITA NELLA \_ \_ TRANSAZIONE**
</dt> <dd> <dl> <dt>

6850 (0x1AC2)
</dt> <dt>



Impossibile completare l'operazione di compressione perché nel file è attiva una transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**VOLUME \_ DI \_ ERRORE DIRTY**
</dt> <dd> <dl> <dt>

6851 (0x1AC3)
</dt> <dt>



Impossibile completare l'operazione perché il volume è dirty. Eseguire chkdsk e riprovare.


</dt> </dl> </dd> <dt>

<span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**ERRORE \_ NESSUN RILEVAMENTO DEI COLLEGAMENTI NELLA \_ \_ \_ \_ TRANSAZIONE**
</dt> <dd> <dl> <dt>

6852 (0x1AC4)
</dt> <dt>



Impossibile completare l'operazione di rilevamento dei collegamenti perché è attiva una transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**OPERAZIONE \_ DI ERRORE NON SUPPORTATA NELLA \_ \_ \_ \_ TRANSAZIONE**
</dt> <dd> <dl> <dt>

6853 (0x1AC5)
</dt> <dt>



Questa operazione non può essere eseguita in una transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**HANDLE \_ \_ SCADUTO ERRORE**
</dt> <dd> <dl> <dt>

6854 (0x1AC6)
</dt> <dt>



L'handle non è più associato correttamente alla transazione. Potrebbe essere stato aperto in un gestore delle risorse transazionale che è stato successivamente forzato a riavviare. Chiudere l'handle e aprirne uno nuovo.


</dt> </dl> </dd> <dt>

<span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**TRANSAZIONE \_ DI \_ ERRORE NON \_ INTEGRATA**
</dt> <dd> <dl> <dt>

6855 (0x1AC7)
</dt> <dt>



Impossibile eseguire l'operazione specificata perché gestione risorse non è integrata nella transazione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**ERRORE \_ CTX \_ WINSTATION \_ NOME NON \_ VALIDO**
</dt> <dd> <dl> <dt>

7001 (0x1B59)
</dt> <dt>



Il nome di sessione specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**ERRORE \_ CTX \_ \_ PD NON VALIDO**
</dt> <dd> <dl> <dt>

7002 (0x1B5A)
</dt> <dt>



Il driver di protocollo specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**ERRORE \_ CTX \_ PD \_ NON \_ TROVATO**
</dt> <dd> <dl> <dt>

7003 (0x1B5B)
</dt> <dt>



Il driver di protocollo specificato non è stato trovato nel percorso di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**ERRORE \_ CTX \_ WD NON \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

7004 (0x1B5C)
</dt> <dt>



Il driver di connessione terminale specificato non è stato trovato nel percorso di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**ERRORE \_ CTX: \_ IMPOSSIBILE CREARE LA VOCE \_ \_ \_ EVENTLOG**
</dt> <dd> <dl> <dt>

7005 (0x1B5D)
</dt> <dt>



Impossibile creare una chiave del Registro di sistema per la registrazione eventi per questa sessione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**ERRORE \_ DI COLLISIONE DEL NOME \_ DEL \_ SERVIZIO CTX \_**
</dt> <dd> <dl> <dt>

7006 (0x1B5E)
</dt> <dt>



Nel sistema esiste già un servizio con lo stesso nome.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**ERRORE \_ CTX \_ CLOSE \_ PENDING**
</dt> <dd> <dl> <dt>

7007 (0x1B5F)
</dt> <dt>



Un'operazione di chiusura è in sospeso nella sessione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**ERRORE \_ CTX \_ NO \_ OUTBUF**
</dt> <dd> <dl> <dt>

7008 (0x1B60)
</dt> <dt>



Non sono disponibili buffer di output gratuiti.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**ERRORE \_ CTX \_ MODEM \_ INF NON \_ \_ TROVATO**
</dt> <dd> <dl> <dt>

7009 (0x1B61)
</dt> <dt>



The MODEM. File INF non trovato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**ERRORE \_ CTX \_ NOME MODEM NON \_ VALIDO**
</dt> <dd> <dl> <dt>

7010 (0x1B62)
</dt> <dt>



Il nome del modem non è stato trovato in MODEM.INF.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**ERRORE \_ CTX \_ MODEM RESPONSE \_ \_ ERROR**
</dt> <dd> <dl> <dt>

7011 (0x1B63)
</dt> <dt>



Il modem non ha accettato il comando inviato. Verificare che il nome del modem configurato corrisponda al modem collegato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**ERRORE \_ TIMEOUT RISPOSTA MODEM CTX \_ \_ \_**
</dt> <dd> <dl> <dt>

7012 (0x1B64)
</dt> <dt>



Il modem non ha risposto al comando inviato. Verificare che il modem sia cablato e acceso correttamente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**ERRORE \_ CTX \_ MODEM RESPONSE NO \_ \_ \_ CARRIER**
</dt> <dd> <dl> <dt>

7013 (0x1B65)
</dt> <dt>



Il rilevamento del vettore non è riuscito o il vettore è stato eliminato a causa della disconnessione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**ERRORE \_ CTX \_ MODEM RESPONSE NO \_ \_ \_ DIALTONE**
</dt> <dd> <dl> <dt>

7014 (0x1B66)
</dt> <dt>



Segnale acustico non rilevato entro il tempo richiesto. Verificare che il cavo telefonico sia collegato correttamente e funzionante.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**ERRORE \_ RISPOSTA MODEM CTX \_ \_ \_ OCCUPATO**
</dt> <dd> <dl> <dt>

7015 (0x1B67)
</dt> <dt>



Rilevato segnale di occupato nel sito remoto al callback.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**ERRORE \_ CTX \_ MODEM RESPONSE \_ \_ VOICE**
</dt> <dd> <dl> <dt>

7016 (0x1B68)
</dt> <dt>



Voce rilevata nel sito remoto al callback.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**ERRORE \_ CTX \_ TD \_ ERROR**
</dt> <dd> <dl> <dt>

7017 (0x1B69)
</dt> <dt>



Errore del driver di trasporto.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**ERRORE \_ CTX \_ WINSTATION \_ NON \_ TROVATO**
</dt> <dd> <dl> <dt>

7022 (0x1B6E)
</dt> <dt>



Impossibile trovare la sessione specificata.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**ERRORE \_ CTX \_ WINSTATION \_ GIÀ \_ ESISTENTE**
</dt> <dd> <dl> <dt>

7023 (0x1B6F)
</dt> <dt>



Il nome di sessione specificato è già in uso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**ERRORE \_ CTX \_ WINSTATION \_ OCCUPATO**
</dt> <dd> <dl> <dt>

7024 (0x1B70)
</dt> <dt>



L'attività che si sta tentando di eseguire non può essere completata perché Servizi Desktop remoto è attualmente occupato. Riprovare tra alcuni minuti. Altri utenti dovrebbero comunque essere in grado di accedere.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**ERRORE \_ CTX \_ MODALITÀ VIDEO NON \_ \_ INTERATTIVA**
</dt> <dd> <dl> <dt>

7025 (0x1B71)
</dt> <dt>



È stato effettuato un tentativo di connessione a una sessione la cui modalità video non è supportata dal client corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**ERRORE \_ CTX \_ GRAPHICS NON \_ VALIDO**
</dt> <dd> <dl> <dt>

7035 (0x1B7B)
</dt> <dt>



L'applicazione ha tentato di abilitare la modalità grafica DOS. La modalità grafica DOS non è supportata.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**ERRORE \_ CTX \_ LOGON \_ DISABILITATO**
</dt> <dd> <dl> <dt>

7037 (0x1B7D)
</dt> <dt>



Il privilegio di accesso interattivo è stato disabilitato. Contatta l'amministratore.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**ERRORE \_ CTX \_ NOT \_ CONSOLE**
</dt> <dd> <dl> <dt>

7038 (0x1B7E)
</dt> <dt>



L'operazione richiesta può essere eseguita solo nella console di sistema. Questo è molto spesso il risultato di un driver o di una DLL di sistema che richiede l'accesso diretto alla console.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**ERRORE \_ TIMEOUT \_ QUERY CLIENT CTX \_ \_**
</dt> <dd> <dl> <dt>

7040 (0x1B80)
</dt> <dt>



Il client non è riuscito a rispondere al messaggio di connessione del server.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**ERRORE \_ DI DISCONNESSIONE DELLA CONSOLE CTX \_ \_**
</dt> <dd> <dl> <dt>

7041 (0x1B81)
</dt> <dt>



La disconnessione della sessione della console non è supportata.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**ERRORE \_ DI CONNESSIONE DELLA CONSOLE CTX \_ \_**
</dt> <dd> <dl> <dt>

7042 (0x1B82)
</dt> <dt>



La riconnessione di una sessione disconnessa alla console non è supportata.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**ERRORE \_ CTX \_ SHADOW \_ DENIED**
</dt> <dd> <dl> <dt>

7044 (0x1B84)
</dt> <dt>



La richiesta di controllare un'altra sessione in remoto è stata negata.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**ERRORE \_ CTX \_ ACCESSO WINSTATION \_ \_ NEGATO**
</dt> <dd> <dl> <dt>

7045 (0x1B85)
</dt> <dt>



L'accesso alla sessione richiesto è negato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**ERRORE \_ CTX \_ NON VALIDO \_ WD**
</dt> <dd> <dl> <dt>

7049 (0x1B89)
</dt> <dt>



Il driver di connessione terminale specificato non è valido.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**ERRORE \_ CTX \_ SHADOW \_ INVALID**
</dt> <dd> <dl> <dt>

7050 (0x1B8A)
</dt> <dt>



La sessione richiesta non può essere controllata in remoto. È possibile che la sessione sia disconnessa o non abbia attualmente un utente connesso.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**ERRORE \_ CTX \_ SHADOW \_ DISABLED**
</dt> <dd> <dl> <dt>

7051 (0x1B8B)
</dt> <dt>



La sessione richiesta non è configurata per consentire il controllo remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**ERRORE \_ LICENZA CLIENT CTX \_ IN \_ \_ \_ USO**
</dt> <dd> <dl> <dt>

7052 (0x1B8C)
</dt> <dt>



La richiesta di connessione a questo Terminal Server è stata rifiutata. Il numero di licenza client di Terminal Server è attualmente usato da un altro utente. Contattare l'amministratore di sistema per ottenere un numero di licenza univoco.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**ERRORE \_ LICENZA CLIENT CTX \_ NON \_ \_ \_ IMPOSTATA**
</dt> <dd> <dl> <dt>

7053 (0x1B8D)
</dt> <dt>



La richiesta di connessione a questo Terminal Server è stata rifiutata. Il numero di licenza client di Terminal Server non è stato immesso per questa copia del client Terminal Server. Contattare l'amministratore di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**ERRORE \_ LICENZA CTX \_ NON \_ \_ DISPONIBILE**
</dt> <dd> <dl> <dt>

7054 (0x1B8E)
</dt> <dt>



Il numero di connessioni al computer è limitato e tutte le connessioni sono attualmente in uso. Provare a connettersi in un secondo momento o contattare l'amministratore di sistema.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**ERRORE \_ CLIENT DI LICENZA CTX NON \_ \_ \_ VALIDO**
</dt> <dd> <dl> <dt>

7055 (0x1B8F)
</dt> <dt>



Il client in uso non è concesso in licenza per l'uso di questo sistema. La richiesta di accesso viene negata.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**ERRORE \_ LICENZA CTX \_ \_ SCADUTA**
</dt> <dd> <dl> <dt>

7056 (0x1B90)
</dt> <dt>



La licenza di sistema è scaduta. La richiesta di accesso viene negata.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**ERRORE \_ CTX \_ SHADOW NOT \_ \_ RUNNING**
</dt> <dd> <dl> <dt>

7057 (0x1B91)
</dt> <dt>



Impossibile terminare il controllo remoto perché la sessione specificata non è attualmente controllata in remoto.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**ERROR \_ CTX \_ SHADOW \_ ENDED \_ BY \_ MODE \_ CHANGE**
</dt> <dd> <dl> <dt>

7058 (0x1B92)
</dt> <dt>



Il controllo remoto della console è stato terminato perché la modalità di visualizzazione è stata modificata. La modifica della modalità di visualizzazione in una sessione di controllo remoto non è supportata.


</dt> </dl> </dd> <dt>

<span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**NUMERO \_ DI \_ ATTIVAZIONI DI ERRORE \_ SUPERATO**
</dt> <dd> <dl> <dt>

7059 (0x1B93)
</dt> <dt>



L'attivazione è già stata reimpostata per il numero massimo di volte per questa installazione. Il timer di attivazione non verrà cancellato.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**ERRORE \_ CTX \_ WINSTATIONS \_ DISABILITATO**
</dt> <dd> <dl> <dt>

7060 (0x1B94)
</dt> <dt>



Gli account di accesso remoti sono attualmente disabilitati.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**ERRORE \_ LIVELLO DI CRITTOGRAFIA CTX \_ \_ \_ RICHIESTO**
</dt> <dd> <dl> <dt>

7061 (0x1B95)
</dt> <dt>



Non si dispone del livello di crittografia appropriato per accedere a questa sessione.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**ERRORE \_ SESSIONE CTX \_ IN \_ \_ USO**
</dt> <dd> <dl> <dt>

7062 (0x1B96)
</dt> <dt>



L'utente \\ \\ %s %s è attualmente connesso al computer. Solo l'utente corrente o un amministratore può accedere al computer.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**ERRORE \_ CTX \_ NO FORCE \_ \_ LOGOFF**
</dt> <dd> <dl> <dt>

7063 (0x1B97)
</dt> <dt>



L'utente \\ \\ %s %s è già connesso alla console di questo computer. Non si dispone dell'autorizzazione per accedere al momento. Per risolvere il problema, contattare %s \\ \\ %s e disconnettersi.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**ERRORE \_ CTX \_ ACCOUNT \_ RESTRICTION**
</dt> <dd> <dl> <dt>

7064 (0x1B98)
</dt> <dt>



Non è possibile accedere a causa di una restrizione dell'account.


</dt> </dl> </dd> <dt>

<span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**ERRORE \_ DEL PROTOCOLLO \_ \_ RDP**
</dt> <dd> <dl> <dt>

7065 (0x1B99)
</dt> <dt>



Il componente del protocollo RDP %2 ha rilevato un errore nel flusso del protocollo e ha disconnesso il client.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**ERRORE \_ CTX \_ CDM \_ CONNECT**
</dt> <dd> <dl> <dt>

7066 (0x1B9A)
</dt> <dt>



Il servizio mapping unità client si è connesso alla connessione terminale.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**ERRORE \_ CTX \_ CDM \_ DISCONNECT**
</dt> <dd> <dl> <dt>

7067 (0x1B9B)
</dt> <dt>



Il servizio mapping unità client si è disconnesso alla connessione terminale.


</dt> </dl> </dd> <dt>

<span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**ERRORE \_ DEL LIVELLO DI SICUREZZA CTX \_ \_ \_**
</dt> <dd> <dl> <dt>

7068 (0x1B9C)
</dt> <dt>



Il livello di sicurezza di Terminal Server ha rilevato un errore nel flusso del protocollo e ha disconnesso il client.


</dt> </dl> </dd> <dt>

<span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**ERRORE \_ TS \_ SESSIONI INCOMPATIBILI \_**
</dt> <dd> <dl> <dt>

7069 (0x1B9D)
</dt> <dt>



La sessione di destinazione non è compatibile con la sessione corrente.


</dt> </dl> </dd> <dt>

<span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**ERRORE \_ DEL \_ SOTTOSISTEMA VIDEO \_ TS \_**
</dt> <dd> <dl> <dt>

7070 (0x1B9E)
</dt> <dt>



Windows non è in grado di connettersi alla sessione perché si è verificato un problema nel sottosistema Windows video. Provare a connettersi di nuovo in un secondo momento oppure contattare l'amministratore del server per assistenza.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**SEQUENZA DI \_ API FRS ERR \_ NON \_ \_ VALIDA**
</dt> <dd> <dl> <dt>

8001 (0x1F41)
</dt> <dt>



L'API del servizio Replica file è stata chiamata in modo non corretto.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**SERVIZIO DI AVVIO \_ DI FRS ERR \_ \_**
</dt> <dd> <dl> <dt>

8002 (0x1F42)
</dt> <dt>



Non è possibile avviare il servizio replica file.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**FRS \_ ERR \_ STOPPING \_ SERVICE**
</dt> <dd> <dl> <dt>

8003 (0x1F43)
</dt> <dt>



Il servizio replica file non può essere arrestato.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**API INTERNA FRS \_ ERR \_ \_**
</dt> <dd> <dl> <dt>

8004 (0x1F44)
</dt> <dt>



L'API del servizio Replica file ha terminato la richiesta. Il registro eventi può contenere altre informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**FRS \_ ERR \_ INTERNAL**
</dt> <dd> <dl> <dt>

8005 (0x1F45)
</dt> <dt>



Il servizio di replica file ha terminato la richiesta. Il registro eventi può contenere altre informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**FRS \_ ERR \_ SERVICE \_ COMM**
</dt> <dd> <dl> <dt>

8006 (0x1F46)
</dt> <dt>



Non è possibile contattare il servizio replica file. Il registro eventi può contenere altre informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**FRS \_ ERR \_ INSUFFICIENT \_ PRIV**
</dt> <dd> <dl> <dt>

8007 (0x1F47)
</dt> <dt>



Il servizio replica file non è in grado di soddisfare la richiesta perché i privilegi dell'utente non sono sufficienti. Il registro eventi può contenere altre informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**AUTENTICAZIONE FRS \_ \_ ERR**
</dt> <dd> <dl> <dt>

8008 (0x1F48)
</dt> <dt>



Il servizio replica file non è in grado di soddisfare la richiesta perché la RPC autenticata non è disponibile. Il registro eventi può contenere altre informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**FRS \_ ERR \_ PARENT \_ INSUFFICIENT \_ PRIV**
</dt> <dd> <dl> <dt>

8009 (0x1F49)
</dt> <dt>



Il servizio replica file non è in grado di soddisfare la richiesta perché l'utente non dispone di privilegi sufficienti sul controller di dominio. Il registro eventi può contenere altre informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**AUTENTICAZIONE PADRE \_ FRS ERR \_ \_**
</dt> <dd> <dl> <dt>

8010 (0x1F4A)
</dt> <dt>



Il servizio replica file non è in grado di soddisfare la richiesta perché la rpc autenticata non è disponibile nel controller di dominio. Il registro eventi può contenere altre informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**FRS \_ ERR \_ CHILD \_ TO \_ PARENT \_ COMM**
</dt> <dd> <dl> <dt>

8011 (0x1F4B)
</dt> <dt>



Il servizio replica file non può comunicare con il servizio replica file nel controller di dominio. Il registro eventi può contenere altre informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**FRS \_ ERR \_ DA PADRE A \_ \_ \_ COMM FIGLIO**
</dt> <dd> <dl> <dt>

8012 (0x1F4C)
</dt> <dt>



Il servizio Replica file nel controller di dominio non può comunicare con il servizio replica file nel computer. Il registro eventi può contenere altre informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**FRS \_ ERR \_ SYSVOL \_ POPULATE**
</dt> <dd> <dl> <dt>

8013 (0x1F4D)
</dt> <dt>



Il servizio replica file non è in grado di popolare il volume di sistema a causa di un errore interno. Il registro eventi può contenere altre informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**\_FRS ERR \_ SYSVOL \_ POPULATE TIMEOUT (TIMEOUT POPOLAMENTO SYSVOL FRS \_ ERR)**
</dt> <dd> <dl> <dt>

8014 (0x1F4E)
</dt> <dt>



Il servizio replica file non è in grado di popolare il volume di sistema a causa di un timeout interno. Il registro eventi può contenere altre informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**FRS \_ ERR \_ SYSVOL \_ È \_ OCCUPATO**
</dt> <dd> <dl> <dt>

8015 (0x1F4F)
</dt> <dt>



Il servizio replica file non è in grado di elaborare la richiesta. Il volume di sistema è occupato con una richiesta precedente.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**FRS \_ ERR \_ SYSVOL \_ DEMOTE**
</dt> <dd> <dl> <dt>

8016 (0x1F50)
</dt> <dt>



Il servizio replica file non è in grado di arrestare la replica del volume di sistema a causa di un errore interno. Il registro eventi può contenere altre informazioni.


</dt> </dl> </dd> <dt>

<span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**PARAMETRO DEL SERVIZIO \_ FRS ERR \_ \_ NON \_ VALIDO**
</dt> <dd> <dl> <dt>

8017 (0x1F51)
</dt> <dt>



Il servizio replica file ha rilevato un parametro non valido.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Winerror</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di errore di sistema](system-error-codes.md)
</dt> </dl>

 

 




