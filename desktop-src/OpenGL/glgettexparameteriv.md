---
title: funzione glGetTexParameteriv (GL. h)
description: Le funzioni glGetTexParameterfv e glGetTexParameteriv restituiscono i valori dei parametri della trama. | funzione glGetTexParameteriv (GL. h)
ms.assetid: b89d10f1-5e30-4d25-8953-fbd59781fdac
keywords:
- funzione glGetTexParameteriv OpenGL
topic_type:
- apiref
api_name:
- glGetTexParameteriv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ca78983594487fd22917c15a5b211c529b6b14d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321813"
---
# <a name="glgettexparameteriv-function"></a><span data-ttu-id="434fc-105">glGetTexParameteriv (funzione)</span><span class="sxs-lookup"><span data-stu-id="434fc-105">glGetTexParameteriv function</span></span>

<span data-ttu-id="434fc-106">Le funzioni [**glGetTexParameterfv**](glgettexparameterfv.md) e **glGetTexParameteriv** restituiscono i valori dei parametri della trama.</span><span class="sxs-lookup"><span data-stu-id="434fc-106">The [**glGetTexParameterfv**](glgettexparameterfv.md) and **glGetTexParameteriv** functions return texture parameter values.</span></span>

## <a name="syntax"></a><span data-ttu-id="434fc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="434fc-107">Syntax</span></span>


```C++
void WINAPI glGetTexParameteriv(
   GLenum target,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="434fc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="434fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="434fc-109">*target*</span><span class="sxs-lookup"><span data-stu-id="434fc-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="434fc-110">Nome simbolico della trama di destinazione.</span><span class="sxs-lookup"><span data-stu-id="434fc-110">The symbolic name of the target texture.</span></span> <span data-ttu-id="434fc-111">\_ \_ Viene accettata la trama GL 1D e GL \_ texture \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="434fc-111">GL\_TEXTURE\_1D and GL\_TEXTURE\_2D are accepted.</span></span>

</dd> <dt>

<span data-ttu-id="434fc-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="434fc-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="434fc-113">Nome simbolico di un parametro di trama.</span><span class="sxs-lookup"><span data-stu-id="434fc-113">The symbolic name of a texture parameter.</span></span> <span data-ttu-id="434fc-114">Vengono accettati i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="434fc-114">The following values are accepted.</span></span>



| <span data-ttu-id="434fc-115">Valore</span><span class="sxs-lookup"><span data-stu-id="434fc-115">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="434fc-116">Significato</span><span class="sxs-lookup"><span data-stu-id="434fc-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span><dl> <span data-ttu-id="434fc-117"><dt>**\_ \_ filtro mag trama di contabilità \_**</dt></span><span class="sxs-lookup"><span data-stu-id="434fc-117"><dt>**GL\_TEXTURE\_MAG\_FILTER**</dt></span></span> </dl>       | <span data-ttu-id="434fc-118">Restituisce il filtro di ingrandimento della trama a valore singolo, una costante simbolica.</span><span class="sxs-lookup"><span data-stu-id="434fc-118">Returns the single-valued texture magnification filter, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span><dl> <span data-ttu-id="434fc-119"><dt>**\_ \_ Filtro minimo trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="434fc-119"><dt>**GL\_TEXTURE\_MIN\_FILTER**</dt></span></span> </dl>       | <span data-ttu-id="434fc-120">Restituisce il filtro minification di trama a valore singolo, una costante simbolica.</span><span class="sxs-lookup"><span data-stu-id="434fc-120">Returns the single-valued texture minification filter, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                                       |
| <span id="GL_TEXTURE_WRAP_S"></span><span id="gl_texture_wrap_s"></span><dl> <span data-ttu-id="434fc-121"><dt>**\_wrapping di trama GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="434fc-121"><dt>**GL\_TEXTURE\_WRAP\_S**</dt></span></span> </dl>                   | <span data-ttu-id="434fc-122">Restituisce la funzione di wrapping a valore singolo per le coordinate di trama *s*, una costante simbolica.</span><span class="sxs-lookup"><span data-stu-id="434fc-122">Returns the single-valued wrapping function for texture coordinate *s*, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_WRAP_T"></span><span id="gl_texture_wrap_t"></span><dl> <span data-ttu-id="434fc-123"><dt>**\_wrapping trama \_ GL \_ T**</dt></span><span class="sxs-lookup"><span data-stu-id="434fc-123"><dt>**GL\_TEXTURE\_WRAP\_T**</dt></span></span> </dl>                   | <span data-ttu-id="434fc-124">Restituisce la funzione di wrapping a valore singolo per la coordinata di trama *t*, una costante simbolica.</span><span class="sxs-lookup"><span data-stu-id="434fc-124">Returns the single-valued wrapping function for texture coordinate *t*, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| <span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span><dl> <span data-ttu-id="434fc-125"><dt>**\_ \_ colore bordo trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="434fc-125"><dt>**GL\_TEXTURE\_BORDER\_COLOR**</dt></span></span> </dl> | <span data-ttu-id="434fc-126">Restituisce quattro numeri interi o a virgola mobile che comprendono il colore RGBA del bordo della trama.</span><span class="sxs-lookup"><span data-stu-id="434fc-126">Returns four integer or floating-point numbers that comprise the RGBA color of the texture border.</span></span> <span data-ttu-id="434fc-127">I valori a virgola mobile vengono restituiti nell'intervallo compreso tra \[ 0 e 1 \] .</span><span class="sxs-lookup"><span data-stu-id="434fc-127">Floating-point values are returned in the range \[0,1\].</span></span> <span data-ttu-id="434fc-128">I valori integer vengono restituiti come mapping lineare della rappresentazione a virgola mobile interna, in modo che 1,0 sia mappato al valore integer rappresentabile più positivo e-1,0 sia mappato al valore integer rappresentabile più negativo.</span><span class="sxs-lookup"><span data-stu-id="434fc-128">Integer values are returned as a linear mapping of the internal floating-point representation such that 1.0 maps to the most positive representable integer and -1.0 maps to the most negative representable integer.</span></span><br/> |
| <span id="GL_TEXTURE_PRIORITY"></span><span id="gl_texture_priority"></span><dl> <span data-ttu-id="434fc-129"><dt>**\_priorità trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="434fc-129"><dt>**GL\_TEXTURE\_PRIORITY**</dt></span></span> </dl>              | <span data-ttu-id="434fc-130">Restituisce la priorità di residenza della trama di destinazione (o della trama denominata associata).</span><span class="sxs-lookup"><span data-stu-id="434fc-130">Returns the residence priority of the target texture (or the named texture bound to it).</span></span> <span data-ttu-id="434fc-131">Il valore iniziale è 1.</span><span class="sxs-lookup"><span data-stu-id="434fc-131">The initial value is 1.</span></span> <span data-ttu-id="434fc-132">Vedere [**glPrioritizeTextures**](glprioritizetextures.md).</span><span class="sxs-lookup"><span data-stu-id="434fc-132">See [**glPrioritizeTextures**](glprioritizetextures.md).</span></span><br/>                                                                                                                                                                                                        |
| <span id="GL_TEXTURE_RESIDENT"></span><span id="gl_texture_resident"></span><dl> <span data-ttu-id="434fc-133"><dt>**\_residente trama \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="434fc-133"><dt>**GL\_TEXTURE\_RESIDENT**</dt></span></span> </dl>              | <span data-ttu-id="434fc-134">Restituisce lo stato di residenza della trama di destinazione.</span><span class="sxs-lookup"><span data-stu-id="434fc-134">Returns the residence status of the target texture.</span></span> <span data-ttu-id="434fc-135">Se il valore restituito in params è GL \_ true, la trama è residente nella memoria della trama.</span><span class="sxs-lookup"><span data-stu-id="434fc-135">If the value returned in params is GL\_TRUE, the texture is resident in texture memory.</span></span> <span data-ttu-id="434fc-136">Vedere [**glAreTexturesResident**](glaretexturesresident.md).</span><span class="sxs-lookup"><span data-stu-id="434fc-136">See [**glAreTexturesResident**](glaretexturesresident.md).</span></span><br/>                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="434fc-137">*params*</span><span class="sxs-lookup"><span data-stu-id="434fc-137">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="434fc-138">Restituisce i parametri della trama.</span><span class="sxs-lookup"><span data-stu-id="434fc-138">Returns the texture parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="434fc-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="434fc-139">Return value</span></span>

<span data-ttu-id="434fc-140">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="434fc-140">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="434fc-141">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="434fc-141">Error codes</span></span>

<span data-ttu-id="434fc-142">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="434fc-142">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="434fc-143">Nome</span><span class="sxs-lookup"><span data-stu-id="434fc-143">Name</span></span>                                                                                                  | <span data-ttu-id="434fc-144">Significato</span><span class="sxs-lookup"><span data-stu-id="434fc-144">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="434fc-145"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="434fc-145"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="434fc-146">la *destinazione* o il *nome* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="434fc-146">*target* or *name* was not an accepted value.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="434fc-147"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="434fc-147"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="434fc-148">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="434fc-148">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="434fc-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="434fc-149">Remarks</span></span>

<span data-ttu-id="434fc-150">La funzione **glGetTexParameter** restituisce in *params* il valore o i valori del parametro texture specificato come *pname*.</span><span class="sxs-lookup"><span data-stu-id="434fc-150">The **glGetTexParameter** function returns in *params* the value or values of the texture parameter specified as *pname*.</span></span> <span data-ttu-id="434fc-151">Il parametro *target* definisce la trama di destinazione, ovvero GL \_ texture \_ 1D o GL \_ trama \_ 2D, per specificare una texturatura bidimensionale o bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="434fc-151">The *target* parameter defines the target texture, either GL\_TEXTURE\_1D or GL\_TEXTURE\_2D, to specify one-dimensional or two-dimensional texturing.</span></span> <span data-ttu-id="434fc-152">Il parametro *pname* accetta gli stessi simboli di [**glTexParameter**](gltexparameter-functions.md), con le stesse interpretazioni.</span><span class="sxs-lookup"><span data-stu-id="434fc-152">The *pname* parameter accepts the same symbols as [**glTexParameter**](gltexparameter-functions.md), with the same interpretations.</span></span>

<span data-ttu-id="434fc-153">Se viene generato un errore, non viene apportata alcuna modifica al contenuto di *params*.</span><span class="sxs-lookup"><span data-stu-id="434fc-153">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="434fc-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="434fc-154">Requirements</span></span>



| <span data-ttu-id="434fc-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="434fc-155">Requirement</span></span> | <span data-ttu-id="434fc-156">Valore</span><span class="sxs-lookup"><span data-stu-id="434fc-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="434fc-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="434fc-157">Minimum supported client</span></span><br/> | <span data-ttu-id="434fc-158">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="434fc-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="434fc-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="434fc-159">Minimum supported server</span></span><br/> | <span data-ttu-id="434fc-160">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="434fc-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="434fc-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="434fc-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="434fc-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="434fc-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="434fc-163">Libreria</span><span class="sxs-lookup"><span data-stu-id="434fc-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="434fc-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="434fc-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="434fc-165">DLL</span><span class="sxs-lookup"><span data-stu-id="434fc-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="434fc-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="434fc-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="434fc-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="434fc-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="434fc-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="434fc-168">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="434fc-169">**Remo**</span><span class="sxs-lookup"><span data-stu-id="434fc-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="434fc-170">**glTexParameter**</span><span class="sxs-lookup"><span data-stu-id="434fc-170">**glTexParameter**</span></span>](gltexparameter-functions.md)
</dt> </dl>

 

 





