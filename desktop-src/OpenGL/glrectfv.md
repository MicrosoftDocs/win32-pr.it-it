---
title: funzione glRectfv (GL. h)
description: La funzione glRectfv disegna un rettangolo.
ms.assetid: 2053890e-bae7-4c06-98e7-5ce4314fe95c
keywords:
- funzione glRectfv OpenGL
topic_type:
- apiref
api_name:
- glRectfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 871cd3edc44598ba66fb686d9957af7322d77730
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400248"
---
# <a name="glrectfv-function"></a><span data-ttu-id="ddbed-104">glRectfv (funzione)</span><span class="sxs-lookup"><span data-stu-id="ddbed-104">glRectfv function</span></span>

<span data-ttu-id="ddbed-105">La funzione [**glRectfv**](glrectdv.md) disegna un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="ddbed-105">The [**glRectfv**](glrectdv.md) function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddbed-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ddbed-106">Syntax</span></span>


```C++
void WINAPI glRectfv(
   const GLfloat *v1,
   const GLfloat *v2
);
```



## <a name="parameters"></a><span data-ttu-id="ddbed-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ddbed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddbed-108">*v1*</span><span class="sxs-lookup"><span data-stu-id="ddbed-108">*v1*</span></span> 
</dt> <dd>

<span data-ttu-id="ddbed-109">Puntatore a un vertice di un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="ddbed-109">A pointer to one vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="ddbed-110">*v2*</span><span class="sxs-lookup"><span data-stu-id="ddbed-110">*v2*</span></span> 
</dt> <dd>

<span data-ttu-id="ddbed-111">puntatore al vertice opposto del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="ddbed-111">a pointer to the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddbed-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ddbed-112">Return value</span></span>

<span data-ttu-id="ddbed-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ddbed-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ddbed-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ddbed-114">Error codes</span></span>

<span data-ttu-id="ddbed-115">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="ddbed-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ddbed-116">Nome</span><span class="sxs-lookup"><span data-stu-id="ddbed-116">Name</span></span>                                                                                                  | <span data-ttu-id="ddbed-117">Significato</span><span class="sxs-lookup"><span data-stu-id="ddbed-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ddbed-118"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ddbed-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ddbed-119">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ddbed-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ddbed-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="ddbed-120">Remarks</span></span>

<span data-ttu-id="ddbed-121">La funzione **glRectf** supporta una specifica efficiente di rettangoli come due punti d'angolo.</span><span class="sxs-lookup"><span data-stu-id="ddbed-121">The **glRectf** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="ddbed-122">Ogni comando Rectangle accetta quattro argomenti, organizzati come due coppie consecutive di coordinate (*x*, *y*) o come due puntatori a matrici, ognuna contenente una coppia (*x*, *y*).</span><span class="sxs-lookup"><span data-stu-id="ddbed-122">Each rectangle command takes four arguments, organized either as two consecutive pairs of (*x*, *y*) coordinates, or as two pointers to arrays, each containing an (*x*, *y*) pair.</span></span> <span data-ttu-id="ddbed-123">Il rettangolo risultante è definito nel piano *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="ddbed-123">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="ddbed-124">La funzione **glRectf**(*x1,* *Y1,* *X2,* *Y2*) è esattamente equivalente alla sequenza seguente:</span><span class="sxs-lookup"><span data-stu-id="ddbed-124">The **glRectf**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="ddbed-125">**glBegin**( \_ poligono GL);</span><span class="sxs-lookup"><span data-stu-id="ddbed-125">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="ddbed-126">**glVertex2**( *x1,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="ddbed-126">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="ddbed-127">**glVertex2**( *X2,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="ddbed-127">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="ddbed-128">**glVertex2**( *X2,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="ddbed-128">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="ddbed-129">**glVertex2**( *x1,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="ddbed-129">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="ddbed-130">**glEnd**();</span><span class="sxs-lookup"><span data-stu-id="ddbed-130">**glEnd**( );</span></span>

<span data-ttu-id="ddbed-131">Si noti che se il secondo vertice è sopra e a destra del primo vertice, il rettangolo viene costruito con una bobina in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="ddbed-131">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddbed-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ddbed-132">Requirements</span></span>



| <span data-ttu-id="ddbed-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddbed-133">Requirement</span></span> | <span data-ttu-id="ddbed-134">Valore</span><span class="sxs-lookup"><span data-stu-id="ddbed-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddbed-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ddbed-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ddbed-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ddbed-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ddbed-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ddbed-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ddbed-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ddbed-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ddbed-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ddbed-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddbed-140"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddbed-140"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ddbed-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="ddbed-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="ddbed-142"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ddbed-142"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ddbed-143">DLL</span><span class="sxs-lookup"><span data-stu-id="ddbed-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddbed-144"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddbed-144"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddbed-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ddbed-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddbed-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ddbed-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ddbed-147">**Remo**</span><span class="sxs-lookup"><span data-stu-id="ddbed-147">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ddbed-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="ddbed-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





