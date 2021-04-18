---
title: funzione gluEndCurve (Glu. h)
description: Le funzioni gluBeginCurve e gluEndCurve delimitano una definizione di curva B-spline (NURBS) razionale non uniforme. | funzione gluEndCurve (Glu. h)
ms.assetid: b00ec687-6127-4585-b7b7-06e8dca78cfc
keywords:
- funzione gluEndCurve OpenGL
topic_type:
- apiref
api_name:
- gluEndCurve
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49f6c0c08bf31135ca82e87d2093ef3b57197955
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321738"
---
# <a name="gluendcurve-function"></a><span data-ttu-id="5b968-105">gluEndCurve (funzione)</span><span class="sxs-lookup"><span data-stu-id="5b968-105">gluEndCurve function</span></span>

<span data-ttu-id="5b968-106">Le funzioni [**gluBeginCurve**](glubegincurve.md) e **gluEndCurve** delimitano una definizione di curva B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) razionale non uniforme.</span><span class="sxs-lookup"><span data-stu-id="5b968-106">The [**gluBeginCurve**](glubegincurve.md) and **gluEndCurve** functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) curve definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b968-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b968-107">Syntax</span></span>


```C++
void WINAPI gluEndCurve(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="5b968-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5b968-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b968-109">*juje*</span><span class="sxs-lookup"><span data-stu-id="5b968-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="5b968-110">Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="5b968-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b968-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b968-111">Return value</span></span>

<span data-ttu-id="5b968-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="5b968-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b968-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b968-113">Remarks</span></span>

<span data-ttu-id="5b968-114">Usare [**gluBeginCurve**](glubegincurve.md) per contrassegnare l'inizio di una definizione di curva NURBS.</span><span class="sxs-lookup"><span data-stu-id="5b968-114">Use [**gluBeginCurve**](glubegincurve.md) to mark the beginning of a NURBS curve definition.</span></span> <span data-ttu-id="5b968-115">Dopo la chiamata a **gluBeginCurve**, effettuare una o più chiamate a [**gluNurbsCurve**](glunurbscurve.md) per definire gli attributi della curva.</span><span class="sxs-lookup"><span data-stu-id="5b968-115">After calling **gluBeginCurve**, make one or more calls to [**gluNurbsCurve**](glunurbscurve.md) to define the attributes of the curve.</span></span> <span data-ttu-id="5b968-116">Esattamente una delle chiamate a **gluNurbsCurve** deve avere un tipo di curva di GL \_ Mappa1 \_ Vertex \_ 3 o GL \_ Mappa1 \_ Vertex \_ 4.</span><span class="sxs-lookup"><span data-stu-id="5b968-116">Exactly one of the calls to **gluNurbsCurve** must have a curve type of GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4.</span></span> <span data-ttu-id="5b968-117">Per contrassegnare la fine della definizione della curva NURBS, chiamare **gluEndCurve**.</span><span class="sxs-lookup"><span data-stu-id="5b968-117">To mark the end of the NURBS curve definition, call **gluEndCurve**.</span></span>

<span data-ttu-id="5b968-118">Gli analizzatori OpenGL vengono usati per eseguire il rendering della curva NURBS come una serie di segmenti di linea.</span><span class="sxs-lookup"><span data-stu-id="5b968-118">OpenGL evaluators are used to render the NURBS curve as a series of line segments.</span></span> <span data-ttu-id="5b968-119">Lo stato dell'analizzatore viene mantenuto durante il rendering con [**glPushAttrib**](glpushattrib.md) (GL \_ eval \_ bit) e [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="5b968-119">Evaluator state is preserved during rendering with [**glPushAttrib**](glpushattrib.md) (GL\_EVAL\_BIT ) and [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="5b968-120">Per informazioni sullo stato che queste chiamate conservano, vedere **glPushAttrib**.</span><span class="sxs-lookup"><span data-stu-id="5b968-120">For information on exactly what state these calls preserve, see **glPushAttrib**.</span></span>

## <a name="examples"></a><span data-ttu-id="5b968-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="5b968-121">Examples</span></span>

<span data-ttu-id="5b968-122">Le funzioni seguenti eseguono il rendering di una curva NURBS con trama con normali; le coordinate di trama e le normali vengono specificate anche come curve NURBS:</span><span class="sxs-lookup"><span data-stu-id="5b968-122">The following functions render a textured NURBS curve with normals; texture coordinates and normals are also specified as NURBS curves:</span></span>

``` syntax
gluBeginCurve(nobj); 
gluNurbsCurve(nobj, . . ., GL_MAP1_TEXTURE_COORD_2); 
gluNurbsCurve(nobj, . . ., GL_MAP1_NORMAL); 
gluNurbsCurve(nobj, . . ., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj);
```

## <a name="requirements"></a><span data-ttu-id="5b968-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b968-123">Requirements</span></span>



| <span data-ttu-id="5b968-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b968-124">Requirement</span></span> | <span data-ttu-id="5b968-125">Valore</span><span class="sxs-lookup"><span data-stu-id="5b968-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5b968-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b968-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5b968-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5b968-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5b968-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b968-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5b968-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5b968-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5b968-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b968-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b968-131"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b968-131"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="5b968-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="5b968-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="5b968-133"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b968-133"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5b968-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5b968-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b968-135"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b968-135"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b968-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5b968-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b968-137">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="5b968-137">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="5b968-138">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="5b968-138">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="5b968-139">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="5b968-139">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="5b968-140">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="5b968-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="5b968-141">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="5b968-141">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> </dl>

 

 





