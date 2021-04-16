---
title: funzione glLoadIdentity (GL. h)
description: La funzione glLoadIdentity sostituisce la matrice corrente con la matrice di identità.
ms.assetid: 59273aa9-4db3-4c8c-8364-f54c03d2f97a
keywords:
- funzione glLoadIdentity OpenGL
topic_type:
- apiref
api_name:
- glLoadIdentity
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a2afde8ae06602933d6790c4fce33e9130a78cb
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104553644"
---
# <a name="glloadidentity-function"></a><span data-ttu-id="65561-104">glLoadIdentity (funzione)</span><span class="sxs-lookup"><span data-stu-id="65561-104">glLoadIdentity function</span></span>

<span data-ttu-id="65561-105">La funzione **glLoadIdentity** sostituisce la matrice corrente con la matrice di identità.</span><span class="sxs-lookup"><span data-stu-id="65561-105">The **glLoadIdentity** function replaces the current matrix with the identity matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="65561-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="65561-106">Syntax</span></span>


```C++
void WINAPI glLoadIdentity(void);
```



## <a name="parameters"></a><span data-ttu-id="65561-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="65561-107">Parameters</span></span>

<span data-ttu-id="65561-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="65561-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="65561-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="65561-109">Return value</span></span>

<span data-ttu-id="65561-110">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="65561-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="65561-111">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="65561-111">Error codes</span></span>

<span data-ttu-id="65561-112">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="65561-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="65561-113">Nome</span><span class="sxs-lookup"><span data-stu-id="65561-113">Name</span></span>                                                                                                  | <span data-ttu-id="65561-114">Significato</span><span class="sxs-lookup"><span data-stu-id="65561-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="65561-115"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="65561-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="65561-116">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="65561-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="65561-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="65561-117">Remarks</span></span>

<span data-ttu-id="65561-118">La funzione **glLoadIdentity** sostituisce la matrice corrente con la matrice di identità.</span><span class="sxs-lookup"><span data-stu-id="65561-118">The **glLoadIdentity** function replaces the current matrix with the identity matrix.</span></span> <span data-ttu-id="65561-119">È semanticamente equivalente alla chiamata di [**glLoadMatrix**](glloadmatrix.md) con la matrice di identità seguente.</span><span class="sxs-lookup"><span data-stu-id="65561-119">It is semantically equivalent to calling [**glLoadMatrix**](glloadmatrix.md) with the following identity matrix.</span></span>

![Diagramma che mostra la matrice di identità che glLoadIdentity chiama.](images/load01.png)

<span data-ttu-id="65561-121">Tuttavia, in alcuni casi, è più efficiente.</span><span class="sxs-lookup"><span data-stu-id="65561-121">However, in some cases, it is more efficient.</span></span>

<span data-ttu-id="65561-122">Le funzioni seguenti consentono di recuperare informazioni correlate a **glLoadIdentity**:</span><span class="sxs-lookup"><span data-stu-id="65561-122">The following functions retrieve information related to **glLoadIdentity**:</span></span>

<span data-ttu-id="65561-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento della \_ modalità matrice GL \_</span><span class="sxs-lookup"><span data-stu-id="65561-123">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MATRIX\_MODE</span></span>

<span data-ttu-id="65561-124">**glGet** con argomento GL \_ MODELVIEW \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="65561-124">**glGet** with argument GL\_MODELVIEW\_MATRIX</span></span>

<span data-ttu-id="65561-125">**glGet** con matrice di \_ proiezione GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="65561-125">**glGet** with argument GL\_PROJECTION\_MATRIX</span></span>

<span data-ttu-id="65561-126">**glGet** con argomento della \_ matrice di trama GL \_</span><span class="sxs-lookup"><span data-stu-id="65561-126">**glGet** with argument GL\_TEXTURE\_MATRIX</span></span>

## <a name="requirements"></a><span data-ttu-id="65561-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="65561-127">Requirements</span></span>



| <span data-ttu-id="65561-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="65561-128">Requirement</span></span> | <span data-ttu-id="65561-129">Valore</span><span class="sxs-lookup"><span data-stu-id="65561-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65561-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65561-130">Minimum supported client</span></span><br/> | <span data-ttu-id="65561-131">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="65561-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="65561-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="65561-132">Minimum supported server</span></span><br/> | <span data-ttu-id="65561-133">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="65561-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="65561-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="65561-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="65561-135"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="65561-135"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="65561-136">Libreria</span><span class="sxs-lookup"><span data-stu-id="65561-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="65561-137"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65561-137"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="65561-138">DLL</span><span class="sxs-lookup"><span data-stu-id="65561-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65561-139"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65561-139"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65561-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="65561-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65561-141">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="65561-141">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="65561-142">**Remo**</span><span class="sxs-lookup"><span data-stu-id="65561-142">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="65561-143">**glLoadMatrix**</span><span class="sxs-lookup"><span data-stu-id="65561-143">**glLoadMatrix**</span></span>](glloadmatrix.md)
</dt> <dt>

[<span data-ttu-id="65561-144">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="65561-144">**glMatrixMode**</span></span>](glmatrixmode.md)
</dt> <dt>

[<span data-ttu-id="65561-145">**glMultMatrix**</span><span class="sxs-lookup"><span data-stu-id="65561-145">**glMultMatrix**</span></span>](glmultmatrix.md)
</dt> <dt>

[<span data-ttu-id="65561-146">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="65561-146">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





