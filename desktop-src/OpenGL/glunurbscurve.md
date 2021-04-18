---
title: funzione gluNurbsCurve (Glu. h)
description: La funzione gluNurbsCurve definisce la forma di una curva B-spline (NURBS) razionale non uniforme.
ms.assetid: d03064a5-26f5-487f-877f-3748646bcb2f
keywords:
- funzione gluNurbsCurve OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCurve
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c38e3d5fe35e994afa4b5d8b91c4244573132c5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301354"
---
# <a name="glunurbscurve-function"></a><span data-ttu-id="d894a-104">gluNurbsCurve (funzione)</span><span class="sxs-lookup"><span data-stu-id="d894a-104">gluNurbsCurve function</span></span>

<span data-ttu-id="d894a-105">La funzione **gluNurbsCurve** definisce la forma di una curva B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) razionale non uniforme.</span><span class="sxs-lookup"><span data-stu-id="d894a-105">The **gluNurbsCurve** function defines the shape of a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) curve.</span></span>

## <a name="syntax"></a><span data-ttu-id="d894a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d894a-106">Syntax</span></span>


```C++
void WINAPI gluNurbsCurve(
   GLUnurbs *nobj,
   GLint    nknots,
   GLfloat  *knot,
   GLint    stride,
   GLfloat  *ctlarray,
   GLint    order,
   GLenum   type
);
```



## <a name="parameters"></a><span data-ttu-id="d894a-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d894a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d894a-108">*juje*</span><span class="sxs-lookup"><span data-stu-id="d894a-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="d894a-109">Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="d894a-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d894a-110">*nknots*</span><span class="sxs-lookup"><span data-stu-id="d894a-110">*nknots*</span></span> 
</dt> <dd>

<span data-ttu-id="d894a-111">Numero di nodi nel *nodo*.</span><span class="sxs-lookup"><span data-stu-id="d894a-111">The number of knots in *knot*.</span></span> <span data-ttu-id="d894a-112">Il parametro *nknots* è uguale al numero di punti di controllo più l'ordine.</span><span class="sxs-lookup"><span data-stu-id="d894a-112">The *nknots* parameter equals the number of control points plus the order.</span></span>

</dd> <dt>

<span data-ttu-id="d894a-113">*forma*</span><span class="sxs-lookup"><span data-stu-id="d894a-113">*knot*</span></span> 
</dt> <dd>

<span data-ttu-id="d894a-114">Matrice di valori dei nodi nondecreasing di *nknots* .</span><span class="sxs-lookup"><span data-stu-id="d894a-114">An array of *nknots* nondecreasing knot values.</span></span>

</dd> <dt>

<span data-ttu-id="d894a-115">*stride*</span><span class="sxs-lookup"><span data-stu-id="d894a-115">*stride*</span></span> 
</dt> <dd>

<span data-ttu-id="d894a-116">Offset (come numero di valori a virgola mobile e precisione singola) tra i punti di controllo della curva successiva.</span><span class="sxs-lookup"><span data-stu-id="d894a-116">The offset (as a number of single-precision floating-point values) between successive curve control points.</span></span>

</dd> <dt>

<span data-ttu-id="d894a-117">*ctlarray*</span><span class="sxs-lookup"><span data-stu-id="d894a-117">*ctlarray*</span></span> 
</dt> <dd>

<span data-ttu-id="d894a-118">Puntatore a una matrice di punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="d894a-118">A pointer to an array of control points.</span></span> <span data-ttu-id="d894a-119">Le coordinate devono accettare il *tipo*.</span><span class="sxs-lookup"><span data-stu-id="d894a-119">The coordinates must agree with *type*.</span></span>

</dd> <dt>

<span data-ttu-id="d894a-120">*order*</span><span class="sxs-lookup"><span data-stu-id="d894a-120">*order*</span></span> 
</dt> <dd>

<span data-ttu-id="d894a-121">Ordine della curva NURBS.</span><span class="sxs-lookup"><span data-stu-id="d894a-121">The order of the NURBS curve.</span></span> <span data-ttu-id="d894a-122">Il parametro *Order* è uguale al grado + 1; di conseguenza, una curva cubica ha un ordine di 4.</span><span class="sxs-lookup"><span data-stu-id="d894a-122">The *order* parameter equals degree + 1; hence a cubic curve has an order of 4.</span></span>

</dd> <dt>

<span data-ttu-id="d894a-123">*type*</span><span class="sxs-lookup"><span data-stu-id="d894a-123">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="d894a-124">Tipo della curva.</span><span class="sxs-lookup"><span data-stu-id="d894a-124">The type of the curve.</span></span> <span data-ttu-id="d894a-125">Se questa curva è definita all'interno di una coppia [**gluBeginCurve**](glubegincurve.md) / [**gluEndCurve**](gluendcurve.md) , il tipo può essere uno qualsiasi dei tipi di analizzatore unidimensionali validi, ad esempio GL \_ Mappa1 \_ Vertex \_ 3 o GL \_ Mappa1 \_ Color \_ 4.</span><span class="sxs-lookup"><span data-stu-id="d894a-125">If this curve is defined within a [**gluBeginCurve**](glubegincurve.md)/[**gluEndCurve**](gluendcurve.md) pair, then the type can be any of the valid one-dimensional evaluator types (such as GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_COLOR\_4).</span></span> <span data-ttu-id="d894a-126">Tra una coppia [**gluBeginTrim**](glubegintrim.md) / [**gluEndTrim**](gluendtrim.md) , gli unici tipi validi sono Glu \_ Mappa1 \_ Trim \_ 2 e Glu \_ Mappa1 \_ Trim \_ 3.</span><span class="sxs-lookup"><span data-stu-id="d894a-126">Between a [**gluBeginTrim**](glubegintrim.md)/[**gluEndTrim**](gluendtrim.md) pair, the only valid types are GLU\_MAP1\_TRIM\_2 and GLU\_MAP1\_TRIM\_3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d894a-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d894a-127">Return value</span></span>

<span data-ttu-id="d894a-128">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="d894a-128">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d894a-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="d894a-129">Remarks</span></span>

<span data-ttu-id="d894a-130">Quando **gluNurbsCurve** viene visualizzato tra una coppia **gluBeginCurve** / **gluEndCurve** , descrive una curva di cui eseguire il rendering.</span><span class="sxs-lookup"><span data-stu-id="d894a-130">When **gluNurbsCurve** appears between a **gluBeginCurve**/**gluEndCurve** pair, it describes a curve to be rendered.</span></span> <span data-ttu-id="d894a-131">Si associano le coordinate posizionali, di trama e di colore presentando ciascuna come **gluNurbsCurve** distinta tra una coppia **gluBeginCurve** / **gluEndCurve** .</span><span class="sxs-lookup"><span data-stu-id="d894a-131">You associate positional, texture, and color coordinates by presenting each as a separate **gluNurbsCurve** between a **gluBeginCurve**/**gluEndCurve** pair.</span></span> <span data-ttu-id="d894a-132">Non eseguire più di una chiamata a **gluNurbsCurve** per i dati di colore, posizione e trama all'interno di una singola coppia di  / **gluEndCurve** gluBeginCurve.</span><span class="sxs-lookup"><span data-stu-id="d894a-132">Do not make more than one call to **gluNurbsCurve** for color, position, and texture data within a single **gluBeginCurve**/**gluEndCurve** pair.</span></span> <span data-ttu-id="d894a-133">Eseguire esattamente una chiamata per descrivere la posizione della curva (un *tipo* di GL \_ Mappa1 \_ Vertex \_ 3 o GL \_ Mappa1 \_ Vertex \_ 4).</span><span class="sxs-lookup"><span data-stu-id="d894a-133">Make exactly one call to describe the position of the curve (a *type* of GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4).</span></span>

<span data-ttu-id="d894a-134">Quando **gluNurbsCurve** viene visualizzato tra una coppia [**gluBeginTrim**](glubegintrim.md) / [**gluEndTrim**](gluendtrim.md) , descrive una curva di trimming su una superficie NURBS.</span><span class="sxs-lookup"><span data-stu-id="d894a-134">When **gluNurbsCurve** appears between a [**gluBeginTrim**](glubegintrim.md)/[**gluEndTrim**](gluendtrim.md) pair, it describes a trimming curve on a NURBS surface.</span></span> <span data-ttu-id="d894a-135">Se *Type* è Glu \_ Mappa1 \_ Trim \_ 2, descrive una curva nello spazio di parametri bidimensionali (*u* e *v*).</span><span class="sxs-lookup"><span data-stu-id="d894a-135">If *type* is GLU\_MAP1\_TRIM\_2, it describes a curve in two-dimensional (*u* and *v*) parameter space.</span></span> <span data-ttu-id="d894a-136">Se è GLU \_ Mappa1 \_ Trim \_ 3, descrive una curva in uno spazio di parametri omogeneo (*u*, *v* e *w*) bidimensionale.</span><span class="sxs-lookup"><span data-stu-id="d894a-136">If it is GLU\_MAP1\_TRIM\_3, it describes a curve in two-dimensional homogeneous (*u*, *v*, and *w*) parameter space.</span></span> <span data-ttu-id="d894a-137">Per ulteriori informazioni sulle curve di trimming, vedere **gluBeginTrim**.</span><span class="sxs-lookup"><span data-stu-id="d894a-137">For more discussion about trimming curves, see **gluBeginTrim**.</span></span>

## <a name="examples"></a><span data-ttu-id="d894a-138">Esempio</span><span class="sxs-lookup"><span data-stu-id="d894a-138">Examples</span></span>

<span data-ttu-id="d894a-139">Le funzioni seguenti eseguono il rendering di una curva NURBS con trama con normali:</span><span class="sxs-lookup"><span data-stu-id="d894a-139">The following functions render a textured NURBS curve with normals:</span></span>

``` syntax
gluBeginCurve(nobj); 
    gluNurbsCurve(nobj, ..., GL_MAP1_TEXTURE_COORD_2); 
    gluNurbsCurve(nobj, ..., GL_MAP1_NORMAL); 
    gluNurbsCurve(nobj, ..., GL_MAP1_VERTEX_4);  
gluEndCurve(nobj); 
```

## <a name="requirements"></a><span data-ttu-id="d894a-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d894a-140">Requirements</span></span>



| <span data-ttu-id="d894a-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="d894a-141">Requirement</span></span> | <span data-ttu-id="d894a-142">Valore</span><span class="sxs-lookup"><span data-stu-id="d894a-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d894a-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d894a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d894a-144">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d894a-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d894a-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d894a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d894a-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d894a-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d894a-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d894a-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="d894a-148"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="d894a-148"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="d894a-149">Libreria</span><span class="sxs-lookup"><span data-stu-id="d894a-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="d894a-150"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d894a-150"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d894a-151">DLL</span><span class="sxs-lookup"><span data-stu-id="d894a-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d894a-152"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d894a-152"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d894a-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d894a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d894a-154">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="d894a-154">**gluBeginCurve**</span></span>](glubegincurve.md)
</dt> <dt>

[<span data-ttu-id="d894a-155">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="d894a-155">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="d894a-156">**gluEndCurve**</span><span class="sxs-lookup"><span data-stu-id="d894a-156">**gluEndCurve**</span></span>](gluendcurve.md)
</dt> <dt>

[<span data-ttu-id="d894a-157">**gluEndTrim**</span><span class="sxs-lookup"><span data-stu-id="d894a-157">**gluEndTrim**</span></span>](gluendtrim.md)
</dt> <dt>

[<span data-ttu-id="d894a-158">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="d894a-158">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="d894a-159">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="d894a-159">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





