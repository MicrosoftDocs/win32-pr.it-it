---
title: funzione gluNurbsSurface (Glu. h)
description: La funzione gluNurbsSurface definisce la forma di una superficie NURBS (B-spline) razionale non uniforme.
ms.assetid: ee86376c-26ba-49a9-b0b0-4ca936b6614b
keywords:
- funzione gluNurbsSurface OpenGL
topic_type:
- apiref
api_name:
- gluNurbsSurface
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c784741eded406a49bba90f67544a406ab024a6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963734"
---
# <a name="glunurbssurface-function"></a><span data-ttu-id="2d79c-104">gluNurbsSurface (funzione)</span><span class="sxs-lookup"><span data-stu-id="2d79c-104">gluNurbsSurface function</span></span>

<span data-ttu-id="2d79c-105">La funzione **gluNurbsSurface** definisce la forma di una superficie [NURBS](using-nurbs-curves-and-surfaces.md)(B-spline) razionale non uniforme.</span><span class="sxs-lookup"><span data-stu-id="2d79c-105">The **gluNurbsSurface** function defines the shape of a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d79c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d79c-106">Syntax</span></span>


```C++
void WINAPI gluNurbsSurface(
   GLUnurbs *nobj,
   GLint    sknot_count,
   float    *sknot,
   GLint    tknot_count,
   GLfloat  *tknot,
   GLint    s_stride,
   GLint    t_stride,
   GLfloat  *ctlarray,
   GLint    sorder,
   GLint    torder,
   GLenum   type
);
```



## <a name="parameters"></a><span data-ttu-id="2d79c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d79c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d79c-108">*juje*</span><span class="sxs-lookup"><span data-stu-id="2d79c-108">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="2d79c-109">Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="2d79c-109">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> <dt>

<span data-ttu-id="2d79c-110">*\_conteggio sknot*</span><span class="sxs-lookup"><span data-stu-id="2d79c-110">*sknot\_count*</span></span> 
</dt> <dd>

<span data-ttu-id="2d79c-111">Numero di nodi nella direzione di *u* parametrica.</span><span class="sxs-lookup"><span data-stu-id="2d79c-111">The number of knots in the parametric *u* direction.</span></span>

</dd> <dt>

<span data-ttu-id="2d79c-112">*sknot*</span><span class="sxs-lookup"><span data-stu-id="2d79c-112">*sknot*</span></span> 
</dt> <dd>

<span data-ttu-id="2d79c-113">Una matrice di *sknot \_ count* nondecreasing Knot values nella direzione parametrica *u* .</span><span class="sxs-lookup"><span data-stu-id="2d79c-113">An array of *sknot\_count* nondecreasing knot values in the parametric *u* direction.</span></span>

</dd> <dt>

<span data-ttu-id="2d79c-114">*\_conteggio tknot*</span><span class="sxs-lookup"><span data-stu-id="2d79c-114">*tknot\_count*</span></span> 
</dt> <dd>

<span data-ttu-id="2d79c-115">Numero di nodi nella direzione della *v* parametrica.</span><span class="sxs-lookup"><span data-stu-id="2d79c-115">The number of knots in the parametric *v* direction.</span></span>

</dd> <dt>

<span data-ttu-id="2d79c-116">*tknot*</span><span class="sxs-lookup"><span data-stu-id="2d79c-116">*tknot*</span></span> 
</dt> <dd>

<span data-ttu-id="2d79c-117">Una matrice di *tknot \_ count* nondecreasing Knot values nella direzione parametrica *v* .</span><span class="sxs-lookup"><span data-stu-id="2d79c-117">An array of *tknot\_count* nondecreasing knot values in the parametric *v* direction.</span></span>

</dd> <dt>

<span data-ttu-id="2d79c-118">*\_stride s*</span><span class="sxs-lookup"><span data-stu-id="2d79c-118">*s\_stride*</span></span> 
</dt> <dd>

<span data-ttu-id="2d79c-119">Offset (sotto forma di numero di singoli valori del punto di precisionfloating) tra punti di controllo successivi nella direzione *u* parametrica in *ctlarray*.</span><span class="sxs-lookup"><span data-stu-id="2d79c-119">The offset (as a number of single precisionfloating-point values) between successive control points in the parametric *u* direction in *ctlarray*.</span></span>

</dd> <dt>

<span data-ttu-id="2d79c-120">*t \_ stride*</span><span class="sxs-lookup"><span data-stu-id="2d79c-120">*t\_stride*</span></span> 
</dt> <dd>

<span data-ttu-id="2d79c-121">Offset (nei singoli valori del punto di precisionfloating) tra i punti di controllo successivi nella direzione parametrica *v* in *ctlarray*.</span><span class="sxs-lookup"><span data-stu-id="2d79c-121">The offset (in single precisionfloating-point values) between successive control points in the parametric *v* direction in *ctlarray*.</span></span>

</dd> <dt>

<span data-ttu-id="2d79c-122">*ctlarray*</span><span class="sxs-lookup"><span data-stu-id="2d79c-122">*ctlarray*</span></span> 
</dt> <dd>

<span data-ttu-id="2d79c-123">Matrice contenente i punti di controllo per la superficie NURBS.</span><span class="sxs-lookup"><span data-stu-id="2d79c-123">An array containing control points for the NURBS surface.</span></span> <span data-ttu-id="2d79c-124">Gli offset tra i punti di controllo successivi nelle direzioni parametriche *u* e *v* sono forniti da *s \_ stride* e *t \_ stride*.</span><span class="sxs-lookup"><span data-stu-id="2d79c-124">The offsets between successive control points in the parametric *u* and *v* directions are given by *s\_stride* and *t\_stride*.</span></span>

</dd> <dt>

<span data-ttu-id="2d79c-125">*sorder*</span><span class="sxs-lookup"><span data-stu-id="2d79c-125">*sorder*</span></span> 
</dt> <dd>

<span data-ttu-id="2d79c-126">Ordine della superficie NURBS nella direzione di *u* parametrica.</span><span class="sxs-lookup"><span data-stu-id="2d79c-126">The order of the NURBS surface in the parametric *u* direction.</span></span> <span data-ttu-id="2d79c-127">L'ordine è uno più del grado, quindi una superficie cubica in *u* ha un ordine *u* di 4.</span><span class="sxs-lookup"><span data-stu-id="2d79c-127">The order is one more than the degree, hence a surface that is cubic in *u* has a *u* order of 4.</span></span>

</dd> <dt>

<span data-ttu-id="2d79c-128">*torder*</span><span class="sxs-lookup"><span data-stu-id="2d79c-128">*torder*</span></span> 
</dt> <dd>

<span data-ttu-id="2d79c-129">Ordine della superficie NURBS nella direzione della *v* parametrica.</span><span class="sxs-lookup"><span data-stu-id="2d79c-129">The order of the NURBS surface in the parametric *v* direction.</span></span> <span data-ttu-id="2d79c-130">L'ordine è uno più del grado, quindi una superficie cubica in *v* ha un ordine *v* pari a 4.</span><span class="sxs-lookup"><span data-stu-id="2d79c-130">The order is one more than the degree, hence a surface that is cubic in *v* has a *v* order of 4.</span></span>

</dd> <dt>

<span data-ttu-id="2d79c-131">*type*</span><span class="sxs-lookup"><span data-stu-id="2d79c-131">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="2d79c-132">Tipo della superficie.</span><span class="sxs-lookup"><span data-stu-id="2d79c-132">The type of the surface.</span></span> <span data-ttu-id="2d79c-133">Il parametro di *tipo* può essere qualsiasi tipo di analizzatore bidimensionale valido, ad esempio GL \_ map2 \_ Vertex \_ 3 o GL \_ map2 \_ Color \_ 4.</span><span class="sxs-lookup"><span data-stu-id="2d79c-133">The *type* parameter can be any of the valid two-dimensional evaluator types (such as GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_COLOR\_4).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d79c-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d79c-134">Return value</span></span>

<span data-ttu-id="2d79c-135">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="2d79c-135">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d79c-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d79c-136">Remarks</span></span>

<span data-ttu-id="2d79c-137">Utilizzare **gluNurbsSurface** all'interno di una definizione di superficie NURBS per descrivere la forma di una superficie NURBS (prima di qualsiasi taglio).</span><span class="sxs-lookup"><span data-stu-id="2d79c-137">Use **gluNurbsSurface** within a NURBS surface definition to describe the shape of a NURBS surface (before any trimming).</span></span> <span data-ttu-id="2d79c-138">Per contrassegnare l'inizio di una definizione di superficie NURBS, utilizzare la funzione [**gluBeginSurface**](glubeginsurface.md) .</span><span class="sxs-lookup"><span data-stu-id="2d79c-138">To mark the beginning of a NURBS surface definition, use the [**gluBeginSurface**](glubeginsurface.md) function.</span></span> <span data-ttu-id="2d79c-139">Per contrassegnare la fine di una definizione di superficie NURBS, utilizzare la funzione [**gluEndSurface**](gluendsurface.md) .</span><span class="sxs-lookup"><span data-stu-id="2d79c-139">To mark the end of a NURBS surface definition, use the [**gluEndSurface**](gluendsurface.md) function.</span></span> <span data-ttu-id="2d79c-140">Chiamare **gluNurbsSurface** solo all'interno di una definizione di superficie NURBS.</span><span class="sxs-lookup"><span data-stu-id="2d79c-140">Call **gluNurbsSurface** within a NURBS surface definition only.</span></span>

<span data-ttu-id="2d79c-141">Si associano le coordinate posizionali, di trama e di colore a una superficie presentando ognuno come **gluNurbsSurface** separato tra una coppia di  / **gluEndSurface** gluBeginSurface.</span><span class="sxs-lookup"><span data-stu-id="2d79c-141">You associate positional, texture, and color coordinates with a surface by presenting each as a separate **gluNurbsSurface** between a **gluBeginSurface**/**gluEndSurface** pair.</span></span> <span data-ttu-id="2d79c-142">All'interno di una singola coppia **gluBeginSurface** / **gluEndSurface** , è possibile effettuare una sola chiamata a **gluNurbsSurface** per i dati di colore, posizione e trama.</span><span class="sxs-lookup"><span data-stu-id="2d79c-142">Within a single **gluBeginSurface**/**gluEndSurface** pair, you can make only one call to **gluNurbsSurface** for color, position, and texture data.</span></span> <span data-ttu-id="2d79c-143">Eseguire esattamente una chiamata per descrivere la posizione della superficie (un *tipo* di GL \_ map2 \_ Vertex \_ 3 o GL \_ map2 \_ Vertex \_ 4).</span><span class="sxs-lookup"><span data-stu-id="2d79c-143">Make exactly one call to describe the position of the surface (a *type* of GL\_MAP2\_VERTEX\_3 or GL\_MAP2\_VERTEX\_4).</span></span>

<span data-ttu-id="2d79c-144">È possibile tagliare una superficie NURBS usando le funzioni [**gluNurbsCurve**](glunurbscurve.md) e [**gluPwlCurve**](glupwlcurve.md) tra le chiamate a [**gluBeginTrim**](glubegintrim.md) e [**gluEndTrim**](gluendtrim.md).</span><span class="sxs-lookup"><span data-stu-id="2d79c-144">You can trim a NURBS surface by using the [**gluNurbsCurve**](glunurbscurve.md) and [**gluPwlCurve**](glupwlcurve.md) functions between calls to [**gluBeginTrim**](glubegintrim.md) and [**gluEndTrim**](gluendtrim.md).</span></span>

<span data-ttu-id="2d79c-145">Un **gluNurbsSurface** con *sknot \_ numero* di nodi nella direzione *u* e i nodi *\_ conteggio tknot* nella direzione *v* con Orders *sorder* e *torder* devono avere (*sknot \_ count*  - *sorder*) multipied by (*tknot \_ count*  - *torder*) punti di controllo.</span><span class="sxs-lookup"><span data-stu-id="2d79c-145">A **gluNurbsSurface** with *sknot\_count* knots in the *u* direction and *tknot\_count* knots in the *v* direction with orders *sorder* and *torder* must have (*sknot\_count* -*sorder*) multipied by (*tknot\_count* -*torder*) control points.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d79c-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d79c-146">Requirements</span></span>



| <span data-ttu-id="2d79c-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d79c-147">Requirement</span></span> | <span data-ttu-id="2d79c-148">Valore</span><span class="sxs-lookup"><span data-stu-id="2d79c-148">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2d79c-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d79c-149">Minimum supported client</span></span><br/> | <span data-ttu-id="2d79c-150">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2d79c-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2d79c-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d79c-151">Minimum supported server</span></span><br/> | <span data-ttu-id="2d79c-152">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2d79c-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2d79c-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d79c-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d79c-154"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d79c-154"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="2d79c-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="2d79c-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="2d79c-156"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d79c-156"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2d79c-157">DLL</span><span class="sxs-lookup"><span data-stu-id="2d79c-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d79c-158"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d79c-158"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d79c-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2d79c-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d79c-160">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="2d79c-160">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="2d79c-161">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="2d79c-161">**gluBeginTrim**</span></span>](glubegintrim.md)
</dt> <dt>

[<span data-ttu-id="2d79c-162">**gluEndSurface**</span><span class="sxs-lookup"><span data-stu-id="2d79c-162">**gluEndSurface**</span></span>](gluendsurface.md)
</dt> <dt>

[<span data-ttu-id="2d79c-163">**gluEndTrim**</span><span class="sxs-lookup"><span data-stu-id="2d79c-163">**gluEndTrim**</span></span>](gluendtrim.md)
</dt> <dt>

[<span data-ttu-id="2d79c-164">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="2d79c-164">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="2d79c-165">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="2d79c-165">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> <dt>

[<span data-ttu-id="2d79c-166">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="2d79c-166">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





