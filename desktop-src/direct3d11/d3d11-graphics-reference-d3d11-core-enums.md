---
title: Enumerazioni di base di Direct3D 11
description: Questa sezione contiene informazioni sulle enumerazioni di base.
ms.assetid: 1641713a-5ac8-4597-900b-1bba54f9f522
keywords:
- enumerazioni, Direct3D 11 Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b012ae34367ef849bebf3fb25780310fcb924ba9
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104399901"
---
# <a name="direct3d-11-core-enumerations"></a><span data-ttu-id="5f19c-104">Enumerazioni di base di Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="5f19c-104">Direct3D 11 core enumerations</span></span>

<span data-ttu-id="5f19c-105">Questa sezione contiene informazioni sulle enumerazioni di base.</span><span class="sxs-lookup"><span data-stu-id="5f19c-105">This section contains information about the core enumerations.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5f19c-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="5f19c-106">In this section</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5f19c-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="5f19c-107">Topic</span></span></th>
<th><span data-ttu-id="5f19c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f19c-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f19c-109"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_async_getdata_flag"><strong>D3D11_ASYNC_GETDATA_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-109"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_async_getdata_flag"><strong>D3D11_ASYNC_GETDATA_FLAG</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-110">Flag facoltativi che controllano il comportamento di <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-getdata"><strong>sul ID3D11DeviceContext:: GetData</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5f19c-110">Optional flags that control the behavior of <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-getdata"><strong>ID3D11DeviceContext::GetData</strong></a>.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-111"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_blend"><strong>D3D11_BLEND</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-111"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_blend"><strong>D3D11_BLEND</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-112">Fattori di Blend, che modulano i valori per il pixel shader e la destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="5f19c-112">Blend factors, which modulate values for the pixel shader and render target.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-113"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_blend_op"><strong>D3D11_BLEND_OP</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-113"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_blend_op"><strong>D3D11_BLEND_OP</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-114">Operazione di fusione RGB o Alpha.</span><span class="sxs-lookup"><span data-stu-id="5f19c-114">RGB or alpha blending operation.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-115"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_clear_flag"><strong>D3D11_CLEAR_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-115"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_clear_flag"><strong>D3D11_CLEAR_FLAG</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-116">Specifica le parti del depth stencil da cancellare.</span><span class="sxs-lookup"><span data-stu-id="5f19c-116">Specifies the parts of the depth stencil to clear.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-117"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_color_write_enable"><strong>D3D11_COLOR_WRITE_ENABLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-117"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_color_write_enable"><strong>D3D11_COLOR_WRITE_ENABLE</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-118">Identificare i componenti di ogni pixel di una destinazione di rendering scrivibile durante la fusione.</span><span class="sxs-lookup"><span data-stu-id="5f19c-118">Identify which components of each pixel of a render target are writable during blending.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-119"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_comparison_func"><strong>D3D11_COMPARISON_FUNC</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-119"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_comparison_func"><strong>D3D11_COMPARISON_FUNC</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-120">Opzioni di confronto.</span><span class="sxs-lookup"><span data-stu-id="5f19c-120">Comparison options.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-121"><a href="/windows/win32/api/D3D11_3/ne-d3d11_3-d3d11_conservative_rasterization_mode"><strong>D3D11_CONSERVATIVE_RASTERIZATION_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-121"><a href="/windows/win32/api/D3D11_3/ne-d3d11_3-d3d11_conservative_rasterization_mode"><strong>D3D11_CONSERVATIVE_RASTERIZATION_MODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-122">Indica se la rasterizzazione conservativa è attiva o disattivata.</span><span class="sxs-lookup"><span data-stu-id="5f19c-122">Identifies whether conservative rasterization is on or off.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-123"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_conservative_rasterization_tier"><strong>D3D11_CONSERVATIVE_RASTERIZATION_TIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-123"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_conservative_rasterization_tier"><strong>D3D11_CONSERVATIVE_RASTERIZATION_TIER</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-124">Specifica se l'hardware e il driver supportano la rasterizzazione conservativa e il livello di livello.</span><span class="sxs-lookup"><span data-stu-id="5f19c-124">Specifies if the hardware and driver support conservative rasterization and at what tier level.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-125"><a href="/windows/win32/api/D3D11_3/ne-d3d11_3-d3d11_context_type"><strong>D3D11_CONTEXT_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-125"><a href="/windows/win32/api/D3D11_3/ne-d3d11_3-d3d11_context_type"><strong>D3D11_CONTEXT_TYPE</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-126">Specifica il contesto in cui viene eseguita una query.</span><span class="sxs-lookup"><span data-stu-id="5f19c-126">Specifies the context in which a query occurs.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-127"><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_copy_flags"><strong>D3D11_COPY_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-127"><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_copy_flags"><strong>D3D11_COPY_FLAGS</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="5f19c-128">Questa enumerazione è supportata dal runtime Direct3D 11,1, disponibile nei sistemi operativi Windows 8 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5f19c-128">This enumeration is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="5f19c-129">Specifica come gestire il contenuto esistente di una risorsa durante un'operazione di copia o aggiornamento di un'area all'interno di tale risorsa.</span><span class="sxs-lookup"><span data-stu-id="5f19c-129">Specifies how to handle the existing contents of a resource during a copy or update operation of a region within that resource.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-130"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_counter"><strong>D3D11_COUNTER</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-130"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_counter"><strong>D3D11_COUNTER</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-131">Opzioni per i contatori delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="5f19c-131">Options for performance counters.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-132"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_counter_type"><strong>D3D11_COUNTER_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-132"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_counter_type"><strong>D3D11_COUNTER_TYPE</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-133">Tipo di dati di un contatore delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="5f19c-133">Data type of a performance counter.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-134"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_create_device_flag"><strong>D3D11_CREATE_DEVICE_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-134"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_create_device_flag"><strong>D3D11_CREATE_DEVICE_FLAG</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-135">Descrive i parametri usati per creare un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f19c-135">Describes parameters that are used to create a device.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-136"><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_1_create_device_context_state_flag"><strong>D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-136"><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_1_create_device_context_state_flag"><strong>D3D11_1_CREATE_DEVICE_CONTEXT_STATE_FLAG</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-137">Descrive i flag usati per creare un oggetto stato del contesto del dispositivo (<a href="/windows/win32/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a>) con il metodo <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate"><strong>ID3D11Device1:: CreateDeviceContextState</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="5f19c-137">Describes flags that are used to create a device context state object (<a href="/windows/win32/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate"><strong>ID3DDeviceContextState</strong></a>) with the <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate"><strong>ID3D11Device1::CreateDeviceContextState</strong></a> method.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-138"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_cull_mode"><strong>D3D11_CULL_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-138"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_cull_mode"><strong>D3D11_CULL_MODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-139">Indica che i triangoli rivolti a una direzione particolare non vengono disegnati.</span><span class="sxs-lookup"><span data-stu-id="5f19c-139">Indicates triangles facing a particular direction are not drawn.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-140"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_depth_write_mask"><strong>D3D11_DEPTH_WRITE_MASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-140"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_depth_write_mask"><strong>D3D11_DEPTH_WRITE_MASK</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-141">Identificare la parte di un buffer di stencil Depth per la scrittura di dati di profondità.</span><span class="sxs-lookup"><span data-stu-id="5f19c-141">Identify the portion of a depth-stencil buffer for writing depth data.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-142"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_device_context_type"><strong>D3D11_DEVICE_CONTEXT_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-142"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_device_context_type"><strong>D3D11_DEVICE_CONTEXT_TYPE</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-143">Opzioni del contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f19c-143">Device context options.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-144"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-144"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-145">Opzioni della funzionalità Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="5f19c-145">Direct3D 11 feature options.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-146"><a href="/windows/win32/api/d3d11_3/ne-d3d11_3-d3d11_fence_flag"><strong>D3D11_FENCE_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-146"><a href="/windows/win32/api/d3d11_3/ne-d3d11_3-d3d11_fence_flag"><strong>D3D11_FENCE_FLAG</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-147">Specifica le opzioni di recinzione.</span><span class="sxs-lookup"><span data-stu-id="5f19c-147">Specifies fence options.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-148"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_fill_mode"><strong>D3D11_FILL_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-148"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_fill_mode"><strong>D3D11_FILL_MODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-149">Determina la modalità di riempimento da utilizzare durante il rendering dei triangoli.</span><span class="sxs-lookup"><span data-stu-id="5f19c-149">Determines the fill mode to use when rendering triangles.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-150"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_filter"><strong>D3D11_FILTER</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-150"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_filter"><strong>D3D11_FILTER</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-151">Opzioni di filtro durante il campionamento della trama.</span><span class="sxs-lookup"><span data-stu-id="5f19c-151">Filtering options during texture sampling.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-152"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_filter_type"><strong>D3D11_FILTER_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-152"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_filter_type"><strong>D3D11_FILTER_TYPE</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-153">Tipi di filtri di ingrandimento o campionatore minification.</span><span class="sxs-lookup"><span data-stu-id="5f19c-153">Types of magnification or minification sampler filters.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-154"><a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_filter_reduction_type"><strong>D3D11_FILTER_REDUCTION_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-154"><a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_filter_reduction_type"><strong>D3D11_FILTER_REDUCTION_TYPE</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-155">Specifica il tipo di riduzione del filtro del campionatore.</span><span class="sxs-lookup"><span data-stu-id="5f19c-155">Specifies the type of sampler filter reduction.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-156"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-156"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-157">Quali risorse sono supportate per un formato specificato e un dispositivo specifico (vedere <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkformatsupport"><strong>ID3D11Device:: CheckFormatSupport</strong></a> e <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device:: CheckFeatureSupport</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="5f19c-157">Which resources are supported for a given format and given device (see <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkformatsupport"><strong>ID3D11Device::CheckFormatSupport</strong></a> and <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device::CheckFeatureSupport</strong></a>).</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-158"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-158"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-159">Opzioni di supporto delle risorse non ordinate per una risorsa di calcolo shader (vedere <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device:: CheckFeatureSupport</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="5f19c-159">Unordered resource support options for a compute shader resource (see <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device::CheckFeatureSupport</strong></a>).</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-160"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_input_classification"><strong>D3D11_INPUT_CLASSIFICATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-160"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_input_classification"><strong>D3D11_INPUT_CLASSIFICATION</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-161">Tipo di dati contenuti in uno slot di input.</span><span class="sxs-lookup"><span data-stu-id="5f19c-161">Type of data contained in an input slot.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-162"><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_logic_op"><strong>D3D11_LOGIC_OP</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-162"><a href="/windows/win32/api/D3D11_1/ne-d3d11_1-d3d11_logic_op"><strong>D3D11_LOGIC_OP</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="5f19c-163">Questa enumerazione è supportata dal runtime Direct3D 11,1, disponibile nei sistemi operativi Windows 8 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5f19c-163">This enumeration is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="5f19c-164">Specifica le operazioni logiche da configurare per una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="5f19c-164">Specifies logical operations to configure for a render target.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-165"><a href="/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive"><strong>D3D11_PRIMITIVE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-165"><a href="/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_primitive"><strong>D3D11_PRIMITIVE</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-166">Indica il modo in cui la pipeline interpreta le primitive di input di geometria o Hull shader.</span><span class="sxs-lookup"><span data-stu-id="5f19c-166">Indicates how the pipeline interprets geometry or hull shader input primitives.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-167"><a href="/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)"><strong>D3D11_PRIMITIVE_TOPOLOGY</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-167"><a href="/previous-versions/windows/desktop/legacy/ff476189(v=vs.85)"><strong>D3D11_PRIMITIVE_TOPOLOGY</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-168">Il modo in cui la pipeline interpreta i dati dei vertici associati alla fase input-assembler.</span><span class="sxs-lookup"><span data-stu-id="5f19c-168">How the pipeline interprets vertex data that is bound to the input-assembler stage.</span></span> <span data-ttu-id="5f19c-169">Questi valori di topologia primitivi determinano il rendering dei dati dei vertici sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="5f19c-169">These primitive topology values determine how the vertex data is rendered on screen.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-170"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_query"><strong>D3D11_QUERY</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-170"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_query"><strong>D3D11_QUERY</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-171">Tipi di query.</span><span class="sxs-lookup"><span data-stu-id="5f19c-171">Query types.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-172"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_query_misc_flag"><strong>D3D11_QUERY_MISC_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-172"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_query_misc_flag"><strong>D3D11_QUERY_MISC_FLAG</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-173">Flag che descrivono il comportamento delle query varie.</span><span class="sxs-lookup"><span data-stu-id="5f19c-173">Flags that describe miscellaneous query behavior.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-174"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_raise_flag"><strong>D3D11_RAISE_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-174"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_raise_flag"><strong>D3D11_RAISE_FLAG</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-175">Opzioni per la generazione di un errore a un'eccezione non continuabile.</span><span class="sxs-lookup"><span data-stu-id="5f19c-175">Option(s) for raising an error to a non-continuable exception.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-176"><a href="https://www.bing.com/search?q=<strong>D3D11_SHADER_CACHE_SUPPORT_FLAGS</strong>"><strong>D3D11_SHADER_CACHE_SUPPORT_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-176"><a href="https://www.bing.com/search?q=<strong>D3D11_SHADER_CACHE_SUPPORT_FLAGS</strong>"><strong>D3D11_SHADER_CACHE_SUPPORT_FLAGS</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-177">Viene descritto il livello di supporto per la memorizzazione nella cache dello shader nel driver grafico corrente.</span><span class="sxs-lookup"><span data-stu-id="5f19c-177">Describes the level of support for shader caching in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-178"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_shader_min_precision_support"><strong>D3D11_SHADER_MIN_PRECISION_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-178"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_shader_min_precision_support"><strong>D3D11_SHADER_MIN_PRECISION_SUPPORT</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="5f19c-179">Questa enumerazione è supportata dal runtime Direct3D 11,1, disponibile nei sistemi operativi Windows 8 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="5f19c-179">This enumeration is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="5f19c-180">Valori che specificano i livelli di precisione minimi alle fasi dello shader.</span><span class="sxs-lookup"><span data-stu-id="5f19c-180">Values that specify minimum precision levels at shader stages.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-181"><a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_shared_resource_tier"><strong>D3D11_SHARED_RESOURCE_TIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-181"><a href="/windows/win32/api/d3d11/ne-d3d11-d3d11_shared_resource_tier"><strong>D3D11_SHARED_RESOURCE_TIER</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-182">Definisce le costanti che specificano un livello per il supporto delle risorse condivise.</span><span class="sxs-lookup"><span data-stu-id="5f19c-182">Defines constants that specify a tier for shared resource support.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-183"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_stencil_op"><strong>D3D11_STENCIL_OP</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-183"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_stencil_op"><strong>D3D11_STENCIL_OP</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-184">Operazioni dello stencil che possono essere eseguite durante i test di stencil di profondità.</span><span class="sxs-lookup"><span data-stu-id="5f19c-184">The stencil operations that can be performed during depth-stencil testing.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-185"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_texture_address_mode"><strong>D3D11_TEXTURE_ADDRESS_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-185"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_texture_address_mode"><strong>D3D11_TEXTURE_ADDRESS_MODE</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-186">Identificare una tecnica per la risoluzione di coordinate di trama esterne ai limiti di una trama.</span><span class="sxs-lookup"><span data-stu-id="5f19c-186">Identify a technique for resolving texture coordinates that are outside of the boundaries of a texture.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-187"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_texturecube_face"><strong>D3D11_TEXTURECUBE_FACE</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-187"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_texturecube_face"><strong>D3D11_TEXTURECUBE_FACE</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-188">Facce diverse di una trama del cubo.</span><span class="sxs-lookup"><span data-stu-id="5f19c-188">The different faces of a cube texture.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="5f19c-189"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier"><strong>D3D11_TILED_RESOURCES_TIER</strong></a></span><span class="sxs-lookup"><span data-stu-id="5f19c-189"><a href="/windows/win32/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier"><strong>D3D11_TILED_RESOURCES_TIER</strong></a></span></span><br/></td>
<td><span data-ttu-id="5f19c-190">Indica il livello di livello al quale sono supportate le risorse affiancate.</span><span class="sxs-lookup"><span data-stu-id="5f19c-190">Indicates the tier level at which tiled resources are supported.</span></span><br/></td>
</tr>
</tbody>
</table>

## <a name="related-topics"></a><span data-ttu-id="5f19c-191">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5f19c-191">Related topics</span></span>

[<span data-ttu-id="5f19c-192">Riferimento principale</span><span class="sxs-lookup"><span data-stu-id="5f19c-192">Core reference</span></span>](d3d11-graphics-reference-d3d11-core.md)