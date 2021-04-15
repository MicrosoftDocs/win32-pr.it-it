---
title: funzione glRectsv (GL. h)
description: La funzione glRectsv disegna un rettangolo.
ms.assetid: 0f7dc4fc-b6ce-4240-89d9-69f54c0c9f2b
keywords:
- funzione glRectsv OpenGL
topic_type:
- apiref
api_name:
- glRectsv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90bdf6ce7d882db9c7cc1f78deddc3ca651a2c6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479258"
---
# <a name="glrectsv-function"></a><span data-ttu-id="42654-104">glRectsv (funzione)</span><span class="sxs-lookup"><span data-stu-id="42654-104">glRectsv function</span></span>

<span data-ttu-id="42654-105">La funzione **glRectsv** disegna un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="42654-105">The **glRectsv** function draws a rectangle.</span></span>

## <a name="syntax"></a><span data-ttu-id="42654-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="42654-106">Syntax</span></span>


```C++
void WINAPI glRectsv(
   const GLshort *v1,
   const GLshort *v2
);
```



## <a name="parameters"></a><span data-ttu-id="42654-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="42654-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42654-108">*v1*</span><span class="sxs-lookup"><span data-stu-id="42654-108">*v1*</span></span> 
</dt> <dd>

<span data-ttu-id="42654-109">Puntatore a un vertice di un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="42654-109">A pointer to one vertex of a rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="42654-110">*v2*</span><span class="sxs-lookup"><span data-stu-id="42654-110">*v2*</span></span> 
</dt> <dd>

<span data-ttu-id="42654-111">puntatore al vertice opposto del rettangolo.</span><span class="sxs-lookup"><span data-stu-id="42654-111">a pointer to the opposite vertex of the rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42654-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="42654-112">Return value</span></span>

<span data-ttu-id="42654-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="42654-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="42654-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="42654-114">Error codes</span></span>

<span data-ttu-id="42654-115">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="42654-115">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="42654-116">Nome</span><span class="sxs-lookup"><span data-stu-id="42654-116">Name</span></span>                                                                                                  | <span data-ttu-id="42654-117">Significato</span><span class="sxs-lookup"><span data-stu-id="42654-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="42654-118"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="42654-118"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="42654-119">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="42654-119">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="42654-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="42654-120">Remarks</span></span>

<span data-ttu-id="42654-121">La funzione **glRects** supporta una specifica efficiente di rettangoli come due punti d'angolo.</span><span class="sxs-lookup"><span data-stu-id="42654-121">The **glRects** function supports efficient specification of rectangles as two corner points.</span></span> <span data-ttu-id="42654-122">Ogni comando Rectangle accetta quattro argomenti, organizzati come due coppie consecutive di coordinate (*x*, *y*) o come due puntatori a matrici, ognuna contenente una coppia (*x,* *y*).</span><span class="sxs-lookup"><span data-stu-id="42654-122">Each rectangle command takes four arguments, organized either as two consecutive pairs of (*x*, *y*) coordinates, or as two pointers to arrays, each containing an (*x,* *y*) pair.</span></span> <span data-ttu-id="42654-123">Il rettangolo risultante è definito nel piano *z* = 0.</span><span class="sxs-lookup"><span data-stu-id="42654-123">The resulting rectangle is defined in the *z* = 0 plane.</span></span>

<span data-ttu-id="42654-124">La funzione **glRects**(*x1,* *Y1,* *X2,* *Y2*) è esattamente equivalente alla sequenza seguente:</span><span class="sxs-lookup"><span data-stu-id="42654-124">The **glRects**(*x1,* *y1,* *x2,* *y2*) function is exactly equivalent to the following sequence:</span></span>

<span data-ttu-id="42654-125">**glBegin**( \_ poligono GL);</span><span class="sxs-lookup"><span data-stu-id="42654-125">**glBegin**(GL\_POLYGON);</span></span>

<span data-ttu-id="42654-126">**glVertex2**( *x1,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="42654-126">**glVertex2**( *x1,* *y1* );</span></span>

<span data-ttu-id="42654-127">**glVertex2**( *X2,* *Y1* );</span><span class="sxs-lookup"><span data-stu-id="42654-127">**glVertex2**( *x2,* *y1* );</span></span>

<span data-ttu-id="42654-128">**glVertex2**( *X2,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="42654-128">**glVertex2**( *x2,* *y2* );</span></span>

<span data-ttu-id="42654-129">**glVertex2**( *x1,* *Y2* );</span><span class="sxs-lookup"><span data-stu-id="42654-129">**glVertex2**( *x1,* *y2* );</span></span>

<span data-ttu-id="42654-130">**glEnd**();</span><span class="sxs-lookup"><span data-stu-id="42654-130">**glEnd**( );</span></span>

<span data-ttu-id="42654-131">Si noti che se il secondo vertice è sopra e a destra del primo vertice, il rettangolo viene costruito con una bobina in senso antiorario.</span><span class="sxs-lookup"><span data-stu-id="42654-131">Notice that if the second vertex is above and to the right of the first vertex, the rectangle is constructed with a counterclockwise winding.</span></span>

## <a name="requirements"></a><span data-ttu-id="42654-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="42654-132">Requirements</span></span>



| <span data-ttu-id="42654-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="42654-133">Requirement</span></span> | <span data-ttu-id="42654-134">Valore</span><span class="sxs-lookup"><span data-stu-id="42654-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42654-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42654-135">Minimum supported client</span></span><br/> | <span data-ttu-id="42654-136">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="42654-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="42654-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="42654-137">Minimum supported server</span></span><br/> | <span data-ttu-id="42654-138">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="42654-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="42654-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="42654-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="42654-140"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="42654-140"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="42654-141">Libreria</span><span class="sxs-lookup"><span data-stu-id="42654-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="42654-142"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="42654-142"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="42654-143">DLL</span><span class="sxs-lookup"><span data-stu-id="42654-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42654-144"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42654-144"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42654-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="42654-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42654-146">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="42654-146">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="42654-147">**Remo**</span><span class="sxs-lookup"><span data-stu-id="42654-147">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="42654-148">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="42654-148">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





