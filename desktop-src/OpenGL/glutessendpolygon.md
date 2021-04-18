---
title: funzione gluTessEndPolygon (Glu. h)
description: Le funzioni gluTessBeginPolygon e gluTessEndPolygon delimitano una descrizione del poligono. | funzione gluTessEndPolygon (Glu. h)
ms.assetid: c9ae2075-59d7-4c1a-b720-0aa05954525c
keywords:
- funzione gluTessEndPolygon OpenGL
topic_type:
- apiref
api_name:
- gluTessEndPolygon
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8353f9176e5bdb64dc0e3cd21bd42735e57b541b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321445"
---
# <a name="glutessendpolygon-function"></a><span data-ttu-id="5c97d-105">gluTessEndPolygon (funzione)</span><span class="sxs-lookup"><span data-stu-id="5c97d-105">gluTessEndPolygon function</span></span>

<span data-ttu-id="5c97d-106">Le funzioni [**gluTessBeginPolygon**](glutessbeginpolygon.md) e **gluTessEndPolygon** delimitano una descrizione del poligono.</span><span class="sxs-lookup"><span data-stu-id="5c97d-106">The [**gluTessBeginPolygon**](glutessbeginpolygon.md) and **gluTessEndPolygon** functions delimit a polygon description.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c97d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c97d-107">Syntax</span></span>


```C++
void WINAPI gluTessEndPolygon(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="5c97d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c97d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c97d-109">*Tess*</span><span class="sxs-lookup"><span data-stu-id="5c97d-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="5c97d-110">Oggetto a mosaico creato con [**gluNewTess**](glunewtess.md).</span><span class="sxs-lookup"><span data-stu-id="5c97d-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c97d-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c97d-111">Return value</span></span>

<span data-ttu-id="5c97d-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="5c97d-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c97d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c97d-113">Remarks</span></span>

<span data-ttu-id="5c97d-114">Le funzioni [**gluTessBeginPolygon**](glutessbeginpolygon.md) e **gluTessEndPolygon** delimitano la definizione di un poligono non convesso.</span><span class="sxs-lookup"><span data-stu-id="5c97d-114">The [**gluTessBeginPolygon**](glutessbeginpolygon.md) and **gluTessEndPolygon** functions delimit the definition of a nonconvex polygon.</span></span> <span data-ttu-id="5c97d-115">All'interno di ogni coppia **gluTessBeginPolygon**  /  **gluTessEndPolygon** , includere una o più chiamate a [**gluTessBeginContour**](glutessbegincontour.md).</span><span class="sxs-lookup"><span data-stu-id="5c97d-115">Within each **gluTessBeginPolygon** / **gluTessEndPolygon** pair, include one or more calls to [**gluTessBeginContour**](glutessbegincontour.md).</span></span> <span data-ttu-id="5c97d-116">All'interno di ogni contorno sono presenti zero o più chiamate a [**gluTessVertex**](glutessvertex.md).</span><span class="sxs-lookup"><span data-stu-id="5c97d-116">Within each contour, there are zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="5c97d-117">I vertici specificano un contorno chiuso (l'ultimo vertice di ogni contorno viene automaticamente collegato al primo).</span><span class="sxs-lookup"><span data-stu-id="5c97d-117">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span>

<span data-ttu-id="5c97d-118">Il parametro di *\_ dati Polygon* è un puntatore a una struttura di dati definita dal programmatore.</span><span class="sxs-lookup"><span data-stu-id="5c97d-118">The *polygon\_data* parameter is a pointer to a programmer-defined data structure.</span></span> <span data-ttu-id="5c97d-119">Se vengono specificati i callback appropriati (vedere [*gluTessCallback*](glutess.md)), questo puntatore viene restituito alla funzione o alle funzioni di callback, rendendolo un modo pratico per archiviare le informazioni per poligono.</span><span class="sxs-lookup"><span data-stu-id="5c97d-119">If the appropriate callbacks are specified (see [*gluTessCallback*](glutess.md)), this pointer is returned to the callback function or functions, making it a convenient way to store per-polygon information.</span></span>

<span data-ttu-id="5c97d-120">Quando si chiama **gluTessEndPolygon**, il poligono è tassellati e i triangoli risultanti vengono descritti tramite callback.</span><span class="sxs-lookup"><span data-stu-id="5c97d-120">When you call **gluTessEndPolygon**, the polygon is tessellated, and the resulting triangles are described through callbacks.</span></span> <span data-ttu-id="5c97d-121">Per le descrizioni delle funzioni di callback, vedere [*gluTessCallback*](glutess.md).</span><span class="sxs-lookup"><span data-stu-id="5c97d-121">For descriptions of the callback functions, see [*gluTessCallback*](glutess.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5c97d-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="5c97d-122">Examples</span></span>

<span data-ttu-id="5c97d-123">Di seguito viene descritto un quadrilatero con un foro triangolare:</span><span class="sxs-lookup"><span data-stu-id="5c97d-123">The following describes a quadrilateral with a triangular hole:</span></span>

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

## <a name="requirements"></a><span data-ttu-id="5c97d-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c97d-124">Requirements</span></span>



| <span data-ttu-id="5c97d-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c97d-125">Requirement</span></span> | <span data-ttu-id="5c97d-126">Valore</span><span class="sxs-lookup"><span data-stu-id="5c97d-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5c97d-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c97d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5c97d-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5c97d-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5c97d-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c97d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5c97d-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5c97d-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5c97d-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c97d-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c97d-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c97d-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="5c97d-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="5c97d-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="5c97d-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c97d-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5c97d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="5c97d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c97d-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c97d-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c97d-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c97d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c97d-138">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="5c97d-138">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="5c97d-139">**gluTessBeginContour**</span><span class="sxs-lookup"><span data-stu-id="5c97d-139">**gluTessBeginContour**</span></span>](glutessbegincontour.md)
</dt> <dt>

[<span data-ttu-id="5c97d-140">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="5c97d-140">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="5c97d-141">**gluTessEndContour**</span><span class="sxs-lookup"><span data-stu-id="5c97d-141">**gluTessEndContour**</span></span>](glutessendcontour.md)
</dt> <dt>

[<span data-ttu-id="5c97d-142">**gluTessNormal**</span><span class="sxs-lookup"><span data-stu-id="5c97d-142">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="5c97d-143">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="5c97d-143">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="5c97d-144">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="5c97d-144">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





