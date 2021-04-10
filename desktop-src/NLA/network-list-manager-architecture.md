---
title: Architettura di Network List Manager
description: Architettura di Network List Manager
ms.assetid: d3d03891-7c61-4f7e-a2e2-ef13353e8688
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a567b103cfd5d9944aa33a799c2cc1bc4b983759
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955827"
---
# <a name="network-list-manager-architecture"></a>Architettura di Network List Manager

Gestione elenco reti viene eseguito come servizio nel contesto di Svchost.exe e viene avviato durante la procedura di avvio del computer. Il servizio Network List Manager gestisce una tabella di reti e attributi di rete disponibili recuperati dalle applicazioni tramite l'API Network List Manager. Network List Manager fornisce funzioni di base per filtrare ed eseguire query sul servizio Network List Manager per reti specifiche e recuperare gli attributi di queste reti. Il diagramma seguente illustra l'architettura di Network List Manager e l'interazione tra il servizio Network List Manager e l'applicazione client.

![diagramma dell'architettura di riconoscimento della rete](images/architecture.png)

 

 




