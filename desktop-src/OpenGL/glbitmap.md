---
title: funzione glBitmap (GL. h)
description: La funzione glBitmap disegna una bitmap.
ms.assetid: 3cd8e41b-016b-4610-833a-048b5e50ae7c
keywords:
- funzione glBitmap OpenGL
topic_type:
- apiref
api_name:
- glBitmap
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aeb97bb16a1e3c4c29d1dfb1a5320c02f44404d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048470"
---
# <a name="glbitmap-function"></a><span data-ttu-id="c03a8-104">glBitmap (funzione)</span><span class="sxs-lookup"><span data-stu-id="c03a8-104">glBitmap function</span></span>

<span data-ttu-id="c03a8-105">La funzione **glBitmap** disegna una bitmap.</span><span class="sxs-lookup"><span data-stu-id="c03a8-105">The **glBitmap** function draws a bitmap.</span></span>

## <a name="syntax"></a><span data-ttu-id="c03a8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c03a8-106">Syntax</span></span>


```C++
void WINAPI glBitmap(
         GLSizei width,
         GLSizei height,
         GLfloat xorig,
         GLfloat yorig,
         GLfloat xmove,
         GLfloat ymove,
   const GLubyte *bitmap
);
```



## <a name="parameters"></a><span data-ttu-id="c03a8-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c03a8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c03a8-108">*width*</span><span class="sxs-lookup"><span data-stu-id="c03a8-108">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="c03a8-109">Larghezza in pixel dell'immagine bitmap.</span><span class="sxs-lookup"><span data-stu-id="c03a8-109">The pixel width of the bitmap image.</span></span>

</dd> <dt>

<span data-ttu-id="c03a8-110">*height*</span><span class="sxs-lookup"><span data-stu-id="c03a8-110">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="c03a8-111">Altezza in pixel dell'immagine bitmap.</span><span class="sxs-lookup"><span data-stu-id="c03a8-111">The pixel height of the bitmap image.</span></span>

</dd> <dt>

<span data-ttu-id="c03a8-112">*xorig*</span><span class="sxs-lookup"><span data-stu-id="c03a8-112">*xorig*</span></span> 
</dt> <dd>

<span data-ttu-id="c03a8-113">Posizione *x* dell'origine nell'immagine bitmap.</span><span class="sxs-lookup"><span data-stu-id="c03a8-113">The *x* location of the origin in the bitmap image.</span></span> <span data-ttu-id="c03a8-114">L'origine viene misurata dall'angolo inferiore sinistro della bitmap, con le direzioni giuste e verso l'alto sono gli assi positivi.</span><span class="sxs-lookup"><span data-stu-id="c03a8-114">The origin is measured from the lower-left corner of the bitmap, with right and up directions being the positive axes.</span></span>

</dd> <dt>

<span data-ttu-id="c03a8-115">*yorig*</span><span class="sxs-lookup"><span data-stu-id="c03a8-115">*yorig*</span></span> 
</dt> <dd>

<span data-ttu-id="c03a8-116">Posizione *y* dell'origine nell'immagine bitmap.</span><span class="sxs-lookup"><span data-stu-id="c03a8-116">The *y* location of the origin in the bitmap image.</span></span> <span data-ttu-id="c03a8-117">L'origine viene misurata dall'angolo inferiore sinistro della bitmap, con le direzioni giuste e verso l'alto sono gli assi positivi.</span><span class="sxs-lookup"><span data-stu-id="c03a8-117">The origin is measured from the lower-left corner of the bitmap, with right and up directions being the positive axes.</span></span>

</dd> <dt>

<span data-ttu-id="c03a8-118">*xmove*</span><span class="sxs-lookup"><span data-stu-id="c03a8-118">*xmove*</span></span> 
</dt> <dd>

<span data-ttu-id="c03a8-119">Offset *x* da aggiungere alla posizione raster corrente dopo che la bitmap è stata disegnata.</span><span class="sxs-lookup"><span data-stu-id="c03a8-119">The *x* offset to be added to the current raster position after the bitmap is drawn.</span></span>

</dd> <dt>

<span data-ttu-id="c03a8-120">*ymove*</span><span class="sxs-lookup"><span data-stu-id="c03a8-120">*ymove*</span></span> 
</dt> <dd>

<span data-ttu-id="c03a8-121">Offset *y* da aggiungere alla posizione raster corrente dopo che la bitmap è stata disegnata.</span><span class="sxs-lookup"><span data-stu-id="c03a8-121">The *y* offset to be added to the current raster position after the bitmap is drawn.</span></span>

</dd> <dt>

<span data-ttu-id="c03a8-122">*bitmap*</span><span class="sxs-lookup"><span data-stu-id="c03a8-122">*bitmap*</span></span> 
</dt> <dd>

<span data-ttu-id="c03a8-123">Indirizzo dell'immagine bitmap.</span><span class="sxs-lookup"><span data-stu-id="c03a8-123">The address of the bitmap image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c03a8-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c03a8-124">Return value</span></span>

<span data-ttu-id="c03a8-125">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="c03a8-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c03a8-126">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="c03a8-126">Error codes</span></span>

<span data-ttu-id="c03a8-127">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="c03a8-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="c03a8-128">Nome</span><span class="sxs-lookup"><span data-stu-id="c03a8-128">Name</span></span>                                                                                                  | <span data-ttu-id="c03a8-129">Significato</span><span class="sxs-lookup"><span data-stu-id="c03a8-129">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c03a8-130"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c03a8-130"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="c03a8-131">la *larghezza* o l' *altezza* è negativa.</span><span class="sxs-lookup"><span data-stu-id="c03a8-131">*width* or *height* is negative.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="c03a8-132"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c03a8-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="c03a8-133">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="c03a8-133">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c03a8-134">Commenti</span><span class="sxs-lookup"><span data-stu-id="c03a8-134">Remarks</span></span>

<span data-ttu-id="c03a8-135">Una bitmap è un'immagine binaria.</span><span class="sxs-lookup"><span data-stu-id="c03a8-135">A bitmap is a binary image.</span></span> <span data-ttu-id="c03a8-136">Quando viene disegnata, la bitmap viene posizionata in relazione alla posizione raster corrente e i pixel framebuffer corrispondenti a 1S nella bitmap vengono scritti usando il colore o l'indice raster corrente.</span><span class="sxs-lookup"><span data-stu-id="c03a8-136">When drawn, the bitmap is positioned relative to the current raster position, and framebuffer pixels corresponding to 1s in the bitmap are written using the current raster color or index.</span></span> <span data-ttu-id="c03a8-137">I pixel del buffer dei frame corrispondenti agli zeri nella bitmap non vengono modificati.</span><span class="sxs-lookup"><span data-stu-id="c03a8-137">Frame-buffer pixels corresponding to zeros in the bitmap are not modified.</span></span>

<span data-ttu-id="c03a8-138">L'immagine bitmap viene interpretata come dati di immagine per la funzione [**glDrawPixels**](gldrawpixels.md) , con *larghezza* e *altezza* corrispondenti agli argomenti di larghezza e altezza della funzione e con il *tipo* impostato su GL \_ bitmap e *Format* impostato su GL \_ Color \_ index.</span><span class="sxs-lookup"><span data-stu-id="c03a8-138">The bitmap image is interpreted like image data for the [**glDrawPixels**](gldrawpixels.md) function, with *width* and *height* corresponding to the width and height arguments of that function, and with *type* set to GL\_BITMAP and *format* set to GL\_COLOR\_INDEX.</span></span> <span data-ttu-id="c03a8-139">Le modalità specificate utilizzando [**glPixelStore**](glpixelstore-functions.md) influiscono sull'interpretazione dei dati dell'immagine bitmap. le modalità specificate tramite [**glPixelTransfer**](glpixeltransfer.md) non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="c03a8-139">Modes you specify using [**glPixelStore**](glpixelstore-functions.md) affect the interpretation of bitmap image data; modes you specify using [**glPixelTransfer**](glpixeltransfer.md) do not.</span></span>

<span data-ttu-id="c03a8-140">Se la posizione raster corrente non è valida, **glBitmap** viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="c03a8-140">If the current raster position is invalid, **glBitmap** is ignored.</span></span> <span data-ttu-id="c03a8-141">In caso contrario, l'angolo inferiore sinistro dell'immagine bitmap viene posizionato alle coordinate della finestra seguenti:</span><span class="sxs-lookup"><span data-stu-id="c03a8-141">Otherwise, the lower-left corner of the bitmap image is positioned at the following window coordinates:</span></span>

<span data-ttu-id="c03a8-142">*x*<sub>w</sub>  =  *x*<sub>r</sub> *x*?</span><span class="sxs-lookup"><span data-stu-id="c03a8-142">*x*<sub>w</sub> = *x*<sub>r</sub> *x*?</span></span>

<span data-ttu-id="c03a8-143">*y*<sub>w</sub>  =  *y*<sub>r</sub> *y*?</span><span class="sxs-lookup"><span data-stu-id="c03a8-143">*y*<sub>w</sub> = *y*<sub>r</sub> *y*?</span></span>

<span data-ttu-id="c03a8-144">In queste coordinate (*x*<sub>r</sub> , *y*<sub>r</sub> ) è la posizione raster e (*x*?</span><span class="sxs-lookup"><span data-stu-id="c03a8-144">In these coordinates, (*x*<sub>r</sub> , *y*<sub>r</sub> ) is the raster position, and (*x*?</span></span> <span data-ttu-id="c03a8-145">, *y*?</span><span class="sxs-lookup"><span data-stu-id="c03a8-145">, *y*?</span></span> <span data-ttu-id="c03a8-146">) è l'origine della bitmap.</span><span class="sxs-lookup"><span data-stu-id="c03a8-146">) is the bitmap origin.</span></span> <span data-ttu-id="c03a8-147">I frammenti vengono quindi generati per ogni pixel corrispondente a 1 nell'immagine bitmap.</span><span class="sxs-lookup"><span data-stu-id="c03a8-147">Fragments are then generated for each pixel corresponding to a 1 in the bitmap image.</span></span> <span data-ttu-id="c03a8-148">Questi frammenti vengono generati usando la coordinata *z*, il colore o l'indice dei colori e le coordinate correnti della trama raster.</span><span class="sxs-lookup"><span data-stu-id="c03a8-148">These fragments are generated using the current raster *z*-coordinate, color or color index, and current raster texture coordinates.</span></span> <span data-ttu-id="c03a8-149">Vengono quindi trattati come se fossero stati generati da un punto, una linea o un poligono, tra cui il mapping di trama, la nebbia e tutte le operazioni per frammento, ad esempio Alpha e test di profondità.</span><span class="sxs-lookup"><span data-stu-id="c03a8-149">They are then treated just as if they had been generated by a point, line, or polygon, including texture mapping, fogging, and all per-fragment operations such as alpha and depth testing.</span></span>

<span data-ttu-id="c03a8-150">Dopo che la bitmap è stata disegnata, le coordinate *x* e *y* della posizione raster corrente sono offset da *XMOVE* e *ymove*.</span><span class="sxs-lookup"><span data-stu-id="c03a8-150">After the bitmap has been drawn, the *x* and *y* coordinates of the current raster position are offset by *xmove* and *ymove*.</span></span> <span data-ttu-id="c03a8-151">Non viene apportata alcuna modifica alla coordinata *z* della posizione raster corrente o al colore raster, all'indice o alle coordinate di trama correnti.</span><span class="sxs-lookup"><span data-stu-id="c03a8-151">No change is made to the *z*-coordinate of the current raster position, or to the current raster color, index, or texture coordinates.</span></span>

<span data-ttu-id="c03a8-152">Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glBitmap** :</span><span class="sxs-lookup"><span data-stu-id="c03a8-152">The following functions retrieve information related to the **glBitmap** function:</span></span>

<span data-ttu-id="c03a8-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Current \_ raster \_ position</span><span class="sxs-lookup"><span data-stu-id="c03a8-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CURRENT\_RASTER\_POSITION</span></span>

 

<span data-ttu-id="c03a8-154">**glGet** con argomento GL \_ Current \_ \_ color raster</span><span class="sxs-lookup"><span data-stu-id="c03a8-154">**glGet** with argument GL\_CURRENT\_RASTER\_COLOR</span></span>

 

<span data-ttu-id="c03a8-155">**glGet** con argomento GL \_ Current \_ \_ index raster</span><span class="sxs-lookup"><span data-stu-id="c03a8-155">**glGet** with argument GL\_CURRENT\_RASTER\_INDEX</span></span>

 

<span data-ttu-id="c03a8-156">**glGet** con argomento con \_ \_ coordinate di \_ trama \_ raster correnti</span><span class="sxs-lookup"><span data-stu-id="c03a8-156">**glGet** with argument GL\_CURRENT\_RASTER\_TEXTURE\_COORDS</span></span>

 

<span data-ttu-id="c03a8-157">**glGet** con argomento GL \_ Current \_ raster \_ position \_ valido</span><span class="sxs-lookup"><span data-stu-id="c03a8-157">**glGet** with argument GL\_CURRENT\_RASTER\_POSITION\_VALID</span></span>

## <a name="requirements"></a><span data-ttu-id="c03a8-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c03a8-158">Requirements</span></span>



| <span data-ttu-id="c03a8-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="c03a8-159">Requirement</span></span> | <span data-ttu-id="c03a8-160">Valore</span><span class="sxs-lookup"><span data-stu-id="c03a8-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c03a8-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c03a8-161">Minimum supported client</span></span><br/> | <span data-ttu-id="c03a8-162">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c03a8-162">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c03a8-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c03a8-163">Minimum supported server</span></span><br/> | <span data-ttu-id="c03a8-164">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c03a8-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c03a8-165">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c03a8-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="c03a8-166"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c03a8-166"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c03a8-167">Libreria</span><span class="sxs-lookup"><span data-stu-id="c03a8-167">Library</span></span><br/>                  | <dl> <span data-ttu-id="c03a8-168"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c03a8-168"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c03a8-169">DLL</span><span class="sxs-lookup"><span data-stu-id="c03a8-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c03a8-170"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c03a8-170"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c03a8-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c03a8-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c03a8-172">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c03a8-172">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c03a8-173">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="c03a8-173">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="c03a8-174">**Remo**</span><span class="sxs-lookup"><span data-stu-id="c03a8-174">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c03a8-175">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="c03a8-175">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="c03a8-176">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="c03a8-176">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="c03a8-177">**glRasterPos**</span><span class="sxs-lookup"><span data-stu-id="c03a8-177">**glRasterPos**</span></span>](glrasterpos-functions.md)
</dt> </dl>

 

 





