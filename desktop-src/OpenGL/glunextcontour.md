---
title: funzione gluNextContour (Glu. h)
description: La funzione gluNextContour contrassegna l'inizio di un altro contorno.
ms.assetid: 622cd631-3426-4206-9e23-af2a74343da5
keywords:
- funzione gluNextContour OpenGL
topic_type:
- apiref
api_name:
- gluNextContour
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b798eba50205053c019e3e8d1708c9ed834e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400420"
---
# <a name="glunextcontour-function"></a><span data-ttu-id="d0f57-104">gluNextContour (funzione)</span><span class="sxs-lookup"><span data-stu-id="d0f57-104">gluNextContour function</span></span>

<span data-ttu-id="d0f57-105">\[La funzione **gluNextContour** è obsoleta e viene fornita solo per compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="d0f57-105">\[The **gluNextContour** function is obsolete and is provided for backward compatibility only.</span></span> <span data-ttu-id="d0f57-106">La funzione **gluNextContour** è mappata a [**GluTessEndContour**](glutessendcontour.md) seguito da [**gluTessBeginContour**](glutessbegincontour.md).\]</span><span class="sxs-lookup"><span data-stu-id="d0f57-106">The **gluNextContour** function is mapped to [**gluTessEndContour**](glutessendcontour.md) followed by [**gluTessBeginContour**](glutessbegincontour.md).\]</span></span>

<span data-ttu-id="d0f57-107">La funzione **gluNextContour** contrassegna l'inizio di un altro contorno.</span><span class="sxs-lookup"><span data-stu-id="d0f57-107">The **gluNextContour** function marks the beginning of another contour.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0f57-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0f57-108">Syntax</span></span>


```C++
void WINAPI gluNextContour(
   GLUtesselator *tess,
   GLenum        type
);
```



## <a name="parameters"></a><span data-ttu-id="d0f57-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0f57-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0f57-110">*Tess*</span><span class="sxs-lookup"><span data-stu-id="d0f57-110">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="d0f57-111">Oggetto a mosaico creato con [**gluNewTess**](glunewtess.md).</span><span class="sxs-lookup"><span data-stu-id="d0f57-111">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d0f57-112">*type*</span><span class="sxs-lookup"><span data-stu-id="d0f57-112">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="d0f57-113">Tipo del contorno definito.</span><span class="sxs-lookup"><span data-stu-id="d0f57-113">The type of the contour being defined.</span></span> <span data-ttu-id="d0f57-114">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="d0f57-114">The following values are valid.</span></span>



| <span data-ttu-id="d0f57-115">Valore</span><span class="sxs-lookup"><span data-stu-id="d0f57-115">Value</span></span>                                                                                                                                                                | <span data-ttu-id="d0f57-116">Significato</span><span class="sxs-lookup"><span data-stu-id="d0f57-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_EXTERIOR"></span><span id="glu_exterior"></span><dl> <span data-ttu-id="d0f57-117"><dt>**GLU \_ esterno**</dt></span><span class="sxs-lookup"><span data-stu-id="d0f57-117"><dt>**GLU\_EXTERIOR**</dt></span></span> </dl>           | <span data-ttu-id="d0f57-118">Un contorno esterno definisce un limite esterno del poligono.</span><span class="sxs-lookup"><span data-stu-id="d0f57-118">An exterior contour defines an exterior boundary of the polygon.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GLU_INTERIOR"></span><span id="glu_interior"></span><dl> <span data-ttu-id="d0f57-119"><dt>**GLU \_ interno**</dt></span><span class="sxs-lookup"><span data-stu-id="d0f57-119"><dt>**GLU\_INTERIOR**</dt></span></span> </dl>           | <span data-ttu-id="d0f57-120">Un contorno interno definisce un confine interno del poligono, ad esempio un foro.</span><span class="sxs-lookup"><span data-stu-id="d0f57-120">An interior contour defines an interior boundary of the polygon (such as a hole).</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GLU_UNKNOWN"></span><span id="glu_unknown"></span><dl> <span data-ttu-id="d0f57-121"><dt>**GLU \_ sconosciuto**</dt></span><span class="sxs-lookup"><span data-stu-id="d0f57-121"><dt>**GLU\_UNKNOWN**</dt></span></span> </dl>              | <span data-ttu-id="d0f57-122">Un contorno sconosciuto viene analizzato dalla libreria per determinare se è interno o esterno.</span><span class="sxs-lookup"><span data-stu-id="d0f57-122">An unknown contour is analyzed by the library to determine whether it is interior or exterior.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CCW__GLU_CW"></span><span id="glu_ccw__glu_cw"></span><dl> <span data-ttu-id="d0f57-123"><dt>**GLU \_ CCW, Glu \_ CW**</dt></span><span class="sxs-lookup"><span data-stu-id="d0f57-123"><dt>**GLU\_CCW, GLU\_CW**</dt></span></span> </dl> | <span data-ttu-id="d0f57-124">Il primo \_ contorno Glu CCW o Glu \_ CW definito viene considerato esterno.</span><span class="sxs-lookup"><span data-stu-id="d0f57-124">The first GLU\_CCW or GLU\_CW contour defined is considered to be exterior.</span></span> <span data-ttu-id="d0f57-125">Tutti gli altri contorni sono considerati esterni se sono orientati nella stessa direzione (in senso orario o in senso antiorario) del primo contorno e, in caso contrario, interni.</span><span class="sxs-lookup"><span data-stu-id="d0f57-125">All other contours are considered to be exterior if they are oriented in the same direction (clockwise or counterclockwise) as the first contour, and interior if they are not.</span></span><br/> <span data-ttu-id="d0f57-126">Se un contorno è di tipo GLU \_ CCW o Glu \_ CW, è necessario che tutti i contorni siano dello stesso tipo. in caso contrario, tutti i \_ contorni di GLU CCW e Glu \_ CW verranno modificati in Glu \_ Unknown.</span><span class="sxs-lookup"><span data-stu-id="d0f57-126">If one contour is of type GLU\_CCW or GLU\_CW, then all contours must be of the same type (if they are not, then all GLU\_CCW and GLU\_CW contours will be changed to GLU\_UNKNOWN).</span></span> <span data-ttu-id="d0f57-127">Si noti che non esiste alcuna differenza reale tra i \_ tipi di contorno Glu CCW e Glu \_ CW.</span><span class="sxs-lookup"><span data-stu-id="d0f57-127">Note that there is no real difference between the GLU\_CCW and GLU\_CW contour types.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0f57-128">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0f57-128">Return value</span></span>

<span data-ttu-id="d0f57-129">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="d0f57-129">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0f57-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0f57-130">Remarks</span></span>

<span data-ttu-id="d0f57-131">Usare la funzione **gluNextContour** per descrivere i poligoni con più contorni.</span><span class="sxs-lookup"><span data-stu-id="d0f57-131">Use the **gluNextContour** function to describe polygons with multiple contours.</span></span> <span data-ttu-id="d0f57-132">Dopo aver descritto il primo contorno tramite una serie di chiamate [**gluTessVertex**](glutessvertex.md) , una chiamata **gluNextContour** indica che il contorno precedente è completo e che il contorno successivo sta per iniziare.</span><span class="sxs-lookup"><span data-stu-id="d0f57-132">After you describe the first contour through a series of [**gluTessVertex**](glutessvertex.md) calls, a **gluNextContour** call indicates that the previous contour is complete and that the next contour is about to begin.</span></span> <span data-ttu-id="d0f57-133">Eseguire un'altra serie di chiamate **gluTessVertex** per descrivere il nuovo contorno.</span><span class="sxs-lookup"><span data-stu-id="d0f57-133">Perform another series of **gluTessVertex** calls to describe the new contour.</span></span> <span data-ttu-id="d0f57-134">Ripetere questo processo fino a quando non sono stati descritti tutti i contorni.</span><span class="sxs-lookup"><span data-stu-id="d0f57-134">Repeat this process until all contours have been described.</span></span>

<span data-ttu-id="d0f57-135">Il parametro di *tipo* definisce il tipo di contorno che segue.</span><span class="sxs-lookup"><span data-stu-id="d0f57-135">The *type* parameter defines what type of contour follows.</span></span>

<span data-ttu-id="d0f57-136">Per definire il tipo del primo contorno, è possibile chiamare **gluNextContour** prima di descrivere il primo contorno.</span><span class="sxs-lookup"><span data-stu-id="d0f57-136">To define the type of the first contour, you can call **gluNextContour** before describing the first contour.</span></span> <span data-ttu-id="d0f57-137">Se non si chiama **gluNextContour** prima del primo contorno, il primo contorno è contrassegnato come Glu \_ esterno.</span><span class="sxs-lookup"><span data-stu-id="d0f57-137">If you do not call **gluNextContour** before the first contour, the first contour is marked GLU\_EXTERIOR.</span></span>

## <a name="examples"></a><span data-ttu-id="d0f57-138">Esempio</span><span class="sxs-lookup"><span data-stu-id="d0f57-138">Examples</span></span>

<span data-ttu-id="d0f57-139">È possibile descrivere un quadrilatero con un foro triangolare nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="d0f57-139">You can describe a quadrilateral with a triangular hole in it as follows:</span></span>

``` syntax
gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4);  
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7);  
gluEndPolygon(tess);
```

## <a name="requirements"></a><span data-ttu-id="d0f57-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0f57-140">Requirements</span></span>



| <span data-ttu-id="d0f57-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0f57-141">Requirement</span></span> | <span data-ttu-id="d0f57-142">Valore</span><span class="sxs-lookup"><span data-stu-id="d0f57-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d0f57-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0f57-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d0f57-144">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d0f57-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d0f57-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0f57-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d0f57-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d0f57-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d0f57-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0f57-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0f57-148"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0f57-148"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="d0f57-149">Libreria</span><span class="sxs-lookup"><span data-stu-id="d0f57-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="d0f57-150"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0f57-150"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d0f57-151">DLL</span><span class="sxs-lookup"><span data-stu-id="d0f57-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0f57-152"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0f57-152"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0f57-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0f57-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0f57-154">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="d0f57-154">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="d0f57-155">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="d0f57-155">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="d0f57-156">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="d0f57-156">**gluTessBeginPolygon**</span></span>](glubeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="d0f57-157">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="d0f57-157">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="d0f57-158">**gluTessEndContour**</span><span class="sxs-lookup"><span data-stu-id="d0f57-158">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="d0f57-159">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="d0f57-159">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





