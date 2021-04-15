---
title: Interfaccia IResultType (WdsSharedIDL. h)
description: Espone informazioni sul tipo di proprietà.
ms.assetid: 68abd470-2505-4836-a17f-f1c14157f8e7
keywords:
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultType
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultType, descritte
topic_type:
- apiref
api_name:
- IResultType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88451739a6ca2eb600838ea137ebc1ddba98f3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476127"
---
# <a name="iresulttype-interface"></a><span data-ttu-id="7b2d8-105">Interfaccia IResultType</span><span class="sxs-lookup"><span data-stu-id="7b2d8-105">IResultType interface</span></span>

> [!NOTE]
> <span data-ttu-id="7b2d8-106">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7b2d8-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="7b2d8-107">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="7b2d8-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="7b2d8-108">Espone informazioni sul tipo di proprietà.</span><span class="sxs-lookup"><span data-stu-id="7b2d8-108">Exposes property type information.</span></span>

## <a name="members"></a><span data-ttu-id="7b2d8-109">Membri</span><span class="sxs-lookup"><span data-stu-id="7b2d8-109">Members</span></span>

<span data-ttu-id="7b2d8-110">L'interfaccia **IResultType** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7b2d8-110">The **IResultType** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7b2d8-111">**IResultType** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7b2d8-111">**IResultType** also has these types of members:</span></span>

-   [<span data-ttu-id="7b2d8-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7b2d8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b2d8-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7b2d8-113">Properties</span></span>

<span data-ttu-id="7b2d8-114">L'interfaccia **IResultType** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="7b2d8-114">The **IResultType** interface has these properties.</span></span>



| <span data-ttu-id="7b2d8-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="7b2d8-115">Property</span></span>                                                                 | <span data-ttu-id="7b2d8-116">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="7b2d8-116">Access type</span></span>           | <span data-ttu-id="7b2d8-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b2d8-117">Description</span></span>                                                                           |
|:-------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b2d8-118">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="7b2d8-118">**DisplayName**</span></span>](-search-2x-iresulttype-displayname.md)<br/>     | <span data-ttu-id="7b2d8-119">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b2d8-119">Read-only</span></span><br/>  | <span data-ttu-id="7b2d8-120">Nome visualizzato localizzato del tipo:</span><span class="sxs-lookup"><span data-stu-id="7b2d8-120">Localized display name of the type:</span></span><br/>                                        |
| [<span data-ttu-id="7b2d8-121">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="7b2d8-121">**GetProperty**</span></span>](-search-2x-iresulttype-getproperty.md)<br/>     | <span data-ttu-id="7b2d8-122">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="7b2d8-122">Read/write</span></span><br/> | <span data-ttu-id="7b2d8-123">Questa proprietà contiene informazioni sulle proprietà specificate.</span><span class="sxs-lookup"><span data-stu-id="7b2d8-123">This property contains specified property information.</span></span> <br/>                    |
| [<span data-ttu-id="7b2d8-124">**PreceivedType**</span><span class="sxs-lookup"><span data-stu-id="7b2d8-124">**PreceivedType**</span></span>](-search-2x-iresulttype-preceivedtype.md)<br/> | <span data-ttu-id="7b2d8-125">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b2d8-125">Read-only</span></span><br/>  | <span data-ttu-id="7b2d8-126">Questa proprietà contiene la stringa utilizzata per identificare il tipo nell'indice.</span><span class="sxs-lookup"><span data-stu-id="7b2d8-126">This property contains the string used to identify the type in the index.</span></span> <br/> |
| [<span data-ttu-id="7b2d8-127">**PropertyCount**</span><span class="sxs-lookup"><span data-stu-id="7b2d8-127">**PropertyCount**</span></span>](-search-2x-iresulttype-propertycount.md)<br/> | <span data-ttu-id="7b2d8-128">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b2d8-128">Read-only</span></span><br/>  | <span data-ttu-id="7b2d8-129">Questa proprietà contiene il numero di proprietà esposte dal tipo.</span><span class="sxs-lookup"><span data-stu-id="7b2d8-129">This property contains the number of properties exposed by the type.</span></span> <br/>      |
| [<span data-ttu-id="7b2d8-130">**UID**</span><span class="sxs-lookup"><span data-stu-id="7b2d8-130">**UID**</span></span>](-search-2x-iresulttype-uid.md)<br/>                     | <span data-ttu-id="7b2d8-131">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="7b2d8-131">Read-only</span></span><br/>  | <span data-ttu-id="7b2d8-132">Questa proprietà contiene l'identificatore univoco per il tipo.</span><span class="sxs-lookup"><span data-stu-id="7b2d8-132">This property contains the unique identifier for the type.</span></span> <br/>                |



 

## <a name="remarks"></a><span data-ttu-id="7b2d8-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b2d8-133">Remarks</span></span>

<span data-ttu-id="7b2d8-134">Questi metodi espongono i tipi di informazioni restituite.</span><span class="sxs-lookup"><span data-stu-id="7b2d8-134">These methods expose the types of information returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b2d8-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b2d8-135">Requirements</span></span>



| <span data-ttu-id="7b2d8-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b2d8-136">Requirement</span></span> | <span data-ttu-id="7b2d8-137">Valore</span><span class="sxs-lookup"><span data-stu-id="7b2d8-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b2d8-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b2d8-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7b2d8-139">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7b2d8-139">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7b2d8-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b2d8-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7b2d8-141">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="7b2d8-141">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7b2d8-142">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="7b2d8-142">Redistributable</span></span><br/>          | <span data-ttu-id="7b2d8-143">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="7b2d8-143">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="7b2d8-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b2d8-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b2d8-145"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b2d8-145"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

