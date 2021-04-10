---
title: funzione glCopyPixels (GL. h)
description: La funzione glCopyPixels copia i pixel nel framebuffer.
ms.assetid: c4055928-7b8b-4d0f-94f3-e3b9c0503308
keywords:
- funzione glCopyPixels OpenGL
topic_type:
- apiref
api_name:
- glCopyPixels
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7ba0833534d21e48c251da6491fee2996c3ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964354"
---
# <a name="glcopypixels-function"></a><span data-ttu-id="fa0b9-104">glCopyPixels (funzione)</span><span class="sxs-lookup"><span data-stu-id="fa0b9-104">glCopyPixels function</span></span>

<span data-ttu-id="fa0b9-105">La funzione **glCopyPixels** copia i pixel nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-105">The **glCopyPixels** function copies pixels in the framebuffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa0b9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa0b9-106">Syntax</span></span>


```C++
void WINAPI glCopyPixels(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height,
   GLenum  type
);
```



## <a name="parameters"></a><span data-ttu-id="fa0b9-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="fa0b9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa0b9-108">*x*</span><span class="sxs-lookup"><span data-stu-id="fa0b9-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="fa0b9-109">Coordinata del piano x della finestra dell'angolo inferiore sinistro dell'area rettangolare dei pixel da copiare.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-109">The window x-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b9-110">*y*</span><span class="sxs-lookup"><span data-stu-id="fa0b9-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="fa0b9-111">Coordinata del piano y della finestra dell'angolo inferiore sinistro dell'area rettangolare dei pixel da copiare.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-111">The window y-plane coordinate of the lower-left corner of the rectangular region of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b9-112">*width*</span><span class="sxs-lookup"><span data-stu-id="fa0b9-112">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="fa0b9-113">Dimensione della larghezza dell'area rettangolare dei pixel da copiare.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-113">The width dimension of the rectangular region of pixels to be copied.</span></span> <span data-ttu-id="fa0b9-114">Deve essere non negativo.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-114">Must be nonnegative.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b9-115">*height*</span><span class="sxs-lookup"><span data-stu-id="fa0b9-115">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="fa0b9-116">Dimensione dell'altezza dell'area rettangolare dei pixel da copiare.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-116">The height dimension of the rectangular region of pixels to be copied.</span></span> <span data-ttu-id="fa0b9-117">Deve essere non negativo.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-117">Must be nonnegative.</span></span>

</dd> <dt>

<span data-ttu-id="fa0b9-118">*type*</span><span class="sxs-lookup"><span data-stu-id="fa0b9-118">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="fa0b9-119">Specifica se **glCopyPixels** consiste nel copiare i valori dei colori, i valori di profondità o i valori dello stencil.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-119">Specifies whether **glCopyPixels** is to copy color values, depth values, or stencil values.</span></span> <span data-ttu-id="fa0b9-120">Le costanti simboliche accettabili sono.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-120">The acceptable symbolic constants are.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fa0b9-121">Valore</span><span class="sxs-lookup"><span data-stu-id="fa0b9-121">Value</span></span></th>
<th><span data-ttu-id="fa0b9-122">Significato</span><span class="sxs-lookup"><span data-stu-id="fa0b9-122">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="GL_COLOR"></span><span id="gl_color"></span><dl> <span data-ttu-id="fa0b9-123"><dt><strong>GL_COLOR</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fa0b9-123"><dt><strong>GL_COLOR</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="fa0b9-124">La funzione <strong>glCopyPixels</strong> legge gli indici o i colori RGBA dal buffer attualmente specificato come buffer di origine di lettura (vedere <a href="glreadbuffer.md"><strong>glReadBuffer</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="fa0b9-124">The <strong>glCopyPixels</strong> function reads indexes or RGBA colors from the buffer currently specified as the read source buffer (see <a href="glreadbuffer.md"><strong>glReadBuffer</strong></a>).</span></span> <br/> <span data-ttu-id="fa0b9-125">Se OpenGL è in modalità di indice a colori:</span><span class="sxs-lookup"><span data-stu-id="fa0b9-125">If OpenGL is in color-index mode:</span></span><br/>
<ol>
<li><span data-ttu-id="fa0b9-126">Ogni indice letto da questo buffer viene convertito in un formato a virgola fissa con un numero di bit non specificato a destra del punto binario.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-126">Each index that is read from this buffer is converted to a fixed-point format with an unspecified number of bits to the right of the binary point.</span></span></li>
<li><span data-ttu-id="fa0b9-127">Ogni indice viene spostato a sinistra di GL_INDEX_SHIFT bit e aggiunto al GL_INDEX_OFFSET. Se GL_INDEX_SHIFT è negativo, lo spostamento è a destra.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-127">Each index is shifted left by GL_INDEX_SHIFT bits, and added to GL_INDEX_OFFSET.If GL_INDEX_SHIFT is negative, the shift is to the right.</span></span> <span data-ttu-id="fa0b9-128">In entrambi i casi, i bit a zero riempiono i percorsi di bit non specificati nel risultato.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-128">In either case, zero bits fill otherwise unspecified bit locations in the result.</span></span><br/></li>
<li><span data-ttu-id="fa0b9-129">Se GL_MAP_COLOR è true, l'indice viene sostituito con il valore a cui fa riferimento nella tabella di ricerca GL_PIXEL_MAP_I_TO_I.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-129">If GL_MAP_COLOR is true, the index is replaced with the value that it references in lookup table GL_PIXEL_MAP_I_TO_I.</span></span></li>
<li><span data-ttu-id="fa0b9-130">Se la sostituzione della ricerca dell'indice viene eseguita o meno, la parte intera dell'indice è quindi <strong>e</strong>ed è con 2<em><sup>b</sup></em> 1, dove <em>b</em> è il numero di bit in un buffer di indice dei colori.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-130">Whether the lookup replacement of the index is done or not, the integer part of the index is then <strong>AND</strong>ed with 2<em><sup>b</sup></em> 1, where <em>b</em> is the number of bits in a color-index buffer.</span></span></li>
</ol>
<span data-ttu-id="fa0b9-131">Se OpenGL è in modalità RGBA:</span><span class="sxs-lookup"><span data-stu-id="fa0b9-131">If OpenGL is in RGBA mode:</span></span><br/>
<ol>
<li><span data-ttu-id="fa0b9-132">I componenti rosso, verde, blu e alfa di ogni pixel letti vengono convertiti in un formato a virgola mobile interno con precisione non specificata.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-132">The red, green, blue, and alpha components of each pixel that is read are converted to an internal floating-point format with unspecified precision.</span></span></li>
<li><span data-ttu-id="fa0b9-133">La conversione esegue il mapping del valore del componente rappresentabile più grande a 1,0 e il valore del componente zero a 0,0.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-133">The conversion maps the largest representable component value to 1.0, and component value zero to 0.0.</span></span></li>
<li><span data-ttu-id="fa0b9-134">I valori dei colori a virgola mobile risultanti vengono moltiplicati per GL_c_SCALE e aggiunti a GL_c_BIAS, dove <em>c</em> è rosso, verde, blu e alfa per i rispettivi componenti colore.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-134">The resulting floating-point color values are then multiplied by GL_c_SCALE and added to GL_c_BIAS, where <em>c</em> is RED, GREEN, BLUE, and ALPHA for the respective color components.</span></span></li>
<li><span data-ttu-id="fa0b9-135">I risultati vengono fissati nell'intervallo [0, 1].</span><span class="sxs-lookup"><span data-stu-id="fa0b9-135">The results are clamped to the range [0,1].</span></span></li>
<li><span data-ttu-id="fa0b9-136">Se GL_MAP_COLOR è true, ogni componente colore viene ridimensionato in base alle dimensioni della tabella di ricerca GL_PIXEL_MAP_c_TO_c e quindi sostituito dal valore a cui fa riferimento nella tabella. <em>c</em> è rispettivamente R, G, B o A.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-136">If GL_MAP_COLOR is true, each color component is scaled by the size of lookup table GL_PIXEL_MAP_c_TO_c, and then replaced by the value that it references in that table; <em>c</em> is R, G, B, or A, respectively.</span></span> <span data-ttu-id="fa0b9-137">Gli indici o i colori RGBA risultanti vengono quindi convertiti in frammenti associando <em>la posizione raster</em>corrente e le coordinate della trama a ogni pixel, quindi assegnando le coordinate della finestra (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), dove (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) è la posizione raster corrente e il pixel è il pixel nella posizione <em>i</em> nella riga <em>j</em> .</span><span class="sxs-lookup"><span data-stu-id="fa0b9-137">The resulting indexes or RGBA colors are then converted to fragments by attaching the current raster position <em>z</em>-coordinate and texture coordinates to each pixel, and then assigning window coordinates (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position, and the pixel was the pixel in the <em>i</em> position in the <em>j</em> row.</span></span> <span data-ttu-id="fa0b9-138">Questi frammenti di pixel vengono quindi trattati come i frammenti generati dalla rasterizzazione di punti, linee o poligoni.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-138">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="fa0b9-139">Il mapping di trama, la nebbia e tutte le operazioni di frammento vengono applicati prima che i frammenti vengano scritti nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-139">Texture mapping, fog, and all the fragment operations are applied before the fragments are written to the framebuffer.</span></span><br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span id="GL_DEPTH"></span><span id="gl_depth"></span><dl> <span data-ttu-id="fa0b9-140"><dt><strong>GL_DEPTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fa0b9-140"><dt><strong>GL_DEPTH</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="fa0b9-141">I valori di profondità vengono letti dal buffer di profondità e vengono convertiti direttamente in un formato a virgola mobile interno con precisione non specificata.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-141">Depth values are read from the depth buffer and converted directly to an internal floating-point format with unspecified precision.</span></span> <span data-ttu-id="fa0b9-142">Il valore di profondità a virgola mobile risultante viene moltiplicato per GL_DEPTH_SCALE e aggiunto al GL_DEPTH_BIAS.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-142">The resulting floating-point depth value is then multiplied by GL_DEPTH_SCALE and added to GL_DEPTH_BIAS.</span></span> <span data-ttu-id="fa0b9-143">Il risultato viene bloccato nell'intervallo [0, 1].</span><span class="sxs-lookup"><span data-stu-id="fa0b9-143">The result is clamped to the range [0,1].</span></span> <br/> <span data-ttu-id="fa0b9-144">I componenti di profondità risultanti vengono quindi convertiti in frammenti associando il colore della posizione raster corrente o l'indice dei colori e le coordinate di trama a ogni pixel, assegnando quindi le coordinate della finestra (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), dove (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) è la posizione raster corrente e il pixel è il pixel nella posizione <em>i</em> nella riga <em>j</em> .</span><span class="sxs-lookup"><span data-stu-id="fa0b9-144">The resulting depth components are then converted to fragments by attaching the current raster position color or color index and texture coordinates to each pixel, then assigning window coordinates (<em>x</em><sub>r</sub> + i, <em>y</em><sub>r</sub> + <em>j</em>), where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position, and the pixel was the pixel in the <em>i</em> position in the <em>j</em> row.</span></span> <span data-ttu-id="fa0b9-145">Questi frammenti di pixel vengono quindi trattati come i frammenti generati dalla rasterizzazione di punti, linee o poligoni.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-145">These pixel fragments are then treated just like the fragments generated by rasterizing points, lines, or polygons.</span></span> <span data-ttu-id="fa0b9-146">Il mapping di trama, la nebbia e tutte le operazioni di frammento vengono applicati prima che i frammenti vengano scritti nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-146">Texture mapping, fog, and all the fragment operations are applied before the fragments are written to the framebuffer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="GL_STENCIL"></span><span id="gl_stencil"></span><dl> <span data-ttu-id="fa0b9-147"><dt><strong>GL_STENCIL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="fa0b9-147"><dt><strong>GL_STENCIL</strong></dt> </span></span></dl></td>
<td><span data-ttu-id="fa0b9-148">Gli indici degli stencil vengono letti dal buffer dello stencil e convertiti in un formato a virgola fissa interno con un numero di bit non specificato a destra del punto binario.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-148">Stencil indexes are read from the stencil buffer and converted to an internal fixed-point format with an unspecified number of bits to the right of the binary point.</span></span> <span data-ttu-id="fa0b9-149">Ogni indice a virgola fissa viene quindi spostato a sinistra di GL_INDEX_SHIFT bit e aggiunto al GL_INDEX_OFFSET.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-149">Each fixed-point index is then shifted left by GL_INDEX_SHIFT bits, and added to GL_INDEX_OFFSET.</span></span> <span data-ttu-id="fa0b9-150">Se GL_INDEX_SHIFT è negativo, lo spostamento è a destra.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-150">If GL_INDEX_SHIFT is negative, the shift is to the right.</span></span> <span data-ttu-id="fa0b9-151">In entrambi i casi, i bit a zero riempiono i percorsi di bit non specificati nel risultato.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-151">In either case, zero bits fill otherwise unspecified bit locations in the result.</span></span> <span data-ttu-id="fa0b9-152">Se GL_MAP_STENCIL è true, l'indice viene sostituito con il valore a cui fa riferimento nella tabella di ricerca GL_PIXEL_MAP_S_TO_S.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-152">If GL_MAP_STENCIL is true, the index is replaced with the value that it references in lookup table GL_PIXEL_MAP_S_TO_S.</span></span> <span data-ttu-id="fa0b9-153">Se la sostituzione della ricerca dell'indice viene eseguita o meno, la parte integer dell'indice è quindi <strong>e</strong>ed è con 2<sup>b</sup> - 1, dove <em>b</em> è il numero di bit nel buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-153">Whether the lookup replacement of the index is done or not, the integer part of the index is then <strong>AND</strong>ed with 2<sup>b</sup> - 1, where <em>b</em> is the number of bits in the stencil buffer.</span></span> <span data-ttu-id="fa0b9-154">Gli indici stencil risultanti vengono quindi scritti nel buffer dello stencil in modo tale che l'indice letto dalla posizione <em>i</em> della riga <em>j</em> venga scritto in location (<em>x</em><sub>r</sub> + <em>i</em>, <em>y</em><sub>r</sub> + <em>j</em>), dove (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) è la posizione raster corrente.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-154">The resulting stencil indexes are then written to the stencil buffer such that the index read from the <em>i</em> location of the <em>j</em> row is written to location (<em>x</em><sub>r</sub> + <em>i</em>, <em>y</em><sub>r</sub> + <em>j</em>), where (<em>x</em><sub>r</sub> , <em>y</em><sub>r</sub> ) is the current raster position.</span></span> <span data-ttu-id="fa0b9-155">Solo il test di proprietà dei pixel, il test a forbice e lo stencil writemask influiscono su queste Scritture.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-155">Only the pixel-ownership test, the scissor test, and the stencil writemask affect these writes.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa0b9-156">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fa0b9-156">Return value</span></span>

<span data-ttu-id="fa0b9-157">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-157">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fa0b9-158">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="fa0b9-158">Error codes</span></span>

<span data-ttu-id="fa0b9-159">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="fa0b9-159">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="fa0b9-160">Nome</span><span class="sxs-lookup"><span data-stu-id="fa0b9-160">Name</span></span>                                                                                                  | <span data-ttu-id="fa0b9-161">Significato</span><span class="sxs-lookup"><span data-stu-id="fa0b9-161">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fa0b9-162"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fa0b9-162"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="fa0b9-163">il *tipo* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-163">*type* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="fa0b9-164"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fa0b9-164"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="fa0b9-165">La *larghezza* o l'altezza è negativa.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-165">Either *width* or height was negative.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="fa0b9-166"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fa0b9-166"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fa0b9-167">il *tipo* è la \_ profondità GL e non è presente alcun buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-167">*type* was GL\_DEPTH and there was no depth buffer.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="fa0b9-168"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fa0b9-168"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fa0b9-169">il *tipo* è lo \_ stencil GL e non è presente alcun buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-169">*type* was GL\_STENCIL and there was no stencil buffer.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="fa0b9-170"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="fa0b9-170"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="fa0b9-171">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="fa0b9-171">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="fa0b9-172">Commenti</span><span class="sxs-lookup"><span data-stu-id="fa0b9-172">Remarks</span></span>

<span data-ttu-id="fa0b9-173">La funzione **glCopyPixels** copia un rettangolo di pixel allineato a schermo dalla posizione del framebuffer specificata in un'area relativa alla posizione raster corrente.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-173">The **glCopyPixels** function copies a screen-aligned rectangle of pixels from the specified framebuffer location to a region relative to the current raster position.</span></span> <span data-ttu-id="fa0b9-174">L'operazione è definita correttamente solo se l'intera area di origine pixel si trova all'interno della parte esposta della finestra.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-174">Its operation is well defined only if the entire pixel source region is within the exposed portion of the window.</span></span> <span data-ttu-id="fa0b9-175">I risultati delle copie dall'esterno della finestra o dalle aree della finestra che non sono esposte sono dipendenti dall'hardware e non definiti.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-175">Results of copies from outside the window, or from regions of the window that are not exposed, are hardware dependent and undefined.</span></span>

<span data-ttu-id="fa0b9-176">I parametri *x* e *y* specificano le coordinate della finestra dell'angolo inferiore sinistro dell'area rettangolare da copiare.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-176">The *x* and *y* parameters specify the window coordinates of the lower-left corner of the rectangular region to be copied.</span></span> <span data-ttu-id="fa0b9-177">I parametri *Width* e *Height* specificano le dimensioni dell'area rettangolare da copiare.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-177">The *width* and *height* parameters specify the dimensions of the rectangular region to be copied.</span></span> <span data-ttu-id="fa0b9-178">La *larghezza* e l' *altezza* non devono essere negative.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-178">Both *width* and *height* must be nonnegative.</span></span>

<span data-ttu-id="fa0b9-179">Diversi parametri controllano l'elaborazione dei dati pixel durante la copia.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-179">Several parameters control the processing of the pixel data while it is being copied.</span></span> <span data-ttu-id="fa0b9-180">Questi parametri vengono impostati con tre funzioni: [**glPixelTransfer**](glpixeltransfer.md), [**glPixelMap**](glpixelmap.md)e [**glPixelZoom**](glpixelzoom.md).</span><span class="sxs-lookup"><span data-stu-id="fa0b9-180">These parameters are set with three functions: [**glPixelTransfer**](glpixeltransfer.md), [**glPixelMap**](glpixelmap.md), and [**glPixelZoom**](glpixelzoom.md).</span></span> <span data-ttu-id="fa0b9-181">In questo argomento vengono descritti gli effetti sui **glCopyPixels** della maggior parte, ma non tutti, dei parametri specificati da queste tre funzioni.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-181">This topic describes the effects on **glCopyPixels** of most, but not all, of the parameters specified by these three functions.</span></span>

<span data-ttu-id="fa0b9-182">La funzione **glCopyPixels** copia i valori da ogni pixel con l'angolo inferiore sinistro in corrispondenza di (*x*  +  *i*, *y*  +  *j*) per 0 = *i*  <  *larghezza* e 0 = *j*  <  *altezza*.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-182">The **glCopyPixels** function copies values from each pixel with the lower-left corner at (*x* + *i*, *y* + *j*) for 0 = *i* < *width* and 0 = *j* < *height*.</span></span> <span data-ttu-id="fa0b9-183">Questo pixel viene *definito il pixel i nella* riga *j* .</span><span class="sxs-lookup"><span data-stu-id="fa0b9-183">This pixel is said to be the *i* pixel in the *j* row.</span></span> <span data-ttu-id="fa0b9-184">I pixel vengono copiati nell'ordine delle righe dalla riga più bassa alla riga più alta, da sinistra a destra in ogni riga.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-184">Pixels are copied in row order from the lowest to the highest row, left to right in each row.</span></span>

<span data-ttu-id="fa0b9-185">Il parametro di *tipo* specifica se i dati relativi al colore, alla profondità o allo stencil devono essere copiati.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-185">The *type* parameter specifies whether color, depth, or stencil data is to be copied.</span></span>

<span data-ttu-id="fa0b9-186">La rasterizzazione descritta fino a questo punto presuppone i fattori di zoom pixel di 1,0.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-186">The rasterization described thus far assumes pixel zoom factors of 1.0.</span></span> <span data-ttu-id="fa0b9-187">Se si usa [**glPixelZoom**](glpixelzoom.md) per modificare i fattori di zoom *x* e *y* pixel, i pixel vengono convertiti in frammenti come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-187">If you use [**glPixelZoom**](glpixelzoom.md) to change the *x* and *y* pixel zoom factors, pixels are converted to fragments as follows.</span></span> <span data-ttu-id="fa0b9-188">Se (*x*<sub>r</sub> , *y*<sub>r</sub> ) è la posizione raster corrente e un pixel specificato si trova nella posizione *i* nella riga *j* del rettangolo pixel di origine, vengono generati frammenti per i pixel i cui centri si trovano nel rettangolo con gli angoli</span><span class="sxs-lookup"><span data-stu-id="fa0b9-188">If (*x*<sub>r</sub> , *y*<sub>r</sub> ) is the current raster position, and a given pixel is in the *i* location in the *j* row of the source pixel rectangle, then fragments are generated for pixels whose centers are in the rectangle with corners at</span></span>

<span data-ttu-id="fa0b9-189">(*x*<sub>r</sub>  +  *Zoom*? i, y <sub>r</sub>  +  *Zoom*<sub>y</sub> *j*)</span><span class="sxs-lookup"><span data-stu-id="fa0b9-189">(*x*<sub>r</sub> + *zoom*? i, y <sub>r</sub> + *zoom*<sub>y</sub> *j*)</span></span>

<span data-ttu-id="fa0b9-190">e</span><span class="sxs-lookup"><span data-stu-id="fa0b9-190">and</span></span>

<span data-ttu-id="fa0b9-191">(*x*<sub>r</sub>  +  *Zoom*?</span><span class="sxs-lookup"><span data-stu-id="fa0b9-191">(*x*<sub>r</sub> + *zoom*?</span></span> <span data-ttu-id="fa0b9-192">(*i* + 1), *y*<sub>r</sub>  +  *Zoom*<sub>y</sub> (*j* + 1))</span><span class="sxs-lookup"><span data-stu-id="fa0b9-192">(*i* + 1), *y*<sub>r</sub> + *zoom*<sub>y</sub> (*j* + 1))</span></span>

<span data-ttu-id="fa0b9-193">dove *Zoom*? è il valore di GL \_ Zoom \_ X e *Zoom*<sub>y</sub> è il valore di GL \_ Zoom \_ y.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-193">where *zoom*? is the value of GL\_ZOOM\_X and *zoom*<sub>y</sub> is the value of GL\_ZOOM\_Y.</span></span>

<span data-ttu-id="fa0b9-194">Le modalità specificate da [**glPixelStore**](glpixelstore-functions.md) non hanno effetto sull'operazione di **glCopyPixels**.</span><span class="sxs-lookup"><span data-stu-id="fa0b9-194">Modes specified by [**glPixelStore**](glpixelstore-functions.md) have no effect on the operation of **glCopyPixels**.</span></span>

<span data-ttu-id="fa0b9-195">Le funzioni seguenti consentono di recuperare informazioni correlate a **glCopyPixels**:</span><span class="sxs-lookup"><span data-stu-id="fa0b9-195">The following functions retrieve information related to **glCopyPixels**:</span></span>

<span data-ttu-id="fa0b9-196">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Current \_ raster \_ position</span><span class="sxs-lookup"><span data-stu-id="fa0b9-196">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>

<span data-ttu-id="fa0b9-197">**glGet** con argomento GL \_ Current \_ raster \_ position \_ valido</span><span class="sxs-lookup"><span data-stu-id="fa0b9-197">**glGet** with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>

<span data-ttu-id="fa0b9-198">Per copiare il pixel di colore nell'angolo inferiore sinistro della finestra nella posizione raster corrente, usare</span><span class="sxs-lookup"><span data-stu-id="fa0b9-198">To copy the color pixel in the lower-left corner of the window to the current raster position, use</span></span>

<span data-ttu-id="fa0b9-199">**glCopyPixels**(0, 0, 1, 1, \_ colore GL);</span><span class="sxs-lookup"><span data-stu-id="fa0b9-199">**glCopyPixels**( 0, 0, 1, 1, GL\_COLOR );</span></span>

## <a name="requirements"></a><span data-ttu-id="fa0b9-200">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa0b9-200">Requirements</span></span>



| <span data-ttu-id="fa0b9-201">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa0b9-201">Requirement</span></span> | <span data-ttu-id="fa0b9-202">Valore</span><span class="sxs-lookup"><span data-stu-id="fa0b9-202">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa0b9-203">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa0b9-203">Minimum supported client</span></span><br/> | <span data-ttu-id="fa0b9-204">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fa0b9-204">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="fa0b9-205">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fa0b9-205">Minimum supported server</span></span><br/> | <span data-ttu-id="fa0b9-206">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="fa0b9-206">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fa0b9-207">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fa0b9-207">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa0b9-208"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa0b9-208"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="fa0b9-209">Libreria</span><span class="sxs-lookup"><span data-stu-id="fa0b9-209">Library</span></span><br/>                  | <dl> <span data-ttu-id="fa0b9-210"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa0b9-210"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="fa0b9-211">DLL</span><span class="sxs-lookup"><span data-stu-id="fa0b9-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa0b9-212"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa0b9-212"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa0b9-213">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fa0b9-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa0b9-214">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="fa0b9-214">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="fa0b9-215">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="fa0b9-215">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="fa0b9-216">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="fa0b9-216">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="fa0b9-217">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="fa0b9-217">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="fa0b9-218">**Remo**</span><span class="sxs-lookup"><span data-stu-id="fa0b9-218">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="fa0b9-219">**glGet**</span><span class="sxs-lookup"><span data-stu-id="fa0b9-219">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="fa0b9-220">**glPixelMap**</span><span class="sxs-lookup"><span data-stu-id="fa0b9-220">**glPixelMap**</span></span>](glpixelmap.md)
</dt> <dt>

[<span data-ttu-id="fa0b9-221">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="fa0b9-221">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="fa0b9-222">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="fa0b9-222">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="fa0b9-223">**glPixelZoom**</span><span class="sxs-lookup"><span data-stu-id="fa0b9-223">**glPixelZoom**</span></span>](glpixelzoom.md)
</dt> <dt>

[<span data-ttu-id="fa0b9-224">**glRasterPos**</span><span class="sxs-lookup"><span data-stu-id="fa0b9-224">**glRasterPos**</span></span>](glrasterpos-functions.md)
</dt> <dt>

[<span data-ttu-id="fa0b9-225">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="fa0b9-225">**glReadBuffer**</span></span>](glreadbuffer.md)
</dt> <dt>

[<span data-ttu-id="fa0b9-226">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="fa0b9-226">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="fa0b9-227">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="fa0b9-227">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





