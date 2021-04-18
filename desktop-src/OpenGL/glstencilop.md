---
title: funzione glStencilOp (GL. h)
description: La funzione glStencilOp imposta le azioni di test dello stencil.
ms.assetid: 16809735-5624-49cf-bfa5-9908d008b234
keywords:
- funzione glStencilOp OpenGL
topic_type:
- apiref
api_name:
- glStencilOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b23162f8606ed68dc90a0cb6debdcc903e0ccd0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302190"
---
# <a name="glstencilop-function"></a><span data-ttu-id="13c58-104">glStencilOp (funzione)</span><span class="sxs-lookup"><span data-stu-id="13c58-104">glStencilOp function</span></span>

<span data-ttu-id="13c58-105">La funzione **glStencilOp** imposta le azioni di test dello stencil.</span><span class="sxs-lookup"><span data-stu-id="13c58-105">The **glStencilOp** function sets the stencil test actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="13c58-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13c58-106">Syntax</span></span>


```C++
void WINAPI glStencilOp(
   GLenum fail,
   GLenum zfail,
   GLenum zpass
);
```



## <a name="parameters"></a><span data-ttu-id="13c58-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="13c58-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13c58-108">*esito negativo*</span><span class="sxs-lookup"><span data-stu-id="13c58-108">*fail*</span></span> 
</dt> <dd>

<span data-ttu-id="13c58-109">Azione da intraprendere quando il test di stencil ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="13c58-109">The action to take when the stencil test fails.</span></span> <span data-ttu-id="13c58-110">Vengono accettate le sei costanti simboliche seguenti.</span><span class="sxs-lookup"><span data-stu-id="13c58-110">The following six symbolic constants are accepted.</span></span>



| <span data-ttu-id="13c58-111">Valore</span><span class="sxs-lookup"><span data-stu-id="13c58-111">Value</span></span>                                                                                                                                                | <span data-ttu-id="13c58-112">Significato</span><span class="sxs-lookup"><span data-stu-id="13c58-112">Meaning</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="GL_KEEP"></span><span id="gl_keep"></span><dl> <span data-ttu-id="13c58-113"><dt>**\_conservazione GL**</dt></span><span class="sxs-lookup"><span data-stu-id="13c58-113"><dt>**GL\_KEEP**</dt></span></span> </dl>          | <span data-ttu-id="13c58-114">Mantiene il valore corrente.</span><span class="sxs-lookup"><span data-stu-id="13c58-114">Keeps the current value.</span></span><br/>                                                                         |
| <span id="GL_ZERO"></span><span id="gl_zero"></span><dl> <span data-ttu-id="13c58-115"><dt>**\_zero GL**</dt></span><span class="sxs-lookup"><span data-stu-id="13c58-115"><dt>**GL\_ZERO**</dt></span></span> </dl>          | <span data-ttu-id="13c58-116">Imposta il valore del buffer dello stencil su zero.</span><span class="sxs-lookup"><span data-stu-id="13c58-116">Sets the stencil buffer value to zero.</span></span><br/>                                                           |
| <span id="GL_REPLACE"></span><span id="gl_replace"></span><dl> <span data-ttu-id="13c58-117"><dt>**\_sostituzione GL**</dt></span><span class="sxs-lookup"><span data-stu-id="13c58-117"><dt>**GL\_REPLACE**</dt></span></span> </dl> | <span data-ttu-id="13c58-118">Imposta il valore del buffer dello stencil su *ref*, come specificato da **glStencilFunc**.</span><span class="sxs-lookup"><span data-stu-id="13c58-118">Sets the stencil buffer value to *ref*, as specified by **glStencilFunc**.</span></span><br/>                       |
| <span id="GL_INCR"></span><span id="gl_incr"></span><dl> <span data-ttu-id="13c58-119"><dt>**\_incr GL**</dt></span><span class="sxs-lookup"><span data-stu-id="13c58-119"><dt>**GL\_INCR**</dt></span></span> </dl>          | <span data-ttu-id="13c58-120">Incrementa il valore del buffer dello stencil corrente.</span><span class="sxs-lookup"><span data-stu-id="13c58-120">Increments the current stencil buffer value.</span></span> <span data-ttu-id="13c58-121">Si blocca al valore unsignable massimo rappresentabile.</span><span class="sxs-lookup"><span data-stu-id="13c58-121">Clamps to the maximum representable unsigned value.</span></span><br/> |
| <span id="GL_DECR"></span><span id="gl_decr"></span><dl> <span data-ttu-id="13c58-122"><dt>**\_Decr GL**</dt></span><span class="sxs-lookup"><span data-stu-id="13c58-122"><dt>**GL\_DECR**</dt></span></span> </dl>          | <span data-ttu-id="13c58-123">Decrementa il valore del buffer dello stencil corrente.</span><span class="sxs-lookup"><span data-stu-id="13c58-123">Decrements the current stencil buffer value.</span></span> <span data-ttu-id="13c58-124">Morsetti a zero.</span><span class="sxs-lookup"><span data-stu-id="13c58-124">Clamps to zero.</span></span><br/>                                     |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <span data-ttu-id="13c58-125"><dt>**GL \_ invertiti**</dt></span><span class="sxs-lookup"><span data-stu-id="13c58-125"><dt>**GL\_INVERT**</dt></span></span> </dl>    | <span data-ttu-id="13c58-126">Bit per bit il valore del buffer dello stencil corrente viene invertito.</span><span class="sxs-lookup"><span data-stu-id="13c58-126">Bitwise inverts the current stencil buffer value.</span></span><br/>                                                |



 

</dd> <dt>

<span data-ttu-id="13c58-127">*zfail*</span><span class="sxs-lookup"><span data-stu-id="13c58-127">*zfail*</span></span> 
</dt> <dd>

<span data-ttu-id="13c58-128">Azione dello stencil quando il test di stencil viene superato, ma il test di profondità non riesce.</span><span class="sxs-lookup"><span data-stu-id="13c58-128">Stencil action when the stencil test passes, but the depth test fails.</span></span> <span data-ttu-id="13c58-129">Accetta le stesse costanti simboliche di *Fail.*</span><span class="sxs-lookup"><span data-stu-id="13c58-129">Accepts the same symbolic constants as *fail.*</span></span>

</dd> <dt>

<span data-ttu-id="13c58-130">*zpass*</span><span class="sxs-lookup"><span data-stu-id="13c58-130">*zpass*</span></span> 
</dt> <dd>

<span data-ttu-id="13c58-131">Azione stencil quando il test di stencil e il test di profondità superano o quando il test di stencil viene superato e non è stato abilitato alcun buffer di profondità o test di profondità.</span><span class="sxs-lookup"><span data-stu-id="13c58-131">Stencil action when both the stencil test and the depth test pass, or when the stencil test passes and either there is no depth buffer or depth testing is not enabled.</span></span> <span data-ttu-id="13c58-132">Accetta le stesse costanti simboliche di *Fail*.</span><span class="sxs-lookup"><span data-stu-id="13c58-132">Accepts the same symbolic constants as *fail*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13c58-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="13c58-133">Return value</span></span>

<span data-ttu-id="13c58-134">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="13c58-134">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="13c58-135">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="13c58-135">Error codes</span></span>

<span data-ttu-id="13c58-136">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="13c58-136">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="13c58-137">Nome</span><span class="sxs-lookup"><span data-stu-id="13c58-137">Name</span></span>                                                                                                  | <span data-ttu-id="13c58-138">Significato</span><span class="sxs-lookup"><span data-stu-id="13c58-138">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="13c58-139"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="13c58-139"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="13c58-140">*Fail*, *zfail* o *ZPass* è un valore qualsiasi diverso da sei valori costanti definiti.</span><span class="sxs-lookup"><span data-stu-id="13c58-140">*fail*, *zfail*, or *zpass* was any value other than the six defined constant values.</span></span><br/>                                      |
| <dl> <span data-ttu-id="13c58-141"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="13c58-141"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="13c58-142">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="13c58-142">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="13c58-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="13c58-143">Remarks</span></span>

<span data-ttu-id="13c58-144">La creazione di stencil, ad esempio il buffer *z*, Abilita e Disabilita il disegno in base ai singoli pixel.</span><span class="sxs-lookup"><span data-stu-id="13c58-144">Stenciling, like *z*-buffering, enables and disables drawing on a per-pixel basis.</span></span> <span data-ttu-id="13c58-145">Si disegnano i piani stencil usando le primitive di disegno OpenGL, quindi si esegue il rendering di geometria e immagini, usando i piani degli stencil per mascherare parti dello schermo.</span><span class="sxs-lookup"><span data-stu-id="13c58-145">You draw into the stencil planes using OpenGL drawing primitives, then render geometry and images, using the stencil planes to mask out portions of the screen.</span></span> <span data-ttu-id="13c58-146">Lo stencil viene in genere usato negli algoritmi di rendering multipass per ottenere effetti speciali, ad esempio decalcomanie, struttura e rendering di geometria continua costruttiva.</span><span class="sxs-lookup"><span data-stu-id="13c58-146">Stenciling is typically used in multipass rendering algorithms to achieve special effects, such as decals, outlining, and constructive solid geometry rendering.</span></span>

<span data-ttu-id="13c58-147">Il test di stencil Elimina in modo condizionale un pixel in base al risultato di un confronto tra il valore nel buffer dello stencil e un valore di riferimento.</span><span class="sxs-lookup"><span data-stu-id="13c58-147">The stencil test conditionally eliminates a pixel based on the outcome of a comparison between the value in the stencil buffer and a reference value.</span></span> <span data-ttu-id="13c58-148">Il test è abilitato con le chiamate [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) con il test di stencil GL degli argomenti \_ \_ e controllato con [**glStencilFunc**](glstencilfunc.md).</span><span class="sxs-lookup"><span data-stu-id="13c58-148">The test is enabled with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) calls with argument GL\_STENCIL\_TEST, and controlled with [**glStencilFunc**](glstencilfunc.md).</span></span>

<span data-ttu-id="13c58-149">La funzione **glStencilOp** accetta tre argomenti che indicano cosa accade al valore dello stencil archiviato mentre è abilitato lo stencil.</span><span class="sxs-lookup"><span data-stu-id="13c58-149">The **glStencilOp** function takes three arguments that indicate what happens to the stored stencil value while stenciling is enabled.</span></span> <span data-ttu-id="13c58-150">Se il test di stencil ha esito negativo, non viene apportata alcuna modifica ai buffer di colore o profondità del pixel e l'operazione ha *esito negativo* indica cosa accade al contenuto del buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="13c58-150">If the stencil test fails, no change is made to the pixel's color or depth buffers, and *fail* specifies what happens to the stencil buffer contents.</span></span>

<span data-ttu-id="13c58-151">I valori del buffer dello stencil vengono considerati come interi senza segno.</span><span class="sxs-lookup"><span data-stu-id="13c58-151">Stencil buffer values are treated as unsigned integers.</span></span> <span data-ttu-id="13c58-152">Quando viene incrementato e decrementato, i valori vengono fissati a 0 e 2 *n* 1, dove *n* è il valore restituito dall'esecuzione di una query sui bit dello \_ stencil GL \_ .</span><span class="sxs-lookup"><span data-stu-id="13c58-152">When incremented and decremented, values are clamped to 0 and 2 *n* 1, where *n* is the value returned by querying GL\_STENCIL\_BITS.</span></span>

<span data-ttu-id="13c58-153">Gli altri due argomenti per **glStencilOp** specificano le azioni del buffer dello stencil dovrebbero avere esito positivo dei test del buffer di profondità (*ZPass*) o Fail (*zfail*).</span><span class="sxs-lookup"><span data-stu-id="13c58-153">The other two arguments to **glStencilOp** specify stencil buffer actions should subsequent depth buffer tests succeed (*zpass*) or fail (*zfail*).</span></span> <span data-ttu-id="13c58-154">Vedere [**glDepthFunc**](gldepthfunc.md). Vengono specificati con le stesse sei costanti simboliche di *non riuscite*.</span><span class="sxs-lookup"><span data-stu-id="13c58-154">(See [**glDepthFunc**](gldepthfunc.md).) They are specified using the same six symbolic constants as *fail*.</span></span> <span data-ttu-id="13c58-155">Si noti che *zfail* viene ignorato quando non è presente alcun buffer di profondità o quando il buffer di profondità non è abilitato.</span><span class="sxs-lookup"><span data-stu-id="13c58-155">Note that *zfail* is ignored when there is no depth buffer, or when the depth buffer is not enabled.</span></span> <span data-ttu-id="13c58-156">In questi casi, *Fail* e *ZPass* specificano l'azione dello stencil quando il test di stencil ha esito negativo e passa rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="13c58-156">In these cases, *fail* and *zpass* specify stencil action when the stencil test fails and passes, respectively.</span></span>

<span data-ttu-id="13c58-157">Inizialmente il test di stencil è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="13c58-157">Initially the stencil test is disabled.</span></span> <span data-ttu-id="13c58-158">Se non è presente alcun buffer dello stencil, non può verificarsi alcuna modifica dello stencil ed è come se i test di stencil fossero sempre passati, indipendentemente da qualsiasi chiamata a **glStencilOp**.</span><span class="sxs-lookup"><span data-stu-id="13c58-158">If there is no stencil buffer, no stencil modification can occur and it is as if the stencil tests always pass, regardless of any call to **glStencilOp**.</span></span>

<span data-ttu-id="13c58-159">Le funzioni seguenti consentono di recuperare informazioni correlate a **glStencilOp**:</span><span class="sxs-lookup"><span data-stu-id="13c58-159">The following functions retrieve information related to **glStencilOp**:</span></span>

<span data-ttu-id="13c58-160">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con stencil GL \_ argomento \_ non riuscito</span><span class="sxs-lookup"><span data-stu-id="13c58-160">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_STENCIL\_FAIL</span></span>

<span data-ttu-id="13c58-161">**glGet** con passaggio di \_ \_ profondità del passaggio dello stencil di \_ argomento GL \_</span><span class="sxs-lookup"><span data-stu-id="13c58-161">**glGet** with argument GL\_STENCIL\_PASS\_DEPTH\_PASS</span></span>

<span data-ttu-id="13c58-162">**glGet** con errore di \_ \_ profondità di passaggio dello stencil GL \_ argomento \_</span><span class="sxs-lookup"><span data-stu-id="13c58-162">**glGet** with argument GL\_STENCIL\_PASS\_DEPTH\_FAIL</span></span>

<span data-ttu-id="13c58-163">**glGet** con \_ bit stencil GL \_ argomento</span><span class="sxs-lookup"><span data-stu-id="13c58-163">**glGet** with argument GL\_STENCIL\_BITS</span></span>

<span data-ttu-id="13c58-164">[**glIsEnabled**](glisenabled.md) con \_ test stencil GL \_ argomento</span><span class="sxs-lookup"><span data-stu-id="13c58-164">[**glIsEnabled**](glisenabled.md) with argument GL\_STENCIL\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="13c58-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13c58-165">Requirements</span></span>



| <span data-ttu-id="13c58-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="13c58-166">Requirement</span></span> | <span data-ttu-id="13c58-167">Valore</span><span class="sxs-lookup"><span data-stu-id="13c58-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13c58-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13c58-168">Minimum supported client</span></span><br/> | <span data-ttu-id="13c58-169">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="13c58-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="13c58-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="13c58-170">Minimum supported server</span></span><br/> | <span data-ttu-id="13c58-171">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="13c58-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="13c58-172">Intestazione</span><span class="sxs-lookup"><span data-stu-id="13c58-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="13c58-173"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="13c58-173"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="13c58-174">Libreria</span><span class="sxs-lookup"><span data-stu-id="13c58-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="13c58-175"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13c58-175"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="13c58-176">DLL</span><span class="sxs-lookup"><span data-stu-id="13c58-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13c58-177"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13c58-177"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13c58-178">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13c58-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13c58-179">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="13c58-179">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="13c58-180">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="13c58-180">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="13c58-181">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="13c58-181">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="13c58-182">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="13c58-182">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="13c58-183">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="13c58-183">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="13c58-184">**Remo**</span><span class="sxs-lookup"><span data-stu-id="13c58-184">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="13c58-185">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="13c58-185">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="13c58-186">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="13c58-186">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="13c58-187">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="13c58-187">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





