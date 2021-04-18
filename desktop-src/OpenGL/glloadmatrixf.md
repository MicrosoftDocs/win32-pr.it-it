---
title: funzione glLoadMatrixf (GL. h)
description: La funzione glLoadMatrixf sostituisce la matrice corrente con una matrice arbitraria. | funzione glLoadMatrixf (GL. h)
ms.assetid: 6e1337b0-d1e7-4002-a561-d959d7f70942
keywords:
- funzione glLoadMatrixf OpenGL
topic_type:
- apiref
api_name:
- glLoadMatrixf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a0c54f4f7f7255b2dde724cf018d57fab6cf3e7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321209"
---
# <a name="glloadmatrixf-function"></a><span data-ttu-id="25b79-105">glLoadMatrixf (funzione)</span><span class="sxs-lookup"><span data-stu-id="25b79-105">glLoadMatrixf function</span></span>

<span data-ttu-id="25b79-106">Le funzioni [**glLoadMatrixd**](glloadmatrixd.md) e **glLoadMatrixf** sostituiscono la matrice corrente con una matrice arbitraria.</span><span class="sxs-lookup"><span data-stu-id="25b79-106">The [**glLoadMatrixd**](glloadmatrixd.md) and **glLoadMatrixf** functions replace the current matrix with an arbitrary matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="25b79-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25b79-107">Syntax</span></span>


```C++
void WINAPI glLoadMatrixf(
   const GLfloat *m
);
```



## <a name="parameters"></a><span data-ttu-id="25b79-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="25b79-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25b79-109">*m*</span><span class="sxs-lookup"><span data-stu-id="25b79-109">*m*</span></span> 
</dt> <dd>

<span data-ttu-id="25b79-110">Puntatore a una matrice 4x4 archiviato nell'ordine colonna-Major come 16 valori consecutivi.</span><span class="sxs-lookup"><span data-stu-id="25b79-110">A pointer to a 4x4 matrix stored in column-major order as 16 consecutive values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25b79-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25b79-111">Return value</span></span>

<span data-ttu-id="25b79-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="25b79-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="25b79-113">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="25b79-113">Error codes</span></span>

<span data-ttu-id="25b79-114">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="25b79-114">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="25b79-115">Nome</span><span class="sxs-lookup"><span data-stu-id="25b79-115">Name</span></span>                                                                                                  | <span data-ttu-id="25b79-116">Significato</span><span class="sxs-lookup"><span data-stu-id="25b79-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="25b79-117"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="25b79-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="25b79-118">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="25b79-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="25b79-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="25b79-119">Remarks</span></span>

<span data-ttu-id="25b79-120">La funzione **glLoadMatrix** sostituisce la matrice corrente con quella specificata in *m*.</span><span class="sxs-lookup"><span data-stu-id="25b79-120">The **glLoadMatrix** function replaces the current matrix with the one specified in *m*.</span></span> <span data-ttu-id="25b79-121">La matrice corrente è la matrice di proiezione, la matrice Modelview o la matrice di trama, determinata dalla modalità matrice corrente (vedere [**glMatrixMode**](glmatrixmode.md)).</span><span class="sxs-lookup"><span data-stu-id="25b79-121">The current matrix is the projection matrix, modelview matrix, or texture matrix, determined by the current matrix mode (see [**glMatrixMode**](glmatrixmode.md)).</span></span>

<span data-ttu-id="25b79-122">Il parametro *m* punta a una matrice 4x4 di valori a virgola mobile a precisione singola o a precisione doppia archiviati in ordine colonna-principale.</span><span class="sxs-lookup"><span data-stu-id="25b79-122">The *m* parameter points to a 4x4 matrix of single-precision or double-precision floating-point values stored in column-major order.</span></span> <span data-ttu-id="25b79-123">Ovvero la matrice viene archiviata come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="25b79-123">That is, the matrix is stored as shown in the following image.</span></span>

![Diagramma che mostra la matrice 4x4 a cui punta il parametro m.](images/load02.png)

<span data-ttu-id="25b79-125">Le funzioni seguenti consentono di recuperare informazioni correlate a **glLoadMatrix**:</span><span class="sxs-lookup"><span data-stu-id="25b79-125">The following functions retrieve information related to **glLoadMatrix**:</span></span>

<span data-ttu-id="25b79-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ modalità matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="25b79-126">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="25b79-127">**glGet** con argomento GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="25b79-127">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="25b79-128">**glGet** con matrice di \_ proiezione GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="25b79-128">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="25b79-129">**glGet** con argomento della \_ matrice di trama GL \_</span><span class="sxs-lookup"><span data-stu-id="25b79-129">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="25b79-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25b79-130">Requirements</span></span>



| <span data-ttu-id="25b79-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="25b79-131">Requirement</span></span> | <span data-ttu-id="25b79-132">Valore</span><span class="sxs-lookup"><span data-stu-id="25b79-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25b79-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25b79-133">Minimum supported client</span></span><br/> | <span data-ttu-id="25b79-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="25b79-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="25b79-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25b79-135">Minimum supported server</span></span><br/> | <span data-ttu-id="25b79-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="25b79-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="25b79-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25b79-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="25b79-138"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="25b79-138"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="25b79-139">Libreria</span><span class="sxs-lookup"><span data-stu-id="25b79-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="25b79-140"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="25b79-140"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="25b79-141">DLL</span><span class="sxs-lookup"><span data-stu-id="25b79-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25b79-142"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25b79-142"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25b79-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25b79-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25b79-144">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="25b79-144">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="25b79-145">**Remo**</span><span class="sxs-lookup"><span data-stu-id="25b79-145">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="25b79-146">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="25b79-146">**glLoadIdentity**</span></span>](glloadidentity.md)
</dt> <dt>

[<span data-ttu-id="25b79-147">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="25b79-147">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="25b79-148">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="25b79-148">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="25b79-149">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="25b79-149">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





