---
description: Il raggruppamento peer-to-peer è una tecnologia che consente a uno sviluppatore di creare una rete peer sicura in modo rapido ed efficace.
ms.assetid: ee72f60b-1e5b-4b69-bda0-2ae80734c144
title: Come usare i gruppi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bce7280afe226fea20cde633a3971f62f606e1814ad4ab62bcc09025a125e72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519391"
---
# <a name="how-to-work-with-groups"></a>Come usare i gruppi

Il raggruppamento peer-to-peer è una tecnologia che consente a uno sviluppatore di creare una rete peer sicura in modo rapido ed efficace. L'elenco seguente identifica le considerazioni principali per la creazione di un'applicazione di raggruppamento peer.

-   [Recupero di un'identità peer](#obtaining-a-peer-identity)
-   [Avvio di un gruppo peer](#starting-up-the-peer-grouping-infrastructure)
-   [Registrazione per gli eventi di raggruppamento](#registering-for-peer-grouping-events)
-   [Connessione a un gruppo](#obtaining-a-group-handle)
-   [Creazione di ruoli di amministratore e membro](#creating-administrator-and-member-roles)
-   [Ricerca di un peer](#finding-a-peer)
-   [Connessione diretta a un peer](#connecting-directly-to-a-peer)
-   [Chiusura e arresto di un gruppo](#closing-and-shutting-down-a-peer-group)

## <a name="obtaining-a-peer-identity"></a>Recupero di un'identità peer

Prima di creare o connettersi a un gruppo, un peer deve ottenere un'identità peer, ovvero un nome usato per identificare in modo univoco un peer a un gruppo. Per ottenere un elenco enumerato di tutte le identità peer definite nel peer, chiamare [**PeerEnumIdentities**](/windows/desktop/api/P2P/nf-p2p-peerenumidentities), che restituisce un handle per l'enumerazione. Per ottenere le identità peer, chiamare [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) con l'handle di enumerazione e il numero di membri da recuperare. Continuare a **chiamare PeerGetNextItem** finché il *parametro pCount* non restituisce un valore minore del numero di identità peer richieste.

Se non esiste un'identità peer per il peer, è possibile crearla chiamando [**PeerIdentityCreate**](/windows/desktop/api/P2P/nf-p2p-peeridentitycreate). Dopo aver creato un'identità peer, il peer genera un BLOB XML di identità che contiene la chiave pubblica assegnata

Le informazioni sull'identità peer vengono ottenute chiamando [**PeerIdentityGetXML.**](/windows/desktop/api/P2P/nf-p2p-peeridentitygetxml) Queste informazioni sull'identità peer vengono usate dall'autore del gruppo o da un amministratore per rilasciare le credenziali necessarie per l'aggiunta al gruppo, come BLOB XML di invito.

Per altre informazioni sulle identità peer, vedere la documentazione [dell'API di Identity Manager](identity-manager-api.md)

## <a name="starting-up-the-peer-grouping-infrastructure"></a>Avvio dell'infrastruttura di raggruppamento peer

Prima che qualsiasi funzione nell'API Di raggruppamento peer venga chiamata da un'applicazione, è necessario [**chiamare PeerGroupStartup.**](/windows/desktop/api/P2P/nf-p2p-peergroupstartup) Questa funzione inizializza l'infrastruttura di raggruppamento peer per l'applicazione e imposta la versione supportata.

## <a name="obtaining-a-group-handle"></a>Recupero di un handle di gruppo

Per connettersi a un gruppo e iniziare a partecipare, è necessario ottenere un handle a un gruppo peer. L'elenco seguente identifica i tre modi per connettersi a un gruppo peer:

-   Creazione di un gruppo peer chiamando [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), che inizializza un nuovo gruppo peer e restituisce un handle valido con il peer come proprietario e amministratore unico.
-   Aggiunta a un gruppo peer chiamando [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin). Per partecipare a un gruppo peer, un peer deve ricevere un invito da un amministratore del gruppo peer. Per ottenere un invito, inviare il BLOB XML delle informazioni di identità all'amministratore che crea un invito e lo invia all'utente tramite un meccanismo esterno, ad esempio posta elettronica o FTP. L'invito e l'identità peer vengono passati a **PeerGroupJoin**, che restituisce un handle valido per il gruppo.
-   Apertura di un gruppo peer a cui un peer è stato aggiunto in precedenza chiamando [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen). In questo caso, non è necessario ottenere un invito.

Dopo aver ottenuto un handle di gruppo peer valido da una delle funzioni precedenti, è possibile connettersi a un gruppo peer chiamando [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) con il nuovo handle.

> [!Note]  
> Se la connessione a un gruppo peer ha esito negativo, si verifica l'evento PEER \_ GROUP \_ EVENT CONNECTION \_ \_ FAILED. Il gestore può tentare di ristabilire la connessione al gruppo peer.

 

## <a name="registering-for-peer-grouping-events"></a>Registrazione per gli eventi di raggruppamento peer

Prima che un peer partecipi a un gruppo peer, il peer deve registrarsi per gli eventi del gruppo peer. Per eseguire la registrazione per eventi peer specifici, chiamare [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent)e passare uno o più tipi di evento peer definiti in PEER \_ GROUP EVENT \_ \_ TYPE. È necessario registrarsi per ogni evento peer che si applica all'applicazione. Ad esempio, per ricevere dati tramite una connessione diretta, registrarsi per gli eventi PEER GROUP EVENT DIRECT CONNECTION e \_ PEER GROUP EVENT INCOMING \_ \_ \_ \_ \_ \_ \_ DATA. Ogni chiamata accetta un handle di evento e restituisce un handle **HPEEREVENT** per tale evento peer.

I gestori eventi possono ottenere i dati associati a un evento peer passando l'handle agli eventi peer registrati [**a PeerGroupGetEventData.**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) Questi dati dell'evento peer vengono restituiti come unione \_ DATI \_ EVENTI GRUPPO \_ PEER. Se la coda di eventi peer è vuota, questa funzione restituisce PEER \_ S \_ NO EVENT \_ \_ DATA.

È possibile annullare la registrazione per gli eventi peer chiamando [**PeerGroupUnregisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupunregisterevent) e fornendo l'handle per l'evento peer di cui annullare la registrazione. Dopo la chiamata della funzione, gli eventi peer associati all'handle non vengono più registrati.

## <a name="creating-administrator-and-member-roles"></a>Creazione di ruoli di amministratore e membro

Il peer che crea il gruppo peer è noto come autore del gruppo peer e ha il ruolo di amministratore per impostazione predefinita. Solo l'autore del gruppo peer può impostare le proprietà del gruppo.

I peer invitati al gruppo peer possono essere un amministratore o un membro. Se viene assegnato un ruolo di amministratore dall'amministratore che emette l'invito, può invitare nuovi membri al gruppo peer e allo stesso modo assegnare il ruolo di amministratore ad altri membri.

I ruoli dei membri del gruppo peer vengono impostati negli inviti assegnati dall'amministratore a un membro. Per aggiungere altri amministratori, impostare il valore del *parametro pRoles* di [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) su PEER GROUP ROLE ADMIN durante \_ la creazione di un \_ \_ invito.

I membri possono partecipare a un gruppo peer, ma non possono invitare e autorizzare nuovi membri, impostare le proprietà del gruppo o aggiornare o eliminare record di gruppo che non creano in modo specifico. Per assegnare lo stato del membro a un peer partecipante, impostare il valore del parametro **pRoles** di [**PeerGroupCreateInvitation**](/windows/desktop/api/P2P/nf-p2p-peergroupcreateinvitation) su PEER GROUP ROLE MEMBER quando si crea un invito per \_ tale \_ \_ peer.

Per modificare il ruolo di un membro, è necessario che a tale membro siano rilasciate nuove credenziali contenenti il nuovo ruolo. A tale scopo, ottenere la [**struttura PEER \_ CREDENTIAL \_ INFO**](/windows/desktop/api/P2P/ns-p2p-peer_credential_info) per questo membro dalla struttura PEER \_ MEMBER restituita da [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers). Modificare il **campo pRoles** in **PEER CREDENTIAL \_ \_ INFO** nel nuovo ruolo e passare la struttura a [**PeerGroupIssueCredentials**](/windows/desktop/api/P2P/nf-p2p-peergroupissuecredentials).

Le nuove credenziali non saranno effettive per il peer fino a quando non si connettono al gruppo peer. Se sono attualmente connessi, devono chiudere il gruppo e riconnettersi per ottenere le credenziali aggiornate.

## <a name="finding-a-peer"></a>Ricerca di un peer

Per ottenere un elenco enumerato di tutti i peer che partecipano al gruppo peer, chiamare [**PeerGroupEnumMembers**](/windows/desktop/api/P2P/nf-p2p-peergroupenummembers) con l'handle del gruppo, che restituisce un handle per l'enumerazione. Per ottenere i membri, chiamare [**PeerGetNextItem con**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem) l'handle di enumerazione e il numero di membri da recuperare. Continuare a **chiamare PeerGetNextItem** finché il *parametro pCount* non restituisce un valore minore del numero di membri richiesti. Si noti che l'elenco completo dei membri disponibili potrebbe non essere restituito.

Ogni membro è rappresentato come una struttura [**PEER \_ MEMBER,**](/windows/desktop/api/P2P/ns-p2p-peer_member) che contiene l'identità del peer, gli ID nodo e gli indirizzi IP per i peer attivi.

Al termine, chiudere l'enumerazione e rilasciare la memoria associata chiamando [**PeerEndEnumeration**](/windows/desktop/api/P2P/nf-p2p-peerendenumeration).

## <a name="connecting-directly-to-a-peer"></a>Connessione diretta a un peer

Quando un peer è connesso a un gruppo peer, gli scambi diretti uno-a-uno con altri membri connessi vengono avviati chiamando [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) e fornendo l'identità dell'altro peer. Questa chiamata è asincrona e restituisce un ID di connessione a 64 bit. Se la chiamata ha esito positivo, si riceve l'evento peer PEER \_ GROUP EVENT DIRECT CONNECTION event per indicare che la connessione ha esito \_ \_ \_ \_ positivo. Se la connessione ha esito positivo, l'ID connessione è valido e può essere usato per inviare e ricevere dati tramite la connessione diretta.

Per poter ricevere connessioni dirette, anche l'altro peer deve essere stato registrato in precedenza per l'evento peer PEER \_ \_ GROUP EVENT DIRECT \_ \_ CONNECTION.

Per inviare dati a un peer, chiamare [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata) con un ID di connessione valido. Per ricevere dati, l'altro peer deve essere registrato per l'evento peer PEER \_ \_ GROUP EVENT INCOMING \_ \_ DATA. Analogamente, se il peer mittente vuole ricevere i dati a sua volta, deve essere registrato anche per l'evento peer PEER \_ GROUP \_ EVENT INCOMING \_ \_ DATA.

Per ricevere il set totale di connessioni dirette attualmente attive con altri peer in un gruppo, chiamare [**PeerGroupEnumConnections**](/windows/desktop/api/P2P/nf-p2p-peergroupenumconnections) per aprire l'enumerazione e scorrere l'elenco di connessioni tramite [**PeerGetNextItem**](/windows/desktop/api/P2P/nf-p2p-peergetnextitem).

Per chiudere una connessione diretta, chiamare [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) e passare l'ID connessione.

## <a name="closing-and-shutting-down-a-peer-group"></a>Chiusura e arresto di un gruppo peer

Per chiudere una connessione a un gruppo peer, chiamare [**PeerGroupClose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose), che invalida l'handle del gruppo, ma non arresta l'infrastruttura di raggruppamento peer. I dati del gruppo peer-to-peer vengono eliminati chiamando [**PeerGroupDelete.**](/windows/desktop/api/P2P/nf-p2p-peergroupdelete)

Al termine dell'uso dell'infrastruttura di raggruppamento peer, l'applicazione deve chiamare [**PeerGroupShutdown.**](/windows/desktop/api/P2P/nf-p2p-peergroupshutdown)

 

 



