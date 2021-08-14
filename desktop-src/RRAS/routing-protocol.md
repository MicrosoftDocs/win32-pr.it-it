---
title: Protocollo di routing
description: Un protocollo di routing è un tipo di client che viene registrato con gestione tabelle di routing. I router usano i protocolli di routing per scambiare informazioni relative alle route verso una destinazione.
ms.assetid: 957ec896-94e3-4bdb-801a-12b861460fff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 879d540662db7d1a1603bf40818101d0e7f9cb6988d4c0065f922fdc8f73e381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119977844"
---
# <a name="routing-protocol"></a>Protocollo di routing

Un protocollo di routing è un tipo di client che viene registrato con gestione tabelle di routing. I router usano i protocolli di routing per scambiare informazioni relative alle route verso una destinazione.

I protocolli di routing sono unicast o multicast. I protocolli di routing annunciano le route a una destinazione.

Una route unicast a una destinazione viene usata da un protocollo di routing unicast per inoltrare i dati unicast a tale destinazione. Esempi di protocolli di routing unicast includono: Routing Information Protocol (RIP), Open Shortest Path First (OSPF) e Border Gateway Protocol (BGP).

Una route multicast a una destinazione viene usata da alcuni protocolli di routing multicast per creare le informazioni usate per inoltrare i dati multicast dagli host nella rete di destinazione della route (nota come inoltro del percorso inverso). Esempi di protocolli di routing multicast includono: Multicast Open Shortest Path First (MOSPF), Distance Vector Multicast Routing Protocol (DVMRP) e Protocol Independent Multicast (PIM).

Il gestore tabelle di routing supporta più istanze dello stesso protocollo ,ad esempio l'implementazione microsoft di OSPF e OSPF di terze parti, in esecuzione nel router. In questo modo i router possono usare le diverse funzionalità di ogni versione. Questi protocolli hanno identificatori di protocollo diversi.

Gli identificatori di protocollo sono costituiti da un identificatore del fornitore e da un identificatore specifico del protocollo. L'identificatore specifico del protocollo è lo stesso per diverse implementazioni del protocollo, ad esempio l'implementazione microsoft di OSPF e un'implementazione di terze parti di OSPF. Solo quando vengono combinati gli identificatori specifici del fornitore e del protocollo, esiste un identificatore univoco per un protocollo di routing.

Un protocollo con lo stesso identificatore di protocollo, ovvero lo stesso identificatore fornitore e identificatore specifico del protocollo, può essere registrato più volte con il gestore tabelle di routing. Ogni volta, il protocollo viene registrato usando un identificatore di istanza del protocollo diverso. Ad esempio, un'implementazione di OSPF da un fornitore specifico può registrarsi come Vendor-OSPF-1 e Vendor-OSPF-2. Ciò consente a un'implementazione specifica del protocollo di partizionare le informazioni conservate nella tabella di routing.

 

 




