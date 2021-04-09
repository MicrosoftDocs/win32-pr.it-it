---
title: funzione glMapGrid1d (GL. h)
description: Definisce una mesh unidimensionale. | funzione glMapGrid1d (GL. h)
ms.assetid: a0bc822e-dd98-4586-a322-2779e11f38ca
keywords:
- funzione glMapGrid1d OpenGL
topic_type:
- apiref
api_name:
- glMapGrid1d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30b1900f5597e8c516100504ca7288137ed99ded
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886084"
---
# <a name="glmapgrid1d-function"></a><span data-ttu-id="b89ff-105">glMapGrid1d (funzione)</span><span class="sxs-lookup"><span data-stu-id="b89ff-105">glMapGrid1d function</span></span>

<span data-ttu-id="b89ff-106">Definisce una mesh unidimensionale.</span><span class="sxs-lookup"><span data-stu-id="b89ff-106">Defines a one-dimensional mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="b89ff-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b89ff-107">Syntax</span></span>


```C++
void WINAPI glMapGrid1d(
   GLint    un,
   GLdouble u1,
   GLdouble u2
);
```



## <a name="parameters"></a><span data-ttu-id="b89ff-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b89ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b89ff-109">*non*</span><span class="sxs-lookup"><span data-stu-id="b89ff-109">*un*</span></span> 
</dt> <dd>

<span data-ttu-id="b89ff-110">Il numero di partizioni nell'intervallo di intervallo della griglia \[ U1, U2 \] .</span><span class="sxs-lookup"><span data-stu-id="b89ff-110">The number of partitions in the grid range interval \[u1, u2\].</span></span> <span data-ttu-id="b89ff-111">Il valore deve essere positivo.</span><span class="sxs-lookup"><span data-stu-id="b89ff-111">This value must be positive.</span></span>

</dd> <dt>

<span data-ttu-id="b89ff-112">*U1*</span><span class="sxs-lookup"><span data-stu-id="b89ff-112">*u1*</span></span> 
</dt> <dd>

<span data-ttu-id="b89ff-113">Valore usato come mapping per il valore di dominio della griglia integer i = 0.</span><span class="sxs-lookup"><span data-stu-id="b89ff-113">A value used as the mapping for integer grid domain value i = 0.</span></span>

</dd> <dt>

<span data-ttu-id="b89ff-114">*U2*</span><span class="sxs-lookup"><span data-stu-id="b89ff-114">*u2*</span></span> 
</dt> <dd>

<span data-ttu-id="b89ff-115">Valore usato come mapping per il valore di dominio della griglia integer i = un.</span><span class="sxs-lookup"><span data-stu-id="b89ff-115">A value used as the mapping for integer grid domain value i = un.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b89ff-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b89ff-116">Return value</span></span>

<span data-ttu-id="b89ff-117">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="b89ff-117">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b89ff-118">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="b89ff-118">Error codes</span></span>

<span data-ttu-id="b89ff-119">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="b89ff-119">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b89ff-120">Nome</span><span class="sxs-lookup"><span data-stu-id="b89ff-120">Name</span></span>                                                                                                  | <span data-ttu-id="b89ff-121">Significato</span><span class="sxs-lookup"><span data-stu-id="b89ff-121">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b89ff-122"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b89ff-122"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="b89ff-123">Una o *VN* non è *un* valore positivo.</span><span class="sxs-lookup"><span data-stu-id="b89ff-123">Either *un* or *vn* was not positive.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="b89ff-124"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b89ff-124"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b89ff-125">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b89ff-125">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b89ff-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="b89ff-126">Remarks</span></span>

<span data-ttu-id="b89ff-127">Usare le funzioni **glMapGrid** e [glEvalMesh](glevalmesh-functions.md) riunisceper reagire per generare e valutare in modo efficiente una serie di valori di dominio mappa uniformemente spazi.</span><span class="sxs-lookup"><span data-stu-id="b89ff-127">Use the **glMapGrid** and [glEvalMesh](glevalmesh-functions.md) functions togetherto efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="b89ff-128">La funzione glEvalMesh esegue il passaggio del dominio Integer di una griglia bidimensionale, il cui intervallo è il dominio delle mappe di valutazione specificate da [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="b89ff-128">The glEvalMesh function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span>

<span data-ttu-id="b89ff-129">Le funzioni **glMapGrid1** e [**glMapGrid2**](glmapgrid2d.md) specificano i mapping della griglia lineare tra le coordinate di griglia integer i (o i e j), per le coordinate della mappa di valutazione a virgola mobile u (o u e v).</span><span class="sxs-lookup"><span data-stu-id="b89ff-129">The **glMapGrid1** and [**glMapGrid2**](glmapgrid2d.md) functions specify the linear grid mappings between the i (or i and j) integer grid coordinates, to the u (or u and v) floating-point evaluation map coordinates.</span></span> <span data-ttu-id="b89ff-130">Per informazioni dettagliate sulla valutazione delle coordinate di e v, vedere [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md) .</span><span class="sxs-lookup"><span data-stu-id="b89ff-130">See [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md) for details of how u and v coordinates are evaluated.</span></span>

<span data-ttu-id="b89ff-131">La funzione **glMapGrid1** specifica un singolo mapping lineare, in modo tale che la *coordinata* della griglia Integer 0 sia mappata esattamente a U1 e che le coordinate della griglia integer non siano corrette per *U2*.</span><span class="sxs-lookup"><span data-stu-id="b89ff-131">The **glMapGrid1** function specifies a single linear mapping such that integer grid coordinate 0 maps exactly to u1, and integer grid coordinate *un* maps exactly to *u2*.</span></span> <span data-ttu-id="b89ff-132">Tutte le altre coordinate della griglia integer *di cui è* stato eseguito il mapping:</span><span class="sxs-lookup"><span data-stu-id="b89ff-132">All other integer grid coordinates *i* are mapped such that:</span></span>

<span data-ttu-id="b89ff-133">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="b89ff-133">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="b89ff-134">La funzione [**glMapGrid2**](glmapgrid2d.md) specifica due mapping lineari di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="b89ff-134">The [**glMapGrid2**](glmapgrid2d.md) function specifies two such linear mappings.</span></span> <span data-ttu-id="b89ff-135">Viene eseguito il mapping tra le coordinate della griglia integer *i = 0* esattamente la *U1* e la coordinata di griglia integer *i = un* esattamente con *U2*.</span><span class="sxs-lookup"><span data-stu-id="b89ff-135">One maps integer grid coordinate *i = 0* exactly to *u1*, and integer grid coordinate *i = un* exactly to *u2*.</span></span> <span data-ttu-id="b89ff-136">L'altra coordinata della griglia di tipo integer *j = 0* esattamente alla *V1* e la coordinata della griglia integer *j = VN* esattamente alla versione *v2*.</span><span class="sxs-lookup"><span data-stu-id="b89ff-136">The other maps integer grid coordinate *j = 0* exactly to *v1*, and integer grid coordinate *j = vn* exactly to *v2*.</span></span> <span data-ttu-id="b89ff-137">Sono state mappate altre coordinate della griglia integer i e j</span><span class="sxs-lookup"><span data-stu-id="b89ff-137">Other integer grid coordinates i and j are mapped such that</span></span>

<span data-ttu-id="b89ff-138">*u = i (U2 U1)/un + U1*</span><span class="sxs-lookup"><span data-stu-id="b89ff-138">*u = i(u2 u1)/un + u1*</span></span>

<span data-ttu-id="b89ff-139">*v = j (v2 v1)/VN + V1*</span><span class="sxs-lookup"><span data-stu-id="b89ff-139">*v = j (v2 v1)/vn + v1*</span></span>

<span data-ttu-id="b89ff-140">I mapping specificati da **glMapGrid** vengono usati in modo identico da [glEvalMesh](glevalmesh-functions.md) e [**glEvalPoint**](glevalpoint.md).</span><span class="sxs-lookup"><span data-stu-id="b89ff-140">The mappings specified by **glMapGrid** are used identically by [glEvalMesh](glevalmesh-functions.md) and [**glEvalPoint**](glevalpoint.md).</span></span>

<span data-ttu-id="b89ff-141">Le funzioni seguenti consentono di recuperare informazioni correlate a **glMapGrid**:</span><span class="sxs-lookup"><span data-stu-id="b89ff-141">The following functions retrieve information related to **glMapGrid**:</span></span>

<dl>

<span data-ttu-id="b89ff-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Mappa1 \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="b89ff-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="b89ff-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ map2 \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="b89ff-143">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_DOMAIN</span></span>  
<span data-ttu-id="b89ff-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento dei \_ \_ segmenti della griglia Mappa1 \_</span><span class="sxs-lookup"><span data-stu-id="b89ff-144">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>  
<span data-ttu-id="b89ff-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento dei \_ \_ segmenti della griglia map2 \_</span><span class="sxs-lookup"><span data-stu-id="b89ff-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="b89ff-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b89ff-146">Requirements</span></span>



| <span data-ttu-id="b89ff-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="b89ff-147">Requirement</span></span> | <span data-ttu-id="b89ff-148">Valore</span><span class="sxs-lookup"><span data-stu-id="b89ff-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b89ff-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b89ff-149">Minimum supported client</span></span><br/> | <span data-ttu-id="b89ff-150">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b89ff-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b89ff-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b89ff-151">Minimum supported server</span></span><br/> | <span data-ttu-id="b89ff-152">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b89ff-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b89ff-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b89ff-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="b89ff-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b89ff-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b89ff-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="b89ff-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="b89ff-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b89ff-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b89ff-157">DLL</span><span class="sxs-lookup"><span data-stu-id="b89ff-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b89ff-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b89ff-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b89ff-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b89ff-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b89ff-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b89ff-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b89ff-161">**Remo**</span><span class="sxs-lookup"><span data-stu-id="b89ff-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b89ff-162">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="b89ff-162">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="b89ff-163">glEvalMesh</span><span class="sxs-lookup"><span data-stu-id="b89ff-163">glEvalMesh</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="b89ff-164">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="b89ff-164">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="b89ff-165">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="b89ff-165">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="b89ff-166">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="b89ff-166">**glMap2**</span></span>](glmap2.md)
</dt> </dl>

 

 





