---
title: Ruolo di Network List Manager
description: Ruolo di Network List Manager
ms.assetid: 056d7b0f-5ff7-4b87-8bfe-d4e2018ee638
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3976cdee7a8fa93a7c0dc883f25d65c2e4ae6e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856941"
---
# <a name="the-role-of-network-list-manager"></a><span data-ttu-id="aad1e-103">Ruolo di Network List Manager</span><span class="sxs-lookup"><span data-stu-id="aad1e-103">The Role of Network List Manager</span></span>

<span data-ttu-id="aad1e-104">Prima di Windows XP e Windows Server 2003, era necessario che le applicazioni chiamassero diverse API non correlate per ottenere i dati sugli attributi di rete, ad esempio l'indirizzo IP, il controller di dominio o il Domain Name System (DNS).</span><span class="sxs-lookup"><span data-stu-id="aad1e-104">Prior to Windows XP and Windows Server 2003, applications were required to call a number of unrelated APIs to obtain data about network attributes such as the IP address, the domain controller, or the Domain Name System (DNS).</span></span> <span data-ttu-id="aad1e-105">A partire da Windows XP e Windows Server 2003, l'API Winsock di riconoscimento del percorso di rete include un set limitato di funzionalità relative al percorso di rete.</span><span class="sxs-lookup"><span data-stu-id="aad1e-105">Starting with Windows XP and Windows Server 2003, the Network Location Awareness Winsock API featured a limited set of network location functionality.</span></span> <span data-ttu-id="aad1e-106">In Windows Server 2008 e Windows Vista, il servizio Network Awareness acquisisce gli attributi di rete in un'unica posizione e consente alle applicazioni di eseguire query e recuperare specifiche reti e attributi.</span><span class="sxs-lookup"><span data-stu-id="aad1e-106">In Windows Server 2008 and Windows Vista, the Network Awareness service captures the network attributes in one location and allows applications to query and retrieve specific networks and attributes.</span></span> <span data-ttu-id="aad1e-107">Network List Manager sostituisce la funzionalità dell'API Winsock precedente (disponibile come provider di spazio dei nomi Winsock) mantenendo la compatibilità con le applicazioni meno recenti tramite l'API Winsock.</span><span class="sxs-lookup"><span data-stu-id="aad1e-107">Network List Manager replaces the functionality of the previous Winsock API (available as a Winsock Name Space Provider) while maintaining compatibility with older applications using the Winsock API.</span></span>

 

 




