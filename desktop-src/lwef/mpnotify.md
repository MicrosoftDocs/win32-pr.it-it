---
title: Enumerazione MPNOTIFY (MpClient. h)
description: Possibili notifiche di callback.
ms.assetid: CCD0CD89-2C6E-453F-9437-E6ED87AD9F29
keywords:
- Funzionalità dell'ambiente Windows legacy dell'enumerazione MPNOTIFY
- Funzionalità dell'ambiente Windows legacy del puntatore di enumerazione PMPNOTIFY
topic_type:
- apiref
api_name:
- MPNOTIFY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afa0eeb6cb1d610f28cc82f578617f7bd71cf886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301946"
---
# <a name="mpnotify-enumeration"></a>Enumerazione MPNOTIFY

Possibili notifiche di callback.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagMPNOTIFY { 
  MPNOTIFY_NONE,
  MPNOTIFY_CALL_START,
  MPNOTIFY_CALL_COMPLETE,
  MPNOTIFY_INTERNAL_FAILURE,
  MPNOTIFY_STATUS_SERVICE_START,
  MPNOTIFY_STATUS_SERVICE_RUNNING,
  MPNOTIFY_STATUS_SERVICE_STOP,
  MPNOTIFY_STATUS_COMPONENT,
  MPNOTIFY_STATUS_CHANGE,
  MPNOTIFY_STATUS_COMPONENT_CONFIGURATION,
  MPNOTIFY_STATUS_EXPIRATION_CHANGE,
  MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE,
  MPNOTIFY_SCAN_START,
  MPNOTIFY_SCAN_PAUSED,
  MPNOTIFY_SCAN_RESUMED,
  MPNOTIFY_SCAN_CANCEL,
  MPNOTIFY_SCAN_COMPLETE,
  MPNOTIFY_SCAN_PROGRESS,
  MPNOTIFY_SCAN_ERROR,
  MPNOTIFY_SCAN_INFECTED,
  MPNOTIFY_SCAN_MEMORYSTART,
  MPNOTIFY_SCAN_MEMORYCOMPLETE,
  MPNOTIFY_SCAN_SFC_BUILD_START,
  MPNOTIFY_SCAN_SFC_BUILD_COMPLETE,
  MPNOTIFY_SCAN_FASTPATH_START,
  MPNOTIFY_SCAN_FASTPATH_COMPLETE,
  MPNOTIFY_SCAN_FASTPATH_PROGRESS,
  MPNOTIFY_CLEAN_START,
  MPNOTIFY_CLEAN_COMPLETE,
  MPNOTIFY_CLEAN_RESTOREPOINT_START,
  MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED,
  MPNOTIFY_CLEAN_RESTOREPOINT_FAILED,
  MPNOTIFY_CLEAN_THREAT_START,
  MPNOTIFY_CLEAN_THREAT_SUCCEEDED,
  MPNOTIFY_CLEAN_THREAT_FAILED,
  MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED,
  MPNOTIFY_CLEAN_RESOURCE_FAILED,
  MPNOTIFY_CLEAN_THREAT_COMPLETE,
  MPNOTIFY_PRECHECK_START,
  MPNOTIFY_PRECHECK_COMPLETE,
  MPNOTIFY_PRECHECK_RESOURCE_BLOCKED,
  MPNOTIFY_THREAT_DETECTED,
  MPNOTIFY_THREAT_MODIFIED,
  MPNOTIFY_THREAT_CLEAN_SUCCEEDED,
  MPNOTIFY_THREAT_CLEAN_FAILED,
  MPNOTIFY_THREAT_ABANDONED,
  MPNOTIFY_THREAT_CLEAN_EVENT_START,
  MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE,
  MPNOTIFY_SIGUPDATE_START,
  MPNOTIFY_SIGUPDATE_SEARCH_START,
  MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE,
  MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_START,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE,
  MPNOTIFY_SIGUPDATE_INSTALL_START,
  MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS,
  MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE,
  MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED,
  MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED,
  MPNOTIFY_SIGUPDATE_COMPLETE,
  MPNOTIFY_SAMPLE_START,
  MPNOTIFY_SAMPLE_COMPLETE,
  MPNOTIFY_SAMPLE_ITEM_START,
  MPNOTIFY_SAMPLE_ITEM_SUCCEEDED,
  MPNOTIFY_SAMPLE_ITEM_FAILED,
  MPNOTIFY_RESERVED_DATA,
  MPNOTIFY_FASTPATH_SIG_ADDED,
  MPNOTIFY_FASTPATH_SIG_REMOVED,
  MPNOTIFY_NIS_PRIVATE,
  MPNOTIFY_HEALTH_CHANGE,
  MPNOTIFY_HEALTH_RECOVERY,
  MPNOTIFY_HEALTH_START,
  MPNOTIFY_ENDOFLIFE_CHANGE,
  MPNOTIFY_MALWARETOAST_DATA
} MPNOTIFY, *PMPNOTIFY;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**MPNOTIFY \_ None**
</dt> <dd></dd> <dt>

<span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**\_inizio chiamata \_ MPNOTIFY**
</dt> <dd>

Avvio della chiamata di notifica.

</dd> <dt>

<span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**\_chiamata MPNOTIFY \_ completata**
</dt> <dd>

Chiamata di notifica completata.

</dd> <dt>

<span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**\_errore interno \_ MPNOTIFY**
</dt> <dd>

Errore interno generico.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**\_ \_ avvio servizio stato \_ MPNOTIFY**
</dt> <dd>

Il servizio malware Protection è stato avviato.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**\_servizio stato \_ MPNOTIFY \_ in esecuzione**
</dt> <dd>

Il servizio malware Protection è in esecuzione.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**\_ \_ arresto servizio stato \_ MPNOTIFY**
</dt> <dd>

Il servizio malware Protection è stato arrestato.

</dd> <dt>

<span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**\_componente stato \_ MPNOTIFY**
</dt> <dd>

Stato di abilitazione/disabilitazione del componente specifico.

</dd> <dt>

<span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**\_modifica stato \_ MPNOTIFY**
</dt> <dd>

Lo stato generale del prodotto è stato modificato. Chiamare [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md) per ottenere lo stato corrente.

</dd> <dt>

<span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**\_configurazione del \_ componente \_ stato MPNOTIFY**
</dt> <dd>

Un particolare componente ha modificato la configurazione.

</dd> <dt>

<span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**\_ \_ modifica scadenza stato \_ MPNOTIFY**
</dt> <dd>

Lo stato di scadenza del prodotto è stato modificato.

</dd> <dt>

<span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**\_ \_ \_ modifica analisi offline stato \_ MPNOTIFY**
</dt> <dd>

Stato di analisi non in linea obbligatorio modificato.

</dd> <dt>

<span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**\_avvio dell'analisi MPNOTIFY \_**
</dt> <dd>

Analisi avviata.

</dd> <dt>

<span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**\_analisi MPNOTIFY \_ sospesa**
</dt> <dd>

Analisi sospesa.

</dd> <dt>

<span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**\_analisi MPNOTIFY \_ ripresa**
</dt> <dd>

analisi ripresa.

</dd> <dt>

<span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**\_annullamento dell'analisi MPNOTIFY \_**
</dt> <dd>

Analisi annullata.

</dd> <dt>

<span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**\_analisi MPNOTIFY \_ completata**
</dt> <dd>

Analisi completata.

</dd> <dt>

<span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**\_stato analisi \_ MPNOTIFY**
</dt> <dd>

Notifica di stato per la risorsa specifica sottoposta a scansione.

</dd> <dt>

<span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**\_errore di analisi MPNOTIFY \_**
</dt> <dd>

Errore durante l'analisi di una determinata risorsa. L'analisi continuerà comunque.

</dd> <dt>

<span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**\_analisi MPNOTIFY \_ infettata**
</dt> <dd>

L'analisi ha rilevato una risorsa infetta.

</dd> <dt>

<span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**MPNOTIFY \_ Scan \_ MEMORYSTART**
</dt> <dd>

L'analisi dello stato di avanzamento per notificare la parte dell'analisi di sistema è stata avviata.

</dd> <dt>

<span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**MPNOTIFY \_ Scan \_ MEMORYCOMPLETE**
</dt> <dd>

Analisi dello stato di avanzamento per notificare la porzione di analisi della memoria del sistema completata.

</dd> <dt>

<span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**\_ \_ \_ avvio compilazione SFC MPNOTIFY \_ Scan**
</dt> <dd>

Lo stato di avanzamento dell'analisi per notificare la compilazione SFC è stato avviato.

</dd> <dt>

<span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**\_compilazione SFC di MPNOTIFY Scan \_ \_ \_ completata**
</dt> <dd>

Analisi dello stato di avanzamento per notificare la parte di compilazione SFC completata.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**avvio di MPNOTIFY \_ Scan \_ FastPath \_**
</dt> <dd>

L'analisi FastPath SpyNet è iniziata.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**\_FastPath MPNOTIFY \_ Scan \_ completato**
</dt> <dd>

Analisi FastPath SpyNet terminata.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**MPNOTIFY \_ Scan \_ FastPath- \_ stato**
</dt> <dd>

Notifica sullo stato di avanzamento per le ripetizioni FastPath, utilizzate internamente e convertite nello **\_ \_ stato di analisi MPNOTIFY** per l'esterno.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**\_Inizio pulizia \_ MPNOTIFY**
</dt> <dd>

Pulizia avviata.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**\_pulizia MPNOTIFY \_ completata**
</dt> <dd>

Pulizia completata.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**MPNOTIFY \_ Clean \_ RESTOREPOINT \_ Start**
</dt> <dd>

Avvio della creazione di un punto di ripristino del sistema.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**MPNOTIFY \_ Clean \_ RESTOREPOINT \_ riuscita**
</dt> <dd>

Creazione del punto di ripristino del sistema completata.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**\_RESTOREPOINT Clean \_ MPNOTIFY \_ non riuscita**
</dt> <dd>

Impossibile creare il punto di ripristino del sistema.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**\_avvio della \_ minaccia MPNOTIFY Clean \_**
</dt> <dd>

Viene avviata la pulizia per una minaccia specifica.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**\_minaccia MPNOTIFY \_ pulita \_ riuscita**
</dt> <dd>

La pulizia è riuscita per una minaccia specifica.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**\_minaccia MPNOTIFY \_ Clean \_ non riuscita**
</dt> <dd>

La pulizia non è riuscita per una minaccia specifica. **Errore \_ Il codice di errore della \_ minaccia MP \_ non \_ trovato** indica che la minaccia non è stata trovata (e non è un errore di pulizia).

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**\_risorsa pulita \_ MPNOTIFY \_ riuscita**
</dt> <dd>

La pulizia è riuscita per una determinata risorsa.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**\_risorsa pulita \_ MPNOTIFY \_ non riuscita**
</dt> <dd>

La pulizia non è riuscita per una determinata risorsa.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**MPNOTIFY \_ una \_ minaccia pulita \_ completa**
</dt> <dd>

La pulizia è stata completata per una minaccia specifica.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**\_avvio della PREVERIFICA MPNOTIFY \_**
</dt> <dd>

Verifica preliminare pulita avviata.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**\_PRECONTROLLO MPNOTIFY \_ completato**
</dt> <dd>

Pulizia Preverifica completata.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**\_risorsa PREVERIFICA \_ MPNOTIFY \_ bloccata**
</dt> <dd>

Pulire la Preverifica della risorsa bloccata rilevata.

</dd> <dt>

<span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**è \_ stata \_ rilevata una minaccia MPNOTIFY**
</dt> <dd>

Nuova minaccia rilevata nel sistema.

</dd> <dt>

<span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**\_minaccia MPNOTIFY \_ modificata**
</dt> <dd>

Informazioni sulle minacce modificate. Ad esempio, è stata aggiunta una nuova risorsa.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**la \_ pulizia della minaccia MPNOTIFY è \_ \_ riuscita**
</dt> <dd>

L'azione di pulizia è riuscita per una minaccia.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**la \_ pulizia della minaccia MPNOTIFY \_ \_ non è riuscita**
</dt> <dd>

Azione di pulizia non riuscita per una minaccia. **Errore \_ Il codice di errore della \_ minaccia MP \_ non \_ trovato** indica che la minaccia non è stata trovata (e non è un errore di pulizia).

</dd> <dt>

<span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**\_minaccia MPNOTIFY \_ abbandonata**
</dt> <dd>

Non è stata eseguita alcuna correzione prima dell'arresto del servizio.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**\_ \_ \_ inizio evento MPNOTIFY Threat \_ clean**
</dt> <dd>

È stata avviata un'azione di pulizia.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**\_evento MPNOTIFY \_ Threat \_ Clean \_ completato**
</dt> <dd>

È stata terminata un'azione di pulizia.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**\_inizio MPNOTIFY SIGUPDATE \_**
</dt> <dd>

Aggiornamento della firma avviato.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**\_avvio della \_ ricerca \_ SIGUPDATE di MPNOTIFY**
</dt> <dd>

Ricerca degli aggiornamenti avviata.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**\_ricerca MPNOTIFY \_ SIGUPDATE \_ completata**
</dt> <dd>

Ricerca degli aggiornamenti completata.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**\_ \_ aggiornamento software MPNOTIFY \_ SIGUPDATE \_ disponibile**
</dt> <dd>

Aggiornamento software disponibile.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**avvio del download di MPNOTIFY \_ SIGUPDATE \_ \_**
</dt> <dd>

Download avviato.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**stato del download di MPNOTIFY \_ SIGUPDATE \_ \_**
</dt> <dd>

Il download è in corso. I dati di callback contengono lo stato di avanzamento.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**Download di MPNOTIFY \_ SIGUPDATE \_ \_ completato**
</dt> <dd>

Download completato.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**\_ \_ avvio installazione di MPNOTIFY SIGUPDATE \_**
</dt> <dd>

Installazione avviata.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**stato di installazione di MPNOTIFY \_ SIGUPDATE \_ \_**
</dt> <dd>

Installazione in corso. I dati di callback contengono lo stato di avanzamento.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**installazione di MPNOTIFY \_ SIGUPDATE \_ \_ completata**
</dt> <dd>

Installazione completata.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**riavvio di MPNOTIFY \_ SIGUPDATE \_ \_ obbligatorio**
</dt> <dd>

Aggiornamento richiede il riavvio.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**\_richiesta SIGUPDATE \_ MPNOTIFY \_ elaborata**
</dt> <dd>

Il servizio ha elaborato una richiesta di aggiornamento della firma. Esito negativo o esito positivo è indicato da **HRESULT** nei dati di callback.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ completata**
</dt> <dd>

Aggiornamento completato. **S \_ FALSE** Status indica che non è necessario alcun aggiornamento.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**\_inizio dell'esempio MPNOTIFY \_**
</dt> <dd>

Invio di esempio avviato.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**\_esempio MPNOTIFY \_ completato**
</dt> <dd>

Invio di esempio completato.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**\_inizio dell' \_ elemento di esempio MPNOTIFY \_**
</dt> <dd>

Invio di elementi di esempio specifico avviato. L'indice degli elementi di esempio è disponibile nei [**\_ dati MPSAMPLE**](mpsample-data.md).

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**\_elemento di esempio MPNOTIFY \_ \_ riuscito**
</dt> <dd>

Invio specifico di un elemento di esempio completato.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**\_elemento di esempio MPNOTIFY \_ \_ non riuscito**
</dt> <dd>

Invio specifico di un elemento di esempio non riuscito. Il codice di errore è disponibile nei [**\_ dati di MPCALLBACK**](mpcallback-data.md).

</dd> <dt>

<span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**MPNOTIFY \_ \_ dati riservati**
</dt> <dd>

Dati riservati interni.

</dd> <dt>

<span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**MPNOTIFY \_ FastPath \_ sig \_ aggiunto**
</dt> <dd>

Una firma FastPath ha aggiunto o disabilitato una firma.

</dd> <dt>

<span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**MPNOTIFY \_ FastPath \_ sig \_ rimosso**
</dt> <dd>

È stata rimossa una firma FastPath.

</dd> <dt>

<span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**MPNOTIFY \_ NIS \_ privato**
</dt> <dd>

Notifiche privato NIS. Non è necessario che i partner si registrino a questo.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**\_Modifica integrità \_ MPNOTIFY**
</dt> <dd>

Il servizio AM è entrato in uno stato nuovo.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**\_ripristino integrità \_ MPNOTIFY**
</dt> <dd>

Il servizio AM è stato recuperato da uno stato.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**\_inizio integrità \_ MPNOTIFY**
</dt> <dd>

Il servizio AM ha inizializzato l'integrità del sistema.

</dd> <dt>

<span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**\_modifica MPNOTIFY ENDOFLIFE \_**
</dt> <dd>

Le date di scadenza per il servizio AM sono state modificate.

</dd> <dt>

<span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**\_dati MALWARETOAST di MPNOTIFY \_**
</dt> <dd>

Il servizio AM ha rilevato malware che potrebbe aver causato la modifica delle impostazioni critiche nel computer.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md)
</dt> <dt>

[**\_dati MPCALLBACK**](mpcallback-data.md)
</dt> <dt>

[**\_dati MPSAMPLE**](mpsample-data.md)
</dt> </dl>

 

 





