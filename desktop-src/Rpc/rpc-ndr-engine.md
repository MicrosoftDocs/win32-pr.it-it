---
title: Motore di recapito RPC (RPC)
description: Il motore di rappresentazione dei dati di rete (NDR) RPC (Remote Procedure Call) è il motore di marshalling dei componenti RPC e DCOM.
ms.assetid: E452AA27-053D-4032-868B-CF2D5C0D4BE0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bf7ba92a74d2d7dc8c394c561f65337db13af99
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047720"
---
# <a name="rpc-ndr-engine-rpc"></a>Motore di recapito RPC (RPC)

Il motore di rappresentazione dei dati di rete (NDR) RPC (Remote Procedure Call) è il motore di marshalling dei componenti RPC e DCOM. Il motore NDR gestisce tutti i problemi relativi agli stub di una chiamata remota. Come processo, il marshalling del rapporto di recapito è determinato dal codice C da stub generati da MIDL, da un generatore di tipi JIT MIDL o da stub generati da altri strumenti o scritti manualmente. Il motore di NDR, a sua volta, determina il tempo di esecuzione sottostante (DCOM o RPC) che comunica con trasporti specifici.

Sebbene gli stub siano codice C generati da MIDL, è consigliabile che le applicazioni trattino gli stub come opachi ed è fortemente sconsigliato modificare qualsiasi elemento all'interno dello stub. Il comportamento non è definito se le routine NDR sono denominate fuori contesto.

Il motore di mancato recapito RPC viene descritto più dettagliatamente negli argomenti seguenti:

-   [Sintassi transfer e NDR64](transfer-syntax-and-ndr64.md)
-   [Stringhe di formato di recapito RPC](rpc-ndr-format-strings.md)
-   [Riferimento all'interfaccia RPC NDR](rpc-ndr-interface-reference.md)

 

 




