---
title: Codici di errore client (WinBio \_ Err. h)
description: Codici di errore definiti nel \_ file di intestazione WinBio Err. h.
ms.assetid: fc1565d2-43f1-45cd-ab84-4e557cf78107
topic_type:
- apiref
api_name:
- WINBIO_E_UNSUPPORTED_FACTOR
- WINBIO_E_INVALID_UNIT
- WINBIO_E_UNKNOWN_ID
- WINBIO_E_CANCELED
- WINBIO_E_NO_MATCH
- WINBIO_E_CAPTURE_ABORTED
- WINBIO_E_ENROLLMENT_IN_PROGRESS
- WINBIO_E_BAD_CAPTURE
- WINBIO_E_INVALID_CONTROL_CODE
- WINBIO_E_DATA_COLLECTION_IN_PROGRESS
- WINBIO_E_UNSUPPORTED_DATA_FORMAT
- WINBIO_E_UNSUPPORTED_DATA_TYPE
- WINBIO_E_UNSUPPORTED_PURPOSE
- WINBIO_E_INVALID_DEVICE_STATE
- WINBIO_E_DEVICE_BUSY
- WINBIO_E_DATABASE_CANT_CREATE
- WINBIO_E_DATABASE_CANT_OPEN
- WINBIO_E_DATABASE_CANT_CLOSE
- WINBIO_E_DATABASE_CANT_ERASE
- WINBIO_E_DATABASE_CANT_FIND
- WINBIO_E_DATABASE_ALREADY_EXISTS
- WINBIO_E_DATABASE_FULL
- WINBIO_E_DATABASE_LOCKED
- WINBIO_E_DATABASE_CORRUPTED
- WINBIO_E_DATABASE_NO_SUCH_RECORD
- WINBIO_E_DUPLICATE_ENROLLMENT
- WINBIO_E_DATABASE_READ_ERROR
- WINBIO_E_DATABASE_WRITE_ERROR
- WINBIO_E_DATABASE_NO_RESULTS
- WINBIO_E_DATABASE_NO_MORE_RECORDS
- WINBIO_E_DATABASE_EOF
- WINBIO_E_DATABASE_BAD_INDEX_VECTOR
- WINBIO_E_INCORRECT_BSP
- WINBIO_E_INCORRECT_SENSOR_POOL
- WINBIO_E_NO_CAPTURE_DATA
- WINBIO_E_INVALID_SENSOR_MODE
- WINBIO_E_LOCK_VIOLATION
- WINBIO_E_DUPLICATE_TEMPLATE
- WINBIO_E_INVALID_OPERATION
- WINBIO_E_SESSION_BUSY
- WINBIO_E_CRED_PROV_DISABLED
- WINBIO_E_CRED_PROV_NO_CREDENTIAL
- WINBIO_E_DISABLED
- WINBIO_E_CONFIGURATION_FAILURE
- WINBIO_E_SENSOR_UNAVAILABLE
- WINBIO_E_SAS_ENABLED
- WINBIO_E_DEVICE_FAILURE
- WINBIO_E_FAST_USER_SWITCH_DISABLED
- WINBIO_E_NOT_ACTIVE_CONSOLE
- WINBIO_E_EVENT_MONITOR_ACTIVE
- WINBIO_E_INVALID_PROPERTY_TYPE
- WINBIO_E_INVALID_PROPERTY_ID
- WINBIO_E_UNSUPPORTED_PROPERTY
- WINBIO_E_ADAPTER_INTEGRITY_FAILURE
- WINBIO_I_MORE_DATA
api_location:
- Winbio_err.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 000723612a2f7f9f5575fc767924d4d6c697468a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048668"
---
# <a name="client-error-codes"></a>Codici di errore client

I codici di errore seguenti vengono definiti nel \_ file di intestazione WinBio Err. h.



| Costante/valore                                                                                                                                                                                                                                                                                         | Descrizione                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_E_UNSUPPORTED_FACTOR"></span><span id="winbio_e_unsupported_factor"></span><dl> <dt>**WINBIO \_ E \_ \_ fattore**</dt> <dt>0x80098001</dt> non supportato </dl>                              | Il fattore biometrico specificato non è supportato.<br/>                                                       |
| <span id="WINBIO_E_INVALID_UNIT"></span><span id="winbio_e_invalid_unit"></span><dl> <dt>**WINBIO \_ 0x80098002 \_ \_ unità E non valido**</dt> <dt></dt> </dl>                                                | Il numero ID unità non corrisponde a un dispositivo biometrico valido.<br/>                                    |
| <span id="WINBIO_E_UNKNOWN_ID"></span><span id="winbio_e_unknown_id"></span><dl> <dt>**WINBIO \_ \_ \_ ID sconosciuto E**</dt> <dt>0x80098003</dt> </dl>                                                      | L'esempio Biometric non corrisponde ad alcuna identità nota.<br/>                                                |
| <span id="WINBIO_E_CANCELED"></span><span id="winbio_e_canceled"></span><dl> <dt>**WINBIO \_ E \_ 0x80098004 annullato**</dt> <dt></dt> </dl>                                                             | L'operazione biometrica è stata annullata prima del completamento.<br/>                                         |
| <span id="WINBIO_E_NO_MATCH"></span><span id="winbio_e_no_match"></span><dl> <dt>**WINBIO \_ E \_ Nessuna \_ corrispondenza**</dt> <dt>0x80098005</dt> </dl>                                                            | L'esempio Biometric non corrisponde all'identità o al Sottofattore specificato.<br/>                              |
| <span id="WINBIO_E_CAPTURE_ABORTED"></span><span id="winbio_e_capture_aborted"></span><dl> <dt>**WINBIO \_ Acquisizione E 0x80098006 \_ \_ interrotti**</dt> <dt></dt> </dl>                                       | Non è stato possibile acquisire un campione biometrico perché l'operazione di acquisizione è stata interrotta.<br/>                    |
| <span id="WINBIO_E_ENROLLMENT_IN_PROGRESS"></span><span id="winbio_e_enrollment_in_progress"></span><dl> <dt>**WINBIO \_ \_Registrazione E \_ in \_ corso**</dt> <dt>0x80098007</dt> </dl>                 | Non è stato possibile avviare una transazione di registrazione perché è già in corso un'altra registrazione.<br/>      |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <dt>**WINBIO \_ 0x80098008 \_ di \_ acquisizione E non valido**</dt> <dt></dt> </dl>                                                   | Non è possibile usare l'esempio acquisito per altre operazioni biometriche.<br/>                                   |
| <span id="WINBIO_E_INVALID_CONTROL_CODE"></span><span id="winbio_e_invalid_control_code"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ codice di controllo non valido**</dt> <dt>0x80098009</dt> </dl>                       | L'unità biometrica non supporta il codice di controllo unità specificato.<br/>                                   |
| <span id="WINBIO_E_DATA_COLLECTION_IN_PROGRESS"></span><span id="winbio_e_data_collection_in_progress"></span><dl> <dt>**WINBIO \_ E \_ \_ raccolta dati \_ in \_ corso**</dt> <dt>0x8009800B</dt> </dl> | È già in corso un'operazione di raccolta dati in sospeso.<br/>                                            |
| <span id="WINBIO_E_UNSUPPORTED_DATA_FORMAT"></span><span id="winbio_e_unsupported_data_format"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ formato dati non supportato**</dt> <dt>0x8009800C</dt> </dl>              | Il driver del sensore biometrico non supporta il formato di dati richiesto.<br/>                                |
| <span id="WINBIO_E_UNSUPPORTED_DATA_TYPE"></span><span id="winbio_e_unsupported_data_type"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ tipo di dati**</dt> <dt>0x8009800D</dt> non supportato </dl>                    | Il driver del sensore biometrico non supporta il tipo di dati richiesto.<br/>                                  |
| <span id="WINBIO_E_UNSUPPORTED_PURPOSE"></span><span id="winbio_e_unsupported_purpose"></span><dl> <dt>**WINBIO \_ E \_ \_ scopo**</dt> <dt>0x8009800E</dt> non supportato </dl>                           | Il driver del sensore biometrico non supporta lo scopo dei dati richiesti.<br/>                               |
| <span id="WINBIO_E_INVALID_DEVICE_STATE"></span><span id="winbio_e_invalid_device_state"></span><dl> <dt>**WINBIO \_ E \_ 0x8009800F \_ \_ stato dispositivo non valido**</dt> <dt></dt> </dl>                       | L'unità biometrica non è nello stato appropriato per eseguire l'operazione specificata.<br/>                      |
| <span id="WINBIO_E_DEVICE_BUSY"></span><span id="winbio_e_device_busy"></span><dl> <dt>**WINBIO \_ 0x80098010 \_ dispositivo E \_ occupato**</dt> <dt></dt> </dl>                                                   | Non è stato possibile eseguire l'operazione perché il dispositivo sensore era occupato.<br/>                               |
| <span id="WINBIO_E_DATABASE_CANT_CREATE"></span><span id="winbio_e_database_cant_create"></span><dl> <dt>**WINBIO \_ \_ \_ \_ Creazione**</dt> di <dt>0x80098011</dt> nel database E non riuscita </dl>                       | L'adattatore di archiviazione non è stato in grado di creare un nuovo database.<br/>                                             |
| <span id="WINBIO_E_DATABASE_CANT_OPEN"></span><span id="winbio_e_database_cant_open"></span><dl> <dt>**WINBIO \_ 0x80098012 del database E non \_ \_ \_ aperto**</dt> <dt></dt> </dl>                             | L'adattatore di archiviazione non è stato in grado di aprire un database esistente.<br/>                                         |
| <span id="WINBIO_E_DATABASE_CANT_CLOSE"></span><span id="winbio_e_database_cant_close"></span><dl> <dt>**WINBIO \_ 0x80098013 \_ di \_ \_ chiusura del database E**</dt> <dt></dt> </dl>                          | L'adattatore di archiviazione non è stato in grado di chiudere un database.<br/>                                                  |
| <span id="WINBIO_E_DATABASE_CANT_ERASE"></span><span id="winbio_e_database_cant_erase"></span><dl> <dt>**WINBIO \_ 0x80098014 \_ di \_ \_ cancellazione del database E**</dt> <dt></dt> </dl>                          | L'adattatore di archiviazione non è stato in grado di cancellare un database.<br/>                                                  |
| <span id="WINBIO_E_DATABASE_CANT_FIND"></span><span id="winbio_e_database_cant_find"></span><dl> <dt>**WINBIO \_ Non è stato \_ \_ \_ trovato**</dt> alcun <dt>0x80098015</dt> del database E </dl>                             | L'adattatore di archiviazione non è stato in grado di trovare un database.<br/>                                                   |
| <span id="WINBIO_E_DATABASE_ALREADY_EXISTS"></span><span id="winbio_e_database_already_exists"></span><dl> <dt>**WINBIO \_ Il \_ database \_ E \_ esiste già**</dt> <dt>0x80098016</dt> </dl>              | L'adattatore di archiviazione non è stato in grado di creare un database perché il database specificato esiste già.<br/>   |
| <span id="WINBIO_E_DATABASE_FULL"></span><span id="winbio_e_database_full"></span><dl> <dt>**WINBIO \_ 0x80098018 \_ \_ completo del database E**</dt> <dt></dt> </dl>                                             | L'adattatore di archiviazione non è stato in grado di aggiungere un record al database perché il database è pieno.<br/>         |
| <span id="WINBIO_E_DATABASE_LOCKED"></span><span id="winbio_e_database_locked"></span><dl> <dt>**WINBIO \_ E \_ database \_ bloccato**</dt> <dt>0x80098019</dt> </dl>                                       | Il database è bloccato e il relativo contenuto non è accessibile.<br/>                                              |
| <span id="WINBIO_E_DATABASE_CORRUPTED"></span><span id="winbio_e_database_corrupted"></span><dl> <dt>**WINBIO \_ 0x8009801A \_ \_ danneggiato del database E**</dt> <dt></dt> </dl>                              | Il contenuto del database è stato danneggiato e non è accessibile.<br/>                               |
| <span id="WINBIO_E_DATABASE_NO_SUCH_RECORD"></span><span id="winbio_e_database_no_such_record"></span><dl> <dt>**WINBIO \_ \_Database E \_ nessun \_ \_ record di questo tipo**</dt> <dt>0x8009801B</dt> </dl>             | Nessun record è stato eliminato perché l'identità e il fattore secondario specificati non sono presenti nel database.<br/> |
| <span id="WINBIO_E_DUPLICATE_ENROLLMENT"></span><span id="winbio_e_duplicate_enrollment"></span><dl> <dt>**WINBIO \_ E 0x8009801C di \_ \_ registrazione duplicati**</dt> <dt></dt> </dl>                        | L'identità e il Sottofattore specificati sono già registrati nel database.<br/>                            |
| <span id="WINBIO_E_DATABASE_READ_ERROR"></span><span id="winbio_e_database_read_error"></span><dl> <dt>**WINBIO \_ \_Errore di \_ lettura \_ del database E**</dt> <dt>0x8009801D</dt> </dl>                          | Si è verificato un errore durante il tentativo di lettura dal database.<br/>                                              |
| <span id="WINBIO_E_DATABASE_WRITE_ERROR"></span><span id="winbio_e_database_write_error"></span><dl> <dt>**WINBIO \_ \_Errore di \_ scrittura \_ del database E**</dt> <dt>0x8009801E</dt> </dl>                       | Si è verificato un errore nel tentativo di scrivere nel database.<br/>                                               |
| <span id="WINBIO_E_DATABASE_NO_RESULTS"></span><span id="winbio_e_database_no_results"></span><dl> <dt>**WINBIO \_ \_Database E \_ senza \_ risultati**</dt> <dt>0x8009801F</dt> </dl>                          | Nessun record nel database corrispondente alla query.<br/>                                                          |
| <span id="WINBIO_E_DATABASE_NO_MORE_RECORDS"></span><span id="winbio_e_database_no_more_records"></span><dl> <dt>**WINBIO \_ \_Database E \_ non \_ più \_ record**</dt> <dt>0x80098020</dt> </dl>          | Sono stati recuperati tutti i record della query di database più recente.<br/>                                   |
| <span id="WINBIO_E_DATABASE_EOF"></span><span id="winbio_e_database_eof"></span><dl> <dt>**WINBIO \_ E \_ database \_ EOF**</dt> <dt>0x80098021</dt> </dl>                                                | Un'operazione di database ha rilevato in modo imprevisto la fine del file.<br/>                                     |
| <span id="WINBIO_E_DATABASE_BAD_INDEX_VECTOR"></span><span id="winbio_e_database_bad_index_vector"></span><dl> <dt>**WINBIO \_ 0x80098022 \_ \_ \_ \_ Vector index non valido del database E**</dt> <dt></dt> </dl>       | Un'operazione sul database non è riuscita a causa di un vettore di indice non valido.<br/>                                           |
| <span id="WINBIO_E_INCORRECT_BSP"></span><span id="winbio_e_incorrect_bsp"></span><dl> <dt>**WINBIO \_ 0x80098024 \_ \_ BSP errato**</dt> <dt></dt> </dl>                                             | L'unità biometrica non appartiene al provider di servizi specificato.<br/>                                  |
| <span id="WINBIO_E_INCORRECT_SENSOR_POOL"></span><span id="winbio_e_incorrect_sensor_pool"></span><dl> <dt>**WINBIO \_ 0x80098025 \_ \_ \_ pool di sensori errato E**</dt> <dt></dt> </dl>                    | L'unità biometrica non appartiene al pool di sensori specificato.<br/>                                       |
| <span id="WINBIO_E_NO_CAPTURE_DATA"></span><span id="winbio_e_no_capture_data"></span><dl> <dt>**WINBIO \_ E \_ nessun \_ \_ dato di acquisizione**</dt> <dt>0x80098026</dt> </dl>                                      | Il buffer di acquisizione dell'adattatore del sensore è vuoto.<br/>                                                            |
| <span id="WINBIO_E_INVALID_SENSOR_MODE"></span><span id="winbio_e_invalid_sensor_mode"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ modalità sensore non valida**</dt> <dt>0x80098027</dt> </dl>                          | L'adattatore del sensore non supporta la modalità del sensore specificata nella configurazione.<br/>                    |
| <span id="WINBIO_E_LOCK_VIOLATION"></span><span id="winbio_e_lock_violation"></span><dl> <dt>**WINBIO \_ 0x8009802A \_ \_ violazione di blocco E**</dt> <dt></dt> </dl>                                          | Impossibile eseguire l'operazione richiesta a causa di un conflitto di blocco.<br/>                                 |
| <span id="WINBIO_E_DUPLICATE_TEMPLATE"></span><span id="winbio_e_duplicate_template"></span><dl> <dt>**WINBIO \_ E \_ \_ modello duplicato**</dt> <dt>0x8009802B</dt> </dl>                              | I dati in un modello biometrico corrispondono a quelli di un altro modello già presente nel database.<br/>             |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <dt>**WINBIO \_ E \_ 0x8009802C \_ operazione non valida**</dt> <dt></dt> </dl>                                 | L'operazione richiesta non è valida per lo stato corrente della sessione o dell'unità biometrica.<br/>       |
| <span id="WINBIO_E_SESSION_BUSY"></span><span id="winbio_e_session_busy"></span><dl> <dt>**WINBIO \_ 0x8009802D \_ \_ occupato della sessione E**</dt> <dt></dt> </dl>                                                | La sessione non può iniziare una nuova operazione perché è già in corso un'altra operazione.<br/>             |
| <span id="WINBIO_E_CRED_PROV_DISABLED"></span><span id="winbio_e_cred_prov_disabled"></span><dl> <dt>**WINBIO \_ E \_ cred \_ prov \_ disabled**</dt> <dt>0x80098030</dt> </dl>                             | Le impostazioni dei criteri di sistema hanno disabilitato il provider di credenziali biometrico.<br/>                                |
| <span id="WINBIO_E_CRED_PROV_NO_CREDENTIAL"></span><span id="winbio_e_cred_prov_no_credential"></span><dl> <dt>**WINBIO \_ E \_ creda \_ \_ Nessuna \_ credenziale**</dt> <dt>0x80098031</dt> </dl>             | Impossibile trovare la credenziale richiesta.<br/>                                                                |
| <span id="WINBIO_E_DISABLED"></span><span id="winbio_e_disabled"></span><dl> <dt>**WINBIO \_ E \_ disabilitato**</dt> <dt>0x80098032</dt> </dl>                                                             | Le impostazioni dei criteri di sistema hanno disabilitato il servizio biometrico.<br/>                                            |
| <span id="WINBIO_E_CONFIGURATION_FAILURE"></span><span id="winbio_e_configuration_failure"></span><dl> <dt>**WINBIO \_ \_ \_ Errore di configurazione E**</dt> <dt>0x80098033</dt> </dl>                     | Non è stato possibile configurare l'unità biometrica.<br/>                                                            |
| <span id="WINBIO_E_SENSOR_UNAVAILABLE"></span><span id="winbio_e_sensor_unavailable"></span><dl> <dt>**WINBIO \_ \_Sensore E \_**</dt> <dt>0x80098034</dt> non disponibile </dl>                              | Non è possibile creare un pool privato perché una o più unità biometriche non sono disponibili.<br/>                |
| <span id="WINBIO_E_SAS_ENABLED"></span><span id="winbio_e_sas_enabled"></span><dl> <dt>**WINBIO \_ 0x80098035 \_ SAS \_ abilitato**</dt> <dt></dt> </dl>                                                   | Per l'accesso è necessaria una sequenza di attenzione sicura (CTRL + ALT + CANC).<br/>                                   |
| <span id="WINBIO_E_DEVICE_FAILURE"></span><span id="winbio_e_device_failure"></span><dl> <dt>**WINBIO \_ \_ \_ Errore del dispositivo E**</dt> <dt>0x80098036</dt> </dl>                                          | Un sensore biometrico non è riuscito.<br/>                                                                         |
| <span id="WINBIO_E_FAST_USER_SWITCH_DISABLED"></span><span id="winbio_e_fast_user_switch_disabled"></span><dl> <dt>**WINBIO \_ E \_ \_ switch utente \_ veloce \_ disabilitato**</dt> <dt>0x80098037</dt> </dl>       | >cambio rapido utente è disabilitato.<br/>                                                                   |
| <span id="WINBIO_E_NOT_ACTIVE_CONSOLE"></span><span id="winbio_e_not_active_console"></span><dl> <dt>**WINBIO \_ 0x80098038 \_ \_ \_ console E non attiva**</dt> <dt></dt> </dl>                             | Non è possibile aprire il pool di sensori di sistema da sessioni client Terminal Server.<br/>                          |
| <span id="WINBIO_E_EVENT_MONITOR_ACTIVE"></span><span id="winbio_e_event_monitor_active"></span><dl> <dt>**WINBIO \_ E \_ \_ monitoraggio eventi \_ attivi**</dt> <dt>0x80098039</dt> </dl>                      | È già presente un monitoraggio eventi attivo associato alla sessione specificata.<br/>                        |
| <span id="WINBIO_E_INVALID_PROPERTY_TYPE"></span><span id="winbio_e_invalid_property_type"></span><dl> <dt>**WINBIO \_ E \_ il \_ \_ tipo di proprietà**</dt> <dt>0x8009803A</dt> non è valido </dl>                    | Il valore specificato non è un tipo di proprietà valido.<br/>                                                      |
| <span id="WINBIO_E_INVALID_PROPERTY_ID"></span><span id="winbio_e_invalid_property_id"></span><dl> <dt>**WINBIO \_ E \_ \_ \_ ID proprietà non valido**</dt> <dt>0x8009803B</dt> </dl>                          | Il valore specificato non è un ID di proprietà valido.<br/>                                                        |
| <span id="WINBIO_E_UNSUPPORTED_PROPERTY"></span><span id="winbio_e_unsupported_property"></span><dl> <dt>**WINBIO \_ E \_ \_ proprietà non supportata**</dt> <dt>0x8009803C</dt> </dl>                        | L'unità biometrica non supporta la proprietà specificata.<br/>                                            |
| <span id="WINBIO_E_ADAPTER_INTEGRITY_FAILURE"></span><span id="winbio_e_adapter_integrity_failure"></span><dl> <dt>**WINBIO \_ \_Errore di \_ integrità \_ dell'adapter E**</dt> <dt>0x8009803D</dt> </dl>        | L'adapter non ha superato il controllo di integrità.<br/>                                                          |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <dt>**WINBIO \_ \_Maggiore 0x00090001 \_ dati**</dt> <dt></dt> </dl>                                                         | Per il modello di registrazione corrente è necessario un altro esempio.<br/>                                          |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>WinBio \_ Err. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





