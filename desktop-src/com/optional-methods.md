---
title: Metodi facoltativi
description: Metodi facoltativi
ms.assetid: 8cdb5686-177c-48c9-8315-e5921520007c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904aad26ecfba6396c9911b247443f9a956bca7f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104118491"
---
# <a name="optional-methods"></a><span data-ttu-id="dd0ef-103">Metodi facoltativi</span><span class="sxs-lookup"><span data-stu-id="dd0ef-103">Optional Methods</span></span>

<span data-ttu-id="dd0ef-104">Un componente OLE può implementare un'interfaccia senza implementare tutta la semantica di ogni metodo nell'interfaccia, restituendo invece E \_ NOTIMPL o S \_ OK in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="dd0ef-104">An OLE component can implement an interface without implementing all the semantics of every method in the interface, instead returning E\_NOTIMPL or S\_OK as appropriate.</span></span> <span data-ttu-id="dd0ef-105">Nella tabella seguente vengono descritti i metodi che non devono essere implementati da un contenitore di controlli ActiveX (ovvero il contenitore di controlli può restituire E \_ NOTIMPL).</span><span class="sxs-lookup"><span data-stu-id="dd0ef-105">The following table describes those methods that an ActiveX control container is not required to implement (i.e. the control container can return E\_NOTIMPL).</span></span>

<span data-ttu-id="dd0ef-106">La tabella seguente descrive i metodi facoltativi. Si noti che il metodo deve ancora esistere, ma può semplicemente restituire E \_ NOTIMPL anziché implementare la semantica reale.</span><span class="sxs-lookup"><span data-stu-id="dd0ef-106">The table below describes optional methods; note that the method must still exist, but can simply return E\_NOTIMPL instead of implementing real semantics.</span></span> <span data-ttu-id="dd0ef-107">Si noti che tutti i metodi di un'interfaccia obbligatoria non elencati di seguito devono essere considerati obbligatori e non possono restituire E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="dd0ef-107">Note that any method from a mandatory interface that is not listed below must be considered mandatory and may not return E\_NOTIMPL.</span></span>

## <a name="ioleclientsite"></a><span data-ttu-id="dd0ef-108">IOleClientSite</span><span class="sxs-lookup"><span data-stu-id="dd0ef-108">IOleClientSite</span></span>



| <span data-ttu-id="dd0ef-109">Metodo</span><span class="sxs-lookup"><span data-stu-id="dd0ef-109">Method</span></span>                                                     | <span data-ttu-id="dd0ef-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd0ef-110">Comments</span></span>                                                                                                 |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd0ef-111">**SaveObject**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-111">**SaveObject**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-saveobject)<br/> | <span data-ttu-id="dd0ef-112">Necessaria per il corretto supporto della persistenza.</span><span class="sxs-lookup"><span data-stu-id="dd0ef-112">Necessary for persistence to be successfully supported.</span></span><br/>                                       |
| [<span data-ttu-id="dd0ef-113">**GetMoniker**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-113">**GetMoniker**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-getmoniker)<br/> | <span data-ttu-id="dd0ef-114">Necessaria solo se il contenitore supporta il collegamento a controlli all'interno di un modulo o di un documento.</span><span class="sxs-lookup"><span data-stu-id="dd0ef-114">Necessary only if the container supports linking to controls within its own form or document.</span></span><br/> |



 

## <a name="ioleinplacesite"></a><span data-ttu-id="dd0ef-115">IOleInPlaceSite</span><span class="sxs-lookup"><span data-stu-id="dd0ef-115">IOleInPlaceSite</span></span>



| <span data-ttu-id="dd0ef-116">Metodo</span><span class="sxs-lookup"><span data-stu-id="dd0ef-116">Method</span></span>                                                                     | <span data-ttu-id="dd0ef-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd0ef-117">Comments</span></span>                                                 |
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="dd0ef-118">**ContextSensitiveHelp**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-118">**ContextSensitiveHelp**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/> | <span data-ttu-id="dd0ef-119">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="dd0ef-119">Optional</span></span><br/>                                      |
| [<span data-ttu-id="dd0ef-120">**Scorrimento**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-120">**Scroll**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-scroll)<br/>                        | <span data-ttu-id="dd0ef-121">Può restituire S \_ false senza azione.</span><span class="sxs-lookup"><span data-stu-id="dd0ef-121">May return S\_FALSE with no action.</span></span><br/>           |
| [<span data-ttu-id="dd0ef-122">**DiscardUndoState**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-122">**DiscardUndoState**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-discardundostate)<br/>    | <span data-ttu-id="dd0ef-123">Può restituire S \_ OK senza alcuna azione.</span><span class="sxs-lookup"><span data-stu-id="dd0ef-123">Can return S\_OK with no action.</span></span><br/>              |
| [<span data-ttu-id="dd0ef-124">**DeactivateAndUndo**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-124">**DeactivateAndUndo**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-deactivateandundo)<br/>  | <span data-ttu-id="dd0ef-125">La disattivazione è obbligatoria. Undo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="dd0ef-125">Deactivation is mandatory; Undo is optional.</span></span> <br/> |



 

## <a name="iolecontrolsite"></a><span data-ttu-id="dd0ef-126">IOleControlSite</span><span class="sxs-lookup"><span data-stu-id="dd0ef-126">IOleControlSite</span></span>



| <span data-ttu-id="dd0ef-127">Metodo</span><span class="sxs-lookup"><span data-stu-id="dd0ef-127">Method</span></span>                                                                          | <span data-ttu-id="dd0ef-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd0ef-128">Comments</span></span>                                                                                                                                                            |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd0ef-129">**GetExtendedControl**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-129">**GetExtendedControl**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol)<br/>     | <span data-ttu-id="dd0ef-130">Necessaria per i contenitori che supportano i controlli estesi.</span><span class="sxs-lookup"><span data-stu-id="dd0ef-130">Necessary for containers that support extended controls.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="dd0ef-131">**ShowPropertyFrame**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-131">**ShowPropertyFrame**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe)<br/>       | <span data-ttu-id="dd0ef-132">Necessaria per i contenitori che desiderano includere le proprie pagine delle proprietà per gestire le proprietà di controllo estese, oltre a quelle fornite da un controllo.</span><span class="sxs-lookup"><span data-stu-id="dd0ef-132">Necessary for containers that wish to include their own property pages to handle extended control properties in addition to those provided by a control.</span></span><br/> |
| [<span data-ttu-id="dd0ef-133">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-133">**TranslateAccelerator**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator)<br/> | <span data-ttu-id="dd0ef-134">Può restituire S \_ false senza azione.</span><span class="sxs-lookup"><span data-stu-id="dd0ef-134">May return S\_FALSE with no action.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="dd0ef-135">**LockInPlaceActive**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-135">**LockInPlaceActive**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive)<br/>       | <span data-ttu-id="dd0ef-136">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="dd0ef-136">Optional</span></span><br/>                                                                                                                                                 |



 

## <a name="idispatch-ambient-properties"></a><span data-ttu-id="dd0ef-137">IDispatch (proprietà di ambiente)</span><span class="sxs-lookup"><span data-stu-id="dd0ef-137">IDispatch (Ambient properties)</span></span>



| <span data-ttu-id="dd0ef-138">Metodo</span><span class="sxs-lookup"><span data-stu-id="dd0ef-138">Method</span></span>                      | <span data-ttu-id="dd0ef-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd0ef-139">Comments</span></span>                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="dd0ef-140">GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="dd0ef-140">GetTypeInfoCount</span></span><br/> | <span data-ttu-id="dd0ef-141">Necessaria per i contenitori che supportano le proprietà di ambiente non standard.</span><span class="sxs-lookup"><span data-stu-id="dd0ef-141">Necessary for containers that support non-standard ambient properties.</span></span><br/> |
| <span data-ttu-id="dd0ef-142">GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="dd0ef-142">GetTypeInfo</span></span><br/>      | <span data-ttu-id="dd0ef-143">Necessaria per i contenitori che supportano le proprietà di ambiente non standard.</span><span class="sxs-lookup"><span data-stu-id="dd0ef-143">Necessary for containers that support non-standard ambient properties.</span></span><br/> |
| <span data-ttu-id="dd0ef-144">GetIDsOfNames</span><span class="sxs-lookup"><span data-stu-id="dd0ef-144">GetIDsOfNames</span></span><br/>    | <span data-ttu-id="dd0ef-145">Necessaria per i contenitori che supportano le proprietà di ambiente non standard.</span><span class="sxs-lookup"><span data-stu-id="dd0ef-145">Necessary for containers that support non-standard ambient properties.</span></span><br/> |



 

## <a name="idispatch-event-sink"></a><span data-ttu-id="dd0ef-146">IDispatch (sink di evento)</span><span class="sxs-lookup"><span data-stu-id="dd0ef-146">IDispatch (Event sink)</span></span>



| <span data-ttu-id="dd0ef-147">Metodo</span><span class="sxs-lookup"><span data-stu-id="dd0ef-147">Method</span></span>                      | <span data-ttu-id="dd0ef-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd0ef-148">Comments</span></span>                                                                               |
|-----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd0ef-149">GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="dd0ef-149">GetTypeInfoCount</span></span><br/> | <span data-ttu-id="dd0ef-150">Il controllo è in grado di riconoscere le proprie informazioni sul tipo, pertanto non è necessario chiamarlo.</span><span class="sxs-lookup"><span data-stu-id="dd0ef-150">The control knows its own type information, so it has no need to call this.</span></span><br/> |
| <span data-ttu-id="dd0ef-151">GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="dd0ef-151">GetTypeInfo</span></span><br/>      | <span data-ttu-id="dd0ef-152">Il controllo è in grado di riconoscere le proprie informazioni sul tipo, pertanto non è necessario chiamarlo.</span><span class="sxs-lookup"><span data-stu-id="dd0ef-152">The control knows its own type information, so it has no need to call this.</span></span><br/> |
| <span data-ttu-id="dd0ef-153">GetIDsOfNames</span><span class="sxs-lookup"><span data-stu-id="dd0ef-153">GetIDsOfNames</span></span><br/>    | <span data-ttu-id="dd0ef-154">Il controllo è in grado di riconoscere le proprie informazioni sul tipo, pertanto non è necessario chiamarlo.</span><span class="sxs-lookup"><span data-stu-id="dd0ef-154">The control knows its own type information, so it has no need to call this.</span></span><br/> |



 

## <a name="ioleinplaceframe"></a><span data-ttu-id="dd0ef-155">IOleInPlaceFrame</span><span class="sxs-lookup"><span data-stu-id="dd0ef-155">IOleInPlaceFrame</span></span>



| <span data-ttu-id="dd0ef-156">Metodo</span><span class="sxs-lookup"><span data-stu-id="dd0ef-156">Method</span></span>                                                                           | <span data-ttu-id="dd0ef-157">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd0ef-157">Comments</span></span>                                                                |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="dd0ef-158">**ContextSensitiveHelp**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-158">**ContextSensitiveHelp**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>       |                                                                         |
| [<span data-ttu-id="dd0ef-159">**GetBorder**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-159">**GetBorder**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)<br/>                    | <span data-ttu-id="dd0ef-160">Necessaria per i contenitori con interfaccia utente della barra degli strumenti (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="dd0ef-160">Necessary for containers with toolbar UI (which is optional)</span></span><br/> |
| [<span data-ttu-id="dd0ef-161">**RequestBorderSpace**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-161">**RequestBorderSpace**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)<br/>  | <span data-ttu-id="dd0ef-162">Necessaria per i contenitori con interfaccia utente della barra degli strumenti (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="dd0ef-162">Necessary for containers with toolbar UI (which is optional)</span></span><br/> |
| [<span data-ttu-id="dd0ef-163">**SetBorderSpace**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-163">**SetBorderSpace**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)<br/>          | <span data-ttu-id="dd0ef-164">Necessaria per i contenitori con interfaccia utente della barra degli strumenti (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="dd0ef-164">Necessary for containers with toolbar UI (which is optional)</span></span><br/> |
| [<span data-ttu-id="dd0ef-165">**InsertMenus**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-165">**InsertMenus**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-insertmenus)<br/>                   | <span data-ttu-id="dd0ef-166">Necessaria per i contenitori con interfaccia utente di menu (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="dd0ef-166">Necessary for containers with menu UI (which is optional)</span></span><br/>    |
| [<span data-ttu-id="dd0ef-167">**SetMenu**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-167">**SetMenu**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)<br/>                           | <span data-ttu-id="dd0ef-168">Necessaria per i contenitori con interfaccia utente di menu (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="dd0ef-168">Necessary for containers with menu UI (which is optional)</span></span><br/>    |
| [<span data-ttu-id="dd0ef-169">**RemoveMenus**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-169">**RemoveMenus**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-removemenus)<br/>                   | <span data-ttu-id="dd0ef-170">Necessaria per i contenitori con interfaccia utente di menu (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="dd0ef-170">Necessary for containers with menu UI (which is optional)</span></span><br/>    |
| [<span data-ttu-id="dd0ef-171">**SetStatusText**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-171">**SetStatusText**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)<br/>               | <span data-ttu-id="dd0ef-172">Necessaria solo per i contenitori con una riga di stato</span><span class="sxs-lookup"><span data-stu-id="dd0ef-172">Necessary only for containers that have a status line</span></span><br/>        |
| [<span data-ttu-id="dd0ef-173">**EnableModeless**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-173">**EnableModeless**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-enablemodeless)<br/>             | <span data-ttu-id="dd0ef-174">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="dd0ef-174">Optional</span></span><br/>                                                     |
| [<span data-ttu-id="dd0ef-175">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-175">**TranslateAccelerator**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-translateaccelerator)<br/> | <span data-ttu-id="dd0ef-176">Facoltativo</span><span class="sxs-lookup"><span data-stu-id="dd0ef-176">Optional</span></span><br/>                                                     |



 

## <a name="iolecontainer"></a><span data-ttu-id="dd0ef-177">IOleContainer</span><span class="sxs-lookup"><span data-stu-id="dd0ef-177">IOleContainer</span></span>



| <span data-ttu-id="dd0ef-178">Metodo</span><span class="sxs-lookup"><span data-stu-id="dd0ef-178">Method</span></span>                                                                    | <span data-ttu-id="dd0ef-179">Commenti</span><span class="sxs-lookup"><span data-stu-id="dd0ef-179">Comments</span></span>                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dd0ef-180">**ParseDisplayName**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-180">**ParseDisplayName**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iparsedisplayname-parsedisplayname)<br/> | <span data-ttu-id="dd0ef-181">Solo se è supportato il collegamento a controlli o altri incorporamenti nel contenitore, perché questa operazione è necessaria per l'associazione del moniker.</span><span class="sxs-lookup"><span data-stu-id="dd0ef-181">Only if linking to controls or other embeddings in the container is supported, as this is necessary for moniker binding.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="dd0ef-182">**LockContainer**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-182">**LockContainer**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-lockcontainer)<br/>           | <span data-ttu-id="dd0ef-183">Come per ParseDisplayName</span><span class="sxs-lookup"><span data-stu-id="dd0ef-183">As for ParseDisplayName</span></span><br/>                                                                                                                                                                                                                   |
| [<span data-ttu-id="dd0ef-184">**EnumObjects**</span><span class="sxs-lookup"><span data-stu-id="dd0ef-184">**EnumObjects**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-enumobjects)<br/>               | <span data-ttu-id="dd0ef-185">Restituisce tutti i controlli ActiveX tramite un enumeratore con [**IEnumUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown), ma non necessariamente tutti gli oggetti (poiché non c'è alcuna garanzia che tutti gli oggetti siano controlli ActiveX; alcuni possono essere controlli di Windows normali).</span><span class="sxs-lookup"><span data-stu-id="dd0ef-185">Returns all ActiveX controls through an enumerator with [**IEnumUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown), but not necessarily all objects (because there's no guarantee that all objects are ActiveX controls; some may be regular Windows controls).</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="dd0ef-186">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dd0ef-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd0ef-187">Contenitori</span><span class="sxs-lookup"><span data-stu-id="dd0ef-187">Containers</span></span>](containers.md)
</dt> </dl>

 

