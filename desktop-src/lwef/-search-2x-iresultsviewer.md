---
title: Interfaccia IResultsViewer (WdsSharedIDL. h)
description: Espone metodi e proprietà per la visualizzazione dei risultati.
ms.assetid: 4d476511-d65c-4417-8073-337cfbae621d
keywords:
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultsViewer
- Funzionalità dell'ambiente Windows legacy dell'interfaccia IResultsViewer, descritte
topic_type:
- apiref
api_name:
- IResultsViewer
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18702812394f6e7fedd626062aa8c0116cab8427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518124"
---
# <a name="iresultsviewer-interface"></a><span data-ttu-id="35ed5-105">Interfaccia IResultsViewer</span><span class="sxs-lookup"><span data-stu-id="35ed5-105">IResultsViewer interface</span></span>

> [!NOTE]
> <span data-ttu-id="35ed5-106">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="35ed5-106">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="35ed5-107">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="35ed5-107">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="35ed5-108">Espone metodi e proprietà per la visualizzazione dei risultati.</span><span class="sxs-lookup"><span data-stu-id="35ed5-108">Exposes methods and properties for the results view.</span></span>

## <a name="members"></a><span data-ttu-id="35ed5-109">Membri</span><span class="sxs-lookup"><span data-stu-id="35ed5-109">Members</span></span>

<span data-ttu-id="35ed5-110">L'interfaccia **IResultsViewer** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="35ed5-110">The **IResultsViewer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="35ed5-111">**IResultsViewer** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="35ed5-111">**IResultsViewer** also has these types of members:</span></span>

-   [<span data-ttu-id="35ed5-112">Metodi</span><span class="sxs-lookup"><span data-stu-id="35ed5-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="35ed5-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="35ed5-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="35ed5-114">Metodi</span><span class="sxs-lookup"><span data-stu-id="35ed5-114">Methods</span></span>

<span data-ttu-id="35ed5-115">L'interfaccia **IResultsViewer** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="35ed5-115">The **IResultsViewer** interface has these methods.</span></span>



| <span data-ttu-id="35ed5-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="35ed5-116">Method</span></span>                                                   | <span data-ttu-id="35ed5-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35ed5-117">Description</span></span>                                                                            |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="35ed5-118">**GoBack**</span><span class="sxs-lookup"><span data-stu-id="35ed5-118">**GoBack**</span></span>](-search-2x-iresultsviewer-goback.md)       | <span data-ttu-id="35ed5-119">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="35ed5-119">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="35ed5-120">**GoForward**</span><span class="sxs-lookup"><span data-stu-id="35ed5-120">**GoForward**</span></span>](-search-2x-iresultsviewer-goforward.md) | <span data-ttu-id="35ed5-121">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="35ed5-121">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="35ed5-122">**Aggiorna**</span><span class="sxs-lookup"><span data-stu-id="35ed5-122">**Refresh**</span></span>](-search-2x-iresultsviewer-refresh.md)     | <span data-ttu-id="35ed5-123">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="35ed5-123">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="35ed5-124">**Interrompere**</span><span class="sxs-lookup"><span data-stu-id="35ed5-124">**Stop**</span></span>](-search-2x-iresultsviewer-stop.md)           | <span data-ttu-id="35ed5-125">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="35ed5-125">Not implemented.</span></span><br/>                                                            |
| [<span data-ttu-id="35ed5-126">**Aggiornamento**</span><span class="sxs-lookup"><span data-stu-id="35ed5-126">**Update**</span></span>](-search-2x-iresultsviewer-update.md)       | <span data-ttu-id="35ed5-127">Applica le modifiche alle query e sposta la visualizzazione al nuovo set di risultati.</span><span class="sxs-lookup"><span data-stu-id="35ed5-127">Applies any query changes and navigates the view to the new set of results.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="35ed5-128">Proprietà</span><span class="sxs-lookup"><span data-stu-id="35ed5-128">Properties</span></span>

<span data-ttu-id="35ed5-129">L'interfaccia **IResultsViewer** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="35ed5-129">The **IResultsViewer** interface has these properties.</span></span>



| <span data-ttu-id="35ed5-130">Proprietà</span><span class="sxs-lookup"><span data-stu-id="35ed5-130">Property</span></span>                                                                            | <span data-ttu-id="35ed5-131">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="35ed5-131">Access type</span></span>           | <span data-ttu-id="35ed5-132">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35ed5-132">Description</span></span>                                                                                      |
|:------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="35ed5-133">**Contenuto**</span><span class="sxs-lookup"><span data-stu-id="35ed5-133">**Contents**</span></span>](-search-2x-iresultsviewer-contents.md)<br/>                   | <span data-ttu-id="35ed5-134">Sola scrittura</span><span class="sxs-lookup"><span data-stu-id="35ed5-134">Write-only</span></span><br/> | <span data-ttu-id="35ed5-135">Questa proprietà tiene traccia del tipo di contenuto visualizzato nella visualizzazione risultati.</span><span class="sxs-lookup"><span data-stu-id="35ed5-135">This property tracks the type of the content being displayed in the results view.</span></span> <br/>    |
| [<span data-ttu-id="35ed5-136">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="35ed5-136">**DisplayName**</span></span>](-search-2x-iresultsviewer-displayname.md)<br/>             | <span data-ttu-id="35ed5-137">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="35ed5-137">Read-only</span></span><br/>  | <span data-ttu-id="35ed5-138">Nome visualizzato localizzato del tipo.</span><span class="sxs-lookup"><span data-stu-id="35ed5-138">Localized display name of the type.</span></span><br/>                                                   |
| [<span data-ttu-id="35ed5-139">**EnumSelectedItems**</span><span class="sxs-lookup"><span data-stu-id="35ed5-139">**EnumSelectedItems**</span></span>](-search-2x-iresultsviewer-enumselecteditems.md)<br/> | <span data-ttu-id="35ed5-140">Sola scrittura</span><span class="sxs-lookup"><span data-stu-id="35ed5-140">Write-only</span></span><br/> | <span data-ttu-id="35ed5-141">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="35ed5-141">Not implemented.</span></span><br/>                                                                      |
| [<span data-ttu-id="35ed5-142">**FilterType**</span><span class="sxs-lookup"><span data-stu-id="35ed5-142">**FilterType**</span></span>](-search-2x-iresultsviewer-filtertype.md)<br/>               | <span data-ttu-id="35ed5-143">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="35ed5-143">Read/write</span></span><br/> | <span data-ttu-id="35ed5-144">Questa proprietà consente di impostare o restituire il nome del tipo preceived in base al quale filtrare i risultati.</span><span class="sxs-lookup"><span data-stu-id="35ed5-144">This property will set or return the name of the preceived type to filter results by.</span></span><br/> |
| [<span data-ttu-id="35ed5-145">**HeaderStyle**</span><span class="sxs-lookup"><span data-stu-id="35ed5-145">**HeaderStyle**</span></span>](-search-2x-iresultsviewer-headerstyle.md)<br/>             | <span data-ttu-id="35ed5-146">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="35ed5-146">Read/write</span></span><br/> | <span data-ttu-id="35ed5-147">Stile dell'intestazione visualizzata nella visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="35ed5-147">The style of header displayed in the view.</span></span><br/>                                            |
| [<span data-ttu-id="35ed5-148">**IsUpdateNeeded**</span><span class="sxs-lookup"><span data-stu-id="35ed5-148">**IsUpdateNeeded**</span></span>](-search-2x-iresultsviewer-isupdateneeded.md)<br/>       | <span data-ttu-id="35ed5-149">Sola scrittura</span><span class="sxs-lookup"><span data-stu-id="35ed5-149">Write-only</span></span><br/> | <span data-ttu-id="35ed5-150">Restituisce TRUE se la query views è stata modificata ed è necessario aggiornarla.</span><span class="sxs-lookup"><span data-stu-id="35ed5-150">This returns TRUE if the views query has been modified and needs updating.</span></span> <br/>           |
| [<span data-ttu-id="35ed5-151">**ItemStore sconosciuta**</span><span class="sxs-lookup"><span data-stu-id="35ed5-151">**ItemStore**</span></span>](-search-2x-iresultsviewer-itemstore.md)<br/>                 | <span data-ttu-id="35ed5-152">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="35ed5-152">Read/write</span></span><br/> | <span data-ttu-id="35ed5-153">Questa proprietà consente di impostare o restituire il nome dell'archivio in base al quale filtrare i risultati.</span><span class="sxs-lookup"><span data-stu-id="35ed5-153">This property will set or return the name of the store to filter results by.</span></span><br/>          |
| [<span data-ttu-id="35ed5-154">**PreviewStyle**</span><span class="sxs-lookup"><span data-stu-id="35ed5-154">**PreviewStyle**</span></span>](-search-2x-iresultsviewer-previewstyle.md)<br/>           | <span data-ttu-id="35ed5-155">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="35ed5-155">Read/write</span></span><br/> | <span data-ttu-id="35ed5-156">Controlla la modalità di visualizzazione del riquadro di anteprima.</span><span class="sxs-lookup"><span data-stu-id="35ed5-156">Controls the preview pane's display mode.</span></span><br/>                                             |
| [<span data-ttu-id="35ed5-157">**PropertyFilters**</span><span class="sxs-lookup"><span data-stu-id="35ed5-157">**PropertyFilters**</span></span>](-search-2x-iresultsviewer-propertyfilters.md)<br/>     | <span data-ttu-id="35ed5-158">Sola scrittura</span><span class="sxs-lookup"><span data-stu-id="35ed5-158">Write-only</span></span><br/> | <span data-ttu-id="35ed5-159">Quando si chiama la raccolta di filtri di proprietà, restituirà quanto segue:</span><span class="sxs-lookup"><span data-stu-id="35ed5-159">When calling the property filter collection it will return the following:</span></span><br/>             |
| [<span data-ttu-id="35ed5-160">**QueryText**</span><span class="sxs-lookup"><span data-stu-id="35ed5-160">**QueryText**</span></span>](-search-2x-iresultsviewer-querytext.md)<br/>                 | <span data-ttu-id="35ed5-161">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="35ed5-161">Read/write</span></span><br/> | <span data-ttu-id="35ed5-162">Ottiene o imposta il testo della query corrente.</span><span class="sxs-lookup"><span data-stu-id="35ed5-162">Gets or sets the current query text.</span></span><br/>                                                  |
| [<span data-ttu-id="35ed5-163">**ResultsStyle**</span><span class="sxs-lookup"><span data-stu-id="35ed5-163">**ResultsStyle**</span></span>](-search-2x-iresultsviewer-resultsstyle.md)<br/>           | <span data-ttu-id="35ed5-164">Sola scrittura</span><span class="sxs-lookup"><span data-stu-id="35ed5-164">Write-only</span></span><br/> | <span data-ttu-id="35ed5-165">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="35ed5-165">Not implemented.</span></span><br/>                                                                      |
| [<span data-ttu-id="35ed5-166">**SortOrderProperty**</span><span class="sxs-lookup"><span data-stu-id="35ed5-166">**SortOrderProperty**</span></span>](-search-2x-iresultsviewer-sortorderproperty.md)<br/> | <span data-ttu-id="35ed5-167">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="35ed5-167">Read/write</span></span><br/> | <span data-ttu-id="35ed5-168">Questa proprietà consente di impostare o restituire l'ordine delle colonne in base a cui ordinare i risultati.</span><span class="sxs-lookup"><span data-stu-id="35ed5-168">This property will set or return the order of columns to sort results by.</span></span> <br/>            |
| [<span data-ttu-id="35ed5-169">**SortProperty**</span><span class="sxs-lookup"><span data-stu-id="35ed5-169">**SortProperty**</span></span>](-search-2x-iresultsviewer-sortproperty.md)<br/>           | <span data-ttu-id="35ed5-170">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="35ed5-170">Read/write</span></span><br/> | <span data-ttu-id="35ed5-171">Questa proprietà consente di impostare o restituire l'IndexColumn della proprietà per ordinare i risultati in base a.</span><span class="sxs-lookup"><span data-stu-id="35ed5-171">This property will set or return the IndexColumn of the property to sort results by.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="35ed5-172">Commenti</span><span class="sxs-lookup"><span data-stu-id="35ed5-172">Remarks</span></span>

<span data-ttu-id="35ed5-173">Questi metodi e proprietà vengono utilizzati per modificare le informazioni visualizzate.</span><span class="sxs-lookup"><span data-stu-id="35ed5-173">These methods and properties are used to manipulate the information viewed.</span></span>

## <a name="requirements"></a><span data-ttu-id="35ed5-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="35ed5-174">Requirements</span></span>



| <span data-ttu-id="35ed5-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="35ed5-175">Requirement</span></span> | <span data-ttu-id="35ed5-176">Valore</span><span class="sxs-lookup"><span data-stu-id="35ed5-176">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="35ed5-177">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35ed5-177">Minimum supported client</span></span><br/> | <span data-ttu-id="35ed5-178">Solo app desktop Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="35ed5-178">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="35ed5-179">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="35ed5-179">Minimum supported server</span></span><br/> | <span data-ttu-id="35ed5-180">Windows Server 2003 con \[ solo app desktop SP1\]</span><span class="sxs-lookup"><span data-stu-id="35ed5-180">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="35ed5-181">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="35ed5-181">Redistributable</span></span><br/>          | <span data-ttu-id="35ed5-182">Windows Desktop Search (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="35ed5-182">Windows Desktop Search (WDS) 3.0</span></span><br/>                                               |
| <span data-ttu-id="35ed5-183">Intestazione</span><span class="sxs-lookup"><span data-stu-id="35ed5-183">Header</span></span><br/>                   | <dl> <span data-ttu-id="35ed5-184"><dt>WdsSharedIDL. h</dt></span><span class="sxs-lookup"><span data-stu-id="35ed5-184"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

