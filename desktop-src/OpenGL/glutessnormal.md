---
title: funzione gluTessNormal (Glu. h)
description: La funzione gluTessNormal specifica un normale per un poligono.
ms.assetid: 8c3a90d3-760d-4a0a-9808-a797383fcc42
keywords:
- funzione gluTessNormal OpenGL
topic_type:
- apiref
api_name:
- gluTessNormal
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af04ab2364fafcea709ca36cab2f10a8bea1a96f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964827"
---
# <a name="glutessnormal-function"></a><span data-ttu-id="33080-104">gluTessNormal (funzione)</span><span class="sxs-lookup"><span data-stu-id="33080-104">gluTessNormal function</span></span>

<span data-ttu-id="33080-105">La funzione **gluTessNormal** specifica un normale per un poligono.</span><span class="sxs-lookup"><span data-stu-id="33080-105">The **gluTessNormal** function specifies a normal for a polygon.</span></span>

## <a name="syntax"></a><span data-ttu-id="33080-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33080-106">Syntax</span></span>


```C++
void WINAPI gluTessNormal(
   GLUtesselator *tess,
   GLdouble      x,
   GLdouble      y,
   GLdouble      z
);
```



## <a name="parameters"></a><span data-ttu-id="33080-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="33080-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33080-108">*Tess*</span><span class="sxs-lookup"><span data-stu-id="33080-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="33080-109">Oggetto a mosaico creato con [**gluNewTess**](glunewtess.md).</span><span class="sxs-lookup"><span data-stu-id="33080-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="33080-110">*x*</span><span class="sxs-lookup"><span data-stu-id="33080-110">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="33080-111">Componente della coordinata x di un normale.</span><span class="sxs-lookup"><span data-stu-id="33080-111">The x-coordinate component of a normal.</span></span>

</dd> <dt>

<span data-ttu-id="33080-112">*y*</span><span class="sxs-lookup"><span data-stu-id="33080-112">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="33080-113">Componente della coordinata y di un normale.</span><span class="sxs-lookup"><span data-stu-id="33080-113">The y-coordinate component of a normal.</span></span>

</dd> <dt>

<span data-ttu-id="33080-114">*z*</span><span class="sxs-lookup"><span data-stu-id="33080-114">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="33080-115">Componente della coordinata z di un normale.</span><span class="sxs-lookup"><span data-stu-id="33080-115">The z-coordinate component of a normal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33080-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33080-116">Return value</span></span>

<span data-ttu-id="33080-117">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="33080-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33080-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="33080-118">Remarks</span></span>

<span data-ttu-id="33080-119">La funzione **gluTessNormal** descrive un normale per un poligono definito dall'utente.</span><span class="sxs-lookup"><span data-stu-id="33080-119">The **gluTessNormal** function describes a normal for a polygon that you define.</span></span> <span data-ttu-id="33080-120">Tutti i dati di input vengono proiettati su un piano perpendicolare a uno dei tre assi delle coordinate prima dello schema a mosaico e tutti i triangoli di output sono orientati in senso antiorario rispetto al normale.</span><span class="sxs-lookup"><span data-stu-id="33080-120">All input data is projected onto a plane perpendicular to one of the three coordinate axes before tessellation, and all output triangles are oriented counterclockwise with respect to the normal.</span></span> <span data-ttu-id="33080-121">(Per ottenere l'orientamento in senso orario, invertire il segno del normale fornito).</span><span class="sxs-lookup"><span data-stu-id="33080-121">(To obtain clockwise orientation, reverse the sign of the supplied normal).</span></span> <span data-ttu-id="33080-122">Ad esempio, se si è certi che tutti i poligoni si trovano nel piano x-y, chiamare **gluTessNormal**(tess, 0,0, 0,0, 1,0) prima di eseguire il rendering di tutti i poligoni.</span><span class="sxs-lookup"><span data-stu-id="33080-122">For example, if you know that all polygons lie in the x-y plane, call **gluTessNormal**(tess, 0.0, 0.0, 1.0) before rendering any polygons.</span></span>

<span data-ttu-id="33080-123">Se il valore normale fornito è (0,0, 0,0, 0,0) (il valore predefinito), il normale viene determinato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="33080-123">If the supplied normal is (0.0, 0.0, 0.0) (the default value), the normal is determined as follows:</span></span>

1.  <span data-ttu-id="33080-124">La direzione della normale, fino al segno, viene rilevata mediante l'adattamento di un piano ai vertici, indipendentemente dalla modalità di connessione dei vertici.</span><span class="sxs-lookup"><span data-stu-id="33080-124">The direction of the normal, up to its sign, is found by fitting a plane to the vertexes, without regard to how the vertexes are connected.</span></span> <span data-ttu-id="33080-125">Si prevede che i dati di input si trovino approssimativamente nel piano; in caso contrario, la proiezione perpendicolare a uno dei tre assi delle coordinate può modificare notevolmente la geometria.</span><span class="sxs-lookup"><span data-stu-id="33080-125">It is expected that the input data lies approximately in the plane; otherwise projection perpendicular to one of the three coordinate axes can change the geometry substantially.</span></span>
2.  <span data-ttu-id="33080-126">Il segno della normale viene scelto in modo che la somma delle aree firmate di tutti i contorni di input sia non negativo (dove un contorno in senso antiorario ha un'area positiva).</span><span class="sxs-lookup"><span data-stu-id="33080-126">The sign of the normal is chosen so that the sum of the signed areas of all input contours is nonnegative (where a counterclockwise contour has positive area).</span></span>

<span data-ttu-id="33080-127">Il normale fornito viene mantenuto finché un'altra chiamata a **gluTessNormal** non la modifica.</span><span class="sxs-lookup"><span data-stu-id="33080-127">The supplied normal persists until another call to **gluTessNormal** changes it.</span></span>

## <a name="requirements"></a><span data-ttu-id="33080-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33080-128">Requirements</span></span>



| <span data-ttu-id="33080-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="33080-129">Requirement</span></span> | <span data-ttu-id="33080-130">Valore</span><span class="sxs-lookup"><span data-stu-id="33080-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="33080-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33080-131">Minimum supported client</span></span><br/> | <span data-ttu-id="33080-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="33080-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="33080-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33080-133">Minimum supported server</span></span><br/> | <span data-ttu-id="33080-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="33080-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="33080-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33080-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="33080-136"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="33080-136"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="33080-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="33080-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="33080-138"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33080-138"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="33080-139">DLL</span><span class="sxs-lookup"><span data-stu-id="33080-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33080-140"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33080-140"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33080-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33080-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33080-142">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="33080-142">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="33080-143">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="33080-143">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="33080-144">**gluTessEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="33080-144">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> </dl>

 

 





