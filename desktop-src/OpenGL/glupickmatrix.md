---
title: funzione gluPickMatrix (Glu. h)
description: La funzione gluPickMatrix definisce un'area di selezione.
ms.assetid: 2f57345c-17a0-4716-8ab8-170aaed2b4f9
keywords:
- funzione gluPickMatrix OpenGL
topic_type:
- apiref
api_name:
- gluPickMatrix
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c54e62f82f52fedc7de7c7c4af1cd3ed1ccdf149
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963733"
---
# <a name="glupickmatrix-function"></a><span data-ttu-id="9feac-104">gluPickMatrix (funzione)</span><span class="sxs-lookup"><span data-stu-id="9feac-104">gluPickMatrix function</span></span>

<span data-ttu-id="9feac-105">La funzione **gluPickMatrix** definisce un'area di selezione.</span><span class="sxs-lookup"><span data-stu-id="9feac-105">The **gluPickMatrix** function defines a picking region.</span></span>

## <a name="syntax"></a><span data-ttu-id="9feac-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9feac-106">Syntax</span></span>


```C++
void WINAPI gluPickMatrix(
   GLdouble x,
   GLdouble y,
   GLdouble height,
   GLdouble width,
   GLint    viewport[4]
);
```



## <a name="parameters"></a><span data-ttu-id="9feac-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9feac-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9feac-108">*x*</span><span class="sxs-lookup"><span data-stu-id="9feac-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="9feac-109">Coordinata x della finestra di un'area di selezione.</span><span class="sxs-lookup"><span data-stu-id="9feac-109">The x window coordinate of a picking region.</span></span>

</dd> <dt>

<span data-ttu-id="9feac-110">*y*</span><span class="sxs-lookup"><span data-stu-id="9feac-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="9feac-111">Coordinata della finestra y di un'area di selezione.</span><span class="sxs-lookup"><span data-stu-id="9feac-111">The y window coordinate of a picking region.</span></span>

</dd> <dt>

<span data-ttu-id="9feac-112">*height*</span><span class="sxs-lookup"><span data-stu-id="9feac-112">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="9feac-113">Altezza dell'area di selezione nelle coordinate della finestra.</span><span class="sxs-lookup"><span data-stu-id="9feac-113">The height of the picking region in window coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="9feac-114">*width*</span><span class="sxs-lookup"><span data-stu-id="9feac-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="9feac-115">Larghezza dell'area di selezione nelle coordinate della finestra.</span><span class="sxs-lookup"><span data-stu-id="9feac-115">The width of the picking region in window coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="9feac-116">*Viewport*</span><span class="sxs-lookup"><span data-stu-id="9feac-116">*viewport*</span></span> 
</dt> <dd>

<span data-ttu-id="9feac-117">Viewport corrente (come da una chiamata [**glGetIntegerv**](glgetintegerv.md) ).</span><span class="sxs-lookup"><span data-stu-id="9feac-117">The current viewport (as from a [**glGetIntegerv**](glgetintegerv.md) call).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9feac-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9feac-118">Return value</span></span>

<span data-ttu-id="9feac-119">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="9feac-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9feac-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="9feac-120">Remarks</span></span>

<span data-ttu-id="9feac-121">La funzione **gluPickMatrix** crea una matrice di proiezione che è possibile usare per limitare il disegno a una piccola area del viewport.</span><span class="sxs-lookup"><span data-stu-id="9feac-121">The **gluPickMatrix** function creates a projection matrix you can use to restrict drawing to a small region of the viewport.</span></span>

1.  <span data-ttu-id="9feac-122">Usare **gluPickMatrix** per limitare il disegno a una piccola area attorno al cursore.</span><span class="sxs-lookup"><span data-stu-id="9feac-122">Use **gluPickMatrix** to restrict drawing to a small region around the cursor.</span></span>
2.  <span data-ttu-id="9feac-123">Immettere la modalità di selezione (con [**glRenderMode**](glrendermode.md)) e quindi eseguire nuovamente il rendering della scena.</span><span class="sxs-lookup"><span data-stu-id="9feac-123">Enter selection mode (with [**glRenderMode**](glrendermode.md)), and then rerender the scene.</span></span>

    <span data-ttu-id="9feac-124">Tutte le primitive che sarebbero state disegnate accanto al cursore vengono identificate e archiviate nel buffer di selezione.</span><span class="sxs-lookup"><span data-stu-id="9feac-124">All primitives that would have been drawn near the cursor are identified and stored in the selection buffer.</span></span>

<span data-ttu-id="9feac-125">La matrice creata da **gluPickMatrix** viene moltiplicata per la matrice corrente esattamente come se [**glMultMatrix**](glmultmatrix.md) venisse chiamato con la matrice generata.</span><span class="sxs-lookup"><span data-stu-id="9feac-125">The matrix created by **gluPickMatrix** is multiplied by the current matrix just as if [**glMultMatrix**](glmultmatrix.md) were called with the generated matrix.</span></span>

1.  <span data-ttu-id="9feac-126">Chiamare [**glLoadIdentity**](glloadidentity.md) per caricare una matrice di identità nello stack della matrice della prospettiva.</span><span class="sxs-lookup"><span data-stu-id="9feac-126">Call [**glLoadIdentity**](glloadidentity.md) to load an identity matrix onto the perspective matrix stack.</span></span>
2.  <span data-ttu-id="9feac-127">Chiamare **gluPickMatrix**.</span><span class="sxs-lookup"><span data-stu-id="9feac-127">Call **gluPickMatrix**.</span></span>
3.  <span data-ttu-id="9feac-128">Chiamare una funzione (ad esempio [**gluPerspective**](gluperspective.md)) per moltiplicare la matrice della prospettiva per la matrice di selezione.</span><span class="sxs-lookup"><span data-stu-id="9feac-128">Call a function (such as [**gluPerspective**](gluperspective.md)) to multiply the perspective matrix by the pick matrix.</span></span>

<span data-ttu-id="9feac-129">Quando si usa **gluPickMatrix** per selezionare una spline B-spline razionale non uniforme ([NURBS](using-nurbs-curves-and-surfaces.md)), prestare attenzione a disattivare la proprietà NURBS, Glu \_ auto \_ Load \_ Matrix.</span><span class="sxs-lookup"><span data-stu-id="9feac-129">When using **gluPickMatrix** to pick Non-Uniform Rational B-Spline ([NURBS](using-nurbs-curves-and-surfaces.md)), be careful to turn off the NURBS property, GLU\_AUTO\_LOAD\_MATRIX.</span></span> <span data-ttu-id="9feac-130">Se \_ \_ la matrice di caricamento automatico Glu non è disattivata \_ , qualsiasi superficie NURBS sottoposta a rendering viene suddivisa in modo diverso rispetto alla matrice di selezione rispetto alla relativa suddivisione senza la matrice di selezione.</span><span class="sxs-lookup"><span data-stu-id="9feac-130">If GLU\_AUTO\_LOAD\_MATRIX is not turned off, any NURBS surface rendered is subdivided differently with the pick matrix from how it was subdivided without the pick matrix.</span></span>

## <a name="examples"></a><span data-ttu-id="9feac-131">Esempio</span><span class="sxs-lookup"><span data-stu-id="9feac-131">Examples</span></span>

<span data-ttu-id="9feac-132">Quando si esegue il rendering di una scena come segue:</span><span class="sxs-lookup"><span data-stu-id="9feac-132">When rendering a scene as follows:</span></span>


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



<span data-ttu-id="9feac-133">il codice seguente seleziona una parte del viewport:</span><span class="sxs-lookup"><span data-stu-id="9feac-133">the following code selects a portion of the viewport:</span></span>


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPickMatrix(x, y, width, height, viewport);  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



## <a name="requirements"></a><span data-ttu-id="9feac-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9feac-134">Requirements</span></span>



| <span data-ttu-id="9feac-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="9feac-135">Requirement</span></span> | <span data-ttu-id="9feac-136">Valore</span><span class="sxs-lookup"><span data-stu-id="9feac-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9feac-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9feac-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9feac-138">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9feac-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9feac-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9feac-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9feac-140">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9feac-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9feac-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9feac-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="9feac-142"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="9feac-142"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="9feac-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="9feac-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="9feac-144"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9feac-144"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9feac-145">DLL</span><span class="sxs-lookup"><span data-stu-id="9feac-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9feac-146"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9feac-146"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9feac-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9feac-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9feac-148">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="9feac-148">**glGetIntegerv**</span></span>](glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="9feac-149">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="9feac-149">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="9feac-150">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="9feac-150">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="9feac-151">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="9feac-151">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="9feac-152">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="9feac-152">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





