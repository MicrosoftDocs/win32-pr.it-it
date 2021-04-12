---
title: Invio della chiamata al programma server
description: Una volta che il tempo di esecuzione RPC lato client si è connesso all'endpoint server, il marshalling degli argomenti e li invia al server.
ms.assetid: 170316b1-4185-45b1-845e-ca6f0285b7f9
keywords:
- RPC (Remote Procedure Call), attività, invio della chiamata al server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba3a2dac77ec13fb00374faef456a52f0f24e99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331783"
---
# <a name="sending-the-call-to-the-server-program"></a>Invio della chiamata al programma server

Una volta che il tempo di esecuzione RPC lato client si è connesso all'endpoint server, il marshalling degli argomenti e li invia al server. Il tempo di esecuzione RPC del server assegna gli argomenti con marshalling allo stub che li rimuove e li passa alle routine del server. Quando le routine del server restituiscono, lo stub preleva i \[ parametri out \] e \[ in, out \] e il valore restituito, li Marshall e invia i dati di marshalling al runtime RPC del server. Il tempo di esecuzione RPC invia i dati al client, in cui il tempo di esecuzione RPC del client li consegna allo stub lato client che li rimuove e li restituisce al chiamante.

 

 




