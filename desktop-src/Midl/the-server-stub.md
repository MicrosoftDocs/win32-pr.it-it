---
title: Stub del server
description: Lo stub del server fornisce punti di ingresso surrogati sul server per ciascuna delle operazioni definite nel file IDL di input.
ms.assetid: e3263543-e78b-40a8-aafa-4315850112a8
keywords:
- MIDL Compiler MIDL, MIDL e RPC MIDL, interfacce, stub server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b351c53fa9e1d1716e1240ddf4febdccdadda46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045148"
---
# <a name="the-server-stub"></a>Stub del server

Lo stub del server fornisce punti di ingresso surrogati sul server per ciascuna delle operazioni definite nel file IDL di input.

Quando una routine stub del server viene richiamata dalla libreria di runtime RPC, esegue le funzioni seguenti:

-   Esegue l'unmarshalling degli argomenti di input (decomprime gli argomenti dai formati trasmessi).
-   Chiama l'implementazione effettiva della stored procedure nel server.
-   Esegue il marshalling degli argomenti di output (crea il pacchetto degli argomenti nei form trasmessi).

Il compilatore MIDL commuta [**/Server**](-server.md), [**/sstub**](-sstub.md)e [**/out**](-out.md) influisce sul file stub del server.

 

 




