---
title: Interfacce shader (grafica Direct3D 12)
description: D3d12shader. h dichiara le interfacce seguenti.
ms.assetid: 791d2c91-3791-47fe-b887-8117ecc798ba
keywords:
- interfacce, Direct3D 12 shader
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16f111572aacca36f12600b0cf334895684064e5
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300836"
---
# <a name="shader-interfaces-direct3d-12-graphics"></a><span data-ttu-id="7e749-104">Interfacce shader (grafica Direct3D 12)</span><span class="sxs-lookup"><span data-stu-id="7e749-104">Shader Interfaces (Direct3D 12 Graphics)</span></span>

<span data-ttu-id="7e749-105">d3d12shader. h dichiara le interfacce seguenti.</span><span class="sxs-lookup"><span data-stu-id="7e749-105">d3d12shader.h declares the following interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7e749-106">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="7e749-106">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7e749-107">Argomento</span><span class="sxs-lookup"><span data-stu-id="7e749-107">Topic</span></span></th>
<th><span data-ttu-id="7e749-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e749-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7e749-109"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionparameterreflection"><strong>ID3D12FunctionParameterReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e749-109"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionparameterreflection"><strong>ID3D12FunctionParameterReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="7e749-110">Un'interfaccia function-parameter-Reflection accede alle informazioni sul parametro della funzione.</span><span class="sxs-lookup"><span data-stu-id="7e749-110">A function-parameter-reflection interface accesses function-parameter info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7e749-111">Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 12 per creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7e749-111">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e749-112"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection"><strong>ID3D12FunctionReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e749-112"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12functionreflection"><strong>ID3D12FunctionReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="7e749-113">Un'interfaccia di reflection di funzione accede alle informazioni sulla funzione.</span><span class="sxs-lookup"><span data-stu-id="7e749-113">A function-reflection interface accesses function info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7e749-114">Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 12 per creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7e749-114">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e749-115"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12libraryreflection"><strong>ID3D12LibraryReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e749-115"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12libraryreflection"><strong>ID3D12LibraryReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="7e749-116">Un'interfaccia di reflection di libreria accede alle informazioni della libreria.</span><span class="sxs-lookup"><span data-stu-id="7e749-116">A library-reflection interface accesses library info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7e749-117">Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 12 per creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="7e749-117">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e749-118"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection"><strong>ID3D12ShaderReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e749-118"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflection"><strong>ID3D12ShaderReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="7e749-119">Un'interfaccia di Reflection shader accede alle informazioni sullo shader.</span><span class="sxs-lookup"><span data-stu-id="7e749-119">A shader-reflection interface accesses shader information.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e749-120"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer"><strong>ID3D12ShaderReflectionConstantBuffer</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e749-120"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionconstantbuffer"><strong>ID3D12ShaderReflectionConstantBuffer</strong></a></span></span><br/></td>
<td><span data-ttu-id="7e749-121">Questa interfaccia di Reflection shader fornisce l'accesso a un buffer costante.</span><span class="sxs-lookup"><span data-stu-id="7e749-121">This shader-reflection interface provides access to a constant buffer.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e749-122"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectiontype"><strong>ID3D12ShaderReflectionType</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e749-122"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectiontype"><strong>ID3D12ShaderReflectionType</strong></a></span></span><br/></td>
<td><span data-ttu-id="7e749-123">Questa interfaccia di Reflection shader consente di accedere al tipo di variabile.</span><span class="sxs-lookup"><span data-stu-id="7e749-123">This shader-reflection interface provides access to variable type.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e749-124"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable"><strong>ID3D12ShaderReflectionVariable</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e749-124"><a href="/windows/desktop/api/d3d12shader/nn-d3d12shader-id3d12shaderreflectionvariable"><strong>ID3D12ShaderReflectionVariable</strong></a></span></span><br/></td>
<td><span data-ttu-id="7e749-125">Questa interfaccia di Reflection shader consente di accedere a una variabile.</span><span class="sxs-lookup"><span data-stu-id="7e749-125">This shader-reflection interface provides access to a variable.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="7e749-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7e749-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e749-127">Guida di riferimento a Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="7e749-127">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> <dt>

[<span data-ttu-id="7e749-128">Riferimento shader</span><span class="sxs-lookup"><span data-stu-id="7e749-128">Shader Reference</span></span>](d3d12-graphics-reference-shader-reference.md)
</dt> </dl>

 

 





