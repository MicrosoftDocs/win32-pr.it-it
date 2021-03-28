---
title: 'Interfacce shader (grafica Direct3D 11) '
description: Questa sezione contiene informazioni sulle interfacce dello shader.
ms.assetid: 1791d2c9-3791-47fe-b887-a8117ecc798b
keywords:
- interfacce, Direct3D 11 shader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d55e591d56442b641482a76a4ec93c0055029fc0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400119"
---
# <a name="shader-interfaces-direct3d-11-graphics"></a><span data-ttu-id="81c00-104">Interfacce shader (grafica Direct3D 11) </span><span class="sxs-lookup"><span data-stu-id="81c00-104">Shader Interfaces (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="81c00-105">Questa sezione contiene informazioni sulle interfacce dello shader.</span><span class="sxs-lookup"><span data-stu-id="81c00-105">This section contains information about the shader interfaces.</span></span>

<span data-ttu-id="81c00-106">Ognuna di queste interfacce shader gestisce uno shader compilato.</span><span class="sxs-lookup"><span data-stu-id="81c00-106">Each of these shader interfaces manages a compiled shader.</span></span> <span data-ttu-id="81c00-107">L'interfaccia viene creata quando viene compilato uno shader e viene quindi passata a diverse API che necessitano dell'accesso a uno shader compilato. ad esempio quando si associa uno shader a una fase della pipeline o si recupera una firma dello shader.</span><span class="sxs-lookup"><span data-stu-id="81c00-107">The interface is created when a shader is compiled, and is then passed to various APIs that need access to a compiled shader; such as when binding a shader to a pipeline stage or getting a shader signature.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="81c00-108">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="81c00-108">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="81c00-109">Argomento</span><span class="sxs-lookup"><span data-stu-id="81c00-109">Topic</span></span></th>
<th><span data-ttu-id="81c00-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81c00-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="81c00-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance"><strong>ID3D11ClassInstance</strong></a></span><span class="sxs-lookup"><span data-stu-id="81c00-111"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance"><strong>ID3D11ClassInstance</strong></a></span></span><br/></td>
<td><span data-ttu-id="81c00-112">Questa interfaccia incapsula una classe HLSL.</span><span class="sxs-lookup"><span data-stu-id="81c00-112">This interface encapsulates an HLSL class.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c00-113"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage"><strong>ID3D11ClassLinkage</strong></a></span><span class="sxs-lookup"><span data-stu-id="81c00-113"><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage"><strong>ID3D11ClassLinkage</strong></a></span></span><br/></td>
<td><span data-ttu-id="81c00-114">Questa interfaccia incapsula un collegamento dinamico HLSL.</span><span class="sxs-lookup"><span data-stu-id="81c00-114">This interface encapsulates an HLSL dynamic linkage.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81c00-115"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader"><strong>ID3D11ComputeShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="81c00-115"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11computeshader"><strong>ID3D11ComputeShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="81c00-116">Un'interfaccia compute shader gestisce un programma eseguibile (Compute Shader) che controlla la fase compute shader.</span><span class="sxs-lookup"><span data-stu-id="81c00-116">A compute-shader interface manages an executable program (a compute shader) that controls the compute-shader stage.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c00-117"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader"><strong>ID3D11DomainShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="81c00-117"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11domainshader"><strong>ID3D11DomainShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="81c00-118">Un'interfaccia di shader Domain gestisce un programma eseguibile (un Domain shader) che controlla la fase del dominio shader.</span><span class="sxs-lookup"><span data-stu-id="81c00-118">A domain-shader interface manages an executable program (a domain shader) that controls the domain-shader stage.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81c00-119"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a></span><span class="sxs-lookup"><span data-stu-id="81c00-119"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a></span></span><br/></td>
<td><span data-ttu-id="81c00-120">Per costruire shader costituiti da una sequenza di chiamate di funzione precompilate che passano i valori tra loro, viene utilizzata un'interfaccia Graph di collegamento a funzioni.</span><span class="sxs-lookup"><span data-stu-id="81c00-120">A function-linking-graph interface is used for constructing shaders that consist of a sequence of precompiled function calls that pass values to each other.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="81c00-121">Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="81c00-121">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c00-122"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionreflection"><strong>ID3D11FunctionReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="81c00-122"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionreflection"><strong>ID3D11FunctionReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="81c00-123">Un'interfaccia di reflection di funzione accede alle informazioni sulla funzione.</span><span class="sxs-lookup"><span data-stu-id="81c00-123">A function-reflection interface accesses function info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="81c00-124">Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="81c00-124">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81c00-125"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionparameterreflection"><strong>ID3D11FunctionParameterReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="81c00-125"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionparameterreflection"><strong>ID3D11FunctionParameterReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="81c00-126">Un'interfaccia function-parameter-Reflection accede alle informazioni sul parametro della funzione.</span><span class="sxs-lookup"><span data-stu-id="81c00-126">A function-parameter-reflection interface accesses function-parameter info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="81c00-127">Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="81c00-127">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c00-128"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader"><strong>ID3D11GeometryShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="81c00-128"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11geometryshader"><strong>ID3D11GeometryShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="81c00-129">Un'interfaccia geometry shader gestisce un programma eseguibile (Geometry shader) che controlla la fase geometry-shader.</span><span class="sxs-lookup"><span data-stu-id="81c00-129">A geometry-shader interface manages an executable program (a geometry shader) that controls the geometry-shader stage.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81c00-130"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader"><strong>ID3D11HullShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="81c00-130"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11hullshader"><strong>ID3D11HullShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="81c00-131">Un'interfaccia Hull shader gestisce un programma eseguibile (uno scafo) che controlla la fase Hull shader.</span><span class="sxs-lookup"><span data-stu-id="81c00-131">A hull-shader interface manages an executable program (a hull shader) that controls the hull-shader stage.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c00-132"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11libraryreflection"><strong>ID3D11LibraryReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="81c00-132"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11libraryreflection"><strong>ID3D11LibraryReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="81c00-133">Un'interfaccia di reflection di libreria accede alle informazioni della libreria.</span><span class="sxs-lookup"><span data-stu-id="81c00-133">A library-reflection interface accesses library info.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="81c00-134">Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="81c00-134">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81c00-135"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a></span><span class="sxs-lookup"><span data-stu-id="81c00-135"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a></span></span><br/></td>
<td><span data-ttu-id="81c00-136">Viene usata un'interfaccia del linker per collegare un modulo shader.</span><span class="sxs-lookup"><span data-stu-id="81c00-136">A linker interface is used to link a shader module.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="81c00-137">Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="81c00-137">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c00-138"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linkingnode"><strong>ID3D11LinkingNode</strong></a></span><span class="sxs-lookup"><span data-stu-id="81c00-138"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linkingnode"><strong>ID3D11LinkingNode</strong></a></span></span><br/></td>
<td><span data-ttu-id="81c00-139">Per il collegamento dello shader viene utilizzata un'interfaccia del nodo di collegamento.</span><span class="sxs-lookup"><span data-stu-id="81c00-139">A linking-node interface is used for shader linking.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="81c00-140">Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="81c00-140">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81c00-141"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module"><strong>ID3D11Module</strong></a></span><span class="sxs-lookup"><span data-stu-id="81c00-141"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module"><strong>ID3D11Module</strong></a></span></span><br/></td>
<td><span data-ttu-id="81c00-142">Un'interfaccia del modulo crea un'istanza di un modulo usato per la riassociazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="81c00-142">A module interface creates an instance of a module that is used for resource rebinding.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="81c00-143">Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="81c00-143">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c00-144"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance"><strong>ID3D11ModuleInstance</strong></a></span><span class="sxs-lookup"><span data-stu-id="81c00-144"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance"><strong>ID3D11ModuleInstance</strong></a></span></span><br/></td>
<td><span data-ttu-id="81c00-145">Per la riassociazione delle risorse viene usata un'interfaccia di istanza modulo.</span><span class="sxs-lookup"><span data-stu-id="81c00-145">A module-instance interface is used for resource rebinding.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="81c00-146">Questa interfaccia fa parte della tecnologia di collegamento dello shader HLSL che è possibile usare in tutte le piattaforme Direct3D 11 per creare funzioni HLSL precompilate, assemblarle in librerie e collegarle in shader completi in fase di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="81c00-146">This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81c00-147"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader"><strong>ID3D11PixelShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="81c00-147"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11pixelshader"><strong>ID3D11PixelShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="81c00-148">Un'interfaccia pixel shader gestisce un programma eseguibile (un pixel shader) che controlla la fase pixel shader.</span><span class="sxs-lookup"><span data-stu-id="81c00-148">A pixel-shader interface manages an executable program (a pixel shader) that controls the pixel-shader stage.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c00-149"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflection"><strong>ID3D11ShaderReflection</strong></a></span><span class="sxs-lookup"><span data-stu-id="81c00-149"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflection"><strong>ID3D11ShaderReflection</strong></a></span></span><br/></td>
<td><span data-ttu-id="81c00-150">Un'interfaccia di Reflection shader accede alle informazioni sullo shader.</span><span class="sxs-lookup"><span data-stu-id="81c00-150">A shader-reflection interface accesses shader information.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81c00-151"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer"><strong>ID3D11ShaderReflectionConstantBuffer</strong></a></span><span class="sxs-lookup"><span data-stu-id="81c00-151"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionconstantbuffer"><strong>ID3D11ShaderReflectionConstantBuffer</strong></a></span></span><br/></td>
<td><span data-ttu-id="81c00-152">Questa interfaccia di Reflection shader fornisce l'accesso a un buffer costante.</span><span class="sxs-lookup"><span data-stu-id="81c00-152">This shader-reflection interface provides access to a constant buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c00-153"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectiontype"><strong>ID3D11ShaderReflectionType</strong></a></span><span class="sxs-lookup"><span data-stu-id="81c00-153"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectiontype"><strong>ID3D11ShaderReflectionType</strong></a></span></span><br/></td>
<td><span data-ttu-id="81c00-154">Questa interfaccia di Reflection shader consente di accedere al tipo di variabile.</span><span class="sxs-lookup"><span data-stu-id="81c00-154">This shader-reflection interface provides access to variable type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81c00-155"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionvariable"><strong>ID3D11ShaderReflectionVariable</strong></a></span><span class="sxs-lookup"><span data-stu-id="81c00-155"><a href="/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11shaderreflectionvariable"><strong>ID3D11ShaderReflectionVariable</strong></a></span></span><br/></td>
<td><span data-ttu-id="81c00-156">Questa interfaccia di Reflection shader consente di accedere a una variabile.</span><span class="sxs-lookup"><span data-stu-id="81c00-156">This shader-reflection interface provides access to a variable.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c00-157"><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a></span><span class="sxs-lookup"><span data-stu-id="81c00-157"><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a></span></span><br/></td>
<td><span data-ttu-id="81c00-158">Un'interfaccia <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a> implementa i metodi per ottenere tracce di esecuzioni dello shader.</span><span class="sxs-lookup"><span data-stu-id="81c00-158">An <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertrace"><strong>ID3D11ShaderTrace</strong></a> interface implements methods for obtaining traces of shader executions.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="81c00-159"><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a></span><span class="sxs-lookup"><span data-stu-id="81c00-159"><a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a></span></span><br/></td>
<td><span data-ttu-id="81c00-160">Un'interfaccia <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a> implementa un metodo per la generazione di oggetti di informazioni di traccia dello shader.</span><span class="sxs-lookup"><span data-stu-id="81c00-160">An <a href="/windows/desktop/api/D3D11ShaderTracing/nn-d3d11shadertracing-id3d11shadertracefactory"><strong>ID3D11ShaderTraceFactory</strong></a> interface implements a method for generating shader trace information objects.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="81c00-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader"><strong>ID3D11VertexShader</strong></a></span><span class="sxs-lookup"><span data-stu-id="81c00-161"><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader"><strong>ID3D11VertexShader</strong></a></span></span><br/></td>
<td><span data-ttu-id="81c00-162">Un'interfaccia vertex shader gestisce un programma eseguibile (Vertex shader) che controlla la fase vertex shader.</span><span class="sxs-lookup"><span data-stu-id="81c00-162">A vertex-shader interface manages an executable program (a vertex shader) that controls the vertex-shader stage.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="81c00-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="81c00-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81c00-164">Riferimento shader</span><span class="sxs-lookup"><span data-stu-id="81c00-164">Shader Reference</span></span>](d3d11-graphics-reference-d3d11-shader.md)
</dt> </dl>

 

