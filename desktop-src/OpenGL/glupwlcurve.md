---
title: funzione gluPwlCurve (Glu. h)
description: La funzione gluPwlCurve descrive una curva di taglio a tratti lineare non uniforme (NURBS, B-spline).
ms.assetid: 3d08e7e8-dfdf-447c-9795-bd73299412b5
keywords:
- funzione gluPwlCurve OpenGL
topic_type:
- apiref
api_name:
- gluPwlCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d15c532659811c7e499369e7798c4b1ceaf842bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302106"
---
# <a name="glupwlcurve-function"></a><span data-ttu-id="cd055-104">gluPwlCurve (funzione)</span><span class="sxs-lookup"><span data-stu-id="cd055-104">gluPwlCurve function</span></span>

<span data-ttu-id="cd055-105">La funzione **gluPwlCurve** descrive una curva di taglio A tratti lineare non uniforme ([NURBS](using-nurbs-curves-and-surfaces.md), B-spline).</span><span class="sxs-lookup"><span data-stu-id="cd055-105">The **gluPwlCurve** function describes a piecewise linear Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) trimming curve.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd055-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd055-106">Syntax</span></span>


```C++
void WINAPI gluPwlCurve(
   GLUnurbs *nobj,
   GLint    count,
   GLfloat  *array,
   GLint    stride,
   GLenum   type
);
```



## <a name="parameters"></a><span data-ttu-id="cd055-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd055-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd055-108">*juje*</span><span class="sxs-lookup"><span data-stu-id="cd055-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="cd055-109">Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="cd055-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="cd055-110">*count*</span><span class="sxs-lookup"><span data-stu-id="cd055-110">*count*</span></span> 
</dt> <dd>

<span data-ttu-id="cd055-111">Numero di punti sulla curva.</span><span class="sxs-lookup"><span data-stu-id="cd055-111">The number of points on the curve.</span></span>

</dd> <dt>

<span data-ttu-id="cd055-112">*array*</span><span class="sxs-lookup"><span data-stu-id="cd055-112">*array*</span></span> 
</dt> <dd>

<span data-ttu-id="cd055-113">Matrice contenente i punti della curva.</span><span class="sxs-lookup"><span data-stu-id="cd055-113">An array containing the curve points.</span></span>

</dd> <dt>

<span data-ttu-id="cd055-114">*stride*</span><span class="sxs-lookup"><span data-stu-id="cd055-114">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="cd055-115">Offset (un numero di valori a virgola mobile e precisione singola) tra i punti sulla curva.</span><span class="sxs-lookup"><span data-stu-id="cd055-115">The offset (a number of single-precision floating-point values) between points on the curve.</span></span>

</dd> <dt>

<span data-ttu-id="cd055-116">*type*</span><span class="sxs-lookup"><span data-stu-id="cd055-116">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="cd055-117">Tipo di curva.</span><span class="sxs-lookup"><span data-stu-id="cd055-117">The type of curve.</span></span> <span data-ttu-id="cd055-118">Deve essere GLU \_ Mappa1 \_ Trim \_ 2 o Glu \_ Mappa1 \_ Trim \_ 3.</span><span class="sxs-lookup"><span data-stu-id="cd055-118">Must be either GLU\_MAP1\_TRIM\_2 or GLU\_MAP1\_TRIM\_3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd055-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd055-119">Return value</span></span>

<span data-ttu-id="cd055-120">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="cd055-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd055-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd055-121">Remarks</span></span>

<span data-ttu-id="cd055-122">La funzione **gluPwlCurve** descrive una curva di trimming lineare a tratti per una superficie NURBS.</span><span class="sxs-lookup"><span data-stu-id="cd055-122">The **gluPwlCurve** function describes a piecewise linear trimming curve for a NURBS surface.</span></span> <span data-ttu-id="cd055-123">Una curva lineare a tratti è costituita da un elenco di coordinate dei punti nello spazio dei parametri per la superficie NURBS da tagliare.</span><span class="sxs-lookup"><span data-stu-id="cd055-123">A piecewise linear curve consists of a list of coordinates of points in the parameter space for the NURBS surface to be trimmed.</span></span> <span data-ttu-id="cd055-124">Questi punti sono connessi con segmenti di linea per formare una curva.</span><span class="sxs-lookup"><span data-stu-id="cd055-124">These points are connected with line segments to form a curve.</span></span> <span data-ttu-id="cd055-125">Se la curva è un'approssimazione a una curva reale, è necessario che i punti siano sufficientemente vicini che il tracciato risultante appaia curvo in corrispondenza della risoluzione utilizzata nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cd055-125">If the curve is an approximation to a real curve, the points should be close enough that the resulting path appears curved at the resolution used in the application.</span></span>

<span data-ttu-id="cd055-126">Se *Type* è Glu \_ Mappa1 \_ Trim \_ 2, descrive una curva nello spazio di parametri bidimensionali (*u* e *v*).</span><span class="sxs-lookup"><span data-stu-id="cd055-126">If *type* is GLU\_MAP1\_TRIM\_2, it describes a curve in two-dimensional (*u* and *v*) parameter space.</span></span> <span data-ttu-id="cd055-127">Se è GLU \_ Mappa1 \_ Trim \_ 3, descrive una curva in uno spazio di parametri omogeneo (*u*, *v* e *w*) bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="cd055-127">If it is GLU\_MAP1\_TRIM\_3, then it describes a curve in two-dimensional homogeneous (*u*, *v*, and *w*) parameter space.</span></span> <span data-ttu-id="cd055-128">Per ulteriori informazioni sulle curve di trimming, vedere [**gluBeginTrim**](glubegintrim.md).</span><span class="sxs-lookup"><span data-stu-id="cd055-128">For more information about trimming curves, see [**gluBeginTrim**](glubegintrim.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd055-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd055-129">Requirements</span></span>



| <span data-ttu-id="cd055-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd055-130">Requirement</span></span> | <span data-ttu-id="cd055-131">Valore</span><span class="sxs-lookup"><span data-stu-id="cd055-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cd055-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd055-132">Minimum supported client</span></span><br/> | <span data-ttu-id="cd055-133">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cd055-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cd055-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cd055-134">Minimum supported server</span></span><br/> | <span data-ttu-id="cd055-135">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="cd055-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cd055-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd055-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd055-137"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd055-137"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="cd055-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="cd055-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="cd055-139"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd055-139"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cd055-140">DLL</span><span class="sxs-lookup"><span data-stu-id="cd055-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd055-141"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd055-141"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd055-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd055-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd055-143">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="cd055-143">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="cd055-144">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="cd055-144">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="cd055-145">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="cd055-145">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="cd055-146">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="cd055-146">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> </dl>

 

 





