---
title: Protocollo di routing
description: Un protocollo di routing è un tipo di client che esegue la registrazione con gestione tabelle di routing. I router utilizzano i protocolli di routing per scambiare informazioni riguardanti le route a una destinazione.
ms.assetid: 957ec896-94e3-4bdb-801a-12b861460fff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e64d12912494d0d6c20f484eba588b47670a808
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044619"
---
# <a name="routing-protocol"></a>Protocollo di routing

Un protocollo di routing è un tipo di client che esegue la registrazione con gestione tabelle di routing. I router utilizzano i protocolli di routing per scambiare informazioni riguardanti le route a una destinazione.

I protocolli di routing sono unicast o multicast. I protocolli di routing annunciano le route a una destinazione.

Una route unicast a una destinazione viene utilizzata da un protocollo di routing unicast per inoltrare i dati unicast a tale destinazione. Tra gli esempi di protocolli di routing unicast sono inclusi: Routing Information Protocol (RIP), Open Short Path First (OSPF) e Border Gateway Protocol (BGP).

Una route multicast a una destinazione viene utilizzata da alcuni protocolli di routing multicast per creare le informazioni utilizzate per inoltrare i dati multicast dagli host nella rete di destinazione della route (noto come inoltro del percorso inverso). Esempi di protocolli di routing multicast sono: multicast Open Short Path First (MOSPF), Distance Vector Multicast Routing Protocol (DVMRP) e Protocol Independent Multicast (PIM).

Gestione tabelle di routing supporta più istanze dello stesso protocollo, ad esempio l'implementazione Microsoft di OSPF e un OSPF di terze parti, in esecuzione sul router. Questo consente ai router di usare le diverse funzionalità di ogni versione. Questi protocolli hanno identificatori di protocollo diversi.

Gli identificatori di protocollo sono costituiti da un identificatore del fornitore e da un identificatore specifico del protocollo. L'identificatore specifico del protocollo è identico per le diverse implementazioni del protocollo, ad esempio l'implementazione di OSPF di Microsoft e un'implementazione di terze parti di OSPF. Solo quando vengono combinati gli identificatori specifici del fornitore e del protocollo, esiste un identificatore univoco per un protocollo di routing.

Un protocollo con lo stesso identificatore di protocollo (ovvero lo stesso identificatore del fornitore e identificatore specifico del protocollo) può registrare più volte con gestione tabelle di routing. Ogni volta, il protocollo viene registrato utilizzando un identificatore di istanza di protocollo diverso. Ad esempio, un'implementazione di OSPF da un particolare fornitore può essere registrata come vendor-OSPF-1 e vendor-OSPF-2. Questo consente a un'implementazione del protocollo specifica di partizionare le informazioni che mantiene nella tabella di routing.

 

 




