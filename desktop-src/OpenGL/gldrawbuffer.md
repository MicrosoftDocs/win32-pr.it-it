---
title: funzione glDrawBuffer (GL. h)
description: La funzione glDrawBuffer specifica i buffer dei colori da disegnare in.
ms.assetid: ea625699-303b-4e60-b9aa-771949a8d52d
keywords:
- funzione glDrawBuffer OpenGL
topic_type:
- apiref
api_name:
- glDrawBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a99bd2b184766f1621d89b2c8d642902d300e14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301266"
---
# <a name="gldrawbuffer-function"></a><span data-ttu-id="f5cb4-104">glDrawBuffer (funzione)</span><span class="sxs-lookup"><span data-stu-id="f5cb4-104">glDrawBuffer function</span></span>

<span data-ttu-id="f5cb4-105">La funzione **glDrawBuffer** specifica i buffer dei colori da disegnare in.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-105">The **glDrawBuffer** function specifies which color buffers are to be drawn into.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5cb4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5cb4-106">Syntax</span></span>


```C++
void WINAPI glDrawBuffer(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="f5cb4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5cb4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5cb4-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="f5cb4-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="f5cb4-109">Consente di specificare fino a quattro buffer di colore da disegnare con le costanti simboliche accettabili seguenti.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-109">Specifies up to four color buffers to be drawn into with the following acceptable symbolic constants.</span></span>



| <span data-ttu-id="f5cb4-110">Valore</span><span class="sxs-lookup"><span data-stu-id="f5cb4-110">Value</span></span>                                                                                                                                                                       | <span data-ttu-id="f5cb4-111">Significato</span><span class="sxs-lookup"><span data-stu-id="f5cb4-111">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_NONE"></span><span id="gl_none"></span><dl> <span data-ttu-id="f5cb4-112"><dt>**GL \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="f5cb4-112"><dt>**GL\_NONE**</dt></span></span> </dl>                                 | <span data-ttu-id="f5cb4-113">Non viene scritto alcun buffer dei colori.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-113">No color buffers are written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_FRONT_LEFT"></span><span id="gl_front_left"></span><dl> <span data-ttu-id="f5cb4-114"><dt>**GL \_ anteriore \_ sinistra**</dt></span><span class="sxs-lookup"><span data-stu-id="f5cb4-114"><dt>**GL\_FRONT\_LEFT**</dt></span></span> </dl>              | <span data-ttu-id="f5cb4-115">Viene scritto solo il buffer dei colori in primo piano.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-115">Only the front-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT_RIGHT"></span><span id="gl_front_right"></span><dl> <span data-ttu-id="f5cb4-116"><dt>**GL in \_ primo piano \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f5cb4-116"><dt>**GL\_FRONT\_RIGHT**</dt></span></span> </dl>           | <span data-ttu-id="f5cb4-117">Viene scritto solo il buffer dei colori front-right.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-117">Only the front-right color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                     |
| <span id="GL_BACK_LEFT"></span><span id="gl_back_left"></span><dl> <span data-ttu-id="f5cb4-118"><dt>**GL \_ a \_ sinistra**</dt></span><span class="sxs-lookup"><span data-stu-id="f5cb4-118"><dt>**GL\_BACK\_LEFT**</dt></span></span> </dl>                 | <span data-ttu-id="f5cb4-119">Viene scritto solo il buffer dei colori Back-left.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-119">Only the back-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="GL_BACK_RIGHT"></span><span id="gl_back_right"></span><dl> <span data-ttu-id="f5cb4-120"><dt>**GL \_ a \_ destra**</dt></span><span class="sxs-lookup"><span data-stu-id="f5cb4-120"><dt>**GL\_BACK\_RIGHT**</dt></span></span> </dl>              | <span data-ttu-id="f5cb4-121">Viene scritto solo il buffer dei colori back-right.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-121">Only the back-right color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="GL_FRONT"></span><span id="gl_front"></span><dl> <span data-ttu-id="f5cb4-122"><dt>**\_primo piano GL**</dt></span><span class="sxs-lookup"><span data-stu-id="f5cb4-122"><dt>**GL\_FRONT**</dt></span></span> </dl>                              | <span data-ttu-id="f5cb4-123">Vengono scritti solo i buffer dei colori Front-Left e front-right.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-123">Only the front-left and front-right color buffers are written.</span></span> <span data-ttu-id="f5cb4-124">Se non è presente alcun buffer di colore front-right, viene scritto solo il buffer di colore anteriore sinistro.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-124">If there is no front-right color buffer, only the front left-color buffer is written.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="GL_BACK"></span><span id="gl_back"></span><dl> <span data-ttu-id="f5cb4-125"><dt>**indietro per GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f5cb4-125"><dt>**GL\_BACK**</dt></span></span> </dl>                                 | <span data-ttu-id="f5cb4-126">Vengono scritti solo i buffer dei colori Back-left e back-right.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-126">Only the back-left and back-right color buffers are written.</span></span> <span data-ttu-id="f5cb4-127">Se non è presente alcun buffer dei colori di back-right, viene scritto solo il buffer di colore Back-left.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-127">If there is no back-right color buffer, only the back-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                  |
| <span id="GL_LEFT"></span><span id="gl_left"></span><dl> <span data-ttu-id="f5cb4-128"><dt>**GL a \_ sinistra**</dt></span><span class="sxs-lookup"><span data-stu-id="f5cb4-128"><dt>**GL\_LEFT**</dt></span></span> </dl>                                 | <span data-ttu-id="f5cb4-129">Vengono scritti solo i buffer dei colori Front-Left e back-left.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-129">Only the front-left and back-left color buffers are written.</span></span> <span data-ttu-id="f5cb4-130">Se non è presente alcun buffer dei colori Back-left, viene scritto solo il buffer di colore in primo piano.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-130">If there is no back-left color buffer, only the front-left color buffer is written.</span></span><br/>                                                                                                                                                                                                                                                  |
| <span id="GL_RIGHT"></span><span id="gl_right"></span><dl> <span data-ttu-id="f5cb4-131"><dt>**GL a \_ destra**</dt></span><span class="sxs-lookup"><span data-stu-id="f5cb4-131"><dt>**GL\_RIGHT**</dt></span></span> </dl>                              | <span data-ttu-id="f5cb4-132">Vengono scritti solo i buffer dei colori Front-Right e back-right.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-132">Only the front-right and back-right color buffers are written.</span></span> <span data-ttu-id="f5cb4-133">Se non è presente alcun buffer dei colori back-right, viene scritto solo il buffer del colore front-right.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-133">If there is no back-right color buffer, only the front-right color buffer is written.</span></span><br/>                                                                                                                                                                                                                                              |
| <span id="GL_FRONT_AND_BACK"></span><span id="gl_front_and_back"></span><dl> <span data-ttu-id="f5cb4-134"><dt>**\_primo \_ e \_ indietro GL**</dt></span><span class="sxs-lookup"><span data-stu-id="f5cb4-134"><dt>**GL\_FRONT\_AND\_BACK**</dt></span></span> </dl> | <span data-ttu-id="f5cb4-135">Vengono scritti tutti i buffer di colore anteriore e posteriore (in primo piano, a sinistra, in primo piano, a sinistra, a destra).</span><span class="sxs-lookup"><span data-stu-id="f5cb4-135">All the front and back color buffers (front-left, front-right, back-left, back-right) are written.</span></span> <span data-ttu-id="f5cb4-136">Se non sono presenti buffer di colore di sfondo, vengono scritti solo i buffer dei colori Front-Left e front-right.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-136">If there are no back color buffers, only the front-left and front-right color buffers are written.</span></span> <span data-ttu-id="f5cb4-137">Se non sono presenti buffer di colore corretti, vengono scritti solo i buffer dei colori in primo piano e a sinistra.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-137">If there are no right color buffers, only the front-left and back-left color buffers are written.</span></span> <span data-ttu-id="f5cb4-138">Se non sono presenti buffer a destra o a sinistra, viene scritto solo il buffer dei colori in primo piano.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-138">If there are no right or back color buffers, only the front-left color buffer is written.</span></span><br/> |
| <span id="GL_AUXi"></span><span id="gl_auxi"></span><span id="GL_AUXI"></span><dl> <span data-ttu-id="f5cb4-139"><dt>**\_Auxi GL**</dt></span><span class="sxs-lookup"><span data-stu-id="f5cb4-139"><dt>**GL\_AUXi**</dt></span></span> </dl>       | <span data-ttu-id="f5cb4-140">*Viene scritto* solo il buffer dei colori ausiliario; *i* è compreso tra 0 e GL \_ aux \_ buffers-1.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-140">Only the auxiliary color buffer *i* is written; *i* is between 0 and GL\_AUX\_BUFFERS - 1.</span></span> <span data-ttu-id="f5cb4-141">(GL \_ \_I buffer aux non corrispondono al limite massimo. utilizzare [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) per eseguire una query sul numero di buffer ausiliari disponibili.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-141">(GL\_AUX\_BUFFERS is not the upper limit; use [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) to query the number of available auxiliary buffers.)</span></span><br/>                                                                                                                            |



 

<span data-ttu-id="f5cb4-142">Il valore predefinito è GL \_ front per i contesti con buffer singolo e GL \_ indietro per i contesti con doppio buffer.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-142">The default value is GL\_FRONT for single-buffered contexts, and GL\_BACK for double-buffered contexts.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5cb4-143">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5cb4-143">Return value</span></span>

<span data-ttu-id="f5cb4-144">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-144">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f5cb4-145">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="f5cb4-145">Error codes</span></span>

<span data-ttu-id="f5cb4-146">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="f5cb4-146">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f5cb4-147">Nome</span><span class="sxs-lookup"><span data-stu-id="f5cb4-147">Name</span></span>                                                                                                  | <span data-ttu-id="f5cb4-148">Significato</span><span class="sxs-lookup"><span data-stu-id="f5cb4-148">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f5cb4-149"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f5cb4-149"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="f5cb4-150">la *modalità* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-150">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="f5cb4-151"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f5cb4-151"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f5cb4-152">Nessuno dei buffer indicati dalla *modalità* esisteva.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-152">None of the buffers indicated by *mode* existed.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="f5cb4-153"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f5cb4-153"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f5cb4-154">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="f5cb4-154">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |


## <a name="remarks"></a><span data-ttu-id="f5cb4-155">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5cb4-155">Remarks</span></span>

<span data-ttu-id="f5cb4-156">Quando i colori vengono scritti nel framebuffer, vengono scritti nei buffer dei colori specificati da **glDrawBuffer**.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-156">When colors are written to the framebuffer, they are written into the color buffers specified by **glDrawBuffer**.</span></span>

<span data-ttu-id="f5cb4-157">Se per il disegno è selezionato più di un buffer di colore, le operazioni di fusione o logiche vengono calcolate e applicate in modo indipendente per ogni buffer di colore e possono produrre risultati diversi in ogni buffer.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-157">If more than one color buffer is selected for drawing, then blending or logical operations are computed and applied independently for each color buffer and can produce different results in each buffer.</span></span>

<span data-ttu-id="f5cb4-158">I contesti monoscopiche includono solo i buffer a sinistra e i contesti stereoscopici includono entrambi i buffer a sinistra e a destra.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-158">Monoscopic contexts include only left buffers, and stereoscopic contexts include both left and right buffers.</span></span> <span data-ttu-id="f5cb4-159">Analogamente, i contesti con buffer singolo includono solo i buffer di primo livello e i contesti a doppio buffer includono i buffer front e back.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-159">Likewise, single-buffered contexts include only front buffers, and double-buffered contexts include both front and back buffers.</span></span> <span data-ttu-id="f5cb4-160">Il contesto è selezionato nell'inizializzazione di OpenGL.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-160">The context is selected at OpenGL initialization.</span></span>

<span data-ttu-id="f5cb4-161">È sempre il caso GL \_ aux *i* = GL \_ AUX0 + *i*.</span><span class="sxs-lookup"><span data-stu-id="f5cb4-161">It is always the case that GL\_AUX *i* = GL\_AUX0 + *i*.</span></span>

<span data-ttu-id="f5cb4-162">Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glDrawBuffer** :</span><span class="sxs-lookup"><span data-stu-id="f5cb4-162">The following functions retrieve information related to the **glDrawBuffer** function:</span></span>

<span data-ttu-id="f5cb4-163">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con il \_ buffer di disegnato GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="f5cb4-163">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DRAW\_BUFFER</span></span>

<span data-ttu-id="f5cb4-164">**glGet** con gli argomenti GL \_ aux \_ buffers</span><span class="sxs-lookup"><span data-stu-id="f5cb4-164">**glGet** with argument GL\_AUX\_BUFFERS</span></span>

## <a name="requirements"></a><span data-ttu-id="f5cb4-165">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5cb4-165">Requirements</span></span>



| <span data-ttu-id="f5cb4-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5cb4-166">Requirement</span></span> | <span data-ttu-id="f5cb4-167">Valore</span><span class="sxs-lookup"><span data-stu-id="f5cb4-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5cb4-168">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5cb4-168">Minimum supported client</span></span><br/> | <span data-ttu-id="f5cb4-169">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f5cb4-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f5cb4-170">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5cb4-170">Minimum supported server</span></span><br/> | <span data-ttu-id="f5cb4-171">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f5cb4-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f5cb4-172">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5cb4-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5cb4-173"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5cb4-173"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f5cb4-174">Libreria</span><span class="sxs-lookup"><span data-stu-id="f5cb4-174">Library</span></span><br/>                  | <dl> <span data-ttu-id="f5cb4-175"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5cb4-175"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f5cb4-176">DLL</span><span class="sxs-lookup"><span data-stu-id="f5cb4-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5cb4-177"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5cb4-177"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5cb4-178">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5cb4-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5cb4-179">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f5cb4-179">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f5cb4-180">**glBlendFunc**</span><span class="sxs-lookup"><span data-stu-id="f5cb4-180">**glBlendFunc**</span></span>](glblendfunc.md)
</dt> <dt>

[<span data-ttu-id="f5cb4-181">**glColorMask**</span><span class="sxs-lookup"><span data-stu-id="f5cb4-181">**glColorMask**</span></span>](glcolormask.md)
</dt> <dt>

[<span data-ttu-id="f5cb4-182">**Remo**</span><span class="sxs-lookup"><span data-stu-id="f5cb4-182">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f5cb4-183">**glGet**</span><span class="sxs-lookup"><span data-stu-id="f5cb4-183">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="f5cb4-184">**glIndexMask**</span><span class="sxs-lookup"><span data-stu-id="f5cb4-184">**glIndexMask**</span></span>](glindexmask.md)
</dt> <dt>

[<span data-ttu-id="f5cb4-185">**glLogicOp**</span><span class="sxs-lookup"><span data-stu-id="f5cb4-185">**glLogicOp**</span></span>](gllogicop.md)
</dt> <dt>

[<span data-ttu-id="f5cb4-186">**glReadBuffer**</span><span class="sxs-lookup"><span data-stu-id="f5cb4-186">**glReadBuffer**</span></span>](glreadbuffer.md)
</dt> </dl>

 

 





