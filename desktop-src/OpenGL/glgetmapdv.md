---
title: funzione glGetMapdv (GL. h)
description: Le funzioni glGetMapdv, glGetMapfv e glGetMapiv restituiscono parametri di valutazione. | funzione glGetMapdv (GL. h)
ms.assetid: 3b4fc03b-ada4-4f4a-a234-fa6439f2e5c8
keywords:
- funzione glGetMapdv OpenGL
topic_type:
- apiref
api_name:
- glGetMapdv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbf7dd5104ce7a47b0d1215221c115a7191f4548
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321421"
---
# <a name="glgetmapdv-function"></a><span data-ttu-id="b1969-105">glGetMapdv (funzione)</span><span class="sxs-lookup"><span data-stu-id="b1969-105">glGetMapdv function</span></span>

<span data-ttu-id="b1969-106">Le funzioni **glGetMapdv**, [**glGetMapfv**](glgetmapfv.md)e [**glGetMapiv**](glgetmapiv.md) restituiscono parametri di valutazione.</span><span class="sxs-lookup"><span data-stu-id="b1969-106">The **glGetMapdv**, [**glGetMapfv**](glgetmapfv.md), and [**glGetMapiv**](glgetmapiv.md) functions return evaluator parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1969-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1969-107">Syntax</span></span>


```C++
void WINAPI glGetMapdv(
   GLenum   target,
   GLenum   query,
   GLdouble *v
);
```



## <a name="parameters"></a><span data-ttu-id="b1969-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1969-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1969-109">*target*</span><span class="sxs-lookup"><span data-stu-id="b1969-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="b1969-110">Nome simbolico di una mappa.</span><span class="sxs-lookup"><span data-stu-id="b1969-110">The symbolic name of a map.</span></span> <span data-ttu-id="b1969-111">I valori accettati sono i seguenti: GL \_ Mappa1 \_ Color \_ 4, GL \_ Mappa1 \_ index, GL \_ Mappa1 \_ Normal, GL \_ Mappa1 \_ texture \_ Coord \_ 1, GL \_ Mappa1 \_ texture \_ Coord \_ 2, GL \_ MAPPA1 \_ texture \_ Coord \_ 3, GL \_ MAPPA1 \_ texture \_ Coord \_ 4, GL \_ Mappa1 \_ Vertex \_ 3, GL \_ Mappa1 \_ Vertex \_ 4, GL \_ map2 \_ Color \_ 4, GL \_ map2 \_ index, GL \_ map2 \_ Normal, GL \_ map2 \_ texture \_ Coord \_ 1, GL \_ map2 \_ texture \_ Coord \_ 2, GL \_ MAP2 texture \_ \_ Coord \_ 3, GL \_ map2 \_ texture \_ Coord \_ 4, GL \_ map2 \_ Vertex \_ 3 e GL \_ map2 \_ Vertex \_ 4.</span><span class="sxs-lookup"><span data-stu-id="b1969-111">The following are accepted values: GL\_MAP1\_COLOR\_4, GL\_MAP1\_INDEX, GL\_MAP1\_NORMAL, GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP1\_VERTEX\_3, GL\_MAP1\_VERTEX\_4, GL\_MAP2\_COLOR\_4, GL\_MAP2\_INDEX, GL\_MAP2\_NORMAL, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, GL\_MAP2\_TEXTURE\_COORD\_4, GL\_MAP2\_VERTEX\_3, and GL\_MAP2\_VERTEX\_4.</span></span>

</dd> <dt>

<span data-ttu-id="b1969-112">*query*</span><span class="sxs-lookup"><span data-stu-id="b1969-112">*query*</span></span> 
</dt> <dd>

<span data-ttu-id="b1969-113">Specifica il parametro da restituire.</span><span class="sxs-lookup"><span data-stu-id="b1969-113">Specifies which parameter to return.</span></span> <span data-ttu-id="b1969-114">I nomi simbolici seguenti sono accettati.</span><span class="sxs-lookup"><span data-stu-id="b1969-114">The following symbolic names are accepted.</span></span>



| <span data-ttu-id="b1969-115">Valore</span><span class="sxs-lookup"><span data-stu-id="b1969-115">Value</span></span>                                                                                                                                             | <span data-ttu-id="b1969-116">Significato</span><span class="sxs-lookup"><span data-stu-id="b1969-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COEFF"></span><span id="gl_coeff"></span><dl> <span data-ttu-id="b1969-117"><dt>**\_Coeff GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b1969-117"><dt>**GL\_COEFF**</dt></span></span> </dl>    | <span data-ttu-id="b1969-118">Il parametro *v* restituisce i punti di controllo per la funzione di valutazione.</span><span class="sxs-lookup"><span data-stu-id="b1969-118">The *v* parameter returns the control points for the evaluator function.</span></span> <span data-ttu-id="b1969-119">Gli analizzatori unidimensionali restituiscono punti di controllo degli *ordini* e gli analizzatori bidimensionali restituiscono punti di controllo *uorder* *x* *Vorder* .</span><span class="sxs-lookup"><span data-stu-id="b1969-119">One-dimensional evaluators return *order* control points, and two-dimensional evaluators return *uorder* *x* *vorder* control points.</span></span> <span data-ttu-id="b1969-120">Ogni punto di controllo è costituito da un valore a virgola mobile a precisione singola, a due, tre o quattro, a virgola mobile e precisione doppia, a seconda del tipo di analizzatore.</span><span class="sxs-lookup"><span data-stu-id="b1969-120">Each control point consists of one, two, three, or four integer, single-precision floating-point, or double-precision floating-point values, depending on the type of the evaluator.</span></span> <span data-ttu-id="b1969-121">I punti di controllo bidimensionali vengono restituiti in ordine di riga, incrementando rapidamente l'indice *uorder* e l'indice *Vorder* dopo ogni riga.</span><span class="sxs-lookup"><span data-stu-id="b1969-121">Two-dimensional control points are returned in row-major order, incrementing the *uorder* index quickly, and the *vorder* index after each row.</span></span> <span data-ttu-id="b1969-122">I valori integer, se richiesti, vengono calcolati mediante l'arrotondamento dei valori a virgola mobile interni ai valori integer più vicini.</span><span class="sxs-lookup"><span data-stu-id="b1969-122">Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.</span></span><br/> |
| <span id="GL_ORDER"></span><span id="gl_order"></span><dl> <span data-ttu-id="b1969-123"><dt>**\_ordine GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b1969-123"><dt>**GL\_ORDER**</dt></span></span> </dl>    | <span data-ttu-id="b1969-124">Il parametro *v* restituisce l'ordine della funzione dell'analizzatore.</span><span class="sxs-lookup"><span data-stu-id="b1969-124">The *v* parameter returns the order of the evaluator function.</span></span> <span data-ttu-id="b1969-125">Gli analizzatori unidimensionali restituiscono un singolo valore, *Order*.</span><span class="sxs-lookup"><span data-stu-id="b1969-125">One-dimensional evaluators return a single value, *order*.</span></span> <span data-ttu-id="b1969-126">Gli analizzatori bidimensionali restituiscono due valori, *uorder* e *Vorder*.</span><span class="sxs-lookup"><span data-stu-id="b1969-126">Two-dimensional evaluators return two values, *uorder* and *vorder*.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_DOMAIN"></span><span id="gl_domain"></span><dl> <span data-ttu-id="b1969-127"><dt>**\_dominio GL**</dt></span><span class="sxs-lookup"><span data-stu-id="b1969-127"><dt>**GL\_DOMAIN**</dt></span></span> </dl> | <span data-ttu-id="b1969-128">Il parametro *v* restituisce i parametri di mapping *u* e *v* lineari.</span><span class="sxs-lookup"><span data-stu-id="b1969-128">The *v* parameter returns the linear *u* and *v* mapping parameters.</span></span> <span data-ttu-id="b1969-129">Gli analizzatori unidimensionali restituiscono due valori, *u* 1 e *u* 2, come specificato da [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="b1969-129">One-dimensional evaluators return two values, *u* 1 and *u* 2, as specified by [**glMap1**](glmap1.md).</span></span> <span data-ttu-id="b1969-130">Gli analizzatori bidimensionali restituiscono quattro valori (*U1*, *U2*, *V1* e *v2*) come specificato da [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="b1969-130">Two-dimensional evaluators return four values (*u1*, *u2*, *v1*, and *v2*) as specified by [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="b1969-131">I valori integer, se richiesti, vengono calcolati mediante l'arrotondamento dei valori a virgola mobile interni ai valori integer più vicini.</span><span class="sxs-lookup"><span data-stu-id="b1969-131">Integer values, when requested, are computed by rounding the internal floating-point values to the nearest integer values.</span></span><br/>                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="b1969-132">*v*</span><span class="sxs-lookup"><span data-stu-id="b1969-132">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="b1969-133">Restituisce i dati richiesti.</span><span class="sxs-lookup"><span data-stu-id="b1969-133">Returns the requested data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1969-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b1969-134">Return value</span></span>

<span data-ttu-id="b1969-135">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="b1969-135">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b1969-136">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="b1969-136">Error codes</span></span>

<span data-ttu-id="b1969-137">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="b1969-137">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="b1969-138">Nome</span><span class="sxs-lookup"><span data-stu-id="b1969-138">Name</span></span>                                                                                                  | <span data-ttu-id="b1969-139">Significato</span><span class="sxs-lookup"><span data-stu-id="b1969-139">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b1969-140"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b1969-140"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="b1969-141">*target* o *query* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="b1969-141">*target* or *query* was not an accepted value.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="b1969-142"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b1969-142"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="b1969-143">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="b1969-143">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b1969-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="b1969-144">Remarks</span></span>

<span data-ttu-id="b1969-145">La funzione **glGetMap** restituisce i parametri dell'analizzatore.</span><span class="sxs-lookup"><span data-stu-id="b1969-145">The **glGetMap** function returns evaluator parameters.</span></span> <span data-ttu-id="b1969-146">Le funzioni **glMap1** e **glMap2** definiscono gli analizzatori. Il parametro *target* specifica una mappa, *query* seleziona un parametro specifico e *v* punta alla risorsa di archiviazione in cui verranno restituiti i valori.</span><span class="sxs-lookup"><span data-stu-id="b1969-146">(The **glMap1** and **glMap2** functions define evaluators.) The *target* parameter specifies a map, *query* selects a specific parameter, and *v* points to storage where the values will be returned.</span></span>

<span data-ttu-id="b1969-147">I valori accettabili per il parametro di *destinazione* sono descritti in [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="b1969-147">The acceptable values for the *target* parameter are described in [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span>

<span data-ttu-id="b1969-148">Se viene generato un errore, non viene apportata alcuna modifica al contenuto di *v*.</span><span class="sxs-lookup"><span data-stu-id="b1969-148">If an error is generated, no change is made to the contents of *v*.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1969-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1969-149">Requirements</span></span>



| <span data-ttu-id="b1969-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1969-150">Requirement</span></span> | <span data-ttu-id="b1969-151">Valore</span><span class="sxs-lookup"><span data-stu-id="b1969-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1969-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1969-152">Minimum supported client</span></span><br/> | <span data-ttu-id="b1969-153">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b1969-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b1969-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1969-154">Minimum supported server</span></span><br/> | <span data-ttu-id="b1969-155">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b1969-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b1969-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1969-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1969-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1969-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="b1969-158">Libreria</span><span class="sxs-lookup"><span data-stu-id="b1969-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="b1969-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1969-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="b1969-160">DLL</span><span class="sxs-lookup"><span data-stu-id="b1969-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1969-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1969-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1969-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1969-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1969-163">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="b1969-163">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="b1969-164">**Remo**</span><span class="sxs-lookup"><span data-stu-id="b1969-164">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="b1969-165">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="b1969-165">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="b1969-166">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="b1969-166">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="b1969-167">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="b1969-167">**glMap2**</span></span>](glmap2.md)
</dt> </dl>

 

 





