---
title: Sviluppo di un server RPC a prestazioni elevate
description: Le informazioni contenute in questa sezione si applicano alle sequenze remote del protocollo ncacn \_ IP \_ TCP, ncacn \_ http, ncacn \_ np e a Windows 2000 e Windows XP.
ms.assetid: 7b4239af-951b-4d1b-8ac3-224279f6929e
keywords:
- RPC (Remote Procedure Call), procedure consigliate, sviluppo di un server a prestazioni elevate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a18319c1f4ade80ae026b68c8f5540030b992b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473990"
---
# <a name="developing-a-high-performance-rpc-server"></a>Sviluppo di un server RPC a prestazioni elevate

Le informazioni contenute in questa sezione si applicano alle sequenze remote del protocollo: [**ncacn \_ IP \_ TCP**](/windows/desktop/Midl/ncacn-ip-tcp), [**ncacn \_ http**](/windows/desktop/Midl/ncacn-http), [**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np)e a Windows 2000 e Windows XP.

In questa sezione vengono illustrati tre aspetti principali delle prestazioni del server RPC:

-   [Latenza di rete e velocità effettiva](network-latency-and-throughput.md)
-   [Scalabilità](scalability.md)
-   [Suggerimenti sulle prestazioni RPC varie](miscellaneous-rpc-performance-tips.md)

La lunghezza del percorso del codice è un'altra considerazione primaria per le prestazioni RPC. La lunghezza del percorso del codice è in genere ben riconosciuta e, poiché la letteratura e gli strumenti sono ampiamente disponibili in questo argomento, questo articolo non risolve il problema.

Una regola importante e stabilita per le prestazioni generali da ricordare considerando le prestazioni RPC è la seguente: individuare il collo di bottiglia nel sistema e risolverlo. Il collo di bottiglia del controllo potrebbe non essere la programmazione RPC e, in tal caso, l'ottimizzazione delle prestazioni in RPC non comporterà un miglioramento delle prestazioni fino a quando non verrà risolto il collo di bottiglia. Ad esempio, un sistema afflitto dalla contesa di risorse non necessita di un uso più efficiente della rete.

Se il sistema viene distribuito in diversi ambienti, è consigliabile assicurarsi che tutti gli aspetti siano ben ottimizzati, in quanto ambienti diversi possono produrre colli di bottiglia delle prestazioni diversi.

 

 