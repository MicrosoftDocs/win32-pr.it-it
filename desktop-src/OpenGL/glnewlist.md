---
title: funzione glNewList (GL. h)
description: Le funzioni glNewList e glEndList creano o sostituiscono un elenco di visualizzazione. | funzione glNewList (GL. h)
ms.assetid: 9c6556d4-855f-4cba-94cc-27b5f1e4607a
keywords:
- funzione glNewList OpenGL
topic_type:
- apiref
api_name:
- glNewList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6135f67c07f69d24df67d4f1899404359efaa7aa
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321644"
---
# <a name="glnewlist-function"></a><span data-ttu-id="18ca3-105">glNewList (funzione)</span><span class="sxs-lookup"><span data-stu-id="18ca3-105">glNewList function</span></span>

<span data-ttu-id="18ca3-106">Le funzioni **glNewList** e [**glEndList**](glendlist.md) creano o sostituiscono un elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="18ca3-106">The **glNewList** and [**glEndList**](glendlist.md) functions create or replace a display list.</span></span>

## <a name="syntax"></a><span data-ttu-id="18ca3-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18ca3-107">Syntax</span></span>


```C++
void WINAPI glNewList(
   GLuint list,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="18ca3-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="18ca3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18ca3-109">*list*</span><span class="sxs-lookup"><span data-stu-id="18ca3-109">*list*</span></span> 
</dt> <dd>

<span data-ttu-id="18ca3-110">Nome dell'elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="18ca3-110">The display list name.</span></span>

</dd> <dt>

<span data-ttu-id="18ca3-111">*mode*</span><span class="sxs-lookup"><span data-stu-id="18ca3-111">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="18ca3-112">Modalità di compilazione.</span><span class="sxs-lookup"><span data-stu-id="18ca3-112">The compilation mode.</span></span> <span data-ttu-id="18ca3-113">Vengono accettati i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="18ca3-113">The following values are accepted.</span></span>



| <span data-ttu-id="18ca3-114">Valore</span><span class="sxs-lookup"><span data-stu-id="18ca3-114">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="18ca3-115">Significato</span><span class="sxs-lookup"><span data-stu-id="18ca3-115">Meaning</span></span>                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="GL_COMPILE"></span><span id="gl_compile"></span><dl> <span data-ttu-id="18ca3-116"><dt>**\_compilazione GL**</dt></span><span class="sxs-lookup"><span data-stu-id="18ca3-116"><dt>**GL\_COMPILE**</dt></span></span> </dl>                                       | <span data-ttu-id="18ca3-117">I comandi sono semplicemente compilati.</span><span class="sxs-lookup"><span data-stu-id="18ca3-117">Commands are merely compiled.</span></span><br/>                                     |
| <span id="GL_COMPILE_AND_EXECUTE"></span><span id="gl_compile_and_execute"></span><dl> <span data-ttu-id="18ca3-118"><dt>**\_compilazione \_ ed \_ esecuzione GL**</dt></span><span class="sxs-lookup"><span data-stu-id="18ca3-118"><dt>**GL\_COMPILE\_AND\_EXECUTE**</dt></span></span> </dl> | <span data-ttu-id="18ca3-119">I comandi vengono eseguiti Man mano che vengono compilati nell'elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="18ca3-119">Commands are executed as they are compiled into the display list.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18ca3-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="18ca3-120">Return value</span></span>

<span data-ttu-id="18ca3-121">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="18ca3-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="18ca3-122">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="18ca3-122">Error codes</span></span>

<span data-ttu-id="18ca3-123">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="18ca3-123">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="18ca3-124">Nome</span><span class="sxs-lookup"><span data-stu-id="18ca3-124">Name</span></span>                                                                                                  | <span data-ttu-id="18ca3-125">Significato</span><span class="sxs-lookup"><span data-stu-id="18ca3-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="18ca3-126"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="18ca3-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="18ca3-127">*List* è zero.</span><span class="sxs-lookup"><span data-stu-id="18ca3-127">*list* was zero.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="18ca3-128"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="18ca3-128"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="18ca3-129">la *modalità* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="18ca3-129">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="18ca3-130"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="18ca3-130"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="18ca3-131">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="18ca3-131">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="18ca3-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="18ca3-132">Remarks</span></span>

<span data-ttu-id="18ca3-133">Gli elenchi di visualizzazione sono gruppi di comandi OpenGL archiviati per l'esecuzione successiva.</span><span class="sxs-lookup"><span data-stu-id="18ca3-133">Display lists are groups of OpenGL commands that have been stored for subsequent execution.</span></span> <span data-ttu-id="18ca3-134">Gli elenchi di visualizzazione vengono creati con **glNewList**.</span><span class="sxs-lookup"><span data-stu-id="18ca3-134">The display lists are created with **glNewList**.</span></span> <span data-ttu-id="18ca3-135">Tutti i comandi successivi vengono inseriti nell'elenco di visualizzazione, nell'ordine emesso, fino a quando non viene chiamato **glEndList** .</span><span class="sxs-lookup"><span data-stu-id="18ca3-135">All subsequent commands are placed in the display list, in the order issued, until **glEndList** is called.</span></span>

<span data-ttu-id="18ca3-136">La funzione **glNewList** ha due parametri.</span><span class="sxs-lookup"><span data-stu-id="18ca3-136">The **glNewList** function has two parameters.</span></span> <span data-ttu-id="18ca3-137">Il primo parametro, *List*, è un numero intero positivo che diventa il nome univoco per l'elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="18ca3-137">The first parameter, *list*, is a positive integer that becomes the unique name for the display list.</span></span> <span data-ttu-id="18ca3-138">I nomi possono essere creati e riservati con [**glGenLists**](glgenlists.md) e sono stati testati per l'univocità con l'indisponibilità [**.**](glislist.md)</span><span class="sxs-lookup"><span data-stu-id="18ca3-138">Names can be created and reserved with [**glGenLists**](glgenlists.md) and tested for uniqueness with [**glIsList**](glislist.md).</span></span> <span data-ttu-id="18ca3-139">Il secondo parametro, *mode*, è una costante simbolica che può assumere uno dei due valori precedenti.</span><span class="sxs-lookup"><span data-stu-id="18ca3-139">The second parameter, *mode*, is a symbolic constant that can assume one of the two preceding values.</span></span>

<span data-ttu-id="18ca3-140">Alcuni comandi non vengono compilati nell'elenco di visualizzazione, ma vengono eseguiti immediatamente, indipendentemente dalla modalità elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="18ca3-140">Certain commands are not compiled into the display list, but are executed immediately, regardless of the display list mode.</span></span> <span data-ttu-id="18ca3-141">Questi comandi sono [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**Glis**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md)e tutte le routine [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) .</span><span class="sxs-lookup"><span data-stu-id="18ca3-141">These commands are [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**glIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md), and all of the [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) routines.</span></span>

<span data-ttu-id="18ca3-142">Analogamente, [**glTexImage2D**](glteximage2d.md) e [**glTexImage1D**](glteximage1d.md) vengono eseguiti immediatamente e non vengono compilati nell'elenco di visualizzazione quando il primo argomento è la trama del proxy GL \_ \_ \_ 2D o GL proxy texture \_ \_ \_ 1D, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="18ca3-142">Similarly, [**glTexImage2D**](glteximage2d.md) and [**glTexImage1D**](glteximage1d.md) are executed immediately and not compiled into the display list when their first argument is GL\_PROXY\_TEXTURE\_2D or GL\_PROXY\_TEXTURE\_1D, respectively.</span></span>

<span data-ttu-id="18ca3-143">Quando viene rilevata la funzione **glEndList** , la definizione dell'elenco di visualizzazione viene completata associando l'elenco all' *elenco* dei nomi univoci (specificato nel comando **glNewList** ).</span><span class="sxs-lookup"><span data-stu-id="18ca3-143">When the **glEndList** function is encountered, the display list definition is completed by associating the list with the unique name *list* (specified in the **glNewList** command).</span></span> <span data-ttu-id="18ca3-144">Se un elenco di visualizzazione con l' *elenco dei* nomi esiste già, viene sostituito solo quando viene chiamato **glEndList** .</span><span class="sxs-lookup"><span data-stu-id="18ca3-144">If a display list with name *list* already exists, it is replaced only when **glEndList** is called.</span></span>

<span data-ttu-id="18ca3-145">Le funzioni [**glCallList**](glcalllist.md) e [**glCallLists**](glcalllists.md) possono essere immesse negli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="18ca3-145">The [**glCallList**](glcalllist.md) and [**glCallLists**](glcalllists.md) functions can be entered into display lists.</span></span> <span data-ttu-id="18ca3-146">I comandi nell'elenco di visualizzazione o negli elenchi eseguiti da **glCallList** o **glCallLists** non sono inclusi nell'elenco di visualizzazione creato, anche se la modalità di creazione dell'elenco è la \_ compilazione e l'esecuzione di GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="18ca3-146">The commands in the display list or lists executed by **glCallList** or **glCallLists** are not included in the display list being created, even if the list creation mode is GL\_COMPILE\_AND\_EXECUTE.</span></span>

<span data-ttu-id="18ca3-147">La funzione seguente recupera le informazioni correlate a **glNewList**:</span><span class="sxs-lookup"><span data-stu-id="18ca3-147">The following function retrieves information related to **glNewList**:</span></span>

<span data-ttu-id="18ca3-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ modalità matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="18ca3-148">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="18ca3-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18ca3-149">Requirements</span></span>



| <span data-ttu-id="18ca3-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="18ca3-150">Requirement</span></span> | <span data-ttu-id="18ca3-151">Valore</span><span class="sxs-lookup"><span data-stu-id="18ca3-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18ca3-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18ca3-152">Minimum supported client</span></span><br/> | <span data-ttu-id="18ca3-153">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="18ca3-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="18ca3-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18ca3-154">Minimum supported server</span></span><br/> | <span data-ttu-id="18ca3-155">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="18ca3-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="18ca3-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="18ca3-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="18ca3-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="18ca3-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="18ca3-158">Libreria</span><span class="sxs-lookup"><span data-stu-id="18ca3-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="18ca3-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18ca3-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="18ca3-160">DLL</span><span class="sxs-lookup"><span data-stu-id="18ca3-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18ca3-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18ca3-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18ca3-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18ca3-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18ca3-163">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="18ca3-163">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="18ca3-164">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="18ca3-164">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="18ca3-165">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="18ca3-165">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="18ca3-166">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="18ca3-166">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="18ca3-167">**Remo**</span><span class="sxs-lookup"><span data-stu-id="18ca3-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="18ca3-168">**glEndList**</span><span class="sxs-lookup"><span data-stu-id="18ca3-168">**glEndList**</span></span>](glendlist.md)
</dt> <dt>

[<span data-ttu-id="18ca3-169">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="18ca3-169">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="18ca3-170">**Pagina di**</span><span class="sxs-lookup"><span data-stu-id="18ca3-170">**glIsList**</span></span>](glislist.md)
</dt> </dl>

 

 





