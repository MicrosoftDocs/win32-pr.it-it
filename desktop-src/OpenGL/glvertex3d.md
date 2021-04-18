---
title: funzione glVertex3d (GL. h)
description: Specifica un vertice. | funzione glVertex3d (GL. h)
ms.assetid: 531a552d-7979-4994-ad28-73c2d3987bae
keywords:
- funzione glVertex3d OpenGL
topic_type:
- apiref
api_name:
- glVertex3d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 608ab02bf2cd41b7f2ffcc8fa3fe8cb2dea0ca89
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321846"
---
# <a name="glvertex3d-function"></a><span data-ttu-id="b3ae8-105">glVertex3d (funzione)</span><span class="sxs-lookup"><span data-stu-id="b3ae8-105">glVertex3d function</span></span>

<span data-ttu-id="b3ae8-106">Specifica un vertice.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3ae8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3ae8-107">Syntax</span></span>


```C++
void WINAPI glVertex3d(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a><span data-ttu-id="b3ae8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b3ae8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3ae8-109">*x*</span><span class="sxs-lookup"><span data-stu-id="b3ae8-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="b3ae8-110">Specifica la coordinata x di un vertice.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="b3ae8-111">*y*</span><span class="sxs-lookup"><span data-stu-id="b3ae8-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="b3ae8-112">Specifica la coordinata y di un vertice.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="b3ae8-113">*z*</span><span class="sxs-lookup"><span data-stu-id="b3ae8-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="b3ae8-114">Specifica la coordinata z di un vertice.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-114">Specifies the z-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3ae8-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b3ae8-115">Return value</span></span>

<span data-ttu-id="b3ae8-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-116">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3ae8-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3ae8-117">Remarks</span></span>

<span data-ttu-id="b3ae8-118">I comandi della funzione glVertex vengono usati all'interno delle coppie [**glBegin**](glbegin.md) / [**glEnd**](glend.md) per specificare i vertici punto, linea e poligono.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-118">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="b3ae8-119">Le coordinate di colore, normali e di trama correnti sono associate al vertice quando viene chiamato glVertex.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-119">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="b3ae8-120">Quando si specificano solo *x* e *y* , il valore predefinito per *z* è 0,0 e *w* viene impostato su 1,0.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-120">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="b3ae8-121">Quando vengono specificati *x*, *y* e *z* , il valore predefinito di *w* è 1,0.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-121">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="b3ae8-122">La chiamata di glVertex all'esterno di una coppia **glBegin** / **glEnd** comporta un comportamento non definito.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-122">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3ae8-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3ae8-123">Requirements</span></span>



| <span data-ttu-id="b3ae8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3ae8-124">Requirement</span></span> | <span data-ttu-id="b3ae8-125">Valore</span><span class="sxs-lookup"><span data-stu-id="b3ae8-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3ae8-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3ae8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b3ae8-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b3ae8-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b3ae8-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3ae8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b3ae8-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b3ae8-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b3ae8-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3ae8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3ae8-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3ae8-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b3ae8-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="b3ae8-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="b3ae8-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3ae8-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b3ae8-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b3ae8-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3ae8-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3ae8-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3ae8-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3ae8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3ae8-137">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b3ae8-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b3ae8-138">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="b3ae8-138">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="b3ae8-139">**glColor**</span><span class="sxs-lookup"><span data-stu-id="b3ae8-139">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="b3ae8-140">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="b3ae8-140">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="b3ae8-141">**Remo**</span><span class="sxs-lookup"><span data-stu-id="b3ae8-141">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b3ae8-142">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="b3ae8-142">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="b3ae8-143">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="b3ae8-143">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="b3ae8-144">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="b3ae8-144">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="b3ae8-145">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="b3ae8-145">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="b3ae8-146">**glRect**</span><span class="sxs-lookup"><span data-stu-id="b3ae8-146">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="b3ae8-147">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="b3ae8-147">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





