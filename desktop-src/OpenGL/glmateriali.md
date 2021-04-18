---
title: funzione glMateriali (GL. h)
description: La funzione TheglMateriali specifica i parametri del materiale per il modello di illuminazione.
ms.assetid: e3722dfd-3bdd-4460-8226-e50580ca1d79
keywords:
- funzione glMateriali OpenGL
topic_type:
- apiref
api_name:
- glMateriali
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dc4f1bf6628f1674cf9c3534b9f0c9d028246d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301260"
---
# <a name="glmateriali-function"></a><span data-ttu-id="881a9-104">glMateriali (funzione)</span><span class="sxs-lookup"><span data-stu-id="881a9-104">glMateriali function</span></span>

<span data-ttu-id="881a9-105">La funzione **glMateriali** specifica i parametri del materiale per il modello di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="881a9-105">The **glMateriali** function specifies material parameters for the lighting model.</span></span>

## <a name="syntax"></a><span data-ttu-id="881a9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="881a9-106">Syntax</span></span>


```C++
void WINAPI glMateriali(
   GLenum face,
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a><span data-ttu-id="881a9-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="881a9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="881a9-108">*faccia*</span><span class="sxs-lookup"><span data-stu-id="881a9-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="881a9-109">Il volto o i visi da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="881a9-109">The face or faces that are being updated.</span></span> <span data-ttu-id="881a9-110">Deve essere uno dei seguenti: GL \_ Front, GL \_ back o GL \_ front e GL \_ back.</span><span class="sxs-lookup"><span data-stu-id="881a9-110">Must be one of the following: GL\_FRONT, GL\_BACK, or GL\_FRONT and GL\_BACK.</span></span>

</dd> <dt>

<span data-ttu-id="881a9-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="881a9-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="881a9-112">Parametro Material a valore singolo della faccia o delle facce da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="881a9-112">The single-valued material parameter of the face or faces being updated.</span></span> <span data-ttu-id="881a9-113">Deve essere GL \_ lucentezza.</span><span class="sxs-lookup"><span data-stu-id="881a9-113">Must be GL\_SHININESS.</span></span>



| <span data-ttu-id="881a9-114">Valore</span><span class="sxs-lookup"><span data-stu-id="881a9-114">Value</span></span>                                                                                                                                                      | <span data-ttu-id="881a9-115">Significato</span><span class="sxs-lookup"><span data-stu-id="881a9-115">Meaning</span></span>                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <span data-ttu-id="881a9-116"><dt>**\_lucentezza GL**</dt></span><span class="sxs-lookup"><span data-stu-id="881a9-116"><dt>**GL\_SHININESS**</dt></span></span> </dl> | <span data-ttu-id="881a9-117">Il parametro *param* è un singolo integer che specifica l'esponente speculare RGBA del materiale.</span><span class="sxs-lookup"><span data-stu-id="881a9-117">The *param* parameter is a single integer that specifies the RGBA specular exponent of the material.</span></span> <span data-ttu-id="881a9-118">Viene eseguito il mapping diretto dei valori integer.</span><span class="sxs-lookup"><span data-stu-id="881a9-118">Integer values are mapped directly.</span></span> <span data-ttu-id="881a9-119">Sono accettati solo i valori nell'intervallo compreso tra \[ 0 e 128 \] .</span><span class="sxs-lookup"><span data-stu-id="881a9-119">Only values in the range \[0, 128\] are accepted.</span></span> <span data-ttu-id="881a9-120">L'esponente speculare predefinito per i materiali front-end e di back-end è 0.</span><span class="sxs-lookup"><span data-stu-id="881a9-120">The default specular exponent for both front-facing and back-facing materials is 0.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="881a9-121">*param*</span><span class="sxs-lookup"><span data-stu-id="881a9-121">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="881a9-122">Valore in cui verrà impostato il parametro GL \_ lucentezza.</span><span class="sxs-lookup"><span data-stu-id="881a9-122">The value to which parameter GL\_SHININESS will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="881a9-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="881a9-123">Return value</span></span>

<span data-ttu-id="881a9-124">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="881a9-124">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="881a9-125">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="881a9-125">Error codes</span></span>

<span data-ttu-id="881a9-126">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="881a9-126">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="881a9-127">Nome</span><span class="sxs-lookup"><span data-stu-id="881a9-127">Name</span></span>                                                                                              | <span data-ttu-id="881a9-128">Significato</span><span class="sxs-lookup"><span data-stu-id="881a9-128">Meaning</span></span>                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="881a9-129"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="881a9-129"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="881a9-130">*Face* o *pname* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="881a9-130">Either *face* or *pname* was not an accepted value.</span></span><br/>                |
| <dl> <span data-ttu-id="881a9-131"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="881a9-131"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="881a9-132">È stato specificato un esponente speculare non compreso nell'intervallo \[ 0, 128 \] .</span><span class="sxs-lookup"><span data-stu-id="881a9-132">A specular exponent outside the range of \[0, 128\] was specified.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="881a9-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="881a9-133">Remarks</span></span>

<span data-ttu-id="881a9-134">La funzione **glMateriali** assegna valori ai parametri del materiale.</span><span class="sxs-lookup"><span data-stu-id="881a9-134">The **glMateriali** function assigns values to material parameters.</span></span> <span data-ttu-id="881a9-135">Sono disponibili due set di parametri Material corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="881a9-135">There are two matched sets of material parameters.</span></span> <span data-ttu-id="881a9-136">Uno, il set in *primo piano* , viene usato per ombreggiare punti, linee, bitmap e tutti i poligoni (quando l'illuminazione bilaterale è disabilitata) o solo i poligoni di fronte (quando è abilitata l'illuminazione bilaterale).</span><span class="sxs-lookup"><span data-stu-id="881a9-136">One, the *front-facing* set, is used to shade points, lines, bitmaps, and all polygons (when two-sided lighting is disabled), or just front-facing polygons (when two-sided lighting is enabled).</span></span> <span data-ttu-id="881a9-137">L'altro set, *back-facing*, viene usato per ombreggiare i poligoni di back-end solo quando è abilitata l'illuminazione a due lati.</span><span class="sxs-lookup"><span data-stu-id="881a9-137">The other set, *back-facing*, is used to shade back-facing polygons only when two-sided lighting is enabled.</span></span> <span data-ttu-id="881a9-138">Per informazioni dettagliate sui calcoli di illuminazione unilaterale e bilaterale, vedere [**glLightModel**](gllightmodel-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="881a9-138">Refer to [**glLightModel**](gllightmodel-functions.md) for details concerning one-sided and two-sided lighting calculations.</span></span>

<span data-ttu-id="881a9-139">La funzione **glMateriali** accetta tre argomenti.</span><span class="sxs-lookup"><span data-stu-id="881a9-139">The **glMateriali** function takes three arguments.</span></span> <span data-ttu-id="881a9-140">Il *primo, ovvero, specifica* se i materiali di contabilità GL \_ , i \_ materiali back GL o entrambi i \_ materiali GL front \_ e \_ back verranno modificati.</span><span class="sxs-lookup"><span data-stu-id="881a9-140">The first, *face*, specifies whether the GL\_FRONT materials, the GL\_BACK materials, or both GL\_FRONT\_AND\_BACK materials will be modified.</span></span> <span data-ttu-id="881a9-141">Il secondo, *pname*, specifica quale dei diversi parametri in uno o entrambi i set verranno modificati.</span><span class="sxs-lookup"><span data-stu-id="881a9-141">The second, *pname*, specifies which of several parameters in one or both sets will be modified.</span></span> <span data-ttu-id="881a9-142">Il *terzo parametro specifica* il valore che verrà assegnato al parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="881a9-142">The third, *param*, specifies what value will be assigned to the specified parameter.</span></span>

<span data-ttu-id="881a9-143">I parametri del materiale vengono usati nell'equazione di illuminazione applicata facoltativamente a ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="881a9-143">Material parameters are used in the lighting equation that is optionally applied to each vertex.</span></span> <span data-ttu-id="881a9-144">L'equazione viene illustrata in [**glLightModel**](gllightmodel-functions.md).</span><span class="sxs-lookup"><span data-stu-id="881a9-144">The equation is discussed in [**glLightModel**](gllightmodel-functions.md).</span></span>

<span data-ttu-id="881a9-145">I parametri Material possono essere aggiornati in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="881a9-145">The material parameters can be updated at any time.</span></span> <span data-ttu-id="881a9-146">In particolare, è possibile chiamare **glMateriali** tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="881a9-146">In particular, **glMateriali** can be called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="881a9-147">Se è necessario modificare un solo parametro Material per ogni vertice, tuttavia, [**glColorMaterial**](glcolormaterial.md) è preferibile rispetto a **glMateriali**.</span><span class="sxs-lookup"><span data-stu-id="881a9-147">If only a single material parameter is to be changed per vertex, however, [**glColorMaterial**](glcolormaterial.md) is preferred over **glMateriali**.</span></span>

<span data-ttu-id="881a9-148">La funzione seguente recupera le informazioni correlate a **glMateriali**:</span><span class="sxs-lookup"><span data-stu-id="881a9-148">The following function retrieves information related to **glMateriali**:</span></span>

[<span data-ttu-id="881a9-149">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="881a9-149">**glGetMaterial**</span></span>](glgetmaterial.md)

## <a name="requirements"></a><span data-ttu-id="881a9-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="881a9-150">Requirements</span></span>



| <span data-ttu-id="881a9-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="881a9-151">Requirement</span></span> | <span data-ttu-id="881a9-152">Valore</span><span class="sxs-lookup"><span data-stu-id="881a9-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="881a9-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="881a9-153">Minimum supported client</span></span><br/> | <span data-ttu-id="881a9-154">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="881a9-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="881a9-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="881a9-155">Minimum supported server</span></span><br/> | <span data-ttu-id="881a9-156">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="881a9-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="881a9-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="881a9-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="881a9-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="881a9-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="881a9-159">Libreria</span><span class="sxs-lookup"><span data-stu-id="881a9-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="881a9-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="881a9-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="881a9-161">DLL</span><span class="sxs-lookup"><span data-stu-id="881a9-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="881a9-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="881a9-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="881a9-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="881a9-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="881a9-164">**glColorMaterial**</span><span class="sxs-lookup"><span data-stu-id="881a9-164">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="881a9-165">**glLight**</span><span class="sxs-lookup"><span data-stu-id="881a9-165">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="881a9-166">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="881a9-166">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





