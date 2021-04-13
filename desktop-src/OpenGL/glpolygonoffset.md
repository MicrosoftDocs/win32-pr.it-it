---
title: funzione glPolygonOffset (GL. h)
description: La funzione glPolygonOffset imposta la scala e le unità che OpenGL USA per calcolare i valori di profondità.
ms.assetid: 06bc1aba-1692-40f0-8535-2cb65b487490
keywords:
- funzione glPolygonOffset OpenGL
topic_type:
- apiref
api_name:
- glPolygonOffset
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84fa7d130fcc300fc1ebe33d091253e33f2d1e03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400701"
---
# <a name="glpolygonoffset-function"></a><span data-ttu-id="92b94-104">glPolygonOffset (funzione)</span><span class="sxs-lookup"><span data-stu-id="92b94-104">glPolygonOffset function</span></span>

<span data-ttu-id="92b94-105">La funzione **glPolygonOffset** imposta la scala e le unità che OpenGL USA per calcolare i valori di profondità.</span><span class="sxs-lookup"><span data-stu-id="92b94-105">The **glPolygonOffset** function sets the scale and units OpenGL uses to calculate depth values.</span></span>

## <a name="syntax"></a><span data-ttu-id="92b94-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="92b94-106">Syntax</span></span>


```C++
void WINAPI glPolygonOffset(
   GLfloat factor,
   GLfloat units
);
```



## <a name="parameters"></a><span data-ttu-id="92b94-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="92b94-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92b94-108">*Factor*</span><span class="sxs-lookup"><span data-stu-id="92b94-108">*factor*</span></span> 
</dt> <dd>

<span data-ttu-id="92b94-109">Specifica un fattore di scala utilizzato per creare un offset della profondità della variabile per ogni poligono.</span><span class="sxs-lookup"><span data-stu-id="92b94-109">Specifies a scale factor that is used to create a variable depth offset for each polygon.</span></span> <span data-ttu-id="92b94-110">Il valore iniziale è zero.</span><span class="sxs-lookup"><span data-stu-id="92b94-110">The initial value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="92b94-111">*unità*</span><span class="sxs-lookup"><span data-stu-id="92b94-111">*units*</span></span> 
</dt> <dd>

<span data-ttu-id="92b94-112">Specifica un valore moltiplicato per un valore specifico dell'implementazione per creare un offset di profondità costante.</span><span class="sxs-lookup"><span data-stu-id="92b94-112">Specifies a value that is multiplied by an implementation-specific value to create a constant depth offset.</span></span> <span data-ttu-id="92b94-113">Il valore iniziale è 0.</span><span class="sxs-lookup"><span data-stu-id="92b94-113">The initial value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92b94-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="92b94-114">Return value</span></span>

<span data-ttu-id="92b94-115">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="92b94-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="92b94-116">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="92b94-116">Error codes</span></span>

<span data-ttu-id="92b94-117">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="92b94-117">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="92b94-118">Nome</span><span class="sxs-lookup"><span data-stu-id="92b94-118">Name</span></span>                                                                                                  | <span data-ttu-id="92b94-119">Significato</span><span class="sxs-lookup"><span data-stu-id="92b94-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="92b94-120"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="92b94-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="92b94-121">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="92b94-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="92b94-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="92b94-122">Remarks</span></span>

<span data-ttu-id="92b94-123">Quando l' \_ offset del poligono GL \_ è abilitato, il valore di profondità di ogni frammento verrà sfalsato dopo l'interpolazione tra i valori di profondità dei vertici appropriati.</span><span class="sxs-lookup"><span data-stu-id="92b94-123">When GL\_POLYGON\_OFFSET is enabled, each fragment's depth value will be offset after it is interpolated from the depth values of the appropriate vertices.</span></span> <span data-ttu-id="92b94-124">Il valore dell'offset è *Factor* \* ? z + r \* *Units*, dove? z è una misurazione della variazione di profondità rispetto all'area dello schermo del poligono e r è il valore più piccolo garantito per produrre un offset risolvibile per una determinata implementazione.</span><span class="sxs-lookup"><span data-stu-id="92b94-124">The value of the offset is *factor* \* ?z + r \**units*, where ?z is a measurement of the change in depth relative to the screen area of the polygon, and r is the smallest value that is guaranteed to produce a resolvable offset for a given implementation.</span></span> <span data-ttu-id="92b94-125">L'offset viene aggiunto prima che il test di profondità venga eseguito e prima che il valore venga scritto nel buffer di profondità.</span><span class="sxs-lookup"><span data-stu-id="92b94-125">The offset is added before the depth test is performed and before the value is written into the depth buffer.</span></span>

<span data-ttu-id="92b94-126">La funzione **glPolygonOffset** è utile per il rendering di immagini a linee nascoste, per l'applicazione di decalcomanie alle superfici e per il rendering di solidi con bordi evidenziati.</span><span class="sxs-lookup"><span data-stu-id="92b94-126">The **glPolygonOffset** function is useful for rendering hidden-line images, for applying decals to surfaces, and for rendering solids with highlighted edges.</span></span>

<span data-ttu-id="92b94-127">La funzione **glPolygonOffset** non ha effetto sulle coordinate di profondità inserite nel buffer di feedback.</span><span class="sxs-lookup"><span data-stu-id="92b94-127">The **glPolygonOffset** function has no effect on depth coordinates placed in the feedback buffer.</span></span> <span data-ttu-id="92b94-128">Inoltre, non ha alcun effetto sulla selezione.</span><span class="sxs-lookup"><span data-stu-id="92b94-128">It also has no effect on selection.</span></span>

<span data-ttu-id="92b94-129">Le funzioni seguenti consentono di recuperare informazioni correlate a **glPolygonOffset**:</span><span class="sxs-lookup"><span data-stu-id="92b94-129">The following functions retrieve information related to **glPolygonOffset**:</span></span>

-   <span data-ttu-id="92b94-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con \_ \_ fattore offset poligono \_ GL</span><span class="sxs-lookup"><span data-stu-id="92b94-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POLYGON\_OFFSET\_FACTOR</span></span>
-   <span data-ttu-id="92b94-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con l'argomento \_ \_ unità di offset poligono GL \_</span><span class="sxs-lookup"><span data-stu-id="92b94-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_POLYGON\_OFFSET\_UNITS</span></span>
-   <span data-ttu-id="92b94-132">[**glIsEnabled**](glisenabled.md) con \_ \_ riempimento offset poligono \_ GL</span><span class="sxs-lookup"><span data-stu-id="92b94-132">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_OFFSET\_FILL</span></span>
-   <span data-ttu-id="92b94-133">[**glIsEnabled**](glisenabled.md) con argomento \_ linea di \_ offset poligono GL \_</span><span class="sxs-lookup"><span data-stu-id="92b94-133">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_OFFSET\_LINE</span></span>
-   <span data-ttu-id="92b94-134">[**glIsEnabled**](glisenabled.md) con punto di \_ offset del poligono GL argomento \_ \_</span><span class="sxs-lookup"><span data-stu-id="92b94-134">[**glIsEnabled**](glisenabled.md) with argument GL\_POLYGON\_OFFSET\_POINT</span></span>

> [!Note]  
> <span data-ttu-id="92b94-135">La funzione **glPolygonOffset** è disponibile solo in OpenGl versione 1,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="92b94-135">The **glPolygonOffset** function is only available in OpenGl version 1.1 or greater.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="92b94-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="92b94-136">Requirements</span></span>



| <span data-ttu-id="92b94-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="92b94-137">Requirement</span></span> | <span data-ttu-id="92b94-138">Valore</span><span class="sxs-lookup"><span data-stu-id="92b94-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92b94-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92b94-139">Minimum supported client</span></span><br/> | <span data-ttu-id="92b94-140">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="92b94-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="92b94-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="92b94-141">Minimum supported server</span></span><br/> | <span data-ttu-id="92b94-142">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="92b94-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="92b94-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="92b94-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="92b94-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="92b94-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="92b94-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="92b94-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="92b94-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92b94-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="92b94-147">DLL</span><span class="sxs-lookup"><span data-stu-id="92b94-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92b94-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92b94-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92b94-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="92b94-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92b94-150">**glDepthFunc**</span><span class="sxs-lookup"><span data-stu-id="92b94-150">**glDepthFunc**</span></span>](gldepthfunc.md)
</dt> <dt>

[<span data-ttu-id="92b94-151">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="92b94-151">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="92b94-152">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="92b94-152">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="92b94-153">**glGet**</span><span class="sxs-lookup"><span data-stu-id="92b94-153">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="92b94-154">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="92b94-154">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="92b94-155">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="92b94-155">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="92b94-156">**glStencilOp**</span><span class="sxs-lookup"><span data-stu-id="92b94-156">**glStencilOp**</span></span>](glstencilop.md)
</dt> <dt>

[<span data-ttu-id="92b94-157">**glTexEnv**</span><span class="sxs-lookup"><span data-stu-id="92b94-157">**glTexEnv**</span></span>](gltexenv-functions.md)
</dt> </dl>

 

 





