---
title: funzione glMultMatrixf (GL. h)
description: La funzione glMultMatrixf moltiplica la matrice corrente in base a una matrice arbitraria. | funzione glMultMatrixf (GL. h)
ms.assetid: fea5e557-09bd-4c45-89cc-9f3739b577bb
keywords:
- funzione glMultMatrixf OpenGL
topic_type:
- apiref
api_name:
- glMultMatrixf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f981b78dc2d9f152a4a7d1f40c4a2d1f120944b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104557598"
---
# <a name="glmultmatrixf-function"></a><span data-ttu-id="a339f-105">glMultMatrixf (funzione)</span><span class="sxs-lookup"><span data-stu-id="a339f-105">glMultMatrixf function</span></span>

<span data-ttu-id="a339f-106">Le funzioni [**glMultMatrixd**](glmultmatrixd.md) e **glMultMatrixf** moltiplicano la matrice corrente in base a una matrice arbitraria.</span><span class="sxs-lookup"><span data-stu-id="a339f-106">The [**glMultMatrixd**](glmultmatrixd.md) and **glMultMatrixf** functions multiply the current matrix by an arbitrary matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="a339f-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a339f-107">Syntax</span></span>


```C++
void WINAPI glMultMatrixf(
   const GLfloat *m
);
```



## <a name="parameters"></a><span data-ttu-id="a339f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a339f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a339f-109">*m*</span><span class="sxs-lookup"><span data-stu-id="a339f-109">*m*</span></span> 
</dt> <dd>

<span data-ttu-id="a339f-110">Puntatore a una matrice 4x4 archiviato nell'ordine colonna-Major come 16 valori consecutivi.</span><span class="sxs-lookup"><span data-stu-id="a339f-110">A pointer to a 4x4 matrix stored in column-major order as 16 consecutive values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a339f-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a339f-111">Return value</span></span>

<span data-ttu-id="a339f-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="a339f-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a339f-113">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a339f-113">Error codes</span></span>

<span data-ttu-id="a339f-114">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="a339f-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a339f-115">Nome</span><span class="sxs-lookup"><span data-stu-id="a339f-115">Name</span></span>                                                                                                  | <span data-ttu-id="a339f-116">Significato</span><span class="sxs-lookup"><span data-stu-id="a339f-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a339f-117"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a339f-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a339f-118">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a339f-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a339f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="a339f-119">Remarks</span></span>

<span data-ttu-id="a339f-120">La funzione **glMultMatrix** moltiplica la matrice corrente in base a quella specificata in *m*.</span><span class="sxs-lookup"><span data-stu-id="a339f-120">The **glMultMatrix** function multiplies the current matrix by the one specified in *m*.</span></span> <span data-ttu-id="a339f-121">Ovvero, se M è la matrice corrente e T è la matrice passata a **glMultMatrix**, m viene sostituito con m T.</span><span class="sxs-lookup"><span data-stu-id="a339f-121">That is, if M is the current matrix and T is the matrix passed to **glMultMatrix**, then M is replaced with M   T.</span></span>

<span data-ttu-id="a339f-122">La matrice corrente è la matrice di proiezione, la matrice Modelview o la matrice di trama, determinata dalla modalità matrice corrente (vedere [**glMatrixMode**](glmatrixmode.md)).</span><span class="sxs-lookup"><span data-stu-id="a339f-122">The current matrix is the projection matrix, modelview matrix, or texture matrix, determined by the current matrix mode (see [**glMatrixMode**](glmatrixmode.md)).</span></span>

<span data-ttu-id="a339f-123">Il parametro *m* punta a una matrice 4x4 di valori a virgola mobile a precisione singola o a precisione doppia archiviati in ordine colonna-principale.</span><span class="sxs-lookup"><span data-stu-id="a339f-123">The *m* parameter points to a 4x4 matrix of single-precision or double-precision floating-point values stored in column-major order.</span></span> <span data-ttu-id="a339f-124">Ovvero la matrice viene archiviata come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="a339f-124">That is, the matrix is stored as shown in the following image.</span></span>

![! [Diagramma che mostra la matrice 4x4 a cui punta il parametro m.]](images/multi01.png)

<span data-ttu-id="a339f-126">Le funzioni seguenti consentono di recuperare informazioni correlate a **glMultMatrix**:</span><span class="sxs-lookup"><span data-stu-id="a339f-126">The following functions retrieve information related to **glMultMatrix**:</span></span>

<span data-ttu-id="a339f-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ modalità matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="a339f-127">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="a339f-128">**glGet** con argomento GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="a339f-128">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="a339f-129">**glGet** con matrice di \_ proiezione GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="a339f-129">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="a339f-130">**glGet** con argomento della \_ matrice di trama GL \_</span><span class="sxs-lookup"><span data-stu-id="a339f-130">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="a339f-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a339f-131">Requirements</span></span>



| <span data-ttu-id="a339f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a339f-132">Requirement</span></span> | <span data-ttu-id="a339f-133">Valore</span><span class="sxs-lookup"><span data-stu-id="a339f-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a339f-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a339f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a339f-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a339f-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a339f-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a339f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a339f-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a339f-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a339f-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a339f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="a339f-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a339f-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a339f-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="a339f-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="a339f-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a339f-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a339f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="a339f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a339f-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a339f-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a339f-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a339f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a339f-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a339f-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a339f-146">**Remo**</span><span class="sxs-lookup"><span data-stu-id="a339f-146">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a339f-147">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="a339f-147">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="a339f-148">**glLoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="a339f-148">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="a339f-149">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="a339f-149">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="a339f-150">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="a339f-150">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





