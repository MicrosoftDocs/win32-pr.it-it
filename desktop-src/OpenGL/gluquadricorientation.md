---
title: funzione gluQuadricOrientation (Glu. h)
description: La funzione gluQuadricOrientation specifica l'orientamento all'interno o all'esterno di quadriche.
ms.assetid: 4e3fc6d3-5a39-455b-bd24-8eb497333096
keywords:
- funzione gluQuadricOrientation OpenGL
topic_type:
- apiref
api_name:
- gluQuadricOrientation
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05ffb1eeff199297943e678783731a26a38092a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739791"
---
# <a name="gluquadricorientation-function"></a><span data-ttu-id="3fd09-104">gluQuadricOrientation (funzione)</span><span class="sxs-lookup"><span data-stu-id="3fd09-104">gluQuadricOrientation function</span></span>

<span data-ttu-id="3fd09-105">La funzione **gluQuadricOrientation** specifica l'orientamento all'interno o all'esterno di quadriche.</span><span class="sxs-lookup"><span data-stu-id="3fd09-105">The **gluQuadricOrientation** function specifies inside or outside orientation for quadrics.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fd09-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3fd09-106">Syntax</span></span>


```C++
void WINAPI gluQuadricOrientation(
   GLUquadric *quadObject,
   GLenum     orientation
);
```



## <a name="parameters"></a><span data-ttu-id="3fd09-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3fd09-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fd09-108">*quadObject*</span><span class="sxs-lookup"><span data-stu-id="3fd09-108">*quadObject*</span></span> 
</dt> <dd>

<span data-ttu-id="3fd09-109">Oggetto quadrica (creato con [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="3fd09-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="3fd09-110">*orientamento*</span><span class="sxs-lookup"><span data-stu-id="3fd09-110">*orientation*</span></span> 
</dt> <dd>

<span data-ttu-id="3fd09-111">Orientamento desiderato.</span><span class="sxs-lookup"><span data-stu-id="3fd09-111">The desired orientation.</span></span> <span data-ttu-id="3fd09-112">I valori seguenti sono validi.</span><span class="sxs-lookup"><span data-stu-id="3fd09-112">The following values are valid.</span></span>



| <span data-ttu-id="3fd09-113">Valore</span><span class="sxs-lookup"><span data-stu-id="3fd09-113">Value</span></span>                                                                                                                                                   | <span data-ttu-id="3fd09-114">Significato</span><span class="sxs-lookup"><span data-stu-id="3fd09-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="GLU_OUTSIDE"></span><span id="glu_outside"></span><dl> <span data-ttu-id="3fd09-115"><dt>**GLU \_ esterno**</dt></span><span class="sxs-lookup"><span data-stu-id="3fd09-115"><dt>**GLU\_OUTSIDE**</dt></span></span> </dl> | <span data-ttu-id="3fd09-116">Creare quadriche con normali che puntano verso l'esterno.</span><span class="sxs-lookup"><span data-stu-id="3fd09-116">Draw quadrics with normals pointing outward.</span></span> <span data-ttu-id="3fd09-117">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="3fd09-117">This is the default value.</span></span><br/> |
| <span id="GLU_INSIDE"></span><span id="glu_inside"></span><dl> <span data-ttu-id="3fd09-118"><dt>**GLU \_ all'interno**</dt></span><span class="sxs-lookup"><span data-stu-id="3fd09-118"><dt>**GLU\_INSIDE**</dt></span></span> </dl>    | <span data-ttu-id="3fd09-119">Creare quadriche con normali che puntano verso l'interno.</span><span class="sxs-lookup"><span data-stu-id="3fd09-119">Draw quadrics with normals pointing inward.</span></span><br/>                             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fd09-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3fd09-120">Return value</span></span>

<span data-ttu-id="3fd09-121">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="3fd09-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fd09-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="3fd09-122">Remarks</span></span>

<span data-ttu-id="3fd09-123">La funzione **gluQuadricOrientation** specifica il tipo di orientamento desiderato per il rendering di quadriche con **quadObject**.</span><span class="sxs-lookup"><span data-stu-id="3fd09-123">The **gluQuadricOrientation** function specifies what kind of orientation is desired for quadrics rendered with **quadObject**.</span></span> <span data-ttu-id="3fd09-124">L'interpretazione di verso l'esterno e verso l'interno dipende dal quadrica che si sta disegnando.</span><span class="sxs-lookup"><span data-stu-id="3fd09-124">The interpretation of outward and inward depends on the quadric being drawn.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fd09-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fd09-125">Requirements</span></span>



| <span data-ttu-id="3fd09-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fd09-126">Requirement</span></span> | <span data-ttu-id="3fd09-127">Valore</span><span class="sxs-lookup"><span data-stu-id="3fd09-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd09-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fd09-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3fd09-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3fd09-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3fd09-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fd09-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3fd09-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3fd09-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3fd09-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3fd09-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fd09-133"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fd09-133"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="3fd09-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="3fd09-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="3fd09-135"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3fd09-135"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3fd09-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3fd09-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fd09-137"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fd09-137"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fd09-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3fd09-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fd09-139">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="3fd09-139">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> <dt>

[<span data-ttu-id="3fd09-140">**gluQuadricDrawStyle**</span><span class="sxs-lookup"><span data-stu-id="3fd09-140">**gluQuadricDrawStyle**</span></span>](gluquadricdrawstyle.md)
</dt> <dt>

[<span data-ttu-id="3fd09-141">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="3fd09-141">**gluQuadricNormals**</span></span>](gluquadricnormals.md)
</dt> <dt>

[<span data-ttu-id="3fd09-142">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="3fd09-142">**gluQuadricTexture**</span></span>](gluquadrictexture.md)
</dt> </dl>

 

 





