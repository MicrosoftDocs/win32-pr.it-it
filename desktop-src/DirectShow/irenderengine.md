---
description: "L'interfaccia IRenderEngine esegue il rendering di un progetto di servizi di modifica DirectShow (DES) costruendo un grafico di filtro da una sequenza temporale. DES fornisce due componenti che implementano questa interfaccia: il motore di rendering di base crea output non compresso."
ms.assetid: e2a91b34-ee4d-405e-81bf-29d15ea6342a
title: Interfaccia IRenderEngine (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d8c57e976fac877a02c3f3993fb3fe4d27f9033b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332576"
---
# <a name="irenderengine-interface"></a><span data-ttu-id="4550b-103">Interfaccia IRenderEngine</span><span class="sxs-lookup"><span data-stu-id="4550b-103">IRenderEngine interface</span></span>

> [!Note]  
> <span data-ttu-id="4550b-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="4550b-104">\[Deprecated.</span></span> <span data-ttu-id="4550b-105">Questa API può essere rimossa dalle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4550b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4550b-106">L' `IRenderEngine` interfaccia esegue il rendering di un progetto di [servizi di modifica DirectShow](directshow-editing-services.md) (des) costruendo un grafico di filtro da una sequenza temporale.</span><span class="sxs-lookup"><span data-stu-id="4550b-106">The `IRenderEngine` interface renders a [DirectShow Editing Services](directshow-editing-services.md) (DES) project by constructing a filter graph from a timeline.</span></span>

<span data-ttu-id="4550b-107">DES fornisce due componenti che implementano questa interfaccia:</span><span class="sxs-lookup"><span data-stu-id="4550b-107">DES provides two components that implement this interface:</span></span>

-   <span data-ttu-id="4550b-108">Il *motore di rendering di base* crea output non compresso.</span><span class="sxs-lookup"><span data-stu-id="4550b-108">The *basic render engine* creates uncompressed output.</span></span> <span data-ttu-id="4550b-109">È possibile usare l'output per l'anteprima oppure instradarlo tramite filtri di compressione e scriverlo in un file.</span><span class="sxs-lookup"><span data-stu-id="4550b-109">You can use the output for preview, or route it through compression filters and write it to a file.</span></span>
-   <span data-ttu-id="4550b-110">Il *motore di rendering intelligente* crea l'output compresso, usando la *ricompressione intelligente*.</span><span class="sxs-lookup"><span data-stu-id="4550b-110">The *smart render engine* creates compressed output, using *smart recompression*.</span></span> <span data-ttu-id="4550b-111">Con la ricompressione intelligente, un file di origine viene ricompresso solo se il formato è diverso dal formato di output.</span><span class="sxs-lookup"><span data-stu-id="4550b-111">With smart recompression, a source file is recompressed only if its format differs from the output format.</span></span> <span data-ttu-id="4550b-112">Un'origine con un formato corrispondente viene scritta direttamente nel file di output.</span><span class="sxs-lookup"><span data-stu-id="4550b-112">A source with a matching format is written directly to the output file.</span></span> <span data-ttu-id="4550b-113">A seconda dello scenario, la ricompressione intelligente può migliorare significativamente il tempo di rendering.</span><span class="sxs-lookup"><span data-stu-id="4550b-113">Depending on the scenario, smart recompression can greatly improve rendering time.</span></span>

<span data-ttu-id="4550b-114">Il motore di rendering intelligente supporta anche l'interfaccia [**ISmartRenderEngine**](ismartrenderengine.md) .</span><span class="sxs-lookup"><span data-stu-id="4550b-114">The smart render engine also supports the [**ISmartRenderEngine**](ismartrenderengine.md) interface.</span></span>

<span data-ttu-id="4550b-115">Sebbene un'applicazione possa creare un grafico di filtro e passarlo a un motore di rendering, lo scenario tipico è che il motore di rendering crei il grafico dei filtri.</span><span class="sxs-lookup"><span data-stu-id="4550b-115">Although an application can create a filter graph and pass it to a render engine, the typical scenario is for the render engine to create the filter graph.</span></span> <span data-ttu-id="4550b-116">La compilazione del grafo è un processo in due fasi.</span><span class="sxs-lookup"><span data-stu-id="4550b-116">Building the graph is a two-stage process.</span></span> <span data-ttu-id="4550b-117">Per prima cosa, compilare il front-end chiamando il metodo [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) .</span><span class="sxs-lookup"><span data-stu-id="4550b-117">First, build the front end by calling the [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) method.</span></span> <span data-ttu-id="4550b-118">Connettere quindi i pin di output sul front-end ai filtri di rendering desiderati:</span><span class="sxs-lookup"><span data-stu-id="4550b-118">Then connect the output pins on the front end to the desired rendering filters:</span></span>

-   <span data-ttu-id="4550b-119">Renderer video e audio per l'anteprima</span><span class="sxs-lookup"><span data-stu-id="4550b-119">Video and audio renderers for preview, or</span></span>
-   <span data-ttu-id="4550b-120">Compresser, multiplexer e writer di file per generare l'output finale.</span><span class="sxs-lookup"><span data-stu-id="4550b-120">Compressors, multiplexers, and file writers to generate the final output.</span></span>

## <a name="members"></a><span data-ttu-id="4550b-121">Membri</span><span class="sxs-lookup"><span data-stu-id="4550b-121">Members</span></span>

<span data-ttu-id="4550b-122">L'interfaccia **IRenderEngine** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4550b-122">The **IRenderEngine** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4550b-123">**IRenderEngine** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4550b-123">**IRenderEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="4550b-124">Metodi</span><span class="sxs-lookup"><span data-stu-id="4550b-124">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4550b-125">Metodi</span><span class="sxs-lookup"><span data-stu-id="4550b-125">Methods</span></span>

<span data-ttu-id="4550b-126">L'interfaccia **IRenderEngine** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="4550b-126">The **IRenderEngine** interface has these methods.</span></span>



| <span data-ttu-id="4550b-127">Metodo</span><span class="sxs-lookup"><span data-stu-id="4550b-127">Method</span></span>                                                                             | <span data-ttu-id="4550b-128">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4550b-128">Description</span></span>                                                                           |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="4550b-129">**Commit**</span><span class="sxs-lookup"><span data-stu-id="4550b-129">**Commit**</span></span>](irenderengine-commit.md)                                             | <span data-ttu-id="4550b-130">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="4550b-130">Not implemented.</span></span><br/>                                                           |
| [<span data-ttu-id="4550b-131">**ConnectFrontEnd**</span><span class="sxs-lookup"><span data-stu-id="4550b-131">**ConnectFrontEnd**</span></span>](irenderengine-connectfrontend.md)                           | <span data-ttu-id="4550b-132">Compila il front-end del grafico di filtro dalla sequenza temporale corrente.</span><span class="sxs-lookup"><span data-stu-id="4550b-132">Builds the front end of the filter graph from the current timeline.</span></span><br/>        |
| [<span data-ttu-id="4550b-133">**Liberare**</span><span class="sxs-lookup"><span data-stu-id="4550b-133">**Decommit**</span></span>](irenderengine-decommit.md)                                         | <span data-ttu-id="4550b-134">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="4550b-134">Not implemented.</span></span><br/>                                                           |
| [<span data-ttu-id="4550b-135">**DoSmartRecompression**</span><span class="sxs-lookup"><span data-stu-id="4550b-135">**DoSmartRecompression**</span></span>](irenderengine-dosmartrecompression.md)                 | <span data-ttu-id="4550b-136">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="4550b-136">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="4550b-137">**Getcaps**</span><span class="sxs-lookup"><span data-stu-id="4550b-137">**GetCaps**</span></span>](irenderengine-getcaps.md)                                           | <span data-ttu-id="4550b-138">Non implementato.</span><span class="sxs-lookup"><span data-stu-id="4550b-138">Not implemented.</span></span><br/>                                                           |
| [<span data-ttu-id="4550b-139">**GetFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="4550b-139">**GetFilterGraph**</span></span>](irenderengine-getfiltergraph.md)                             | <span data-ttu-id="4550b-140">Recupera il grafico di filtro creato dal motore di rendering, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="4550b-140">Retrieves the filter graph that the render engine has constructed, if any.</span></span><br/> |
| [<span data-ttu-id="4550b-141">**GetGroupOutputPin**</span><span class="sxs-lookup"><span data-stu-id="4550b-141">**GetGroupOutputPin**</span></span>](irenderengine-getgroupoutputpin.md)                       | <span data-ttu-id="4550b-142">Recupera il pin di output per il gruppo specificato.</span><span class="sxs-lookup"><span data-stu-id="4550b-142">Retrieves the output pin for the specified group.</span></span><br/>                          |
| [<span data-ttu-id="4550b-143">**GetTimelineObject**</span><span class="sxs-lookup"><span data-stu-id="4550b-143">**GetTimelineObject**</span></span>](irenderengine-gettimelineobject.md)                       | <span data-ttu-id="4550b-144">Recupera la sequenza temporale attualmente utilizzata dal motore di rendering.</span><span class="sxs-lookup"><span data-stu-id="4550b-144">Retrieves the timeline that the render engine is currently using.</span></span><br/>          |
| [<span data-ttu-id="4550b-145">**GetVendorString**</span><span class="sxs-lookup"><span data-stu-id="4550b-145">**GetVendorString**</span></span>](irenderengine-getvendorstring.md)                           | <span data-ttu-id="4550b-146">Recupera la stringa del fornitore.</span><span class="sxs-lookup"><span data-stu-id="4550b-146">Retrieves the vendor string.</span></span><br/>                                               |
| [<span data-ttu-id="4550b-147">**RenderOutputPins**</span><span class="sxs-lookup"><span data-stu-id="4550b-147">**RenderOutputPins**</span></span>](irenderengine-renderoutputpins.md)                         | <span data-ttu-id="4550b-148">Crea la parte in anteprima del grafico del filtro.</span><span class="sxs-lookup"><span data-stu-id="4550b-148">Creates the previewing portion of the filter graph.</span></span><br/>                        |
| [<span data-ttu-id="4550b-149">**ScrapIt**</span><span class="sxs-lookup"><span data-stu-id="4550b-149">**ScrapIt**</span></span>](irenderengine-scrapit.md)                                           | <span data-ttu-id="4550b-150">Elimina il grafico di filtro del motore di rendering e tutti gli oggetti associati.</span><span class="sxs-lookup"><span data-stu-id="4550b-150">Discards the render engine's filter graph and all associated objects.</span></span><br/>      |
| [<span data-ttu-id="4550b-151">**SetDynamicReconnectLevel**</span><span class="sxs-lookup"><span data-stu-id="4550b-151">**SetDynamicReconnectLevel**</span></span>](irenderengine-setdynamicreconnectlevel.md)         | <span data-ttu-id="4550b-152">Imposta il livello di riconnessione dinamica durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="4550b-152">Sets the level of dynamic reconnection during rendering.</span></span><br/>                   |
| [<span data-ttu-id="4550b-153">**SetFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="4550b-153">**SetFilterGraph**</span></span>](irenderengine-setfiltergraph.md)                             | <span data-ttu-id="4550b-154">Specifica un grafico di filtro per il motore di rendering da usare.</span><span class="sxs-lookup"><span data-stu-id="4550b-154">Specifies a filter graph for the render engine to use.</span></span><br/>                     |
| [<span data-ttu-id="4550b-155">**SetInterestRange**</span><span class="sxs-lookup"><span data-stu-id="4550b-155">**SetInterestRange**</span></span>](irenderengine-setinterestrange.md)                         | <span data-ttu-id="4550b-156">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="4550b-156">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="4550b-157">**SetInterestRange2**</span><span class="sxs-lookup"><span data-stu-id="4550b-157">**SetInterestRange2**</span></span>](irenderengine-setinterestrange2.md)                       | <span data-ttu-id="4550b-158">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="4550b-158">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="4550b-159">**SetRenderRange**</span><span class="sxs-lookup"><span data-stu-id="4550b-159">**SetRenderRange**</span></span>](irenderengine-setrenderrange.md)                             | <span data-ttu-id="4550b-160">Imposta l'intervallo di tempo di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="4550b-160">Sets the range of time to be rendered.</span></span><br/>                                     |
| [<span data-ttu-id="4550b-161">**SetRenderRange2**</span><span class="sxs-lookup"><span data-stu-id="4550b-161">**SetRenderRange2**</span></span>](irenderengine-setrenderrange2.md)                           | <span data-ttu-id="4550b-162">Imposta l'intervallo di tempo di cui eseguire il rendering, come **valore Double**.</span><span class="sxs-lookup"><span data-stu-id="4550b-162">Sets the range of time to be rendered, as a **double**.</span></span><br/>                    |
| [<span data-ttu-id="4550b-163">**SetSourceConnectCallback**</span><span class="sxs-lookup"><span data-stu-id="4550b-163">**SetSourceConnectCallback**</span></span>](irenderengine-setsourceconnectcallback.md)         | <span data-ttu-id="4550b-164">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="4550b-164">Not supported.</span></span><br/>                                                             |
| [<span data-ttu-id="4550b-165">**SetSourceNameValidation**</span><span class="sxs-lookup"><span data-stu-id="4550b-165">**SetSourceNameValidation**</span></span>](irenderengine-setsourcenamevalidation.md)           | <span data-ttu-id="4550b-166">Specifica il modo in cui il motore di rendering convalida i nomi di file.</span><span class="sxs-lookup"><span data-stu-id="4550b-166">Specifies how the render engine validates file names.</span></span><br/>                      |
| [<span data-ttu-id="4550b-167">**SetTimelineObject**</span><span class="sxs-lookup"><span data-stu-id="4550b-167">**SetTimelineObject**</span></span>](irenderengine-settimelineobject.md)                       | <span data-ttu-id="4550b-168">Imposta la sequenza temporale per il motore di rendering da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="4550b-168">Sets the timeline for the render engine to use.</span></span><br/>                            |
| [<span data-ttu-id="4550b-169">**UseInSmartRecompressionGraph**</span><span class="sxs-lookup"><span data-stu-id="4550b-169">**UseInSmartRecompressionGraph**</span></span>](irenderengine-useinsmartrecompressiongraph.md) | <span data-ttu-id="4550b-170">Non supportata.</span><span class="sxs-lookup"><span data-stu-id="4550b-170">Not supported.</span></span><br/>                                                             |



 

## <a name="remarks"></a><span data-ttu-id="4550b-171">Commenti</span><span class="sxs-lookup"><span data-stu-id="4550b-171">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4550b-172">Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.</span><span class="sxs-lookup"><span data-stu-id="4550b-172">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4550b-173">Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="4550b-173">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4550b-174">Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="4550b-174">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4550b-175">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4550b-175">Requirements</span></span>



| <span data-ttu-id="4550b-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="4550b-176">Requirement</span></span> | <span data-ttu-id="4550b-177">Valore</span><span class="sxs-lookup"><span data-stu-id="4550b-177">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4550b-178">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4550b-178">Header</span></span><br/>  | <dl> <span data-ttu-id="4550b-179"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="4550b-179"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4550b-180">Libreria</span><span class="sxs-lookup"><span data-stu-id="4550b-180">Library</span></span><br/> | <dl> <span data-ttu-id="4550b-181"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4550b-181"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4550b-182">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4550b-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4550b-183">Rendering di un progetto</span><span class="sxs-lookup"><span data-stu-id="4550b-183">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 
