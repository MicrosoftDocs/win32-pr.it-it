---
title: Connessione del client e del server
description: Per comunicare, i programmi client e server devono stabilire una sessione di comunicazione attraverso la rete o le reti che li collegano.
ms.assetid: 1164252a-7615-4958-9d2f-cf35c0db513a
keywords:
- RPC (Remote Procedure Call), attività, connessione di client e server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98a22ea7a9a6dd30f2b9495b6d2ee868aac217f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471390"
---
# <a name="connecting-the-client-and-the-server"></a>Connessione del client e del server

Per comunicare, i programmi client e server devono stabilire una sessione di comunicazione attraverso la rete o le reti che li collegano. Una volta stabilita la connessione, il client può chiamare le procedure remote nel programma server come se fossero locali per il programma client.

In questa sezione viene fornita una panoramica concettuale su come stabilire una connessione tra client e server per chiamate a procedure remote. Non fornisce una descrizione approfondita di questo argomento. Tutti i concetti illustrati in questa sezione sono descritti in dettaglio nei capitoli successivi e nella sezione riferimento alle funzioni RPC.

La discussione presentata in questa sezione è divisa negli argomenti seguenti:

-   [Terminologia di associazione RPC essenziale](essential-rpc-binding-terminology.md)
-   [Preparazione del server per una connessione](how-the-server-prepares-for-a-connection.md)
-   [Come il client stabilisce una connessione](how-the-client-establishes-a-connection.md)

Si noti che la discussione presuppone handle di binding espliciti. Tuttavia, se l'applicazione usa altri tipi di handle di associazione, potrebbe essere necessario modificare i passaggi presentati in questa sezione. Per ulteriori informazioni, vedere [Binding e handle](binding-and-handles.md).

 

 




