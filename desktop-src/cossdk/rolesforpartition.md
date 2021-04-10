---
description: La raccolta RolesForPartition è sempre correlata a un oggetto nella raccolta di partizioni. Include un oggetto per ogni ruolo assegnato alla partizione a cui è correlato.
ms.assetid: 56985f55-d6e8-4066-b6d5-21c62d4278ce
title: Raccolta RolesForPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForPartition
api_type:
- COM
api_location: ''
ms.openlocfilehash: c97d524e3fc516086db3a815396d6d59f9369b31
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126333"
---
# <a name="rolesforpartition-collection"></a><span data-ttu-id="16de2-104">Raccolta RolesForPartition</span><span class="sxs-lookup"><span data-stu-id="16de2-104">RolesForPartition collection</span></span>

<span data-ttu-id="16de2-105">La raccolta **RolesForPartition** è sempre correlata a un oggetto nella raccolta di [**partizioni**](partitions.md) .</span><span class="sxs-lookup"><span data-stu-id="16de2-105">The **RolesForPartition** collection is always related to an object in the [**Partitions**](partitions.md) collection.</span></span> <span data-ttu-id="16de2-106">Include un oggetto per ogni ruolo assegnato alla partizione a cui è correlato.</span><span class="sxs-lookup"><span data-stu-id="16de2-106">It holds an object for each role assigned to the partition to which it is related.</span></span>

<span data-ttu-id="16de2-107">Questa raccolta non supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="16de2-107">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="16de2-108">Membri</span><span class="sxs-lookup"><span data-stu-id="16de2-108">Members</span></span>

<span data-ttu-id="16de2-109">La raccolta **RolesForPartition** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="16de2-109">The **RolesForPartition** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="16de2-110">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="16de2-110">Related Collections</span></span>

<span data-ttu-id="16de2-111">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="16de2-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="16de2-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="16de2-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="16de2-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="16de2-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="16de2-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="16de2-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="16de2-115">**UsersInPartitionRole**</span><span class="sxs-lookup"><span data-stu-id="16de2-115">**UsersInPartitionRole**</span></span>](usersinpartitionrole.md)

<span data-ttu-id="16de2-116">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="16de2-116">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="16de2-117">**Partizioni**</span><span class="sxs-lookup"><span data-stu-id="16de2-117">**Partitions**</span></span>](partitions.md)

## <a name="properties"></a><span data-ttu-id="16de2-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="16de2-118">Properties</span></span>

<span data-ttu-id="16de2-119">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="16de2-119">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="16de2-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16de2-120">Description</span></span>](#description)
-   [<span data-ttu-id="16de2-121">Nome</span><span class="sxs-lookup"><span data-stu-id="16de2-121">Name</span></span>](#name)

### <a name="description"></a><span data-ttu-id="16de2-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16de2-122">Description</span></span>



| <span data-ttu-id="16de2-123">Voce</span><span class="sxs-lookup"><span data-stu-id="16de2-123">Entry</span></span> | <span data-ttu-id="16de2-124">Valore</span><span class="sxs-lookup"><span data-stu-id="16de2-124">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="16de2-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16de2-125">Description</span></span>    | <span data-ttu-id="16de2-126">Descrizione del ruolo.</span><span class="sxs-lookup"><span data-stu-id="16de2-126">A description of the role.</span></span> |
| <span data-ttu-id="16de2-127">Access</span><span class="sxs-lookup"><span data-stu-id="16de2-127">Access</span></span>         | <span data-ttu-id="16de2-128">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="16de2-128">ReadOnly</span></span>                   |
| <span data-ttu-id="16de2-129">Type</span><span class="sxs-lookup"><span data-stu-id="16de2-129">Type</span></span>           | <span data-ttu-id="16de2-130">string</span><span class="sxs-lookup"><span data-stu-id="16de2-130">String</span></span>                     |
| <span data-ttu-id="16de2-131">Predefinito</span><span class="sxs-lookup"><span data-stu-id="16de2-131">Default</span></span>        | <span data-ttu-id="16de2-132">""</span><span class="sxs-lookup"><span data-stu-id="16de2-132">""</span></span>                         |
| <span data-ttu-id="16de2-133">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="16de2-133">Minimum system</span></span> | <span data-ttu-id="16de2-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="16de2-134">Windows Server 2003</span></span>        |



 

### <a name="name"></a><span data-ttu-id="16de2-135">Nome</span><span class="sxs-lookup"><span data-stu-id="16de2-135">Name</span></span>



| <span data-ttu-id="16de2-136">Voce</span><span class="sxs-lookup"><span data-stu-id="16de2-136">Entry</span></span> | <span data-ttu-id="16de2-137">Valore</span><span class="sxs-lookup"><span data-stu-id="16de2-137">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16de2-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16de2-138">Description</span></span>    | <span data-ttu-id="16de2-139">Nome del ruolo.</span><span class="sxs-lookup"><span data-stu-id="16de2-139">The role name.</span></span> <span data-ttu-id="16de2-140">Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono rimossi. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="16de2-140">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="16de2-141">Access</span><span class="sxs-lookup"><span data-stu-id="16de2-141">Access</span></span>         | <span data-ttu-id="16de2-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="16de2-142">ReadOnly</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="16de2-143">Type</span><span class="sxs-lookup"><span data-stu-id="16de2-143">Type</span></span>           | <span data-ttu-id="16de2-144">string</span><span class="sxs-lookup"><span data-stu-id="16de2-144">String</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="16de2-145">Predefinito</span><span class="sxs-lookup"><span data-stu-id="16de2-145">Default</span></span>        | <span data-ttu-id="16de2-146">""</span><span class="sxs-lookup"><span data-stu-id="16de2-146">""</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="16de2-147">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="16de2-147">Minimum system</span></span> | <span data-ttu-id="16de2-148">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="16de2-148">Windows Server 2003</span></span>                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a><span data-ttu-id="16de2-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="16de2-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16de2-150">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="16de2-150">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
