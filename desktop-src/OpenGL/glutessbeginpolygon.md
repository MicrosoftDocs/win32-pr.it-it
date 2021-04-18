---
title: funzione gluTessBeginPolygon (Glu. h)
description: Le funzioni gluTessBeginPolygon e gluTessEndPolygon delimitano una descrizione del poligono. | funzione gluTessBeginPolygon (Glu. h)
ms.assetid: 3a04363a-c492-4fa5-b312-f2fa2a805782
keywords:
- funzione gluTessBeginPolygon OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34fad4c620890df109449b9a222d3355041ac77f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321737"
---
# <a name="glutessbeginpolygon-function"></a><span data-ttu-id="1737f-105">gluTessBeginPolygon (funzione)</span><span class="sxs-lookup"><span data-stu-id="1737f-105">gluTessBeginPolygon function</span></span>

<span data-ttu-id="1737f-106">Le funzioni **gluTessBeginPolygon** e [**gluTessEndPolygon**](glutessendpolygon.md) delimitano una descrizione del poligono.</span><span class="sxs-lookup"><span data-stu-id="1737f-106">The **gluTessBeginPolygon** and [**gluTessEndPolygon**](glutessendpolygon.md) functions delimit a polygon description.</span></span>

## <a name="syntax"></a><span data-ttu-id="1737f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1737f-107">Syntax</span></span>


```C++
void WINAPI gluTessBeginPolygon(
   GLUtesselator *tess,
   void          *polygon_data
);
```



## <a name="parameters"></a><span data-ttu-id="1737f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1737f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1737f-109">*Tess*</span><span class="sxs-lookup"><span data-stu-id="1737f-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="1737f-110">Oggetto a mosaico creato con [**gluNewTess**](glunewtess.md).</span><span class="sxs-lookup"><span data-stu-id="1737f-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="1737f-111">*\_dati Polygon*</span><span class="sxs-lookup"><span data-stu-id="1737f-111">*polygon\_data*</span></span> 
</dt> <dd>

<span data-ttu-id="1737f-112">Puntatore a una struttura di dati poligono definita dal programmatore.</span><span class="sxs-lookup"><span data-stu-id="1737f-112">A pointer to a programmer-defined polygon data structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1737f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1737f-113">Return value</span></span>

<span data-ttu-id="1737f-114">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="1737f-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1737f-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="1737f-115">Remarks</span></span>

<span data-ttu-id="1737f-116">Le funzioni **gluTessBeginPolygon** e [**gluTessEndPolygon**](glutessendpolygon.md) delimitano la definizione di un poligono non convesso.</span><span class="sxs-lookup"><span data-stu-id="1737f-116">The **gluTessBeginPolygon** and [**gluTessEndPolygon**](glutessendpolygon.md) functions delimit the definition of a nonconvex polygon.</span></span> <span data-ttu-id="1737f-117">All'interno di ogni coppia **gluTessBeginPolygon**  /  **gluTessEndPolygon** , includere una o più chiamate a [**gluTessBeginContour**](glutessbegincontour.md).</span><span class="sxs-lookup"><span data-stu-id="1737f-117">Within each **gluTessBeginPolygon** / **gluTessEndPolygon** pair, include one or more calls to [**gluTessBeginContour**](glutessbegincontour.md).</span></span> <span data-ttu-id="1737f-118">All'interno di ogni contorno sono presenti zero o più chiamate a [**gluTessVertex**](glutessvertex.md).</span><span class="sxs-lookup"><span data-stu-id="1737f-118">Within each contour, there are zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="1737f-119">I vertici specificano un contorno chiuso (l'ultimo vertice di ogni contorno viene automaticamente collegato al primo).</span><span class="sxs-lookup"><span data-stu-id="1737f-119">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span>

<span data-ttu-id="1737f-120">Il parametro di *\_ dati Polygon* è un puntatore a una struttura di dati definita dal programmatore.</span><span class="sxs-lookup"><span data-stu-id="1737f-120">The *polygon\_data* parameter is a pointer to a programmer-defined data structure.</span></span> <span data-ttu-id="1737f-121">Se vengono specificati i callback appropriati (vedere [*gluTessCallback*](glutess.md)), questo puntatore viene restituito alla funzione o alle funzioni di callback, rendendolo un modo pratico per archiviare le informazioni per poligono.</span><span class="sxs-lookup"><span data-stu-id="1737f-121">If the appropriate callbacks are specified (see [*gluTessCallback*](glutess.md)), this pointer is returned to the callback function or functions, making it a convenient way to store per-polygon information.</span></span>

<span data-ttu-id="1737f-122">Quando si chiama [**gluTessEndPolygon**](glutessendpolygon.md), il poligono è tassellati e i triangoli risultanti vengono descritti tramite callback.</span><span class="sxs-lookup"><span data-stu-id="1737f-122">When you call [**gluTessEndPolygon**](glutessendpolygon.md), the polygon is tessellated, and the resulting triangles are described through callbacks.</span></span> <span data-ttu-id="1737f-123">Per le descrizioni delle funzioni di callback, vedere [*gluTessCallback*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="1737f-123">For descriptions of the callback functions, see [*gluTessCallback*](glutess.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1737f-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="1737f-124">Examples</span></span>

<span data-ttu-id="1737f-125">Di seguito viene descritto un quadrilatero con un foro triangolare:</span><span class="sxs-lookup"><span data-stu-id="1737f-125">The following describes a quadrilateral with a triangular hole:</span></span>

``` syntax
gluTessBeginPolygon(tobj, NULL); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v1, v1); 
    gluTessVertex(tobj, v2, v2); 
    gluTessVertex(tobj, v3, v3); 
    gluTessVertex(tobj, v4, v4); 
  gluTessEndContour(tobj); 
  gluTessBeginContour(tobj); 
    gluTessVertex(tobj, v5, v5); 
    gluTessVertex(tobj, v6, v6); 
    gluTessVertex(tobj, v7, v7); 
  gluTessEndContour(tobj); 
gluTessEndPolygon(tobj);
```

## <a name="requirements"></a><span data-ttu-id="1737f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1737f-126">Requirements</span></span>



| <span data-ttu-id="1737f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1737f-127">Requirement</span></span> | <span data-ttu-id="1737f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="1737f-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1737f-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1737f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1737f-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1737f-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1737f-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1737f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1737f-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="1737f-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1737f-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1737f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="1737f-134"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="1737f-134"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="1737f-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="1737f-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="1737f-136"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1737f-136"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1737f-137">DLL</span><span class="sxs-lookup"><span data-stu-id="1737f-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1737f-138"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1737f-138"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1737f-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1737f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1737f-140">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="1737f-140">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="1737f-141">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="1737f-141">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="1737f-142">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="1737f-142">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="1737f-143">**gluTessEndContour**</span><span class="sxs-lookup"><span data-stu-id="1737f-143">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="1737f-144">**gluTessNormal**</span><span class="sxs-lookup"><span data-stu-id="1737f-144">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="1737f-145">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="1737f-145">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="1737f-146">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="1737f-146">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





