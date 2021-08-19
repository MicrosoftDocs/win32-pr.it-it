---
title: Oggetto SystemMonitor (Isysmon.h)
description: Questa classe contiene i metodi e le proprietà utilizzati per configurare il controllo Monitoraggio di sistema.
ms.assetid: 5a6195ee-ed89-4f5d-85dd-88cf4a9b5155
keywords:
- Oggetto SystemMonitor SysMon
- Oggetto SystemMonitor SysMon , descritto
topic_type:
- apiref
api_name:
- SystemMonitor
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88b9489c2e966abdf3c329d952a76bd30de487cca99a3e00c8ff46431a163ec9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117954506"
---
# <a name="systemmonitor-object"></a>Oggetto SystemMonitor

Questa classe contiene i metodi e le proprietà utilizzati per configurare il controllo Monitoraggio di sistema.

## <a name="members"></a>Membri

**L'oggetto SystemMonitor** ha questi tipi di membri:

-   [Eventi](#events)
-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="events"></a>Eventi

**L'oggetto SystemMonitor** include questi eventi.



| Event                                                         | Descrizione                                                                                                                 |
|:--------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [**OnCounterAdded**](systemmonitor-oncounteradded.md)        | Notifica all'utente quando un contatore viene aggiunto [**all'insieme Counters.**](counters.md)<br/>                             |
| [**OnCounterDeleted**](-systemmonitor-oncounterdeleted.md)   | Notifica all'utente prima che un contatore venga eliminato dalla [**raccolta Counters.**](counters.md)<br/>                       |
| [**OnCounterSelected**](-systemmonitor-oncounterselected.md) | Invia una notifica quando viene selezionato un contatore.<br/>                                                                         |
| [**OnDblClick**](-systemmonitor-ondblclick.md)               | Notifica quando un utente fa doppio clic sulla linea del grafico, sulla barra dell'istogramma o sull'elemento del report con il pulsante sinistro del mouse.<br/> |
| [**OnSampleCollected**](-systemmonitor-onsamplecollected.md) | Notifica all'utente quando sono stati raccolti i valori di esempio per i contatori.<br/>                                            |



 

### <a name="methods"></a>Metodi

**L'oggetto SystemMonitor** dispone di questi metodi.



| Metodo                                                       | Descrizione                                                                                                                                                              |
|:-------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Blocco in batch**](systemmonitor-batchinglock.md)           | Blocca Monitoraggio di sistema per impedire il campionamento dei dati del contatore dal nuovo contatore o file di log aggiunto.<br/>                                                   |
| [**BrowseCounters**](systemmonitor-browsecounters.md)       | Consente di visualizzare **la finestra di dialogo** Aggiungi contatore .<br/>                                                                                                                      |
| [**ClearData**](systemmonitor-cleardata.md)                 | Cancella tutti i campi dati nel controllo .<br/>                                                                                                                        |
| [**CollectSample**](systemmonitor-collectsample.md)         | Campione un valore per ogni contatore **nell'oggetto raccolta** Counters.<br/>                                                                                       |
| [**Copia**](systemmonitor-copy.md)                           | Copia negli Appunti le impostazioni delle proprietà, l'elenco dei contatori e i dati dei contatori del controllo come oggetto HTML.<br/>                                                |
| [**Proprietà di visualizzazione**](systemmonitor-displayproperties.md) | Consente di visualizzare **Graph finestra di dialogo** Proprietà .<br/>                                                                                                                 |
| [**GetLogViewRange**](systemmonitor-getlogviewrange.md)     | Recupera la data di inizio utilizzata per recuperare i valori dei contatori dai file di log.<br/>                                                                               |
| [**LoadSettings**](systemmonitor-loadsettings.md)           | Aggiunge i contatori nel file di modello HTML a Monitoraggio di sistema.<br/>                                                                                            |
| [**Incolla**](systemmonitor-paste.md)                         | Aggiunge l'elenco dei contatori copiati negli Appunti all'insieme corrente di contatori. <br/>                                                        |
| [**Relog**](systemmonitor-relog.md)                         | Riloga i dati del contatore in un nuovo file. È inoltre possibile utilizzare questo metodo per specificare un nuovo tipo di file e ridurre il numero di esempi contenuti nel file di log.<br/> |
| [**Reset**](systemmonitor-reset.md)                         | Rimuove tutti [**gli oggetti CounterItem**](counteritem.md) dall'oggetto **raccolta Counters.**<br/>                                                               |
| [**SaveAs**](systemmonitor-saveas.md)                       | Salva i valori dei contatori nella visualizzazione grafico in un file di log.<br/>                                                                                                     |
| [**ScaleToFit**](systemmonitor-scaletofit.md)               | Ridimensionare i valori dei contatori in base al grafico.<br/>                                                                                                                     |
| [**SetLogViewRange**](systemmonitor-setlogviewrange.md)     | Imposta la data di inizio utilizzata per recuperare i valori dei contatori dai file di log.<br/>                                                                                    |
| [**UpdateGraph**](systemmonitor-updategraph.md)             | Aggiorna il contenuto delle finestre di Monitoraggio di sistema.<br/>                                                                                                         |



 

### <a name="properties"></a>Proprietà

**L'oggetto SystemMonitor** dispone di queste proprietà.



| Proprietà                                                                                | Descrizione                                                                                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aspetto**](systemmonitor-appearance.md)<br/>                               | Recupera o imposta l'aspetto del controllo per includere o omettere effetti di visualizzazione tridimensionali.<br/>                                                                                                                        |
| [**Backcolor**](systemmonitor-backcolor.md)<br/>                                 | Recupera o imposta il colore di sfondo delle visualizzazioni grafico e report.<br/>                                                                                                                                                        |
| [**BackColorCtl**](systemmonitor-backcolorctl.md)<br/>                           | Recupera o imposta il colore di sfondo del controllo .<br/>                                                                                                                                                                       |
| [**BorderStyle**](systemmonitor-borderstyle.md)<br/>                             | Recupera o imposta lo stile del bordo del controllo .<br/>                                                                                                                                                                           |
| [**ChartScroll**](systemmonitor-chartscroll.md)<br/>                             | Recupera o imposta un valore che determina se il grafico a linee scorre nella visualizzazione.<br/>                                                                                                                                             |
| [**Contatori**](systemmonitor-counters.md)<br/>                                   | Recupera la raccolta di [**oggetti CounterItem.**](counteritem.md)<br/>                                                                                                                                                      |
| [**DataPointCount**](systemmonitor-datapointcount.md)<br/>                       | Recupera o imposta il numero di punti dati visualizzati in un grafico a linee.<br/>                                                                                                                                                       |
| [**Tipo di origine dati**](systemmonitor-datasourcetype.md)<br/>                       | Recupera o imposta l'origine dei dati del contatore delle prestazioni.<br/>                                                                                                                                                                |
| [**DisplayType**](systemmonitor-displaytype.md)<br/>                             | Recupera o imposta il tipo di grafico utilizzato per creare un grafico dei dati del contatore delle prestazioni.<br/>                                                                                                                                              |
| [**EnableDigitGrouping**](systemmonitor-enabledigitgrouping.md)<br/>             | Recupera o imposta un valore che determina se SYSMON utilizza il raggruppamento di cifre durante la visualizzazione di valori numerici.<br/>                                                                                                                      |
| [**EnableToolTips**](systemmonitor-enabletooltips.md)<br/>                       | Recupera o imposta un valore che determina se viene visualizzata una descrizione comando quando il puntatore del mouse viene posizionato su un contatore in una delle visualizzazioni grafico.<br/>                                                                                             |
| [**Font**](systemmonitor-font.md)<br/>                                           | Recupera o imposta il tipo di carattere utilizzato nel controllo .<br/>                                                                                                                                                                              |
| [**ColorePrimoPiano**](systemmonitor-forecolor.md)<br/>                                 | Recupera o imposta il colore del testo visualizzato nel controllo .<br/>                                                                                                                                                         |
| [**GraphTitle**](systemmonitor-graphtitle.md)<br/>                               | Recupera o imposta il titolo del grafico.<br/>                                                                                                                                                                                    |
| [**GridColor**](systemmonitor-gridcolor.md)<br/>                                 | Recupera o imposta il colore delle linee della griglia utilizzate nel grafico.<br/>                                                                                                                                                             |
| [**Evidenziazione**](systemmonitor-highlight.md)<br/>                                 | Recupera o imposta un valore che indica se i valori dei contatori selezionati sono evidenziati nel grafico.<br/>                                                                                                               |
| [**LogFileName**](systemmonitor-logfilename.md)<br/>                             | Obsoleta. Recupera o imposta il nome di un file di log da utilizzare come origine dei valori dei contatori visualizzati in Monitoraggio di sistema.<br/>                                                                                                   |
| [**LogFiles**](systemmonitor-logfilename.md)<br/>                                | Raccolta di uno o più file di log da utilizzare come origine dei valori dei contatori visualizzati in Monitoraggio di sistema.<br/>                                                                                                                  |
| [**LogSourceStartTime**](systemmonitor-logsourcestarttime.md)<br/>               | Recupera il timestamp del valore del contatore meno recente da un contatore nella raccolta di contatori registrato nei file di log.<br/>                                                                                           |
| [**LogSourceStopTime**](systemmonitor-logsourcestoptime.md)<br/>                 | Recupera il timestamp del valore del contatore più recente da un contatore nella raccolta di contatori registrato nei file di log.<br/>                                                                                             |
| [**LogViewStart**](systemmonitor-logviewstart.md)<br/>                           | Recupera o imposta la data di inizio utilizzata per recuperare i valori dei contatori dai file di log.<br/>                                                                                                                                      |
| [**LogViewStop**](systemmonitor-logviewstop.md)<br/>                             | Recupera o imposta la data di fine utilizzata per recuperare i valori dei contatori dai file di log.<br/>                                                                                                                                        |
| [**ManualUpdate**](systemmonitor-manualupdate.md)<br/>                           | Recupera o imposta un valore che indica se il contenuto di Monitoraggio di sistema verrà aggiornato manualmente o automaticamente a intervalli specificati.<br/>                                                                           |
| [**MaximumScale**](systemmonitor-maximumscale.md)<br/>                           | Recupera o imposta il valore massimo dell'asse verticale (Y) del grafico.<br/>                                                                                                                                                   |
| [**MinimumScale**](systemmonitor-minimumscale.md)<br/>                           | Recupera o imposta il valore minimo dell'asse verticale (Y) del grafico.<br/>                                                                                                                                                   |
| [**MonitorDuplicateInstances**](systemmonitor-monitorduplicateinstances.md)<br/> | Recupera o imposta un valore che determina se è possibile monitorare più istanze di un contatore.<br/>                                                                                                                          |
| [**ReadOnly**](systemmonitor-readonly.md)<br/>                                   | Recupera o imposta un valore che determina se un utente può modificare i valori delle proprietà del controllo .<br/>                                                                                                                      |
| [**ReportValueType**](systemmonitor-reportvaluetype.md)<br/>                     | Recupera o imposta un valore che determina se le visualizzazioni Istogramma e Report tracciano l'ultimo valore campionato durante l'intervallo di campionamento o un valore calcolato dal campionamento, ad esempio il valore medio o minimo del contatore.<br/> |
| [**ShowHorizontalGrid**](systemmonitor-showhorizontalgrid.md)<br/>               | Recupera o imposta un valore che determina se le linee griglia orizzontali vengono visualizzate nel grafico.<br/>                                                                                                                          |
| [**ShowLegend**](systemmonitor-showlegend.md)<br/>                               | Recupera o imposta un valore che determina se la legenda viene visualizzata.<br/>                                                                                                                                                   |
| [**ShowScaleLabels**](systemmonitor-showscalelabels.md)<br/>                     | Recupera o imposta un valore che determina se le etichette di scala vengono visualizzate sull'asse verticale del grafico.<br/>                                                                                                          |
| [**ShowTimeAxisLabels**](systemmonitor-showtimeaxislabels.md)<br/>               | Recupera o imposta un valore che determina se l'asse orizzontale (X) della visualizzazione grafico contiene etichette.<br/>                                                                                                                      |
| [**Mostrabarrastrumenti**](systemmonitor-showtoolbar.md)<br/>                             | Recupera o imposta un valore che determina se la barra degli strumenti viene visualizzata nel controllo .<br/>                                                                                                                                   |
| [**ShowValueBar**](systemmonitor-showvaluebar.md)<br/>                           | Recupera o imposta un valore che determina se la barra dei valori (il set di valori statistici sotto il grafico) viene visualizzata nel controllo .<br/>                                                                                 |
| [**ShowVerticalGrid**](systemmonitor-showverticalgrid.md)<br/>                   | Recupera o imposta un valore che determina se le linee della griglia verticali vengono visualizzate nel grafico.<br/>                                                                                                                            |
| [**SqlDsnName**](systemmonitor-sqldsnname.md)<br/>                               | Recupera o imposta il nome dell'origine dati ODBC.<br/>                                                                                                                                                                                 |
| [**SqlLogSetName**](systemmonitor-sqllogsetname.md)<br/>                         | Recupera o imposta il nome descrittivo del set di log.<br/>                                                                                                                                                                          |
| [**TimeBarColor**](systemmonitor-timebarcolor.md)<br/>                           | Recupera o imposta il colore della barra del tempo, ovvero la barra verticale che si sposta nella finestra del grafico per indicare il passaggio di ogni intervallo di campionamento nella visualizzazione grafico a linee.<br/>                                                  |
| [**UpdateInterval**](systemmonitor-updateinterval.md)<br/>                       | Recupera o imposta il tempo di attesa di SYSMON prima del successivo aggiornamento del grafico o del report.<br/>                                                                                                                  |
| [**YAxisLabel**](systemmonitor-yaxislabel.md)<br/>                               | Recupera o imposta l'etichetta dell'asse verticale (Y) del grafico.<br/>                                                                                                                                                           |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Isysmon.h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





