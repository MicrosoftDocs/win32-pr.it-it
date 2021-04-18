---
description: Questo argomento descrive considerazioni specifiche sulla programmazione quando si usa l'infrastruttura peer.
ms.assetid: 525b0625-ec13-4aba-a741-dbacff3587f9
title: Considerazioni sulla programmazione (peer-to-peer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89956cbdbbc8d2ed89226a490bbae505862ab18f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312226"
---
# <a name="programming-considerations-peer-to-peer"></a>Considerazioni sulla programmazione (peer-to-peer)

Questo argomento descrive considerazioni specifiche sulla programmazione quando si usa l'infrastruttura peer.

Quando si usa l'infrastruttura peer per sviluppare applicazioni peer, è necessario tenere conto delle considerazioni di programmazione seguenti:

-   IPv6

    Per l'infrastruttura peer è necessario che IPv6 sia installato e avviato per consentire il funzionamento delle applicazioni di rete peer.

-   Porte del firewall

    Quando si utilizza un firewall in una rete, ad esempio il firewall della connessione Internet IPv6, è necessario aprire porte specifiche per consentire il funzionamento dell'infrastruttura peer. È necessario aprire le seguenti porte:

    Porta TCP 3587 per l'infrastruttura di raggruppamento peer.

    Porta UDP 3540 per l'infrastruttura di Peer Graphing.

    > [!Note]  
    > Le applicazioni che utilizzano l'infrastruttura peer Graphing su TCP scelgono la propria porta TCP quando chiamano [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).

     

-   Opzione socket

    Quando si tenta di connettersi direttamente ad altri nodi peer IPv6 (senza usare l'infrastruttura peer), assicurarsi che il livello di protezione IPV6 dell'opzione socket \_ \_ sia impostato sul **livello di protezione \_ \_ senza restrizioni**.

-   Larghezza di banda

    Quando si usa PNRP, un'applicazione può pubblicare uno o più [nomi di peer](peer-names.md) che possono essere risolti. Per ogni nome peer registrato con PNRP, si verifica un aumento della larghezza di banda di rete usato da PNRP per pubblicare il nome peer e lo si mantiene disponibile per la risoluzione da parte di altri nodi.

    Per evitare di utilizzare troppa larghezza di banda, le applicazioni devono evitare di registrare un numero elevato di nomi di peer in un computer. Ad esempio, un'applicazione che pubblica immagini non deve creare un nome peer per ogni immagine, ma deve creare un nome peer per il servizio che pubblica le immagini e usare un protocollo diverso per consentire ai client di eseguire query sul servizio per immagini specifiche.

-   Registrazione del nome peer

    È possibile che alcune applicazioni debbano registrare lo stesso [nome peer](peer-names.md) in più di un computer. In genere, ciò si verifica se un nome peer è associato a una persona che utilizza più di un computer. Un metodo che è possibile utilizzare per registrare lo stesso nome peer in più computer consiste nel creare un gruppo peer per la persona e connettersi a tale gruppo da tutti i computer. Un altro metodo consiste nel creare un'identità peer e un nome peer in un computer, esportare l'identità peer dal computer e importarla in altri computer. In questo modo è possibile creare lo stesso nome peer sicuro in tutti i computer che hanno importato l'identità peer.

 

 



