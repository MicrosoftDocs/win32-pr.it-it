---
description: È possibile utilizzare il servizio partizioni COM+ per installare versioni diverse di un'applicazione COM+ in un computer ed eseguirle contemporaneamente.
ms.assetid: fd22a64c-f2d8-48af-86e1-985e21b0f8fa
title: Partizioni COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd4e1efdd42ac407d8937c4090c59e65472ed69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877505"
---
# <a name="com-partitions"></a><span data-ttu-id="2fd72-103">Partizioni COM+</span><span class="sxs-lookup"><span data-stu-id="2fd72-103">COM+ Partitions</span></span>

<span data-ttu-id="2fd72-104">È possibile utilizzare il servizio partizioni COM+ per installare versioni diverse di un'applicazione COM+ in un computer ed eseguirle contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="2fd72-104">You can use the COM+ partitions service to install different versions of a COM+ application on a computer and run them simultaneously.</span></span>

<span data-ttu-id="2fd72-105">**Windows XP:** La possibilità di creare, configurare o delegare partizioni COM+ non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="2fd72-105">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="2fd72-106">La partizione globale è l'unica partizione COM+ disponibile.</span><span class="sxs-lookup"><span data-stu-id="2fd72-106">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="2fd72-107">\* \* Windows 2000: \* \* il servizio partizioni COM+ non è disponibile in Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2fd72-107">\*\*Windows 2000:  \*\* The COM+ partitions service is not available in Windows 2000.</span></span>

<span data-ttu-id="2fd72-108">Negli argomenti seguenti vengono fornite informazioni sul servizio partizioni COM+.</span><span class="sxs-lookup"><span data-stu-id="2fd72-108">The following topics provide information about the COM+ partitions service.</span></span>



| <span data-ttu-id="2fd72-109">Argomento</span><span class="sxs-lookup"><span data-stu-id="2fd72-109">Topic</span></span>                                                               | <span data-ttu-id="2fd72-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fd72-110">Description</span></span>                                                                 |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="2fd72-111">Concetti relativi alle partizioni COM+</span><span class="sxs-lookup"><span data-stu-id="2fd72-111">COM+ Partitions Concepts</span></span>](com--partitions-concepts.md)<br/> | <span data-ttu-id="2fd72-112">Viene fornita una panoramica dell'utilizzo di partizioni COM+.</span><span class="sxs-lookup"><span data-stu-id="2fd72-112">Provides an overview of using COM+ partitions.</span></span><br/>                   |
| [<span data-ttu-id="2fd72-113">Attività partizioni COM+</span><span class="sxs-lookup"><span data-stu-id="2fd72-113">COM+ Partitions Tasks</span></span>](com--partitions-tasks.md)<br/>       | <span data-ttu-id="2fd72-114">Vengono fornite istruzioni per la creazione e la gestione di partizioni COM+.</span><span class="sxs-lookup"><span data-stu-id="2fd72-114">Provides instructions for creating and managing COM+ partitions.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="2fd72-115">Il servizio partizioni COM+ non è abilitato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2fd72-115">The COM+ partitions service is not enabled by default.</span></span> <span data-ttu-id="2fd72-116">Per utilizzare il servizio partizioni COM+, è necessario abilitarlo tramite lo strumento di amministrazione Servizi componenti o modificando la proprietà PartitionsEnabled nella raccolta [**LocalComputer**](localcomputer.md) su true.</span><span class="sxs-lookup"><span data-stu-id="2fd72-116">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

 

 




