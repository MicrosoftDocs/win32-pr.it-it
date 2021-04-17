---
description: Il raggruppamento peer-to-peer è una tecnologia che consente a uno sviluppatore di creare una rete peer sicura in modo rapido ed efficace.
ms.assetid: ee72f60b-1e5b-4b69-bda0-2ae80734c144
title: Come lavorare con i gruppi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7bebf958d0c3fdee6ad0dc400d495c54ec2e6fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529125"
---
# <a name="how-to-work-with-groups"></a>Come lavorare con i gruppi

Il raggruppamento peer-to-peer è una tecnologia che consente a uno sviluppatore di creare una rete peer sicura in modo rapido ed efficace. Nell'elenco seguente sono riportate le considerazioni principali per la creazione di un'applicazione di raggruppamento peer.

-   [Ottenere un'identità peer](#obtaining-a-peer-identity)
-   [Avvio di un gruppo peer](#starting-up-the-peer-grouping-infrastructure)
-   [Registrazione per gli eventi di raggruppamento](#registering-for-peer-grouping-events)
-   [Connessione a un gruppo](#obtaining-a-group-handle)
-   [Creazione di ruoli amministratore e membro](#creating-administrator-and-member-roles)
-   [Ricerca di un peer](#finding-a-peer)
-   [Connessione diretta a un peer](#connecting-directly-to-a-peer)
-   [Chiusura e arresto di un gruppo](#closing-and-shutting-down-a-peer-group)

## <a name="obtaining-a-peer-identity"></a>Ottenere un'identità peer

Prima di creare o connettersi a un gruppo, un peer deve ottenere un'identità peer, ovvero un nome usato per identificare in modo univoco un peer per un gruppo. Per ottenere un elenco enumerato di tutte le identità peer definite nel peer, chiamare [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities), che restituisce un handle per l'enumerazione. Per ottenere le identità peer, chiamare [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) con l'handle dell'enumerazione e il numero di membri da recuperare. Continuare a chiamare **PeerGetNextItem** fino a quando il parametro *pcount* non restituisce un valore inferiore al numero di identità peer richieste.

Se non esiste un'identità peer per il peer, è possibile crearla chiamando [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate). Dopo aver creato un'identità peer, il peer genera un BLOB XML di identità che contiene la chiave pubblica assegnata

Le informazioni sull'identità peer vengono ottenute chiamando [**PeerIdentityGetXML**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml). Queste informazioni sull'identità del peer vengono usate dall'autore del gruppo o da un amministratore per emettere le credenziali necessarie per partecipare al gruppo, come un BLOB XML di invito.

Per ulteriori informazioni sulle identità peer, consultare la documentazione dell' [API di Identity Manager](identity-manager-api.md)

## <a name="starting-up-the-peer-grouping-infrastructure"></a>Avvio dell'infrastruttura di raggruppamento dei peer

Prima che qualsiasi funzione nell'API di raggruppamento peer venga chiamata da un'applicazione, è necessario chiamare [**PeerGroupStartup**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) . Questa funzione Inizializza l'infrastruttura di raggruppamento peer per l'applicazione e imposta la versione supportata.

## <a name="obtaining-a-group-handle"></a>Ottenere un handle di gruppo

Per connettersi a un gruppo e iniziare a partecipare, è necessario ottenere un handle per un gruppo peer. Nell'elenco seguente vengono identificati i tre modi per connettersi a un gruppo peer:

-   Creazione di un gruppo peer chiamando [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), che Inizializza un nuovo gruppo peer e restituisce un handle valido con il peer come proprietario e amministratore esclusivo.
-   Unione di un gruppo peer chiamando [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin). Per partecipare a un gruppo peer, un peer deve ricevere un invito da un amministratore del gruppo peer. Per ottenere un invito, inviare il BLOB XML delle informazioni di identità all'amministratore che crea un invito e lo invia all'utente tramite un meccanismo esterno, ad esempio posta elettronica o FTP. L'invito e l'identità del peer vengono passati a **PeerGroupJoin**, che restituisce un handle valido al gruppo.
-   Apertura di un gruppo peer a cui è stato aggiunto un peer precedentemente chiamando [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen). In questa situazione, non è necessario ottenere un invito.

Dopo aver ottenuto un handle di gruppo peer valido da una delle funzioni sopra riportate, è possibile connettersi a un gruppo peer chiamando [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) con il nuovo handle.

> [!Note]  
> Se la connessione a un gruppo peer ha esito negativo \_ , \_ si verifica l'evento di connessione all'evento di gruppo peer \_ \_ non riuscita. Il gestore può tentare di ristabilire la connessione al gruppo peer.

 

## <a name="registering-for-peer-grouping-events"></a>Registrazione per eventi di raggruppamento peer

Prima che un peer partecipi a un gruppo peer, è necessario che il peer si registri per gli eventi del gruppo peer. Per eseguire la registrazione per eventi peer specifici, chiamare [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)e passare uno o più tipi di evento peer definiti nel tipo di \_ evento del gruppo peer \_ \_ . È necessario registrarsi per ogni evento peer applicabile all'applicazione; per ricevere i dati tramite una connessione diretta, ad esempio, effettuare la registrazione per gli eventi di connessione diretta degli eventi del \_ gruppo peer \_ \_ \_ e \_ dei gruppi peer \_ \_ \_ . Ogni chiamata accetta un handle di evento e restituisce un handle **HPEEREVENT** per l'evento peer.

I gestori eventi possono ottenere i dati associati a un evento peer passando l'handle agli eventi peer registrati a [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata). Questi dati dell'evento peer vengono restituiti come \_ Unione di dati degli eventi del gruppo peer \_ \_ . Se la coda degli eventi peer è vuota, questa funzione restituisce il PEER \_ S \_ senza \_ dati dell'evento \_ .

È possibile annullare la registrazione per gli eventi del peer chiamando [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) e specificando l'handle per l'evento peer di cui si vuole annullare la registrazione. Dopo la chiamata della funzione, gli eventi peer associati all'handle non vengono più registrati.

## <a name="creating-administrator-and-member-roles"></a>Creazione di ruoli amministratore e membro

Il peer che crea il gruppo peer è noto come autore del gruppo peer e ha il ruolo di amministratore per impostazione predefinita. Solo l'autore del gruppo peer può impostare le proprietà del gruppo.

I peer invitati al gruppo peer possono essere un amministratore o un membro. Se viene assegnato un ruolo di amministratore dall'amministratore che emette l'invito, può invitare nuovi membri al gruppo peer e assegnare allo stesso modo il ruolo di amministratore ad altri membri.

I ruoli dei membri del gruppo peer sono impostati negli inviti che l'amministratore assegna a un membro. Per aggiungere altri amministratori, impostare il valore del parametro *proletari* di [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) su amministratore del \_ ruolo del gruppo peer \_ quando si \_ Crea un invito.

I membri possono partecipare a un gruppo peer, ma non possono invitare e autorizzare nuovi membri, impostare proprietà dei gruppi o aggiornare o eliminare i record di gruppo che non vengono creati in modo specifico. Per assegnare lo stato dei membri a un peer partecipante, impostare il valore del parametro **proletari** di [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) su \_ membro del ruolo del gruppo peer \_ \_ quando si crea un invito per quel peer.

Per modificare il ruolo di un membro, è necessario che le nuove credenziali contenenti il nuovo ruolo vengano rilasciate a tale membro. A tale scopo, ottenere la struttura delle [**\_ \_ informazioni sulle credenziali peer**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) per questo membro dalla \_ struttura del membro peer restituita da [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers). Modificare il campo **proletari** nelle **\_ \_ informazioni sulle credenziali peer** nel nuovo ruolo e passare la struttura a [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials).

Le nuove credenziali non verranno applicate al peer fino a quando non si connetteranno al gruppo peer. Se sono attualmente connesse, è necessario chiudere il gruppo e riconnettersi per ottenere le credenziali aggiornate.

## <a name="finding-a-peer"></a>Ricerca di un peer

Per ottenere un elenco enumerato di tutti i peer che partecipano al gruppo peer, chiamare [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) con l'handle di gruppo, che restituisce un handle per l'enumerazione. Per ottenere i membri, chiamare [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) con l'handle enum e il numero di membri da recuperare. Continuare a chiamare **PeerGetNextItem** fino a quando il parametro *pcount* non restituisce un valore inferiore al numero di membri richiesti. Si noti che non è possibile restituire l'elenco completo dei membri disponibili.

Ogni membro è rappresentato come struttura [**del \_ membro peer**](/windows/desktop/api/P2P/ns-p2p-peer_member) , che contiene l'identità del peer, gli ID del nodo e gli indirizzi IP per i peer attivi.

Al termine, chiudere l'enumerazione e rilasciare la memoria associata chiamando [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration).

## <a name="connecting-directly-to-a-peer"></a>Connessione diretta a un peer

Quando un peer è connesso a un gruppo peer, vengono avviati scambi diretti uno-a-uno con altri membri connessi chiamando [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) e specificando l'identità dell'altro peer. Questa chiamata è asincrona e restituisce un ID di connessione a 64 bit. Se la chiamata ha esito positivo, si riceve l'evento \_ \_ \_ \_ peer di evento peer di connessione diretta evento \_ per indicare che la connessione ha avuto esito positivo. Se la connessione ha esito positivo, l'ID connessione è valido e può essere utilizzato per inviare e ricevere dati tramite la connessione diretta.

Per essere in grado di ricevere connessioni dirette, è necessario che anche l'altro peer sia stato registrato in precedenza per l' \_ \_ \_ evento peer di connessione diretta all'evento del gruppo peer \_ .

Per inviare dati a un peer, chiamare [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) con un ID connessione valido. Per ricevere i dati, l'altro peer deve essere registrato per l' \_ \_ \_ \_ evento peer dei dati in ingresso dell'evento di gruppo peer. Analogamente, se il peer di invio desidera ricevere i dati a sua volta, è necessario registrarlo anche per l' \_ \_ \_ evento peer di dati in ingresso dell'evento di gruppo peer \_ .

Per ricevere il set totale di connessioni dirette attualmente attive con altri peer in un gruppo, chiamare [**PeerGroupEnumConnections**](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections) per aprire l'enumerazione e scorrere l'elenco delle connessioni usando [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem).

Per chiudere una connessione diretta, chiamare [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) e passare l'ID connessione.

## <a name="closing-and-shutting-down-a-peer-group"></a>Chiusura e arresto di un gruppo peer

Per chiudere una connessione a un gruppo peer, chiamare [**PeerGroupClose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose), che invalida l'handle di gruppo, ma non arresta l'infrastruttura di raggruppamento peer. I dati del gruppo peer-to-peer vengono eliminati chiamando [**PeerGroupDelete**](/windows/desktop/api/P2P/nf-p2p-peergroupdelete).

Quando l'applicazione ha terminato l'utilizzo dell'infrastruttura di raggruppamento dei peer, deve chiamare [**PeerGroupShutdown**](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown).

 

 



