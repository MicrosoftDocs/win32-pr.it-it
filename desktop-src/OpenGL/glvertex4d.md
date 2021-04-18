---
title: funzione glVertex4d (GL. h)
description: Specifica un vertice. | funzione glVertex4d (GL. h)
ms.assetid: d9203e4f-5ed2-41e7-b619-65cee3132ed9
keywords:
- funzione glVertex4d OpenGL
topic_type:
- apiref
api_name:
- glVertex4d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a28a64c35ff30cc668839899dca4f3dc2958ff9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106322002"
---
# <a name="glvertex4d-function"></a><span data-ttu-id="ad555-105">glVertex4d (funzione)</span><span class="sxs-lookup"><span data-stu-id="ad555-105">glVertex4d function</span></span>

<span data-ttu-id="ad555-106">Specifica un vertice.</span><span class="sxs-lookup"><span data-stu-id="ad555-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad555-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad555-107">Syntax</span></span>


```C++
void WINAPI glVertex4d(
   GLdouble x,
   GLdouble y,
   GLdouble z,
   GLdouble w
);
```



## <a name="parameters"></a><span data-ttu-id="ad555-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad555-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad555-109">*x*</span><span class="sxs-lookup"><span data-stu-id="ad555-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="ad555-110">Specifica la coordinata x di un vertice.</span><span class="sxs-lookup"><span data-stu-id="ad555-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="ad555-111">*y*</span><span class="sxs-lookup"><span data-stu-id="ad555-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="ad555-112">Specifica la coordinata y di un vertice.</span><span class="sxs-lookup"><span data-stu-id="ad555-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="ad555-113">*z*</span><span class="sxs-lookup"><span data-stu-id="ad555-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="ad555-114">Specifica la coordinata z di un vertice.</span><span class="sxs-lookup"><span data-stu-id="ad555-114">Specifies the z-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="ad555-115">*w*</span><span class="sxs-lookup"><span data-stu-id="ad555-115">*w*</span></span> 
</dt> <dd>

<span data-ttu-id="ad555-116">Specifica la coordinata w di un vertice.</span><span class="sxs-lookup"><span data-stu-id="ad555-116">Specifies the w-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad555-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad555-117">Return value</span></span>

<span data-ttu-id="ad555-118">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ad555-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad555-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad555-119">Remarks</span></span>

<span data-ttu-id="ad555-120">I comandi della funzione glVertex vengono usati all'interno delle coppie [**glBegin**](glbegin.md) / [**glEnd**](glend.md) per specificare i vertici punto, linea e poligono.</span><span class="sxs-lookup"><span data-stu-id="ad555-120">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="ad555-121">Le coordinate di colore, normali e di trama correnti sono associate al vertice quando viene chiamato glVertex.</span><span class="sxs-lookup"><span data-stu-id="ad555-121">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="ad555-122">Quando si specificano solo *x* e *y* , il valore predefinito per *z* è 0,0 e *w* viene impostato su 1,0.</span><span class="sxs-lookup"><span data-stu-id="ad555-122">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="ad555-123">Quando vengono specificati *x*, *y* e *z* , il valore predefinito di *w* è 1,0.</span><span class="sxs-lookup"><span data-stu-id="ad555-123">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="ad555-124">La chiamata di glVertex all'esterno di una coppia **glBegin** / **glEnd** comporta un comportamento non definito.</span><span class="sxs-lookup"><span data-stu-id="ad555-124">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad555-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad555-125">Requirements</span></span>



| <span data-ttu-id="ad555-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad555-126">Requirement</span></span> | <span data-ttu-id="ad555-127">Valore</span><span class="sxs-lookup"><span data-stu-id="ad555-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad555-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad555-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ad555-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ad555-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ad555-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad555-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ad555-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ad555-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ad555-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad555-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad555-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad555-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ad555-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="ad555-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="ad555-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad555-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ad555-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ad555-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad555-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad555-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad555-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad555-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad555-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ad555-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ad555-140">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="ad555-140">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="ad555-141">**glColor**</span><span class="sxs-lookup"><span data-stu-id="ad555-141">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="ad555-142">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="ad555-142">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="ad555-143">**Remo**</span><span class="sxs-lookup"><span data-stu-id="ad555-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ad555-144">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="ad555-144">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="ad555-145">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="ad555-145">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="ad555-146">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="ad555-146">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="ad555-147">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="ad555-147">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="ad555-148">**glRect**</span><span class="sxs-lookup"><span data-stu-id="ad555-148">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="ad555-149">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="ad555-149">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





