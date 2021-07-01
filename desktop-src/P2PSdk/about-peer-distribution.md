---
description: L'API di distribuzione peer, che supporta la funzionalità Branch Cache in Windows 7, Windows Server 2008 R2, Windows 8 e Windows Server 2012, offre un set di API della piattaforma che possono aumentare la velocità di risposta di rete delle applicazioni centralizzate quando si accede da uffici remoti e consentono di ridurre l'utilizzo complessivo della rete WAN (Wide Area Network) senza interferire con le tecnologie di sicurezza di rete.
ms.assetid: feb9666e-563a-49f4-ad1c-f166a0faff31
title: Informazioni sulla distribuzione peer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c996aed35ac691284ba61b757d6ff5a88033aad
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120436"
---
# <a name="about-peer-distribution"></a>Informazioni sulla distribuzione peer

L'API di distribuzione peer, che supporta la funzionalità Branch Cache in Windows 7, Windows Server 2008 R2, Windows 8 e Windows Server 2012, offre un set di API della piattaforma che possono aumentare la velocità di risposta di rete delle applicazioni centralizzate quando si accede da uffici remoti e consentono di ridurre l'utilizzo complessivo della rete WAN (Wide Area Network) senza interferire con le tecnologie di sicurezza di rete.

Il sistema di distribuzione peer offre un set di API della piattaforma utilizzate dagli editori che forniscono contenuti digitali e consumer che lo richiedono. Per distinguere facilmente questi ruoli, può essere più semplice pensare all'autore in un ruolo del server e al consumer in un ruolo client. A parte questo, è importante ricordare che, a parte questi ruoli concettuali, il servizio di distribuzione peer è un vero e proprio sistema peer, come indicato dalla possibilità per qualsiasi nodo di distribuzione peer di pubblicare e utilizzare contenuto digitale. Le API della piattaforma di distribuzione peer vengono esposte agli editori e ai consumer da una libreria di importazione Win32 (**PeerDist.Lib**).

Il ciclo di vita del contenuto fornito da un editore e recuperato da un consumer con il servizio di distribuzione peer è costituito dalle operazioni seguenti:



|                         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Pubblicazione del contenuto** | La pubblicazione viene eseguita per produrre una descrizione del contenuto, in breve Informazioni sul **contenuto** o **Informazioni** sul contenuto. Queste informazioni sul contenuto possono quindi essere usate da un'istanza del servizio di distribuzione peer per autenticare e ricompilare il contenuto. Quando il contenuto viene pubblicato da un'applicazione nel servizio di distribuzione peer, che concettualmente è un'operazione sul lato server, tale contenuto viene associato all'identità del server di pubblicazione, che si basa sul SID dell'utente associato al token di accesso del thread. Questa associazione viene eseguita per limitare l'accesso al contenuto da parte di entità non autorizzate. È tuttavia importante notare che l'accesso alle informazioni sul contenuto equivale all'accesso al contenuto stesso, perché le informazioni sul contenuto possono essere usate per ottenere il contenuto dai peer o da una cache ospitata.<br/> È disponibile una nuova versione della struttura dei dati delle informazioni sul contenuto in Windows 8; Tuttavia, la versione precedente è ancora supportata. Per interagire con i client Windows 7, un amministratore può configurare il servizio di distribuzione peer per l'uso della versione precedente della struttura dei dati di informazioni sul contenuto.<br/> |
| **Recupero del contenuto**   | Perché un consumer recupeni contenuto dal servizio di distribuzione peer, è necessario fornire l'accesso alle informazioni sul contenuto pubblicate associate a tale contenuto. Il servizio di distribuzione peer usato per pubblicare il contenuto può fornire le informazioni sul contenuto associate. Quando il consumer ha le informazioni sul contenuto, è possibile usare altre API di distribuzione peer per richiedere il contenuto dal servizio di distribuzione peer. Il servizio di distribuzione peer tenterà di recuperare il contenuto dalla rete locale. Se il contenuto non è disponibile, l'applicazione client è responsabile del recupero del contenuto dal server di origine.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| **Rimozione della pubblicazione** | Per le applicazioni che hanno pubblicato contenuto nel servizio di distribuzione peer, è stata fornita la funzione [**PeerDistServerUnpublish**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverunpublish) per consentire l'annullamento della pubblicazione del contenuto. Dopo l'annullamento della pubblicazione del contenuto, il servizio di distribuzione peer locale non fornirà più le informazioni sul contenuto associate a tale contenuto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="asynchronous-completions"></a>Completamenti asincroni

L'API di distribuzione peer supporta un modello API asincrono e di conseguenza le API di distribuzione peer consentono l'uso di porte di completamento I/O o eventi come meccanismi di segnalazione per l'elaborazione dei completamenti asincroni delle operazioni di distribuzione peer. Per entrambi i meccanismi, la distribuzione peer usa una [**struttura OVERLAPPED.**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) In generale, la distribuzione peer assume la proprietà di una struttura **OVERLAPPED** ed eventuali parametri out passati dal client alle funzioni API asincrone. Il client non deve accedere a queste risorse fino al completamento della funzione asincrona specifica. Non appena le funzioni asincrone vengono completate, il servizio di distribuzione peer non richiederà più l'accesso a queste risorse e potrebbe essere riutilizzato in base alle esigenze dell'applicazione chiamante.

Non sarà presente alcun completamento asincrono se la funzione restituisce codice di errore diverso da **ERROR \_ IO \_ PENDING.** La restituzione di un valore diverso da **ERROR \_ IO \_ PENDING** indica che la chiamata non è riuscita in modo sincrono. Se l'API di distribuzione peer restituisce **ERROR \_ IO \_ PENDING**, il chiamante deve attendere il completamento asincrono.

Il codice di errore del completamento asincrono può essere recuperato in uno dei due modi seguenti:

**Completamento basato sulla porta di completamento I/O**

L'utente richiama il meccanismo di porta di completamento I/O fornendo un handle di porta di completamento e una chiave di completamento alle funzioni API seguenti:

<dl>

[**PeerDistRegisterForStatusChangeNotification**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistregisterforstatuschangenotification)  
[**PeerDistServerPublishStream**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserverpublishstream)  
[**PeerDistServerOpenContentInformation**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistserveropencontentinformation)  
[**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent)  
</dl>

L'utente crea una porta di completamento chiamando [**CreateIoCompletionPort.**](/windows/desktop/FileIO/createiocompletionport) Questo handle di porta di completamento può essere usato contemporaneamente per altre operazioni di I/O asincrone e per operazioni specifiche della distribuzione peer.

Il chiamante deve usare [**la funzione GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) per gestire il completamento asincrono. Se l'operazione asincrona non riesce, la funzione **GetQueuedCompletionStatus** restituirà **FALSE** e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) restituirà il codice di errore appropriato. Il chiamante deve ignorare tutti i campi della struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) se il codice di errore è diverso da **ERROR \_ SUCCESS.** L'operazione asincrona ha esito positivo **se la funzione GetQueuedCompletionStatus** restituisce **TRUE.**

Per altre informazioni, vedere [Porte di completamento I/O.](/windows/desktop/FileIO/i-o-completion-ports)

**Completamento basato su eventi**

Se il chiamante imposta un handle di evento valido per il campo *hEvent* della struttura [**OVERLAPPED,**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) la distribuzione peer lo usa per segnalare che l'operazione di I/O asincrona associata è stata completata.

Un chiamante del thread può gestire le operazioni sovrapposte specificando un handle per l'oggetto evento di reimpostazione manuale della struttura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) in una delle funzioni di attesa. Dopo la segnalazione dell'evento, il chiamante deve [**chiamare PeerGetOverlappedResult passando**](https://www.bing.com/search?q=**PeerGetOverlappedResult**) la struttura **OVERLAPPED** appropriata. **PeerGetOverlappedResult** restituirà **FALSE** e il chiamante deve chiamare [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per recuperare il codice di errore. Il chiamante deve ignorare tutti i campi della struttura **OVERLAPPED** se il codice di errore è diverso **da ERROR \_ SUCCESS.** L'operazione asincrona ha esito positivo se la **funzione PeerGetOverlappedResult** restituisce **TRUE.**

Se il chiamante fornisce una porta di completamento insieme a un evento, l'evento verrà usato come meccanismo di completamento.

**Windows 7:** Usare la [**funzione GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) anziché [**PeerGetOverlappedResult**](https://www.bing.com/search?q=**PeerGetOverlappedResult**).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulle API di distribuzione peer](peer-distribution-api-reference.md)
</dt> </dl>

 

