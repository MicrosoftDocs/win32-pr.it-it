---
description: Contiene un oggetto per ogni proprietà del server di pubblicazione per la raccolta SubscriptionsForComponent padre.
ms.assetid: 7699c258-ca11-4652-b2f7-b2f2307c01fc
title: Raccolta PublisherProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublisherProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: bdab3e8143ea3d35d07adb5caa73639fcb568cd1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127015"
---
# <a name="publisherproperties-collection"></a><span data-ttu-id="4105d-103">Raccolta PublisherProperties</span><span class="sxs-lookup"><span data-stu-id="4105d-103">PublisherProperties collection</span></span>

<span data-ttu-id="4105d-104">Contiene un oggetto per ogni proprietà del server di pubblicazione per la raccolta [**SubscriptionsForComponent**](subscriptionsforcomponent.md) padre.</span><span class="sxs-lookup"><span data-stu-id="4105d-104">Contains an object for each publisher property for the parent [**SubscriptionsForComponent**](subscriptionsforcomponent.md) collection.</span></span>

<span data-ttu-id="4105d-105">Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="4105d-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="4105d-106">Membri</span><span class="sxs-lookup"><span data-stu-id="4105d-106">Members</span></span>

<span data-ttu-id="4105d-107">La raccolta **PublisherProperties** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="4105d-107">The **PublisherProperties** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="4105d-108">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="4105d-108">Related Collections</span></span>

<span data-ttu-id="4105d-109">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="4105d-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="4105d-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="4105d-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="4105d-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="4105d-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="4105d-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="4105d-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="4105d-113">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="4105d-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="4105d-114">**SubscriptionsForComponent**</span><span class="sxs-lookup"><span data-stu-id="4105d-114">**SubscriptionsForComponent**</span></span>](subscriptionsforcomponent.md)

## <a name="properties"></a><span data-ttu-id="4105d-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4105d-115">Properties</span></span>

<span data-ttu-id="4105d-116">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="4105d-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="4105d-117">Nome</span><span class="sxs-lookup"><span data-stu-id="4105d-117">Name</span></span>](#name)
-   [<span data-ttu-id="4105d-118">Valore</span><span class="sxs-lookup"><span data-stu-id="4105d-118">Value</span></span>](#value)

### <a name="name"></a><span data-ttu-id="4105d-119">Nome</span><span class="sxs-lookup"><span data-stu-id="4105d-119">Name</span></span>



| <span data-ttu-id="4105d-120">Voce</span><span class="sxs-lookup"><span data-stu-id="4105d-120">Entry</span></span> | <span data-ttu-id="4105d-121">Valore</span><span class="sxs-lookup"><span data-stu-id="4105d-121">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4105d-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4105d-122">Description</span></span>    | <span data-ttu-id="4105d-123">Nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="4105d-123">The name of the property.</span></span> <span data-ttu-id="4105d-124">Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono rimossi. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="4105d-124">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="4105d-125">Access</span><span class="sxs-lookup"><span data-stu-id="4105d-125">Access</span></span>         | <span data-ttu-id="4105d-126">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="4105d-126">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="4105d-127">Type</span><span class="sxs-lookup"><span data-stu-id="4105d-127">Type</span></span>           | <span data-ttu-id="4105d-128">string</span><span class="sxs-lookup"><span data-stu-id="4105d-128">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="4105d-129">Predefinito</span><span class="sxs-lookup"><span data-stu-id="4105d-129">Default</span></span>        | <span data-ttu-id="4105d-130">"Nuova proprietà"</span><span class="sxs-lookup"><span data-stu-id="4105d-130">"New Property"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="4105d-131">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="4105d-131">Minimum system</span></span> | <span data-ttu-id="4105d-132">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="4105d-132">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="value"></a><span data-ttu-id="4105d-133">Valore</span><span class="sxs-lookup"><span data-stu-id="4105d-133">Value</span></span>



| <span data-ttu-id="4105d-134">Voce</span><span class="sxs-lookup"><span data-stu-id="4105d-134">Entry</span></span> | <span data-ttu-id="4105d-135">Valore</span><span class="sxs-lookup"><span data-stu-id="4105d-135">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="4105d-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4105d-136">Description</span></span>    | <span data-ttu-id="4105d-137">Valore per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="4105d-137">A value for the property.</span></span> |
| <span data-ttu-id="4105d-138">Access</span><span class="sxs-lookup"><span data-stu-id="4105d-138">Access</span></span>         | <span data-ttu-id="4105d-139">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4105d-139">ReadWrite</span></span>                 |
| <span data-ttu-id="4105d-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="4105d-140">Type</span></span>           | <span data-ttu-id="4105d-141">Variant</span><span class="sxs-lookup"><span data-stu-id="4105d-141">Variant</span></span>                   |
| <span data-ttu-id="4105d-142">Predefinito</span><span class="sxs-lookup"><span data-stu-id="4105d-142">Default</span></span>        | <span data-ttu-id="4105d-143">N/D</span><span class="sxs-lookup"><span data-stu-id="4105d-143">N/A</span></span>                       |
| <span data-ttu-id="4105d-144">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="4105d-144">Minimum system</span></span> | <span data-ttu-id="4105d-145">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="4105d-145">Windows 2000</span></span>              |



 

## <a name="see-also"></a><span data-ttu-id="4105d-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4105d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4105d-147">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="4105d-147">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
