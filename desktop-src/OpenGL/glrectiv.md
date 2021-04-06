---
title: funzione glRectiv (GL. h)
description: La funzione glRectiv disegna un rettangolo.
ms.assetid: 24db6fc0-9b53-4e72-9b12-18ea65409f12
keywords:
- funzione glRectiv OpenGL
topic_type:
- apiref
api_name:
- glRectiv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 668e1f253a44833ee7b1e0210327e93536bb850f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873345"
---
# <a name="glrectiv-function"></a><span data-ttu-id="5c6d8-104">glRectiv (funzione)</span><span class="sxs-lookup"><span data-stu-id="5c6d8-104">glRectiv function</span></span>

<span data-ttu-id="5c6d8-105">La funzione **glRectiv** disegna un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="5c6d8-105">The **glRectiv** function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c6d8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c6d8-106">Syntax</span></span>


```C++
void WINAPI glRectiv(
   const GLint *v1,
   const GLint *v2
);
```



## <a name="parameters"></a><span data-ttu-id="5c6d8-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c6d8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c6d8-108">*v1*</span><span class="sxs-lookup"><span data-stu-id="5c6d8-108">*v1*</span></span> 
</dt> <dd>

<span data-ttu-id="5c6d8-109">Puntatore a un vertice di un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="5c6d8-109">A pointer to one vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="5c6d8-110">*v2*</span><span class="sxs-lookup"><span data-stu-id="5c6d8-110">*v2*</span></span> 
</dt> <dd>

<span data-ttu-id="5c6d8-111">puntatore al vertice opposto del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="5c6d8-111">a pointer to the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c6d8-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c6d8-112">Return value</span></span>

<span data-ttu-id="5c6d8-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="5c6d8-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5c6d8-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="5c6d8-114">Error codes</span></span>

<span data-ttu-id="5c6d8-115">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="5c6d8-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="5c6d8-116">Nome</span><span class="sxs-lookup"><span data-stu-id="5c6d8-116">Name</span></span>                                                                                                  | <span data-ttu-id="5c6d8-117">Significato</span><span class="sxs-lookup"><span data-stu-id="5c6d8-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5c6d8-118"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5c6d8-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="5c6d8-119">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="5c6d8-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5c6d8-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c6d8-120">Remarks</span></span>

<span data-ttu-id="5c6d8-121">La funzione **glRecti** supporta una specifica efficiente di rettangoli come due punti d'angolo.</span><span class="sxs-lookup"><span data-stu-id="5c6d8-121">The **glRecti** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="5c6d8-122">Ogni comando Rectangle accetta quattro argomenti, organizzati come due coppie consecutive di coordinate (*x*, *y*) o come due puntatori a matrici, ognuna contenente una coppia (*x*, *y*).</span><span class="sxs-lookup"><span data-stu-id="5c6d8-122">Each rectangle command takes four arguments, organized either as two consecutive pairs of (*x*, *y*) coordinates, or as two pointers to arrays, each containing an (*x*, *y*) pair.</span></span> <span data-ttu-id="5c6d8-123">Il rettangolo risultante è definito nel piano *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="5c6d8-123">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="5c6d8-124">La funzione **glRecti**(*x1,* *Y1,* *X2,* *Y2*) è esattamente equivalente alla sequenza seguente:</span><span class="sxs-lookup"><span data-stu-id="5c6d8-124">The **glRecti**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="5c6d8-125">**glBegin**( \_ poligono GL);</span><span class="sxs-lookup"><span data-stu-id="5c6d8-125">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="5c6d8-126">**glVertex2**( *x1,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="5c6d8-126">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="5c6d8-127">**glVertex2**( *X2,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="5c6d8-127">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="5c6d8-128">**glVertex2**( *X2,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="5c6d8-128">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="5c6d8-129">**glVertex2**( *x1,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="5c6d8-129">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="5c6d8-130">**glEnd**();</span><span class="sxs-lookup"><span data-stu-id="5c6d8-130">**glEnd**( );</span></span>

<span data-ttu-id="5c6d8-131">Si noti che se il secondo vertice è sopra e a destra del primo vertice, il rettangolo viene costruito con una bobina in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="5c6d8-131">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c6d8-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c6d8-132">Requirements</span></span>



| <span data-ttu-id="5c6d8-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c6d8-133">Requirement</span></span> | <span data-ttu-id="5c6d8-134">Valore</span><span class="sxs-lookup"><span data-stu-id="5c6d8-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c6d8-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c6d8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5c6d8-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5c6d8-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5c6d8-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c6d8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5c6d8-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5c6d8-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5c6d8-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c6d8-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c6d8-140"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c6d8-140"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="5c6d8-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="5c6d8-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="5c6d8-142"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c6d8-142"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="5c6d8-143">DLL</span><span class="sxs-lookup"><span data-stu-id="5c6d8-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c6d8-144"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c6d8-144"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c6d8-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c6d8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c6d8-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="5c6d8-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="5c6d8-147">**Remo**</span><span class="sxs-lookup"><span data-stu-id="5c6d8-147">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="5c6d8-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="5c6d8-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





