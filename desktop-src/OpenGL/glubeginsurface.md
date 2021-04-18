---
title: funzione gluBeginSurface (Glu. h)
description: Le funzioni gluBeginSurface e gluEndSurface delimitano una definizione di superficie B-spline (NURBS) razionale non uniforme. | funzione gluBeginSurface (Glu. h)
ms.assetid: 7189f05e-0c4d-4f82-8a82-a51fcc51b202
keywords:
- funzione gluBeginSurface OpenGL
topic_type:
- apiref
api_name:
- gluBeginSurface
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bbd09030290f78fac987a52cddd977a502dda06
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321401"
---
# <a name="glubeginsurface-function"></a><span data-ttu-id="7ddcf-105">gluBeginSurface (funzione)</span><span class="sxs-lookup"><span data-stu-id="7ddcf-105">gluBeginSurface function</span></span>

<span data-ttu-id="7ddcf-106">Le funzioni **gluBeginSurface** e [**gluEndSurface**](gluendsurface.md) delimitano una definizione di superficie B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) razionale non uniforme.</span><span class="sxs-lookup"><span data-stu-id="7ddcf-106">The **gluBeginSurface** and [**gluEndSurface**](gluendsurface.md) functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) surface definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ddcf-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ddcf-107">Syntax</span></span>


```C++
void WINAPI gluBeginSurface(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="7ddcf-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ddcf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ddcf-109">*juje*</span><span class="sxs-lookup"><span data-stu-id="7ddcf-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="7ddcf-110">Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="7ddcf-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ddcf-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ddcf-111">Return value</span></span>

<span data-ttu-id="7ddcf-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="7ddcf-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ddcf-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ddcf-113">Remarks</span></span>

<span data-ttu-id="7ddcf-114">Le funzioni **gluBeginSurface** e **gluEndSurface** contrassegnano l'inizio e la fine delle definizioni della superficie NURBS, definite con le chiamate a **gluNurbsSurface**.</span><span class="sxs-lookup"><span data-stu-id="7ddcf-114">The **gluBeginSurface** and **gluEndSurface** functions mark the beginning and end of NURBS surface definitions, which are defined with calls to **gluNurbsSurface**.</span></span>

1.  <span data-ttu-id="7ddcf-115">Chiamare **gluBeginSurface** per contrassegnare l'inizio di una definizione di superficie NURBS.</span><span class="sxs-lookup"><span data-stu-id="7ddcf-115">Call **gluBeginSurface** to mark the beginning of a NURBS surface definition.</span></span>
2.  <span data-ttu-id="7ddcf-116">Eseguire una o più chiamate a **gluNurbsSurface** per definire gli attributi della superficie.</span><span class="sxs-lookup"><span data-stu-id="7ddcf-116">Make one or more calls to **gluNurbsSurface** to define the attributes of the surface.</span></span>

    <span data-ttu-id="7ddcf-117">Una di queste chiamate a **gluNurbsSurface** deve avere un tipo di superficie di GL \_ map2 \_ Vertex \_ 3 o GL \_ map2 \_ Vertex \_ 4.</span><span class="sxs-lookup"><span data-stu-id="7ddcf-117">Exactly one of these calls to **gluNurbsSurface** must have a surface type of GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_VERTEX\_4.</span></span>

3.  <span data-ttu-id="7ddcf-118">Per contrassegnare la fine della definizione della superficie NURBS, chiamare **gluEndSurface**.</span><span class="sxs-lookup"><span data-stu-id="7ddcf-118">To mark the end of the NURBS surface definition, call **gluEndSurface**.</span></span>

<span data-ttu-id="7ddcf-119">Le funzioni [**gluBeginTrim**](glubegintrim.md), [**gluPwlCurve**](glupwlcurve.md), [**gluNurbsCurve**](glunurbscurve.md)e [**gluEndTrim**](gluendtrim.md) supportano il taglio di superfici NURBS.</span><span class="sxs-lookup"><span data-stu-id="7ddcf-119">The [**gluBeginTrim**](glubegintrim.md), [**gluPwlCurve**](glupwlcurve.md), [**gluNurbsCurve**](glunurbscurve.md), and [**gluEndTrim**](gluendtrim.md) functions support trimming of NURBS surfaces.</span></span>

<span data-ttu-id="7ddcf-120">Usare gli analizzatori OpenGL per eseguire il rendering della superficie NURBS come un set di poligoni.</span><span class="sxs-lookup"><span data-stu-id="7ddcf-120">Use OpenGL evaluators to render the NURBS surface as a set of polygons.</span></span> <span data-ttu-id="7ddcf-121">Mantenere lo stato dell'analizzatore durante il rendering con [**glPushAttrib**](glpushattrib.md)(bit valutazione GL \_ \_ ) e [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="7ddcf-121">Preserve the evaluator state during rendering with [**glPushAttrib**](glpushattrib.md)(GL\_EVAL\_BIT) and [**glPopAttrib**](glpopattrib.md).</span></span>

## <a name="examples"></a><span data-ttu-id="7ddcf-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="7ddcf-122">Examples</span></span>

<span data-ttu-id="7ddcf-123">Le funzioni seguenti eseguono il rendering di una superficie NURBS con trama con normali; le coordinate di trama e le normali sono descritte anche come superfici NURBS:</span><span class="sxs-lookup"><span data-stu-id="7ddcf-123">The following functions render a textured NURBS surface with normals; the texture coordinates and normals are also described as NURBS surfaces:</span></span>

``` syntax
gluBeginSurface(nobj); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_TEXTURE_COORD_2); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_NORMAL); 
    gluNurbsSurface(nobj, . . ., GL_MAP2_VERTEX_4); 
gluEndSurface(nobj);
```

## <a name="requirements"></a><span data-ttu-id="7ddcf-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ddcf-124">Requirements</span></span>



| <span data-ttu-id="7ddcf-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ddcf-125">Requirement</span></span> | <span data-ttu-id="7ddcf-126">Valore</span><span class="sxs-lookup"><span data-stu-id="7ddcf-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7ddcf-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ddcf-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7ddcf-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7ddcf-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7ddcf-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ddcf-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7ddcf-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7ddcf-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7ddcf-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ddcf-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ddcf-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ddcf-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="7ddcf-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="7ddcf-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="7ddcf-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ddcf-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7ddcf-135">DLL</span><span class="sxs-lookup"><span data-stu-id="7ddcf-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ddcf-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ddcf-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ddcf-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ddcf-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ddcf-138">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="7ddcf-138">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="7ddcf-139">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="7ddcf-139">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="7ddcf-140">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="7ddcf-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="7ddcf-141">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="7ddcf-141">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> <dt>

[<span data-ttu-id="7ddcf-142">**gluNurbsSurface**</span><span class="sxs-lookup"><span data-stu-id="7ddcf-142">**gluNurbsSurface**</span></span>](glunurbssurface.md)
</dt> <dt>

[<span data-ttu-id="7ddcf-143">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="7ddcf-143">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





