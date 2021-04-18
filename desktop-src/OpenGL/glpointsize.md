---
title: funzione glPointSize (GL. h)
description: La funzione glPointSize specifica il diametro dei punti rasterizzati.
ms.assetid: efa35fa8-721a-48e5-bf59-d33b9bbe7f73
keywords:
- funzione glPointSize OpenGL
topic_type:
- apiref
api_name:
- glPointSize
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e6b9525e302cad1eb940184eb5eb83e11744bba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301795"
---
# <a name="glpointsize-function"></a><span data-ttu-id="a66da-104">glPointSize (funzione)</span><span class="sxs-lookup"><span data-stu-id="a66da-104">glPointSize function</span></span>

<span data-ttu-id="a66da-105">La funzione **glPointSize** specifica il diametro dei punti rasterizzati.</span><span class="sxs-lookup"><span data-stu-id="a66da-105">The **glPointSize** function specifies the diameter of rasterized points.</span></span>

## <a name="syntax"></a><span data-ttu-id="a66da-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a66da-106">Syntax</span></span>


```C++
void WINAPI glPointSize(
   GLfloat size
);
```



## <a name="parameters"></a><span data-ttu-id="a66da-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a66da-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a66da-108">*size*</span><span class="sxs-lookup"><span data-stu-id="a66da-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="a66da-109">Diametro dei punti rasterizzati.</span><span class="sxs-lookup"><span data-stu-id="a66da-109">The diameter of rasterized points.</span></span> <span data-ttu-id="a66da-110">Il valore predefinito è 1,0.</span><span class="sxs-lookup"><span data-stu-id="a66da-110">The default is 1.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a66da-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a66da-111">Return value</span></span>

<span data-ttu-id="a66da-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="a66da-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a66da-113">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a66da-113">Error codes</span></span>

<span data-ttu-id="a66da-114">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="a66da-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a66da-115">Nome</span><span class="sxs-lookup"><span data-stu-id="a66da-115">Name</span></span>                                                                                                  | <span data-ttu-id="a66da-116">Significato</span><span class="sxs-lookup"><span data-stu-id="a66da-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a66da-117"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a66da-117"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="a66da-118">*dimensioni* minori o uguali a zero.</span><span class="sxs-lookup"><span data-stu-id="a66da-118">*size* was less than or equal to zero.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="a66da-119"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a66da-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a66da-120">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a66da-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a66da-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="a66da-121">Remarks</span></span>

<span data-ttu-id="a66da-122">La funzione **glPointSize** specifica il diametro rasterizzato dei punti con alias e con alias.</span><span class="sxs-lookup"><span data-stu-id="a66da-122">The **glPointSize** function specifies the rasterized diameter of both aliased and antialiased points.</span></span> <span data-ttu-id="a66da-123">L'uso di una dimensione del punto diversa da 1,0 ha effetti diversi, a seconda che sia abilitato l'anti-aliasing del punto.</span><span class="sxs-lookup"><span data-stu-id="a66da-123">Using a point size other than 1.0 has different effects, depending on whether point antialiasing is enabled.</span></span> <span data-ttu-id="a66da-124">L'anti-aliasing del punto viene controllato chiamando [**glEnable**](glenable.md) e **glDisable** con l'argomento GL \_ Point \_ Smooth.</span><span class="sxs-lookup"><span data-stu-id="a66da-124">Point antialiasing is controlled by calling [**glEnable**](glenable.md) and **glDisable** with argument GL\_POINT\_SMOOTH.</span></span>

<span data-ttu-id="a66da-125">Se l'anti-aliasing del punto è disabilitato, le dimensioni effettive vengono determinate mediante l'arrotondamento della dimensione fornita all'intero più vicino.</span><span class="sxs-lookup"><span data-stu-id="a66da-125">If point antialiasing is disabled, the actual size is determined by rounding the supplied size to the nearest integer.</span></span> <span data-ttu-id="a66da-126">Se l'arrotondamento restituisce il valore 0, è come se la dimensione del punto fosse 1. Se le dimensioni arrotondate sono dispari, il punto centrale (*x*,*y*) del frammento di pixel che rappresenta il punto viene calcolato come</span><span class="sxs-lookup"><span data-stu-id="a66da-126">(If the rounding results in the value 0, it is as if the point size were 1.) If the rounded size is odd, then the center point (*x*,*y*) of the pixel fragment that represents the point is computed as</span></span>

<span data-ttu-id="a66da-127">(*x*<sub>w</sub> + 0,5, *y*<sub>w</sub> +. 5)</span><span class="sxs-lookup"><span data-stu-id="a66da-127">(*x*<sub>w</sub> + .5, *y*<sub>w</sub> + .5)</span></span>

<span data-ttu-id="a66da-128">dove gli indici *w* indicano le coordinate della finestra.</span><span class="sxs-lookup"><span data-stu-id="a66da-128">where *w* subscripts indicate window coordinates.</span></span> <span data-ttu-id="a66da-129">Tutti i pixel che si trovano all'interno della griglia quadrata della dimensione arrotondata al centro, ovvero *x*,*y*, costituiscono il frammento.</span><span class="sxs-lookup"><span data-stu-id="a66da-129">All pixels that lie within the square grid of the rounded size centered at (*x*,*y*) make up the fragment.</span></span> <span data-ttu-id="a66da-130">Se le dimensioni sono pari, il punto centrale è</span><span class="sxs-lookup"><span data-stu-id="a66da-130">If the size is even, the center point is</span></span>

<span data-ttu-id="a66da-131">(*x*<sub>w</sub> + 0,5, *y*<sub>w</sub> +. 5)</span><span class="sxs-lookup"><span data-stu-id="a66da-131">(*x*<sub>w</sub> + .5, *y*<sub>w</sub> + .5)</span></span>

<span data-ttu-id="a66da-132">e i centri dei frammenti rasterizzati sono le coordinate della finestra a metà Integer all'interno del quadrato della dimensione arrotondata al centro in corrispondenza di (*x*,*y*).</span><span class="sxs-lookup"><span data-stu-id="a66da-132">and the rasterized fragment's centers are the half-integer window coordinates within the square of the rounded size centered at (*x*,*y*).</span></span> <span data-ttu-id="a66da-133">A tutti i frammenti di pixel prodotti nella rasterizzazione di un punto nonantialiased vengono assegnati gli stessi dati associati; oggetto del vertice che corrisponde al punto.</span><span class="sxs-lookup"><span data-stu-id="a66da-133">All pixel fragments produced in rasterizing a nonantialiased point are assigned the same associated data; that of the vertex corresponding to the point.</span></span>

<span data-ttu-id="a66da-134">Se l'anti-aliasing è abilitato, la rasterizzazione dei punti produce un frammento per ogni quadrato di pixel che interseca l'area che si trova all'interno del cerchio con diametro uguale alle dimensioni del punto corrente e centrato ai punti (*x*<sub>w</sub> ,*y*<sub>w</sub> ).</span><span class="sxs-lookup"><span data-stu-id="a66da-134">If antialiasing is enabled, then point rasterization produces a fragment for each pixel square that intersects the region lying within the circle having diameter equal to the current point size and centered at the points (*x*<sub>w</sub> ,*y*<sub>w</sub> ).</span></span> <span data-ttu-id="a66da-135">Il valore di code coverage per ogni frammento è l'area delle coordinate della finestra dell'intersezione dell'area circolare con il quadrato pixel corrispondente.</span><span class="sxs-lookup"><span data-stu-id="a66da-135">The coverage value for each fragment is the window coordinate area of the intersection of the circular region with the corresponding pixel square.</span></span> <span data-ttu-id="a66da-136">Questo valore viene salvato e utilizzato nel passaggio di rasterizzazione finale.</span><span class="sxs-lookup"><span data-stu-id="a66da-136">This value is saved and used in the final rasterization step.</span></span> <span data-ttu-id="a66da-137">I dati associati a ogni frammento sono i dati associati al punto che si sta rasterizzando.</span><span class="sxs-lookup"><span data-stu-id="a66da-137">The data associated with each fragment is the data associated with the point being rasterized.</span></span>

<span data-ttu-id="a66da-138">Quando l'anti-aliasing del punto è abilitato, non sono supportate tutte le dimensioni.</span><span class="sxs-lookup"><span data-stu-id="a66da-138">Not all sizes are supported when point antialiasing is enabled.</span></span> <span data-ttu-id="a66da-139">Se viene richiesta una dimensione non supportata, vengono usate le dimensioni più vicine supportate.</span><span class="sxs-lookup"><span data-stu-id="a66da-139">If an unsupported size is requested, the nearest supported size is used.</span></span> <span data-ttu-id="a66da-140">È garantita la garanzia che siano supportate solo le dimensioni 1,0; altre dipendono dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="a66da-140">Only size 1.0 is guaranteed to be supported; others depend on the implementation.</span></span> <span data-ttu-id="a66da-141">È possibile eseguire una query sull'intervallo di dimensioni supportate e sulla differenza di dimensioni tra le dimensioni supportate nell'intervallo chiamando [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con gli argomenti \_ intervallo di dimensioni del punto GL \_ \_ e \_ granularità delle dimensioni del punto GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a66da-141">The range of supported sizes and the size difference between supported sizes within the range can be queried by calling [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with arguments GL\_POINT\_SIZE\_RANGE and GL\_POINT\_SIZE\_GRANULARITY.</span></span>

<span data-ttu-id="a66da-142">La dimensione in punti specificata da **glPointSize** viene sempre restituita \_ quando \_ viene eseguita una query sulle dimensioni del punto GL.</span><span class="sxs-lookup"><span data-stu-id="a66da-142">The point size specified by **glPointSize** is always returned when GL\_POINT\_SIZE is queried.</span></span> <span data-ttu-id="a66da-143">Il bloccaggio e l'arrotondamento per i punti con alias e con alias non hanno effetto sul valore specificato.</span><span class="sxs-lookup"><span data-stu-id="a66da-143">Clamping and rounding for aliased and antialiased points have no effect on the specified value.</span></span>

<span data-ttu-id="a66da-144">Le dimensioni del punto non con alias possono essere fissate a un valore massimo dipendente dall'implementazione.</span><span class="sxs-lookup"><span data-stu-id="a66da-144">Non-antialiased point size may be clamped to an implementation-dependent maximum.</span></span> <span data-ttu-id="a66da-145">Sebbene non sia possibile eseguire query su questo valore massimo, il valore non deve essere minore del valore massimo per i punti con alias, arrotondato al valore intero più vicino.</span><span class="sxs-lookup"><span data-stu-id="a66da-145">Although this maximum cannot be queried, it must be no less than the maximum value for antialiased points, rounded to the nearest integer value.</span></span>

<span data-ttu-id="a66da-146">Le funzioni seguenti consentono di recuperare informazioni correlate a **glPointSize**:</span><span class="sxs-lookup"><span data-stu-id="a66da-146">The following functions retrieve information related to **glPointSize**:</span></span>

<span data-ttu-id="a66da-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con \_ dimensione punto GL \_ argomento</span><span class="sxs-lookup"><span data-stu-id="a66da-147">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POINT\_SIZE</span></span>

<span data-ttu-id="a66da-148">**glGet** con intervallo di \_ dimensioni punti GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="a66da-148">**glGet** with argument GL\_POINT\_SIZE\_RANGE</span></span>

<span data-ttu-id="a66da-149">**glGet** con \_ \_ granularità delle dimensioni dei punti GL degli argomenti \_</span><span class="sxs-lookup"><span data-stu-id="a66da-149">**glGet** with argument GL\_POINT\_SIZE\_GRANULARITY</span></span>

<span data-ttu-id="a66da-150">[**glIsEnabled**](glisenabled.md) con l'argomento \_ punto GL \_ smussato</span><span class="sxs-lookup"><span data-stu-id="a66da-150">[**glIsEnabled**](glisenabled.md) with argument GL\_POINT\_SMOOTH</span></span>

## <a name="requirements"></a><span data-ttu-id="a66da-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a66da-151">Requirements</span></span>



| <span data-ttu-id="a66da-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="a66da-152">Requirement</span></span> | <span data-ttu-id="a66da-153">Valore</span><span class="sxs-lookup"><span data-stu-id="a66da-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a66da-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a66da-154">Minimum supported client</span></span><br/> | <span data-ttu-id="a66da-155">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a66da-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a66da-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a66da-156">Minimum supported server</span></span><br/> | <span data-ttu-id="a66da-157">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a66da-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a66da-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a66da-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="a66da-159"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a66da-159"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a66da-160">Libreria</span><span class="sxs-lookup"><span data-stu-id="a66da-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="a66da-161"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a66da-161"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a66da-162">DLL</span><span class="sxs-lookup"><span data-stu-id="a66da-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a66da-163"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a66da-163"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a66da-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a66da-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a66da-165">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a66da-165">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a66da-166">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="a66da-166">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="a66da-167">**Remo**</span><span class="sxs-lookup"><span data-stu-id="a66da-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a66da-168">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="a66da-168">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





