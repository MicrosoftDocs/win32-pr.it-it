---
description: Contiene un oggetto per ogni proprietà del Sottoscrittore per la raccolta SubscriptionsForComponent padre.
ms.assetid: 58c9edbd-1128-4b8c-bb5a-528c212aa6a7
title: Raccolta SubscriberProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriberProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7c7a563e3fd3e917812426e34debd87bfd534b46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877614"
---
# <a name="subscriberproperties-collection"></a><span data-ttu-id="07bab-103">Raccolta SubscriberProperties</span><span class="sxs-lookup"><span data-stu-id="07bab-103">SubscriberProperties collection</span></span>

<span data-ttu-id="07bab-104">Contiene un oggetto per ogni proprietà del Sottoscrittore per la raccolta [**SubscriptionsForComponent**](subscriptionsforcomponent.md) padre.</span><span class="sxs-lookup"><span data-stu-id="07bab-104">Contains an object for each subscriber property for the parent [**SubscriptionsForComponent**](subscriptionsforcomponent.md) collection.</span></span>

<span data-ttu-id="07bab-105">Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="07bab-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="07bab-106">Membri</span><span class="sxs-lookup"><span data-stu-id="07bab-106">Members</span></span>

<span data-ttu-id="07bab-107">La raccolta **SubscriberProperties** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="07bab-107">The **SubscriberProperties** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="07bab-108">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="07bab-108">Related Collections</span></span>

<span data-ttu-id="07bab-109">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="07bab-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="07bab-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="07bab-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="07bab-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="07bab-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="07bab-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="07bab-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="07bab-113">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="07bab-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="07bab-114">**SubscriptionsForComponent**</span><span class="sxs-lookup"><span data-stu-id="07bab-114">**SubscriptionsForComponent**</span></span>](subscriptionsforcomponent.md)

## <a name="properties"></a><span data-ttu-id="07bab-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="07bab-115">Properties</span></span>

<span data-ttu-id="07bab-116">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="07bab-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="07bab-117">Nome</span><span class="sxs-lookup"><span data-stu-id="07bab-117">Name</span></span>](#name)
-   [<span data-ttu-id="07bab-118">Valore</span><span class="sxs-lookup"><span data-stu-id="07bab-118">Value</span></span>](#value)

### <a name="name"></a><span data-ttu-id="07bab-119">Nome</span><span class="sxs-lookup"><span data-stu-id="07bab-119">Name</span></span>



| <span data-ttu-id="07bab-120">Voce</span><span class="sxs-lookup"><span data-stu-id="07bab-120">Entry</span></span> | <span data-ttu-id="07bab-121">Valore</span><span class="sxs-lookup"><span data-stu-id="07bab-121">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07bab-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07bab-122">Description</span></span>    | <span data-ttu-id="07bab-123">Nome della proprietà.</span><span class="sxs-lookup"><span data-stu-id="07bab-123">The name of the property.</span></span> <span data-ttu-id="07bab-124">Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono rimossi. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="07bab-124">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="07bab-125">Access</span><span class="sxs-lookup"><span data-stu-id="07bab-125">Access</span></span>         | <span data-ttu-id="07bab-126">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="07bab-126">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="07bab-127">Type</span><span class="sxs-lookup"><span data-stu-id="07bab-127">Type</span></span>           | <span data-ttu-id="07bab-128">string</span><span class="sxs-lookup"><span data-stu-id="07bab-128">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="07bab-129">Predefinito</span><span class="sxs-lookup"><span data-stu-id="07bab-129">Default</span></span>        | <span data-ttu-id="07bab-130">"Nuova proprietà"</span><span class="sxs-lookup"><span data-stu-id="07bab-130">"New Property"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="07bab-131">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="07bab-131">Minimum system</span></span> | <span data-ttu-id="07bab-132">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07bab-132">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="value"></a><span data-ttu-id="07bab-133">Valore</span><span class="sxs-lookup"><span data-stu-id="07bab-133">Value</span></span>



| <span data-ttu-id="07bab-134">Voce</span><span class="sxs-lookup"><span data-stu-id="07bab-134">Entry</span></span> | <span data-ttu-id="07bab-135">Valore</span><span class="sxs-lookup"><span data-stu-id="07bab-135">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="07bab-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07bab-136">Description</span></span>    | <span data-ttu-id="07bab-137">Valore per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="07bab-137">A value for the property.</span></span> |
| <span data-ttu-id="07bab-138">Access</span><span class="sxs-lookup"><span data-stu-id="07bab-138">Access</span></span>         | <span data-ttu-id="07bab-139">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="07bab-139">ReadWrite</span></span>                 |
| <span data-ttu-id="07bab-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="07bab-140">Type</span></span>           | <span data-ttu-id="07bab-141">Variant</span><span class="sxs-lookup"><span data-stu-id="07bab-141">Variant</span></span>                   |
| <span data-ttu-id="07bab-142">Predefinito</span><span class="sxs-lookup"><span data-stu-id="07bab-142">Default</span></span>        | <span data-ttu-id="07bab-143">N/D</span><span class="sxs-lookup"><span data-stu-id="07bab-143">N/A</span></span>                       |
| <span data-ttu-id="07bab-144">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="07bab-144">Minimum system</span></span> | <span data-ttu-id="07bab-145">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="07bab-145">Windows 2000</span></span>              |



 

## <a name="see-also"></a><span data-ttu-id="07bab-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07bab-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07bab-147">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="07bab-147">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
