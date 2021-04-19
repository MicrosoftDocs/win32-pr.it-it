---
title: funzione glGetTexParameterfv (GL. h)
description: Le funzioni glGetTexParameterfv e glGetTexParameteriv restituiscono i valori dei parametri della trama. | funzione glGetTexParameterfv (GL. h)
ms.assetid: 616292ea-222c-4efe-bb69-3058d9c99910
keywords:
- funzione glGetTexParameterfv OpenGL
topic_type:
- apiref
api_name:
- glGetTexParameterfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b0af6e5fd91d38240dd3463b9440333b5da431d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321814"
---
# <a name="glgettexparameterfv-function"></a><span data-ttu-id="2f29f-105">glGetTexParameterfv (funzione)</span><span class="sxs-lookup"><span data-stu-id="2f29f-105">glGetTexParameterfv function</span></span>

<span data-ttu-id="2f29f-106">Le funzioni **glGetTexParameterfv** e [**glGetTexParameteriv**](glgettexparameteriv.md) restituiscono i valori dei parametri della trama.</span><span class="sxs-lookup"><span data-stu-id="2f29f-106">The **glGetTexParameterfv** and [**glGetTexParameteriv**](glgettexparameteriv.md) functions return texture parameter values.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f29f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f29f-107">Syntax</span></span>


```C++
void WINAPI glGetTexParameterfv(
   GLenum  target,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="2f29f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f29f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f29f-109">*target*</span><span class="sxs-lookup"><span data-stu-id="2f29f-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="2f29f-110">Nome simbolico della trama di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2f29f-110">The symbolic name of the target texture.</span></span> <span data-ttu-id="2f29f-111">\_ \_ Viene accettata la trama GL 1D e GL \_ texture \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="2f29f-111">GL\_TEXTURE\_1D and GL\_TEXTURE\_2D are accepted.</span></span>

</dd> <dt>

<span data-ttu-id="2f29f-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="2f29f-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="2f29f-113">Nome simbolico di un parametro di trama.</span><span class="sxs-lookup"><span data-stu-id="2f29f-113">The symbolic name of a texture parameter.</span></span> <span data-ttu-id="2f29f-114">Vengono accettati i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="2f29f-114">The following values are accepted.</span></span>



| <span data-ttu-id="2f29f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="2f29f-115">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="2f29f-116">Significato</span><span class="sxs-lookup"><span data-stu-id="2f29f-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <span data-ttu-id="2f29f-117"><dt>**\_ \_ filtro mag trama di contabilità \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2f29f-117"><dt>**GL\_TEXTURE\_MAG\_FILTER**</dt></span></span> </dl>       | <span data-ttu-id="2f29f-118">Restituisce il filtro di ingrandimento della trama a valore singolo, una costante simbolica.</span><span class="sxs-lookup"><span data-stu-id="2f29f-118">Returns the single-valued texture magnification filter, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <span data-ttu-id="2f29f-119"><dt>**\_ \_ Filtro minimo trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2f29f-119"><dt>**GL\_TEXTURE\_MIN\_FILTER**</dt></span></span> </dl>       | <span data-ttu-id="2f29f-120">Restituisce il filtro minification di trama a valore singolo, una costante simbolica.</span><span class="sxs-lookup"><span data-stu-id="2f29f-120">Returns the single-valued texture minification filter, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                                       |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <span data-ttu-id="2f29f-121"><dt>**\_wrapping di trama GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2f29f-121"><dt>**GL\_TEXTURE\_WRAP\_S**</dt></span></span> </dl>                   | <span data-ttu-id="2f29f-122">Restituisce la funzione di wrapping a valore singolo per le coordinate di trama *s*, una costante simbolica.</span><span class="sxs-lookup"><span data-stu-id="2f29f-122">Returns the single-valued wrapping function for texture coordinate *s*, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <span data-ttu-id="2f29f-123"><dt>**\_wrapping trama \_ GL \_ T**</dt></span><span class="sxs-lookup"><span data-stu-id="2f29f-123"><dt>**GL\_TEXTURE\_WRAP\_T**</dt></span></span> </dl>                   | <span data-ttu-id="2f29f-124">Restituisce la funzione di wrapping a valore singolo per la coordinata di trama *t*, una costante simbolica.</span><span class="sxs-lookup"><span data-stu-id="2f29f-124">Returns the single-valued wrapping function for texture coordinate *t*, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <span data-ttu-id="2f29f-125"><dt>**\_ \_ colore bordo trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2f29f-125"><dt>**GL\_TEXTURE\_BORDER\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="2f29f-126">Restituisce quattro numeri interi o a virgola mobile che comprendono il colore RGBA del bordo della trama.</span><span class="sxs-lookup"><span data-stu-id="2f29f-126">Returns four integer or floating-point numbers that comprise the RGBA color of the texture border.</span></span> <span data-ttu-id="2f29f-127">I valori a virgola mobile vengono restituiti nell'intervallo compreso tra \[ 0 e 1 \] .</span><span class="sxs-lookup"><span data-stu-id="2f29f-127">Floating-point values are returned in the range \[0,1\].</span></span> <span data-ttu-id="2f29f-128">I valori integer vengono restituiti come mapping lineare della rappresentazione a virgola mobile interna, in modo che 1,0 sia mappato al valore integer rappresentabile più positivo e-1,0 sia mappato al valore integer rappresentabile più negativo.</span><span class="sxs-lookup"><span data-stu-id="2f29f-128">Integer values are returned as a linear mapping of the internal floating-point representation such that 1.0 maps to the most positive representable integer and -1.0 maps to the most negative representable integer.</span></span><br/> |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <span data-ttu-id="2f29f-129"><dt>**\_priorità trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2f29f-129"><dt>**GL\_TEXTURE\_PRIORITY**</dt></span></span> </dl>              | <span data-ttu-id="2f29f-130">Restituisce la priorità di residenza della trama di destinazione (o della trama denominata associata).</span><span class="sxs-lookup"><span data-stu-id="2f29f-130">Returns the residence priority of the target texture (or the named texture bound to it).</span></span> <span data-ttu-id="2f29f-131">Il valore iniziale è 1.</span><span class="sxs-lookup"><span data-stu-id="2f29f-131">The initial value is 1.</span></span> <span data-ttu-id="2f29f-132">Vedere [**glPrioritizeTextures**](glprioritizetextures.md).</span><span class="sxs-lookup"><span data-stu-id="2f29f-132">See [**glPrioritizeTextures**](glprioritizetextures.md).</span></span><br/>                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_RESIDENT"></span><span id="gl_texture_resident"></span><dl> <span data-ttu-id="2f29f-133"><dt>**\_residente trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="2f29f-133"><dt>**GL\_TEXTURE\_RESIDENT**</dt></span></span> </dl>              | <span data-ttu-id="2f29f-134">Restituisce lo stato di residenza della trama di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2f29f-134">Returns the residence status of the target texture.</span></span> <span data-ttu-id="2f29f-135">Se il valore restituito in params è GL \_ true, la trama è residente nella memoria della trama.</span><span class="sxs-lookup"><span data-stu-id="2f29f-135">If the value returned in params is GL\_TRUE, the texture is resident in texture memory.</span></span> <span data-ttu-id="2f29f-136">Vedere [**glAreTexturesResident**](glaretexturesresident.md).</span><span class="sxs-lookup"><span data-stu-id="2f29f-136">See [**glAreTexturesResident**](glaretexturesresident.md).</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="2f29f-137">*params*</span><span class="sxs-lookup"><span data-stu-id="2f29f-137">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="2f29f-138">Restituisce i parametri della trama.</span><span class="sxs-lookup"><span data-stu-id="2f29f-138">Returns the texture parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f29f-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f29f-139">Return value</span></span>

<span data-ttu-id="2f29f-140">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="2f29f-140">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2f29f-141">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="2f29f-141">Error codes</span></span>

<span data-ttu-id="2f29f-142">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="2f29f-142">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="2f29f-143">Nome</span><span class="sxs-lookup"><span data-stu-id="2f29f-143">Name</span></span>                                                                                                  | <span data-ttu-id="2f29f-144">Significato</span><span class="sxs-lookup"><span data-stu-id="2f29f-144">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2f29f-145"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2f29f-145"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="2f29f-146">la *destinazione* o il *nome* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="2f29f-146">*target* or *name* was not an accepted value.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="2f29f-147"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2f29f-147"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="2f29f-148">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="2f29f-148">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2f29f-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f29f-149">Remarks</span></span>

<span data-ttu-id="2f29f-150">La funzione **glGetTexParameter** restituisce in *params* il valore o i valori del parametro texture specificato come *pname*.</span><span class="sxs-lookup"><span data-stu-id="2f29f-150">The **glGetTexParameter** function returns in *params* the value or values of the texture parameter specified as *pname*.</span></span> <span data-ttu-id="2f29f-151">Il parametro *target* definisce la trama di destinazione, ovvero GL \_ texture \_ 1D o GL \_ trama \_ 2D, per specificare una texturatura bidimensionale o bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="2f29f-151">The *target* parameter defines the target texture, either GL\_TEXTURE\_1D or GL\_TEXTURE\_2D, to specify one-dimensional or two-dimensional texturing.</span></span> <span data-ttu-id="2f29f-152">Il parametro *pname* accetta gli stessi simboli di [**glTexParameter**](gltexparameter-functions.md), con le stesse interpretazioni.</span><span class="sxs-lookup"><span data-stu-id="2f29f-152">The *pname* parameter accepts the same symbols as [**glTexParameter**](gltexparameter-functions.md), with the same interpretations.</span></span>

<span data-ttu-id="2f29f-153">Se viene generato un errore, non viene apportata alcuna modifica al contenuto di *params*.</span><span class="sxs-lookup"><span data-stu-id="2f29f-153">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f29f-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f29f-154">Requirements</span></span>



| <span data-ttu-id="2f29f-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f29f-155">Requirement</span></span> | <span data-ttu-id="2f29f-156">Valore</span><span class="sxs-lookup"><span data-stu-id="2f29f-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f29f-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f29f-157">Minimum supported client</span></span><br/> | <span data-ttu-id="2f29f-158">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2f29f-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2f29f-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f29f-159">Minimum supported server</span></span><br/> | <span data-ttu-id="2f29f-160">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2f29f-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2f29f-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2f29f-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f29f-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f29f-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2f29f-163">Libreria</span><span class="sxs-lookup"><span data-stu-id="2f29f-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="2f29f-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f29f-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2f29f-165">DLL</span><span class="sxs-lookup"><span data-stu-id="2f29f-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f29f-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f29f-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f29f-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f29f-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f29f-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="2f29f-168">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="2f29f-169">**Remo**</span><span class="sxs-lookup"><span data-stu-id="2f29f-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="2f29f-170">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="2f29f-170">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





