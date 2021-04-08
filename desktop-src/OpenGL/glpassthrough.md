---
title: funzione glPassThrough (GL. h)
description: La funzione glPassThrough inserisce un marcatore nel buffer di feedback.
ms.assetid: 14664ac6-eb25-46ae-86d8-7ece31df103f
keywords:
- funzione glPassThrough OpenGL
topic_type:
- apiref
api_name:
- glPassThrough
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd1174dd933d46813a89c35b781d0408c3ac5476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741135"
---
# <a name="glpassthrough-function"></a><span data-ttu-id="3c7f2-104">glPassThrough (funzione)</span><span class="sxs-lookup"><span data-stu-id="3c7f2-104">glPassThrough function</span></span>

<span data-ttu-id="3c7f2-105">La funzione **glPassThrough** inserisce un marcatore nel buffer di feedback.</span><span class="sxs-lookup"><span data-stu-id="3c7f2-105">The **glPassThrough** function places a marker in the feedback buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c7f2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c7f2-106">Syntax</span></span>


```C++
void WINAPI glPassThrough(
   GLfloat token
);
```



## <a name="parameters"></a><span data-ttu-id="3c7f2-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c7f2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c7f2-108">*token*</span><span class="sxs-lookup"><span data-stu-id="3c7f2-108">*token*</span></span> 
</dt> <dd>

<span data-ttu-id="3c7f2-109">Valore del marcatore da inserire nel buffer di feedback.</span><span class="sxs-lookup"><span data-stu-id="3c7f2-109">A marker value to be placed in the feedback buffer.</span></span> <span data-ttu-id="3c7f2-110">Viene indicato con il seguente valore di identificazione univoco.</span><span class="sxs-lookup"><span data-stu-id="3c7f2-110">It is indicated with the following unique identifying value.</span></span>



| <span data-ttu-id="3c7f2-111">Valore</span><span class="sxs-lookup"><span data-stu-id="3c7f2-111">Value</span></span>                                                                                                                                                                                   | <span data-ttu-id="3c7f2-112">Significato</span><span class="sxs-lookup"><span data-stu-id="3c7f2-112">Meaning</span></span>                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_PASS_THROUGH_TOKEN"></span><span id="gl_pass_through_token"></span><dl> <span data-ttu-id="3c7f2-113"><dt>**\_token pass- \_ through per GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3c7f2-113"><dt>**GL\_PASS\_THROUGH\_TOKEN**</dt></span></span> </dl> | <span data-ttu-id="3c7f2-114">Viene mantenuto l'ordine dei comandi **glPassThrough** rispetto alla specifica delle primitive grafiche.</span><span class="sxs-lookup"><span data-stu-id="3c7f2-114">The order of **glPassThrough** commands with respect to the specification of graphics primitives is maintained.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c7f2-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c7f2-115">Return value</span></span>

<span data-ttu-id="3c7f2-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="3c7f2-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3c7f2-117">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="3c7f2-117">Error codes</span></span>

<span data-ttu-id="3c7f2-118">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="3c7f2-118">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3c7f2-119">Nome</span><span class="sxs-lookup"><span data-stu-id="3c7f2-119">Name</span></span>                                                                                                  | <span data-ttu-id="3c7f2-120">Significato</span><span class="sxs-lookup"><span data-stu-id="3c7f2-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3c7f2-121"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3c7f2-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3c7f2-122">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="3c7f2-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3c7f2-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c7f2-123">Remarks</span></span>

<span data-ttu-id="3c7f2-124">Il feedback è una modalità di rendering OpenGL selezionata chiamando [**glRenderMode**](glrendermode.md) con \_ feedback GL.</span><span class="sxs-lookup"><span data-stu-id="3c7f2-124">Feedback is an OpenGL render mode selected by calling [**glRenderMode**](glrendermode.md) with GL\_FEEDBACK.</span></span> <span data-ttu-id="3c7f2-125">Quando OpenGL è in modalità di feedback, nessun pixel viene prodotto dalla rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="3c7f2-125">When OpenGL is in feedback mode, no pixels are produced by rasterization.</span></span> <span data-ttu-id="3c7f2-126">Al contrario, le informazioni sulle primitive che sarebbero state rasterizzate vengono riportate all'applicazione da OpenGL.</span><span class="sxs-lookup"><span data-stu-id="3c7f2-126">Instead, information about primitives that would have been rasterized is fed back to the application by OpenGL.</span></span> <span data-ttu-id="3c7f2-127">Per una descrizione del buffer di feedback e dei relativi valori, vedere [**glFeedbackBuffer**](glfeedbackbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="3c7f2-127">See [**glFeedbackBuffer**](glfeedbackbuffer.md) for a description of the feedback buffer and the values in it.</span></span>

<span data-ttu-id="3c7f2-128">La funzione **glPassThrough** inserisce un marcatore definito dall'utente nel buffer di feedback quando viene eseguito in modalità di feedback.</span><span class="sxs-lookup"><span data-stu-id="3c7f2-128">The **glPassThrough** function inserts a user-defined marker in the feedback buffer when it is executed in feedback mode.</span></span> <span data-ttu-id="3c7f2-129">Il parametro *token* viene restituito come se fosse una primitiva.</span><span class="sxs-lookup"><span data-stu-id="3c7f2-129">The *token* parameter is returned as if it were a primitive.</span></span>

<span data-ttu-id="3c7f2-130">La funzione **glPassThrough** viene ignorata se OpenGL non è in modalità di feedback.</span><span class="sxs-lookup"><span data-stu-id="3c7f2-130">The **glPassThrough** function is ignored if OpenGL is not in feedback mode.</span></span>

<span data-ttu-id="3c7f2-131">La funzione seguente recupera le informazioni correlate a **glPassThrough**:</span><span class="sxs-lookup"><span data-stu-id="3c7f2-131">The following function retrieves information related to **glPassThrough**:</span></span>

<span data-ttu-id="3c7f2-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con modalità di \_ rendering GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="3c7f2-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="3c7f2-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c7f2-133">Requirements</span></span>



| <span data-ttu-id="3c7f2-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c7f2-134">Requirement</span></span> | <span data-ttu-id="3c7f2-135">Valore</span><span class="sxs-lookup"><span data-stu-id="3c7f2-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c7f2-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c7f2-136">Minimum supported client</span></span><br/> | <span data-ttu-id="3c7f2-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3c7f2-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3c7f2-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c7f2-138">Minimum supported server</span></span><br/> | <span data-ttu-id="3c7f2-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3c7f2-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3c7f2-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c7f2-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c7f2-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c7f2-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3c7f2-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="3c7f2-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c7f2-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c7f2-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3c7f2-144">DLL</span><span class="sxs-lookup"><span data-stu-id="3c7f2-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c7f2-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c7f2-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c7f2-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c7f2-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c7f2-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3c7f2-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3c7f2-148">**Remo**</span><span class="sxs-lookup"><span data-stu-id="3c7f2-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3c7f2-149">**glFeedbackBuffer**</span><span class="sxs-lookup"><span data-stu-id="3c7f2-149">**glFeedbackBuffer**</span></span>](glfeedbackbuffer.md)
</dt> <dt>

[<span data-ttu-id="3c7f2-150">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="3c7f2-150">**glRenderMode**</span></span>](glrendermode.md)
</dt> </dl>

 

 





