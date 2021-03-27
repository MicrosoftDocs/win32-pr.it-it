---
title: API stato processo
description: Ottenere informazioni su processi, moduli (file eseguibili o dll) e driver di dispositivo. Raccogliere i dati di utilizzo della memoria. Eseguire snapshot della quantità di memoria mappata fisicamente al contesto del processo.
ms.assetid: 512c3f0f-b1b5-43a0-9460-eb668315d6f4
keywords:
- API stato processo
- Helper stato processo
- PSAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6a2234ee53acda22df6b6be6267815ba68090be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047217"
---
# <a name="process-status-api"></a><span data-ttu-id="140a0-108">API stato processo</span><span class="sxs-lookup"><span data-stu-id="140a0-108">Process Status API</span></span>

<span data-ttu-id="140a0-109">Lo stato del processo Application Programming Interface (PSAPI) è una libreria helper che consente di ottenere più facilmente informazioni sui processi e sui driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="140a0-109">The process status application programming interface (PSAPI) is a helper library that makes it easier for you to obtain information about processes and device drivers.</span></span> <span data-ttu-id="140a0-110">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="140a0-110">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="140a0-111">Informazioni su PSAPI</span><span class="sxs-lookup"><span data-stu-id="140a0-111">About PSAPI</span></span>](about-psapi.md)
-   [<span data-ttu-id="140a0-112">Uso di PSAPI</span><span class="sxs-lookup"><span data-stu-id="140a0-112">Using PSAPI</span></span>](using-psapi.md)
-   [<span data-ttu-id="140a0-113">Riferimento a PSAPI</span><span class="sxs-lookup"><span data-stu-id="140a0-113">PSAPI Reference</span></span>](psapi-reference.md)

<span data-ttu-id="140a0-114">Queste funzioni sono disponibili in Psapi.dll.</span><span class="sxs-lookup"><span data-stu-id="140a0-114">These functions are available in Psapi.dll.</span></span>

<span data-ttu-id="140a0-115">Le stesse informazioni sono disponibili a livello generale tramite i dati sulle prestazioni nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="140a0-115">The same information is generally available through the performance data in the registry.</span></span> <span data-ttu-id="140a0-116">Per altre informazioni, vedere [i contatori delle prestazioni](/windows/desktop/PerfCtrs/performance-counters-portal).</span><span class="sxs-lookup"><span data-stu-id="140a0-116">For more information, see [Performance Counters](/windows/desktop/PerfCtrs/performance-counters-portal).</span></span>

 

 