---
title: funzione glRotatef (GL. h)
description: La funzione glRotatef moltiplica la matrice corrente in base a una matrice di rotazione.
ms.assetid: 8216a125-de8c-44e5-afb3-3d4e5ffc600d
keywords:
- funzione glRotatef OpenGL
topic_type:
- apiref
api_name:
- glRotatef
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 953b8ffc5f89e5a4cf9901e4cb5fb5afb4c8dfdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479330"
---
# <a name="glrotatef-function"></a><span data-ttu-id="167d9-104">glRotatef (funzione)</span><span class="sxs-lookup"><span data-stu-id="167d9-104">glRotatef function</span></span>

<span data-ttu-id="167d9-105">La funzione **glRotatef** moltiplica la matrice corrente in base a una matrice di rotazione.</span><span class="sxs-lookup"><span data-stu-id="167d9-105">The **glRotatef** function multiplies the current matrix by a rotation matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="167d9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="167d9-106">Syntax</span></span>


```C++
void WINAPI glRotatef(
   GLfloat angle,
   GLfloat x,
   GLfloat y,
   GLfloat z
);
```



## <a name="parameters"></a><span data-ttu-id="167d9-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="167d9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="167d9-108">*angolo*</span><span class="sxs-lookup"><span data-stu-id="167d9-108">*angle*</span></span> 
</dt> <dd>

<span data-ttu-id="167d9-109">Angolo di rotazione, in gradi.</span><span class="sxs-lookup"><span data-stu-id="167d9-109">The angle of rotation, in degrees.</span></span>

</dd> <dt>

<span data-ttu-id="167d9-110">*x*</span><span class="sxs-lookup"><span data-stu-id="167d9-110">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="167d9-111">Coordinata *x* di un vettore.</span><span class="sxs-lookup"><span data-stu-id="167d9-111">The *x* coordinate of a vector.</span></span>

</dd> <dt>

<span data-ttu-id="167d9-112">*y*</span><span class="sxs-lookup"><span data-stu-id="167d9-112">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="167d9-113">Coordinata *y* di un vettore.</span><span class="sxs-lookup"><span data-stu-id="167d9-113">The *y* coordinate of a vector.</span></span>

</dd> <dt>

<span data-ttu-id="167d9-114">*z*</span><span class="sxs-lookup"><span data-stu-id="167d9-114">*z*</span></span> 
</dt> <dd>

<span data-ttu-id="167d9-115">Coordinata *z* di un vettore.</span><span class="sxs-lookup"><span data-stu-id="167d9-115">The *z* coordinate of a vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="167d9-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="167d9-116">Return value</span></span>

<span data-ttu-id="167d9-117">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="167d9-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="167d9-118">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="167d9-118">Error codes</span></span>

<span data-ttu-id="167d9-119">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="167d9-119">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="167d9-120">Nome</span><span class="sxs-lookup"><span data-stu-id="167d9-120">Name</span></span>                                                                                                  | <span data-ttu-id="167d9-121">Significato</span><span class="sxs-lookup"><span data-stu-id="167d9-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="167d9-122"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="167d9-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="167d9-123">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="167d9-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="167d9-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="167d9-124">Remarks</span></span>

<span data-ttu-id="167d9-125">La funzione **glRotatef** calcola una matrice che esegue una rotazione in senso antiorario dei gradi *angolari* sul vettore dall'origine al punto (*x*, *y*, *z*).</span><span class="sxs-lookup"><span data-stu-id="167d9-125">The **glRotatef** function computes a matrix that performs a counterclockwise rotation of *angle* degrees about the vector from the origin through the point (*x*, *y*, *z*).</span></span>

<span data-ttu-id="167d9-126">La matrice corrente (vedere [**glMatrixMode**](glmatrixmode.md)) viene moltiplicata per la matrice di rotazione, con il prodotto che sostituisce la matrice corrente.</span><span class="sxs-lookup"><span data-stu-id="167d9-126">The current matrix (see [**glMatrixMode**](glmatrixmode.md)) is multiplied by this rotation matrix, with the product replacing the current matrix.</span></span> <span data-ttu-id="167d9-127">Ovvero, se M è la matrice corrente e R è la matrice di traslazione, M viene sostituito con M R.</span><span class="sxs-lookup"><span data-stu-id="167d9-127">That is, if M is the current matrix and R is the translation matrix, then M is replaced with M   R.</span></span>

<span data-ttu-id="167d9-128">Se la modalità matrice è la \_ proiezione GL MODELVIEW o GL \_ , vengono ruotati tutti gli oggetti disegnati dopo **glRotatef** .</span><span class="sxs-lookup"><span data-stu-id="167d9-128">If the matrix mode is either GL\_MODELVIEW or GL\_PROJECTION, all objects drawn after **glRotatef** is called are rotated.</span></span> <span data-ttu-id="167d9-129">Usare [**glPushMatrix**](glpushmatrix.md) e [**glPopMatrix**](glpopmatrix.md) per salvare e ripristinare il sistema di coordinate non ruotato.</span><span class="sxs-lookup"><span data-stu-id="167d9-129">Use [**glPushMatrix**](glpushmatrix.md) and [**glPopMatrix**](glpopmatrix.md) to save and restore the unrotated coordinate system.</span></span>

<span data-ttu-id="167d9-130">Le funzioni seguenti consentono di recuperare informazioni correlate a **glRotatef**:</span><span class="sxs-lookup"><span data-stu-id="167d9-130">The following functions retrieve information related to **glRotatef**:</span></span>

<span data-ttu-id="167d9-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con modalità di \_ rendering GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="167d9-131">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

<span data-ttu-id="167d9-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ modalità matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="167d9-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="167d9-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="167d9-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="167d9-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con matrice di \_ proiezione GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="167d9-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="167d9-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ matrice di trama GL \_</span><span class="sxs-lookup"><span data-stu-id="167d9-135">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="167d9-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="167d9-136">Requirements</span></span>



| <span data-ttu-id="167d9-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="167d9-137">Requirement</span></span> | <span data-ttu-id="167d9-138">Valore</span><span class="sxs-lookup"><span data-stu-id="167d9-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="167d9-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="167d9-139">Minimum supported client</span></span><br/> | <span data-ttu-id="167d9-140">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="167d9-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="167d9-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="167d9-141">Minimum supported server</span></span><br/> | <span data-ttu-id="167d9-142">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="167d9-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="167d9-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="167d9-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="167d9-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="167d9-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="167d9-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="167d9-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="167d9-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="167d9-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="167d9-147">DLL</span><span class="sxs-lookup"><span data-stu-id="167d9-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="167d9-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="167d9-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="167d9-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="167d9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="167d9-150">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="167d9-150">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="167d9-151">**Remo**</span><span class="sxs-lookup"><span data-stu-id="167d9-151">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="167d9-152">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="167d9-152">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="167d9-153">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="167d9-153">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="167d9-154">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="167d9-154">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="167d9-155">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="167d9-155">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> <dt>

[<span data-ttu-id="167d9-156">**glScale**</span><span class="sxs-lookup"><span data-stu-id="167d9-156">**glScale**</span></span>](glscale.md)
</dt> <dt>

[<span data-ttu-id="167d9-157">**glTranslate**</span><span class="sxs-lookup"><span data-stu-id="167d9-157">**glTranslate**</span></span>](gltranslate.md)
</dt> </dl>

 

 





