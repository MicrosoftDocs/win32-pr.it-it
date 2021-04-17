---
title: funzione glColorMaterial (GL. h)
description: La funzione glColorMaterial fa sì che un colore del materiale tenga traccia del colore corrente.
ms.assetid: 6dbef2c2-f902-4f25-8a87-9e3d710dd807
keywords:
- funzione glColorMaterial OpenGL
topic_type:
- apiref
api_name:
- glColorMaterial
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32823eaa82e6a260790dd6fa23747f2b4228649
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400706"
---
# <a name="glcolormaterial-function"></a><span data-ttu-id="833af-104">glColorMaterial (funzione)</span><span class="sxs-lookup"><span data-stu-id="833af-104">glColorMaterial function</span></span>

<span data-ttu-id="833af-105">La funzione **glColorMaterial** fa sì che un colore del materiale tenga traccia del colore corrente.</span><span class="sxs-lookup"><span data-stu-id="833af-105">The **glColorMaterial** function causes a material color to track the current color.</span></span>

## <a name="syntax"></a><span data-ttu-id="833af-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="833af-106">Syntax</span></span>


```C++
void WINAPI glColorMaterial(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="833af-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="833af-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="833af-108">*faccia*</span><span class="sxs-lookup"><span data-stu-id="833af-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="833af-109">Specifica se i parametri del materiale anteriore, posteriore o anteriore e posteriore devono tenere traccia del colore corrente.</span><span class="sxs-lookup"><span data-stu-id="833af-109">Specifies whether front, back, or both front and back material parameters should track the current color.</span></span> <span data-ttu-id="833af-110">I valori accettati sono GL \_ Front, GL \_ back e GL \_ front \_ e \_ back.</span><span class="sxs-lookup"><span data-stu-id="833af-110">Accepted values are GL\_FRONT, GL\_BACK, and GL\_FRONT\_AND\_BACK.</span></span> <span data-ttu-id="833af-111">Il valore predefinito è GL \_ front \_ e \_ back.</span><span class="sxs-lookup"><span data-stu-id="833af-111">The default value is GL\_FRONT\_AND\_BACK.</span></span>

</dd> <dt>

<span data-ttu-id="833af-112">*mode*</span><span class="sxs-lookup"><span data-stu-id="833af-112">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="833af-113">Specifica quali dei diversi parametri del materiale tengono traccia del colore corrente.</span><span class="sxs-lookup"><span data-stu-id="833af-113">Specifies which of several material parameters track the current color.</span></span> <span data-ttu-id="833af-114">I valori accettati sono GL \_ Emission, GL \_ ambient, GL Diffusion, GL \_ \_ Specular e GL \_ ambient \_ e \_ Diffusion.</span><span class="sxs-lookup"><span data-stu-id="833af-114">Accepted values are GL\_EMISSION, GL\_AMBIENT, GL\_DIFFUSE, GL\_SPECULAR, and GL\_AMBIENT\_AND\_DIFFUSE.</span></span> <span data-ttu-id="833af-115">Il valore predefinito è GL \_ ambient \_ e \_ Diffusion.</span><span class="sxs-lookup"><span data-stu-id="833af-115">The default value is GL\_AMBIENT\_AND\_DIFFUSE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="833af-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="833af-116">Return value</span></span>

<span data-ttu-id="833af-117">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="833af-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="833af-118">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="833af-118">Error codes</span></span>

<span data-ttu-id="833af-119">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="833af-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="833af-120">Nome</span><span class="sxs-lookup"><span data-stu-id="833af-120">Name</span></span>                                                                                                  | <span data-ttu-id="833af-121">Significato</span><span class="sxs-lookup"><span data-stu-id="833af-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="833af-122"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="833af-122"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="833af-123">il tipo *o la* *modalità* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="833af-123">*face* or *mode* was not an accepted value.</span></span><br/>                                                                                |
| <dl> <span data-ttu-id="833af-124"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="833af-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="833af-125">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="833af-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="833af-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="833af-126">Remarks</span></span>

<span data-ttu-id="833af-127">La funzione **glColorMaterial** specifica i parametri del materiale che tengono traccia del colore corrente.</span><span class="sxs-lookup"><span data-stu-id="833af-127">The **glColorMaterial** function specifies which material parameters track the current color.</span></span> <span data-ttu-id="833af-128">Quando si Abilita il \_ \_ materiale del colore GL, per ogni materiale o materiale specificato da *Face*, il parametro Material o i parametri specificati in *modalità* tengono sempre traccia del colore corrente.</span><span class="sxs-lookup"><span data-stu-id="833af-128">When you enable GL\_COLOR\_MATERIAL, for each of the material or materials specified by *face*, the material parameter or parameters specified by *mode* track the current color at all times.</span></span> <span data-ttu-id="833af-129">Abilitare e disabilitare \_ \_ il materiale di colore GL con le funzioni [**glEnable**](glenable.md) e [**glDisable**](gldisable.md), che è possibile chiamare con il \_ materiale di colore GL \_ come argomento.</span><span class="sxs-lookup"><span data-stu-id="833af-129">Enable and disable GL\_COLOR\_MATERIAL with the functions [**glEnable**](glenable.md) and [**glDisable**](gldisable.md), which you call with GL\_COLOR\_MATERIAL as their argument.</span></span> <span data-ttu-id="833af-130">Per impostazione predefinita, \_ il \_ materiale colore GL è disabilitato.</span><span class="sxs-lookup"><span data-stu-id="833af-130">By default, GL\_COLOR\_MATERIAL is disabled.</span></span>

<span data-ttu-id="833af-131">Con **glColorMaterial** è possibile modificare un subset di parametri Material per ogni vertice usando solo la funzione [**glColor**](glcolor-functions.md) , senza chiamare [**glMaterial**](glmaterial-functions.md).</span><span class="sxs-lookup"><span data-stu-id="833af-131">With **glColorMaterial**, you can change a subset of material parameters for each vertex using only the [**glColor**](glcolor-functions.md) function, without calling [**glMaterial**](glmaterial-functions.md).</span></span> <span data-ttu-id="833af-132">Se si prevede di specificare solo un subset di parametri per ogni vertice, è preferibile farlo con **glColorMaterial** che con **glMaterial**.</span><span class="sxs-lookup"><span data-stu-id="833af-132">If you are going to specify only such a subset of parameters for each vertex, it is better to do so with **glColorMaterial** than with **glMaterial**.</span></span>

<span data-ttu-id="833af-133">Le funzioni seguenti consentono di recuperare informazioni correlate a **glColorMaterial**:</span><span class="sxs-lookup"><span data-stu-id="833af-133">The following functions retrieve information related to **glColorMaterial**:</span></span>

<span data-ttu-id="833af-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con parametro del \_ materiale colore GL argomento \_ \_</span><span class="sxs-lookup"><span data-stu-id="833af-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_COLOR\_MATERIAL\_PARAMETER</span></span>

<span data-ttu-id="833af-135">**glGet** con argomento del \_ colore del \_ materiale GL \_</span><span class="sxs-lookup"><span data-stu-id="833af-135">**glGet** with argument GL\_COLOR\_MATERIAL\_FACE</span></span>

<span data-ttu-id="833af-136">[**glIsEnabled**](glisenabled.md) con argomento relativo al \_ colore del \_ materiale GL</span><span class="sxs-lookup"><span data-stu-id="833af-136">[**glIsEnabled**](glisenabled.md) with argument GL\_COLOR\_MATERIAL</span></span>

## <a name="requirements"></a><span data-ttu-id="833af-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="833af-137">Requirements</span></span>



| <span data-ttu-id="833af-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="833af-138">Requirement</span></span> | <span data-ttu-id="833af-139">Valore</span><span class="sxs-lookup"><span data-stu-id="833af-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="833af-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="833af-140">Minimum supported client</span></span><br/> | <span data-ttu-id="833af-141">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="833af-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="833af-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="833af-142">Minimum supported server</span></span><br/> | <span data-ttu-id="833af-143">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="833af-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="833af-144">Intestazione</span><span class="sxs-lookup"><span data-stu-id="833af-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="833af-145"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="833af-145"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="833af-146">Libreria</span><span class="sxs-lookup"><span data-stu-id="833af-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="833af-147"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="833af-147"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="833af-148">DLL</span><span class="sxs-lookup"><span data-stu-id="833af-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="833af-149"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="833af-149"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="833af-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="833af-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="833af-151">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="833af-151">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="833af-152">**glColor**</span><span class="sxs-lookup"><span data-stu-id="833af-152">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="833af-153">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="833af-153">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="833af-154">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="833af-154">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="833af-155">**Remo**</span><span class="sxs-lookup"><span data-stu-id="833af-155">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="833af-156">**glGet**</span><span class="sxs-lookup"><span data-stu-id="833af-156">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="833af-157">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="833af-157">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="833af-158">**glLight**</span><span class="sxs-lookup"><span data-stu-id="833af-158">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="833af-159">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="833af-159">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> <dt>

[<span data-ttu-id="833af-160">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="833af-160">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> </dl>

 

 





