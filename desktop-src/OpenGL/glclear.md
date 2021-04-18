---
title: funzione glClear (GL. h)
description: La funzione glClear Cancella i buffer sui valori predefiniti.
ms.assetid: 9818f969-3145-45ea-aa9c-2abed953a8e0
keywords:
- funzione glClear OpenGL
topic_type:
- apiref
api_name:
- glClear
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db935e46c65c42976024a8afbb98028294710c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301800"
---
# <a name="glclear-function"></a><span data-ttu-id="367af-104">glClear (funzione)</span><span class="sxs-lookup"><span data-stu-id="367af-104">glClear function</span></span>

<span data-ttu-id="367af-105">La funzione **glClear** Cancella i buffer sui valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="367af-105">The **glClear** function clears buffers to preset values.</span></span>

## <a name="syntax"></a><span data-ttu-id="367af-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="367af-106">Syntax</span></span>


```C++
void WINAPI glClear(
   GLbitfield mask
);
```



## <a name="parameters"></a><span data-ttu-id="367af-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="367af-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="367af-108">*maschera*</span><span class="sxs-lookup"><span data-stu-id="367af-108">*mask*</span></span> 
</dt> <dd>

<span data-ttu-id="367af-109">Operatori OR bit per bit delle maschere che indicano i buffer da cancellare.</span><span class="sxs-lookup"><span data-stu-id="367af-109">Bitwise OR operators of masks that indicate the buffers to be cleared.</span></span> <span data-ttu-id="367af-110">Le quattro maschere sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="367af-110">The four masks are as follows.</span></span>



| <span data-ttu-id="367af-111">Valore</span><span class="sxs-lookup"><span data-stu-id="367af-111">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="367af-112">Significato</span><span class="sxs-lookup"><span data-stu-id="367af-112">Meaning</span></span>                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span><dl> <span data-ttu-id="367af-113"><dt>**\_bit del \_ buffer dei colori GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="367af-113"><dt>**GL\_COLOR\_BUFFER\_BIT**</dt></span></span> </dl>       | <span data-ttu-id="367af-114">Buffer attualmente abilitati per la scrittura di colori.</span><span class="sxs-lookup"><span data-stu-id="367af-114">The buffers currently enabled for color writing.</span></span><br/> |
| <span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span><dl> <span data-ttu-id="367af-115"><dt>**\_ \_ bit buffer di profondità GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="367af-115"><dt>**GL\_DEPTH\_BUFFER\_BIT**</dt></span></span> </dl>       | <span data-ttu-id="367af-116">Buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="367af-116">The depth buffer.</span></span><br/>                                |
| <span id="GL_ACCUM_BUFFER_BIT"></span><span id="gl_accum_buffer_bit"></span><dl> <span data-ttu-id="367af-117"><dt>**\_bit del buffer di accut GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="367af-117"><dt>**GL\_ACCUM\_BUFFER\_BIT**</dt></span></span> </dl>       | <span data-ttu-id="367af-118">Buffer di accumulo.</span><span class="sxs-lookup"><span data-stu-id="367af-118">The accumulation buffer.</span></span><br/>                         |
| <span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span><dl> <span data-ttu-id="367af-119"><dt>**\_ \_ bit buffer dello stencil GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="367af-119"><dt>**GL\_STENCIL\_BUFFER\_BIT**</dt></span></span> </dl> | <span data-ttu-id="367af-120">Buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="367af-120">The stencil buffer.</span></span><br/>                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="367af-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="367af-121">Return value</span></span>

<span data-ttu-id="367af-122">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="367af-122">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="367af-123">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="367af-123">Error codes</span></span>

<span data-ttu-id="367af-124">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="367af-124">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="367af-125">Nome</span><span class="sxs-lookup"><span data-stu-id="367af-125">Name</span></span>                                                                                                  | <span data-ttu-id="367af-126">Significato</span><span class="sxs-lookup"><span data-stu-id="367af-126">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="367af-127"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="367af-127"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="367af-128">Un bit diverso dai quattro bit definiti è stato impostato nella *maschera*.</span><span class="sxs-lookup"><span data-stu-id="367af-128">Any bit other than the four defined bits was set in *mask*.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="367af-129"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="367af-129"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="367af-130">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="367af-130">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="367af-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="367af-131">Remarks</span></span>

<span data-ttu-id="367af-132">La funzione **glClear** imposta l'area bitplane della finestra sui valori selezionati in precedenza da [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md)e [**glClearAccum**](glclearaccum.md).</span><span class="sxs-lookup"><span data-stu-id="367af-132">The **glClear** function sets the bitplane area of the window to values previously selected by [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md), and [**glClearAccum**](glclearaccum.md).</span></span> <span data-ttu-id="367af-133">È possibile cancellare contemporaneamente più buffer di colori selezionando più di un buffer alla volta usando [**glDrawBuffer**](gldrawbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="367af-133">You can clear multiple color buffers simultaneously by selecting more than one buffer at a time using [**glDrawBuffer**](gldrawbuffer.md).</span></span>

<span data-ttu-id="367af-134">Il test di proprietà dei pixel, il test a forbice, il dithering e il buffer writemasks influiscono sul funzionamento di **glClear**.</span><span class="sxs-lookup"><span data-stu-id="367af-134">The pixel-ownership test, the scissor test, dithering, and the buffer writemasks affect the operation of **glClear**.</span></span> <span data-ttu-id="367af-135">La casella a forbice delimita l'area deselezionata.</span><span class="sxs-lookup"><span data-stu-id="367af-135">The scissor box bounds the cleared region.</span></span> <span data-ttu-id="367af-136">La funzione **glClear** ignora la funzione Alpha, la funzione Blend, l'operazione logica, lo stencil, il mapping della trama e il buffer *z*.</span><span class="sxs-lookup"><span data-stu-id="367af-136">The **glClear** function ignores the alpha function, blend function, logical operation, stenciling, texture mapping, and *z*-buffering.</span></span>

<span data-ttu-id="367af-137">La funzione **glClear** accetta un solo argomento (*maschera*) che rappresenta l'operatore OR bit per bit di diversi valori che indicano il buffer da cancellare.</span><span class="sxs-lookup"><span data-stu-id="367af-137">The **glClear** function takes a single argument (*mask*) that is the bitwise OR of several values indicating which buffer is to be cleared.</span></span>

<span data-ttu-id="367af-138">Il valore a cui viene cancellato ogni buffer dipende dall'impostazione del valore Clear per il buffer.</span><span class="sxs-lookup"><span data-stu-id="367af-138">The value to which each buffer is cleared depends on the setting of the clear value for that buffer.</span></span>

<span data-ttu-id="367af-139">Se non è presente un buffer, una chiamata **glClear** indirizzata a tale buffer non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="367af-139">If a buffer is not present, a **glClear** call directed at that buffer has no effect.</span></span>

<span data-ttu-id="367af-140">Le funzioni seguenti consentono di recuperare informazioni correlate a **glClear**:</span><span class="sxs-lookup"><span data-stu-id="367af-140">The following functions retrieve information related to **glClear**:</span></span>

<span data-ttu-id="367af-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con l'argomento contabilità GL \_ \_ Clear \_ value</span><span class="sxs-lookup"><span data-stu-id="367af-141">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ACCUM\_CLEAR\_VALUE</span></span>

<span data-ttu-id="367af-142">**glGet** con \_ \_ valore Clear Depth Depth \_</span><span class="sxs-lookup"><span data-stu-id="367af-142">**glGet** with argument GL\_DEPTH\_CLEAR\_VALUE</span></span>

<span data-ttu-id="367af-143">**glGet** con valore di \_ cancellazione dell'indice GL dell'argomento \_ \_</span><span class="sxs-lookup"><span data-stu-id="367af-143">**glGet** with argument GL\_INDEX\_CLEAR\_VALUE</span></span>

<span data-ttu-id="367af-144">**glGet** con valore di \_ cancellazione del colore GL argomento \_ \_</span><span class="sxs-lookup"><span data-stu-id="367af-144">**glGet** with argument GL\_COLOR\_CLEAR\_VALUE</span></span>

<span data-ttu-id="367af-145">**glGet** con il \_ \_ valore Clear dello stencil GL degli argomenti \_</span><span class="sxs-lookup"><span data-stu-id="367af-145">**glGet** with argument GL\_STENCIL\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="367af-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="367af-146">Requirements</span></span>



| <span data-ttu-id="367af-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="367af-147">Requirement</span></span> | <span data-ttu-id="367af-148">Valore</span><span class="sxs-lookup"><span data-stu-id="367af-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="367af-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="367af-149">Minimum supported client</span></span><br/> | <span data-ttu-id="367af-150">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="367af-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="367af-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="367af-151">Minimum supported server</span></span><br/> | <span data-ttu-id="367af-152">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="367af-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="367af-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="367af-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="367af-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="367af-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="367af-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="367af-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="367af-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="367af-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="367af-157">DLL</span><span class="sxs-lookup"><span data-stu-id="367af-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="367af-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="367af-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="367af-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="367af-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="367af-160">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="367af-160">**glClearAccum**</span></span>](glclearaccum.md)
</dt> <dt>

[<span data-ttu-id="367af-161">**glClearColor**</span><span class="sxs-lookup"><span data-stu-id="367af-161">**glClearColor**</span></span>](glclearcolor.md)
</dt> <dt>

[<span data-ttu-id="367af-162">**glClearDepth**</span><span class="sxs-lookup"><span data-stu-id="367af-162">**glClearDepth**</span></span>](glcleardepth.md)
</dt> <dt>

[<span data-ttu-id="367af-163">**glClearIndex**</span><span class="sxs-lookup"><span data-stu-id="367af-163">**glClearIndex**</span></span>](glclearindex.md)
</dt> <dt>

[<span data-ttu-id="367af-164">**glClearStencil**</span><span class="sxs-lookup"><span data-stu-id="367af-164">**glClearStencil**</span></span>](glclearstencil.md)
</dt> <dt>

[<span data-ttu-id="367af-165">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="367af-165">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="367af-166">**glGet**</span><span class="sxs-lookup"><span data-stu-id="367af-166">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="367af-167">**glScissor**</span><span class="sxs-lookup"><span data-stu-id="367af-167">**glScissor**</span></span>](glscissor.md)
</dt> </dl>

 

 





