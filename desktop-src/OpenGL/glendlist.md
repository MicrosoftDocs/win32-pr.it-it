---
title: funzione glEndList (GL. h)
description: Le funzioni glNewList e glEndList creano o sostituiscono un elenco di visualizzazione. | funzione glEndList (GL. h)
ms.assetid: dd749932-7b3c-47e5-8d91-90d272a7dc41
keywords:
- funzione glEndList OpenGL
topic_type:
- apiref
api_name:
- glEndList
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f8db8c2abea44d678268f804159b60fe695f96
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321717"
---
# <a name="glendlist-function"></a><span data-ttu-id="25588-105">glEndList (funzione)</span><span class="sxs-lookup"><span data-stu-id="25588-105">glEndList function</span></span>

<span data-ttu-id="25588-106">Le funzioni [**glNewList**](glnewlist.md) e **glEndList** creano o sostituiscono un elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="25588-106">The [**glNewList**](glnewlist.md) and **glEndList** functions create or replace a display list.</span></span>

## <a name="syntax"></a><span data-ttu-id="25588-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25588-107">Syntax</span></span>


```C++
void WINAPI glEndList(void);
```



## <a name="parameters"></a><span data-ttu-id="25588-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="25588-108">Parameters</span></span>

<span data-ttu-id="25588-109">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="25588-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="25588-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25588-110">Return value</span></span>

<span data-ttu-id="25588-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="25588-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="25588-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="25588-112">Error codes</span></span>

<span data-ttu-id="25588-113">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="25588-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="25588-114">Nome</span><span class="sxs-lookup"><span data-stu-id="25588-114">Name</span></span>                                                                                                  | <span data-ttu-id="25588-115">Significato</span><span class="sxs-lookup"><span data-stu-id="25588-115">Meaning</span></span>                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="25588-116"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="25588-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="25588-117">**glEndList** è stato chiamato senza un **glNewList** precedente o se **glNewList** è stato chiamato durante la definizione di un elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="25588-117">**glEndList** was called without a preceding **glNewList**, or if **glnewlist** was called while a display list was being defined.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="25588-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="25588-118">Remarks</span></span>

<span data-ttu-id="25588-119">Gli elenchi di visualizzazione sono gruppi di comandi OpenGL archiviati per l'esecuzione successiva.</span><span class="sxs-lookup"><span data-stu-id="25588-119">Display lists are groups of OpenGL commands that have been stored for subsequent execution.</span></span> <span data-ttu-id="25588-120">Gli elenchi di visualizzazione vengono creati con [**glNewList**](glnewlist.md).</span><span class="sxs-lookup"><span data-stu-id="25588-120">The display lists are created with [**glNewList**](glnewlist.md).</span></span> <span data-ttu-id="25588-121">Tutti i comandi successivi vengono inseriti nell'elenco di visualizzazione, nell'ordine emesso, fino a quando non viene chiamato **glEndList** .</span><span class="sxs-lookup"><span data-stu-id="25588-121">All subsequent commands are placed in the display list, in the order issued, until **glEndList** is called.</span></span>

<span data-ttu-id="25588-122">La funzione [**glNewList**](glnewlist.md) ha due parametri.</span><span class="sxs-lookup"><span data-stu-id="25588-122">The [**glNewList**](glnewlist.md) function has two parameters.</span></span> <span data-ttu-id="25588-123">Il primo parametro, *List*, è un numero intero positivo che diventa il nome univoco per l'elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="25588-123">The first parameter, *list*, is a positive integer that becomes the unique name for the display list.</span></span> <span data-ttu-id="25588-124">I nomi possono essere creati e riservati con [**glGenLists**](glgenlists.md) e sono stati testati per l'univocità con l'indisponibilità [**.**](glislist.md)</span><span class="sxs-lookup"><span data-stu-id="25588-124">Names can be created and reserved with [**glGenLists**](glgenlists.md) and tested for uniqueness with [**glIsList**](glislist.md).</span></span> <span data-ttu-id="25588-125">Il secondo parametro, *mode*, è una costante simbolica che può assumere uno dei due valori precedenti.</span><span class="sxs-lookup"><span data-stu-id="25588-125">The second parameter, *mode*, is a symbolic constant that can assume one of the two preceding values.</span></span>

<span data-ttu-id="25588-126">Alcuni comandi non vengono compilati nell'elenco di visualizzazione, ma vengono eseguiti immediatamente, indipendentemente dalla modalità elenco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="25588-126">Certain commands are not compiled into the display list, but are executed immediately, regardless of the display list mode.</span></span> <span data-ttu-id="25588-127">Questi comandi sono [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**Glis**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md)e tutte le routine [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) .</span><span class="sxs-lookup"><span data-stu-id="25588-127">These commands are [**glColorPointer**](glcolorpointer.md), [**glDeleteLists**](gldeletelists.md), [**glDisableClientState**](gldisableclientstate.md), [**glEdgeFlagPointer**](gledgeflagpointer.md), [**glEnableClientState**](glenableclientstate.md), [**glFeedbackBuffer**](glfeedbackbuffer.md), [**glFinish**](glfinish.md), [**glFlush**](glflush.md), [**glGenLists**](glgenlists.md), [**glIndexPointer**](glindexpointer.md), [**glInterleavedArrays**](glinterleavedarrays.md), [**glIsEnabled**](glisenabled.md), [**glIsList**](glislist.md), [**glNormalPointer**](glnormalpointer.md), [**glPopClientAttrib**](glpopclientattrib.md), [**glPixelStore**](glpixelstore-functions.md), [**glPushClientAttrib**](glpushclientattrib.md), [**glReadPixels**](glreadpixels.md), [**glRenderMode**](glrendermode.md), [**glSelectBuffer**](glselectbuffer.md), [**glTexCoordPointer**](gltexcoordpointer.md), [**glVertexPointer**](glvertexpointer.md), and all of the [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) routines.</span></span>

<span data-ttu-id="25588-128">Analogamente, [**glTexImage2D**](glteximage2d.md) e [**glTexImage1D**](glteximage1d.md) vengono eseguiti immediatamente e non vengono compilati nell'elenco di visualizzazione quando il primo argomento è la trama del proxy GL \_ \_ \_ 2D o GL proxy texture \_ \_ \_ 1D, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="25588-128">Similarly, [**glTexImage2D**](glteximage2d.md) and [**glTexImage1D**](glteximage1d.md) are executed immediately and not compiled into the display list when their first argument is GL\_PROXY\_TEXTURE\_2D or GL\_PROXY\_TEXTURE\_1D, respectively.</span></span>

<span data-ttu-id="25588-129">Quando viene rilevata la funzione **glEndList** , la definizione dell'elenco di visualizzazione viene completata associando l'elenco all' *elenco* dei nomi univoci (specificato nel comando [**glNewList**](glnewlist.md) ).</span><span class="sxs-lookup"><span data-stu-id="25588-129">When the **glEndList** function is encountered, the display list definition is completed by associating the list with the unique name *list* (specified in the [**glNewList**](glnewlist.md) command).</span></span> <span data-ttu-id="25588-130">Se un elenco di visualizzazione con l' *elenco dei* nomi esiste già, viene sostituito solo quando viene chiamato **glEndList** .</span><span class="sxs-lookup"><span data-stu-id="25588-130">If a display list with name *list* already exists, it is replaced only when **glEndList** is called.</span></span>

<span data-ttu-id="25588-131">Le funzioni [**glCallList**](glcalllist.md) e [**glCallLists**](glcalllists.md) possono essere immesse negli elenchi di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="25588-131">The [**glCallList**](glcalllist.md) and [**glCallLists**](glcalllists.md) functions can be entered into display lists.</span></span> <span data-ttu-id="25588-132">I comandi nell'elenco di visualizzazione o negli elenchi eseguiti da **glCallList** o **glCallLists** non sono inclusi nell'elenco di visualizzazione creato, anche se la modalità di creazione dell'elenco è la \_ compilazione e l'esecuzione di GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="25588-132">The commands in the display list or lists executed by **glCallList** or **glCallLists** are not included in the display list being created, even if the list creation mode is GL\_COMPILE\_AND\_EXECUTE.</span></span>

<span data-ttu-id="25588-133">La funzione seguente recupera le informazioni correlate a [**glNewList**](glnewlist.md):</span><span class="sxs-lookup"><span data-stu-id="25588-133">The following function retrieves information related to [**glNewList**](glnewlist.md):</span></span>

<span data-ttu-id="25588-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ modalità matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="25588-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="25588-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25588-135">Requirements</span></span>



| <span data-ttu-id="25588-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="25588-136">Requirement</span></span> | <span data-ttu-id="25588-137">Valore</span><span class="sxs-lookup"><span data-stu-id="25588-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25588-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25588-138">Minimum supported client</span></span><br/> | <span data-ttu-id="25588-139">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="25588-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="25588-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25588-140">Minimum supported server</span></span><br/> | <span data-ttu-id="25588-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="25588-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="25588-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25588-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="25588-143"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="25588-143"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="25588-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="25588-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="25588-145"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25588-145"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="25588-146">DLL</span><span class="sxs-lookup"><span data-stu-id="25588-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25588-147"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25588-147"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25588-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25588-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25588-149">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="25588-149">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="25588-150">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="25588-150">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="25588-151">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="25588-151">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="25588-152">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="25588-152">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="25588-153">**Remo**</span><span class="sxs-lookup"><span data-stu-id="25588-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="25588-154">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="25588-154">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="25588-155">**Pagina di**</span><span class="sxs-lookup"><span data-stu-id="25588-155">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="25588-156">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="25588-156">**glNewList**</span></span>](glnewlist.md)
</dt> </dl>

 

 





