---
title: funzione glEvalPoint1 (GL. h)
description: Le funzioni glEvalPoint1 e glEvalPoint2 generano e valutano un singolo punto in una rete mesh. | funzione glEvalPoint1 (GL. h)
ms.assetid: 5ef1d2f0-d77b-4bb8-a0d4-45c1a6a91c18
keywords:
- funzione glEvalPoint1 OpenGL
topic_type:
- apiref
api_name:
- glEvalPoint1
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34b9c3b8e17f5a0554c1864a401ecf49343806c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "103886230"
---
# <a name="glevalpoint1-function"></a><span data-ttu-id="044a7-105">glEvalPoint1 (funzione)</span><span class="sxs-lookup"><span data-stu-id="044a7-105">glEvalPoint1 function</span></span>

<span data-ttu-id="044a7-106">Le funzioni [**glEvalPoint1**](glevalpoint.md) e **glEvalPoint2** generano e valutano un singolo punto in una rete mesh.</span><span class="sxs-lookup"><span data-stu-id="044a7-106">The [**glEvalPoint1**](glevalpoint.md) and **glEvalPoint2** functions generate and evaluate a single point in a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="044a7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="044a7-107">Syntax</span></span>


```C++
void glEvalPoint1(
   GLint i
);
```



## <a name="parameters"></a><span data-ttu-id="044a7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="044a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="044a7-109">*i*</span><span class="sxs-lookup"><span data-stu-id="044a7-109">*i*</span></span> 
</dt> <dd>

<span data-ttu-id="044a7-110">Valore integer per la variabile di dominio Grid *i*.</span><span class="sxs-lookup"><span data-stu-id="044a7-110">The integer value for grid domain variable *i*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="044a7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="044a7-111">Return value</span></span>

<span data-ttu-id="044a7-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="044a7-112">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="044a7-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="044a7-113">Remarks</span></span>

<span data-ttu-id="044a7-114">Le funzioni [**glMapGrid**](glmapgrid-functions.md) e [**glEvalMesh**](glevalmesh-functions.md) vengono usate in tandem per generare e valutare in modo efficiente una serie di valori di dominio mappa uniformemente spazi.</span><span class="sxs-lookup"><span data-stu-id="044a7-114">The [**glMapGrid**](glmapgrid-functions.md) and [**glEvalMesh**](glevalmesh-functions.md) functions are used in tandem to efficiently generate and evaluate a series of evenly spaced map domain values.</span></span> <span data-ttu-id="044a7-115">È possibile utilizzare **glEvalPoint** per valutare un singolo punto della griglia nello stesso Gridspace attraversato da **glEvalMesh**.</span><span class="sxs-lookup"><span data-stu-id="044a7-115">You can use **glEvalPoint** to evaluate a single grid point in the same gridspace that is traversed by **glEvalMesh**.</span></span> <span data-ttu-id="044a7-116">La chiamata a [**glEvalPoint1**](glevalpoint.md) equivale alla chiamata a</span><span class="sxs-lookup"><span data-stu-id="044a7-116">Calling [**glEvalPoint1**](glevalpoint.md) is equivalent to calling</span></span>

<span data-ttu-id="044a7-117">**glEvalCoord1** (*i* ?*u*  + *u* 1);</span><span class="sxs-lookup"><span data-stu-id="044a7-117">**glEvalCoord1** (*i* ?*u* +*u* 1 );</span></span>

<span data-ttu-id="044a7-118">dove</span><span class="sxs-lookup"><span data-stu-id="044a7-118">where</span></span>

<span data-ttu-id="044a7-119">? *u* = (*u* 2 *u* 1)/*n*</span><span class="sxs-lookup"><span data-stu-id="044a7-119">?*u* = (*u* 2 *u* 1 )/*n*</span></span>

<span data-ttu-id="044a7-120">e *n*, *u* 1 e *u* 2 sono gli argomenti della funzione **glMapGrid1** più recente.</span><span class="sxs-lookup"><span data-stu-id="044a7-120">and *n*, *u* 1 , and *u* 2 are the arguments to the most recent **glMapGrid1** function.</span></span> <span data-ttu-id="044a7-121">Il requisito numerico assoluto è che se *i*  =  *n*, il valore calcolato da (*i* ?*u* + U1) è esattamente *u* 2.</span><span class="sxs-lookup"><span data-stu-id="044a7-121">The one absolute numeric requirement is that if *i* = *n*, then the value computed from (*i* ?*u* + u1 ) is exactly *u* 2 .</span></span>

<span data-ttu-id="044a7-122">Nel caso bidimensionale, **glEvalPoint2**, Let</span><span class="sxs-lookup"><span data-stu-id="044a7-122">In the two-dimensional case, **glEvalPoint2**, let</span></span>

<span data-ttu-id="044a7-123">? *u* = (*u* 2 *u* 1)/*n*</span><span class="sxs-lookup"><span data-stu-id="044a7-123">?*u* = (*u* 2 *u* 1 )/*n*</span></span>

<span data-ttu-id="044a7-124">? *v* = (*v* 2 *v* 1)/*m*</span><span class="sxs-lookup"><span data-stu-id="044a7-124">?*v* = (*v* 2 *v* 1 )/*m*</span></span>

<span data-ttu-id="044a7-125">dove *n*, *u* 1, *u* 2, *m*, *v* 1 e *v* 2 sono gli argomenti della funzione **glMapGrid2** più recente.</span><span class="sxs-lookup"><span data-stu-id="044a7-125">where *n*, *u* 1 , *u* 2 , *m*, *v* 1 , and *v* 2  are the arguments to the most recent **glMapGrid2** function.</span></span> <span data-ttu-id="044a7-126">Quindi la funzione **glEvalPoint2** equivale a chiamare</span><span class="sxs-lookup"><span data-stu-id="044a7-126">Then the **glEvalPoint2** function is equivalent to calling</span></span>

<span data-ttu-id="044a7-127">**glEvalCoord2** (*i* ?*u*  +  *u* 1, *j* ?*v*  +  *v* 1);</span><span class="sxs-lookup"><span data-stu-id="044a7-127">**glEvalCoord2** (*i* ?*u* + *u* 1 , *j* ?*v* + *v* 1 );</span></span>

<span data-ttu-id="044a7-128">Gli unici requisiti numerici assoluti sono che se *i* = *n*, il valore calcolato da (*i* ?*u*  +  *u* 1) è esattamente U2 e se *j*  =  *m*, il valore calcolato da (*j* ?*v*  +  *v* 1) è esattamente *v* 2.</span><span class="sxs-lookup"><span data-stu-id="044a7-128">The only absolute numeric requirements are that if *i*=*n*, then the value computed from (*i* ?*u* + *u* 1 ) is exactly u2 , and if *j* = *m*, then the value computed from (*j* ?*v* + *v* 1  ) is exactly *v* 2 .</span></span>

<span data-ttu-id="044a7-129">Le funzioni seguenti consentono di recuperare informazioni relative a [**glEvalPoint1**](glevalpoint.md) e **glEvalPoint2**:</span><span class="sxs-lookup"><span data-stu-id="044a7-129">The following functions retrieve information relating to [**glEvalPoint1**](glevalpoint.md) and **glEvalPoint2**:</span></span>

<span data-ttu-id="044a7-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Mappa1 \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="044a7-130">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAP1\_GRID\_DOMAIN</span></span>

<span data-ttu-id="044a7-131">**glGet** con argomento GL \_ map2 \_ Grid \_ Domain</span><span class="sxs-lookup"><span data-stu-id="044a7-131">**glGet** with argument GL\_MAP2\_GRID\_DOMAIN</span></span>

<span data-ttu-id="044a7-132">**glGet** con argomento dei \_ \_ segmenti della griglia Mappa1 \_</span><span class="sxs-lookup"><span data-stu-id="044a7-132">**glGet** with argument GL\_MAP1\_GRID\_SEGMENTS</span></span>

<span data-ttu-id="044a7-133">**glGet** con argomento dei \_ \_ segmenti della griglia map2 \_</span><span class="sxs-lookup"><span data-stu-id="044a7-133">**glGet** with argument GL\_MAP2\_GRID\_SEGMENTS</span></span>

## <a name="requirements"></a><span data-ttu-id="044a7-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="044a7-134">Requirements</span></span>



| <span data-ttu-id="044a7-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="044a7-135">Requirement</span></span> | <span data-ttu-id="044a7-136">Valore</span><span class="sxs-lookup"><span data-stu-id="044a7-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="044a7-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="044a7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="044a7-138">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="044a7-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="044a7-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="044a7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="044a7-140">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="044a7-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="044a7-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="044a7-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="044a7-142"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="044a7-142"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="044a7-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="044a7-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="044a7-144"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="044a7-144"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="044a7-145">DLL</span><span class="sxs-lookup"><span data-stu-id="044a7-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="044a7-146"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="044a7-146"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="044a7-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="044a7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="044a7-148">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="044a7-148">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="044a7-149">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="044a7-149">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="044a7-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="044a7-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="044a7-151">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="044a7-151">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="044a7-152">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="044a7-152">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="044a7-153">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="044a7-153">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> </dl>

 

 





