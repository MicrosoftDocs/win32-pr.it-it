---
title: funzione glAlphaFunc (GL. h)
description: La funzione glAlphaFunc consente all'applicazione di impostare la funzione di test alfa.
ms.assetid: 6c0c06b5-1bad-4590-a262-f134f63f0936
keywords:
- funzione glAlphaFunc OpenGL
topic_type:
- apiref
api_name:
- glAlphaFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf96cfe2be0224c9c2e2409fc68805b530ae1f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301806"
---
# <a name="glalphafunc-function"></a><span data-ttu-id="2f85a-104">glAlphaFunc (funzione)</span><span class="sxs-lookup"><span data-stu-id="2f85a-104">glAlphaFunc function</span></span>

<span data-ttu-id="2f85a-105">La funzione **glAlphaFunc** consente all'applicazione di impostare la funzione di test alfa.</span><span class="sxs-lookup"><span data-stu-id="2f85a-105">The **glAlphaFunc** function enables your application to set the alpha test function.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f85a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f85a-106">Syntax</span></span>


```C++
void WINAPI glAlphaFunc(
   GLenum   func,
   GLclampf ref
);
```



## <a name="parameters"></a><span data-ttu-id="2f85a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f85a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f85a-108">*func*</span><span class="sxs-lookup"><span data-stu-id="2f85a-108">*func*</span></span> 
</dt> <dd>

<span data-ttu-id="2f85a-109">Funzione di confronto alfa.</span><span class="sxs-lookup"><span data-stu-id="2f85a-109">The alpha comparison function.</span></span> <span data-ttu-id="2f85a-110">Di seguito sono riportate le costanti simboliche accettate e i relativi significati.</span><span class="sxs-lookup"><span data-stu-id="2f85a-110">The following are the accepted symbolic constants and their meanings.</span></span>



| <span data-ttu-id="2f85a-111">Valore</span><span class="sxs-lookup"><span data-stu-id="2f85a-111">Value</span></span>                                                                                                                                                   | <span data-ttu-id="2f85a-112">Significato</span><span class="sxs-lookup"><span data-stu-id="2f85a-112">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <span data-ttu-id="2f85a-113"><dt>**GL \_ mai**</dt></span><span class="sxs-lookup"><span data-stu-id="2f85a-113"><dt>**GL\_NEVER**</dt></span></span> </dl>          | <span data-ttu-id="2f85a-114">Non viene mai passato.</span><span class="sxs-lookup"><span data-stu-id="2f85a-114">Never passes.</span></span><br/>                                                                       |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <span data-ttu-id="2f85a-115"><dt>**\_meno GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2f85a-115"><dt>**GL\_LESS**</dt></span></span> </dl>             | <span data-ttu-id="2f85a-116">Passa se il valore alfa in ingresso è minore del valore di riferimento.</span><span class="sxs-lookup"><span data-stu-id="2f85a-116">Passes if the incoming alpha value is less than the reference value.</span></span><br/>                |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <span data-ttu-id="2f85a-117"><dt>**GL \_ uguale**</dt></span><span class="sxs-lookup"><span data-stu-id="2f85a-117"><dt>**GL\_EQUAL**</dt></span></span> </dl>          | <span data-ttu-id="2f85a-118">Passa se il valore alfa in ingresso è uguale al valore di riferimento.</span><span class="sxs-lookup"><span data-stu-id="2f85a-118">Passes if the incoming alpha value is equal to the reference value.</span></span><br/>                 |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <span data-ttu-id="2f85a-119"><dt>**\_LEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2f85a-119"><dt>**GL\_LEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="2f85a-120">Passa se il valore alfa in ingresso è minore o uguale al valore di riferimento.</span><span class="sxs-lookup"><span data-stu-id="2f85a-120">Passes if the incoming alpha value is less than or equal to the reference value.</span></span><br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <span data-ttu-id="2f85a-121"><dt>**maggiore di GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2f85a-121"><dt>**GL\_GREATER**</dt></span></span> </dl>    | <span data-ttu-id="2f85a-122">Passa se il valore alfa in ingresso è maggiore del valore di riferimento.</span><span class="sxs-lookup"><span data-stu-id="2f85a-122">Passes if the incoming alpha value is greater than the reference value.</span></span><br/>             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <span data-ttu-id="2f85a-123"><dt>**\_NOTEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2f85a-123"><dt>**GL\_NOTEQUAL**</dt></span></span> </dl> | <span data-ttu-id="2f85a-124">Passa se il valore alfa in ingresso non è uguale al valore di riferimento.</span><span class="sxs-lookup"><span data-stu-id="2f85a-124">Passes if the incoming alpha value is not equal to the reference value.</span></span><br/>             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <span data-ttu-id="2f85a-125"><dt>**\_GEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2f85a-125"><dt>**GL\_GEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="2f85a-126">Passa se il valore alfa in ingresso è maggiore o uguale al valore di riferimento.</span><span class="sxs-lookup"><span data-stu-id="2f85a-126">Passes if the incoming alpha value is greater than or equal to the reference value.</span></span><br/> |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <span data-ttu-id="2f85a-127"><dt>**GL \_ Always**</dt></span><span class="sxs-lookup"><span data-stu-id="2f85a-127"><dt>**GL\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="2f85a-128">Passa sempre.</span><span class="sxs-lookup"><span data-stu-id="2f85a-128">Always passes.</span></span> <span data-ttu-id="2f85a-129">Questo è il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="2f85a-129">This is the default.</span></span><br/>                                                 |



 

</dd> <dt>

<span data-ttu-id="2f85a-130">*ref*</span><span class="sxs-lookup"><span data-stu-id="2f85a-130">*ref*</span></span> 
</dt> <dd>

<span data-ttu-id="2f85a-131">Valore di riferimento a cui vengono confrontati i valori alfa in ingresso.</span><span class="sxs-lookup"><span data-stu-id="2f85a-131">The reference value to which incoming alpha values are compared.</span></span> <span data-ttu-id="2f85a-132">Questo valore viene fissato nell'intervallo compreso tra 0 e 1, dove 0 rappresenta il valore alfa più basso possibile e 1 il valore massimo possibile.</span><span class="sxs-lookup"><span data-stu-id="2f85a-132">This value is clamped to the range 0 through 1, where 0 represents the lowest possible alpha value and 1 the highest possible value.</span></span> <span data-ttu-id="2f85a-133">Il riferimento predefinito è 0.</span><span class="sxs-lookup"><span data-stu-id="2f85a-133">The default reference is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f85a-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f85a-134">Return value</span></span>

<span data-ttu-id="2f85a-135">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="2f85a-135">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2f85a-136">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="2f85a-136">Error codes</span></span>

<span data-ttu-id="2f85a-137">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="2f85a-137">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="2f85a-138">Nome</span><span class="sxs-lookup"><span data-stu-id="2f85a-138">Name</span></span>                                                                                                  | <span data-ttu-id="2f85a-139">Significato</span><span class="sxs-lookup"><span data-stu-id="2f85a-139">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2f85a-140"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2f85a-140"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="2f85a-141">*Func* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="2f85a-141">*func* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="2f85a-142"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2f85a-142"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="2f85a-143">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="2f85a-143">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2f85a-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f85a-144">Remarks</span></span>

<span data-ttu-id="2f85a-145">Il test alfa Elimina i frammenti a seconda del risultato di un confronto tra i valori alfa dei frammenti in ingresso e un valore di riferimento costante.</span><span class="sxs-lookup"><span data-stu-id="2f85a-145">The alpha test discards fragments depending on the outcome of a comparison between the incoming fragments' alpha values and a constant reference value.</span></span> <span data-ttu-id="2f85a-146">La funzione **glAlphaFunc** specifica il riferimento e la funzione di confronto.</span><span class="sxs-lookup"><span data-stu-id="2f85a-146">The **glAlphaFunc** function specifies the reference and comparison function.</span></span> <span data-ttu-id="2f85a-147">Il confronto viene eseguito solo se è abilitato il test alfa.</span><span class="sxs-lookup"><span data-stu-id="2f85a-147">The comparison is performed only if alpha testing is enabled.</span></span> <span data-ttu-id="2f85a-148">(Per altre informazioni su GL \_ \_Test alfa, vedere [**glEnable**](glenable.md).</span><span class="sxs-lookup"><span data-stu-id="2f85a-148">(For more information on GL\_ALPHA\_TEST, see [**glEnable**](glenable.md).)</span></span>

<span data-ttu-id="2f85a-149">I parametri *Func* e *ref* specificano le condizioni in base alle quali viene disegnato il pixel.</span><span class="sxs-lookup"><span data-stu-id="2f85a-149">The *func* and *ref* parameters specify the conditions under which the pixel is drawn.</span></span> <span data-ttu-id="2f85a-150">Il valore alfa in ingresso viene confrontato con *ref* utilizzando la funzione specificata da *Func*.</span><span class="sxs-lookup"><span data-stu-id="2f85a-150">The incoming alpha value is compared to *ref* using the function specified by *func*.</span></span> <span data-ttu-id="2f85a-151">Se il confronto passa, il frammento in ingresso viene disegnato, condizionale nei test dello stencil e del buffer di profondità successivi.</span><span class="sxs-lookup"><span data-stu-id="2f85a-151">If the comparison passes, the incoming fragment is drawn, conditional on subsequent stencil and depth-buffer tests.</span></span> <span data-ttu-id="2f85a-152">Se il confronto ha esito negativo, non viene apportata alcuna modifica al framebuffer nella posizione in cui si trova il pixel.</span><span class="sxs-lookup"><span data-stu-id="2f85a-152">If the comparison fails, no change is made to the framebuffer at that pixel location.</span></span>

<span data-ttu-id="2f85a-153">La funzione **glAlphaFunc** opera su tutte le Scritture in pixel, incluse quelle derivanti dalla conversione dell'analisi di punti, linee, poligoni e bitmap e dalle operazioni di copia e di copia dei pixel.</span><span class="sxs-lookup"><span data-stu-id="2f85a-153">The **glAlphaFunc** function operates on all pixel writes, including those resulting from the scan conversion of points, lines, polygons, and bitmaps, and from pixel draw and copy operations.</span></span> <span data-ttu-id="2f85a-154">La funzione **glAlphaFunc** non influisce sulle operazioni di cancellazione dello schermo.</span><span class="sxs-lookup"><span data-stu-id="2f85a-154">The **glAlphaFunc** function does not affect screen clear operations.</span></span>

<span data-ttu-id="2f85a-155">Il test alfa viene eseguito solo in modalità RGBA.</span><span class="sxs-lookup"><span data-stu-id="2f85a-155">Alpha testing is done only in RGBA mode.</span></span>

<span data-ttu-id="2f85a-156">Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glAlphaFunc** :</span><span class="sxs-lookup"><span data-stu-id="2f85a-156">The following functions retrieve information related to the **glAlphaFunc** function:</span></span>

<span data-ttu-id="2f85a-157">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Alpha \_ test \_ Func</span><span class="sxs-lookup"><span data-stu-id="2f85a-157">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ALPHA\_TEST\_FUNC</span></span>

<span data-ttu-id="2f85a-158">**glGet** con argomento \_ ref di \_ test di Alpha \_</span><span class="sxs-lookup"><span data-stu-id="2f85a-158">**glGet** with argument GL\_ALPHA\_TEST\_REF</span></span>

<span data-ttu-id="2f85a-159">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Alpha \_ test</span><span class="sxs-lookup"><span data-stu-id="2f85a-159">[**glIsEnabled**](glisenabled.md) with argument GL\_ALPHA\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="2f85a-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f85a-160">Requirements</span></span>



| <span data-ttu-id="2f85a-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f85a-161">Requirement</span></span> | <span data-ttu-id="2f85a-162">Valore</span><span class="sxs-lookup"><span data-stu-id="2f85a-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f85a-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f85a-163">Minimum supported client</span></span><br/> | <span data-ttu-id="2f85a-164">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2f85a-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2f85a-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f85a-165">Minimum supported server</span></span><br/> | <span data-ttu-id="2f85a-166">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2f85a-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2f85a-167">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2f85a-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f85a-168"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f85a-168"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2f85a-169">Libreria</span><span class="sxs-lookup"><span data-stu-id="2f85a-169">Library</span></span><br/>                  | <dl> <span data-ttu-id="2f85a-170"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f85a-170"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2f85a-171">DLL</span><span class="sxs-lookup"><span data-stu-id="2f85a-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f85a-172"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f85a-172"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f85a-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f85a-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f85a-174">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="2f85a-174">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="2f85a-175">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="2f85a-175">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="2f85a-176">**glClear**</span><span class="sxs-lookup"><span data-stu-id="2f85a-176">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="2f85a-177">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="2f85a-177">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="2f85a-178">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="2f85a-178">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="2f85a-179">**Remo**</span><span class="sxs-lookup"><span data-stu-id="2f85a-179">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="2f85a-180">**glGet**</span><span class="sxs-lookup"><span data-stu-id="2f85a-180">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="2f85a-181">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="2f85a-181">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="2f85a-182">**glStencilFunc**</span><span class="sxs-lookup"><span data-stu-id="2f85a-182">**glStencilFunc**</span></span>](glstencilfunc.md)
</dt> </dl>

 

 





