---
title: funzione glEvalPoint2 (GL. h)
description: Le funzioni glEvalPoint1 e glEvalPoint2 generano e valutano un singolo punto in una rete mesh. | funzione glEvalPoint2 (GL. h)
ms.assetid: babae9c7-84a8-4a7e-b6f9-97c4e8bd42fe
keywords:
- funzione glEvalPoint2 OpenGL
topic_type:
- apiref
api_name:
- glEvalPoint2
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fafe728249f988462b0929873bbb195fed1e7c9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321891"
---
# <a name="glevalpoint2-function"></a><span data-ttu-id="ae9f6-105">glEvalPoint2 (funzione)</span><span class="sxs-lookup"><span data-stu-id="ae9f6-105">glEvalPoint2 function</span></span>

<span data-ttu-id="ae9f6-106">Le funzioni [**glEvalPoint1**](glevalpoint.md) e **glEvalPoint2** generano e valutano un singolo punto in una rete mesh.</span><span class="sxs-lookup"><span data-stu-id="ae9f6-106">The [**glEvalPoint1**](glevalpoint.md) and **glEvalPoint2** functions generate and evaluate a single point in a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae9f6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ae9f6-107">Syntax</span></span>


```C++
void glEvalPoint2(
   GLint i,
   GLint j
);
```



## <a name="parameters"></a><span data-ttu-id="ae9f6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="ae9f6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae9f6-109">*i*</span><span class="sxs-lookup"><span data-stu-id="ae9f6-109">*i*</span></span> 
</dt> <dd>

<span data-ttu-id="ae9f6-110">Valore integer per la variabile di dominio Grid *i*.</span><span class="sxs-lookup"><span data-stu-id="ae9f6-110">The integer value for grid domain variable *i*.</span></span>

</dd> <dt>

<span data-ttu-id="ae9f6-111">*j*</span><span class="sxs-lookup"><span data-stu-id="ae9f6-111">*j*</span></span> 
</dt> <dd>

<span data-ttu-id="ae9f6-112">Valore integer per la variabile di dominio Grid *j* .</span><span class="sxs-lookup"><span data-stu-id="ae9f6-112">The integer value for grid domain variable *j* .</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae9f6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ae9f6-113">Return value</span></span>

<span data-ttu-id="ae9f6-114">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ae9f6-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae9f6-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="ae9f6-115">Remarks</span></span>

<span data-ttu-id="ae9f6-116">Le funzioni [**glMapGrid**](glmapgrid-functions.md) e [**glEvalMesh**](glevalmesh-functions.md) vengono usate in tandem per generare e valutare in modo efficiente una serie di valori di dominio mappa uniformemente spazi.</span><span class="sxs-lookup"><span data-stu-id="ae9f6-116">The [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) functions are used in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="ae9f6-117">È possibile utilizzare **glEvalPoint** per valutare un singolo punto della griglia nello stesso Gridspace attraversato da **glEvalMesh**.</span><span class="sxs-lookup"><span data-stu-id="ae9f6-117">You can use **glEvalPoint** to evaluate a single grid point in the same gridspace that is traversed by **glEvalMesh**.</span></span> <span data-ttu-id="ae9f6-118">La chiamata a [**glEvalPoint1**](glevalpoint.md) equivale alla chiamata a</span><span class="sxs-lookup"><span data-stu-id="ae9f6-118">Calling [**glEvalPoint1**](glevalpoint.md) is equivalent to calling</span></span>

<span data-ttu-id="ae9f6-119">**glEvalCoord1** (*i* ?*u*  + *u* 1);</span><span class="sxs-lookup"><span data-stu-id="ae9f6-119">**glEvalCoord1** (*i* ?*u* +*u* 1 );</span></span>

<span data-ttu-id="ae9f6-120">dove</span><span class="sxs-lookup"><span data-stu-id="ae9f6-120">where</span></span>

<span data-ttu-id="ae9f6-121">? *u* = (*u* 2 *u* 1)/*n*</span><span class="sxs-lookup"><span data-stu-id="ae9f6-121">?*u* = (*u* 2 *u* 1 )/*n*</span></span>

<span data-ttu-id="ae9f6-122">e *n*, *u* 1 e *u* 2 sono gli argomenti della funzione **glMapGrid1** più recente.</span><span class="sxs-lookup"><span data-stu-id="ae9f6-122">and *n*, *u* 1 , and *u* 2 are the arguments to the most recent **glMapGrid1** function.</span></span> <span data-ttu-id="ae9f6-123">Il requisito numerico assoluto è che se *i*  =  *n*, il valore calcolato da (*i* ?*u* + U1) è esattamente *u* 2.</span><span class="sxs-lookup"><span data-stu-id="ae9f6-123">The one absolute numeric requirement is that if *i* = *n*, then the value computed from (*i* ?*u* + u1 ) is exactly *u* 2 .</span></span>

<span data-ttu-id="ae9f6-124">Nel caso bidimensionale, **glEvalPoint2**, Let</span><span class="sxs-lookup"><span data-stu-id="ae9f6-124">In the two-dimensional case, **glEvalPoint2**, let</span></span>

<span data-ttu-id="ae9f6-125">? *u* = (*u* 2 *u* 1)/*n*</span><span class="sxs-lookup"><span data-stu-id="ae9f6-125">?*u* = (*u* 2 *u* 1 )/*n*</span></span>

<span data-ttu-id="ae9f6-126">? *v* = (*v* 2 *v* 1)/*m*</span><span class="sxs-lookup"><span data-stu-id="ae9f6-126">?*v* = (*v* 2 *v* 1 )/*m*</span></span>

<span data-ttu-id="ae9f6-127">dove *n*, *u* 1, *u* 2, *m*, *v* 1 e *v* 2 sono gli argomenti della funzione **glMapGrid2** più recente.</span><span class="sxs-lookup"><span data-stu-id="ae9f6-127">where *n*, *u* 1 , *u* 2 , *m*, *v* 1 , and *v* 2  are the arguments to the most recent **glMapGrid2** function.</span></span> <span data-ttu-id="ae9f6-128">Quindi la funzione **glEvalPoint2** equivale a chiamare</span><span class="sxs-lookup"><span data-stu-id="ae9f6-128">Then the **glEvalPoint2** function is equivalent to calling</span></span>

<span data-ttu-id="ae9f6-129">**glEvalCoord2** (*i* ?*u*  +  *u* 1, *j* ?*v*  +  *v* 1);</span><span class="sxs-lookup"><span data-stu-id="ae9f6-129">**glEvalCoord2** (*i* ?*u* + *u* 1 , *j* ?*v* + *v* 1 );</span></span>

<span data-ttu-id="ae9f6-130">Gli unici requisiti numerici assoluti sono che se *i* = *n*, il valore calcolato da (*i* ?*u*  +  *u* 1) è esattamente U2 e se *j*  =  *m*, il valore calcolato da (*j* ?*v*  +  *v* 1) è esattamente *v* 2.</span><span class="sxs-lookup"><span data-stu-id="ae9f6-130">The only absolute numeric requirements are that if *i*=*n*, then the value computed from (*i* ?*u* + *u* 1 ) is exactly u2 , and if *j* = *m*, then the value computed from (*j* ?*v* + *v* 1  ) is exactly *v* 2 .</span></span>

<span data-ttu-id="ae9f6-131">Le funzioni seguenti consentono di recuperare informazioni relative a [**glEvalPoint1**](glevalpoint.md) e **glEvalPoint2**:</span><span class="sxs-lookup"><span data-stu-id="ae9f6-131">The following functions retrieve information relating to [**glEvalPoint1**](glevalpoint.md) and **glEvalPoint2**:</span></span>

<span data-ttu-id="ae9f6-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Mappa1 \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="ae9f6-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>

<span data-ttu-id="ae9f6-133">**glGet** con argomento GL \_ map2 \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="ae9f6-133">**glGet** with argument GL\_MAP2\_GRID\_DOMAIN</span></span>

<span data-ttu-id="ae9f6-134">**glGet** con argomento dei \_ \_ segmenti della griglia Mappa1 \_</span><span class="sxs-lookup"><span data-stu-id="ae9f6-134">**glGet** with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>

<span data-ttu-id="ae9f6-135">**glGet** con argomento dei \_ \_ segmenti della griglia map2 \_</span><span class="sxs-lookup"><span data-stu-id="ae9f6-135">**glGet** with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="ae9f6-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ae9f6-136">Requirements</span></span>



| <span data-ttu-id="ae9f6-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae9f6-137">Requirement</span></span> | <span data-ttu-id="ae9f6-138">Valore</span><span class="sxs-lookup"><span data-stu-id="ae9f6-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae9f6-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae9f6-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ae9f6-140">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ae9f6-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ae9f6-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ae9f6-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ae9f6-142">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ae9f6-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ae9f6-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ae9f6-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae9f6-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae9f6-144"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ae9f6-145">Libreria</span><span class="sxs-lookup"><span data-stu-id="ae9f6-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="ae9f6-146"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae9f6-146"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ae9f6-147">DLL</span><span class="sxs-lookup"><span data-stu-id="ae9f6-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae9f6-148"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae9f6-148"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae9f6-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ae9f6-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae9f6-150">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="ae9f6-150">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="ae9f6-151">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="ae9f6-151">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="ae9f6-152">**glGet**</span><span class="sxs-lookup"><span data-stu-id="ae9f6-152">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="ae9f6-153">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="ae9f6-153">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="ae9f6-154">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="ae9f6-154">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="ae9f6-155">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="ae9f6-155">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> </dl>

 

 





