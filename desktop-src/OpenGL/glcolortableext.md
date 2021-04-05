---
title: funzione glColorTableEXT (GL. h)
description: La funzione glColorTableEXT specifica il formato e le dimensioni di una tavolozza per le trame con tavolozza di destinazione.
ms.assetid: f3d7b1a1-97a5-47ef-a0ca-5e58acb86bb4
keywords:
- funzione glColorTableEXT OpenGL
topic_type:
- apiref
api_name:
- glColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0d5fd5c848e787f480e3e1893b9b25e4bbd3de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742210"
---
# <a name="glcolortableext-function"></a><span data-ttu-id="5f6c4-104">glColorTableEXT (funzione)</span><span class="sxs-lookup"><span data-stu-id="5f6c4-104">glColorTableEXT function</span></span>

<span data-ttu-id="5f6c4-105">La funzione **glColorTableEXT** specifica il formato e le dimensioni di una tavolozza per le trame con tavolozza di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-105">The **glColorTableEXT** function specifies the format and size of a palette for targeted paletted textures.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f6c4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f6c4-106">Syntax</span></span>


```C++
void WINAPI glColorTableEXT(
         GLenum  target,
         GLenum  internalFormat,
         GLsizei width,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a><span data-ttu-id="5f6c4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f6c4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f6c4-108">*target*</span><span class="sxs-lookup"><span data-stu-id="5f6c4-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="5f6c4-109">Trama di destinazione per la quale è stata modificata la tavolozza.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-109">The target texture that is to have its palette changed.</span></span> <span data-ttu-id="5f6c4-110">Deve essere una trama \_ 1D, una trama \_ 2D, una \_ trama proxy \_ 1D o una trama del proxy \_ \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-110">Must be TEXTURE\_1D, TEXTURE\_2D, PROXY\_TEXTURE\_1D, or PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="5f6c4-111">*internalFormat*</span><span class="sxs-lookup"><span data-stu-id="5f6c4-111">*internalFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="5f6c4-112">Il formato interno e la risoluzione della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-112">The internal format and resolution of the palette.</span></span> <span data-ttu-id="5f6c4-113">Questo parametro può assumere uno dei seguenti valori simbolici.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-113">This parameter can assume one of the following symbolic values.</span></span>



| <span data-ttu-id="5f6c4-114">Costante</span><span class="sxs-lookup"><span data-stu-id="5f6c4-114">Constant</span></span>       | <span data-ttu-id="5f6c4-115">Formato di base</span><span class="sxs-lookup"><span data-stu-id="5f6c4-115">Base Format</span></span> | <span data-ttu-id="5f6c4-116">Bit R</span><span class="sxs-lookup"><span data-stu-id="5f6c4-116">R Bits</span></span> | <span data-ttu-id="5f6c4-117">Bit G</span><span class="sxs-lookup"><span data-stu-id="5f6c4-117">G Bits</span></span> | <span data-ttu-id="5f6c4-118">Bit B</span><span class="sxs-lookup"><span data-stu-id="5f6c4-118">B Bits</span></span> | <span data-ttu-id="5f6c4-119">Bit</span><span class="sxs-lookup"><span data-stu-id="5f6c4-119">A Bits</span></span> |
|----------------|-------------|--------|--------|--------|--------|
| <span data-ttu-id="5f6c4-120">GL \_ R3 \_ G3 \_ B2</span><span class="sxs-lookup"><span data-stu-id="5f6c4-120">GL\_R3\_G3\_B2</span></span> | <span data-ttu-id="5f6c4-121">GL \_ RGB</span><span class="sxs-lookup"><span data-stu-id="5f6c4-121">GL\_RGB</span></span>     | <span data-ttu-id="5f6c4-122">3</span><span class="sxs-lookup"><span data-stu-id="5f6c4-122">3</span></span>      | <span data-ttu-id="5f6c4-123">3</span><span class="sxs-lookup"><span data-stu-id="5f6c4-123">3</span></span>      | <span data-ttu-id="5f6c4-124">2</span><span class="sxs-lookup"><span data-stu-id="5f6c4-124">2</span></span>      |        |
| <span data-ttu-id="5f6c4-125">\_RGB4 GL</span><span class="sxs-lookup"><span data-stu-id="5f6c4-125">GL\_RGB4</span></span>       | <span data-ttu-id="5f6c4-126">GL \_ RGB</span><span class="sxs-lookup"><span data-stu-id="5f6c4-126">GL\_RGB</span></span>     | <span data-ttu-id="5f6c4-127">4</span><span class="sxs-lookup"><span data-stu-id="5f6c4-127">4</span></span>      | <span data-ttu-id="5f6c4-128">4</span><span class="sxs-lookup"><span data-stu-id="5f6c4-128">4</span></span>      | <span data-ttu-id="5f6c4-129">4</span><span class="sxs-lookup"><span data-stu-id="5f6c4-129">4</span></span>      |        |
| <span data-ttu-id="5f6c4-130">\_RGB5 GL</span><span class="sxs-lookup"><span data-stu-id="5f6c4-130">GL\_RGB5</span></span>       | <span data-ttu-id="5f6c4-131">GL \_ RGB</span><span class="sxs-lookup"><span data-stu-id="5f6c4-131">GL\_RGB</span></span>     | <span data-ttu-id="5f6c4-132">5</span><span class="sxs-lookup"><span data-stu-id="5f6c4-132">5</span></span>      | <span data-ttu-id="5f6c4-133">5</span><span class="sxs-lookup"><span data-stu-id="5f6c4-133">5</span></span>      | <span data-ttu-id="5f6c4-134">5</span><span class="sxs-lookup"><span data-stu-id="5f6c4-134">5</span></span>      |        |
| <span data-ttu-id="5f6c4-135">\_RGB8 GL</span><span class="sxs-lookup"><span data-stu-id="5f6c4-135">GL\_RGB8</span></span>       | <span data-ttu-id="5f6c4-136">GL \_ RGB</span><span class="sxs-lookup"><span data-stu-id="5f6c4-136">GL\_RGB</span></span>     | <span data-ttu-id="5f6c4-137">8</span><span class="sxs-lookup"><span data-stu-id="5f6c4-137">8</span></span>      | <span data-ttu-id="5f6c4-138">8</span><span class="sxs-lookup"><span data-stu-id="5f6c4-138">8</span></span>      | <span data-ttu-id="5f6c4-139">8</span><span class="sxs-lookup"><span data-stu-id="5f6c4-139">8</span></span>      |        |
| <span data-ttu-id="5f6c4-140">\_RGB10 GL</span><span class="sxs-lookup"><span data-stu-id="5f6c4-140">GL\_RGB10</span></span>      | <span data-ttu-id="5f6c4-141">GL \_ RGB</span><span class="sxs-lookup"><span data-stu-id="5f6c4-141">GL\_RGB</span></span>     | <span data-ttu-id="5f6c4-142">10</span><span class="sxs-lookup"><span data-stu-id="5f6c4-142">10</span></span>     | <span data-ttu-id="5f6c4-143">10</span><span class="sxs-lookup"><span data-stu-id="5f6c4-143">10</span></span>     | <span data-ttu-id="5f6c4-144">10</span><span class="sxs-lookup"><span data-stu-id="5f6c4-144">10</span></span>     |        |
| <span data-ttu-id="5f6c4-145">\_RGB12 GL</span><span class="sxs-lookup"><span data-stu-id="5f6c4-145">GL\_RGB12</span></span>      | <span data-ttu-id="5f6c4-146">GL \_ RGB</span><span class="sxs-lookup"><span data-stu-id="5f6c4-146">GL\_RGB</span></span>     | <span data-ttu-id="5f6c4-147">12</span><span class="sxs-lookup"><span data-stu-id="5f6c4-147">12</span></span>     | <span data-ttu-id="5f6c4-148">12</span><span class="sxs-lookup"><span data-stu-id="5f6c4-148">12</span></span>     | <span data-ttu-id="5f6c4-149">12</span><span class="sxs-lookup"><span data-stu-id="5f6c4-149">12</span></span>     |        |
| <span data-ttu-id="5f6c4-150">\_Rgb16 GL</span><span class="sxs-lookup"><span data-stu-id="5f6c4-150">GL\_RGB16</span></span>      | <span data-ttu-id="5f6c4-151">GL \_ RGB</span><span class="sxs-lookup"><span data-stu-id="5f6c4-151">GL\_RGB</span></span>     | <span data-ttu-id="5f6c4-152">16</span><span class="sxs-lookup"><span data-stu-id="5f6c4-152">16</span></span>     | <span data-ttu-id="5f6c4-153">16</span><span class="sxs-lookup"><span data-stu-id="5f6c4-153">16</span></span>     | <span data-ttu-id="5f6c4-154">16</span><span class="sxs-lookup"><span data-stu-id="5f6c4-154">16</span></span>     |        |
| <span data-ttu-id="5f6c4-155">\_RGBA2 GL</span><span class="sxs-lookup"><span data-stu-id="5f6c4-155">GL\_RGBA2</span></span>      | <span data-ttu-id="5f6c4-156">\_RGBA GL</span><span class="sxs-lookup"><span data-stu-id="5f6c4-156">GL\_RGBA</span></span>    | <span data-ttu-id="5f6c4-157">2</span><span class="sxs-lookup"><span data-stu-id="5f6c4-157">2</span></span>      | <span data-ttu-id="5f6c4-158">2</span><span class="sxs-lookup"><span data-stu-id="5f6c4-158">2</span></span>      | <span data-ttu-id="5f6c4-159">2</span><span class="sxs-lookup"><span data-stu-id="5f6c4-159">2</span></span>      | <span data-ttu-id="5f6c4-160">2</span><span class="sxs-lookup"><span data-stu-id="5f6c4-160">2</span></span>      |
| <span data-ttu-id="5f6c4-161">\_RGBA4 GL</span><span class="sxs-lookup"><span data-stu-id="5f6c4-161">GL\_RGBA4</span></span>      | <span data-ttu-id="5f6c4-162">\_RGBA GL</span><span class="sxs-lookup"><span data-stu-id="5f6c4-162">GL\_RGBA</span></span>    | <span data-ttu-id="5f6c4-163">4</span><span class="sxs-lookup"><span data-stu-id="5f6c4-163">4</span></span>      | <span data-ttu-id="5f6c4-164">4</span><span class="sxs-lookup"><span data-stu-id="5f6c4-164">4</span></span>      | <span data-ttu-id="5f6c4-165">4</span><span class="sxs-lookup"><span data-stu-id="5f6c4-165">4</span></span>      | <span data-ttu-id="5f6c4-166">4</span><span class="sxs-lookup"><span data-stu-id="5f6c4-166">4</span></span>      |
| <span data-ttu-id="5f6c4-167">GL \_ RGB5 \_ a1</span><span class="sxs-lookup"><span data-stu-id="5f6c4-167">GL\_RGB5\_A1</span></span>   | <span data-ttu-id="5f6c4-168">\_RGBA GL</span><span class="sxs-lookup"><span data-stu-id="5f6c4-168">GL\_RGBA</span></span>    | <span data-ttu-id="5f6c4-169">5</span><span class="sxs-lookup"><span data-stu-id="5f6c4-169">5</span></span>      | <span data-ttu-id="5f6c4-170">5</span><span class="sxs-lookup"><span data-stu-id="5f6c4-170">5</span></span>      | <span data-ttu-id="5f6c4-171">5</span><span class="sxs-lookup"><span data-stu-id="5f6c4-171">5</span></span>      | <span data-ttu-id="5f6c4-172">1</span><span class="sxs-lookup"><span data-stu-id="5f6c4-172">1</span></span>      |
| <span data-ttu-id="5f6c4-173">\_Rgba8 GL</span><span class="sxs-lookup"><span data-stu-id="5f6c4-173">GL\_RGBA8</span></span>      | <span data-ttu-id="5f6c4-174">\_RGBA GL</span><span class="sxs-lookup"><span data-stu-id="5f6c4-174">GL\_RGBA</span></span>    | <span data-ttu-id="5f6c4-175">8</span><span class="sxs-lookup"><span data-stu-id="5f6c4-175">8</span></span>      | <span data-ttu-id="5f6c4-176">8</span><span class="sxs-lookup"><span data-stu-id="5f6c4-176">8</span></span>      | <span data-ttu-id="5f6c4-177">8</span><span class="sxs-lookup"><span data-stu-id="5f6c4-177">8</span></span>      | <span data-ttu-id="5f6c4-178">8</span><span class="sxs-lookup"><span data-stu-id="5f6c4-178">8</span></span>      |
| <span data-ttu-id="5f6c4-179">GL \_ RG10 \_ a2</span><span class="sxs-lookup"><span data-stu-id="5f6c4-179">GL\_RG10\_A2</span></span>   | <span data-ttu-id="5f6c4-180">\_RGBA GL</span><span class="sxs-lookup"><span data-stu-id="5f6c4-180">GL\_RGBA</span></span>    | <span data-ttu-id="5f6c4-181">10</span><span class="sxs-lookup"><span data-stu-id="5f6c4-181">10</span></span>     | <span data-ttu-id="5f6c4-182">10</span><span class="sxs-lookup"><span data-stu-id="5f6c4-182">10</span></span>     | <span data-ttu-id="5f6c4-183">10</span><span class="sxs-lookup"><span data-stu-id="5f6c4-183">10</span></span>     | <span data-ttu-id="5f6c4-184">2</span><span class="sxs-lookup"><span data-stu-id="5f6c4-184">2</span></span>      |
| <span data-ttu-id="5f6c4-185">\_RGB12 GL</span><span class="sxs-lookup"><span data-stu-id="5f6c4-185">GL\_RGB12</span></span>      | <span data-ttu-id="5f6c4-186">\_RGBA GL</span><span class="sxs-lookup"><span data-stu-id="5f6c4-186">GL\_RGBA</span></span>    | <span data-ttu-id="5f6c4-187">12</span><span class="sxs-lookup"><span data-stu-id="5f6c4-187">12</span></span>     | <span data-ttu-id="5f6c4-188">12</span><span class="sxs-lookup"><span data-stu-id="5f6c4-188">12</span></span>     | <span data-ttu-id="5f6c4-189">12</span><span class="sxs-lookup"><span data-stu-id="5f6c4-189">12</span></span>     | <span data-ttu-id="5f6c4-190">12</span><span class="sxs-lookup"><span data-stu-id="5f6c4-190">12</span></span>     |
| <span data-ttu-id="5f6c4-191">\_RGBA16 GL</span><span class="sxs-lookup"><span data-stu-id="5f6c4-191">GL\_RGBA16</span></span>     | <span data-ttu-id="5f6c4-192">\_RGBA GL</span><span class="sxs-lookup"><span data-stu-id="5f6c4-192">GL\_RGBA</span></span>    | <span data-ttu-id="5f6c4-193">16</span><span class="sxs-lookup"><span data-stu-id="5f6c4-193">16</span></span>     | <span data-ttu-id="5f6c4-194">16</span><span class="sxs-lookup"><span data-stu-id="5f6c4-194">16</span></span>     | <span data-ttu-id="5f6c4-195">16</span><span class="sxs-lookup"><span data-stu-id="5f6c4-195">16</span></span>     | <span data-ttu-id="5f6c4-196">16</span><span class="sxs-lookup"><span data-stu-id="5f6c4-196">16</span></span>     |



 

</dd> <dt>

<span data-ttu-id="5f6c4-197">*width*</span><span class="sxs-lookup"><span data-stu-id="5f6c4-197">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="5f6c4-198">Dimensione della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-198">The size of the palette.</span></span> <span data-ttu-id="5f6c4-199">Deve essere 2n = 1 per alcuni numeri interi *n*.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-199">Must be 2n = 1 for some integer *n*.</span></span>

</dd> <dt>

<span data-ttu-id="5f6c4-200">*format*</span><span class="sxs-lookup"><span data-stu-id="5f6c4-200">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="5f6c4-201">Formato dei dati pixel.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-201">The format of the pixel data.</span></span> <span data-ttu-id="5f6c4-202">Vengono accettate le seguenti costanti simboliche.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-202">The following symbolic constants are accepted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5f6c4-203">Valore</span><span class="sxs-lookup"><span data-stu-id="5f6c4-203">Value</span></span></th>
<th><span data-ttu-id="5f6c4-204">Significato</span><span class="sxs-lookup"><span data-stu-id="5f6c4-204">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="5f6c4-205"><dt><strong>GL_RGBA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5f6c4-205"><dt><strong>GL_RGBA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5f6c4-206">Ogni pixel è un gruppo di quattro componenti in questo ordine: rosso, verde, blu, alfa.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-206">Each pixel is a group of four components in this order: red, green, blue, alpha.</span></span> <span data-ttu-id="5f6c4-207">Il formato RGBA viene determinato in questo modo:</span><span class="sxs-lookup"><span data-stu-id="5f6c4-207">The RGBA format is determined in this way:</span></span> <br/>
<ol>
<li><span data-ttu-id="5f6c4-208">La funzione <strong>glColorTableEXT</strong> converte i valori a virgola mobile direttamente in un formato interno con precisione non specificata.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-208">The <strong>glColorTableEXT</strong> function converts floating-point values directly to an internal format with unspecified precision.</span></span> <span data-ttu-id="5f6c4-209">Per i valori integer con segno viene eseguito il mapping lineare al formato interno, in modo che il valore integer rappresentabile più positivo sia mappato a 1,0 e che il valore integer rappresentabile più negativo sia mappato a-1,0.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-209">Signed integer values are mapped linearly to the internal format such that the most positive representable integer value maps to 1.0, and the most negative representable integer value maps to -1.0.</span></span> <span data-ttu-id="5f6c4-210">Viene eseguito il mapping dei dati integer senza segno in modo analogo: il valore integer più grande viene mappato a 1,0 e zero viene mappato a 0,0.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-210">Unsigned integer data is mapped similarly: the largest integer value maps to 1.0, and zero maps to 0.0.</span></span></li>
<li><span data-ttu-id="5f6c4-211">La funzione <strong>glColorTableEXT</strong> moltiplica i valori di colore risultanti per GL_c_SCALE e li aggiunge a GL_c_BIAS, dove <em>c</em> è rosso, verde, blu e alfa per i rispettivi componenti di colore.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-211">The <strong>glColorTableEXT</strong> function multiplies the resulting color values by GL_c_SCALE and adds them to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span> <span data-ttu-id="5f6c4-212">I risultati vengono fissati nell'intervallo [0, 1].</span><span class="sxs-lookup"><span data-stu-id="5f6c4-212">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="5f6c4-213">Se GL_MAP_COLOR è <strong>true</strong>, <strong>glColorTableEXT</strong> ridimensiona ogni componente del colore in base alla dimensione della tabella di ricerca GL_PIXEL_MAP_c_TO_c, quindi sostituisce il componente in base al valore a cui fa riferimento nella tabella. <em>c</em> è rispettivamente R, G, B o A.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-213">If GL_MAP_COLOR is <strong>TRUE</strong>, <strong>glColorTableEXT</strong> scales each color component by the size of lookup table GL_PIXEL_MAP_c_TO_c, then replaces the component by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span></li>
<li><span data-ttu-id="5f6c4-214">La funzione <strong>glColorTableEXT</strong> converte i colori RGBA risultanti in frammenti associando <em>la posizione raster</em>corrente e le coordinate della trama a ogni pixel, quindi assegnando le coordinate della finestra <em>x</em> e <em>y</em> al frammento <em>n</em>, ad esempio<em>x</em>?</span><span class="sxs-lookup"><span data-stu-id="5f6c4-214">The <strong>glColorTableEXT</strong> function converts the resulting RGBA colors to fragments by attaching the current raster position <em>z</em>-coordinate and texture coordinates to each pixel, then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em>th fragment such that<em>x</em>?</span></span><span data-ttu-id="5f6c4-215"> = <em>larghezza</em> <em>x</em><sub>r</sub> + <em>n</em> mod</span><span class="sxs-lookup"><span data-stu-id="5f6c4-215"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="5f6c4-216"><em></em>y?</span><span class="sxs-lookup"><span data-stu-id="5f6c4-216"><em></em>y?</span></span><span data-ttu-id="5f6c4-217"> = <em>y</em><sub>r</sub> +<em>n/Larghezza</em></span><span class="sxs-lookup"><span data-stu-id="5f6c4-217"> = <em>y</em><sub>r</sub> +<em>n / width</em></span></span><br/> <span data-ttu-id="5f6c4-218">dove (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) è la posizione raster corrente.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-218">where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="5f6c4-219">Questi frammenti di pixel vengono quindi trattati come i frammenti generati dalla rasterizzazione di punti, linee o poligoni.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-219">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="5f6c4-220">La funzione <strong>glColorTableEXT</strong> applica il mapping di trama, la nebbia e tutte le operazioni di frammento prima di scrivere i frammenti sul framebuffer.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-220">The <strong>glColorTableEXT</strong> function applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="5f6c4-221"><dt><strong>GL_RED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5f6c4-221"><dt><strong>GL_RED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5f6c4-222">Ogni pixel è un singolo componente rosso.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-222">Each pixel is a single red component.</span></span><br/> <span data-ttu-id="5f6c4-223">La funzione <strong>glColorTableEXT</strong> converte il componente nel formato interno nello stesso modo in cui il componente rosso di un pixel RGBA è, quindi lo converte in un pixel RGBA con il verde e il blu impostati su 0,0 e Alpha impostato su 1,0.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-223">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the red component of an RGBA pixel is, then converts it to an RGBA pixel with green and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="5f6c4-224">Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-224">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="5f6c4-225"><dt><strong>GL_GREEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5f6c4-225"><dt><strong>GL_GREEN</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5f6c4-226">Ogni pixel è un singolo componente verde.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-226">Each pixel is a single green component.</span></span><br/> <span data-ttu-id="5f6c4-227">La funzione <strong>glColorTableEXT</strong> converte il componente nel formato interno nello stesso modo in cui il componente verde di un pixel RGBA è e quindi lo converte in un pixel RGBA con il rosso e il blu impostati su 0,0 e Alpha impostato su 1,0.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-227">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the green component of an RGBA pixel is, and then converts it to an RGBA pixel with red and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="5f6c4-228">Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-228">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="5f6c4-229"><dt><strong>GL_BLUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5f6c4-229"><dt><strong>GL_BLUE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5f6c4-230">Ogni pixel è un singolo componente blu.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-230">Each pixel is a single blue component.</span></span><br/> <span data-ttu-id="5f6c4-231">La funzione <strong>glColorTableEXT</strong> converte il componente nel formato interno nello stesso modo in cui il componente blu di un pixel RGBA è e quindi lo converte in un pixel RGBA con rosso e verde impostato su 0,0 e Alpha impostato su 1,0.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-231">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the blue component of an RGBA pixel is, and then converts it to an RGBA pixel with red and green set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="5f6c4-232">Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-232">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="5f6c4-233"><dt><strong>GL_ALPHA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5f6c4-233"><dt><strong>GL_ALPHA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5f6c4-234">Ogni pixel è un singolo componente alfa.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-234">Each pixel is a single alpha component.</span></span><br/> <span data-ttu-id="5f6c4-235">La funzione <strong>glColorTableEXT</strong> converte il componente nel formato interno nello stesso modo in cui il componente alfa di un pixel RGBA è e quindi lo converte in un pixel RGBA con rosso, verde e blu impostato su 0,0.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-235">The <strong>glColorTableEXT</strong> function converts this component to the internal format in the same way that the alpha component of an RGBA pixel is, and then converts it to an RGBA pixel with red, green, and blue set to 0.0.</span></span> <span data-ttu-id="5f6c4-236">Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-236">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="5f6c4-237"><dt><strong>GL_RGB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5f6c4-237"><dt><strong>GL_RGB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5f6c4-238">Ogni pixel è un gruppo di tre componenti in questo ordine: rosso, verde, blu.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-238">Each pixel is a group of three components in this order: red, green, blue.</span></span><br/> <span data-ttu-id="5f6c4-239">La funzione <strong>glColorTableEXT</strong> converte ogni componente nel formato interno nello stesso modo in cui i componenti rosso, verde e blu di un pixel RGBA sono.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-239">The <strong>glColorTableEXT</strong> function converts each component to the internal format in the same way that the red, green, and blue components of an RGBA pixel are.</span></span> <span data-ttu-id="5f6c4-240">Il colore triple viene convertito in un pixel RGBA con Alpha impostato su 1,0.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-240">The color triple is converted to an RGBA pixel with alpha set to 1.0.</span></span> <span data-ttu-id="5f6c4-241">Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-241">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="5f6c4-242"><dt><strong>GL_BGR_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5f6c4-242"><dt><strong>GL_BGR_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5f6c4-243">Ogni pixel è un gruppo di tre componenti in questo ordine: blu, verde, rosso.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-243">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="5f6c4-244">GL_BGR_EXT fornisce un formato corrispondente al layout di memoria delle bitmap indipendenti dal dispositivo (DIB) Windows.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-244">GL_BGR_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="5f6c4-245">In questo modo, le applicazioni possono usare gli stessi dati con le chiamate di funzione di Windows e le chiamate di funzione pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-245">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="5f6c4-246"><dt><strong>GL_BGRA_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5f6c4-246"><dt><strong>GL_BGRA_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5f6c4-247">Ogni pixel è un gruppo di quattro componenti in questo ordine: blu, verde, rosso, alfa.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-247">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="5f6c4-248">GL_BGRA_EXT fornisce un formato corrispondente al layout di memoria delle bitmap indipendenti dal dispositivo (DIB) Windows.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-248">GL_BGRA_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="5f6c4-249">In questo modo, le applicazioni possono usare gli stessi dati con le chiamate di funzione di Windows e le chiamate di funzione pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-249">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="5f6c4-250">*type*</span><span class="sxs-lookup"><span data-stu-id="5f6c4-250">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="5f6c4-251">Tipo di dati per i *dati*.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-251">The data type for *data*.</span></span> <span data-ttu-id="5f6c4-252">Sono accettate le costanti simboliche seguenti: GL \_ UNsigned \_ byte, GL \_ byte, GL \_ unsigned \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int e GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-252">The following symbolic constants are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

<span data-ttu-id="5f6c4-253">Nella tabella seguente viene riepilogato il significato delle costanti valide per il parametro di *tipo* .</span><span class="sxs-lookup"><span data-stu-id="5f6c4-253">The following table summarizes the meaning of the valid constants for the *type* parameter.</span></span>



| <span data-ttu-id="5f6c4-254">Valore</span><span class="sxs-lookup"><span data-stu-id="5f6c4-254">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="5f6c4-255">Significato</span><span class="sxs-lookup"><span data-stu-id="5f6c4-255">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="5f6c4-256"><dt>**\_byte senza segno GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5f6c4-256"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="5f6c4-257">Intero senza segno a 8 bit</span><span class="sxs-lookup"><span data-stu-id="5f6c4-257">Unsigned 8-bit integer</span></span><br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="5f6c4-258"><dt>**\_byte GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5f6c4-258"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="5f6c4-259">Valore intero con segno a 8 bit</span><span class="sxs-lookup"><span data-stu-id="5f6c4-259">Signed 8-bit integer</span></span><br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="5f6c4-260"><dt>**\_short senza segno GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5f6c4-260"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="5f6c4-261">Intero senza segno a 16 bit</span><span class="sxs-lookup"><span data-stu-id="5f6c4-261">Unsigned 16-bit integer</span></span><br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="5f6c4-262"><dt>**\_short GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5f6c4-262"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="5f6c4-263">Valore intero a 16 bit con segno</span><span class="sxs-lookup"><span data-stu-id="5f6c4-263">Signed 16-bit integer</span></span><br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="5f6c4-264"><dt>**GL \_ senza segno \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="5f6c4-264"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="5f6c4-265">Intero senza segno a 32 bit</span><span class="sxs-lookup"><span data-stu-id="5f6c4-265">Unsigned 32-bit integer</span></span><br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="5f6c4-266"><dt>**GL \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="5f6c4-266"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="5f6c4-267">Intero a 32 bit</span><span class="sxs-lookup"><span data-stu-id="5f6c4-267">32-bit integer</span></span><br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="5f6c4-268"><dt>**GL \_ float**</dt></span><span class="sxs-lookup"><span data-stu-id="5f6c4-268"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="5f6c4-269">Valore a virgola mobile e precisione singola</span><span class="sxs-lookup"><span data-stu-id="5f6c4-269">Single-precision floating-point value</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5f6c4-270">*data*</span><span class="sxs-lookup"><span data-stu-id="5f6c4-270">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="5f6c4-271">Puntatore ai dati della trama con tavolozza.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-271">A pointer to the paletted texture data.</span></span> <span data-ttu-id="5f6c4-272">I dati vengono considerati come singoli pixel di una voce della tavolozza della trama da 1 a D per una voce della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-272">The data is treated as single pixels of a 1-D texture palette entry for a palette entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f6c4-273">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5f6c4-273">Return value</span></span>

<span data-ttu-id="5f6c4-274">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-274">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5f6c4-275">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="5f6c4-275">Error codes</span></span>

<span data-ttu-id="5f6c4-276">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="5f6c4-276">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5f6c4-277">Nome</span><span class="sxs-lookup"><span data-stu-id="5f6c4-277">Name</span></span>                                                                                                  | <span data-ttu-id="5f6c4-278">Significato</span><span class="sxs-lookup"><span data-stu-id="5f6c4-278">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5f6c4-279"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5f6c4-279"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="5f6c4-280">*Width* non è un numero intero valido.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-280">*width* was an invalid integer.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="5f6c4-281"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5f6c4-281"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="5f6c4-282">*target*, *internalFormat*, *Format* o *Type* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-282">*target*, *internalFormat*, *format*, or *type* was not an accepted value.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="5f6c4-283"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5f6c4-283"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5f6c4-284">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="5f6c4-284">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5f6c4-285">Commenti</span><span class="sxs-lookup"><span data-stu-id="5f6c4-285">Remarks</span></span>

<span data-ttu-id="5f6c4-286">Le trame con tavolozza sono definite con una tavolozza di colori e un set di dati immagine costituito da indici per le voci di colori di una tavolozza (tabella dei colori).</span><span class="sxs-lookup"><span data-stu-id="5f6c4-286">Paletted textures are defined with a palette of colors and a set of image data that is composed of indexes to color entries of a palette (a color table).</span></span>

<span data-ttu-id="5f6c4-287">La funzione **glColorTableEXT** specifica la tavolozza di trama di una trama di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-287">The **glColorTableEXT** function specifies the texture palette of a targeted texture.</span></span> <span data-ttu-id="5f6c4-288">Preleva i *dati* dalla memoria e li converte come se ogni voce della tavolozza è un singolo pixel di una trama da 1 a D.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-288">It takes the *data* from memory and converts the data as if each palette entry is a single pixel of a 1-D texture.</span></span> <span data-ttu-id="5f6c4-289">La funzione **glColorTableEXT** decomprime e converte i dati e li converte in un formato interno che corrisponde al *formato* specificato il più vicino possibile.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-289">The **glColorTableEXT** function unpacks and converts the data and translates it into an internal format that matches the given *format* as closely as possible.</span></span>

<span data-ttu-id="5f6c4-290">Se la *larghezza* della tavolozza è maggiore dell'intervallo degli indici di colore nei dati della trama, alcune voci della tavolozza sono inutilizzate.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-290">If a palette's *width* is greater than the range of the color indexes in the texture data, some of the palette entries are unused.</span></span> <span data-ttu-id="5f6c4-291">Se la *larghezza* della tavolozza è inferiore all'intervallo degli indici dei colori nei dati della trama, i bit più significativi dei dati della trama vengono ignorati e viene usato solo il numero appropriato di bit nell'indice quando si accede alla tavolozza.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-291">If a palette's *width* is less than the range of the color indexes in the texture data, the most significant bits of the texture data are ignored and only the appropriate number of bits in the index are used when accessing the palette.</span></span> <span data-ttu-id="5f6c4-292">Quando si specifica una *destinazione* proxy usando \_ la trama \_ del proxy 1D \_ o \_ la trama del proxy 2D, la tavolozza della trama del proxy viene ridimensionata e i parametri vengono impostati, ma non viene eseguito il trasferimento o l'accesso ai dati.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-292">When you specify a proxy *target* using PROXY\_TEXTURE\_1D or PROXY\_TEXTURE\_2D, the palette of the proxy texture is resized and its parameters are set but no data is transferred or accessed.</span></span>

<span data-ttu-id="5f6c4-293">Quando il parametro di *destinazione* è GL \_ proxy \_ texture \_ 1D o \_ GL proxy \_ texture \_ 2D e l'implementazione non supporta i valori specificati per il *formato* o la *larghezza*, **glColorTableEXT** può non essere in grado di creare la tabella dei colori richiesta.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-293">When the *target* parameter is GL\_PROXY\_TEXTURE\_1D or GL\_PROXY\_TEXTURE\_2D, and the implementation does not support the values specified for either *format* or *width*, **glColorTableEXT** can fail to create the requested color table.</span></span> <span data-ttu-id="5f6c4-294">In questo caso, la tabella dei colori è vuota e tutti i parametri recuperati saranno pari a zero.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-294">In this case, the color table is empty and all parameters retrieved will be zero.</span></span> <span data-ttu-id="5f6c4-295">È possibile determinare se OpenGL supporta un formato e una dimensione della tabella dei colori specifici chiamando **glColorTableEXT** con una destinazione proxy e quindi chiamando [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) o [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) per determinare se il parametro width corrisponde a quello impostato da **glColorTableEXT**.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-295">You can determine whether OpenGL supports a particular color table format and size by calling **glColorTableEXT** with a proxy target, and then calling [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) or [**glGetColorTableParameterfvEXT**](glgetcolortableparameterfvext.md) to determine whether the width parameter matches that set by **glColorTableEXT**.</span></span> <span data-ttu-id="5f6c4-296">Se la larghezza recuperata è zero, la richiesta della tabella dei colori di **glColorTable** non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-296">If the retrieved width is zero, the color table request by **glColorTable** failed.</span></span> <span data-ttu-id="5f6c4-297">Se la larghezza recuperata è diversa da zero, è possibile chiamare **glColorTable** con la destinazione reale con trama \_ 1D o trama \_ 2D per impostare la tabella dei colori.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-297">If the retrieved width is not zero, you can call **glColorTable** with the real target with TEXTURE\_1D or TEXTURE\_2D to set the color table.</span></span>

> [!Note]  
> <span data-ttu-id="5f6c4-298">La funzione **glColorTableEXT** è una funzione di estensione che non fa parte della libreria OpenGL standard, ma fa parte dell'estensione di trama di GL \_ ext con \_ tavolozza \_ .</span><span class="sxs-lookup"><span data-stu-id="5f6c4-298">The **glColorTableEXT** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="5f6c4-299">Per verificare se l'implementazione di OpenGL supporta **glColorTableEXT**, chiamare [**glGetString**](glgetstring.md)(GL \_ Extensions).</span><span class="sxs-lookup"><span data-stu-id="5f6c4-299">To check whether your implementation of OpenGL supports **glColorTableEXT**, call [**glGetString**](glgetstring.md)(GL\_EXTENSIONS).</span></span> <span data-ttu-id="5f6c4-300">Se restituisce \_ \_ la trama della tavolozza GL ext \_ , **glColorTableEXT** è supportato.</span><span class="sxs-lookup"><span data-stu-id="5f6c4-300">If it returns GL\_EXT\_paletted\_texture, **glColorTableEXT** is supported.</span></span> <span data-ttu-id="5f6c4-301">Per ottenere l'indirizzo della funzione di una funzione di estensione, chiamare [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span><span class="sxs-lookup"><span data-stu-id="5f6c4-301">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

 

<span data-ttu-id="5f6c4-302">Per recuperare i dati effettivi della tabella dei colori specificati dalla funzione **glColorTableEXT** , chiamare [**glGetColorTableEXT**](glgetcolortableext.md).</span><span class="sxs-lookup"><span data-stu-id="5f6c4-302">To retrieve the actual color table data specified by the **glColorTableEXT** function, call [**glGetColorTableEXT**](glgetcolortableext.md).</span></span> <span data-ttu-id="5f6c4-303">Per recuperare i parametri, ad esempio *Width* e *Format*, della tabella dei colori specificata dalla funzione **GlColorTableEXT** , chiamare la funzione **glGetColorTableParameterivEXT** o **glGetColorTableParameterfvEXT** .</span><span class="sxs-lookup"><span data-stu-id="5f6c4-303">To retrieve the parameters, such as *width* and *format*, of the color table specified by the **glColorTableEXT** function, call the **glGetColorTableParameterivEXT** or **glGetColorTableParameterfvEXT** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f6c4-304">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f6c4-304">Requirements</span></span>



| <span data-ttu-id="5f6c4-305">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f6c4-305">Requirement</span></span> | <span data-ttu-id="5f6c4-306">Valore</span><span class="sxs-lookup"><span data-stu-id="5f6c4-306">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="5f6c4-307">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f6c4-307">Minimum supported client</span></span><br/> | <span data-ttu-id="5f6c4-308">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5f6c4-308">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="5f6c4-309">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f6c4-309">Minimum supported server</span></span><br/> | <span data-ttu-id="5f6c4-310">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5f6c4-310">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5f6c4-311">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5f6c4-311">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f6c4-312"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f6c4-312"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f6c4-313">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f6c4-313">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f6c4-314">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5f6c4-314">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5f6c4-315">**glColorSubTableEXT**</span><span class="sxs-lookup"><span data-stu-id="5f6c4-315">**glColorSubTableEXT**</span></span>](glcolorsubtableext.md)
</dt> <dt>

[<span data-ttu-id="5f6c4-316">**Remo**</span><span class="sxs-lookup"><span data-stu-id="5f6c4-316">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5f6c4-317">**glGetColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="5f6c4-317">**glGetColorTableEXT**</span></span>](glgetcolortableext.md)
</dt> <dt>

[<span data-ttu-id="5f6c4-318">**glGetColorTableParameterfvEXT**</span><span class="sxs-lookup"><span data-stu-id="5f6c4-318">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="5f6c4-319">**glGetColorTableParameterivEXT**</span><span class="sxs-lookup"><span data-stu-id="5f6c4-319">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="5f6c4-320">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="5f6c4-320">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





