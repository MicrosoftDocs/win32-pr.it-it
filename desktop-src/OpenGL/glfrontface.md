---
title: funzione glFrontFace (GL. h)
description: La funzione glFrontFace definisce i poligoni di fronte e indietro.
ms.assetid: 4087107c-99cd-4c26-92e3-8dc43633d51f
keywords:
- funzione glFrontFace OpenGL
topic_type:
- apiref
api_name:
- glFrontFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 106fa40989f21e50eb738f1a218394e8e7e9b4bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964911"
---
# <a name="glfrontface-function"></a><span data-ttu-id="45809-104">glFrontFace (funzione)</span><span class="sxs-lookup"><span data-stu-id="45809-104">glFrontFace function</span></span>

<span data-ttu-id="45809-105">La funzione **glFrontFace** definisce i poligoni di fronte e indietro.</span><span class="sxs-lookup"><span data-stu-id="45809-105">The **glFrontFace** function defines front-facing and back-facing polygons.</span></span>

## <a name="syntax"></a><span data-ttu-id="45809-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45809-106">Syntax</span></span>


```C++
void WINAPI glFrontFace(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="45809-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="45809-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45809-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="45809-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="45809-109">Orientamento dei poligoni in primo piano.</span><span class="sxs-lookup"><span data-stu-id="45809-109">The orientation of front-facing polygons.</span></span> <span data-ttu-id="45809-110">GL \_ CW e GL \_ CCW sono accettati.</span><span class="sxs-lookup"><span data-stu-id="45809-110">GL\_CW and GL\_CCW are accepted.</span></span> <span data-ttu-id="45809-111">Il valore predefinito è GL \_ CCW.</span><span class="sxs-lookup"><span data-stu-id="45809-111">The default value is GL\_CCW.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45809-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45809-112">Return value</span></span>

<span data-ttu-id="45809-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="45809-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="45809-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="45809-114">Error codes</span></span>

<span data-ttu-id="45809-115">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="45809-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="45809-116">Nome</span><span class="sxs-lookup"><span data-stu-id="45809-116">Name</span></span>                                                                                                  | <span data-ttu-id="45809-117">Significato</span><span class="sxs-lookup"><span data-stu-id="45809-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="45809-118"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="45809-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="45809-119">la *modalità* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="45809-119">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="45809-120"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="45809-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="45809-121">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="45809-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="45809-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="45809-122">Remarks</span></span>

<span data-ttu-id="45809-123">In una scena composta interamente da superfici chiuse opache, i poligoni di back-end non sono mai visibili.</span><span class="sxs-lookup"><span data-stu-id="45809-123">In a scene composed entirely of opaque closed surfaces, back-facing polygons are never visible.</span></span> <span data-ttu-id="45809-124">Eliminando questi poligoni invisibili si ha il vantaggio evidente di velocizzare il rendering dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="45809-124">Eliminating these invisible polygons has the obvious benefit of speeding up the rendering of the image.</span></span> <span data-ttu-id="45809-125">È possibile abilitare e disabilitare l'eliminazione di poligoni di back-end con [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) usando la superficie di selezione dell'argomento GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="45809-125">You enable and disable elimination of back-facing polygons with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) using argument GL\_CULL\_FACE.</span></span>

<span data-ttu-id="45809-126">La proiezione di un poligono per le coordinate della finestra viene definita in senso orario se un oggetto immaginario che segue il percorso dal primo vertice, il secondo vertice e così via, fino all'ultimo vertice e infine al primo vertice, si sposta in senso orario sull'interno del poligono.</span><span class="sxs-lookup"><span data-stu-id="45809-126">The projection of a polygon to window coordinates is said to have clockwise winding if an imaginary object following the path from its first vertex, its second vertex, and so on, to its last vertex, and finally back to its first vertex, moves in a clockwise direction about the interior of the polygon.</span></span> <span data-ttu-id="45809-127">La chiusura del poligono viene definita in senso antiorario se l'oggetto immaginario che segue lo stesso percorso si sposta in senso antiorario sull'interno del poligono.</span><span class="sxs-lookup"><span data-stu-id="45809-127">The polygon's winding is said to be counterclockwise if the imaginary object following the same path moves in a counterclockwise direction about the interior of the polygon.</span></span> <span data-ttu-id="45809-128">La funzione **glFrontFace** specifica se i poligoni con avvolgimento in senso orario nelle coordinate della finestra o in senso antiorario nelle coordinate della finestra vengono portati in primo piano.</span><span class="sxs-lookup"><span data-stu-id="45809-128">The **glFrontFace** function specifies whether polygons with clockwise winding in window coordinates, or counterclockwise winding in window coordinates, are taken to be front-facing.</span></span> <span data-ttu-id="45809-129">Passando GL \_ CCW alla *modalità* , vengono selezionati i poligoni in senso antiorario come front-end; GL \_ CW seleziona i poligoni in senso orario come front-end.</span><span class="sxs-lookup"><span data-stu-id="45809-129">Passing GL\_CCW to *mode* selects counterclockwise polygons as front-facing; GL\_CW selects clockwise polygons as front-facing.</span></span> <span data-ttu-id="45809-130">Per impostazione predefinita, i poligoni in senso antiorario vengono considerati front-end.</span><span class="sxs-lookup"><span data-stu-id="45809-130">By default, counterclockwise polygons are taken to be front-facing.</span></span>

<span data-ttu-id="45809-131">La funzione seguente recupera informazioni su **glFrontface**:</span><span class="sxs-lookup"><span data-stu-id="45809-131">The following function retrieves information about **glFrontface**:</span></span>

<span data-ttu-id="45809-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con front-end GL argomento \_ \_</span><span class="sxs-lookup"><span data-stu-id="45809-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_FRONT\_FACE</span></span>

## <a name="requirements"></a><span data-ttu-id="45809-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45809-133">Requirements</span></span>



| <span data-ttu-id="45809-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="45809-134">Requirement</span></span> | <span data-ttu-id="45809-135">Valore</span><span class="sxs-lookup"><span data-stu-id="45809-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45809-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45809-136">Minimum supported client</span></span><br/> | <span data-ttu-id="45809-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="45809-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="45809-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45809-138">Minimum supported server</span></span><br/> | <span data-ttu-id="45809-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="45809-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="45809-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="45809-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="45809-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="45809-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="45809-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="45809-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="45809-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45809-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="45809-144">DLL</span><span class="sxs-lookup"><span data-stu-id="45809-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45809-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45809-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45809-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45809-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45809-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="45809-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="45809-148">**glCullFace**</span><span class="sxs-lookup"><span data-stu-id="45809-148">**glCullFace**</span></span>](glcullface.md)
</dt> <dt>

[<span data-ttu-id="45809-149">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="45809-149">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="45809-150">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="45809-150">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="45809-151">**Remo**</span><span class="sxs-lookup"><span data-stu-id="45809-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="45809-152">**glGet**</span><span class="sxs-lookup"><span data-stu-id="45809-152">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="45809-153">**glLightModel**</span><span class="sxs-lookup"><span data-stu-id="45809-153">**glLightModel**</span></span>](gllightmodel-functions.md)
</dt> </dl>

 

 





