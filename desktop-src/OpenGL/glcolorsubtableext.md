---
title: funzione glColorSubTableEXT (GL. h)
description: La funzione glColorSubTableEXT specifica una parte della tavolozza della trama di destinazione da sostituire.
ms.assetid: 21430245-f837-4c7a-944f-b44482254b12
keywords:
- funzione glColorSubTableEXT OpenGL
topic_type:
- apiref
api_name:
- glColorSubTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0386bda82bf08ae778d20b1be69858698ac7bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873974"
---
# <a name="glcolorsubtableext-function"></a><span data-ttu-id="4fe96-104">glColorSubTableEXT (funzione)</span><span class="sxs-lookup"><span data-stu-id="4fe96-104">glColorSubTableEXT function</span></span>

<span data-ttu-id="4fe96-105">La funzione **glColorSubTableEXT** specifica una parte della tavolozza della trama di destinazione da sostituire.</span><span class="sxs-lookup"><span data-stu-id="4fe96-105">The **glColorSubTableEXT** function specifies a portion of the targeted texture's palette to be replaced.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fe96-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4fe96-106">Syntax</span></span>


```C++
void WINAPI glColorSubTableEXT(
         GLenum  target,
         GLsizei start,
         GLsizei count,
         GLenum  format,
         GLenum  type,
   const GLvoid  *data
);
```



## <a name="parameters"></a><span data-ttu-id="4fe96-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4fe96-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fe96-108">*target*</span><span class="sxs-lookup"><span data-stu-id="4fe96-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="4fe96-109">Trama della tavolozza di destinazione per la quale è stata modificata la tavolozza.</span><span class="sxs-lookup"><span data-stu-id="4fe96-109">The target paletted texture that is to have its palette changed.</span></span> <span data-ttu-id="4fe96-110">Deve essere una trama \_ 1D o trama \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="4fe96-110">Must be TEXTURE\_1D or TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="4fe96-111">*start*</span><span class="sxs-lookup"><span data-stu-id="4fe96-111">*start*</span></span> 
</dt> <dd>

<span data-ttu-id="4fe96-112">Voce di indice della tavolozza iniziale della tavolozza da modificare.</span><span class="sxs-lookup"><span data-stu-id="4fe96-112">The starting palette index entry of the palette to be changed.</span></span>

</dd> <dt>

<span data-ttu-id="4fe96-113">*count*</span><span class="sxs-lookup"><span data-stu-id="4fe96-113">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="4fe96-114">Numero di voci di indice della tavolozza della tavolozza da modificare a partire dall' *inizio*.</span><span class="sxs-lookup"><span data-stu-id="4fe96-114">The number of palette index entries of the palette to be changed beginning at *start*.</span></span> <span data-ttu-id="4fe96-115">Il parametro *count* determina l'intervallo delle voci di indice della tavolozza modificate.</span><span class="sxs-lookup"><span data-stu-id="4fe96-115">The *count* parameter determines the range of palette index entries that are changed.</span></span>

</dd> <dt>

<span data-ttu-id="4fe96-116">*format*</span><span class="sxs-lookup"><span data-stu-id="4fe96-116">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="4fe96-117">Formato dei dati pixel.</span><span class="sxs-lookup"><span data-stu-id="4fe96-117">The format of the pixel data.</span></span> <span data-ttu-id="4fe96-118">Vengono accettate le seguenti costanti simboliche.</span><span class="sxs-lookup"><span data-stu-id="4fe96-118">The following symbolic constants are accepted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4fe96-119">Valore</span><span class="sxs-lookup"><span data-stu-id="4fe96-119">Value</span></span></th>
<th><span data-ttu-id="4fe96-120">Significato</span><span class="sxs-lookup"><span data-stu-id="4fe96-120">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="4fe96-121"><dt><strong>GL_RGBA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4fe96-121"><dt><strong>GL_RGBA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="4fe96-122">Ogni pixel è un gruppo di quattro componenti nell'ordine seguente: rosso, verde, blu, alfa.</span><span class="sxs-lookup"><span data-stu-id="4fe96-122">Each pixel is a group of four components in the following order: red, green, blue, alpha.</span></span> <span data-ttu-id="4fe96-123">Il formato RGBA viene determinato in questo modo:</span><span class="sxs-lookup"><span data-stu-id="4fe96-123">The RGBA format is determined in this way:</span></span> <br/>
<ol>
<li><span data-ttu-id="4fe96-124">La funzione <strong>glColorSubTableEXT</strong> converte i valori a virgola mobile direttamente in un formato interno con precisione non specificata.</span><span class="sxs-lookup"><span data-stu-id="4fe96-124">The <strong>glColorSubTableEXT</strong> function converts floating-point values directly to an internal format with unspecified precision.</span></span> <span data-ttu-id="4fe96-125">Per i valori integer con segno viene eseguito il mapping lineare al formato interno, in modo che il valore integer rappresentabile più positivo sia mappato a 1,0 e che il valore rappresentativo più negativo sia mappato a-1,0.</span><span class="sxs-lookup"><span data-stu-id="4fe96-125">Signed integer values are mapped linearly to the internal format such that the most positive representable integer value maps to 1.0, and the most negative representable value maps to -1.0.</span></span> <span data-ttu-id="4fe96-126">Viene eseguito il mapping dei dati integer senza segno in modo analogo: il valore integer più grande viene mappato a 1,0 e zero viene mappato a 0,0.</span><span class="sxs-lookup"><span data-stu-id="4fe96-126">Unsigned integer data is mapped similarly: the largest integer value maps to 1.0, and zero maps to 0.0.</span></span></li>
<li><span data-ttu-id="4fe96-127">La funzione <strong>glColorSubTableEXT</strong> moltiplica i valori di colore risultanti per GL_c_SCALE e li aggiunge a GL_c_BIAS, dove <em>c</em> è rosso, verde, blu e alfa per i rispettivi componenti di colore.</span><span class="sxs-lookup"><span data-stu-id="4fe96-127">The <strong>glColorSubTableEXT</strong> function multiplies the resulting color values by GL_c_SCALE and adds them to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span> <span data-ttu-id="4fe96-128">I risultati vengono fissati nell'intervallo [0, 1].</span><span class="sxs-lookup"><span data-stu-id="4fe96-128">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="4fe96-129">Se GL_MAP_COLOR è <strong>true</strong>, <strong>glColorSubTableEXT</strong> ridimensiona ogni componente del colore in base alla dimensione della tabella di ricerca GL_PIXEL_MAP_c_TO_c, quindi sostituisce il componente in base al valore a cui fa riferimento nella tabella. <em>c</em> è rispettivamente R, G, B o A.</span><span class="sxs-lookup"><span data-stu-id="4fe96-129">If GL_MAP_COLOR is <strong>TRUE</strong>, <strong>glColorSubTableEXT</strong> scales each color component by the size of lookup table GL_PIXEL_MAP_c_TO_c, then replaces the component by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span></li>
<li><span data-ttu-id="4fe96-130">La funzione <strong>glColorSubTableEXT</strong> converte i colori RGBA risultanti in frammenti associando <em>la posizione raster</em>corrente e le coordinate della trama a ogni pixel, quindi assegnando le coordinate della finestra <em>x</em> e <em>y</em> al frammento <em>n</em>, ad esempio<em>x</em>?</span><span class="sxs-lookup"><span data-stu-id="4fe96-130">The <strong>glColorSubTableEXT</strong> function converts the resulting RGBA colors to fragments by attaching the current raster position <em>z</em>-coordinate and texture coordinates to each pixel, then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em>th fragment such that<em>x</em>?</span></span><span data-ttu-id="4fe96-131"> = <em>larghezza</em> <em>x</em><sub>r</sub> + <em>n</em> mod</span><span class="sxs-lookup"><span data-stu-id="4fe96-131"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="4fe96-132"><em>y</em>?</span><span class="sxs-lookup"><span data-stu-id="4fe96-132"><em>y</em>?</span></span><span data-ttu-id="4fe96-133"> = <em>y</em><sub>r</sub> +<em>n/Larghezza</em></span><span class="sxs-lookup"><span data-stu-id="4fe96-133"> = <em>y</em><sub>r</sub> +<em>n / width</em></span></span><br/> <span data-ttu-id="4fe96-134">dove (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) è la posizione raster corrente.</span><span class="sxs-lookup"><span data-stu-id="4fe96-134">where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="4fe96-135">Questi frammenti di pixel vengono quindi trattati come i frammenti generati dalla rasterizzazione di punti, linee o poligoni.</span><span class="sxs-lookup"><span data-stu-id="4fe96-135">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="4fe96-136">La funzione <strong>glColorSubTableEXT</strong> applica il mapping di trama, la nebbia e tutte le operazioni di frammento prima di scrivere i frammenti sul framebuffer.</span><span class="sxs-lookup"><span data-stu-id="4fe96-136">The <strong>glColorSubTableEXT</strong> function applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="4fe96-137"><dt><strong>GL_RED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4fe96-137"><dt><strong>GL_RED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="4fe96-138">Ogni pixel è un singolo componente rosso.</span><span class="sxs-lookup"><span data-stu-id="4fe96-138">Each pixel is a single red component.</span></span><br/> <span data-ttu-id="4fe96-139">La funzione <strong>glColorSubTableEXT</strong> converte il componente nel formato interno nello stesso modo in cui il componente rosso di un pixel RGBA è, quindi lo converte in un pixel RGBA con il verde e il blu impostati su 0,0 e Alpha impostato su 1,0.</span><span class="sxs-lookup"><span data-stu-id="4fe96-139">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the red component of an RGBA pixel is, then converts it to an RGBA pixel with green and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="4fe96-140">Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="4fe96-140">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="4fe96-141"><dt><strong>GL_GREEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4fe96-141"><dt><strong>GL_GREEN</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="4fe96-142">Ogni pixel è un singolo componente verde.</span><span class="sxs-lookup"><span data-stu-id="4fe96-142">Each pixel is a single green component.</span></span><br/> <span data-ttu-id="4fe96-143">La funzione <strong>glColorSubTableEXT</strong> converte il componente nel formato interno nello stesso modo in cui il componente verde di un pixel RGBA è e quindi lo converte in un pixel RGBA con il rosso e il blu impostati su 0,0 e Alpha impostato su 1,0.</span><span class="sxs-lookup"><span data-stu-id="4fe96-143">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the green component of an RGBA pixel is, and then converts it to an RGBA pixel with red and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="4fe96-144">Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="4fe96-144">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="4fe96-145"><dt><strong>GL_BLUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4fe96-145"><dt><strong>GL_BLUE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="4fe96-146">Ogni pixel è un singolo componente blu.</span><span class="sxs-lookup"><span data-stu-id="4fe96-146">Each pixel is a single blue component.</span></span><br/> <span data-ttu-id="4fe96-147">La funzione <strong>glColorSubTableEXT</strong> converte il componente nel formato interno nello stesso modo in cui il componente blu di un pixel RGBA è e quindi lo converte in un pixel RGBA con rosso e verde impostato su 0,0 e Alpha impostato su 1,0.</span><span class="sxs-lookup"><span data-stu-id="4fe96-147">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the blue component of an RGBA pixel is, and then converts it to an RGBA pixel with red and green set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="4fe96-148">Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="4fe96-148">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="4fe96-149"><dt><strong>GL_ALPHA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4fe96-149"><dt><strong>GL_ALPHA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="4fe96-150">Ogni pixel è un singolo componente alfa.</span><span class="sxs-lookup"><span data-stu-id="4fe96-150">Each pixel is a single alpha component.</span></span><br/> <span data-ttu-id="4fe96-151">La funzione <strong>glColorSubTableEXT</strong> converte il componente nel formato interno nello stesso modo in cui il componente alfa di un pixel RGBA è e quindi lo converte in un pixel RGBA con rosso, verde e blu impostato su 0,0.</span><span class="sxs-lookup"><span data-stu-id="4fe96-151">The <strong>glColorSubTableEXT</strong> function converts this component to the internal format in the same way that the alpha component of an RGBA pixel is, and then converts it to an RGBA pixel with red, green, and blue set to 0.0.</span></span> <span data-ttu-id="4fe96-152">Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="4fe96-152">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="4fe96-153"><dt><strong>GL_RGB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4fe96-153"><dt><strong>GL_RGB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="4fe96-154">Ogni pixel è un gruppo di tre componenti in questo ordine: rosso, verde, blu.</span><span class="sxs-lookup"><span data-stu-id="4fe96-154">Each pixel is a group of three components in this order: red, green, blue.</span></span><br/> <span data-ttu-id="4fe96-155">La funzione <strong>glColorSubTableEXT</strong> converte ogni componente nel formato interno nello stesso modo in cui i componenti rosso, verde e blu di un pixel RGBA sono.</span><span class="sxs-lookup"><span data-stu-id="4fe96-155">The <strong>glColorSubTableEXT</strong> function converts each component to the internal format in the same way that the red, green, and blue components of an RGBA pixel are.</span></span> <span data-ttu-id="4fe96-156">Il colore triple viene convertito in un pixel RGBA con Alpha impostato su 1,0.</span><span class="sxs-lookup"><span data-stu-id="4fe96-156">The color triple is converted to an RGBA pixel with alpha set to 1.0.</span></span> <span data-ttu-id="4fe96-157">Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="4fe96-157">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="4fe96-158"><dt><strong>GL_BGR_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4fe96-158"><dt><strong>GL_BGR_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="4fe96-159">Ogni pixel è un gruppo di tre componenti in questo ordine: blu, verde, rosso.</span><span class="sxs-lookup"><span data-stu-id="4fe96-159">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="4fe96-160">GL_BGR_EXT fornisce un formato corrispondente al layout di memoria delle bitmap indipendenti dal dispositivo (DIB) Windows.</span><span class="sxs-lookup"><span data-stu-id="4fe96-160">GL_BGR_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="4fe96-161">In questo modo, le applicazioni possono usare gli stessi dati con le chiamate di funzione di Windows e le chiamate di funzione pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="4fe96-161">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="4fe96-162"><dt><strong>GL_BGRA_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4fe96-162"><dt><strong>GL_BGRA_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="4fe96-163">Ogni pixel è un gruppo di quattro componenti in questo ordine: blu, verde, rosso, alfa.</span><span class="sxs-lookup"><span data-stu-id="4fe96-163">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="4fe96-164">GL_BGRA_EXT fornisce un formato corrispondente al layout di memoria delle bitmap indipendenti dal dispositivo (DIB) Windows.</span><span class="sxs-lookup"><span data-stu-id="4fe96-164">GL_BGRA_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="4fe96-165">In questo modo, le applicazioni possono usare gli stessi dati con le chiamate di funzione di Windows e le chiamate di funzione pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="4fe96-165">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="4fe96-166">*type*</span><span class="sxs-lookup"><span data-stu-id="4fe96-166">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="4fe96-167">Tipo di dati per i *dati*.</span><span class="sxs-lookup"><span data-stu-id="4fe96-167">The data type for *data*.</span></span> <span data-ttu-id="4fe96-168">Sono accettate le costanti simboliche seguenti: GL \_ UNsigned \_ byte, GL \_ byte, GL \_ unsigned \_ short, GL \_ short, GL \_ unsigned \_ int, GL \_ int e GL \_ float.</span><span class="sxs-lookup"><span data-stu-id="4fe96-168">The following symbolic constants are accepted: GL\_UNSIGNED\_BYTE, GL\_BYTE, GL\_UNSIGNED\_SHORT, GL\_SHORT, GL\_UNSIGNED\_INT, GL\_INT, and GL\_FLOAT.</span></span>

<span data-ttu-id="4fe96-169">Nella tabella seguente viene riepilogato il significato delle costanti valide per il parametro di *tipo* .</span><span class="sxs-lookup"><span data-stu-id="4fe96-169">The following table summarizes the meaning of the valid constants for the *type* parameter.</span></span>



| <span data-ttu-id="4fe96-170">Valore</span><span class="sxs-lookup"><span data-stu-id="4fe96-170">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="4fe96-171">Significato</span><span class="sxs-lookup"><span data-stu-id="4fe96-171">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="4fe96-172"><dt>**\_byte senza segno GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4fe96-172"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="4fe96-173">Intero senza segno a 8 bit</span><span class="sxs-lookup"><span data-stu-id="4fe96-173">Unsigned 8-bit integer</span></span><br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="4fe96-174"><dt>**\_byte GL**</dt></span><span class="sxs-lookup"><span data-stu-id="4fe96-174"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="4fe96-175">Valore intero con segno a 8 bit</span><span class="sxs-lookup"><span data-stu-id="4fe96-175">Signed 8-bit integer</span></span><br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="4fe96-176"><dt>**\_short senza segno GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4fe96-176"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="4fe96-177">Intero senza segno a 16 bit</span><span class="sxs-lookup"><span data-stu-id="4fe96-177">Unsigned 16-bit integer</span></span><br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="4fe96-178"><dt>**\_short GL**</dt></span><span class="sxs-lookup"><span data-stu-id="4fe96-178"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="4fe96-179">Valore intero a 16 bit con segno</span><span class="sxs-lookup"><span data-stu-id="4fe96-179">Signed 16-bit integer</span></span><br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="4fe96-180"><dt>**GL \_ senza segno \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="4fe96-180"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="4fe96-181">Intero senza segno a 32 bit</span><span class="sxs-lookup"><span data-stu-id="4fe96-181">Unsigned 32-bit integer</span></span><br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="4fe96-182"><dt>**GL \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="4fe96-182"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="4fe96-183">Intero a 32 bit</span><span class="sxs-lookup"><span data-stu-id="4fe96-183">32-bit integer</span></span><br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="4fe96-184"><dt>**GL \_ float**</dt></span><span class="sxs-lookup"><span data-stu-id="4fe96-184"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="4fe96-185">Valore a virgola mobile e precisione singola</span><span class="sxs-lookup"><span data-stu-id="4fe96-185">Single-precision floating-point value</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4fe96-186">*data*</span><span class="sxs-lookup"><span data-stu-id="4fe96-186">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="4fe96-187">Puntatore ai dati della trama con tavolozza.</span><span class="sxs-lookup"><span data-stu-id="4fe96-187">A pointer to the paletted texture data.</span></span> <span data-ttu-id="4fe96-188">I dati vengono considerati come singoli pixel di una voce della tavolozza della trama da 1 a D per una voce della tavolozza.</span><span class="sxs-lookup"><span data-stu-id="4fe96-188">The data is treated as single pixels of a 1-D texture palette entry for a palette entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fe96-189">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4fe96-189">Return value</span></span>

<span data-ttu-id="4fe96-190">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="4fe96-190">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4fe96-191">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="4fe96-191">Error codes</span></span>

<span data-ttu-id="4fe96-192">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="4fe96-192">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="4fe96-193">Nome</span><span class="sxs-lookup"><span data-stu-id="4fe96-193">Name</span></span>                                                                                              | <span data-ttu-id="4fe96-194">Significato</span><span class="sxs-lookup"><span data-stu-id="4fe96-194">Meaning</span></span>                                                                                                                               |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4fe96-195"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4fe96-195"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="4fe96-196">*inizio* o *conteggio* è un numero intero non valido.</span><span class="sxs-lookup"><span data-stu-id="4fe96-196">*start* or *count* was an invalid integer.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="4fe96-197"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4fe96-197"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="4fe96-198">la *destinazione*, il *formato* o il *tipo* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="4fe96-198">*target*, *format*,or *type* was not an accepted value.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="4fe96-199"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4fe96-199"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="4fe96-200">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="4fe96-200">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="4fe96-201">Commenti</span><span class="sxs-lookup"><span data-stu-id="4fe96-201">Remarks</span></span>

<span data-ttu-id="4fe96-202">La funzione **glColorSubTableEXT** specifica parti della tavolozza della trama di destinazione corrente da sostituire.</span><span class="sxs-lookup"><span data-stu-id="4fe96-202">The **glColorSubTableEXT** function specifies portions of the current targeted texture's palette to be replaced.</span></span> <span data-ttu-id="4fe96-203">A differenza di [**glColorTableEXT**](glcolortableext.md), non è possibile specificare il parametro di *destinazione* come tavolozza di trama del proxy.</span><span class="sxs-lookup"><span data-stu-id="4fe96-203">Unlike [**glColorTableEXT**](glcolortableext.md), you cannot specify the *target* parameter to be a proxy texture palette.</span></span>

> [!Note]  
> <span data-ttu-id="4fe96-204">La funzione **glColorSubTableEXT** è una funzione di estensione che non fa parte della libreria OpenGL standard, ma fa parte dell'estensione di trama di GL \_ ext con \_ tavolozza \_ .</span><span class="sxs-lookup"><span data-stu-id="4fe96-204">The **glColorSubTableEXT** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="4fe96-205">Per verificare se l'implementazione di OpenGL supporta **glColorSubTableEXT**, chiamare [**glGetString**](glgetstring.md)(GL \_ Extensions).</span><span class="sxs-lookup"><span data-stu-id="4fe96-205">To check whether your implementation of OpenGL supports **glColorSubTableEXT**, call [**glGetString**](glgetstring.md)(GL\_EXTENSIONS).</span></span> <span data-ttu-id="4fe96-206">Se restituisce \_ \_ la trama della tavolozza GL ext \_ , **glColorSubTableEXT** è supportato.</span><span class="sxs-lookup"><span data-stu-id="4fe96-206">If it returns GL\_EXT\_paletted\_texture, **glColorSubTableEXT** is supported.</span></span> <span data-ttu-id="4fe96-207">Per ottenere l'indirizzo della funzione di una funzione di estensione, chiamare [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span><span class="sxs-lookup"><span data-stu-id="4fe96-207">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4fe96-208">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4fe96-208">Requirements</span></span>



| <span data-ttu-id="4fe96-209">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fe96-209">Requirement</span></span> | <span data-ttu-id="4fe96-210">Valore</span><span class="sxs-lookup"><span data-stu-id="4fe96-210">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="4fe96-211">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4fe96-211">Minimum supported client</span></span><br/> | <span data-ttu-id="4fe96-212">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4fe96-212">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="4fe96-213">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4fe96-213">Minimum supported server</span></span><br/> | <span data-ttu-id="4fe96-214">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4fe96-214">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4fe96-215">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4fe96-215">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fe96-216"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fe96-216"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fe96-217">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4fe96-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fe96-218">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4fe96-218">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4fe96-219">**glColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="4fe96-219">**glColorTableEXT**</span></span>](glcolortableext.md)
</dt> <dt>

[<span data-ttu-id="4fe96-220">**Remo**</span><span class="sxs-lookup"><span data-stu-id="4fe96-220">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4fe96-221">**glGetColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="4fe96-221">**glGetColorTableEXT**</span></span>](glgetcolortableext.md)
</dt> <dt>

[<span data-ttu-id="4fe96-222">**glGetColorTableParameterfvEXT**</span><span class="sxs-lookup"><span data-stu-id="4fe96-222">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="4fe96-223">**glGetColorTableParameterivEXT**</span><span class="sxs-lookup"><span data-stu-id="4fe96-223">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="4fe96-224">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="4fe96-224">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="4fe96-225">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="4fe96-225">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





