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
# <a name="network-list-manager-architecture"></a><span data-ttu-id="88f49-103">Architettura di Network List Manager</span><span class="sxs-lookup"><span data-stu-id="88f49-103">Network List Manager Architecture</span></span>

<span data-ttu-id="88f49-104">Gestione elenco reti viene eseguito come servizio nel contesto di Svchost.exe e viene avviato durante la procedura di avvio del computer.</span><span class="sxs-lookup"><span data-stu-id="88f49-104">Network List Manager runs as a service in the context of Svchost.exe and is started during the computer boot procedure.</span></span> <span data-ttu-id="88f49-105">Il servizio Network List Manager gestisce una tabella di reti e attributi di rete disponibili recuperati dalle applicazioni tramite l'API Network List Manager.</span><span class="sxs-lookup"><span data-stu-id="88f49-105">The Network List Manager service maintains a table of available networks and network attributes that are retrieved by applications through the Network List Manager API.</span></span> <span data-ttu-id="88f49-106">Network List Manager fornisce funzioni di base per filtrare ed eseguire query sul servizio Network List Manager per reti specifiche e recuperare gli attributi di queste reti.</span><span class="sxs-lookup"><span data-stu-id="88f49-106">Network List Manager provides basic functions to filter and query the Network List Manager service for specific networks and retrieve the attributes of these networks.</span></span> <span data-ttu-id="88f49-107">Il diagramma seguente illustra l'architettura di Network List Manager e l'interazione tra il servizio Network List Manager e l'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="88f49-107">The following diagram shows the Network List Manager architecture and the interaction between the Network List Manager service and the client application.</span></span>

![diagramma dell'architettura di riconoscimento della rete](images/architecture.png)

 

 




