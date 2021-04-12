---
title: funzione glCopyTexSubImage2D (GL. h)
description: La funzione glCopyTexSubImage2D copia un'immagine secondaria di un'immagine di trama bidimensionale dal framebuffer.
ms.assetid: cbb644d4-6a23-4d66-8599-5f8b48e9b91f
keywords:
- funzione glCopyTexSubImage2D OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage2D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c966d031bb154b59cc54ae2e5d254347aa88d2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400704"
---
# <a name="glcopytexsubimage2d-function"></a><span data-ttu-id="cc520-104">glCopyTexSubImage2D (funzione)</span><span class="sxs-lookup"><span data-stu-id="cc520-104">glCopyTexSubImage2D function</span></span>

<span data-ttu-id="cc520-105">La funzione **glCopyTexSubImage2D** copia un'immagine secondaria di un'immagine di trama bidimensionale dal framebuffer.</span><span class="sxs-lookup"><span data-stu-id="cc520-105">The **glCopyTexSubImage2D** function copies a sub-image of a two-dimensional texture image from the framebuffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc520-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc520-106">Syntax</span></span>


```C++
void WINAPI glCopyTexSubImage2D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   yoffset,
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="cc520-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc520-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc520-108">*target*</span><span class="sxs-lookup"><span data-stu-id="cc520-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="cc520-109">Destinazione in cui verranno modificati i dati dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="cc520-109">The target to which the image data will be changed.</span></span> <span data-ttu-id="cc520-110">Deve avere il valore di \_ trama GL \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="cc520-110">Must have the value GL\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="cc520-111">*level*</span><span class="sxs-lookup"><span data-stu-id="cc520-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="cc520-112">Numero del livello di dettaglio.</span><span class="sxs-lookup"><span data-stu-id="cc520-112">The level-of-detail number.</span></span> <span data-ttu-id="cc520-113">Il livello 0 è l'immagine di base.</span><span class="sxs-lookup"><span data-stu-id="cc520-113">Level 0 is the base image.</span></span> <span data-ttu-id="cc520-114">Il livello *n* è l'immagine di riduzione del mipmap *n*.</span><span class="sxs-lookup"><span data-stu-id="cc520-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="cc520-115">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="cc520-115">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="cc520-116">Offset Texel nella direzione *x* all'interno della matrice di trame.</span><span class="sxs-lookup"><span data-stu-id="cc520-116">The texel offset in the *x* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="cc520-117">*yoffset*</span><span class="sxs-lookup"><span data-stu-id="cc520-117">*yoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="cc520-118">Offset Texel nella direzione *y* all'interno della matrice di trame.</span><span class="sxs-lookup"><span data-stu-id="cc520-118">The texel offset in the *y* direction within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="cc520-119">*x*</span><span class="sxs-lookup"><span data-stu-id="cc520-119">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="cc520-120">Coordinate del piano x della finestra dell'angolo inferiore sinistro della riga di pixel da copiare.</span><span class="sxs-lookup"><span data-stu-id="cc520-120">The window x-plane coordinates of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="cc520-121">*y*</span><span class="sxs-lookup"><span data-stu-id="cc520-121">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="cc520-122">Coordinate del piano y della finestra dell'angolo inferiore sinistro della riga di pixel da copiare.</span><span class="sxs-lookup"><span data-stu-id="cc520-122">The window y-plane coordinates of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="cc520-123">*width*</span><span class="sxs-lookup"><span data-stu-id="cc520-123">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="cc520-124">Larghezza dell'immagine secondaria dell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="cc520-124">The width of the sub-image of the texture image.</span></span> <span data-ttu-id="cc520-125">La specifica di un'immagine secondaria della trama con larghezza zero non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="cc520-125">Specifying a texture sub-image with zero width has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="cc520-126">*height*</span><span class="sxs-lookup"><span data-stu-id="cc520-126">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="cc520-127">Altezza dell'immagine secondaria dell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="cc520-127">The height of the sub-image of the texture image.</span></span> <span data-ttu-id="cc520-128">La specifica di un'immagine secondaria della trama con larghezza zero non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="cc520-128">Specifying a texture sub-image with zero width has no effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc520-129">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cc520-129">Return value</span></span>

<span data-ttu-id="cc520-130">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="cc520-130">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cc520-131">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="cc520-131">Error codes</span></span>

<span data-ttu-id="cc520-132">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="cc520-132">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="cc520-133">Nome</span><span class="sxs-lookup"><span data-stu-id="cc520-133">Name</span></span>                                                                                                  | <span data-ttu-id="cc520-134">Significato</span><span class="sxs-lookup"><span data-stu-id="cc520-134">Meaning</span></span>                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cc520-135"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc520-135"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="cc520-136">*target* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="cc520-136">*target* was not an accepted value.</span></span><br/>                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="cc520-137"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc520-137"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="cc520-138">il *livello* è minore di zero o maggiore di *log* 2 (*Max*), dove *Max* è il valore restituito della \_ dimensione della trama GL Max \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cc520-138">*level* was less than zero or greater than *log* 2 (*max*), where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="cc520-139"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc520-139"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="cc520-140">il valore di *xoffset* è minore di *Border* o (  +  *larghezza* xoffset) è maggiore di (*w*  +  *Border*), *yoffset* è minore di *Border* oppure (*yoffset*  +  *Height*) è maggioredi (  +  *bordo* h), dove *w* è la larghezza della trama GL e il bordo è il \_ bordo della \_ trama GL  \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="cc520-140">*xoffset* was less than *border* or (*xoffset* + *width*)was greater than (*w* + *border*), *yoffset* was less than *border*, or (*yoffset* + *height*) was greater than (*h* + *border*), where *w* is GL\_TEXTURE\_WIDTH and *border* is GL\_TEXTURE\_BORDER.</span></span> <span data-ttu-id="cc520-141">Si noti che *w* include il doppio della larghezza del *bordo* .</span><span class="sxs-lookup"><span data-stu-id="cc520-141">Note that *w* includes twice the *border* width.</span></span><br/> |
| <dl> <span data-ttu-id="cc520-142"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc520-142"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="cc520-143">la *larghezza* era minore *del bordo* o *y* era minore del *bordo*, dove *Border* è lo spessore del bordo della matrice di trame.</span><span class="sxs-lookup"><span data-stu-id="cc520-143">*width* was less than *border* or *y* was less than *border*, where *border* is the border width of the texture array.</span></span><br/>                                                                                                                                                                                           |
| <dl> <span data-ttu-id="cc520-144"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc520-144"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="cc520-145">La matrice di trama non è stata definita da un'operazione [**glTexImage1D**](glteximage1d.md) precedente.</span><span class="sxs-lookup"><span data-stu-id="cc520-145">The texture array was not defined by a previous [**glTexImage1D**](glteximage1d.md) operation.</span></span><br/>                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="cc520-146"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cc520-146"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="cc520-147">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="cc520-147">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                                                                                                                       |



## <a name="remarks"></a><span data-ttu-id="cc520-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="cc520-148">Remarks</span></span>

<span data-ttu-id="cc520-149">La funzione **glCopyTexSubImage2D** sostituisce una parte rettangolare di un'immagine con trama bidimensionale con pixel del framebuffer corrente, anziché dalla memoria principale come nel caso di [**glTexSubImage2D**](gltexsubimage2d.md).</span><span class="sxs-lookup"><span data-stu-id="cc520-149">The **glCopyTexSubImage2D** function replaces a rectangular portion of a two-dimensional texture image with pixels from the current framebuffer, rather than from main memory as is the case for [**glTexSubImage2D**](gltexsubimage2d.md).</span></span>

<span data-ttu-id="cc520-150">Un rettangolo di pixel che inizia con le coordinate della finestra *x* e *y* e con la *larghezza* e l' *altezza* delle dimensioni sostituisce la parte della matrice di trama con gli indici *xoffset* tramite *xoffset* + (*Width* -1), con gli indici *yoffset* a *yoffset* + (*Width* -1) al livello mipmap specificato dal *livello*.</span><span class="sxs-lookup"><span data-stu-id="cc520-150">A rectangle of pixels beginning with the *x* and *y* window coordinates and with the dimensions *width* and *height* replaces the portion of the texture array with the indexes *xoffset* through *xoffset* + (*width* - 1), with the indexes *yoffset* through *yoffset* + (*width* - 1) at the mipmap level specified by *level*.</span></span> <span data-ttu-id="cc520-151">Il rettangolo di destinazione nella matrice di trama non può includere Texel all'esterno della matrice di trama specificata in origine.</span><span class="sxs-lookup"><span data-stu-id="cc520-151">The destination rectangle in the texture array cannot include any texels outside the originally specified texture array.</span></span>

<span data-ttu-id="cc520-152">La funzione **glCopyTexSubImage2D** elabora i pixel in una riga nello stesso modo in cui si trova [**glCopyPixels**](glcopypixels.md), ad eccezione del fatto che prima della conversione finale dei pixel, tutti i valori dei componenti pixel vengono bloccati nell'intervallo \[ 0, 1 \] e vengono convertiti nel formato interno della trama per l'archiviazione nella matrice di trame.</span><span class="sxs-lookup"><span data-stu-id="cc520-152">The **glCopyTexSubImage2D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md), except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="cc520-153">L'ordinamento dei pixel è determinato da coordinate *x* inferiori corrispondenti a coordinate di trama inferiori.</span><span class="sxs-lookup"><span data-stu-id="cc520-153">Pixel ordering is determined with lower *x* coordinates corresponding to lower texture coordinates.</span></span> <span data-ttu-id="cc520-154">Se uno dei pixel all'interno di una riga specificata del framebuffer corrente è esterno alla finestra associata al contesto di rendering corrente, i relativi valori non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="cc520-154">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="cc520-155">Se uno dei pixel all'interno del rettangolo specificato del framebuffer corrente è esterno alla finestra di lettura associata al contesto di rendering corrente, i valori ottenuti per tali pixel non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="cc520-155">If any of the pixels within the specified rectangle of the current framebuffer are outside the read window associated with the current rendering context, then the values obtained for those pixels are undefined.</span></span> <span data-ttu-id="cc520-156">Non viene apportata alcuna modifica al parametro *internalFormat*, *Width*, *Height* o *Border* della matrice di trama specificata o ai valori Texel al di fuori dell'immagine secondaria della trama specificata.</span><span class="sxs-lookup"><span data-stu-id="cc520-156">No change is made to the *internalFormat*, *width*, *height*, or *border* parameter of the specified texture array or to texel values outside the specified texture sub-image.</span></span>

<span data-ttu-id="cc520-157">Non è possibile includere chiamate a **glCopyTexSubImage2D** negli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="cc520-157">You cannot include calls to **glCopyTexSubImage2D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="cc520-158">La funzione **glCopyTexSubImage2D** è disponibile solo in OpenGL versione 1,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="cc520-158">The **glCopyTexSubImage2D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="cc520-159">La texturing non ha alcun effetto sulla modalità di indicizzazione del colore.</span><span class="sxs-lookup"><span data-stu-id="cc520-159">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="cc520-160">Le funzioni [**glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) influiscono sulle immagini della trama esattamente come influiscono sul modo in cui i pixel vengono disegnati usando [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="cc520-160">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect the way pixels are drawn using [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="cc520-161">Le funzioni seguenti consentono di recuperare informazioni correlate a **glCopyTexSubImage2D**:</span><span class="sxs-lookup"><span data-stu-id="cc520-161">The following functions retrieve information related to **glCopyTexSubImage2D**:</span></span>

[<span data-ttu-id="cc520-162">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="cc520-162">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="cc520-163">[**glIsEnabled**](glisenabled.md) con argomento di \_ trama GL \_ 2D</span><span class="sxs-lookup"><span data-stu-id="cc520-163">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_2D</span></span>

## <a name="requirements"></a><span data-ttu-id="cc520-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc520-164">Requirements</span></span>



| <span data-ttu-id="cc520-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc520-165">Requirement</span></span> | <span data-ttu-id="cc520-166">Valore</span><span class="sxs-lookup"><span data-stu-id="cc520-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc520-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc520-167">Minimum supported client</span></span><br/> | <span data-ttu-id="cc520-168">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cc520-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cc520-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cc520-169">Minimum supported server</span></span><br/> | <span data-ttu-id="cc520-170">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cc520-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cc520-171">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc520-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="cc520-172"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc520-172"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="cc520-173">Libreria</span><span class="sxs-lookup"><span data-stu-id="cc520-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="cc520-174"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc520-174"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cc520-175">DLL</span><span class="sxs-lookup"><span data-stu-id="cc520-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc520-176"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc520-176"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc520-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc520-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc520-178">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="cc520-178">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="cc520-179">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="cc520-179">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="cc520-180">**glCopyTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="cc520-180">**glCopyTexSubImage1D**</span></span>](glcopytexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="cc520-181">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="cc520-181">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="cc520-182">**Remo**</span><span class="sxs-lookup"><span data-stu-id="cc520-182">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="cc520-183">**glFog**</span><span class="sxs-lookup"><span data-stu-id="cc520-183">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="cc520-184">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="cc520-184">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="cc520-185">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="cc520-185">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="cc520-186">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="cc520-186">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="cc520-187">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="cc520-187">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="cc520-188">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="cc520-188">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="cc520-189">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="cc520-189">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="cc520-190">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="cc520-190">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





