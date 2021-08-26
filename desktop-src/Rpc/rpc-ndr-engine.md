---
title: Motore NDR RPC (RPC)
description: Il motore di rappresentazione dei dati di rete RPC (Remote Procedure Call) è il motore di marshalling dei componenti RPC e DCOM.
ms.assetid: E452AA27-053D-4032-868B-CF2D5C0D4BE0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0dd01ae40562528ac89c8b9dcfb0b9009ead5ca1a92b2cde90c3274d574fc1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018421"
---
# <a name="rpc-ndr-engine-rpc"></a>Motore NDR RPC (RPC)

Il motore di rappresentazione dei dati di rete RPC (Remote Procedure Call) è il motore di marshalling dei componenti RPC e DCOM. Il motore NDR gestisce tutti i problemi relativi agli stub di una chiamata remota. Come processo, il marshalling NDR è guidato dal codice C da stub generati da MIDL, da un generatore di tipo JIT MIDL o da stub generati da altri strumenti o scritti manualmente. A sua volta, il motore NDR determina il runtime sottostante (DCOM o RPC) che comunica con trasporti specifici.

Anche se gli stub sono codice C generati da MIDL, si consiglia alle applicazioni di considerare gli stub come opachi e fortemente sconsigliati di modificare qualsiasi elemento all'interno dello stub. Il comportamento non è definito se queste routine NDR vengono chiamate fuori contesto.

Il motore NDR RPC è descritto in modo più dettagliato negli argomenti seguenti:

-   [Sintassi di trasferimento e NDR64](transfer-syntax-and-ndr64.md)
-   [Stringhe di formato NDR RPC](rpc-ndr-format-strings.md)
-   [Informazioni di riferimento per l'interfaccia NDR RPC](rpc-ndr-interface-reference.md)

 

 




