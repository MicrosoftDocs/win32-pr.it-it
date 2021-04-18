---
description: Contiene un oggetto per ogni ruolo assegnato al metodo al quale è correlata la raccolta. I ruoli devono essere già assegnati a livello di applicazione.
ms.assetid: 3a086163-e367-4dd1-996b-821b3e1111b2
title: Raccolta RolesForMethod
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForMethod
api_type:
- COM
api_location: ''
ms.openlocfilehash: c73ba5f7a14a5efc6711a65f211cd036e1c2a14d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304939"
---
# <a name="rolesformethod-collection"></a><span data-ttu-id="fbbef-104">Raccolta RolesForMethod</span><span class="sxs-lookup"><span data-stu-id="fbbef-104">RolesForMethod collection</span></span>

<span data-ttu-id="fbbef-105">Contiene un oggetto per ogni ruolo assegnato al metodo al quale è correlata la raccolta.</span><span class="sxs-lookup"><span data-stu-id="fbbef-105">Contains an object for each role assigned to the method to which the collection is related.</span></span> <span data-ttu-id="fbbef-106">I ruoli devono essere già assegnati a livello di applicazione.</span><span class="sxs-lookup"><span data-stu-id="fbbef-106">The roles must already be assigned at the application level.</span></span>

<span data-ttu-id="fbbef-107">Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="fbbef-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="fbbef-108">Membri</span><span class="sxs-lookup"><span data-stu-id="fbbef-108">Members</span></span>

<span data-ttu-id="fbbef-109">La raccolta **RolesForMethod** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="fbbef-109">The **RolesForMethod** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="fbbef-110">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="fbbef-110">Related Collections</span></span>

<span data-ttu-id="fbbef-111">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="fbbef-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="fbbef-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="fbbef-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="fbbef-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="fbbef-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="fbbef-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="fbbef-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="fbbef-115">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="fbbef-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="fbbef-116">**MethodsForInterface**</span><span class="sxs-lookup"><span data-stu-id="fbbef-116">**MethodsForInterface**</span></span>](methodsforinterface.md)

## <a name="properties"></a><span data-ttu-id="fbbef-117">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fbbef-117">Properties</span></span>

<span data-ttu-id="fbbef-118">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="fbbef-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="fbbef-119">Nome</span><span class="sxs-lookup"><span data-stu-id="fbbef-119">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="fbbef-120">Nome</span><span class="sxs-lookup"><span data-stu-id="fbbef-120">Name</span></span>



| <span data-ttu-id="fbbef-121">Voce</span><span class="sxs-lookup"><span data-stu-id="fbbef-121">Entry</span></span> | <span data-ttu-id="fbbef-122">Valore</span><span class="sxs-lookup"><span data-stu-id="fbbef-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbbef-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fbbef-123">Description</span></span>    | <span data-ttu-id="fbbef-124">Nome del ruolo.</span><span class="sxs-lookup"><span data-stu-id="fbbef-124">The role name.</span></span> <span data-ttu-id="fbbef-125">Deve essere già un ruolo assegnato all'applicazione (visualizzato nella raccolta Roles).</span><span class="sxs-lookup"><span data-stu-id="fbbef-125">Must already be a role assigned to the application (appearing in the Roles collection).</span></span> <span data-ttu-id="fbbef-126">Gli spazi aggiuntivi all'inizio e alla fine della stringa vengono rimossi. Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="fbbef-126">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="fbbef-127">Access</span><span class="sxs-lookup"><span data-stu-id="fbbef-127">Access</span></span>         | <span data-ttu-id="fbbef-128">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="fbbef-128">WriteOnce</span></span>                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="fbbef-129">Type</span><span class="sxs-lookup"><span data-stu-id="fbbef-129">Type</span></span>           | <span data-ttu-id="fbbef-130">string</span><span class="sxs-lookup"><span data-stu-id="fbbef-130">String</span></span>                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="fbbef-131">Predefinito</span><span class="sxs-lookup"><span data-stu-id="fbbef-131">Default</span></span>        | <span data-ttu-id="fbbef-132">"Nuovo ruolo"</span><span class="sxs-lookup"><span data-stu-id="fbbef-132">"New Role"</span></span>                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="fbbef-133">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="fbbef-133">Minimum system</span></span> | <span data-ttu-id="fbbef-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fbbef-134">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="see-also"></a><span data-ttu-id="fbbef-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fbbef-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbbef-136">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="fbbef-136">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
