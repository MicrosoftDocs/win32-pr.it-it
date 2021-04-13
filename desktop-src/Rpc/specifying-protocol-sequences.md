---
title: Specifica di sequenze di protocollo
description: Le applicazioni server devono selezionare una o più sequenze di protocollo da utilizzare durante la comunicazione con il client in rete. La scelta delle sequenze di protocollo dipende dalla rete. Vedere interpretazione delle informazioni di binding e selezione di una sequenza di protocollo.
ms.assetid: bde26a86-dc4f-4d18-ba51-c6536c62bb75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a700299e3d2bd98fa5fb0aaebea25e907d85afb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338486"
---
# <a name="specifying-protocol-sequences"></a>Specifica di sequenze di protocollo

Le applicazioni server devono selezionare una o più sequenze di protocollo da utilizzare durante la comunicazione con il client in rete. La scelta delle sequenze di protocollo dipende dalla rete. Vedere [interpretazione delle informazioni di binding](interpreting-binding-information.md) e [selezione di una sequenza di protocollo](selecting-a-protocol-sequence.md).

Il programma server può consentire ai client di connettersi utilizzando qualsiasi sequenza di protocollo supportata dalla rete. A tale scopo, richiamare [**RpcServerUseAllProtSeqs**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqs) e passare RPC \_ C \_ PROTSEQ \_ Max \_ Rich \_ default come primo parametro. Tuttavia, questo non è l'approccio consigliato. Piuttosto, l'uso di **ncalrpc** per le chiamate locali e **ncacn \_ \_ TCP** o **ncacn \_ http** per le chiamate remote è in genere sufficiente. Le reti eterogeneo non sono comuni e praticamente tutte le reti supportano TCP/IP.

Se si desidera che il client limiti l'allocazione delle porte per gli endpoint dinamici a un intervallo di porte specifico, chiamare invece [**RpcServerUseAllProtseqsEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsex) . Questa funzione è specifica di Microsoft RPC ed è estremamente utile per le chiamate a procedure remote che passano attraverso un firewall. Usa un parametro aggiuntivo per passare i flag di controllo dell'allocazione delle porte alla funzione. Vedere [configurazione del registro di sistema per le allocazioni delle porte e l'associazione selettiva](configuring-the-windows-xp-2000-nt-registry-for-port-allocations-and-selective-binding.md).

È possibile specificare le sequenze di protocollo e le informazioni sugli endpoint nel file MIDL quando si sviluppano le interfacce del server. In tal caso, il server deve utilizzare [**RpcServerUseAllProtseqsIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsif) per registrare tutte le sequenze di protocollo e le informazioni sull'endpoint associate fornite nel file IDL. Inoltre, esiste una funzione [**RpcServerUseAllProtseqsIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseallprotseqsifex) corrispondente che consente anche al server di passare i flag di allocazione delle porte-controllo.

Se si desidera configurare i programmi client e server per comunicare con una sequenza di protocollo specificata, l'applicazione server deve chiamare [**RpcServerUseProtseq**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseq). Per un elenco completo delle sequenze del protocollo RPC Microsoft, vedere [costanti di sequenza del protocollo](protocol-sequence-constants.md).

Microsoft RPC fornisce inoltre [**RpcServerUseProtseqEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqex) per consentire alle applicazioni di selezionare sequenze di protocolli specifiche e di controllare l'allocazione dinamica delle porte.

Oltre ai protocolli orientati alla connessione, Microsoft RPC supporta anche i protocolli di datagramma (senza connessione). Sono consigliati i protocolli orientati alla connessione. i protocolli di datagramma hanno set di funzionalità diversi rispetto ai protocolli orientati alla connessione e devono essere usati solo se uno sviluppatore di sistemi distribuiti richiede una funzionalità disponibile solo nei protocolli di datagramma. Di seguito sono riportate alcune delle funzionalità disponibili quando si usano protocolli di datagramma:

-   I datagrammi supportano i protocolli di trasporto senza connessione UDP e IPX.
-   Poiché non è necessario stabilire e mantenere una connessione, il protocollo RPC del datagramma richiede meno overhead delle risorse.
-   Datagrammi consente un binding più rapido.
-   Come per la RPC orientata alla connessione, le chiamate RPC di datagramma sono per impostazione predefinita *nonidempotent*. Ciò significa che la chiamata non viene eseguita più di una volta. Tuttavia, una funzione può essere contrassegnata come idempotente nel file IDL indicando a RPC che è innocuo eseguire la funzione più volte in risposta a una singola richiesta client. In questo modo, il tempo di esecuzione verrà mantenuto nel server. Si noti che una chiamata idempotente verrebbe eseguita di nuovo solo in rare circostanze in una rete instabile.
-   Datagramma RPC supporta l'attributo [broadcast](/windows/desktop/Midl/broadcast) IDL. Broadcast consente a un client di emettere messaggi su più server contemporaneamente. Ciò consente al client di individuare uno dei diversi server disponibili nella rete o di controllare contemporaneamente più server. Si noti che il datagramma broadcast è valido solo all'interno del collegamento locale e in genere non attraversa i router. Le chiamate broadcast sono implicitamente idempotente. Se la chiamata contiene \[ parametri **out** \] , viene restituita solo la prima risposta al server. Una volta che un server risponde, tutte le RPC future sull'handle di associazione verranno inviate solo a tale server, incluse le chiamate con l'attributo broadcast. Per inviare un'altra trasmissione, creare un nuovo handle di binding o chiamare [**RpcBindingReset**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingreset) sull'handle esistente.
-   Datagramma RPC supporta [l'attributo](/windows/desktop/Midl/maybe) IDL. Ciò consente al client di inviare una chiamata al server senza attendere una risposta o una conferma. La chiamata non può contenere \[  \] parametri out. Le chiamate che usano le chiamate **\[ probabilmente \]** sono implicitamente idempotente.

 

 