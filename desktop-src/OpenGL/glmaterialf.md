---
title: funzione glMaterialf (GL. h)
description: La funzione glMaterialf specifica i parametri del materiale per il modello di illuminazione.
ms.assetid: c6d183c4-2d1f-4fb9-b24f-c132ebfc708d
keywords:
- funzione glMaterialf OpenGL
topic_type:
- apiref
api_name:
- glMaterialf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c77cb1be5595f4a872988bbc6480d4cd6f65aae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302624"
---
# <a name="glmaterialf-function"></a><span data-ttu-id="e6e3d-104">glMaterialf (funzione)</span><span class="sxs-lookup"><span data-stu-id="e6e3d-104">glMaterialf function</span></span>

<span data-ttu-id="e6e3d-105">La funzione **glMaterialf** specifica i parametri del materiale per il modello di illuminazione.</span><span class="sxs-lookup"><span data-stu-id="e6e3d-105">The **glMaterialf** function specifies material parameters for the lighting model.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6e3d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6e3d-106">Syntax</span></span>


```C++
void WINAPI glMaterialf(
   GLenum  face,
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a><span data-ttu-id="e6e3d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e6e3d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6e3d-108">*faccia*</span><span class="sxs-lookup"><span data-stu-id="e6e3d-108">*face*</span></span> 
</dt> <dd>

<span data-ttu-id="e6e3d-109">Il volto o i visi da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="e6e3d-109">The face or faces that are being updated.</span></span> <span data-ttu-id="e6e3d-110">Deve essere uno dei seguenti: GL \_ Front, GL \_ back o GL \_ front e GL \_ back.</span><span class="sxs-lookup"><span data-stu-id="e6e3d-110">Must be one of the following: GL\_FRONT, GL\_BACK, or GL\_FRONT and GL\_BACK.</span></span>

</dd> <dt>

<span data-ttu-id="e6e3d-111">*pname*</span><span class="sxs-lookup"><span data-stu-id="e6e3d-111">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="e6e3d-112">Parametro Material a valore singolo della faccia o delle facce da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="e6e3d-112">The single-valued material parameter of the face or faces being updated.</span></span> <span data-ttu-id="e6e3d-113">Deve essere GL \_ lucentezza.</span><span class="sxs-lookup"><span data-stu-id="e6e3d-113">Must be GL\_SHININESS.</span></span>



| <span data-ttu-id="e6e3d-114">Valore</span><span class="sxs-lookup"><span data-stu-id="e6e3d-114">Value</span></span>                                                                                                                                                      | <span data-ttu-id="e6e3d-115">Significato</span><span class="sxs-lookup"><span data-stu-id="e6e3d-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <span data-ttu-id="e6e3d-116"><dt>**\_lucentezza GL**</dt></span><span class="sxs-lookup"><span data-stu-id="e6e3d-116"><dt>**GL\_SHININESS**</dt></span></span> </dl> | <span data-ttu-id="e6e3d-117">Il parametro *param* è un singolo valore a virgola mobile che specifica l'esponente speculare RGBA del materiale.</span><span class="sxs-lookup"><span data-stu-id="e6e3d-117">The *param* parameter is a single floating-point value that specifies the RGBA specular exponent of the material.</span></span> <span data-ttu-id="e6e3d-118">Viene eseguito il mapping diretto dei valori integer.</span><span class="sxs-lookup"><span data-stu-id="e6e3d-118">Integer values are mapped directly.</span></span> <span data-ttu-id="e6e3d-119">Sono accettati solo i valori nell'intervallo compreso tra \[ 0 e 128 \] .</span><span class="sxs-lookup"><span data-stu-id="e6e3d-119">Only values in the range \[0, 128\] are accepted.</span></span> <span data-ttu-id="e6e3d-120">L'esponente speculare predefinito per i materiali front-end e di back-end è 0.</span><span class="sxs-lookup"><span data-stu-id="e6e3d-120">The default specular exponent for both front-facing and back-facing materials is 0.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="e6e3d-121">*param*</span><span class="sxs-lookup"><span data-stu-id="e6e3d-121">*param*</span></span> 
</dt> <dd>

<span data-ttu-id="e6e3d-122">Valore in cui verrà impostato il parametro GL \_ lucentezza.</span><span class="sxs-lookup"><span data-stu-id="e6e3d-122">The value to which parameter GL\_SHININESS will be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6e3d-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e6e3d-123">Return value</span></span>

<span data-ttu-id="e6e3d-124">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="e6e3d-124">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e6e3d-125">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="e6e3d-125">Error codes</span></span>

<span data-ttu-id="e6e3d-126">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="e6e3d-126">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e6e3d-127">Nome</span><span class="sxs-lookup"><span data-stu-id="e6e3d-127">Name</span></span>                                                                                              | <span data-ttu-id="e6e3d-128">Significato</span><span class="sxs-lookup"><span data-stu-id="e6e3d-128">Meaning</span></span>                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e6e3d-129"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e6e3d-129"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>  | <span data-ttu-id="e6e3d-130">*Face* o *pname* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="e6e3d-130">Either *face* or *pname* was not an accepted value.</span></span><br/>                |
| <dl> <span data-ttu-id="e6e3d-131"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e6e3d-131"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl> | <span data-ttu-id="e6e3d-132">È stato specificato un esponente speculare non compreso nell'intervallo \[ 0, 128 \] .</span><span class="sxs-lookup"><span data-stu-id="e6e3d-132">A specular exponent outside the range of \[0, 128\] was specified.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e6e3d-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6e3d-133">Remarks</span></span>

<span data-ttu-id="e6e3d-134">La funzione **glMaterialf** assegna valori ai parametri del materiale.</span><span class="sxs-lookup"><span data-stu-id="e6e3d-134">The **glMaterialf** function assigns values to material parameters.</span></span> <span data-ttu-id="e6e3d-135">Sono disponibili due set di parametri Material corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="e6e3d-135">There are two matched sets of material parameters.</span></span> <span data-ttu-id="e6e3d-136">Uno, il set in *primo piano* , viene usato per ombreggiare punti, linee, bitmap e tutti i poligoni (quando l'illuminazione bilaterale è disabilitata) o solo i poligoni di fronte (quando è abilitata l'illuminazione bilaterale).</span><span class="sxs-lookup"><span data-stu-id="e6e3d-136">One, the *front-facing* set, is used to shade points, lines, bitmaps, and all polygons (when two-sided lighting is disabled), or just front-facing polygons (when two-sided lighting is enabled).</span></span> <span data-ttu-id="e6e3d-137">L'altro set, *back-facing*, viene usato per ombreggiare i poligoni di back-end solo quando è abilitata l'illuminazione a due lati.</span><span class="sxs-lookup"><span data-stu-id="e6e3d-137">The other set, *back-facing*, is used to shade back-facing polygons only when two-sided lighting is enabled.</span></span> <span data-ttu-id="e6e3d-138">Per informazioni dettagliate sui calcoli di illuminazione unilaterale e bilaterale, vedere [**glLightModel**](gllightmodel-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="e6e3d-138">Refer to [**glLightModel**](gllightmodel-functions.md) for details concerning one-sided and two-sided lighting calculations.</span></span>

<span data-ttu-id="e6e3d-139">La funzione **glMaterialf** accetta tre argomenti.</span><span class="sxs-lookup"><span data-stu-id="e6e3d-139">The **glMaterialf** function takes three arguments.</span></span> <span data-ttu-id="e6e3d-140">Il *primo, ovvero, specifica* se i materiali di contabilità GL \_ , i \_ materiali back GL o entrambi i \_ materiali GL front \_ e \_ back verranno modificati.</span><span class="sxs-lookup"><span data-stu-id="e6e3d-140">The first, *face*, specifies whether the GL\_FRONT materials, the GL\_BACK materials, or both GL\_FRONT\_AND\_BACK materials will be modified.</span></span> <span data-ttu-id="e6e3d-141">Il secondo, *pname*, specifica quale dei diversi parametri in uno o entrambi i set verranno modificati.</span><span class="sxs-lookup"><span data-stu-id="e6e3d-141">The second, *pname*, specifies which of several parameters in one or both sets will be modified.</span></span> <span data-ttu-id="e6e3d-142">Il *terzo parametro specifica* il valore che verrà assegnato al parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="e6e3d-142">The third, *param*, specifies what value will be assigned to the specified parameter.</span></span>

<span data-ttu-id="e6e3d-143">I parametri del materiale vengono usati nell'equazione di illuminazione applicata facoltativamente a ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="e6e3d-143">Material parameters are used in the lighting equation that is optionally applied to each vertex.</span></span> <span data-ttu-id="e6e3d-144">L'equazione viene illustrata in [**glLightModel**](gllightmodel-functions.md).</span><span class="sxs-lookup"><span data-stu-id="e6e3d-144">The equation is discussed in [**glLightModel**](gllightmodel-functions.md).</span></span>

<span data-ttu-id="e6e3d-145">I parametri Material possono essere aggiornati in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="e6e3d-145">The material parameters can be updated at any time.</span></span> <span data-ttu-id="e6e3d-146">In particolare, è possibile chiamare **glMaterialf** tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e6e3d-146">In particular, **glMaterialf** can be called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <span data-ttu-id="e6e3d-147">Se è necessario modificare un solo parametro Material per ogni vertice, tuttavia, [**glColorMaterial**](glcolormaterial.md) è preferibile rispetto a **glMaterialf**.</span><span class="sxs-lookup"><span data-stu-id="e6e3d-147">If only a single material parameter is to be changed per vertex, however, [**glColorMaterial**](glcolormaterial.md) is preferred over **glMaterialf**.</span></span>

<span data-ttu-id="e6e3d-148">La funzione seguente recupera le informazioni correlate a **glMaterialf**:</span><span class="sxs-lookup"><span data-stu-id="e6e3d-148">The following function retrieves information related to **glMaterialf**:</span></span>

[<span data-ttu-id="e6e3d-149">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="e6e3d-149">**glGetMaterial**</span></span>](glgetmaterial.md)

## <a name="requirements"></a><span data-ttu-id="e6e3d-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6e3d-150">Requirements</span></span>



| <span data-ttu-id="e6e3d-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6e3d-151">Requirement</span></span> | <span data-ttu-id="e6e3d-152">Valore</span><span class="sxs-lookup"><span data-stu-id="e6e3d-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6e3d-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6e3d-153">Minimum supported client</span></span><br/> | <span data-ttu-id="e6e3d-154">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e6e3d-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e6e3d-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e6e3d-155">Minimum supported server</span></span><br/> | <span data-ttu-id="e6e3d-156">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e6e3d-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e6e3d-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6e3d-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6e3d-158"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6e3d-158"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e6e3d-159">Libreria</span><span class="sxs-lookup"><span data-stu-id="e6e3d-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="e6e3d-160"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6e3d-160"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e6e3d-161">DLL</span><span class="sxs-lookup"><span data-stu-id="e6e3d-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6e3d-162"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6e3d-162"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6e3d-163">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6e3d-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6e3d-164">**glColorMaterial**</span><span class="sxs-lookup"><span data-stu-id="e6e3d-164">**glColorMaterial**</span></span>](glcolormaterial.md)
</dt> <dt>

[<span data-ttu-id="e6e3d-165">**glLight**</span><span class="sxs-lookup"><span data-stu-id="e6e3d-165">**glLight**</span></span>](gllight-functions.md)
</dt> <dt>

[<span data-ttu-id="e6e3d-166">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="e6e3d-166">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





