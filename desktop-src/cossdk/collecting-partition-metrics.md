---
description: Raccolta delle metriche della partizione
ms.assetid: 2dc35011-24fa-49df-9cf8-96db2de39efa
title: Raccolta delle metriche della partizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6467dfb9c891e7ae57505c8ec3815bfa99e49d8a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126363"
---
# <a name="collecting-partition-metrics"></a><span data-ttu-id="eaf98-103">Raccolta delle metriche della partizione</span><span class="sxs-lookup"><span data-stu-id="eaf98-103">Collecting Partition Metrics</span></span>

<span data-ttu-id="eaf98-104">In alcuni casi, un'organizzazione potrebbe voler raccogliere informazioni sull'uso dell'applicazione COM+ ai fini del monitoraggio, della pianificazione della capacità e dell'account delle risorse.</span><span class="sxs-lookup"><span data-stu-id="eaf98-104">In some cases, an organization might want to collect information on COM+ application use for the purposes of monitoring, capacity planning, and resource accounting.</span></span>

<span data-ttu-id="eaf98-105">Ad esempio, un provider di servizi dell'applicazione (ASP) potrebbe voler addebitare un cliente per l'utilizzo delle risorse.</span><span class="sxs-lookup"><span data-stu-id="eaf98-105">For example, an application service provider (ASP) might want to charge a customer for its resource usage.</span></span> <span data-ttu-id="eaf98-106">A tale scopo, COM+ consente di raccogliere informazioni relative a eventi e metriche in base a ogni partizione.</span><span class="sxs-lookup"><span data-stu-id="eaf98-106">To do this, COM+ allows you to collect event and metrics information on a per-partition basis.</span></span>

<span data-ttu-id="eaf98-107">Per raccogliere queste informazioni per una partizione specifica, è necessario specificare, per ogni interfaccia di strumentazione COM+, il membro dell'ID di partizione all'interno della struttura di eventi standard.</span><span class="sxs-lookup"><span data-stu-id="eaf98-107">The way to collect this information for a specific partition is by specifying, for each COM+ instrumentation interface, the partition ID member within the standard event structure.</span></span> <span data-ttu-id="eaf98-108">La struttura dell'evento è il primo valore di un'interfaccia di strumentazione COM+.</span><span class="sxs-lookup"><span data-stu-id="eaf98-108">The event structure is the first value of a COM+ instrumentation interface.</span></span> <span data-ttu-id="eaf98-109">Per ulteriori informazioni, vedere [interfacce di strumentazione com+](com--instrumentation-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="eaf98-109">For more information, see [COM+ Instrumentation Interfaces](com--instrumentation-interfaces.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eaf98-110">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eaf98-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eaf98-111">Configurazione della cache della partizione</span><span class="sxs-lookup"><span data-stu-id="eaf98-111">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="eaf98-112">Raggruppamento di applicazioni in partizioni</span><span class="sxs-lookup"><span data-stu-id="eaf98-112">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="eaf98-113">Gestione delle partizioni locali</span><span class="sxs-lookup"><span data-stu-id="eaf98-113">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="eaf98-114">Gestione di partizioni all'interno Active Directory</span><span class="sxs-lookup"><span data-stu-id="eaf98-114">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="eaf98-115">Impostazione dei diritti amministrativi per una partizione</span><span class="sxs-lookup"><span data-stu-id="eaf98-115">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



