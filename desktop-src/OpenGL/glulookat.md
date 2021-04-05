---
title: funzione gluLookAt (Glu. h)
description: La funzione gluLookAt definisce una trasformazione di visualizzazione.
ms.assetid: 1fd87701-19c2-49b9-99ac-10e70aaedbfd
keywords:
- funzione gluLookAt OpenGL
topic_type:
- apiref
api_name:
- gluLookAt
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5866f3c06ef6969c95eeef4b23fff7a4e7852eb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874614"
---
# <a name="glulookat-function"></a><span data-ttu-id="18661-104">gluLookAt (funzione)</span><span class="sxs-lookup"><span data-stu-id="18661-104">gluLookAt function</span></span>

<span data-ttu-id="18661-105">La funzione **gluLookAt** definisce una trasformazione di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="18661-105">The **gluLookAt** function defines a viewing transformation.</span></span>

## <a name="syntax"></a><span data-ttu-id="18661-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18661-106">Syntax</span></span>


```C++
void WINAPI gluLookAt(
   GLdouble eyex,
   GLdouble eyey,
   GLdouble eyez,
   GLdouble centerx,
   GLdouble centery,
   GLdouble centerz,
   GLdouble upx,
   GLdouble upy,
   GLdouble upz
);
```



## <a name="parameters"></a><span data-ttu-id="18661-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="18661-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18661-108">*eyex*</span><span class="sxs-lookup"><span data-stu-id="18661-108">*eyex*</span></span> 
</dt> <dd>

<span data-ttu-id="18661-109">Posizione del punto d'occhio.</span><span class="sxs-lookup"><span data-stu-id="18661-109">The position of the eye point.</span></span>

</dd> <dt>

<span data-ttu-id="18661-110">*eyey*</span><span class="sxs-lookup"><span data-stu-id="18661-110">*eyey*</span></span> 
</dt> <dd>

<span data-ttu-id="18661-111">Posizione del punto d'occhio.</span><span class="sxs-lookup"><span data-stu-id="18661-111">The position of the eye point.</span></span>

</dd> <dt>

<span data-ttu-id="18661-112">*Eyez*</span><span class="sxs-lookup"><span data-stu-id="18661-112">*eyez*</span></span> 
</dt> <dd>

<span data-ttu-id="18661-113">Posizione del punto d'occhio.</span><span class="sxs-lookup"><span data-stu-id="18661-113">The position of the eye point.</span></span>

</dd> <dt>

<span data-ttu-id="18661-114">*CenterX*</span><span class="sxs-lookup"><span data-stu-id="18661-114">*centerx*</span></span> 
</dt> <dd>

<span data-ttu-id="18661-115">Posizione del punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="18661-115">The position of the reference point.</span></span>

</dd> <dt>

<span data-ttu-id="18661-116">*CenterY*</span><span class="sxs-lookup"><span data-stu-id="18661-116">*centery*</span></span> 
</dt> <dd>

<span data-ttu-id="18661-117">Posizione del punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="18661-117">The position of the reference point.</span></span>

</dd> <dt>

<span data-ttu-id="18661-118">*CenterZ*</span><span class="sxs-lookup"><span data-stu-id="18661-118">*centerz*</span></span> 
</dt> <dd>

<span data-ttu-id="18661-119">Posizione del punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="18661-119">The position of the reference point.</span></span>

</dd> <dt>

<span data-ttu-id="18661-120">*UPX*</span><span class="sxs-lookup"><span data-stu-id="18661-120">*upx*</span></span> 
</dt> <dd>

<span data-ttu-id="18661-121">Direzione del vettore verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="18661-121">The direction of the up vector.</span></span>

</dd> <dt>

<span data-ttu-id="18661-122">*upy*</span><span class="sxs-lookup"><span data-stu-id="18661-122">*upy*</span></span> 
</dt> <dd>

<span data-ttu-id="18661-123">Direzione del vettore verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="18661-123">The direction of the up vector.</span></span>

</dd> <dt>

<span data-ttu-id="18661-124">*UPZ*</span><span class="sxs-lookup"><span data-stu-id="18661-124">*upz*</span></span> 
</dt> <dd>

<span data-ttu-id="18661-125">Direzione del vettore verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="18661-125">The direction of the up vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18661-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="18661-126">Return value</span></span>

<span data-ttu-id="18661-127">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="18661-127">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="18661-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="18661-128">Remarks</span></span>

<span data-ttu-id="18661-129">La funzione **gluLookAt** crea una matrice di visualizzazione derivata da un punto d'occhio, un punto di riferimento che indica il centro della scena e un vettore up.</span><span class="sxs-lookup"><span data-stu-id="18661-129">The **gluLookAt** function creates a viewing matrix derived from an eye point, a reference point indicating the center of the scene, and an up vector.</span></span> <span data-ttu-id="18661-130">La matrice esegue il mapping del punto di riferimento all'asse z negativo e il punto d'occhio all'origine, in modo che quando si usa una matrice di proiezione tipica, il centro della scena viene mappato al centro del viewport.</span><span class="sxs-lookup"><span data-stu-id="18661-130">The matrix maps the reference point to the negative z-axis and the eye point to the origin, so that when you use a typical projection matrix, the center of the scene maps to the center of the viewport.</span></span> <span data-ttu-id="18661-131">Analogamente, la direzione descritta dal vettore up proiettata sul piano di visualizzazione viene mappata all'asse y positivo in modo che punti verso l'alto nel viewport.</span><span class="sxs-lookup"><span data-stu-id="18661-131">Similarly, the direction described by the up vector projected onto the viewing plane is mapped to the positive y-axis so that it points upward in the viewport.</span></span> <span data-ttu-id="18661-132">Il vettore up non deve essere parallelo alla linea di vista dall'occhio al punto di riferimento.</span><span class="sxs-lookup"><span data-stu-id="18661-132">The up vector must not be parallel to the line of sight from the eye to the reference point.</span></span>

<span data-ttu-id="18661-133">La matrice generata da **gluLookAt** moltiplica la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="18661-133">The matrix generated by **gluLookAt** postmultiplies the current matrix.</span></span>

## <a name="requirements"></a><span data-ttu-id="18661-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18661-134">Requirements</span></span>



| <span data-ttu-id="18661-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="18661-135">Requirement</span></span> | <span data-ttu-id="18661-136">Valore</span><span class="sxs-lookup"><span data-stu-id="18661-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="18661-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18661-137">Minimum supported client</span></span><br/> | <span data-ttu-id="18661-138">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="18661-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="18661-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="18661-139">Minimum supported server</span></span><br/> | <span data-ttu-id="18661-140">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="18661-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="18661-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="18661-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="18661-142"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="18661-142"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="18661-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="18661-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="18661-144"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18661-144"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="18661-145">DLL</span><span class="sxs-lookup"><span data-stu-id="18661-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18661-146"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18661-146"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18661-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18661-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18661-148">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="18661-148">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="18661-149">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="18661-149">**gluPerspective**</span></span>](gluperspective.md)
</dt> </dl>

 

 





