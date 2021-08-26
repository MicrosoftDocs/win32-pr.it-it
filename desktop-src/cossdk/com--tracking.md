---
description: Rilevamento COM+
ms.assetid: ad3bdeb5-f303-411a-abfb-ccde3f9a86b9
title: Rilevamento COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 069d910f0c559776125342b861e71566fb20f45231f960b1c1dcb18262171926
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029491"
---
# <a name="com-tracking"></a>Rilevamento COM+

Il servizio di rilevamento COM+ consente di creare programmi amministrativi e di diagnostica personalizzati che monitorino lo stato e le prestazioni dell'esecuzione di applicazioni COM+. Il rilevamento COM+ fornisce informazioni statistiche sull'uso di applicazioni COM+ e informazioni sullo stato, ad esempio se un'istanza dell'applicazione server COM+ è sospesa o è stata riciclata. Gli strumenti possono usare le informazioni di rilevamento nel monitoraggio diagnostico o a scopo di visualizzazione. Ad esempio, lo strumento amministrativo Servizi componenti usa il rilevamento COM+ per visualizzare lo stato delle istanze dell'applicazione COM+ nelle cartelle Applicazioni COM+ e Processi in esecuzione.

Il rilevamento COM+ calcola e aggiorna periodicamente un set di metriche di uso comune, rendendo disponibili queste informazioni ai programmi che ne hanno bisogno. È simile alla strumentazione COM+, in quanto entrambi i servizi raccolgono automaticamente i dati dalle istanze dell'applicazione COM+ e rendono questi dati disponibili per i consumer. Tuttavia, esistono alcune importanti differenze tra questi servizi, sia nella funzionalità fornita che nell'utilizzo tipico. La tabella seguente riepiloga queste differenze.



| Strumentazione COM+                                                                                                                                                                                                   | Rilevamento COM+                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dati granulari. Il servizio di strumentazione COM+ notifica ai sottoscrittori registrati i singoli eventi discreti (ad esempio, il metodo chiamato, oggetto eliminato) che si verificano in un'istanza dell'applicazione COM+.<br/> | Dati aggregati. Il rilevamento COM+ calcola e aggiorna periodicamente le metriche di uso comune per lo stato e le prestazioni delle istanze dell'applicazione COM+.<br/> |
| I sottoscrittori di eventi calcolano in genere le metriche per conto proprio, usando algoritmi e criteri ad hoc.<br/>                                                                                                           | Le metriche vengono calcolate automaticamente dal servizio di rilevamento COM+. Tutti i consumer ottengono gli stessi dati, senza supporto per le metriche personalizzate.<br/>                |
| Dopo la registrazione di una sottoscrizione, il consumer non riceve informazioni su un'istanza dell'applicazione COM+ fino a quando non si verifica un evento.<br/>                                                                    | I dati di rilevamento per tutte le istanze dell'applicazione COM+ possono essere recuperati in qualsiasi momento.<br/>                                                                         |
| Supporta solo un meccanismo di sottoscrizione basato su eventi COM+ per i consumer.<br/>                                                                                                                                     | Supporta sia un meccanismo di sottoscrizione basato su eventi COM+ che il polling in un'interfaccia del server locale COM.<br/>                                                  |
| Esempio                                                                                                                                                                                                               |                                                                                                                                                                   |
| Notifiche quando viene chiamato o restituito un metodo.<br/>                                                                                                                                                           | Tempo medio di risposta alle chiamate, numero di chiamate al metodo riuscite o non riuscite in un periodo di tempo recente, numero di oggetti attualmente in una chiamata al metodo.<br/>     |
| Notifiche quando un oggetto viene aggiunto o ottenuto dal pool di oggetti.<br/>                                                                                                                                  | Numero di oggetti nel pool, numero totale di oggetti.<br/>                                                                                                |
| Notifiche quando un'applicazione server COM+ viene avviata, sospesa o riciclata.<br/>                                                                                                                               | Stato del processo dell'applicazione server COM+, ad esempio se è sospeso o riciclato.<br/>                                                         |
| Notifiche degli eventi di avvio, preparazione, interruzione ed commit della transazione.<br/>                                                                                                                                      | Nessun equivalente.<br/>                                                                                                                                         |
| Notifiche di tentativi di autenticazione a livello di chiamata di metodo riusciti e non riusciti.<br/>                                                                                                                           | Nessun equivalente.<br/>                                                                                                                                         |



 

Anche se il rilevamento COM+ è più limitato in termini di ambito dei dati e flessibilità per il calcolo delle metriche, le metriche fornite dovrebbero essere sufficienti per un'ampia gamma di programmi amministrativi e diagnostici. L'uso del rilevamento COM+, quando possibile, può semplificare la progettazione di questi programmi. Inoltre, l'uso del rilevamento COM+ nei sistemi di produzione può avere un impatto sulle prestazioni significativamente inferiore, rendendolo più appropriato per gli strumenti di monitoraggio in tempo reale.

## <a name="how-com-tracking-collects-data"></a>Come il rilevamento COM+ raccoglie i dati

Quando viene avviato un processo dell'applicazione server COM+, COM+ registra il processo con il *server di monitoraggio*, un componente dell'applicazione di sistema. Anche i componenti nelle applicazioni della libreria COM+ e nei servizi senza contesti SWC (Components Without Components) supportano il rilevamento. Quando un componente di libreria o un contesto SWC viene creato in un processo, COM+ registra il processo con il server di monitoraggio se non è già stato registrato.

COM+ aggiorna le statistiche per un processo monitorato quando si verificano determinati eventi nel processo, ad esempio la creazione di un oggetto o il completamento di una chiamata al metodo. I dati aggiornati vengono inviati periodicamente al server di monitoraggio, a quel punto diventano disponibili per i consumer. Il server di monitoraggio è anche responsabile del calcolo di alcune delle metriche usate dalle funzionalità di riciclo e monitoraggio dei blocchi delle applicazioni COM+. Questi dati sono disponibili anche per i consumer.

I dati di rilevamento sono organizzati in base al processo che ha generato i dati. I dati a livello di singole applicazioni o componenti COM+ nel processo sono disponibili anche per i consumer che necessitano di queste informazioni.

## <a name="events-versus-polling"></a>Eventi e polling

Il rilevamento COM+ supporta due meccanismi per un consumer per ottenere i dati di rilevamento dal server di rilevamento, un meccanismo di sottoscrizione basato su eventi COM+ e un'interfaccia del server locale COM.

I programmi che devono ricevere periodicamente una notifica con dati di rilevamento aggiornati possono registrare una sottoscrizione per l'interfaccia eventi [**IComTrackingInfoEvents.**](/windows/desktop/api/ComSvcs/nn-comsvcs-icomtrackinginfoevents) Approssimativamente ogni tre secondi, il server di rilevamento chiama il metodo [**IComTrackingInfoEvents::OnNewTrackingInfo**](/windows/desktop/api/ComSvcs/nf-comsvcs-icomtrackinginfoevents-onnewtrackinginfo) di ogni sottoscrittore, inviando i dati di rilevamento più recenti sotto forma di oggetto raccolta. Questo oggetto implementa [**l'interfaccia IComTrackingInfoCollection**](/windows/desktop/api/ComSvcs/nn-comsvcs-icomtrackinginfocollection) e i sottoscrittori possono esplorare questa raccolta per trovare i dati a cui sono interessati.

Per vari motivi, potrebbe essere più opportuno che un programma eseegui il polling dei dati nel server di rilevamento. Ad esempio, uno strumento di monitoraggio potrebbe richiedere aggiornamenti molto meno frequentemente rispetto a un programma che visualizza lo stato in un'interfaccia utente. Inoltre, un programma può usare solo una piccola parte dei dati di rilevamento disponibili per il sistema (ad esempio, uno strumento potrebbe monitorare solo le prestazioni delle istanze di una singola applicazione COM+). Il modello di sottoscrizione invia a ogni sottoscrittore i dati di rilevamento per tutte le applicazioni COM+ in ogni notifica ed è responsabilità del sottoscrittore trovare i dati che desidera. Infine, gli eventi COM+ sono un meccanismo di notifica degli eventi ottimale. I servizi di recapito affidabile dei messaggi non vengono forniti e non è possibile che un sottoscrittore rilevi che il server di monitoraggio non è riuscito a inviare una notifica.

Un programma che richiede un maggiore controllo sul recupero dei dati di rilevamento può usare [**l'interfaccia IGetAppTrackerData**](/windows/desktop/api/ComSvcs/nn-comsvcs-igetapptrackerdata) del server di rilevamento.

 

 




