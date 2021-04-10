---
title: funzione gluTessProperty (Glu. h)
description: La funzione gluTessProperty imposta la proprietà di un oggetto a mosaico.
ms.assetid: 1306b9ef-4f1e-4684-99ea-464bae1d0a61
keywords:
- funzione gluTessProperty OpenGL
topic_type:
- apiref
api_name:
- gluTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe21f2961cd4cb1df31a1fdb3f407a71d6e6d68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121250"
---
# <a name="glutessproperty-function"></a><span data-ttu-id="d0adf-104">gluTessProperty (funzione)</span><span class="sxs-lookup"><span data-stu-id="d0adf-104">gluTessProperty function</span></span>

<span data-ttu-id="d0adf-105">La funzione **gluTessProperty** imposta la proprietà di un oggetto a mosaico.</span><span class="sxs-lookup"><span data-stu-id="d0adf-105">The **gluTessProperty** function sets the property of a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0adf-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0adf-106">Syntax</span></span>


```C++
void WINAPI gluTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      value
);
```



## <a name="parameters"></a><span data-ttu-id="d0adf-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0adf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0adf-108">*Tess*</span><span class="sxs-lookup"><span data-stu-id="d0adf-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="d0adf-109">Oggetto a mosaico creato con [**gluNewTess**](glunewtess.md).</span><span class="sxs-lookup"><span data-stu-id="d0adf-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="d0adf-110">*che*</span><span class="sxs-lookup"><span data-stu-id="d0adf-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="d0adf-111">Valore della proprietà da impostare.</span><span class="sxs-lookup"><span data-stu-id="d0adf-111">The property value to set.</span></span> <span data-ttu-id="d0adf-112">Sono validi i valori seguenti: \_ regola di Winding di Glu Tess \_ \_ , Glu \_ Tess \_ \_ solo limite e Glu \_ Tess \_ tolerance.</span><span class="sxs-lookup"><span data-stu-id="d0adf-112">The following values are valid: GLU\_TESS\_WINDING\_RULE, GLU\_TESS\_BOUNDARY\_ONLY, and GLU\_TESS\_TOLERANCE.</span></span>



| <span data-ttu-id="d0adf-113">Valore</span><span class="sxs-lookup"><span data-stu-id="d0adf-113">Value</span></span>                                                                                                                                                                                      | <span data-ttu-id="d0adf-114">Significato</span><span class="sxs-lookup"><span data-stu-id="d0adf-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_TESS_WINDING_RULE"></span><span id="glu_tess_winding_rule"></span><dl> <span data-ttu-id="d0adf-115"><dt>**\_regola di \_ Winding di Glu Tess \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d0adf-115"><dt>**GLU\_TESS\_WINDING\_RULE**</dt></span></span> </dl>    | <span data-ttu-id="d0adf-116">Determina quali parti del poligono sono all'interno.</span><span class="sxs-lookup"><span data-stu-id="d0adf-116">Determines which parts of the polygon are on the interior.</span></span> <span data-ttu-id="d0adf-117">Il parametro value può essere impostato su uno dei seguenti elementi: GLU \_ Tess \_ Winding \_ dispari, Glu \_ Tess \_ Winding \_ diverso da zero, GLU \_ Tess \_ Winding \_ positivo, Glu \_ Tess \_ Winding \_ negativo o Glu \_ Tess \_ Winding \_ ABS \_ GEQ \_ Two.</span><span class="sxs-lookup"><span data-stu-id="d0adf-117">The value parameter may be set to one of the following: GLU\_TESS\_WINDING\_ODD, GLU\_TESS\_WINDING\_NONZERO, GLU\_TESS\_WINDING\_POSITIVE, GLU\_TESS\_WINDING\_NEGATIVE, or GLU\_TESS\_WINDING\_ABS\_GEQ\_TWO.</span></span> <br/> <span data-ttu-id="d0adf-118">Per comprendere il funzionamento della regola di avvolgimento, considerare prima di tutto che i contorni di input partizionano il piano in aree.</span><span class="sxs-lookup"><span data-stu-id="d0adf-118">To understand how the winding rule works, first consider that the input contours partition the plane into regions.</span></span> <span data-ttu-id="d0adf-119">La regola di chiusura determina quali di queste aree sono all'interno del poligono.</span><span class="sxs-lookup"><span data-stu-id="d0adf-119">The winding rule determines which of these regions are inside the polygon.</span></span><br/> <span data-ttu-id="d0adf-120">Per un C a contorno singolo, il numero di serie di un punto x è semplicemente il numero con segno di rivoluzioni che vengono apportate intorno a x mentre si sposta una volta attorno al linguaggio C (in senso antiorario è positivo).</span><span class="sxs-lookup"><span data-stu-id="d0adf-120">For a single-contour C, the winding number of a point x is simply the signed number of revolutions we make around x as we travel once around C (where counterclockwise is positive).</span></span> <span data-ttu-id="d0adf-121">Quando sono presenti diversi contorni, i singoli numeri di avvolgimento vengono sommati.</span><span class="sxs-lookup"><span data-stu-id="d0adf-121">When there are several contours, the individual winding numbers are summed.</span></span> <span data-ttu-id="d0adf-122">Questa procedura associa un valore intero con segno a ogni punto x del piano.</span><span class="sxs-lookup"><span data-stu-id="d0adf-122">This procedure associates a signed integer value with each point x in the plane.</span></span> <span data-ttu-id="d0adf-123">Si noti che il numero di avvolgimento è lo stesso per tutti i punti in una singola area.</span><span class="sxs-lookup"><span data-stu-id="d0adf-123">Note that the winding number is the same for all points in a single region.</span></span><br/> <span data-ttu-id="d0adf-124">La regola di avvolgimento classifica un'area come "interna" Se il numero di avvolgimento appartiene alla categoria scelta (dispari, diverso da zero, positivo, negativo o valore assoluto di almeno due).</span><span class="sxs-lookup"><span data-stu-id="d0adf-124">The winding rule classifies a region as "inside" if its winding number belongs to the chosen category (odd, nonzero, positive, negative, or absolute value of at least two).</span></span> <span data-ttu-id="d0adf-125">La regola mosaico precedente (precedente a GLU 1,2) usava la regola "dispari".</span><span class="sxs-lookup"><span data-stu-id="d0adf-125">The previous GLU tessellator (prior to GLU 1.2) used the "odd" rule.</span></span> <span data-ttu-id="d0adf-126">La regola "diverso da zero" (GLU \_ Tess \_ Winding \_ diverso da zero) è un altro modo comune per definire la parte interna.</span><span class="sxs-lookup"><span data-stu-id="d0adf-126">The "nonzero" rule (GLU\_TESS\_WINDING\_NONZERO) is another common way to define the interior.</span></span> <span data-ttu-id="d0adf-127">Le altre tre regole (GLU \_ Tess \_ Winding \_ positivo, Glu \_ Tess \_ Winding \_ negative, Glu \_ Tess \_ Winding \_ ABS \_ GEQ \_ Two) sono utili per le operazioni di gestione dei poligoni.</span><span class="sxs-lookup"><span data-stu-id="d0adf-127">The other three rules (GLU\_TESS\_WINDING\_POSITIVE, GLU\_TESS\_WINDING\_NEGATIVE, GLU\_TESS\_WINDING\_ABS\_GEQ\_TWO) are useful for polygon CSG operations.</span></span><br/> |
| <span id="GLU_TESS_BOUNDARY_ONLY"></span><span id="glu_tess_boundary_only"></span><dl> <span data-ttu-id="d0adf-128"><dt>**\_ \_ solo limite del \_ solo Glu Tess**</dt></span><span class="sxs-lookup"><span data-stu-id="d0adf-128"><dt>**GLU\_TESS\_BOUNDARY\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="d0adf-129">Specifica un valore booleano (impostare valore su GL \_ true o GL \_ false).</span><span class="sxs-lookup"><span data-stu-id="d0adf-129">Specifies a Boolean value (set value to GL\_TRUE or GL\_FALSE).</span></span> <span data-ttu-id="d0adf-130">Quando si imposta Value su GL \_ true, viene restituito un set di contorni chiusi che separa l'interno e l'esterno del poligono anziché uno a mosaico.</span><span class="sxs-lookup"><span data-stu-id="d0adf-130">When you set value to GL\_TRUE, a set of closed contours separating the polygon interior and exterior is returned instead of a tessellation.</span></span> <span data-ttu-id="d0adf-131">I contorni esterni sono orientati in senso antiorario rispetto alla normale; i contorni interni sono orientati in senso orario.</span><span class="sxs-lookup"><span data-stu-id="d0adf-131">Exterior contours are oriented counterclockwise with respect to the normal; interior contours are oriented clockwise.</span></span> <span data-ttu-id="d0adf-132">\_ \_ \_ \_ Per ogni contorno i callback dei dati Begin Tess Begin e Glu Tess Begin \_ data usano il tipo \_ di riga GL \_ .</span><span class="sxs-lookup"><span data-stu-id="d0adf-132">The GLU\_TESS\_BEGIN and GLU\_TESS\_BEGIN\_DATA callbacks use the type GL\_LINE\_LOOP for each contour.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GLU_TESS_TOLERANCE"></span><span id="glu_tess_tolerance"></span><dl> <span data-ttu-id="d0adf-133"><dt>**\_tolleranza Glu Tess \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d0adf-133"><dt>**GLU\_TESS\_TOLERANCE**</dt></span></span> </dl>              | <span data-ttu-id="d0adf-134">Specifica una tolleranza per l'Unione delle funzionalità per ridurre le dimensioni dell'output.</span><span class="sxs-lookup"><span data-stu-id="d0adf-134">Specifies a tolerance for merging features to reduce the size of the output.</span></span> <span data-ttu-id="d0adf-135">Ad esempio, due vertici che sono molto vicini tra loro possono essere sostituiti da un singolo vertice.</span><span class="sxs-lookup"><span data-stu-id="d0adf-135">For example, two vertexes that are very close to each other might be replaced by a single vertex.</span></span> <span data-ttu-id="d0adf-136">La tolleranza viene moltiplicata per la grandezza della coordinata più grande di qualsiasi vertice di input; Specifica la distanza massima che qualsiasi funzionalità può spostare come risultato di una singola operazione di merge.</span><span class="sxs-lookup"><span data-stu-id="d0adf-136">The tolerance is multiplied by the largest coordinate magnitude of any input vertex; this specifies the maximum distance that any feature can move as the result of a single merge operation.</span></span> <span data-ttu-id="d0adf-137">Se una singola funzionalità partecipa a diverse operazioni di Unione, la distanza totale spostata può essere maggiore.</span><span class="sxs-lookup"><span data-stu-id="d0adf-137">If a single feature takes part in several merge operations, the total distance moved can be larger.</span></span> <br/> <span data-ttu-id="d0adf-138">L'Unione delle funzionalità è completamente facoltativa. la tolleranza è solo un suggerimento.</span><span class="sxs-lookup"><span data-stu-id="d0adf-138">Feature merging is completely optional; the tolerance is only a hint.</span></span> <span data-ttu-id="d0adf-139">È possibile eseguire il merge dell'implementazione in alcuni casi, non in altri, oppure non unire mai le funzionalità.</span><span class="sxs-lookup"><span data-stu-id="d0adf-139">The implementation is free to merge in some cases and not in others, or to never merge features at all.</span></span> <span data-ttu-id="d0adf-140">La tolleranza predefinita è zero.</span><span class="sxs-lookup"><span data-stu-id="d0adf-140">The default tolerance is zero.</span></span><br/> <span data-ttu-id="d0adf-141">L'implementazione corrente unisce i vertici solo se sono esattamente coincidenti, indipendentemente dalla tolleranza corrente.</span><span class="sxs-lookup"><span data-stu-id="d0adf-141">The current implementation merges vertexes only if they are exactly coincident, regardless of the current tolerance.</span></span> <span data-ttu-id="d0adf-142">Un vertice viene inserito in un bordo solo se l'implementazione non è in grado di distinguere il lato del bordo su cui si trova il vertice.</span><span class="sxs-lookup"><span data-stu-id="d0adf-142">A vertex is spliced into an edge only if the implementation is unable to distinguish which side of the edge the vertex lies on.</span></span> <span data-ttu-id="d0adf-143">Due bordi vengono uniti solo quando entrambi gli endpoint sono identici.</span><span class="sxs-lookup"><span data-stu-id="d0adf-143">Two edges are merged only when both endpoints are identical.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="d0adf-144">*value*</span><span class="sxs-lookup"><span data-stu-id="d0adf-144">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="d0adf-145">Valore della proprietà indicata.</span><span class="sxs-lookup"><span data-stu-id="d0adf-145">The value of the indicated property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0adf-146">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0adf-146">Return value</span></span>

<span data-ttu-id="d0adf-147">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="d0adf-147">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0adf-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0adf-148">Remarks</span></span>

<span data-ttu-id="d0adf-149">La funzione **gluTessProperty** controlla le proprietà archiviate in un oggetto a mosaico.</span><span class="sxs-lookup"><span data-stu-id="d0adf-149">The **gluTessProperty** function controls properties stored in a tessellation object.</span></span> <span data-ttu-id="d0adf-150">Queste proprietà influiscono sul modo in cui i poligoni vengono interpretati e sottoposti a rendering.</span><span class="sxs-lookup"><span data-stu-id="d0adf-150">These properties affect the way the polygons are interpreted and rendered.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0adf-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0adf-151">Requirements</span></span>



| <span data-ttu-id="d0adf-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0adf-152">Requirement</span></span> | <span data-ttu-id="d0adf-153">Valore</span><span class="sxs-lookup"><span data-stu-id="d0adf-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d0adf-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0adf-154">Minimum supported client</span></span><br/> | <span data-ttu-id="d0adf-155">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d0adf-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d0adf-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0adf-156">Minimum supported server</span></span><br/> | <span data-ttu-id="d0adf-157">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d0adf-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d0adf-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0adf-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0adf-159"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0adf-159"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="d0adf-160">Libreria</span><span class="sxs-lookup"><span data-stu-id="d0adf-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="d0adf-161"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0adf-161"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="d0adf-162">DLL</span><span class="sxs-lookup"><span data-stu-id="d0adf-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0adf-163"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0adf-163"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0adf-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0adf-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0adf-165">**gluGetTessProperty**</span><span class="sxs-lookup"><span data-stu-id="d0adf-165">**gluGetTessProperty**</span></span>](glugettessproperty.md)
</dt> <dt>

[<span data-ttu-id="d0adf-166">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="d0adf-166">**gluNewTess**</span></span>](glunewtess.md)
</dt> </dl>

 

 





