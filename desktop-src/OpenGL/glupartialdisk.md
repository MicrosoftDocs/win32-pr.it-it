---
title: funzione gluPartialDisk (Glu. h)
description: La funzione gluPartialDisk disegna un arco di un disco.
ms.assetid: 46809c15-88c3-40fa-965a-7aeeedc1c598
keywords:
- funzione gluPartialDisk OpenGL
topic_type:
- apiref
api_name:
- gluPartialDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36e35a6ea905f20e1cb30eddc5b270786614403b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300952"
---
# <a name="glupartialdisk-function"></a><span data-ttu-id="9532b-104">gluPartialDisk (funzione)</span><span class="sxs-lookup"><span data-stu-id="9532b-104">gluPartialDisk function</span></span>

<span data-ttu-id="9532b-105">La funzione **gluPartialDisk** disegna un arco di un disco.</span><span class="sxs-lookup"><span data-stu-id="9532b-105">The **gluPartialDisk** function draws an arc of a disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="9532b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9532b-106">Syntax</span></span>


```C++
void WINAPI gluPartialDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops,
   GLdouble   startAngle,
   GLdouble   sweepAngle
);
```



## <a name="parameters"></a><span data-ttu-id="9532b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9532b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9532b-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="9532b-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="9532b-109">Oggetto quadrica (creato con [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="9532b-109">A quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="9532b-110">*innerRadius*</span><span class="sxs-lookup"><span data-stu-id="9532b-110">*innerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="9532b-111">Raggio interno del disco parziale (può essere zero).</span><span class="sxs-lookup"><span data-stu-id="9532b-111">The inner radius of the partial disk (can be zero).</span></span>

</dd> <dt>

<span data-ttu-id="9532b-112">*outerRadius*</span><span class="sxs-lookup"><span data-stu-id="9532b-112">*outerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="9532b-113">Raggio esterno del disco parziale.</span><span class="sxs-lookup"><span data-stu-id="9532b-113">The outer radius of the partial disk.</span></span>

</dd> <dt>

<span data-ttu-id="9532b-114">*fette*</span><span class="sxs-lookup"><span data-stu-id="9532b-114">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="9532b-115">Numero di suddivisioni intorno all'asse z.</span><span class="sxs-lookup"><span data-stu-id="9532b-115">The number of subdivisions around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="9532b-116">*cicli*</span><span class="sxs-lookup"><span data-stu-id="9532b-116">*loops*</span></span> 
</dt> <dd>

<span data-ttu-id="9532b-117">Numero di anelli concentrici sull'origine in cui è suddiviso il disco parziale.</span><span class="sxs-lookup"><span data-stu-id="9532b-117">The number of concentric rings about the origin into which the partial disk is subdivided.</span></span>

</dd> <dt>

<span data-ttu-id="9532b-118">*startAngle*</span><span class="sxs-lookup"><span data-stu-id="9532b-118">*startAngle*</span></span> 
</dt> <dd>

<span data-ttu-id="9532b-119">Angolo iniziale, in gradi, della parte del disco.</span><span class="sxs-lookup"><span data-stu-id="9532b-119">The starting angle, in degrees, of the disk portion.</span></span>

</dd> <dt>

<span data-ttu-id="9532b-120">*sweepAngle*</span><span class="sxs-lookup"><span data-stu-id="9532b-120">*sweepAngle*</span></span> 
</dt> <dd>

<span data-ttu-id="9532b-121">Angolo dello sweep, in gradi, della parte del disco.</span><span class="sxs-lookup"><span data-stu-id="9532b-121">The sweep angle, in degrees, of the disk portion.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9532b-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9532b-122">Return value</span></span>

<span data-ttu-id="9532b-123">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="9532b-123">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9532b-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="9532b-124">Remarks</span></span>

<span data-ttu-id="9532b-125">La funzione **gluPartialDisk** esegue il rendering di un disco parziale sul piano *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="9532b-125">The **gluPartialDisk** function renders a partial disk on the *z* = 0 plane.</span></span> <span data-ttu-id="9532b-126">Un disco parziale è simile a un disco completo, ad eccezione del fatto che è incluso solo il subset del disco da *startAngle* a *startAngle*  +  *sweepAngle* (dove 0 gradi si trova lungo l'asse y positivo, 90 gradi si trova lungo l'asse x positivo, 180 gradi si trova lungo l'asse y negativo e 270 gradi si trova lungo l'asse x negativo).</span><span class="sxs-lookup"><span data-stu-id="9532b-126">A partial disk is similar to a full disk, except that only the subset of the disk from *startAngle* through *startAngle* + *sweepAngle* is included (where 0 degrees is along the positive y-axis, 90 degrees is along the positive x-axis, 180 degrees is along the negative y-axis, and 270 degrees is along the negative x-axis).</span></span>

<span data-ttu-id="9532b-127">Il disco parziale ha un raggio di *OuterRadius* e contiene un foro circolare concentrico con un raggio di *InnerRadius*.</span><span class="sxs-lookup"><span data-stu-id="9532b-127">The partial disk has a radius of *outerRadius* and contains a concentric circular hole with a radius of *innerRadius*.</span></span> <span data-ttu-id="9532b-128">Se *InnerRadius* è zero, non viene generato alcun Hole.</span><span class="sxs-lookup"><span data-stu-id="9532b-128">If *innerRadius* is zero, then no hole is generated.</span></span> <span data-ttu-id="9532b-129">Il disco parziale viene suddiviso intorno all'asse z in sezioni (ad esempio, sezioni della pizza) e anche sull'asse z negli anelli, come specificato dalle *sezioni* e dai *cicli*, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="9532b-129">The partial disk is subdivided around the z-axis into slices (like pizza slices), and also about the z-axis into rings (as specified by *slices* and *loops*, respectively).</span></span>

<span data-ttu-id="9532b-130">Per quanto riguarda l'orientamento, il lato z positivo del disco parziale viene considerato esterno (vedere [**gluQuadricOrientation**](gluquadricorientation.md)).</span><span class="sxs-lookup"><span data-stu-id="9532b-130">With respect to orientation, the positive z-side of the partial disk is considered to be outside (see [**gluQuadricOrientation**](gluquadricorientation.md)).</span></span> <span data-ttu-id="9532b-131">Ciò significa che se l'orientamento è impostato su GLU \_ all'esterno, eventuali normali generano un punto lungo l'asse z positivo.</span><span class="sxs-lookup"><span data-stu-id="9532b-131">This means that if the orientation is set to GLU\_OUTSIDE, then any normals generated point along the positive z-axis.</span></span>

<span data-ttu-id="9532b-132">Se è stata attivata la texturing (con [**gluQuadricTexture**](gluquadrictexture.md)), **gluPartialDisk** genera le coordinate di trama in modo lineare, in modo da dove *r*  =  *OuterRadius*, il valore in (*r*, 0, 0) è (1, 0,5); at (0, *r*, 0) è (0,5, 1); at (*r*, 0, 0) è (0, 0,5); e at (0, *r*, 0) è (0,5, 0).</span><span class="sxs-lookup"><span data-stu-id="9532b-132">If you have turned on texturing (with [**gluQuadricTexture**](gluquadrictexture.md)), **gluPartialDisk** generates texture coordinates linearly such that where *r* = *outerRadius*, the value at (*r*, 0, 0) is (1, 0.5); at (0, *r*, 0) it is (0.5, 1); at (*r*, 0, 0) it is (0, 0.5); and at (0, *r*, 0) it is (0.5, 0).</span></span>

## <a name="requirements"></a><span data-ttu-id="9532b-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9532b-133">Requirements</span></span>



| <span data-ttu-id="9532b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="9532b-134">Requirement</span></span> | <span data-ttu-id="9532b-135">Valore</span><span class="sxs-lookup"><span data-stu-id="9532b-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9532b-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9532b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9532b-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9532b-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9532b-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9532b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9532b-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9532b-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9532b-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9532b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="9532b-141"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="9532b-141"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="9532b-142">Libreria</span><span class="sxs-lookup"><span data-stu-id="9532b-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="9532b-143"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9532b-143"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9532b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="9532b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9532b-145"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9532b-145"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9532b-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9532b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9532b-147">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="9532b-147">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="9532b-148">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="9532b-148">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="9532b-149">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="9532b-149">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="9532b-150">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="9532b-150">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="9532b-151">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="9532b-151">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="9532b-152">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="9532b-152">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





