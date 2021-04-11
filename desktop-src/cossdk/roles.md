---
description: La raccolta Roles è sempre correlata a un oggetto nella raccolta Applications. Include un oggetto per ogni ruolo assegnato all'applicazione a cui è correlato.
ms.assetid: 87f39c2a-ad66-4390-9220-06751dcebd95
title: Raccolta Roles
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Roles
api_type:
- COM
api_location: ''
ms.openlocfilehash: f676a53f5fe54e42ca2a489ad834b9c91e4e0ef5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225756"
---
# <a name="roles-collection"></a><span data-ttu-id="7350e-104">Raccolta Roles</span><span class="sxs-lookup"><span data-stu-id="7350e-104">Roles collection</span></span>

<span data-ttu-id="7350e-105">La raccolta **roles** è sempre correlata a un oggetto nella raccolta [**Applications**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="7350e-105">The **Roles** collection is always related to an object in the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="7350e-106">Include un oggetto per ogni ruolo assegnato all'applicazione a cui è correlato.</span><span class="sxs-lookup"><span data-stu-id="7350e-106">It holds an object for each role assigned to the application to which it is related.</span></span>

<span data-ttu-id="7350e-107">Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="7350e-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="7350e-108">Membri</span><span class="sxs-lookup"><span data-stu-id="7350e-108">Members</span></span>

<span data-ttu-id="7350e-109">La raccolta **roles** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="7350e-109">The **Roles** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="7350e-110">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="7350e-110">Related Collections</span></span>

<span data-ttu-id="7350e-111">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="7350e-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="7350e-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="7350e-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="7350e-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="7350e-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="7350e-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="7350e-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="7350e-115">**UsersInRole**</span><span class="sxs-lookup"><span data-stu-id="7350e-115">**UsersInRole**</span></span>](usersinrole.md)

<span data-ttu-id="7350e-116">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="7350e-116">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="7350e-117">**Applicazioni**</span><span class="sxs-lookup"><span data-stu-id="7350e-117">**Applications**</span></span>](applications.md)

## <a name="properties"></a><span data-ttu-id="7350e-118">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7350e-118">Properties</span></span>

<span data-ttu-id="7350e-119">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="7350e-119">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="7350e-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7350e-120">Description</span></span>](#description)
-   [<span data-ttu-id="7350e-121">Nome</span><span class="sxs-lookup"><span data-stu-id="7350e-121">Name</span></span>](#name)

### <a name="description"></a><span data-ttu-id="7350e-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7350e-122">Description</span></span>



| <span data-ttu-id="7350e-123">Voce</span><span class="sxs-lookup"><span data-stu-id="7350e-123">Entry</span></span> | <span data-ttu-id="7350e-124">Valore</span><span class="sxs-lookup"><span data-stu-id="7350e-124">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="7350e-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7350e-125">Description</span></span>    | <span data-ttu-id="7350e-126">Descrizione del ruolo.</span><span class="sxs-lookup"><span data-stu-id="7350e-126">A description of the role.</span></span> |
| <span data-ttu-id="7350e-127">Access</span><span class="sxs-lookup"><span data-stu-id="7350e-127">Access</span></span>         | <span data-ttu-id="7350e-128">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7350e-128">ReadWrite</span></span>                  |
| <span data-ttu-id="7350e-129">Type</span><span class="sxs-lookup"><span data-stu-id="7350e-129">Type</span></span>           | <span data-ttu-id="7350e-130">string</span><span class="sxs-lookup"><span data-stu-id="7350e-130">String</span></span>                     |
| <span data-ttu-id="7350e-131">Predefinito</span><span class="sxs-lookup"><span data-stu-id="7350e-131">Default</span></span>        | <span data-ttu-id="7350e-132">""</span><span class="sxs-lookup"><span data-stu-id="7350e-132">""</span></span>                         |
| <span data-ttu-id="7350e-133">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="7350e-133">Minimum system</span></span> | <span data-ttu-id="7350e-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7350e-134">Windows 2000</span></span>               |



 

### <a name="name"></a><span data-ttu-id="7350e-135">Nome</span><span class="sxs-lookup"><span data-stu-id="7350e-135">Name</span></span>



| <span data-ttu-id="7350e-136">Voce</span><span class="sxs-lookup"><span data-stu-id="7350e-136">Entry</span></span> | <span data-ttu-id="7350e-137">Valore</span><span class="sxs-lookup"><span data-stu-id="7350e-137">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7350e-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7350e-138">Description</span></span>    | <span data-ttu-id="7350e-139">Nome del ruolo.</span><span class="sxs-lookup"><span data-stu-id="7350e-139">The role name.</span></span> <span data-ttu-id="7350e-140">Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono rimossi. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="7350e-140">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="7350e-141">Access</span><span class="sxs-lookup"><span data-stu-id="7350e-141">Access</span></span>         | <span data-ttu-id="7350e-142">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="7350e-142">WriteOnce</span></span>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="7350e-143">Type</span><span class="sxs-lookup"><span data-stu-id="7350e-143">Type</span></span>           | <span data-ttu-id="7350e-144">string</span><span class="sxs-lookup"><span data-stu-id="7350e-144">String</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="7350e-145">Predefinito</span><span class="sxs-lookup"><span data-stu-id="7350e-145">Default</span></span>        | <span data-ttu-id="7350e-146">"Nuovo ruolo"</span><span class="sxs-lookup"><span data-stu-id="7350e-146">"New Role"</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="7350e-147">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="7350e-147">Minimum system</span></span> | <span data-ttu-id="7350e-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7350e-148">Windows 2000</span></span>                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a><span data-ttu-id="7350e-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7350e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7350e-150">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="7350e-150">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
