---
title: funzione glFrustum (GL. h)
description: La funzione glFrustum moltiplica la matrice corrente in base a una matrice di prospettive.
ms.assetid: aa44c3fc-3bf6-4ef3-bb29-98e3056cdad3
keywords:
- funzione glFrustum OpenGL
topic_type:
- apiref
api_name:
- glFrustum
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce67879ca20819713e61a9392bf77be2f15211d5
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104563948"
---
# <a name="glfrustum-function"></a><span data-ttu-id="11e4c-104">glFrustum (funzione)</span><span class="sxs-lookup"><span data-stu-id="11e4c-104">glFrustum function</span></span>

<span data-ttu-id="11e4c-105">La funzione **glFrustum** moltiplica la matrice corrente in base a una matrice di prospettive.</span><span class="sxs-lookup"><span data-stu-id="11e4c-105">The **glFrustum** function multiplies the current matrix by a perspective matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="11e4c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="11e4c-106">Syntax</span></span>


```C++
void WINAPI glFrustum(
   GLdouble left,
   GLdouble right,
   GLdouble bottom,
   GLdouble top,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a><span data-ttu-id="11e4c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="11e4c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11e4c-108">*sinistra*</span><span class="sxs-lookup"><span data-stu-id="11e4c-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="11e4c-109">Coordinata per il piano di ritaglio verticale verso sinistra.</span><span class="sxs-lookup"><span data-stu-id="11e4c-109">The coordinate for the left-vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="11e4c-110">*Ok*</span><span class="sxs-lookup"><span data-stu-id="11e4c-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="11e4c-111">Coordinata per il piano di ritaglio verticale a destra.</span><span class="sxs-lookup"><span data-stu-id="11e4c-111">The coordinate for the right-vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="11e4c-112">*parte inferiore*</span><span class="sxs-lookup"><span data-stu-id="11e4c-112">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="11e4c-113">Coordinata per il piano di ritaglio orizzontale inferiore.</span><span class="sxs-lookup"><span data-stu-id="11e4c-113">The coordinate for the bottom-horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="11e4c-114">*top*</span><span class="sxs-lookup"><span data-stu-id="11e4c-114">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="11e4c-115">Coordinata per il piano di ritaglio orizzontale inferiore.</span><span class="sxs-lookup"><span data-stu-id="11e4c-115">The coordinate for the bottom-horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="11e4c-116">*zNear*</span><span class="sxs-lookup"><span data-stu-id="11e4c-116">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="11e4c-117">Distanze rispetto al piano di ritaglio quasi approfondito.</span><span class="sxs-lookup"><span data-stu-id="11e4c-117">The distances to the near-depth clipping plane.</span></span> <span data-ttu-id="11e4c-118">Deve essere un valore positivo.</span><span class="sxs-lookup"><span data-stu-id="11e4c-118">Must be positive.</span></span>

</dd> <dt>

<span data-ttu-id="11e4c-119">*zFar*</span><span class="sxs-lookup"><span data-stu-id="11e4c-119">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="11e4c-120">Distanze per i piani di ritaglio molto profondi.</span><span class="sxs-lookup"><span data-stu-id="11e4c-120">The distances to the far-depth clipping planes.</span></span> <span data-ttu-id="11e4c-121">Deve essere un valore positivo.</span><span class="sxs-lookup"><span data-stu-id="11e4c-121">Must be positive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11e4c-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="11e4c-122">Return value</span></span>

<span data-ttu-id="11e4c-123">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="11e4c-123">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="11e4c-124">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="11e4c-124">Error codes</span></span>

<span data-ttu-id="11e4c-125">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="11e4c-125">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="11e4c-126">Nome</span><span class="sxs-lookup"><span data-stu-id="11e4c-126">Name</span></span>                                                                                                  | <span data-ttu-id="11e4c-127">Significato</span><span class="sxs-lookup"><span data-stu-id="11e4c-127">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11e4c-128"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="11e4c-128"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="11e4c-129">*zNear* o *zFar* non è postitive.</span><span class="sxs-lookup"><span data-stu-id="11e4c-129">*zNear* or *zFar* was not postitive.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="11e4c-130"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="11e4c-130"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="11e4c-131">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="11e4c-131">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="11e4c-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="11e4c-132">Remarks</span></span>

<span data-ttu-id="11e4c-133">La funzione **glFrustum** descrive una matrice di prospettive che produce una proiezione prospettica.</span><span class="sxs-lookup"><span data-stu-id="11e4c-133">The **glFrustum** function describes a perspective matrix that produces a perspective projection.</span></span> <span data-ttu-id="11e4c-134">I parametri (*Left*, *Bottom*, *zNear*) e (*right*, *Top*, *zNear*) specificano i punti sul piano di ritaglio vicino di cui è stato eseguito il mapping rispettivamente agli angoli inferiore sinistro e superiore destro della finestra, supponendo che l'occhio si trovi in (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="11e4c-134">The (*left*, *bottom*, *zNear*) and (*right*, *top*, *zNear*) parameters specify the points on the near clipping plane that are mapped to the lower-left and upper-right corners of the window, respectively, assuming that the eye is located at (0,0,0).</span></span> <span data-ttu-id="11e4c-135">Il parametro *zFar* specifica il percorso del piano di ritaglio estremo.</span><span class="sxs-lookup"><span data-stu-id="11e4c-135">The *zFar* parameter specifies the location of the far clipping plane.</span></span> <span data-ttu-id="11e4c-136">Sia *zNear* che *zFar* devono essere positivi.</span><span class="sxs-lookup"><span data-stu-id="11e4c-136">Both *zNear* and *zFar* must be positive.</span></span> <span data-ttu-id="11e4c-137">La matrice corrispondente è illustrata nell'immagine seguente.</span><span class="sxs-lookup"><span data-stu-id="11e4c-137">The corresponding matrix is shown in the following image.</span></span>

![Diagramma che mostra la matrice della prospettiva che produce una proiezione prospettica.](images/frust01.png)![Equazioni che mostrano la funzione glFrustum che descrive una matrice di prospettive.](images/frust02.png)

<span data-ttu-id="11e4c-140">La funzione **glFrustum** moltiplica la matrice corrente in base a questa matrice, con il risultato che sostituisce la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="11e4c-140">The **glFrustum** function multiplies the current matrix by this matrix, with the result replacing the current matrix.</span></span> <span data-ttu-id="11e4c-141">Ovvero, se M è la matrice corrente e F è la matrice della prospettiva tronco, **glFrustum** sostituisce M con m F.</span><span class="sxs-lookup"><span data-stu-id="11e4c-141">That is, if M is the current matrix and F is the frustum perspective matrix, then **glFrustum** replaces M with M   F.</span></span>

<span data-ttu-id="11e4c-142">Usare [**glPushMatrix**](glpushmatrix.md) e [**glPopMatrix**](glpopmatrix.md) per salvare e ripristinare lo stack della matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="11e4c-142">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore the current matrix stack.</span></span>

<span data-ttu-id="11e4c-143">La precisione del buffer di profondità è interessata dai valori specificati per *zNear* e *zFar*.</span><span class="sxs-lookup"><span data-stu-id="11e4c-143">Depth-buffer precision is affected by the values specified for *zNear* and *zFar*.</span></span> <span data-ttu-id="11e4c-144">Maggiore è il rapporto tra *zFar* e *zNear* , minore è il buffer di profondità che si distingue tra le superfici che si avvicinano tra loro.</span><span class="sxs-lookup"><span data-stu-id="11e4c-144">The greater the ratio of *zFar* to *zNear* is, the less effective the depth buffer will be at distinguishing between surfaces that are near each other.</span></span> <span data-ttu-id="11e4c-145">Se</span><span class="sxs-lookup"><span data-stu-id="11e4c-145">If</span></span>

![Equazione che mostra il rapporto tra distanza e prossimità.](images/frust03.png)

<span data-ttu-id="11e4c-147">approssimativamente i bit di *log* 2 (*r*) della precisione del buffer di profondità vanno persi.</span><span class="sxs-lookup"><span data-stu-id="11e4c-147">roughly *log* 2 (*r*) bits of depth buffer precision are lost.</span></span> <span data-ttu-id="11e4c-148">Poiché *r* si avvicina a infinito perché *zNear* si avvicina a zero, è consigliabile non impostare mai *zNear* su zero.</span><span class="sxs-lookup"><span data-stu-id="11e4c-148">Because *r* approaches infinity as *zNear* approaches zero, you should never set *zNear* to zero.</span></span>

<span data-ttu-id="11e4c-149">Le funzioni seguenti recuperano informazioni su **glFrustum**:</span><span class="sxs-lookup"><span data-stu-id="11e4c-149">The following functions retrieve information about **glFrustum**:</span></span>

<span data-ttu-id="11e4c-150">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ modalità matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="11e4c-150">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="11e4c-151">**glGet** con argomento GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="11e4c-151">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="11e4c-152">**glGet** con matrice di \_ proiezione GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="11e4c-152">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="11e4c-153">**glGet** con argomento della \_ matrice di trama GL \_</span><span class="sxs-lookup"><span data-stu-id="11e4c-153">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="11e4c-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="11e4c-154">Requirements</span></span>



| <span data-ttu-id="11e4c-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="11e4c-155">Requirement</span></span> | <span data-ttu-id="11e4c-156">Valore</span><span class="sxs-lookup"><span data-stu-id="11e4c-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11e4c-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11e4c-157">Minimum supported client</span></span><br/> | <span data-ttu-id="11e4c-158">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="11e4c-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="11e4c-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="11e4c-159">Minimum supported server</span></span><br/> | <span data-ttu-id="11e4c-160">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="11e4c-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="11e4c-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="11e4c-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="11e4c-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="11e4c-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="11e4c-163">Libreria</span><span class="sxs-lookup"><span data-stu-id="11e4c-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="11e4c-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11e4c-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="11e4c-165">DLL</span><span class="sxs-lookup"><span data-stu-id="11e4c-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11e4c-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11e4c-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11e4c-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="11e4c-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11e4c-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="11e4c-168">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="11e4c-169">**Remo**</span><span class="sxs-lookup"><span data-stu-id="11e4c-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="11e4c-170">**glGet**</span><span class="sxs-lookup"><span data-stu-id="11e4c-170">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="11e4c-171">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="11e4c-171">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="11e4c-172">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="11e4c-172">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="11e4c-173">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="11e4c-173">**glOrtho**</span></span>](glortho.md)
</dt> <dt>

[<span data-ttu-id="11e4c-174">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="11e4c-174">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="11e4c-175">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="11e4c-175">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="11e4c-176">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="11e4c-176">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





