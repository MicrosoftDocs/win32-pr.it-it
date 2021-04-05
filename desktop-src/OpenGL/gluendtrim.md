---
title: funzione gluEndTrim (Glu. h)
description: Le funzioni gluBeginTrim e gluEndTrim delimitano una definizione del ciclo di taglio razionale B-spline (NURBS) non uniforme. | funzione gluEndTrim (Glu. h)
ms.assetid: e85cc60b-4492-441d-b778-31a3d52b398a
keywords:
- funzione gluEndTrim OpenGL
topic_type:
- apiref
api_name:
- gluEndTrim
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4105cc911105f0444ba17c6b57a3deb048bc96d2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104058526"
---
# <a name="gluendtrim-function"></a><span data-ttu-id="87c79-105">gluEndTrim (funzione)</span><span class="sxs-lookup"><span data-stu-id="87c79-105">gluEndTrim function</span></span>

<span data-ttu-id="87c79-106">Le funzioni [**gluBeginTrim**](glubegintrim.md) e **gluEndTrim** delimitano una definizione del ciclo di taglio razionale B-spline ([NURBS](using-nurbs-curves-and-surfaces.md)) non uniforme.</span><span class="sxs-lookup"><span data-stu-id="87c79-106">The [**gluBeginTrim**](glubegintrim.md) and **gluEndTrim** functions delimit a Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)) trimming loop definition.</span></span>

## <a name="syntax"></a><span data-ttu-id="87c79-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87c79-107">Syntax</span></span>


```C++
void WINAPI gluEndTrim(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a><span data-ttu-id="87c79-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="87c79-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87c79-109">*juje*</span><span class="sxs-lookup"><span data-stu-id="87c79-109">*nobj*</span></span> 
</dt> <dd>

<span data-ttu-id="87c79-110">Oggetto NURBS (creato con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span><span class="sxs-lookup"><span data-stu-id="87c79-110">The NURBS object (created with [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87c79-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="87c79-111">Return value</span></span>

<span data-ttu-id="87c79-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="87c79-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87c79-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="87c79-113">Remarks</span></span>

<span data-ttu-id="87c79-114">Usare [**gluBeginTrim**](glubegintrim.md) per contrassegnare l'inizio di un ciclo di trimming e **gluEndTrim** per contrassegnare la fine di un ciclo di taglio.</span><span class="sxs-lookup"><span data-stu-id="87c79-114">Use [**gluBeginTrim**](glubegintrim.md) to mark the beginning of a trimming loop, and **gluEndTrim** to mark the end of a trimming loop.</span></span> <span data-ttu-id="87c79-115">Un ciclo di taglio è un set di segmenti orientati a curva (forma di curva chiusa) che definiscono i limiti di una superficie NURBS.</span><span class="sxs-lookup"><span data-stu-id="87c79-115">A trimming loop is a set of oriented curve segments (forming a closed curve) that define boundaries of a NURBS surface.</span></span> <span data-ttu-id="87c79-116">Includere questi cicli di taglio nella definizione di una superficie NURBS, tra le chiamate a [**gluBeginSurface**](glubeginsurface.md) e [**gluEndSurface**](gluendsurface.md).</span><span class="sxs-lookup"><span data-stu-id="87c79-116">You include these trimming loops in the definition of a NURBS surface, between calls to [**gluBeginSurface**](glubeginsurface.md) and [**gluEndSurface**](gluendsurface.md).</span></span>

<span data-ttu-id="87c79-117">La definizione di una superficie NURBS può contenere molti cicli di trimming.</span><span class="sxs-lookup"><span data-stu-id="87c79-117">The definition for a NURBS surface can contain many trimming loops.</span></span> <span data-ttu-id="87c79-118">Se, ad esempio, si scrive una definizione per una superficie NURBS simile a un rettangolo con un foro punzonato, la definizione conterrebbe due cicli di trimming.</span><span class="sxs-lookup"><span data-stu-id="87c79-118">For example, if you write a definition for a NURBS surface that resembles a rectangle with a hole punched out, the definition would contain two trimming loops.</span></span> <span data-ttu-id="87c79-119">Un ciclo definisce il bordo esterno del rettangolo. l'altro definisce il foro punzonato.</span><span class="sxs-lookup"><span data-stu-id="87c79-119">One loop would define the outer edge of the rectangle; the other would define the punched-out hole.</span></span> <span data-ttu-id="87c79-120">Le definizioni di ognuno di questi cicli di taglio sono racchiuse tra parentesi [](glubegintrim.md)da una coppia di  /  **gluEndTrim** gluBeginTrim.</span><span class="sxs-lookup"><span data-stu-id="87c79-120">The definitions of each of these trimming loops would be bracketed by a [**gluBeginTrim**](glubegintrim.md) / **gluEndTrim** pair.</span></span>

<span data-ttu-id="87c79-121">La definizione di un singolo ciclo di taglio chiuso può essere costituita da più segmenti di curva, ciascuno dei quali viene descritto come una serie di segmenti lineari che formano una curva lineare (vedere [**gluPwlCurve**](glupwlcurve.md)), come una singola curva NURBS (vedere [**gluNurbsCurve**](glunurbscurve.md)) o come una combinazione di entrambi in qualsiasi ordine.</span><span class="sxs-lookup"><span data-stu-id="87c79-121">The definition of a single closed trimming loop can consist of multiple curve segments, each described as a series of line segments that form a linear curve (see [**gluPwlCurve**](glupwlcurve.md)), as a single NURBS curve (see [**gluNurbsCurve**](glunurbscurve.md)), or as a combination of both in any order.</span></span> <span data-ttu-id="87c79-122">Le uniche chiamate di libreria che possono essere visualizzate in una definizione del ciclo di Trimming (tra le chiamate a [**gluBeginTrim**](glubegintrim.md) e **GluEndTrim**) sono **gluPwlCurve** e **gluNurbsCurve**.</span><span class="sxs-lookup"><span data-stu-id="87c79-122">The only library calls that can appear in a trimming-loop definition (between the calls to [**gluBeginTrim**](glubegintrim.md) and **gluEndTrim**) are **gluPwlCurve** and **gluNurbsCurve**.</span></span>

<span data-ttu-id="87c79-123">L'area visualizzata della superficie NURBS è l'area del dominio a sinistra della curva di taglio Man mano che aumenta il parametro della curva.</span><span class="sxs-lookup"><span data-stu-id="87c79-123">The displayed area of the NURBS surface is the region in the domain to the left of the trimming curve as the curve parameter increases.</span></span> <span data-ttu-id="87c79-124">Pertanto, l'area mantenuta della superficie NURBS si trova all'interno di un ciclo di trimming in senso antiorario e al di fuori di un ciclo di taglio</span><span class="sxs-lookup"><span data-stu-id="87c79-124">Thus, the retained region of the NURBS surface is inside a counterclockwise trimming loop and outside a clockwise trimming loop.</span></span> <span data-ttu-id="87c79-125">Per il rettangolo indicato in precedenza, il ciclo di taglio per il bordo esterno del rettangolo viene eseguito in senso antiorario, mentre il ciclo di taglio per il foro punzonato viene eseguito in senso orario.</span><span class="sxs-lookup"><span data-stu-id="87c79-125">For the rectangle mentioned earlier, the trimming loop for the outer edge of the rectangle runs counterclockwise, while the trimming loop for the punched-out hole runs clockwise.</span></span>

<span data-ttu-id="87c79-126">Se si usa più di una curva per definire un singolo ciclo di taglio, i segmenti di curva devono formare un ciclo chiuso (ovvero, l'endpoint di ogni curva deve essere il punto iniziale della curva successiva e l'endpoint della curva finale deve essere il punto iniziale della prima curva).</span><span class="sxs-lookup"><span data-stu-id="87c79-126">If you use more than one curve to define a single trimming loop, the curve segments must form a closed loop (that is, the endpoint of each curve must be the starting point of the next curve, and the endpoint of the final curve must be the starting point of the first curve).</span></span> <span data-ttu-id="87c79-127">Se gli endpoint della curva sono sufficientemente vicini, ma non esattamente coincidenti, saranno costretti a trovare una corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="87c79-127">If the endpoints of the curve are sufficiently close together but not exactly coincident, they will be forced to match.</span></span> <span data-ttu-id="87c79-128">Se gli endpoint non sono sufficientemente vicini, viene restituito un errore (vedere [*gluNurbsCallback*](glunurbs.md)).</span><span class="sxs-lookup"><span data-stu-id="87c79-128">If the endpoints are not sufficiently close, an error results (see [*gluNurbsCallback*](glunurbs.md)).</span></span>

<span data-ttu-id="87c79-129">Se una definizione del ciclo di trimming contiene più curve, la direzione delle curve deve essere coerente, ovvero l'interno deve trovarsi a sinistra di tutte le curve.</span><span class="sxs-lookup"><span data-stu-id="87c79-129">If a trimming-loop definition contains multiple curves, the direction of the curves must be consistent (that is, the inside must be to the left of all of the curves).</span></span> <span data-ttu-id="87c79-130">È possibile usare i cicli di trimming nidificati purché gli orientamenti della curva si alternano correttamente.</span><span class="sxs-lookup"><span data-stu-id="87c79-130">You can use nested trimming loops as long as the curve orientations alternate correctly.</span></span> <span data-ttu-id="87c79-131">Le curve di trimming non possono essere autointersecate, né possono intersecarsi tra loro (o risultati di errore).</span><span class="sxs-lookup"><span data-stu-id="87c79-131">Trimming curves cannot be self-intersecting, nor can they intersect one another (or an error results).</span></span>

<span data-ttu-id="87c79-132">Se per una superficie NURBS non vengono fornite informazioni di taglio, viene disegnata l'intera superficie.</span><span class="sxs-lookup"><span data-stu-id="87c79-132">If no trimming information is given for a NURBS surface, the entire surface is drawn.</span></span>

## <a name="examples"></a><span data-ttu-id="87c79-133">Esempio</span><span class="sxs-lookup"><span data-stu-id="87c79-133">Examples</span></span>

<span data-ttu-id="87c79-134">Questo frammento di codice definisce un ciclo di trimming costituito da una curva lineare a tratti e due curve NURBS:</span><span class="sxs-lookup"><span data-stu-id="87c79-134">This code fragment defines a trimming loop that consists of one piecewise linear curve and two NURBS curves:</span></span>

``` syntax
gluBeginTrim(nobj); 
    gluPwlCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_2); 
    gluNurbsCurve(. . ., GLU_MAP1_TRIM_3);  
gluEndTrim(nobj);
```

## <a name="requirements"></a><span data-ttu-id="87c79-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87c79-135">Requirements</span></span>



| <span data-ttu-id="87c79-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="87c79-136">Requirement</span></span> | <span data-ttu-id="87c79-137">Valore</span><span class="sxs-lookup"><span data-stu-id="87c79-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="87c79-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87c79-138">Minimum supported client</span></span><br/> | <span data-ttu-id="87c79-139">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="87c79-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="87c79-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87c79-140">Minimum supported server</span></span><br/> | <span data-ttu-id="87c79-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="87c79-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="87c79-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87c79-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="87c79-143"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="87c79-143"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="87c79-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="87c79-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="87c79-145"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87c79-145"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="87c79-146">DLL</span><span class="sxs-lookup"><span data-stu-id="87c79-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87c79-147"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87c79-147"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87c79-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87c79-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87c79-149">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="87c79-149">**gluBeginSurface**</span></span>](glubeginsurface.md)
</dt> <dt>

[<span data-ttu-id="87c79-150">**gluEndSurface**</span><span class="sxs-lookup"><span data-stu-id="87c79-150">**gluEndSurface**</span></span>](gluendsurface.md)
</dt> <dt>

[<span data-ttu-id="87c79-151">**gluNewNurbsRenderer**</span><span class="sxs-lookup"><span data-stu-id="87c79-151">**gluNewNurbsRenderer**</span></span>](glunewnurbsrenderer.md)
</dt> <dt>

[<span data-ttu-id="87c79-152">*gluNurbsCallback*</span><span class="sxs-lookup"><span data-stu-id="87c79-152">*gluNurbsCallback*</span></span>](glunurbs.md)
</dt> <dt>

[<span data-ttu-id="87c79-153">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="87c79-153">**gluNurbsCurve**</span></span>](glunurbscurve.md)
</dt> <dt>

[<span data-ttu-id="87c79-154">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="87c79-154">**gluPwlCurve**</span></span>](glupwlcurve.md)
</dt> </dl>

 

 





