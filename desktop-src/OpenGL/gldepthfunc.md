---
title: funzione glDepthFunc (GL. h)
description: La funzione glDepthFunc specifica il valore usato per i confronti del buffer di profondità.
ms.assetid: 6ab8774a-8887-4c1e-b567-4492c0a60cf2
keywords:
- funzione glDepthFunc OpenGL
topic_type:
- apiref
api_name:
- glDepthFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dec5130edb0b8ef30af1397be501fa9cd5d5744
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475844"
---
# <a name="gldepthfunc-function"></a><span data-ttu-id="a3887-104">glDepthFunc (funzione)</span><span class="sxs-lookup"><span data-stu-id="a3887-104">glDepthFunc function</span></span>

<span data-ttu-id="a3887-105">La funzione **glDepthFunc** specifica il valore usato per i confronti del buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="a3887-105">The **glDepthFunc** function specifies the value used for depth-buffer comparisons.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3887-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a3887-106">Syntax</span></span>


```C++
void WINAPI glDepthFunc(
   GLenum func
);
```



## <a name="parameters"></a><span data-ttu-id="a3887-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a3887-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3887-108">*func*</span><span class="sxs-lookup"><span data-stu-id="a3887-108">*func*</span></span> 
</dt> <dd>

<span data-ttu-id="a3887-109">Specifica la funzione di confronto di profondità.</span><span class="sxs-lookup"><span data-stu-id="a3887-109">Specifies the depth-comparison function.</span></span> <span data-ttu-id="a3887-110">Vengono accettate le seguenti costanti simboliche.</span><span class="sxs-lookup"><span data-stu-id="a3887-110">The following symbolic constants are accepted.</span></span>



| <span data-ttu-id="a3887-111">Valore</span><span class="sxs-lookup"><span data-stu-id="a3887-111">Value</span></span>                                                                                                                                                   | <span data-ttu-id="a3887-112">Significato</span><span class="sxs-lookup"><span data-stu-id="a3887-112">Meaning</span></span>                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <span data-ttu-id="a3887-113"><dt>**GL \_ mai**</dt></span><span class="sxs-lookup"><span data-stu-id="a3887-113"><dt>**GL\_NEVER**</dt></span></span> </dl>          | <span data-ttu-id="a3887-114">Non viene mai passato.</span><span class="sxs-lookup"><span data-stu-id="a3887-114">Never passes.</span></span><br/>                                                                                  |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <span data-ttu-id="a3887-115"><dt>**\_meno GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a3887-115"><dt>**GL\_LESS**</dt></span></span> </dl>             | <span data-ttu-id="a3887-116">Passa se il valore *z* in ingresso è minore del valore *z* archiviato.</span><span class="sxs-lookup"><span data-stu-id="a3887-116">Passes if the incoming *z* value is less than the stored *z* value.</span></span> <span data-ttu-id="a3887-117">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="a3887-117">This is the default value.</span></span><br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <span data-ttu-id="a3887-118"><dt>**\_LEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a3887-118"><dt>**GL\_LEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="a3887-119">Passa se il valore z in ingresso è minore o uguale al valore z archiviato.</span><span class="sxs-lookup"><span data-stu-id="a3887-119">Passes if the incoming z value is less than or equal to the stored z value.</span></span><br/>                    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <span data-ttu-id="a3887-120"><dt>**GL \_ uguale**</dt></span><span class="sxs-lookup"><span data-stu-id="a3887-120"><dt>**GL\_EQUAL**</dt></span></span> </dl>          | <span data-ttu-id="a3887-121">Passa se il valore z in ingresso è uguale al valore z archiviato.</span><span class="sxs-lookup"><span data-stu-id="a3887-121">Passes if the incoming z value is equal to the stored z value.</span></span><br/>                                 |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <span data-ttu-id="a3887-122"><dt>**maggiore di GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a3887-122"><dt>**GL\_GREATER**</dt></span></span> </dl>    | <span data-ttu-id="a3887-123">Passa se il valore z in ingresso è maggiore del valore z archiviato.</span><span class="sxs-lookup"><span data-stu-id="a3887-123">Passes if the incoming z value is greater than the stored z value.</span></span><br/>                             |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <span data-ttu-id="a3887-124"><dt>**\_NOTEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a3887-124"><dt>**GL\_NOTEQUAL**</dt></span></span> </dl> | <span data-ttu-id="a3887-125">Passa se il valore z in entrata non è uguale al valore z archiviato.</span><span class="sxs-lookup"><span data-stu-id="a3887-125">Passes if the incoming z value is not equal to the stored z value.</span></span><br/>                             |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <span data-ttu-id="a3887-126"><dt>**\_GEQUAL GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a3887-126"><dt>**GL\_GEQUAL**</dt></span></span> </dl>       | <span data-ttu-id="a3887-127">Passa se il valore z in ingresso è maggiore o uguale al valore z archiviato.</span><span class="sxs-lookup"><span data-stu-id="a3887-127">Passes if the incoming z value is greater than or equal to the stored z value.</span></span><br/>                 |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <span data-ttu-id="a3887-128"><dt>**GL \_ Always**</dt></span><span class="sxs-lookup"><span data-stu-id="a3887-128"><dt>**GL\_ALWAYS**</dt></span></span> </dl>       | <span data-ttu-id="a3887-129">Passa sempre.</span><span class="sxs-lookup"><span data-stu-id="a3887-129">Always passes.</span></span><br/>                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3887-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a3887-130">Return value</span></span>

<span data-ttu-id="a3887-131">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="a3887-131">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a3887-132">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a3887-132">Error codes</span></span>

<span data-ttu-id="a3887-133">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="a3887-133">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a3887-134">Nome</span><span class="sxs-lookup"><span data-stu-id="a3887-134">Name</span></span>                                                                                                  | <span data-ttu-id="a3887-135">Significato</span><span class="sxs-lookup"><span data-stu-id="a3887-135">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a3887-136"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a3887-136"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a3887-137">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a3887-137">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a3887-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="a3887-138">Remarks</span></span>

<span data-ttu-id="a3887-139">La funzione **glDepthFunc** specifica la funzione utilizzata per confrontare ogni valore di pixel *z* in ingresso con il valore *z* presente nel buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="a3887-139">The **glDepthFunc** function specifies the function used to compare each incoming pixel *z* value with the *z* value present in the depth buffer.</span></span> <span data-ttu-id="a3887-140">Il confronto viene eseguito solo se è abilitato il test di profondità.</span><span class="sxs-lookup"><span data-stu-id="a3887-140">The comparison is performed only if depth testing is enabled.</span></span> <span data-ttu-id="a3887-141">(Vedere [**glEnable**](glenable.md) con l'argomento GL \_ TEST di profondità \_ .</span><span class="sxs-lookup"><span data-stu-id="a3887-141">(See [**glEnable**](glenable.md) with the argument GL\_DEPTH\_TEST.)</span></span>

<span data-ttu-id="a3887-142">Inizialmente, il test di profondità è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="a3887-142">Initially, depth testing is disabled.</span></span>

<span data-ttu-id="a3887-143">Le funzioni seguenti consentono di recuperare informazioni correlate a **glDepthFunc**:</span><span class="sxs-lookup"><span data-stu-id="a3887-143">The following functions retrieve information related to **glDepthFunc**:</span></span>

<span data-ttu-id="a3887-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Depth \_ Func</span><span class="sxs-lookup"><span data-stu-id="a3887-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DEPTH\_FUNC</span></span>

<span data-ttu-id="a3887-145">[**glIsEnabled**](glisenabled.md) con il \_ test di profondità di argomento GL \_</span><span class="sxs-lookup"><span data-stu-id="a3887-145">[**glIsEnabled**](glisenabled.md) with argument GL\_DEPTH\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="a3887-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a3887-146">Requirements</span></span>



| <span data-ttu-id="a3887-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3887-147">Requirement</span></span> | <span data-ttu-id="a3887-148">Valore</span><span class="sxs-lookup"><span data-stu-id="a3887-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3887-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3887-149">Minimum supported client</span></span><br/> | <span data-ttu-id="a3887-150">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a3887-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a3887-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a3887-151">Minimum supported server</span></span><br/> | <span data-ttu-id="a3887-152">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a3887-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a3887-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a3887-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3887-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3887-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a3887-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="a3887-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="a3887-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a3887-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a3887-157">DLL</span><span class="sxs-lookup"><span data-stu-id="a3887-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3887-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3887-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3887-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a3887-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3887-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a3887-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a3887-161">**glDepthRange**</span><span class="sxs-lookup"><span data-stu-id="a3887-161">**glDepthRange**</span></span>](gldepthrange.md)
</dt> <dt>

[<span data-ttu-id="a3887-162">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="a3887-162">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="a3887-163">**Remo**</span><span class="sxs-lookup"><span data-stu-id="a3887-163">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a3887-164">**glGet**</span><span class="sxs-lookup"><span data-stu-id="a3887-164">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="a3887-165">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="a3887-165">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





