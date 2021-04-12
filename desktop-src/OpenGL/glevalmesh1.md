---
title: funzione glEvalMesh1 (GL. h)
description: Calcola una griglia unidimensionale di punti o linee.
ms.assetid: 176a4b81-f1a7-42fc-8ecd-bba77a0ec5b3
keywords:
- funzione glEvalMesh1 OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8950dcf397816fca8eb5a6add45c45512c48866
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518094"
---
# <a name="glevalmesh1-function"></a><span data-ttu-id="117e1-104">glEvalMesh1 (funzione)</span><span class="sxs-lookup"><span data-stu-id="117e1-104">glEvalMesh1 function</span></span>

<span data-ttu-id="117e1-105">Calcola una griglia unidimensionale di punti o linee.</span><span class="sxs-lookup"><span data-stu-id="117e1-105">Computes a one-dimensional grid of points or lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="117e1-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="117e1-106">Syntax</span></span>


```C++
void WINAPI glEvalMesh1(
   GLenum mode,
   GLint  i1,
   GLint  i2
);
```



## <a name="parameters"></a><span data-ttu-id="117e1-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="117e1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="117e1-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="117e1-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="117e1-109">Valore che specifica se calcolare una mesh unidimensionale di punti o linee.</span><span class="sxs-lookup"><span data-stu-id="117e1-109">A value that specifies whether to compute a one-dimensional mesh of points or lines.</span></span> <span data-ttu-id="117e1-110">Sono accettate le costanti simboliche seguenti: GL \_ Point e GL \_ line.</span><span class="sxs-lookup"><span data-stu-id="117e1-110">The following symbolic constants are accepted: GL\_POINT and GL\_LINE.</span></span>

</dd> <dt>

<span data-ttu-id="117e1-111">*I1*</span><span class="sxs-lookup"><span data-stu-id="117e1-111">*i1*</span></span> 
</dt> <dd>

<span data-ttu-id="117e1-112">Primo valore integer per la variabile di dominio Grid i.</span><span class="sxs-lookup"><span data-stu-id="117e1-112">The first integer value for grid domain variable i.</span></span>

</dd> <dt>

<span data-ttu-id="117e1-113">*I2*</span><span class="sxs-lookup"><span data-stu-id="117e1-113">*i2*</span></span> 
</dt> <dd>

<span data-ttu-id="117e1-114">Ultimo valore integer per la variabile di dominio Grid i.</span><span class="sxs-lookup"><span data-stu-id="117e1-114">The last integer value for grid domain variable i.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="117e1-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="117e1-115">Return value</span></span>

<span data-ttu-id="117e1-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="117e1-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="117e1-117">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="117e1-117">Error codes</span></span>

<span data-ttu-id="117e1-118">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="117e1-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="117e1-119">Nome</span><span class="sxs-lookup"><span data-stu-id="117e1-119">Name</span></span>                                                                                                  | <span data-ttu-id="117e1-120">Significato</span><span class="sxs-lookup"><span data-stu-id="117e1-120">Meaning</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="117e1-121"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="117e1-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="117e1-122">Indica che la *modalità* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="117e1-122">Indicates that *mode* is not an accepted value.</span></span> <br/>                                                                            |
| <dl> <span data-ttu-id="117e1-123"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="117e1-123"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="117e1-124">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="117e1-124">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="117e1-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="117e1-125">Remarks</span></span>

<span data-ttu-id="117e1-126">Usare [**glMapGrid**](glmapgrid-functions.md) e [**glEvalMesh**](glevalmesh-functions.md) insieme per generare e valutare in modo efficiente una serie di valori di dominio mappa uniformemente spazi.</span><span class="sxs-lookup"><span data-stu-id="117e1-126">Use [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) together to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="117e1-127">La funzione **glEvalMesh** esegue il passaggio del dominio Integer di una griglia bidimensionale, il cui intervallo è il dominio delle mappe di valutazione specificate da [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="117e1-127">The **glEvalMesh** function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="117e1-128">Il parametro mode determina se i vertici risultanti sono connessi come punti, linee o poligoni riempiti.</span><span class="sxs-lookup"><span data-stu-id="117e1-128">The mode parameter determines whether the resulting vertices are connected as points, lines, or filled polygons.</span></span>

<span data-ttu-id="117e1-129">Nel caso unidimensionale, **glEvalMesh1**, la mesh viene generata come se fosse stato eseguito il frammento di codice seguente:</span><span class="sxs-lookup"><span data-stu-id="117e1-129">In the one-dimensional case, **glEvalMesh1**, the mesh is generated as if the following code fragment were executed:</span></span>

<span data-ttu-id="117e1-130">[**glBegin**](glbegin.md)(*tipo*);</span><span class="sxs-lookup"><span data-stu-id="117e1-130">[**glBegin**](glbegin.md)(*type*);</span></span>

<span data-ttu-id="117e1-131">for (i = I1; i <= I2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="117e1-131">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="117e1-132">{</span><span class="sxs-lookup"><span data-stu-id="117e1-132">{</span></span>

<span data-ttu-id="117e1-133">[**glEvalCoord1**](glevalcoord1d.md)(i? u + U1)</span><span class="sxs-lookup"><span data-stu-id="117e1-133">[**glEvalCoord1**](glevalcoord1d.md)(i?u + u1)</span></span>

<span data-ttu-id="117e1-134">}</span><span class="sxs-lookup"><span data-stu-id="117e1-134">}</span></span>

<span data-ttu-id="117e1-135">[**glEnd**](glend.md)();</span><span class="sxs-lookup"><span data-stu-id="117e1-135">[**glEnd**](glend.md)( );</span></span>

<span data-ttu-id="117e1-136">dove</span><span class="sxs-lookup"><span data-stu-id="117e1-136">where</span></span>

<span data-ttu-id="117e1-137">? u = (U2 U1)/n</span><span class="sxs-lookup"><span data-stu-id="117e1-137">?u = (u2 u1) / n</span></span>

<span data-ttu-id="117e1-138">e n, U1 e U2 sono gli argomenti della funzione [**glMapGrid1**](glmapgrid1d.md) più recente.</span><span class="sxs-lookup"><span data-stu-id="117e1-138">and n, u1, and u2 are the arguments to the most recent [**glMapGrid1**](glmapgrid1d.md) function.</span></span> <span data-ttu-id="117e1-139">Il parametro di *tipo* è \_ punti GL se Mode è il \_ punto GL oppure GL \_ Lines If mode è GL \_ line.</span><span class="sxs-lookup"><span data-stu-id="117e1-139">The *type* parameter is GL\_POINTS if mode is GL\_POINT, or GL\_LINES if mode is GL\_LINE.</span></span> <span data-ttu-id="117e1-140">Un requisito numerico assoluto è che se i = n, il valore calcolato da i? u + U1 è esattamente U2.</span><span class="sxs-lookup"><span data-stu-id="117e1-140">The one absolute numeric requirement is that if i = n, then the value computed from i?u + u1 is exactly u2.</span></span>

## <a name="requirements"></a><span data-ttu-id="117e1-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="117e1-141">Requirements</span></span>



| <span data-ttu-id="117e1-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="117e1-142">Requirement</span></span> | <span data-ttu-id="117e1-143">Valore</span><span class="sxs-lookup"><span data-stu-id="117e1-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="117e1-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="117e1-144">Minimum supported client</span></span><br/> | <span data-ttu-id="117e1-145">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="117e1-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="117e1-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="117e1-146">Minimum supported server</span></span><br/> | <span data-ttu-id="117e1-147">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="117e1-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="117e1-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="117e1-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="117e1-149"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="117e1-149"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="117e1-150">Libreria</span><span class="sxs-lookup"><span data-stu-id="117e1-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="117e1-151"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="117e1-151"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="117e1-152">DLL</span><span class="sxs-lookup"><span data-stu-id="117e1-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="117e1-153"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="117e1-153"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="117e1-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="117e1-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="117e1-155">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="117e1-155">**glBegin**</span></span>](glbegin.md)
</dt> </dl>

 

 





