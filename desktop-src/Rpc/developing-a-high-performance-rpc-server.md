---
title: Sviluppo di un server RPC a prestazioni elevate
description: Le informazioni contenute in questa sezione si applicano alle sequenze di protocollo remoto ncacn \_ ip \_ tcp, ncacn \_ http, ncacn np e \_ a Windows 2000 e Windows XP.
ms.assetid: 7b4239af-951b-4d1b-8ac3-224279f6929e
keywords:
- RPC Remote Procedure Call , procedure consigliate, sviluppo di un server ad alte prestazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 841c52587410b10ae17f2ebd858863327aaf5ab1def92600259c8e49edc87946
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021770"
---
# <a name="developing-a-high-performance-rpc-server"></a>Sviluppo di un server RPC a prestazioni elevate

Le informazioni contenute in questa sezione si applicano alle sequenze di protocollo remoto: [**ncacn \_ ip \_ tcp**](/windows/desktop/Midl/ncacn-ip-tcp), [**ncacn \_ http**](/windows/desktop/Midl/ncacn-http), [**ncacn \_ np**](/windows/desktop/Midl/ncacn-np)e a Windows 2000 e Windows XP.

Questa sezione tratta tre aspetti principali delle prestazioni del server RPC:

-   [Latenza di rete e velocità effettiva](network-latency-and-throughput.md)
-   [Scalabilità](scalability.md)
-   [Prestazioni RPC varie Suggerimenti](miscellaneous-rpc-performance-tips.md)

La lunghezza del percorso del codice è un'altra considerazione primaria sulle prestazioni per RPC. La lunghezza del percorso del codice è generalmente ben compresa e, poiché la documentazione e gli strumenti sono ampiamente disponibili in tale argomento, questo articolo non tratta questo argomento.

Una regola di prestazioni generale importante e consolidata da ricordare considerando le prestazioni RPC è la seguente: individuare il collo di bottiglia nel sistema e lavorare per risolverlo. Il collo di bottiglia del controllo potrebbe non essere la programmazione RPC e, in tal caso, l'ottimizzazione delle prestazioni in RPC non comporterà prestazioni migliorate fino a quando tale collo di bottiglia non viene corretto. Ad esempio, non è necessario che un sistema danneggiato da una contentione di risorse usi la rete in modo più efficiente.

Se il sistema viene distribuito in diversi ambienti, è buona idea assicurarsi che tutti gli aspetti del sistema siano ottimizzati, perché ambienti diversi possono produrre colli di bottiglia delle prestazioni diversi.

 

 