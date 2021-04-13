---
title: funzione glLogicOp (GL. h)
description: La funzione glLogicOp specifica un'operazione pixel logica per il rendering dell'indice dei colori.
ms.assetid: 29edf9bd-f3b8-4de7-9afb-07714f4efd92
keywords:
- funzione glLogicOp OpenGL
topic_type:
- apiref
api_name:
- glLogicOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb29e8f845e99f6d3c988dfd0c0201de129bee69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519150"
---
# <a name="gllogicop-function"></a><span data-ttu-id="31b6f-104">glLogicOp (funzione)</span><span class="sxs-lookup"><span data-stu-id="31b6f-104">glLogicOp function</span></span>

<span data-ttu-id="31b6f-105">La funzione **glLogicOp** specifica un'operazione pixel logica per il rendering dell'indice dei colori.</span><span class="sxs-lookup"><span data-stu-id="31b6f-105">The **glLogicOp** function specifies a logical pixel operation for color index rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="31b6f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31b6f-106">Syntax</span></span>


```C++
void WINAPI glLogicOp(
   GLenum opcode
);
```



## <a name="parameters"></a><span data-ttu-id="31b6f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="31b6f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31b6f-108">*codice operativo*</span><span class="sxs-lookup"><span data-stu-id="31b6f-108">*opcode*</span></span> 
</dt> <dd>

<span data-ttu-id="31b6f-109">Costante simbolica che seleziona un'operazione logica.</span><span class="sxs-lookup"><span data-stu-id="31b6f-109">A symbolic constant that selects a logical operation.</span></span> <span data-ttu-id="31b6f-110">I simboli seguenti sono accettati, dove s è uguale al valore del bit di origine e d è il valore del bit di destinazione.</span><span class="sxs-lookup"><span data-stu-id="31b6f-110">The following symbols are accepted where s equals the value of the source bit and d is the value of the destination bit.</span></span>



| <span data-ttu-id="31b6f-111">Valore</span><span class="sxs-lookup"><span data-stu-id="31b6f-111">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="31b6f-112">Significato</span><span class="sxs-lookup"><span data-stu-id="31b6f-112">Meaning</span></span>              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="GL_CLEAR"></span><span id="gl_clear"></span><dl> <span data-ttu-id="31b6f-113"><dt>**\_cancellazione GL**</dt></span><span class="sxs-lookup"><span data-stu-id="31b6f-113"><dt>**GL\_CLEAR**</dt></span></span> </dl>                          | <span data-ttu-id="31b6f-114">0</span><span class="sxs-lookup"><span data-stu-id="31b6f-114">0</span></span><br/>         |
| <span id="GL_SET"></span><span id="gl_set"></span><dl> <span data-ttu-id="31b6f-115"><dt>**\_set GL**</dt></span><span class="sxs-lookup"><span data-stu-id="31b6f-115"><dt>**GL\_SET**</dt></span></span> </dl>                                | <span data-ttu-id="31b6f-116">1</span><span class="sxs-lookup"><span data-stu-id="31b6f-116">1</span></span><br/>         |
| <span id="GL_COPY"></span><span id="gl_copy"></span><dl> <span data-ttu-id="31b6f-117"><dt>**\_copia GL**</dt></span><span class="sxs-lookup"><span data-stu-id="31b6f-117"><dt>**GL\_COPY**</dt></span></span> </dl>                             | <span data-ttu-id="31b6f-118">s</span><span class="sxs-lookup"><span data-stu-id="31b6f-118">s</span></span><br/>         |
| <span id="GL_COPY_INVERTED"></span><span id="gl_copy_inverted"></span><dl> <span data-ttu-id="31b6f-119"><dt>**\_copia GL \_ invertita**</dt></span><span class="sxs-lookup"><span data-stu-id="31b6f-119"><dt>**GL\_COPY\_INVERTED**</dt></span></span> </dl> | <span data-ttu-id="31b6f-120">! s</span><span class="sxs-lookup"><span data-stu-id="31b6f-120">!s</span></span><br/>        |
| <span id="GL_NOOP"></span><span id="gl_noop"></span><dl> <span data-ttu-id="31b6f-121"><dt>**\_NoOp GL**</dt></span><span class="sxs-lookup"><span data-stu-id="31b6f-121"><dt>**GL\_NOOP**</dt></span></span> </dl>                             | <span data-ttu-id="31b6f-122">d</span><span class="sxs-lookup"><span data-stu-id="31b6f-122">d</span></span><br/>         |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <span data-ttu-id="31b6f-123"><dt>**GL \_ invertiti**</dt></span><span class="sxs-lookup"><span data-stu-id="31b6f-123"><dt>**GL\_INVERT**</dt></span></span> </dl>                       | <span data-ttu-id="31b6f-124">! d</span><span class="sxs-lookup"><span data-stu-id="31b6f-124">!d</span></span><br/>        |
| <span id="GL_AND"></span><span id="gl_and"></span><dl> <span data-ttu-id="31b6f-125"><dt>**GL \_ e**</dt></span><span class="sxs-lookup"><span data-stu-id="31b6f-125"><dt>**GL\_AND**</dt></span></span> </dl>                                | <span data-ttu-id="31b6f-126">s & d</span><span class="sxs-lookup"><span data-stu-id="31b6f-126">s & d</span></span><br/>     |
| <span id="GL_NAND"></span><span id="gl_nand"></span><dl> <span data-ttu-id="31b6f-127"><dt>**\_NAND GL**</dt></span><span class="sxs-lookup"><span data-stu-id="31b6f-127"><dt>**GL\_NAND**</dt></span></span> </dl>                             | <span data-ttu-id="31b6f-128">! (s & d)</span><span class="sxs-lookup"><span data-stu-id="31b6f-128">!(s & d)</span></span><br/>  |
| <span id="GL_OR"></span><span id="gl_or"></span><dl> <span data-ttu-id="31b6f-129"><dt>**GL \_ o**</dt></span><span class="sxs-lookup"><span data-stu-id="31b6f-129"><dt>**GL\_OR**</dt></span></span> </dl>                                   | <span data-ttu-id="31b6f-130">s \| d</span><span class="sxs-lookup"><span data-stu-id="31b6f-130">s \| d</span></span><br/>    |
| <span id="GL_NOR"></span><span id="gl_nor"></span><dl> <span data-ttu-id="31b6f-131"><dt>**GL \_ e**</dt></span><span class="sxs-lookup"><span data-stu-id="31b6f-131"><dt>**GL\_NOR**</dt></span></span> </dl>                                | <span data-ttu-id="31b6f-132">! (s \| d)</span><span class="sxs-lookup"><span data-stu-id="31b6f-132">!(s \| d)</span></span><br/> |
| <span id="GL_XOR"></span><span id="gl_xor"></span><dl> <span data-ttu-id="31b6f-133"><dt>**\_Xor GL**</dt></span><span class="sxs-lookup"><span data-stu-id="31b6f-133"><dt>**GL\_XOR**</dt></span></span> </dl>                                | <span data-ttu-id="31b6f-134">s ^ d</span><span class="sxs-lookup"><span data-stu-id="31b6f-134">s ^ d</span></span><br/>     |
| <span id="GL_EQUIV"></span><span id="gl_equiv"></span><dl> <span data-ttu-id="31b6f-135"><dt>**\_equiv GL**</dt></span><span class="sxs-lookup"><span data-stu-id="31b6f-135"><dt>**GL\_EQUIV**</dt></span></span> </dl>                          | <span data-ttu-id="31b6f-136">! (s ^ d)</span><span class="sxs-lookup"><span data-stu-id="31b6f-136">!(s ^ d)</span></span><br/>  |
| <span id="GL_AND_REVERSE"></span><span id="gl_and_reverse"></span><dl> <span data-ttu-id="31b6f-137"><dt>**GL \_ e \_ Reverse**</dt></span><span class="sxs-lookup"><span data-stu-id="31b6f-137"><dt>**GL\_AND\_REVERSE**</dt></span></span> </dl>       | <span data-ttu-id="31b6f-138">s &! d</span><span class="sxs-lookup"><span data-stu-id="31b6f-138">s & !d</span></span><br/>    |
| <span id="GL_AND_INVERTED"></span><span id="gl_and_inverted"></span><dl> <span data-ttu-id="31b6f-139"><dt>**GL \_ e \_ invertiti**</dt></span><span class="sxs-lookup"><span data-stu-id="31b6f-139"><dt>**GL\_AND\_INVERTED**</dt></span></span> </dl>    | <span data-ttu-id="31b6f-140">! s & d</span><span class="sxs-lookup"><span data-stu-id="31b6f-140">!s & d</span></span><br/>    |
| <span id="GL_OR_REVERSE"></span><span id="gl_or_reverse"></span><dl> <span data-ttu-id="31b6f-141"><dt>**GL \_ o \_ Reverse**</dt></span><span class="sxs-lookup"><span data-stu-id="31b6f-141"><dt>**GL\_OR\_REVERSE**</dt></span></span> </dl>          | <span data-ttu-id="31b6f-142">s \| ! d</span><span class="sxs-lookup"><span data-stu-id="31b6f-142">s \| !d</span></span><br/>   |
| <span id="GL_OR_INVERTED"></span><span id="gl_or_inverted"></span><dl> <span data-ttu-id="31b6f-143"><dt>**GL \_ o \_ invertiti**</dt></span><span class="sxs-lookup"><span data-stu-id="31b6f-143"><dt>**GL\_OR\_INVERTED**</dt></span></span> </dl>       | <span data-ttu-id="31b6f-144">! s \| d</span><span class="sxs-lookup"><span data-stu-id="31b6f-144">!s \| d</span></span><br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31b6f-145">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="31b6f-145">Return value</span></span>

<span data-ttu-id="31b6f-146">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="31b6f-146">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="31b6f-147">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="31b6f-147">Error codes</span></span>

<span data-ttu-id="31b6f-148">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="31b6f-148">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="31b6f-149">Nome</span><span class="sxs-lookup"><span data-stu-id="31b6f-149">Name</span></span>                                                                                                  | <span data-ttu-id="31b6f-150">Significato</span><span class="sxs-lookup"><span data-stu-id="31b6f-150">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="31b6f-151"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="31b6f-151"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="31b6f-152">*OpCode* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="31b6f-152">*opcode* was not an accepted value.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="31b6f-153"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="31b6f-153"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="31b6f-154">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="31b6f-154">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="31b6f-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="31b6f-155">Remarks</span></span>

<span data-ttu-id="31b6f-156">La funzione **glLogicOp** specifica un'operazione logica che, se abilitata, viene applicata tra l'indice dei colori in ingresso e l'indice dei colori nella posizione corrispondente nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="31b6f-156">The **glLogicOp** function specifies a logical operation that, when enabled, is applied between the incoming color index and the color index at the corresponding location in the framebuffer.</span></span> <span data-ttu-id="31b6f-157">L'operazione logica è abilitata o disabilitata con [**glEnable**](glenable.md) e **glDisable** usando la costante simbolica GL \_ logica \_ op.</span><span class="sxs-lookup"><span data-stu-id="31b6f-157">The logical operation is enabled or disabled with [**glEnable**](glenable.md) and **glDisable** using the symbolic constant GL\_LOGIC\_OP.</span></span>

<span data-ttu-id="31b6f-158">Il parametro *OpCode* è una costante simbolica scelta nell'elenco seguente.</span><span class="sxs-lookup"><span data-stu-id="31b6f-158">The *opcode* parameter is a symbolic constant chosen from the list below.</span></span> <span data-ttu-id="31b6f-159">Nella spiegazione delle operazioni logiche, *s* rappresenta l'indice dei colori in ingresso e *d* rappresenta l'indice nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="31b6f-159">In the explanation of the logical operations, *s* represents the incoming color index and *d* represents the index in the framebuffer.</span></span> <span data-ttu-id="31b6f-160">Vengono utilizzati gli operatori di linguaggio C standard.</span><span class="sxs-lookup"><span data-stu-id="31b6f-160">Standard C-language operators are used.</span></span> <span data-ttu-id="31b6f-161">Poiché gli operatori bit per bit suggeriscono, l'operazione logica viene applicata indipendentemente a ogni coppia di bit degli indici di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="31b6f-161">As these bitwise operators suggest, the logical operation is applied independently to each bit pair of the source and destination indexes.</span></span>

<span data-ttu-id="31b6f-162">Le operazioni di pixel logici non vengono applicate ai buffer dei colori RGBA.</span><span class="sxs-lookup"><span data-stu-id="31b6f-162">Logical pixel operations are not applied to RGBA color buffers.</span></span>

<span data-ttu-id="31b6f-163">Quando per il disegno è abilitato più di un buffer di indice dei colori, le operazioni logiche vengono eseguite separatamente per ogni buffer abilitato, usando il contenuto del buffer per l'indice di destinazione (vedere [**glDrawBuffer**](gldrawbuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="31b6f-163">When more than one color-index buffer is enabled for drawing, logical operations are done separately for each enabled buffer, using the contents of that buffer for the destination index (see [**glDrawBuffer**](gldrawbuffer.md)).</span></span>

<span data-ttu-id="31b6f-164">Il parametro *OpCode* deve essere uno dei 16 valori accettati.</span><span class="sxs-lookup"><span data-stu-id="31b6f-164">The *opcode* parameter must be one of the 16 accepted values.</span></span> <span data-ttu-id="31b6f-165">Altri valori generano un errore.</span><span class="sxs-lookup"><span data-stu-id="31b6f-165">Other values result in an error.</span></span>

<span data-ttu-id="31b6f-166">Le funzioni seguenti consentono di recuperare informazioni correlate a **glLogicOp**:</span><span class="sxs-lookup"><span data-stu-id="31b6f-166">The following functions retrieve information related to **glLogicOp**:</span></span>

<span data-ttu-id="31b6f-167">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ \_ modalità operativa logica \_</span><span class="sxs-lookup"><span data-stu-id="31b6f-167">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LOGIC\_OP\_MODE</span></span>

<span data-ttu-id="31b6f-168">[**glIsEnabled**](glisenabled.md) con argomento GL \_ logica \_ op</span><span class="sxs-lookup"><span data-stu-id="31b6f-168">[**glIsEnabled**](glisenabled.md) with argument GL\_LOGIC\_OP</span></span>

## <a name="requirements"></a><span data-ttu-id="31b6f-169">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31b6f-169">Requirements</span></span>



| <span data-ttu-id="31b6f-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="31b6f-170">Requirement</span></span> | <span data-ttu-id="31b6f-171">Valore</span><span class="sxs-lookup"><span data-stu-id="31b6f-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31b6f-172">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31b6f-172">Minimum supported client</span></span><br/> | <span data-ttu-id="31b6f-173">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="31b6f-173">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="31b6f-174">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31b6f-174">Minimum supported server</span></span><br/> | <span data-ttu-id="31b6f-175">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="31b6f-175">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="31b6f-176">Intestazione</span><span class="sxs-lookup"><span data-stu-id="31b6f-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="31b6f-177"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="31b6f-177"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="31b6f-178">Libreria</span><span class="sxs-lookup"><span data-stu-id="31b6f-178">Library</span></span><br/>                  | <dl> <span data-ttu-id="31b6f-179"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31b6f-179"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="31b6f-180">DLL</span><span class="sxs-lookup"><span data-stu-id="31b6f-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31b6f-181"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31b6f-181"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31b6f-182">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31b6f-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31b6f-183">**glAlphaFunc**</span><span class="sxs-lookup"><span data-stu-id="31b6f-183">**glAlphaFunc**</span></span>](glalphafunc.md)
</dt> <dt>

[<span data-ttu-id="31b6f-184">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="31b6f-184">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="31b6f-185">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="31b6f-185">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="31b6f-186">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="31b6f-186">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="31b6f-187">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="31b6f-187">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="31b6f-188">**Remo**</span><span class="sxs-lookup"><span data-stu-id="31b6f-188">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="31b6f-189">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="31b6f-189">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="31b6f-190">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="31b6f-190">**glStencilOp**</span></span>](glstencilop.md)
</dt> </dl>

 

 





