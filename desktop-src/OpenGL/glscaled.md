---
title: funzione glScaled (GL. h)
description: Le funzioni glScaled e glScalef moltiplicano la matrice corrente in base a una matrice di scala generale. | funzione glScaled (GL. h)
ms.assetid: 3846289f-5c7b-4bb6-95a8-90a58dd8b9d9
keywords:
- funzione glScaled OpenGL
topic_type:
- apiref
api_name:
- glScaled
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2655924f5716e142832882441066d4772d0e63
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104569100"
---
# <a name="glscaled-function"></a><span data-ttu-id="ce04a-105">glScaled (funzione)</span><span class="sxs-lookup"><span data-stu-id="ce04a-105">glScaled function</span></span>

<span data-ttu-id="ce04a-106">Le funzioni **glScaled** e [**glScalef**](glscalef.md) moltiplicano la matrice corrente in base a una matrice di scala generale.</span><span class="sxs-lookup"><span data-stu-id="ce04a-106">The **glScaled** and [**glScalef**](glscalef.md) functions multiply the current matrix by a general scaling matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce04a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ce04a-107">Syntax</span></span>


```C++
void WINAPI glScaled(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a><span data-ttu-id="ce04a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ce04a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce04a-109">*x*</span><span class="sxs-lookup"><span data-stu-id="ce04a-109">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="ce04a-110">Fattori di scala lungo l'asse *x* .</span><span class="sxs-lookup"><span data-stu-id="ce04a-110">Scale factors along the *x* axis.</span></span>

</dd> <dt>

<span data-ttu-id="ce04a-111">*y*</span><span class="sxs-lookup"><span data-stu-id="ce04a-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="ce04a-112">Fattori di scala lungo l'asse *y* .</span><span class="sxs-lookup"><span data-stu-id="ce04a-112">Scale factors along the *y* axis.</span></span>

</dd> <dt>

<span data-ttu-id="ce04a-113">*z*</span><span class="sxs-lookup"><span data-stu-id="ce04a-113">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="ce04a-114">Fattori di scala lungo l'asse *z* .</span><span class="sxs-lookup"><span data-stu-id="ce04a-114">Scale factors along the *z* axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce04a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ce04a-115">Return value</span></span>

<span data-ttu-id="ce04a-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ce04a-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ce04a-117">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ce04a-117">Error codes</span></span>

<span data-ttu-id="ce04a-118">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="ce04a-118">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ce04a-119">Nome</span><span class="sxs-lookup"><span data-stu-id="ce04a-119">Name</span></span>                                                                                                  | <span data-ttu-id="ce04a-120">Significato</span><span class="sxs-lookup"><span data-stu-id="ce04a-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ce04a-121"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ce04a-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ce04a-122">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ce04a-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ce04a-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="ce04a-123">Remarks</span></span>

<span data-ttu-id="ce04a-124">La funzione **glScaled** produce una scala generale lungo gli assi *x*, *y* e *z* .</span><span class="sxs-lookup"><span data-stu-id="ce04a-124">The **glScaled** function produces a general scaling along the *x*, *y*, and *z* axes.</span></span> <span data-ttu-id="ce04a-125">I tre argomenti indicano i fattori di scala desiderati lungo ognuno dei tre assi.</span><span class="sxs-lookup"><span data-stu-id="ce04a-125">The three arguments indicate the desired scale factors along each of the three axes.</span></span> <span data-ttu-id="ce04a-126">La matrice risultante è</span><span class="sxs-lookup"><span data-stu-id="ce04a-126">The resulting matrix is</span></span>

![Diagramma che mostra la matrice di fattori di scala lungo gli assi x, y e z.](images/scale01.png)

<span data-ttu-id="ce04a-128">La matrice corrente (vedere [**glMatrixMode**](glmatrixmode.md)) viene moltiplicata per questa matrice di scala, con il prodotto che sostituisce la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="ce04a-128">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this scale matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="ce04a-129">Ovvero, se M è la matrice corrente e S è la matrice di scala, M viene sostituito con M S.</span><span class="sxs-lookup"><span data-stu-id="ce04a-129">That is, if M is the current matrix and S is the scale matrix, then M is replaced with M   S.</span></span>

<span data-ttu-id="ce04a-130">Se la modalità matrice è una \_ proiezione GL MODELVIEW o GL \_ , vengono ridimensionati tutti gli oggetti disegnati dopo **glScaled** .</span><span class="sxs-lookup"><span data-stu-id="ce04a-130">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glScaled** is called are scaled.</span></span> <span data-ttu-id="ce04a-131">Usare [**glPushMatrix**](glpushmatrix.md) e [**glPopMatrix**](glpopmatrix.md) per salvare e ripristinare il sistema di coordinate non ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="ce04a-131">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore the unscaled coordinate system.</span></span>

<span data-ttu-id="ce04a-132">Se si applicano fattori di scala diversi da 1,0 alla matrice Modelview e l'illuminazione è abilitata, è probabile che anche la normalizzazione automatica delle normali sia abilitata ([**glEnable**](glenable.md) e [**GLDISABLE**](gldisable.md) con argument GL \_ Normalize).</span><span class="sxs-lookup"><span data-stu-id="ce04a-132">If scale factors other than 1.0 are applied to the modelview matrix and lighting is enabled, automatic normalization of normals should probably also be enabled ([**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with argument GL\_NORMALIZE).</span></span>

<span data-ttu-id="ce04a-133">Le funzioni seguenti consentono di recuperare informazioni correlate a **glScaled**:</span><span class="sxs-lookup"><span data-stu-id="ce04a-133">The following functions retrieve information related to **glScaled**:</span></span>

<span data-ttu-id="ce04a-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ modalità matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="ce04a-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="ce04a-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="ce04a-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="ce04a-136">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con matrice di \_ proiezione GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="ce04a-136">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="ce04a-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ matrice di trama GL \_</span><span class="sxs-lookup"><span data-stu-id="ce04a-137">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="ce04a-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ce04a-138">Requirements</span></span>



| <span data-ttu-id="ce04a-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce04a-139">Requirement</span></span> | <span data-ttu-id="ce04a-140">Valore</span><span class="sxs-lookup"><span data-stu-id="ce04a-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce04a-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce04a-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ce04a-142">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ce04a-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ce04a-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ce04a-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ce04a-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ce04a-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ce04a-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ce04a-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce04a-146"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce04a-146"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ce04a-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="ce04a-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="ce04a-148"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ce04a-148"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ce04a-149">DLL</span><span class="sxs-lookup"><span data-stu-id="ce04a-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce04a-150"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce04a-150"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce04a-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ce04a-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce04a-152">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ce04a-152">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ce04a-153">**Remo**</span><span class="sxs-lookup"><span data-stu-id="ce04a-153">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ce04a-154">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="ce04a-154">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="ce04a-155">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="ce04a-155">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="ce04a-156">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="ce04a-156">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="ce04a-157">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="ce04a-157">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="ce04a-158">**glRotated**</span><span class="sxs-lookup"><span data-stu-id="ce04a-158">**glRotated**</span></span>](glrotated.md)
</dt> <dt>

[<span data-ttu-id="ce04a-159">**glRotatef**</span><span class="sxs-lookup"><span data-stu-id="ce04a-159">**glRotatef**</span></span>](glrotatef.md)
</dt> <dt>

[<span data-ttu-id="ce04a-160">**glTranslate**</span><span class="sxs-lookup"><span data-stu-id="ce04a-160">**glTranslate**</span></span>](gltranslate.md)
</dt> </dl>

 

 





