---
title: funzione glRects (GL. h)
description: La funzione glRects disegna un rettangolo.
ms.assetid: cf56352a-3396-4061-aa5e-dada986cf4ca
keywords:
- funzione glRects OpenGL
topic_type:
- apiref
api_name:
- glRects
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcaa60d87c85001120da3a12005ca147b684b7a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121586"
---
# <a name="glrects-function"></a><span data-ttu-id="ba094-104">glRects (funzione)</span><span class="sxs-lookup"><span data-stu-id="ba094-104">glRects function</span></span>

<span data-ttu-id="ba094-105">La funzione **glRects** disegna un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="ba094-105">The **glRects** function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba094-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba094-106">Syntax</span></span>


```C++
void WINAPI glRects(
   GLshort x1,
   GLshort y1,
   GLshort x2,
   GLshort y2
);
```



## <a name="parameters"></a><span data-ttu-id="ba094-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ba094-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba094-108">*X1*</span><span class="sxs-lookup"><span data-stu-id="ba094-108">*x1*</span></span> 
</dt> <dd>

<span data-ttu-id="ba094-109">Coordinata *x* del vertice di un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="ba094-109">The *x* coordinate of the vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="ba094-110">*Y1*</span><span class="sxs-lookup"><span data-stu-id="ba094-110">*y1*</span></span> 
</dt> <dd>

<span data-ttu-id="ba094-111">Coordinata *y* del vertice di un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="ba094-111">The *y* coordinate of the vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="ba094-112">*X2*</span><span class="sxs-lookup"><span data-stu-id="ba094-112">*x2*</span></span> 
</dt> <dd>

<span data-ttu-id="ba094-113">Coordinata *x* del vertice opposto del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="ba094-113">The *x* coordinate of the opposite vertex of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="ba094-114">*Y2*</span><span class="sxs-lookup"><span data-stu-id="ba094-114">*y2*</span></span> 
</dt> <dd>

<span data-ttu-id="ba094-115">Coordinata *y* del vertice opposto del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="ba094-115">The *y* coordinate of the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba094-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ba094-116">Return value</span></span>

<span data-ttu-id="ba094-117">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ba094-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ba094-118">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ba094-118">Error codes</span></span>

<span data-ttu-id="ba094-119">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="ba094-119">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ba094-120">Nome</span><span class="sxs-lookup"><span data-stu-id="ba094-120">Name</span></span>                                                                                                  | <span data-ttu-id="ba094-121">Significato</span><span class="sxs-lookup"><span data-stu-id="ba094-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ba094-122"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ba094-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ba094-123">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ba094-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ba094-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba094-124">Remarks</span></span>

<span data-ttu-id="ba094-125">La funzione **glRects** supporta una specifica efficiente di rettangoli come due punti d'angolo.</span><span class="sxs-lookup"><span data-stu-id="ba094-125">The **glRects** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="ba094-126">Ogni comando Rectangle accetta quattro argomenti, organizzati come due coppie consecutive di coordinate (x, *y*) o come due puntatori a matrici, ognuna contenente una coppia (*x*, *y*).</span><span class="sxs-lookup"><span data-stu-id="ba094-126">Each rectangle command takes four arguments, organized either as two consecutive pairs of (x, *y*) coordinates, or as two pointers to arrays, each containing an (*x*, *y*) pair.</span></span> <span data-ttu-id="ba094-127">Il rettangolo risultante è definito nel piano *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="ba094-127">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="ba094-128">La funzione **glRects**(*x1,* *Y1,* *X2,* *Y2*) è esattamente equivalente alla sequenza seguente:</span><span class="sxs-lookup"><span data-stu-id="ba094-128">The **glRects**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="ba094-129">**glBegin**( \_ poligono GL);</span><span class="sxs-lookup"><span data-stu-id="ba094-129">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="ba094-130">**glVertex2**( *x1,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="ba094-130">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="ba094-131">**glVertex2**( *X2,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="ba094-131">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="ba094-132">**glVertex2**( *X2,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="ba094-132">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="ba094-133">**glVertex2**( *x1,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="ba094-133">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="ba094-134">**glEnd**();</span><span class="sxs-lookup"><span data-stu-id="ba094-134">**glEnd**( );</span></span>

<span data-ttu-id="ba094-135">Si noti che se il secondo vertice è sopra e a destra del primo vertice, il rettangolo viene costruito con una bobina in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="ba094-135">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba094-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba094-136">Requirements</span></span>



| <span data-ttu-id="ba094-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba094-137">Requirement</span></span> | <span data-ttu-id="ba094-138">Valore</span><span class="sxs-lookup"><span data-stu-id="ba094-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba094-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba094-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ba094-140">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ba094-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ba094-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba094-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ba094-142">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ba094-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ba094-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ba094-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba094-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba094-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ba094-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="ba094-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="ba094-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba094-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ba094-147">DLL</span><span class="sxs-lookup"><span data-stu-id="ba094-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba094-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba094-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba094-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba094-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba094-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ba094-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ba094-151">**Remo**</span><span class="sxs-lookup"><span data-stu-id="ba094-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ba094-152">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="ba094-152">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





