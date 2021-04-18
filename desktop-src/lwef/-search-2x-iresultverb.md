---
title: Interfaccia IResultVerb (WdsSharedIDL. h)
description: Espone le proprietà del verbo.
ms.assetid: 8cc8408e-0117-4344-ad26-0c4a5d09a935
keywords:
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultVerb
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultVerb, descritte
topic_type:
- apiref
api_name:
- IResultVerb
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d922b9e9b3eb93697ed7daf2688001b031db0c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301947"
---
# <a name="iresultverb-interface"></a><span data-ttu-id="3c4b7-105">Interfaccia IResultVerb</span><span class="sxs-lookup"><span data-stu-id="3c4b7-105">IResultVerb interface</span></span>

> [!NOTE]
> <span data-ttu-id="3c4b7-106">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="3c4b7-107">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="3c4b7-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="3c4b7-108">Espone le proprietà del verbo.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-108">Exposes verb properties.</span></span>

## <a name="members"></a><span data-ttu-id="3c4b7-109">Membri</span><span class="sxs-lookup"><span data-stu-id="3c4b7-109">Members</span></span>

<span data-ttu-id="3c4b7-110">L'interfaccia **IResultVerb** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3c4b7-110">The **IResultVerb** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3c4b7-111">**IResultVerb** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="3c4b7-111">**IResultVerb** also has these types of members:</span></span>

-   [<span data-ttu-id="3c4b7-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3c4b7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3c4b7-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3c4b7-113">Properties</span></span>

<span data-ttu-id="3c4b7-114">L'interfaccia **IResultVerb** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-114">The **IResultVerb** interface has these properties.</span></span>



| <span data-ttu-id="3c4b7-115">Proprietà</span><span class="sxs-lookup"><span data-stu-id="3c4b7-115">Property</span></span>                                                             | <span data-ttu-id="3c4b7-116">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="3c4b7-116">Access type</span></span>           | <span data-ttu-id="3c4b7-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c4b7-117">Description</span></span>                                                                                                       |
|:---------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c4b7-118">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="3c4b7-118">**DisplayName**</span></span>](-search-2x-iresultverb-displayname.md)<br/> | <span data-ttu-id="3c4b7-119">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3c4b7-119">Read-only</span></span><br/>  | <span data-ttu-id="3c4b7-120">Questa proprietà restituisce un puntatore al nome visualizzato localizzato per il verbo.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-120">This property returns a pointer to the localized display name for the verb.</span></span> <br/>                           |
| [<span data-ttu-id="3c4b7-121">**DoIt**</span><span class="sxs-lookup"><span data-stu-id="3c4b7-121">**DoIt**</span></span>](-search-2x-iresultverb-doit.md)<br/>               | <span data-ttu-id="3c4b7-122">Sola scrittura</span><span class="sxs-lookup"><span data-stu-id="3c4b7-122">Write-only</span></span><br/> | <span data-ttu-id="3c4b7-123">Esegue il verbo.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-123">Executes the verb.</span></span> <br/>                                                                                    |
| [<span data-ttu-id="3c4b7-124">**Abilitato**</span><span class="sxs-lookup"><span data-stu-id="3c4b7-124">**Enabled**</span></span>](-search-2x-iresultverb-enabled.md)<br/>         | <span data-ttu-id="3c4b7-125">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3c4b7-125">Read-only</span></span><br/>  | <span data-ttu-id="3c4b7-126">Questa proprietà restituisce TRUE se il verbo è abilitato.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-126">This property returns TRUE if the verb is enabled.</span></span> <br/>                                                    |
| [<span data-ttu-id="3c4b7-127">**HelpText**</span><span class="sxs-lookup"><span data-stu-id="3c4b7-127">**HelpText**</span></span>](-search-2x-iresultverb-helptext.md)<br/>       | <span data-ttu-id="3c4b7-128">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3c4b7-128">Read-only</span></span><br/>  | <span data-ttu-id="3c4b7-129">Questa proprietà restituisce un puntatore alla stringa della Guida localizzata per il verbo.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-129">This property returns a pointer to the localized help string for the verb.</span></span> <br/>                            |
| [<span data-ttu-id="3c4b7-130">**Icona**</span><span class="sxs-lookup"><span data-stu-id="3c4b7-130">**Icon**</span></span>](-search-2x-iresultverb-icon.md)<br/>               | <span data-ttu-id="3c4b7-131">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3c4b7-131">Read-only</span></span><br/>  | <span data-ttu-id="3c4b7-132">Questa proprietà restituisce un puntatore per gestire l'icona facoltativa associata al verbo.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-132">This property returns a pointer to handle of the optional icon associated with the verb.</span></span> <br/>              |
| [<span data-ttu-id="3c4b7-133">**Nome**</span><span class="sxs-lookup"><span data-stu-id="3c4b7-133">**Name**</span></span>](-search-2x-iresultverb-name.md)<br/>               | <span data-ttu-id="3c4b7-134">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="3c4b7-134">Read-only</span></span><br/>  | <span data-ttu-id="3c4b7-135">Questa proprietà restituisce un puntatore al nome cononical per il verbo, ad esempio Print, Open e così via.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-135">This property returns a pointer to the cononical name for the verb such as print, open, and so forth.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="3c4b7-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c4b7-136">Remarks</span></span>

<span data-ttu-id="3c4b7-137">Questi metodi espongono proprietà e azioni applicabili ai verbi.</span><span class="sxs-lookup"><span data-stu-id="3c4b7-137">These methods expose properties and actions applicable to verbs.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c4b7-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c4b7-138">Requirements</span></span>



| <span data-ttu-id="3c4b7-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c4b7-139">Requirement</span></span> | <span data-ttu-id="3c4b7-140">Valore</span><span class="sxs-lookup"><span data-stu-id="3c4b7-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c4b7-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c4b7-141">Minimum supported client</span></span><br/> | <span data-ttu-id="3c4b7-142">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3c4b7-142">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3c4b7-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c4b7-143">Minimum supported server</span></span><br/> | <span data-ttu-id="3c4b7-144">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="3c4b7-144">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3c4b7-145">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="3c4b7-145">Redistributable</span></span><br/>          | <span data-ttu-id="3c4b7-146">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="3c4b7-146">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="3c4b7-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c4b7-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c4b7-148"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c4b7-148"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

