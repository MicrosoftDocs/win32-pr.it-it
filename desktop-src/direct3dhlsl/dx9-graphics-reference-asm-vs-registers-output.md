---
title: Registri di output
description: Registri di output
ms.assetid: 44148185-1051-44b9-afde-a2ecd76c829f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4a0b397d17b841877796bd9c33432896208ed6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992752"
---
# <a name="output-registers"></a><span data-ttu-id="320fc-103">Registri di output</span><span class="sxs-lookup"><span data-stu-id="320fc-103">Output Registers</span></span>

-   <span data-ttu-id="320fc-104">Registro colori vertici</span><span class="sxs-lookup"><span data-stu-id="320fc-104">Vertex Color Register</span></span>
-   <span data-ttu-id="320fc-105">Registro di nebbia</span><span class="sxs-lookup"><span data-stu-id="320fc-105">Fog Register</span></span>
-   <span data-ttu-id="320fc-106">Posizione \_ Registro</span><span class="sxs-lookup"><span data-stu-id="320fc-106">Position\_Register</span></span>
-   <span data-ttu-id="320fc-107">\_Registro dimensioni \_ punti</span><span class="sxs-lookup"><span data-stu-id="320fc-107">Point\_Size\_Register</span></span>
-   <span data-ttu-id="320fc-108">\_Registro coordinate \_ trama</span><span class="sxs-lookup"><span data-stu-id="320fc-108">Texture\_Coordinate\_Register</span></span>

<span data-ttu-id="320fc-109">I nomi dei registri sono preceduti da una lettera minuscola o, a indicare che i registri di output sono di sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="320fc-109">Register names are preceded by a lowercase letter o, indicating that the output registers are write-only.</span></span>

## <a name="vertex-color-register---od0-od1"></a><span data-ttu-id="320fc-110">Registro colori vertici-oD0, oD1</span><span class="sxs-lookup"><span data-stu-id="320fc-110">Vertex Color Register - oD0, oD1</span></span>

<span data-ttu-id="320fc-111">oD0 è il registro colori diffuso.</span><span class="sxs-lookup"><span data-stu-id="320fc-111">oD0 is the diffuse color register.</span></span> <span data-ttu-id="320fc-112">oD1 è il registro colore speculare.</span><span class="sxs-lookup"><span data-stu-id="320fc-112">oD1 is the specular color register.</span></span> <span data-ttu-id="320fc-113">Il valore oD0 viene interpolato e viene scritto nel registro colore di input 0 (V0) del pixel shader.</span><span class="sxs-lookup"><span data-stu-id="320fc-113">The oD0 value is interpolated and is written to the input color register 0 (v0) of the pixel shader.</span></span> <span data-ttu-id="320fc-114">Il valore oD1 viene interpolato e scritto nel registro colori di input 1 (V1) del pixel shader.</span><span class="sxs-lookup"><span data-stu-id="320fc-114">The oD1 value is interpolated and written to the input color register 1 (v1) of the pixel shader.</span></span> <span data-ttu-id="320fc-115">Per ulteriori informazioni sui registri dei colori pixel shader, vedere registri.</span><span class="sxs-lookup"><span data-stu-id="320fc-115">For more information about pixel shader color registers, see Registers.</span></span>



| <span data-ttu-id="320fc-116">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="320fc-116">Vertex shader versions</span></span> | <span data-ttu-id="320fc-117">1\_1</span><span class="sxs-lookup"><span data-stu-id="320fc-117">1\_1</span></span> | <span data-ttu-id="320fc-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="320fc-118">2\_0</span></span> | <span data-ttu-id="320fc-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="320fc-119">2\_sw</span></span> | <span data-ttu-id="320fc-120">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="320fc-120">2\_x</span></span> | <span data-ttu-id="320fc-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="320fc-121">3\_0</span></span> | <span data-ttu-id="320fc-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="320fc-122">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="320fc-123">Registro colori vertici</span><span class="sxs-lookup"><span data-stu-id="320fc-123">Vertex Color Register</span></span>  | <span data-ttu-id="320fc-124">x</span><span class="sxs-lookup"><span data-stu-id="320fc-124">x</span></span>    | <span data-ttu-id="320fc-125">x</span><span class="sxs-lookup"><span data-stu-id="320fc-125">x</span></span>    | <span data-ttu-id="320fc-126">x</span><span class="sxs-lookup"><span data-stu-id="320fc-126">x</span></span>     | <span data-ttu-id="320fc-127">x</span><span class="sxs-lookup"><span data-stu-id="320fc-127">x</span></span>    |      |       |



 

## <a name="fog-register---ofog"></a><span data-ttu-id="320fc-128">Registro di nebbia-oFog</span><span class="sxs-lookup"><span data-stu-id="320fc-128">Fog Register - oFog</span></span>

<span data-ttu-id="320fc-129">Il valore di nebbia di output viene registrato.</span><span class="sxs-lookup"><span data-stu-id="320fc-129">The output fog value registers.</span></span> <span data-ttu-id="320fc-130">Il valore è il fattore di nebbia da interpolare e quindi indirizzato alla tabella Fog.</span><span class="sxs-lookup"><span data-stu-id="320fc-130">The value is the fog factor to be interpolated and then routed to the fog table.</span></span> <span data-ttu-id="320fc-131">Viene utilizzato solo il componente x scalare della nebbia.</span><span class="sxs-lookup"><span data-stu-id="320fc-131">Only the scalar x-component of the fog is used.</span></span> <span data-ttu-id="320fc-132">I valori vengono fissati tra zero e uno prima del passaggio al rasterizzatore.</span><span class="sxs-lookup"><span data-stu-id="320fc-132">Values are clamped between zero and one before passing to the rasterizer.</span></span>



| <span data-ttu-id="320fc-133">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="320fc-133">Vertex shader versions</span></span> | <span data-ttu-id="320fc-134">1\_1</span><span class="sxs-lookup"><span data-stu-id="320fc-134">1\_1</span></span> | <span data-ttu-id="320fc-135">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="320fc-135">2\_0</span></span> | <span data-ttu-id="320fc-136">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="320fc-136">2\_sw</span></span> | <span data-ttu-id="320fc-137">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="320fc-137">2\_x</span></span> | <span data-ttu-id="320fc-138">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="320fc-138">3\_0</span></span> | <span data-ttu-id="320fc-139">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="320fc-139">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="320fc-140">Registro di nebbia</span><span class="sxs-lookup"><span data-stu-id="320fc-140">Fog Register</span></span>           | <span data-ttu-id="320fc-141">x</span><span class="sxs-lookup"><span data-stu-id="320fc-141">x</span></span>    | <span data-ttu-id="320fc-142">x</span><span class="sxs-lookup"><span data-stu-id="320fc-142">x</span></span>    | <span data-ttu-id="320fc-143">x</span><span class="sxs-lookup"><span data-stu-id="320fc-143">x</span></span>     | <span data-ttu-id="320fc-144">x</span><span class="sxs-lookup"><span data-stu-id="320fc-144">x</span></span>    |      |       |



 

## <a name="position-register---opos"></a><span data-ttu-id="320fc-145">Posizione Register-oPos</span><span class="sxs-lookup"><span data-stu-id="320fc-145">Position Register - oPos</span></span>

<span data-ttu-id="320fc-146">La posizione di output viene registrata.</span><span class="sxs-lookup"><span data-stu-id="320fc-146">The output position registers.</span></span> <span data-ttu-id="320fc-147">Il valore è la posizione nello spazio di ritaglio omogeneo.</span><span class="sxs-lookup"><span data-stu-id="320fc-147">The value is the position in homogeneous clipping space.</span></span> <span data-ttu-id="320fc-148">Questo valore deve essere scritto dal vertex shader.</span><span class="sxs-lookup"><span data-stu-id="320fc-148">This value must be written by the vertex shader.</span></span>



| <span data-ttu-id="320fc-149">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="320fc-149">Vertex shader versions</span></span> | <span data-ttu-id="320fc-150">1\_1</span><span class="sxs-lookup"><span data-stu-id="320fc-150">1\_1</span></span> | <span data-ttu-id="320fc-151">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="320fc-151">2\_0</span></span> | <span data-ttu-id="320fc-152">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="320fc-152">2\_sw</span></span> | <span data-ttu-id="320fc-153">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="320fc-153">2\_x</span></span> | <span data-ttu-id="320fc-154">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="320fc-154">3\_0</span></span> | <span data-ttu-id="320fc-155">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="320fc-155">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="320fc-156">Posizione registro</span><span class="sxs-lookup"><span data-stu-id="320fc-156">Position Register</span></span>      | <span data-ttu-id="320fc-157">x</span><span class="sxs-lookup"><span data-stu-id="320fc-157">x</span></span>    | <span data-ttu-id="320fc-158">x</span><span class="sxs-lookup"><span data-stu-id="320fc-158">x</span></span>    | <span data-ttu-id="320fc-159">x</span><span class="sxs-lookup"><span data-stu-id="320fc-159">x</span></span>     | <span data-ttu-id="320fc-160">x</span><span class="sxs-lookup"><span data-stu-id="320fc-160">x</span></span>    |      |       |



 

## <a name="point-size-register---opts"></a><span data-ttu-id="320fc-161">Registro dimensioni punti-opz</span><span class="sxs-lookup"><span data-stu-id="320fc-161">Point Size Register - oPts</span></span>

<span data-ttu-id="320fc-162">Registri delle dimensioni del punto di output.</span><span class="sxs-lookup"><span data-stu-id="320fc-162">The output point-size registers.</span></span> <span data-ttu-id="320fc-163">Viene utilizzato solo il componente x scalare della dimensione del punto.</span><span class="sxs-lookup"><span data-stu-id="320fc-163">Only the scalar x-component of the point size is used.</span></span>



| <span data-ttu-id="320fc-164">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="320fc-164">Vertex shader versions</span></span> | <span data-ttu-id="320fc-165">1\_1</span><span class="sxs-lookup"><span data-stu-id="320fc-165">1\_1</span></span> | <span data-ttu-id="320fc-166">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="320fc-166">2\_0</span></span> | <span data-ttu-id="320fc-167">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="320fc-167">2\_sw</span></span> | <span data-ttu-id="320fc-168">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="320fc-168">2\_x</span></span> | <span data-ttu-id="320fc-169">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="320fc-169">3\_0</span></span> | <span data-ttu-id="320fc-170">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="320fc-170">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="320fc-171">Registro dimensioni punti</span><span class="sxs-lookup"><span data-stu-id="320fc-171">Point Size Register</span></span>    | <span data-ttu-id="320fc-172">x</span><span class="sxs-lookup"><span data-stu-id="320fc-172">x</span></span>    | <span data-ttu-id="320fc-173">x</span><span class="sxs-lookup"><span data-stu-id="320fc-173">x</span></span>    | <span data-ttu-id="320fc-174">x</span><span class="sxs-lookup"><span data-stu-id="320fc-174">x</span></span>     | <span data-ttu-id="320fc-175">x</span><span class="sxs-lookup"><span data-stu-id="320fc-175">x</span></span>    |      |       |



 

## <a name="texture-coordinate-register---ot0-to-ot7"></a><span data-ttu-id="320fc-176">Registro delle coordinate di trama-oT0 in oT7</span><span class="sxs-lookup"><span data-stu-id="320fc-176">Texture Coordinate Register - oT0 to oT7</span></span>

<span data-ttu-id="320fc-177">Le coordinate di trama di output vengono registrate.</span><span class="sxs-lookup"><span data-stu-id="320fc-177">The output texture coordinates registers.</span></span> <span data-ttu-id="320fc-178">In particolare, si tratta di una matrice di registri di dati di output che vengono iterati e usati come coordinate di trama in base alle fasi di campionamento della trama che indirizzano i dati al pixel shader.</span><span class="sxs-lookup"><span data-stu-id="320fc-178">Specifically, these are an array of output data registers that are iterated and used as texture coordinates by the texture sampling stages routing data to the pixel shader.</span></span>



| <span data-ttu-id="320fc-179">Versioni vertex shader</span><span class="sxs-lookup"><span data-stu-id="320fc-179">Vertex shader versions</span></span>      | <span data-ttu-id="320fc-180">1\_1</span><span class="sxs-lookup"><span data-stu-id="320fc-180">1\_1</span></span> | <span data-ttu-id="320fc-181">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="320fc-181">2\_0</span></span> | <span data-ttu-id="320fc-182">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="320fc-182">2\_sw</span></span> | <span data-ttu-id="320fc-183">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="320fc-183">2\_x</span></span> | <span data-ttu-id="320fc-184">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="320fc-184">3\_0</span></span> | <span data-ttu-id="320fc-185">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="320fc-185">3\_sw</span></span> |
|-----------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="320fc-186">Registro coordinate trama</span><span class="sxs-lookup"><span data-stu-id="320fc-186">Texture Coordinate Register</span></span> | <span data-ttu-id="320fc-187">x</span><span class="sxs-lookup"><span data-stu-id="320fc-187">x</span></span>    | <span data-ttu-id="320fc-188">x</span><span class="sxs-lookup"><span data-stu-id="320fc-188">x</span></span>    | <span data-ttu-id="320fc-189">x</span><span class="sxs-lookup"><span data-stu-id="320fc-189">x</span></span>     | <span data-ttu-id="320fc-190">x</span><span class="sxs-lookup"><span data-stu-id="320fc-190">x</span></span>    |      |       |



 

<span data-ttu-id="320fc-191">Quando si scrive in un registro delle coordinate di trama, è consigliabile passare solo il numero di valori a virgola mobile della dimensione della mappa di trama corrispondente.</span><span class="sxs-lookup"><span data-stu-id="320fc-191">When writing to a texture coordinate register, it is recommended to pass only as many floating point values as the dimension of the corresponding texture map.</span></span> <span data-ttu-id="320fc-192">Controllare i valori passati con un modificatore.</span><span class="sxs-lookup"><span data-stu-id="320fc-192">Control the values passed with a modifier.</span></span> <span data-ttu-id="320fc-193">Ad esempio, usare. XY per una mappa di trama 2D.</span><span class="sxs-lookup"><span data-stu-id="320fc-193">For example, use .xy for a 2D texture map.</span></span>

<span data-ttu-id="320fc-194">Quando è abilitata la proiezione di trama per una fase di trama, è necessario scrivere tutti i quattro valori a virgola mobile nel registro di trama corrispondente.</span><span class="sxs-lookup"><span data-stu-id="320fc-194">When texture projection is enabled for a texture stage, all four floating point values must be written to the corresponding texture register.</span></span>

<span data-ttu-id="320fc-195">\*Quando si usa la pipeline programmabile, i flag di trasformazione della trama D3DTTFF devono essere pari a zero.</span><span class="sxs-lookup"><span data-stu-id="320fc-195">Any of the D3DTTFF\* texture transform flags should be zero when the programmable pipeline is being used.</span></span>

### <a name="texture-coordinate-range"></a><span data-ttu-id="320fc-196">Intervallo di coordinate di trama</span><span class="sxs-lookup"><span data-stu-id="320fc-196">Texture Coordinate Range</span></span>

<span data-ttu-id="320fc-197">I dati dei vertici degli oggetti forniscono coordinate di trama di input.</span><span class="sxs-lookup"><span data-stu-id="320fc-197">Object vertex data supplies input texture coordinates.</span></span> <span data-ttu-id="320fc-198">Per gli oggetti che non utilizzano trame affiancate sono in genere presenti coordinate di trama nell'intervallo compreso tra \[ 0 e 1 \] .</span><span class="sxs-lookup"><span data-stu-id="320fc-198">Objects that do not used tiled textures commonly have texture coordinates in the range \[0,1\].</span></span> <span data-ttu-id="320fc-199">Gli oggetti che utilizzano trame affiancate, ad esempio il terreno, presentano in genere coordinate di trama che variano da \[ -?, +? \] dove?</span><span class="sxs-lookup"><span data-stu-id="320fc-199">Objects that use tiled textures, such as terrain, typically have texture coordinates that range from \[-?,+?\] where ?</span></span> <span data-ttu-id="320fc-200">può essere un numero a virgola mobile di grandi dimensioni.</span><span class="sxs-lookup"><span data-stu-id="320fc-200">can be a large floating point number.</span></span>

<span data-ttu-id="320fc-201">L'interpolazione delle coordinate di trama viene eseguita sui dati dei vertici per la rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="320fc-201">Texture coordinate interpolation is performed on vertex data for rasterization.</span></span> <span data-ttu-id="320fc-202">Durante la rasterizzazione, le coordinate di trama vengono interpolate tra i vertici degli oggetti, modificati dal wrapping della trama e ridimensionati in base alle dimensioni della trama (tenendo conto della modalità di indirizzamento della trama) per produrre un indice Integer.</span><span class="sxs-lookup"><span data-stu-id="320fc-202">During rasterization, texture coordinates are interpolated between object vertices, modified by texture wrapping and scaled by the texture size (also taking into account texture address mode) to produce an integer index.</span></span> <span data-ttu-id="320fc-203">L'indice viene quindi utilizzato per eseguire una ricerca di trama.</span><span class="sxs-lookup"><span data-stu-id="320fc-203">The index is then used to perform a texture lookup.</span></span> <span data-ttu-id="320fc-204">È possibile utilizzare MaxTextureRepeat per determinare il numero di volte in cui una trama può essere affiancata.</span><span class="sxs-lookup"><span data-stu-id="320fc-204">MaxTextureRepeat can be used to determine how many times a texture can be tiled.</span></span>

<span data-ttu-id="320fc-205">Se le coordinate di trama vengono lette direttamente in un pixel shader (usando TEXCOORD o texcrd), l'intervallo delle coordinate di trama dipende dall'istruzione e dalla versione pixel shader.</span><span class="sxs-lookup"><span data-stu-id="320fc-205">If texture coordinates are read directly into a pixel shader (using texcoord or texcrd), the texture coordinate range depends on the instruction and the pixel shader version.</span></span>

## <a name="related-topics"></a><span data-ttu-id="320fc-206">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="320fc-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="320fc-207">Registri vertex shader</span><span class="sxs-lookup"><span data-stu-id="320fc-207">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




