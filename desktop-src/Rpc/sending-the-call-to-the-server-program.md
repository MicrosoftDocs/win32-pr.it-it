---
title: Invio della chiamata al programma server
description: Dopo che il tempo di esecuzione RPC sul lato client è stato connesso all'endpoint server, esegue il marshalling degli argomenti e li invia al server.
ms.assetid: 170316b1-4185-45b1-845e-ca6f0285b7f9
keywords:
- Chiamata di procedura remota RPC , attività, invio della chiamata al server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a02d4fc1d69ba45cc6de3d43fba62724de1277471992790e3098225f579d305
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017911"
---
# <a name="sending-the-call-to-the-server-program"></a>Invio della chiamata al programma server

Dopo che il tempo di esecuzione RPC sul lato client è stato connesso all'endpoint server, esegue il marshalling degli argomenti e li invia al server. La fase di esecuzione RPC del server fornisce gli argomenti di cui è stato eseguito il marshalling per lo stub che ne esegue l'unmarshalling e quindi li passa alle routine del server. Quando le routine del server restituiscono , lo stub preleva i parametri out e in,out e il valore restituito, li esegue il marshalling e invia i dati di cui è stato eseguito il marshalling al tempo di esecuzione \[ \] RPC del \[ \] server. Il tempo di esecuzione RPC invia i dati al client, in cui il tempo di esecuzione RPC client li trasmette al lato client stub che li annulla il marshalling e li restituisce al chiamante.

 

 




