---
description: In questa sezione vengono descritte le strutture di NPP utilizzate dai metodi NPP.
ms.assetid: f0729dc5-6b5f-4f24-85d6-47c45f1bf9be
title: Strutture NPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b514bded37450f6a7c33a016b231bb38f0c1812
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308160"
---
# <a name="npp-structures"></a><span data-ttu-id="d1ac1-103">Strutture NPP</span><span class="sxs-lookup"><span data-stu-id="d1ac1-103">NPP Structures</span></span>

<span data-ttu-id="d1ac1-104">In questa sezione vengono descritte le strutture di NPP utilizzate dai metodi NPP.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-104">This section describes the NPP structures used by NPP methods.</span></span> <span data-ttu-id="d1ac1-105">Queste strutture vengono utilizzate per recuperare le statistiche, fornire informazioni statistiche e sullo stato del sistema e indicare i computer che eseguono Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-105">These structures are used to retrieve statistics, provide system status and statistical information, and indicate which computers are running Network Monitor.</span></span> <span data-ttu-id="d1ac1-106">Queste strutture sono descritte nelle tabelle seguenti.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-106">The following tables describes these structures.</span></span>



| <span data-ttu-id="d1ac1-107">Strutture NPP</span><span class="sxs-lookup"><span data-stu-id="d1ac1-107">NPP Structures</span></span>                     | <span data-ttu-id="d1ac1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1ac1-108">Description</span></span>                                                                                                                      |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1ac1-109">SESSIONSTATS</span><span class="sxs-lookup"><span data-stu-id="d1ac1-109">SESSIONSTATS</span></span>](sessionstats.md)   | <span data-ttu-id="d1ac1-110">Fornisce informazioni sulla sessione quando vengono recuperate le statistiche di conversazione.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-110">Provides session information when conversation statistics are retrieved.</span></span>                                                         |
| [<span data-ttu-id="d1ac1-111">STATIONSTATS</span><span class="sxs-lookup"><span data-stu-id="d1ac1-111">STATIONSTATS</span></span>](stationstats.md)   | <span data-ttu-id="d1ac1-112">Fornisce statistiche relative a una [*stazione*](s.md)specifica.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-112">Provides statistics about a specific [*station*](s.md).</span></span>                                                     |
| [<span data-ttu-id="d1ac1-113">Statistiche</span><span class="sxs-lookup"><span data-stu-id="d1ac1-113">STATISTICS</span></span>](statistics.md)       | <span data-ttu-id="d1ac1-114">Fornisce le statistiche di rete quando vengono recuperate le statistiche totali e quando l'acquisizione corrente è stata sospesa o arrestata.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-114">Provides network statistics when total statistics are retrieved and when the current capture has paused or stopped.</span></span>              |
| [<span data-ttu-id="d1ac1-115">QUERYTABLE</span><span class="sxs-lookup"><span data-stu-id="d1ac1-115">QUERYTABLE</span></span>](querytable.md)       | <span data-ttu-id="d1ac1-116">Indica i computer che utilizzano Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-116">Indicates which computers are using Network Monitor.</span></span>                                                                             |
| [<span data-ttu-id="d1ac1-117">STATIONQUERY</span><span class="sxs-lookup"><span data-stu-id="d1ac1-117">STATIONQUERY</span></span>](stationquery.md)   | <span data-ttu-id="d1ac1-118">Fornisce informazioni su un computer che utilizza Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-118">Provides information about a computer that is using Network Monitor.</span></span> <span data-ttu-id="d1ac1-119">Questa struttura viene utilizzata dalla struttura **QUERYTABLE** di NPP.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-119">This structure is used by the NPP **QUERYTABLE** structure.</span></span> |
| [<span data-ttu-id="d1ac1-120">NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="d1ac1-120">NETWORKSTATUS</span></span>](networkstatus.md) | <span data-ttu-id="d1ac1-121">Fornisce lo stato corrente della rete in termini di stato del sistema.</span><span class="sxs-lookup"><span data-stu-id="d1ac1-121">Provides current network status in terms of system state.</span></span>                                                                        |



 

 

 



