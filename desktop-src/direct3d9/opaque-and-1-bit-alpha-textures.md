---
description: Il formato di trama DXT1 è per le trame opache o con un solo colore trasparente.
ms.assetid: a890ed0a-1f68-45b8-93cb-b621d1908d9f
title: Trame alfa opache e a 1 bit (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f629eff594d28d9a807021c0b9df0bd05ea66c3
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104567420"
---
# <a name="opaque-and-1-bit-alpha-textures-direct3d-9"></a><span data-ttu-id="ffff0-103">Trame alfa opache e a 1 bit (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ffff0-103">Opaque and 1-Bit Alpha Textures (Direct3D 9)</span></span>

<span data-ttu-id="ffff0-104">Il formato di trama DXT1 è per le trame opache o con un solo colore trasparente.</span><span class="sxs-lookup"><span data-stu-id="ffff0-104">Texture format DXT1 is for textures that are opaque or have a single transparent color.</span></span>

<span data-ttu-id="ffff0-105">Per ogni blocco alfa opaco o a 1 bit, vengono archiviati i valori a 2 16 bit (formato RGB 5:6:5) e una bitmap 4x4 con 2 bit per pixel.</span><span class="sxs-lookup"><span data-stu-id="ffff0-105">For each opaque or 1-bit alpha block, two 16-bit values (RGB 5:6:5 format) and a 4x4 bitmap with 2 bits per pixel are stored.</span></span> <span data-ttu-id="ffff0-106">Questo totale 64 bit per 16 Texel o quattro bit per Texel.</span><span class="sxs-lookup"><span data-stu-id="ffff0-106">This totals 64 bits for 16 texels, or four bits per texel.</span></span> <span data-ttu-id="ffff0-107">Nella bitmap a blocchi sono disponibili 2 bit per Texel per la selezione tra i quattro colori, due dei quali sono archiviati nei dati codificati.</span><span class="sxs-lookup"><span data-stu-id="ffff0-107">In the block bitmap, there are 2 bits per texel to select between the four colors, two of which are stored in the encoded data.</span></span> <span data-ttu-id="ffff0-108">Gli altri due colori sono derivati da questi colori archiviati dall'interpolazione lineare.</span><span class="sxs-lookup"><span data-stu-id="ffff0-108">The other two colors are derived from these stored colors by linear interpolation.</span></span> <span data-ttu-id="ffff0-109">Questo layout è illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="ffff0-109">This layout is shown in the following diagram.</span></span>

![diagramma del layout bitmap](images/colors1.png)

<span data-ttu-id="ffff0-111">Il formato Alpha a 1 bit si distingue dal formato opaco confrontando i valori dei colori a 2 16 bit archiviati nel blocco.</span><span class="sxs-lookup"><span data-stu-id="ffff0-111">The 1-bit alpha format is distinguished from the opaque format by comparing the two 16-bit color values stored in the block.</span></span> <span data-ttu-id="ffff0-112">Vengono considerati come interi senza segno.</span><span class="sxs-lookup"><span data-stu-id="ffff0-112">They are treated as unsigned integers.</span></span> <span data-ttu-id="ffff0-113">Se il primo colore è maggiore del secondo, significa che sono definiti solo Texel opachi.</span><span class="sxs-lookup"><span data-stu-id="ffff0-113">If the first color is greater than the second, it implies that only opaque texels are defined.</span></span> <span data-ttu-id="ffff0-114">Ciò significa che per rappresentare i Texel vengono utilizzati quattro colori.</span><span class="sxs-lookup"><span data-stu-id="ffff0-114">This means four colors are used to represent the texels.</span></span> <span data-ttu-id="ffff0-115">Nella codifica a quattro colori sono presenti due colori derivati e tutti e quattro i colori vengono distribuiti equamente nello spazio colore RGB.</span><span class="sxs-lookup"><span data-stu-id="ffff0-115">In four-color encoding, there are two derived colors and all four colors are equally distributed in RGB color space.</span></span> <span data-ttu-id="ffff0-116">Questo formato è analogo al formato RGB 5:6:5.</span><span class="sxs-lookup"><span data-stu-id="ffff0-116">This format is analogous to RGB 5:6:5 format.</span></span> <span data-ttu-id="ffff0-117">In caso contrario, per la trasparenza alpha a 1 bit vengono utilizzati tre colori e il quarto è riservato per rappresentare i Texel trasparenti.</span><span class="sxs-lookup"><span data-stu-id="ffff0-117">Otherwise, for 1-bit alpha transparency, three colors are used and the fourth is reserved to represent transparent texels.</span></span>

<span data-ttu-id="ffff0-118">Nella codifica a tre colori è presente un colore derivato e il quarto codice a 2 bit è riservato per indicare un Texel trasparente (informazioni Alpha).</span><span class="sxs-lookup"><span data-stu-id="ffff0-118">In three-color encoding, there is one derived color and the fourth 2-bit code is reserved to indicate a transparent texel (alpha information).</span></span> <span data-ttu-id="ffff0-119">Questo formato è analogo a RGBA 5:5:5:1, in cui viene usato il bit finale per la codifica della maschera alfa.</span><span class="sxs-lookup"><span data-stu-id="ffff0-119">This format is analogous to RGBA 5:5:5:1, where the final bit is used for encoding the alpha mask.</span></span>

<span data-ttu-id="ffff0-120">Nell'esempio di codice seguente viene illustrato l'algoritmo per decidere se è selezionata la codifica a tre o quattro colori:</span><span class="sxs-lookup"><span data-stu-id="ffff0-120">The following code example illustrates the algorithm for deciding whether three- or four-color encoding is selected:</span></span>


```
if (color_0 > color_1) 
{
    // Four-color block: derive the other two colors.    
    // 00 = color_0, 01 = color_1, 10 = color_2, 11 = color_3
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block.
    color_2 = (2 * color_0 + color_1 + 1) / 3;
    color_3 = (color_0 + 2 * color_1 + 1) / 3;
}    
else
{ 
    // Three-color block: derive the other color.
    // 00 = color_0,  01 = color_1,  10 = color_2,  
    // 11 = transparent.
    // These 2-bit codes correspond to the 2-bit fields 
    // stored in the 64-bit block. 
    color_2 = (color_0 + color_1) / 2;    
    color_3 = transparent;    

}
```



<span data-ttu-id="ffff0-121">Prima di eseguire la fusione è consigliabile impostare su zero i componenti RGBA del pixel di trasparenza.</span><span class="sxs-lookup"><span data-stu-id="ffff0-121">It is recommended that you set the RGBA components of the transparency pixel to zero before blending.</span></span>

<span data-ttu-id="ffff0-122">Nelle tabelle seguenti viene illustrato il layout di memoria per il blocco a 8 byte.</span><span class="sxs-lookup"><span data-stu-id="ffff0-122">The following tables show the memory layout for the 8-byte block.</span></span> <span data-ttu-id="ffff0-123">Si presuppone che il primo indice corrisponda alla coordinata y e il secondo corrisponda alla coordinata x.</span><span class="sxs-lookup"><span data-stu-id="ffff0-123">It is assumed that the first index corresponds to the y-coordinate and the second corresponds to the x-coordinate.</span></span> <span data-ttu-id="ffff0-124">Ad esempio, Texel \[ 1 \] \[ 2 \] fa riferimento al pixel della mappa di trama in corrispondenza di (x, y) = (2, 1).</span><span class="sxs-lookup"><span data-stu-id="ffff0-124">For example, Texel\[1\]\[2\] refers to the texture map pixel at (x,y) = (2,1).</span></span>

<span data-ttu-id="ffff0-125">Questa tabella contiene il layout di memoria per il blocco a 8 byte (64 bit).</span><span class="sxs-lookup"><span data-stu-id="ffff0-125">This table contains the memory layout for the 8-byte (64-bit) block.</span></span>



| <span data-ttu-id="ffff0-126">Indirizzo di Word</span><span class="sxs-lookup"><span data-stu-id="ffff0-126">Word address</span></span> | <span data-ttu-id="ffff0-127">Word a 16 bit</span><span class="sxs-lookup"><span data-stu-id="ffff0-127">16-bit word</span></span>    |
|--------------|----------------|
| <span data-ttu-id="ffff0-128">0</span><span class="sxs-lookup"><span data-stu-id="ffff0-128">0</span></span>            | <span data-ttu-id="ffff0-129">Colore \_ 0</span><span class="sxs-lookup"><span data-stu-id="ffff0-129">Color\_0</span></span>       |
| <span data-ttu-id="ffff0-130">1</span><span class="sxs-lookup"><span data-stu-id="ffff0-130">1</span></span>            | <span data-ttu-id="ffff0-131">Colore \_ 1</span><span class="sxs-lookup"><span data-stu-id="ffff0-131">Color\_1</span></span>       |
| <span data-ttu-id="ffff0-132">2</span><span class="sxs-lookup"><span data-stu-id="ffff0-132">2</span></span>            | <span data-ttu-id="ffff0-133">Bitmap Word \_ 0</span><span class="sxs-lookup"><span data-stu-id="ffff0-133">Bitmap Word\_0</span></span> |
| <span data-ttu-id="ffff0-134">3</span><span class="sxs-lookup"><span data-stu-id="ffff0-134">3</span></span>            | <span data-ttu-id="ffff0-135">Bitmap Word \_ 1</span><span class="sxs-lookup"><span data-stu-id="ffff0-135">Bitmap Word\_1</span></span> |



 

<span data-ttu-id="ffff0-136">\_Il colore 0 e \_ il colore 1, i colori dei due estremi sono disposti come segue:</span><span class="sxs-lookup"><span data-stu-id="ffff0-136">Color\_0 and Color\_1, the colors at the two extremes, are laid out as follows:</span></span>



| <span data-ttu-id="ffff0-137">BITS</span><span class="sxs-lookup"><span data-stu-id="ffff0-137">Bits</span></span>        | <span data-ttu-id="ffff0-138">Colore</span><span class="sxs-lookup"><span data-stu-id="ffff0-138">Color</span></span>                 |
|-------------|-----------------------|
| <span data-ttu-id="ffff0-139">4:0 (LSB \* )</span><span class="sxs-lookup"><span data-stu-id="ffff0-139">4:0 (LSB\*)</span></span> | <span data-ttu-id="ffff0-140">Componente colore blu</span><span class="sxs-lookup"><span data-stu-id="ffff0-140">Blue color component</span></span>  |
| <span data-ttu-id="ffff0-141">10:5</span><span class="sxs-lookup"><span data-stu-id="ffff0-141">10:5</span></span>        | <span data-ttu-id="ffff0-142">Componente colore verde</span><span class="sxs-lookup"><span data-stu-id="ffff0-142">Green color component</span></span> |
| <span data-ttu-id="ffff0-143">15:11</span><span class="sxs-lookup"><span data-stu-id="ffff0-143">15:11</span></span>       | <span data-ttu-id="ffff0-144">Componente colore rosso</span><span class="sxs-lookup"><span data-stu-id="ffff0-144">Red color component</span></span>   |



 

<span data-ttu-id="ffff0-145">\*bit meno significativo</span><span class="sxs-lookup"><span data-stu-id="ffff0-145">\*least-significant bit</span></span>

<span data-ttu-id="ffff0-146">La bitmap Word \_ 0 è configurata come segue:</span><span class="sxs-lookup"><span data-stu-id="ffff0-146">Bitmap Word\_0 is laid out as follows:</span></span>



| <span data-ttu-id="ffff0-147">BITS</span><span class="sxs-lookup"><span data-stu-id="ffff0-147">Bits</span></span>          | <span data-ttu-id="ffff0-148">Texel</span><span class="sxs-lookup"><span data-stu-id="ffff0-148">Texel</span></span>           |
|---------------|-----------------|
| <span data-ttu-id="ffff0-149">1:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="ffff0-149">1:0 (LSB)</span></span>     | <span data-ttu-id="ffff0-150">Texel \[ 0 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="ffff0-150">Texel\[0\]\[0\]</span></span> |
| <span data-ttu-id="ffff0-151">3:2</span><span class="sxs-lookup"><span data-stu-id="ffff0-151">3:2</span></span>           | <span data-ttu-id="ffff0-152">Texel \[ 0 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="ffff0-152">Texel\[0\]\[1\]</span></span> |
| <span data-ttu-id="ffff0-153">5:4</span><span class="sxs-lookup"><span data-stu-id="ffff0-153">5:4</span></span>           | <span data-ttu-id="ffff0-154">Texel \[ 0 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="ffff0-154">Texel\[0\]\[2\]</span></span> |
| <span data-ttu-id="ffff0-155">7:6</span><span class="sxs-lookup"><span data-stu-id="ffff0-155">7:6</span></span>           | <span data-ttu-id="ffff0-156">Texel \[ 0 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="ffff0-156">Texel\[0\]\[3\]</span></span> |
| <span data-ttu-id="ffff0-157">9:8</span><span class="sxs-lookup"><span data-stu-id="ffff0-157">9:8</span></span>           | <span data-ttu-id="ffff0-158">Texel \[ 1 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="ffff0-158">Texel\[1\]\[0\]</span></span> |
| <span data-ttu-id="ffff0-159">11:10</span><span class="sxs-lookup"><span data-stu-id="ffff0-159">11:10</span></span>         | <span data-ttu-id="ffff0-160">Texel \[ 1 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="ffff0-160">Texel\[1\]\[1\]</span></span> |
| <span data-ttu-id="ffff0-161">13:12</span><span class="sxs-lookup"><span data-stu-id="ffff0-161">13:12</span></span>         | <span data-ttu-id="ffff0-162">Texel \[ 1 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="ffff0-162">Texel\[1\]\[2\]</span></span> |
| <span data-ttu-id="ffff0-163">15:14 (MSB \* )</span><span class="sxs-lookup"><span data-stu-id="ffff0-163">15:14 (MSB\*)</span></span> | <span data-ttu-id="ffff0-164">Texel \[ 1 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="ffff0-164">Texel\[1\]\[3\]</span></span> |



 

<span data-ttu-id="ffff0-165">\*bit più significativo (MSB)</span><span class="sxs-lookup"><span data-stu-id="ffff0-165">\*most significant bit (MSB)</span></span>

<span data-ttu-id="ffff0-166">La bitmap Word \_ 1 è configurata come segue:</span><span class="sxs-lookup"><span data-stu-id="ffff0-166">Bitmap Word\_1 is laid out as follows:</span></span>



| <span data-ttu-id="ffff0-167">BITS</span><span class="sxs-lookup"><span data-stu-id="ffff0-167">Bits</span></span>        | <span data-ttu-id="ffff0-168">Texel</span><span class="sxs-lookup"><span data-stu-id="ffff0-168">Texel</span></span>           |
|-------------|-----------------|
| <span data-ttu-id="ffff0-169">1:0 (LSB)</span><span class="sxs-lookup"><span data-stu-id="ffff0-169">1:0 (LSB)</span></span>   | <span data-ttu-id="ffff0-170">Texel \[ 2 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="ffff0-170">Texel\[2\]\[0\]</span></span> |
| <span data-ttu-id="ffff0-171">3:2</span><span class="sxs-lookup"><span data-stu-id="ffff0-171">3:2</span></span>         | <span data-ttu-id="ffff0-172">Texel \[ 2 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="ffff0-172">Texel\[2\]\[1\]</span></span> |
| <span data-ttu-id="ffff0-173">5:4</span><span class="sxs-lookup"><span data-stu-id="ffff0-173">5:4</span></span>         | <span data-ttu-id="ffff0-174">Texel \[ 2 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="ffff0-174">Texel\[2\]\[2\]</span></span> |
| <span data-ttu-id="ffff0-175">7:6</span><span class="sxs-lookup"><span data-stu-id="ffff0-175">7:6</span></span>         | <span data-ttu-id="ffff0-176">Texel \[ 2 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="ffff0-176">Texel\[2\]\[3\]</span></span> |
| <span data-ttu-id="ffff0-177">9:8</span><span class="sxs-lookup"><span data-stu-id="ffff0-177">9:8</span></span>         | <span data-ttu-id="ffff0-178">Texel \[ 3 \] \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="ffff0-178">Texel\[3\]\[0\]</span></span> |
| <span data-ttu-id="ffff0-179">11:10</span><span class="sxs-lookup"><span data-stu-id="ffff0-179">11:10</span></span>       | <span data-ttu-id="ffff0-180">Texel \[ 3 \] \[ 1\]</span><span class="sxs-lookup"><span data-stu-id="ffff0-180">Texel\[3\]\[1\]</span></span> |
| <span data-ttu-id="ffff0-181">13:12</span><span class="sxs-lookup"><span data-stu-id="ffff0-181">13:12</span></span>       | <span data-ttu-id="ffff0-182">Texel \[ 3 \] \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="ffff0-182">Texel\[3\]\[2\]</span></span> |
| <span data-ttu-id="ffff0-183">15:14 (MSB)</span><span class="sxs-lookup"><span data-stu-id="ffff0-183">15:14 (MSB)</span></span> | <span data-ttu-id="ffff0-184">Texel \[ 3 \] \[ 3\]</span><span class="sxs-lookup"><span data-stu-id="ffff0-184">Texel\[3\]\[3\]</span></span> |



 

## <a name="example-of-opaque-color-encoding"></a><span data-ttu-id="ffff0-185">Esempio di codifica dei colori opaca</span><span class="sxs-lookup"><span data-stu-id="ffff0-185">Example of Opaque Color Encoding</span></span>

<span data-ttu-id="ffff0-186">Come esempio di codifica opaca, si supponga che i colori rosso e nero siano estremi.</span><span class="sxs-lookup"><span data-stu-id="ffff0-186">As an example of opaque encoding, assume that the colors red and black are at the extremes.</span></span> <span data-ttu-id="ffff0-187">Il colore rosso è \_ 0 e il nero è il colore \_ 1.</span><span class="sxs-lookup"><span data-stu-id="ffff0-187">Red is color\_0, and black is color\_1.</span></span> <span data-ttu-id="ffff0-188">Sono disponibili quattro colori interpolati che formano la sfumatura distribuita in modo uniforme tra di essi.</span><span class="sxs-lookup"><span data-stu-id="ffff0-188">There are four interpolated colors that form the uniformly distributed gradient between them.</span></span> <span data-ttu-id="ffff0-189">Per determinare i valori per la bitmap 4x4, vengono usati i calcoli seguenti:</span><span class="sxs-lookup"><span data-stu-id="ffff0-189">To determine the values for the 4x4 bitmap, the following calculations are used:</span></span>


```
00 ? color_0
01 ? color_1
10 ? 2/3 color_0 + 1/3 color_1
11 ? 1/3 color_0 + 2/3 color_1
```



<span data-ttu-id="ffff0-190">La bitmap sarà quindi simile al diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="ffff0-190">The bitmap then looks like the following diagram.</span></span>

![Diagramma che mostra il layout della bitmap espansa.](images/colors2.png)

<span data-ttu-id="ffff0-192">Questo aspetto è simile alla serie di colori illustrata di seguito.</span><span class="sxs-lookup"><span data-stu-id="ffff0-192">This looks like the following illustrated series of colors.</span></span>

> [!Note]  
> <span data-ttu-id="ffff0-193">In un'immagine, pixel (0, 0) viene visualizzato in alto a sinistra.</span><span class="sxs-lookup"><span data-stu-id="ffff0-193">In an image, pixel (0,0) appears on the top left.</span></span>

 

![illustrazione di una sfumatura con codifica opaca](images/redsquares.png)

## <a name="example-of-1-bit-alpha-encoding"></a><span data-ttu-id="ffff0-195">Esempio di codifica Alpha a 1 bit</span><span class="sxs-lookup"><span data-stu-id="ffff0-195">Example of 1-Bit Alpha Encoding</span></span>

<span data-ttu-id="ffff0-196">Questo formato è selezionato quando l'intero senza segno a 16 bit, colore \_ 0, è minore dell'intero senza segno a 16 bit, colore \_ 1.</span><span class="sxs-lookup"><span data-stu-id="ffff0-196">This format is selected when the unsigned 16-bit integer, color\_0, is less than the unsigned 16-bit integer, color\_1.</span></span> <span data-ttu-id="ffff0-197">Un esempio di in cui è possibile usare questo formato è il lascia su un albero, visualizzato su un cielo blu.</span><span class="sxs-lookup"><span data-stu-id="ffff0-197">An example of where this format can be used is leaves on a tree, shown against a blue sky.</span></span> <span data-ttu-id="ffff0-198">Alcuni Texel possono essere contrassegnati come trasparenti mentre tre tonalità di verde sono ancora disponibili per le foglie.</span><span class="sxs-lookup"><span data-stu-id="ffff0-198">Some texels can be marked as transparent while three shades of green are still available for the leaves.</span></span> <span data-ttu-id="ffff0-199">Due colori correggono gli estremi e il terzo è un colore interpolato.</span><span class="sxs-lookup"><span data-stu-id="ffff0-199">Two colors fix the extremes, and the third is an interpolated color.</span></span>

<span data-ttu-id="ffff0-200">Nell'illustrazione seguente viene illustrato un esempio di tale immagine.</span><span class="sxs-lookup"><span data-stu-id="ffff0-200">The following illustration is an example of such a picture.</span></span>

![illustrazione della codifica Alpha a 1 bit](images/greenthing.png)

<span data-ttu-id="ffff0-202">Si noti che, in cui l'immagine viene visualizzata come bianca, il Texel viene codificato come trasparente.</span><span class="sxs-lookup"><span data-stu-id="ffff0-202">Note that where the image is shown as white, the texel would be encoded as transparent.</span></span> <span data-ttu-id="ffff0-203">Si noti inoltre che i componenti RGBA dei Texel trasparenti devono essere impostati su zero prima della fusione.</span><span class="sxs-lookup"><span data-stu-id="ffff0-203">Also note that the RGBA components of the transparent texels should be set to zero before blending.</span></span>

<span data-ttu-id="ffff0-204">La codifica bitmap per i colori e la trasparenza viene determinata utilizzando i calcoli seguenti.</span><span class="sxs-lookup"><span data-stu-id="ffff0-204">The bitmap encoding for the colors and the transparency is determined using the following calculations.</span></span>


```
00 ? color_0
01 ? color_1
10 ? 1/2 color_0 + 1/2 color_1
11   ?   Transparent
```



<span data-ttu-id="ffff0-205">La bitmap sarà quindi simile al diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="ffff0-205">The bitmap then looks like the following diagram.</span></span>

![diagramma del layout di bitmap espanso](images/colors3.png)

## <a name="related-topics"></a><span data-ttu-id="ffff0-207">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ffff0-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffff0-208">Risorse di trama compresse</span><span class="sxs-lookup"><span data-stu-id="ffff0-208">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 



