---
title: Effetto turbolenza
description: Usare l'effetto di turbolenza per generare una bitmap basata sulla funzione di disturbo Perlin.
ms.assetid: 86C1990E-958C-46D7-840A-E4A17F1D1740
keywords:
- effetto turbolenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f67f615ec5b68ca285a048b68bc7bc8eab6e24
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104551996"
---
# <a name="turbulence-effect"></a><span data-ttu-id="e297a-104">Effetto turbolenza</span><span class="sxs-lookup"><span data-stu-id="e297a-104">Turbulence effect</span></span>

<span data-ttu-id="e297a-105">Usare l'effetto di turbolenza per generare una bitmap basata sulla funzione di disturbo Perlin.</span><span class="sxs-lookup"><span data-stu-id="e297a-105">Use the turbulence effect to generate a bitmap based on the Perlin noise function.</span></span>

<span data-ttu-id="e297a-106">L'effetto turbolenza non ha un'immagine di input.</span><span class="sxs-lookup"><span data-stu-id="e297a-106">The turbulence effect has no input image.</span></span>

<span data-ttu-id="e297a-107">Il CLSID per questo effetto è CLSID \_ D2D1Turbulence.</span><span class="sxs-lookup"><span data-stu-id="e297a-107">The CLSID for this effect is CLSID\_D2D1Turbulence.</span></span>

-   [<span data-ttu-id="e297a-108">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="e297a-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="e297a-109">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="e297a-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="e297a-110">Modalità rumore</span><span class="sxs-lookup"><span data-stu-id="e297a-110">Noise modes</span></span>](#noise-modes)
-   [<span data-ttu-id="e297a-111">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="e297a-111">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="e297a-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e297a-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="e297a-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e297a-113">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="e297a-114">Immagine di esempio</span><span class="sxs-lookup"><span data-stu-id="e297a-114">Example image</span></span>

![schermata di esempio di effetto che mostra l'output dell'effetto di turbolenza.](images/32-turbulence.png)

<span data-ttu-id="e297a-116">L'effetto di turbolenza calcola la somma di una o più ottave della funzione di disturbo Perlin.</span><span class="sxs-lookup"><span data-stu-id="e297a-116">The Turbulence effect computes the sum of one or more octaves of the Perlin noise function.</span></span> <span data-ttu-id="e297a-117">Il rumore Perlin è una funzione pseudo-casuale il cui valore dipende dalla frequenza, dalla posizione e dal valore di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="e297a-117">Perlin noise is a pseudo-random function whose value depends on the frequency, position, and seed value.</span></span> <span data-ttu-id="e297a-118">L'effetto genera i valori RGBA usando una di queste equazioni.</span><span class="sxs-lookup"><span data-stu-id="e297a-118">The effect generates the RGBA values using one of these equations.</span></span>

<span data-ttu-id="e297a-119">Se si seleziona la \_ modalità di sintesi rumore del rumore di turbolenza d2d1 \_ \_ \_ , l'effetto usa questa equazione.</span><span class="sxs-lookup"><span data-stu-id="e297a-119">If you select the D2D1\_TURBULENCE\_NOISE\_FRACTAL\_SUM noise mode the effect uses this equation.</span></span>

![Screenshot che mostra la funzione di turbolenza usata per generare una bitmap.](images/turbulence-equation1.png)

<span data-ttu-id="e297a-121">Se si seleziona la \_ \_ \_ modalità rumore di turbolenza del rumore d2d1, l'effetto usa questa equazione.</span><span class="sxs-lookup"><span data-stu-id="e297a-121">If you select the D2D1\_TURBULENCE\_NOISE\_TURBULENCE noise mode the effect uses this equation.</span></span>

![funzione di turbolenza usata per generare una bitmap.](images/turbulence-equation2.png)

> [!Note]  
> <span data-ttu-id="e297a-123">La `PerlinNoise` funzione ha un intervallo di \[ -1, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="e297a-123">The `PerlinNoise` function has a range of \[-1, 1\].</span></span>

 

<span data-ttu-id="e297a-124">Questo effetto restituisce i valori dei pixel in alfa premoltiplicati.</span><span class="sxs-lookup"><span data-stu-id="e297a-124">This effect outputs pixel values in premultiplied alpha.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="e297a-125">Proprietà effetto</span><span class="sxs-lookup"><span data-stu-id="e297a-125">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e297a-126">Nome visualizzato e enumerazione dell'indice</span><span class="sxs-lookup"><span data-stu-id="e297a-126">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="e297a-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e297a-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e297a-128">Offset</span><span class="sxs-lookup"><span data-stu-id="e297a-128">Offset</span></span><br/> <span data-ttu-id="e297a-129">D2D1_TURBULENCE_PROP_OFFSET</span><span class="sxs-lookup"><span data-stu-id="e297a-129">D2D1_TURBULENCE_PROP_OFFSET</span></span><br/></td>
<td><span data-ttu-id="e297a-130">Coordinate in cui viene generato l'output di turbolenza.</span><span class="sxs-lookup"><span data-stu-id="e297a-130">The coordinates where the turbulence output is generated.</span></span><br/> <span data-ttu-id="e297a-131">L'algoritmo utilizzato per generare il rumore Perlin è dipendente dalla posizione, quindi un offset diverso restituisce un output diverso.</span><span class="sxs-lookup"><span data-stu-id="e297a-131">The algorithm used to generate the Perlin noise is position dependent, so a different offset results in a different output.</span></span> <span data-ttu-id="e297a-132">Questa proprietà non è associata e le unità sono specificate in DIP</span><span class="sxs-lookup"><span data-stu-id="e297a-132">This property is not bounded and the units are specified in DIPs</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e297a-133">L'offset non ha lo stesso effetto di una traduzione perché l'output della funzione Noise è infinito e la funzione esegue il wrapping intorno al riquadro.</span><span class="sxs-lookup"><span data-stu-id="e297a-133">The offset does not have the same effect as a translation because the noise function output is infinite and the function will wrap around the tile.</span></span>
</blockquote>
<br/> <span data-ttu-id="e297a-134">Il tipo è D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="e297a-134">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="e297a-135">Il valore predefinito è {0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="e297a-135">The default value is {0.0f, 0.0f}.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e297a-136">Dimensione</span><span class="sxs-lookup"><span data-stu-id="e297a-136">Size</span></span><br/> <span data-ttu-id="e297a-137">D2D1_TURBULENCE_PROP_SIZE</span><span class="sxs-lookup"><span data-stu-id="e297a-137">D2D1_TURBULENCE_PROP_SIZE</span></span><br/></td>
<td><span data-ttu-id="e297a-138">Dimensioni dell'output di turbolenza.</span><span class="sxs-lookup"><span data-stu-id="e297a-138">The size of the turbulence output.</span></span><br/> <span data-ttu-id="e297a-139">Questa proprietà non è associata e le unità sono specificate in DIP</span><span class="sxs-lookup"><span data-stu-id="e297a-139">This property is not bounded and the units are specified in DIPs</span></span> <br/>
<br/> <span data-ttu-id="e297a-140">Il tipo è D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="e297a-140">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="e297a-141">Il valore predefinito è {0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="e297a-141">The default value is {0.0f, 0.0f}.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e297a-142">BaseFrequency</span><span class="sxs-lookup"><span data-stu-id="e297a-142">BaseFrequency</span></span><br/> <span data-ttu-id="e297a-143">D2D1_TURBULENCE_PROP_BASE_FREQUENCY</span><span class="sxs-lookup"><span data-stu-id="e297a-143">D2D1_TURBULENCE_PROP_BASE_FREQUENCY</span></span><br/></td>
<td><span data-ttu-id="e297a-144">Frequenze di base nella direzione X e Y.</span><span class="sxs-lookup"><span data-stu-id="e297a-144">The base frequencies in the X and Y direction.</span></span> <span data-ttu-id="e297a-145">Questa proprietà è di tipo float e deve essere maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="e297a-145">This property is a float and must be greater than 0.</span></span> <span data-ttu-id="e297a-146">Le unità vengono specificate in 1/dip.</span><span class="sxs-lookup"><span data-stu-id="e297a-146">The units are specified in 1/DIPs.</span></span> <br/> <span data-ttu-id="e297a-147">Il valore 1 (1/DIP) per la frequenza di base determina il rumore Perlin che completa un ciclo intero tra due pixel.</span><span class="sxs-lookup"><span data-stu-id="e297a-147">A value of 1 (1/DIPs) for the base frequency results in the Perlin noise completing an entire cycle between two pixels.</span></span> <span data-ttu-id="e297a-148">L'interpolazione semplificata per questi pixel restituisce pixel completamente casuali, poiché non esiste alcuna correlazione tra i pixel.</span><span class="sxs-lookup"><span data-stu-id="e297a-148">The ease interpolation for these pixels results in completely random pixels, since there is no correlation between the pixels.</span></span><br/> <span data-ttu-id="e297a-149">Il valore 0.1 (1/DIP) per la frequenza di base, la funzione del rumore Perlin si ripete ogni 10 DIP.</span><span class="sxs-lookup"><span data-stu-id="e297a-149">A value of 0.1(1/DIPs) for the base frequency, the Perlin noise function repeats every 10 DIPs.</span></span> <span data-ttu-id="e297a-150">Ciò comporta una correlazione tra i pixel e l'effetto di turbolenza tipico è visibile.</span><span class="sxs-lookup"><span data-stu-id="e297a-150">This results in correlation between pixels and the typical turbulence effect is visible.</span></span><br/> <span data-ttu-id="e297a-151">Il tipo è D2D1_VECTOR_2F.</span><span class="sxs-lookup"><span data-stu-id="e297a-151">The type is D2D1_VECTOR_2F.</span></span><br/> <span data-ttu-id="e297a-152">Il valore predefinito è {0,01 f, 0,01 f}.</span><span class="sxs-lookup"><span data-stu-id="e297a-152">The default value is {0.01f, 0.01f}.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e297a-153">NumOctaves</span><span class="sxs-lookup"><span data-stu-id="e297a-153">NumOctaves</span></span><br/> <span data-ttu-id="e297a-154">D2D1_TURBULENCE_PROP_NUM_OCTAVES</span><span class="sxs-lookup"><span data-stu-id="e297a-154">D2D1_TURBULENCE_PROP_NUM_OCTAVES</span></span><br/></td>
<td><span data-ttu-id="e297a-155">Numero di ottave per la funzione noise.</span><span class="sxs-lookup"><span data-stu-id="e297a-155">The number of octaves for the noise function.</span></span> <span data-ttu-id="e297a-156">Questa proprietà è un oggetto UINT32 e deve essere maggiore di 0.</span><span class="sxs-lookup"><span data-stu-id="e297a-156">This property is a UINT32 and must be greater than 0.</span></span><br/> <span data-ttu-id="e297a-157">Il tipo è UINT32.</span><span class="sxs-lookup"><span data-stu-id="e297a-157">The type is UINT32.</span></span><br/> <span data-ttu-id="e297a-158">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="e297a-158">The default value is 1.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e297a-159">Seed</span><span class="sxs-lookup"><span data-stu-id="e297a-159">Seed</span></span><br/> <span data-ttu-id="e297a-160">D2D1_TURBULENCE_PROP_SEED</span><span class="sxs-lookup"><span data-stu-id="e297a-160">D2D1_TURBULENCE_PROP_SEED</span></span><br/></td>
<td><span data-ttu-id="e297a-161">Valore di inizializzazione per il generatore pseudo-casuale.</span><span class="sxs-lookup"><span data-stu-id="e297a-161">The seed for the pseudo random generator.</span></span> <span data-ttu-id="e297a-162">Questa proprietà non è associata.</span><span class="sxs-lookup"><span data-stu-id="e297a-162">This property is unbounded.</span></span><br/> <span data-ttu-id="e297a-163">Il tipo è UINT32.</span><span class="sxs-lookup"><span data-stu-id="e297a-163">The type is UINT32.</span></span><br/> <span data-ttu-id="e297a-164">Il valore predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="e297a-164">The default value is 0.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e297a-165">Rumore</span><span class="sxs-lookup"><span data-stu-id="e297a-165">Noise</span></span><br/> <span data-ttu-id="e297a-166">D2D1_TURBULENCE_PROP_NOISE</span><span class="sxs-lookup"><span data-stu-id="e297a-166">D2D1_TURBULENCE_PROP_NOISE</span></span><br/></td>
<td><span data-ttu-id="e297a-167">Modalità rumore di turbolenza.</span><span class="sxs-lookup"><span data-stu-id="e297a-167">The turbulence noise mode.</span></span> <span data-ttu-id="e297a-168">Questa proprietà può essere una somma o una <em>turbolenza</em> <em>frattale</em> .</span><span class="sxs-lookup"><span data-stu-id="e297a-168">This property can be either <em>fractal sum</em> or <em>turbulence</em>.</span></span> <span data-ttu-id="e297a-169">Indica se generare una bitmap basata sul rumore frattale o sulla funzione di turbolenza.</span><span class="sxs-lookup"><span data-stu-id="e297a-169">Indicates whether to generate a bitmap based on Fractal Noise or the Turbulence function.</span></span> <span data-ttu-id="e297a-170">Per altre informazioni, vedere <a href="#noise-modes">modalità di disturbo</a> .</span><span class="sxs-lookup"><span data-stu-id="e297a-170">See <a href="#noise-modes">Noise modes</a> for more info.</span></span> <br/> <span data-ttu-id="e297a-171">Il tipo è D2D1_TURBULENCE_NOISE.</span><span class="sxs-lookup"><span data-stu-id="e297a-171">The type is D2D1_TURBULENCE_NOISE.</span></span><br/> <span data-ttu-id="e297a-172">Il valore predefinito è D2D1_TURBULENCE_NOISE_FRACTAL_SUM.</span><span class="sxs-lookup"><span data-stu-id="e297a-172">The default value is D2D1_TURBULENCE_NOISE_FRACTAL_SUM.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e297a-173">Cucibile</span><span class="sxs-lookup"><span data-stu-id="e297a-173">Stitchable</span></span><br/> <span data-ttu-id="e297a-174">D2D1_TURBULENCE_PROP_STITCHABLE</span><span class="sxs-lookup"><span data-stu-id="e297a-174">D2D1_TURBULENCE_PROP_STITCHABLE</span></span><br/></td>
<td><span data-ttu-id="e297a-175">Attiva o disattiva l'Unione.</span><span class="sxs-lookup"><span data-stu-id="e297a-175">Turns stitching on or off.</span></span> <span data-ttu-id="e297a-176">La frequenza di base viene modificata in modo che sia possibile unire le bitmap di output.</span><span class="sxs-lookup"><span data-stu-id="e297a-176">The base frequency is adjusted so that output bitmap can be stitched.</span></span> <span data-ttu-id="e297a-177">Questa opzione è utile se si desidera affiancare più copie dell'output dell'effetto di turbolenza.</span><span class="sxs-lookup"><span data-stu-id="e297a-177">This is useful if you want to tile multiple copies of the turbulence effect output.</span></span>
<ul>
<li><span data-ttu-id="e297a-178">True la bitmap di output può essere affiancata (usando l'effetto del riquadro) senza l'aspetto di Seam.</span><span class="sxs-lookup"><span data-stu-id="e297a-178">True   The output bitmap can be tiled (using the tile effect) without the appearance of seams.</span></span> <span data-ttu-id="e297a-179">La frequenza di base viene modificata in modo che sia possibile unire le bitmap di output.</span><span class="sxs-lookup"><span data-stu-id="e297a-179">The base frequency is adjusted so that output bitmap can be stitched.</span></span></li>
<li><span data-ttu-id="e297a-180">False la frequenza di base non è regolata, quindi le Seam possono apparire tra i riquadri se la bitmap è affiancata.</span><span class="sxs-lookup"><span data-stu-id="e297a-180">False   The base frequency is not adjusted, so seams may appear between tiles if the bitmap is tiled.</span></span></li>
</ul>
<br/> <span data-ttu-id="e297a-181">Il tipo è BOOL.</span><span class="sxs-lookup"><span data-stu-id="e297a-181">The type is BOOL.</span></span><br/> <span data-ttu-id="e297a-182">Il valore predefinito è FALSE.</span><span class="sxs-lookup"><span data-stu-id="e297a-182">The default value is FALSE.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="noise-modes"></a><span data-ttu-id="e297a-183">Modalità rumore</span><span class="sxs-lookup"><span data-stu-id="e297a-183">Noise modes</span></span>



| <span data-ttu-id="e297a-184">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="e297a-184">Enumeration</span></span>                           | <span data-ttu-id="e297a-185">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e297a-185">Description</span></span>                                                                           |
|---------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e297a-186">\_ \_ \_ Somma frattale rumore di turbolenza d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="e297a-186">D2D1\_TURBULENCE\_NOISE\_FRACTAL\_SUM</span></span> | <span data-ttu-id="e297a-187">Calcola una somma delle ottave, spostando l'intervallo di output da \[ -1, 1 \] , a \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="e297a-187">Computes a sum of the octaves, shifting the output range from \[-1, 1\], to \[0, 1\].</span></span> |
| <span data-ttu-id="e297a-188">\_ \_ Turbolenza del rumore di TURBOLENZa d2d1 \_</span><span class="sxs-lookup"><span data-stu-id="e297a-188">D2D1\_TURBULENCE\_NOISE\_TURBULENCE</span></span>   | <span data-ttu-id="e297a-189">Calcola una somma del valore assoluto di ogni ottava.</span><span class="sxs-lookup"><span data-stu-id="e297a-189">Computes a sum of the absolute value of each octave.</span></span>                                  |



 

> [!Note]  
> <span data-ttu-id="e297a-190">Nessuna delle due modalità contiene un morsetto esplicito dei valori di output.</span><span class="sxs-lookup"><span data-stu-id="e297a-190">Neither mode contains an explicit clamp of the output values.</span></span>

 

## <a name="output-bitmap"></a><span data-ttu-id="e297a-191">Bitmap di output</span><span class="sxs-lookup"><span data-stu-id="e297a-191">Output bitmap</span></span>

<span data-ttu-id="e297a-192">Questo effetto genera una bitmap di dimensioni infinite logicamente.</span><span class="sxs-lookup"><span data-stu-id="e297a-192">This effect generates a logically infinite sized bitmap.</span></span>

## <a name="requirements"></a><span data-ttu-id="e297a-193">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e297a-193">Requirements</span></span>



| <span data-ttu-id="e297a-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="e297a-194">Requirement</span></span> | <span data-ttu-id="e297a-195">Valore</span><span class="sxs-lookup"><span data-stu-id="e297a-195">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e297a-196">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e297a-196">Minimum supported client</span></span> | <span data-ttu-id="e297a-197">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="e297a-197">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e297a-198">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e297a-198">Minimum supported server</span></span> | <span data-ttu-id="e297a-199">Windows 8 e aggiornamento della piattaforma per app desktop Windows 7 app \[ \| Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="e297a-199">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="e297a-200">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e297a-200">Header</span></span>                   | <span data-ttu-id="e297a-201">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="e297a-201">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="e297a-202">Libreria</span><span class="sxs-lookup"><span data-stu-id="e297a-202">Library</span></span>                  | <span data-ttu-id="e297a-203">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="e297a-203">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="e297a-204">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e297a-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e297a-205">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="e297a-205">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

