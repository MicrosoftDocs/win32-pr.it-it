---
title: funzione glVertex4s (GL. h)
description: Specifica un vertice. | funzione glVertex4s (GL. h)
ms.assetid: 5030e0dd-9a81-482d-8d87-bfc9355a3c92
keywords:
- funzione glVertex4s OpenGL
topic_type:
- apiref
api_name:
- glVertex4s
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efcf64b6864d27e8df77056db14e9132cfbaaf5e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321999"
---
# <a name="glvertex4s-function"></a><span data-ttu-id="5040d-105">glVertex4s (funzione)</span><span class="sxs-lookup"><span data-stu-id="5040d-105">glVertex4s function</span></span>

<span data-ttu-id="5040d-106">Specifica un vertice.</span><span class="sxs-lookup"><span data-stu-id="5040d-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="5040d-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5040d-107">Syntax</span></span>


```C++
void WINAPI glVertex4s(
   GLshort x,
   GLshort y,
   GLshort z,
   GLshort w
);
```



## <a name="parameters"></a><span data-ttu-id="5040d-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5040d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5040d-109">*x*</span><span class="sxs-lookup"><span data-stu-id="5040d-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="5040d-110">Specifica la coordinata x di un vertice.</span><span class="sxs-lookup"><span data-stu-id="5040d-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="5040d-111">*y*</span><span class="sxs-lookup"><span data-stu-id="5040d-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="5040d-112">Specifica la coordinata y di un vertice.</span><span class="sxs-lookup"><span data-stu-id="5040d-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="5040d-113">*z*</span><span class="sxs-lookup"><span data-stu-id="5040d-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="5040d-114">Specifica la coordinata z di un vertice.</span><span class="sxs-lookup"><span data-stu-id="5040d-114">Specifies the z-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="5040d-115">*w*</span><span class="sxs-lookup"><span data-stu-id="5040d-115">*w*</span></span> 
</dt> <dd>

<span data-ttu-id="5040d-116">Specifica la coordinata w di un vertice.</span><span class="sxs-lookup"><span data-stu-id="5040d-116">Specifies the w-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5040d-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5040d-117">Return value</span></span>

<span data-ttu-id="5040d-118">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="5040d-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5040d-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="5040d-119">Remarks</span></span>

<span data-ttu-id="5040d-120">I comandi della funzione glVertex vengono usati all'interno delle coppie [**glBegin**](glbegin.md) / [**glEnd**](glend.md) per specificare i vertici punto, linea e poligono.</span><span class="sxs-lookup"><span data-stu-id="5040d-120">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="5040d-121">Le coordinate di colore, normali e di trama correnti sono associate al vertice quando viene chiamato glVertex.</span><span class="sxs-lookup"><span data-stu-id="5040d-121">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="5040d-122">Quando si specificano solo *x* e *y* , il valore predefinito per *z* è 0,0 e *w* viene impostato su 1,0.</span><span class="sxs-lookup"><span data-stu-id="5040d-122">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="5040d-123">Quando vengono specificati *x*, *y* e *z* , il valore predefinito di *w* è 1,0.</span><span class="sxs-lookup"><span data-stu-id="5040d-123">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="5040d-124">La chiamata di glVertex all'esterno di una coppia **glBegin** / **glEnd** comporta un comportamento non definito.</span><span class="sxs-lookup"><span data-stu-id="5040d-124">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="5040d-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5040d-125">Requirements</span></span>



| <span data-ttu-id="5040d-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5040d-126">Requirement</span></span> | <span data-ttu-id="5040d-127">Valore</span><span class="sxs-lookup"><span data-stu-id="5040d-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5040d-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5040d-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5040d-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5040d-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5040d-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5040d-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5040d-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5040d-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5040d-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5040d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="5040d-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5040d-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5040d-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="5040d-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="5040d-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5040d-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5040d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5040d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5040d-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5040d-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5040d-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5040d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5040d-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5040d-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5040d-140">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="5040d-140">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="5040d-141">**glColor**</span><span class="sxs-lookup"><span data-stu-id="5040d-141">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="5040d-142">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="5040d-142">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="5040d-143">**Remo**</span><span class="sxs-lookup"><span data-stu-id="5040d-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5040d-144">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="5040d-144">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="5040d-145">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="5040d-145">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="5040d-146">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="5040d-146">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="5040d-147">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="5040d-147">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="5040d-148">**glRect**</span><span class="sxs-lookup"><span data-stu-id="5040d-148">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="5040d-149">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="5040d-149">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





