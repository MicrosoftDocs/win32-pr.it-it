---
title: Funzioni D3DX (grafica Direct3D 11)
description: Questa sezione contiene informazioni sulle funzioni D3DX 11.
ms.assetid: 7548c02e-c8c2-4629-95ac-d21ca7a39f0a
keywords:
- funzioni, DirectX 11 D3DX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b76c1764f464461b4800a9161ac37dcff8c539a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400062"
---
# <a name="d3dx-functions-direct3d-11-graphics"></a><span data-ttu-id="75ce6-104">Funzioni D3DX (grafica Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="75ce6-104">D3DX Functions (Direct3D 11 Graphics)</span></span>

<span data-ttu-id="75ce6-105">Questa sezione contiene informazioni sulle funzioni D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="75ce6-105">This section contains information about the D3DX 11 functions.</span></span>

> [!Note]  
> <span data-ttu-id="75ce6-106">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-106">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 


## <a name="in-this-section"></a><span data-ttu-id="75ce6-107">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="75ce6-107">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="75ce6-108">Argomento</span><span class="sxs-lookup"><span data-stu-id="75ce6-108">Topic</span></span></th>
<th><span data-ttu-id="75ce6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75ce6-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="75ce6-110"><a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-110"><a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-111">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-111">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-112">Invece di usare questa funzione, è consigliabile eseguire la compilazione offline usando il Fxc.exe compilatore da riga di comando o una delle API di compilazione HLSL, ad esempio l'API <a href="/windows/desktop/direct3dhlsl/d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="75ce6-112">Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the <a href="/windows/desktop/direct3dhlsl/d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-113">Compilare uno shader o un effetto da un file.</span><span class="sxs-lookup"><span data-stu-id="75ce6-113">Compile a shader or an effect from a file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ce6-114"><a href="d3dx11compilefrommemory.md"><strong>D3DX11CompileFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-114"><a href="d3dx11compilefrommemory.md"><strong>D3DX11CompileFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-115">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-115">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-116">Invece di usare questa funzione, è consigliabile eseguire la compilazione offline usando il Fxc.exe compilatore da riga di comando o una delle API di compilazione HLSL, ad esempio l'API <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="75ce6-116">Instead of using this function, we recommend that you compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-117">Compilare uno shader o un effetto caricato in memoria.</span><span class="sxs-lookup"><span data-stu-id="75ce6-117">Compile a shader or an effect that is loaded in memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ce6-118"><a href="d3dx11compilefromresource.md"><strong>D3DX11CompileFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-118"><a href="d3dx11compilefromresource.md"><strong>D3DX11CompileFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-119">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-119">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-120">Invece di usare questa funzione, è consigliabile usare le <a href="/windows/desktop/menurc/resources-functions">funzioni di risorsa</a>, quindi compilare offline usando il Fxc.exe compilatore della riga di comando o usare una delle API di compilazione HLSL, ad esempio l'API <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="75ce6-120">Instead of using this function, we recommend that you use <a href="/windows/desktop/menurc/resources-functions">resource functions</a>, then compile offline by using the Fxc.exe command-line compiler or use one of the HLSL compile APIs, like the <a href="/windows/desktop/direct3dhlsl/d3dcompile"><strong>D3DCompile</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-121">Compilare uno shader o un effetto da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="75ce6-121">Compile a shader or an effect from a resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ce6-122"><a href="d3dx11computenormalmap.md"><strong>D3DX11ComputeNormalMap</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-122"><a href="d3dx11computenormalmap.md"><strong>D3DX11ComputeNormalMap</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-123">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-123">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-124">Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>ComputeNormalMap</strong>.</span><span class="sxs-lookup"><span data-stu-id="75ce6-124">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>ComputeNormalMap</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-125">Converte una mappa di altezza in una mappa normale.</span><span class="sxs-lookup"><span data-stu-id="75ce6-125">Converts a height map into a normal map.</span></span> <span data-ttu-id="75ce6-126">Ai componenti (x, y, z) di ogni normale viene eseguito il mapping ai canali (r, g, b) della trama di output.</span><span class="sxs-lookup"><span data-stu-id="75ce6-126">The (x,y,z) components of each normal are mapped to the (r,g,b) channels of the output texture.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ce6-127"><a href="d3dx11createasynccompilerprocessor.md"><strong>D3DX11CreateAsyncCompilerProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-127"><a href="d3dx11createasynccompilerprocessor.md"><strong>D3DX11CreateAsyncCompilerProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-128">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-128">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="75ce6-129">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="75ce6-129">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-130">Creare un processore di dati asincrono per uno shader.</span><span class="sxs-lookup"><span data-stu-id="75ce6-130">Create an asynchronous-data processor for a shader.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ce6-131"><a href="d3dx11createasyncfileloader.md"><strong>D3DX11CreateAsyncFileLoader</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-131"><a href="d3dx11createasyncfileloader.md"><strong>D3DX11CreateAsyncFileLoader</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-132">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-132">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="75ce6-133">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="75ce6-133">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-134">Creare un caricatore di file asincrono.</span><span class="sxs-lookup"><span data-stu-id="75ce6-134">Create an asynchronous-file loader.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ce6-135"><a href="d3dx11createasyncmemoryloader.md"><strong>D3DX11CreateAsyncMemoryLoader</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-135"><a href="d3dx11createasyncmemoryloader.md"><strong>D3DX11CreateAsyncMemoryLoader</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-136">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-136">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="75ce6-137">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="75ce6-137">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-138">Creare un caricatore di memoria asincrono.</span><span class="sxs-lookup"><span data-stu-id="75ce6-138">Create an asynchronous-memory loader.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ce6-139"><a href="d3dx11createasyncresourceloader.md"><strong>D3DX11CreateAsyncResourceLoader</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-139"><a href="d3dx11createasyncresourceloader.md"><strong>D3DX11CreateAsyncResourceLoader</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-140">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-140">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="75ce6-141">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="75ce6-141">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-142">Creare un caricatore di risorse asincrono.</span><span class="sxs-lookup"><span data-stu-id="75ce6-142">Create an asynchronous-resource loader.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ce6-143"><a href="d3dx11createasyncshaderpreprocessprocessor.md"><strong>D3DX11CreateAsyncShaderPreprocessProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-143"><a href="d3dx11createasyncshaderpreprocessprocessor.md"><strong>D3DX11CreateAsyncShaderPreprocessProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-144">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-144">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="75ce6-145">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="75ce6-145">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-146">Creare un elaboratore di dati per uno shader in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="75ce6-146">Create a data processor for a shader asynchronously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ce6-147"><a href="d3dx11createasynctextureinfoprocessor.md"><strong>D3DX11CreateAsyncTextureInfoProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-147"><a href="d3dx11createasynctextureinfoprocessor.md"><strong>D3DX11CreateAsyncTextureInfoProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-148">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-148">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="75ce6-149">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="75ce6-149">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-150">Creare un elaboratore di dati da utilizzare con una <a href="id3dx11threadpump.md"><strong>pompa di thread</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="75ce6-150">Create a data processor to be used with a <a href="id3dx11threadpump.md"><strong>thread pump</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ce6-151"><a href="d3dx11createasynctextureprocessor.md"><strong>D3DX11CreateAsyncTextureProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-151"><a href="d3dx11createasynctextureprocessor.md"><strong>D3DX11CreateAsyncTextureProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-152">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-152">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="75ce6-153">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="75ce6-153">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-154">Creare un elaboratore di dati da utilizzare con una <a href="id3dx11threadpump.md"><strong>pompa di thread</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="75ce6-154">Create a data processor to be used with a <a href="id3dx11threadpump.md"><strong>thread pump</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ce6-155"><a href="d3dx11createasyncshaderresourceviewprocessor.md"><strong>D3DX11CreateAsyncShaderResourceViewProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-155"><a href="d3dx11createasyncshaderresourceviewprocessor.md"><strong>D3DX11CreateAsyncShaderResourceViewProcessor</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-156">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-156">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="75ce6-157">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="75ce6-157">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-158">Creare un elaboratore di dati che caricherà una risorsa e quindi crei una visualizzazione delle risorse shader.</span><span class="sxs-lookup"><span data-stu-id="75ce6-158">Create a data processor that will load a resource and then create a shader-resource view for it.</span></span> <span data-ttu-id="75ce6-159">I processori di dati sono un componente della funzionalità asincrona di caricamento dei dati in D3DX11 che usa le <a href="id3dx11threadpump.md"><strong>pompe di thread</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="75ce6-159">Data processors are a component of the asynchronous data loading feature in D3DX11 that uses <a href="id3dx11threadpump.md"><strong>thread pumps</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ce6-160"><a href="d3dx11createshaderresourceviewfromfile.md"><strong>D3DX11CreateShaderResourceViewFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-160"><a href="d3dx11createshaderresourceviewfromfile.md"><strong>D3DX11CreateShaderResourceViewFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-161">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-161">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="75ce6-162">Anziché utilizzare questa funzione, è consigliabile utilizzare le seguenti operazioni:</span><span class="sxs-lookup"><span data-stu-id="75ce6-162">Instead of using this function, we recommend that you use these:</span></span></p>
<ul>
<li><span data-ttu-id="75ce6-163">Libreria <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMFILE</strong> (dove xxx è DDS o WIC)</span><span class="sxs-lookup"><span data-stu-id="75ce6-163"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromFile</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="75ce6-164">Libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (strumenti), <strong>LOADFROMXXXFILE</strong> (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi, quindi <strong>CreateShaderResourceView</strong></span><span class="sxs-lookup"><span data-stu-id="75ce6-164"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXFile</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateShaderResourceView</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="75ce6-165">Creare una visualizzazione risorse shader da un file.</span><span class="sxs-lookup"><span data-stu-id="75ce6-165">Create a shader-resource view from a file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ce6-166"><a href="d3dx11createshaderresourceviewfrommemory.md"><strong>D3DX11CreateShaderResourceViewFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-166"><a href="d3dx11createshaderresourceviewfrommemory.md"><strong>D3DX11CreateShaderResourceViewFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-167">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-167">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="75ce6-168">Anziché utilizzare questa funzione, è consigliabile utilizzare le seguenti operazioni:</span><span class="sxs-lookup"><span data-stu-id="75ce6-168">Instead of using this function, we recommend that you use these:</span></span></p>
<ul>
<li><span data-ttu-id="75ce6-169">Libreria <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMMEMORY</strong> (dove xxx è DDS o WIC)</span><span class="sxs-lookup"><span data-stu-id="75ce6-169"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromMemory</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="75ce6-170">Libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (strumenti), <strong>LOADFROMXXXMEMORY</strong> (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi, quindi <strong>CreateShaderResourceView</strong></span><span class="sxs-lookup"><span data-stu-id="75ce6-170"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateShaderResourceView</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="75ce6-171">Creare una visualizzazione risorse shader da un file in memoria.</span><span class="sxs-lookup"><span data-stu-id="75ce6-171">Create a shader-resource view from a file in memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ce6-172"><a href="d3dx11createshaderresourceviewfromresource.md"><strong>D3DX11CreateShaderResourceViewFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-172"><a href="d3dx11createshaderresourceviewfromresource.md"><strong>D3DX11CreateShaderResourceViewFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-173">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-173">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="75ce6-174">Anziché utilizzare questa funzione, è consigliabile utilizzare le funzioni della <a href="/windows/desktop/menurc/resources-functions">risorsa</a>, quindi:</span><span class="sxs-lookup"><span data-stu-id="75ce6-174">Instead of using this function, we recommend that you use <a href="/windows/desktop/menurc/resources-functions">resource functions</a>, then these:</span></span></p>
<ul>
<li><span data-ttu-id="75ce6-175">Libreria <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMMEMORY</strong> (dove xxx è DDS o WIC)</span><span class="sxs-lookup"><span data-stu-id="75ce6-175"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromMemory</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="75ce6-176">Libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (strumenti), <strong>LOADFROMXXXMEMORY</strong> (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi, quindi <strong>CreateShaderResourceView</strong></span><span class="sxs-lookup"><span data-stu-id="75ce6-176"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateShaderResourceView</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="75ce6-177">Creare una visualizzazione risorse shader da una risorsa.</span><span class="sxs-lookup"><span data-stu-id="75ce6-177">Create a shader-resource view from a resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ce6-178"><a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-178"><a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-179">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-179">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="75ce6-180">Anziché utilizzare questa funzione, è consigliabile utilizzare le seguenti operazioni:</span><span class="sxs-lookup"><span data-stu-id="75ce6-180">Instead of using this function, we recommend that you use these:</span></span></p>
<ul>
<li><span data-ttu-id="75ce6-181">Libreria <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMFILE</strong> (dove xxx è DDS o WIC)</span><span class="sxs-lookup"><span data-stu-id="75ce6-181"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromFile</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="75ce6-182">Libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (strumenti), <strong>LOADFROMXXXFILE</strong> (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi, quindi <strong>createTexture</strong></span><span class="sxs-lookup"><span data-stu-id="75ce6-182"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXFile</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateTexture</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="75ce6-183">Creare una risorsa di trama da un file.</span><span class="sxs-lookup"><span data-stu-id="75ce6-183">Create a texture resource from a file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ce6-184"><a href="d3dx11createtexturefrommemory.md"><strong>D3DX11CreateTextureFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-184"><a href="d3dx11createtexturefrommemory.md"><strong>D3DX11CreateTextureFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-185">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-185">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="75ce6-186">Anziché utilizzare questa funzione, è consigliabile utilizzare le seguenti operazioni:</span><span class="sxs-lookup"><span data-stu-id="75ce6-186">Instead of using this function, we recommend that you use these:</span></span></p>
<ul>
<li><span data-ttu-id="75ce6-187">Libreria <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMMEMORY</strong> (dove xxx è DDS o WIC)</span><span class="sxs-lookup"><span data-stu-id="75ce6-187"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromMemory</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="75ce6-188">Libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (strumenti), <strong>LOADFROMXXXMEMORY</strong> (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi, quindi <strong>createTexture</strong></span><span class="sxs-lookup"><span data-stu-id="75ce6-188"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateTexture</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="75ce6-189">Creare una risorsa di trama da un file che risiede nella memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="75ce6-189">Create a texture resource from a file residing in system memory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ce6-190"><a href="d3dx11createtexturefromresource.md"><strong>D3DX11CreateTextureFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-190"><a href="d3dx11createtexturefromresource.md"><strong>D3DX11CreateTextureFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-191">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-191">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
<p>[!Note]<br />
<span data-ttu-id="75ce6-192">Anziché utilizzare questa funzione, è consigliabile utilizzare le funzioni della <a href="/windows/desktop/menurc/resources-functions">risorsa</a>, quindi:</span><span class="sxs-lookup"><span data-stu-id="75ce6-192">Instead of using this function, we recommend that you use <a href="/windows/desktop/menurc/resources-functions">resource functions</a>, then these:</span></span></p>
<ul>
<li><span data-ttu-id="75ce6-193">Libreria <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> (Runtime), <strong>CREATEXXXTEXTUREFROMMEMORY</strong> (dove xxx è DDS o WIC)</span><span class="sxs-lookup"><span data-stu-id="75ce6-193"><a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library (runtime), <strong>CreateXXXTextureFromMemory</strong> (where XXX is DDS or WIC)</span></span></li>
<li><span data-ttu-id="75ce6-194">Libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (strumenti), <strong>LOADFROMXXXMEMORY</strong> (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi, quindi <strong>createTexture</strong></span><span class="sxs-lookup"><span data-stu-id="75ce6-194"><a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games) then <strong>CreateTexture</strong></span></span></li>
</ul>
</blockquote>
<br/> <span data-ttu-id="75ce6-195">Creare una trama da un'altra risorsa.</span><span class="sxs-lookup"><span data-stu-id="75ce6-195">Create a texture from another resource.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ce6-196"><a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-196"><a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-197">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-197">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="75ce6-198">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="75ce6-198">See Remarks.</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-199">Creare una pompa di thread.</span><span class="sxs-lookup"><span data-stu-id="75ce6-199">Create a thread pump.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ce6-200"><a href="d3dx11filtertexture.md"><strong>D3DX11FilterTexture</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-200"><a href="d3dx11filtertexture.md"><strong>D3DX11FilterTexture</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-201">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-201">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-202">Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>GenerateMipMaps</strong> e <strong>GenerateMipMaps3D</strong>.</span><span class="sxs-lookup"><span data-stu-id="75ce6-202">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>GenerateMipMaps</strong> and <strong>GenerateMipMaps3D</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-203">Genera la catena mipmap usando un filtro di trama particolare.</span><span class="sxs-lookup"><span data-stu-id="75ce6-203">Generates mipmap chain using a particular texture filter.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ce6-204"><a href="d3dx11getimageinfofromfile.md"><strong>D3DX11GetImageInfoFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-204"><a href="d3dx11getimageinfofromfile.md"><strong>D3DX11GetImageInfoFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-205">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-205">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-206">Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>GETMETADATAFROMXXXFILE</strong> (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi.</span><span class="sxs-lookup"><span data-stu-id="75ce6-206">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>GetMetadataFromXXXFile</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-207">Recupera le informazioni su un file di immagine specificato.</span><span class="sxs-lookup"><span data-stu-id="75ce6-207">Retrieves information about a given image file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ce6-208"><a href="d3dx11getimageinfofrommemory.md"><strong>D3DX11GetImageInfoFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-208"><a href="d3dx11getimageinfofrommemory.md"><strong>D3DX11GetImageInfoFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-209">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-209">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-210">Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>GETMETADATAFROMXXXMEMORY</strong> (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi.</span><span class="sxs-lookup"><span data-stu-id="75ce6-210">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>GetMetadataFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-211">Ottenere informazioni su un'immagine già caricata in memoria.</span><span class="sxs-lookup"><span data-stu-id="75ce6-211">Get information about an image already loaded into memory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ce6-212"><a href="d3dx11getimageinfofromresource.md"><strong>D3DX11GetImageInfoFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-212"><a href="d3dx11getimageinfofromresource.md"><strong>D3DX11GetImageInfoFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-213">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-213">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-214">Anziché utilizzare questa funzione, è consigliabile utilizzare le funzioni della <a href="/windows/desktop/menurc/resources-functions">risorsa</a>, quindi utilizzare la libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> (strumenti), <strong>LOADFROMXXXMEMORY</strong> (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi.</span><span class="sxs-lookup"><span data-stu-id="75ce6-214">Instead of using this function, we recommend that you use <a href="/windows/desktop/menurc/resources-functions">resource functions</a>, then use <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library (tools), <strong>LoadFromXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-215">Recupera le informazioni su una determinata immagine in una risorsa.</span><span class="sxs-lookup"><span data-stu-id="75ce6-215">Retrieves information about a given image in a resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ce6-216"><a href="d3dx11loadtexturefromtexture.md"><strong>D3DX11LoadTextureFromTexture</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-216"><a href="d3dx11loadtexturefromtexture.md"><strong>D3DX11LoadTextureFromTexture</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-217">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-217">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-218">Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>ridimensionare</strong>, <strong>convertire</strong>, <strong>comprimere</strong>, <strong>decomprimere</strong>e/o <strong>CopyRectangle</strong>.</span><span class="sxs-lookup"><span data-stu-id="75ce6-218">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>Resize</strong>, <strong>Convert</strong>, <strong>Compress</strong>, <strong>Decompress</strong>, and/or <strong>CopyRectangle</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-219">Caricare una trama da una trama.</span><span class="sxs-lookup"><span data-stu-id="75ce6-219">Load a texture from a texture.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ce6-220"><a href="d3dx11preprocessshaderfromfile.md"><strong>D3DX11PreprocessShaderFromFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-220"><a href="d3dx11preprocessshaderfromfile.md"><strong>D3DX11PreprocessShaderFromFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-221">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-221">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-222">Invece di usare questa funzione, è consigliabile usare l'API <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="75ce6-222">Instead of using this function, we recommend that you use the <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-223">Creare uno shader da un file senza compilarlo.</span><span class="sxs-lookup"><span data-stu-id="75ce6-223">Create a shader from a file without compiling it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ce6-224"><a href="d3dx11preprocessshaderfrommemory.md"><strong>D3DX11PreprocessShaderFromMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-224"><a href="d3dx11preprocessshaderfrommemory.md"><strong>D3DX11PreprocessShaderFromMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-225">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-225">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-226">Invece di usare questa funzione, è consigliabile usare l'API <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="75ce6-226">Instead of using this function, we recommend that you use the <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-227">Creare uno shader dalla memoria senza compilarlo.</span><span class="sxs-lookup"><span data-stu-id="75ce6-227">Create a shader from memory without compiling it.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ce6-228"><a href="d3dx11preprocessshaderfromresource.md"><strong>D3DX11PreprocessShaderFromResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-228"><a href="d3dx11preprocessshaderfromresource.md"><strong>D3DX11PreprocessShaderFromResource</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-229">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-229">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-230">Invece di usare questa funzione, è consigliabile usare l'API <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="75ce6-230">Instead of using this function, we recommend that you use the <a href="/windows/desktop/direct3dhlsl/d3dpreprocess"><strong>D3DPreprocess</strong></a> API.</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-231">Creare uno shader da una risorsa senza compilarlo.</span><span class="sxs-lookup"><span data-stu-id="75ce6-231">Create a shader from a resource without compiling it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ce6-232"><a href="d3dx11savetexturetofile.md"><strong>D3DX11SaveTextureToFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-232"><a href="d3dx11savetexturetofile.md"><strong>D3DX11SaveTextureToFile</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-233">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-233">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-234">Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>CaptureTexture</strong> quindi <strong>SAVETOXXXFILE</strong> (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi.</span><span class="sxs-lookup"><span data-stu-id="75ce6-234">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>CaptureTexture</strong> then <strong>SaveToXXXFile</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span> <span data-ttu-id="75ce6-235">Per lo scenario semplificato della creazione di una schermata da una trama di destinazione di rendering, è consigliabile usare la libreria <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> , <strong>SaveDDSTextureToFile</strong> o <strong>SaveWICTextureToFile</strong>.</span><span class="sxs-lookup"><span data-stu-id="75ce6-235">For the simplified scenario of creating a screen shot from a render target texture, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a> library, <strong>SaveDDSTextureToFile</strong> or <strong>SaveWICTextureToFile</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-236">Salva una trama in un file.</span><span class="sxs-lookup"><span data-stu-id="75ce6-236">Save a texture to a file.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ce6-237"><a href="d3dx11savetexturetomemory.md"><strong>D3DX11SaveTextureToMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-237"><a href="d3dx11savetexturetomemory.md"><strong>D3DX11SaveTextureToMemory</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-238">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-238">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-239">Anziché utilizzare questa funzione, è consigliabile utilizzare la libreria <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> , <strong>CaptureTexture</strong> quindi <strong>SAVETOXXXMEMORY</strong> (dove xxx è WIC, DDS o TGA; WIC non supporta DDS e TGA; D3DX 9 supporta TGA come formato di origine dell'arte comune per i giochi.</span><span class="sxs-lookup"><span data-stu-id="75ce6-239">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a> library, <strong>CaptureTexture</strong> then <strong>SaveToXXXMemory</strong> (where XXX is WIC, DDS, or TGA; WIC doesn't support DDS and TGA; D3DX 9 supported TGA as a common art source format for games).</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-240">Salva una trama in memoria.</span><span class="sxs-lookup"><span data-stu-id="75ce6-240">Save a texture to memory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="75ce6-241"><a href="d3dx11shprojectcubemap.md"><strong>D3DX11SHProjectCubeMap</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-241"><a href="d3dx11shprojectcubemap.md"><strong>D3DX11SHProjectCubeMap</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-242">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-242">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-243">Invece di usare questa funzione, è consigliabile usare la libreria <a href="https://github.com/Microsoft/DirectXMath/tree/master/SHMath">matematica delle armoniche sferiche</a> <strong>SHProjectCubeMap</strong>.</span><span class="sxs-lookup"><span data-stu-id="75ce6-243">Instead of using this function, we recommend that you use the <a href="https://github.com/Microsoft/DirectXMath/tree/master/SHMath">Spherical Harmonics Math</a> library, <strong>SHProjectCubeMap</strong>.</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-244">Proietta una funzione rappresentata in una mappa cubo in armoniche sferiche.</span><span class="sxs-lookup"><span data-stu-id="75ce6-244">Projects a function represented in a cube map into spherical harmonics.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="75ce6-245"><a href="d3dx11unsetalldeviceobjects.md"><strong>D3DX11UnsetAllDeviceObjects</strong></a></span><span class="sxs-lookup"><span data-stu-id="75ce6-245"><a href="d3dx11unsetalldeviceobjects.md"><strong>D3DX11UnsetAllDeviceObjects</strong></a></span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-246">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="75ce6-246">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>
</blockquote>
<br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="75ce6-247">Invece di usare questa funzione, è consigliabile usare il metodo <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate"><strong>sul ID3D11DeviceContext:: ClearState</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="75ce6-247">Instead of using this function, we recommend that you use the <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate"><strong>ID3D11DeviceContext::ClearState</strong></a> method.</span></span>
</blockquote>
<br/> <span data-ttu-id="75ce6-248">Rimuove tutte le risorse dal dispositivo impostando i relativi puntatori su <strong>null</strong>.</span><span class="sxs-lookup"><span data-stu-id="75ce6-248">Removes all resources from the device by setting their pointers to <strong>NULL</strong>.</span></span> <span data-ttu-id="75ce6-249">Questa operazione deve essere chiamata durante l'arresto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="75ce6-249">This should be called during shutdown of your application.</span></span> <span data-ttu-id="75ce6-250">Consente di assicurare che, quando si rilasciano tutte le relative risorse, nessuna delle quali è associata al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="75ce6-250">It helps ensure that when one is releasing all of their resources that none of them are bound to the device.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="75ce6-251">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="75ce6-251">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75ce6-252">Informazioni di riferimento su D3DX 11</span><span class="sxs-lookup"><span data-stu-id="75ce6-252">D3DX 11 Reference</span></span>](d3d11-graphics-reference-d3dx11.md)
</dt> </dl>

 

