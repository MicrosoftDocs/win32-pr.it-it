---
title: funzione glGetTexLevelParameteriv (GL. h)
description: Le funzioni glGetTexLevelParameterfv e glGetTexLevelParameteriv restituiscono i valori dei parametri di trama per un livello di dettaglio specifico. | funzione glGetTexLevelParameteriv (GL. h)
ms.assetid: 536d7bc9-1599-47ff-8559-374f96f1d5f3
keywords:
- funzione glGetTexLevelParameteriv OpenGL
topic_type:
- apiref
api_name:
- glGetTexLevelParameteriv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfc0fa167eae842784e967538ff1539e0b43a6a2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103969082"
---
# <a name="glgettexlevelparameteriv-function"></a><span data-ttu-id="8635e-105">glGetTexLevelParameteriv (funzione)</span><span class="sxs-lookup"><span data-stu-id="8635e-105">glGetTexLevelParameteriv function</span></span>

<span data-ttu-id="8635e-106">Le funzioni [**glGetTexLevelParameterfv**](glgettexlevelparameterfv.md) e **glGetTexLevelParameteriv** restituiscono i valori dei parametri di trama per un livello di dettaglio specifico.</span><span class="sxs-lookup"><span data-stu-id="8635e-106">The [**glGetTexLevelParameterfv**](glgettexlevelparameterfv.md) and **glGetTexLevelParameteriv** functions return texture parameter values for a specific level of detail.</span></span>

## <a name="syntax"></a><span data-ttu-id="8635e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8635e-107">Syntax</span></span>


```C++
void WINAPI glGetTexLevelParameteriv(
   GLenum target,
   GLint  level,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="8635e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="8635e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8635e-109">*target*</span><span class="sxs-lookup"><span data-stu-id="8635e-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="8635e-110">Il nome simbolico della trama di destinazione: GL \_ texture \_ 1D, GL \_ texture \_ 2D, GL \_ proxy \_ texture \_ 1D o GL \_ proxy \_ texture \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="8635e-110">The symbolic name of the target texture: either GL\_TEXTURE\_1D, GL\_TEXTURE\_2D, GL\_PROXY\_TEXTURE\_1D, or GL\_PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="8635e-111">*level*</span><span class="sxs-lookup"><span data-stu-id="8635e-111">*level*</span></span> 
</dt> <dd>

<span data-ttu-id="8635e-112">Il numero del livello di dettaglio dell'immagine desiderata.</span><span class="sxs-lookup"><span data-stu-id="8635e-112">The level-of-detail number of the desired image.</span></span> <span data-ttu-id="8635e-113">Il livello 0 è il livello dell'immagine di base.</span><span class="sxs-lookup"><span data-stu-id="8635e-113">Level 0 is the base image level.</span></span> <span data-ttu-id="8635e-114">Il livello *n* è l'immagine di riduzione del mipmap *n*.</span><span class="sxs-lookup"><span data-stu-id="8635e-114">Level *n* is the *n* th mipmap reduction image.</span></span>

</dd> <dt>

<span data-ttu-id="8635e-115">*pname*</span><span class="sxs-lookup"><span data-stu-id="8635e-115">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="8635e-116">Nome simbolico di un parametro di trama.</span><span class="sxs-lookup"><span data-stu-id="8635e-116">The symbolic name of a texture parameter.</span></span> <span data-ttu-id="8635e-117">I nomi di parametro seguenti sono accettati.</span><span class="sxs-lookup"><span data-stu-id="8635e-117">The following parameter names are accepted.</span></span>



| <span data-ttu-id="8635e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="8635e-118">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="8635e-119">Significato</span><span class="sxs-lookup"><span data-stu-id="8635e-119">Meaning</span></span>                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span><dl> <span data-ttu-id="8635e-120"><dt>**\_spessore trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8635e-120"><dt>**GL\_TEXTURE\_WIDTH**</dt></span></span> </dl>                                | <span data-ttu-id="8635e-121">Il parametro *params* restituisce un singolo valore contenente la larghezza dell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="8635e-121">The *params* parameter returns a single value containing the width of the texture image.</span></span> <span data-ttu-id="8635e-122">Questo valore include il bordo dell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="8635e-122">This value includes the border of the texture image.</span></span><br/>                                                                                                                                          |
| <span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span><dl> <span data-ttu-id="8635e-123"><dt>**\_altezza trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8635e-123"><dt>**GL\_TEXTURE\_HEIGHT**</dt></span></span> </dl>                             | <span data-ttu-id="8635e-124">Il parametro *params* restituisce un singolo valore contenente l'altezza dell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="8635e-124">The *params* parameter returns a single value containing the height of the texture image.</span></span> <span data-ttu-id="8635e-125">Questo valore include il bordo dell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="8635e-125">This value includes the border of the texture image.</span></span><br/>                                                                                                                                         |
| <span id="GL_TEXTURE_INTERNAL_FORMAT"></span><span id="gl_texture_internal_format"></span><dl> <span data-ttu-id="8635e-126"><dt>**\_ \_ formato interno trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8635e-126"><dt>**GL\_TEXTURE\_INTERNAL\_FORMAT**</dt></span></span> </dl> | <span data-ttu-id="8635e-127">Il parametro *params* restituisce un singolo valore che descrive il formato di Texel della trama.</span><span class="sxs-lookup"><span data-stu-id="8635e-127">The *params* parameter returns a single value which describes the texel format of the texture.</span></span><br/>                                                                                                                                                                                         |
| <span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span><dl> <span data-ttu-id="8635e-128"><dt>**\_bordo trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8635e-128"><dt>**GL\_TEXTURE\_BORDER**</dt></span></span> </dl>                             | <span data-ttu-id="8635e-129">Il parametro *params* restituisce un singolo valore, ovvero la larghezza, in pixel, del bordo dell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="8635e-129">The *params* parameter returns a single value: the width in pixels of the border of the texture image.</span></span><br/>                                                                                                                                                                                 |
| <span id="GL_TEXTURE_RED_SIZE"></span><span id="gl_texture_red_size"></span><dl> <span data-ttu-id="8635e-130"><dt>**\_ \_ dimensioni rosse trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8635e-130"><dt>**GL\_TEXTURE\_RED\_SIZE**</dt></span></span> </dl>                      | <span data-ttu-id="8635e-131">Risoluzione dell'archiviazione interna del componente rosso di un Texel.</span><span class="sxs-lookup"><span data-stu-id="8635e-131">The internal storage resolution of the red component of a texel.</span></span> <span data-ttu-id="8635e-132">La risoluzione scelta da OpenGL sarà una corrispondenza di chiusura per la risoluzione richiesta dall'utente con l'argomento Component di [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="8635e-132">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>       |
| <span id="GL_TEXTURE_GREEN_SIZE"></span><span id="gl_texture_green_size"></span><dl> <span data-ttu-id="8635e-133"><dt>**\_ \_ dimensioni verdi trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8635e-133"><dt>**GL\_TEXTURE\_GREEN\_SIZE**</dt></span></span> </dl>                | <span data-ttu-id="8635e-134">Risoluzione dell'archiviazione interna del componente verde di un Texel.</span><span class="sxs-lookup"><span data-stu-id="8635e-134">The internal storage resolution of the green component of a texel.</span></span> <span data-ttu-id="8635e-135">La risoluzione scelta da OpenGL sarà una corrispondenza di chiusura per la risoluzione richiesta dall'utente con l'argomento Component di [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="8635e-135">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>     |
| <span id="GL_TEXTURE_BLUE_SIZE"></span><span id="gl_texture_blue_size"></span><dl> <span data-ttu-id="8635e-136"><dt>**\_ \_ dimensioni blu trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8635e-136"><dt>**GL\_TEXTURE\_BLUE\_SIZE**</dt></span></span> </dl>                   | <span data-ttu-id="8635e-137">Risoluzione dell'archiviazione interna del componente blu di un Texel.</span><span class="sxs-lookup"><span data-stu-id="8635e-137">The internal storage resolution of the blue component of a texel.</span></span> <span data-ttu-id="8635e-138">La risoluzione scelta da OpenGL sarà una corrispondenza di chiusura per la risoluzione richiesta dall'utente con l'argomento Component di [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="8635e-138">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>      |
| <span id="GL_TEXTURE_ALPHA_SIZE"></span><span id="gl_texture_alpha_size"></span><dl> <span data-ttu-id="8635e-139"><dt>**\_ \_ dimensioni alfa trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="8635e-139"><dt>**GL\_TEXTURE\_ALPHA\_SIZE**</dt></span></span> </dl>                | <span data-ttu-id="8635e-140">Risoluzione dell'archiviazione interna del componente alfa di un Texel.</span><span class="sxs-lookup"><span data-stu-id="8635e-140">The internal storage resolution of the alpha component of a texel.</span></span> <span data-ttu-id="8635e-141">La risoluzione scelta da OpenGL sarà una corrispondenza di chiusura per la risoluzione richiesta dall'utente con l'argomento Component di [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="8635e-141">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/>     |
| <span id="GL_TEXTURE_LUMINANCE_SIZE"></span><span id="gl_texture_luminance_size"></span><dl> <span data-ttu-id="8635e-142"><dt>**\_ \_ dimensioni luminanza trama GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8635e-142"><dt>**GL\_TEXTURE\_LUMINANCE\_SIZE**</dt></span></span> </dl>    | <span data-ttu-id="8635e-143">Risoluzione dell'archiviazione interna del componente luminanza di un Texel.</span><span class="sxs-lookup"><span data-stu-id="8635e-143">The internal storage resolution of the luminance component of a texel.</span></span> <span data-ttu-id="8635e-144">La risoluzione scelta da OpenGL sarà una corrispondenza di chiusura per la risoluzione richiesta dall'utente con l'argomento Component di [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="8635e-144">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/> |
| <span id="GL_TEXTURE_INTENSITY_SIZE"></span><span id="gl_texture_intensity_size"></span><dl> <span data-ttu-id="8635e-145"><dt>**\_dimensioni dell' \_ intensità della trama GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8635e-145"><dt>**GL\_TEXTURE\_INTENSITY\_SIZE**</dt></span></span> </dl>    | <span data-ttu-id="8635e-146">Risoluzione dell'archiviazione interna del componente Intensity di un Texel.</span><span class="sxs-lookup"><span data-stu-id="8635e-146">The internal storage resolution of the intensity component of a texel.</span></span> <span data-ttu-id="8635e-147">La risoluzione scelta da OpenGL sarà una corrispondenza di chiusura per la risoluzione richiesta dall'utente con l'argomento Component di [**glTexImage1D**](glteximage1d.md) o [**glTexImage2D**](glteximage2d.md).</span><span class="sxs-lookup"><span data-stu-id="8635e-147">The resolution chosen by the OpenGL will be a close match for the resolution requested by the user with the component argument of [**glTexImage1D**](glteximage1d.md) or [**glTexImage2D**](glteximage2d.md).</span></span><br/> |
| <span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span><dl> <span data-ttu-id="8635e-148"><dt>**\_componenti di trama GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8635e-148"><dt>**GL\_TEXTURE\_COMPONENTS**</dt></span></span> </dl>                 | <span data-ttu-id="8635e-149">Il parametro *params* restituisce un singolo valore, ovvero il numero di componenti nell'immagine della trama.</span><span class="sxs-lookup"><span data-stu-id="8635e-149">The *params* parameter returns a single value: the number of components in the texture image.</span></span><br/>                                                                                                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="8635e-150">*params*</span><span class="sxs-lookup"><span data-stu-id="8635e-150">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="8635e-151">Restituisce i dati richiesti.</span><span class="sxs-lookup"><span data-stu-id="8635e-151">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8635e-152">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8635e-152">Return value</span></span>

<span data-ttu-id="8635e-153">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="8635e-153">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8635e-154">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="8635e-154">Error codes</span></span>

<span data-ttu-id="8635e-155">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="8635e-155">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="8635e-156">Nome</span><span class="sxs-lookup"><span data-stu-id="8635e-156">Name</span></span>                                                                                                  | <span data-ttu-id="8635e-157">Significato</span><span class="sxs-lookup"><span data-stu-id="8635e-157">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8635e-158"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8635e-158"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="8635e-159">*target* o *pname* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="8635e-159">*target* or *pname* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="8635e-160"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8635e-160"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="8635e-161">il *livello* è minore di zero o maggiore di *log* 2 *(max)*, dove *Max* è il valore restituito della \_ dimensione della trama GL Max \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8635e-161">*level* is less than zero or greater than *log* 2 *(max)*, where *max* is the returned value of GL\_MAX\_TEXTURE\_SIZE.</span></span><br/>      |
| <dl> <span data-ttu-id="8635e-162"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="8635e-162"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="8635e-163">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="8635e-163">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8635e-164">Commenti</span><span class="sxs-lookup"><span data-stu-id="8635e-164">Remarks</span></span>

<span data-ttu-id="8635e-165">La funzione **glGetTexLevelParameter** restituisce i valori dei parametri di trama di *params* per un valore specifico del livello di dettaglio, specificato come *Level*.</span><span class="sxs-lookup"><span data-stu-id="8635e-165">The **glGetTexLevelParameter** function returns in *params* texture parameter values for a specific level-of-detail value, specified as *level*.</span></span> <span data-ttu-id="8635e-166">Il parametro *target* definisce la trama di destinazione, ovvero GL \_ texture \_ 1D, GL \_ texture \_ 2D, GL \_ proxy \_ texture \_ 1D o GL \_ proxy \_ texture \_ 2D per specificare il texturing unidimensionale o bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="8635e-166">The *target* parameter defines the target texture, either GL\_TEXTURE\_1D, GL\_TEXTURE\_2D, GL\_PROXY\_TEXTURE\_1D, or GL\_PROXY\_TEXTURE\_2D to specify one-dimensional or two-dimensional texturing.</span></span> <span data-ttu-id="8635e-167">Il parametro *pname* specifica il parametro della trama il cui valore o i valori verranno restituiti.</span><span class="sxs-lookup"><span data-stu-id="8635e-167">The *pname* parameter specifies the texture parameter whose value or values will be returned.</span></span>

<span data-ttu-id="8635e-168">Se viene generato un errore, non viene apportata alcuna modifica al contenuto di *params*.</span><span class="sxs-lookup"><span data-stu-id="8635e-168">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="8635e-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8635e-169">Requirements</span></span>



| <span data-ttu-id="8635e-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="8635e-170">Requirement</span></span> | <span data-ttu-id="8635e-171">Valore</span><span class="sxs-lookup"><span data-stu-id="8635e-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8635e-172">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8635e-172">Minimum supported client</span></span><br/> | <span data-ttu-id="8635e-173">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8635e-173">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="8635e-174">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8635e-174">Minimum supported server</span></span><br/> | <span data-ttu-id="8635e-175">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8635e-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8635e-176">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8635e-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="8635e-177"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="8635e-177"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="8635e-178">Libreria</span><span class="sxs-lookup"><span data-stu-id="8635e-178">Library</span></span><br/>                  | <dl> <span data-ttu-id="8635e-179"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8635e-179"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8635e-180">DLL</span><span class="sxs-lookup"><span data-stu-id="8635e-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8635e-181"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8635e-181"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8635e-182">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8635e-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8635e-183">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="8635e-183">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="8635e-184">**Remo**</span><span class="sxs-lookup"><span data-stu-id="8635e-184">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="8635e-185">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="8635e-185">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="8635e-186">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="8635e-186">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="8635e-187">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="8635e-187">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> <dt>

[<span data-ttu-id="8635e-188">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="8635e-188">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





