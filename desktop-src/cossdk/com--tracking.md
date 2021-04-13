---
description: Rilevamento COM+
ms.assetid: ad3bdeb5-f303-411a-abfb-ccde3f9a86b9
title: Rilevamento COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 828cc87b5a24363fd814d37c29e61a3ce204d988
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483061"
---
# <a name="com-tracking"></a>Rilevamento COM+

Il servizio di rilevamento COM+ consente di compilare programmi amministrativi e di diagnostica personalizzati che tengono traccia dello stato e delle prestazioni dell'esecuzione di applicazioni COM+. Il rilevamento COM+ fornisce informazioni statistiche sull'utilizzo delle applicazioni COM+, nonché informazioni sullo stato, ad esempio se un'istanza dell'applicazione server COM+ è sospesa o è stata riciclata. Gli strumenti possono utilizzare le informazioni di rilevamento nel monitoraggio diagnostico o a scopo di visualizzazione. Lo strumento di amministrazione Servizi componenti, ad esempio, utilizza il rilevamento COM+ per visualizzare lo stato delle istanze dell'applicazione COM+ nelle cartelle applicazioni COM+ e processi in esecuzione.

Il rilevamento COM+ calcola e aggiorna periodicamente un set di metriche di uso comune, rendendo queste informazioni disponibili ai programmi che lo richiedono. È simile alla strumentazione COM+ in quanto entrambi i servizi raccolgono automaticamente i dati dalle istanze dell'applicazione COM+ e rendono tali dati disponibili ai consumer. Tuttavia, esistono alcune differenze importanti tra questi servizi, sia nella funzionalità fornita che nell'utilizzo tipico. Nella tabella seguente sono riepilogate queste differenze.



| Strumentazione COM+                                                                                                                                                                                                   | Rilevamento COM+                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dati con granularità fine. Il servizio di strumentazione COM+ invia una notifica ai sottoscrittori registrati dei singoli eventi discreti (ad esempio, metodo chiamato, oggetto distrutto) che si verificano in un'istanza dell'applicazione COM+.<br/> | Dati aggregati. Il rilevamento COM+ calcola e aggiorna periodicamente le metriche usate comunemente per lo stato e le prestazioni delle istanze di applicazioni COM+.<br/> |
| I sottoscrittori di eventi in genere calcolano la metrica autonomamente, usando algoritmi e criteri ad hoc.<br/>                                                                                                           | Le metriche vengono calcolate automaticamente dal servizio di rilevamento COM+. Tutti i consumer ottengono gli stessi dati, senza supporto per le metriche personalizzate.<br/>                |
| Dopo la registrazione di una sottoscrizione, il consumer non riceve alcuna informazione su un'istanza dell'applicazione COM+ fino a quando non si verifica un evento.<br/>                                                                    | I dati di rilevamento per tutte le istanze dell'applicazione COM+ possono essere recuperati in qualsiasi momento.<br/>                                                                         |
| Supporta solo un meccanismo di sottoscrizione basata su eventi COM+ per i consumer.<br/>                                                                                                                                     | Supporta sia un meccanismo di sottoscrizione basato su eventi COM+ sia il polling su un'interfaccia server locale COM.<br/>                                                  |
| Esempio                                                                                                                                                                                                               |                                                                                                                                                                   |
| Notifiche quando un metodo viene chiamato o restituisce.<br/>                                                                                                                                                           | Tempo medio di risposta delle chiamate, numero di chiamate al metodo che hanno avuto esito positivo o negativo in un periodo di tempo recente, numero di oggetti attualmente in una chiamata al metodo.<br/>     |
| Notifiche quando un oggetto viene aggiunto o ottenuto dal pool di oggetti.<br/>                                                                                                                                  | Numero di oggetti nel pool, numero totale di oggetti.<br/>                                                                                                |
| Notifiche quando un'applicazione server COM+ viene avviata, sospesa o riciclata.<br/>                                                                                                                               | Stato del processo dell'applicazione server COM+, ad esempio se è in pausa o riciclato.<br/>                                                         |
| Notifiche degli eventi di avvio, preparazione, interruzione e commit delle transazioni.<br/>                                                                                                                                      | Nessun equivalente.<br/>                                                                                                                                         |
| Notifiche di tentativi di autenticazione a livello di chiamata al metodo riusciti e non riusciti.<br/>                                                                                                                           | Nessun equivalente.<br/>                                                                                                                                         |



 

Sebbene il rilevamento COM+ sia più limitato in termini di ambito dei dati e flessibilità per il calcolo delle metriche, le metriche fornite dovrebbero essere sufficienti per un'ampia gamma di programmi amministrativi e di diagnostica. L'utilizzo del rilevamento COM+, quando possibile, può semplificare la progettazione di questi programmi. Inoltre, l'utilizzo del rilevamento COM+ nei sistemi di produzione può avere un notevole calo delle prestazioni, rendendolo più appropriato per gli strumenti di monitoraggio in tempo reale.

## <a name="how-com-tracking-collects-data"></a>Raccolta dei dati in rilevamento COM+

Quando viene avviato un processo dell'applicazione server COM+, COM+ registra il processo con il *server di rilevamento*, un componente dell'applicazione di sistema. I componenti in applicazioni della libreria COM+ e i contesti di servizi senza componenti (SWC) supportano anche il rilevamento. Quando un componente della libreria o un contesto SWC viene creato in un processo, COM+ registra il processo con il server di rilevamento se non è già stato registrato.

COM+ aggiorna le statistiche per un processo rilevato quando si verificano determinati eventi nel processo, ad esempio la creazione di un oggetto o il completamento di una chiamata al metodo. I dati aggiornati vengono inviati periodicamente al server di rilevamento, a quel punto diventa disponibile per i consumer. Il server di rilevamento è inoltre responsabile del calcolo di alcune delle metriche utilizzate dalle funzionalità di monitoraggio e blocco delle applicazioni COM+. Questi dati sono disponibili anche per gli utenti.

I dati di rilevamento sono organizzati in base al processo che ha generato i dati. I dati a livello di singole applicazioni o componenti COM+ del processo sono disponibili anche per gli utenti che necessitano di queste informazioni.

## <a name="events-versus-polling"></a>Eventi e polling

Il rilevamento COM+ supporta due meccanismi che consentono a un consumer di ottenere i dati di rilevamento dal server tracker, un meccanismo di sottoscrizione basato su eventi COM+ e un'interfaccia server locale COM.

I programmi che devono essere notificati periodicamente con i dati di rilevamento aggiornati possono registrare una sottoscrizione per l'interfaccia eventi [**IComTrackingInfoEvents**](/windows/desktop/api/ComSvcs/nn-comsvcs-icomtrackinginfoevents) . Approssimativamente ogni tre secondi, il server di rilevamento chiama il metodo [**IComTrackingInfoEvents:: OnNewTrackingInfo**](/windows/desktop/api/ComSvcs/nf-comsvcs-icomtrackinginfoevents-onnewtrackinginfo) di ogni Sottoscrittore, inviando i dati di rilevamento più recenti sotto forma di oggetto raccolta. Questo oggetto implementa l'interfaccia [**IComTrackingInfoCollection**](/windows/desktop/api/ComSvcs/nn-comsvcs-icomtrackinginfocollection) e i sottoscrittori possono esplorare questa raccolta per trovare i dati a cui sono interessati.

Per diversi motivi, potrebbe essere opportuno che un programma esegua il polling del server di rilevamento per i dati. Uno strumento di monitoraggio, ad esempio, potrebbe richiedere aggiornamenti con una frequenza molto inferiore rispetto a un programma che visualizza lo stato in un'interfaccia utente. Inoltre, un programma può utilizzare solo una piccola parte dei dati di rilevamento disponibili per il sistema. ad esempio, è possibile che uno strumento monitori solo le prestazioni delle istanze di una singola applicazione COM+. Il modello di sottoscrizione Invia a ogni Sottoscrittore i dati di rilevamento per tutte le applicazioni COM+ in ogni notifica ed è responsabilità del Sottoscrittore individuare i dati desiderati. Infine, gli eventi COM+ sono un meccanismo di notifica degli eventi con il massimo sforzo. I servizi di recapito dei messaggi affidabili non sono disponibili e non è possibile che un Sottoscrittore rilevi che il server di rilevamento non è stato in grado di inviare una notifica.

Un programma che necessita di un maggiore controllo sul recupero dei dati di rilevamento può usare l'interfaccia [**IGetAppTrackerData**](/windows/desktop/api/ComSvcs/nn-comsvcs-igetapptrackerdata) del server tracker.

 

 




