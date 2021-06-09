---
title: Oggetto Texture
description: In Direct3D 10 si specificano i campionatori e le trame in modo indipendente; Il campionamento delle trame viene implementato usando un oggetto trama basata su modelli. Questo oggetto trama basata su modelli ha un formato specifico, restituisce un tipo specifico e implementa diversi metodi.
ms.assetid: e8cb483a-d831-4942-b6fe-61dd5edb1813
keywords:
- HLSL dell'oggetto Texture
topic_type:
- apiref
api_name:
- Texture Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1881ba4a88e97e978e2646c92d276bb9763ffd
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825771"
---
# <a name="texture-object"></a><span data-ttu-id="91d97-105">Oggetto Texture</span><span class="sxs-lookup"><span data-stu-id="91d97-105">Texture Object</span></span>

<span data-ttu-id="91d97-106">In Direct3D 10 si specificano i campionatori e le trame in modo indipendente; Il campionamento delle trame viene implementato usando un oggetto trama basata su modelli.</span><span class="sxs-lookup"><span data-stu-id="91d97-106">In Direct3D 10, you specify the samplers and textures independently; texture sampling is implemented by using a templated-texture object.</span></span> <span data-ttu-id="91d97-107">Questo oggetto trama basata su modelli ha un formato specifico, restituisce un tipo specifico e implementa diversi metodi.</span><span class="sxs-lookup"><span data-stu-id="91d97-107">This templated-texture object has a specific format, returns a specific type, and implements several methods.</span></span>

<span data-ttu-id="91d97-108">Differenze tra Direct3D9 e Direct3D10:</span><span class="sxs-lookup"><span data-stu-id="91d97-108">Differences between Direct3D9 and Direct3D10:</span></span>

- <span data-ttu-id="91d97-109">In Direct3D 9 i campionatori sono associati a trame specifiche.</span><span class="sxs-lookup"><span data-stu-id="91d97-109">In Direct3D 9, samplers are bound to specific textures.</span></span>
- <span data-ttu-id="91d97-110">In Direct3D 10 le trame e i campionatori sono oggetti indipendenti.</span><span class="sxs-lookup"><span data-stu-id="91d97-110">In Direct3D 10, textures and samplers are independent objects.</span></span> <span data-ttu-id="91d97-111">Ogni oggetto trama basata su modello implementa metodi di campionamento delle trame che accettano sia la trama che il campionatore come parametri di input.</span><span class="sxs-lookup"><span data-stu-id="91d97-111">Each templated-texture object implements texture sampling methods that take both the texture and the sampler as input parameters.</span></span>



 

<span data-ttu-id="91d97-112">Ecco la sintassi per la creazione di tutti gli oggetti trama (ad eccezione degli oggetti multicampionato).</span><span class="sxs-lookup"><span data-stu-id="91d97-112">Here is the syntax for creating all texture objects (except multisampled objects).</span></span>



| <span data-ttu-id="91d97-113">Nome tipo \[ < *Object1* > \] ;</span><span class="sxs-lookup"><span data-stu-id="91d97-113">Object1 \[<*Type*>\] *Name*;</span></span> |
|------------------------------------|



 

<span data-ttu-id="91d97-114">Gli oggetti multicampionato (Texture2DMS e Texture2DMSArray) richiedono che le dimensioni della trama siano dichiarate ed espresse in modo esplicito come numero di campioni.</span><span class="sxs-lookup"><span data-stu-id="91d97-114">Multisampled objects (Texture2DMS and Texture2DMSArray) require the texture size to be explicitly stated and expressed as the number of samples.</span></span>



| <span data-ttu-id="91d97-115">Tipo \[ < *Object2, Nome* > \] *esempi*;</span><span class="sxs-lookup"><span data-stu-id="91d97-115">Object2 \[<*Type, Samples*>\] *Name*;</span></span> |
|---------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="91d97-116">Parametri</span><span class="sxs-lookup"><span data-stu-id="91d97-116">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91d97-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="91d97-117">Item</span></span></th>
<th><span data-ttu-id="91d97-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91d97-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="91d97-119"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Oggetto</em></span><span class="sxs-lookup"><span data-stu-id="91d97-119"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="91d97-120">Oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="91d97-120">A texture object.</span></span> <span data-ttu-id="91d97-121">Deve essere uno dei tipi seguenti.</span><span class="sxs-lookup"><span data-stu-id="91d97-121">Must be one of the following types.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="91d97-122">Tipo Object1</span><span class="sxs-lookup"><span data-stu-id="91d97-122">Object1 Type</span></span></th>
<th><span data-ttu-id="91d97-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91d97-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="91d97-124">Buffer</span><span class="sxs-lookup"><span data-stu-id="91d97-124">Buffer</span></span></td>
<td><span data-ttu-id="91d97-125">Buffer</span><span class="sxs-lookup"><span data-stu-id="91d97-125">Buffer</span></span> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="91d97-126">Texture1D</span><span class="sxs-lookup"><span data-stu-id="91d97-126">Texture1D</span></span></td>
<td><span data-ttu-id="91d97-127">Trama 1D</span><span class="sxs-lookup"><span data-stu-id="91d97-127">1D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91d97-128">Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="91d97-128">Texture1DArray</span></span></td>
<td><span data-ttu-id="91d97-129">Matrice di trame 1D</span><span class="sxs-lookup"><span data-stu-id="91d97-129">Array of 1D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91d97-130">Texture2D</span><span class="sxs-lookup"><span data-stu-id="91d97-130">Texture2D</span></span></td>
<td><span data-ttu-id="91d97-131">Trama 2D</span><span class="sxs-lookup"><span data-stu-id="91d97-131">2D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91d97-132">Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="91d97-132">Texture2DArray</span></span></td>
<td><span data-ttu-id="91d97-133">Matrice di trame 2D</span><span class="sxs-lookup"><span data-stu-id="91d97-133">Array of 2D textures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91d97-134">Texture3D</span><span class="sxs-lookup"><span data-stu-id="91d97-134">Texture3D</span></span></td>
<td><span data-ttu-id="91d97-135">Trama 3D</span><span class="sxs-lookup"><span data-stu-id="91d97-135">3D texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91d97-136">TextureCube</span><span class="sxs-lookup"><span data-stu-id="91d97-136">TextureCube</span></span></td>
<td><span data-ttu-id="91d97-137">Trama del cubo</span><span class="sxs-lookup"><span data-stu-id="91d97-137">Cube texture</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91d97-138">TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="91d97-138">TextureCubeArray</span></span>  </td>
<td><span data-ttu-id="91d97-139">Matrice di trame del cubo</span><span class="sxs-lookup"><span data-stu-id="91d97-139">Array of cube textures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91d97-140">Tipo Object2</span><span class="sxs-lookup"><span data-stu-id="91d97-140">Object2 Type</span></span></td>
<td><span data-ttu-id="91d97-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91d97-141">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="91d97-142">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="91d97-142">Texture2DMS</span></span></td>
<td><span data-ttu-id="91d97-143">Trama multicampionata 2D</span><span class="sxs-lookup"><span data-stu-id="91d97-143">2D multisampled texture</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="91d97-144">Texture2DMSArray</span><span class="sxs-lookup"><span data-stu-id="91d97-144">Texture2DMSArray</span></span></td>
<td><span data-ttu-id="91d97-145">Matrice di trame multicampionato 2D</span><span class="sxs-lookup"><span data-stu-id="91d97-145">Array of 2D multisampled textures</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<ol>
<li><span data-ttu-id="91d97-146">Il tipo Buffer supporta la maggior parte dei metodi dell'oggetto trama, ad eccezione di GetDimensions.</span><span class="sxs-lookup"><span data-stu-id="91d97-146">The Buffer type supports most texture object methods except GetDimensions.</span></span></li>
<li><span data-ttu-id="91d97-147">TextureCubeArray è disponibile nel modello shader 4.1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="91d97-147">TextureCubeArray is available in shader model 4.1 or higher.</span></span></li>
<li><span data-ttu-id="91d97-148">Il modello shader 4.1 è disponibile in Direct3D 10.1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="91d97-148">Shader model 4.1 is available in Direct3D 10.1 or higher.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91d97-149"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>digitare</em></span><span class="sxs-lookup"><span data-stu-id="91d97-149"><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="91d97-150">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="91d97-150">Optional.</span></span> <span data-ttu-id="91d97-151">Qualsiasi <a href="dx-graphics-hlsl-scalar.md">tipo HLSL scalare o</a> tipo <a href="dx-graphics-hlsl-vector.md"><strong>HLSL vettore,</strong></a>racchiuso tra parentesi angolari.</span><span class="sxs-lookup"><span data-stu-id="91d97-151">Any <a href="dx-graphics-hlsl-scalar.md">scalar HLSL type</a> or <a href="dx-graphics-hlsl-vector.md"><strong>vector HLSL type</strong></a>, surrounded by angle brackets.</span></span> <span data-ttu-id="91d97-152">Il tipo predefinito è <strong>float4.</strong></span><span class="sxs-lookup"><span data-stu-id="91d97-152">The default type is <strong>float4</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91d97-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Nome</em></span><span class="sxs-lookup"><span data-stu-id="91d97-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="91d97-154">Stringa ASCII che specifica il nome dell'oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="91d97-154">An ASCII string that specifies the texture object name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91d97-155"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Campioni</em></span><span class="sxs-lookup"><span data-stu-id="91d97-155"><span id="Samples"></span><span id="samples"></span><span id="SAMPLES"></span><em>Samples</em></span></span></p></td>
<td><p><span data-ttu-id="91d97-156">Numero di campioni (intervalli compresi tra 1 e 128).</span><span class="sxs-lookup"><span data-stu-id="91d97-156">The number of samples (ranges between 1 and 128).</span></span></p></td>
</tr>
</tbody>
</table>



 

## <a name="example-1"></a><span data-ttu-id="91d97-157">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="91d97-157">Example 1</span></span>

<span data-ttu-id="91d97-158">Di seguito è riportato un esempio di dichiarazione di un oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="91d97-158">Here is an example of declaring a texture object.</span></span>


```
Texture2D <float4> MyTex;

Texture2DMS <float4, 128> MyMSTex;
```



## <a name="texture-object-methods"></a><span data-ttu-id="91d97-159">Metodi dell'oggetto Texture</span><span class="sxs-lookup"><span data-stu-id="91d97-159">Texture Object Methods</span></span>

<span data-ttu-id="91d97-160">Ogni oggetto trama implementa determinati metodi. Ecco la tabella che elenca tutti i metodi.</span><span class="sxs-lookup"><span data-stu-id="91d97-160">Each texture object implements certain methods; here's the table that lists all of the methods.</span></span> <span data-ttu-id="91d97-161">Vedere la pagina di riferimento per ogni metodo per vedere quali oggetti possono usare tale metodo.</span><span class="sxs-lookup"><span data-stu-id="91d97-161">See the reference page for each method to see what objects can use that method.</span></span>



| <span data-ttu-id="91d97-162">Metodo Texture</span><span class="sxs-lookup"><span data-stu-id="91d97-162">Texture Method</span></span>                                                                     | <span data-ttu-id="91d97-163">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91d97-163">Description</span></span>                                                                                                       | <span data-ttu-id="91d97-164">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="91d97-164">vs\_4\_0</span></span> | <span data-ttu-id="91d97-165">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="91d97-165">vs\_4\_1</span></span>  | <span data-ttu-id="91d97-166">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="91d97-166">ps\_4\_0</span></span> | <span data-ttu-id="91d97-167">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="91d97-167">ps\_4\_1</span></span>  | <span data-ttu-id="91d97-168">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="91d97-168">gs\_4\_0</span></span> | <span data-ttu-id="91d97-169">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="91d97-169">gs\_4\_1</span></span>  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|----------|-----------|----------|-----------|----------|-----------|
| [<span data-ttu-id="91d97-170">CalculateLevelOfDetail</span><span class="sxs-lookup"><span data-stu-id="91d97-170">CalculateLevelOfDetail</span></span>](dx-graphics-hlsl-to-calculate-lod.md)                    | <span data-ttu-id="91d97-171">Calcolare il LOD e restituire un risultato con chiusura.</span><span class="sxs-lookup"><span data-stu-id="91d97-171">Calculate the LOD, return a clamped result.</span></span>                                                                       |          |           |          | <span data-ttu-id="91d97-172">x</span><span class="sxs-lookup"><span data-stu-id="91d97-172">x</span></span>         |          |           |
| [<span data-ttu-id="91d97-173">CalculateLevelOfDetailUnclamped</span><span class="sxs-lookup"><span data-stu-id="91d97-173">CalculateLevelOfDetailUnclamped</span></span>](dx-graphics-hlsl-to-calculate-lod-unclamped.md) | <span data-ttu-id="91d97-174">Calcolare il LOD e restituire un risultato senza ritorno a capo.</span><span class="sxs-lookup"><span data-stu-id="91d97-174">Calculate the LOD, return an unclamped result.</span></span>                                                                    |          |           |          | <span data-ttu-id="91d97-175">x</span><span class="sxs-lookup"><span data-stu-id="91d97-175">x</span></span>         |          |           |
| [<span data-ttu-id="91d97-176">Raccogliere</span><span class="sxs-lookup"><span data-stu-id="91d97-176">Gather</span></span>](dx-graphics-hlsl-to-gather.md)                                           | <span data-ttu-id="91d97-177">Ottiene i quattro campioni (solo componente rosso) che verrebbero usati per l'interpolazione bilineare durante il campionamento di una trama.</span><span class="sxs-lookup"><span data-stu-id="91d97-177">Gets the four samples (red component only) that would be used for bilinear interpolation when sampling a texture.</span></span> |          | <span data-ttu-id="91d97-178">x</span><span class="sxs-lookup"><span data-stu-id="91d97-178">x</span></span>         |          | <span data-ttu-id="91d97-179">x</span><span class="sxs-lookup"><span data-stu-id="91d97-179">x</span></span>         |          | <span data-ttu-id="91d97-180">x</span><span class="sxs-lookup"><span data-stu-id="91d97-180">x</span></span>         |
| [<span data-ttu-id="91d97-181">GetDimensions</span><span class="sxs-lookup"><span data-stu-id="91d97-181">GetDimensions</span></span>](dx-graphics-hlsl-to-getdimensions.md)                             | <span data-ttu-id="91d97-182">Ottiene la dimensione della trama per un livello mipmap specificato.</span><span class="sxs-lookup"><span data-stu-id="91d97-182">Get the texture dimension for a specified mipmap level.</span></span>                                                           | <span data-ttu-id="91d97-183">x</span><span class="sxs-lookup"><span data-stu-id="91d97-183">x</span></span>        | <span data-ttu-id="91d97-184">x</span><span class="sxs-lookup"><span data-stu-id="91d97-184">x</span></span>         | <span data-ttu-id="91d97-185">x</span><span class="sxs-lookup"><span data-stu-id="91d97-185">x</span></span>        | <span data-ttu-id="91d97-186">x</span><span class="sxs-lookup"><span data-stu-id="91d97-186">x</span></span>         | <span data-ttu-id="91d97-187">x</span><span class="sxs-lookup"><span data-stu-id="91d97-187">x</span></span>        | <span data-ttu-id="91d97-188">x</span><span class="sxs-lookup"><span data-stu-id="91d97-188">x</span></span>         |
| [<span data-ttu-id="91d97-189">GetDimensions (MultiSample)</span><span class="sxs-lookup"><span data-stu-id="91d97-189">GetDimensions (MultiSample)</span></span>](dx-graphics-hlsl-to-getdimensions.md)               | <span data-ttu-id="91d97-190">Ottiene la dimensione della trama per un livello mipmap specificato.</span><span class="sxs-lookup"><span data-stu-id="91d97-190">Get the texture dimension for a specified mipmap level.</span></span>                                                           |          | <span data-ttu-id="91d97-191">x</span><span class="sxs-lookup"><span data-stu-id="91d97-191">x</span></span>         |          | <span data-ttu-id="91d97-192">x</span><span class="sxs-lookup"><span data-stu-id="91d97-192">x</span></span>         |          | <span data-ttu-id="91d97-193">x</span><span class="sxs-lookup"><span data-stu-id="91d97-193">x</span></span>         |
| [<span data-ttu-id="91d97-194">GetSamplePosition</span><span class="sxs-lookup"><span data-stu-id="91d97-194">GetSamplePosition</span></span>](dx-graphics-hlsl-to-get-sample-position.md)                   | <span data-ttu-id="91d97-195">Ottiene la posizione dell'esempio specificato.</span><span class="sxs-lookup"><span data-stu-id="91d97-195">Get the position of the specified sample.</span></span>                                                                         |          | <span data-ttu-id="91d97-196">x</span><span class="sxs-lookup"><span data-stu-id="91d97-196">x</span></span>         |          | <span data-ttu-id="91d97-197">x</span><span class="sxs-lookup"><span data-stu-id="91d97-197">x</span></span>         |          | <span data-ttu-id="91d97-198">x</span><span class="sxs-lookup"><span data-stu-id="91d97-198">x</span></span>         |
| [<span data-ttu-id="91d97-199">Load</span><span class="sxs-lookup"><span data-stu-id="91d97-199">Load</span></span>](dx-graphics-hlsl-to-load.md)                                               | <span data-ttu-id="91d97-200">Caricare i dati senza filtri o campionamenti.</span><span class="sxs-lookup"><span data-stu-id="91d97-200">Load data without any filtering or sampling.</span></span>                                                                      | <span data-ttu-id="91d97-201">x</span><span class="sxs-lookup"><span data-stu-id="91d97-201">x</span></span>        | <span data-ttu-id="91d97-202">x</span><span class="sxs-lookup"><span data-stu-id="91d97-202">x</span></span>         | <span data-ttu-id="91d97-203">x</span><span class="sxs-lookup"><span data-stu-id="91d97-203">x</span></span>        | <span data-ttu-id="91d97-204">x</span><span class="sxs-lookup"><span data-stu-id="91d97-204">x</span></span>         | <span data-ttu-id="91d97-205">x</span><span class="sxs-lookup"><span data-stu-id="91d97-205">x</span></span>        | <span data-ttu-id="91d97-206">x</span><span class="sxs-lookup"><span data-stu-id="91d97-206">x</span></span>         |
| [<span data-ttu-id="91d97-207">Load (Multisample)</span><span class="sxs-lookup"><span data-stu-id="91d97-207">Load (Multisample)</span></span>](dx-graphics-hlsl-to-load.md)                                 | <span data-ttu-id="91d97-208">Caricare i dati senza filtri o campionamenti.</span><span class="sxs-lookup"><span data-stu-id="91d97-208">Load data without any filtering or sampling.</span></span>                                                                      |          | <span data-ttu-id="91d97-209">x</span><span class="sxs-lookup"><span data-stu-id="91d97-209">x</span></span>         | <span data-ttu-id="91d97-210">x</span><span class="sxs-lookup"><span data-stu-id="91d97-210">x</span></span>        | <span data-ttu-id="91d97-211">x</span><span class="sxs-lookup"><span data-stu-id="91d97-211">x</span></span>         |          | <span data-ttu-id="91d97-212">x</span><span class="sxs-lookup"><span data-stu-id="91d97-212">x</span></span>         |
| [<span data-ttu-id="91d97-213">Esempio</span><span class="sxs-lookup"><span data-stu-id="91d97-213">Sample</span></span>](dx-graphics-hlsl-to-sample.md)                                           | <span data-ttu-id="91d97-214">Campionare una trama.</span><span class="sxs-lookup"><span data-stu-id="91d97-214">Sample a texture.</span></span>                                                                                                 |          |           | <span data-ttu-id="91d97-215">x</span><span class="sxs-lookup"><span data-stu-id="91d97-215">x</span></span>        | <span data-ttu-id="91d97-216">x</span><span class="sxs-lookup"><span data-stu-id="91d97-216">x</span></span>         |          |           |
| [<span data-ttu-id="91d97-217">SampleBias</span><span class="sxs-lookup"><span data-stu-id="91d97-217">SampleBias</span></span>](dx-graphics-hlsl-to-samplebias.md)                                   | <span data-ttu-id="91d97-218">Campionare una trama, dopo aver applicato il valore di distorsione al livello mipmap.</span><span class="sxs-lookup"><span data-stu-id="91d97-218">Sample a texture, after applying the bias value to the mipmap level.</span></span>                                              |          |           | <span data-ttu-id="91d97-219">x</span><span class="sxs-lookup"><span data-stu-id="91d97-219">x</span></span>        | <span data-ttu-id="91d97-220">x</span><span class="sxs-lookup"><span data-stu-id="91d97-220">x</span></span>         |          |           |
| [<span data-ttu-id="91d97-221">SampleCmp</span><span class="sxs-lookup"><span data-stu-id="91d97-221">SampleCmp</span></span>](dx-graphics-hlsl-to-samplecmp.md)                                     | <span data-ttu-id="91d97-222">Campionare una trama usando un valore di confronto per rifiutare gli esempi.</span><span class="sxs-lookup"><span data-stu-id="91d97-222">Sample a texture, using a comparison value to reject samples.</span></span>                                                     |          |           | <span data-ttu-id="91d97-223">x</span><span class="sxs-lookup"><span data-stu-id="91d97-223">x</span></span>        | <span data-ttu-id="91d97-224">x</span><span class="sxs-lookup"><span data-stu-id="91d97-224">x</span></span>         |          |           |
| [<span data-ttu-id="91d97-225">SampleCmpLevelZero</span><span class="sxs-lookup"><span data-stu-id="91d97-225">SampleCmpLevelZero</span></span>](dx-graphics-hlsl-to-samplecmplevelzero.md)                   | <span data-ttu-id="91d97-226">Campionare una trama (solo livello mipmap 0), usando un valore di confronto per rifiutare i campioni.</span><span class="sxs-lookup"><span data-stu-id="91d97-226">Sample a texture (mipmap level 0 only), using a comparison value to reject samples.</span></span>                               | <span data-ttu-id="91d97-227">x</span><span class="sxs-lookup"><span data-stu-id="91d97-227">x</span></span>        | <span data-ttu-id="91d97-228">x</span><span class="sxs-lookup"><span data-stu-id="91d97-228">x</span></span>         | <span data-ttu-id="91d97-229">x</span><span class="sxs-lookup"><span data-stu-id="91d97-229">x</span></span>        | <span data-ttu-id="91d97-230">x</span><span class="sxs-lookup"><span data-stu-id="91d97-230">x</span></span>         | <span data-ttu-id="91d97-231">x</span><span class="sxs-lookup"><span data-stu-id="91d97-231">x</span></span>        | <span data-ttu-id="91d97-232">x</span><span class="sxs-lookup"><span data-stu-id="91d97-232">x</span></span>         |
| [<span data-ttu-id="91d97-233">SampleGrad</span><span class="sxs-lookup"><span data-stu-id="91d97-233">SampleGrad</span></span>](dx-graphics-hlsl-to-samplegrad.md)                                   | <span data-ttu-id="91d97-234">Campionare una trama usando una sfumatura per influenzare il modo in cui viene calcolata la posizione del campione.</span><span class="sxs-lookup"><span data-stu-id="91d97-234">Sample a texture using a gradient to influence the way the sample location is calculated.</span></span>                         | <span data-ttu-id="91d97-235">x</span><span class="sxs-lookup"><span data-stu-id="91d97-235">x</span></span>        | <span data-ttu-id="91d97-236">x</span><span class="sxs-lookup"><span data-stu-id="91d97-236">x</span></span>         | <span data-ttu-id="91d97-237">x</span><span class="sxs-lookup"><span data-stu-id="91d97-237">x</span></span>        | <span data-ttu-id="91d97-238">x</span><span class="sxs-lookup"><span data-stu-id="91d97-238">x</span></span>         | <span data-ttu-id="91d97-239">x</span><span class="sxs-lookup"><span data-stu-id="91d97-239">x</span></span>        | <span data-ttu-id="91d97-240">x</span><span class="sxs-lookup"><span data-stu-id="91d97-240">x</span></span>         |
| [<span data-ttu-id="91d97-241">SampleLevel</span><span class="sxs-lookup"><span data-stu-id="91d97-241">SampleLevel</span></span>](dx-graphics-hlsl-to-samplelevel.md)                                 | <span data-ttu-id="91d97-242">Campionare una trama al livello mipmap specificato.</span><span class="sxs-lookup"><span data-stu-id="91d97-242">Sample a texture on the specified mipmap level.</span></span>                                                                   | <span data-ttu-id="91d97-243">x</span><span class="sxs-lookup"><span data-stu-id="91d97-243">x</span></span>        | <span data-ttu-id="91d97-244">x</span><span class="sxs-lookup"><span data-stu-id="91d97-244">x</span></span>         | <span data-ttu-id="91d97-245">x</span><span class="sxs-lookup"><span data-stu-id="91d97-245">x</span></span>        | <span data-ttu-id="91d97-246">x</span><span class="sxs-lookup"><span data-stu-id="91d97-246">x</span></span>         | <span data-ttu-id="91d97-247">x</span><span class="sxs-lookup"><span data-stu-id="91d97-247">x</span></span>        | <span data-ttu-id="91d97-248">x</span><span class="sxs-lookup"><span data-stu-id="91d97-248">x</span></span>         |



 

### <a name="return-type"></a><span data-ttu-id="91d97-249">Tipo restituito</span><span class="sxs-lookup"><span data-stu-id="91d97-249">Return Type</span></span>

<span data-ttu-id="91d97-250">Il tipo restituito di un metodo dell'oggetto trama è float4, a meno che non venga specificato diversamente, ad eccezione degli oggetti trama con antialiasing multicampionato che necessitano sempre del tipo e del numero di campioni specificati.</span><span class="sxs-lookup"><span data-stu-id="91d97-250">The return type of a texture object method is float4 unless specified otherwise, with the exception of the multisampled anti-aliased texture objects that always need the type and sample count specified.</span></span> <span data-ttu-id="91d97-251">Il tipo restituito è lo stesso del tipo di risorsa trama ([**DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span><span class="sxs-lookup"><span data-stu-id="91d97-251">The return type is the same as the texture resource type ([**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span> <span data-ttu-id="91d97-252">In altre parole, può essere uno dei tipi seguenti.</span><span class="sxs-lookup"><span data-stu-id="91d97-252">In other words, it can be any of the following types.</span></span>



| <span data-ttu-id="91d97-253">Tipo</span><span class="sxs-lookup"><span data-stu-id="91d97-253">Type</span></span>                       | <span data-ttu-id="91d97-254">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91d97-254">Description</span></span>                                                                                                                                                             |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91d97-255">float</span><span class="sxs-lookup"><span data-stu-id="91d97-255">float</span></span>                      | <span data-ttu-id="91d97-256">Float a 32 bit (vedere [Regole a virgola mobile](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) per le differenze rispetto a float IEEE)</span><span class="sxs-lookup"><span data-stu-id="91d97-256">32-bit float (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>                            |
| <span data-ttu-id="91d97-257">INT</span><span class="sxs-lookup"><span data-stu-id="91d97-257">int</span></span>                        | <span data-ttu-id="91d97-258">Intero con segno a 32 bit</span><span class="sxs-lookup"><span data-stu-id="91d97-258">32-bit signed integer</span></span>                                                                                                                                                   |
| <span data-ttu-id="91d97-259">int senza segno</span><span class="sxs-lookup"><span data-stu-id="91d97-259">unsigned int</span></span>               | <span data-ttu-id="91d97-260">Intero senza segno a 32 bit</span><span class="sxs-lookup"><span data-stu-id="91d97-260">32-bit unsigned integer</span></span>                                                                                                                                                 |
| <span data-ttu-id="91d97-261">snorm</span><span class="sxs-lookup"><span data-stu-id="91d97-261">snorm</span></span>                      | <span data-ttu-id="91d97-262">Float a 32 bit nell'intervallo compreso tra -1 e 1 inclusi (vedere [Regole a virgola](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) mobile per le differenze rispetto a float IEEE)</span><span class="sxs-lookup"><span data-stu-id="91d97-262">32-bit float in range -1 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span> |
| <span data-ttu-id="91d97-263">unorm</span><span class="sxs-lookup"><span data-stu-id="91d97-263">unorm</span></span>                      | <span data-ttu-id="91d97-264">Float a 32 bit nell'intervallo compreso tra 0 e 1 inclusi (vedere [Regole a virgola](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) mobile per le differenze rispetto a float IEEE)</span><span class="sxs-lookup"><span data-stu-id="91d97-264">32-bit float in range 0 to 1 inclusive (see [Floating-Point Rules](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-float-rules) for differences from IEEE float)</span></span>  |
| <span data-ttu-id="91d97-265">qualsiasi tipo di trama o struct</span><span class="sxs-lookup"><span data-stu-id="91d97-265">any texture type or struct</span></span> | <span data-ttu-id="91d97-266">Il numero di componenti restituiti deve essere compreso tra 1 e 3 inclusi.</span><span class="sxs-lookup"><span data-stu-id="91d97-266">The number of components returned must be between 1 and 3 inclusive.</span></span>                                                                                                    |



 

<span data-ttu-id="91d97-267">Inoltre, il tipo restituito può essere qualsiasi tipo di trama, inclusa una struttura , ma deve essere inferiore a 4 componenti, ad esempio un tipo float1 che restituisce un componente.</span><span class="sxs-lookup"><span data-stu-id="91d97-267">In addition, the return type can be any texture type including a structure but, it must be less than 4 components such as a float1 type which returns one component.</span></span>

## <a name="default-values-for-missing-components-in-a-texture"></a><span data-ttu-id="91d97-268">Valori predefiniti per i componenti mancanti in una trama</span><span class="sxs-lookup"><span data-stu-id="91d97-268">Default Values for Missing Components in a Texture</span></span>

<span data-ttu-id="91d97-269">Il valore predefinito per i componenti mancanti in un tipo di risorsa trama è zero per qualsiasi componente ad eccezione del componente alfa (A); il valore predefinito per la A mancante è uno.</span><span class="sxs-lookup"><span data-stu-id="91d97-269">The default value for missing components in a texture resource type is zero for any component except the alpha component (A); the default value for the missing A is one.</span></span> <span data-ttu-id="91d97-270">Il modo in cui questo oggetto viene visualizzato allo shader dipende dal tipo di risorsa trama.</span><span class="sxs-lookup"><span data-stu-id="91d97-270">The way that this one appears to the shader depends on the texture resource type.</span></span> <span data-ttu-id="91d97-271">Assume la forma del primo componente tipidato effettivamente presente nel tipo di risorsa trama (a partire da sinistra nell'ordine RGBA).</span><span class="sxs-lookup"><span data-stu-id="91d97-271">It takes the form of the first typed component that is actually present in the texture resource type (starting from the left in RGBA order).</span></span> <span data-ttu-id="91d97-272">Se il formato è UNORM o FLOAT, il valore predefinito per la A mancante è 1,0f.</span><span class="sxs-lookup"><span data-stu-id="91d97-272">If this form is UNORM or FLOAT, the default value for the missing A is 1.0f.</span></span> <span data-ttu-id="91d97-273">Se il form è SINT o UINT, il valore predefinito per la A mancante è 0x1.</span><span class="sxs-lookup"><span data-stu-id="91d97-273">If the form is SINT or UINT, the default value for the missing A is 0x1.</span></span>

<span data-ttu-id="91d97-274">Ad esempio, quando uno shader legge il tipo di risorsa texture [**DXGI \_ FORMAT \_ R24 \_ UNORM \_ X8 \_ TYPELESS,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) I valori predefiniti per G e B sono zero e il valore predefinito per A è 1,0f. Quando uno shader legge il tipo di risorsa [**UINT DXGI \_ FORMAT \_ R16G16, \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) il valore predefinito per B è zero e il valore predefinito per A è 0x00000001. Quando uno shader legge il tipo di risorsa trama [**DXGI \_ FORMAT \_ R16 \_ SINT,**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) i valori predefiniti per G e B sono pari a zero e il valore predefinito per A è 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="91d97-274">For example, when a shader reads the [**DXGI\_FORMAT\_R24\_UNORM\_X8\_TYPELESS**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 1.0f; when a shader reads the [**DXGI\_FORMAT\_R16G16\_UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default value for B is zero and the default value for A is 0x00000001; when a shader reads the [**DXGI\_FORMAT\_R16\_SINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) texture resource type, the default values for G and B are zero and the default value for A is 0x00000001.</span></span>

## <a name="example-2"></a><span data-ttu-id="91d97-275">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="91d97-275">Example 2</span></span>

<span data-ttu-id="91d97-276">Di seguito è riportato un esempio di campionamento delle trame usando un metodo di trama.</span><span class="sxs-lookup"><span data-stu-id="91d97-276">Here is an example of texture sampling using a texture method.</span></span>


```
sampler MySamp;
Texture2D <float4> MyTex;
 
float4 main( float2 TexCoords[2] : TEXCOORD ) : SV_Target
{
    return MyTex.Sample( MySamp, TexCoords[0] ));
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="91d97-277">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="91d97-277">Minimum Shader Model</span></span>

<span data-ttu-id="91d97-278">Questo oggetto è supportato nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="91d97-278">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="91d97-279">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="91d97-279">Shader Model</span></span>                                                        | <span data-ttu-id="91d97-280">Supportato</span><span class="sxs-lookup"><span data-stu-id="91d97-280">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="91d97-281">[Modelli shader modello 4](dx-graphics-hlsl-sm4.md) e versioni successive</span><span class="sxs-lookup"><span data-stu-id="91d97-281">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="91d97-282">yes</span><span class="sxs-lookup"><span data-stu-id="91d97-282">yes</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="91d97-283">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="91d97-283">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91d97-284">Modello shader 4</span><span class="sxs-lookup"><span data-stu-id="91d97-284">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

