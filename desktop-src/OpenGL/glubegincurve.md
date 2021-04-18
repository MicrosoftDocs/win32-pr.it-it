---
title: funzione gluBeginCurve (Glu. h)
description: Le funzioni gluBeginCurve e gluEndCurve delimitano una definizione di curva B-spline (NURBS) razionale non uniforme. | funzione gluBeginCurve (Glu. h)
ms.assetid: f7f2e765-1a07-4faa-940c-9cb957dd54d4
keywords:
- funzione gluBeginCurve OpenGL
topic_type:
- apiref
api_name:
- gluBeginCurve
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4e17bd88cfcb49801450ead865c437843d179b5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321986"
---
# <a name="glubegincurve-function"></a><span data-ttu-id="7cec9-105">gluBeginCurve (funzione)</span><span class="sxs-lookup"><span data-stu-id="7cec9-105">gluBeginCurve function</span></span>

<span data-ttu-id="7cec9-106">Le funzioni **gluBeginCurve** e [**gluEndCurve**](gluendcurve.md) delimitano una definizione di curva B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) razionale non uniforme.</span><span class="sxs-lookup"><span data-stu-id="7cec9-106">The **gluBeginCurve** and [**gluEndCurve**](gluendcurve.md) functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) curve definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cec9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7cec9-107">Syntax</span></span>


```C++
void WINAPI gluBeginCurve(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="7cec9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7cec9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7cec9-109">*juje*</span><span class="sxs-lookup"><span data-stu-id="7cec9-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="7cec9-110">Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="7cec9-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7cec9-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7cec9-111">Return value</span></span>

<span data-ttu-id="7cec9-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="7cec9-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cec9-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7cec9-113">Remarks</span></span>

<span data-ttu-id="7cec9-114">Usare **gluBeginCurve** per contrassegnare l'inizio di una definizione di curva NURBS.</span><span class="sxs-lookup"><span data-stu-id="7cec9-114">Use **gluBeginCurve** to mark the beginning of a NURBS curve definition.</span></span> <span data-ttu-id="7cec9-115">Dopo la chiamata a **gluBeginCurve**, effettuare una o più chiamate a [**gluNurbsCurve**](glunurbscurve.md) per definire gli attributi della curva.</span><span class="sxs-lookup"><span data-stu-id="7cec9-115">After calling **gluBeginCurve**, make one or more calls to [**gluNurbsCurve**](glunurbscurve.md) to define the attributes of the curve.</span></span> <span data-ttu-id="7cec9-116">Esattamente una delle chiamate a **gluNurbsCurve** deve avere un tipo di curva di GL \_ Mappa1 \_ Vertex \_ 3 o GL \_ Mappa1 \_ Vertex \_ 4.</span><span class="sxs-lookup"><span data-stu-id="7cec9-116">Exactly one of the calls to **gluNurbsCurve** must have a curve type of GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4.</span></span> <span data-ttu-id="7cec9-117">Per contrassegnare la fine della definizione della curva NURBS, chiamare [**gluEndCurve**](gluendcurve.md).</span><span class="sxs-lookup"><span data-stu-id="7cec9-117">To mark the end of the NURBS curve definition, call [**gluEndCurve**](gluendcurve.md).</span></span>

<span data-ttu-id="7cec9-118">Gli analizzatori OpenGL vengono usati per eseguire il rendering della curva NURBS come una serie di segmenti di linea.</span><span class="sxs-lookup"><span data-stu-id="7cec9-118">OpenGL evaluators are used to render the NURBS curve as a series of line segments.</span></span> <span data-ttu-id="7cec9-119">Lo stato dell'analizzatore viene mantenuto durante il rendering con [**glPushAttrib**](glpushattrib.md) (GL \_ eval \_ bit) e [**glPopAttrib**](glpopattrib.md).</span><span class="sxs-lookup"><span data-stu-id="7cec9-119">Evaluator state is preserved during rendering with [**glPushAttrib**](glpushattrib.md) (GL\_EVAL\_BIT) and [**glPopAttrib**](glpopattrib.md).</span></span> <span data-ttu-id="7cec9-120">Per informazioni sullo stato che queste chiamate conservano, vedere **glPushAttrib**.</span><span class="sxs-lookup"><span data-stu-id="7cec9-120">For information on exactly what state these calls preserve, see **glPushAttrib**.</span></span>

## <a name="examples"></a><span data-ttu-id="7cec9-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="7cec9-121">Examples</span></span>

<span data-ttu-id="7cec9-122">Le funzioni seguenti eseguono il rendering di una curva NURBS con trama con normali; le coordinate di trama e le normali vengono specificate anche come curve NURBS:</span><span class="sxs-lookup"><span data-stu-id="7cec9-122">The following functions render a textured NURBS curve with normals; texture coordinates and normals are also specified as NURBS curves:</span></span>

``` syntax
gluBeginCurve(nobj); 
gluNurbsCurve(nobj, . . ., GL_MAP1_TEXTURE_COORD_2); 
gluNurbsCurve(nobj, . . ., GL_MAP1_NORMAL); 
gluNurbsCurve(nobj, . . ., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj);
```

## <a name="requirements"></a><span data-ttu-id="7cec9-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7cec9-123">Requirements</span></span>



| <span data-ttu-id="7cec9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cec9-124">Requirement</span></span> | <span data-ttu-id="7cec9-125">Valore</span><span class="sxs-lookup"><span data-stu-id="7cec9-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7cec9-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7cec9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7cec9-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7cec9-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7cec9-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7cec9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7cec9-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7cec9-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7cec9-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7cec9-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7cec9-131"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="7cec9-131"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="7cec9-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="7cec9-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="7cec9-133"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7cec9-133"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7cec9-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7cec9-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7cec9-135"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7cec9-135"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cec9-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7cec9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cec9-137">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="7cec9-137">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="7cec9-138">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="7cec9-138">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="7cec9-139">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="7cec9-139">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="7cec9-140">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="7cec9-140">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="7cec9-141">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="7cec9-141">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> </dl>

 

 





