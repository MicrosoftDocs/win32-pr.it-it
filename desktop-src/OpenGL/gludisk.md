---
title: funzione gluDisk (Glu. h)
description: La funzione gluDisk disegna un disco.
ms.assetid: c9260621-930d-47dd-a046-30895779473b
keywords:
- funzione gluDisk OpenGL
topic_type:
- apiref
api_name:
- gluDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9a9e8b547790049c93360f060e944aafcea4511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048332"
---
# <a name="gludisk-function"></a><span data-ttu-id="b25bd-104">gluDisk (funzione)</span><span class="sxs-lookup"><span data-stu-id="b25bd-104">gluDisk function</span></span>

<span data-ttu-id="b25bd-105">La funzione **gluDisk** disegna un disco.</span><span class="sxs-lookup"><span data-stu-id="b25bd-105">The **gluDisk** function draws a disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="b25bd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b25bd-106">Syntax</span></span>


```C++
void WINAPI gluDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops
);
```



## <a name="parameters"></a><span data-ttu-id="b25bd-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="b25bd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b25bd-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="b25bd-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="b25bd-109">Oggetto quadrica (creato con [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="b25bd-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="b25bd-110">*innerRadius*</span><span class="sxs-lookup"><span data-stu-id="b25bd-110">*innerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="b25bd-111">Raggio interno del disco (può essere zero).</span><span class="sxs-lookup"><span data-stu-id="b25bd-111">The inner radius of the disk (may be zero).</span></span>

</dd> <dt>

<span data-ttu-id="b25bd-112">*outerRadius*</span><span class="sxs-lookup"><span data-stu-id="b25bd-112">*outerRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="b25bd-113">Raggio esterno del disco.</span><span class="sxs-lookup"><span data-stu-id="b25bd-113">The outer radius of the disk.</span></span>

</dd> <dt>

<span data-ttu-id="b25bd-114">*fette*</span><span class="sxs-lookup"><span data-stu-id="b25bd-114">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="b25bd-115">Numero di suddivisioni intorno all'asse z.</span><span class="sxs-lookup"><span data-stu-id="b25bd-115">The number of subdivisions around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="b25bd-116">*cicli*</span><span class="sxs-lookup"><span data-stu-id="b25bd-116">*loops*</span></span> 
</dt> <dd>

<span data-ttu-id="b25bd-117">Numero di anelli concentrici sull'origine in cui è suddiviso il disco.</span><span class="sxs-lookup"><span data-stu-id="b25bd-117">The number of concentric rings about the origin into which the disk is subdivided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b25bd-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b25bd-118">Return value</span></span>

<span data-ttu-id="b25bd-119">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="b25bd-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b25bd-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="b25bd-120">Remarks</span></span>

<span data-ttu-id="b25bd-121">La funzione **gluDisk** esegue il rendering di un disco sul piano *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="b25bd-121">The **gluDisk** function renders a disk on the *z* = 0 plane.</span></span> <span data-ttu-id="b25bd-122">Il disco ha un raggio di *OuterRadius* e contiene un foro circolare concentrico con un raggio di *InnerRadius*.</span><span class="sxs-lookup"><span data-stu-id="b25bd-122">The disk has a radius of *outerRadius*, and contains a concentric circular hole with a radius of *innerRadius*.</span></span> <span data-ttu-id="b25bd-123">Se *InnerRadius* è 0, non viene generato alcun Hole.</span><span class="sxs-lookup"><span data-stu-id="b25bd-123">If *innerRadius* is 0, then no hole is generated.</span></span> <span data-ttu-id="b25bd-124">Il disco viene suddiviso in sezioni intorno all'asse z in sezioni, ad esempio le sezioni della pizza, e anche sull'asse z negli anelli, come specificato dalle *sezioni* e dai *cicli*, rispettivamente.</span><span class="sxs-lookup"><span data-stu-id="b25bd-124">The disk is subdivided around the z-axis into slices (like pizza slices) and also about the z-axis into rings (as specified by *slices* and *loops*, respectively).</span></span>

<span data-ttu-id="b25bd-125">Per quanto riguarda l'orientamento, il lato *z* positivo del disco è considerato *esterno* (vedere [**gluQuadricOrientation**](gluquadricorientation.md)).</span><span class="sxs-lookup"><span data-stu-id="b25bd-125">With respect to orientation, the positive *z*-side of the disk is considered to be *outside* (see [**gluQuadricOrientation**](gluquadricorientation.md)).</span></span> <span data-ttu-id="b25bd-126">Ciò significa che se l'orientamento è impostato su GLU \_ all'esterno, eventuali normali generano un punto lungo l'asse z positivo.</span><span class="sxs-lookup"><span data-stu-id="b25bd-126">This means that if the orientation is set to GLU\_OUTSIDE, then any normals generated point along the positive z-axis.</span></span>

<span data-ttu-id="b25bd-127">Se la texturing è attivata (con [**gluQuadricTexture**](gluquadrictexture.md)), le coordinate di trama vengono generate linearmente in modo tale che, dove *r*  =  *OuterRadius*, il valore in (*r*, 0, 0) è (1, 0,5); at (0, *r*, 0) it is (0,5,1); at (-*r*, 0, 0) è (0, 0,5) e at (0,-*r*, 0) è (0,5, 0).</span><span class="sxs-lookup"><span data-stu-id="b25bd-127">If texturing is turned on (with [**gluQuadricTexture**](gluquadrictexture.md)), texture coordinates are generated linearly such that where *r* = *outerRadius*, the value at (*r*, 0, 0) is (1, 0.5); at (0, *r*, 0) it is (0.5, 1); at (-*r*, 0, 0) it is (0, 0.5); and at (0, -*r*, 0) it is (0.5, 0).</span></span>

## <a name="requirements"></a><span data-ttu-id="b25bd-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b25bd-128">Requirements</span></span>



| <span data-ttu-id="b25bd-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="b25bd-129">Requirement</span></span> | <span data-ttu-id="b25bd-130">Valore</span><span class="sxs-lookup"><span data-stu-id="b25bd-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b25bd-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b25bd-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b25bd-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b25bd-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b25bd-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b25bd-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b25bd-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b25bd-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b25bd-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b25bd-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="b25bd-136"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="b25bd-136"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="b25bd-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="b25bd-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="b25bd-138"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b25bd-138"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b25bd-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b25bd-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b25bd-140"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b25bd-140"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b25bd-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b25bd-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b25bd-142">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="b25bd-142">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="b25bd-143">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="b25bd-143">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="b25bd-144">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="b25bd-144">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="b25bd-145">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="b25bd-145">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="b25bd-146">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="b25bd-146">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="b25bd-147">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="b25bd-147">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





