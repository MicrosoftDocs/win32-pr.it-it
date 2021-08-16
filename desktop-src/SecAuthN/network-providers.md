---
description: Un provider di rete è una DLL che supporta un protocollo di rete specifico.
ms.assetid: ebd47c1b-f427-4fa1-a2ec-1e73be297bef
title: Provider di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5443ec7366b0f7ad74037f868e1ca4a93dbd913d0c13fda46c7b9fdabd0e0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786599"
---
# <a name="network-providers"></a>Provider di rete

Un provider di rete è una DLL che supporta un protocollo di rete specifico. Implementa anche [l'API del provider di rete](network-provider-api.md). Ciò consente di interagire con il Windows sistema operativo per ricevere richieste di rete standard, ad esempio richieste di connessione o disconnessione. Per gestire queste richieste, il provider di rete chiama quindi l'API specifica della rete appropriata al protocollo di rete supportato dal provider di rete. In altre parole, il provider di rete esegue il wrapping della funzionalità specifica della rete in una DLL, che espone un'interfaccia standard per Windows.

Usando i provider di Windows, è possibile supportare molti tipi diversi di protocolli di rete senza dover conoscere i dettagli specifici della rete di ogni rete. Questo è essenziale perché vengono sempre sviluppati nuovi protocolli di rete. Con i provider di rete, il supporto di un nuovo protocollo richiede semplicemente la creazione e l'installazione di un nuovo provider di rete.

Per informazioni sulle funzioni e sulle strutture dei provider di rete, vedere gli argomenti seguenti:

-   [Funzioni del provider di rete](authentication-functions.md)
-   [Strutture del provider di rete](authentication-structures.md)

 

 



