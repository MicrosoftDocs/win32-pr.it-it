---
title: funzione glVertex4i (GL. h)
description: Specifica un vertice. | funzione glVertex4i (GL. h)
ms.assetid: eb73c5eb-c03d-489f-b323-bb2245d9b34c
keywords:
- funzione glVertex4i OpenGL
topic_type:
- apiref
api_name:
- glVertex4i
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a354c5b1f386147a55bb94c5bcdacd862c1c41b2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106322000"
---
# <a name="glvertex4i-function"></a><span data-ttu-id="c8bc9-105">glVertex4i (funzione)</span><span class="sxs-lookup"><span data-stu-id="c8bc9-105">glVertex4i function</span></span>

<span data-ttu-id="c8bc9-106">Specifica un vertice.</span><span class="sxs-lookup"><span data-stu-id="c8bc9-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8bc9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c8bc9-107">Syntax</span></span>


```C++
void WINAPI glVertex4i(
   GLint x,
   GLint y,
   GLint z,
   GLint w
);
```



## <a name="parameters"></a><span data-ttu-id="c8bc9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c8bc9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8bc9-109">*x*</span><span class="sxs-lookup"><span data-stu-id="c8bc9-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="c8bc9-110">Specifica la coordinata x di un vertice.</span><span class="sxs-lookup"><span data-stu-id="c8bc9-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="c8bc9-111">*y*</span><span class="sxs-lookup"><span data-stu-id="c8bc9-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="c8bc9-112">Specifica la coordinata y di un vertice.</span><span class="sxs-lookup"><span data-stu-id="c8bc9-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="c8bc9-113">*z*</span><span class="sxs-lookup"><span data-stu-id="c8bc9-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="c8bc9-114">Specifica la coordinata z di un vertice.</span><span class="sxs-lookup"><span data-stu-id="c8bc9-114">Specifies the z-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="c8bc9-115">*w*</span><span class="sxs-lookup"><span data-stu-id="c8bc9-115">*w*</span></span> 
</dt> <dd>

<span data-ttu-id="c8bc9-116">Specifica la coordinata w di un vertice.</span><span class="sxs-lookup"><span data-stu-id="c8bc9-116">Specifies the w-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8bc9-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c8bc9-117">Return value</span></span>

<span data-ttu-id="c8bc9-118">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="c8bc9-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8bc9-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="c8bc9-119">Remarks</span></span>

<span data-ttu-id="c8bc9-120">I comandi della funzione glVertex vengono usati all'interno delle coppie [**glBegin**](glbegin.md) / [**glEnd**](glend.md) per specificare i vertici punto, linea e poligono.</span><span class="sxs-lookup"><span data-stu-id="c8bc9-120">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="c8bc9-121">Le coordinate di colore, normali e di trama correnti sono associate al vertice quando viene chiamato glVertex.</span><span class="sxs-lookup"><span data-stu-id="c8bc9-121">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="c8bc9-122">Quando si specificano solo *x* e *y* , il valore predefinito per *z* è 0,0 e *w* viene impostato su 1,0.</span><span class="sxs-lookup"><span data-stu-id="c8bc9-122">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="c8bc9-123">Quando vengono specificati *x*, *y* e *z* , il valore predefinito di *w* è 1,0.</span><span class="sxs-lookup"><span data-stu-id="c8bc9-123">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="c8bc9-124">La chiamata di glVertex all'esterno di una coppia **glBegin** / **glEnd** comporta un comportamento non definito.</span><span class="sxs-lookup"><span data-stu-id="c8bc9-124">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8bc9-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c8bc9-125">Requirements</span></span>



| <span data-ttu-id="c8bc9-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8bc9-126">Requirement</span></span> | <span data-ttu-id="c8bc9-127">Valore</span><span class="sxs-lookup"><span data-stu-id="c8bc9-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8bc9-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8bc9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c8bc9-129">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c8bc9-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c8bc9-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c8bc9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c8bc9-131">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c8bc9-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c8bc9-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c8bc9-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8bc9-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8bc9-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="c8bc9-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="c8bc9-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="c8bc9-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8bc9-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="c8bc9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c8bc9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8bc9-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8bc9-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8bc9-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c8bc9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8bc9-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="c8bc9-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="c8bc9-140">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="c8bc9-140">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="c8bc9-141">**glColor**</span><span class="sxs-lookup"><span data-stu-id="c8bc9-141">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="c8bc9-142">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="c8bc9-142">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="c8bc9-143">**Remo**</span><span class="sxs-lookup"><span data-stu-id="c8bc9-143">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="c8bc9-144">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="c8bc9-144">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="c8bc9-145">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="c8bc9-145">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="c8bc9-146">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="c8bc9-146">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="c8bc9-147">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="c8bc9-147">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="c8bc9-148">**glRect**</span><span class="sxs-lookup"><span data-stu-id="c8bc9-148">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="c8bc9-149">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="c8bc9-149">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





