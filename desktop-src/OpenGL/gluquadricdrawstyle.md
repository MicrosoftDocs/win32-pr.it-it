---
title: funzione gluQuadricDrawStyle (Glu. h)
description: La funzione gluQuadricDrawStyle specifica lo stile di estrazione desiderato per quadriche.
ms.assetid: 30f6da40-9306-46bb-a815-f51722e57e18
keywords:
- funzione gluQuadricDrawStyle OpenGL
topic_type:
- apiref
api_name:
- gluQuadricDrawStyle
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a1b44b7894ea9762b450c5a5d6c2b022c5e02f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964601"
---
# <a name="gluquadricdrawstyle-function"></a><span data-ttu-id="07855-104">gluQuadricDrawStyle (funzione)</span><span class="sxs-lookup"><span data-stu-id="07855-104">gluQuadricDrawStyle function</span></span>

<span data-ttu-id="07855-105">La funzione **gluQuadricDrawStyle** specifica lo stile di estrazione desiderato per quadriche.</span><span class="sxs-lookup"><span data-stu-id="07855-105">The **gluQuadricDrawStyle** function specifies the draw style desired for quadrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="07855-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07855-106">Syntax</span></span>


```C++
void WINAPI gluQuadricDrawStyle(
   GLUquadric *quadObject,
   GLenum     drawStyle
);
```



## <a name="parameters"></a><span data-ttu-id="07855-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="07855-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07855-108">*quadObject*</span><span class="sxs-lookup"><span data-stu-id="07855-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="07855-109">Oggetto quadrica (creato con [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="07855-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="07855-110">*drawStyle*</span><span class="sxs-lookup"><span data-stu-id="07855-110">*drawStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="07855-111">Stile di disegni desiderato.</span><span class="sxs-lookup"><span data-stu-id="07855-111">The desired draw style.</span></span> <span data-ttu-id="07855-112">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="07855-112">The following values are valid.</span></span>



| <span data-ttu-id="07855-113">Valore</span><span class="sxs-lookup"><span data-stu-id="07855-113">Value</span></span>                                                                                                                                                            | <span data-ttu-id="07855-114">Significato</span><span class="sxs-lookup"><span data-stu-id="07855-114">Meaning</span></span>                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_FILL"></span><span id="glu_fill"></span><dl> <span data-ttu-id="07855-115"><dt>**\_riempimento Glu**</dt></span><span class="sxs-lookup"><span data-stu-id="07855-115"><dt>**GLU\_FILL**</dt></span></span> </dl>                   | <span data-ttu-id="07855-116">Viene eseguito il rendering di quadriche con primitive poligonali.</span><span class="sxs-lookup"><span data-stu-id="07855-116">Quadrics are rendered with polygon primitives.</span></span> <span data-ttu-id="07855-117">I poligoni vengono disegnati in senso antiorario rispetto alle normali (come definito con [**gluQuadricOrientation**](gluquadricorientation.md)).</span><span class="sxs-lookup"><span data-stu-id="07855-117">The polygons are drawn in a counterclockwise fashion with respect to their normals (as defined with [**gluQuadricOrientation**](gluquadricorientation.md)).</span></span><br/> |
| <span id="GLU_LINE"></span><span id="glu_line"></span><dl> <span data-ttu-id="07855-118"><dt>**\_linea Glu**</dt></span><span class="sxs-lookup"><span data-stu-id="07855-118"><dt>**GLU\_LINE**</dt></span></span> </dl>                   | <span data-ttu-id="07855-119">Il rendering di quadriche viene eseguito come un set di righe.</span><span class="sxs-lookup"><span data-stu-id="07855-119">Quadrics are rendered as a set of lines.</span></span><br/>                                                                                                                                                                    |
| <span id="GLU_SILHOUETTE"></span><span id="glu_silhouette"></span><dl> <span data-ttu-id="07855-120"><dt>**\_Siluetta Glu**</dt></span><span class="sxs-lookup"><span data-stu-id="07855-120"><dt>**GLU\_SILHOUETTE**</dt></span></span> </dl> | <span data-ttu-id="07855-121">Il rendering di quadriche viene eseguito come set di righe, ad eccezione del fatto che i bordi che separano i visi complanari non verranno disegnati</span><span class="sxs-lookup"><span data-stu-id="07855-121">Quadrics are rendered as a set of lines, except that edges separating coplanar faces will not be drawn.</span></span><br/>                                                                                                     |
| <span id="GLU_POINT"></span><span id="glu_point"></span><dl> <span data-ttu-id="07855-122"><dt>**punto di GLU \_**</dt></span><span class="sxs-lookup"><span data-stu-id="07855-122"><dt>**GLU\_POINT**</dt></span></span> </dl>                | <span data-ttu-id="07855-123">Il rendering di quadriche viene eseguito come un set di punti.</span><span class="sxs-lookup"><span data-stu-id="07855-123">Quadrics are rendered as a set of points.</span></span><br/>                                                                                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07855-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07855-124">Return value</span></span>

<span data-ttu-id="07855-125">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="07855-125">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="07855-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="07855-126">Remarks</span></span>

<span data-ttu-id="07855-127">La funzione **gluQuadricDrawStyle** specifica lo stile di disegna per quadriche di cui è stato eseguito il rendering con **quadObject**.</span><span class="sxs-lookup"><span data-stu-id="07855-127">The **gluQuadricDrawStyle** function specifies the draw style for quadrics rendered with **quadObject**.</span></span>

## <a name="requirements"></a><span data-ttu-id="07855-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07855-128">Requirements</span></span>



| <span data-ttu-id="07855-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="07855-129">Requirement</span></span> | <span data-ttu-id="07855-130">Valore</span><span class="sxs-lookup"><span data-stu-id="07855-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="07855-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07855-131">Minimum supported client</span></span><br/> | <span data-ttu-id="07855-132">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="07855-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="07855-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07855-133">Minimum supported server</span></span><br/> | <span data-ttu-id="07855-134">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="07855-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="07855-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07855-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="07855-136"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="07855-136"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="07855-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="07855-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="07855-138"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07855-138"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="07855-139">DLL</span><span class="sxs-lookup"><span data-stu-id="07855-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07855-140"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07855-140"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07855-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07855-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07855-142">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="07855-142">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="07855-143">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="07855-143">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> <dt>

[<span data-ttu-id="07855-144">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="07855-144">**gluQuadricOrientation**</span></span>](gluquadricorientation.md)
</dt> <dt>

[<span data-ttu-id="07855-145">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="07855-145">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





