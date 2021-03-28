---
title: Texture (oggetto)
description: In Direct3D 10 specificare i sampler e le trame in modo indipendente; il campionamento della trama viene implementato usando un oggetto con trama basata su modelli. Questo oggetto con trama basata su modelli ha un formato specifico, restituisce un tipo specifico e implementa diversi metodi.
ms.assetid: e8cb483a-d831-4942-b6fe-61dd5edb1813
keywords:
- HLSL oggetto trama
topic_type:
- apiref
api_name:
- Texture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b075ddc1f659923efd03d9fe9d21ee3238e656e9
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "104234915"
---
# <a name="texture-object"></a><span data-ttu-id="edf6d-105">Texture (oggetto)</span><span class="sxs-lookup"><span data-stu-id="edf6d-105">Texture Object</span></span>

<span data-ttu-id="edf6d-106">In Direct3D 10 specificare i sampler e le trame in modo indipendente; il campionamento della trama viene implementato usando un oggetto con trama basata su modelli.</span><span class="sxs-lookup"><span data-stu-id="edf6d-106">In Direct3D 10, you specify the samplers and textures independently; texture sampling is implemented by using a templated-texture object.</span></span> <span data-ttu-id="edf6d-107">Questo oggetto con trama basata su modelli ha un formato specifico, restituisce un tipo specifico e implementa diversi metodi.</span><span class="sxs-lookup"><span data-stu-id="edf6d-107">This templated-texture object has a specific format, returns a specific type, and implements several methods.</span></span>




|                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edf6d-108">Differenze tra Direct3D9 e Direct3D10: in Direct3D 9 i sampler sono associati a trame specifiche; in Direct3D 10, le trame e i sampler sono oggetti indipendenti.</span><span class="sxs-lookup"><span data-stu-id="edf6d-108">Differences between Direct3D9 and Direct3D10: In Direct3D 9, samplers are bound to specific textures; in Direct3D 10, textures and samplers are independent objects.</span></span> <span data-ttu-id="edf6d-109">Ogni oggetto con trama basata su modelli implementa metodi di campionamento di trama che accettano sia la trama sia il campionatore come parametri di input.</span><span class="sxs-lookup"><span data-stu-id="edf6d-109">Each templated-texture object implements texture sampling methods that take both the texture and the sampler as input parameters.</span></span><br/> |



 

<span data-ttu-id="edf6d-110">Di seguito è illustrata la sintassi per la creazione di tutti gli oggetti texture (eccetto gli oggetti multicampionati).</span><span class="sxs-lookup"><span data-stu-id="edf6d-110">Here is the syntax for creating all texture objects (except multisampled objects).</span></span>



| <span data-ttu-id="edf6d-111">\[ <  > \] *Nome* tipo Oggetto1;</span><span class="sxs-lookup"><span data-stu-id="edf6d-111">Object1 \[<*Type*>\] *Name*;</span></span> |
|------------------------------------|



 

<span data-ttu-id="edf6d-112">Per gli oggetti multicampionati (Texture2DMS e Texture2DMSArray) è necessario che la dimensione della trama venga dichiarata in modo esplicito e espressa come numero di campioni.</span><span class="sxs-lookup"><span data-stu-id="edf6d-112">Multisampled objects (Texture2DMS and Texture2DMSArray) require the texture size to be explicitly stated and expressed as the number of samples.</span></span>



| <span data-ttu-id="edf6d-113">\[ < *Tipo oggetto2,* > \] *nome* degli esempi;</span><span class="sxs-lookup"><span data-stu-id="edf6d-113">Object2 \[<*Type, Samples*>\] *Name*;</span></span> |
|---------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="edf6d-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="edf6d-114">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="edf6d-115">Elemento</span><span class="sxs-lookup"><span data-stu-id="edf6d-115">Item</span></span></th>
<th><span data-ttu-id="edf6d-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="edf6d-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="edf6d-117"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Oggetto</em></span><span class="sxs-lookup"><span data-stu-id="edf6d-117"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="edf6d-118">Oggetto texture.</span><span class="sxs-lookup"><span data-stu-id="edf6d-118">A texture object.</span></span> <span data-ttu-id="edf6d-119">Deve essere uno dei seguenti tipi.</span><span class="sxs-lookup"><span data-stu-id="edf6d-119">Must be one of the following types.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="edf6d-120">Tipo Oggetto1</span><span class="sxs-lookup"><span data-stu-id="edf6d-120">Object1 Type</span></span></th>
<th><span data-ttu-id="edf6d-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="edf6d-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="edf6d-122">Buffer</span><span class="sxs-lookup"><span data-stu-id="edf6d-122">Buffer</span></span></td>
<td><span data-ttu-id="edf6d-123">Buffer</span><span class="sxs-lookup"><span data-stu-id="edf6d-123">Buffer</span></span> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="edf6d-124">Texture1D</span><span class="sxs-lookup"><span data-stu-id="edf6d-124">Texture1D</span></span></td>
<td><span data-ttu-id="edf6d-125">trama 1D</span><span class="sxs-lookup"><span data-stu-id="edf6d-125">1D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="edf6d-126">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="edf6d-126">Texture1DArray</span></span></td>
<td><span data-ttu-id="edf6d-127">Matrice di trame 1D</span><span class="sxs-lookup"><span data-stu-id="edf6d-127">Array of 1D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="edf6d-128">Texture2D</span><span class="sxs-lookup"><span data-stu-id="edf6d-128">Texture2D</span></span></td>
<td><span data-ttu-id="edf6d-129">trama 2D</span><span class="sxs-lookup"><span data-stu-id="edf6d-129">2D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="edf6d-130">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="edf6d-130">Texture2DArray</span></span></td>
<td><span data-ttu-id="edf6d-131">Matrice di trame 2D</span><span class="sxs-lookup"><span data-stu-id="edf6d-131">Array of 2D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="edf6d-132">Texture3D</span><span class="sxs-lookup"><span data-stu-id="edf6d-132">Texture3D</span></span></td>
<td><span data-ttu-id="edf6d-133">trama 3D</span><span class="sxs-lookup"><span data-stu-id="edf6d-133">3D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="edf6d-134">TextureCube</span><span class="sxs-lookup"><span data-stu-id="edf6d-134">TextureCube</span></span></td>
<td><span data-ttu-id="edf6d-135">Trama cubo</span><span class="sxs-lookup"><span data-stu-id="edf6d-135">Cube texture</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="edf6d-136">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="edf6d-136">TextureCubeArray</span></span>  </td>
<td><span data-ttu-id="edf6d-137">Matrice di trame del cubo</span><span class="sxs-lookup"><span data-stu-id="edf6d-137">Array of cube textures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="edf6d-138">Tipo oggetto2</span><span class="sxs-lookup"><span data-stu-id="edf6d-138">Object2 Type</span></span></td>
<td><span data-ttu-id="edf6d-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="edf6d-139">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="edf6d-140">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="edf6d-140">Texture2DMS</span></span></td>
<td><span data-ttu-id="edf6d-141">trama multicampionata 2D</span><span class="sxs-lookup"><span data-stu-id="edf6d-141">2D multisampled texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="edf6d-142">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="edf6d-142">Texture2DMSArray</span></span></td>
<td><span data-ttu-id="edf6d-143">Matrice di trame multicampionate 2D</span><span class="sxs-lookup"><span data-stu-id="edf6d-143">Array of 2D multisampled textures</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<ol>
<li><span data-ttu-id="edf6d-144">Il tipo di buffer supporta la maggior parte dei metodi dell'oggetto texture ad eccezione di GetDimensions</span><span class="sxs-lookup"><span data-stu-id="edf6d-144">The Buffer type supports most texture object methods except GetDimensions.</span></span></li>
<li><span data-ttu-id="edf6d-145">TextureCubeArray è disponibile nel modello Shader 4,1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="edf6d-145">TextureCubeArray is available in shader model 4.1 or higher.</span></span></li>
<li><span data-ttu-id="edf6d-146">Il modello di Shader 4,1 è disponibile in Direct3D 10,1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="edf6d-146">Shader model 4.1 is available in Direct3D 10.1 or higher.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edf6d-147"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Tipo</em></span><span class="sxs-lookup"><span data-stu-id="edf6d-147"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="edf6d-148">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="edf6d-148">Optional.</span></span> <span data-ttu-id="edf6d-149">Qualsiasi tipo <a href="dx-graphics-hlsl-scalar.md">scalare HLSL</a> o <a href="dx-graphics-hlsl-vector.md"><strong>vettore HLSL</strong></a>, racchiuso tra parentesi angolari.</span><span class="sxs-lookup"><span data-stu-id="edf6d-149">Any <a href="dx-graphics-hlsl-scalar.md">scalar HLSL type</a> or <a href="dx-graphics-hlsl-vector.md"><strong>vector HLSL type</strong></a>, surrounded by angle brackets.</span></span> <span data-ttu-id="edf6d-150">Il tipo predefinito è <strong>float4</strong>.</span><span class="sxs-lookup"><span data-stu-id="edf6d-150">The default type is <strong>float4</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="edf6d-151"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Nome</em></span><span class="sxs-lookup"><span data-stu-id="edf6d-151"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="edf6d-152">Stringa ASCII che specifica il nome dell'oggetto texture.</span><span class="sxs-lookup"><span data-stu-id="edf6d-152">An ASCII string that specifies the texture object name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="edf6d-153"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Campioni</em></span><span class="sxs-lookup"><span data-stu-id="edf6d-153"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Samples</em></span></span></p></td>
<td><p><span data-ttu-id="edf6d-154">Numero di campioni (compreso tra 1 e 128).</span><span class="sxs-lookup"><span data-stu-id="edf6d-154">The number of samples (ranges between 1 and 128).</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="example-1"></a><span data-ttu-id="edf6d-155">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="edf6d-155">Example 1</span></span>

<span data-ttu-id="edf6d-156">Di seguito è riportato un esempio di dichiarazione di un oggetto texture.</span><span class="sxs-lookup"><span data-stu-id="edf6d-156">Here is an example of declaring a texture object.</span></span>


```
Texture2D <float4> MyTex;

Texture2DMS <float4, 128> MyMSTex;
```



## <a name="texture-object-methods"></a><span data-ttu-id="edf6d-157">Metodi dell'oggetto texture</span><span class="sxs-lookup"><span data-stu-id="edf6d-157">Texture Object Methods</span></span>

<span data-ttu-id="edf6d-158">Ogni oggetto texture implementa determinati metodi; Ecco la tabella in cui sono elencati tutti i metodi.</span><span class="sxs-lookup"><span data-stu-id="edf6d-158">Each texture object implements certain methods; here's the table that lists all of the methods.</span></span> <span data-ttu-id="edf6d-159">Vedere la pagina di riferimento per ogni metodo per vedere quali oggetti possono usare il metodo.</span><span class="sxs-lookup"><span data-stu-id="edf6d-159">See the reference page for each method to see what objects can use that method.</span></span>



| <span data-ttu-id="edf6d-160">Texture (metodo)</span><span class="sxs-lookup"><span data-stu-id="edf6d-160">Texture Method</span></span>                                                                     | <span data-ttu-id="edf6d-161">Descrizione</span><span class="sxs-lookup"><span data-stu-id="edf6d-161">Description</span></span>                                                                                                       | <span data-ttu-id="edf6d-162">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="edf6d-162">vs\_4\_0</span></span> | <span data-ttu-id="edf6d-163">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="edf6d-163">vs\_4\_1</span></span>  | <span data-ttu-id="edf6d-164">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="edf6d-164">ps\_4\_0</span></span> | <span data-ttu-id="edf6d-165">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="edf6d-165">ps\_4\_1</span></span>  | <span data-ttu-id="edf6d-166">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="edf6d-166">gs\_4\_0</span></span> | <span data-ttu-id="edf6d-167">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="edf6d-167">gs\_4\_1</span></span>  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|----------|-----------|----------|-----------|----------|-----------|
| [<span data-ttu-id="edf6d-168">CalculateLevelOfDetail</span><span class="sxs-lookup"><span data-stu-id="edf6d-168">CalculateLevelOfDetail</span></span>](dx-graphics-hlsl-to-calculate-lod.md)                    | <span data-ttu-id="edf6d-169">Calcolare il valore LOD, restituire un risultato bloccato.</span><span class="sxs-lookup"><span data-stu-id="edf6d-169">Calculate the LOD, return a clamped result.</span></span>                                                                       |          |           |          | <span data-ttu-id="edf6d-170">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-170">x</span></span>         |          |           |
| [<span data-ttu-id="edf6d-171">CalculateLevelOfDetailUnclamped</span><span class="sxs-lookup"><span data-stu-id="edf6d-171">CalculateLevelOfDetailUnclamped</span></span>](dx-graphics-hlsl-to-calculate-lod-unclamped.md) | <span data-ttu-id="edf6d-172">Calcolare il valore LOD, restituire un risultato non bloccato.</span><span class="sxs-lookup"><span data-stu-id="edf6d-172">Calculate the LOD, return an unclamped result.</span></span>                                                                    |          |           |          | <span data-ttu-id="edf6d-173">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-173">x</span></span>         |          |           |
| [<span data-ttu-id="edf6d-174">Raccogliere</span><span class="sxs-lookup"><span data-stu-id="edf6d-174">Gather</span></span>](dx-graphics-hlsl-to-gather.md)                                           | <span data-ttu-id="edf6d-175">Ottiene i quattro campioni (solo per il componente rosso) che verrebbero usati per l'interpolazione bilineare durante il campionamento di una trama.</span><span class="sxs-lookup"><span data-stu-id="edf6d-175">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span> |          | <span data-ttu-id="edf6d-176">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-176">x</span></span>         |          | <span data-ttu-id="edf6d-177">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-177">x</span></span>         |          | <span data-ttu-id="edf6d-178">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-178">x</span></span>         |
| [<span data-ttu-id="edf6d-179">GetDimensions</span><span class="sxs-lookup"><span data-stu-id="edf6d-179">GetDimensions</span></span>](dx-graphics-hlsl-to-getdimensions.md)                             | <span data-ttu-id="edf6d-180">Ottiene la dimensione di trama per un livello di mipmap specificato.</span><span class="sxs-lookup"><span data-stu-id="edf6d-180">Get the texture dimension for a specified mipmap level.</span></span>                                                           | <span data-ttu-id="edf6d-181">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-181">x</span></span>        | <span data-ttu-id="edf6d-182">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-182">x</span></span>         | <span data-ttu-id="edf6d-183">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-183">x</span></span>        | <span data-ttu-id="edf6d-184">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-184">x</span></span>         | <span data-ttu-id="edf6d-185">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-185">x</span></span>        | <span data-ttu-id="edf6d-186">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-186">x</span></span>         |
| [<span data-ttu-id="edf6d-187">GetDimensions (multisample)</span><span class="sxs-lookup"><span data-stu-id="edf6d-187">GetDimensions (MultiSample)</span></span>](dx-graphics-hlsl-to-getdimensions.md)               | <span data-ttu-id="edf6d-188">Ottiene la dimensione di trama per un livello di mipmap specificato.</span><span class="sxs-lookup"><span data-stu-id="edf6d-188">Get the texture dimension for a specified mipmap level.</span></span>                                                           |          | <span data-ttu-id="edf6d-189">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-189">x</span></span>         |          | <span data-ttu-id="edf6d-190">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-190">x</span></span>         |          | <span data-ttu-id="edf6d-191">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-191">x</span></span>         |
| [<span data-ttu-id="edf6d-192">GetSamplePosition</span><span class="sxs-lookup"><span data-stu-id="edf6d-192">GetSamplePosition</span></span>](dx-graphics-hlsl-to-get-sample-position.md)                   | <span data-ttu-id="edf6d-193">Ottiene la posizione dell'esempio specificato.</span><span class="sxs-lookup"><span data-stu-id="edf6d-193">Get the position of the specified sample.</span></span>                                                                         |          | <span data-ttu-id="edf6d-194">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-194">x</span></span>         |          | <span data-ttu-id="edf6d-195">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-195">x</span></span>         |          | <span data-ttu-id="edf6d-196">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-196">x</span></span>         |
| [<span data-ttu-id="edf6d-197">Load</span><span class="sxs-lookup"><span data-stu-id="edf6d-197">Load</span></span>](dx-graphics-hlsl-to-load.md)                                               | <span data-ttu-id="edf6d-198">Caricare i dati senza alcun filtro o campionamento.</span><span class="sxs-lookup"><span data-stu-id="edf6d-198">Load data without any filtering or sampling.</span></span>                                                                      | <span data-ttu-id="edf6d-199">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-199">x</span></span>        | <span data-ttu-id="edf6d-200">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-200">x</span></span>         | <span data-ttu-id="edf6d-201">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-201">x</span></span>        | <span data-ttu-id="edf6d-202">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-202">x</span></span>         | <span data-ttu-id="edf6d-203">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-203">x</span></span>        | <span data-ttu-id="edf6d-204">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-204">x</span></span>         |
| [<span data-ttu-id="edf6d-205">Load (campionamento)</span><span class="sxs-lookup"><span data-stu-id="edf6d-205">Load (Multisample)</span></span>](dx-graphics-hlsl-to-load.md)                                 | <span data-ttu-id="edf6d-206">Caricare i dati senza alcun filtro o campionamento.</span><span class="sxs-lookup"><span data-stu-id="edf6d-206">Load data without any filtering or sampling.</span></span>                                                                      |          | <span data-ttu-id="edf6d-207">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-207">x</span></span>         | <span data-ttu-id="edf6d-208">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-208">x</span></span>        | <span data-ttu-id="edf6d-209">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-209">x</span></span>         |          | <span data-ttu-id="edf6d-210">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-210">x</span></span>         |
| [<span data-ttu-id="edf6d-211">Esempio</span><span class="sxs-lookup"><span data-stu-id="edf6d-211">Sample</span></span>](dx-graphics-hlsl-to-sample.md)                                           | <span data-ttu-id="edf6d-212">Campionare una trama.</span><span class="sxs-lookup"><span data-stu-id="edf6d-212">Sample a texture.</span></span>                                                                                                 |          |           | <span data-ttu-id="edf6d-213">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-213">x</span></span>        | <span data-ttu-id="edf6d-214">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-214">x</span></span>         |          |           |
| [<span data-ttu-id="edf6d-215">SampleBias</span><span class="sxs-lookup"><span data-stu-id="edf6d-215">SampleBias</span></span>](dx-graphics-hlsl-to-samplebias.md)                                   | <span data-ttu-id="edf6d-216">Campionare una trama, dopo aver applicato il valore di distorsione al livello mipmap.</span><span class="sxs-lookup"><span data-stu-id="edf6d-216">Sample a texture, after applying the bias value to the mipmap level.</span></span>                                              |          |           | <span data-ttu-id="edf6d-217">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-217">x</span></span>        | <span data-ttu-id="edf6d-218">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-218">x</span></span>         |          |           |
| [<span data-ttu-id="edf6d-219">SampleCmp</span><span class="sxs-lookup"><span data-stu-id="edf6d-219">SampleCmp</span></span>](dx-graphics-hlsl-to-samplecmp.md)                                     | <span data-ttu-id="edf6d-220">Campionare una trama, usando un valore di confronto per rifiutare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="edf6d-220">Sample a texture, using a comparison value to reject samples.</span></span>                                                     |          |           | <span data-ttu-id="edf6d-221">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-221">x</span></span>        | <span data-ttu-id="edf6d-222">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-222">x</span></span>         |          |           |
| [<span data-ttu-id="edf6d-223">SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="edf6d-223">SampleCmpLevelZero</span></span>](dx-graphics-hlsl-to-samplecmplevelzero.md)                   | <span data-ttu-id="edf6d-224">Campionare una trama (solo livello mipmap 0), usando un valore di confronto per rifiutare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="edf6d-224">Sample a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>                               | <span data-ttu-id="edf6d-225">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-225">x</span></span>        | <span data-ttu-id="edf6d-226">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-226">x</span></span>         | <span data-ttu-id="edf6d-227">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-227">x</span></span>        | <span data-ttu-id="edf6d-228">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-228">x</span></span>         | <span data-ttu-id="edf6d-229">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-229">x</span></span>        | <span data-ttu-id="edf6d-230">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-230">x</span></span>         |
| [<span data-ttu-id="edf6d-231">SampleGrad</span><span class="sxs-lookup"><span data-stu-id="edf6d-231">SampleGrad</span></span>](dx-graphics-hlsl-to-samplegrad.md)                                   | <span data-ttu-id="edf6d-232">Campionare una trama utilizzando una sfumatura per influenzare il modo in cui viene calcolata la posizione di esempio.</span><span class="sxs-lookup"><span data-stu-id="edf6d-232">Sample a texture using a gradient to influence the way the sample location is calculated.</span></span>                         | <span data-ttu-id="edf6d-233">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-233">x</span></span>        | <span data-ttu-id="edf6d-234">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-234">x</span></span>         | <span data-ttu-id="edf6d-235">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-235">x</span></span>        | <span data-ttu-id="edf6d-236">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-236">x</span></span>         | <span data-ttu-id="edf6d-237">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-237">x</span></span>        | <span data-ttu-id="edf6d-238">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-238">x</span></span>         |
| [<span data-ttu-id="edf6d-239">SampleLevel</span><span class="sxs-lookup"><span data-stu-id="edf6d-239">SampleLevel</span></span>](dx-graphics-hlsl-to-samplelevel.md)                                 | <span data-ttu-id="edf6d-240">Campiona una trama sul livello mipmap specificato.</span><span class="sxs-lookup"><span data-stu-id="edf6d-240">Sample a texture on the specified mipmap level.</span></span>                                                                   | <span data-ttu-id="edf6d-241">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-241">x</span></span>        | <span data-ttu-id="edf6d-242">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-242">x</span></span>         | <span data-ttu-id="edf6d-243">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-243">x</span></span>        | <span data-ttu-id="edf6d-244">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-244">x</span></span>         | <span data-ttu-id="edf6d-245">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-245">x</span></span>        | <span data-ttu-id="edf6d-246">x</span><span class="sxs-lookup"><span data-stu-id="edf6d-246">x</span></span>         |



 

### <a name="return-type"></a><span data-ttu-id="edf6d-247">Tipo restituito</span><span class="sxs-lookup"><span data-stu-id="edf6d-247">Return Type</span></span>

<span data-ttu-id="edf6d-248">Il tipo restituito di un metodo dell'oggetto texture è float4, a meno che non sia specificato diversamente, ad eccezione degli oggetti trama con anti-aliasing multicampionato che richiedono sempre il tipo e il numero di campione specificati.</span><span class="sxs-lookup"><span data-stu-id="edf6d-248">The return type of a texture object method is float4 unless specified otherwise, with the exception of the multisampled anti-aliased texture objects that always need the type and sample count specified.</span></span> <span data-ttu-id="edf6d-249">Il tipo restituito è uguale al tipo di risorsa trama ([**\_ formato DXGI**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span><span class="sxs-lookup"><span data-stu-id="edf6d-249">The return type is the same as the texture resource type ([**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span> <span data-ttu-id="edf6d-250">In altre parole, può essere uno qualsiasi dei seguenti tipi.</span><span class="sxs-lookup"><span data-stu-id="edf6d-250">In other words, it can be any of the following types.</span></span>



| <span data-ttu-id="edf6d-251">Tipo</span><span class="sxs-lookup"><span data-stu-id="edf6d-251">Type</span></span>                       | <span data-ttu-id="edf6d-252">Descrizione</span><span class="sxs-lookup"><span data-stu-id="edf6d-252">Description</span></span>                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edf6d-253">float</span><span class="sxs-lookup"><span data-stu-id="edf6d-253">float</span></span>                      | <span data-ttu-id="edf6d-254">float a 32 bit (vedere [le regole a virgola mobile per le](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) differenze rispetto a IEEE float)</span><span class="sxs-lookup"><span data-stu-id="edf6d-254">32-bit float (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>                            |
| <span data-ttu-id="edf6d-255">INT</span><span class="sxs-lookup"><span data-stu-id="edf6d-255">int</span></span>                        | <span data-ttu-id="edf6d-256">Intero con segno a 32 bit</span><span class="sxs-lookup"><span data-stu-id="edf6d-256">32-bit signed integer</span></span>                                                                                                                                                   |
| <span data-ttu-id="edf6d-257">int senza segno</span><span class="sxs-lookup"><span data-stu-id="edf6d-257">unsigned int</span></span>               | <span data-ttu-id="edf6d-258">Intero senza segno a 32 bit</span><span class="sxs-lookup"><span data-stu-id="edf6d-258">32-bit unsigned integer</span></span>                                                                                                                                                 |
| <span data-ttu-id="edf6d-259">russare</span><span class="sxs-lookup"><span data-stu-id="edf6d-259">snorm</span></span>                      | <span data-ttu-id="edf6d-260">32 bit float nell'intervallo compreso tra 1 e 1 (vedere [le regole a virgola mobile per le](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) differenze rispetto a IEEE float)</span><span class="sxs-lookup"><span data-stu-id="edf6d-260">32-bit float in range -1 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span> |
| <span data-ttu-id="edf6d-261">unorm</span><span class="sxs-lookup"><span data-stu-id="edf6d-261">unorm</span></span>                      | <span data-ttu-id="edf6d-262">32 bit float nell'intervallo compreso tra 0 e 1 (vedere [regole a virgola mobile per le](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) differenze rispetto a IEEE float)</span><span class="sxs-lookup"><span data-stu-id="edf6d-262">32-bit float in range 0 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>  |
| <span data-ttu-id="edf6d-263">qualsiasi tipo di trama o struct</span><span class="sxs-lookup"><span data-stu-id="edf6d-263">any texture type or struct</span></span> | <span data-ttu-id="edf6d-264">Il numero di componenti restituiti deve essere compreso tra 1 e 3.</span><span class="sxs-lookup"><span data-stu-id="edf6d-264">The number of components returned must be between 1 and 3 inclusive.</span></span>                                                                                                    |



 

<span data-ttu-id="edf6d-265">Inoltre, il tipo restituito può essere qualsiasi tipo di trama, inclusa una struttura, ma deve essere inferiore a 4 componenti, ad esempio un tipo float1 che restituisce un componente.</span><span class="sxs-lookup"><span data-stu-id="edf6d-265">In addition, the return type can be any texture type including a structure but, it must be less than 4 components such as a float1 type which returns one component.</span></span>

## <a name="default-values-for-missing-components-in-a-texture"></a><span data-ttu-id="edf6d-266">Valori predefiniti per i componenti mancanti in una trama</span><span class="sxs-lookup"><span data-stu-id="edf6d-266">Default Values for Missing Components in a Texture</span></span>

<span data-ttu-id="edf6d-267">Il valore predefinito per i componenti mancanti in un tipo di risorsa trama è zero per qualsiasi componente eccetto il componente alfa (A); il valore predefinito per l'oggetto mancante è uno.</span><span class="sxs-lookup"><span data-stu-id="edf6d-267">The default value for missing components in a texture resource type is zero for any component except the alpha component (A); the default value for the missing A is one.</span></span> <span data-ttu-id="edf6d-268">Il modo in cui questo aspetto viene visualizzato nello shader dipende dal tipo di risorsa trama.</span><span class="sxs-lookup"><span data-stu-id="edf6d-268">The way that this one appears to the shader depends on the texture resource type.</span></span> <span data-ttu-id="edf6d-269">Prende il formato del primo componente tipizzato che è effettivamente presente nel tipo di risorsa trama (a partire da sinistra nell'ordine RGBA).</span><span class="sxs-lookup"><span data-stu-id="edf6d-269">It takes the form of the first typed component that is actually present in the texture resource type (starting from the left in RGBA order).</span></span> <span data-ttu-id="edf6d-270">Se il formato è UNORM o FLOAT, il valore predefinito per l'oggetto mancante A è 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="edf6d-270">If this form is UNORM or FLOAT, the default value for the missing A is 1.0f.</span></span> <span data-ttu-id="edf6d-271">Se il form è SINT o UINT, il valore predefinito per l'oggetto mancante A è 0x1.</span><span class="sxs-lookup"><span data-stu-id="edf6d-271">If the form is SINT or UINT, the default value for the missing A is 0x1.</span></span>

<span data-ttu-id="edf6d-272">Ad esempio, quando uno shader legge il [**formato DXGI \_ \_ R24 \_ UNORM \_ x8 \_ tipo**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) di risorsa trama, i valori predefiniti per G e B sono pari A zero e il valore predefinito per a è 1,0 f; quando uno shader legge il [**formato DXGI \_ \_ R16G16 \_ uint**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) trama tipo di risorsa, il valore predefinito per B è zero e il valore predefinito per a è 0x00000001; quando uno shader legge il [**formato DXGI \_ \_ R16 \_ Sint**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture tipo di risorsa, i valori predefiniti per G e B sono pari a zero e il valore predefinito per a è 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="edf6d-272">For example, when a shader reads the [**DXGI\_FORMAT\_R24\_UNORM\_X8\_TYPELESS**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 1.0f; when a shader reads the [**DXGI\_FORMAT\_R16G16\_UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default value for B is zero and the default value for A is 0x00000001; when a shader reads the [**DXGI\_FORMAT\_R16\_SINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 0x00000001.</span></span>

## <a name="example-2"></a><span data-ttu-id="edf6d-273">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="edf6d-273">Example 2</span></span>

<span data-ttu-id="edf6d-274">Di seguito è riportato un esempio di campionamento di trama usando un metodo texture.</span><span class="sxs-lookup"><span data-stu-id="edf6d-274">Here is an example of texture sampling using a texture method.</span></span>


```
sampler MySamp;
Texture2D <float4> MyTex;
 
float4 main( float2 TexCoords[2] : TEXCOORD ) : SV_Target
{
    return MyTex.Sample( MySamp, TexCoords[0] ));
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="edf6d-275">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="edf6d-275">Minimum Shader Model</span></span>

<span data-ttu-id="edf6d-276">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="edf6d-276">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="edf6d-277">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="edf6d-277">Shader Model</span></span>                                                        | <span data-ttu-id="edf6d-278">Supportato</span><span class="sxs-lookup"><span data-stu-id="edf6d-278">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="edf6d-279">[Shader Model 4](dx-graphics-hlsl-sm4.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="edf6d-279">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="edf6d-280">sì</span><span class="sxs-lookup"><span data-stu-id="edf6d-280">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="edf6d-281">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="edf6d-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edf6d-282">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="edf6d-282">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

