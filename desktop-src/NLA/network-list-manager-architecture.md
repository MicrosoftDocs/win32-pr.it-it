---
title: Architettura di Network List Manager
description: Architettura di Network List Manager
ms.assetid: d3d03891-7c61-4f7e-a2e2-ef13353e8688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108ecbb36c5421bc7e3057c43feb10f92400493b306ecb21502a541c1bb4cba6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685647"
---
# <a name="network-list-manager-architecture"></a>Architettura di Network List Manager

Network List Manager viene eseguito come servizio nel contesto di Svchost.exe e viene avviato durante la procedura di avvio del computer. Il servizio Network List Manager gestisce una tabella delle reti disponibili e degli attributi di rete recuperati dalle applicazioni tramite l'API Gestione elenchi di rete. Gestione elenchi di rete offre funzioni di base per filtrare ed eseguire query sul servizio Gestione elenchi reti per reti specifiche e recuperare gli attributi di queste reti. Il diagramma seguente illustra l'architettura di Network List Manager e l'interazione tra il servizio Network List Manager e l'applicazione client.

![Diagramma dell'architettura di riconoscimento della rete](images/architecture.png)

 

 




