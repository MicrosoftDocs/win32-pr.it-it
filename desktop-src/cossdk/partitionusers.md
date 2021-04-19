---
description: Contiene un oggetto per ogni utente della partizione.
ms.assetid: baec56ae-be8a-42a7-90bc-1db7c5cd7fe2
title: Raccolta PartitionUsers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PartitionUsers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1521642879037938451decd873a9aa14211ce296
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305134"
---
# <a name="partitionusers-collection"></a><span data-ttu-id="498e3-103">Raccolta PartitionUsers</span><span class="sxs-lookup"><span data-stu-id="498e3-103">PartitionUsers collection</span></span>

<span data-ttu-id="498e3-104">Contiene un oggetto per ogni utente della partizione.</span><span class="sxs-lookup"><span data-stu-id="498e3-104">Contains an object for each partition user.</span></span>

<span data-ttu-id="498e3-105">Questa raccolta supporta i metodi [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) dell'oggetto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="498e3-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="498e3-106">Membri</span><span class="sxs-lookup"><span data-stu-id="498e3-106">Members</span></span>

<span data-ttu-id="498e3-107">La raccolta **PartitionUsers** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="498e3-107">The **PartitionUsers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="498e3-108">Raccolte correlate</span><span class="sxs-lookup"><span data-stu-id="498e3-108">Related Collections</span></span>

<span data-ttu-id="498e3-109">È possibile passare da questa raccolta a una delle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="498e3-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="498e3-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="498e3-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="498e3-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="498e3-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="498e3-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="498e3-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="498e3-113">È possibile passare a questa raccolta dalle raccolte seguenti:</span><span class="sxs-lookup"><span data-stu-id="498e3-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="498e3-114">**Radice**</span><span class="sxs-lookup"><span data-stu-id="498e3-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="498e3-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="498e3-115">Properties</span></span>

<span data-ttu-id="498e3-116">Le proprietà seguenti sono supportate dall'oggetto [**COMAdminCatalogObject**](comadmincatalogobject.md) all'interno della raccolta:</span><span class="sxs-lookup"><span data-stu-id="498e3-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="498e3-117">AccountName</span><span class="sxs-lookup"><span data-stu-id="498e3-117">AccountName</span></span>](#accountname)
-   [<span data-ttu-id="498e3-118">DefaultPartitionID</span><span class="sxs-lookup"><span data-stu-id="498e3-118">DefaultPartitionID</span></span>](#defaultpartitionid)

### <a name="accountname"></a><span data-ttu-id="498e3-119">AccountName</span><span class="sxs-lookup"><span data-stu-id="498e3-119">AccountName</span></span>



| <span data-ttu-id="498e3-120">Voce</span><span class="sxs-lookup"><span data-stu-id="498e3-120">Entry</span></span> | <span data-ttu-id="498e3-121">Valore</span><span class="sxs-lookup"><span data-stu-id="498e3-121">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="498e3-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="498e3-122">Description</span></span>    | <span data-ttu-id="498e3-123">Nome dell'account dell'utente della partizione.</span><span class="sxs-lookup"><span data-stu-id="498e3-123">Name of the partition user's account.</span></span> <span data-ttu-id="498e3-124">Questa proprietà viene restituita quando il metodo della proprietà [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) o [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) viene chiamato su un oggetto di questa raccolta.</span><span class="sxs-lookup"><span data-stu-id="498e3-124">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="498e3-125">Access</span><span class="sxs-lookup"><span data-stu-id="498e3-125">Access</span></span>         | <span data-ttu-id="498e3-126">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="498e3-126">WriteOnce</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="498e3-127">Type</span><span class="sxs-lookup"><span data-stu-id="498e3-127">Type</span></span>           | <span data-ttu-id="498e3-128">string</span><span class="sxs-lookup"><span data-stu-id="498e3-128">String</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="498e3-129">Predefinito</span><span class="sxs-lookup"><span data-stu-id="498e3-129">Default</span></span>        | <span data-ttu-id="498e3-130">"Nuovo utente"</span><span class="sxs-lookup"><span data-stu-id="498e3-130">"New User"</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="498e3-131">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="498e3-131">Minimum system</span></span> | <span data-ttu-id="498e3-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="498e3-132">Windows Server 2003</span></span>                                                                                                                                                                                          |



 

### <a name="defaultpartitionid"></a><span data-ttu-id="498e3-133">DefaultPartitionID</span><span class="sxs-lookup"><span data-stu-id="498e3-133">DefaultPartitionID</span></span>



| <span data-ttu-id="498e3-134">Voce</span><span class="sxs-lookup"><span data-stu-id="498e3-134">Entry</span></span> | <span data-ttu-id="498e3-135">Valore</span><span class="sxs-lookup"><span data-stu-id="498e3-135">Value</span></span> |
|----------------|--------------------------------------------------------------------|
| <span data-ttu-id="498e3-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="498e3-136">Description</span></span>    | <span data-ttu-id="498e3-137">Identificatore univoco globale per la partizione dell'applicazione di base.</span><span class="sxs-lookup"><span data-stu-id="498e3-137">The globally unique identifier for the base application partition.</span></span> |
| <span data-ttu-id="498e3-138">Access</span><span class="sxs-lookup"><span data-stu-id="498e3-138">Access</span></span>         | <span data-ttu-id="498e3-139">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="498e3-139">ReadWrite</span></span>                                                          |
| <span data-ttu-id="498e3-140">Type</span><span class="sxs-lookup"><span data-stu-id="498e3-140">Type</span></span>           | <span data-ttu-id="498e3-141">string</span><span class="sxs-lookup"><span data-stu-id="498e3-141">String</span></span>                                                             |
| <span data-ttu-id="498e3-142">Predefinito</span><span class="sxs-lookup"><span data-stu-id="498e3-142">Default</span></span>        | <span data-ttu-id="498e3-143">{41E90F3E-56C1-4633-81C3-6E8BAC8BDD70}</span><span class="sxs-lookup"><span data-stu-id="498e3-143">{41E90F3E-56C1-4633-81C3-6E8BAC8BDD70}</span></span>                             |
| <span data-ttu-id="498e3-144">Sistema minimo</span><span class="sxs-lookup"><span data-stu-id="498e3-144">Minimum system</span></span> | <span data-ttu-id="498e3-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="498e3-145">Windows Server 2003</span></span>                                                |



 

## <a name="see-also"></a><span data-ttu-id="498e3-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="498e3-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="498e3-147">Raccolte di amministrazione COM+</span><span class="sxs-lookup"><span data-stu-id="498e3-147">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
