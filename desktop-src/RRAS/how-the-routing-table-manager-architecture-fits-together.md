---
title: Interazione tra l'architettura di gestione tabelle di routing
description: Nella figura seguente viene illustrata la relazione tra i diversi componenti di un router.
ms.assetid: 862566ce-47c4-424a-84c2-99f4c92efcc0
keywords:
- RTM, architettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc36c339ac89f01d5ba14c00857b3ced9c29414c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332751"
---
# <a name="how-the-routing-table-manager-architecture-fits-together"></a>Interazione tra l'architettura di gestione tabelle di routing

Nella figura seguente viene illustrata la relazione tra i diversi componenti di un router.

![relazione tra componenti router](images/rtsrvarch.png)

Quando il router viene bootstrap, viene avviato il servizio Gestione router, oltre a uno o più protocolli di routing. I protocolli di routing sono associati alle varie interfacce sul router. Gestione router avvia inoltre gestione tabelle di routing.

Nella figura seguente viene illustrata la relazione tra i client di e i diversi componenti di gestione tabelle di routing.

![relazione tra client e componenti di gestione tabelle di routing](images/rtmentrel.png)

Gestione router avvia una o più istanze di gestione tabelle di routing. Quando vengono avviate più istanze di gestione tabelle di routing, il router è stato configurato per fungere da uno o più router virtuali. Ogni istanza di gestione tabelle di routing è proprietaria di una o più interfacce. ogni interfaccia può essere di proprietà di un'istanza di gestione tabelle di routing.

Ogni istanza di gestione tabelle di routing è indipendente dagli altri. Nessuna informazione viene scambiata tra le istanze.

Ogni istanza di gestione tabelle di routing contiene una o più tabelle di routing. Ogni tabella di routing è associata a una famiglia di indirizzi.

Ogni tabella di routing contiene una o più viste. In questo esempio, la tabella di routing viene visualizzata con una visualizzazione unicast e multicast. Ogni visualizzazione è un subset della tabella di routing.

Nella figura seguente viene illustrata la relazione tra i client di e più istanze di gestione tabelle di routing, le tabelle di routing e le viste.

![client di relazioni, gestione tabelle di routing, tabelle di routing, viste](images/multrtabrel.png)

Un'istanza del client può essere registrata più volte con un'istanza di gestione tabelle di routing, una volta per ogni famiglia di indirizzi. Un client può eseguire la registrazione a ogni istanza di gestione tabelle di routing.

Nella figura seguente viene illustrata la correlazione tra le voci della tabella di routing. Per ulteriori informazioni sulle voci della tabella di routing, vedere [voci della tabella di routing](routing-table-entries.md).

![relazione tra le voci della tabella di routing](images/nexthop.png)

La tabella di routing contiene destinazioni. Ogni destinazione è correlata a una o più route. Ogni route ha zero, uno o più puntatori agli hop successivi associati alla route. Ogni puntatore si riferisce all'hop successivo effettivo nell'elenco di hop successivi. Ogni client che esegue la registrazione con gestione tabelle di routing crea un elenco di hop successivi di proprietà del client.

Le route possono contenere solo puntatori all'elenco di hop successivo associato al client proprietario della route.

 

 




