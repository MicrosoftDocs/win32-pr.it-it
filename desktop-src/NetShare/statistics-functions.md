---
description: Il sistema operativo Windows accumula un set di statistiche operative per le workstation e i server dal momento in cui viene avviata la workstation o il servizio Server.
ms.assetid: 4e0217bf-7550-40a2-b47c-8e898a586005
title: Funzioni statistiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce62e12f3c4894ba86ff5e5aaaa38801d272195c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315884"
---
# <a name="statistics-functions"></a><span data-ttu-id="d582f-103">Funzioni statistiche</span><span class="sxs-lookup"><span data-stu-id="d582f-103">Statistics Functions</span></span>

<span data-ttu-id="d582f-104">Il sistema operativo Windows accumula un set di statistiche operative per le workstation e i server dal momento in cui viene avviata la workstation o il servizio Server.</span><span class="sxs-lookup"><span data-stu-id="d582f-104">The Windows operating system accumulates a set of operating statistics for workstations and servers from the time that the workstation or server service is started.</span></span> <span data-ttu-id="d582f-105">Per recuperare queste statistiche, è possibile chiamare la seguente funzione di statistiche di gestione di rete.</span><span class="sxs-lookup"><span data-stu-id="d582f-105">To retrieve these statistics, you can call the following network management statistics function.</span></span>



| <span data-ttu-id="d582f-106">Funzione</span><span class="sxs-lookup"><span data-stu-id="d582f-106">Function</span></span>                                     | <span data-ttu-id="d582f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d582f-107">Description</span></span>                                                                                 |
|----------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d582f-108">**NetStatisticsGet**</span><span class="sxs-lookup"><span data-stu-id="d582f-108">**NetStatisticsGet**</span></span>](/windows/desktop/api/Lmstats/nf-lmstats-netstatisticsget) | <span data-ttu-id="d582f-109">Recupera le statistiche operative per un servizio. supporta i servizi workstation e server.</span><span class="sxs-lookup"><span data-stu-id="d582f-109">Retrieves operating statistics for a service; supports the workstation and server services.</span></span> |



 

<span data-ttu-id="d582f-110">La funzione **NetStatisticsGet** restituisce una struttura [**Stat \_ workstation \_ 0**](/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0-r1) quando vengono richieste statistiche Workstation; la funzione restituisce una struttura [**Stat \_ server \_ 0**](/windows/desktop/api/Lmstats/ns-lmstats-stat_server_0) quando vengono richieste le statistiche del server.</span><span class="sxs-lookup"><span data-stu-id="d582f-110">The **NetStatisticsGet** function returns a [**STAT\_WORKSTATION\_0**](/windows/win32/api/lmstats/ns-lmstats-stat_workstation_0-r1) structure when workstation statistics are requested; the function returns a [**STAT\_SERVER\_0**](/windows/desktop/api/Lmstats/ns-lmstats-stat_server_0) structure when server statistics are requested.</span></span>

 

 



