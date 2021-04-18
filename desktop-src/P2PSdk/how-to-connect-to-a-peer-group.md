---
description: Questo argomento illustra il modo in cui un'applicazione si connette a un gruppo peer usando le API di raggruppamento peer.
ms.assetid: 56fa28d8-3b3a-4cd5-8448-c8c4ce8d0b2c
title: Come connettersi a un gruppo peer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bb3f41342573742e634a6e7ebce283188f3ffd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312268"
---
# <a name="how-to-connect-to-a-peer-group"></a>Come connettersi a un gruppo peer

Questo argomento illustra il modo in cui un'applicazione si connette a un gruppo peer usando le API di raggruppamento peer.

## <a name="joining-a-peer-group"></a>Aggiunta a un gruppo peer

Per partecipare a un gruppo peer, chiamare [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin), passando il nome dell'identità del peer e l'invito (e un nome di Cloud PNRP facoltativo, se il nome del cloud nell'invito è ambiguo).

In caso di esito positivo, [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) restituisce un handle al gruppo peer.

Se il peer è stato aggiunto in precedenza al gruppo peer e l'handle è stato chiuso, il gruppo peer deve essere riaperto chiamando [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) e passando il nome del gruppo peer. Questa chiamata restituisce un nuovo handle del gruppo peer.

Una volta che il gruppo peer è stato aggiunto correttamente, il peer può connettersi direttamente al gruppo peer e iniziare a interagire chiamando [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect). Dopo la connessione, il peer viene considerato "online".

Se un'applicazione non è in grado di interagire con il gruppo al momento, può rimanere "offline". Se si sceglie di partecipare direttamente al gruppo peer in un'istanza successiva, una chiamata successiva a [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) lo porta online. Dopo che un peer è stato aggiunto al gruppo peer, deve connettersi almeno una volta prima che sia in grado di pubblicare i record nel gruppo peer.

## <a name="opening-a-peer-group-without-connecting-offline"></a>Apertura di un gruppo peer senza connessione (offline)

Spesso può essere necessario che un'applicazione si connetta a un gruppo peer, ma non la partecipi direttamente, riceve e pubblica gli aggiornamenti dei record, ma non invia o riceve messaggi di dati. Un'applicazione è in questo stato "offline" immediatamente dopo la chiamata a [**PeerGroupCreate**](/windows/desktop/api/P2P/nf-p2p-peergroupcreate), [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin)o [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) .

Un'applicazione offline può essere spostata online in qualsiasi momento chiamando [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect). Una volta stabilita la connessione, un gruppo peer non può passare alla modalità offline finché tutte le altre applicazioni associate a questa identità e che condividono questo gruppo non avranno anche connessioni chiuse.

Un gruppo peer è una risorsa condivisa con lo stesso gruppo peer disponibile per più applicazioni. Se più di un'applicazione per la stessa identità e l'utente di Windows utilizza lo stesso gruppo peer, condividono anche lo stesso database e le stesse connessioni sottostanti (Neighbor e Direct). Se una di queste applicazioni chiama [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect), tutte le altre applicazioni per questa identità/utente che partecipano al gruppo si connetteranno anche al gruppo. Se un record viene aggiunto da un'applicazione mentre il gruppo è offline, è possibile visualizzarne anche altre applicazioni. Di conseguenza, un'applicazione deve essere pronta per essere portata online in qualsiasi momento.

## <a name="connecting-to-a-peer-group-online"></a>Connessione a un gruppo peer (online)

Per iniziare a partecipare a un gruppo, chiamare [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) dopo la creazione, l'aggiunta o l'apertura del gruppo. In questo stato, le connessioni dirette possono essere aperte con altri peer che partecipano allo stesso gruppo chiamando [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection).

Per rilevare se un tentativo di connessione non è riuscito, effettuare la registrazione per l' \_ \_ evento di \_ connessione evento \_ non riuscita di un gruppo peer. Questo evento viene generato se l'infrastruttura di raggruppamento non riesce a trovare un altro membro a cui connettersi o se la connessione non riesce prima che il database del gruppo venga sincronizzato e non è possibile stabilire un'altra connessione.

Anche se più applicazioni eseguite sul peer e che partecipano allo stesso gruppo con la stessa identità peer possono essere offline, una chiamata a [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect) da parte di una qualsiasi delle applicazioni determina la modalità online per tutte le applicazioni.

Inoltre, se un'applicazione nel peer è connessa al gruppo, tutte le altre applicazioni che chiamano [**PeerGroupJoin**](/windows/desktop/api/P2P/nf-p2p-peergroupjoin) o [**PeerGroupOpen**](/windows/desktop/api/P2P/nf-p2p-peergroupopen) sono immediatamente connesse. Se un'applicazione chiama [**PeerGroupClose**](/windows/desktop/api/P2P/nf-p2p-peergroupclose), l'handle viene chiuso solo per tale applicazione. Quindi, una chiamata successiva a **PeerGroupOpen** da parte dell'applicazione restituisce un nuovo handle di gruppo e l'applicazione viene portata online immediatamente se le altre applicazioni che partecipano allo stesso gruppo sono ancora connesse.

## <a name="sending-and-receiving-data"></a>Invio e ricezione di dati

Per inviare e ricevere dati tra nodi membro specifici del gruppo, è necessario stabilire connessioni dirette con i membri con cui si intende interagire. Stabilire una connessione diretta è una chiamata asincrona a [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection), passando l'handle per un gruppo connesso e l'identità del peer all'interno del gruppo a cui ci si vuole connettere. Questo metodo restituirà un ID connessione. Se la chiamata ha esito positivo, \_ \_ viene generato un evento di connessione diretta a un evento del gruppo peer \_ \_ sul peer, convalidando l'ID connessione.

Per ricevere connessioni dirette da altri peer online, effettuare la registrazione per l' \_ evento di connessione diretta a eventi del gruppo peer \_ \_ \_ con una chiamata a [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent).

Una volta stabilita una connessione diretta, l'applicazione può iniziare a inviare dati con chiamate a [**PeerGroupSendData**](/windows/desktop/api/P2P/nf-p2p-peergroupsenddata), passando l'ID connessione valido. L'ordinamento delle trasmissioni di dati multipart è gestito da **PeerGroupSendData**. Tuttavia, le applicazioni devono implementare uno stack di protocolli appropriato per la gestione dei dati opachi restituiti da questa chiamata API.

Per ricevere dati tramite una connessione diretta, l'applicazione deve registrarsi per l' \_ \_ evento di \_ dati in ingresso evento del gruppo peer \_ con [**PeerGroupRegisterEvent**](/windows/desktop/api/P2P/nf-p2p-peergroupregisterevent). Il gestore eventi è responsabile dell'acquisizione e dell'ordinamento dei dati opachi e della relativa passata all'applicazione. Questi dati vengono ottenuti nel gestore eventi chiamando [**PeerGroupGetEventData**](/windows/desktop/api/P2P/nf-p2p-peergroupgeteventdata) con l'handle per gli eventi registrati.

Una connessione diretta viene chiusa chiamando [**PeerGroupCloseDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupclosedirectconnection) e passando l'ID connessione ottenuto da una precedente chiamata a [**PeerGroupOpenDirectConnection**](/windows/desktop/api/P2P/nf-p2p-peergroupopendirectconnection) o ricevuta nei dati dell'evento per la \_ \_ connessione diretta del gruppo di eventi peer \_ \_ .

 

 



