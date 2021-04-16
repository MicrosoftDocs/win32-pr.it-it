---
title: Funzioni di avviso
description: Le funzioni di avviso di gestione della rete notificano ai programmi e alle applicazioni del servizio di rete eventi di rete.
ms.assetid: e131191b-7413-45ff-84cd-b3a873d33ca1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80fde863b27bebc8bf815c939f7edf96cd998442
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473558"
---
# <a name="alert-functions"></a>Funzioni di avviso

\[Le funzioni di avviso non sono supportate a partire da Windows Vista, perché i servizi Alerter e Messenger non sono supportati.\]

Le funzioni di avviso di gestione della rete notificano ai programmi e alle applicazioni del servizio di rete eventi di rete. Un *evento* è una particolare istanza di un processo, un'occorrenza o uno stato di hardware definito da un'applicazione. Le funzioni di avviso consentono alle applicazioni di indicare quando si verificano eventi predefiniti.

**Windows Server 2003:** I servizi Alerter e Messenger sono disabilitati per impostazione predefinita in Windows Server 2003. È necessario riabilitare i servizi prima di chiamare le funzioni di avviso di gestione di rete o le [funzioni del messaggio](message-functions.md)di gestione di rete.

Le funzioni di avviso sono elencate di seguito.



| Funzione                                   | Descrizione                                                                                                                                                                                            |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAlertRaise**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise)     | Notifica a tutti i client registrati che si è verificato un determinato evento.                                                                                                                                  |
| [**NetAlertRaiseEx non**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) | Semplifica la notifica ai client registrati che si è verificato un determinato evento, perché, a differenza di **NetAlertRaise**, **NetAlertRaiseEx non** non richiede una struttura di [**\_ avviso STD**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) . |



 

Il servizio Alerter deve essere in esecuzione nel computer client quando si chiama la funzione **NetAlertRaise** o **NetAlertRaiseEx non** . Se il servizio non è in esecuzione, le funzioni hanno esito negativo e il **file di errore non è stato \_ \_ \_ trovato**. Il servizio Alerter nel client chiama la funzione [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend) per inviare informazioni ai destinatari.

Applicazioni, servizi di rete e componenti di rete interni utilizzano le funzioni di avviso di gestione della rete per generare un avviso, notificando a varie applicazioni o utenti quando si verifica un particolare tipo di evento. Le funzioni di categoria degli avvisi, i tipi di dati, le strutture e le costanti sono definite in LMCONS. H, LMERR. H e LMALERT. File di intestazione H. Per accedere a queste definizioni, definire le costanti incluse \_ NETERRORS e incl \_ NETALERT e includere il file di intestazione LM. H.

LMALERT. Il file H definisce le classi di avviso seguenti (tipi di eventi di rete) per l'invio di avvisi:

-   Eventi di rete che richiedono assistenza amministrativa
-   Aggiunta di una voce a un file di log degli errori
-   Ricezione di un messaggio trasmesso da un utente o da un'applicazione
-   Completamento di un processo di stampa
-   Uso di determinate applicazioni o risorse da parte degli utenti

È possibile definire altre classi di avvisi per le applicazioni di rete in base alle esigenze. Se, ad esempio, un'applicazione in un server scrive regolarmente grandi quantità di dati in un'unità disco, l'applicazione esegue il rischio di riempire il disco. In questo caso, potrebbe essere necessario aggiungere l'evento "No Free Disk Space" per attivare un avviso che informa l'applicazione di sospendere o terminare il processo di riempimento del disco. Il nome dell'evento per un avviso può essere qualsiasi stringa di testo.

Quando si genera un avviso con una chiamata alla funzione [**NetAlertRaise**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise) , i dati del messaggio devono essere costituiti da una struttura di intestazione di [**\_ avviso STD**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) , seguita da dati di lunghezza fissa aggiuntivi che sono specifici dell'avviso in un [**\_ altro amministratore \_**](/windows/desktop/api/Lmalert/ns-lmalert-admin_other_info), altre informazioni, [**ERRLOG \_ altre \_**](/windows/desktop/api/Lmalert/ns-lmalert-errlog_other_info)informazioni, [**stampa \_ altre \_**](/windows/desktop/api/Lmalert/ns-lmalert-print_other_info)informazioni o altra struttura di [**\_ \_ informazioni dell'utente**](/windows/desktop/api/Lmalert/ns-lmalert-user_other_info) . I dati aggiuntivi a lunghezza variabile possono seguire la struttura specifica dell'avviso. (Le chiamate alla funzione [**NetAlertRaiseEx non**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) non richiedono una struttura **di \_ avviso STD** ). L'applicazione chiamante deve allocare la memoria per tutte le strutture e i dati a lunghezza variabile e liberare la memoria dopo la restituzione della chiamata.

Le macro seguenti sono disponibili per l'utilizzo con i buffer dei dati di avviso.



| Macro                                          | Descrizione                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**\_altre \_ informazioni sull'avviso**](/windows/desktop/api/Lmalert/nf-lmalert-alert_other_info) | Restituisce un puntatore ai dati a lunghezza fissa che seguono la struttura **di \_ avviso STD** in un messaggio di avviso. |
| [**\_dati var \_ avviso**](/windows/desktop/api/Lmalert/nf-lmalert-alert_var_data)     | Restituisce un puntatore ai dati a lunghezza variabile che seguono i dati specifici dell'avviso in un messaggio di avviso.   |



 

Anziché utilizzare le funzioni di avviso di gestione della rete, è possibile utilizzare l'SDK Strumentazione gestione Windows (WMI) per la notifica degli eventi. Per ulteriori informazioni sulle piattaforme che supportano il modello di eventi WMI, vedere [WMI Infrastructure](/windows/desktop/WmiSdk/wmi-infrastructure) and [Monitoring Events](/windows/desktop/WmiSdk/monitoring-events) nella documentazione di WMI.

 

 