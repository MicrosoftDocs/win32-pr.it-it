---
title: funzione glGetMaterialfv (GL. h)
description: Le funzioni glGetMaterialfv e glGetMaterialiv restituiscono parametri di materiale. | funzione glGetMaterialfv (GL. h)
ms.assetid: b61dbe0c-5cc2-4397-9d7c-b99507a9f037
keywords:
- funzione glGetMaterialfv OpenGL
topic_type:
- apiref
api_name:
- glGetMaterialfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce33ee1f88d492f67cf3ebb93c575f8f36d1ffa0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352531"
---
# <a name="glgetmaterialfv-function"></a><span data-ttu-id="d08cf-105">glGetMaterialfv (funzione)</span><span class="sxs-lookup"><span data-stu-id="d08cf-105">glGetMaterialfv function</span></span>

<span data-ttu-id="d08cf-106">Le funzioni **glGetMaterialfv** e [**glGetMaterialiv**](glgetmaterialiv.md) restituiscono parametri di materiale.</span><span class="sxs-lookup"><span data-stu-id="d08cf-106">The **glGetMaterialfv** and [**glGetMaterialiv**](glgetmaterialiv.md) functions return material parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="d08cf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d08cf-107">Syntax</span></span>


```C++
void WINAPI glGetMaterialfv(
   GLenum  face,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="d08cf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="d08cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d08cf-109">*faccia*</span><span class="sxs-lookup"><span data-stu-id="d08cf-109">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="d08cf-110">Specifica quale dei due materiali viene sottoposto a query.</span><span class="sxs-lookup"><span data-stu-id="d08cf-110">Specifies which of the two materials is being queried.</span></span> <span data-ttu-id="d08cf-111">GL \_ front o GL \_ back sono accettati, che rappresentano rispettivamente i materiali anteriore e posteriore.</span><span class="sxs-lookup"><span data-stu-id="d08cf-111">GL\_FRONT or GL\_BACK are accepted, representing the front and back materials, respectively.</span></span>

</dd> <dt>

<span data-ttu-id="d08cf-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="d08cf-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="d08cf-113">Parametro Material da restituire.</span><span class="sxs-lookup"><span data-stu-id="d08cf-113">The material parameter to return.</span></span> <span data-ttu-id="d08cf-114">Vengono accettati i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="d08cf-114">The following values are accepted.</span></span>



| <span data-ttu-id="d08cf-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d08cf-115">Value</span></span>                                                                                                                                                                   | <span data-ttu-id="d08cf-116">Significato</span><span class="sxs-lookup"><span data-stu-id="d08cf-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <span data-ttu-id="d08cf-117"><dt>**\_ambiente GL**</dt></span><span class="sxs-lookup"><span data-stu-id="d08cf-117"><dt>**GL\_AMBIENT**</dt></span></span> </dl>                    | <span data-ttu-id="d08cf-118">Il parametro *params* restituisce quattro valori integer o a virgola mobile che rappresentano la reflection di ambiente del materiale.</span><span class="sxs-lookup"><span data-stu-id="d08cf-118">The *params* parameter returns four integer or floating-point values representing the ambient reflectance of the material.</span></span> <span data-ttu-id="d08cf-119">Per i valori integer, quando richiesto, viene eseguito il mapping lineare dalla rappresentazione a virgola mobile interna, in modo che 1,0 sia mappato al valore integer rappresentabile più positivo e-1,0 sia mappato al valore integer rappresentabile più negativo.</span><span class="sxs-lookup"><span data-stu-id="d08cf-119">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="d08cf-120">Se il valore interno non è compreso nell'intervallo \[ -1, 1 \] , il valore restituito intero corrispondente non è definito.</span><span class="sxs-lookup"><span data-stu-id="d08cf-120">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>     |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <span data-ttu-id="d08cf-121"><dt>**GL \_ diffuse**</dt></span><span class="sxs-lookup"><span data-stu-id="d08cf-121"><dt>**GL\_DIFFUSE**</dt></span></span> </dl>                    | <span data-ttu-id="d08cf-122">Il parametro *params* restituisce quattro valori integer o a virgola mobile che rappresentano la riflettenza diffusa del materiale.</span><span class="sxs-lookup"><span data-stu-id="d08cf-122">The *params* parameter returns four integer or floating-point values representing the diffuse reflectance of the material.</span></span> <span data-ttu-id="d08cf-123">Per i valori integer, quando richiesto, viene eseguito il mapping lineare dalla rappresentazione a virgola mobile interna, in modo che 1,0 sia mappato al valore integer rappresentabile più positivo e-1,0 sia mappato al valore integer rappresentabile più negativo.</span><span class="sxs-lookup"><span data-stu-id="d08cf-123">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="d08cf-124">Se il valore interno non è compreso nell'intervallo \[ -1, 1 \] , il valore restituito intero corrispondente non è definito.</span><span class="sxs-lookup"><span data-stu-id="d08cf-124">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>     |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <span data-ttu-id="d08cf-125"><dt>**\_speculare GL**</dt></span><span class="sxs-lookup"><span data-stu-id="d08cf-125"><dt>**GL\_SPECULAR**</dt></span></span> </dl>                 | <span data-ttu-id="d08cf-126">Il parametro *params* restituisce quattro valori integer o a virgola mobile che rappresentano la reflection speculare del materiale.</span><span class="sxs-lookup"><span data-stu-id="d08cf-126">The *params* parameter returns four integer or floating-point values representing the specular reflectance of the material.</span></span> <span data-ttu-id="d08cf-127">Per i valori integer, quando richiesto, viene eseguito il mapping lineare dalla rappresentazione a virgola mobile interna, in modo che 1,0 sia mappato al valore integer rappresentabile più positivo e-1,0 sia mappato al valore integer rappresentabile più negativo.</span><span class="sxs-lookup"><span data-stu-id="d08cf-127">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="d08cf-128">Se il valore interno non è compreso nell'intervallo \[ -1, 1 \] , il valore restituito intero corrispondente non è definito.</span><span class="sxs-lookup"><span data-stu-id="d08cf-128">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/>    |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <span data-ttu-id="d08cf-129"><dt>**\_emissione GL**</dt></span><span class="sxs-lookup"><span data-stu-id="d08cf-129"><dt>**GL\_EMISSION**</dt></span></span> </dl>                 | <span data-ttu-id="d08cf-130">Il parametro *params* restituisce quattro valori integer o a virgola mobile che rappresentano l'intensità della luce emessa del materiale.</span><span class="sxs-lookup"><span data-stu-id="d08cf-130">The *params* parameter returns four integer or floating-point values representing the emitted light intensity of the material.</span></span> <span data-ttu-id="d08cf-131">Per i valori integer, quando richiesto, viene eseguito il mapping lineare dalla rappresentazione a virgola mobile interna, in modo che 1,0 sia mappato al valore integer rappresentabile più positivo e-1,0 sia mappato al valore integer rappresentabile più negativo.</span><span class="sxs-lookup"><span data-stu-id="d08cf-131">Integer values, when requested, are linearly mapped from the internal floating-point representation such that 1.0 maps to the most positive representable integer value, and -1.0 maps to the most negative representable integer value.</span></span> <span data-ttu-id="d08cf-132">Se il valore interno non è compreso nell'intervallo \[ -1, 1 \] , il valore restituito intero corrispondente non è definito.</span><span class="sxs-lookup"><span data-stu-id="d08cf-132">If the internal value is outside the range \[-1,1\], the corresponding integer return value is undefined.</span></span><br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <span data-ttu-id="d08cf-133"><dt>**\_lucentezza GL**</dt></span><span class="sxs-lookup"><span data-stu-id="d08cf-133"><dt>**GL\_SHININESS**</dt></span></span> </dl>              | <span data-ttu-id="d08cf-134">Il parametro *params* restituisce un intero o un valore a virgola mobile che rappresenta l'esponente speculare del materiale.</span><span class="sxs-lookup"><span data-stu-id="d08cf-134">The *params* parameter returns one integer or floating-point value representing the specular exponent of the material.</span></span> <span data-ttu-id="d08cf-135">I valori integer, se richiesti, vengono calcolati mediante l'arrotondamento del valore a virgola mobile interno al valore intero più vicino.</span><span class="sxs-lookup"><span data-stu-id="d08cf-135">Integer values, when requested, are computed by rounding the internal floating-point value to the nearest integer value.</span></span><br/>                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <span data-ttu-id="d08cf-136"><dt>**indici di \_ colore GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d08cf-136"><dt>**GL\_COLOR\_INDEXES**</dt></span></span> </dl> | <span data-ttu-id="d08cf-137">Il parametro *params* restituisce tre valori integer o a virgola mobile che rappresentano gli indici di ambiente, diffusi e speculari del materiale.</span><span class="sxs-lookup"><span data-stu-id="d08cf-137">The *params* parameter returns three integer or floating-point values representing the ambient, diffuse, and specular indexes of the material.</span></span> <span data-ttu-id="d08cf-138">Usare questi indici solo per l'illuminazione degli indici dei colori.</span><span class="sxs-lookup"><span data-stu-id="d08cf-138">Use these indexes only for color-index lighting.</span></span> <span data-ttu-id="d08cf-139">Gli altri parametri vengono usati solo per l'illuminazione RGBA. I valori integer, se richiesti, vengono calcolati mediante l'arrotondamento dei valori a virgola mobile interni ai valori integer più vicini.</span><span class="sxs-lookup"><span data-stu-id="d08cf-139">(The other parameters are all used only for RGBA lighting.) Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.</span></span><br/>                                                                                            |



 

</dd> <dt>

<span data-ttu-id="d08cf-140">*params*</span><span class="sxs-lookup"><span data-stu-id="d08cf-140">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="d08cf-141">Restituisce i dati richiesti.</span><span class="sxs-lookup"><span data-stu-id="d08cf-141">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d08cf-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d08cf-142">Return value</span></span>

<span data-ttu-id="d08cf-143">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="d08cf-143">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d08cf-144">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="d08cf-144">Error codes</span></span>

<span data-ttu-id="d08cf-145">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="d08cf-145">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="d08cf-146">Nome</span><span class="sxs-lookup"><span data-stu-id="d08cf-146">Name</span></span>                                                                                                  | <span data-ttu-id="d08cf-147">Significato</span><span class="sxs-lookup"><span data-stu-id="d08cf-147">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d08cf-148"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d08cf-148"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="d08cf-149">*target* o *query* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="d08cf-149">*target* or *query* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="d08cf-150"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d08cf-150"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="d08cf-151">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="d08cf-151">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="d08cf-152">Commenti</span><span class="sxs-lookup"><span data-stu-id="d08cf-152">Remarks</span></span>

<span data-ttu-id="d08cf-153">La funzione **glGetMaterial** restituisce in *params* il valore o i valori del parametro *pname* della *superficie* del materiale.</span><span class="sxs-lookup"><span data-stu-id="d08cf-153">The **glGetMaterial** function returns in *params* the value or values of parameter *pname* of material *face*.</span></span>

<span data-ttu-id="d08cf-154">Se viene generato un errore, non viene apportata alcuna modifica al contenuto di *params*.</span><span class="sxs-lookup"><span data-stu-id="d08cf-154">If an error is generated, no change is made to the contents of *params*.</span></span>

## <a name="requirements"></a><span data-ttu-id="d08cf-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d08cf-155">Requirements</span></span>



| <span data-ttu-id="d08cf-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="d08cf-156">Requirement</span></span> | <span data-ttu-id="d08cf-157">Valore</span><span class="sxs-lookup"><span data-stu-id="d08cf-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d08cf-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d08cf-158">Minimum supported client</span></span><br/> | <span data-ttu-id="d08cf-159">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d08cf-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d08cf-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d08cf-160">Minimum supported server</span></span><br/> | <span data-ttu-id="d08cf-161">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d08cf-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d08cf-162">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d08cf-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="d08cf-163"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="d08cf-163"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="d08cf-164">Libreria</span><span class="sxs-lookup"><span data-stu-id="d08cf-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="d08cf-165"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d08cf-165"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d08cf-166">DLL</span><span class="sxs-lookup"><span data-stu-id="d08cf-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d08cf-167"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d08cf-167"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d08cf-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d08cf-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d08cf-169">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="d08cf-169">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="d08cf-170">**Remo**</span><span class="sxs-lookup"><span data-stu-id="d08cf-170">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="d08cf-171">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="d08cf-171">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





