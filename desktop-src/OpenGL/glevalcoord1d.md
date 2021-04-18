---
title: funzione glEvalCoord1d (GL. h)
description: La funzione glEvalCoord1d valuta i mapping unidimensionali abilitati.
ms.assetid: 5e884f11-fb3f-4158-8041-6c71509bf7d5
keywords:
- funzione glEvalCoord1d OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord1d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 239d0cc6267989bfd4ae020f1f8935c0cca1c192
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301168"
---
# <a name="glevalcoord1d-function"></a><span data-ttu-id="63304-104">glEvalCoord1d (funzione)</span><span class="sxs-lookup"><span data-stu-id="63304-104">glEvalCoord1d function</span></span>

<span data-ttu-id="63304-105">La funzione **glEvalCoord1d** valuta i mapping unidimensionali abilitati.</span><span class="sxs-lookup"><span data-stu-id="63304-105">The **glEvalCoord1d** function evaluates enabled one-dimensional maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="63304-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63304-106">Syntax</span></span>


```C++
void WINAPI glEvalCoord1d(
   GLdouble u
);
```



## <a name="parameters"></a><span data-ttu-id="63304-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="63304-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63304-108">*u*</span><span class="sxs-lookup"><span data-stu-id="63304-108">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="63304-109">Valore che rappresenta la coordinata di dominio *u* per la funzione di base definita in una funzione [**glMap1**](glmap1.md) precedente.</span><span class="sxs-lookup"><span data-stu-id="63304-109">A value that is the domain coordinate *u* to the basis function defined in a previous [**glMap1**](glmap1.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63304-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63304-110">Return value</span></span>

<span data-ttu-id="63304-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="63304-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="63304-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="63304-112">Remarks</span></span>

<span data-ttu-id="63304-113">La funzione **glEvalCoord1d** valuta le mappe unidimensionali abilitate all'argomento *u*.</span><span class="sxs-lookup"><span data-stu-id="63304-113">The **glEvalCoord1d** function evaluates enabled one-dimensional maps at argument *u*.</span></span> <span data-ttu-id="63304-114">Definire Maps con [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="63304-114">Define maps with [**glMap1**](glmap1.md).</span></span> <span data-ttu-id="63304-115">Abilitarli o disabilitarli con [**glEnable**](glenable.md) e [**glDisable**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="63304-115">Enable or disable them with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="63304-116">Quando viene eseguita una delle funzioni **glEvalCoord** , vengono valutate tutte le mappe attualmente abilitate della dimensione indicata.</span><span class="sxs-lookup"><span data-stu-id="63304-116">When one of the **glEvalCoord** functions is issued, all currently enabled maps of the indicated dimension are evaluated.</span></span> <span data-ttu-id="63304-117">Quindi, per ogni mappa abilitata, è come se la funzione OpenGL corrispondente venisse eseguita con il valore calcolato.</span><span class="sxs-lookup"><span data-stu-id="63304-117">Then, for each enabled map, it is as if the corresponding OpenGL function were issued with the computed value.</span></span> <span data-ttu-id="63304-118">Ovvero, se \_ \_ è abilitato l'indice GL MAPPA1 o GL \_ map2 \_ , viene simulata una funzione [**glIndex**](glindex-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="63304-118">That is, if GL\_MAP1\_INDEX or GL\_MAP2\_INDEX is enabled, a [**glIndex**](glindex-functions.md) function is simulated.</span></span> <span data-ttu-id="63304-119">Se GL \_ Mappa1 \_ Color \_ 4 o GL \_ map2 \_ Color \_ 4 è abilitato, viene simulata una funzione **glcolor** .</span><span class="sxs-lookup"><span data-stu-id="63304-119">If GL\_MAP1\_COLOR\_4 or GL\_MAP2\_COLOR\_4 is enabled, a **glcolor** function is simulated.</span></span> <span data-ttu-id="63304-120">Se GL \_ Mappa1 \_ Normal o GL \_ map2 \_ Normal è abilitato, viene prodotto un vettore normale e, se è presente una \_ MAPPA1 \_ trama \_ Coord \_ 1, GL \_ Mappa1 \_ trama \_ Coord \_ 2, GL \_ Mappa1 \_ texture \_ Coord \_ 3, GL \_ Mappa1 \_ texture \_ Coord \_ 4, GL \_ map2 \_ texture \_ Coord \_ 1, GL \_ map2 \_ texture \_ Coord \_ 2, GL \_ map2 \_ texture \_ Coord \_ 3 e GL \_ map2 \_ texture \_ Coord \_ 4 è abilitato, viene simulata una funzione [**glTexCoord**](gltexcoord-functions.md) appropriata.</span><span class="sxs-lookup"><span data-stu-id="63304-120">If GL\_MAP1\_NORMAL or GL\_MAP2\_NORMAL is enabled, a normal vector is produced, and if any of GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, and GL\_MAP2\_TEXTURE\_COORD\_4 is enabled, then an appropriate [**glTexCoord**](gltexcoord-functions.md) function is simulated.</span></span>

<span data-ttu-id="63304-121">OpenGL usa i valori valutati anziché i valori correnti per le valutazioni abilitate e i valori correnti in caso contrario, per le coordinate di colore, indice dei colori, normale e trama.</span><span class="sxs-lookup"><span data-stu-id="63304-121">OpenGL uses evaluated values instead of current values for those evaluations that are enabled, and current values otherwise, for color, color index, normal, and texture coordinates.</span></span> <span data-ttu-id="63304-122">Tuttavia, i valori valutati non aggiornano i valori correnti.</span><span class="sxs-lookup"><span data-stu-id="63304-122">However, the evaluated values do not update the current values.</span></span> <span data-ttu-id="63304-123">Pertanto, se le funzioni [**glVertex**](glvertex-functions.md) sono intercalate con le funzioni **glEvalCoord** , le coordinate di colore, normali e di trama associate alle funzioni **glVertex** non sono interessate dai valori generati dalle funzioni **glEvalCoord** , ma solo dalle funzioni [**glColor**](glcolor-functions.md) [**, glIndex,**](glindex-functions.md) [**glNormal**](glnormal-functions.md)e [**glTexCoord**](gltexcoord-functions.md) più recenti.</span><span class="sxs-lookup"><span data-stu-id="63304-123">Thus, if [**glVertex**](glvertex-functions.md) functions are interspersed with **glEvalCoord** functions, the color, normal, and texture coordinates associated with the **glVertex** functions are not affected by the values generated by the **glEvalCoord** functions, but only by the most recent [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md), and [**glTexCoord**](gltexcoord-functions.md) functions.</span></span>

<span data-ttu-id="63304-124">Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glEvalCoord1d** :</span><span class="sxs-lookup"><span data-stu-id="63304-124">The following functions retrieve information related to the **glEvalCoord1d** function:</span></span>

<span data-ttu-id="63304-125">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="63304-125">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_3</span></span>

<span data-ttu-id="63304-126">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="63304-126">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_4</span></span>

<span data-ttu-id="63304-127">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ index</span><span class="sxs-lookup"><span data-stu-id="63304-127">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_INDEX</span></span>

<span data-ttu-id="63304-128">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ Color \_ 4</span><span class="sxs-lookup"><span data-stu-id="63304-128">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_COLOR\_4</span></span>

<span data-ttu-id="63304-129">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ Normal</span><span class="sxs-lookup"><span data-stu-id="63304-129">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_NORMAL</span></span>

<span data-ttu-id="63304-130">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="63304-130">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="63304-131">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="63304-131">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="63304-132">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 3</span><span class="sxs-lookup"><span data-stu-id="63304-132">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="63304-133">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="63304-133">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="63304-134">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="63304-134">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_3</span></span>

<span data-ttu-id="63304-135">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="63304-135">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_4</span></span>

<span data-ttu-id="63304-136">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ index</span><span class="sxs-lookup"><span data-stu-id="63304-136">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_INDEX</span></span>

<span data-ttu-id="63304-137">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ Color \_ 4</span><span class="sxs-lookup"><span data-stu-id="63304-137">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_COLOR\_4</span></span>

<span data-ttu-id="63304-138">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ Normal</span><span class="sxs-lookup"><span data-stu-id="63304-138">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_NORMAL</span></span>

<span data-ttu-id="63304-139">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ trama \_ Coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="63304-139">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="63304-140">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ trama \_ Coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="63304-140">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="63304-141">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ trama \_ Coord \_ 3</span><span class="sxs-lookup"><span data-stu-id="63304-141">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="63304-142">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ trama \_ Coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="63304-142">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="63304-143">[**glIsEnabled**](glisenabled.md) con argomento GL \_ auto \_ Normal</span><span class="sxs-lookup"><span data-stu-id="63304-143">[**glIsEnabled**](glisenabled.md) with argument GL\_AUTO\_NORMAL</span></span>

## <a name="requirements"></a><span data-ttu-id="63304-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63304-144">Requirements</span></span>



| <span data-ttu-id="63304-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="63304-145">Requirement</span></span> | <span data-ttu-id="63304-146">Valore</span><span class="sxs-lookup"><span data-stu-id="63304-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63304-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63304-147">Minimum supported client</span></span><br/> | <span data-ttu-id="63304-148">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="63304-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="63304-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63304-149">Minimum supported server</span></span><br/> | <span data-ttu-id="63304-150">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="63304-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="63304-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63304-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="63304-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="63304-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="63304-153">Libreria</span><span class="sxs-lookup"><span data-stu-id="63304-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="63304-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63304-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="63304-155">DLL</span><span class="sxs-lookup"><span data-stu-id="63304-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63304-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63304-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63304-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63304-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63304-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="63304-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="63304-159">**glColor**</span><span class="sxs-lookup"><span data-stu-id="63304-159">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="63304-160">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="63304-160">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="63304-161">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="63304-161">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="63304-162">**Remo**</span><span class="sxs-lookup"><span data-stu-id="63304-162">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="63304-163">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="63304-163">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="63304-164">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="63304-164">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="63304-165">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="63304-165">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="63304-166">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="63304-166">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="63304-167">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="63304-167">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="63304-168">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="63304-168">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="63304-169">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="63304-169">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="63304-170">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="63304-170">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> <dt>

[<span data-ttu-id="63304-171">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="63304-171">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="63304-172">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="63304-172">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="63304-173">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="63304-173">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





