---
description: VDS fornisce due oggetti helper, ovvero l'oggetto di enumerazione e l'oggetto asincrono. Questo argomento descrive ognuno di questi oggetti e fornisce collegamenti ad esempi di funzionamento dei chiamanti con ognuno di essi.
ms.assetid: 0f809c71-a3bd-4c62-8086-9651ea1a3400
title: Oggetti helper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5193003abd10d9fa2c311b250272d9ad5847a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234005"
---
# <a name="helper-objects"></a><span data-ttu-id="56012-104">Oggetti helper</span><span class="sxs-lookup"><span data-stu-id="56012-104">Helper Objects</span></span>

<span data-ttu-id="56012-105">\[A partire da Windows 8 e Windows Server 2012, l'interfaccia com del [servizio dischi virtuali](virtual-disk-service-portal.md) viene sostituita dall' [API di gestione archiviazione di Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="56012-105">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="56012-106">VDS fornisce due oggetti helper, ovvero l'oggetto di enumerazione e l'oggetto asincrono.</span><span class="sxs-lookup"><span data-stu-id="56012-106">VDS provides two helper objects: the enumeration object and the async object.</span></span> <span data-ttu-id="56012-107">Questo argomento descrive ognuno di questi oggetti e fornisce collegamenti ad esempi di funzionamento dei chiamanti con ognuno di essi.</span><span class="sxs-lookup"><span data-stu-id="56012-107">This topic describes each of these objects and provides links to examples of how callers work with each.</span></span>

## <a name="enumeration-object"></a><span data-ttu-id="56012-108">Enumerazione (oggetto)</span><span class="sxs-lookup"><span data-stu-id="56012-108">Enumeration Object</span></span>

<span data-ttu-id="56012-109">Un oggetto di enumerazione enumera un set di oggetti VDS di un tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="56012-109">An enumeration object enumerates through a set of VDS objects of a given type.</span></span> <span data-ttu-id="56012-110">Gli oggetti possono essere provider, sottosistemi, controller, lun, Plex di LUN, unità, dischi, dischi, volumi o Plex del volume.</span><span class="sxs-lookup"><span data-stu-id="56012-110">Objects can be providers, subsystems, controllers, LUNs, LUN plexes, drives, disk packs, disks, volumes, or volume plexes.</span></span> <span data-ttu-id="56012-111">I chiamanti possono ottenere un puntatore a un oggetto specifico selezionando l'oggetto desiderato dall'enumerazione restituita dal metodo appropriato.</span><span class="sxs-lookup"><span data-stu-id="56012-111">Callers can get a pointer to a specific object by selecting the desired object from the enumeration that is returned by the appropriate method.</span></span> <span data-ttu-id="56012-112">Per un esempio di codice, vedere [utilizzo di oggetti di enumerazione](working-with-enumeration-objects.md).</span><span class="sxs-lookup"><span data-stu-id="56012-112">For a code example, see [Working with Enumeration Objects](working-with-enumeration-objects.md).</span></span>

<span data-ttu-id="56012-113">Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.</span><span class="sxs-lookup"><span data-stu-id="56012-113">The following table lists related interfaces, enumerations, and structures.</span></span> 

| <span data-ttu-id="56012-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="56012-114">Type</span></span>                                              | <span data-ttu-id="56012-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="56012-115">Element</span></span>                                  |
|---------------------------------------------------|------------------------------------------|
| <span data-ttu-id="56012-116">Interfacce sempre esposte da questo oggetto</span><span class="sxs-lookup"><span data-stu-id="56012-116">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="56012-117">**IEnumVdsObject**</span><span class="sxs-lookup"><span data-stu-id="56012-117">**IEnumVdsObject**</span></span>](/windows/desktop/api/Vds/nn-vds-ienumvdsobject) |
| <span data-ttu-id="56012-118">Enumerazioni associate</span><span class="sxs-lookup"><span data-stu-id="56012-118">Associated enumerations</span></span>                           | <span data-ttu-id="56012-119">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="56012-119">None.</span></span>                                    |
| <span data-ttu-id="56012-120">Strutture associate</span><span class="sxs-lookup"><span data-stu-id="56012-120">Associated structures</span></span>                             | <span data-ttu-id="56012-121">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="56012-121">None.</span></span>                                    |



 

## <a name="async-object"></a><span data-ttu-id="56012-122">Oggetto asincrono</span><span class="sxs-lookup"><span data-stu-id="56012-122">Async Object</span></span>

<span data-ttu-id="56012-123">Un oggetto asincrono gestisce le operazioni asincrone.</span><span class="sxs-lookup"><span data-stu-id="56012-123">An async object manages asynchronous operations.</span></span> <span data-ttu-id="56012-124">I metodi che avviano operazioni asincrone restituiscono un puntatore a un'interfaccia [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) , che consente al chiamante di annullare, attendere ed eseguire query sullo stato dell'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="56012-124">Methods that initiate asynchronous operations return a pointer to an [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) interface, which allows the caller to cancel, wait for, and query the status of the asynchronous operation.</span></span>

<span data-ttu-id="56012-125">Le operazioni VDS con esecuzione prolungata tendono a essere implementate in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="56012-125">Long-running VDS operations tend to be implemented asynchronously.</span></span> <span data-ttu-id="56012-126">I programmi del provider software di base e dinamici implementano i metodi asincroni in modo coerente per le operazioni di volume, partizione e disco.</span><span class="sxs-lookup"><span data-stu-id="56012-126">The basic and dynamic software provider programs implement asynchronous methods consistently for volume, partition, and disk operations.</span></span> <span data-ttu-id="56012-127">I provider hardware implementano facoltativamente metodi correlati a Async in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="56012-127">Hardware providers optionally implement async-related methods asynchronously.</span></span> <span data-ttu-id="56012-128">Indipendentemente dal modo in cui il provider implementa il metodo, l'operazione deve restituire un puntatore a un'interfaccia [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) al chiamante.</span><span class="sxs-lookup"><span data-stu-id="56012-128">Regardless of how the provider implements the method, the operation must return a pointer to an [**IVdsAsync**](/windows/desktop/api/Vds/nn-vds-ivdsasync) interface to the caller.</span></span> <span data-ttu-id="56012-129">Per un esempio di codice, vedere [gestione delle operazioni asincrone](managing-asynchronous-operations.md).</span><span class="sxs-lookup"><span data-stu-id="56012-129">For a code example, see [Managing Asynchronous Operations](managing-asynchronous-operations.md).</span></span>

<span data-ttu-id="56012-130">Le operazioni asincrone includono:</span><span class="sxs-lookup"><span data-stu-id="56012-130">Asynchronous operations include:</span></span>

-   <span data-ttu-id="56012-131">Creazione di un LUN, un volume o una partizione.</span><span class="sxs-lookup"><span data-stu-id="56012-131">Creating a LUN, volume, or partition.</span></span>
-   <span data-ttu-id="56012-132">Formattazione di un volume o di una partizione.</span><span class="sxs-lookup"><span data-stu-id="56012-132">Formatting a volume or partition.</span></span>
-   <span data-ttu-id="56012-133">Aggiunta o rimozione di un LUN o un plex del volume.</span><span class="sxs-lookup"><span data-stu-id="56012-133">Adding or removing a LUN or volume plex.</span></span>
-   <span data-ttu-id="56012-134">Suddivisione di un volume Plex.</span><span class="sxs-lookup"><span data-stu-id="56012-134">Breaking a volume plex.</span></span>
-   <span data-ttu-id="56012-135">Estensione o compattazione di un LUN o un volume.</span><span class="sxs-lookup"><span data-stu-id="56012-135">Extending or shrinking a LUN or volume.</span></span>
-   <span data-ttu-id="56012-136">Ripristino di un LUN o un volume.</span><span class="sxs-lookup"><span data-stu-id="56012-136">Recovering a LUN or volume.</span></span>
-   <span data-ttu-id="56012-137">Pulizia di un disco.</span><span class="sxs-lookup"><span data-stu-id="56012-137">Cleaning a disk.</span></span>
-   <span data-ttu-id="56012-138">Sostituzione di un disco.</span><span class="sxs-lookup"><span data-stu-id="56012-138">Replacing a disk.</span></span>

<span data-ttu-id="56012-139">Nella tabella seguente sono elencate le interfacce, le enumerazioni e le strutture correlate.</span><span class="sxs-lookup"><span data-stu-id="56012-139">The following table lists related interfaces, enumerations, and structures.</span></span> 

| <span data-ttu-id="56012-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="56012-140">Type</span></span>                                              | <span data-ttu-id="56012-141">Elemento</span><span class="sxs-lookup"><span data-stu-id="56012-141">Element</span></span>                        |
|---------------------------------------------------|--------------------------------|
| <span data-ttu-id="56012-142">Interfacce sempre esposte da questo oggetto</span><span class="sxs-lookup"><span data-stu-id="56012-142">Interfaces that are always exposed by this object</span></span> | [<span data-ttu-id="56012-143">**IVdsAsync**</span><span class="sxs-lookup"><span data-stu-id="56012-143">**IVdsAsync**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsasync) |
| <span data-ttu-id="56012-144">Enumerazioni associate</span><span class="sxs-lookup"><span data-stu-id="56012-144">Associated enumerations</span></span>                           | <span data-ttu-id="56012-145">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="56012-145">None.</span></span>                          |
| <span data-ttu-id="56012-146">Strutture associate</span><span class="sxs-lookup"><span data-stu-id="56012-146">Associated structures</span></span>                             | <span data-ttu-id="56012-147">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="56012-147">None.</span></span>                          |



 

## <a name="related-topics"></a><span data-ttu-id="56012-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="56012-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56012-149">Modello a oggetti VDS</span><span class="sxs-lookup"><span data-stu-id="56012-149">VDS Object Model</span></span>](vds-object-model.md)
</dt> <dt>

[<span data-ttu-id="56012-150">**IVdsAsync**</span><span class="sxs-lookup"><span data-stu-id="56012-150">**IVdsAsync**</span></span>](/windows/desktop/api/Vds/nn-vds-ivdsasync)
</dt> <dt>

[<span data-ttu-id="56012-151">Utilizzo di oggetti di enumerazione</span><span class="sxs-lookup"><span data-stu-id="56012-151">Working with Enumeration Objects</span></span>](working-with-enumeration-objects.md)
</dt> <dt>

[<span data-ttu-id="56012-152">Gestione delle operazioni asincrone</span><span class="sxs-lookup"><span data-stu-id="56012-152">Managing Asynchronous Operations</span></span>](managing-asynchronous-operations.md)
</dt> </dl>

 

 
