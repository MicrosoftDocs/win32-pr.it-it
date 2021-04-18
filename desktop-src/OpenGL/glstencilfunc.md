---
title: funzione glStencilFunc (GL. h)
description: La funzione glStencilFunc imposta la funzione e il valore di riferimento per il test di stencil.
ms.assetid: 6c84415b-4d22-494b-90f2-6243d1406725
keywords:
- funzione glStencilFunc OpenGL
topic_type:
- apiref
api_name:
- glStencilFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd4f9c0a5ec905ecb061ddb54984bf35ff8edc3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302706"
---
# <a name="glstencilfunc-function"></a><span data-ttu-id="0a37b-104">glStencilFunc (funzione)</span><span class="sxs-lookup"><span data-stu-id="0a37b-104">glStencilFunc function</span></span>

<span data-ttu-id="0a37b-105">La funzione **glStencilFunc** imposta la funzione e il valore di riferimento per il test di stencil.</span><span class="sxs-lookup"><span data-stu-id="0a37b-105">The **glStencilFunc** function sets the function and reference value for stencil testing.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a37b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0a37b-106">Syntax</span></span>


```C++
void WINAPI glStencilFunc(
   GLenum func,
   GLint  ref,
   GLuint mask
);
```



## <a name="parameters"></a><span data-ttu-id="0a37b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="0a37b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a37b-108">*func*</span><span class="sxs-lookup"><span data-stu-id="0a37b-108">*func*</span></span> 
</dt> <dd>

<span data-ttu-id="0a37b-109">Funzione di test.</span><span class="sxs-lookup"><span data-stu-id="0a37b-109">The test function.</span></span> <span data-ttu-id="0a37b-110">I seguenti otto token sono validi.</span><span class="sxs-lookup"><span data-stu-id="0a37b-110">The following eight tokens are valid.</span></span>



| <span data-ttu-id="0a37b-111">Valore</span><span class="sxs-lookup"><span data-stu-id="0a37b-111">Value</span></span>                                                                                                                                                   | <span data-ttu-id="0a37b-112">Significato</span><span class="sxs-lookup"><span data-stu-id="0a37b-112">Meaning</span></span>                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <span data-ttu-id="0a37b-113"><dt>**GL \_ mai**</dt></span><span class="sxs-lookup"><span data-stu-id="0a37b-113"><dt>**GL\_NEVER**</dt></span></span> </dl>          | <span data-ttu-id="0a37b-114">Ha sempre esito negativo.</span><span class="sxs-lookup"><span data-stu-id="0a37b-114">Always fails.</span></span><br/>                                         |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <span data-ttu-id="0a37b-115"><dt>**\_meno GL**</dt></span><span class="sxs-lookup"><span data-stu-id="0a37b-115"><dt>**GL\_LESS**</dt></span></span> </dl>             | <span data-ttu-id="0a37b-116">Passa se (  &  *maschera* di riferimento) < (maschera di *stencil*  &  ).</span><span class="sxs-lookup"><span data-stu-id="0a37b-116">Passes if (*ref* & *mask*) < (*stencil* & *mask*).</span></span><br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <span data-ttu-id="0a37b-117"><dt>**\_LEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="0a37b-117"><dt>**GL\_LEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="0a37b-118">Passa se (*ref*  &  *mask*) = (  &  *maschera* di stencil).</span><span class="sxs-lookup"><span data-stu-id="0a37b-118">Passes if (*ref* & *mask*) = (*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <span data-ttu-id="0a37b-119"><dt>**maggiore di GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0a37b-119"><dt>**GL\_GREATER**</dt></span></span> </dl>    | <span data-ttu-id="0a37b-120">Passa se (  &  *maschera* di riferimento) > (maschera di *stencil*  &  ).</span><span class="sxs-lookup"><span data-stu-id="0a37b-120">Passes if (*ref* & *mask*) > (*stencil* & *mask*).</span></span><br/> |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <span data-ttu-id="0a37b-121"><dt>**\_GEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="0a37b-121"><dt>**GL\_GEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="0a37b-122">Passa se (*ref*  &  *mask*) = (  &  *maschera* di stencil).</span><span class="sxs-lookup"><span data-stu-id="0a37b-122">Passes if (*ref* & *mask*) = (*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <span data-ttu-id="0a37b-123"><dt>**GL \_ uguale**</dt></span><span class="sxs-lookup"><span data-stu-id="0a37b-123"><dt>**GL\_EQUAL**</dt></span></span> </dl>          | <span data-ttu-id="0a37b-124">Passa se (*ref*  &  *mask*) = (  &  *maschera* di stencil).</span><span class="sxs-lookup"><span data-stu-id="0a37b-124">Passes if (*ref* & *mask*) = (*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <span data-ttu-id="0a37b-125"><dt>**\_NOTEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="0a37b-125"><dt>**GL\_NOTEQUAL**</dt></span></span> </dl> | <span data-ttu-id="0a37b-126">Passa se (*ref*  &  *mask*)?</span><span class="sxs-lookup"><span data-stu-id="0a37b-126">Passes if (*ref* & *mask*) ?</span></span> <span data-ttu-id="0a37b-127">(*stencil*  &  *mask*).</span><span class="sxs-lookup"><span data-stu-id="0a37b-127">(*stencil* & *mask*).</span></span><br/>    |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <span data-ttu-id="0a37b-128"><dt>**GL \_ Always**</dt></span><span class="sxs-lookup"><span data-stu-id="0a37b-128"><dt>**GL\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="0a37b-129">Passa sempre.</span><span class="sxs-lookup"><span data-stu-id="0a37b-129">Always passes.</span></span><br/>                                        |



 

</dd> <dt>

<span data-ttu-id="0a37b-130">*ref*</span><span class="sxs-lookup"><span data-stu-id="0a37b-130">*ref*</span></span> 
</dt> <dd>

<span data-ttu-id="0a37b-131">Valore di riferimento per il test di stencil.</span><span class="sxs-lookup"><span data-stu-id="0a37b-131">The reference value for the stencil test.</span></span> <span data-ttu-id="0a37b-132">Il parametro *ref* viene bloccato nell'intervallo \[ 0, 2 *n* 1 \] , dove *n* è il numero di bitplane nel buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="0a37b-132">The *ref* parameter is clamped to the range \[0, 2 *n* 1\], where *n* is the number of bitplanes in the stencil buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0a37b-133">*maschera*</span><span class="sxs-lookup"><span data-stu-id="0a37b-133">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="0a37b-134">Maschera che è **e** ed è il valore di riferimento e il valore dello stencil archiviato al termine del test.</span><span class="sxs-lookup"><span data-stu-id="0a37b-134">A mask that is **AND** ed with both the reference value and the stored stencil value when the test is done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a37b-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0a37b-135">Return value</span></span>

<span data-ttu-id="0a37b-136">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="0a37b-136">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0a37b-137">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="0a37b-137">Error codes</span></span>

<span data-ttu-id="0a37b-138">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="0a37b-138">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="0a37b-139">Nome</span><span class="sxs-lookup"><span data-stu-id="0a37b-139">Name</span></span>                                                                                                  | <span data-ttu-id="0a37b-140">Significato</span><span class="sxs-lookup"><span data-stu-id="0a37b-140">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0a37b-141"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0a37b-141"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="0a37b-142">*Func* non è uno degli otto valori accettati.</span><span class="sxs-lookup"><span data-stu-id="0a37b-142">*func* was not one of the eight accepted values.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="0a37b-143"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0a37b-143"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="0a37b-144">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="0a37b-144">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0a37b-145">Commenti</span><span class="sxs-lookup"><span data-stu-id="0a37b-145">Remarks</span></span>

<span data-ttu-id="0a37b-146">La creazione di stencil, ad esempio il buffer *z*, Abilita e Disabilita il disegno in base ai singoli pixel.</span><span class="sxs-lookup"><span data-stu-id="0a37b-146">Stenciling, like *z*-buffering, enables and disables drawing on a per-pixel basis.</span></span> <span data-ttu-id="0a37b-147">Si disegnano i piani stencil usando le primitive di disegno OpenGL, quindi si esegue il rendering di geometria e immagini, usando i piani degli stencil per mascherare parti dello schermo.</span><span class="sxs-lookup"><span data-stu-id="0a37b-147">You draw into the stencil planes using OpenGL drawing primitives, then render geometry and images, using the stencil planes to mask out portions of the screen.</span></span> <span data-ttu-id="0a37b-148">Lo stencil viene in genere usato negli algoritmi di rendering multipass per ottenere effetti speciali, ad esempio decalcomanie, struttura e rendering di geometria continua costruttiva.</span><span class="sxs-lookup"><span data-stu-id="0a37b-148">Stenciling is typically used in multipass rendering algorithms to achieve special effects, such as decals, outlining, and constructive solid geometry rendering.</span></span>

<span data-ttu-id="0a37b-149">Il test di stencil Elimina in modo condizionale un pixel in base al risultato di un confronto tra il valore di riferimento e il valore nel buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="0a37b-149">The stencil test conditionally eliminates a pixel based on the outcome of a comparison between the reference value and the value in the stencil buffer.</span></span> <span data-ttu-id="0a37b-150">Il test è abilitato da [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) con il test di stencil GL degli argomenti \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0a37b-150">The test is enabled by [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with argument GL\_STENCIL\_TEST.</span></span> <span data-ttu-id="0a37b-151">Le azioni eseguite in base al risultato del test dello stencil vengono specificate con [**glStencilOp**](glstencilop.md).</span><span class="sxs-lookup"><span data-stu-id="0a37b-151">Actions taken based on the outcome of the stencil test are specified with [**glStencilOp**](glstencilop.md).</span></span>

<span data-ttu-id="0a37b-152">Il parametro *Func* è una costante simbolica che determina la funzione di confronto dello stencil.</span><span class="sxs-lookup"><span data-stu-id="0a37b-152">The *func* parameter is a symbolic constant that determines the stencil comparison function.</span></span> <span data-ttu-id="0a37b-153">Accetta uno degli otto valori indicati sopra.</span><span class="sxs-lookup"><span data-stu-id="0a37b-153">It accepts one of the eight values shown above.</span></span> <span data-ttu-id="0a37b-154">Il parametro *ref* è un valore di riferimento integer utilizzato nel confronto tra stencil.</span><span class="sxs-lookup"><span data-stu-id="0a37b-154">The *ref* parameter is an integer reference value that is used in the stencil comparison.</span></span> <span data-ttu-id="0a37b-155">Viene premuto nell'intervallo \[ 0, 2 *n* 1 \] , dove *n* è il numero di bitplane nel buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="0a37b-155">It is clamped to the range \[0, 2 *n* 1\], where *n* is the number of bitplanes in the stencil buffer.</span></span> <span data-ttu-id="0a37b-156">Il parametro *mask* è bit per bit **e** ed è il valore di riferimento e il valore dello stencil archiviato, con i valori **e che** partecipano al confronto.</span><span class="sxs-lookup"><span data-stu-id="0a37b-156">The *mask* parameter is bitwise **AND** ed with both the reference value and the stored stencil value, with the **AND** ed values participating in the comparison.</span></span>

<span data-ttu-id="0a37b-157">Se *stencil* rappresenta il valore archiviato nella posizione del buffer dello stencil corrispondente, l'elenco precedente mostra l'effetto di ogni funzione di confronto che può essere specificata da *Func*.</span><span class="sxs-lookup"><span data-stu-id="0a37b-157">If *stencil* represents the value stored in the corresponding stencil buffer location, the preceding list shows the effect of each comparison function that can be specified by *func*.</span></span> <span data-ttu-id="0a37b-158">Solo se il confronto ha esito positivo è il pixel passato alla fase successiva nel processo di rasterizzazione (vedere [**glStencilOp**](glstencilop.md)).</span><span class="sxs-lookup"><span data-stu-id="0a37b-158">Only if the comparison succeeds is the pixel passed through to the next stage in the rasterization process (see [**glStencilOp**](glstencilop.md)).</span></span> <span data-ttu-id="0a37b-159">Tutti i test considerano i valori degli *stencil* come interi senza segno nell'intervallo \[ 0, 2 *n* 1 \] , dove *n* è il numero di bitplane nel buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="0a37b-159">All tests treat *stencil* values as unsigned integers in the range \[0, 2 *n* 1\], where *n* is the number of bitplanes in the stencil buffer.</span></span>

<span data-ttu-id="0a37b-160">Inizialmente, il test di stencil è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="0a37b-160">Initially, the stencil test is disabled.</span></span> <span data-ttu-id="0a37b-161">Se non è presente alcun buffer dello stencil, non può verificarsi alcuna modifica dello stencil ed è come se il test di stencil venisse sempre superato.</span><span class="sxs-lookup"><span data-stu-id="0a37b-161">If there is no stencil buffer, no stencil modification can occur and it is as if the stencil test always passes.</span></span>

<span data-ttu-id="0a37b-162">Le funzioni seguenti consentono di recuperare informazioni correlate a **glStencilFunc**:</span><span class="sxs-lookup"><span data-stu-id="0a37b-162">The following functions retrieve information related to **glStencilFunc**:</span></span>

<span data-ttu-id="0a37b-163">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argument GL \_ stencil \_ Func</span><span class="sxs-lookup"><span data-stu-id="0a37b-163">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_FUNC</span></span>

<span data-ttu-id="0a37b-164">**glGet** con \_ \_ maschera valore stencil GL \_ argomento</span><span class="sxs-lookup"><span data-stu-id="0a37b-164">**glGet** with argument GL\_STENCIL\_VALUE\_MASK</span></span>

<span data-ttu-id="0a37b-165">**glGet** con argomento \_ ref dello stencil GL \_</span><span class="sxs-lookup"><span data-stu-id="0a37b-165">**glGet** with argument GL\_STENCIL\_REF</span></span>

<span data-ttu-id="0a37b-166">**glGet** con \_ bit stencil GL \_ argomento</span><span class="sxs-lookup"><span data-stu-id="0a37b-166">**glGet** with argument GL\_STENCIL\_BITS</span></span>

<span data-ttu-id="0a37b-167">[**glIsEnabled**](glisenabled.md) con \_ test stencil GL \_ argomento</span><span class="sxs-lookup"><span data-stu-id="0a37b-167">[**glIsEnabled**](glisenabled.md) with argument GL\_STENCIL\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="0a37b-168">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0a37b-168">Requirements</span></span>



| <span data-ttu-id="0a37b-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a37b-169">Requirement</span></span> | <span data-ttu-id="0a37b-170">Valore</span><span class="sxs-lookup"><span data-stu-id="0a37b-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a37b-171">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a37b-171">Minimum supported client</span></span><br/> | <span data-ttu-id="0a37b-172">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0a37b-172">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0a37b-173">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0a37b-173">Minimum supported server</span></span><br/> | <span data-ttu-id="0a37b-174">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0a37b-174">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0a37b-175">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0a37b-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a37b-176"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a37b-176"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0a37b-177">Libreria</span><span class="sxs-lookup"><span data-stu-id="0a37b-177">Library</span></span><br/>                  | <dl> <span data-ttu-id="0a37b-178"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a37b-178"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0a37b-179">DLL</span><span class="sxs-lookup"><span data-stu-id="0a37b-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a37b-180"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a37b-180"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a37b-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0a37b-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a37b-182">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="0a37b-182">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="0a37b-183">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="0a37b-183">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="0a37b-184">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="0a37b-184">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="0a37b-185">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="0a37b-185">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="0a37b-186">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="0a37b-186">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="0a37b-187">**Remo**</span><span class="sxs-lookup"><span data-stu-id="0a37b-187">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="0a37b-188">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="0a37b-188">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="0a37b-189">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="0a37b-189">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="0a37b-190">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="0a37b-190">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





