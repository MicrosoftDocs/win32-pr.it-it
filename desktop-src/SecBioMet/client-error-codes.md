---
title: Codici di errore client (Winbio \_ err.h)
description: Codici di errore definiti nel file di intestazione \_ Winbio err.h.
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
ms.openlocfilehash: bcb8450b85eaa6c49b66a3a86789c126cc04b9a661a7e4c5074784f8cba6bf72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993841"
---
# <a name="client-error-codes"></a>Codici di errore del client

I codici di errore seguenti sono definiti nel file di intestazione \_ Winbio err.h.



| Costante/valore                                                                                                                                                                                                                                                                                         | Descrizione                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_E_UNSUPPORTED_FACTOR"></span><span id="winbio_e_unsupported_factor"></span><dl> <dt>**WINBIO \_ E \_ UNSUPPORTED \_ FACTOR**</dt> <dt>0x80098001</dt> </dl>                              | Il fattore biometrico specificato non è supportato.<br/>                                                       |
| <span id="WINBIO_E_INVALID_UNIT"></span><span id="winbio_e_invalid_unit"></span><dl> <dt>**WINBIO \_ E \_ UNITÀ \_ NON**</dt> VALIDA <dt>0x80098002</dt> </dl>                                                | Il numero ID unità non corrisponde a un dispositivo biometrico valido.<br/>                                    |
| <span id="WINBIO_E_UNKNOWN_ID"></span><span id="winbio_e_unknown_id"></span><dl> <dt>**WINBIO \_ E \_ ID \_ SCONOSCIUTO**</dt> <dt>0x80098003</dt> </dl>                                                      | L'esempio biometrico non corrisponde ad alcuna identità nota.<br/>                                                |
| <span id="WINBIO_E_CANCELED"></span><span id="winbio_e_canceled"></span><dl> <dt>**WINBIO \_ E \_ CANCELED**</dt> <dt>0x80098004</dt> </dl>                                                             | L'operazione biometrica è stata annullata prima del completamento.<br/>                                         |
| <span id="WINBIO_E_NO_MATCH"></span><span id="winbio_e_no_match"></span><dl> <dt>**WINBIO \_ E \_ NESSUNA \_ CORRISPONDENZA**</dt> <dt>0x80098005</dt> </dl>                                                            | Il campione biometrico non corrisponde all'identità o al fattore secondario specificato.<br/>                              |
| <span id="WINBIO_E_CAPTURE_ABORTED"></span><span id="winbio_e_capture_aborted"></span><dl> <dt>**WINBIO \_ E \_ CAPTURE \_ ABORTED**</dt> <dt>0x80098006</dt> </dl>                                       | Non è stato possibile acquisire un campione biometrico perché l'operazione di acquisizione è stata interrotta.<br/>                    |
| <span id="WINBIO_E_ENROLLMENT_IN_PROGRESS"></span><span id="winbio_e_enrollment_in_progress"></span><dl> <dt>**WINBIO \_ REGISTRAZIONE \_ \_ IN CORSO \_ 0X80098007**</dt> <dt></dt> </dl>                 | Non è stato possibile iniziare una transazione di registrazione perché è già in corso un'altra registrazione.<br/>      |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <dt>**WINBIO \_ E \_ BAD \_ CAPTURE**</dt> <dt>0x80098008</dt> </dl>                                                   | L'esempio acquisito non può essere usato per ulteriori operazioni biometriche.<br/>                                   |
| <span id="WINBIO_E_INVALID_CONTROL_CODE"></span><span id="winbio_e_invalid_control_code"></span><dl> <dt>**WINBIO \_ E \_ CODICE DI CONTROLLO NON \_ \_ VALIDO**</dt> <dt>0x80098009</dt> </dl>                       | L'unità biometrica non supporta il codice di controllo unità specificato.<br/>                                   |
| <span id="WINBIO_E_DATA_COLLECTION_IN_PROGRESS"></span><span id="winbio_e_data_collection_in_progress"></span><dl> <dt>**WINBIO \_ E \_ RACCOLTA DATI IN CORSO \_ \_ \_ 0X8009800B**</dt> <dt></dt> </dl> | È già in corso un'operazione di raccolta dati in sospeso.<br/>                                            |
| <span id="WINBIO_E_UNSUPPORTED_DATA_FORMAT"></span><span id="winbio_e_unsupported_data_format"></span><dl> <dt>**WINBIO \_ E \_ FORMATO DATI NON \_ \_ SUPPORTATO**</dt> <dt>0x8009800C</dt> </dl>              | Il driver del sensore biometrico non supporta il formato dati richiesto.<br/>                                |
| <span id="WINBIO_E_UNSUPPORTED_DATA_TYPE"></span><span id="winbio_e_unsupported_data_type"></span><dl> <dt>**WINBIO \_ E \_ TIPO DI DATI NON \_ \_ SUPPORTATO**</dt> <dt>0x8009800D</dt> </dl>                    | Il driver del sensore biometrico non supporta il tipo di dati richiesto.<br/>                                  |
| <span id="WINBIO_E_UNSUPPORTED_PURPOSE"></span><span id="winbio_e_unsupported_purpose"></span><dl> <dt>**WINBIO \_ E \_ SCOPO \_ NON SUPPORTATO**</dt> <dt>0x8009800E</dt> </dl>                           | Il driver del sensore biometrico non supporta lo scopo dei dati richiesti.<br/>                               |
| <span id="WINBIO_E_INVALID_DEVICE_STATE"></span><span id="winbio_e_invalid_device_state"></span><dl> <dt>**WINBIO \_ E \_ STATO DISPOSITIVO NON VALIDO \_ \_ 0x8009800F**</dt> <dt></dt> </dl>                       | L'unità biometrica non è nello stato corretto per eseguire l'operazione specificata.<br/>                      |
| <span id="WINBIO_E_DEVICE_BUSY"></span><span id="winbio_e_device_busy"></span><dl> <dt>**WINBIO \_ E \_ DISPOSITIVO \_ OCCUPATO**</dt> <dt>0X80098010</dt> </dl>                                                   | Non è stato possibile eseguire l'operazione perché il dispositivo sensore era occupato.<br/>                               |
| <span id="WINBIO_E_DATABASE_CANT_CREATE"></span><span id="winbio_e_database_cant_create"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ CANT \_ CREATE**</dt> <dt>0x80098011</dt> </dl>                       | L'adattatore di archiviazione non è riuscito a creare un nuovo database.<br/>                                             |
| <span id="WINBIO_E_DATABASE_CANT_OPEN"></span><span id="winbio_e_database_cant_open"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ CANT \_ OPEN**</dt> <dt>0x80098012</dt> </dl>                             | L'adattatore di archiviazione non è stato in grado di aprire un database esistente.<br/>                                         |
| <span id="WINBIO_E_DATABASE_CANT_CLOSE"></span><span id="winbio_e_database_cant_close"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ CANT \_ CLOSE**</dt> <dt>0x80098013</dt> </dl>                          | L'adattatore di archiviazione non è riuscito a chiudere un database.<br/>                                                  |
| <span id="WINBIO_E_DATABASE_CANT_ERASE"></span><span id="winbio_e_database_cant_erase"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ CANT \_ ERASE**</dt> <dt>0x80098014</dt> </dl>                          | La scheda di archiviazione non è stata in grado di cancellare un database.<br/>                                                  |
| <span id="WINBIO_E_DATABASE_CANT_FIND"></span><span id="winbio_e_database_cant_find"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ CANT \_ FIND**</dt> <dt>0x80098015</dt> </dl>                             | L'adattatore di archiviazione non è riuscito a trovare un database.<br/>                                                   |
| <span id="WINBIO_E_DATABASE_ALREADY_EXISTS"></span><span id="winbio_e_database_already_exists"></span><dl> <dt>**WINBIO \_ E \_ DATABASE ALREADY EXISTS \_ \_ 0x80098016**</dt> <dt></dt> </dl>              | L'adattatore di archiviazione non è riuscito a creare un database perché il database specificato esiste già.<br/>   |
| <span id="WINBIO_E_DATABASE_FULL"></span><span id="winbio_e_database_full"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ FULL**</dt> <dt>0x80098018</dt> </dl>                                             | L'adattatore di archiviazione non è stato in grado di aggiungere un record al database perché il database è pieno.<br/>         |
| <span id="WINBIO_E_DATABASE_LOCKED"></span><span id="winbio_e_database_locked"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ BLOCCATO**</dt> <dt>0x80098019</dt> </dl>                                       | Il database è bloccato e il relativo contenuto non è accessibile.<br/>                                              |
| <span id="WINBIO_E_DATABASE_CORRUPTED"></span><span id="winbio_e_database_corrupted"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ DANNEGGIATO**</dt> <dt>0x8009801A</dt> </dl>                              | Il contenuto del database è danneggiato e non è accessibile.<br/>                               |
| <span id="WINBIO_E_DATABASE_NO_SUCH_RECORD"></span><span id="winbio_e_database_no_such_record"></span><dl> <dt>**WINBIO \_ E \_ DATABASE NO SUCH \_ \_ \_ RECORD**</dt> <dt>0X8009801B</dt> </dl>             | Nessun record è stato eliminato perché l'identità e il fattore secondario specificati non sono presenti nel database.<br/> |
| <span id="WINBIO_E_DUPLICATE_ENROLLMENT"></span><span id="winbio_e_duplicate_enrollment"></span><dl> <dt>**WINBIO \_ E \_ DUPLICATE \_ ENROLLMENT**</dt> <dt>0x8009801C</dt> </dl>                        | L'identità e il fattore secondario specificati sono già registrati nel database.<br/>                            |
| <span id="WINBIO_E_DATABASE_READ_ERROR"></span><span id="winbio_e_database_read_error"></span><dl> <dt>**WINBIO \_ E \_ DATABASE READ ERROR \_ \_ 0x8009801D**</dt> <dt></dt> </dl>                          | Si è verificato un errore durante il tentativo di lettura dal database.<br/>                                              |
| <span id="WINBIO_E_DATABASE_WRITE_ERROR"></span><span id="winbio_e_database_write_error"></span><dl> <dt>**WINBIO \_ E \_ DATABASE WRITE ERROR \_ \_ 0x8009801E**</dt> <dt></dt> </dl>                       | Si è verificato un errore nel tentativo di scrivere nel database.<br/>                                               |
| <span id="WINBIO_E_DATABASE_NO_RESULTS"></span><span id="winbio_e_database_no_results"></span><dl> <dt>**WINBIO \_ E \_ DATABASE NO RESULTS \_ \_ 0x8009801F**</dt> <dt></dt> </dl>                          | Nessun record nel database corrisponde alla query.<br/>                                                          |
| <span id="WINBIO_E_DATABASE_NO_MORE_RECORDS"></span><span id="winbio_e_database_no_more_records"></span><dl> <dt>**WINBIO \_ E \_ DATABASE NO MORE \_ \_ \_ RECORDS**</dt> <dt>0X80098020</dt> </dl>          | Sono stati recuperati tutti i record della query di database più recente.<br/>                                   |
| <span id="WINBIO_E_DATABASE_EOF"></span><span id="winbio_e_database_eof"></span><dl> <dt>**WINBIO \_ E \_ DATABASE \_ EOF**</dt> <dt>0x80098021</dt> </dl>                                                | Un'operazione di database ha rilevato in modo imprevisto la fine del file.<br/>                                     |
| <span id="WINBIO_E_DATABASE_BAD_INDEX_VECTOR"></span><span id="winbio_e_database_bad_index_vector"></span><dl> <dt>**WINBIO \_ E \_ DATABASE BAD INDEX \_ \_ \_ VECTOR**</dt> <dt>0x80098022</dt> </dl>       | Operazione di database non riuscita a causa di un vettore di indice in formato non valido.<br/>                                           |
| <span id="WINBIO_E_INCORRECT_BSP"></span><span id="winbio_e_incorrect_bsp"></span><dl> <dt>**WINBIO \_ E \_ \_ ERRATO BSP**</dt> <dt>0x80098024</dt> </dl>                                             | L'unità biometrica non appartiene al provider di servizi specificato.<br/>                                  |
| <span id="WINBIO_E_INCORRECT_SENSOR_POOL"></span><span id="winbio_e_incorrect_sensor_pool"></span><dl> <dt>**WINBIO \_ E \_ POOL DI SENSORI \_ \_ NON**</dt> <dt>0X80098025</dt> </dl>                    | L'unità biometrica non appartiene al pool di sensori specificato.<br/>                                       |
| <span id="WINBIO_E_NO_CAPTURE_DATA"></span><span id="winbio_e_no_capture_data"></span><dl> <dt>**WINBIO \_ E \_ NO \_ CAPTURE \_ DATA**</dt> <dt>0x80098026</dt> </dl>                                      | Il buffer di acquisizione dell'adattatore del sensore è vuoto.<br/>                                                            |
| <span id="WINBIO_E_INVALID_SENSOR_MODE"></span><span id="winbio_e_invalid_sensor_mode"></span><dl> <dt>**WINBIO \_ E \_ MODALITÀ SENSORE NON \_ \_ VALIDA**</dt> <dt>0X80098027</dt> </dl>                          | L'adattatore del sensore non supporta la modalità sensore specificata nella configurazione.<br/>                    |
| <span id="WINBIO_E_LOCK_VIOLATION"></span><span id="winbio_e_lock_violation"></span><dl> <dt>**WINBIO \_ E \_ \_ VIOLAZIONE DI**</dt> <dt>0X8009802A</dt> </dl>                                          | Impossibile eseguire l'operazione richiesta a causa di un conflitto di blocco.<br/>                                 |
| <span id="WINBIO_E_DUPLICATE_TEMPLATE"></span><span id="winbio_e_duplicate_template"></span><dl> <dt>**WINBIO \_ E \_ \_ DUPLICA MODELLO**</dt> <dt>0x8009802B</dt> </dl>                              | I dati in un modello biometrico corrispondono a quello di un altro modello già presente nel database.<br/>             |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <dt>**WINBIO \_ E \_ OPERAZIONE \_ NON VALIDA**</dt> <dt>0x8009802C</dt> </dl>                                 | L'operazione richiesta non è valida per lo stato corrente della sessione o per l'unità biometrica.<br/>       |
| <span id="WINBIO_E_SESSION_BUSY"></span><span id="winbio_e_session_busy"></span><dl> <dt>**WINBIO \_ E \_ SESSIONE \_ OCCUPATA**</dt> <dt>0X8009802D</dt> </dl>                                                | La sessione non può iniziare una nuova operazione perché è già in corso un'altra operazione.<br/>             |
| <span id="WINBIO_E_CRED_PROV_DISABLED"></span><span id="winbio_e_cred_prov_disabled"></span><dl> <dt>**WINBIO \_ E \_ CRED \_ PROV \_ DISABLED**</dt> <dt>0x80098030</dt> </dl>                             | Le impostazioni dei criteri di sistema hanno disabilitato il provider di credenziali biometriche.<br/>                                |
| <span id="WINBIO_E_CRED_PROV_NO_CREDENTIAL"></span><span id="winbio_e_cred_prov_no_credential"></span><dl> <dt>**WINBIO \_ E \_ CRED \_ PROV \_ NO \_ CREDENTIAL**</dt> <dt>0x80098031</dt> </dl>             | La credenziale richiesta non è stata trovata.<br/>                                                                |
| <span id="WINBIO_E_DISABLED"></span><span id="winbio_e_disabled"></span><dl> <dt>**WINBIO \_ E \_ DISABLED**</dt> <dt>0x80098032</dt> </dl>                                                             | Le impostazioni dei criteri di sistema hanno disabilitato il servizio biometrico.<br/>                                            |
| <span id="WINBIO_E_CONFIGURATION_FAILURE"></span><span id="winbio_e_configuration_failure"></span><dl> <dt>**WINBIO \_ ERRORE \_ DI \_ CONFIGURAZIONE**</dt> <dt>0X80098033</dt> </dl>                     | Impossibile configurare l'unità biometrica.<br/>                                                            |
| <span id="WINBIO_E_SENSOR_UNAVAILABLE"></span><span id="winbio_e_sensor_unavailable"></span><dl> <dt>**WINBIO \_ E \_ SENSOR \_ UNAVAILABLE**</dt> <dt>0x80098034</dt> </dl>                              | Non è possibile creare un pool privato perché una o più unità biometriche non sono disponibili.<br/>                |
| <span id="WINBIO_E_SAS_ENABLED"></span><span id="winbio_e_sas_enabled"></span><dl> <dt>**WINBIO \_ E \_ SAS \_ ENABLED**</dt> <dt>0x80098035</dt> </dl>                                                   | Per l'accesso è necessaria una sequenza di attenzione sicura (CTRL+ALT+CANC).<br/>                                   |
| <span id="WINBIO_E_DEVICE_FAILURE"></span><span id="winbio_e_device_failure"></span><dl> <dt>**WINBIO \_ E \_ ERRORE \_ DEL**</dt> DISPOSITIVO <dt>0x80098036</dt> </dl>                                          | Un sensore biometrico ha avuto esito negativo.<br/>                                                                         |
| <span id="WINBIO_E_FAST_USER_SWITCH_DISABLED"></span><span id="winbio_e_fast_user_switch_disabled"></span><dl> <dt>**WINBIO \_ E \_ FAST CAMBIO UTENTE DISABILITATO \_ \_ \_ 0x80098037**</dt> <dt></dt> </dl>       | >cambio utente rapido è disabilitato.<br/>                                                                   |
| <span id="WINBIO_E_NOT_ACTIVE_CONSOLE"></span><span id="winbio_e_not_active_console"></span><dl> <dt>**WINBIO \_ E \_ NON ATTIVA CONSOLE \_ \_ 0x80098038**</dt> <dt></dt> </dl>                             | Non è possibile aprire il pool di sensori di sistema dalle sessioni client di Terminal Server.<br/>                          |
| <span id="WINBIO_E_EVENT_MONITOR_ACTIVE"></span><span id="winbio_e_event_monitor_active"></span><dl> <dt>**WINBIO \_ E \_ EVENT \_ MONITOR \_ ACTIVE**</dt> <dt>0x80098039</dt> </dl>                      | Alla sessione specificata è già associato un monitoraggio eventi attivo.<br/>                        |
| <span id="WINBIO_E_INVALID_PROPERTY_TYPE"></span><span id="winbio_e_invalid_property_type"></span><dl> <dt>**WINBIO \_ E \_ TIPO DI PROPRIETÀ \_ \_ NON**</dt> <dt>VALIDO 0x8009803A</dt> </dl>                    | Il valore specificato non è un tipo di proprietà valido.<br/>                                                      |
| <span id="WINBIO_E_INVALID_PROPERTY_ID"></span><span id="winbio_e_invalid_property_id"></span><dl> <dt>**WINBIO \_ E \_ ID PROPRIETÀ NON \_ \_ VALIDO**</dt> <dt>0x8009803B</dt> </dl>                          | Il valore specificato non è un ID di proprietà valido.<br/>                                                        |
| <span id="WINBIO_E_UNSUPPORTED_PROPERTY"></span><span id="winbio_e_unsupported_property"></span><dl> <dt>**WINBIO \_ E \_ UNSUPPORTED \_ PROPERTY**</dt> <dt>0x8009803C</dt> </dl>                        | L'unità biometrica non supporta la proprietà specificata.<br/>                                            |
| <span id="WINBIO_E_ADAPTER_INTEGRITY_FAILURE"></span><span id="winbio_e_adapter_integrity_failure"></span><dl> <dt>**WINBIO \_ ERRORE \_ DI \_ INTEGRITÀ \_ DELL'ADAPTER E**</dt> <dt>0X8009803D</dt> </dl>        | L'adapter non ha superato il controllo di integrità.<br/>                                                          |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <dt>**WINBIO \_ I \_ MORE \_ DATA**</dt> <dt>0x00090001</dt> </dl>                                                         | È necessario un altro esempio per il modello di registrazione corrente.<br/>                                          |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ err.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti dell'applicazione client](client-application-constants.md)
</dt> </dl>

 

 





