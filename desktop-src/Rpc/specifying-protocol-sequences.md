---
title: Specifica delle sequenze di protocollo
description: Le applicazioni server devono selezionare una o più sequenze di protocollo da usare per la comunicazione con il client in rete. La scelta delle sequenze di protocollo dipende dalla rete. Vedere Interpretazione delle informazioni di associazione e Selezione di una sequenza di protocollo.
ms.assetid: bde26a86-dc4f-4d18-ba51-c6536c62bb75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f43b8dc7b21fc2a6bebe98010b80dbf369ac96bb185cc75afa3b0a4f1acbba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925151"
---
# <a name="specifying-protocol-sequences"></a>Specifica delle sequenze di protocollo

Le applicazioni server devono selezionare una o più sequenze di protocollo da usare per la comunicazione con il client in rete. La scelta delle sequenze di protocollo dipende dalla rete. Vedere [Interpretazione delle informazioni di associazione](interpreting-binding-information.md) e Selezione di una sequenza di [protocollo](selecting-a-protocol-sequence.md).

Il programma server può consentire ai client di connettersi usando qualsiasi sequenza di protocollo supportato dalla rete. A tale scopo, richiamare [**RpcServerUseAllProtseqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs) e passare RPC \_ C \_ PROTSEQ \_ MAX \_ REQS \_ DEFAULT come primo parametro. Tuttavia, questo non è l'approccio consigliato. È invece sufficiente **usare ncalrpc per** le chiamate locali e **ncacn \_ ip \_ tcp** o **ncacn \_ http** per le chiamate remote. Le reti eterogenee non sono comuni e praticamente tutte le reti supportano TCP/IP.

Se si vuole che il client limiti l'allocazione delle porte per gli endpoint dinamici a un intervallo di porte specifico, chiamare [**rpcServerUseAllProtseqsEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex) Questa funzione è specifica di RPC Microsoft ed è estremamente utile per le chiamate di procedura remota che passano attraverso un firewall. Usa un parametro aggiuntivo per passare alla funzione i flag di controllo di allocazione delle porte. Vedere [Configurazione del Registro di sistema per le allocazioni di porte e l'associazione selettiva.](configuring-the-windows-xp-2000-nt-registry-for-port-allocations-and-selective-binding.md)

È possibile specificare sequenze di protocollo e informazioni sugli endpoint nel file MIDL quando si sviluppano le interfacce del server. In caso contrario, il server deve usare [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsif) per registrare tutte le sequenze di protocollo e le informazioni sull'endpoint associate fornite nel file IDL. Esiste anche una funzione [**RpcServerUseAllProtseqsIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex) corrispondente che consente al server di passare i flag di allocazione delle porte e di controllo.

Se si desidera configurare i programmi client e server per comunicare con una sequenza di protocollo specificata, l'applicazione server deve chiamare [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq). Per un elenco completo delle sequenze del protocollo RPC Microsoft, vedere [Costanti della sequenza di protocollo](protocol-sequence-constants.md).

Microsoft RPC fornisce anche [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) per consentire alle applicazioni di selezionare sequenze di protocollo specifiche e controllare l'allocazione dinamica delle porte.

Oltre ai protocolli orientati alla connessione, Microsoft RPC supporta anche protocolli di datagrammi (senza connessione). È consigliabile utilizzare protocolli orientati alla connessione. I protocolli datagram hanno set di funzionalità diversi rispetto ai protocolli orientati alla connessione e devono essere usati solo se uno sviluppatore di sistemi distribuiti richiede una funzionalità disponibile solo nei protocolli di datagramma. Alcune delle funzionalità disponibili quando si usano i protocolli di datagramma sono:

-   I datagrammi supportano i protocolli di trasporto senza connessione UDP e IPX.
-   Poiché non è necessario stabilire e mantenere una connessione, il protocollo RPC del datagramma richiede meno sovraccarico delle risorse.
-   I datagrammi consentono un'associazione più veloce.
-   Come per rpc orientato alla connessione, le chiamate RPC del datagramma sono *per impostazione predefinita nonidempotent.* Ciò significa che la chiamata non deve essere eseguita più di una volta. Tuttavia, una funzione può essere contrassegnata come idempotente nel file IDL indicando a RPC che è innocuo eseguire la funzione più di una volta in risposta a una singola richiesta client. Ciò consente al tempo di esecuzione di mantenere meno stato nel server. Si noti che una chiamata idempotente verrà rieseguiti solo in rare circostanze in una rete instabile.
-   Il datagramma RPC supporta [l'attributo](/windows/desktop/Midl/broadcast) IDL broadcast. La trasmissione consente a un client di inviare messaggi a più server contemporaneamente. Ciò consente al client di individuare uno dei diversi server disponibili nella rete o di controllare più server contemporaneamente. Si noti che la trasmissione del datagramma è valida solo all'interno del collegamento locale e in genere non attraversa i router. Le chiamate broadcast sono implicitamente idempotenti. Se la chiamata contiene \[ **parametri out,** \] viene restituita solo la prima risposta del server. Quando un server risponde, tutte le RPC future su tale handle di associazione verranno inviate solo a tale server, incluse le chiamate con l'attributo broadcast. Per inviare un'altra trasmissione, creare un nuovo handle di associazione o chiamare [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) sull'handle esistente.
-   Il datagramma RPC supporta [l'attributo](/windows/desktop/Midl/maybe) IDL. In questo modo il client può inviare una chiamata al server senza attendere una risposta o una conferma. La chiamata non può contenere \[ **parametri out.** \] Le chiamate che **\[ usano le chiamate maybe \]** sono implicitamente idempotenti.

 

 