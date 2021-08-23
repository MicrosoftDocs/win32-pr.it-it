---
title: Enumerazione MPNOTIFY (MpClient.h)
description: Possibili notifiche di callback.
ms.assetid: CCD0CD89-2C6E-453F-9437-E6ED87AD9F29
keywords:
- Enumerazione MPNOTIFY Funzionalità dell'Windows legacy
- Puntatore di enumerazione PMPNOTIFY Legacy Windows'ambiente
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
ms.openlocfilehash: ed62a9f868aa39cbc0cfc7702afc99849005a22106892696eca857ffb20673af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747789"
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

<span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**MPNOTIFY \_ NONE**
</dt> <dd></dd> <dt>

<span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**MPNOTIFY \_ CALL \_ START**
</dt> <dd>

Avvio della chiamata di notifica.

</dd> <dt>

<span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**CHIAMATA MPNOTIFY \_ \_ COMPLETATA**
</dt> <dd>

Chiamata di notifica completata.

</dd> <dt>

<span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**ERRORE INTERNO \_ \_ MPNOTIFY**
</dt> <dd>

Errore interno generico.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**MPNOTIFY \_ STATUS \_ SERVICE \_ START**
</dt> <dd>

Il servizio di protezione da malware è stato avviato.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**SERVIZIO DI STATO MPNOTIFY \_ \_ IN \_ ESECUZIONE**
</dt> <dd>

Il servizio di protezione da malware è in esecuzione.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**MPNOTIFY \_ STATUS \_ SERVICE \_ STOP**
</dt> <dd>

Il servizio di protezione da malware è stato arrestato.

</dd> <dt>

<span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**COMPONENTE DI STATO \_ \_ MPNOTIFY**
</dt> <dd>

Stato di abilitazione/disabilitazione di un componente specifico.

</dd> <dt>

<span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**MODIFICA DELLO STATO \_ DI MPNOTIFY \_**
</dt> <dd>

Lo stato complessivo del prodotto è cambiato. Chiamare [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md) per ottenere lo stato corrente.

</dd> <dt>

<span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**CONFIGURAZIONE DEL COMPONENTE \_ DI STATO MPNOTIFY \_ \_**
</dt> <dd>

La configurazione di un determinato componente è stata modificata.

</dd> <dt>

<span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**MODIFICA SCADENZA STATO MPNOTIFY \_ \_ \_**
</dt> <dd>

Lo stato di scadenza del prodotto è stato modificato.

</dd> <dt>

<span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**MODIFICA ANALISI \_ \_ OFFLINE STATO \_ MPNOTIFY \_**
</dt> <dd>

Lo stato richiesto per l'analisi offline è cambiato.

</dd> <dt>

<span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**MPNOTIFY \_ SCAN \_ START**
</dt> <dd>

Analisi avviata.

</dd> <dt>

<span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**ANALISI MPNOTIFY \_ \_ SOSPESA**
</dt> <dd>

Analisi sospesa.

</dd> <dt>

<span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**ANALISI MPNOTIFY \_ \_ RIPRESA**
</dt> <dd>

analisi ripresa.

</dd> <dt>

<span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**MPNOTIFY \_ SCAN \_ CANCEL**
</dt> <dd>

Analisi annullata.

</dd> <dt>

<span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**ANALISI MPNOTIFY \_ \_ COMPLETATA**
</dt> <dd>

Analisi completata.

</dd> <dt>

<span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**MPNOTIFY \_ SCAN \_ PROGRESS**
</dt> <dd>

Notifica dello stato di avanzamento per la risorsa specifica analizzata.

</dd> <dt>

<span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**ERRORE DI ANALISI \_ \_ MPNOTIFY**
</dt> <dd>

Errore durante l'analisi di una determinata risorsa. L'analisi continuerà comunque.

</dd> <dt>

<span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**MPNOTIFY \_ SCAN \_ INFECTED**
</dt> <dd>

L'analisi ha rilevato una risorsa infetto.

</dd> <dt>

<span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**MPNOTIFY \_ SCAN \_ MEMORYSTART**
</dt> <dd>

Stato dell'analisi per notificare l'avvio della parte di analisi della memoria dell'analisi del sistema.

</dd> <dt>

<span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**MPNOTIFY \_ SCAN \_ MEMORYCOMPLETE**
</dt> <dd>

Stato dell'analisi per notificare il completamento dell'analisi della memoria dell'analisi del sistema.

</dd> <dt>

<span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**MPNOTIFY \_ SCAN \_ SFC \_ BUILD \_ START**
</dt> <dd>

Analizzare lo stato di avanzamento per notificare l'avvio della parte di compilazione sfc.

</dd> <dt>

<span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**MPNOTIFY \_ SCAN \_ SFC \_ BUILD \_ COMPLETE**
</dt> <dd>

Analizzare lo stato di avanzamento per notificare il completamento della parte di compilazione sfc.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**MPNOTIFY \_ SCAN \_ FASTPATH \_ START**
</dt> <dd>

L'analisi di fastpath spynet è iniziata.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**MPNOTIFY \_ SCAN \_ FASTPATH \_ COMPLETE**
</dt> <dd>

L'analisi di fastpath spynet è terminata.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**MPNOTIFY \_ SCAN \_ FASTPATH \_ PROGRESS**
</dt> <dd>

Notifica dello stato di avanzamento per le analisi fastpath, usata internamente e convertita in **MPNOTIFY \_ SCAN \_ PROGRESS** per l'esterno.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**AVVIO PULIZIA \_ \_ MPNOTIFY**
</dt> <dd>

Pulizia avviata.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**MPNOTIFY \_ CLEAN \_ COMPLETE**
</dt> <dd>

Pulizia completata.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**MPNOTIFY \_ CLEAN \_ RESTOREPOINT \_ START**
</dt> <dd>

È stato avviato il processo di creazione di un punto di ripristino del sistema.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**MPNOTIFY \_ CLEAN \_ RESTOREPOINT \_ SUCCEEDED**
</dt> <dd>

Il punto di ripristino del sistema è stato creato correttamente.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**MPNOTIFY \_ CLEAN \_ RESTOREPOINT \_ FAILED**
</dt> <dd>

Creazione del punto di ripristino del sistema non riuscita.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**MPNOTIFY \_ CLEAN \_ THREAT \_ START**
</dt> <dd>

Viene avviata la pulizia per una determinata minaccia.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**MPNOTIFY \_ CLEAN \_ THREAT \_ SUCCEEDED**
</dt> <dd>

La pulizia viene completata per una determinata minaccia.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**MPNOTIFY \_ CLEAN \_ THREAT \_ FAILED**
</dt> <dd>

La pulizia non è riuscita per una determinata minaccia. **ERRORE \_ Il codice di errore MP \_ THREAT \_ NOT \_ FOUND** (MINACCIA NON TROVATA) indica che la minaccia non è stata trovata (e non è un errore da pulire).

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**LA RISORSA PULITA MPNOTIFY \_ \_ È \_ RIUSCITA**
</dt> <dd>

La pulizia viene completata per una determinata risorsa.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**LA RISORSA PULITA MPNOTIFY \_ \_ NON È \_ RIUSCITA**
</dt> <dd>

Pulizia non riuscita per una determinata risorsa.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**MPNOTIFY \_ CLEAN \_ THREAT \_ COMPLETE**
</dt> <dd>

La pulizia è stata completata per una determinata minaccia.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**MPNOTIFY \_ PRECHECK \_ START**
</dt> <dd>

Pulizia della verifica preliminare avviata.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**MPNOTIFY \_ PRECHECK \_ COMPLETE**
</dt> <dd>

Pulizia della verifica preliminare completata.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**MPNOTIFY \_ PRECHECK \_ RESOURCE \_ BLOCKED**
</dt> <dd>

Pulisci verifica preliminare rilevata risorsa bloccata.

</dd> <dt>

<span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**RILEVATA MINACCIA MPNOTIFY \_ \_**
</dt> <dd>

Nuova minaccia rilevata nel sistema.

</dd> <dt>

<span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**MODIFICA DELLA \_ MINACCIA MPNOTIFY \_**
</dt> <dd>

Informazioni sulle minacce modificate. Ad esempio, è stata aggiunta una nuova risorsa.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**MPNOTIFY \_ THREAT \_ CLEAN \_ SUCCEEDED**
</dt> <dd>

L'azione di pulizia è riuscita per una minaccia.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**MPNOTIFY \_ THREAT \_ CLEAN \_ FAILED**
</dt> <dd>

L'azione di pulizia non è riuscita per una minaccia. **ERRORE \_ Il codice di errore MP \_ THREAT \_ NOT \_ FOUND** indica che la minaccia non è stata trovata (e non è stato possibile eseguire la pulizia).

</dd> <dt>

<span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**MINACCIA MPNOTIFY \_ \_ ABBANDONATA**
</dt> <dd>

Non si è verificata alcuna correzione prima dell'arresto del servizio.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**AVVIO DELL'EVENTO MPNOTIFY \_ THREAT \_ \_ \_ CLEAN**
</dt> <dd>

È stata avviata un'azione di pulizia.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**MPNOTIFY \_ THREAT \_ CLEAN \_ EVENT \_ COMPLETE**
</dt> <dd>

Un'azione di pulizia è terminata.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**MPNOTIFY \_ SIGUPDATE \_ START**
</dt> <dd>

Aggiornamento della firma avviato.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**AVVIO RICERCA MPNOTIFY \_ SIGUPDATE \_ \_**
</dt> <dd>

Cercare gli aggiornamenti avviati.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**RICERCA MPNOTIFY \_ SIGUPDATE \_ \_ COMPLETATA**
</dt> <dd>

Ricerca degli aggiornamenti completata.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**AGGIORNAMENTO SOFTWARE MPNOTIFY \_ SIGUPDATE \_ \_ \_ DISPONIBILE**
</dt> <dd>

Aggiornamento software disponibile.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**AVVIO DEL DOWNLOAD DI MPNOTIFY \_ SIGUPDATE \_ \_**
</dt> <dd>

Download avviato.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**STATO DEL DOWNLOAD DI MPNOTIFY \_ SIGUPDATE \_ \_**
</dt> <dd>

Download in corso. I dati di callback contengono lo stato di avanzamento.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**DOWNLOAD DI MPNOTIFY \_ SIGUPDATE \_ \_ COMPLETATO**
</dt> <dd>

Download completato.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**AVVIO INSTALLAZIONE DI MPNOTIFY \_ SIGUPDATE \_ \_**
</dt> <dd>

Installazione avviata.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**STATO DI INSTALLAZIONE DI MPNOTIFY \_ SIGUPDATE \_ \_**
</dt> <dd>

Installazione in corso. I dati di callback contengono lo stato di avanzamento.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**INSTALLAZIONE DI MPNOTIFY \_ SIGUPDATE \_ \_ COMPLETATA**
</dt> <dd>

Installazione completata.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**È NECESSARIO RIAVVIARE MPNOTIFY \_ SIGUPDATE \_ \_**
</dt> <dd>

L'aggiornamento richiede il riavvio.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**RICHIESTA MPNOTIFY \_ SIGUPDATE \_ \_ ELABORATA**
</dt> <dd>

Il servizio ha elaborato una richiesta di aggiornamento della firma. L'esito negativo o positivo è indicato **da hResult** nei dati di callback.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ COMPLETATO**
</dt> <dd>

Aggiornamento completato. **S \_ Lo** stato FALSE indica che non sono necessari aggiornamenti.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**AVVIO \_ DELL'ESEMPIO MPNOTIFY \_**
</dt> <dd>

Invio di esempio avviato.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**ESEMPIO MPNOTIFY \_ \_ COMPLETATO**
</dt> <dd>

Invio di esempio completato.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**AVVIO ELEMENTO DI ESEMPIO MPNOTIFY \_ \_ \_**
</dt> <dd>

Invio di elementi di esempio specifico avviato. L'indice degli elementi di esempio è disponibile in [**MPSAMPLE \_ DATA.**](mpsample-data.md)

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**ELEMENTO DI ESEMPIO MPNOTIFY \_ \_ \_ RIUSCITO**
</dt> <dd>

Invio dell'elemento di esempio specifico riuscito.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**ELEMENTO DI ESEMPIO MPNOTIFY \_ \_ NON \_ RIUSCITO**
</dt> <dd>

L'invio di un elemento di esempio specifico non è riuscito. Il codice di errore è disponibile in [**MPCALLBACK \_ DATA.**](mpcallback-data.md)

</dd> <dt>

<span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**MPNOTIFY \_ RESERVED \_ DATA**
</dt> <dd>

Dati riservati interni.

</dd> <dt>

<span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**AGGIUNTA DI MPNOTIFY \_ FASTPATH \_ SIG \_**
</dt> <dd>

Una firma Fastpath ha aggiunto o disabilitato una firma.

</dd> <dt>

<span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**MPNOTIFY \_ FASTPATH \_ SIG \_ RIMOSSO**
</dt> <dd>

Una firma FastPath è stata rimossa.

</dd> <dt>

<span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**MPNOTIFY \_ NIS \_ PRIVATE**
</dt> <dd>

Notifcations private NIS. Nessun partner deve registrarsi a questo scopo.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**MODIFICA \_ DELL'INTEGRITÀ \_ MPNOTIFY**
</dt> <dd>

Il servizio AM ha immesso un nuovo stato.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**RIPRISTINO \_ DELL'INTEGRITÀ \_ MPNOTIFY**
</dt> <dd>

Il servizio AM è stato ripristinato da uno stato.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**AVVIO INTEGRITÀ MPNOTIFY \_ \_**
</dt> <dd>

Il servizio AM ha inizializzato l'integrità del sistema.

</dd> <dt>

<span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**MODIFICA DI MPNOTIFY \_ \_ ENDOFLIFE**
</dt> <dd>

Le date di scadenza "Fine vita" per il servizio AM sono state modificate.

</dd> <dt>

<span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**MPNOTIFY \_ MALWARETOAST \_ DATA**
</dt> <dd>

Il servizio AM ha rilevato malware che potrebbe aver causato la modifica delle impostazioni critiche nel computer.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                            |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md)
</dt> <dt>

[**DATI \_ MPCALLBACK**](mpcallback-data.md)
</dt> <dt>

[**DATI \_ MPSAMPLE**](mpsample-data.md)
</dt> </dl>

 

 





