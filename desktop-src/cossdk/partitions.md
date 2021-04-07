---
description: Specifica le applicazioni contenute all'interno di ogni partizione.
ms.assetid: 264a35fd-ba71-4ae9-908a-24a72167c26b
title: Raccolta partizioni
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Partitions
api_type:
- COM
api_location: ''
ms.openlocfilehash: b1016ae932d6841a5db590f2d24496113d3cefc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749079"
---
# <a name="partitions-collection"></a><span data-ttu-id="4295f-103">Raccolta partizioni</span><span class="sxs-lookup"><span data-stu-id="4295f-103">Partitions collection</span></span>

<span data-ttu-id="4295f-104">Specifica le applicazioni contenute all'interno di ogni partizione.</span><span class="sxs-lookup"><span data-stu-id="4295f-104">Specifies the applications contained within each partition.</span></span>

<span data-ttu-id="4295f-105">Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="4295f-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="4295f-106">Membri</span><span class="sxs-lookup"><span data-stu-id="4295f-106">Members</span></span>

<span data-ttu-id="4295f-107">La raccolta di **partizioni** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="4295f-107">The **Partitions** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="4295f-108">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="4295f-108">Related Collections</span></span>

<span data-ttu-id="4295f-109">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="4295f-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="4295f-110">**Applicazioni**</span><span class="sxs-lookup"><span data-stu-id="4295f-110">**Applications**</span></span>](applications.md)
-   [<span data-ttu-id="4295f-111">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="4295f-111">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="4295f-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="4295f-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="4295f-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="4295f-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="4295f-114">**RolesForPartition**</span><span class="sxs-lookup"><span data-stu-id="4295f-114">**RolesForPartition**</span></span>](rolesforpartition.md)

<span data-ttu-id="4295f-115">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="4295f-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="4295f-116">**Radice**</span><span class="sxs-lookup"><span data-stu-id="4295f-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="4295f-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4295f-117">Properties</span></span>

<span data-ttu-id="4295f-118">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="4295f-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="4295f-119">Modificabili</span><span class="sxs-lookup"><span data-stu-id="4295f-119">Changeable</span></span>](#changeable)
-   [<span data-ttu-id="4295f-120">Cancellabile</span><span class="sxs-lookup"><span data-stu-id="4295f-120">Deleteable</span></span>](#deleteable)
-   [<span data-ttu-id="4295f-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4295f-121">Description</span></span>](#description)
-   [<span data-ttu-id="4295f-122">ID</span><span class="sxs-lookup"><span data-stu-id="4295f-122">ID</span></span>](#partitions-collection)
-   [<span data-ttu-id="4295f-123">Nome</span><span class="sxs-lookup"><span data-stu-id="4295f-123">Name</span></span>](#name)

### <a name="changeable"></a><span data-ttu-id="4295f-124">Modificabili</span><span class="sxs-lookup"><span data-stu-id="4295f-124">Changeable</span></span>



| <span data-ttu-id="4295f-125">Voce</span><span class="sxs-lookup"><span data-stu-id="4295f-125">Entry</span></span> | <span data-ttu-id="4295f-126">Valore</span><span class="sxs-lookup"><span data-stu-id="4295f-126">Value</span></span> |
|----------------|--------------------------------------------------|
| <span data-ttu-id="4295f-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4295f-127">Description</span></span>    | <span data-ttu-id="4295f-128">Determina se la partizione può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="4295f-128">Determines whether this partition is changeable.</span></span> |
| <span data-ttu-id="4295f-129">Access</span><span class="sxs-lookup"><span data-stu-id="4295f-129">Access</span></span>         | <span data-ttu-id="4295f-130">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4295f-130">ReadWrite</span></span>                                        |
| <span data-ttu-id="4295f-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="4295f-131">Type</span></span>           | <span data-ttu-id="4295f-132">Bool</span><span class="sxs-lookup"><span data-stu-id="4295f-132">Bool</span></span>                                             |
| <span data-ttu-id="4295f-133">Predefinito</span><span class="sxs-lookup"><span data-stu-id="4295f-133">Default</span></span>        | <span data-ttu-id="4295f-134">Vero</span><span class="sxs-lookup"><span data-stu-id="4295f-134">True</span></span>                                             |
| <span data-ttu-id="4295f-135">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="4295f-135">Minimum system</span></span> | <span data-ttu-id="4295f-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4295f-136">Windows Server 2003</span></span>                              |



 

### <a name="deleteable"></a><span data-ttu-id="4295f-137">Cancellabile</span><span class="sxs-lookup"><span data-stu-id="4295f-137">Deleteable</span></span>



| <span data-ttu-id="4295f-138">Voce</span><span class="sxs-lookup"><span data-stu-id="4295f-138">Entry</span></span> | <span data-ttu-id="4295f-139">Valore</span><span class="sxs-lookup"><span data-stu-id="4295f-139">Value</span></span> |
|----------------|---------------------------------------------------|
| <span data-ttu-id="4295f-140">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4295f-140">Description</span></span>    | <span data-ttu-id="4295f-141">Determina se la partizione può essere eliminata.</span><span class="sxs-lookup"><span data-stu-id="4295f-141">Determines whether this partition can be deleted.</span></span> |
| <span data-ttu-id="4295f-142">Access</span><span class="sxs-lookup"><span data-stu-id="4295f-142">Access</span></span>         | <span data-ttu-id="4295f-143">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4295f-143">ReadWrite</span></span>                                         |
| <span data-ttu-id="4295f-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="4295f-144">Type</span></span>           | <span data-ttu-id="4295f-145">Bool</span><span class="sxs-lookup"><span data-stu-id="4295f-145">Bool</span></span>                                              |
| <span data-ttu-id="4295f-146">Predefinito</span><span class="sxs-lookup"><span data-stu-id="4295f-146">Default</span></span>        | <span data-ttu-id="4295f-147">Vero</span><span class="sxs-lookup"><span data-stu-id="4295f-147">True</span></span>                                              |
| <span data-ttu-id="4295f-148">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="4295f-148">Minimum system</span></span> | <span data-ttu-id="4295f-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4295f-149">Windows Server 2003</span></span>                               |



 

### <a name="description"></a><span data-ttu-id="4295f-150">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4295f-150">Description</span></span>



| <span data-ttu-id="4295f-151">Voce</span><span class="sxs-lookup"><span data-stu-id="4295f-151">Entry</span></span> | <span data-ttu-id="4295f-152">Valore</span><span class="sxs-lookup"><span data-stu-id="4295f-152">Value</span></span> |
|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="4295f-153">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4295f-153">Description</span></span>    | <span data-ttu-id="4295f-154">Questa proprietà rappresenta la descrizione che identifica la partizione.</span><span class="sxs-lookup"><span data-stu-id="4295f-154">This property represents the description identifying the partition.</span></span> |
| <span data-ttu-id="4295f-155">Access</span><span class="sxs-lookup"><span data-stu-id="4295f-155">Access</span></span>         | <span data-ttu-id="4295f-156">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4295f-156">ReadWrite</span></span>                                                           |
| <span data-ttu-id="4295f-157">Type</span><span class="sxs-lookup"><span data-stu-id="4295f-157">Type</span></span>           | <span data-ttu-id="4295f-158">string</span><span class="sxs-lookup"><span data-stu-id="4295f-158">String</span></span>                                                              |
| <span data-ttu-id="4295f-159">Predefinito</span><span class="sxs-lookup"><span data-stu-id="4295f-159">Default</span></span>        | <span data-ttu-id="4295f-160">""</span><span class="sxs-lookup"><span data-stu-id="4295f-160">""</span></span>                                                                  |
| <span data-ttu-id="4295f-161">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="4295f-161">Minimum system</span></span> | <span data-ttu-id="4295f-162">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4295f-162">Windows Server 2003</span></span>                                                 |



 

### <a name="id"></a><span data-ttu-id="4295f-163">ID</span><span class="sxs-lookup"><span data-stu-id="4295f-163">ID</span></span>



| <span data-ttu-id="4295f-164">Voce</span><span class="sxs-lookup"><span data-stu-id="4295f-164">Entry</span></span> | <span data-ttu-id="4295f-165">Valore</span><span class="sxs-lookup"><span data-stu-id="4295f-165">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4295f-166">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4295f-166">Description</span></span>    | <span data-ttu-id="4295f-167">GUID che rappresenta la partizione.</span><span class="sxs-lookup"><span data-stu-id="4295f-167">A GUID representing the partition.</span></span> <span data-ttu-id="4295f-168">Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="4295f-168">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="4295f-169">Access</span><span class="sxs-lookup"><span data-stu-id="4295f-169">Access</span></span>         | <span data-ttu-id="4295f-170">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="4295f-170">WriteOnce</span></span>                                                                                                                                                          |
| <span data-ttu-id="4295f-171">Type</span><span class="sxs-lookup"><span data-stu-id="4295f-171">Type</span></span>           | <span data-ttu-id="4295f-172">string</span><span class="sxs-lookup"><span data-stu-id="4295f-172">String</span></span>                                                                                                                                                             |
| <span data-ttu-id="4295f-173">Predefinito</span><span class="sxs-lookup"><span data-stu-id="4295f-173">Default</span></span>        | <Generated>                                                                                                                                                  |
| <span data-ttu-id="4295f-174">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="4295f-174">Minimum system</span></span> | <span data-ttu-id="4295f-175">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4295f-175">Windows Server 2003</span></span>                                                                                                                                                |



 

### <a name="name"></a><span data-ttu-id="4295f-176">Nome</span><span class="sxs-lookup"><span data-stu-id="4295f-176">Name</span></span>



| <span data-ttu-id="4295f-177">Voce</span><span class="sxs-lookup"><span data-stu-id="4295f-177">Entry</span></span> | <span data-ttu-id="4295f-178">Valore</span><span class="sxs-lookup"><span data-stu-id="4295f-178">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4295f-179">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4295f-179">Description</span></span>    | <span data-ttu-id="4295f-180">Rappresenta il nome della partizione.</span><span class="sxs-lookup"><span data-stu-id="4295f-180">Represents the partition name.</span></span> <span data-ttu-id="4295f-181">Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono rimossi. Questa proprietà viene restituita quando il metodo della proprietà [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="4295f-181">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="4295f-182">Access</span><span class="sxs-lookup"><span data-stu-id="4295f-182">Access</span></span>         | <span data-ttu-id="4295f-183">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4295f-183">ReadWrite</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="4295f-184">Type</span><span class="sxs-lookup"><span data-stu-id="4295f-184">Type</span></span>           | <span data-ttu-id="4295f-185">string</span><span class="sxs-lookup"><span data-stu-id="4295f-185">String</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="4295f-186">Predefinito</span><span class="sxs-lookup"><span data-stu-id="4295f-186">Default</span></span>        | <span data-ttu-id="4295f-187">"Nuova partizione"</span><span class="sxs-lookup"><span data-stu-id="4295f-187">"New Partition"</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="4295f-188">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="4295f-188">Minimum system</span></span> | <span data-ttu-id="4295f-189">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4295f-189">Windows Server 2003</span></span>                                                                                                                                                                                                                    |



 

## <a name="see-also"></a><span data-ttu-id="4295f-190">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4295f-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4295f-191">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="4295f-191">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
