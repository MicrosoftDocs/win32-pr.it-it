---
title: funzione glOrtho (GL. h)
description: La funzione glOrtho moltiplica la matrice corrente in base a una matrice ortogonale.
ms.assetid: 5c70819f-e9b6-49e2-add5-9f6e6aba26ee
keywords:
- funzione glOrtho OpenGL
topic_type:
- apiref
api_name:
- glOrtho
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46abbb0edd2dfc7fc51aaf7fa6519dc5367b109c
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104550712"
---
# <a name="glortho-function"></a><span data-ttu-id="49fcd-104">glOrtho (funzione)</span><span class="sxs-lookup"><span data-stu-id="49fcd-104">glOrtho function</span></span>

<span data-ttu-id="49fcd-105">La funzione **glOrtho** moltiplica la matrice corrente in base a una matrice ortogonale.</span><span class="sxs-lookup"><span data-stu-id="49fcd-105">The **glOrtho** function multiplies the current matrix by an orthographic matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="49fcd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="49fcd-106">Syntax</span></span>


```C++
void WINAPI glOrtho(
   GLdouble left,
   GLdouble right,
   GLdouble bottom,
   GLdouble top,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a><span data-ttu-id="49fcd-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="49fcd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49fcd-108">*sinistra*</span><span class="sxs-lookup"><span data-stu-id="49fcd-108">*left*</span></span> 
</dt> <dd>

<span data-ttu-id="49fcd-109">Coordinate per il piano di ritaglio verticale sinistro.</span><span class="sxs-lookup"><span data-stu-id="49fcd-109">The coordinates for the left vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="49fcd-110">*Ok*</span><span class="sxs-lookup"><span data-stu-id="49fcd-110">*right*</span></span> 
</dt> <dd>

<span data-ttu-id="49fcd-111">Coordinate per il piano di ritaglio verticale giustaper.</span><span class="sxs-lookup"><span data-stu-id="49fcd-111">The coordinates for theright vertical clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="49fcd-112">*parte inferiore*</span><span class="sxs-lookup"><span data-stu-id="49fcd-112">*bottom*</span></span> 
</dt> <dd>

<span data-ttu-id="49fcd-113">Coordinate per il piano di ritaglio orizzontale inferiore.</span><span class="sxs-lookup"><span data-stu-id="49fcd-113">The coordinates for the bottom horizontal clipping plane.</span></span>

</dd> <dt>

<span data-ttu-id="49fcd-114">*top*</span><span class="sxs-lookup"><span data-stu-id="49fcd-114">*top*</span></span> 
</dt> <dd>

<span data-ttu-id="49fcd-115">Coordinate per i primi piani di ritaglio orizzontali.</span><span class="sxs-lookup"><span data-stu-id="49fcd-115">The coordinates for the top horizontal clipping plans.</span></span>

</dd> <dt>

<span data-ttu-id="49fcd-116">*zNear*</span><span class="sxs-lookup"><span data-stu-id="49fcd-116">*zNear*</span></span> 
</dt> <dd>

<span data-ttu-id="49fcd-117">Distanze rispetto al piano di ritaglio di profondità più vicino.</span><span class="sxs-lookup"><span data-stu-id="49fcd-117">The distances to the nearer depth clipping plane.</span></span> <span data-ttu-id="49fcd-118">Questa distanza è negativa se il piano deve trovarsi dietro il visualizzatore.</span><span class="sxs-lookup"><span data-stu-id="49fcd-118">This distance is negative if the plane is to be behind the viewer.</span></span>

</dd> <dt>

<span data-ttu-id="49fcd-119">*zFar*</span><span class="sxs-lookup"><span data-stu-id="49fcd-119">*zFar*</span></span> 
</dt> <dd>

<span data-ttu-id="49fcd-120">Distanze rispetto al piano di ritaglio più profondo.</span><span class="sxs-lookup"><span data-stu-id="49fcd-120">The distances to the farther depth clipping plane.</span></span> <span data-ttu-id="49fcd-121">Questa distanza è negativa se il piano deve trovarsi dietro il visualizzatore.</span><span class="sxs-lookup"><span data-stu-id="49fcd-121">This distance is negative if the plane is to be behind the viewer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49fcd-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49fcd-122">Return value</span></span>

<span data-ttu-id="49fcd-123">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="49fcd-123">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="49fcd-124">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="49fcd-124">Error codes</span></span>

<span data-ttu-id="49fcd-125">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="49fcd-125">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="49fcd-126">Nome</span><span class="sxs-lookup"><span data-stu-id="49fcd-126">Name</span></span>                                                                                                  | <span data-ttu-id="49fcd-127">Significato</span><span class="sxs-lookup"><span data-stu-id="49fcd-127">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="49fcd-128"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="49fcd-128"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="49fcd-129">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="49fcd-129">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="49fcd-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="49fcd-130">Remarks</span></span>

<span data-ttu-id="49fcd-131">La funzione **glOrtho** descrive una matrice di prospettive che produce una proiezione parallela.</span><span class="sxs-lookup"><span data-stu-id="49fcd-131">The **glOrtho** function describes a perspective matrix that produces a parallel projection.</span></span> <span data-ttu-id="49fcd-132">I parametri (*Left*, *Bottom*, *near*) e (*right*, *Top*, *near*) specificano i punti sul piano di ritaglio vicino di cui è stato eseguito il mapping rispettivamente agli angoli inferiore sinistro e superiore destro della finestra, supponendo che l'occhio si trovi in (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="49fcd-132">The (*left*, *bottom*, *near*) and (*right*, *top*, *near*) parameters specify the points on the near clipping plane that are mapped to the lower-left and upper-right corners of the window, respectively, assuming that the eye is located at (0, 0, 0).</span></span> <span data-ttu-id="49fcd-133">Il parametro *lontano* specifica il percorso del piano di ritaglio estremo.</span><span class="sxs-lookup"><span data-stu-id="49fcd-133">The *far* parameter specifies the location of the far clipping plane.</span></span> <span data-ttu-id="49fcd-134">Sia *zNear* che *zFar* possono essere positivi o negativi.</span><span class="sxs-lookup"><span data-stu-id="49fcd-134">Both *zNear* and *zFar* can be either positive or negative.</span></span> <span data-ttu-id="49fcd-135">La matrice corrispondente è illustrata nell'immagine seguente.</span><span class="sxs-lookup"><span data-stu-id="49fcd-135">The corresponding matrix is shown in the following image.</span></span>

![Diagramma che mostra la matrice della prospettiva descritta dalla funzione glOrtho.](images/ortho1.png)

<span data-ttu-id="49fcd-137">dove</span><span class="sxs-lookup"><span data-stu-id="49fcd-137">where</span></span>

![Equazioni che descrivono la matrice della prospettiva.](images/ortho2.png)

<span data-ttu-id="49fcd-139">La matrice corrente viene moltiplicata per questa matrice con il risultato che sostituisce la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="49fcd-139">The current matrix is multiplied by this matrix with the result replacing the current matrix.</span></span> <span data-ttu-id="49fcd-140">Ovvero, se M è la matrice corrente e O è la matrice Ortho, M viene sostituito con M O.</span><span class="sxs-lookup"><span data-stu-id="49fcd-140">That is, if M is the current matrix and O is the ortho matrix, then M is replaced with M   O.</span></span>

<span data-ttu-id="49fcd-141">Usare [**glPushMatrix**](glpushmatrix.md) e **glPopMatrix** per salvare e ripristinare lo stack della matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="49fcd-141">Use [**glPushMatrix**](glpushmatrix.md) and **glPopMatrix** to save and restore the current matrix stack.</span></span> <span data-ttu-id="49fcd-142">Usare [**glMatrixMode**](glmatrixmode.md) per impostare la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="49fcd-142">Use [**glMatrixMode**](glmatrixmode.md) to set the current matrix.</span></span>

<span data-ttu-id="49fcd-143">Le funzioni seguenti consentono di recuperare informazioni correlate a **glOrtho**:</span><span class="sxs-lookup"><span data-stu-id="49fcd-143">The following functions retrieve information related to **glOrtho**:</span></span>

<span data-ttu-id="49fcd-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ modalità matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="49fcd-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="49fcd-145">**glGet** con argomento GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="49fcd-145">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="49fcd-146">**glGet** con matrice di \_ proiezione GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="49fcd-146">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="49fcd-147">**glGet** con argomento della \_ matrice di trama GL \_</span><span class="sxs-lookup"><span data-stu-id="49fcd-147">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="49fcd-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="49fcd-148">Requirements</span></span>



| <span data-ttu-id="49fcd-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="49fcd-149">Requirement</span></span> | <span data-ttu-id="49fcd-150">Valore</span><span class="sxs-lookup"><span data-stu-id="49fcd-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49fcd-151">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49fcd-151">Minimum supported client</span></span><br/> | <span data-ttu-id="49fcd-152">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="49fcd-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="49fcd-153">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="49fcd-153">Minimum supported server</span></span><br/> | <span data-ttu-id="49fcd-154">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="49fcd-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="49fcd-155">Intestazione</span><span class="sxs-lookup"><span data-stu-id="49fcd-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="49fcd-156"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="49fcd-156"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="49fcd-157">Libreria</span><span class="sxs-lookup"><span data-stu-id="49fcd-157">Library</span></span><br/>                  | <dl> <span data-ttu-id="49fcd-158"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49fcd-158"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="49fcd-159">DLL</span><span class="sxs-lookup"><span data-stu-id="49fcd-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49fcd-160"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49fcd-160"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49fcd-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49fcd-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49fcd-162">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="49fcd-162">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="49fcd-163">**Remo**</span><span class="sxs-lookup"><span data-stu-id="49fcd-163">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="49fcd-164">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="49fcd-164">**glFrustum**</span></span>](glfrustum.md)
</dt> <dt>

[<span data-ttu-id="49fcd-165">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="49fcd-165">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="49fcd-166">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="49fcd-166">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="49fcd-167">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="49fcd-167">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="49fcd-168">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="49fcd-168">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





