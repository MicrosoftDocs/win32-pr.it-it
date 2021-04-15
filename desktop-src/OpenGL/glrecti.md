---
title: funzione glRecti (GL. h)
description: La funzione glRecti disegna un rettangolo.
ms.assetid: 8f618b5e-5406-4342-8f7a-83a65bad8a6f
keywords:
- funzione glRecti OpenGL
topic_type:
- apiref
api_name:
- glRecti
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a17512c9720aea1d2b9dcf5c90b0bde4c67b8fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475250"
---
# <a name="glrecti-function"></a><span data-ttu-id="e88b0-104">glRecti (funzione)</span><span class="sxs-lookup"><span data-stu-id="e88b0-104">glRecti function</span></span>

<span data-ttu-id="e88b0-105">La funzione **glRecti** disegna un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="e88b0-105">The **glRecti** function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="e88b0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e88b0-106">Syntax</span></span>


```C++
void WINAPI glRecti(
   GLint x1,
   GLint y1,
   GLint x2,
   GLint y2
);
```



## <a name="parameters"></a><span data-ttu-id="e88b0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e88b0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e88b0-108">*X1*</span><span class="sxs-lookup"><span data-stu-id="e88b0-108">*x1*</span></span> 
</dt> <dd>

<span data-ttu-id="e88b0-109">Coordinata *x* del vertice di un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="e88b0-109">The *x* coordinate of the vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="e88b0-110">*Y1*</span><span class="sxs-lookup"><span data-stu-id="e88b0-110">*y1*</span></span> 
</dt> <dd>

<span data-ttu-id="e88b0-111">Coordinata *y* del vertice di un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="e88b0-111">The *y* coordinate of the vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="e88b0-112">*X2*</span><span class="sxs-lookup"><span data-stu-id="e88b0-112">*x2*</span></span> 
</dt> <dd>

<span data-ttu-id="e88b0-113">Coordinata *x* del vertice opposto del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="e88b0-113">The *x* coordinate of the opposite vertex of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="e88b0-114">*Y2*</span><span class="sxs-lookup"><span data-stu-id="e88b0-114">*y2*</span></span> 
</dt> <dd>

<span data-ttu-id="e88b0-115">Coordinata *y* del vertice opposto del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="e88b0-115">The *y* coordinate of the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e88b0-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e88b0-116">Return value</span></span>

<span data-ttu-id="e88b0-117">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="e88b0-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e88b0-118">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="e88b0-118">Error codes</span></span>

<span data-ttu-id="e88b0-119">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="e88b0-119">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e88b0-120">Nome</span><span class="sxs-lookup"><span data-stu-id="e88b0-120">Name</span></span>                                                                                                  | <span data-ttu-id="e88b0-121">Significato</span><span class="sxs-lookup"><span data-stu-id="e88b0-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e88b0-122"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e88b0-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e88b0-123">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e88b0-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e88b0-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="e88b0-124">Remarks</span></span>

<span data-ttu-id="e88b0-125">La funzione **glRecti** supporta una specifica efficiente di rettangoli come due punti d'angolo.</span><span class="sxs-lookup"><span data-stu-id="e88b0-125">The **glRecti** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="e88b0-126">Ogni comando Rectangle accetta quattro argomenti, organizzati come due coppie consecutive di coordinate (*x*, *y*) o come due puntatori a matrici, ognuna contenente una coppia (*x*, *y*).</span><span class="sxs-lookup"><span data-stu-id="e88b0-126">Each rectangle command takes four arguments, organized either as two consecutive pairs of (*x*, *y*) coordinates, or as two pointers to arrays, each containing an (*x*, *y*) pair.</span></span> <span data-ttu-id="e88b0-127">Il rettangolo risultante è definito nel piano *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="e88b0-127">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="e88b0-128">La funzione **glRecti**(*x1,* *Y1,* *X2,* *Y2*) è esattamente equivalente alla sequenza seguente:</span><span class="sxs-lookup"><span data-stu-id="e88b0-128">The **glRecti**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="e88b0-129">**glBegin**( \_ poligono GL);</span><span class="sxs-lookup"><span data-stu-id="e88b0-129">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="e88b0-130">**glVertex2**( *x1,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="e88b0-130">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="e88b0-131">**glVertex2**( *X2,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="e88b0-131">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="e88b0-132">**glVertex2**( *X2,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="e88b0-132">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="e88b0-133">**glVertex2**( *x1,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="e88b0-133">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="e88b0-134">**glEnd**();</span><span class="sxs-lookup"><span data-stu-id="e88b0-134">**glEnd**( );</span></span>

<span data-ttu-id="e88b0-135">Si noti che se il secondo vertice è sopra e a destra del primo vertice, il rettangolo viene costruito con una bobina in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="e88b0-135">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="e88b0-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e88b0-136">Requirements</span></span>



| <span data-ttu-id="e88b0-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="e88b0-137">Requirement</span></span> | <span data-ttu-id="e88b0-138">Valore</span><span class="sxs-lookup"><span data-stu-id="e88b0-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e88b0-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e88b0-139">Minimum supported client</span></span><br/> | <span data-ttu-id="e88b0-140">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e88b0-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e88b0-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e88b0-141">Minimum supported server</span></span><br/> | <span data-ttu-id="e88b0-142">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e88b0-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e88b0-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e88b0-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="e88b0-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e88b0-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e88b0-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="e88b0-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="e88b0-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e88b0-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e88b0-147">DLL</span><span class="sxs-lookup"><span data-stu-id="e88b0-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e88b0-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e88b0-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e88b0-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e88b0-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e88b0-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e88b0-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e88b0-151">**Remo**</span><span class="sxs-lookup"><span data-stu-id="e88b0-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e88b0-152">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="e88b0-152">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





