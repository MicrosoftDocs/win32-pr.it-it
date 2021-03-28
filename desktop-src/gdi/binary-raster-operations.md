---
description: Questa sezione elenca i codici di operazione raster binari usati dalle funzioni GetROP2 e SetROP2. I codici di operazione raster definiscono il modo in cui GDI combina i bit della penna selezionata con i bit nella bitmap di destinazione.
ms.assetid: 9a3a5b5d-b41f-4859-8830-98272983a635
title: Operazioni raster binarie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8a70030b1940c31d036505a80a6b1868aececd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130855"
---
# <a name="binary-raster-operations"></a><span data-ttu-id="337eb-104">Operazioni raster binarie</span><span class="sxs-lookup"><span data-stu-id="337eb-104">Binary Raster Operations</span></span>

<span data-ttu-id="337eb-105">Questa sezione elenca i codici di operazione raster binari usati dalle funzioni [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) e [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) .</span><span class="sxs-lookup"><span data-stu-id="337eb-105">This section lists the binary raster-operation codes used by the [**GetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-getrop2) and [**SetROP2**](/windows/desktop/api/Wingdi/nf-wingdi-setrop2) functions.</span></span> <span data-ttu-id="337eb-106">I codici di operazione raster definiscono il modo in cui GDI combina i bit della penna selezionata con i bit nella bitmap di destinazione.</span><span class="sxs-lookup"><span data-stu-id="337eb-106">Raster-operation codes define how GDI combines the bits from the selected pen with the bits in the destination bitmap.</span></span>

<span data-ttu-id="337eb-107">Ogni codice di operazione raster rappresenta un'operazione booleana in cui vengono combinati i valori dei pixel presenti nella penna selezionata e nella bitmap di destinazione.</span><span class="sxs-lookup"><span data-stu-id="337eb-107">Each raster-operation code represents a Boolean operation in which the values of the pixels in the selected pen and the destination bitmap are combined.</span></span> <span data-ttu-id="337eb-108">Di seguito sono riportati i due operandi utilizzati in queste operazioni.</span><span class="sxs-lookup"><span data-stu-id="337eb-108">The following are the two operands used in these operations.</span></span>



| <span data-ttu-id="337eb-109">Operando</span><span class="sxs-lookup"><span data-stu-id="337eb-109">Operand</span></span> | <span data-ttu-id="337eb-110">Significato</span><span class="sxs-lookup"><span data-stu-id="337eb-110">Meaning</span></span>            |
|---------|--------------------|
| <span data-ttu-id="337eb-111">P</span><span class="sxs-lookup"><span data-stu-id="337eb-111">P</span></span>       | <span data-ttu-id="337eb-112">Penna selezionata</span><span class="sxs-lookup"><span data-stu-id="337eb-112">Selected pen</span></span>       |
| <span data-ttu-id="337eb-113">D</span><span class="sxs-lookup"><span data-stu-id="337eb-113">D</span></span>       | <span data-ttu-id="337eb-114">Bitmap di destinazione</span><span class="sxs-lookup"><span data-stu-id="337eb-114">Destination bitmap</span></span> |



 

<span data-ttu-id="337eb-115">Gli operatori booleani utilizzati in queste operazioni seguono.</span><span class="sxs-lookup"><span data-stu-id="337eb-115">The Boolean operators used in these operations follow.</span></span>



| <span data-ttu-id="337eb-116">Operatore</span><span class="sxs-lookup"><span data-stu-id="337eb-116">Operator</span></span> | <span data-ttu-id="337eb-117">Significato</span><span class="sxs-lookup"><span data-stu-id="337eb-117">Meaning</span></span>                    |
|----------|----------------------------|
| <span data-ttu-id="337eb-118">a</span><span class="sxs-lookup"><span data-stu-id="337eb-118">a</span></span>        | <span data-ttu-id="337eb-119">AND bit per bit</span><span class="sxs-lookup"><span data-stu-id="337eb-119">Bitwise AND</span></span>                |
| <span data-ttu-id="337eb-120">n</span><span class="sxs-lookup"><span data-stu-id="337eb-120">n</span></span>        | <span data-ttu-id="337eb-121">NOT bit per bit (inverso)</span><span class="sxs-lookup"><span data-stu-id="337eb-121">Bitwise NOT (inverse)</span></span>      |
| <span data-ttu-id="337eb-122">o</span><span class="sxs-lookup"><span data-stu-id="337eb-122">o</span></span>        | <span data-ttu-id="337eb-123">OR bit per bit</span><span class="sxs-lookup"><span data-stu-id="337eb-123">Bitwise OR</span></span>                 |
| <span data-ttu-id="337eb-124">x</span><span class="sxs-lookup"><span data-stu-id="337eb-124">x</span></span>        | <span data-ttu-id="337eb-125">OR esclusivo bit per bit (XOR)</span><span class="sxs-lookup"><span data-stu-id="337eb-125">Bitwise exclusive OR (XOR)</span></span> |



 

<span data-ttu-id="337eb-126">Tutte le operazioni booleane vengono presentate in notazione polacca inversa.</span><span class="sxs-lookup"><span data-stu-id="337eb-126">All Boolean operations are presented in reverse Polish notation.</span></span> <span data-ttu-id="337eb-127">Ad esempio, l'operazione seguente sostituisce i valori dei pixel nella bitmap di destinazione con una combinazione dei valori dei pixel della penna e del pennello selezionato:</span><span class="sxs-lookup"><span data-stu-id="337eb-127">For example, the following operation replaces the values of the pixels in the destination bitmap with a combination of the pixel values of the pen and the selected brush:</span></span>


```C++
DPo 
```



<span data-ttu-id="337eb-128">Ogni codice di operazione raster è un intero a 32 bit la cui parola più ordinata è un indice di operazione booleana e la cui parola di basso livello è il codice dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="337eb-128">Each raster-operation code is a 32-bit integer whose high-order word is a Boolean operation index and whose low-order word is the operation code.</span></span> <span data-ttu-id="337eb-129">L'indice dell'operazione a 16 bit è un valore a 8 bit esteso a zero che rappresenta tutti i possibili risultati risultante dall'operazione booleana su due parametri, in questo caso i valori di penna e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="337eb-129">The 16-bit operation index is a zero-extended 8-bit value that represents all possible outcomes resulting from the Boolean operation on two parameters (in this case, the pen and destination values).</span></span> <span data-ttu-id="337eb-130">Ad esempio, gli indici dell'operazione per le operazioni DPo e DPan sono illustrati nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="337eb-130">For example, the operation indexes for the DPo and DPan operations are shown in the following list.</span></span>



| <span data-ttu-id="337eb-131">P</span><span class="sxs-lookup"><span data-stu-id="337eb-131">P</span></span>   | <span data-ttu-id="337eb-132">D</span><span class="sxs-lookup"><span data-stu-id="337eb-132">D</span></span>   | <span data-ttu-id="337eb-133">DPo</span><span class="sxs-lookup"><span data-stu-id="337eb-133">DPo</span></span> | <span data-ttu-id="337eb-134">Dpan</span><span class="sxs-lookup"><span data-stu-id="337eb-134">Dpan</span></span> |
|-----|-----|-----|------|
| <span data-ttu-id="337eb-135">0</span><span class="sxs-lookup"><span data-stu-id="337eb-135">0</span></span>   | <span data-ttu-id="337eb-136">0</span><span class="sxs-lookup"><span data-stu-id="337eb-136">0</span></span>   | <span data-ttu-id="337eb-137">0</span><span class="sxs-lookup"><span data-stu-id="337eb-137">0</span></span>   | <span data-ttu-id="337eb-138">1</span><span class="sxs-lookup"><span data-stu-id="337eb-138">1</span></span>    |
| <span data-ttu-id="337eb-139">0</span><span class="sxs-lookup"><span data-stu-id="337eb-139">0</span></span>   | <span data-ttu-id="337eb-140">1</span><span class="sxs-lookup"><span data-stu-id="337eb-140">1</span></span>   | <span data-ttu-id="337eb-141">1</span><span class="sxs-lookup"><span data-stu-id="337eb-141">1</span></span>   | <span data-ttu-id="337eb-142">1</span><span class="sxs-lookup"><span data-stu-id="337eb-142">1</span></span>    |
| <span data-ttu-id="337eb-143">1</span><span class="sxs-lookup"><span data-stu-id="337eb-143">1</span></span>   | <span data-ttu-id="337eb-144">0</span><span class="sxs-lookup"><span data-stu-id="337eb-144">0</span></span>   | <span data-ttu-id="337eb-145">1</span><span class="sxs-lookup"><span data-stu-id="337eb-145">1</span></span>   | <span data-ttu-id="337eb-146">1</span><span class="sxs-lookup"><span data-stu-id="337eb-146">1</span></span>    |
| <span data-ttu-id="337eb-147">1</span><span class="sxs-lookup"><span data-stu-id="337eb-147">1</span></span>   | <span data-ttu-id="337eb-148">1</span><span class="sxs-lookup"><span data-stu-id="337eb-148">1</span></span>   | <span data-ttu-id="337eb-149">1</span><span class="sxs-lookup"><span data-stu-id="337eb-149">1</span></span>   | <span data-ttu-id="337eb-150">0</span><span class="sxs-lookup"><span data-stu-id="337eb-150">0</span></span>    |



 

<span data-ttu-id="337eb-151">Nell'elenco seguente vengono descritte le modalità di disegno e le operazioni booleane che rappresentano.</span><span class="sxs-lookup"><span data-stu-id="337eb-151">The following list outlines the drawing modes and the Boolean operations that they represent.</span></span>



| <span data-ttu-id="337eb-152">Operazione raster</span><span class="sxs-lookup"><span data-stu-id="337eb-152">Raster operation</span></span> | <span data-ttu-id="337eb-153">Operazione booleana</span><span class="sxs-lookup"><span data-stu-id="337eb-153">Boolean operation</span></span> |
|------------------|-------------------|
| <span data-ttu-id="337eb-154">R2 \_ nero</span><span class="sxs-lookup"><span data-stu-id="337eb-154">R2\_BLACK</span></span>        | <span data-ttu-id="337eb-155">0</span><span class="sxs-lookup"><span data-stu-id="337eb-155">0</span></span>                 |
| <span data-ttu-id="337eb-156">\_COPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-156">R2\_COPYPEN</span></span>      | <span data-ttu-id="337eb-157">P</span><span class="sxs-lookup"><span data-stu-id="337eb-157">P</span></span>                 |
| <span data-ttu-id="337eb-158">\_MASKNOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-158">R2\_MASKNOTPEN</span></span>   | <span data-ttu-id="337eb-159">DPna</span><span class="sxs-lookup"><span data-stu-id="337eb-159">DPna</span></span>              |
| <span data-ttu-id="337eb-160">\_MASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-160">R2\_MASKPEN</span></span>      | <span data-ttu-id="337eb-161">DPa</span><span class="sxs-lookup"><span data-stu-id="337eb-161">DPa</span></span>               |
| <span data-ttu-id="337eb-162">\_MASKPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="337eb-162">R2\_MASKPENNOT</span></span>   | <span data-ttu-id="337eb-163">PDna</span><span class="sxs-lookup"><span data-stu-id="337eb-163">PDna</span></span>              |
| <span data-ttu-id="337eb-164">\_MERGENOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-164">R2\_MERGENOTPEN</span></span>  | <span data-ttu-id="337eb-165">DPno</span><span class="sxs-lookup"><span data-stu-id="337eb-165">DPno</span></span>              |
| <span data-ttu-id="337eb-166">\_MERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-166">R2\_MERGEPEN</span></span>     | <span data-ttu-id="337eb-167">DPo</span><span class="sxs-lookup"><span data-stu-id="337eb-167">DPo</span></span>               |
| <span data-ttu-id="337eb-168">\_MERGEPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="337eb-168">R2\_MERGEPENNOT</span></span>  | <span data-ttu-id="337eb-169">PDno</span><span class="sxs-lookup"><span data-stu-id="337eb-169">PDno</span></span>              |
| <span data-ttu-id="337eb-170">\_NOP R2</span><span class="sxs-lookup"><span data-stu-id="337eb-170">R2\_NOP</span></span>          | <span data-ttu-id="337eb-171">D</span><span class="sxs-lookup"><span data-stu-id="337eb-171">D</span></span>                 |
| <span data-ttu-id="337eb-172">R2 \_ non</span><span class="sxs-lookup"><span data-stu-id="337eb-172">R2\_NOT</span></span>          | <span data-ttu-id="337eb-173">Dn</span><span class="sxs-lookup"><span data-stu-id="337eb-173">Dn</span></span>                |
| <span data-ttu-id="337eb-174">\_NOTCOPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-174">R2\_NOTCOPYPEN</span></span>   | <span data-ttu-id="337eb-175">PN</span><span class="sxs-lookup"><span data-stu-id="337eb-175">Pn</span></span>                |
| <span data-ttu-id="337eb-176">\_NOTMASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-176">R2\_NOTMASKPEN</span></span>   | <span data-ttu-id="337eb-177">DPan</span><span class="sxs-lookup"><span data-stu-id="337eb-177">DPan</span></span>              |
| <span data-ttu-id="337eb-178">\_NOTMERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-178">R2\_NOTMERGEPEN</span></span>  | <span data-ttu-id="337eb-179">DPon</span><span class="sxs-lookup"><span data-stu-id="337eb-179">DPon</span></span>              |
| <span data-ttu-id="337eb-180">\_NOTXORPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-180">R2\_NOTXORPEN</span></span>    | <span data-ttu-id="337eb-181">DPxn</span><span class="sxs-lookup"><span data-stu-id="337eb-181">DPxn</span></span>              |
| <span data-ttu-id="337eb-182">\_Bianco R2</span><span class="sxs-lookup"><span data-stu-id="337eb-182">R2\_WHITE</span></span>        | <span data-ttu-id="337eb-183">1</span><span class="sxs-lookup"><span data-stu-id="337eb-183">1</span></span>                 |
| <span data-ttu-id="337eb-184">\_XORPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-184">R2\_XORPEN</span></span>       | <span data-ttu-id="337eb-185">DPx</span><span class="sxs-lookup"><span data-stu-id="337eb-185">DPx</span></span>               |



 

<span data-ttu-id="337eb-186">Per un dispositivo monocromatico, GDI esegue il mapping tra il valore zero e il nero e il valore da 1 a bianco.</span><span class="sxs-lookup"><span data-stu-id="337eb-186">For a monochrome device, GDI maps the value zero to black and the value 1 to white.</span></span> <span data-ttu-id="337eb-187">Se un'applicazione tenta di creare con una penna nera in una destinazione bianca usando le operazioni raster binarie disponibili, si verificano i risultati seguenti.</span><span class="sxs-lookup"><span data-stu-id="337eb-187">If an application attempts to draw with a black pen on a white destination by using the available binary raster operations, the following results occur.</span></span>



| <span data-ttu-id="337eb-188">Operazione raster</span><span class="sxs-lookup"><span data-stu-id="337eb-188">Raster operation</span></span> | <span data-ttu-id="337eb-189">Risultato</span><span class="sxs-lookup"><span data-stu-id="337eb-189">Result</span></span>             |
|------------------|--------------------|
| <span data-ttu-id="337eb-190">R2 \_ nero</span><span class="sxs-lookup"><span data-stu-id="337eb-190">R2\_BLACK</span></span>        | <span data-ttu-id="337eb-191">Linea nera visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-191">Visible black line</span></span> |
| <span data-ttu-id="337eb-192">\_COPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-192">R2\_COPYPEN</span></span>      | <span data-ttu-id="337eb-193">Linea nera visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-193">Visible black line</span></span> |
| <span data-ttu-id="337eb-194">\_MASKNOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-194">R2\_MASKNOTPEN</span></span>   | <span data-ttu-id="337eb-195">Nessuna riga visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-195">No visible line</span></span>    |
| <span data-ttu-id="337eb-196">\_MASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-196">R2\_MASKPEN</span></span>      | <span data-ttu-id="337eb-197">Linea nera visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-197">Visible black line</span></span> |
| <span data-ttu-id="337eb-198">\_MASKPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="337eb-198">R2\_MASKPENNOT</span></span>   | <span data-ttu-id="337eb-199">Linea nera visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-199">Visible black line</span></span> |
| <span data-ttu-id="337eb-200">\_MERGENOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-200">R2\_MERGENOTPEN</span></span>  | <span data-ttu-id="337eb-201">Nessuna riga visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-201">No visible line</span></span>    |
| <span data-ttu-id="337eb-202">\_MERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-202">R2\_MERGEPEN</span></span>     | <span data-ttu-id="337eb-203">Linea nera visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-203">Visible black line</span></span> |
| <span data-ttu-id="337eb-204">\_MERGEPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="337eb-204">R2\_MERGEPENNOT</span></span>  | <span data-ttu-id="337eb-205">Linea nera visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-205">Visible black line</span></span> |
| <span data-ttu-id="337eb-206">\_NOP R2</span><span class="sxs-lookup"><span data-stu-id="337eb-206">R2\_NOP</span></span>          | <span data-ttu-id="337eb-207">Nessuna riga visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-207">No visible line</span></span>    |
| <span data-ttu-id="337eb-208">R2 \_ non</span><span class="sxs-lookup"><span data-stu-id="337eb-208">R2\_NOT</span></span>          | <span data-ttu-id="337eb-209">Linea nera visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-209">Visible black line</span></span> |
| <span data-ttu-id="337eb-210">\_NOTCOPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-210">R2\_NOTCOPYPEN</span></span>   | <span data-ttu-id="337eb-211">Nessuna riga visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-211">No visible line</span></span>    |
| <span data-ttu-id="337eb-212">\_NOTMASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-212">R2\_NOTMASKPEN</span></span>   | <span data-ttu-id="337eb-213">Nessuna riga visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-213">No visible line</span></span>    |
| <span data-ttu-id="337eb-214">\_NOTMERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-214">R2\_NOTMERGEPEN</span></span>  | <span data-ttu-id="337eb-215">Linea nera visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-215">Visible black line</span></span> |
| <span data-ttu-id="337eb-216">\_NOTXORPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-216">R2\_NOTXORPEN</span></span>    | <span data-ttu-id="337eb-217">Linea nera visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-217">Visible black line</span></span> |
| <span data-ttu-id="337eb-218">\_Bianco R2</span><span class="sxs-lookup"><span data-stu-id="337eb-218">R2\_WHITE</span></span>        | <span data-ttu-id="337eb-219">Nessuna riga visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-219">No visible line</span></span>    |
| <span data-ttu-id="337eb-220">\_XORPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-220">R2\_XORPEN</span></span>       | <span data-ttu-id="337eb-221">Nessuna riga visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-221">No visible line</span></span>    |



 

<span data-ttu-id="337eb-222">Per un dispositivo a colori, GDI USA valori RGB per rappresentare i colori della penna e della destinazione.</span><span class="sxs-lookup"><span data-stu-id="337eb-222">For a color device, GDI uses RGB values to represent the colors of the pen and the destination.</span></span> <span data-ttu-id="337eb-223">Un valore di colore RGB è un valore long integer che contiene un campo di colore rosso, verde e blu, ognuno dei quali specifica l'intensità del colore specificato.</span><span class="sxs-lookup"><span data-stu-id="337eb-223">An RGB color value is a long integer that contains a red, a green, and a blue color field, each specifying the intensity of the specified color.</span></span> <span data-ttu-id="337eb-224">Le intensità sono comprese tra 0 e 255.</span><span class="sxs-lookup"><span data-stu-id="337eb-224">Intensities range from 0 through 255.</span></span> <span data-ttu-id="337eb-225">I valori vengono compressi nei tre byte di ordine inferiore del valore long integer.</span><span class="sxs-lookup"><span data-stu-id="337eb-225">The values are packed in the three low-order bytes of the long integer.</span></span> <span data-ttu-id="337eb-226">Il colore di una penna è sempre un colore a tinta unita, ma il colore della destinazione può essere costituito da una combinazione di due o tre colori.</span><span class="sxs-lookup"><span data-stu-id="337eb-226">The color of a pen is always a solid color, but the color of the destination may be a mixture of any two or three colors.</span></span> <span data-ttu-id="337eb-227">Se un'applicazione tenta di creare con una penna bianca in una destinazione blu usando le operazioni raster binarie disponibili, si verificano i risultati seguenti.</span><span class="sxs-lookup"><span data-stu-id="337eb-227">If an application attempts to draw with a white pen on a blue destination by using the available binary raster operations, the following results occur.</span></span>



| <span data-ttu-id="337eb-228">Operazione raster</span><span class="sxs-lookup"><span data-stu-id="337eb-228">Raster operation</span></span> | <span data-ttu-id="337eb-229">Risultato</span><span class="sxs-lookup"><span data-stu-id="337eb-229">Result</span></span>                 |
|------------------|------------------------|
| <span data-ttu-id="337eb-230">R2 \_ nero</span><span class="sxs-lookup"><span data-stu-id="337eb-230">R2\_BLACK</span></span>        | <span data-ttu-id="337eb-231">Linea nera visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-231">Visible black line</span></span>     |
| <span data-ttu-id="337eb-232">\_COPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-232">R2\_COPYPEN</span></span>      | <span data-ttu-id="337eb-233">Riga bianca visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-233">Visible white line</span></span>     |
| <span data-ttu-id="337eb-234">\_MASKNOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-234">R2\_MASKNOTPEN</span></span>   | <span data-ttu-id="337eb-235">Linea nera visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-235">Visible black line</span></span>     |
| <span data-ttu-id="337eb-236">\_MASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-236">R2\_MASKPEN</span></span>      | <span data-ttu-id="337eb-237">Linea blu invisibile</span><span class="sxs-lookup"><span data-stu-id="337eb-237">Invisible blue line</span></span>    |
| <span data-ttu-id="337eb-238">\_MASKPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="337eb-238">R2\_MASKPENNOT</span></span>   | <span data-ttu-id="337eb-239">Linea rossa/verde visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-239">Visible red/green line</span></span> |
| <span data-ttu-id="337eb-240">\_MERGENOTPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-240">R2\_MERGENOTPEN</span></span>  | <span data-ttu-id="337eb-241">Linea blu invisibile</span><span class="sxs-lookup"><span data-stu-id="337eb-241">Invisible blue line</span></span>    |
| <span data-ttu-id="337eb-242">\_MERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-242">R2\_MERGEPEN</span></span>     | <span data-ttu-id="337eb-243">Riga bianca visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-243">Visible white line</span></span>     |
| <span data-ttu-id="337eb-244">\_MERGEPENNOT R2</span><span class="sxs-lookup"><span data-stu-id="337eb-244">R2\_MERGEPENNOT</span></span>  | <span data-ttu-id="337eb-245">Riga bianca visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-245">Visible white line</span></span>     |
| <span data-ttu-id="337eb-246">\_NOP R2</span><span class="sxs-lookup"><span data-stu-id="337eb-246">R2\_NOP</span></span>          | <span data-ttu-id="337eb-247">Linea blu invisibile</span><span class="sxs-lookup"><span data-stu-id="337eb-247">Invisible blue line</span></span>    |
| <span data-ttu-id="337eb-248">R2 \_ non</span><span class="sxs-lookup"><span data-stu-id="337eb-248">R2\_NOT</span></span>          | <span data-ttu-id="337eb-249">Linea rossa/verde visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-249">Visible red/green line</span></span> |
| <span data-ttu-id="337eb-250">\_NOTCOPYPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-250">R2\_NOTCOPYPEN</span></span>   | <span data-ttu-id="337eb-251">Linea nera visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-251">Visible black line</span></span>     |
| <span data-ttu-id="337eb-252">\_NOTMASKPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-252">R2\_NOTMASKPEN</span></span>   | <span data-ttu-id="337eb-253">Linea rossa/verde visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-253">Visible red/green line</span></span> |
| <span data-ttu-id="337eb-254">\_NOTMERGEPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-254">R2\_NOTMERGEPEN</span></span>  | <span data-ttu-id="337eb-255">Linea nera visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-255">Visible black line</span></span>     |
| <span data-ttu-id="337eb-256">\_NOTXORPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-256">R2\_NOTXORPEN</span></span>    | <span data-ttu-id="337eb-257">Linea blu invisibile</span><span class="sxs-lookup"><span data-stu-id="337eb-257">Invisible blue line</span></span>    |
| <span data-ttu-id="337eb-258">\_Bianco R2</span><span class="sxs-lookup"><span data-stu-id="337eb-258">R2\_WHITE</span></span>        | <span data-ttu-id="337eb-259">Riga bianca visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-259">Visible white line</span></span>     |
| <span data-ttu-id="337eb-260">\_XORPEN R2</span><span class="sxs-lookup"><span data-stu-id="337eb-260">R2\_XORPEN</span></span>       | <span data-ttu-id="337eb-261">Linea rossa/verde visibile</span><span class="sxs-lookup"><span data-stu-id="337eb-261">Visible red/green line</span></span> |



 

 

 



