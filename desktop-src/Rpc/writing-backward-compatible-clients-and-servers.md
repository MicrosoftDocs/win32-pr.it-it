---
title: Scrittura di client e server compatibili con le versioni precedenti
description: In teoria, lo schema di controllo delle versioni di RPC consente di impedire la comunicazione non consentita tra server e client modificati e le relative controparti distribuite.
ms.assetid: 0c7d6716-e4ed-447e-bf64-906d55bec907
keywords:
- RPC, procedure consigliate, compatibilità con le versioni precedenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac5ae011c8a9c346bc0f89fb73e26265d487721
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116781"
---
# <a name="writing-backward-compatible-clients-and-servers"></a>Scrittura di client e server compatibili con le versioni precedenti

In teoria, lo schema di controllo delle versioni di RPC consente di impedire la comunicazione non consentita tra server e client modificati e le relative controparti distribuite. In pratica, tuttavia, gli sviluppatori devono spesso introdurre modifiche alle interfacce esistenti senza modificare la versione, perché i client e i server precedenti devono essere in grado di comunicare con quelli nuovi. Si tratta di un problema di dimensioni maggiori per RPC standard rispetto a COM; l'esecuzione di query è un metodo naturale per la ricerca di interfacce supportate in COM, mentre nella gestione delle eccezioni RPC deve essere utilizzato per la copertura equivalente.

In questa sezione vengono descritte le procedure di programmazione RPC migliori per risolvere queste situazioni. Questa sezione è divisa negli argomenti seguenti:

-   [Teoria del controllo delle versioni per RPC e COM](the-versioning-theory-for-rpc-and-com.md)
-   [Modifica delle interfacce in modo compatibile con le versioni precedenti](changing-interfaces-in-a-backward-compatible-manner.md)
-   [Esempi di modifiche incompatibili](examples-of-incompatible-changes.md)

 

 




