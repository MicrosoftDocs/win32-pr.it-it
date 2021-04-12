---
title: funzione gluPerspective (Glu. h)
description: La funzione gluPerspective imposta una matrice di proiezione prospettica.
ms.assetid: 125e2828-a2d7-4c6c-9370-eb21a581ced8
keywords:
- funzione gluPerspective OpenGL
topic_type:
- apiref
api_name:
- gluPerspective
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf30fc7dc4c6ba5a56efd3def6a5a7178f81ed49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400821"
---
# <a name="gluperspective-function"></a><span data-ttu-id="133f0-104">gluPerspective (funzione)</span><span class="sxs-lookup"><span data-stu-id="133f0-104">gluPerspective function</span></span>

<span data-ttu-id="133f0-105">La funzione **gluPerspective** imposta una matrice di proiezione prospettica.</span><span class="sxs-lookup"><span data-stu-id="133f0-105">The **gluPerspective** function sets up a perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="133f0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="133f0-106">Syntax</span></span>


```C++
void WINAPI gluPerspective(
   GLdouble fovy,
   GLdouble aspect,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a><span data-ttu-id="133f0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="133f0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="133f0-108">*fovy*</span><span class="sxs-lookup"><span data-stu-id="133f0-108">*fovy*</span></span> 
</dt> <dd>

<span data-ttu-id="133f0-109">Campo dell'angolo di visualizzazione, in gradi, nella direzione y.</span><span class="sxs-lookup"><span data-stu-id="133f0-109">The field of view angle, in degrees, in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="133f0-110">*aspect*</span><span class="sxs-lookup"><span data-stu-id="133f0-110">*aspect*</span></span> 
</dt> <dd>

<span data-ttu-id="133f0-111">Proporzioni che determinano il campo di visualizzazione nella direzione x.</span><span class="sxs-lookup"><span data-stu-id="133f0-111">The aspect ratio that determines the field of view in the x-direction.</span></span> <span data-ttu-id="133f0-112">La proporzioni è il rapporto tra *x* (width) e *y* (Height).</span><span class="sxs-lookup"><span data-stu-id="133f0-112">The aspect ratio is the ratio of *x* (width) to *y* (height).</span></span>

</dd> <dt>

<span data-ttu-id="133f0-113">*zNear*</span><span class="sxs-lookup"><span data-stu-id="133f0-113">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="133f0-114">Distanza dal visualizzatore al piano di ritaglio vicino (sempre positivo).</span><span class="sxs-lookup"><span data-stu-id="133f0-114">The distance from the viewer to the near clipping plane (always positive).</span></span>

</dd> <dt>

<span data-ttu-id="133f0-115">*zFar*</span><span class="sxs-lookup"><span data-stu-id="133f0-115">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="133f0-116">Distanza tra il visualizzatore e il piano di ritaglio (sempre positivo).</span><span class="sxs-lookup"><span data-stu-id="133f0-116">The distance from the viewer to the far clipping plane (always positive).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="133f0-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="133f0-117">Return value</span></span>

<span data-ttu-id="133f0-118">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="133f0-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="133f0-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="133f0-119">Remarks</span></span>

<span data-ttu-id="133f0-120">La funzione **gluPerspective** specifica un tronco di visualizzazione nel sistema di coordinate globali.</span><span class="sxs-lookup"><span data-stu-id="133f0-120">The **gluPerspective** function specifies a viewing frustum into the world coordinate system.</span></span> <span data-ttu-id="133f0-121">In generale, le proporzioni in **gluPerspective** devono corrispondere alle proporzioni del viewport associato.</span><span class="sxs-lookup"><span data-stu-id="133f0-121">In general, the aspect ratio in **gluPerspective** should match the aspect ratio of the associated viewport.</span></span> <span data-ttu-id="133f0-122">Ad esempio, *aspect* = 2,0 indica che l'angolo di visualizzazione del visualizzatore è due volte più ampio in *x* come si trova in *y*.</span><span class="sxs-lookup"><span data-stu-id="133f0-122">For example, *aspect* = 2.0 means the viewer's angle of view is twice as wide in *x* as it is in *y*.</span></span> <span data-ttu-id="133f0-123">Se il riquadro di visualizzazione è a larghezza doppia rispetto all'altezza, viene visualizzata l'immagine senza distorsione.</span><span class="sxs-lookup"><span data-stu-id="133f0-123">If the viewport is twice as wide as it is tall, it displays the image without distortion.</span></span>

<span data-ttu-id="133f0-124">La matrice generata da **gluPerspective** viene moltiplicata per la matrice corrente, esattamente come se [**glMultMatrix**](glmultmatrix.md) venisse chiamato con la matrice generata.</span><span class="sxs-lookup"><span data-stu-id="133f0-124">The matrix generated by **gluPerspective** is multiplied by the current matrix, just as if [**glMultMatrix**](glmultmatrix.md) were called with the generated matrix.</span></span> <span data-ttu-id="133f0-125">Per caricare la matrice della prospettiva nello stack della matrice corrente, anteporre al metodo la chiamata a **gluPerspective** con una chiamata a [**glLoadIdentity**](glloadidentity.md).</span><span class="sxs-lookup"><span data-stu-id="133f0-125">To load the perspective matrix onto the current matrix stack instead, precede the call to **gluPerspective** with a call to [**glLoadIdentity**](glloadidentity.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="133f0-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="133f0-126">Requirements</span></span>



| <span data-ttu-id="133f0-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="133f0-127">Requirement</span></span> | <span data-ttu-id="133f0-128">Valore</span><span class="sxs-lookup"><span data-stu-id="133f0-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="133f0-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="133f0-129">Minimum supported client</span></span><br/> | <span data-ttu-id="133f0-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="133f0-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="133f0-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="133f0-131">Minimum supported server</span></span><br/> | <span data-ttu-id="133f0-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="133f0-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="133f0-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="133f0-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="133f0-134"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="133f0-134"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="133f0-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="133f0-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="133f0-136"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="133f0-136"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="133f0-137">DLL</span><span class="sxs-lookup"><span data-stu-id="133f0-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="133f0-138"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="133f0-138"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="133f0-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="133f0-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="133f0-140">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="133f0-140">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="133f0-141">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="133f0-141">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="133f0-142">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="133f0-142">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="133f0-143">**gluOrtho2D**</span><span class="sxs-lookup"><span data-stu-id="133f0-143">**gluOrtho2D**</span></span>](gluortho2d.md)
</dt> </dl>

 

 





