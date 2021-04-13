---
title: Strutture di base Direct3D 11
description: Questa sezione contiene informazioni sulle strutture di base.
ms.assetid: 2a45182a-7114-4075-b8b8-147f52fe7aa9
keywords:
- strutture, Direct3D 11 Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7025de822265d86e5da9f1da3855d2542c76abf5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399361"
---
# <a name="direct3d-11-core-structures"></a><span data-ttu-id="40678-104">Strutture di base Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="40678-104">Direct3D 11 core structures</span></span>

<span data-ttu-id="40678-105">Questa sezione contiene informazioni sulle strutture di base.</span><span class="sxs-lookup"><span data-stu-id="40678-105">This section contains information about the core structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="40678-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="40678-106">In this section</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="40678-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="40678-107">Topic</span></span></th>
<th><span data-ttu-id="40678-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40678-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="40678-109"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_blend_desc"><strong>D3D11_BLEND_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-109"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_blend_desc"><strong>D3D11_BLEND_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-110">Descrive lo stato di Blend usato in una chiamata a <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-createblendstate"><strong>ID3D11Device:: CreateBlendState</strong></a> per creare un oggetto di stato di Blend.</span><span class="sxs-lookup"><span data-stu-id="40678-110">Describes the blend state that you use in a call to <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11device-createblendstate"><strong>ID3D11Device::CreateBlendState</strong></a> to create a blend-state object.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-111"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1"><strong>D3D11_BLEND_DESC1</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-111"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1"><strong>D3D11_BLEND_DESC1</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="40678-112">Questa struttura è supportata dal runtime Direct3D 11,1, disponibile nei sistemi operativi Windows 8 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="40678-112">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="40678-113">Descrive lo stato di Blend usato in una chiamata a <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1"><strong>ID3D11Device1:: CreateBlendState1</strong></a> per creare un oggetto di stato di Blend.</span><span class="sxs-lookup"><span data-stu-id="40678-113">Describes the blend state that you use in a call to <a href="/windows/win32/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1"><strong>ID3D11Device1::CreateBlendState1</strong></a> to create a blend-state object.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-114"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_box"><strong>D3D11_BOX</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-114"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_box"><strong>D3D11_BOX</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-115">Definisce una casella 3D.</span><span class="sxs-lookup"><span data-stu-id="40678-115">Defines a 3D box.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-116"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_desc"><strong>D3D11_COUNTER_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-116"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_desc"><strong>D3D11_COUNTER_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-117">Descrive un contatore.</span><span class="sxs-lookup"><span data-stu-id="40678-117">Describes a counter.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-118"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_info"><strong>D3D11_COUNTER_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-118"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_counter_info"><strong>D3D11_COUNTER_INFO</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-119">Informazioni sulle funzionalità del contatore delle prestazioni della scheda video.</span><span class="sxs-lookup"><span data-stu-id="40678-119">Information about the video card's performance counter capabilities.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-120"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc"><strong>D3D11_DEPTH_STENCIL_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-120"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc"><strong>D3D11_DEPTH_STENCIL_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-121">Descrive lo stato di depth-stencil.</span><span class="sxs-lookup"><span data-stu-id="40678-121">Describes depth-stencil state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-122"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc"><strong>D3D11_DEPTH_STENCILOP_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-122"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc"><strong>D3D11_DEPTH_STENCILOP_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-123">Operazioni dello stencil che possono essere eseguite in base ai risultati del test dello stencil.</span><span class="sxs-lookup"><span data-stu-id="40678-123">Stencil operations that can be performed based on the results of stencil test.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-124"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_indexed_instanced_indirect_args"><strong>D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-124"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_indexed_instanced_indirect_args"><strong>D3D11_DRAW_INDEXED_INSTANCED_INDIRECT_ARGS</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-125">Argomenti per l'istanza di disegnato indicizzata indiretta.</span><span class="sxs-lookup"><span data-stu-id="40678-125">Arguments for draw indexed instanced indirect.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-126"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_instanced_indirect_args"><strong>D3D11_DRAW_INSTANCED_INDIRECT_ARGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-126"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_draw_instanced_indirect_args"><strong>D3D11_DRAW_INSTANCED_INDIRECT_ARGS</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-127">Argomenti per l'istanza di di estrazione indiretta.</span><span class="sxs-lookup"><span data-stu-id="40678-127">Arguments for draw instanced indirect.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-128"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info"><strong>D3D11_FEATURE_DATA_ARCHITECTURE_INFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-128"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info"><strong>D3D11_FEATURE_DATA_ARCHITECTURE_INFO</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="40678-129">Questa struttura è supportata dal runtime Direct3D 11,1, disponibile nei sistemi operativi Windows 8 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="40678-129">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="40678-130">Vengono fornite informazioni sull'architettura dell'adapter Direct3D 11,1.</span><span class="sxs-lookup"><span data-stu-id="40678-130">Describes information about Direct3D 11.1 adapter architecture.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-131"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-131"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="40678-132">Questa struttura è supportata dal runtime Direct3D 11,1, disponibile nei sistemi operativi Windows 8 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="40678-132">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="40678-133">Descrive le opzioni della funzionalità Direct3D 9 nel driver di grafica corrente.</span><span class="sxs-lookup"><span data-stu-id="40678-133">Describes Direct3D 9 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-134"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options1"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS1</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-134"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options1"><strong>D3D11_FEATURE_DATA_D3D9_OPTIONS1</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-135">Descrive le opzioni della funzionalità Direct3D 9 nel driver di grafica corrente.</span><span class="sxs-lookup"><span data-stu-id="40678-135">Describes Direct3D 9 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-136"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support"><strong>D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-136"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support"><strong>D3D11_FEATURE_DATA_D3D9_SHADOW_SUPPORT</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="40678-137">Questa struttura è supportata dal runtime Direct3D 11,1, disponibile nei sistemi operativi Windows 8 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="40678-137">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="40678-138">Viene descritto il supporto shadow di Direct3D 9 nel driver di grafica corrente.</span><span class="sxs-lookup"><span data-stu-id="40678-138">Describes Direct3D 9 shadow support in the current graphics driver.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-139"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support"><strong>D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-139"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_simple_instancing_support"><strong>D3D11_FEATURE_DATA_D3D9_SIMPLE_INSTANCING_SUPPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-140">Descrive se è supportata la creazione di istanze semplici.</span><span class="sxs-lookup"><span data-stu-id="40678-140">Describes whether simple instancing is supported.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-141"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options"><strong>D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-141"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options"><strong>D3D11_FEATURE_DATA_D3D10_X_HARDWARE_OPTIONS</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-142">Descrive il calcolo dello shader e il supporto dei buffer non elaborati e strutturati nel driver grafico corrente.</span><span class="sxs-lookup"><span data-stu-id="40678-142">Describes compute shader and raw and structured buffer support in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-143"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-143"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="40678-144">Questa struttura è supportata dal runtime Direct3D 11,1, disponibile nei sistemi operativi Windows 8 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="40678-144">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="40678-145">Descrive le opzioni della funzionalità Direct3D 11,1 nel driver di grafica corrente.</span><span class="sxs-lookup"><span data-stu-id="40678-145">Describes Direct3D 11.1 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-146"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS1</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-146"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options1"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS1</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-147">Descrive le opzioni della funzionalità Direct3D 11,2 nel driver di grafica corrente.</span><span class="sxs-lookup"><span data-stu-id="40678-147">Describes Direct3D 11.2 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-148"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS2</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-148"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS2</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-149">Descrive le opzioni della funzionalità Direct3D 11,3 nel driver di grafica corrente.</span><span class="sxs-lookup"><span data-stu-id="40678-149">Describes Direct3D 11.3 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-150"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS3</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-150"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS3</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-151">Descrive le opzioni della funzionalità Direct3D 11,3 nel driver di grafica corrente.</span><span class="sxs-lookup"><span data-stu-id="40678-151">Describes Direct3D 11.3 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-152"><a href="/windows/win32/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS4</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-152"><a href="/windows/win32/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS4</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-153">Descrive le opzioni della funzionalità Direct3D 11,4 nel driver di grafica corrente.</span><span class="sxs-lookup"><span data-stu-id="40678-153">Describes Direct3D 11.4 feature options in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-154"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options5"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS5</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-154"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options5"><strong>D3D11_FEATURE_DATA_D3D11_OPTIONS5</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-155">Descrive il livello di supporto per le risorse condivise nel driver grafico corrente.</span><span class="sxs-lookup"><span data-stu-id="40678-155">Describes the level of support for shared resources in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-156"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_doubles"><strong>D3D11_FEATURE_DATA_DOUBLES</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-156"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_doubles"><strong>D3D11_FEATURE_DATA_DOUBLES</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-157">Viene descritto il supporto del tipo di dati Double nel driver Graphics corrente.</span><span class="sxs-lookup"><span data-stu-id="40678-157">Describes double data type support in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-158"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-158"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-159">Descrive le risorse supportate dal driver grafico corrente per un determinato formato.</span><span class="sxs-lookup"><span data-stu-id="40678-159">Describes which resources are supported by the current graphics driver for a given format.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-160"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-160"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-161">Descrive le opzioni di risorse non ordinate supportate dal driver grafico corrente per un determinato formato.</span><span class="sxs-lookup"><span data-stu-id="40678-161">Describes which unordered resource options are supported by the current graphics driver for a given format.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-162"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_gpu_virtual_address_support"><strong>D3D11_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-162"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_gpu_virtual_address_support"><strong>D3D11_FEATURE_DATA_GPU_VIRTUAL_ADDRESS_SUPPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-163">Descrive il supporto degli indirizzi virtuali della GPU dei dati della funzionalità, inclusi i bit di indirizzo massimo per risorsa e per processo.</span><span class="sxs-lookup"><span data-stu-id="40678-163">Describes feature data GPU virtual address support, including maximum address bits per resource and per process.</span></span> <br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-164"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support"><strong>D3D11_FEATURE_DATA_MARKER_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-164"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_marker_support"><strong>D3D11_FEATURE_DATA_MARKER_SUPPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-165">Descrive se una tecnica di profilatura GPU è supportata.</span><span class="sxs-lookup"><span data-stu-id="40678-165">Describes whether a GPU profiling technique is supported.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-166"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_shader_cache"><strong>D3D11_FEATURE_DATA_SHADER_CACHE</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-166"><a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_shader_cache"><strong>D3D11_FEATURE_DATA_SHADER_CACHE</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-167">Descrive il livello di memorizzazione nella cache dello shader supportato nel driver grafico corrente.</span><span class="sxs-lookup"><span data-stu-id="40678-167">Describes the level of shader caching supported in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-168"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support"><strong>D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-168"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support"><strong>D3D11_FEATURE_DATA_SHADER_MIN_PRECISION_SUPPORT</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="40678-169">Questa struttura è supportata dal runtime Direct3D 11,1, disponibile nei sistemi operativi Windows 8 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="40678-169">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="40678-170">Descrive le opzioni di supporto di precisione per gli shader nel driver grafico corrente.</span><span class="sxs-lookup"><span data-stu-id="40678-170">Describes precision support options for shaders in the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-171"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_threading"><strong>D3D11_FEATURE_DATA_THREADING</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-171"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_feature_data_threading"><strong>D3D11_FEATURE_DATA_THREADING</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-172">Descrive le funzionalità multithread supportate dal driver grafico corrente.</span><span class="sxs-lookup"><span data-stu-id="40678-172">Describes the multi-threading features that are supported by the current graphics driver.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-173"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_input_element_desc"><strong>D3D11_INPUT_ELEMENT_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-173"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_input_element_desc"><strong>D3D11_INPUT_ELEMENT_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-174">Descrizione di un singolo elemento per la fase input-assembler.</span><span class="sxs-lookup"><span data-stu-id="40678-174">A description of a single element for the input-assembler stage.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-175"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics"><strong>D3D11_QUERY_DATA_PIPELINE_STATISTICS</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-175"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics"><strong>D3D11_QUERY_DATA_PIPELINE_STATISTICS</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-176">Eseguire query sulle informazioni sulle attività della pipeline grafica tra le chiamate a <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>sul ID3D11DeviceContext:: Begin</strong></a> e <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>sul ID3D11DeviceContext:: end</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="40678-176">Query information about graphics-pipeline activity in between calls to <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ID3D11DeviceContext::Begin</strong></a> and <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ID3D11DeviceContext::End</strong></a>.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-177"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_so_statistics"><strong>D3D11_QUERY_DATA_SO_STATISTICS</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-177"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_so_statistics"><strong>D3D11_QUERY_DATA_SO_STATISTICS</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-178">Eseguire query sulle informazioni sulla quantità di dati trasmessi ai buffer di output del flusso tra <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>sul ID3D11DeviceContext:: Begin</strong></a> e <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>sul ID3D11DeviceContext:: end</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="40678-178">Query information about the amount of data streamed out to the stream-output buffers in between <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-begin"><strong>ID3D11DeviceContext::Begin</strong></a> and <a href="/windows/win32/api/D3D11/nf-d3d11-id3d11devicecontext-end"><strong>ID3D11DeviceContext::End</strong></a>.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-179"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_timestamp_disjoint"><strong>D3D11_QUERY_DATA_TIMESTAMP_DISJOINT</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-179"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_data_timestamp_disjoint"><strong>D3D11_QUERY_DATA_TIMESTAMP_DISJOINT</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-180">Eseguire query sulle informazioni sull'affidabilità di una query timestamp.</span><span class="sxs-lookup"><span data-stu-id="40678-180">Query information about the reliability of a timestamp query.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-181"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_desc"><strong>D3D11_QUERY_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-181"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_query_desc"><strong>D3D11_QUERY_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-182">Descrive una query.</span><span class="sxs-lookup"><span data-stu-id="40678-182">Describes a query.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-183"><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_query_desc1"><strong>D3D11_QUERY_DESC1</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-183"><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_query_desc1"><strong>D3D11_QUERY_DESC1</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-184">Descrive una query.</span><span class="sxs-lookup"><span data-stu-id="40678-184">Describes a query.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-185"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_rasterizer_desc"><strong>D3D11_RASTERIZER_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-185"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_rasterizer_desc"><strong>D3D11_RASTERIZER_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-186">Descrive lo stato di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="40678-186">Describes rasterizer state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-187"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1"><strong>D3D11_RASTERIZER_DESC1</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-187"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1"><strong>D3D11_RASTERIZER_DESC1</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="40678-188">Questa struttura è supportata dal runtime Direct3D 11,1, disponibile nei sistemi operativi Windows 8 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="40678-188">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="40678-189">Descrive lo stato di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="40678-189">Describes rasterizer state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-190"><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2"><strong>D3D11_RASTERIZER_DESC2</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-190"><a href="/windows/win32/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2"><strong>D3D11_RASTERIZER_DESC2</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-191">Descrive lo stato di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="40678-191">Describes rasterizer state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-192"><a href="d3d11-rect.md"><strong>D3D11_RECT</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-192"><a href="d3d11-rect.md"><strong>D3D11_RECT</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-193">D3D11_RECT viene dichiarata come segue:</span><span class="sxs-lookup"><span data-stu-id="40678-193">D3D11_RECT is declared as follows:</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-194"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_render_target_blend_desc"><strong>D3D11_RENDER_TARGET_BLEND_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-194"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_render_target_blend_desc"><strong>D3D11_RENDER_TARGET_BLEND_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-195">Descrive lo stato di Blend per una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="40678-195">Describes the blend state for a render target.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-196"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1"><strong>D3D11_RENDER_TARGET_BLEND_DESC1</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-196"><a href="/windows/win32/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1"><strong>D3D11_RENDER_TARGET_BLEND_DESC1</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="40678-197">Questa struttura è supportata dal runtime Direct3D 11,1, disponibile nei sistemi operativi Windows 8 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="40678-197">This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</span></span>
</blockquote>
<br/> <span data-ttu-id="40678-198">Descrive lo stato di Blend per una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="40678-198">Describes the blend state for a render target.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-199"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc"><strong>D3D11_SAMPLER_DESC</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-199"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_sampler_desc"><strong>D3D11_SAMPLER_DESC</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-200">Descrive uno stato del campionatore.</span><span class="sxs-lookup"><span data-stu-id="40678-200">Describes a sampler state.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-201"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_so_declaration_entry"><strong>D3D11_SO_DECLARATION_ENTRY</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-201"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_so_declaration_entry"><strong>D3D11_SO_DECLARATION_ENTRY</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-202">Descrizione di un elemento vertice in un buffer vertex in uno slot di output.</span><span class="sxs-lookup"><span data-stu-id="40678-202">Description of a vertex element in a vertex buffer in an output slot.</span></span><br/></td>
</tr>
<tr>
<td><span data-ttu-id="40678-203"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_viewport"><strong>D3D11_VIEWPORT</strong></a></span><span class="sxs-lookup"><span data-stu-id="40678-203"><a href="/windows/win32/api/D3D11/ns-d3d11-d3d11_viewport"><strong>D3D11_VIEWPORT</strong></a></span></span><br/></td>
<td><span data-ttu-id="40678-204">Definisce le dimensioni di un viewport.</span><span class="sxs-lookup"><span data-stu-id="40678-204">Defines the dimensions of a viewport.</span></span><br/></td>
</tr>
</tbody>
</table>

<span data-ttu-id="40678-205">Inoltre, è presente una struttura rettangolare 2D definita in D3D11. h.</span><span class="sxs-lookup"><span data-stu-id="40678-205">In addition, there's a 2D rectangle structure defined in D3D11.h.</span></span>

```cpp
typedef RECT D3D11_RECT;
```

<span data-ttu-id="40678-206">Per la documentazione, vedere [Rect](/previous-versions/dd162897%28v%3dvs.85%29) in [Windows GDI](../gdi/windows-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="40678-206">For documentation, see [RECT](/previous-versions/dd162897%28v%3dvs.85%29) in [Windows GDI](../gdi/windows-gdi.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="40678-207">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="40678-207">Related topics</span></span>

[<span data-ttu-id="40678-208">Riferimento principale</span><span class="sxs-lookup"><span data-stu-id="40678-208">Core Reference</span></span>](d3d11-graphics-reference-d3d11-core.md)