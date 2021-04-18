---
title: funzione glEvalCoord1fv (GL. h)
description: La funzione glEvalCoord1fv valuta i mapping unidimensionali abilitati.
ms.assetid: d5c1cc99-ecf6-4d78-99bb-953b4c362ff4
keywords:
- funzione glEvalCoord1fv OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord1fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9acb1f7060367b02fa836fb149151b8278b7274
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301922"
---
# <a name="glevalcoord1fv-function"></a><span data-ttu-id="0c09d-104">glEvalCoord1fv (funzione)</span><span class="sxs-lookup"><span data-stu-id="0c09d-104">glEvalCoord1fv function</span></span>

<span data-ttu-id="0c09d-105">La funzione **glEvalCoord1fv** valuta i mapping unidimensionali abilitati.</span><span class="sxs-lookup"><span data-stu-id="0c09d-105">The **glEvalCoord1fv** function evaluates enabled one-dimensional maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c09d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c09d-106">Syntax</span></span>


```C++
void WINAPI glEvalCoord1fv(
   const GLfloat *u
);
```



## <a name="parameters"></a><span data-ttu-id="0c09d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="0c09d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c09d-108">*u*</span><span class="sxs-lookup"><span data-stu-id="0c09d-108">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="0c09d-109">Puntatore a una matrice che contiene la coordinata di dominio *u*.</span><span class="sxs-lookup"><span data-stu-id="0c09d-109">A pointer to an array containing the domain coordinate *u*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c09d-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0c09d-110">Return value</span></span>

<span data-ttu-id="0c09d-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="0c09d-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c09d-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c09d-112">Remarks</span></span>

<span data-ttu-id="0c09d-113">La funzione [**glEvalCoord1fv**](glevalcoord1dv.md) valuta le mappe unidimensionali abilitate all'argomento *u*.</span><span class="sxs-lookup"><span data-stu-id="0c09d-113">The [**glEvalCoord1fv**](glevalcoord1dv.md) function evaluates enabled one-dimensional maps at argument *u*.</span></span> <span data-ttu-id="0c09d-114">Definire Maps con [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="0c09d-114">Define maps with [**glMap1**](glmap1.md).</span></span> <span data-ttu-id="0c09d-115">Abilitarli o disabilitarli con [**glEnable**](glenable.md) e [**glDisable**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="0c09d-115">Enable or disable them with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="0c09d-116">Quando viene eseguita una delle funzioni **glEvalCoord** , vengono valutate tutte le mappe attualmente abilitate della dimensione indicata.</span><span class="sxs-lookup"><span data-stu-id="0c09d-116">When one of the **glEvalCoord** functions is issued, all currently enabled maps of the indicated dimension are evaluated.</span></span> <span data-ttu-id="0c09d-117">Quindi, per ogni mappa abilitata, è come se la funzione OpenGL corrispondente venisse eseguita con il valore calcolato.</span><span class="sxs-lookup"><span data-stu-id="0c09d-117">Then, for each enabled map, it is as if the corresponding OpenGL function were issued with the computed value.</span></span> <span data-ttu-id="0c09d-118">Ovvero, se \_ \_ è abilitato l'indice GL MAPPA1 o GL \_ map2 \_ , viene simulata una funzione [**glIndex**](glindex-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="0c09d-118">That is, if GL\_MAP1\_INDEX or GL\_MAP2\_INDEX is enabled, a [**glIndex**](glindex-functions.md) function is simulated.</span></span> <span data-ttu-id="0c09d-119">Se GL \_ Mappa1 \_ Color \_ 4 o GL \_ map2 \_ Color \_ 4 è abilitato, viene simulata una funzione **glcolor** .</span><span class="sxs-lookup"><span data-stu-id="0c09d-119">If GL\_MAP1\_COLOR\_4 or GL\_MAP2\_COLOR\_4 is enabled, a **glcolor** function is simulated.</span></span> <span data-ttu-id="0c09d-120">Se GL \_ Mappa1 \_ Normal o GL \_ map2 \_ Normal è abilitato, viene prodotto un vettore normale e, se è presente una \_ MAPPA1 \_ trama \_ Coord \_ 1, GL \_ Mappa1 \_ trama \_ Coord \_ 2, GL \_ Mappa1 \_ texture \_ Coord \_ 3, GL \_ Mappa1 \_ texture \_ Coord \_ 4, GL \_ map2 \_ texture \_ Coord \_ 1, GL \_ map2 \_ texture \_ Coord \_ 2, GL \_ map2 \_ texture \_ Coord \_ 3 e GL \_ map2 \_ texture \_ Coord \_ 4 è abilitato, viene simulata una funzione [**glTexCoord**](gltexcoord-functions.md) appropriata.</span><span class="sxs-lookup"><span data-stu-id="0c09d-120">If GL\_MAP1\_NORMAL or GL\_MAP2\_NORMAL is enabled, a normal vector is produced, and if any of GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, and GL\_MAP2\_TEXTURE\_COORD\_4 is enabled, then an appropriate [**glTexCoord**](gltexcoord-functions.md) function is simulated.</span></span>

<span data-ttu-id="0c09d-121">OpenGL usa i valori valutati anziché i valori correnti per le valutazioni abilitate e i valori correnti in caso contrario, per le coordinate di colore, indice dei colori, normale e trama.</span><span class="sxs-lookup"><span data-stu-id="0c09d-121">OpenGL uses evaluated values instead of current values for those evaluations that are enabled, and current values otherwise, for color, color index, normal, and texture coordinates.</span></span> <span data-ttu-id="0c09d-122">Tuttavia, i valori valutati non aggiornano i valori correnti.</span><span class="sxs-lookup"><span data-stu-id="0c09d-122">However, the evaluated values do not update the current values.</span></span> <span data-ttu-id="0c09d-123">Pertanto, se le funzioni [**glVertex**](glvertex-functions.md) sono intercalate con le funzioni **glEvalCoord** , le coordinate di colore, normali e di trama associate alle funzioni **glVertex** non sono interessate dai valori generati dalle funzioni **glEvalCoord** , ma solo dalle funzioni [**glColor**](glcolor-functions.md) [**, glIndex,**](glindex-functions.md) [**glNormal**](glnormal-functions.md)e [**glTexCoord**](gltexcoord-functions.md) più recenti.</span><span class="sxs-lookup"><span data-stu-id="0c09d-123">Thus, if [**glVertex**](glvertex-functions.md) functions are interspersed with **glEvalCoord** functions, the color, normal, and texture coordinates associated with the **glVertex** functions are not affected by the values generated by the **glEvalCoord** functions, but only by the most recent [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md), and [**glTexCoord**](gltexcoord-functions.md) functions.</span></span>

<span data-ttu-id="0c09d-124">Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glEvalCoord1fv** :</span><span class="sxs-lookup"><span data-stu-id="0c09d-124">The following functions retrieve information related to the **glEvalCoord1fv** function:</span></span>

<span data-ttu-id="0c09d-125">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="0c09d-125">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_3</span></span>

<span data-ttu-id="0c09d-126">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="0c09d-126">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_4</span></span>

<span data-ttu-id="0c09d-127">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ index</span><span class="sxs-lookup"><span data-stu-id="0c09d-127">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_INDEX</span></span>

<span data-ttu-id="0c09d-128">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ Color \_ 4</span><span class="sxs-lookup"><span data-stu-id="0c09d-128">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_COLOR\_4</span></span>

<span data-ttu-id="0c09d-129">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ Normal</span><span class="sxs-lookup"><span data-stu-id="0c09d-129">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_NORMAL</span></span>

<span data-ttu-id="0c09d-130">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="0c09d-130">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="0c09d-131">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="0c09d-131">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="0c09d-132">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 3</span><span class="sxs-lookup"><span data-stu-id="0c09d-132">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="0c09d-133">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="0c09d-133">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="0c09d-134">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="0c09d-134">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_3</span></span>

<span data-ttu-id="0c09d-135">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="0c09d-135">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_4</span></span>

<span data-ttu-id="0c09d-136">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ index</span><span class="sxs-lookup"><span data-stu-id="0c09d-136">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_INDEX</span></span>

<span data-ttu-id="0c09d-137">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ Color \_ 4</span><span class="sxs-lookup"><span data-stu-id="0c09d-137">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_COLOR\_4</span></span>

<span data-ttu-id="0c09d-138">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ Normal</span><span class="sxs-lookup"><span data-stu-id="0c09d-138">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_NORMAL</span></span>

<span data-ttu-id="0c09d-139">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ trama \_ Coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="0c09d-139">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="0c09d-140">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ trama \_ Coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="0c09d-140">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="0c09d-141">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ trama \_ Coord \_ 3</span><span class="sxs-lookup"><span data-stu-id="0c09d-141">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="0c09d-142">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ trama \_ Coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="0c09d-142">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="0c09d-143">[**glIsEnabled**](glisenabled.md) con argomento GL \_ auto \_ Normal</span><span class="sxs-lookup"><span data-stu-id="0c09d-143">[**glIsEnabled**](glisenabled.md) with argument GL\_AUTO\_NORMAL</span></span>

## <a name="requirements"></a><span data-ttu-id="0c09d-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c09d-144">Requirements</span></span>



| <span data-ttu-id="0c09d-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c09d-145">Requirement</span></span> | <span data-ttu-id="0c09d-146">Valore</span><span class="sxs-lookup"><span data-stu-id="0c09d-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c09d-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c09d-147">Minimum supported client</span></span><br/> | <span data-ttu-id="0c09d-148">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0c09d-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0c09d-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c09d-149">Minimum supported server</span></span><br/> | <span data-ttu-id="0c09d-150">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0c09d-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0c09d-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c09d-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c09d-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c09d-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="0c09d-153">Libreria</span><span class="sxs-lookup"><span data-stu-id="0c09d-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="0c09d-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c09d-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="0c09d-155">DLL</span><span class="sxs-lookup"><span data-stu-id="0c09d-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c09d-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c09d-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c09d-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c09d-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c09d-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="0c09d-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="0c09d-159">**glColor**</span><span class="sxs-lookup"><span data-stu-id="0c09d-159">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="0c09d-160">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="0c09d-160">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="0c09d-161">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="0c09d-161">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="0c09d-162">**Remo**</span><span class="sxs-lookup"><span data-stu-id="0c09d-162">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="0c09d-163">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="0c09d-163">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="0c09d-164">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="0c09d-164">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="0c09d-165">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="0c09d-165">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="0c09d-166">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="0c09d-166">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="0c09d-167">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="0c09d-167">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="0c09d-168">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="0c09d-168">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="0c09d-169">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="0c09d-169">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="0c09d-170">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="0c09d-170">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> <dt>

[<span data-ttu-id="0c09d-171">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="0c09d-171">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="0c09d-172">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="0c09d-172">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="0c09d-173">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="0c09d-173">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





