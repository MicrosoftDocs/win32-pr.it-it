---
description: Questa sezione illustra come verificare il supporto del formato per l'hardware a livello di funzionalità Direct3D usando le chiamate API.
ms.assetid: 0C40C73E-06F3-41FA-AA27-2C0B730B357B
title: 'Verifica del supporto delle funzionalità hardware '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b14f0de50c4236c4fce46ceda1896ee32721c3bd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965711"
---
# <a name="checking-hardware-feature-support"></a><span data-ttu-id="c0a6a-103">Verifica del supporto delle funzionalità hardware </span><span class="sxs-lookup"><span data-stu-id="c0a6a-103">Checking Hardware Feature Support</span></span>

<span data-ttu-id="c0a6a-104">Questa sezione illustra come verificare il supporto del formato per l'hardware a livello di funzionalità Direct3D usando le chiamate API.</span><span class="sxs-lookup"><span data-stu-id="c0a6a-104">This section covers how to check on Format Support for Direct3D Feature Level Hardware using API calls.</span></span>

<span data-ttu-id="c0a6a-105">Per D3D11, usare [**ID3D11Device:: CheckFormatSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkformatsupport) per verificare a livello di codice le informazioni nelle sezioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="c0a6a-105">For D3D11, use [**ID3D11Device::CheckFormatSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkformatsupport) to programmatically verify the info in the previous sections.</span></span> <span data-ttu-id="c0a6a-106">Per D3D12 usare [**ID3D12:: CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span><span class="sxs-lookup"><span data-stu-id="c0a6a-106">For D3D12 use [**ID3D12::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c0a6a-107">Formato destinazione</span><span class="sxs-lookup"><span data-stu-id="c0a6a-107">Format target</span></span></th>
<th><span data-ttu-id="c0a6a-108">D3D12</span><span class="sxs-lookup"><span data-stu-id="c0a6a-108">D3D12</span></span></th>
<th><span data-ttu-id="c0a6a-109">D3D11</span><span class="sxs-lookup"><span data-stu-id="c0a6a-109">D3D11</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c0a6a-110">Buffer</span><span class="sxs-lookup"><span data-stu-id="c0a6a-110">Buffer</span></span></td>
<td><span data-ttu-id="c0a6a-111">D3D12_FORMAT_SUPPORT1_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-111">D3D12_FORMAT_SUPPORT1_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-112">D3D11_FORMAT_SUPPORT_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-112">D3D11_FORMAT_SUPPORT_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0a6a-113">Buffer vertici assembler input</span><span class="sxs-lookup"><span data-stu-id="c0a6a-113">Input Assembler Vertex Buffer</span></span></td>
<td><span data-ttu-id="c0a6a-114">D3D12_FORMAT_SUPPORT1_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-114">D3D12_FORMAT_SUPPORT1_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-115">D3D11_FORMAT_SUPPORT_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-115">D3D11_FORMAT_SUPPORT_IA_VERTEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0a6a-116">Buffer indice input assembler</span><span class="sxs-lookup"><span data-stu-id="c0a6a-116">Input Assembler Index Buffer</span></span></td>
<td><span data-ttu-id="c0a6a-117">D3D12_FORMAT_SUPPORT1_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-117">D3D12_FORMAT_SUPPORT1_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-118">D3D11_FORMAT_SUPPORT_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-118">D3D11_FORMAT_SUPPORT_IA_INDEX_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0a6a-119">Buffer output flusso</span><span class="sxs-lookup"><span data-stu-id="c0a6a-119">Stream Output Buffer</span></span></td>
<td><span data-ttu-id="c0a6a-120">D3D12_FORMAT_SUPPORT1_SO_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-120">D3D12_FORMAT_SUPPORT1_SO_BUFFER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-121">D3D11_FORMAT_SUPPORT_SO_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-121">D3D11_FORMAT_SUPPORT_SO_BUFFER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0a6a-122">Texture1D</span><span class="sxs-lookup"><span data-stu-id="c0a6a-122">Texture1D</span></span></td>
<td><span data-ttu-id="c0a6a-123">D3D12_FORMAT_SUPPORT1_TEXTURE1D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-123">D3D12_FORMAT_SUPPORT1_TEXTURE1D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-124">D3D11_FORMAT_SUPPORT_TEXTURE1D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-124">D3D11_FORMAT_SUPPORT_TEXTURE1D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0a6a-125">Texture2D</span><span class="sxs-lookup"><span data-stu-id="c0a6a-125">Texture2D</span></span></td>
<td><span data-ttu-id="c0a6a-126">D3D12_FORMAT_SUPPORT1_TEXTURE2D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-126">D3D12_FORMAT_SUPPORT1_TEXTURE2D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-127">D3D11_FORMAT_SUPPORT_TEXTURE2D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-127">D3D11_FORMAT_SUPPORT_TEXTURE2D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0a6a-128">Texture3D</span><span class="sxs-lookup"><span data-stu-id="c0a6a-128">Texture3D</span></span></td>
<td><span data-ttu-id="c0a6a-129">D3D12_FORMAT_SUPPORT1_TEXTURE3D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-129">D3D12_FORMAT_SUPPORT1_TEXTURE3D (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-130">D3D11_FORMAT_SUPPORT_TEXTURE3D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-130">D3D11_FORMAT_SUPPORT_TEXTURE3D (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0a6a-131">TextureCube</span><span class="sxs-lookup"><span data-stu-id="c0a6a-131">TextureCube</span></span></td>
<td><span data-ttu-id="c0a6a-132">D3D12_FORMAT_SUPPORT1_TEXTURECUBE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-132">D3D12_FORMAT_SUPPORT1_TEXTURECUBE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-133">D3D11_FORMAT_SUPPORT_TEXTURECUBE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-133">D3D11_FORMAT_SUPPORT_TEXTURECUBE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0a6a-134">LD shader</span><span class="sxs-lookup"><span data-stu-id="c0a6a-134">Shader ld</span></span></td>
<td><span data-ttu-id="c0a6a-135">D3D12_FORMAT_SUPPORT1_SHADER_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-135">D3D12_FORMAT_SUPPORT1_SHADER_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-136">D3D11_FORMAT_SUPPORT_SHADER_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-136">D3D11_FORMAT_SUPPORT_SHADER_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0a6a-137">Esempio di shader (qualsiasi filtro)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-137">Shader sample (any filter)</span></span></td>
<td><span data-ttu-id="c0a6a-138">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-138">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-139">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-139">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0a6a-140">Sample_c shader (filtro di confronto)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-140">Shader sample_c (comparison filter)</span></span></td>
<td><span data-ttu-id="c0a6a-141">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-141">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-142">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-142">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0a6a-143">Esempio di shader (mono 1_bit_filter)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-143">Shader sample (mono 1_bit_filter)</span></span></td>
<td><span data-ttu-id="c0a6a-144">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-144">D3D12_FORMAT_SUPPORT1_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-145">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-145">D3D11_FORMAT_SUPPORT_SHADER_SAMPLE_MONO_TEXT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0a6a-146">Shader gather4</span><span class="sxs-lookup"><span data-stu-id="c0a6a-146">Shader gather4</span></span></td>
<td><span data-ttu-id="c0a6a-147">D3D12_FORMAT_SUPPORT1_SHADER_GATHER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-147">D3D12_FORMAT_SUPPORT1_SHADER_GATHER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-148">D3D11_FORMAT_SUPPORT_SHADER_GATHER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-148">D3D11_FORMAT_SUPPORT_SHADER_GATHER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0a6a-149">Gather4_c shader</span><span class="sxs-lookup"><span data-stu-id="c0a6a-149">Shader gather4_c</span></span></td>
<td><span data-ttu-id="c0a6a-150">D3D12_FORMAT_SUPPORT1_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-150">D3D12_FORMAT_SUPPORT1_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-151">D3D11_FORMAT_SUPPORT_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-151">D3D11_FORMAT_SUPPORT_SHADER_GATHER_COMPARISON (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0a6a-152">Mipmap</span><span class="sxs-lookup"><span data-stu-id="c0a6a-152">Mipmap</span></span></td>
<td><span data-ttu-id="c0a6a-153">D3D12_FORMAT_SUPPORT1_MIP (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-153">D3D12_FORMAT_SUPPORT1_MIP (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-154">D3D11_FORMAT_SUPPORT_MIP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-154">D3D11_FORMAT_SUPPORT_MIP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0a6a-155">Generazione automatica mipmap</span><span class="sxs-lookup"><span data-stu-id="c0a6a-155">Mipmap Auto-Generation</span></span></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c0a6a-156">D3D12 non dispone più di una funzionalità di generazione mipmap dedicata.</span><span class="sxs-lookup"><span data-stu-id="c0a6a-156">D3D12 no longer has a dedicated mipmap generation functionality.</span></span> <span data-ttu-id="c0a6a-157">Le applicazioni devono implementarlo autonomamente usando gli shader.</span><span class="sxs-lookup"><span data-stu-id="c0a6a-157">Applications must implement it on their own using shaders.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="c0a6a-158">D3D11_FORMAT_SUPPORT_MIP_AUTOGEN (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-158">D3D11_FORMAT_SUPPORT_MIP_AUTOGEN (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0a6a-159">RenderTarget</span><span class="sxs-lookup"><span data-stu-id="c0a6a-159">RenderTarget</span></span></td>
<td><span data-ttu-id="c0a6a-160">D3D12_FORMAT_SUPPORT1_RENDER_TARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-160">D3D12_FORMAT_SUPPORT1_RENDER_TARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-161">D3D11_FORMAT_SUPPORT_RENDER_TARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-161">D3D11_FORMAT_SUPPORT_RENDER_TARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0a6a-162">RenderTarget blendable</span><span class="sxs-lookup"><span data-stu-id="c0a6a-162">Blendable RenderTarget</span></span></td>
<td><span data-ttu-id="c0a6a-163">D3D12_FORMAT_SUPPORT1_BLENDABLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-163">D3D12_FORMAT_SUPPORT1_BLENDABLE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-164">D3D11_FORMAT_SUPPORT_BLENDABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-164">D3D11_FORMAT_SUPPORT_BLENDABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0a6a-165">Operazione logica di Unione output</span><span class="sxs-lookup"><span data-stu-id="c0a6a-165">Output Merger Logic Op</span></span></td>
<td><span data-ttu-id="c0a6a-166">D3D12_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP</span><span class="sxs-lookup"><span data-stu-id="c0a6a-166">D3D12_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP</span></span></td>
<td><span data-ttu-id="c0a6a-167">D3D11_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-167">D3D11_FORMAT_SUPPORT2_OUTPUT_MERGER_LOGIC_OP (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0a6a-168">Profondità/stencil di destinazione</span><span class="sxs-lookup"><span data-stu-id="c0a6a-168">Depth/Stencil Target</span></span></td>
<td><span data-ttu-id="c0a6a-169">D3D12_FORMAT_SUPPORT1_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-169">D3D12_FORMAT_SUPPORT1_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-170">D3D11_FORMAT_SUPPORT_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-170">D3D11_FORMAT_SUPPORT_DEPTH_STENCIL (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0a6a-171">UAV e SRV non elaborati</span><span class="sxs-lookup"><span data-stu-id="c0a6a-171">Raw UAV and SRV</span></span></td>


</tr>
<tr class="even">
<td><span data-ttu-id="c0a6a-172">UAV strutturato e SRV</span><span class="sxs-lookup"><span data-stu-id="c0a6a-172">Structured UAV and SRV</span></span></td>


</tr>
<tr class="odd">
<td><span data-ttu-id="c0a6a-173">UAV tipizzato</span><span class="sxs-lookup"><span data-stu-id="c0a6a-173">Typed UAV</span></span></td>
<td><span data-ttu-id="c0a6a-174">D3D12_FORMAT_SUPPORT1_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-174">D3D12_FORMAT_SUPPORT1_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-175">D3D11_FORMAT_SUPPORT_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-175">D3D11_FORMAT_SUPPORT_TYPED_UNORDERED_ACCESS_VIEW (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0a6a-176">Archivio con tipi UAV</span><span class="sxs-lookup"><span data-stu-id="c0a6a-176">UAV Typed Store</span></span></td>
<td><span data-ttu-id="c0a6a-177">D3D12_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-177">D3D12_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-178">D3D11_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-178">D3D11_FORMAT_SUPPORT2_UAV_TYPED_STORE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0a6a-179">Caricamento tipizzato UAV</span><span class="sxs-lookup"><span data-stu-id="c0a6a-179">UAV Typed Load</span></span></td>
<td><span data-ttu-id="c0a6a-180">D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-180">D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-181">D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-181">D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0a6a-182">Aggiunta atomica UAV</span><span class="sxs-lookup"><span data-stu-id="c0a6a-182">UAV Atomic Add</span></span></td>
<td><span data-ttu-id="c0a6a-183">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-183">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-184">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-184">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_ADD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0a6a-185">Operazioni bit per bit atomici UAV</span><span class="sxs-lookup"><span data-stu-id="c0a6a-185">UAV Atomic Bitwise Ops</span></span></td>
<td><span data-ttu-id="c0a6a-186">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-186">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-187">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-187">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_BITWISE_OPS (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0a6a-188">UAV Atomic CMP&Store/CMP&Exch</span><span class="sxs-lookup"><span data-stu-id="c0a6a-188">UAV Atomic Cmp&Store/ Cmp&Exch</span></span></td>
<td><span data-ttu-id="c0a6a-189">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-189">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-190">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-190">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_COMPARE_STORE_OR_COMPARE_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0a6a-191">Scambio atomico UAV</span><span class="sxs-lookup"><span data-stu-id="c0a6a-191">UAV Atomic Exchange</span></span></td>
<td><span data-ttu-id="c0a6a-192">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-192">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-193">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-193">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_EXCHANGE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0a6a-194">Min/max con segno atomico UAV</span><span class="sxs-lookup"><span data-stu-id="c0a6a-194">UAV Atomic Signed Min/Max</span></span></td>
<td><span data-ttu-id="c0a6a-195">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-195">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-196">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-196">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_SIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0a6a-197">Min/max senza segno UAV atomico</span><span class="sxs-lookup"><span data-stu-id="c0a6a-197">UAV Atomic Unsigned Min/Max</span></span></td>
<td><span data-ttu-id="c0a6a-198">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-198">D3D12_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-199">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-199">D3D11_FORMAT_SUPPORT2_UAV_ATOMIC_UNSIGNED_MIN_OR_MAX (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0a6a-200">CPU bloccabile</span><span class="sxs-lookup"><span data-stu-id="c0a6a-200">CPU Lockable</span></span></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c0a6a-201">Solo un singolo formato impedisce l'accesso alla CPU (420_OPAQUE).</span><span class="sxs-lookup"><span data-stu-id="c0a6a-201">Only a single format precludes cpu access (420_OPAQUE).</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="c0a6a-202">D3D11_FORMAT_SUPPORT_CPU_LOCKABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-202">D3D11_FORMAT_SUPPORT_CPU_LOCKABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0a6a-203">RenderTarget multisample 4x</span><span class="sxs-lookup"><span data-stu-id="c0a6a-203">4x Multisample RenderTarget</span></span></td>
<td><span data-ttu-id="c0a6a-204">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-204">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-205">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-205">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0a6a-206">RenderTarget multisample 8x</span><span class="sxs-lookup"><span data-stu-id="c0a6a-206">8x Multisample RenderTarget</span></span></td>
<td><span data-ttu-id="c0a6a-207">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-207">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-208">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-208">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0a6a-209">Altro conteggio multisample RT</span><span class="sxs-lookup"><span data-stu-id="c0a6a-209">Other Multisample Count RT</span></span></td>
<td><span data-ttu-id="c0a6a-210">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-210">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-211">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-211">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RENDERTARGET (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0a6a-212">Risoluzione multicampionamento</span><span class="sxs-lookup"><span data-stu-id="c0a6a-212">Multisample Resolve</span></span></td>
<td><span data-ttu-id="c0a6a-213">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-213">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-214">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-214">D3D11_FORMAT_SUPPORT_MULTISAMPLE_RESOLVE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0a6a-215">Carico multicampionamento</span><span class="sxs-lookup"><span data-stu-id="c0a6a-215">Multisample Load</span></span></td>
<td><span data-ttu-id="c0a6a-216">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-216">D3D12_FORMAT_SUPPORT1_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-217">D3D11_FORMAT_SUPPORT_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-217">D3D11_FORMAT_SUPPORT_MULTISAMPLE_LOAD (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0a6a-218">Visualizza Scan-Out</span><span class="sxs-lookup"><span data-stu-id="c0a6a-218">Display Scan-Out</span></span></td>
<td><span data-ttu-id="c0a6a-219">D3D12_FORMAT_SUPPORT1_DISPLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-219">D3D12_FORMAT_SUPPORT1_DISPLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-220">D3D11_FORMAT_SUPPORT_DISPLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-220">D3D11_FORMAT_SUPPORT_DISPLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0a6a-221">Cast nel layout di bit</span><span class="sxs-lookup"><span data-stu-id="c0a6a-221">Cast Within Bit Layout</span></span></td>
<td><span data-ttu-id="c0a6a-222">D3D12_FORMAT_SUPPORT1_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-222">D3D12_FORMAT_SUPPORT1_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-223">D3D11_FORMAT_SUPPORT_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-223">D3D11_FORMAT_SUPPORT_CAST_WITHIN_BIT_LAYOUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0a6a-224">Supporto del decodificatore video</span><span class="sxs-lookup"><span data-stu-id="c0a6a-224">Video Decoder Support</span></span></td>
<td><span data-ttu-id="c0a6a-225">D3D12_FORMAT_SUPPORT1_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-225">D3D12_FORMAT_SUPPORT1_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-226">D3D11_FORMAT_SUPPORT_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-226">D3D11_FORMAT_SUPPORT_DECODER_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0a6a-227">Input del processore video</span><span class="sxs-lookup"><span data-stu-id="c0a6a-227">Video Processor Input</span></span></td>
<td><span data-ttu-id="c0a6a-228">D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-228">D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-229">D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-229">D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_INPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0a6a-230">Output del processore video</span><span class="sxs-lookup"><span data-stu-id="c0a6a-230">Video Processor Output</span></span></td>
<td><span data-ttu-id="c0a6a-231">D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-231">D3D12_FORMAT_SUPPORT1_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-232">D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-232">D3D11_FORMAT_SUPPORT_VIDEO_PROCESSOR_OUTPUT (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0a6a-233">Risorsa condivisa</span><span class="sxs-lookup"><span data-stu-id="c0a6a-233">Shared Resource</span></span></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c0a6a-234">Le trame di tutti i formati possono essere risorse di cui è stato eseguito il commit condiviso o essere inserite negli heap condivisi.</span><span class="sxs-lookup"><span data-stu-id="c0a6a-234">Textures of all formats may be shared committed resources or be placed in shared heaps.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="c0a6a-235">D3D11_FORMAT_SUPPORT2_SHAREABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-235">D3D11_FORMAT_SUPPORT2_SHAREABLE (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0a6a-236">Castabile backBuffer anche completamente tipizzato</span><span class="sxs-lookup"><span data-stu-id="c0a6a-236">BackBuffer Castable Even Fully Typed</span></span></td>
<td><span data-ttu-id="c0a6a-237">D3D12_FORMAT_SUPPORT1_BACK_BUFFER_CAST (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-237">D3D12_FORMAT_SUPPORT1_BACK_BUFFER_CAST (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="c0a6a-238">Non sono disponibili API.</span><span class="sxs-lookup"><span data-stu-id="c0a6a-238">No API available.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0a6a-239">Risorsa affiancata</span><span class="sxs-lookup"><span data-stu-id="c0a6a-239">Tiled Resource</span></span></td>
<td><span data-ttu-id="c0a6a-240">D3D12_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-240">D3D12_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-241">D3D11_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-241">D3D11_FORMAT_SUPPORT2_TILED (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c0a6a-242">Codificatore video</span><span class="sxs-lookup"><span data-stu-id="c0a6a-242">Video Encoder</span></span></td>
<td><span data-ttu-id="c0a6a-243">D3D12_FORMAT_SUPPORT1_VIDEO_ENCODER (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-243">D3D12_FORMAT_SUPPORT1_VIDEO_ENCODER(<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support1"><strong>D3D12_FORMAT_SUPPORT1</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-244">D3D11_FORMAT_SUPPORT_VIDEO_ENCODER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-244">D3D11_FORMAT_SUPPORT_VIDEO_ENCODER (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support"><strong>D3D11_FORMAT_SUPPORT</strong></a>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c0a6a-245">Sovrapposizione multipiano</span><span class="sxs-lookup"><span data-stu-id="c0a6a-245">Multiplane Overlay</span></span></td>
<td><span data-ttu-id="c0a6a-246">D3D12_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-246">D3D12_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2"><strong>D3D12_FORMAT_SUPPORT2</strong></a>)</span></span></td>
<td><span data-ttu-id="c0a6a-247">D3D11_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span><span class="sxs-lookup"><span data-stu-id="c0a6a-247">D3D11_FORMAT_SUPPORT2_MULTIPLANE_OVERLAY (<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2</strong></a>)</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="c0a6a-248">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c0a6a-248">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0a6a-249">Livelli di funzionalità hardware D3D12</span><span class="sxs-lookup"><span data-stu-id="c0a6a-249">D3D12 Hardware Feature Levels</span></span>](/windows/desktop/direct3d12/hardware-feature-levels)
</dt> <dt>

[<span data-ttu-id="c0a6a-250">**\_formato DXGI**</span><span class="sxs-lookup"><span data-stu-id="c0a6a-250">**DXGI\_FORMAT**</span></span>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)
</dt> <dt>

[<span data-ttu-id="c0a6a-251">**\_Supporto del formato d3d11 \_**</span><span class="sxs-lookup"><span data-stu-id="c0a6a-251">**D3D11\_FORMAT\_SUPPORT**</span></span>](/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support)
</dt> <dt>

[<span data-ttu-id="c0a6a-252">**\_Formato d3d11 \_ SUPPORT2**</span><span class="sxs-lookup"><span data-stu-id="c0a6a-252">**D3D11\_FORMAT\_SUPPORT2**</span></span>](/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2)
</dt> <dt>

[<span data-ttu-id="c0a6a-253">Guida per programmatori per DXGI</span><span class="sxs-lookup"><span data-stu-id="c0a6a-253">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
</dt> </dl>

