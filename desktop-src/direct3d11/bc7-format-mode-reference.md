---
title: Riferimento alla modalità di formattazione BC7
description: Questa documentazione contiene un elenco delle 8 modalità di blocco e delle allocazioni di bit per i blocchi di formato della compressione di trama BC7.
ms.assetid: B1CEB729-6694-49BF-ACB9-FD1EFAB0B0D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719a223e6ac057b949d5e1222582058f637ec526
ms.sourcegitcommit: 62e758931c610782807c7c9fad284921a6c56232
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/22/2020
ms.locfileid: "104398431"
---
# <a name="bc7-format-mode-reference"></a><span data-ttu-id="e6b46-103">Riferimento alla modalità di formattazione BC7</span><span class="sxs-lookup"><span data-stu-id="e6b46-103">BC7 Format Mode Reference</span></span>

<span data-ttu-id="e6b46-104">Questa documentazione contiene un elenco delle 8 modalità di blocco e delle allocazioni di bit per i blocchi di formato della compressione di trama BC7.</span><span class="sxs-lookup"><span data-stu-id="e6b46-104">This documentation contains a list of the 8 block modes and bit allocations for BC7 texture compression format blocks.</span></span>

<span data-ttu-id="e6b46-105">I colori per ogni subset in un blocco sono rappresentati da due colori dell'endpoint espliciti e da un set di colori interpolati tra di essi.</span><span class="sxs-lookup"><span data-stu-id="e6b46-105">The colors for each subset within a block are represented by two explicit endpoint colors and a set of interpolated colors between them.</span></span> <span data-ttu-id="e6b46-106">A seconda della precisione dell'indice del blocco, ogni subset può avere 4, 8 o 16 colori possibili.</span><span class="sxs-lookup"><span data-stu-id="e6b46-106">Depending on the block's index precision, each subset can have 4, 8 or 16 possible colors.</span></span>

-   [<span data-ttu-id="e6b46-107">Modalità 0</span><span class="sxs-lookup"><span data-stu-id="e6b46-107">Mode 0</span></span>](#mode-0)
-   [<span data-ttu-id="e6b46-108">Modalità 1</span><span class="sxs-lookup"><span data-stu-id="e6b46-108">Mode 1</span></span>](#mode-1)
-   [<span data-ttu-id="e6b46-109">Modalità 2</span><span class="sxs-lookup"><span data-stu-id="e6b46-109">Mode 2</span></span>](#mode-2)
-   [<span data-ttu-id="e6b46-110">Modalità 3</span><span class="sxs-lookup"><span data-stu-id="e6b46-110">Mode 3</span></span>](#mode-3)
-   [<span data-ttu-id="e6b46-111">Modalità 4</span><span class="sxs-lookup"><span data-stu-id="e6b46-111">Mode 4</span></span>](#mode-4)
-   [<span data-ttu-id="e6b46-112">Modalità 5</span><span class="sxs-lookup"><span data-stu-id="e6b46-112">Mode 5</span></span>](#mode-5)
-   [<span data-ttu-id="e6b46-113">Modalità 6</span><span class="sxs-lookup"><span data-stu-id="e6b46-113">Mode 6</span></span>](#mode-6)
-   [<span data-ttu-id="e6b46-114">Modalità 7</span><span class="sxs-lookup"><span data-stu-id="e6b46-114">Mode 7</span></span>](#mode-7)
-   [<span data-ttu-id="e6b46-115">Osservazioni:</span><span class="sxs-lookup"><span data-stu-id="e6b46-115">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="e6b46-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e6b46-116">Related topics</span></span>](#related-topics)

## <a name="mode-0"></a><span data-ttu-id="e6b46-117">Modalità 0</span><span class="sxs-lookup"><span data-stu-id="e6b46-117">Mode 0</span></span>

<span data-ttu-id="e6b46-118">La modalità BC7 0 presenta le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="e6b46-118">BC7 Mode 0 has the following characteristics:</span></span>

-   <span data-ttu-id="e6b46-119">Solo componenti colore (nessun Alpha)</span><span class="sxs-lookup"><span data-stu-id="e6b46-119">Color components only (no alpha)</span></span>
-   <span data-ttu-id="e6b46-120">3 subset per blocco</span><span class="sxs-lookup"><span data-stu-id="e6b46-120">3 subsets per block</span></span>
-   <span data-ttu-id="e6b46-121">RGBP 4.4.4.1 endpoint con un P-bit univoco per endpoint</span><span class="sxs-lookup"><span data-stu-id="e6b46-121">RGBP 4.4.4.1 endpoints with a unique P-bit per endpoint</span></span>
-   <span data-ttu-id="e6b46-122">indici a 3 bit</span><span class="sxs-lookup"><span data-stu-id="e6b46-122">3-bit indices</span></span>
-   <span data-ttu-id="e6b46-123">16 partizioni</span><span class="sxs-lookup"><span data-stu-id="e6b46-123">16 partitions</span></span>

![layout a 0 bit in modalità](images/bc7-mode0.png)

## <a name="mode-1"></a><span data-ttu-id="e6b46-125">Modalità 1</span><span class="sxs-lookup"><span data-stu-id="e6b46-125">Mode 1</span></span>

<span data-ttu-id="e6b46-126">La modalità BC7 1 presenta le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="e6b46-126">BC7 Mode 1 has the following characteristics:</span></span>

-   <span data-ttu-id="e6b46-127">Solo componenti colore (nessun Alpha)</span><span class="sxs-lookup"><span data-stu-id="e6b46-127">Color components only (no alpha)</span></span>
-   <span data-ttu-id="e6b46-128">2 subset per blocco</span><span class="sxs-lookup"><span data-stu-id="e6b46-128">2 subsets per block</span></span>
-   <span data-ttu-id="e6b46-129">RGBP 6.6.6.1 endpoint con un P-bit condiviso per subset)</span><span class="sxs-lookup"><span data-stu-id="e6b46-129">RGBP 6.6.6.1 endpoints with a shared P-bit per subset)</span></span>
-   <span data-ttu-id="e6b46-130">indici a 3 bit</span><span class="sxs-lookup"><span data-stu-id="e6b46-130">3-bit indices</span></span>
-   <span data-ttu-id="e6b46-131">64 partizioni</span><span class="sxs-lookup"><span data-stu-id="e6b46-131">64 partitions</span></span>

![layout in modalità 1 bit](images/bc7-mode1.png)

## <a name="mode-2"></a><span data-ttu-id="e6b46-133">Modalità 2</span><span class="sxs-lookup"><span data-stu-id="e6b46-133">Mode 2</span></span>

<span data-ttu-id="e6b46-134">La modalità BC7 2 presenta le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="e6b46-134">BC7 Mode 2 has the following characteristics:</span></span>

-   <span data-ttu-id="e6b46-135">Solo componenti colore (nessun Alpha)</span><span class="sxs-lookup"><span data-stu-id="e6b46-135">Color components only (no alpha)</span></span>
-   <span data-ttu-id="e6b46-136">3 subset per blocco</span><span class="sxs-lookup"><span data-stu-id="e6b46-136">3 subsets per block</span></span>
-   <span data-ttu-id="e6b46-137">Endpoint 5.5.5 RGB</span><span class="sxs-lookup"><span data-stu-id="e6b46-137">RGB 5.5.5 endpoints</span></span>
-   <span data-ttu-id="e6b46-138">indici a 2 bit</span><span class="sxs-lookup"><span data-stu-id="e6b46-138">2-bit indices</span></span>
-   <span data-ttu-id="e6b46-139">64 partizioni</span><span class="sxs-lookup"><span data-stu-id="e6b46-139">64 partitions</span></span>

![layout in modalità a 2 bit](images/bc7-mode2.png)

## <a name="mode-3"></a><span data-ttu-id="e6b46-141">Modalità 3</span><span class="sxs-lookup"><span data-stu-id="e6b46-141">Mode 3</span></span>

<span data-ttu-id="e6b46-142">La modalità BC7 3 presenta le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="e6b46-142">BC7 Mode 3 has the following characteristics:</span></span>

-   <span data-ttu-id="e6b46-143">Solo componenti colore (nessun Alpha)</span><span class="sxs-lookup"><span data-stu-id="e6b46-143">Color components only (no alpha)</span></span>
-   <span data-ttu-id="e6b46-144">2 subset per blocco</span><span class="sxs-lookup"><span data-stu-id="e6b46-144">2 subsets per block</span></span>
-   <span data-ttu-id="e6b46-145">RGBP 7.7.7.1 endpoint con un P bit univoco per subset)</span><span class="sxs-lookup"><span data-stu-id="e6b46-145">RGBP 7.7.7.1 endpoints with a unique P-bit per subset)</span></span>
-   <span data-ttu-id="e6b46-146">indici a 2 bit</span><span class="sxs-lookup"><span data-stu-id="e6b46-146">2-bit indices</span></span>
-   <span data-ttu-id="e6b46-147">64 partizioni</span><span class="sxs-lookup"><span data-stu-id="e6b46-147">64 partitions</span></span>

![layout in modalità a 3 bit](images/bc7-mode3.png)

## <a name="mode-4"></a><span data-ttu-id="e6b46-149">Modalità 4</span><span class="sxs-lookup"><span data-stu-id="e6b46-149">Mode 4</span></span>

<span data-ttu-id="e6b46-150">La modalità BC7 4 presenta le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="e6b46-150">BC7 Mode 4 has the following characteristics:</span></span>

-   <span data-ttu-id="e6b46-151">Componenti colore con componente alfa separato</span><span class="sxs-lookup"><span data-stu-id="e6b46-151">Color components with separate alpha component</span></span>
-   <span data-ttu-id="e6b46-152">1 subset per blocco</span><span class="sxs-lookup"><span data-stu-id="e6b46-152">1 subset per block</span></span>
-   <span data-ttu-id="e6b46-153">Endpoint colori 5.5.5 RGB</span><span class="sxs-lookup"><span data-stu-id="e6b46-153">RGB 5.5.5 color endpoints</span></span>
-   <span data-ttu-id="e6b46-154">endpoint alfa a 6 bit</span><span class="sxs-lookup"><span data-stu-id="e6b46-154">6-bit alpha endpoints</span></span>
-   <span data-ttu-id="e6b46-155">indici a 2 bit a 16 x</span><span class="sxs-lookup"><span data-stu-id="e6b46-155">16 x 2-bit indices</span></span>
-   <span data-ttu-id="e6b46-156">indici a 3 bit a 16 bit</span><span class="sxs-lookup"><span data-stu-id="e6b46-156">16 x 3-bit indices</span></span>
-   <span data-ttu-id="e6b46-157">rotazione componente a 2 bit</span><span class="sxs-lookup"><span data-stu-id="e6b46-157">2-bit component rotation</span></span>
-   <span data-ttu-id="e6b46-158">selettore di indice a 1 bit (se vengono usati gli indici a 2 o 3 bit)</span><span class="sxs-lookup"><span data-stu-id="e6b46-158">1-bit index selector (whether the 2- or 3-bit indices are used)</span></span>

![layout in modalità a 4 bit](images/bc7-mode4.png)

## <a name="mode-5"></a><span data-ttu-id="e6b46-160">Modalità 5</span><span class="sxs-lookup"><span data-stu-id="e6b46-160">Mode 5</span></span>

<span data-ttu-id="e6b46-161">La modalità BC7 5 presenta le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="e6b46-161">BC7 Mode 5 has the following characteristics:</span></span>

-   <span data-ttu-id="e6b46-162">Componenti colore con componente alfa separato</span><span class="sxs-lookup"><span data-stu-id="e6b46-162">Color components with separate alpha component</span></span>
-   <span data-ttu-id="e6b46-163">1 subset per blocco</span><span class="sxs-lookup"><span data-stu-id="e6b46-163">1 subset per block</span></span>
-   <span data-ttu-id="e6b46-164">Endpoint colori 7.7.7 RGB</span><span class="sxs-lookup"><span data-stu-id="e6b46-164">RGB 7.7.7 color endpoints</span></span>
-   <span data-ttu-id="e6b46-165">endpoint alfa a 8 bit</span><span class="sxs-lookup"><span data-stu-id="e6b46-165">8-bit alpha endpoints</span></span>
-   <span data-ttu-id="e6b46-166">indici di colore a 2 bit a 16 x</span><span class="sxs-lookup"><span data-stu-id="e6b46-166">16 x 2-bit color indices</span></span>
-   <span data-ttu-id="e6b46-167">indici alfa a 2 bit a 16 x</span><span class="sxs-lookup"><span data-stu-id="e6b46-167">16 x 2-bit alpha indices</span></span>
-   <span data-ttu-id="e6b46-168">rotazione componente a 2 bit</span><span class="sxs-lookup"><span data-stu-id="e6b46-168">2-bit component rotation</span></span>

![layout in modalità a 5 bit](images/bc7-mode5.png)

## <a name="mode-6"></a><span data-ttu-id="e6b46-170">Modalità 6</span><span class="sxs-lookup"><span data-stu-id="e6b46-170">Mode 6</span></span>

<span data-ttu-id="e6b46-171">La modalità BC7 6 presenta le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="e6b46-171">BC7 Mode 6 has the following characteristics:</span></span>

-   <span data-ttu-id="e6b46-172">Colori combinati e componenti alfa</span><span class="sxs-lookup"><span data-stu-id="e6b46-172">Combined color and alpha components</span></span>
-   <span data-ttu-id="e6b46-173">Un subset per blocco</span><span class="sxs-lookup"><span data-stu-id="e6b46-173">One subset per block</span></span>
-   <span data-ttu-id="e6b46-174">Endpoint RGBAP 7.7.7.7.1 Color (e Alpha) (Unique P-bit per endpoint)</span><span class="sxs-lookup"><span data-stu-id="e6b46-174">RGBAP 7.7.7.7.1 color (and alpha) endpoints (unique P-bit per endpoint)</span></span>
-   <span data-ttu-id="e6b46-175">indici a 4 bit a 16 bit</span><span class="sxs-lookup"><span data-stu-id="e6b46-175">16 x 4-bit indices</span></span>

![layout in modalità a 6 bit](images/bc7-mode6.png)

## <a name="mode-7"></a><span data-ttu-id="e6b46-177">Modalità 7</span><span class="sxs-lookup"><span data-stu-id="e6b46-177">Mode 7</span></span>

<span data-ttu-id="e6b46-178">La modalità BC7 7 presenta le caratteristiche seguenti:</span><span class="sxs-lookup"><span data-stu-id="e6b46-178">BC7 Mode 7 has the following characteristics:</span></span>

-   <span data-ttu-id="e6b46-179">Colori combinati e componenti alfa</span><span class="sxs-lookup"><span data-stu-id="e6b46-179">Combined color and alpha components</span></span>
-   <span data-ttu-id="e6b46-180">2 subset per blocco</span><span class="sxs-lookup"><span data-stu-id="e6b46-180">2 subsets per block</span></span>
-   <span data-ttu-id="e6b46-181">Endpoint RGBAP 5.5.5.5.1 Color (e Alpha) (Unique P-bit per endpoint)</span><span class="sxs-lookup"><span data-stu-id="e6b46-181">RGBAP 5.5.5.5.1 color (and alpha) endpoints (unique P-bit per endpoint)</span></span>
-   <span data-ttu-id="e6b46-182">indici a 2 bit</span><span class="sxs-lookup"><span data-stu-id="e6b46-182">2-bit indices</span></span>
-   <span data-ttu-id="e6b46-183">64 partizioni</span><span class="sxs-lookup"><span data-stu-id="e6b46-183">64 partitions</span></span>

![layout in modalità a 7 bit](images/bc7-mode7.png)

## <a name="remarks"></a><span data-ttu-id="e6b46-185">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6b46-185">Remarks</span></span>

<span data-ttu-id="e6b46-186">Mode 8 (il byte meno significativo è impostato su 0x00) è riservato.</span><span class="sxs-lookup"><span data-stu-id="e6b46-186">Mode 8 (the least significant byte is set to 0x00) is reserved.</span></span> <span data-ttu-id="e6b46-187">Non usarlo nel codificatore.</span><span class="sxs-lookup"><span data-stu-id="e6b46-187">Don't use it in your encoder.</span></span> <span data-ttu-id="e6b46-188">Se si passa questa modalità all'hardware, viene restituito un blocco inizializzato su tutti zeri.</span><span class="sxs-lookup"><span data-stu-id="e6b46-188">If you pass this mode to the hardware, a block initialized to all zeroes is returned.</span></span>

<span data-ttu-id="e6b46-189">In BC7 è possibile codificare il componente alfa in uno dei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="e6b46-189">In BC7, you can encode the alpha component in one of the following ways:</span></span>

-   <span data-ttu-id="e6b46-190">Tipi di blocco senza codifica esplicita del componente alfa.</span><span class="sxs-lookup"><span data-stu-id="e6b46-190">Block types without explicit alpha component encoding.</span></span> <span data-ttu-id="e6b46-191">In questi blocchi, gli endpoint dei colori hanno una codifica solo RGB, con il componente alfa decodificato a 1,0 per tutti i Texel.</span><span class="sxs-lookup"><span data-stu-id="e6b46-191">In these blocks, the color endpoints have an RGB-only encoding, with the alpha component decoded to 1.0 for all texels.</span></span>
-   <span data-ttu-id="e6b46-192">Tipi di blocco con componenti di colore e alfa combinati.</span><span class="sxs-lookup"><span data-stu-id="e6b46-192">Block types with combined color and alpha components.</span></span> <span data-ttu-id="e6b46-193">In questi blocchi, i valori dei colori dell'endpoint vengono specificati nel formato RGBA e i valori del componente alfa vengono interpolati insieme ai valori dei colori.</span><span class="sxs-lookup"><span data-stu-id="e6b46-193">In these blocks, the endpoint color values are specified in the RGBA format, and the alpha component values are interpolated along with the color values.</span></span>
-   <span data-ttu-id="e6b46-194">Tipi di blocco con componenti di colore e alfa separati.</span><span class="sxs-lookup"><span data-stu-id="e6b46-194">Block types with separated color and alpha components.</span></span> <span data-ttu-id="e6b46-195">In questi blocchi il colore e i valori alfa vengono specificati separatamente, ognuno con un proprio set di indici.</span><span class="sxs-lookup"><span data-stu-id="e6b46-195">In these blocks the color and alpha values are specified separately, each with their own set of indices.</span></span> <span data-ttu-id="e6b46-196">Di conseguenza, hanno un vettore effettivo e un canale scalare codificato separatamente, in cui il vettore specifica in genere i canali di colore \[ R, G, B \] e il valore scalare specifica il canale alfa \[ a \] .</span><span class="sxs-lookup"><span data-stu-id="e6b46-196">As a result, they have an effective vector and a scalar channel separately encoded, where the vector commonly specifies the color channels \[R, G, B\] and the scalar specifies the alpha channel \[A\].</span></span> <span data-ttu-id="e6b46-197">Per supportare questo approccio, nella codifica viene fornito un campo a 2 bit separato, che consente di specificare la codifica del canale separata come valore scalare.</span><span class="sxs-lookup"><span data-stu-id="e6b46-197">To support this approach, a separate 2-bit field is provided in the encoding, which permits the specification of the separate channel encoding as a scalar value.</span></span> <span data-ttu-id="e6b46-198">Di conseguenza, il blocco può avere una delle quattro rappresentazioni seguenti di questa codifica alfa (come indicato dal campo a 2 bit):</span><span class="sxs-lookup"><span data-stu-id="e6b46-198">As a result, the block can have one of the following four different representations of this alpha encoding (as indicated by the 2-bit field):</span></span>
    -   <span data-ttu-id="e6b46-199">RGB \| A: canale alfa separato</span><span class="sxs-lookup"><span data-stu-id="e6b46-199">RGB\|A: alpha channel separate</span></span>
    -   <span data-ttu-id="e6b46-200">AGB \| R: canale colori "rosso" separato</span><span class="sxs-lookup"><span data-stu-id="e6b46-200">AGB\|R: "red" color channel separate</span></span>
    -   <span data-ttu-id="e6b46-201">RAB \| G: canale colori "verde" separato</span><span class="sxs-lookup"><span data-stu-id="e6b46-201">RAB\|G: "green" color channel separate</span></span>
    -   <span data-ttu-id="e6b46-202">RGA \| B: canale colori "blu" separato</span><span class="sxs-lookup"><span data-stu-id="e6b46-202">RGA\|B: "blue" color channel separate</span></span>

    <span data-ttu-id="e6b46-203">Il decodificatore Riordina nuovamente l'ordine del canale in RGBA dopo la decodifica, quindi il formato del blocco interno è invisibile per lo sviluppatore.</span><span class="sxs-lookup"><span data-stu-id="e6b46-203">The decoder reorders the channel order back to RGBA after decoding, so the internal block format is invisible to the developer.</span></span> <span data-ttu-id="e6b46-204">I neri con componenti colore e alfa distinti hanno anche due set di dati di indice: uno per il set di canali vettoriale e uno per il canale scalare.</span><span class="sxs-lookup"><span data-stu-id="e6b46-204">Blacks with separate color and alpha components also have two sets of index data: one for the vectored set of channels, and one for the scalar channel.</span></span> <span data-ttu-id="e6b46-205">(Nel caso della modalità 4, questi indici hanno larghezze diverse \[ 2 o 3 bit \] .</span><span class="sxs-lookup"><span data-stu-id="e6b46-205">(In the case of Mode 4, these indices are of differing widths \[2 or 3 bits\].</span></span> <span data-ttu-id="e6b46-206">La modalità 4 contiene inoltre un selettore a 1 bit che specifica se il vettore o il canale scalare utilizza gli indici a 3 bit.</span><span class="sxs-lookup"><span data-stu-id="e6b46-206">Mode 4 also contains a 1-bit selector that specifies whether the vector or the scalar channel uses the 3-bit indices.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6b46-207">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e6b46-207">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6b46-208">Formato BC7</span><span class="sxs-lookup"><span data-stu-id="e6b46-208">BC7 Format</span></span>](bc7-format.md)
</dt> </dl>

 

 




