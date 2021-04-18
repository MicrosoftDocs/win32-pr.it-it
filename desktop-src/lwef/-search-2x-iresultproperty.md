---
title: Interfaccia IResultProperty (WdsSharedIDL. h)
description: Espone le proprietà del risultato.
ms.assetid: 58d8c516-47c6-4cae-b46c-5127baf3054d
keywords:
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultProperty
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultProperty, descritte
topic_type:
- apiref
api_name:
- IResultProperty
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 716c0b3998171731dea5f976afc266fe81b2c613
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302069"
---
# <a name="iresultproperty-interface"></a><span data-ttu-id="b57ee-105">Interfaccia IResultProperty</span><span class="sxs-lookup"><span data-stu-id="b57ee-105">IResultProperty interface</span></span>

> [!NOTE]
> <span data-ttu-id="b57ee-106">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b57ee-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="b57ee-107">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="b57ee-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="b57ee-108">Espone le proprietà del risultato.</span><span class="sxs-lookup"><span data-stu-id="b57ee-108">Exposes result properties.</span></span>

## <a name="members"></a><span data-ttu-id="b57ee-109">Membri</span><span class="sxs-lookup"><span data-stu-id="b57ee-109">Members</span></span>

<span data-ttu-id="b57ee-110">L'interfaccia **IResultProperty** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b57ee-110">The **IResultProperty** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b57ee-111">**IResultProperty** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b57ee-111">**IResultProperty** also has these types of members:</span></span>

-   [<span data-ttu-id="b57ee-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="b57ee-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="b57ee-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b57ee-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b57ee-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="b57ee-114">Methods</span></span>

<span data-ttu-id="b57ee-115">L'interfaccia **IResultProperty** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="b57ee-115">The **IResultProperty** interface has these methods.</span></span>



| <span data-ttu-id="b57ee-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="b57ee-116">Method</span></span>                                                    | <span data-ttu-id="b57ee-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b57ee-117">Description</span></span>                 |
|:----------------------------------------------------------|:----------------------------|
| [<span data-ttu-id="b57ee-118">**GoBack**</span><span class="sxs-lookup"><span data-stu-id="b57ee-118">**GoBack**</span></span>](-search-2x-iresultproperty-goback.md)       | <span data-ttu-id="b57ee-119">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="b57ee-119">Not implemented.</span></span><br/> |
| [<span data-ttu-id="b57ee-120">**GoForward**</span><span class="sxs-lookup"><span data-stu-id="b57ee-120">**GoForward**</span></span>](-search-2x-iresultproperty-goforward.md) | <span data-ttu-id="b57ee-121">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="b57ee-121">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b57ee-122">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b57ee-122">Properties</span></span>

<span data-ttu-id="b57ee-123">L'interfaccia **IResultProperty** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b57ee-123">The **IResultProperty** interface has these properties.</span></span>



| <span data-ttu-id="b57ee-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b57ee-124">Property</span></span>                                                                   | <span data-ttu-id="b57ee-125">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="b57ee-125">Access type</span></span>          | <span data-ttu-id="b57ee-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b57ee-126">Description</span></span>                                           |
|:---------------------------------------------------------------------------|:---------------------|:------------------------------------------------------|
| [<span data-ttu-id="b57ee-127">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b57ee-127">**DataType**</span></span>](-search-2x-iresultproperty-datatype.md)<br/>         | <span data-ttu-id="b57ee-128">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="b57ee-128">Read-only</span></span><br/> | <span data-ttu-id="b57ee-129">Tipo di dati Properties.</span><span class="sxs-lookup"><span data-stu-id="b57ee-129">A properties data type.</span></span> <br/>                   |
| [<span data-ttu-id="b57ee-130">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="b57ee-130">**DisplayName**</span></span>](-search-2x-iresultproperty-displayname.md)<br/>   | <span data-ttu-id="b57ee-131">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="b57ee-131">Read-only</span></span><br/> | <span data-ttu-id="b57ee-132">Nome visualizzato localizzato della proprietà.</span><span class="sxs-lookup"><span data-stu-id="b57ee-132">Localized display name of the property.</span></span> <br/>   |
| [<span data-ttu-id="b57ee-133">**DisplayState**</span><span class="sxs-lookup"><span data-stu-id="b57ee-133">**DisplayState**</span></span>](-search-2x-iresultproperty-displaystate.md)<br/> | <span data-ttu-id="b57ee-134">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="b57ee-134">Read-only</span></span><br/> | <span data-ttu-id="b57ee-135">Visibilità della proprietà.</span><span class="sxs-lookup"><span data-stu-id="b57ee-135">Visability of the property.</span></span> <br/>               |
| [<span data-ttu-id="b57ee-136">**Suggerimento**</span><span class="sxs-lookup"><span data-stu-id="b57ee-136">**Hint**</span></span>](-search-2x-iresultproperty-hint.md)<br/>                 | <span data-ttu-id="b57ee-137">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="b57ee-137">Read-only</span></span><br/> | <span data-ttu-id="b57ee-138">Valore speciale usato per facilitare il recupero dei dati.</span><span class="sxs-lookup"><span data-stu-id="b57ee-138">Special value used to aid data retrieval.</span></span> <br/> |
| [<span data-ttu-id="b57ee-139">**IndexColumn**</span><span class="sxs-lookup"><span data-stu-id="b57ee-139">**IndexColumn**</span></span>](-search-2x-iresultproperty-indexcolumn.md)<br/>   | <span data-ttu-id="b57ee-140">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="b57ee-140">Read-only</span></span><br/> | <span data-ttu-id="b57ee-141">Nome della colonna proprietà nell'indice.</span><span class="sxs-lookup"><span data-stu-id="b57ee-141">Properties column name in the index.</span></span> <br/>      |
| [<span data-ttu-id="b57ee-142">**UID**</span><span class="sxs-lookup"><span data-stu-id="b57ee-142">**UID**</span></span>](-search-2x-iresultproperty-uid.md)<br/>                   | <span data-ttu-id="b57ee-143">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="b57ee-143">Read-only</span></span><br/> | <span data-ttu-id="b57ee-144">Identificatore univoco per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="b57ee-144">Unique identifier for the property.</span></span> <br/>       |



 

## <a name="remarks"></a><span data-ttu-id="b57ee-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="b57ee-145">Remarks</span></span>

<span data-ttu-id="b57ee-146">Si tratta degli elementi che restituiscono proprietà.</span><span class="sxs-lookup"><span data-stu-id="b57ee-146">These are the items return properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="b57ee-147">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b57ee-147">Requirements</span></span>



| <span data-ttu-id="b57ee-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="b57ee-148">Requirement</span></span> | <span data-ttu-id="b57ee-149">Valore</span><span class="sxs-lookup"><span data-stu-id="b57ee-149">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="b57ee-150">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b57ee-150">Minimum supported client</span></span><br/> | <span data-ttu-id="b57ee-151">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b57ee-151">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b57ee-152">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b57ee-152">Minimum supported server</span></span><br/> | <span data-ttu-id="b57ee-153">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="b57ee-153">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b57ee-154">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="b57ee-154">Redistributable</span></span><br/>          | <span data-ttu-id="b57ee-155">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="b57ee-155">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="b57ee-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b57ee-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="b57ee-157"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b57ee-157"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

