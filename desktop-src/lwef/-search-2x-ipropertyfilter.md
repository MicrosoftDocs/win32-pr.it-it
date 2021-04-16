---
title: Interfaccia IPropertyFilter (WdsSharedIDL. h)
description: Espone le proprietà utilizzate per filtrare la query.
ms.assetid: 3760c413-931c-44f2-adaf-eb17df4015c3
keywords:
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IPropertyFilter
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IPropertyFilter, descritte
topic_type:
- apiref
api_name:
- IPropertyFilter
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4358ca7e111fd68beb68391ba7f08a9b8095d7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518310"
---
# <a name="ipropertyfilter-interface"></a><span data-ttu-id="80d15-105">Interfaccia IPropertyFilter</span><span class="sxs-lookup"><span data-stu-id="80d15-105">IPropertyFilter interface</span></span>

> [!NOTE]
> <span data-ttu-id="80d15-106">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="80d15-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="80d15-107">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="80d15-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="80d15-108">Espone le proprietà utilizzate per filtrare la query.</span><span class="sxs-lookup"><span data-stu-id="80d15-108">Exposes properties used to filter the query.</span></span>

## <a name="members"></a><span data-ttu-id="80d15-109">Membri</span><span class="sxs-lookup"><span data-stu-id="80d15-109">Members</span></span>

<span data-ttu-id="80d15-110">L'interfaccia **IPropertyFilter** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="80d15-110">The **IPropertyFilter** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="80d15-111">**IPropertyFilter** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="80d15-111">**IPropertyFilter** also has these types of members:</span></span>

-   [<span data-ttu-id="80d15-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="80d15-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80d15-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="80d15-113">Properties</span></span>

<span data-ttu-id="80d15-114">L'interfaccia **IPropertyFilter** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="80d15-114">The **IPropertyFilter** interface has these properties.</span></span>



| <span data-ttu-id="80d15-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="80d15-115">Property</span></span>                                                                                      | <span data-ttu-id="80d15-116">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="80d15-116">Access type</span></span>           | <span data-ttu-id="80d15-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80d15-117">Description</span></span>                                                   |
|:----------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="80d15-118">**IPropertyFilter:: IndexColumn**</span><span class="sxs-lookup"><span data-stu-id="80d15-118">**IPropertyFilter::IndexColumn**</span></span>](-search-2x-ipropertyfilter-indexcolumn.md)<br/>     | <span data-ttu-id="80d15-119">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="80d15-119">Read/write</span></span><br/> | <span data-ttu-id="80d15-120">Nome della colonna indicizzata della proprietà in base a cui filtrare.</span><span class="sxs-lookup"><span data-stu-id="80d15-120">Indexed column name of the property to filter by.</span></span> <br/> |
| [<span data-ttu-id="80d15-121">**IPropertyFilter::LogicOperator**</span><span class="sxs-lookup"><span data-stu-id="80d15-121">**IPropertyFilter::LogicOperator**</span></span>](-search-2x-ipropertyfilter-logicoperator.md)<br/> | <span data-ttu-id="80d15-122">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="80d15-122">Read/write</span></span><br/> | <span data-ttu-id="80d15-123">Operatore logico da usare quando si applica il filtro.</span><span class="sxs-lookup"><span data-stu-id="80d15-123">Logic Operator to use when applying filter.</span></span> <br/>       |
| [<span data-ttu-id="80d15-124">**IPropertyFilter::NestingDepth**</span><span class="sxs-lookup"><span data-stu-id="80d15-124">**IPropertyFilter::NestingDepth**</span></span>](-search-2x-ipropertyfilter-nestingdepth.md)<br/>   | <span data-ttu-id="80d15-125">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="80d15-125">Read/write</span></span><br/> | <span data-ttu-id="80d15-126">Filtra la profondità all'interno di un set annidato di parentesi.</span><span class="sxs-lookup"><span data-stu-id="80d15-126">Filters depth within a nested set of parentheses.</span></span> <br/> |
| [<span data-ttu-id="80d15-127">**IPropertyFilter:: Text**</span><span class="sxs-lookup"><span data-stu-id="80d15-127">**IPropertyFilter::Text**</span></span>](-search-2x-ipropertyfilter-text.md)<br/>                   | <span data-ttu-id="80d15-128">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="80d15-128">Read/write</span></span><br/> | <span data-ttu-id="80d15-129">Testo del filtro.</span><span class="sxs-lookup"><span data-stu-id="80d15-129">Text of the filter.</span></span> <br/>                               |
| [<span data-ttu-id="80d15-130">**IPropertyFilter:: UID**</span><span class="sxs-lookup"><span data-stu-id="80d15-130">**IPropertyFilter::UID**</span></span>](-search-2x-ipropertyfilter-uid.md)<br/>                     | <span data-ttu-id="80d15-131">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="80d15-131">Read/write</span></span><br/> | <span data-ttu-id="80d15-132">UID per la proprietà in base a cui filtrare.</span><span class="sxs-lookup"><span data-stu-id="80d15-132">UID fo the property to filter by.</span></span> <br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="80d15-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="80d15-133">Remarks</span></span>

<span data-ttu-id="80d15-134">Queste proprietà vengono utilizzate per filtrare la query.</span><span class="sxs-lookup"><span data-stu-id="80d15-134">These properties are used to filter the query.</span></span>

## <a name="requirements"></a><span data-ttu-id="80d15-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80d15-135">Requirements</span></span>



| <span data-ttu-id="80d15-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="80d15-136">Requirement</span></span> | <span data-ttu-id="80d15-137">Valore</span><span class="sxs-lookup"><span data-stu-id="80d15-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="80d15-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80d15-138">Minimum supported client</span></span><br/> | <span data-ttu-id="80d15-139">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="80d15-139">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="80d15-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80d15-140">Minimum supported server</span></span><br/> | <span data-ttu-id="80d15-141">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="80d15-141">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="80d15-142">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="80d15-142">Redistributable</span></span><br/>          | <span data-ttu-id="80d15-143">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="80d15-143">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="80d15-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="80d15-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="80d15-145"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="80d15-145"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

