---
title: funzione glGetTexGeniv (GL. h)
description: Le funzioni glGetTexGendv, glGetTexGenfv e glGetTexGeniv restituiscono parametri di generazione delle coordinate di trama. | funzione glGetTexGeniv (GL. h)
ms.assetid: 62c481d1-4862-43bb-9319-5a282c4e47d3
keywords:
- funzione glGetTexGeniv OpenGL
topic_type:
- apiref
api_name:
- glGetTexGeniv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29569c84d21dbb2cd69579c78747e844cfd23ba4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321308"
---
# <a name="glgettexgeniv-function"></a><span data-ttu-id="3299a-105">glGetTexGeniv (funzione)</span><span class="sxs-lookup"><span data-stu-id="3299a-105">glGetTexGeniv function</span></span>

<span data-ttu-id="3299a-106">Le funzioni [**glGetTexGendv**](glgettexgendv.md), [**glGetTexGenfv**](glgettexgenfv.md)e **glGetTexGeniv** restituiscono parametri di generazione delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="3299a-106">The [**glGetTexGendv**](glgettexgendv.md), [**glGetTexGenfv**](glgettexgenfv.md), and **glGetTexGeniv** functions return texture coordinate generation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="3299a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3299a-107">Syntax</span></span>


```C++
void WINAPI glGetTexGeniv(
   GLenum coord,
   GLenum pname,
   GLint  *params
);
```



## <a name="parameters"></a><span data-ttu-id="3299a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3299a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3299a-109">*Coord*</span><span class="sxs-lookup"><span data-stu-id="3299a-109">*coord*</span></span> 
</dt> <dd>

<span data-ttu-id="3299a-110">Coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="3299a-110">A texture coordinate.</span></span> <span data-ttu-id="3299a-111">Deve essere GL \_ S, GL \_ T, GL \_ R o GL \_ Q.</span><span class="sxs-lookup"><span data-stu-id="3299a-111">Must be GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

</dd> <dt>

<span data-ttu-id="3299a-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="3299a-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="3299a-113">Nome simbolico del valore o dei valori da restituire.</span><span class="sxs-lookup"><span data-stu-id="3299a-113">The symbolic name of the value(s) to be returned.</span></span> <span data-ttu-id="3299a-114">Deve essere \_ \_ \_ la modalità gen della trama GL o il nome di una delle equazioni del piano di generazione della trama, ovvero il \_ piano dell'oggetto GL o il \_ \_ piano GL Eye \_ .</span><span class="sxs-lookup"><span data-stu-id="3299a-114">Must be either GL\_TEXTURE\_GEN\_MODE or the name of one of the texture generation plane equations: GL\_OBJECT\_PLANE or GL\_EYE\_PLANE.</span></span> <span data-ttu-id="3299a-115">Questi valori sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="3299a-115">These values are as follows.</span></span>



| <span data-ttu-id="3299a-116">Valore</span><span class="sxs-lookup"><span data-stu-id="3299a-116">Value</span></span>                                                                                                                                                                             | <span data-ttu-id="3299a-117">Significato</span><span class="sxs-lookup"><span data-stu-id="3299a-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span><dl> <span data-ttu-id="3299a-118"><dt>**\_modalità di \_ generazione \_ trama GL**</dt></span><span class="sxs-lookup"><span data-stu-id="3299a-118"><dt>**GL\_TEXTURE\_GEN\_MODE**</dt></span></span> </dl> | <span data-ttu-id="3299a-119">Il parametro *params* restituisce la funzione di generazione della trama a valore singolo, una costante simbolica.</span><span class="sxs-lookup"><span data-stu-id="3299a-119">The *params* parameter returns the single-valued texture generation function, a symbolic constant.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span><dl> <span data-ttu-id="3299a-120"><dt>**\_piano oggetto \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="3299a-120"><dt>**GL\_OBJECT\_PLANE**</dt></span></span> </dl>              | <span data-ttu-id="3299a-121">Il parametro *params* restituisce i quattro coefficienti di equazione del piano che specificano la generazione della coordinata lineare dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="3299a-121">The *params* parameter returns the four plane equation coefficients that specify object linear-coordinate generation.</span></span> <span data-ttu-id="3299a-122">Per i valori integer, quando richiesto, viene eseguito il mapping direttamente dalla rappresentazione a virgola mobile interna.</span><span class="sxs-lookup"><span data-stu-id="3299a-122">Integer values, when requested, are mapped directly from the internal floating-point representation.</span></span><br/>                                                                                                                                                                                                                                    |
| <span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span><dl> <span data-ttu-id="3299a-123"><dt>**\_piano d'occhio GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3299a-123"><dt>**GL\_EYE\_PLANE**</dt></span></span> </dl>                       | <span data-ttu-id="3299a-124">Il parametro *params* restituisce i quattro coefficienti di equazione del piano che specificano la generazione della coordinata lineare degli occhi.</span><span class="sxs-lookup"><span data-stu-id="3299a-124">The *params* parameter returns the four plane equation coefficients that specify eye linear-coordinate generation.</span></span> <span data-ttu-id="3299a-125">Per i valori integer, quando richiesto, viene eseguito il mapping direttamente dalla rappresentazione a virgola mobile interna.</span><span class="sxs-lookup"><span data-stu-id="3299a-125">Integer values, when requested, are mapped directly from the internal floating-point representation.</span></span> <span data-ttu-id="3299a-126">I valori restituiti sono quelli mantenuti in coordinate oculari.</span><span class="sxs-lookup"><span data-stu-id="3299a-126">The returned values are those maintained in eye coordinates.</span></span> <span data-ttu-id="3299a-127">Non sono uguali ai valori specificati tramite [**glTexGen**](gltexgen-functions.md), a meno che non sia stata identificata la matrice Modelview al momento della chiamata di **glTexGen** .</span><span class="sxs-lookup"><span data-stu-id="3299a-127">They are not equal to the values specified using [**glTexGen**](gltexgen-functions.md), unless the modelview matrix was identified at the time **glTexGen** was called.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3299a-128">*params*</span><span class="sxs-lookup"><span data-stu-id="3299a-128">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="3299a-129">Restituisce i dati richiesti.</span><span class="sxs-lookup"><span data-stu-id="3299a-129">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3299a-130">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3299a-130">Return value</span></span>

<span data-ttu-id="3299a-131">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="3299a-131">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3299a-132">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="3299a-132">Error codes</span></span>

<span data-ttu-id="3299a-133">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="3299a-133">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3299a-134">Nome</span><span class="sxs-lookup"><span data-stu-id="3299a-134">Name</span></span>                                                                                                  | <span data-ttu-id="3299a-135">Significato</span><span class="sxs-lookup"><span data-stu-id="3299a-135">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3299a-136"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3299a-136"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="3299a-137">*Coord* o *pname* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="3299a-137">*coord* or *pname* was not an accepted value.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="3299a-138"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3299a-138"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3299a-139">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="3299a-139">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3299a-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="3299a-140">Remarks</span></span>

<span data-ttu-id="3299a-141">La funzione **glGetTexGen** restituisce parametri selezionati in *params* di una funzione di generazione della coordinata di trama specificata con **glTexGen**.</span><span class="sxs-lookup"><span data-stu-id="3299a-141">The **glGetTexGen** function returns in *params* selected parameters of a texture-coordinate generation function that you specified with **glTexGen**.</span></span> <span data-ttu-id="3299a-142">Il parametro *Coord* denomina una delle coordinate di trama (*s*, *t*, *r*, *q*), usando la costante simbolica GL \_ s, GL \_ t, GL \_ r o GL \_ q.</span><span class="sxs-lookup"><span data-stu-id="3299a-142">The *coord* parameter names one of the (*s*, *t*, *r*, *q*) texture coordinates, using the symbolic constant GL\_S, GL\_T, GL\_R, or GL\_Q.</span></span>

<span data-ttu-id="3299a-143">Se viene generato un errore, non viene apportata alcuna modifica al contenuto di *params*.</span><span class="sxs-lookup"><span data-stu-id="3299a-143">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="3299a-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3299a-144">Requirements</span></span>



| <span data-ttu-id="3299a-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="3299a-145">Requirement</span></span> | <span data-ttu-id="3299a-146">Valore</span><span class="sxs-lookup"><span data-stu-id="3299a-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3299a-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3299a-147">Minimum supported client</span></span><br/> | <span data-ttu-id="3299a-148">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3299a-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3299a-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3299a-149">Minimum supported server</span></span><br/> | <span data-ttu-id="3299a-150">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3299a-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3299a-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3299a-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="3299a-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3299a-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3299a-153">Libreria</span><span class="sxs-lookup"><span data-stu-id="3299a-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="3299a-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3299a-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3299a-155">DLL</span><span class="sxs-lookup"><span data-stu-id="3299a-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3299a-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3299a-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3299a-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3299a-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3299a-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3299a-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3299a-159">**Remo**</span><span class="sxs-lookup"><span data-stu-id="3299a-159">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3299a-160">**glTexGen**</span><span class="sxs-lookup"><span data-stu-id="3299a-160">**glTexGen**</span></span>](gltexgen-functions.md)
</dt> </dl>

 

 





