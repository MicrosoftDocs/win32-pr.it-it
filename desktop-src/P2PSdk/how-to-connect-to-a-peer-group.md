---
description: Questo argomento illustra come un'applicazione si connette a un gruppo peer usando le API di raggruppamento peer.
ms.assetid: 56fa28d8-3b3a-4cd5-8448-c8c4ce8d0b2c
title: Come creare Connessione a un gruppo peer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb1cfd08fde0fc733873648dfae1ffb4f86b713b3ed790430686b641a893d23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118612767"
---
# <a name="how-to-connect-to-a-peer-group"></a>Come creare Connessione a un gruppo peer

Questo argomento illustra come un'applicazione si connette a un gruppo peer usando le API di raggruppamento peer.

## <a name="joining-a-peer-group"></a>Aggiunta a un gruppo peer

Per partecipare a un gruppo peer, chiamare [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), passando il nome dell'identità del peer e l'invito (e un nome cloud PNRP facoltativo, se il nome del cloud nell'invito è ambiguo).

In caso di esito positivo, [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) restituisce un handle al gruppo peer.

Se il peer è stato aggiunto in precedenza al gruppo peer e quindi ha chiuso l'handle, il gruppo peer deve essere riaperto chiamando [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) e passando il nome del gruppo peer. Questa chiamata restituisce un nuovo handle del gruppo peer.

Dopo aver aggiunto correttamente il gruppo peer, il peer può connettersi direttamente al gruppo peer e iniziare a interagire chiamando [**PeerGroupConnect.**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) Dopo la connessione, il peer viene considerato "online".

Se un'applicazione non interagirà con il gruppo al momento, può rimanere "offline". Se sceglie di partecipare direttamente al gruppo peer in un'istanza successiva, una chiamata successiva a [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) lo porterà online. Dopo che un peer è stato aggiunto al gruppo peer, deve connettersi almeno una volta prima di poter pubblicare record nel gruppo peer.

## <a name="opening-a-peer-group-without-connecting-offline"></a>Apertura di un gruppo peer senza connessione (offline)

Spesso, è possibile che un'applicazione si connetta a un gruppo peer ma non vi partecipa direttamente, ricevendo e pubblicando aggiornamenti dei record ma non inviando o ricevendo messaggi di dati. Un'applicazione si trova in questo stato "offline" immediatamente dopo la chiamata di [**PeerGroupCreate,**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate) [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)o [**PeerGroupOpen.**](/windows/desktop/api/P2P/nf-p2p-peergroupopen)

Un'applicazione offline può essere online in qualsiasi momento chiamando [**PeerGroupConnect.**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) Dopo la connessione, un gruppo peer non può passare offline fino a quando tutte le altre applicazioni associate a questa identità e che condividono questo gruppo non hanno chiuso le connessioni.

Un gruppo peer è una risorsa condivisa, con lo stesso gruppo peer disponibile per più applicazioni. Se più applicazioni per la stessa identità e Windows utente usano lo stesso gruppo peer, condividono anche lo stesso database sottostante e le stesse connessioni (adiacenti e diretti). Se una di queste applicazioni chiama [**PeerGroupConnect,**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)anche tutte le altre applicazioni per questa identità o utente che partecipano al gruppo si connettono al gruppo. Se un record viene aggiunto da un'applicazione mentre il gruppo è offline, anche altre applicazioni possono visualizzare il record. Di conseguenza, un'applicazione deve essere pronta per essere online in qualsiasi momento.

## <a name="connecting-to-a-peer-group-online"></a>Connessione a un gruppo peer (online)

Per iniziare a partecipare a un gruppo, chiamare [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) dopo la creazione, l'aggiunta o l'apertura del gruppo. In questo stato, le connessioni dirette possono essere aperte con altri peer che partecipano allo stesso gruppo chiamando [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection).

Per rilevare se un tentativo di connessione non è riuscito, registrarsi per l'evento PEER \_ GROUP \_ EVENT CONNECTION \_ \_ FAILED. Questo evento viene generato se l'infrastruttura di raggruppamento non riesce a trovare un altro membro a cui connettersi o se la connessione non riesce prima della sincronizzazione del database del gruppo e non è possibile stabilire un'altra connessione.

Anche se più applicazioni in esecuzione nel peer e che partecipano allo stesso gruppo con la stessa identità peer possono essere offline, una chiamata a [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) da una delle applicazioni comporta la divenire online per tutte le applicazioni.

Inoltre, se un'applicazione nel peer si è connessa al gruppo, anche tutte le altre applicazioni che chiamano [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) o [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) vengono connesse immediatamente. Se un'applicazione chiama [**PeerGroupClose,**](/windows/desktop/api/P2P/nf-p2p-peergroupclose)l'handle viene chiuso solo per tale applicazione. Di conseguenza, una chiamata successiva a **PeerGroupOpen** dall'applicazione restituisce un nuovo handle di gruppo e l'applicazione viene portata online immediatamente se tutte le altre applicazioni che partecipano allo stesso gruppo sono ancora connesse.

## <a name="sending-and-receiving-data"></a>Invio e ricezione di dati

Per inviare e ricevere dati tra nodi membri specifici nel gruppo, è necessario stabilire connessioni dirette con i membri con cui si intende interagire. Stabilire una connessione diretta è una chiamata asincrona a [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection), passando l'handle per un gruppo connesso e l'identità del peer all'interno del gruppo a cui ci si vuole connettere. Questo metodo restituirà un ID di connessione. Se la chiamata ha esito positivo, viene generato un evento \_ PEER GROUP EVENT DIRECT CONNECTION sul \_ \_ \_ peer, convalidando l'ID connessione.

Per ricevere connessioni dirette da altri peer online, registrarsi per l'evento PEER \_ GROUP EVENT DIRECT CONNECTION con una chiamata a \_ \_ \_ [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent).

Dopo aver stabilito una connessione diretta, l'applicazione può iniziare a inviare dati con chiamate a [**PeerGroupSendData,**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata)passando l'ID di connessione valido. L'ordinamento delle trasmissioni di dati multipart viene gestito da **PeerGroupSendData.** Tuttavia, le applicazioni devono implementare uno stack di protocollo appropriato per la gestione dei dati opachi restituiti da questa chiamata API.

Per ricevere dati tramite una connessione diretta, l'applicazione deve registrarsi per l'evento PEER \_ GROUP EVENT INCOMING DATA con \_ \_ \_ [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent). Il gestore eventi è responsabile di ottenere e ordinare i dati opachi e di passarlo all'applicazione. Questi dati vengono ottenuti all'interno del gestore eventi chiamando [**PeerGroupGetEventData con**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) l'handle per gli eventi registrati.

Una connessione diretta viene chiusa chiamando [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) e passando l'ID connessione ottenuto da una chiamata precedente a [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) o ricevuto nei dati dell'evento per PEER \_ EVENT GROUP DIRECT \_ \_ \_ CONNECTION.

 

 



