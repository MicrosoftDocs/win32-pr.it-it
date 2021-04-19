---
title: funzione gluBeginPolygon (Glu. h)
description: Le funzioni gluBeginPolygon e gluEndPolygon delimitano una descrizione del poligono. | funzione gluBeginPolygon (Glu. h)
ms.assetid: e4da731c-2082-4dbc-ae3a-8d6b30d50253
keywords:
- funzione gluBeginPolygon OpenGL
topic_type:
- apiref
api_name:
- gluBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60204e7d937b4686f3757b520c820886e168529e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321402"
---
# <a name="glubeginpolygon-function"></a><span data-ttu-id="d95fc-105">gluBeginPolygon (funzione)</span><span class="sxs-lookup"><span data-stu-id="d95fc-105">gluBeginPolygon function</span></span>

<span data-ttu-id="d95fc-106">\[La funzione **gluBeginPolygon** è obsoleta e viene fornita solo per compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="d95fc-106">\[The **gluBeginPolygon** function is obsolete and is provided for backward compatibility only.</span></span> <span data-ttu-id="d95fc-107">La funzione **gluBeginPolygon** è mappata a [**GluTessBeginPolygon**](glutessbeginpolygon.md) seguito da [**gluTessBeginContour**](glutessbegincontour.md).\]</span><span class="sxs-lookup"><span data-stu-id="d95fc-107">The **gluBeginPolygon** function is mapped to [**gluTessBeginPolygon**](glutessbeginpolygon.md) followed by [**gluTessBeginContour**](glutessbegincontour.md).\]</span></span>

<span data-ttu-id="d95fc-108">Le funzioni **gluBeginPolygon** e [**gluEndPolygon**](gluendpolygon.md) delimitano una descrizione del poligono.</span><span class="sxs-lookup"><span data-stu-id="d95fc-108">The **gluBeginPolygon** and [**gluEndPolygon**](gluendpolygon.md) functions delimit a polygon description.</span></span>

## <a name="syntax"></a><span data-ttu-id="d95fc-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d95fc-109">Syntax</span></span>


```C++
void WINAPI gluBeginPolygon(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="d95fc-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d95fc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d95fc-111">*Tess*</span><span class="sxs-lookup"><span data-stu-id="d95fc-111">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="d95fc-112">Oggetto a mosaico creato con [**gluNewTess**](glunewtess.md).</span><span class="sxs-lookup"><span data-stu-id="d95fc-112">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d95fc-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d95fc-113">Return value</span></span>

<span data-ttu-id="d95fc-114">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="d95fc-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d95fc-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d95fc-115">Remarks</span></span>

<span data-ttu-id="d95fc-116">Usare **gluBeginPolygon** e **gluEndPolygon** per delimitare la definizione di un poligono non convesso.</span><span class="sxs-lookup"><span data-stu-id="d95fc-116">Use **gluBeginPolygon** and **gluEndPolygon** to delimit the definition of a nonconvex polygon.</span></span>

1.  <span data-ttu-id="d95fc-117">Chiamare **gluBeginPolygon**.</span><span class="sxs-lookup"><span data-stu-id="d95fc-117">Call **gluBeginPolygon**.</span></span>
2.  <span data-ttu-id="d95fc-118">Definire i contorni del poligono chiamando [**gluTessVertex**](glutessvertex.md) per ogni vertice e [**gluNextContour**](glunextcontour.md) per avviare ogni nuovo contorno.</span><span class="sxs-lookup"><span data-stu-id="d95fc-118">Define the contours of the polygon by calling [**gluTessVertex**](glutessvertex.md) for each vertex and [**gluNextContour**](glunextcontour.md) to start each new contour.</span></span>
3.  <span data-ttu-id="d95fc-119">Chiamare **gluEndPolygon** per segnalare la fine della definizione.</span><span class="sxs-lookup"><span data-stu-id="d95fc-119">Call **gluEndPolygon** to signal the end of the definition.</span></span>

    <span data-ttu-id="d95fc-120">Una volta chiamato **gluEndPolygon** , il poligono è tassellati e i triangoli risultanti vengono descritti tramite callback.</span><span class="sxs-lookup"><span data-stu-id="d95fc-120">Once **gluEndPolygon** is called, the polygon is tessellated, and the resulting triangles are described through callbacks.</span></span> <span data-ttu-id="d95fc-121">Per le descrizioni delle funzioni di callback, vedere [*gluTessCallback*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="d95fc-121">For descriptions of the callback functions, see [*gluTessCallback*](glutess.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d95fc-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="d95fc-122">Examples</span></span>

<span data-ttu-id="d95fc-123">L'esempio seguente descrive un quadrilatero con un foro triangolare:</span><span class="sxs-lookup"><span data-stu-id="d95fc-123">The following example describes a quadrilateral with a triangular hole:</span></span>

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

## <a name="requirements"></a><span data-ttu-id="d95fc-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d95fc-124">Requirements</span></span>



| <span data-ttu-id="d95fc-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="d95fc-125">Requirement</span></span> | <span data-ttu-id="d95fc-126">Valore</span><span class="sxs-lookup"><span data-stu-id="d95fc-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d95fc-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d95fc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d95fc-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d95fc-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d95fc-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d95fc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d95fc-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d95fc-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d95fc-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d95fc-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d95fc-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="d95fc-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="d95fc-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="d95fc-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="d95fc-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d95fc-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d95fc-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d95fc-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d95fc-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d95fc-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d95fc-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d95fc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d95fc-138">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="d95fc-138">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="d95fc-139">**gluNextContour**</span><span class="sxs-lookup"><span data-stu-id="d95fc-139">**gluNextContour**</span></span>](glunextcontour.md)
</dt> <dt>

[<span data-ttu-id="d95fc-140">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="d95fc-140">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="d95fc-141">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="d95fc-141">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="d95fc-142">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="d95fc-142">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="d95fc-143">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="d95fc-143">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





