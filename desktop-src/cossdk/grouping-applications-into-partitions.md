---
description: Raggruppamento di applicazioni in partizioni
ms.assetid: bdfe2428-9769-4bcb-b74e-a141ba67a67e
title: Raggruppamento di applicazioni in partizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b35c726662d7dbe2cf039678ba5cdb4f94eeea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305323"
---
# <a name="grouping-applications-into-partitions"></a><span data-ttu-id="c1869-103">Raggruppamento di applicazioni in partizioni</span><span class="sxs-lookup"><span data-stu-id="c1869-103">Grouping Applications into Partitions</span></span>

<span data-ttu-id="c1869-104">Quando si decide come raggruppare le applicazioni in partizioni, è necessario che gli amministratori siano consapevoli di alcune regole e restrizioni, incluse le seguenti:</span><span class="sxs-lookup"><span data-stu-id="c1869-104">When deciding how to group applications into partitions, administrators need to be aware of certain rules and restrictions, including the following:</span></span>

-   <span data-ttu-id="c1869-105">Un'applicazione può essere installata in una o più partizioni.</span><span class="sxs-lookup"><span data-stu-id="c1869-105">An application can be installed into one or more partitions.</span></span>
-   <span data-ttu-id="c1869-106">In un'applicazione può esistere una sola istanza di un determinato componente.</span><span class="sxs-lookup"><span data-stu-id="c1869-106">Only one instance of a given component can exist in an application.</span></span>

## <a name="public-and-private-components"></a><span data-ttu-id="c1869-107">Componenti pubblici e privati</span><span class="sxs-lookup"><span data-stu-id="c1869-107">Public and Private Components</span></span>

<span data-ttu-id="c1869-108">Quando si decide come raggruppare le applicazioni COM+, esistono altre restrizioni.</span><span class="sxs-lookup"><span data-stu-id="c1869-108">Other restrictions exist when deciding how to group COM+ applications.</span></span> <span data-ttu-id="c1869-109">Queste restrizioni riguardano i componenti pubblici e privati all'interno di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c1869-109">These restrictions pertain to public versus private components within an application.</span></span> <span data-ttu-id="c1869-110">I componenti dell'applicazione possono in genere essere pubblici o privati.</span><span class="sxs-lookup"><span data-stu-id="c1869-110">Application components can generally be either public or private.</span></span> <span data-ttu-id="c1869-111">Tuttavia, quando si raggruppano le applicazioni in partizioni, gli amministratori devono tenere presente alcune restrizioni relative ai componenti pubblici e privati.</span><span class="sxs-lookup"><span data-stu-id="c1869-111">However, when grouping applications into partitions, administrators should be aware of some restrictions around public and private components.</span></span> <span data-ttu-id="c1869-112">Nella tabella seguente sono elencate queste restrizioni.</span><span class="sxs-lookup"><span data-stu-id="c1869-112">The following table lists these restrictions.</span></span>



| <span data-ttu-id="c1869-113">Se un'applicazione è:</span><span class="sxs-lookup"><span data-stu-id="c1869-113">If an application is:</span></span>              | <span data-ttu-id="c1869-114">I componenti di una partizione possono essere:</span><span class="sxs-lookup"><span data-stu-id="c1869-114">Then components in a partition can be:</span></span>                                                                                   |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1869-115">Un'applicazione server</span><span class="sxs-lookup"><span data-stu-id="c1869-115">A server application</span></span><br/>    | <span data-ttu-id="c1869-116">Public e private.</span><span class="sxs-lookup"><span data-stu-id="c1869-116">Public and private.</span></span><br/>                                                                                           |
| <span data-ttu-id="c1869-117">Un'applicazione di libreria</span><span class="sxs-lookup"><span data-stu-id="c1869-117">A library application</span></span><br/>   | <span data-ttu-id="c1869-118">Solo pubblico.</span><span class="sxs-lookup"><span data-stu-id="c1869-118">Public only.</span></span> <span data-ttu-id="c1869-119">In caso contrario, l'applicazione chiamanti potrebbe avere gli stessi componenti, che creerebbe ambiguità.</span><span class="sxs-lookup"><span data-stu-id="c1869-119">Otherwise, the callers application could have the same components, which would create ambiguity.</span></span><br/> |
| <span data-ttu-id="c1869-120">Nella partizione globale</span><span class="sxs-lookup"><span data-stu-id="c1869-120">In the global partition</span></span><br/> | <span data-ttu-id="c1869-121">Solo pubblico.</span><span class="sxs-lookup"><span data-stu-id="c1869-121">Public only.</span></span> <span data-ttu-id="c1869-122">Ciò garantisce la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="c1869-122">This ensures backward compatibility.</span></span><br/>                                                             |



 

## <a name="application-ids"></a><span data-ttu-id="c1869-123">ID applicazione</span><span class="sxs-lookup"><span data-stu-id="c1869-123">Application IDs</span></span>

<span data-ttu-id="c1869-124">Ogni applicazione COM+ installata in un computer dispone di un ID applicazione univoco.</span><span class="sxs-lookup"><span data-stu-id="c1869-124">Every COM+ application installed on a computer has a unique application ID.</span></span> <span data-ttu-id="c1869-125">Tuttavia, i nomi delle applicazioni devono essere univoci solo all'interno di una singola partizione e non sull'intero computer.</span><span class="sxs-lookup"><span data-stu-id="c1869-125">However, application names need only be unique within a single partition and not on the entire computer.</span></span>

<span data-ttu-id="c1869-126">La tabella seguente mostra cosa accade all'ID applicazione quando un'applicazione viene importata in una partizione o esportata da una partizione.</span><span class="sxs-lookup"><span data-stu-id="c1869-126">The following table shows what happens to the application ID when an application is imported into a partition or exported from a partition.</span></span>



| <span data-ttu-id="c1869-127">Se un'applicazione è:</span><span class="sxs-lookup"><span data-stu-id="c1869-127">If an application is:</span></span>                                              | <span data-ttu-id="c1869-128">Quindi l'ID applicazione:</span><span class="sxs-lookup"><span data-stu-id="c1869-128">Then the application ID:</span></span>                    |
|--------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="c1869-129">Importazione nella partizione globale</span><span class="sxs-lookup"><span data-stu-id="c1869-129">Imported to the global partition</span></span><br/>                        | <span data-ttu-id="c1869-130">Rimane invariato</span><span class="sxs-lookup"><span data-stu-id="c1869-130">Remains the same</span></span><br/>                 |
| <span data-ttu-id="c1869-131">Importazione in una partizione diversa dalla partizione globale</span><span class="sxs-lookup"><span data-stu-id="c1869-131">Imported to a partition other than the global partition</span></span><br/> | <span data-ttu-id="c1869-132">Modificato</span><span class="sxs-lookup"><span data-stu-id="c1869-132">Is changed</span></span><br/>                       |
| <span data-ttu-id="c1869-133">Esportato</span><span class="sxs-lookup"><span data-stu-id="c1869-133">Exported</span></span><br/>                                                | <span data-ttu-id="c1869-134">È incluso nel file esportato</span><span class="sxs-lookup"><span data-stu-id="c1869-134">Is included in the exported file</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="c1869-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c1869-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1869-136">Raccolta delle metriche della partizione</span><span class="sxs-lookup"><span data-stu-id="c1869-136">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="c1869-137">Configurazione della cache della partizione</span><span class="sxs-lookup"><span data-stu-id="c1869-137">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="c1869-138">Gestione delle partizioni locali</span><span class="sxs-lookup"><span data-stu-id="c1869-138">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="c1869-139">Gestione di partizioni all'interno Active Directory</span><span class="sxs-lookup"><span data-stu-id="c1869-139">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> <dt>

[<span data-ttu-id="c1869-140">Impostazione dei diritti amministrativi per una partizione</span><span class="sxs-lookup"><span data-stu-id="c1869-140">Setting Administrative Rights for a Partition</span></span>](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




