---
description: È possibile utilizzare le funzioni seguenti per lavorare con i dati sulle prestazioni in Visual Basic.
ms.assetid: c78eeb43-c713-42cc-a38f-f8aaa04f8dae
title: Funzioni dei contatori delle prestazioni per Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c777aa887b9dc42a061de95fb6f33dbf9d3dff7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881746"
---
# <a name="performance-counters-functions-for-visual-basic"></a><span data-ttu-id="08e19-103">Funzioni dei contatori delle prestazioni per Visual Basic</span><span class="sxs-lookup"><span data-stu-id="08e19-103">Performance Counters Functions for Visual Basic</span></span>

> [!IMPORTANT]
> <span data-ttu-id="08e19-104">Le funzioni descritte in questo argomento possono essere modificate o non disponibili in futuro.</span><span class="sxs-lookup"><span data-stu-id="08e19-104">The functions that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="08e19-105">Microsoft consiglia invece di utilizzare le funzioni descritte in [funzioni dei contatori delle prestazioni](performance-counters-functions.md).</span><span class="sxs-lookup"><span data-stu-id="08e19-105">Instead, Microsoft recommends that you use the functions described in [Performance Counters Functions](performance-counters-functions.md).</span></span>

<span data-ttu-id="08e19-106">È possibile utilizzare le funzioni seguenti per lavorare con i dati sulle prestazioni in Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="08e19-106">You can use the following functions to work with performance data in Visual Basic.</span></span>

- [<span data-ttu-id="08e19-107">**PdhCloseQuery**</span><span class="sxs-lookup"><span data-stu-id="08e19-107">**PdhCloseQuery**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhclosequery)
- [<span data-ttu-id="08e19-108">**PdhCollectQueryData**</span><span class="sxs-lookup"><span data-stu-id="08e19-108">**PdhCollectQueryData**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhcollectquerydata)
- [<span data-ttu-id="08e19-109">**PdhRemoveCounter**</span><span class="sxs-lookup"><span data-stu-id="08e19-109">**PdhRemoveCounter**</span></span>](/windows/desktop/api/Pdh/nf-pdh-pdhremovecounter)
- [<span data-ttu-id="08e19-110">**PdhVbAddCounter**</span><span class="sxs-lookup"><span data-stu-id="08e19-110">**PdhVbAddCounter**</span></span>](pdhvbaddcounter.md)
- [<span data-ttu-id="08e19-111">**PdhVbCreateCounterPathList**</span><span class="sxs-lookup"><span data-stu-id="08e19-111">**PdhVbCreateCounterPathList**</span></span>](pdhvbcreatecounterpathlist.md)
- [<span data-ttu-id="08e19-112">**PdhVbGetCounterPathElements**</span><span class="sxs-lookup"><span data-stu-id="08e19-112">**PdhVbGetCounterPathElements**</span></span>](pdhvbgetcounterpathelements.md)
- [<span data-ttu-id="08e19-113">**PdhVbGetCounterPathFromList**</span><span class="sxs-lookup"><span data-stu-id="08e19-113">**PdhVbGetCounterPathFromList**</span></span>](pdhvbgetcounterpathfromlist.md)
- [<span data-ttu-id="08e19-114">**PdhVbGetDoubleCounterValue**</span><span class="sxs-lookup"><span data-stu-id="08e19-114">**PdhVbGetDoubleCounterValue**</span></span>](pdhvbgetdoublecountervalue.md)
- [<span data-ttu-id="08e19-115">**PdhVbGetLogFileSize**</span><span class="sxs-lookup"><span data-stu-id="08e19-115">**PdhVbGetLogFileSize**</span></span>](pdhvbgetlogfilesize.md)
- [<span data-ttu-id="08e19-116">**PdhVbGetOneCounterPath**</span><span class="sxs-lookup"><span data-stu-id="08e19-116">**PdhVbGetOneCounterPath**</span></span>](pdhvbgetonecounterpath.md)
- [<span data-ttu-id="08e19-117">**PdhVbIsGoodStatus**</span><span class="sxs-lookup"><span data-stu-id="08e19-117">**PdhVbIsGoodStatus**</span></span>](pdhvbisgoodstatus.md)
- [<span data-ttu-id="08e19-118">**PdhVbOpenLog**</span><span class="sxs-lookup"><span data-stu-id="08e19-118">**PdhVbOpenLog**</span></span>](pdhvbopenlog.md)
- [<span data-ttu-id="08e19-119">**PdhVbOpenQuery**</span><span class="sxs-lookup"><span data-stu-id="08e19-119">**PdhVbOpenQuery**</span></span>](pdhvbopenquery.md)
- [<span data-ttu-id="08e19-120">**PdhVbUpdateLog**</span><span class="sxs-lookup"><span data-stu-id="08e19-120">**PdhVbUpdateLog**</span></span>](pdhvbupdatelog.md)

> [!NOTE]
> <span data-ttu-id="08e19-121">Le `PdhVb***` funzioni funzionano in una sessione per processo e non sono thread-safe.</span><span class="sxs-lookup"><span data-stu-id="08e19-121">The `PdhVb***` functions work on a per-process session and are not thread-safe.</span></span> <span data-ttu-id="08e19-122">Queste funzioni devono essere usate solo da semplici applicazioni a thread singolo.</span><span class="sxs-lookup"><span data-stu-id="08e19-122">These functions should only be used from simple single-threaded applications.</span></span>
