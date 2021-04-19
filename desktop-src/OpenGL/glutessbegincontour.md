---
title: funzione gluTessBeginContour (Glu. h)
description: Le funzioni gluTessBeginContour e gluTessEndContour delimitano una descrizione del contorno. | funzione gluTessBeginContour (Glu. h)
ms.assetid: 4008ce9c-86e7-4b24-9bda-5915f469596a
keywords:
- funzione gluTessBeginContour OpenGL
topic_type:
- apiref
api_name:
- gluTessBeginContour
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd28efc96c977e5e0483b4f3d87e9ce840b985cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321597"
---
# <a name="glutessbegincontour-function"></a><span data-ttu-id="9749b-105">gluTessBeginContour (funzione)</span><span class="sxs-lookup"><span data-stu-id="9749b-105">gluTessBeginContour function</span></span>

<span data-ttu-id="9749b-106">Le funzioni **gluTessBeginContour** e [**gluTessEndContour**](glutessendcontour.md) delimitano una descrizione del contorno.</span><span class="sxs-lookup"><span data-stu-id="9749b-106">The **gluTessBeginContour** and [**gluTessEndContour**](glutessendcontour.md) functions delimit a contour description.</span></span>

## <a name="syntax"></a><span data-ttu-id="9749b-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9749b-107">Syntax</span></span>


```C++
void WINAPI gluTessBeginContour(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="9749b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9749b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9749b-109">*Tess*</span><span class="sxs-lookup"><span data-stu-id="9749b-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="9749b-110">Oggetto a mosaico creato con [**gluNewTess**](glunewtess.md).</span><span class="sxs-lookup"><span data-stu-id="9749b-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9749b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9749b-111">Return value</span></span>

<span data-ttu-id="9749b-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="9749b-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9749b-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="9749b-113">Remarks</span></span>

<span data-ttu-id="9749b-114">Le funzioni **gluTessBeginContour** e [**gluTessEndPolygon**](glutessendpolygon.md) delimitano la definizione di un contorno poligono.</span><span class="sxs-lookup"><span data-stu-id="9749b-114">The **gluTessBeginContour** and [**gluTessEndPolygon**](glutessendpolygon.md) functions delimit the definition of a polygon contour.</span></span> <span data-ttu-id="9749b-115">All'interno di ogni coppia **gluTessBeginContour** / **gluTessEndPolygon** , possono essere presenti zero o più chiamate a [**gluTessVertex**](glutessvertex.md).</span><span class="sxs-lookup"><span data-stu-id="9749b-115">Within each **gluTessBeginContour**/**gluTessEndPolygon** pair, there can be zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="9749b-116">I vertici specificano un contorno chiuso (l'ultimo vertice di ogni contorno viene automaticamente collegato al primo).</span><span class="sxs-lookup"><span data-stu-id="9749b-116">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span> <span data-ttu-id="9749b-117">È possibile chiamare **gluTessBeginContour** solo tra [**gluTessBeginPolygon**](glutessbeginpolygon.md) e **gluTessEndPolygon**.</span><span class="sxs-lookup"><span data-stu-id="9749b-117">You can call **gluTessBeginContour** only between [**gluTessBeginPolygon**](glutessbeginpolygon.md) and **gluTessEndPolygon**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9749b-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9749b-118">Requirements</span></span>



| <span data-ttu-id="9749b-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9749b-119">Requirement</span></span> | <span data-ttu-id="9749b-120">Valore</span><span class="sxs-lookup"><span data-stu-id="9749b-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9749b-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9749b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9749b-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9749b-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9749b-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9749b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9749b-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9749b-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9749b-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9749b-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9749b-126"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="9749b-126"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="9749b-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="9749b-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="9749b-128"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9749b-128"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9749b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="9749b-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9749b-130"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9749b-130"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9749b-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9749b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9749b-132">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="9749b-132">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="9749b-133">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="9749b-133">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="9749b-134">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="9749b-134">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="9749b-135">**gluTessEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="9749b-135">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> <dt>

[<span data-ttu-id="9749b-136">**gluTessNormal**</span><span class="sxs-lookup"><span data-stu-id="9749b-136">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="9749b-137">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="9749b-137">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="9749b-138">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="9749b-138">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





