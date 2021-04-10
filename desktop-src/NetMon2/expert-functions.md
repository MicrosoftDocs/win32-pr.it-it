---
description: Le funzioni di supporto seguenti possono essere chiamate solo da esperti che esportano la funzione Run o Configure.
ms.assetid: 6890087c-7c94-41ff-bb5c-4bf88a4e07cc
title: Funzioni di esperti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7441289008c7dcd647775c2932e210ccd09b24bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878670"
---
# <a name="expert-functions"></a><span data-ttu-id="a2eb6-103">Funzioni di esperti</span><span class="sxs-lookup"><span data-stu-id="a2eb6-103">Expert Functions</span></span>

<span data-ttu-id="a2eb6-104">Le funzioni di supporto seguenti possono essere chiamate solo da esperti che esportano la funzione [Run](run.md) o [Configure](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="a2eb6-104">The following helper functions can only be called by experts that export the [Run](run.md) or [Configure](configure.md) function.</span></span>



| <span data-ttu-id="a2eb6-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="a2eb6-105">Function</span></span>                                         | <span data-ttu-id="a2eb6-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2eb6-106">Description</span></span>                                                                             |
|--------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2eb6-107">ExpertGetFrame</span><span class="sxs-lookup"><span data-stu-id="a2eb6-107">ExpertGetFrame</span></span>](expertgetframe.md)             | <span data-ttu-id="a2eb6-108">Recupera un frame specificato dall'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="a2eb6-108">Retrieves a given frame from the capture.</span></span>                                               |
| [<span data-ttu-id="a2eb6-109">ExpertIndicateStatus</span><span class="sxs-lookup"><span data-stu-id="a2eb6-109">ExpertIndicateStatus</span></span>](expertindicatestatus.md) | <span data-ttu-id="a2eb6-110">Indica la percentuale di completamento dell'analisi dell'acquisizione dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="a2eb6-110">Indicates the percentage of completion of the expert's analysis of capture.</span></span>             |
| [<span data-ttu-id="a2eb6-111">ExpertGetStartupInfo</span><span class="sxs-lookup"><span data-stu-id="a2eb6-111">ExpertGetStartupInfo</span></span>](expertgetstartupinfo.md) | <span data-ttu-id="a2eb6-112">Recupera le informazioni di avvio per l'esperto.</span><span class="sxs-lookup"><span data-stu-id="a2eb6-112">Retrieves the startup information for the expert.</span></span>                                       |
| [<span data-ttu-id="a2eb6-113">ExpertMemorySize</span><span class="sxs-lookup"><span data-stu-id="a2eb6-113">ExpertMemorySize</span></span>](expertmemorysize.md)         | <span data-ttu-id="a2eb6-114">Recupera le dimensioni della memoria allocata da una chiamata alla funzione **ExpertAllocMemory** .</span><span class="sxs-lookup"><span data-stu-id="a2eb6-114">Retrieves the size of memory allocated by a call to the **ExpertAllocMemory** function.</span></span> |
| [<span data-ttu-id="a2eb6-115">ExpertSubmitEvent</span><span class="sxs-lookup"><span data-stu-id="a2eb6-115">ExpertSubmitEvent</span></span>](expertsubmitevent.md)       | <span data-ttu-id="a2eb6-116">Indica un problema e recupera le informazioni sul problema, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="a2eb6-116">Indicates a problem and retrieves information about the problem if one exists.</span></span>          |
| [<span data-ttu-id="a2eb6-117">ExpertAllocMemory</span><span class="sxs-lookup"><span data-stu-id="a2eb6-117">ExpertAllocMemory</span></span>](expertallocmemory.md)       | <span data-ttu-id="a2eb6-118">Alloca memoria per l'esperto.</span><span class="sxs-lookup"><span data-stu-id="a2eb6-118">Allocates memory for the expert.</span></span>                                                        |
| [<span data-ttu-id="a2eb6-119">ExpertReallocMemory</span><span class="sxs-lookup"><span data-stu-id="a2eb6-119">ExpertReallocMemory</span></span>](expertreallocmemory.md)   | <span data-ttu-id="a2eb6-120">Modifica le dimensioni della memoria allocata dalla funzione **ExpertAllocMemory** .</span><span class="sxs-lookup"><span data-stu-id="a2eb6-120">Changes the size of the memory allocated by the **ExpertAllocMemory** function.</span></span>         |
| [<span data-ttu-id="a2eb6-121">ExpertFreeMemory</span><span class="sxs-lookup"><span data-stu-id="a2eb6-121">ExpertFreeMemory</span></span>](expertfreememory.md)         | <span data-ttu-id="a2eb6-122">Libera la memoria allocata dall'esperto.</span><span class="sxs-lookup"><span data-stu-id="a2eb6-122">Frees memory allocated by the expert.</span></span>                                                   |



 

<span data-ttu-id="a2eb6-123">Per informazioni sulle funzioni di esportazione, le funzioni di supporto che possono essere chiamate da esperti e analizzatori, strutture ed enumerazioni, vedere gli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="a2eb6-123">For information about export functions, helper functions that can be called by experts and parsers, structures, and enumerations, see the following topics:</span></span>



| <span data-ttu-id="a2eb6-124">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="a2eb6-124">For information about</span></span>                                             | <span data-ttu-id="a2eb6-125">Vedere</span><span class="sxs-lookup"><span data-stu-id="a2eb6-125">See</span></span>                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="a2eb6-126">Funzioni esportate da esperti</span><span class="sxs-lookup"><span data-stu-id="a2eb6-126">Functions that are exported by experts</span></span>                            | [<span data-ttu-id="a2eb6-127">Funzioni di esportazione DLL di esperti</span><span class="sxs-lookup"><span data-stu-id="a2eb6-127">Expert DLL Export Functions</span></span>](expert-dll-export-functions.md)               |
| <span data-ttu-id="a2eb6-128">Strutture utilizzate dalle funzioni di esperti</span><span class="sxs-lookup"><span data-stu-id="a2eb6-128">Structures that are used by expert functions</span></span>                      | [<span data-ttu-id="a2eb6-129">Strutture di esperti</span><span class="sxs-lookup"><span data-stu-id="a2eb6-129">Expert Structures</span></span>](expert-structures.md)                                   |
| <span data-ttu-id="a2eb6-130">Enumerazioni utilizzate da funzioni e strutture di esperti</span><span class="sxs-lookup"><span data-stu-id="a2eb6-130">Enumerations used by expert structures and functions</span></span>              | [<span data-ttu-id="a2eb6-131">Enumerazioni di esperti</span><span class="sxs-lookup"><span data-stu-id="a2eb6-131">Expert Enumerations</span></span>](expert-enumerations.md)                               |
| <span data-ttu-id="a2eb6-132">Funzioni di supporto comuni che possono essere chiamate da esperti e analizzatori</span><span class="sxs-lookup"><span data-stu-id="a2eb6-132">Common helper functions that can be called by experts and parsers</span></span> | [<span data-ttu-id="a2eb6-133">Funzioni comuni di esperti e parser</span><span class="sxs-lookup"><span data-stu-id="a2eb6-133">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |



 

 

 



