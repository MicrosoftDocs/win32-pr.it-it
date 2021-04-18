---
title: funzione glGetColorTableEXT (GL. h)
description: La funzione glGetColorTableEXT ottiene i dati della tabella dei colori della tavolozza della trama di destinazione corrente.
ms.assetid: 9169c4e1-a22e-48fe-bd45-4549c1a10ff0
keywords:
- funzione glGetColorTableEXT OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 811dc53b32c937970fbef8d87fa9a2ef4eb8b978
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302761"
---
# <a name="glgetcolortableext-function"></a><span data-ttu-id="5e1ab-104">glGetColorTableEXT (funzione)</span><span class="sxs-lookup"><span data-stu-id="5e1ab-104">glGetColorTableEXT function</span></span>

<span data-ttu-id="5e1ab-105">La funzione **glGetColorTableEXT** ottiene i dati della tabella dei colori della tavolozza della trama di destinazione corrente.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-105">The **glGetColorTableEXT** function gets the color table data of the current targeted texture palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e1ab-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5e1ab-106">Syntax</span></span>


```C++
void WINAPI glGetColorTableEXT(
         GLenum target,
         GLenum format,
         GLenum type,
   const GLvoid *data
);
```



## <a name="parameters"></a><span data-ttu-id="5e1ab-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5e1ab-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e1ab-108">*target*</span><span class="sxs-lookup"><span data-stu-id="5e1ab-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="5e1ab-109">Trama di destinazione per la quale è stata modificata la tavolozza.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-109">The target texture that is to have its palette changed.</span></span> <span data-ttu-id="5e1ab-110">Deve essere una trama \_ 1D o trama \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-110">Must be TEXTURE\_1D or TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="5e1ab-111">*format*</span><span class="sxs-lookup"><span data-stu-id="5e1ab-111">*format*</span></span> 
</dt> <dd>

<span data-ttu-id="5e1ab-112">Formato dei dati pixel.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-112">The format of the pixel data.</span></span> <span data-ttu-id="5e1ab-113">Vengono accettate le seguenti costanti simboliche.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-113">The following symbolic constants are accepted.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5e1ab-114">Valore</span><span class="sxs-lookup"><span data-stu-id="5e1ab-114">Value</span></span></th>
<th><span data-ttu-id="5e1ab-115">Significato</span><span class="sxs-lookup"><span data-stu-id="5e1ab-115">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_RGBA"></span><span id="gl_rgba"></span><dl> <span data-ttu-id="5e1ab-116"><dt><strong>GL_RGBA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5e1ab-116"><dt><strong>GL_RGBA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5e1ab-117">Ogni pixel è un gruppo di quattro componenti nell'ordine seguente: rosso, verde, blu, alfa.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-117">Each pixel is a group of four components in the following order: red, green, blue, alpha.</span></span> <span data-ttu-id="5e1ab-118">Il formato RGBA viene determinato in questo modo:</span><span class="sxs-lookup"><span data-stu-id="5e1ab-118">The RGBA format is determined in this way:</span></span> <br/>
<ol>
<li><span data-ttu-id="5e1ab-119">La funzione <strong>glGetColorTableEXT</strong> converte i valori a virgola mobile direttamente in un formato interno con precisione non specificata.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-119">The <strong>glGetColorTableEXT</strong> function converts floating-point values directly to an internal format with unspecified precision.</span></span> <span data-ttu-id="5e1ab-120">Per i valori integer con segno viene eseguito il mapping lineare al formato interno, in modo che il valore integer rappresentabile più positivo sia mappato a 1,0 e che il valore integer rappresentabile più negativo sia mappato a-1,0.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-120">Signed integer values are mapped linearly to the internal format such that the most positive representable integer value maps to 1.0, and the most negative representable integer value maps to -1.0.</span></span> <span data-ttu-id="5e1ab-121">Viene eseguito il mapping dei dati integer senza segno in modo analogo: il valore integer più grande viene mappato a 1,0 e zero viene mappato a 0,0.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-121">Unsigned integer data is mapped similarly: the largest integer value maps to 1.0, and zero maps to 0.0.</span></span></li>
<li><span data-ttu-id="5e1ab-122">La funzione <strong>glGetColorTableEXT</strong> moltiplica i valori di colore risultanti per GL_c_SCALE e li aggiunge a GL_c_BIAS, dove <em>c</em> è rosso, verde, blu e alfa per i rispettivi componenti di colore.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-122">The <strong>glGetColorTableEXT</strong> function multiplies the resulting color values by GL_c_SCALE and adds them to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span> <span data-ttu-id="5e1ab-123">I risultati vengono fissati nell'intervallo [0, 1].</span><span class="sxs-lookup"><span data-stu-id="5e1ab-123">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="5e1ab-124">Se GL_MAP_COLOR è <strong>true</strong>, <strong>glGetColorTableEXT</strong> ridimensiona ogni componente del colore in base alla dimensione della tabella di ricerca GL_PIXEL_MAP_c_TO_c, quindi sostituisce il componente in base al valore a cui fa riferimento nella tabella. <em>c</em> è rispettivamente R, G, B o A.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-124">If GL_MAP_COLOR is <strong>TRUE</strong>, <strong>glGetColorTableEXT</strong> scales each color component by the size of lookup table GL_PIXEL_MAP_c_TO_c, then replaces the component by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span></li>
<li><span data-ttu-id="5e1ab-125">La funzione <strong>glGetColorTableEXT</strong> converte i colori RGBA risultanti in frammenti associando la posizione raster corrente della coordinata z e le coordinate di trama a ogni pixel, quindi assegnando le coordinate della finestra <em>x</em> e <em>y</em> al frammento <em>n</em>, ad esempio <em>x</em>?</span><span class="sxs-lookup"><span data-stu-id="5e1ab-125">The <strong>glGetColorTableEXT</strong> function converts the resulting RGBA colors to fragments by attaching the current raster position z-coordinate and texture coordinates to each pixel, then assigning <em>x</em> and <em>y</em> window coordinates to the <em>n</em>th fragment, such that <em>x</em>?</span></span><span data-ttu-id="5e1ab-126"> = <em>larghezza</em> <em>x</em><sub>r</sub> + <em>n</em> mod</span><span class="sxs-lookup"><span data-stu-id="5e1ab-126"> = <em>x</em><sub>r</sub> + <em>n</em> mod <em>width</em></span></span><br/> <span data-ttu-id="5e1ab-127"><em>y</em>?</span><span class="sxs-lookup"><span data-stu-id="5e1ab-127"><em>y</em>?</span></span><span data-ttu-id="5e1ab-128"> = <em>y</em><sub>r</sub> + <em>n/Larghezza</em></span><span class="sxs-lookup"><span data-stu-id="5e1ab-128"> = <em>y</em><sub>r</sub> + <em>n/width</em></span></span><br/> <span data-ttu-id="5e1ab-129">dove (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) è la posizione raster corrente.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-129">where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span><br/></li>
<li><span data-ttu-id="5e1ab-130">Questi frammenti di pixel vengono quindi trattati come i frammenti generati dalla rasterizzazione di punti, linee o poligoni.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-130">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="5e1ab-131">La funzione <strong>glGetColorTableEXT</strong> applica il mapping di trama, la nebbia e tutte le operazioni di frammento prima di scrivere i frammenti sul framebuffer.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-131">The <strong>glGetColorTableEXT</strong> function applies texture mapping, fog, and all the fragment operations before writing the fragments to the framebuffer.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_RED"></span><span id="gl_red"></span><dl> <span data-ttu-id="5e1ab-132"><dt><strong>GL_RED</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5e1ab-132"><dt><strong>GL_RED</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5e1ab-133">Ogni pixel è un singolo componente rosso.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-133">Each pixel is a single red component.</span></span><br/> <span data-ttu-id="5e1ab-134">La funzione <strong>glGetColorTableEXT</strong> converte il componente nel formato interno nello stesso modo in cui il componente rosso di un pixel RGBA è, quindi lo converte in un pixel RGBA con il verde e il blu impostati su 0,0 e Alpha impostato su 1,0.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-134">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the red component of an RGBA pixel is, then converts it to an RGBA pixel with green and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="5e1ab-135">Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-135">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_GREEN"></span><span id="gl_green"></span><dl> <span data-ttu-id="5e1ab-136"><dt><strong>GL_GREEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5e1ab-136"><dt><strong>GL_GREEN</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5e1ab-137">Ogni pixel è un singolo componente verde.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-137">Each pixel is a single green component.</span></span><br/> <span data-ttu-id="5e1ab-138">La funzione <strong>glGetColorTableEXT</strong> converte il componente nel formato interno nello stesso modo in cui il componente verde di un pixel RGBA è e quindi lo converte in un pixel RGBA con il rosso e il blu impostati su 0,0 e Alpha impostato su 1,0.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-138">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the green component of an RGBA pixel is, and then converts it to an RGBA pixel with red and blue set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="5e1ab-139">Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-139">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BLUE"></span><span id="gl_blue"></span><dl> <span data-ttu-id="5e1ab-140"><dt><strong>GL_BLUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5e1ab-140"><dt><strong>GL_BLUE</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5e1ab-141">Ogni pixel è un singolo componente blu.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-141">Each pixel is a single blue component.</span></span><br/> <span data-ttu-id="5e1ab-142">La funzione <strong>glGetColorTableEXT</strong> converte il componente nel formato interno nello stesso modo in cui il componente blu di un pixel RGBA è e quindi lo converte in un pixel RGBA con rosso e verde impostato su 0,0 e Alpha impostato su 1,0.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-142">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the blue component of an RGBA pixel is, and then converts it to an RGBA pixel with red and green set to 0.0, and alpha set to 1.0.</span></span> <span data-ttu-id="5e1ab-143">Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-143">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_ALPHA"></span><span id="gl_alpha"></span><dl> <span data-ttu-id="5e1ab-144"><dt><strong>GL_ALPHA</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5e1ab-144"><dt><strong>GL_ALPHA</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5e1ab-145">Ogni pixel è un singolo componente alfa.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-145">Each pixel is a single alpha component.</span></span><br/> <span data-ttu-id="5e1ab-146">La funzione <strong>glGetColorTableEXT</strong> converte il componente nel formato interno nello stesso modo in cui il componente alfa di un pixel RGBA è e quindi lo converte in un pixel RGBA con rosso, verde e blu impostato su 0,0.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-146">The <strong>glGetColorTableEXT</strong> function converts this component to the internal format in the same way that the alpha component of an RGBA pixel is, and then converts it to an RGBA pixel with red, green, and blue set to 0.0.</span></span> <span data-ttu-id="5e1ab-147">Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-147">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_RGB"></span><span id="gl_rgb"></span><dl> <span data-ttu-id="5e1ab-148"><dt><strong>GL_RGB</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5e1ab-148"><dt><strong>GL_RGB</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5e1ab-149">Ogni pixel è un gruppo di tre componenti in questo ordine: rosso, verde, blu.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-149">Each pixel is a group of three components in this order: red, green, blue.</span></span><br/> <span data-ttu-id="5e1ab-150">La funzione <strong>glGetColorTableEXT</strong> converte ogni componente nel formato interno nello stesso modo in cui i componenti rosso, verde e blu di un pixel RGBA sono.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-150">The <strong>glGetColorTableEXT</strong> function converts each component to the internal format in the same way that the red, green, and blue components of an RGBA pixel are.</span></span> <span data-ttu-id="5e1ab-151">Il colore triple viene convertito in un pixel RGBA con Alpha impostato su 1,0.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-151">The color triple is converted to an RGBA pixel with alpha set to 1.0.</span></span> <span data-ttu-id="5e1ab-152">Dopo questa conversione, il pixel viene considerato come se fosse stato letto come pixel RGBA.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-152">After this conversion, the pixel is treated just as if it had been read as an RGBA pixel.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_BGR_EXT"></span><span id="gl_bgr_ext"></span><dl> <span data-ttu-id="5e1ab-153"><dt><strong>GL_BGR_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5e1ab-153"><dt><strong>GL_BGR_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5e1ab-154">Ogni pixel è un gruppo di tre componenti in questo ordine: blu, verde, rosso.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-154">Each pixel is a group of three components in this order: blue, green, red.</span></span><br/> <span data-ttu-id="5e1ab-155">GL_BGR_EXT fornisce un formato corrispondente al layout di memoria delle bitmap (DIB) indipendenti dal dispositivo di Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-155">GL_BGR_EXT provides a format that matches the memory layout of Microsoft Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="5e1ab-156">Quindi, le applicazioni possono usare gli stessi dati con le chiamate di funzione di Windows e le chiamate di funzione pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-156">Thus, your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="GL_BGRA_EXT"></span><span id="gl_bgra_ext"></span><dl> <span data-ttu-id="5e1ab-157"><dt><strong>GL_BGRA_EXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="5e1ab-157"><dt><strong>GL_BGRA_EXT</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="5e1ab-158">Ogni pixel è un gruppo di quattro componenti in questo ordine: blu, verde, rosso, alfa.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-158">Each pixel is a group of four components in this order: blue, green, red, alpha.</span></span><br/> <span data-ttu-id="5e1ab-159">GL_BGRA_EXT fornisce un formato corrispondente al layout di memoria delle bitmap indipendenti dal dispositivo (DIB) Windows.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-159">GL_BGRA_EXT provides a format that matches the memory layout of Windows device-independent bitmaps (DIBs).</span></span> <span data-ttu-id="5e1ab-160">In questo modo, le applicazioni possono usare gli stessi dati con le chiamate di funzione di Windows e le chiamate di funzione pixel OpenGL.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-160">Thus your applications can use the same data with Windows function calls and OpenGL pixel function calls.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="5e1ab-161">*type*</span><span class="sxs-lookup"><span data-stu-id="5e1ab-161">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="5e1ab-162">Tipo di dati per i *dati*.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-162">The data type for *data*.</span></span> <span data-ttu-id="5e1ab-163">Di seguito sono riportate le costanti simboliche accettate e i relativi significati.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-163">The following are the accepted symbolic constants and their meanings.</span></span>



| <span data-ttu-id="5e1ab-164">Valore</span><span class="sxs-lookup"><span data-stu-id="5e1ab-164">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="5e1ab-165">Significato</span><span class="sxs-lookup"><span data-stu-id="5e1ab-165">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="5e1ab-166"><dt>**\_byte senza segno GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5e1ab-166"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="5e1ab-167">Intero senza segno a 8 bit</span><span class="sxs-lookup"><span data-stu-id="5e1ab-167">Unsigned 8-bit integer</span></span><br/>                |
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="5e1ab-168"><dt>**\_byte GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5e1ab-168"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="5e1ab-169">Valore intero con segno a 8 bit</span><span class="sxs-lookup"><span data-stu-id="5e1ab-169">Signed 8-bit integer</span></span><br/>                  |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="5e1ab-170"><dt>**\_short senza segno GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5e1ab-170"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="5e1ab-171">Intero senza segno a 16 bit</span><span class="sxs-lookup"><span data-stu-id="5e1ab-171">Unsigned 16-bit integer</span></span><br/>               |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="5e1ab-172"><dt>**\_short GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5e1ab-172"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="5e1ab-173">Valore intero a 16 bit con segno</span><span class="sxs-lookup"><span data-stu-id="5e1ab-173">Signed 16-bit integer</span></span><br/>                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="5e1ab-174"><dt>**GL \_ senza segno \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="5e1ab-174"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="5e1ab-175">Intero senza segno a 32 bit</span><span class="sxs-lookup"><span data-stu-id="5e1ab-175">Unsigned 32-bit integer</span></span><br/>               |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="5e1ab-176"><dt>**GL \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="5e1ab-176"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="5e1ab-177">Intero a 32 bit</span><span class="sxs-lookup"><span data-stu-id="5e1ab-177">32-bit integer</span></span><br/>                        |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="5e1ab-178"><dt>**GL \_ float**</dt></span><span class="sxs-lookup"><span data-stu-id="5e1ab-178"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="5e1ab-179">Valore a virgola mobile e precisione singola</span><span class="sxs-lookup"><span data-stu-id="5e1ab-179">Single-precision floating-point value</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5e1ab-180">*data*</span><span class="sxs-lookup"><span data-stu-id="5e1ab-180">*data*</span></span> 
</dt> <dd>

<span data-ttu-id="5e1ab-181">Punta alla posizione in cui devono essere archiviate le informazioni sulla tabella dei colori restituite.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-181">Points to the location where returned color table information is to be stored.</span></span> <span data-ttu-id="5e1ab-182">Ogni voce della tabella dei colori viene archiviata come se fosse un singolo pixel di una trama da 1 a D.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-182">Each color table entry is stored as if it was a single pixel of a 1-D texture.</span></span> <span data-ttu-id="5e1ab-183">Poiché tutte le trame hanno una tavolozza predefinita, **glGetColorTableEXT** restituisce sempre le informazioni della tavolozza anche se i dati della trama non sono in un formato con tavolozza.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-183">Because all textures have a default palette, **glGetColorTableEXT** always returns palette information even if the texture data is not in a paletted format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e1ab-184">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5e1ab-184">Return value</span></span>

<span data-ttu-id="5e1ab-185">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-185">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5e1ab-186">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="5e1ab-186">Error codes</span></span>

<span data-ttu-id="5e1ab-187">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="5e1ab-187">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5e1ab-188">Nome</span><span class="sxs-lookup"><span data-stu-id="5e1ab-188">Name</span></span>                                                                                                  | <span data-ttu-id="5e1ab-189">Significato</span><span class="sxs-lookup"><span data-stu-id="5e1ab-189">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5e1ab-190"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5e1ab-190"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="5e1ab-191">la *destinazione*, il *formato* o il *tipo* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-191">*target*, *format*, or *type* was not an accepted value.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="5e1ab-192"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5e1ab-192"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5e1ab-193">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="5e1ab-193">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5e1ab-194">Commenti</span><span class="sxs-lookup"><span data-stu-id="5e1ab-194">Remarks</span></span>

<span data-ttu-id="5e1ab-195">La funzione **glGetColorTableEXT** ottiene i dati effettivi della tabella dei colori specificati da [**glColorTableEXT**](glcolortableext.md) e [**glColorSubTableEXT**](glcolorsubtableext.md).</span><span class="sxs-lookup"><span data-stu-id="5e1ab-195">The **glGetColorTableEXT** function gets the actual color table data specified by [**glColorTableEXT**](glcolortableext.md) and [**glColorSubTableEXT**](glcolorsubtableext.md).</span></span>

<span data-ttu-id="5e1ab-196">La funzione **glGetColorTableEXT** è una funzione di estensione che non fa parte della libreria OpenGL standard, ma fa parte dell'estensione di trama di GL \_ ext con \_ tavolozza \_ .</span><span class="sxs-lookup"><span data-stu-id="5e1ab-196">The **glGetColorTableEXT** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="5e1ab-197">Per verificare se l'implementazione di OpenGL supporta **glGetColorTableEXT**, chiamare [**glGetString**](glgetstring.md)(GL \_ Extensions).</span><span class="sxs-lookup"><span data-stu-id="5e1ab-197">To check whether your implementation of OpenGL supports **glGetColorTableEXT**, call [**glGetString**](glgetstring.md)(GL\_EXTENSIONS).</span></span> <span data-ttu-id="5e1ab-198">Se restituisce \_ \_ la trama della tavolozza GL ext \_ , **glGetColorTableEXT** è supportato.</span><span class="sxs-lookup"><span data-stu-id="5e1ab-198">If it returns GL\_EXT\_paletted\_texture, **glGetColorTableEXT** is supported.</span></span> <span data-ttu-id="5e1ab-199">Per ottenere l'indirizzo della funzione di una funzione di estensione, chiamare [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span><span class="sxs-lookup"><span data-stu-id="5e1ab-199">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e1ab-200">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5e1ab-200">Requirements</span></span>



| <span data-ttu-id="5e1ab-201">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e1ab-201">Requirement</span></span> | <span data-ttu-id="5e1ab-202">Valore</span><span class="sxs-lookup"><span data-stu-id="5e1ab-202">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="5e1ab-203">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e1ab-203">Minimum supported client</span></span><br/> | <span data-ttu-id="5e1ab-204">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5e1ab-204">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="5e1ab-205">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5e1ab-205">Minimum supported server</span></span><br/> | <span data-ttu-id="5e1ab-206">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5e1ab-206">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5e1ab-207">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5e1ab-207">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e1ab-208"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e1ab-208"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e1ab-209">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5e1ab-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e1ab-210">**glColorSubTableEXT**</span><span class="sxs-lookup"><span data-stu-id="5e1ab-210">**glColorSubTableEXT**</span></span>](glcolorsubtableext.md)
</dt> <dt>

[<span data-ttu-id="5e1ab-211">**glColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="5e1ab-211">**glColorTableEXT**</span></span>](glcolortableext.md)
</dt> <dt>

[<span data-ttu-id="5e1ab-212">**glGetColorTableParameterfvEXT**</span><span class="sxs-lookup"><span data-stu-id="5e1ab-212">**glGetColorTableParameterfvEXT**</span></span>](glgetcolortableparameterfvext.md)
</dt> <dt>

[<span data-ttu-id="5e1ab-213">**glGetColorTableParameterivEXT**</span><span class="sxs-lookup"><span data-stu-id="5e1ab-213">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="5e1ab-214">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="5e1ab-214">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





