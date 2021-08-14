---
title: Come si inserisce l'architettura di Gestione tabelle di routing
description: Nella figura seguente viene illustrata la relazione tra i diversi componenti di un router.
ms.assetid: 862566ce-47c4-424a-84c2-99f4c92efcc0
keywords:
- RTM, architettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1637eed71a89a6de4fa7dad6a4fea4a5918366f69ee05a490824699605a117a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791383"
---
# <a name="how-the-routing-table-manager-architecture-fits-together"></a>Come si inserisce l'architettura di Gestione tabelle di routing

Nella figura seguente viene illustrata la relazione tra i diversi componenti di un router.

![relazione tra i componenti del router](images/rtsrvarch.png)

Quando il router viene avviato, viene avviato il servizio gestione router, nonché uno o più protocolli di routing. I protocolli di routing sono associati alle varie interfacce del router. La gestione router avvia anche la gestione tabelle di routing.

Nella figura seguente viene illustrata la relazione tra i client e i diversi componenti della gestione tabelle di routing.

![relazione tra client e componenti di Gestione tabelle di routing](images/rtmentrel.png)

Gestione router avvia una o più istanze della gestione tabelle di routing. Quando vengono avviate più istanze del gestore tabelle di routing, il router è stato configurato per fungere da uno o più router virtuali. Ogni istanza del gestore tabelle di routing è proprietaria di una o più interfacce. ogni interfaccia può essere di proprietà di una sola istanza del gestore tabelle di routing.

Ogni istanza del gestore tabelle di routing è indipendente dalle altre. nessuna informazione viene scambiata tra le istanze.

Ogni istanza del gestore tabelle di routing contiene una o più tabelle di routing. Ogni tabella di routing è associata a una famiglia di indirizzi.

Ogni tabella di routing contiene una o più viste. In questo esempio la tabella di routing viene visualizzata con una vista unicast e multicast. Ogni vista è un subset della tabella di routing.

Nella figura seguente viene illustrata la relazione tra i client e più istanze del gestore tabelle di routing, delle tabelle di routing e delle viste.

![client di relazione, gestione tabelle di routing, tabelle di routing, viste](images/multrtabrel.png)

Un'istanza del client può eseguire la registrazione più volte con un'istanza del gestore tabelle di routing, una volta per ogni famiglia di indirizzi. Un client può eseguire la registrazione con ogni istanza del gestore tabelle di routing.

Nella figura seguente viene illustrato come sono correlate le voci della tabella di routing. Per altre informazioni sulle voci della tabella di routing, vedere [Voci della tabella di routing.](routing-table-entries.md)

![relazione tra le voci della tabella di routing](images/nexthop.png)

La tabella di routing contiene le destinazioni. Ogni destinazione è correlata a una o più route. Ogni route ha zero, uno o più puntatori agli hop successivi associati alla route. Ogni puntatore fa riferimento all'hop successivo effettivo nell'elenco degli hop successivi. Ogni client registrato con il gestore tabelle di routing crea un elenco di hop successivi di cui il client è proprietario.

Le route possono contenere solo puntatori all'elenco hop successivo associato al client proprietario della route.

 

 




