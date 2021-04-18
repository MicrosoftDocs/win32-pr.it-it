---
title: funzione gluSphere (Glu. h)
description: La funzione gluSphere disegna una sfera.
ms.assetid: 0f1919c6-0551-4d50-b782-767dacc088cb
keywords:
- funzione gluSphere OpenGL
topic_type:
- apiref
api_name:
- gluSphere
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899ff4833c705aae34fdb7830c264fee91414116
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478016"
---
# <a name="glusphere-function"></a><span data-ttu-id="8df25-104">gluSphere (funzione)</span><span class="sxs-lookup"><span data-stu-id="8df25-104">gluSphere function</span></span>

<span data-ttu-id="8df25-105">La funzione **gluSphere** disegna una sfera.</span><span class="sxs-lookup"><span data-stu-id="8df25-105">The **gluSphere** function draws a sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="8df25-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8df25-106">Syntax</span></span>


```C++
void WINAPI gluSphere(
   GLUquadric *qobj,
   GLdouble   radius,
   GLint      slices,
   GLint      stacks
);
```



## <a name="parameters"></a><span data-ttu-id="8df25-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8df25-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8df25-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="8df25-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="8df25-109">Oggetto quadrica (creato con [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="8df25-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="8df25-110">*raggio*</span><span class="sxs-lookup"><span data-stu-id="8df25-110">*radius*</span></span> 
</dt> <dd>

<span data-ttu-id="8df25-111">Raggio della sfera.</span><span class="sxs-lookup"><span data-stu-id="8df25-111">The radius of the sphere.</span></span>

</dd> <dt>

<span data-ttu-id="8df25-112">*fette*</span><span class="sxs-lookup"><span data-stu-id="8df25-112">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="8df25-113">Numero di suddivisioni intorno all'asse z (simili alle linee di longitudine).</span><span class="sxs-lookup"><span data-stu-id="8df25-113">The number of subdivisions around the z-axis (similar to lines of longitude).</span></span>

</dd> <dt>

<span data-ttu-id="8df25-114">*pile*</span><span class="sxs-lookup"><span data-stu-id="8df25-114">*stacks*</span></span> 
</dt> <dd>

<span data-ttu-id="8df25-115">Il numero di suddivisioni lungo l'asse z, simile alle linee di latitudine.</span><span class="sxs-lookup"><span data-stu-id="8df25-115">The number of subdivisions along the z-axis (similar to lines of latitude).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8df25-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8df25-116">Return value</span></span>

<span data-ttu-id="8df25-117">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="8df25-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8df25-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="8df25-118">Remarks</span></span>

<span data-ttu-id="8df25-119">La funzione **gluSphere** disegna una sfera del raggio specificato centrata intorno all'origine.</span><span class="sxs-lookup"><span data-stu-id="8df25-119">The **gluSphere** function draws a sphere of the given radius centered around the origin.</span></span> <span data-ttu-id="8df25-120">La sfera viene suddivisa in sezioni intorno all'asse z e lungo l'asse z negli stack (in modo analogo alle linee di longitudine e latitudine).</span><span class="sxs-lookup"><span data-stu-id="8df25-120">The sphere is subdivided around the z-axis into slices and along the z-axis into stacks (similar to lines of longitude and latitude).</span></span>

<span data-ttu-id="8df25-121">Se l'orientamento è impostato su GLU \_ all'esterno (con **gluQuadricOrientation**), eventuali normali generate fanno riferimento al centro della sfera.</span><span class="sxs-lookup"><span data-stu-id="8df25-121">If the orientation is set to GLU\_OUTSIDE (with **gluQuadricOrientation**), any normals generated point away from the center of the sphere.</span></span> <span data-ttu-id="8df25-122">In caso contrario, puntano verso il centro della sfera.</span><span class="sxs-lookup"><span data-stu-id="8df25-122">Otherwise, they point toward the center of the sphere.</span></span>

<span data-ttu-id="8df25-123">Se la texturing è attivata (con **gluQuadricTexture**): le coordinate di trama vengono generate in modo che *t* sia compreso tra 0,0 e *z* =-*RADIUS* e 1,0 al   =  *raggio* z (*t* aumenta in modo lineare lungo le linee longitudinali); e *è* compreso tra 0,0 e l'asse y positivo, fino a 0,25 sull'asse x positivo, a 0,5 sull'asse y negativo, a 0,75 sull'asse x negativo e viceversa a 1,0 sull'asse y positivo.</span><span class="sxs-lookup"><span data-stu-id="8df25-123">If texturing is turned on (with **gluQuadricTexture**): texture coordinates are generated so that *t* ranges from 0.0 at *z* = -*radius* to 1.0 at *z* = *radius* (*t* increases linearly along longitudinal lines); and *s* ranges from 0.0 at the positive y-axis, to 0.25 at the positive x-axis, to 0.5 at the negative y-axis, to 0.75 at the negative x-axis, and back to 1.0 at the positive y-axis.</span></span>

## <a name="requirements"></a><span data-ttu-id="8df25-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8df25-124">Requirements</span></span>



| <span data-ttu-id="8df25-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="8df25-125">Requirement</span></span> | <span data-ttu-id="8df25-126">Valore</span><span class="sxs-lookup"><span data-stu-id="8df25-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8df25-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8df25-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8df25-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8df25-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="8df25-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8df25-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8df25-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="8df25-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8df25-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8df25-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8df25-132"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="8df25-132"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="8df25-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="8df25-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="8df25-134"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8df25-134"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="8df25-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8df25-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8df25-136"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8df25-136"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8df25-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8df25-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8df25-138">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="8df25-138">**gluCylinder**</span></span>](glucylinder.md)
</dt> <dt>

[<span data-ttu-id="8df25-139">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="8df25-139">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="8df25-140">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="8df25-140">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="8df25-141">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="8df25-141">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="8df25-142">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="8df25-142">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="8df25-143">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="8df25-143">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





