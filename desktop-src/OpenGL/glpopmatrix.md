---
title: funzione glPopMatrix (GL. h)
description: Le funzioni glPushMatrix e glPopMatrix effettuano il push e lo schiocco dello stack della matrice corrente. | funzione glPopMatrix (GL. h)
ms.assetid: 7b4fc26e-36c8-4252-aba7-2e8ec6b34f91
keywords:
- funzione glPopMatrix OpenGL
topic_type:
- apiref
api_name:
- glPopMatrix
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41424a8af3ca6599edc7a66f9e498632640022c5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321404"
---
# <a name="glpopmatrix-function"></a><span data-ttu-id="2dae0-105">glPopMatrix (funzione)</span><span class="sxs-lookup"><span data-stu-id="2dae0-105">glPopMatrix function</span></span>

<span data-ttu-id="2dae0-106">Le funzioni [**glPushMatrix**](glpushmatrix.md) e **glPopMatrix** effettuano il push e lo schiocco dello stack della matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="2dae0-106">The [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix** functions push and pop the current matrix stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dae0-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2dae0-107">Syntax</span></span>


```C++
void WINAPI glPopMatrix(void);
```



## <a name="parameters"></a><span data-ttu-id="2dae0-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="2dae0-108">Parameters</span></span>

<span data-ttu-id="2dae0-109">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="2dae0-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2dae0-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2dae0-110">Return value</span></span>

<span data-ttu-id="2dae0-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="2dae0-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2dae0-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="2dae0-112">Error codes</span></span>

<span data-ttu-id="2dae0-113">Non è possibile eseguire il push di uno stack di matrici completo oppure per estrarre uno stack della matrice che contiene una sola matrice.</span><span class="sxs-lookup"><span data-stu-id="2dae0-113">It is an error to push a full matrix stack, or to pop a matrix stack that contains only a single matrix.</span></span> <span data-ttu-id="2dae0-114">In entrambi i casi, viene impostato il flag di errore e non viene apportata alcuna modifica allo stato OpenGL.</span><span class="sxs-lookup"><span data-stu-id="2dae0-114">In either case, the error flag is set and no other change is made to the OpenGL state.</span></span>

<span data-ttu-id="2dae0-115">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="2dae0-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="2dae0-116">Nome</span><span class="sxs-lookup"><span data-stu-id="2dae0-116">Name</span></span>                                                                                                  | <span data-ttu-id="2dae0-117">Significato</span><span class="sxs-lookup"><span data-stu-id="2dae0-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2dae0-118"><dt>**\_underflow dello stack GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2dae0-118"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="2dae0-119">La funzione è stata chiamata mentre lo stack della matrice corrente contiene una sola matrice.</span><span class="sxs-lookup"><span data-stu-id="2dae0-119">The function was called while the current matrix stack contained only a single matrix.</span></span><br/>                                     |
| <dl> <span data-ttu-id="2dae0-120"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2dae0-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="2dae0-121">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="2dae0-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2dae0-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="2dae0-122">Remarks</span></span>

<span data-ttu-id="2dae0-123">È disponibile una pila di matrici per ogni modalità della matrice.</span><span class="sxs-lookup"><span data-stu-id="2dae0-123">There is a stack of matrices for each of the matrix modes.</span></span> <span data-ttu-id="2dae0-124">In \_ modalità GL MODELVIEW, la profondità dello stack è almeno 32.</span><span class="sxs-lookup"><span data-stu-id="2dae0-124">In GL\_MODELVIEW mode, the stack depth is at least 32.</span></span> <span data-ttu-id="2dae0-125">Nelle altre due modalità, proiezione GL \_ e trama GL \_ , la profondità è almeno 2.</span><span class="sxs-lookup"><span data-stu-id="2dae0-125">In the other two modes, GL\_PROJECTION and GL\_TEXTURE, the depth is at least 2.</span></span> <span data-ttu-id="2dae0-126">La matrice corrente in qualsiasi modalità è la matrice nella parte superiore dello stack per tale modalità.</span><span class="sxs-lookup"><span data-stu-id="2dae0-126">The current matrix in any mode is the matrix on the top of the stack for that mode.</span></span>

<span data-ttu-id="2dae0-127">La funzione [**glPushMatrix**](glpushmatrix.md) esegue il push dello stack della matrice corrente verso il basso di uno, duplicando la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="2dae0-127">The [**glPushMatrix**](glpushmatrix.md) function pushes the current matrix stack down by one, duplicating the current matrix.</span></span> <span data-ttu-id="2dae0-128">Ovvero, dopo una chiamata a **glPushMatrix** , la matrice nella parte superiore dello stack è identica a quella sotto.</span><span class="sxs-lookup"><span data-stu-id="2dae0-128">That is, after a **glPushMatrix** call, the matrix on the top of the stack is identical to the one below it.</span></span> <span data-ttu-id="2dae0-129">La funzione **glPopMatrix** estrae lo stack della matrice corrente, sostituendo la matrice corrente con quella sotto di essa nello stack.</span><span class="sxs-lookup"><span data-stu-id="2dae0-129">The **glPopMatrix** function pops the current matrix stack, replacing the current matrix with the one below it on the stack.</span></span> <span data-ttu-id="2dae0-130">Inizialmente, ogni stack contiene una matrice, una matrice di identità.</span><span class="sxs-lookup"><span data-stu-id="2dae0-130">Initially, each of the stacks contains one matrix, an identity matrix.</span></span>

<span data-ttu-id="2dae0-131">Le funzioni seguenti recuperano informazioni relative a [**glPushMatrix**](glpushmatrix.md) e **glPopMatrix**:</span><span class="sxs-lookup"><span data-stu-id="2dae0-131">The following functions retrieve information related to [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix**:</span></span>

<span data-ttu-id="2dae0-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ modalità matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="2dae0-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="2dae0-133">**glGet** con argomento GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="2dae0-133">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="2dae0-134">**glGet** con matrice di \_ proiezione GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="2dae0-134">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="2dae0-135">**glGet** con argomento della \_ matrice di trama GL \_</span><span class="sxs-lookup"><span data-stu-id="2dae0-135">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

<span data-ttu-id="2dae0-136">**glGet** con argomento \_ MODELVIEW \_ Stack \_ Depth</span><span class="sxs-lookup"><span data-stu-id="2dae0-136">**glGet** with argument GL\_MODELVIEW\_STACK\_DEPTH</span></span>

<span data-ttu-id="2dae0-137">**glGet** con \_ \_ profondità dello stack di proiezione GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="2dae0-137">**glGet** with argument GL\_PROJECTION\_STACK\_DEPTH</span></span>

<span data-ttu-id="2dae0-138">**glGet** con argomento \_ \_ profondità dello stack di trama GL \_</span><span class="sxs-lookup"><span data-stu-id="2dae0-138">**glGet** with argument GL\_TEXTURE\_STACK\_DEPTH</span></span>

<span data-ttu-id="2dae0-139">**glGet** con argomento con \_ \_ profondità massima \_ dello stack MODELVIEW \_</span><span class="sxs-lookup"><span data-stu-id="2dae0-139">**glGet** with argument GL\_MAX\_MODELVIEW\_STACK\_DEPTH</span></span>

<span data-ttu-id="2dae0-140">**glGet** con argomento \_ \_ \_ profondità dello stack di proiezione max \_</span><span class="sxs-lookup"><span data-stu-id="2dae0-140">**glGet** with argument GL\_MAX\_PROJECTION\_STACK\_DEPTH</span></span>

<span data-ttu-id="2dae0-141">**glGet** con argomento di \_ \_ profondità max trama \_ Stack \_</span><span class="sxs-lookup"><span data-stu-id="2dae0-141">**glGet** with argument GL\_MAX\_TEXTURE\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="2dae0-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2dae0-142">Requirements</span></span>



| <span data-ttu-id="2dae0-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dae0-143">Requirement</span></span> | <span data-ttu-id="2dae0-144">Valore</span><span class="sxs-lookup"><span data-stu-id="2dae0-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2dae0-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2dae0-145">Minimum supported client</span></span><br/> | <span data-ttu-id="2dae0-146">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2dae0-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2dae0-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2dae0-147">Minimum supported server</span></span><br/> | <span data-ttu-id="2dae0-148">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2dae0-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2dae0-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2dae0-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dae0-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dae0-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2dae0-151">Libreria</span><span class="sxs-lookup"><span data-stu-id="2dae0-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="2dae0-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2dae0-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2dae0-153">DLL</span><span class="sxs-lookup"><span data-stu-id="2dae0-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2dae0-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2dae0-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dae0-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2dae0-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dae0-156">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="2dae0-156">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="2dae0-157">**Remo**</span><span class="sxs-lookup"><span data-stu-id="2dae0-157">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="2dae0-158">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="2dae0-158">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="2dae0-159">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="2dae0-159">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="2dae0-160">**glLoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="2dae0-160">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="2dae0-161">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="2dae0-161">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="2dae0-162">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="2dae0-162">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="2dae0-163">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="2dae0-163">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="2dae0-164">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="2dae0-164">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="2dae0-165">**glRotate**</span><span class="sxs-lookup"><span data-stu-id="2dae0-165">**glRotate**</span></span>](glrotate.md)
</dt> <dt>

[<span data-ttu-id="2dae0-166">**glScale**</span><span class="sxs-lookup"><span data-stu-id="2dae0-166">**glScale**</span></span>](glscale.md)
</dt> <dt>

[<span data-ttu-id="2dae0-167">**glTranslate**</span><span class="sxs-lookup"><span data-stu-id="2dae0-167">**glTranslate**</span></span>](gltranslate.md)
</dt> <dt>

[<span data-ttu-id="2dae0-168">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="2dae0-168">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





