---
description: Questo argomento illustra considerazioni specifiche sulla programmazione quando si usa l'infrastruttura peer.
ms.assetid: 525b0625-ec13-4aba-a741-dbacff3587f9
title: Considerazioni sulla programmazione (peer-to-peer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d5af967503c216422e3a12572aeeaf91d751473f88d8589c2e125894721b41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119518061"
---
# <a name="programming-considerations-peer-to-peer"></a>Considerazioni sulla programmazione (peer-to-peer)

Questo argomento illustra considerazioni specifiche sulla programmazione quando si usa l'infrastruttura peer.

Quando si usa l'infrastruttura peer per sviluppare applicazioni peer, è necessario tenere in considerazione le considerazioni di programmazione seguenti:

-   IPv6

    L'infrastruttura peer richiede che IPv6 sia installato e avviato per consentire il funzionamento delle applicazioni di rete peer.

-   Porte del firewall

    Quando un firewall viene usato in una rete ,ad esempio il firewall di connessione Internet IPv6, è necessario aprire porte specifiche per consentire il funzionamento dell'infrastruttura peer. Le porte seguenti devono essere aperte:

    Porta TCP 3587 per l'infrastruttura di raggruppamento peer.

    Porta UDP 3540 per l'infrastruttura peer graphing.

    > [!Note]  
    > Le applicazioni che usano Peer Graphing Infrastructure su TCP scelgono la propria porta TCP quando chiamano [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten).

     

-   Opzione socket

    Quando si tenta di connettersi direttamente ad altri nodi peer IPv6 (senza usare l'infrastruttura peer), assicurarsi che l'opzione socket IPV6 PROTECTION LEVEL sia impostata \_ \_ su PROTECTION LEVEL **\_ \_ UNRESTRICTED**.

-   Larghezza di banda

    Quando si usa PNRP, un'applicazione può pubblicare uno o più nomi [peer](peer-names.md) che possono essere risolti. Per ogni nome peer registrato con PNRP, è presente un aumento della larghezza di banda di rete che PNRP usa per pubblicare il nome peer e mantenerlo disponibile per la risoluzione da parte di altri nodi.

    Per evitare di usare una larghezza di banda troppo elevata, le applicazioni devono evitare di registrare un numero elevato di nomi peer in un computer. Ad esempio, un'applicazione che pubblica immagini non deve creare un nome peer per ogni immagine, ma deve creare un nome peer per il servizio che pubblica immagini e usare un protocollo diverso per i client per eseguire query sul servizio per immagini specifiche.

-   Registrazione del nome peer

    Alcune applicazioni potrebbero essere necessarie per registrare lo stesso [nome peer](peer-names.md) in più computer. In genere, ciò si verifica se un nome peer è associato a una persona che usa più di un computer. Un metodo che è possibile usare per registrare lo stesso nome peer in più computer è creare un gruppo peer per la persona e connettersi a tale gruppo da tutti i computer. Un altro metodo è creare un'identità peer e un nome peer in un computer, esportare l'identità peer da tale computer e importarla in altri computer. In questo modo è possibile creare lo stesso nome peer sicuro in tutti i computer che hanno importato l'identità peer.

 

 



