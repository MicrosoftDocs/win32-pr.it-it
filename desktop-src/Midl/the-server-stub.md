---
title: Stub del server
description: Lo stub del server fornisce punti di ingresso surrogati nel server per ognuna delle operazioni definite nel file IDL di input.
ms.assetid: e3263543-e78b-40a8-aafa-4315850112a8
keywords:
- MIDL del compilatore MIDL, MIDL e MIDL RPC, interfacce, stub server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddfc940ebbd90e4e028ce96dc3b5c47eb15179d41cfbd064cd235e87192822f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119559901"
---
# <a name="the-server-stub"></a>Stub del server

Lo stub del server fornisce punti di ingresso surrogati nel server per ognuna delle operazioni definite nel file IDL di input.

Quando una routine stub del server viene richiamata dalla libreria di runtime RPC, esegue le funzioni seguenti:

-   Annulla ilmarshaling degli argomenti di input (decomprime gli argomenti dai formati trasmessi).
-   Chiama l'implementazione effettiva della procedura nel server.
-   Esegue il marshalling degli argomenti di output (esegue il pacchetto degli argomenti nei formati trasmessi).

Le opzioni [**/server**](-server.md), [**/sstub**](-sstub.md)e [**/out**](-out.md) del compilatore MIDL influiscono sul file stub del server.

 

 




