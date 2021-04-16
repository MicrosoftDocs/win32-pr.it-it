---
description: Esistono due modi per codificare le mappe di trama che presentano una trasparenza più complessa.
ms.assetid: cae788f6-60f1-4987-8f06-bf4256bccd9b
title: Trame con canali alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c361b0335ef4f36b4efc9c90c71270e855f5db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104557200"
---
# <a name="textures-with-alpha-channels-direct3d-9"></a><span data-ttu-id="a3bbe-103">Trame con canali alfa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="a3bbe-103">Textures with Alpha Channels (Direct3D 9)</span></span>

<span data-ttu-id="a3bbe-104">Esistono due modi per codificare le mappe di trama che presentano una trasparenza più complessa.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-104">There are two ways to encode texture maps that exhibit more complex transparency.</span></span> <span data-ttu-id="a3bbe-105">In ogni caso, un blocco che descrive la trasparenza precede il blocco a 64 bit già descritto.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-105">In each case, a block that describes the transparency precedes the 64-bit block already described.</span></span> <span data-ttu-id="a3bbe-106">La trasparenza è rappresentata come bitmap 4x4 con 4 bit per pixel (codifica esplicita) o con meno bit e interpolazione lineare che è analoga a quella usata per la codifica dei colori.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-106">The transparency is either represented as a 4x4 bitmap with 4 bits per pixel (explicit encoding), or with fewer bits and linear interpolation that is analogous to what is used for color encoding.</span></span>

<span data-ttu-id="a3bbe-107">Il blocco di trasparenza e il blocco di colore vengono disposti come illustrato nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-107">The transparency block and the color block are arranged as shown in the following table.</span></span>



| <span data-ttu-id="a3bbe-108">Indirizzo di Word</span><span class="sxs-lookup"><span data-stu-id="a3bbe-108">Word address</span></span> | <span data-ttu-id="a3bbe-109">blocco a 64 bit</span><span class="sxs-lookup"><span data-stu-id="a3bbe-109">64-bit block</span></span>                      |
|--------------|-----------------------------------|
| <span data-ttu-id="a3bbe-110">3:0</span><span class="sxs-lookup"><span data-stu-id="a3bbe-110">3:0</span></span>          | <span data-ttu-id="a3bbe-111">Blocco trasparenza</span><span class="sxs-lookup"><span data-stu-id="a3bbe-111">Transparency block</span></span>                |
| <span data-ttu-id="a3bbe-112">7:4</span><span class="sxs-lookup"><span data-stu-id="a3bbe-112">7:4</span></span>          | <span data-ttu-id="a3bbe-113">Descritto in precedenza blocco a 64 bit</span><span class="sxs-lookup"><span data-stu-id="a3bbe-113">Previously described 64-bit block</span></span> |



 

## <a name="explicit-texture-encoding"></a><span data-ttu-id="a3bbe-114">Codifica della trama esplicita</span><span class="sxs-lookup"><span data-stu-id="a3bbe-114">Explicit Texture Encoding</span></span>

<span data-ttu-id="a3bbe-115">Per la codifica di trama esplicita (formati DXT2 e DXT3), i componenti alfa dei Texel che descrivono la trasparenza sono codificati in una bitmap 4x4 con 4 bit per Texel.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-115">For explicit texture encoding (DXT2 and DXT3 formats), the alpha components of the texels that describe transparency are encoded in a 4x4 bitmap with 4 bits per texel.</span></span> <span data-ttu-id="a3bbe-116">Questi quattro bit possono essere realizzati attraverso diversi mezzi, ad esempio la rethering o l'utilizzo dei quattro bit più significativi dei dati alfa.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-116">These four bits can be achieved through a variety of means such as dithering or by using the four most significant bits of the alpha data.</span></span> <span data-ttu-id="a3bbe-117">Tuttavia, vengono usati così come sono, senza alcuna forma di interpolazione.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-117">However they are produced, they are used just as they are, without any form of interpolation.</span></span>

<span data-ttu-id="a3bbe-118">Il diagramma seguente illustra un blocco di trasparenza a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-118">The following diagram shows a 64-bit transparency block.</span></span>

![diagramma di un blocco di trasparenza a 64 bit](images/colors4.png)

> [!Note]  
> <span data-ttu-id="a3bbe-120">Il metodo di compressione di Direct3D usa i quattro bit più significativi.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-120">The compression method of Direct3D uses the four most significant bits.</span></span>

 

<span data-ttu-id="a3bbe-121">Le tabelle seguenti illustrano come le informazioni alfa sono disposte in memoria, per ogni parola a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-121">The following tables illustrate how the alpha information is laid out in memory, for each 16-bit word.</span></span>

<span data-ttu-id="a3bbe-122">Questa tabella contiene il layout per Word 0.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-122">This table contains the layout for word 0.</span></span>



| <span data-ttu-id="a3bbe-123">BITS</span><span class="sxs-lookup"><span data-stu-id="a3bbe-123">Bits</span></span>          | <span data-ttu-id="a3bbe-124">Alfa</span><span class="sxs-lookup"><span data-stu-id="a3bbe-124">Alpha</span></span>      |
|---------------|------------|
| <span data-ttu-id="a3bbe-125">3:0 (LSB \* )</span><span class="sxs-lookup"><span data-stu-id="a3bbe-125">3:0 (LSB\*)</span></span>   | <span data-ttu-id="a3bbe-126">\[0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="a3bbe-126">\[0\]\[0\]</span></span> |
| <span data-ttu-id="a3bbe-127">7:4</span><span class="sxs-lookup"><span data-stu-id="a3bbe-127">7:4</span></span>           | <span data-ttu-id="a3bbe-128">\[0 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="a3bbe-128">\[0\]\[1\]</span></span> |
| <span data-ttu-id="a3bbe-129">11:8</span><span class="sxs-lookup"><span data-stu-id="a3bbe-129">11:8</span></span>          | <span data-ttu-id="a3bbe-130">\[0 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="a3bbe-130">\[0\]\[2\]</span></span> |
| <span data-ttu-id="a3bbe-131">15:12 (MSB \* )</span><span class="sxs-lookup"><span data-stu-id="a3bbe-131">15:12 (MSB\*)</span></span> | <span data-ttu-id="a3bbe-132">\[0 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="a3bbe-132">\[0\]\[3\]</span></span> |



 

<span data-ttu-id="a3bbe-133">\*bit meno significativo, bit più significativo (MSB)</span><span class="sxs-lookup"><span data-stu-id="a3bbe-133">\*least-significant bit, most significant bit (MSB)</span></span>

<span data-ttu-id="a3bbe-134">Questa tabella contiene il layout per Word 1.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-134">This table contains the layout for word 1.</span></span>



| <span data-ttu-id="a3bbe-135">BITS</span><span class="sxs-lookup"><span data-stu-id="a3bbe-135">Bits</span></span>        | <span data-ttu-id="a3bbe-136">Alfa</span><span class="sxs-lookup"><span data-stu-id="a3bbe-136">Alpha</span></span>      |
|-------------|------------|
| <span data-ttu-id="a3bbe-137">3:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="a3bbe-137">3:0 (LSB)</span></span>   | <span data-ttu-id="a3bbe-138">\[1 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="a3bbe-138">\[1\]\[0\]</span></span> |
| <span data-ttu-id="a3bbe-139">7:4</span><span class="sxs-lookup"><span data-stu-id="a3bbe-139">7:4</span></span>         | <span data-ttu-id="a3bbe-140">\[1 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="a3bbe-140">\[1\]\[1\]</span></span> |
| <span data-ttu-id="a3bbe-141">11:8</span><span class="sxs-lookup"><span data-stu-id="a3bbe-141">11:8</span></span>        | <span data-ttu-id="a3bbe-142">\[1 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="a3bbe-142">\[1\]\[2\]</span></span> |
| <span data-ttu-id="a3bbe-143">15:12 (MSB)</span><span class="sxs-lookup"><span data-stu-id="a3bbe-143">15:12 (MSB)</span></span> | <span data-ttu-id="a3bbe-144">\[1 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="a3bbe-144">\[1\]\[3\]</span></span> |



 

<span data-ttu-id="a3bbe-145">Questa tabella contiene il layout per Word 2.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-145">This table contains the layout for word 2.</span></span>



| <span data-ttu-id="a3bbe-146">BITS</span><span class="sxs-lookup"><span data-stu-id="a3bbe-146">Bits</span></span>        | <span data-ttu-id="a3bbe-147">Alfa</span><span class="sxs-lookup"><span data-stu-id="a3bbe-147">Alpha</span></span>      |
|-------------|------------|
| <span data-ttu-id="a3bbe-148">3:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="a3bbe-148">3:0 (LSB)</span></span>   | <span data-ttu-id="a3bbe-149">\[2 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="a3bbe-149">\[2\]\[0\]</span></span> |
| <span data-ttu-id="a3bbe-150">7:4</span><span class="sxs-lookup"><span data-stu-id="a3bbe-150">7:4</span></span>         | <span data-ttu-id="a3bbe-151">\[2 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="a3bbe-151">\[2\]\[1\]</span></span> |
| <span data-ttu-id="a3bbe-152">11:8</span><span class="sxs-lookup"><span data-stu-id="a3bbe-152">11:8</span></span>        | <span data-ttu-id="a3bbe-153">\[2 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="a3bbe-153">\[2\]\[2\]</span></span> |
| <span data-ttu-id="a3bbe-154">15:12 (MSB)</span><span class="sxs-lookup"><span data-stu-id="a3bbe-154">15:12 (MSB)</span></span> | <span data-ttu-id="a3bbe-155">\[2 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="a3bbe-155">\[2\]\[3\]</span></span> |



 

<span data-ttu-id="a3bbe-156">Questa tabella contiene il layout per Word 3.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-156">This table contains the layout for word 3.</span></span>



| <span data-ttu-id="a3bbe-157">BITS</span><span class="sxs-lookup"><span data-stu-id="a3bbe-157">Bits</span></span>        | <span data-ttu-id="a3bbe-158">Alfa</span><span class="sxs-lookup"><span data-stu-id="a3bbe-158">Alpha</span></span>      |
|-------------|------------|
| <span data-ttu-id="a3bbe-159">3:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="a3bbe-159">3:0 (LSB)</span></span>   | <span data-ttu-id="a3bbe-160">\[3 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="a3bbe-160">\[3\]\[0\]</span></span> |
| <span data-ttu-id="a3bbe-161">7:4</span><span class="sxs-lookup"><span data-stu-id="a3bbe-161">7:4</span></span>         | <span data-ttu-id="a3bbe-162">\[3 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="a3bbe-162">\[3\]\[1\]</span></span> |
| <span data-ttu-id="a3bbe-163">11:8</span><span class="sxs-lookup"><span data-stu-id="a3bbe-163">11:8</span></span>        | <span data-ttu-id="a3bbe-164">\[3 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="a3bbe-164">\[3\]\[2\]</span></span> |
| <span data-ttu-id="a3bbe-165">15:12 (MSB)</span><span class="sxs-lookup"><span data-stu-id="a3bbe-165">15:12 (MSB)</span></span> | <span data-ttu-id="a3bbe-166">\[3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="a3bbe-166">\[3\]\[3\]</span></span> |



 

<span data-ttu-id="a3bbe-167">La differenza tra DXT2 e DXT3 consiste nel fatto che, nel formato DXT2, si presuppone che i dati relativi ai colori siano stati premoltiplicati da Alpha.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-167">The difference between DXT2 and DXT3 are that, in the DXT2 format, it is assumed that the color data has been premultiplied by alpha.</span></span> <span data-ttu-id="a3bbe-168">Nel formato DXT3 si presuppone che il colore non sia premoltiplicato da Alpha.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-168">In the DXT3 format, it is assumed that the color is not premultiplied by alpha.</span></span> <span data-ttu-id="a3bbe-169">Questi due formati sono necessari perché, nella maggior parte dei casi, nel momento in cui viene utilizzata una trama, solo l'analisi dei dati non è sufficiente per determinare se i valori dei colori sono stati moltiplicati per alfa.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-169">These two formats are needed because, in most cases, by the time a texture is used, just examining the data is not sufficient to determine if the color values have been multiplied by alpha.</span></span> <span data-ttu-id="a3bbe-170">Poiché queste informazioni sono necessarie in fase di esecuzione, per distinguere questi casi vengono usati i due codici FOURCC.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-170">Because this information is needed at run time, the two FOURCC codes are used to differentiate these cases.</span></span> <span data-ttu-id="a3bbe-171">Tuttavia, i dati e il metodo di interpolazione usati per questi due formati sono identici.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-171">However, the data and interpolation method used for these two formats is identical.</span></span>

<span data-ttu-id="a3bbe-172">Il confronto dei colori usato in DXT1 per determinare se il Texel è trasparente non viene usato in questo formato.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-172">The color compare used in DXT1 to determine if the texel is transparent is not used in this format.</span></span> <span data-ttu-id="a3bbe-173">Si presuppone che senza il confronto dei colori i dati del colore vengano sempre considerati come se fossero in modalità a 4 colori.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-173">It is assumed that without the color compare the color data is always treated as if in 4-color mode.</span></span> <span data-ttu-id="a3bbe-174">In altre parole, l'istruzione If all'inizio del codice DXT1 dovrebbe essere la seguente:</span><span class="sxs-lookup"><span data-stu-id="a3bbe-174">In other words, the if statement at the top of the DXT1 code should be the following:</span></span>


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="three-bit-linear-alpha-interpolation"></a><span data-ttu-id="a3bbe-175">Interpolazione alfa lineare Three-Bit</span><span class="sxs-lookup"><span data-stu-id="a3bbe-175">Three-Bit Linear Alpha Interpolation</span></span>

<span data-ttu-id="a3bbe-176">La codifica della trasparenza per i formati DXT4 e DXT5 si basa su un concetto simile alla codifica lineare utilizzata per il colore.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-176">The encoding of transparency for the DXT4 and DXT5 formats is based on a concept similar to the linear encoding used for color.</span></span> <span data-ttu-id="a3bbe-177">I valori alfa a 2 8 bit e una bitmap 4x4 con tre bit per pixel vengono archiviati nei primi otto byte del blocco.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-177">Two 8-bit alpha values and a 4x4 bitmap with three bits per pixel are stored in the first eight bytes of the block.</span></span> <span data-ttu-id="a3bbe-178">I valori alfa rappresentativi vengono utilizzati per interpolare i valori alfa intermedi.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-178">The representative alpha values are used to interpolate intermediate alpha values.</span></span> <span data-ttu-id="a3bbe-179">Ulteriori informazioni sono disponibili nel modo in cui vengono archiviati i due valori alfa.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-179">Additional information is available in the way the two alpha values are stored.</span></span> <span data-ttu-id="a3bbe-180">Se alfa \_ 0 è maggiore di alfa \_ 1, verranno creati sei valori alfa intermedi dall'interpolazione.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-180">If alpha\_0 is greater than alpha\_1, then six intermediate alpha values are created by the interpolation.</span></span> <span data-ttu-id="a3bbe-181">In caso contrario, vengono interpolati quattro valori alfa intermedi tra gli estremi alfa specificati.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-181">Otherwise, four intermediate alpha values are interpolated between the specified alpha extremes.</span></span> <span data-ttu-id="a3bbe-182">I due valori alfa impliciti aggiuntivi sono 0 (completamente trasparente) e 255 (completamente opaco).</span><span class="sxs-lookup"><span data-stu-id="a3bbe-182">The two additional implicit alpha values are 0 (fully transparent) and 255 (fully opaque).</span></span>

<span data-ttu-id="a3bbe-183">Nell'esempio di codice riportato di seguito viene illustrato questo algoritmo.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-183">The following code example illustrates this algorithm.</span></span>


```
// 8-alpha or 6-alpha block?    
if (alpha_0 > alpha_1) {    
    // 8-alpha block:  derive the other six alphas.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (6 * alpha_0 + 1 * alpha_1 + 3) / 7;    // bit code 010
    alpha_3 = (5 * alpha_0 + 2 * alpha_1 + 3) / 7;    // bit code 011
    alpha_4 = (4 * alpha_0 + 3 * alpha_1 + 3) / 7;    // bit code 100
    alpha_5 = (3 * alpha_0 + 4 * alpha_1 + 3) / 7;    // bit code 101
    alpha_6 = (2 * alpha_0 + 5 * alpha_1 + 3) / 7;    // bit code 110
    alpha_7 = (1 * alpha_0 + 6 * alpha_1 + 3) / 7;    // bit code 111  
}    
else {  
    // 6-alpha block.    
    // Bit code 000 = alpha_0, 001 = alpha_1, others are interpolated.
    alpha_2 = (4 * alpha_0 + 1 * alpha_1 + 2) / 5;    // Bit code 010
    alpha_3 = (3 * alpha_0 + 2 * alpha_1 + 2) / 5;    // Bit code 011
    alpha_4 = (2 * alpha_0 + 3 * alpha_1 + 2) / 5;    // Bit code 100
    alpha_5 = (1 * alpha_0 + 4 * alpha_1 + 2) / 5;    // Bit code 101
    alpha_6 = 0;                                      // Bit code 110
    alpha_7 = 255;                                    // Bit code 111
}
```



<span data-ttu-id="a3bbe-184">Il layout di memoria del blocco alfa è il seguente:</span><span class="sxs-lookup"><span data-stu-id="a3bbe-184">The memory layout of the alpha block is as follows:</span></span>



| <span data-ttu-id="a3bbe-185">Byte</span><span class="sxs-lookup"><span data-stu-id="a3bbe-185">Byte</span></span> | <span data-ttu-id="a3bbe-186">Alfa</span><span class="sxs-lookup"><span data-stu-id="a3bbe-186">Alpha</span></span>                                                          |
|------|----------------------------------------------------------------|
| <span data-ttu-id="a3bbe-187">0</span><span class="sxs-lookup"><span data-stu-id="a3bbe-187">0</span></span>    | <span data-ttu-id="a3bbe-188">Alfa \_ 0</span><span class="sxs-lookup"><span data-stu-id="a3bbe-188">Alpha\_0</span></span>                                                       |
| <span data-ttu-id="a3bbe-189">1</span><span class="sxs-lookup"><span data-stu-id="a3bbe-189">1</span></span>    | <span data-ttu-id="a3bbe-190">Alfa \_ 1</span><span class="sxs-lookup"><span data-stu-id="a3bbe-190">Alpha\_1</span></span>                                                       |
| <span data-ttu-id="a3bbe-191">2</span><span class="sxs-lookup"><span data-stu-id="a3bbe-191">2</span></span>    | <span data-ttu-id="a3bbe-192">\[0 \] \[ 2 \] (2 MSBs), \[ 0 \] \[ 1 \] , \[ 0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="a3bbe-192">\[0\]\[2\] (2 MSBs), \[0\]\[1\], \[0\]\[0\]</span></span>                    |
| <span data-ttu-id="a3bbe-193">3</span><span class="sxs-lookup"><span data-stu-id="a3bbe-193">3</span></span>    | <span data-ttu-id="a3bbe-194">\[1 \] \[ 1 \] (1 MSB), \[ 1 \] \[ 0 \] , \[ 0 \] \[ 3 \] , \[ 0 \] \[ 2 \] (1 LSB)</span><span class="sxs-lookup"><span data-stu-id="a3bbe-194">\[1\]\[1\] (1 MSB), \[1\]\[0\], \[0\]\[3\], \[0\]\[2\] (1 LSB)</span></span> |
| <span data-ttu-id="a3bbe-195">4</span><span class="sxs-lookup"><span data-stu-id="a3bbe-195">4</span></span>    | <span data-ttu-id="a3bbe-196">\[1 \] \[ 3 \] , \[ 1 \] \[ 2 \] , \[ 1 \] \[ 1 \] (2 LSB)</span><span class="sxs-lookup"><span data-stu-id="a3bbe-196">\[1\]\[3\], \[1\]\[2\], \[1\]\[1\] (2 LSBs)</span></span>                    |
| <span data-ttu-id="a3bbe-197">5</span><span class="sxs-lookup"><span data-stu-id="a3bbe-197">5</span></span>    | <span data-ttu-id="a3bbe-198">\[2 \] \[ 2 \] (2 MSBs), \[ 2 \] \[ 1 \] , \[ 2 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="a3bbe-198">\[2\]\[2\] (2 MSBs), \[2\]\[1\], \[2\]\[0\]</span></span>                    |
| <span data-ttu-id="a3bbe-199">6</span><span class="sxs-lookup"><span data-stu-id="a3bbe-199">6</span></span>    | <span data-ttu-id="a3bbe-200">\[3 \] \[ 1 \] (1 MSB), \[ 3 \] \[ 0 \] , \[ 2 \] \[ 3 \] , \[ 2 \] \[ 2 \] (1 LSB)</span><span class="sxs-lookup"><span data-stu-id="a3bbe-200">\[3\]\[1\] (1 MSB), \[3\]\[0\], \[2\]\[3\], \[2\]\[2\] (1 LSB)</span></span> |
| <span data-ttu-id="a3bbe-201">7</span><span class="sxs-lookup"><span data-stu-id="a3bbe-201">7</span></span>    | <span data-ttu-id="a3bbe-202">\[3 \] \[ 3 \] , \[ 3 \] \[ 2 \] , \[ 3 \] \[ 1 \] (2 LSB)</span><span class="sxs-lookup"><span data-stu-id="a3bbe-202">\[3\]\[3\], \[3\]\[2\], \[3\]\[1\] (2 LSBs)</span></span>                    |



 

<span data-ttu-id="a3bbe-203">La differenza tra DXT4 e DXT5 è che nel formato DXT4 si presuppone che i dati dei colori siano stati premoltiplicati da Alpha.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-203">The difference between DXT4 and DXT5 is that in the DXT4 format it is assumed that the color data has been premultiplied by alpha.</span></span> <span data-ttu-id="a3bbe-204">Nel formato DXT5 si presuppone che il colore non sia premoltiplicato da Alpha.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-204">In the DXT5 format, it is assumed the color is not premultiplied by alpha.</span></span> <span data-ttu-id="a3bbe-205">Questi due formati sono necessari perché, nella maggior parte dei casi, nel momento in cui viene utilizzata una trama, solo l'analisi dei dati non è sufficiente per determinare se i valori dei colori sono stati moltiplicati per alfa.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-205">These two formats are needed because, in most cases, by the time a texture is used, just examining the data is not sufficient to determine if the color values have been multiplied by alpha.</span></span> <span data-ttu-id="a3bbe-206">Poiché queste informazioni sono necessarie in fase di esecuzione, per distinguere questi casi vengono usati i due codici FOURCC.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-206">Because this information is needed at run time, the two FOURCC codes are used to differentiate these cases.</span></span> <span data-ttu-id="a3bbe-207">Tuttavia, i dati e il metodo di interpolazione usati per questi due formati sono identici.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-207">However, the data and interpolation method used for these two formats is identical.</span></span>

<span data-ttu-id="a3bbe-208">Il confronto dei colori usato in DXT1 per determinare se il Texel è trasparente non viene usato con questi formati.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-208">The color compare used in DXT1 to determine if the texel is transparent is not used with these formats.</span></span> <span data-ttu-id="a3bbe-209">Si presuppone che senza il confronto dei colori i dati del colore vengano sempre considerati come se fossero in modalità a 4 colori.</span><span class="sxs-lookup"><span data-stu-id="a3bbe-209">It is assumed that without the color compare the color data is always treated as if in 4-color mode.</span></span> <span data-ttu-id="a3bbe-210">In altre parole, l'istruzione If all'inizio del codice DXT1 deve essere:</span><span class="sxs-lookup"><span data-stu-id="a3bbe-210">In other words, the if statement at the top of the DXT1 code should be:</span></span>


```
if ((color_0 > color_1) OR !DXT1) {
```



## <a name="related-topics"></a><span data-ttu-id="a3bbe-211">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a3bbe-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3bbe-212">Risorse di trama compresse</span><span class="sxs-lookup"><span data-stu-id="a3bbe-212">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 



