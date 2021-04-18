---
title: funzione glGetTexLevelParameterfv (GL. h)
description: Le funzioni glGetTexLevelParameterfv e glGetTexLevelParameteriv restituiscono i valori dei parametri di trama per un livello di dettaglio specifico. | funzione glGetTexLevelParameterfv (GL. h)
ms.assetid: 5ea91f2e-c0cd-41ee-be95-df096f1c78ef
keywords:
- funzione glGetTexLevelParameterfv OpenGL
topic_type:
- apiref
api_name:
- glGetTexLevelParameterfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92f8b55b41d3538f116241a0401cedf643a5e55
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321581"
---
# <a name="glgettexlevelparameterfv-function"></a><span data-ttu-id="5c428-105">glGetTexLevelParameterfv (funzione)</span><span class="sxs-lookup"><span data-stu-id="5c428-105">glGetTexLevelParameterfv function</span></span>

<span data-ttu-id="5c428-106">Le funzioni **glGetTexLevelParameterfv** e [**glGetTexLevelParameteriv**](glgettexlevelparameteriv.md) restituiscono i valori dei parametri di trama per un livello di dettaglio specifico.</span><span class="sxs-lookup"><span data-stu-id="5c428-106">The **glGetTexLevelParameterfv** and [**glGetTexLevelParameteriv**](glgettexlevelparameteriv.md) functions return texture parameter values for a specific level of detail.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c428-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c428-107">Syntax</span></span>


```C++
void WINAPI glGetTexLevelParameterfv(
   GLenum  target,
   GLint   level,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="5c428-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c428-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c428-109">*target*</span><span class="sxs-lookup"><span data-stu-id="5c428-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="5c428-110">Il nome simbolico della trama di destinazione: GL \_ texture \_ 1D, GL \_ texture \_ 2D, GL \_ proxy \_ texture \_ 1D o GL \_ proxy \_ texture \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="5c428-110">The symbolic name of the target texture: either GL\_TEXTURE\_1D, GL\_TEXTURE\_2D, GL\_PROXY\_TEXTURE\_1D, or GL\_PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="5c428-111">*level*</span><span class="sxs-lookup"><span data-stu-id="5c428-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="5c428-112">Il numero del livello di dettaglio dell'immagine desiderata.</span><span class="sxs-lookup"><span data-stu-id="5c428-112">The level-of-detail number of the desired image.</span></span> <span data-ttu-id="5c428-113">Il livello 0 è il livello dell'immagine di base.</span><span class="sxs-lookup"><span data-stu-id="5c428-113">Level 0 is the base image level.</span></span> <span data-ttu-id="5c428-114">Il livello *n* è l'immagine di riduzione del mipmap *n*.</span><span class="sxs-lookup"><span data-stu-id="5c428-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="5c428-115">*pname*</span><span class="sxs-lookup"><span data-stu-id="5c428-115">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="5c428-116">Nome simbolico di un parametro di trama.</span><span class="sxs-lookup"><span data-stu-id="5c428-116">The symbolic name of a texture parameter.</span></span> <span data-ttu-id="5c428-117">I nomi di parametro seguenti sono accettati.</span><span class="sxs-lookup"><span data-stu-id="5c428-117">The following parameter names are accepted.</span></span>



| <span data-ttu-id="5c428-118">Valore</span><span class="sxs-lookup"><span data-stu-id="5c428-118">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="5c428-119">Significato</span><span class="sxs-lookup"><span data-stu-id="5c428-119">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span><dl> <span data-ttu-id="5c428-120"><dt>**\_spessore trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5c428-120"><dt>**GL\_TEXTURE\_WIDTH**</dt></span></span> </dl>                                | <span data-ttu-id="5c428-121">Il parametro *params* restituisce un singolo valore contenente la larghezza dell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="5c428-121">The *params* parameter returns a single value containing the width of the texture image.</span></span> <span data-ttu-id="5c428-122">Questo valore include il bordo dell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="5c428-122">This value includes the border of the texture image.</span></span><br/>                                                                                                                                          |
| <span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span><dl> <span data-ttu-id="5c428-123"><dt>**\_altezza trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5c428-123"><dt>**GL\_TEXTURE\_HEIGHT**</dt></span></span> </dl>                             | <span data-ttu-id="5c428-124">Il parametro *params* restituisce un singolo valore contenente l'altezza dell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="5c428-124">The *params* parameter returns a single value containing the height of the texture image.</span></span> <span data-ttu-id="5c428-125">Questo valore include il bordo dell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="5c428-125">This value includes the border of the texture image.</span></span><br/>                                                                                                                                         |
| <span id="GL_TEXTURE_INTERNAL_FORMAT"></span><span id="gl_texture_internal_format"></span><dl> <span data-ttu-id="5c428-126"><dt>**\_ \_ formato interno trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5c428-126"><dt>**GL\_TEXTURE\_INTERNAL\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="5c428-127">Il parametro *params* restituisce un singolo valore che descrive il formato di Texel della trama.</span><span class="sxs-lookup"><span data-stu-id="5c428-127">The *params* parameter returns a single value which describes the texel format of the texture.</span></span><br/>                                                                                                                                                                                         |
| <span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span><dl> <span data-ttu-id="5c428-128"><dt>**\_bordo trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5c428-128"><dt>**GL\_TEXTURE\_BORDER**</dt></span></span> </dl>                             | <span data-ttu-id="5c428-129">Il parametro *params* restituisce un singolo valore, ovvero la larghezza, in pixel, del bordo dell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="5c428-129">The *params* parameter returns a single value: the width in pixels of the border of the texture image.</span></span><br/>                                                                                                                                                                                 |
| <span id="GL_TEXTURE_RED_SIZE"></span><span id="gl_texture_red_size"></span><dl> <span data-ttu-id="5c428-130"><dt>**\_ \_ dimensioni rosse trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5c428-130"><dt>**GL\_TEXTURE\_RED\_SIZE**</dt></span></span> </dl>                      | <span data-ttu-id="5c428-131">Risoluzione dell'archiviazione interna del componente rosso di un Texel.</span><span class="sxs-lookup"><span data-stu-id="5c428-131">The internal storage resolution of the red component of a texel.</span></span> <span data-ttu-id="5c428-132">La risoluzione scelta da OpenGL sarà una corrispondenza di chiusura per la risoluzione richiesta dall'utente con l'argomento Component di [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="5c428-132">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>       |
| <span id="GL_TEXTURE_GREEN_SIZE"></span><span id="gl_texture_green_size"></span><dl> <span data-ttu-id="5c428-133"><dt>**\_ \_ dimensioni verdi trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5c428-133"><dt>**GL\_TEXTURE\_GREEN\_SIZE**</dt></span></span> </dl>                | <span data-ttu-id="5c428-134">Risoluzione dell'archiviazione interna del componente verde di un Texel.</span><span class="sxs-lookup"><span data-stu-id="5c428-134">The internal storage resolution of the green component of a texel.</span></span> <span data-ttu-id="5c428-135">La risoluzione scelta da OpenGL sarà una corrispondenza di chiusura per la risoluzione richiesta dall'utente con l'argomento Component di [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="5c428-135">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>     |
| <span id="GL_TEXTURE_BLUE_SIZE"></span><span id="gl_texture_blue_size"></span><dl> <span data-ttu-id="5c428-136"><dt>**\_ \_ dimensioni blu trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5c428-136"><dt>**GL\_TEXTURE\_BLUE\_SIZE**</dt></span></span> </dl>                   | <span data-ttu-id="5c428-137">Risoluzione dell'archiviazione interna del componente blu di un Texel.</span><span class="sxs-lookup"><span data-stu-id="5c428-137">The internal storage resolution of the blue component of a texel.</span></span> <span data-ttu-id="5c428-138">La risoluzione scelta da OpenGL sarà una corrispondenza di chiusura per la risoluzione richiesta dall'utente con l'argomento Component di [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="5c428-138">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>      |
| <span id="GL_TEXTURE_ALPHA_SIZE"></span><span id="gl_texture_alpha_size"></span><dl> <span data-ttu-id="5c428-139"><dt>**\_ \_ dimensioni alfa trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="5c428-139"><dt>**GL\_TEXTURE\_ALPHA\_SIZE**</dt></span></span> </dl>                | <span data-ttu-id="5c428-140">Risoluzione dell'archiviazione interna del componente alfa di un Texel.</span><span class="sxs-lookup"><span data-stu-id="5c428-140">The internal storage resolution of the alpha component of a texel.</span></span> <span data-ttu-id="5c428-141">La risoluzione scelta da OpenGL sarà una corrispondenza di chiusura per la risoluzione richiesta dall'utente con l'argomento Component di [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="5c428-141">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>     |
| <span id="GL_TEXTURE_LUMINANCE_SIZE"></span><span id="gl_texture_luminance_size"></span><dl> <span data-ttu-id="5c428-142"><dt>**\_ \_ dimensioni luminanza trama GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5c428-142"><dt>**GL\_TEXTURE\_LUMINANCE\_SIZE**</dt></span></span> </dl>    | <span data-ttu-id="5c428-143">Risoluzione dell'archiviazione interna del componente luminanza di un Texel.</span><span class="sxs-lookup"><span data-stu-id="5c428-143">The internal storage resolution of the luminance component of a texel.</span></span> <span data-ttu-id="5c428-144">La risoluzione scelta da OpenGL sarà una corrispondenza di chiusura per la risoluzione richiesta dall'utente con l'argomento Component di [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="5c428-144">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/> |
| <span id="GL_TEXTURE_INTENSITY_SIZE"></span><span id="gl_texture_intensity_size"></span><dl> <span data-ttu-id="5c428-145"><dt>**\_dimensioni dell' \_ intensità della trama GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5c428-145"><dt>**GL\_TEXTURE\_INTENSITY\_SIZE**</dt></span></span> </dl>    | <span data-ttu-id="5c428-146">Risoluzione dell'archiviazione interna del componente Intensity di un Texel.</span><span class="sxs-lookup"><span data-stu-id="5c428-146">The internal storage resolution of the intensity component of a texel.</span></span> <span data-ttu-id="5c428-147">La risoluzione scelta da OpenGL sarà una corrispondenza di chiusura per la risoluzione richiesta dall'utente con l'argomento Component di [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="5c428-147">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/> |
| <span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span><dl> <span data-ttu-id="5c428-148"><dt>**\_componenti di trama GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5c428-148"><dt>**GL\_TEXTURE\_COMPONENTS**</dt></span></span> </dl>                 | <span data-ttu-id="5c428-149">Il parametro *params* restituisce un singolo valore, ovvero il numero di componenti nell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="5c428-149">The *params* parameter returns a single value: the number of components in the texture image.</span></span><br/>                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="5c428-150">*params*</span><span class="sxs-lookup"><span data-stu-id="5c428-150">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="5c428-151">Restituisce i dati richiesti.</span><span class="sxs-lookup"><span data-stu-id="5c428-151">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c428-152">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c428-152">Return value</span></span>

<span data-ttu-id="5c428-153">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="5c428-153">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5c428-154">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="5c428-154">Error codes</span></span>

<span data-ttu-id="5c428-155">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="5c428-155">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5c428-156">Nome</span><span class="sxs-lookup"><span data-stu-id="5c428-156">Name</span></span>                                                                                                  | <span data-ttu-id="5c428-157">Significato</span><span class="sxs-lookup"><span data-stu-id="5c428-157">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5c428-158"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5c428-158"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="5c428-159">*target* o *pname* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="5c428-159">*target* or *pname* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="5c428-160"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5c428-160"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="5c428-161">il *livello* è minore di zero o maggiore di *log* 2 *(max)*, dove *Max* è il valore restituito della \_ dimensione della trama GL Max \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5c428-161">*level* is less than zero or greater than *log* 2 *(max)*, where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>      |
| <dl> <span data-ttu-id="5c428-162"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5c428-162"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5c428-163">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="5c428-163">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5c428-164">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c428-164">Remarks</span></span>

<span data-ttu-id="5c428-165">La funzione **glGetTexLevelParameter** restituisce i valori dei parametri di trama di *params* per un valore specifico del livello di dettaglio, specificato come *Level*.</span><span class="sxs-lookup"><span data-stu-id="5c428-165">The **glGetTexLevelParameter** function returns in *params* texture parameter values for a specific level-of-detail value, specified as *level*.</span></span> <span data-ttu-id="5c428-166">Il parametro *target* definisce la trama di destinazione, ovvero GL \_ texture \_ 1D, GL \_ texture \_ 2D, GL \_ proxy \_ texture \_ 1D o GL \_ proxy \_ texture \_ 2D per specificare il texturing unidimensionale o bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="5c428-166">The *target* parameter defines the target texture, either GL\_TEXTURE\_1D, GL\_TEXTURE\_2D, GL\_PROXY\_TEXTURE\_1D, or GL\_PROXY\_TEXTURE\_2D to specify one-dimensional or two-dimensional texturing.</span></span> <span data-ttu-id="5c428-167">Il parametro *pname* specifica il parametro della trama il cui valore o i valori verranno restituiti.</span><span class="sxs-lookup"><span data-stu-id="5c428-167">The *pname* parameter specifies the texture parameter whose value or values will be returned.</span></span>

<span data-ttu-id="5c428-168">Se viene generato un errore, non viene apportata alcuna modifica al contenuto di *params*.</span><span class="sxs-lookup"><span data-stu-id="5c428-168">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c428-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c428-169">Requirements</span></span>



| <span data-ttu-id="5c428-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c428-170">Requirement</span></span> | <span data-ttu-id="5c428-171">Valore</span><span class="sxs-lookup"><span data-stu-id="5c428-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c428-172">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c428-172">Minimum supported client</span></span><br/> | <span data-ttu-id="5c428-173">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5c428-173">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5c428-174">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c428-174">Minimum supported server</span></span><br/> | <span data-ttu-id="5c428-175">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5c428-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5c428-176">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c428-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c428-177"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c428-177"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5c428-178">Libreria</span><span class="sxs-lookup"><span data-stu-id="5c428-178">Library</span></span><br/>                  | <dl> <span data-ttu-id="5c428-179"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c428-179"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5c428-180">DLL</span><span class="sxs-lookup"><span data-stu-id="5c428-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c428-181"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c428-181"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c428-182">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c428-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c428-183">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5c428-183">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5c428-184">**Remo**</span><span class="sxs-lookup"><span data-stu-id="5c428-184">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5c428-185">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="5c428-185">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="5c428-186">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="5c428-186">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="5c428-187">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="5c428-187">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="5c428-188">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="5c428-188">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





