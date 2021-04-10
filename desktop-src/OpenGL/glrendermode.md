---
title: funzione glRenderMode (GL. h)
description: La funzione glRenderMode imposta la modalità di rasterizzazione.
ms.assetid: bcbc3bba-c552-425b-8284-6cadff0c9f56
keywords:
- funzione glRenderMode OpenGL
topic_type:
- apiref
api_name:
- glRenderMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af07d2492d70f9c0a3a764d767b52b2f71204939
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121450"
---
# <a name="glrendermode-function"></a><span data-ttu-id="bab4b-104">glRenderMode (funzione)</span><span class="sxs-lookup"><span data-stu-id="bab4b-104">glRenderMode function</span></span>

<span data-ttu-id="bab4b-105">La funzione **glRenderMode** imposta la modalità di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="bab4b-105">The **glRenderMode** function sets the rasterization mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="bab4b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bab4b-106">Syntax</span></span>


```C++
GLint WINAPI glRenderMode(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="bab4b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="bab4b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bab4b-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="bab4b-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="bab4b-109">Modalità di rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="bab4b-109">The rasterization mode.</span></span> <span data-ttu-id="bab4b-110">Vengono accettati i tre valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bab4b-110">The following three values are accepted.</span></span> <span data-ttu-id="bab4b-111">Il valore predefinito è GL \_ Render.</span><span class="sxs-lookup"><span data-stu-id="bab4b-111">The default value is GL\_RENDER.</span></span>



| <span data-ttu-id="bab4b-112">Valore</span><span class="sxs-lookup"><span data-stu-id="bab4b-112">Value</span></span>                                                                                                                                                   | <span data-ttu-id="bab4b-113">Significato</span><span class="sxs-lookup"><span data-stu-id="bab4b-113">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_RENDER"></span><span id="gl_render"></span><dl> <span data-ttu-id="bab4b-114"><dt>**\_rendering GL**</dt></span><span class="sxs-lookup"><span data-stu-id="bab4b-114"><dt>**GL\_RENDER**</dt></span></span> </dl>       | <span data-ttu-id="bab4b-115">Modalità di rendering.</span><span class="sxs-lookup"><span data-stu-id="bab4b-115">Render mode.</span></span> <span data-ttu-id="bab4b-116">Le primitive vengono rasterizzate e producono frammenti di pixel, che vengono scritti nel framebuffer.</span><span class="sxs-lookup"><span data-stu-id="bab4b-116">Primitives are rasterized, producing pixel fragments, which are written into the framebuffer.</span></span> <span data-ttu-id="bab4b-117">Si tratta della modalità normale e anche della modalità predefinita.</span><span class="sxs-lookup"><span data-stu-id="bab4b-117">This is the normal mode and also the default mode.</span></span><br/>                                                                                                                                                                                                      |
| <span id="GL_SELECT"></span><span id="gl_select"></span><dl> <span data-ttu-id="bab4b-118"><dt>**\_selezione GL**</dt></span><span class="sxs-lookup"><span data-stu-id="bab4b-118"><dt>**GL\_SELECT**</dt></span></span> </dl>       | <span data-ttu-id="bab4b-119">Modalità di selezione.</span><span class="sxs-lookup"><span data-stu-id="bab4b-119">Selection mode.</span></span> <span data-ttu-id="bab4b-120">Non viene prodotto alcun frammento di pixel e non viene apportata alcuna modifica al contenuto del framebuffer.</span><span class="sxs-lookup"><span data-stu-id="bab4b-120">No pixel fragments are produced, and no change to the framebuffer contents is made.</span></span> <span data-ttu-id="bab4b-121">Al contrario, un record dei nomi delle primitive che sarebbero stati disegnati se la modalità di rendering era GL \_ Render viene restituito in un buffer Select, che deve essere creato (vedere [**glSelectBuffer**](glselectbuffer.md)) prima di immettere la modalità di selezione.</span><span class="sxs-lookup"><span data-stu-id="bab4b-121">Instead, a record of the names of primitives that would have been drawn if the render mode was GL\_RENDER is returned in a select buffer, which must be created (see [**glSelectBuffer**](glselectbuffer.md)) before selection mode is entered.</span></span><br/>               |
| <span id="GL_FEEDBACK"></span><span id="gl_feedback"></span><dl> <span data-ttu-id="bab4b-122"><dt>**\_feedback GL**</dt></span><span class="sxs-lookup"><span data-stu-id="bab4b-122"><dt>**GL\_FEEDBACK**</dt></span></span> </dl> | <span data-ttu-id="bab4b-123">Modalità di feedback.</span><span class="sxs-lookup"><span data-stu-id="bab4b-123">Feedback mode.</span></span> <span data-ttu-id="bab4b-124">Non viene prodotto alcun frammento di pixel e non viene apportata alcuna modifica al contenuto del framebuffer.</span><span class="sxs-lookup"><span data-stu-id="bab4b-124">No pixel fragments are produced, and no change to the framebuffer contents is made.</span></span> <span data-ttu-id="bab4b-125">Al contrario, le coordinate e gli attributi dei vertici che sarebbero stati disegnati avevano la modalità di rendering GL \_ Render sono restituiti in un buffer di feedback, che è necessario creare (vedere [**glFeedbackBuffer**](glfeedbackbuffer.md)) prima di immettere la modalità di feedback.</span><span class="sxs-lookup"><span data-stu-id="bab4b-125">Instead, the coordinates and attributes of vertices that would have been drawn had the render mode been GL\_RENDER are returned in a feedback buffer, which must be created (see [**glFeedbackBuffer**](glfeedbackbuffer.md)) before feedback mode is entered.</span></span><br/> |



 

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="bab4b-126">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="bab4b-126">Error codes</span></span>

<span data-ttu-id="bab4b-127">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="bab4b-127">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="bab4b-128">Nome</span><span class="sxs-lookup"><span data-stu-id="bab4b-128">Name</span></span>                                                                                                  | <span data-ttu-id="bab4b-129">Significato</span><span class="sxs-lookup"><span data-stu-id="bab4b-129">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bab4b-130"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bab4b-130"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="bab4b-131">la *modalità* non è uno dei tre valori accettati.</span><span class="sxs-lookup"><span data-stu-id="bab4b-131">*mode* was not one of three accepted values.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="bab4b-132"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bab4b-132"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="bab4b-133">La funzione è stata chiamata con l'argomento GL \_ Select prima che [**glSelectBuffer**](glselectbuffer.md) venisse chiamato almeno una volta.</span><span class="sxs-lookup"><span data-stu-id="bab4b-133">The function was called with argument GL\_SELECT before [**glSelectBuffer**](glselectbuffer.md) was called at least once.</span></span><br/>       |
| <dl> <span data-ttu-id="bab4b-134"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bab4b-134"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="bab4b-135">La funzione è stata chiamata con l'argomento GL \_ feedback prima che [**glBeedbackBuffer**](glfeedbackbuffer.md) venisse chiamato almeno una volta.</span><span class="sxs-lookup"><span data-stu-id="bab4b-135">The function was called with argument GL\_FEEDBACK before [**glBeedbackBuffer**](glfeedbackbuffer.md) was called at least once.</span></span><br/> |
| <dl> <span data-ttu-id="bab4b-136"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bab4b-136"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="bab4b-137">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="bab4b-137">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="bab4b-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="bab4b-138">Remarks</span></span>

<span data-ttu-id="bab4b-139">La funzione **glRenderMode** accetta un argomento, *mode*, che può assumere uno dei tre valori predefiniti precedenti.</span><span class="sxs-lookup"><span data-stu-id="bab4b-139">The **glRenderMode** function takes one argument, *mode*, which can assume one of three predefined values above.</span></span>

<span data-ttu-id="bab4b-140">Il valore restituito della funzione **glRenderMode** è determinato dalla modalità di rendering nel momento in cui viene chiamato **glRenderMode** , anziché in base alla *modalità*.</span><span class="sxs-lookup"><span data-stu-id="bab4b-140">The return value of the **glRenderMode** function is determined by the render mode at the time **glRenderMode** is called, rather than by *mode*.</span></span> <span data-ttu-id="bab4b-141">I valori restituiti per le tre modalità di rendering sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="bab4b-141">The values returned for the three render modes are as follows.</span></span>



| <span data-ttu-id="bab4b-142">Valore</span><span class="sxs-lookup"><span data-stu-id="bab4b-142">Value</span></span>        | <span data-ttu-id="bab4b-143">Significato</span><span class="sxs-lookup"><span data-stu-id="bab4b-143">Meaning</span></span>                                                                 |
|--------------|-------------------------------------------------------------------------|
| <span data-ttu-id="bab4b-144">\_rendering GL</span><span class="sxs-lookup"><span data-stu-id="bab4b-144">GL\_RENDER</span></span>   | <span data-ttu-id="bab4b-145">Zero.</span><span class="sxs-lookup"><span data-stu-id="bab4b-145">Zero.</span></span>                                                                   |
| <span data-ttu-id="bab4b-146">\_selezione GL</span><span class="sxs-lookup"><span data-stu-id="bab4b-146">GL\_SELECT</span></span>   | <span data-ttu-id="bab4b-147">Numero di record di hit Transfer trasferiti nel buffer di selezione.</span><span class="sxs-lookup"><span data-stu-id="bab4b-147">The number of hit records transferred to the select buffer.</span></span>             |
| <span data-ttu-id="bab4b-148">\_feedback GL</span><span class="sxs-lookup"><span data-stu-id="bab4b-148">GL\_FEEDBACK</span></span> | <span data-ttu-id="bab4b-149">Numero di valori (non vertici) trasferiti al buffer di feedback.</span><span class="sxs-lookup"><span data-stu-id="bab4b-149">The number of values (not vertices) transferred to the feedback buffer.</span></span> |



 

<span data-ttu-id="bab4b-150">Per informazioni dettagliate sull'operazione di selezione e feedback, vedere [**glSelectBuffer**](glselectbuffer.md) e [**glFeedbackBuffer**](glfeedbackbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="bab4b-150">Refer to [**glSelectBuffer**](glselectbuffer.md) and [**glFeedbackBuffer**](glfeedbackbuffer.md) for more details concerning selection and feedback operation.</span></span>

<span data-ttu-id="bab4b-151">Se viene generato un errore, **glRenderMode** restituisce zero indipendentemente dalla modalità di rendering corrente.</span><span class="sxs-lookup"><span data-stu-id="bab4b-151">If an error is generated, **glRenderMode** returns zero regardless of the current render mode.</span></span>

<span data-ttu-id="bab4b-152">La funzione seguente recupera le informazioni correlate a **glRenderMode**:</span><span class="sxs-lookup"><span data-stu-id="bab4b-152">The following function retrieves information related to **glRenderMode**:</span></span>

<span data-ttu-id="bab4b-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con modalità di \_ rendering GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="bab4b-153">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="bab4b-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bab4b-154">Requirements</span></span>



| <span data-ttu-id="bab4b-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="bab4b-155">Requirement</span></span> | <span data-ttu-id="bab4b-156">Valore</span><span class="sxs-lookup"><span data-stu-id="bab4b-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bab4b-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bab4b-157">Minimum supported client</span></span><br/> | <span data-ttu-id="bab4b-158">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bab4b-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bab4b-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bab4b-159">Minimum supported server</span></span><br/> | <span data-ttu-id="bab4b-160">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bab4b-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bab4b-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bab4b-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="bab4b-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="bab4b-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="bab4b-163">Libreria</span><span class="sxs-lookup"><span data-stu-id="bab4b-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="bab4b-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bab4b-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="bab4b-165">DLL</span><span class="sxs-lookup"><span data-stu-id="bab4b-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bab4b-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bab4b-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bab4b-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bab4b-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bab4b-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="bab4b-168">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="bab4b-169">**Remo**</span><span class="sxs-lookup"><span data-stu-id="bab4b-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="bab4b-170">**glFeedbackBuffer**</span><span class="sxs-lookup"><span data-stu-id="bab4b-170">**glFeedbackBuffer**</span></span>](glfeedbackbuffer.md)
</dt> <dt>

[<span data-ttu-id="bab4b-171">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="bab4b-171">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="bab4b-172">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="bab4b-172">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="bab4b-173">**glPassThrough**</span><span class="sxs-lookup"><span data-stu-id="bab4b-173">**glPassThrough**</span></span>](glpassthrough.md)
</dt> <dt>

[<span data-ttu-id="bab4b-174">**glPushName**</span><span class="sxs-lookup"><span data-stu-id="bab4b-174">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="bab4b-175">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="bab4b-175">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





