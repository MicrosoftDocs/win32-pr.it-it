---
title: Connessione del client e del server
description: Per comunicare, i programmi client e server devono stabilire una sessione di comunicazione attraverso la rete o le reti che li connettono.
ms.assetid: 1164252a-7615-4958-9d2f-cf35c0db513a
keywords:
- Chiamata di procedura remota RPC, attività, connessione di client e server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f477802ffb4b72f33ce951bf811b1cb9b770a8272f646507dfaa450934569f32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931228"
---
# <a name="connecting-the-client-and-the-server"></a>Connessione del client e del server

Per comunicare, i programmi client e server devono stabilire una sessione di comunicazione attraverso la rete o le reti che li connettono. Dopo aver stabilito la connessione, il client può chiamare le procedure remote nel programma server come se fossero locali al programma client.

In questa sezione viene fornita una panoramica concettuale di come stabilire una connessione tra client e server per le chiamate di procedura remota. Non fornisce una descrizione approfondita di questo argomento. Tutti i concetti di questa sezione sono presentati in dettaglio nei capitoli successivi e nella sezione Informazioni di riferimento per le funzioni RPC.

La discussione presentata in questa sezione è suddivisa negli argomenti seguenti:

-   [Terminologia essenziale per l'associazione RPC](essential-rpc-binding-terminology.md)
-   [Preparazione del server per una connessione](how-the-server-prepares-for-a-connection.md)
-   [Modalità di connessione stabilita dal client](how-the-client-establishes-a-connection.md)

Si noti che la discussione presuppone handle di associazione espliciti. Tuttavia, se l'applicazione usa altri tipi di handle di associazione, potrebbe essere necessario modificare i passaggi presentati in questa sezione. Per altre informazioni, vedere [Associazione e handle](binding-and-handles.md).

 

 




