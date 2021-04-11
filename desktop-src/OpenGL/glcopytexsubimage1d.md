---
title: funzione glCopyTexSubImage1D (GL. h)
description: La funzione glCopyTexSubImage1D copia un'immagine secondaria di un'immagine di trama unidimensionale dal framebuffer.
ms.assetid: 718aee8a-6dce-49e1-a441-19beccd89f8d
keywords:
- funzione glCopyTexSubImage1D OpenGL
topic_type:
- apiref
api_name:
- glCopyTexSubImage1D
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64006f9cec7e5fd2f3ca6f860249e579b16dbf10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964452"
---
# <a name="glcopytexsubimage1d-function"></a><span data-ttu-id="7fbeb-104">glCopyTexSubImage1D (funzione)</span><span class="sxs-lookup"><span data-stu-id="7fbeb-104">glCopyTexSubImage1D function</span></span>

<span data-ttu-id="7fbeb-105">La funzione **glCopyTexSubImage1D** copia un'immagine secondaria di un'immagine di trama unidimensionale dal framebuffer.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-105">The **glCopyTexSubImage1D** function copies a sub-image of a one-dimensional texture image from the framebuffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fbeb-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7fbeb-106">Syntax</span></span>


```C++
void WINAPI glCopyTexSubImage1D(
   GLenum  target,
   GLint   level,
   GLint   xoffset,
   GLint   x,
   GLint   y,
   GLsizei width
);
```



## <a name="parameters"></a><span data-ttu-id="7fbeb-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7fbeb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fbeb-108">*target*</span><span class="sxs-lookup"><span data-stu-id="7fbeb-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="7fbeb-109">Destinazione in cui verranno modificati i dati dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-109">The target to which the image data will be changed.</span></span> <span data-ttu-id="7fbeb-110">Deve avere il valore GL \_ texture \_ 1D.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-110">Must have the value GL\_TEXTURE\_1D.</span></span>

</dd> <dt>

<span data-ttu-id="7fbeb-111">*level*</span><span class="sxs-lookup"><span data-stu-id="7fbeb-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="7fbeb-112">Numero del livello di dettaglio.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-112">The level-of-detail number.</span></span> <span data-ttu-id="7fbeb-113">Il livello 0 è l'immagine di base.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-113">Level 0 is the base image.</span></span> <span data-ttu-id="7fbeb-114">Il livello *n* è l'immagine di riduzione del mipmap *n*.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="7fbeb-115">*xoffset*</span><span class="sxs-lookup"><span data-stu-id="7fbeb-115">*xoffset*</span></span> 
</dt> <dd>

<span data-ttu-id="7fbeb-116">Offset Texel all'interno della matrice di trame.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-116">The texel offset within the texture array.</span></span>

</dd> <dt>

<span data-ttu-id="7fbeb-117">*x*</span><span class="sxs-lookup"><span data-stu-id="7fbeb-117">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="7fbeb-118">Coordinata del piano x della finestra dell'angolo inferiore sinistro della riga di pixel da copiare.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-118">The window x-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="7fbeb-119">*y*</span><span class="sxs-lookup"><span data-stu-id="7fbeb-119">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="7fbeb-120">Coordinata del piano y della finestra dell'angolo inferiore sinistro della riga di pixel da copiare.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-120">The window y-plane coordinate of the lower-left corner of the row of pixels to be copied.</span></span>

</dd> <dt>

<span data-ttu-id="7fbeb-121">*width*</span><span class="sxs-lookup"><span data-stu-id="7fbeb-121">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="7fbeb-122">Larghezza dell'immagine secondaria dell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-122">The width of the sub-image of the texture image.</span></span> <span data-ttu-id="7fbeb-123">La specifica di un'immagine secondaria della trama con larghezza zero non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-123">Specifying a texture sub-image with zero width has no effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fbeb-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7fbeb-124">Return value</span></span>

<span data-ttu-id="7fbeb-125">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-125">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7fbeb-126">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="7fbeb-126">Error codes</span></span>

<span data-ttu-id="7fbeb-127">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="7fbeb-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7fbeb-128">Nome</span><span class="sxs-lookup"><span data-stu-id="7fbeb-128">Name</span></span>                                                                                                  | <span data-ttu-id="7fbeb-129">Significato</span><span class="sxs-lookup"><span data-stu-id="7fbeb-129">Meaning</span></span>                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7fbeb-130"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7fbeb-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="7fbeb-131">*target* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-131">*target* was not an accepted value.</span></span><br/>                                                                                                                                                                               |
| <dl> <span data-ttu-id="7fbeb-132"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7fbeb-132"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="7fbeb-133">il *livello* è minore di zero o il *livello* è maggiore di *log* 2 (*Max*), dove *Max* è il valore restituito della dimensione della \_ trama GL Max \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7fbeb-133">*level* was less than zero or *level* is greater than *log* 2(*max*), where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="7fbeb-134"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7fbeb-134"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="7fbeb-135">*xoffset* è minore del *bordo* o (  +  *larghezza* xoffset) è maggiore di (  +  *bordo* w), dove *w* è la \_ larghezza della trama GL \_ e il *bordo* è il \_ bordo della trama GL \_ .</span><span class="sxs-lookup"><span data-stu-id="7fbeb-135">*xoffset* was less than *border* or (*xoffset* + *width*)was greater than (*w* + *border*), where *w* is GL\_TEXTURE\_WIDTH and *border* is GL\_TEXTURE\_BORDER.</span></span> <span data-ttu-id="7fbeb-136">Si noti che *w* include il doppio della larghezza del *bordo* .</span><span class="sxs-lookup"><span data-stu-id="7fbeb-136">Note that *w* includes twice the *border* width.</span></span><br/> |
| <dl> <span data-ttu-id="7fbeb-137"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7fbeb-137"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="7fbeb-138">la *larghezza* era minore *del bordo* o *y* era minore del *bordo*, dove *Border* è lo spessore del bordo della matrice di trame.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-138">*width* was less than *border* or *y* was less than *border*, where *border* is the border width of the texture array.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="7fbeb-139"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7fbeb-139"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7fbeb-140">La matrice di trama non è stata definita da un'operazione [**glTexImage1D**](glteximage1d.md) precedente.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-140">The texture array was not defined by a previous [**glTexImage1D**](glteximage1d.md) operation.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="7fbeb-141"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7fbeb-141"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7fbeb-142">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="7fbeb-142">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                        |



## <a name="remarks"></a><span data-ttu-id="7fbeb-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="7fbeb-143">Remarks</span></span>

<span data-ttu-id="7fbeb-144">La funzione **glCopyTexSubImage1D** sostituisce una parte di un'immagine di trama unidimensionale usando i pixel del framebuffer corrente, anziché dalla memoria principale come nel caso di [**glTexSubImage1D**](gltexsubimage1d.md).</span><span class="sxs-lookup"><span data-stu-id="7fbeb-144">The **glCopyTexSubImage1D** function replaces a portion of a one-dimensional texture image using pixels from the current framebuffer, rather than from main memory as is the case for [**glTexSubImage1D**](gltexsubimage1d.md).</span></span>

<span data-ttu-id="7fbeb-145">Una riga di pixel che inizia con le coordinate della finestra specificate da *x* e *y* e con la *larghezza* della lunghezza sostituisce la parte della matrice di trama con gli indici *xoffset* tramite *xoffset* + (*Width* -1).</span><span class="sxs-lookup"><span data-stu-id="7fbeb-145">A row of pixels beginning with the window coordinates specified by *x* and *y* and with the length *width* replaces the portion of the texture array with the indexes *xoffset* through *xoffset* + (*width* - 1).</span></span> <span data-ttu-id="7fbeb-146">La destinazione nella matrice di trame non può includere Texel all'esterno della matrice di trama specificata in origine.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-146">The destination in the texture array cannot include any texels outside the originally specified texture array.</span></span>

<span data-ttu-id="7fbeb-147">La funzione **glCopyTexSubImage1D** elabora i pixel in una riga allo stesso modo di [**glCopyPixels**](glcopypixels.md) , ad eccezione del fatto che prima della conversione finale dei pixel, tutti i valori dei componenti pixel vengono fissati all'intervallo \[ 0, 1 \] e vengono convertiti nel formato interno della trama per l'archiviazione nella matrice di trame.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-147">The **glCopyTexSubImage1D** function processes the pixels in a row in the same way as [**glCopyPixels**](glcopypixels.md) except that before the final conversion of the pixels, all pixel component values are clamped to the range \[0,1\] and converted to the texture's internal format for storage in the texture array.</span></span> <span data-ttu-id="7fbeb-148">L'ordinamento dei pixel è determinato da coordinate *x* inferiori corrispondenti a coordinate di trama inferiori.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-148">Pixel ordering is determined with lower *x* coordinates corresponding to lower texture coordinates.</span></span> <span data-ttu-id="7fbeb-149">Se uno dei pixel all'interno di una riga specificata del framebuffer corrente è esterno alla finestra associata al contesto di rendering corrente, i relativi valori non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-149">If any of the pixels within a specified row of the current framebuffer are outside the window associated with the current rendering context, then their values are undefined.</span></span>

<span data-ttu-id="7fbeb-150">Non viene apportata alcuna modifica al parametro *internalFormat*, *Width* o *Border* della matrice di trama specificata o ai valori Texel al di fuori dell'immagine secondaria della trama specificata.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-150">No change is made to the *internalFormat*, *width*, or *border* parameter of the specified texture array or to texel values outside the specified texture sub-image.</span></span>

<span data-ttu-id="7fbeb-151">Non è possibile includere chiamate a **glCopyTexSubImage1D** negli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-151">You cannot include calls to **glCopyTexSubImage1D** in display lists.</span></span>

> [!Note]  
> <span data-ttu-id="7fbeb-152">La funzione **glCopyTexSubImage1D** è disponibile solo in OpenGL versione 1,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-152">The **glCopyTexSubImage1D** function is only available in OpenGL version 1.1 or later.</span></span>

 

<span data-ttu-id="7fbeb-153">La texturing non ha alcun effetto sulla modalità di indicizzazione del colore.</span><span class="sxs-lookup"><span data-stu-id="7fbeb-153">Texturing has no effect in color-index mode.</span></span> <span data-ttu-id="7fbeb-154">Le funzioni [**glPixelStore**](glpixelstore-functions.md) e [**glPixelTransfer**](glpixeltransfer.md) influiscono sulle immagini della trama esattamente come influiscono sul modo in cui i pixel vengono disegnati usando [**glDrawPixels**](gldrawpixels.md).</span><span class="sxs-lookup"><span data-stu-id="7fbeb-154">The [**glPixelStore**](glpixelstore-functions.md) and [**glPixelTransfer**](glpixeltransfer.md) functions affect texture images in exactly the way they affect the way pixels are drawn using [**glDrawPixels**](gldrawpixels.md).</span></span>

<span data-ttu-id="7fbeb-155">Le funzioni seguenti consentono di recuperare informazioni correlate a **glCopyTexSubImage1D**:</span><span class="sxs-lookup"><span data-stu-id="7fbeb-155">The following functions retrieve information related to **glCopyTexSubImage1D**:</span></span>

[<span data-ttu-id="7fbeb-156">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="7fbeb-156">**glGetTexImage**</span></span>](glgetteximage.md)

<span data-ttu-id="7fbeb-157">[**glIsEnabled**](glisenabled.md) con argomento GL \_ texture \_ 1D</span><span class="sxs-lookup"><span data-stu-id="7fbeb-157">[**glIsEnabled**](glisenabled.md) with argument GL\_TEXTURE\_1D</span></span>

## <a name="requirements"></a><span data-ttu-id="7fbeb-158">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7fbeb-158">Requirements</span></span>



| <span data-ttu-id="7fbeb-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fbeb-159">Requirement</span></span> | <span data-ttu-id="7fbeb-160">Valore</span><span class="sxs-lookup"><span data-stu-id="7fbeb-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fbeb-161">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7fbeb-161">Minimum supported client</span></span><br/> | <span data-ttu-id="7fbeb-162">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7fbeb-162">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7fbeb-163">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7fbeb-163">Minimum supported server</span></span><br/> | <span data-ttu-id="7fbeb-164">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7fbeb-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7fbeb-165">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7fbeb-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fbeb-166"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fbeb-166"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7fbeb-167">Libreria</span><span class="sxs-lookup"><span data-stu-id="7fbeb-167">Library</span></span><br/>                  | <dl> <span data-ttu-id="7fbeb-168"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7fbeb-168"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7fbeb-169">DLL</span><span class="sxs-lookup"><span data-stu-id="7fbeb-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fbeb-170"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fbeb-170"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fbeb-171">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7fbeb-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fbeb-172">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="7fbeb-172">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7fbeb-173">**glCopyTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="7fbeb-173">**glCopyTexSubImage2D**</span></span>](glcopytexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="7fbeb-174">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="7fbeb-174">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="7fbeb-175">**Remo**</span><span class="sxs-lookup"><span data-stu-id="7fbeb-175">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="7fbeb-176">**glFog**</span><span class="sxs-lookup"><span data-stu-id="7fbeb-176">**glFog**</span></span>](glfog.md)
</dt> <dt>

[<span data-ttu-id="7fbeb-177">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="7fbeb-177">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="7fbeb-178">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="7fbeb-178">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="7fbeb-179">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="7fbeb-179">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> <dt>

[<span data-ttu-id="7fbeb-180">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="7fbeb-180">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> <dt>

[<span data-ttu-id="7fbeb-181">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="7fbeb-181">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="7fbeb-182">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="7fbeb-182">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="7fbeb-183">**glTexSubImage1D**</span><span class="sxs-lookup"><span data-stu-id="7fbeb-183">**glTexSubImage1D**</span></span>](gltexsubimage1d.md)
</dt> <dt>

[<span data-ttu-id="7fbeb-184">**glTexSubImage2D**</span><span class="sxs-lookup"><span data-stu-id="7fbeb-184">**glTexSubImage2D**</span></span>](gltexsubimage2d.md)
</dt> <dt>

[<span data-ttu-id="7fbeb-185">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="7fbeb-185">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





