---
description: L'API di distribuzione peer, che supporta la funzionalità cache di Branch in Windows 7, Windows Server 2008 R2, Windows 8 e Windows Server 2012, offre un set di API della piattaforma che può aumentare la velocità di risposta della rete delle applicazioni centralizzate quando si accede da uffici remoti e contribuire a ridurre l'utilizzo di Wide Area Network (WAN) globale senza interferire con le tecnologie di sicurezza di rete
ms.assetid: feb9666e-563a-49f4-ad1c-f166a0faff31
title: Informazioni sulla distribuzione peer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5b9a99a65ea2cfda6dc8ad9accd4d881529e87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881825"
---
# <a name="about-peer-distribution"></a>Informazioni sulla distribuzione peer

L'API di distribuzione peer, che supporta la funzionalità cache di Branch in Windows 7, Windows Server 2008 R2, Windows 8 e Windows Server 2012, offre un set di API della piattaforma che può aumentare la velocità di risposta della rete delle applicazioni centralizzate quando si accede da uffici remoti e contribuire a ridurre l'utilizzo di Wide Area Network (WAN) globale senza interferire con le tecnologie di sicurezza di rete

Il sistema di distribuzione peer offre un set di API della piattaforma usate dagli editori che forniscono contenuti digitali e consumer che lo richiedono. Per distinguere facilmente questi ruoli, potrebbe essere più facile pensare al server di pubblicazione in un ruolo del server e al consumer in un ruolo client. A parte questo, è importante ricordare che, a parte questi ruoli concettuali, il servizio di distribuzione peer è un vero e proprio sistema peer, come indicato dalla possibilità per qualsiasi nodo di distribuzione peer di pubblicare e utilizzare contenuti digitali. Le API della piattaforma di distribuzione peer sono esposte a autori e consumer da una libreria di importazione Win32 (**PeerDist. lib**).

Il ciclo di vita del contenuto fornito da un server di pubblicazione e recuperato da un consumer con il servizio di distribuzione peer è costituito dalle operazioni seguenti:



|                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Pubblicazione del contenuto** | La pubblicazione viene eseguita per produrre una descrizione delle **informazioni sul** contenuto **, o informazioni sul contenuto,** per breve. Queste informazioni sul contenuto possono quindi essere utilizzate da un'istanza del servizio di distribuzione peer per autenticare e ricompilare il contenuto. Quando il contenuto viene pubblicato da un'applicazione nel servizio di distribuzione peer, che è concettualmente un'operazione lato server, il contenuto viene associato all'identità del server di pubblicazione, che è basata sul SID dell'utente associato al token di accesso al thread. Questa associazione viene eseguita per limitare l'accesso al contenuto da entità non autorizzate. Tuttavia, è importante notare che l'accesso alle informazioni sul contenuto è equivalente all'accesso al contenuto stesso, in quanto le informazioni sul contenuto possono essere utilizzate per ottenere il contenuto dai peer o da una cache ospitata.<br/> È disponibile una nuova versione della struttura dei dati delle informazioni sul contenuto in Windows 8. Tuttavia, la versione precedente è ancora supportata. Per interagire con i client Windows 7, un amministratore può configurare il servizio di distribuzione peer per utilizzare la versione precedente della struttura dei dati delle informazioni sul contenuto.<br/> |
| **Recupero del contenuto**   | Affinché un consumer recuperi il contenuto dal servizio di distribuzione peer, è necessario fornire l'accesso alle informazioni sul contenuto pubblicate associate a tale contenuto. Il servizio di distribuzione peer utilizzato per pubblicare il contenuto può fornire le informazioni sul contenuto associate. Quando il consumer ha le informazioni sul contenuto, è possibile usare altre API di distribuzione peer per richiedere contenuto dal servizio di distribuzione peer. Il servizio di distribuzione peer tenterà di recuperare il contenuto dalla rete locale. Se il contenuto non è disponibile, l'applicazione client è responsabile del recupero del contenuto dal server di origine.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Rimozione della pubblicazione** | Per le applicazioni che hanno pubblicato contenuto nel servizio di distribuzione peer, è stata fornita la funzione [**PeerDistServerUnpublish**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverunpublish) per consentire il contenuto non pubblicato. Una volta che il contenuto non è stato pubblicato, il servizio di distribuzione peer locale non fornirà più le informazioni sul contenuto associate a tale contenuto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="asynchronous-completions"></a>Completamenti asincroni

L'API di distribuzione peer supporta un modello API asincrono e, di conseguenza, le API di distribuzione peer consentono l'uso di porte o eventi di completamento di I/O come meccanismi di segnalazione per l'elaborazione dei completamenti di operazioni di distribuzione di peer asincroni. Per uno dei due meccanismi, la distribuzione peer utilizza una struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) . In generale, la distribuzione peer acquisisce la proprietà di una struttura **sovrapposta** e di tutti i parametri out che il client passa alle funzioni API asincrone. Il client non deve accedere a queste risorse finché la funzione asincrona specifica non viene completata. Non appena le funzioni asincrone vengono completate, il servizio di distribuzione peer non richiede più l'accesso a queste risorse e può essere riutilizzato perché l'applicazione chiamante si adatta.

Non vi sarà alcun completamento asincrono se la funzione restituisce un codice di errore diverso da i/o di **errore \_ \_ in sospeso**. La restituzione di un valore diverso da **Error \_ io \_ Pending** significa che la chiamata non è riuscita in modo sincrono. Se l'API di distribuzione peer restituisce un errore di i/o **\_ \_ in sospeso**, il chiamante deve attendere il completamento asincrono.

Il codice di errore del completamento asincrono può essere recuperato in uno dei due modi seguenti:

**Completamento basato sulla porta di completamento I/O**

L'utente richiama il meccanismo della porta di completamento I/O fornendo un handle della porta di completamento e una chiave di completamento per le funzioni API seguenti:

<dl>

[**PeerDistRegisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistregisterforstatuschangenotification)  
[**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream)  
[**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)  
[**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)  
</dl>

L'utente crea una porta di completamento chiamando [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport). Questo handle della porta di completamento può essere utilizzato contemporaneamente per altre operazioni di I/O asincrone, nonché per operazioni specifiche di distribuzione peer.

Il chiamante deve utilizzare la funzione [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) per gestire il completamento asincrono. Se l'operazione asincrona ha esito negativo, la funzione **GetQueuedCompletionStatus** restituirà **false** e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituirà il codice di errore appropriato. Il chiamante deve ignorare tutti i campi della struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) se il codice di errore è diverso da **Error \_ Success**. L'operazione asincrona ha esito positivo se la funzione **GetQueuedCompletionStatus** restituisce **true**.

Per ulteriori informazioni, vedere [porte di completamento I/O](/windows/desktop/FileIO/i-o-completion-ports).

**Completamento basato su eventi**

Se il chiamante imposta un handle di evento valido per il campo *hEvent* della struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) , la distribuzione peer la utilizza per segnalare che l'operazione di i/O asincrona associata è stata completata.

Un chiamante del thread può gestire le operazioni sovrapposte specificando un handle per l'oggetto evento di reimpostazione manuale della struttura [**sovrapposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) in una delle funzioni di attesa. Dopo che l'evento viene segnalato, il chiamante deve chiamare [**PeerGetOverlappedResult**](https://www.bing.com/search?q=**PeerGetOverlappedResult**) passando la struttura **sovrapposta** appropriata. **PeerGetOverlappedResult** restituirà **false** e il chiamante deve chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per recuperare il codice di errore. Il chiamante deve ignorare tutti i campi della struttura **sovrapposta** se il codice di errore è diverso da **Error \_ Success**. L'operazione asincrona ha esito positivo se la funzione **PeerGetOverlappedResult** restituisce **true**.

Se il chiamante fornisce una porta di completamento insieme a un evento, l'evento verrà usato come meccanismo di completamento.

**Windows 7:** Usare la funzione [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) anziché [**PeerGetOverlappedResult**](https://www.bing.com/search?q=**PeerGetOverlappedResult**).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento all'API di distribuzione peer](peer-distribution-api-reference.md)
</dt> </dl>

 

