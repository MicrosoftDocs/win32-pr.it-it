---
title: funzione gluTessEndContour (Glu. h)
description: Le funzioni gluTessBeginContour e gluTessEndContour delimitano una descrizione del contorno. | funzione gluTessEndContour (Glu. h)
ms.assetid: 115db079-cbcb-48e1-8bab-0eb4814afb82
keywords:
- funzione gluTessEndContour OpenGL
topic_type:
- apiref
api_name:
- gluTessEndContour
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ac53f3920476489a1453bb6b5dc1e01d650d4fe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352541"
---
# <a name="glutessendcontour-function"></a><span data-ttu-id="7ff70-105">gluTessEndContour (funzione)</span><span class="sxs-lookup"><span data-stu-id="7ff70-105">gluTessEndContour function</span></span>

<span data-ttu-id="7ff70-106">Le funzioni [**gluTessBeginContour**](glutessbegincontour.md) e **gluTessEndContour** delimitano una descrizione del contorno.</span><span class="sxs-lookup"><span data-stu-id="7ff70-106">The [**gluTessBeginContour**](glutessbegincontour.md) and **gluTessEndContour** functions delimit a contour description.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ff70-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ff70-107">Syntax</span></span>


```C++
void WINAPI gluTessEndContour(
   GLUtesselator *tess
);
```



## <a name="parameters"></a><span data-ttu-id="7ff70-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ff70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ff70-109">*Tess*</span><span class="sxs-lookup"><span data-stu-id="7ff70-109">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="7ff70-110">Oggetto a mosaico creato con [**gluNewTess**](glunewtess.md).</span><span class="sxs-lookup"><span data-stu-id="7ff70-110">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ff70-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ff70-111">Return value</span></span>

<span data-ttu-id="7ff70-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="7ff70-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ff70-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ff70-113">Remarks</span></span>

<span data-ttu-id="7ff70-114">Le funzioni [**gluTessBeginContour**](glutessbegincontour.md) e **gluTessEndContour** delimitano la definizione di un contorno poligono.</span><span class="sxs-lookup"><span data-stu-id="7ff70-114">The [**gluTessBeginContour**](glutessbegincontour.md) and **gluTessEndContour** functions delimit the definition of a polygon contour.</span></span> <span data-ttu-id="7ff70-115">All'interno di ogni coppia **gluTessBeginContour** / **gluTessEndContour** , possono essere presenti zero o più chiamate a [**gluTessVertex**](glutessvertex.md).</span><span class="sxs-lookup"><span data-stu-id="7ff70-115">Within each **gluTessBeginContour**/**gluTessEndContour** pair, there can be zero or more calls to [**gluTessVertex**](glutessvertex.md).</span></span> <span data-ttu-id="7ff70-116">I vertici specificano un contorno chiuso (l'ultimo vertice di ogni contorno viene automaticamente collegato al primo).</span><span class="sxs-lookup"><span data-stu-id="7ff70-116">The vertexes specify a closed contour (the last vertex of each contour is automatically linked to the first).</span></span> <span data-ttu-id="7ff70-117">È possibile chiamare **gluTessBeginContour** solo tra [**gluTessBeginPolygon**](glutessbeginpolygon.md) e [**gluTessEndPolygon**](glutessendpolygon.md).</span><span class="sxs-lookup"><span data-stu-id="7ff70-117">You can call **gluTessBeginContour** only between [**gluTessBeginPolygon**](glutessbeginpolygon.md) and [**gluTessEndPolygon**](glutessendpolygon.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ff70-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ff70-118">Requirements</span></span>



| <span data-ttu-id="7ff70-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ff70-119">Requirement</span></span> | <span data-ttu-id="7ff70-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7ff70-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7ff70-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ff70-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7ff70-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7ff70-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7ff70-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ff70-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7ff70-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7ff70-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7ff70-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ff70-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ff70-126"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ff70-126"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="7ff70-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="7ff70-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="7ff70-128"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ff70-128"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7ff70-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7ff70-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ff70-130"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ff70-130"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ff70-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ff70-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ff70-132">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="7ff70-132">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="7ff70-133">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="7ff70-133">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="7ff70-134">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="7ff70-134">*gluTessCallback*</span></span>](glutess.md)
</dt> <dt>

[<span data-ttu-id="7ff70-135">**gluTessEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="7ff70-135">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> <dt>

[<span data-ttu-id="7ff70-136">**gluTessNormal**</span><span class="sxs-lookup"><span data-stu-id="7ff70-136">**gluTessNormal**</span></span>](glutessnormal.md)
</dt> <dt>

[<span data-ttu-id="7ff70-137">**gluTessProperty**</span><span class="sxs-lookup"><span data-stu-id="7ff70-137">**gluTessProperty**</span></span>](glutessproperty.md)
</dt> <dt>

[<span data-ttu-id="7ff70-138">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="7ff70-138">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





