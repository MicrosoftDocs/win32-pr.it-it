---
description: Le funzioni seguenti sono i punti di ingresso per le DLL di esperti e per le chiamate dal sistema operativo e Network Monitor.
ms.assetid: 1c0dcf6f-7f80-424b-9e6a-5a8b6a5b176f
title: Funzioni di esportazione DLL di esperti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923611521b98619b357eb2de93ee2269caf9c838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966482"
---
# <a name="expert-dll-export-functions"></a><span data-ttu-id="64a03-103">Funzioni di esportazione DLL di esperti</span><span class="sxs-lookup"><span data-stu-id="64a03-103">Expert DLL Export Functions</span></span>

<span data-ttu-id="64a03-104">Le funzioni seguenti sono i punti di ingresso per le DLL di esperti e per le chiamate dal sistema operativo e Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="64a03-104">The following functions are the entry points for expert DLLs and for calls from the operating system and Network Monitor.</span></span>



| <span data-ttu-id="64a03-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="64a03-105">Function</span></span>                                   | <span data-ttu-id="64a03-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64a03-106">Description</span></span>                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64a03-107">**Esperto DllMain**</span><span class="sxs-lookup"><span data-stu-id="64a03-107">**DllMain Expert**</span></span>](dllmain-expert.md)   | <span data-ttu-id="64a03-108">Indica che la DLL di esperti è stata caricata o scaricata.</span><span class="sxs-lookup"><span data-stu-id="64a03-108">Indicates that the expert DLL has been loaded or unloaded.</span></span> <span data-ttu-id="64a03-109">Quando un processo carica o Scarica la DLL, il sistema operativo chiama la funzione [**DllMain**](/windows/desktop/Dlls/dllmain) .</span><span class="sxs-lookup"><span data-stu-id="64a03-109">When a process loads or unloads the DLL, the operating system calls the [**DllMain**](/windows/desktop/Dlls/dllmain) function.</span></span> |
| [<span data-ttu-id="64a03-110">**Registra esperto**</span><span class="sxs-lookup"><span data-stu-id="64a03-110">**Register Expert**</span></span>](register-expert.md) | <span data-ttu-id="64a03-111">Determina le informazioni di base sull'esperto all'interno della DLL.</span><span class="sxs-lookup"><span data-stu-id="64a03-111">Determines basic information about the expert within the DLL.</span></span> <span data-ttu-id="64a03-112">Network Monitor chiama la funzione **Register** .</span><span class="sxs-lookup"><span data-stu-id="64a03-112">Network Monitor calls the **Register** function.</span></span>                                                           |
| [<span data-ttu-id="64a03-113">**Configurare**</span><span class="sxs-lookup"><span data-stu-id="64a03-113">**Configure**</span></span>](configure.md)             | <span data-ttu-id="64a03-114">Configura l'esperto all'interno della DLL.</span><span class="sxs-lookup"><span data-stu-id="64a03-114">Configures the expert within the DLL.</span></span> <span data-ttu-id="64a03-115">Network Monitor chiama la funzione [**Configure**](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="64a03-115">Network Monitor calls the [**Configure**](configure.md) function.</span></span>                                                                 |
| [<span data-ttu-id="64a03-116">**Correre**</span><span class="sxs-lookup"><span data-stu-id="64a03-116">**Run**</span></span>](run.md)                         | <span data-ttu-id="64a03-117">Avvia l'esperto all'interno della DLL.</span><span class="sxs-lookup"><span data-stu-id="64a03-117">Starts the expert within the DLL.</span></span> <span data-ttu-id="64a03-118">Network Monitor chiama la funzione [**Run**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="64a03-118">Network Monitor calls the [**Run**](run.md) function.</span></span>                                                                                 |



 

<span data-ttu-id="64a03-119">Network Monitor fornisce anche strutture, enumerazioni e funzioni di supporto che l'esperto può chiamare.</span><span class="sxs-lookup"><span data-stu-id="64a03-119">Network Monitor also provides structures, enumerations, and helper functions that the expert can call.</span></span>



| <span data-ttu-id="64a03-120">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="64a03-120">For information about</span></span>                                      | <span data-ttu-id="64a03-121">Vedere</span><span class="sxs-lookup"><span data-stu-id="64a03-121">See</span></span>                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="64a03-122">Funzioni helper che possono essere chiamate da esperti e analizzatori</span><span class="sxs-lookup"><span data-stu-id="64a03-122">Helper functions that can be called by experts and parsers</span></span> | [<span data-ttu-id="64a03-123">Funzioni comuni di esperti e parser</span><span class="sxs-lookup"><span data-stu-id="64a03-123">Expert and Parser Common Functions</span></span>](expert-and-parser-common-functions.md) |
| <span data-ttu-id="64a03-124">Funzioni di supporto chiamate solo da esperti</span><span class="sxs-lookup"><span data-stu-id="64a03-124">Helper functions that are called only by experts</span></span>           | [<span data-ttu-id="64a03-125">Funzioni di esperti</span><span class="sxs-lookup"><span data-stu-id="64a03-125">Expert Functions</span></span>](expert-functions.md)                                     |
| <span data-ttu-id="64a03-126">Strutture utilizzate dalle funzioni di esperti</span><span class="sxs-lookup"><span data-stu-id="64a03-126">Structures that are used by expert functions</span></span>               | [<span data-ttu-id="64a03-127">Strutture di esperti</span><span class="sxs-lookup"><span data-stu-id="64a03-127">Expert Structures</span></span>](expert-structures.md)                                   |
| <span data-ttu-id="64a03-128">Enumerazioni utilizzate da funzioni e strutture di esperti</span><span class="sxs-lookup"><span data-stu-id="64a03-128">Enumerations used by expert structures and functions</span></span>       | [<span data-ttu-id="64a03-129">Enumerazioni di esperti</span><span class="sxs-lookup"><span data-stu-id="64a03-129">Expert Enumerations</span></span>](expert-enumerations.md)                               |



 

 

 
