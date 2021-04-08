---
title: Selezione di una sequenza di protocollo
description: Una sequenza di protocollo è il linguaggio usato da un sistema operativo di rete per comunicare in rete con altri computer.
ms.assetid: 9c788b9b-82c5-4a4b-86c6-e9a9df699da3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac6b79f5f7a0829eea88eba77f2d022e8de2ca8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045166"
---
# <a name="selecting-a-protocol-sequence"></a>Selezione di una sequenza di protocollo

Una sequenza di protocollo è il linguaggio usato da un sistema operativo di rete per comunicare in rete con altri computer. In termini più specifici, le applicazioni RPC devono specificare una stringa che rappresenta una combinazione di un protocollo RPC, un protocollo di trasporto e un protocollo di rete.

Microsoft RPC supporta tre protocolli RPC:

-   Protocollo NCACN (Network Computing Architecture)
-   NCADG (Network Computing Architecture datagramma Protocol)
-   Chiamata di procedura remota locale per l'architettura di Network Computing (NCALRPC)

Le applicazioni RPC possono utilizzare il protocollo NCALRPC per richiamare le procedure offerte dai programmi server in esecuzione nello stesso computer in cui viene eseguito il programma client. Questo è, di gran lunga, il metodo più efficiente per chiamare la funzionalità in un processo diverso nello stesso computer.

I protocolli di trasporto e di rete utilizzati dall'applicazione dipendono dai protocolli supportati dalla rete. Molte reti attualmente, tra cui Internet, supportano TCP/IP. Altri protocolli di trasporto e di rete comuni sono IPX/SPX, NetBIOS e AppleTalk DSP. Microsoft RPC supporta questi e altri protocolli di trasporto e di rete. Per un elenco completo, vedere [costanti di sequenza del protocollo](protocol-sequence-constants.md).

Quando l'applicazione usa handle di associazione automatici, non è necessario specificare la sequenza di protocolli. Se usa handle impliciti o espliciti, deve ottenere o specificare la sequenza di protocolli. Ogni sistema distribuito deve esaminare l'ambiente in cui verrà distribuito per determinare la sequenza di protocollo più adatta a tale ambiente.

Non tutte le sequenze di protocollo hanno funzionalità equivalenti. Gli sviluppatori devono verificare che la sequenza di protocollo scelta supporti le funzionalità necessarie. In generale, è consigliabile usare **ncalrpc** per le comunicazioni locali e **ncacn \_ IP \_ TCP** o **ncacn \_ http** per le comunicazioni remote. funzionano in tutti gli ambienti, presentano prestazioni ottimali e supportano tutte le funzionalità necessarie per le procedure consigliate.

I client possono inoltre specificare le informazioni sulla sequenza di protocollo ottenute dal Active Directory, dal registro di sistema, dalle variabili di ambiente create e inizializzate dal programma di installazione, dai file di configurazione specifici dell'applicazione o dalle stringhe letterali nel codice sorgente del programma.

Quando il programma client dispone di una stringa di sequenza di protocollo valida, può passare le informazioni alle funzioni [**errore in RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) e [**errore in RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) per creare l'handle di associazione.

 

 




