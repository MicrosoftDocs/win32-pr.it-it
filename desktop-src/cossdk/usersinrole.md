---
description: Contiene un oggetto per ogni utente nel ruolo a cui è correlata la raccolta.
ms.assetid: e7d9e5e8-1927-42b2-bdd5-0c49a562c31f
title: Raccolta UsersInRole
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UsersInRole
api_type:
- COM
api_location: ''
ms.openlocfilehash: e5bf36937d08efd377b48ef251ffb7219c05504f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225696"
---
# <a name="usersinrole-collection"></a><span data-ttu-id="1cb48-103">Raccolta UsersInRole</span><span class="sxs-lookup"><span data-stu-id="1cb48-103">UsersInRole collection</span></span>

<span data-ttu-id="1cb48-104">Contiene un oggetto per ogni utente nel ruolo a cui è correlata la raccolta.</span><span class="sxs-lookup"><span data-stu-id="1cb48-104">Contains an object for each user in the role to which the collection is related.</span></span>

<span data-ttu-id="1cb48-105">Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="1cb48-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="1cb48-106">Membri</span><span class="sxs-lookup"><span data-stu-id="1cb48-106">Members</span></span>

<span data-ttu-id="1cb48-107">La raccolta **UsersInRole** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="1cb48-107">The **UsersInRole** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="1cb48-108">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="1cb48-108">Related Collections</span></span>

<span data-ttu-id="1cb48-109">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="1cb48-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="1cb48-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="1cb48-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="1cb48-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="1cb48-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="1cb48-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="1cb48-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="1cb48-113">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="1cb48-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="1cb48-114">**Ruoli**</span><span class="sxs-lookup"><span data-stu-id="1cb48-114">**Roles**</span></span>](roles.md)

## <a name="properties"></a><span data-ttu-id="1cb48-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="1cb48-115">Properties</span></span>

<span data-ttu-id="1cb48-116">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="1cb48-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="1cb48-117">Utente</span><span class="sxs-lookup"><span data-stu-id="1cb48-117">User</span></span>](#usersinrole-collection)

### <a name="user"></a><span data-ttu-id="1cb48-118">User</span><span class="sxs-lookup"><span data-stu-id="1cb48-118">User</span></span>



| <span data-ttu-id="1cb48-119">Voce</span><span class="sxs-lookup"><span data-stu-id="1cb48-119">Entry</span></span> | <span data-ttu-id="1cb48-120">Valore</span><span class="sxs-lookup"><span data-stu-id="1cb48-120">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cb48-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1cb48-121">Description</span></span>    | <span data-ttu-id="1cb48-122">Nome utente.</span><span class="sxs-lookup"><span data-stu-id="1cb48-122">The user name.</span></span> <span data-ttu-id="1cb48-123">Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="1cb48-123">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="1cb48-124">Access</span><span class="sxs-lookup"><span data-stu-id="1cb48-124">Access</span></span>         | <span data-ttu-id="1cb48-125">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="1cb48-125">WriteOnce</span></span>                                                                                                                                                                             |
| <span data-ttu-id="1cb48-126">Type</span><span class="sxs-lookup"><span data-stu-id="1cb48-126">Type</span></span>           | <span data-ttu-id="1cb48-127">string</span><span class="sxs-lookup"><span data-stu-id="1cb48-127">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="1cb48-128">Predefinito</span><span class="sxs-lookup"><span data-stu-id="1cb48-128">Default</span></span>        | <span data-ttu-id="1cb48-129">"Nuovo utente"</span><span class="sxs-lookup"><span data-stu-id="1cb48-129">"New User"</span></span>                                                                                                                                                                            |
| <span data-ttu-id="1cb48-130">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="1cb48-130">Minimum system</span></span> | <span data-ttu-id="1cb48-131">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="1cb48-131">Windows 2000</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="1cb48-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1cb48-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cb48-133">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="1cb48-133">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
