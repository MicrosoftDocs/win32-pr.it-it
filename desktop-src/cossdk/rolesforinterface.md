---
description: Contiene un oggetto per ogni ruolo assegnato all'interfaccia a cui è correlata la raccolta. I ruoli devono essere già assegnati a livello di applicazione.
ms.assetid: f5c1dc9a-13da-4504-a244-4ce8058240b8
title: Raccolta RolesForInterface
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 60c52e3cb48adc0ed52ef10bd9e0a73e716fabfc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304611"
---
# <a name="rolesforinterface-collection"></a><span data-ttu-id="d9b84-104">Raccolta RolesForInterface</span><span class="sxs-lookup"><span data-stu-id="d9b84-104">RolesForInterface collection</span></span>

<span data-ttu-id="d9b84-105">Contiene un oggetto per ogni ruolo assegnato all'interfaccia a cui è correlata la raccolta.</span><span class="sxs-lookup"><span data-stu-id="d9b84-105">Contains an object for each role assigned to the interface to which the collection is related.</span></span> <span data-ttu-id="d9b84-106">I ruoli devono essere già assegnati a livello di applicazione.</span><span class="sxs-lookup"><span data-stu-id="d9b84-106">The roles must already be assigned at the application level.</span></span>

<span data-ttu-id="d9b84-107">Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="d9b84-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="d9b84-108">Membri</span><span class="sxs-lookup"><span data-stu-id="d9b84-108">Members</span></span>

<span data-ttu-id="d9b84-109">La raccolta **RolesForInterface** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="d9b84-109">The **RolesForInterface** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="d9b84-110">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="d9b84-110">Related Collections</span></span>

<span data-ttu-id="d9b84-111">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="d9b84-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="d9b84-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="d9b84-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="d9b84-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="d9b84-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="d9b84-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="d9b84-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="d9b84-115">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="d9b84-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="d9b84-116">**InterfacesForComponent**</span><span class="sxs-lookup"><span data-stu-id="d9b84-116">**InterfacesForComponent**</span></span>](interfacesforcomponent.md)

## <a name="properties"></a><span data-ttu-id="d9b84-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="d9b84-117">Properties</span></span>

<span data-ttu-id="d9b84-118">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="d9b84-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="d9b84-119">Nome</span><span class="sxs-lookup"><span data-stu-id="d9b84-119">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="d9b84-120">Nome</span><span class="sxs-lookup"><span data-stu-id="d9b84-120">Name</span></span>



| <span data-ttu-id="d9b84-121">Voce</span><span class="sxs-lookup"><span data-stu-id="d9b84-121">Entry</span></span> | <span data-ttu-id="d9b84-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d9b84-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9b84-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9b84-123">Description</span></span>    | <span data-ttu-id="d9b84-124">Nome del ruolo.</span><span class="sxs-lookup"><span data-stu-id="d9b84-124">The role name.</span></span> <span data-ttu-id="d9b84-125">Deve essere già un ruolo assegnato all'applicazione (visualizzato nella raccolta Roles).</span><span class="sxs-lookup"><span data-stu-id="d9b84-125">Must already be a role assigned to the application (appearing in the Roles collection).</span></span> <span data-ttu-id="d9b84-126">Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono rimossi. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="d9b84-126">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="d9b84-127">Access</span><span class="sxs-lookup"><span data-stu-id="d9b84-127">Access</span></span>         | <span data-ttu-id="d9b84-128">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="d9b84-128">WriteOnce</span></span>                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="d9b84-129">Type</span><span class="sxs-lookup"><span data-stu-id="d9b84-129">Type</span></span>           | <span data-ttu-id="d9b84-130">string</span><span class="sxs-lookup"><span data-stu-id="d9b84-130">String</span></span>                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="d9b84-131">Predefinito</span><span class="sxs-lookup"><span data-stu-id="d9b84-131">Default</span></span>        | <span data-ttu-id="d9b84-132">"Nuovo ruolo"</span><span class="sxs-lookup"><span data-stu-id="d9b84-132">"New Role"</span></span>                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d9b84-133">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="d9b84-133">Minimum system</span></span> | <span data-ttu-id="d9b84-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d9b84-134">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="see-also"></a><span data-ttu-id="d9b84-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9b84-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9b84-136">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="d9b84-136">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
