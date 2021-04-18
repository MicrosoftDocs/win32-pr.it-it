---
description: Attualmente, tutti i tempi delle chiamate vengono lasciati alle applicazioni.
ms.assetid: 9eb98b48-4bee-4f6d-b818-2f81b36591da
title: Timer stato chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d273d7f8439ebfee9d6668565745ed2c209f70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308088"
---
# <a name="call-state-timer"></a><span data-ttu-id="3cdba-103">Timer stato chiamata</span><span class="sxs-lookup"><span data-stu-id="3cdba-103">Call State Timer</span></span>

<span data-ttu-id="3cdba-104">Attualmente, tutti i tempi delle chiamate vengono lasciati alle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="3cdba-104">Currently, all timing of calls is left up to applications.</span></span> <span data-ttu-id="3cdba-105">Questa operazione può essere gravosa se l'applicazione sta monitorando un numero elevato di chiamate e, se sono presenti più applicazioni, possibilmente su più server, può essere necessario per tutti i timer per mantenere le stesse chiamate.</span><span class="sxs-lookup"><span data-stu-id="3cdba-105">This can be burdensome if the application is monitoring a large number of calls, and if multiple applications are present, possibly on multiple servers, it can be necessary for them to all maintain timers on the same calls.</span></span> <span data-ttu-id="3cdba-106">Per questo motivo, è opportuno che la durata dello stato di chiamata venga gestita dal server.</span><span class="sxs-lookup"><span data-stu-id="3cdba-106">It therefore makes more sense for call state timing to be handled by the server.</span></span>

<span data-ttu-id="3cdba-107">Il membro **tStateEntryTime** in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) consente la temporizzazione delle chiamate negli Stati da segnalare.</span><span class="sxs-lookup"><span data-stu-id="3cdba-107">The **tStateEntryTime** member in [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) allows timing of calls in states to be reported.</span></span> <span data-ttu-id="3cdba-108">Il membro (di tipo **sysTime**) indica l'ora in cui è stato immesso lo stato corrente.</span><span class="sxs-lookup"><span data-stu-id="3cdba-108">The member (of type **SYSTIME**) indicates the time at which the current state was entered.</span></span>

 

 



