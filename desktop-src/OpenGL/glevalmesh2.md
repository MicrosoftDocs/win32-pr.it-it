---
title: funzione glEvalMesh2 (GL. h)
description: Calcola una griglia bidimensionale di punti o linee.
ms.assetid: 21e94388-903e-4b9d-8e54-9c914d0ce372
keywords:
- funzione glEvalMesh2 OpenGL
topic_type:
- apiref
api_name:
- glEvalMesh2
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 531e9f1f6288116d052c728654cd2cf03f38550a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740671"
---
# <a name="glevalmesh2-function"></a><span data-ttu-id="2d2a8-104">glEvalMesh2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="2d2a8-104">glEvalMesh2 function</span></span>

<span data-ttu-id="2d2a8-105">Calcola una griglia bidimensionale di punti o linee.</span><span class="sxs-lookup"><span data-stu-id="2d2a8-105">Computes a two-dimensional grid of points or lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d2a8-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d2a8-106">Syntax</span></span>


```C++
void WINAPI glEvalMesh2(
   GLenum mode,
   GLint  i1,
   GLint  i2,
   GLint  j1,
   GLint  j2
);
```



## <a name="parameters"></a><span data-ttu-id="2d2a8-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d2a8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d2a8-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="2d2a8-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="2d2a8-109">Valore che specifica se calcolare una mesh bidimensionale di punti, linee o poligoni.</span><span class="sxs-lookup"><span data-stu-id="2d2a8-109">A value that specifies whether to compute a two-dimensional mesh of points, lines, or polygons.</span></span> <span data-ttu-id="2d2a8-110">Sono accettate le costanti simboliche seguenti: GL \_ Point, GL \_ line e GL \_ Fill.</span><span class="sxs-lookup"><span data-stu-id="2d2a8-110">The following symbolic constants are accepted: GL\_POINT, GL\_LINE, and GL\_FILL.</span></span>

</dd> <dt>

<span data-ttu-id="2d2a8-111">*I1*</span><span class="sxs-lookup"><span data-stu-id="2d2a8-111">*i1*</span></span> 
</dt> <dd>

<span data-ttu-id="2d2a8-112">Primo valore integer per la variabile di dominio Grid i.</span><span class="sxs-lookup"><span data-stu-id="2d2a8-112">The first integer value for grid domain variable i.</span></span>

</dd> <dt>

<span data-ttu-id="2d2a8-113">*I2*</span><span class="sxs-lookup"><span data-stu-id="2d2a8-113">*i2*</span></span> 
</dt> <dd>

<span data-ttu-id="2d2a8-114">Ultimo valore integer per la variabile di dominio Grid i.</span><span class="sxs-lookup"><span data-stu-id="2d2a8-114">The last integer value for grid domain variable i.</span></span>

</dd> <dt>

<span data-ttu-id="2d2a8-115">*J1*</span><span class="sxs-lookup"><span data-stu-id="2d2a8-115">*j1*</span></span> 
</dt> <dd>

<span data-ttu-id="2d2a8-116">Primo valore integer per la variabile di dominio Grid j.</span><span class="sxs-lookup"><span data-stu-id="2d2a8-116">The first integer value for grid domain variable j.</span></span>

</dd> <dt>

<span data-ttu-id="2d2a8-117">*J2*</span><span class="sxs-lookup"><span data-stu-id="2d2a8-117">*j2*</span></span> 
</dt> <dd>

<span data-ttu-id="2d2a8-118">Ultimo valore integer per la variabile di dominio Grid j.</span><span class="sxs-lookup"><span data-stu-id="2d2a8-118">The last integer value for grid domain variable j.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d2a8-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d2a8-119">Return value</span></span>

<span data-ttu-id="2d2a8-120">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="2d2a8-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2d2a8-121">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="2d2a8-121">Error codes</span></span>

<span data-ttu-id="2d2a8-122">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="2d2a8-122">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="2d2a8-123">Nome</span><span class="sxs-lookup"><span data-stu-id="2d2a8-123">Name</span></span>                                                                                                  | <span data-ttu-id="2d2a8-124">Significato</span><span class="sxs-lookup"><span data-stu-id="2d2a8-124">Meaning</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2d2a8-125"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2d2a8-125"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="2d2a8-126">Indica che la *modalità* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="2d2a8-126">Indicates that *mode* is not an accepted value.</span></span> <br/>                                                                            |
| <dl> <span data-ttu-id="2d2a8-127"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2d2a8-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="2d2a8-128">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="2d2a8-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="2d2a8-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d2a8-129">Remarks</span></span>

<span data-ttu-id="2d2a8-130">Usare [**glMapGrid**](glmapgrid-functions.md) e [**glEvalMesh**](glevalmesh-functions.md) in tandem per generare e valutare in modo efficiente una serie di valori di dominio mappa uniformemente spazi.</span><span class="sxs-lookup"><span data-stu-id="2d2a8-130">Use [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="2d2a8-131">La funzione **glEvalMesh** esegue il passaggio del dominio Integer di una griglia bidimensionale, il cui intervallo è il dominio delle mappe di valutazione specificate da [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="2d2a8-131">The **glEvalMesh** function steps through the integer domain of a one- or two-dimensional grid, whose range is the domain of the evaluation maps specified by [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="2d2a8-132">Il parametro mode determina se i vertici risultanti sono connessi come punti, linee o poligoni riempiti.</span><span class="sxs-lookup"><span data-stu-id="2d2a8-132">The mode parameter determines whether the resulting vertices are connected as points, lines, or filled polygons.</span></span>

<span data-ttu-id="2d2a8-133">Nel caso bidimensionale, **glEvalMesh2**, Let</span><span class="sxs-lookup"><span data-stu-id="2d2a8-133">In the two-dimensional case, **glEvalMesh2**, let</span></span>

<span data-ttu-id="2d2a8-134">?</span><span class="sxs-lookup"><span data-stu-id="2d2a8-134">?</span></span> <span data-ttu-id="2d2a8-135">u = (U2 U1)/n</span><span class="sxs-lookup"><span data-stu-id="2d2a8-135">u = (u2 u1)/n</span></span>

<span data-ttu-id="2d2a8-136">?</span><span class="sxs-lookup"><span data-stu-id="2d2a8-136">?</span></span> <span data-ttu-id="2d2a8-137">v = (v2 v1)/m,</span><span class="sxs-lookup"><span data-stu-id="2d2a8-137">v = (v2 v1)/m,</span></span>

<span data-ttu-id="2d2a8-138">dove n, U1, U2, m, V1 e V2 sono gli argomenti della funzione [**glMapGrid2**](glmapgrid-functions.md) più recente.</span><span class="sxs-lookup"><span data-stu-id="2d2a8-138">where n, u1, u2, m, v1, and v2 are the arguments to the most recent [**glMapGrid2**](glmapgrid-functions.md) function.</span></span> <span data-ttu-id="2d2a8-139">Quindi, se *mode* è il \_ riempimento GL, **glEvalMesh2** è equivalente a:</span><span class="sxs-lookup"><span data-stu-id="2d2a8-139">Then, if *mode* is GL\_FILL, **glEvalMesh2** is equivalent to:</span></span>

<span data-ttu-id="2d2a8-140">per (j = J1; j < J2; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="2d2a8-140">for (j = j1; j < j2; j += 1)</span></span>

<span data-ttu-id="2d2a8-141">{</span><span class="sxs-lookup"><span data-stu-id="2d2a8-141">{</span></span>

<span data-ttu-id="2d2a8-142">[**glBegin**](glbegin.md)(GL \_ Quad \_ Strip);</span><span class="sxs-lookup"><span data-stu-id="2d2a8-142">[**glBegin**](glbegin.md)(GL\_QUAD\_STRIP);</span></span>

<span data-ttu-id="2d2a8-143">for (i = I1; i <= I2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="2d2a8-143">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="2d2a8-144">{</span><span class="sxs-lookup"><span data-stu-id="2d2a8-144">{</span></span>

<span data-ttu-id="2d2a8-145">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1 (), j?</span><span class="sxs-lookup"><span data-stu-id="2d2a8-145">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1 ( ) , j ?</span></span> <span data-ttu-id="2d2a8-146">v + v1);</span><span class="sxs-lookup"><span data-stu-id="2d2a8-146">v + v1);</span></span>

<span data-ttu-id="2d2a8-147">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1 (), (j + 1)?</span><span class="sxs-lookup"><span data-stu-id="2d2a8-147">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1 ( ) , (j+1) ?</span></span> <span data-ttu-id="2d2a8-148">v + v1);</span><span class="sxs-lookup"><span data-stu-id="2d2a8-148">v + v1);</span></span>

<span data-ttu-id="2d2a8-149">}</span><span class="sxs-lookup"><span data-stu-id="2d2a8-149">}</span></span>

<span data-ttu-id="2d2a8-150">[**glEnd**](glend.md)(); }</span><span class="sxs-lookup"><span data-stu-id="2d2a8-150">[**glEnd**](glend.md)( ); }</span></span>

<span data-ttu-id="2d2a8-151">Se *mode* è \_ la riga GL, una chiamata a **glEvalMesh2** è equivalente a:</span><span class="sxs-lookup"><span data-stu-id="2d2a8-151">If *mode* is GL\_LINE, then a call to **glEvalMesh2** is equivalent to:</span></span>

<span data-ttu-id="2d2a8-152">per (j = J1; j <= J2; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="2d2a8-152">for (j = j1; j <= j2; j += 1)</span></span>

<span data-ttu-id="2d2a8-153">{</span><span class="sxs-lookup"><span data-stu-id="2d2a8-153">{</span></span>

<span data-ttu-id="2d2a8-154">[**glBegin**](glbegin.md)( \_ striscia di riga GL \_ );</span><span class="sxs-lookup"><span data-stu-id="2d2a8-154">[**glBegin**](glbegin.md)(GL\_LINE\_STRIP);</span></span>

<span data-ttu-id="2d2a8-155">for (i = I1; i <= I2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="2d2a8-155">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="2d2a8-156">{</span><span class="sxs-lookup"><span data-stu-id="2d2a8-156">{</span></span>

<span data-ttu-id="2d2a8-157">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);</span><span class="sxs-lookup"><span data-stu-id="2d2a8-157">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);</span></span>

<span data-ttu-id="2d2a8-158">}</span><span class="sxs-lookup"><span data-stu-id="2d2a8-158">}</span></span>

<span data-ttu-id="2d2a8-159">[**glEnd**](glend.md)();</span><span class="sxs-lookup"><span data-stu-id="2d2a8-159">[**glEnd**](glend.md)( );</span></span>

<span data-ttu-id="2d2a8-160">}</span><span class="sxs-lookup"><span data-stu-id="2d2a8-160">}</span></span>

<span data-ttu-id="2d2a8-161">for (i = I1; i <= I2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="2d2a8-161">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="2d2a8-162">{</span><span class="sxs-lookup"><span data-stu-id="2d2a8-162">{</span></span>

<span data-ttu-id="2d2a8-163">[**glBegin**](glbegin.md)( \_ striscia di riga GL \_ );</span><span class="sxs-lookup"><span data-stu-id="2d2a8-163">[**glBegin**](glbegin.md)(GL\_LINE\_STRIP);</span></span>

<span data-ttu-id="2d2a8-164">per (j = J1; j <= J1; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="2d2a8-164">for (j = j1; j <= j1; j += 1)</span></span>

<span data-ttu-id="2d2a8-165">{</span><span class="sxs-lookup"><span data-stu-id="2d2a8-165">{</span></span>

<span data-ttu-id="2d2a8-166">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);</span><span class="sxs-lookup"><span data-stu-id="2d2a8-166">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);</span></span>

<span data-ttu-id="2d2a8-167">}</span><span class="sxs-lookup"><span data-stu-id="2d2a8-167">}</span></span>

<span data-ttu-id="2d2a8-168">glEnd ();</span><span class="sxs-lookup"><span data-stu-id="2d2a8-168">glEnd( );</span></span>

<span data-ttu-id="2d2a8-169">}</span><span class="sxs-lookup"><span data-stu-id="2d2a8-169">}</span></span>

<span data-ttu-id="2d2a8-170">Infine, se *mode* è \_ il punto GL, una chiamata a **glEvalMesh2** è equivalente a:</span><span class="sxs-lookup"><span data-stu-id="2d2a8-170">And finally, if *mode* is GL\_POINT, then a call to **glEvalMesh2** is equivalent to:</span></span>

<span data-ttu-id="2d2a8-171">[**glBegin**](glbegin.md)( \_ punti GL);</span><span class="sxs-lookup"><span data-stu-id="2d2a8-171">[**glBegin**](glbegin.md)(GL\_POINTS);</span></span>

<span data-ttu-id="2d2a8-172">per (j = J1; j <= J2; j + = 1)</span><span class="sxs-lookup"><span data-stu-id="2d2a8-172">for (j = j1; j <= j2; j += 1)</span></span>

<span data-ttu-id="2d2a8-173">{</span><span class="sxs-lookup"><span data-stu-id="2d2a8-173">{</span></span>

<span data-ttu-id="2d2a8-174">for (i = I1; i <= I2; i + = 1)</span><span class="sxs-lookup"><span data-stu-id="2d2a8-174">for (i = i1; i <= i2; i += 1)</span></span>

<span data-ttu-id="2d2a8-175">{</span><span class="sxs-lookup"><span data-stu-id="2d2a8-175">{</span></span>

<span data-ttu-id="2d2a8-176">[**glEvalCoord2**](glevalcoord2d.md)(i? u + U1, j? v + v1);</span><span class="sxs-lookup"><span data-stu-id="2d2a8-176">[**glEvalCoord2**](glevalcoord2d.md)(i? u + u1, j? v + v1);</span></span>

<span data-ttu-id="2d2a8-177">}</span><span class="sxs-lookup"><span data-stu-id="2d2a8-177">}</span></span>

<span data-ttu-id="2d2a8-178">}</span><span class="sxs-lookup"><span data-stu-id="2d2a8-178">}</span></span>

<span data-ttu-id="2d2a8-179">[**glEnd**](glend.md)();</span><span class="sxs-lookup"><span data-stu-id="2d2a8-179">[**glEnd**](glend.md)( );</span></span>

<span data-ttu-id="2d2a8-180">In tutti e tre i casi, gli unici requisiti numerici assoluti sono che se i = n, il valore calcolato da i? u + U1 è esattamente U2 e se j = m, il valore calcolato da j? v + v1 è esattamente V2.</span><span class="sxs-lookup"><span data-stu-id="2d2a8-180">In all three cases, the only absolute numeric requirements are that if i = n, then the value computed from i? u + u1 is exactly u2, and if j = m, then the value computed from j? v + v1 is exactly v2.</span></span> <span data-ttu-id="2d2a8-181">Le funzioni seguenti consentono di recuperare informazioni relative a **glEvalMesh**:</span><span class="sxs-lookup"><span data-stu-id="2d2a8-181">The following functions retrieve information relating to **glEvalMesh**:</span></span>

<span data-ttu-id="2d2a8-182">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Mappa1 \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="2d2a8-182">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>

<span data-ttu-id="2d2a8-183">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ map2 \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="2d2a8-183">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_DOMAIN</span></span>

<span data-ttu-id="2d2a8-184">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento dei \_ \_ segmenti della griglia Mappa1 \_</span><span class="sxs-lookup"><span data-stu-id="2d2a8-184">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>

<span data-ttu-id="2d2a8-185">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento dei \_ \_ segmenti della griglia map2 \_</span><span class="sxs-lookup"><span data-stu-id="2d2a8-185">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="2d2a8-186">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d2a8-186">Requirements</span></span>



| <span data-ttu-id="2d2a8-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d2a8-187">Requirement</span></span> | <span data-ttu-id="2d2a8-188">Valore</span><span class="sxs-lookup"><span data-stu-id="2d2a8-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d2a8-189">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d2a8-189">Minimum supported client</span></span><br/> | <span data-ttu-id="2d2a8-190">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2d2a8-190">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2d2a8-191">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2d2a8-191">Minimum supported server</span></span><br/> | <span data-ttu-id="2d2a8-192">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2d2a8-192">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2d2a8-193">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d2a8-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d2a8-194"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d2a8-194"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="2d2a8-195">Libreria</span><span class="sxs-lookup"><span data-stu-id="2d2a8-195">Library</span></span><br/>                  | <dl> <span data-ttu-id="2d2a8-196"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d2a8-196"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2d2a8-197">DLL</span><span class="sxs-lookup"><span data-stu-id="2d2a8-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d2a8-198"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d2a8-198"><dt>Opengl32.dll</dt></span></span> </dl> |



 

 





