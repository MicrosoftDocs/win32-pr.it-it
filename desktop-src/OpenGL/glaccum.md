---
title: funzione glAccum (GL. h)
description: La funzione glAccum opera sul buffer di accumulo.
ms.assetid: 3ddd69fe-74fc-4ac0-be8d-bcaa71ac0292
keywords:
- funzione glAccum OpenGL
topic_type:
- apiref
api_name:
- glAccum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d25e02971d07d54567c462708aa4efd87b2d32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741946"
---
# <a name="glaccum-function"></a><span data-ttu-id="bce73-104">glAccum (funzione)</span><span class="sxs-lookup"><span data-stu-id="bce73-104">glAccum function</span></span>

<span data-ttu-id="bce73-105">La funzione **glAccum** opera sul buffer di accumulo.</span><span class="sxs-lookup"><span data-stu-id="bce73-105">The **glAccum** function operates on the accumulation buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="bce73-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bce73-106">Syntax</span></span>


```C++
void WINAPI glAccum(
   GLenum  op,
   GLfloat value
);
```



## <a name="parameters"></a><span data-ttu-id="bce73-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="bce73-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bce73-108">*op*</span><span class="sxs-lookup"><span data-stu-id="bce73-108">*op*</span></span> 
</dt> <dd>

<span data-ttu-id="bce73-109">Operazione del buffer di accumulo.</span><span class="sxs-lookup"><span data-stu-id="bce73-109">The accumulation buffer operation.</span></span> <span data-ttu-id="bce73-110">Le costanti simboliche accettate sono le seguenti.</span><span class="sxs-lookup"><span data-stu-id="bce73-110">The accepted symbolic constants are as follows.</span></span>



| <span data-ttu-id="bce73-111">Valore</span><span class="sxs-lookup"><span data-stu-id="bce73-111">Value</span></span>                                                                                                                                             | <span data-ttu-id="bce73-112">Significato</span><span class="sxs-lookup"><span data-stu-id="bce73-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_ACCUM"></span><span id="gl_accum"></span><dl> <span data-ttu-id="bce73-113"><dt>**\_Accue GL**</dt></span><span class="sxs-lookup"><span data-stu-id="bce73-113"><dt>**GL\_ACCUM**</dt></span></span> </dl>    | <span data-ttu-id="bce73-114">Ottiene R, G, B e un valore dal buffer attualmente selezionato per la lettura (vedere [**glReadBuffer**](glreadbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="bce73-114">Obtains R, G, B, and A values from the buffer currently selected for reading (see [**glReadBuffer**](glreadbuffer.md)).</span></span> <span data-ttu-id="bce73-115">Ogni valore di componente è diviso per 2 *n*  1, dove *n* è il numero di bit allocati a ogni componente colore nel buffer attualmente selezionato.</span><span class="sxs-lookup"><span data-stu-id="bce73-115">Each component value is divided by 2 *n*  1, where *n* is the number of bits allocated to each color component in the currently selected buffer.</span></span> <span data-ttu-id="bce73-116">Il risultato è un valore a virgola mobile nell'intervallo compreso tra \[ 0 \] e 1, moltiplicato per *valore* e aggiunto al componente pixel corrispondente nel buffer di accumulo, aggiornando in tal modo il buffer di accumulo.</span><span class="sxs-lookup"><span data-stu-id="bce73-116">The result is a floating-point value in the range \[0,1\], which is multiplied by *value* and added to the corresponding pixel component in the accumulation buffer, thereby updating the accumulation buffer.</span></span><br/> |
| <span id="GL_LOAD"></span><span id="gl_load"></span><dl> <span data-ttu-id="bce73-117"><dt>**\_carico GL**</dt></span><span class="sxs-lookup"><span data-stu-id="bce73-117"><dt>**GL\_LOAD**</dt></span></span> </dl>       | <span data-ttu-id="bce73-118">Simile a GL \_ accut, ad eccezione del fatto che il valore corrente nel buffer di accumulo non viene utilizzato nel calcolo del nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="bce73-118">Similar to GL\_ACCUM, except that the current value in the accumulation buffer is not used in the calculation of the new value.</span></span> <span data-ttu-id="bce73-119">Ovvero i valori R, G, B e quelli del buffer attualmente selezionato sono divisi per 2 *n*  1, moltiplicati per *valore* e quindi archiviati nella cella corrispondente del buffer di accumulo, sovrascrivendo il valore corrente.</span><span class="sxs-lookup"><span data-stu-id="bce73-119">That is, the R, G, B, and A values from the currently selected buffer are divided by 2 *n*  1, multiplied by *value*, and then stored in the corresponding accumulation buffer cell, overwriting the current value.</span></span><br/>                                                                                                                                      |
| <span id="GL_ADD"></span><span id="gl_add"></span><dl> <span data-ttu-id="bce73-120"><dt>**Aggiunta di GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bce73-120"><dt>**GL\_ADD**</dt></span></span> </dl>          | <span data-ttu-id="bce73-121">Aggiunge un *valore* a ogni R, G, B e a nel buffer di accumulo.</span><span class="sxs-lookup"><span data-stu-id="bce73-121">Adds *value* to each R, G, B, and A in the accumulation buffer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="GL_MULT"></span><span id="gl_mult"></span><dl> <span data-ttu-id="bce73-122"><dt>**\_mult**</dt></span><span class="sxs-lookup"><span data-stu-id="bce73-122"><dt>**GL\_MULT**</dt></span></span> </dl>       | <span data-ttu-id="bce73-123">Moltiplica ogni R, G, B e a nel buffer di accumulo per *valore* e restituisce il componente ridimensionato alla posizione del buffer di accumulo corrispondente.</span><span class="sxs-lookup"><span data-stu-id="bce73-123">Multiplies each R, G, B, and A in the accumulation buffer by *value* and returns the scaled component to its corresponding accumulation buffer location.</span></span><br/>                                                                                                                                                                                                                                                                                                                                |
| <span id="GL_RETURN"></span><span id="gl_return"></span><dl> <span data-ttu-id="bce73-124"><dt>**\_return GL**</dt></span><span class="sxs-lookup"><span data-stu-id="bce73-124"><dt>**GL\_RETURN**</dt></span></span> </dl> | <span data-ttu-id="bce73-125">Trasferisce i valori del buffer di accumulo al buffer dei colori o ai buffer attualmente selezionati per la scrittura.</span><span class="sxs-lookup"><span data-stu-id="bce73-125">Transfers accumulation buffer values to the color buffer or buffers currently selected for writing.</span></span> <span data-ttu-id="bce73-126">Ogni R, G, B e un componente viene moltiplicato per *valore*, quindi moltiplicato per 2 *n*  1, fissato all'intervallo \[ 0, 2 *n*  1 \] e archiviato nella cella del buffer di visualizzazione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="bce73-126">Each R, G, B, and A component is multiplied by *value*, then multiplied by 2 *n*  1, clamped to the range \[0, 2 *n*  1 \], and stored in the corresponding display buffer cell.</span></span> <span data-ttu-id="bce73-127">Le uniche operazioni di frammento applicate a questo trasferimento sono proprietà pixel, Scissor, dithering e colore writemasks.</span><span class="sxs-lookup"><span data-stu-id="bce73-127">The only fragment operations that are applied to this transfer are pixel ownership, scissor, dithering, and color writemasks.</span></span><br/>                                                                        |



 

</dd> <dt>

<span data-ttu-id="bce73-128">*value*</span><span class="sxs-lookup"><span data-stu-id="bce73-128">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="bce73-129">Valore a virgola mobile utilizzato nell'operazione del buffer di accumulo.</span><span class="sxs-lookup"><span data-stu-id="bce73-129">A floating-point value used in the accumulation buffer operation.</span></span> <span data-ttu-id="bce73-130">Il parametro *op* determina il modo in cui viene usato il *valore* .</span><span class="sxs-lookup"><span data-stu-id="bce73-130">The *op* parameter determines how *value* is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bce73-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bce73-131">Return value</span></span>

<span data-ttu-id="bce73-132">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="bce73-132">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bce73-133">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="bce73-133">Error codes</span></span>

<span data-ttu-id="bce73-134">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="bce73-134">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="bce73-135">Nome</span><span class="sxs-lookup"><span data-stu-id="bce73-135">Name</span></span>                                                                                                  | <span data-ttu-id="bce73-136">Significato</span><span class="sxs-lookup"><span data-stu-id="bce73-136">Meaning</span></span>                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bce73-137"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bce73-137"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="bce73-138">*op* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="bce73-138">*op* was not an accepted value.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="bce73-139"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bce73-139"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="bce73-140">Non è stato rilevato alcun buffer di accumulo o la funzione **glAccum** è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="bce73-140">There was no accumulation buffer or the function **glAccum** was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bce73-141">Commenti</span><span class="sxs-lookup"><span data-stu-id="bce73-141">Remarks</span></span>

<span data-ttu-id="bce73-142">Il buffer di accumulo è un buffer di colori a intervalli estesi.</span><span class="sxs-lookup"><span data-stu-id="bce73-142">The accumulation buffer is an extended-range color buffer.</span></span> <span data-ttu-id="bce73-143">Non viene eseguito il rendering delle immagini.</span><span class="sxs-lookup"><span data-stu-id="bce73-143">Images are not rendered into it.</span></span> <span data-ttu-id="bce73-144">Al contrario, le immagini sottoposte a rendering in uno dei buffer dei colori vengono aggiunte al contenuto del buffer di accumulo dopo il rendering.</span><span class="sxs-lookup"><span data-stu-id="bce73-144">Rather, images rendered into one of the color buffers are added to the contents of the accumulation buffer after rendering.</span></span> <span data-ttu-id="bce73-145">È possibile creare effetti quali l'anti-aliasing (di punti, linee e poligoni), la sfocatura del movimento e la profondità del campo accumulando immagini generate con matrici di trasformazione diverse.</span><span class="sxs-lookup"><span data-stu-id="bce73-145">You can create effects such as antialiasing (of points, lines, and polygons), motion blur, and depth of field by accumulating images generated with different transformation matrices.</span></span>

<span data-ttu-id="bce73-146">Ogni pixel nel buffer di accumulo è costituito da valori rosso, verde, blu e alfa.</span><span class="sxs-lookup"><span data-stu-id="bce73-146">Each pixel in the accumulation buffer consists of red, green, blue, and alpha values.</span></span> <span data-ttu-id="bce73-147">Il numero di bit per componente nel buffer di accumulo dipende dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="bce73-147">The number of bits per component in the accumulation buffer depends on the implementation.</span></span> <span data-ttu-id="bce73-148">È possibile esaminare questo numero chiamando [**glGetIntegerv**](glgetintegerv.md) quattro volte, con gli argomenti GL \_ accut \_ Red \_ bits, GL \_ accut \_ Green \_ bits, GL \_ accuy \_ Blue \_ bits e GL \_ accuy \_ Alpha \_ bits, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="bce73-148">You can examine this number by calling [**glGetIntegerv**](glgetintegerv.md) four times, with the arguments GL\_ACCUM\_RED\_BITS, GL\_ACCUM\_GREEN\_BITS, GL\_ACCUM\_BLUE\_BITS, and GL\_ACCUM\_ALPHA\_BITS, respectively.</span></span> <span data-ttu-id="bce73-149">Indipendentemente dal numero di bit per componente, tuttavia, l'intervallo di valori archiviati da ogni componente è \[ 1,? 1 \] .</span><span class="sxs-lookup"><span data-stu-id="bce73-149">Regardless of the number of bits per component, however, the range of values stored by each component is \[ 1,?1\].</span></span> <span data-ttu-id="bce73-150">I pixel del buffer di accumulo sono mappati uno-a-uno con i pixel del framebuffer.</span><span class="sxs-lookup"><span data-stu-id="bce73-150">The accumulation buffer pixels are mapped one-to-one with framebuffer pixels.</span></span>

<span data-ttu-id="bce73-151">La funzione **glAccum** opera sul buffer di accumulo.</span><span class="sxs-lookup"><span data-stu-id="bce73-151">The **glAccum** function operates on the accumulation buffer.</span></span> <span data-ttu-id="bce73-152">Il primo argomento, *op*, è una costante simbolica che seleziona un'operazione del buffer di accumulo.</span><span class="sxs-lookup"><span data-stu-id="bce73-152">The first argument, *op*, is a symbolic constant that selects an accumulation buffer operation.</span></span> <span data-ttu-id="bce73-153">Il secondo argomento, *value*, è un valore a virgola mobile da usare in tale operazione.</span><span class="sxs-lookup"><span data-stu-id="bce73-153">The second argument, *value*, is a floating-point value to be used in that operation.</span></span> <span data-ttu-id="bce73-154">Sono state specificate cinque operazioni: GL \_ accut, GL \_ Load, GL \_ Add, GL \_ mult e GL \_ return.</span><span class="sxs-lookup"><span data-stu-id="bce73-154">Five operations are specified: GL\_ACCUM, GL\_LOAD, GL\_ADD, GL\_MULT, and GL\_RETURN.</span></span>

<span data-ttu-id="bce73-155">Tutte le operazioni del buffer di accumulo sono limitate all'area della casella a forbice corrente e vengono applicate in modo identico ai componenti rosso, verde, blu e alfa di ogni pixel.</span><span class="sxs-lookup"><span data-stu-id="bce73-155">All accumulation buffer operations are limited to the area of the current scissor box and are applied identically to the red, green, blue, and alpha components of each pixel.</span></span> <span data-ttu-id="bce73-156">Il contenuto di un componente pixel del buffer di accumulo non è definito se l'operazione **glAccum** restituisce un valore non compreso nell'intervallo \[ 1, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="bce73-156">The contents of an accumulation buffer pixel component are undefined if the **glAccum** operation results in a value outside the range \[ 1,1\].</span></span>

<span data-ttu-id="bce73-157">Per cancellare il buffer di accumulo, usare la funzione [**glClearAccum**](glclearaccum.md) per specificare R, G, B e un valore per impostarlo su e rilasciare una funzione [**glClear**](glclear.md) con il buffer di accumulo abilitato.</span><span class="sxs-lookup"><span data-stu-id="bce73-157">To clear the accumulation buffer, use the [**glClearAccum**](glclearaccum.md) function to specify R, G, B, and A values to set it to, and issue a [**glClear**](glclear.md) function with the accumulation buffer enabled.</span></span>

<span data-ttu-id="bce73-158">Solo i pixel all'interno della casella Scissor corrente vengono aggiornati da qualsiasi operazione **glAccum** .</span><span class="sxs-lookup"><span data-stu-id="bce73-158">Only those pixels within the current scissor box are updated by any **glAccum** operation.</span></span>

<span data-ttu-id="bce73-159">Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glAccum** :</span><span class="sxs-lookup"><span data-stu-id="bce73-159">The following functions retrieve information related to the **glAccum** function:</span></span>

<span data-ttu-id="bce73-160">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con l'argomento contabilità GL \_ \_ Red \_ BITS</span><span class="sxs-lookup"><span data-stu-id="bce73-160">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_RED\_BITS</span></span>

<span data-ttu-id="bce73-161">**glGet** con argomento GL \_ accut \_ Green \_ BITS</span><span class="sxs-lookup"><span data-stu-id="bce73-161">**glGet** with argument GL\_ACCUM\_GREEN\_BITS</span></span>

<span data-ttu-id="bce73-162">**glGet** con argument GL \_ \_ Blue \_ BITS</span><span class="sxs-lookup"><span data-stu-id="bce73-162">**glGet** with argument GL\_ACCUM\_BLUE\_BITS</span></span>

<span data-ttu-id="bce73-163">**glGet** con argomento GL \_ accuy \_ Alpha \_ BITS</span><span class="sxs-lookup"><span data-stu-id="bce73-163">**glGet** with argument GL\_ACCUM\_ALPHA\_BITS</span></span>

## <a name="requirements"></a><span data-ttu-id="bce73-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bce73-164">Requirements</span></span>



| <span data-ttu-id="bce73-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="bce73-165">Requirement</span></span> | <span data-ttu-id="bce73-166">Valore</span><span class="sxs-lookup"><span data-stu-id="bce73-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bce73-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bce73-167">Minimum supported client</span></span><br/> | <span data-ttu-id="bce73-168">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bce73-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bce73-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bce73-169">Minimum supported server</span></span><br/> | <span data-ttu-id="bce73-170">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bce73-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bce73-171">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bce73-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="bce73-172"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="bce73-172"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="bce73-173">Libreria</span><span class="sxs-lookup"><span data-stu-id="bce73-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="bce73-174"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bce73-174"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bce73-175">DLL</span><span class="sxs-lookup"><span data-stu-id="bce73-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bce73-176"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bce73-176"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bce73-177">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bce73-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bce73-178">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="bce73-178">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="bce73-179">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="bce73-179">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="bce73-180">**glClear**</span><span class="sxs-lookup"><span data-stu-id="bce73-180">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="bce73-181">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="bce73-181">**glClearAccum**</span></span>](glclearaccum.md)
</dt> <dt>

[<span data-ttu-id="bce73-182">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="bce73-182">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="bce73-183">**Remo**</span><span class="sxs-lookup"><span data-stu-id="bce73-183">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="bce73-184">**glGet**</span><span class="sxs-lookup"><span data-stu-id="bce73-184">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="bce73-185">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="bce73-185">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="bce73-186">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="bce73-186">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="bce73-187">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="bce73-187">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="bce73-188">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="bce73-188">**glReadBuffer**</span></span>](glreadbuffer.md)
</dt> <dt>

[<span data-ttu-id="bce73-189">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="bce73-189">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="bce73-190">**glScissor**</span><span class="sxs-lookup"><span data-stu-id="bce73-190">**glScissor**</span></span>](glscissor.md)
</dt> <dt>

[<span data-ttu-id="bce73-191">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="bce73-191">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





