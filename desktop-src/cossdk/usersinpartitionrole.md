---
description: Contiene un oggetto per ogni utente nel ruolo a cui è correlata la raccolta.
ms.assetid: c6aebf7a-04d1-4c7c-a015-bc6fb4841c4a
title: Raccolta UsersInPartitionRole
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UsersInPartitionRole
api_type:
- COM
api_location: ''
ms.openlocfilehash: fce1577636a7b2e678bdade9c32f706c7ccbf158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127007"
---
# <a name="usersinpartitionrole-collection"></a><span data-ttu-id="5489c-103">Raccolta UsersInPartitionRole</span><span class="sxs-lookup"><span data-stu-id="5489c-103">UsersInPartitionRole collection</span></span>

<span data-ttu-id="5489c-104">Contiene un oggetto per ogni utente nel ruolo a cui è correlata la raccolta.</span><span class="sxs-lookup"><span data-stu-id="5489c-104">Contains an object for each user in the role to which the collection is related.</span></span>

<span data-ttu-id="5489c-105">Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="5489c-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="5489c-106">Membri</span><span class="sxs-lookup"><span data-stu-id="5489c-106">Members</span></span>

<span data-ttu-id="5489c-107">La raccolta **UsersInPartitionRole** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="5489c-107">The **UsersInPartitionRole** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="5489c-108">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="5489c-108">Related Collections</span></span>

<span data-ttu-id="5489c-109">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="5489c-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="5489c-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="5489c-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="5489c-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="5489c-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="5489c-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="5489c-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="5489c-113">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="5489c-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="5489c-114">**RolesForPartition**</span><span class="sxs-lookup"><span data-stu-id="5489c-114">**RolesForPartition**</span></span>](rolesforpartition.md)

## <a name="properties"></a><span data-ttu-id="5489c-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5489c-115">Properties</span></span>

<span data-ttu-id="5489c-116">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="5489c-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="5489c-117">Utente</span><span class="sxs-lookup"><span data-stu-id="5489c-117">User</span></span>](#usersinpartitionrole-collection)

### <a name="user"></a><span data-ttu-id="5489c-118">User</span><span class="sxs-lookup"><span data-stu-id="5489c-118">User</span></span>



| <span data-ttu-id="5489c-119">Voce</span><span class="sxs-lookup"><span data-stu-id="5489c-119">Entry</span></span> | <span data-ttu-id="5489c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="5489c-120">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5489c-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5489c-121">Description</span></span>    | <span data-ttu-id="5489c-122">Nome utente.</span><span class="sxs-lookup"><span data-stu-id="5489c-122">The user name.</span></span> <span data-ttu-id="5489c-123">Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="5489c-123">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="5489c-124">Access</span><span class="sxs-lookup"><span data-stu-id="5489c-124">Access</span></span>         | <span data-ttu-id="5489c-125">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="5489c-125">WriteOnce</span></span>                                                                                                                                                                             |
| <span data-ttu-id="5489c-126">Type</span><span class="sxs-lookup"><span data-stu-id="5489c-126">Type</span></span>           | <span data-ttu-id="5489c-127">string</span><span class="sxs-lookup"><span data-stu-id="5489c-127">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="5489c-128">Predefinito</span><span class="sxs-lookup"><span data-stu-id="5489c-128">Default</span></span>        | <span data-ttu-id="5489c-129">"Nuovo utente"</span><span class="sxs-lookup"><span data-stu-id="5489c-129">"New User"</span></span>                                                                                                                                                                            |
| <span data-ttu-id="5489c-130">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="5489c-130">Minimum system</span></span> | <span data-ttu-id="5489c-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5489c-131">Windows Server 2003</span></span>                                                                                                                                                                   |



 

## <a name="see-also"></a><span data-ttu-id="5489c-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5489c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5489c-133">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="5489c-133">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
