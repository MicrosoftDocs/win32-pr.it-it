---
title: Funzioni di avviso
description: Le funzioni di avviso di gestione della rete notificano gli eventi di rete ai programmi e alle applicazioni dei servizi di rete.
ms.assetid: e131191b-7413-45ff-84cd-b3a873d33ca1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411a9bab5f8b74b5dc6e83d9a3c09cdcaeebf66d34c265ad27639e7aab8d7c00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912461"
---
# <a name="alert-functions"></a>Funzioni di avviso

\[Le funzioni di avviso non sono supportate a Windows Vista perché i servizi alerter e messenger non sono supportati.\]

Le funzioni di avviso di gestione della rete notificano gli eventi di rete ai programmi e alle applicazioni dei servizi di rete. Un *evento* è una particolare istanza di un processo, un'occorrenza o uno stato dell'hardware come definito da un'applicazione. Le funzioni di avviso consentono alle applicazioni di indicare quando si verificano eventi predefiniti.

**Windows Server 2003:** I servizi Alerter e Messenger sono disabilitati per impostazione predefinita Windows Server 2003. È necessario ri abilitare i servizi prima di chiamare le funzioni di avviso di gestione della rete o le funzioni message [di gestione di rete](message-functions.md).

Le funzioni di avviso sono elencate di seguito.



| Funzione                                   | Descrizione                                                                                                                                                                                            |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetAlertRaise**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise)     | Notifica a tutti i client registrati che si è verificato un evento specifico.                                                                                                                                  |
| [**NetAlertRaiseEx**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) | Semplifica la notifica ai client registrati che si è verificato un evento specifico, perché, a differenza di **NetAlertRaise,** **NetAlertRaiseEx** non richiede una struttura [**STD \_ ALERT.**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) |



 

Il servizio alerter deve essere in esecuzione nel computer client quando si chiama la **funzione NetAlertRaise** o **la funzione NetAlertRaiseEx.** Se il servizio non è in esecuzione, le funzioni hanno esito negativo con **ERRORE \_ FILE NON \_ \_ TROVATO**. Il servizio alerter nel client chiama la [**funzione NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend) per inviare informazioni ai destinatari.

Le applicazioni, i servizi di rete e i componenti di rete interni usano le funzioni di avviso di gestione della rete per generare un avviso, notificando a diverse applicazioni o utenti quando si verifica un particolare tipo di evento. Le funzioni della categoria di avvisi, i tipi di dati, le strutture e le costanti sono definiti in LMCONS. H, LMERR. H e LMALERT. File di intestazione H. Per accedere a queste definizioni, definire le costanti INCL NETERRORS e INCL NETALERT e includere il file di intestazione \_ \_ LM.H.

The LMALERT. Il file H predifinisce le classi di avviso seguenti (tipi di eventi di rete) per l'invio di avvisi:

-   Eventi di rete che richiedono assistenza amministrativa
-   Aggiunta di una voce a un file di log degli errori
-   Ricezione di un messaggio trasmesso da un utente o da un'applicazione
-   Completamento di un processo di stampa
-   Uso di determinate applicazioni o risorse da parte degli utenti

È possibile definire altre classi di avvisi per le applicazioni di rete in base alle esigenze. Ad esempio, se un'applicazione in un server scrive regolarmente grandi quantità di dati in un'unità disco, l'applicazione rischia di riempire il disco. In questo caso, è possibile aggiungere l'evento "nessun spazio libero su disco" per attivare un avviso che informa l'applicazione di sospendere o terminare il processo che sta riempiendo il disco. Il nome dell'evento per un avviso può essere qualsiasi stringa di testo.

Quando si genera un avviso con una chiamata alla funzione [**NetAlertRaise,**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraise) i dati del messaggio devono essere costituiti da una struttura di intestazione [**STD \_ ALERT,**](/windows/desktop/api/Lmalert/ns-lmalert-std_alert) seguita da dati aggiuntivi a lunghezza fissa specifici dell'avviso in una struttura [**ADMIN OTHER \_ \_ INFO,**](/windows/desktop/api/Lmalert/ns-lmalert-admin_other_info) [**ERRLOG \_ OTHER \_ INFO,**](/windows/desktop/api/Lmalert/ns-lmalert-errlog_other_info) [**PRINT OTHER \_ \_ INFO**](/windows/desktop/api/Lmalert/ns-lmalert-print_other_info)o [**USER OTHER \_ \_ INFO.**](/windows/desktop/api/Lmalert/ns-lmalert-user_other_info) I dati aggiuntivi a lunghezza variabile possono seguire la struttura specifica dell'avviso. Le chiamate alla [**funzione NetAlertRaiseEx**](/windows/desktop/api/Lmalert/nf-lmalert-netalertraiseex) non richiedono una **struttura STD \_ ALERT.** L'applicazione chiamante deve allocare la memoria per tutte le strutture e i dati a lunghezza variabile e liberare la memoria al termine della chiamata.

Le macro seguenti sono disponibili per l'uso con i buffer dei dati degli avvisi.



| Macro                                          | Descrizione                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**INVIA \_ AVVISO PER ALTRE \_ INFORMAZIONI**](/windows/desktop/api/Lmalert/nf-lmalert-alert_other_info) | Restituisce un puntatore ai dati a lunghezza fissa che seguono la **struttura STD \_ ALERT** in un messaggio di avviso. |
| [**ALERT \_ VAR \_ DATA**](/windows/desktop/api/Lmalert/nf-lmalert-alert_var_data)     | Restituisce un puntatore ai dati a lunghezza variabile che seguono i dati specifici dell'avviso in un messaggio di avviso.   |



 

Invece di usare le funzioni di avviso di gestione della rete, è possibile usare l'SDK di Strumentazione gestione Windows (WMI) per la notifica degli eventi. Per altre informazioni sulle piattaforme che supportano il modello di eventi WMI, vedere [Wmi Infrastructure](/windows/desktop/WmiSdk/wmi-infrastructure) and Monitoring Events (Infrastruttura WMI e monitoraggio [degli](/windows/desktop/WmiSdk/monitoring-events) eventi) nella documentazione di WMI.

 

 