---
title: funzione glVertex2s (GL. h)
description: Specifica un vertice. | funzione glVertex2s (GL. h)
ms.assetid: e964d7b0-1cb7-4334-8861-1cc2ee37a71a
keywords:
- funzione glVertex2s OpenGL
topic_type:
- apiref
api_name:
- glVertex2s
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8056c7cb2447eb1bb00915096a618de0d6f272d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321639"
---
# <a name="glvertex2s-function"></a><span data-ttu-id="6b44c-105">glVertex2s (funzione)</span><span class="sxs-lookup"><span data-stu-id="6b44c-105">glVertex2s function</span></span>

<span data-ttu-id="6b44c-106">Specifica un vertice.</span><span class="sxs-lookup"><span data-stu-id="6b44c-106">Specifies a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b44c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b44c-107">Syntax</span></span>


```C++
void WINAPI glVertex2s(
   GLshort x,
   GLshort y
);
```



## <a name="parameters"></a><span data-ttu-id="6b44c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b44c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b44c-109">*x*</span><span class="sxs-lookup"><span data-stu-id="6b44c-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="6b44c-110">Specifica la coordinata x di un vertice.</span><span class="sxs-lookup"><span data-stu-id="6b44c-110">Specifies the x-coordinate of a vertex.</span></span>

</dd> <dt>

<span data-ttu-id="6b44c-111">*y*</span><span class="sxs-lookup"><span data-stu-id="6b44c-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="6b44c-112">Specifica la coordinata y di un vertice.</span><span class="sxs-lookup"><span data-stu-id="6b44c-112">Specifies the y-coordinate of a vertex.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b44c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b44c-113">Return value</span></span>

<span data-ttu-id="6b44c-114">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="6b44c-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b44c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b44c-115">Remarks</span></span>

<span data-ttu-id="6b44c-116">I comandi della funzione glVertex vengono usati all'interno delle coppie [**glBegin**](glbegin.md) / [**glEnd**](glend.md) per specificare i vertici punto, linea e poligono.</span><span class="sxs-lookup"><span data-stu-id="6b44c-116">The glVertex function commands are used within [**glBegin**](glbegin.md)/[**glEnd**](glend.md) pairs to specify point, line, and polygon vertices.</span></span> <span data-ttu-id="6b44c-117">Le coordinate di colore, normali e di trama correnti sono associate al vertice quando viene chiamato glVertex.</span><span class="sxs-lookup"><span data-stu-id="6b44c-117">The current color, normal, and texture coordinates are associated with the vertex when glVertex is called.</span></span> <span data-ttu-id="6b44c-118">Quando si specificano solo *x* e *y* , il valore predefinito per *z* è 0,0 e *w* viene impostato su 1,0.</span><span class="sxs-lookup"><span data-stu-id="6b44c-118">When only *x* and *y* are specified, *z* defaults to 0.0 and *w* defaults to 1.0.</span></span> <span data-ttu-id="6b44c-119">Quando vengono specificati *x*, *y* e *z* , il valore predefinito di *w* è 1,0.</span><span class="sxs-lookup"><span data-stu-id="6b44c-119">When *x*, *y*, and *z* are specified, *w* defaults to 1.0.</span></span> <span data-ttu-id="6b44c-120">La chiamata di glVertex all'esterno di una coppia **glBegin** / **glEnd** comporta un comportamento non definito.</span><span class="sxs-lookup"><span data-stu-id="6b44c-120">Invoking glVertex outside of a **glBegin**/**glEnd** pair results in undefined behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b44c-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b44c-121">Requirements</span></span>



| <span data-ttu-id="6b44c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b44c-122">Requirement</span></span> | <span data-ttu-id="6b44c-123">Valore</span><span class="sxs-lookup"><span data-stu-id="6b44c-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b44c-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b44c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6b44c-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6b44c-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6b44c-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b44c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6b44c-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6b44c-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6b44c-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b44c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b44c-129"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b44c-129"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6b44c-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="6b44c-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="6b44c-131"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b44c-131"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6b44c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6b44c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b44c-133"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b44c-133"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b44c-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b44c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b44c-135">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6b44c-135">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6b44c-136">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="6b44c-136">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="6b44c-137">**glColor**</span><span class="sxs-lookup"><span data-stu-id="6b44c-137">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="6b44c-138">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="6b44c-138">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="6b44c-139">**Remo**</span><span class="sxs-lookup"><span data-stu-id="6b44c-139">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6b44c-140">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="6b44c-140">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="6b44c-141">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="6b44c-141">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="6b44c-142">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="6b44c-142">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="6b44c-143">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="6b44c-143">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="6b44c-144">**glRect**</span><span class="sxs-lookup"><span data-stu-id="6b44c-144">**glRect**</span></span>](glrect-functions.md)
</dt> <dt>

[<span data-ttu-id="6b44c-145">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="6b44c-145">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> </dl>

 

 





