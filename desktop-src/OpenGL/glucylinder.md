---
title: funzione gluCylinder (Glu. h)
description: La funzione gluCylinder disegna un cilindro.
ms.assetid: 43329d2f-50bb-46ea-85cb-22956d0df375
keywords:
- funzione gluCylinder OpenGL
topic_type:
- apiref
api_name:
- gluCylinder
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fd201d1ddd720501715d1ead08d94bab72f7b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301918"
---
# <a name="glucylinder-function"></a><span data-ttu-id="468ef-104">gluCylinder (funzione)</span><span class="sxs-lookup"><span data-stu-id="468ef-104">gluCylinder function</span></span>

<span data-ttu-id="468ef-105">La funzione **gluCylinder** disegna un cilindro.</span><span class="sxs-lookup"><span data-stu-id="468ef-105">The **gluCylinder** function draws a cylinder.</span></span>

## <a name="syntax"></a><span data-ttu-id="468ef-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="468ef-106">Syntax</span></span>


```C++
void WINAPI gluCylinder(
   GLUquadric *qobj,
   GLdouble   baseRadius,
   GLdouble   topRadius,
   GLdouble   height,
   GLint      slices,
   GLint      stacks
);
```



## <a name="parameters"></a><span data-ttu-id="468ef-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="468ef-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="468ef-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="468ef-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="468ef-109">Oggetto quadrica (creato con [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="468ef-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="468ef-110">*baseRadius*</span><span class="sxs-lookup"><span data-stu-id="468ef-110">*baseRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="468ef-111">Raggio del cilindro a *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="468ef-111">The radius of the cylinder at *z* = 0.</span></span>

</dd> <dt>

<span data-ttu-id="468ef-112">*Raggio*</span><span class="sxs-lookup"><span data-stu-id="468ef-112">*topRadius*</span></span> 
</dt> <dd>

<span data-ttu-id="468ef-113">Raggio del cilindro a   =  *altezza* z.</span><span class="sxs-lookup"><span data-stu-id="468ef-113">The radius of the cylinder at *z* = *height*.</span></span>

</dd> <dt>

<span data-ttu-id="468ef-114">*height*</span><span class="sxs-lookup"><span data-stu-id="468ef-114">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="468ef-115">Altezza del cilindro.</span><span class="sxs-lookup"><span data-stu-id="468ef-115">The height of the cylinder.</span></span>

</dd> <dt>

<span data-ttu-id="468ef-116">*fette*</span><span class="sxs-lookup"><span data-stu-id="468ef-116">*slices*</span></span> 
</dt> <dd>

<span data-ttu-id="468ef-117">Numero di suddivisioni intorno all'asse z.</span><span class="sxs-lookup"><span data-stu-id="468ef-117">The number of subdivisions around the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="468ef-118">*pile*</span><span class="sxs-lookup"><span data-stu-id="468ef-118">*stacks*</span></span> 
</dt> <dd>

<span data-ttu-id="468ef-119">Numero di suddivisioni lungo l'asse z.</span><span class="sxs-lookup"><span data-stu-id="468ef-119">The number of subdivisions along the z-axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="468ef-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="468ef-120">Return value</span></span>

<span data-ttu-id="468ef-121">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="468ef-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="468ef-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="468ef-122">Remarks</span></span>

<span data-ttu-id="468ef-123">La funzione **gluCylinder** disegna un cilindro orientato lungo l'asse z.</span><span class="sxs-lookup"><span data-stu-id="468ef-123">The **gluCylinder** function draws a cylinder oriented along the z-axis.</span></span> <span data-ttu-id="468ef-124">La base del cilindro viene posizionata in corrispondenza della *z* = 0 e della parte superiore all'  =  *altezza* z.</span><span class="sxs-lookup"><span data-stu-id="468ef-124">The base of the cylinder is placed at *z* = 0, and the top at *z* = *height*.</span></span> <span data-ttu-id="468ef-125">Analogamente a una sfera, un cilindro viene suddiviso in sezioni intorno all'asse z e lungo l'asse z negli stack.</span><span class="sxs-lookup"><span data-stu-id="468ef-125">Like a sphere, a cylinder is subdivided around the z-axis into slices, and along the z-axis into stacks.</span></span>

<span data-ttu-id="468ef-126">*Si noti che se è* impostato su zero, questa routine genererà un cono.</span><span class="sxs-lookup"><span data-stu-id="468ef-126">Note that if *topRadius* is set to zero, then this routine will generate a cone.</span></span>

<span data-ttu-id="468ef-127">Se l'orientamento è impostato su GLU \_ all'esterno (con [**gluQuadricOrientation**](gluquadricorientation.md)), eventuali normali generati si allontanano dall'asse z.</span><span class="sxs-lookup"><span data-stu-id="468ef-127">If the orientation is set to GLU\_OUTSIDE (with [**gluQuadricOrientation**](gluquadricorientation.md)), then any generated normals point away from the z-axis.</span></span> <span data-ttu-id="468ef-128">In caso contrario, puntano verso l'asse z.</span><span class="sxs-lookup"><span data-stu-id="468ef-128">Otherwise, they point toward the z-axis.</span></span>

<span data-ttu-id="468ef-129">Se la texturing è attivata (con [**gluQuadricTexture**](gluquadrictexture.md)): le coordinate di trama vengono generate in modo che *t* sia lineare da 0,0 a *z* = 0 a 1,0 all'   =  *altezza* z; e *s* intervalli da 0,0 sull'asse y positivo, a 0,25 sull'asse x positivo, fino a 0,5 sull'asse y negativo, fino a 0,75 sull'asse x negativo e viceversa a 1,0 sull'asse y positivo.</span><span class="sxs-lookup"><span data-stu-id="468ef-129">If texturing is turned on (with [**gluQuadricTexture**](gluquadrictexture.md)): texture coordinates are generated so that *t* ranges linearly from 0.0 at *z* = 0 to 1.0 at *z* = *height*; and *s* ranges from 0.0 at the positive y-axis, to 0.25 at the positive x-axis, to 0.5 at the negative y-axis, to 0.75 at the negative x-axis, and back to 1.0 at the positive y-axis.</span></span>

## <a name="requirements"></a><span data-ttu-id="468ef-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="468ef-130">Requirements</span></span>



| <span data-ttu-id="468ef-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="468ef-131">Requirement</span></span> | <span data-ttu-id="468ef-132">Valore</span><span class="sxs-lookup"><span data-stu-id="468ef-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="468ef-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="468ef-133">Minimum supported client</span></span><br/> | <span data-ttu-id="468ef-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="468ef-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="468ef-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="468ef-135">Minimum supported server</span></span><br/> | <span data-ttu-id="468ef-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="468ef-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="468ef-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="468ef-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="468ef-138"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="468ef-138"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="468ef-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="468ef-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="468ef-140"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="468ef-140"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="468ef-141">DLL</span><span class="sxs-lookup"><span data-stu-id="468ef-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="468ef-142"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="468ef-142"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="468ef-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="468ef-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="468ef-144">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="468ef-144">**gluDisk**</span></span>](gludisk.md)
</dt> <dt>

[<span data-ttu-id="468ef-145">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="468ef-145">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="468ef-146">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="468ef-146">**gluPartialDisk**</span></span>](glupartialdisk.md)
</dt> <dt>

[<span data-ttu-id="468ef-147">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="468ef-147">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="468ef-148">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="468ef-148">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> <dt>

[<span data-ttu-id="468ef-149">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="468ef-149">**gluSphere**</span></span>](glusphere.md)
</dt> </dl>

 

 





