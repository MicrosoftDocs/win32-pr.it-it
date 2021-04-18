---
title: funzione glEvalCoord2d (GL. h)
description: La funzione glEvalCoord2d valuta i mapping bidimensionali abilitati.
ms.assetid: 95963abc-841a-4154-92d5-5ae3e6de0f97
keywords:
- funzione glEvalCoord2d OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord2d
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 036e2ee10d1ceac6df6a68a35c1da881d1d478b5
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104552195"
---
# <a name="glevalcoord2d-function"></a><span data-ttu-id="ecf63-104">glEvalCoord2d (funzione)</span><span class="sxs-lookup"><span data-stu-id="ecf63-104">glEvalCoord2d function</span></span>

<span data-ttu-id="ecf63-105">La funzione **glEvalCoord2d** valuta i mapping bidimensionali abilitati.</span><span class="sxs-lookup"><span data-stu-id="ecf63-105">The **glEvalCoord2d** function evaluates enabled two-dimensional maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecf63-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ecf63-106">Syntax</span></span>


```C++
void WINAPI glEvalCoord2d(
   GLdouble u,
   GLdouble v
);
```



## <a name="parameters"></a><span data-ttu-id="ecf63-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ecf63-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecf63-108">*u*</span><span class="sxs-lookup"><span data-stu-id="ecf63-108">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="ecf63-109">Valore che rappresenta la coordinata di dominio *u* per la funzione di base definita in una funzione [**glMap2**](glmap2.md) precedente.</span><span class="sxs-lookup"><span data-stu-id="ecf63-109">A value that is the domain coordinate *u* to the basis function defined in a previous [**glMap2**](glmap2.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="ecf63-110">*v*</span><span class="sxs-lookup"><span data-stu-id="ecf63-110">*v*</span></span> 
</dt> <dd>

<span data-ttu-id="ecf63-111">Valore che rappresenta la coordinata di dominio *v* alla funzione di base definita in una funzione [**glMap2**](glmap2.md) precedente.</span><span class="sxs-lookup"><span data-stu-id="ecf63-111">A value that is the domain coordinate *v* to the basis function defined in a previous [**glMap2**](glmap2.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecf63-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ecf63-112">Return value</span></span>

<span data-ttu-id="ecf63-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ecf63-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecf63-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ecf63-114">Remarks</span></span>

<span data-ttu-id="ecf63-115">La funzione **glEvalCoord2d** valuta le mappe bidimensionali abilitate usando due valori di dominio, *u* e *v*.</span><span class="sxs-lookup"><span data-stu-id="ecf63-115">The **glEvalCoord2d** function evaluates enabled two-dimensional maps using two domain values, *u* and *v*.</span></span> <span data-ttu-id="ecf63-116">Definire Maps con [**glMap1**](glmap1.md) e [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="ecf63-116">Define maps with [**glMap1**](glmap1.md) and [**glMap2**](glmap2.md).</span></span> <span data-ttu-id="ecf63-117">Abilitarli o disabilitarli con [**glEnable**](glenable.md) e [**glDisable**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="ecf63-117">Enable or disable them with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="ecf63-118">Quando viene eseguita una delle funzioni **glEvalCoord** , vengono valutate tutte le mappe attualmente abilitate della dimensione indicata.</span><span class="sxs-lookup"><span data-stu-id="ecf63-118">When one of the **glEvalCoord** functions is issued, all currently enabled maps of the indicated dimension are evaluated.</span></span> <span data-ttu-id="ecf63-119">Quindi, per ogni mappa abilitata, è come se la funzione OpenGL corrispondente venisse eseguita con il valore calcolato.</span><span class="sxs-lookup"><span data-stu-id="ecf63-119">Then, for each enabled map, it is as if the corresponding OpenGL function were issued with the computed value.</span></span> <span data-ttu-id="ecf63-120">Ovvero, se \_ \_ è abilitato l'indice GL MAPPA1 o GL \_ map2 \_ , viene simulata una funzione [**glIndex**](glindex-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="ecf63-120">That is, if GL\_MAP1\_INDEX or GL\_MAP2\_INDEX is enabled, a [**glIndex**](glindex-functions.md) function is simulated.</span></span> <span data-ttu-id="ecf63-121">Se GL \_ Mappa1 \_ Color \_ 4 o GL \_ map2 \_ Color \_ 4 è abilitato, viene simulata una funzione **glcolor** .</span><span class="sxs-lookup"><span data-stu-id="ecf63-121">If GL\_MAP1\_COLOR\_4 or GL\_MAP2\_COLOR\_4 is enabled, a **glcolor** function is simulated.</span></span> <span data-ttu-id="ecf63-122">Se GL \_ Mappa1 \_ Normal o GL \_ map2 \_ Normal è abilitato, viene prodotto un vettore normale e, se è presente una \_ MAPPA1 \_ trama \_ Coord \_ 1, GL \_ Mappa1 \_ trama \_ Coord \_ 2, GL \_ Mappa1 \_ texture \_ Coord \_ 3, GL \_ Mappa1 \_ texture \_ Coord \_ 4, GL \_ map2 \_ texture \_ Coord \_ 1, GL \_ map2 \_ texture \_ Coord \_ 2, GL \_ map2 \_ texture \_ Coord \_ 3 e GL \_ map2 \_ texture \_ Coord \_ 4 è abilitato, viene simulata una funzione [**glTexCoord**](gltexcoord-functions.md) appropriata.</span><span class="sxs-lookup"><span data-stu-id="ecf63-122">If GL\_MAP1\_NORMAL or GL\_MAP2\_NORMAL is enabled, a normal vector is produced, and if any of GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, and GL\_MAP2\_TEXTURE\_COORD\_4 is enabled, then an appropriate [**glTexCoord**](gltexcoord-functions.md) function is simulated.</span></span>

<span data-ttu-id="ecf63-123">OpenGL usa i valori valutati anziché i valori correnti per le valutazioni abilitate e i valori correnti in caso contrario, per le coordinate di colore, indice dei colori, normale e trama.</span><span class="sxs-lookup"><span data-stu-id="ecf63-123">OpenGL uses evaluated values instead of current values for those evaluations that are enabled, and current values otherwise, for color, color index, normal, and texture coordinates.</span></span> <span data-ttu-id="ecf63-124">Tuttavia, i valori valutati non aggiornano i valori correnti.</span><span class="sxs-lookup"><span data-stu-id="ecf63-124">However, the evaluated values do not update the current values.</span></span> <span data-ttu-id="ecf63-125">Pertanto, se le funzioni [**glVertex**](glvertex-functions.md) sono intercalate con le funzioni **glEvalCoord** , le coordinate di colore, normali e di trama associate alle funzioni **glVertex** non sono interessate dai valori generati dalle funzioni **glEvalCoord** , ma solo dalle funzioni [**glColor**](glcolor-functions.md) [**, glIndex,**](glindex-functions.md) [**glNormal**](glnormal-functions.md)e [**glTexCoord**](gltexcoord-functions.md) più recenti.</span><span class="sxs-lookup"><span data-stu-id="ecf63-125">Thus, if [**glVertex**](glvertex-functions.md) functions are interspersed with **glEvalCoord** functions, the color, normal, and texture coordinates associated with the **glVertex** functions are not affected by the values generated by the **glEvalCoord** functions, but only by the most recent [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md), and [**glTexCoord**](gltexcoord-functions.md) functions.</span></span>

<span data-ttu-id="ecf63-126">Se è abilitata la generazione automatica normale, **glEvalCoord2d** chiama [**glEnable**](glenable.md) con argomento GL \_ auto \_ Normal per generare le normalità della superficie in modo analitico, indipendentemente dal contenuto o abilitando la \_ \_ mappa normale GL map2.</span><span class="sxs-lookup"><span data-stu-id="ecf63-126">If automatic normal generation is enabled, **glEvalCoord2d** calls [**glEnable**](glenable.md) with argument GL\_AUTO\_NORMAL to generate surface normals analytically, regardless of the contents or enabling of the GL\_MAP2\_NORMAL map.</span></span> <span data-ttu-id="ecf63-127">Let</span><span class="sxs-lookup"><span data-stu-id="ecf63-127">Let</span></span>

![Equazione che mostra un valore di prodotto incrociato per una mappa m.](images/evlcrd01.png)

<span data-ttu-id="ecf63-129">Il normale **n** generato è</span><span class="sxs-lookup"><span data-stu-id="ecf63-129">The generated normal **n** is</span></span>

![Equazione che mostra la n normale generata per la mappa.](images/evlcrd02.png)

<span data-ttu-id="ecf63-131">Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glEvalCoord2d** :</span><span class="sxs-lookup"><span data-stu-id="ecf63-131">The following functions retrieve information related to the **glEvalCoord2d** function:</span></span>

<span data-ttu-id="ecf63-132">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="ecf63-132">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_3</span></span>

<span data-ttu-id="ecf63-133">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="ecf63-133">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_4</span></span>

<span data-ttu-id="ecf63-134">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ index</span><span class="sxs-lookup"><span data-stu-id="ecf63-134">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_INDEX</span></span>

<span data-ttu-id="ecf63-135">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ Color \_ 4</span><span class="sxs-lookup"><span data-stu-id="ecf63-135">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_COLOR\_4</span></span>

<span data-ttu-id="ecf63-136">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ Normal</span><span class="sxs-lookup"><span data-stu-id="ecf63-136">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_NORMAL</span></span>

<span data-ttu-id="ecf63-137">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="ecf63-137">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="ecf63-138">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="ecf63-138">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="ecf63-139">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 3</span><span class="sxs-lookup"><span data-stu-id="ecf63-139">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="ecf63-140">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="ecf63-140">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="ecf63-141">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="ecf63-141">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_3</span></span>

<span data-ttu-id="ecf63-142">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="ecf63-142">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_4</span></span>

<span data-ttu-id="ecf63-143">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ index</span><span class="sxs-lookup"><span data-stu-id="ecf63-143">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_INDEX</span></span>

<span data-ttu-id="ecf63-144">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ Color \_ 4</span><span class="sxs-lookup"><span data-stu-id="ecf63-144">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_COLOR\_4</span></span>

<span data-ttu-id="ecf63-145">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ Normal</span><span class="sxs-lookup"><span data-stu-id="ecf63-145">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_NORMAL</span></span>

<span data-ttu-id="ecf63-146">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ trama \_ Coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="ecf63-146">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="ecf63-147">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ trama \_ Coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="ecf63-147">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="ecf63-148">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ trama \_ Coord \_ 3</span><span class="sxs-lookup"><span data-stu-id="ecf63-148">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="ecf63-149">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ trama \_ Coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="ecf63-149">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="ecf63-150">[**glIsEnabled**](glisenabled.md) con argomento GL \_ auto \_ Normal</span><span class="sxs-lookup"><span data-stu-id="ecf63-150">[**glIsEnabled**](glisenabled.md) with argument GL\_AUTO\_NORMAL</span></span>

## <a name="requirements"></a><span data-ttu-id="ecf63-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ecf63-151">Requirements</span></span>



| <span data-ttu-id="ecf63-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecf63-152">Requirement</span></span> | <span data-ttu-id="ecf63-153">Valore</span><span class="sxs-lookup"><span data-stu-id="ecf63-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ecf63-154">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecf63-154">Minimum supported client</span></span><br/> | <span data-ttu-id="ecf63-155">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ecf63-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ecf63-156">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ecf63-156">Minimum supported server</span></span><br/> | <span data-ttu-id="ecf63-157">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ecf63-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ecf63-158">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ecf63-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecf63-159"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecf63-159"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ecf63-160">Libreria</span><span class="sxs-lookup"><span data-stu-id="ecf63-160">Library</span></span><br/>                  | <dl> <span data-ttu-id="ecf63-161"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ecf63-161"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ecf63-162">DLL</span><span class="sxs-lookup"><span data-stu-id="ecf63-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecf63-163"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecf63-163"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecf63-164">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ecf63-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecf63-165">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ecf63-165">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ecf63-166">**glColor**</span><span class="sxs-lookup"><span data-stu-id="ecf63-166">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="ecf63-167">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="ecf63-167">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="ecf63-168">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="ecf63-168">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="ecf63-169">**Remo**</span><span class="sxs-lookup"><span data-stu-id="ecf63-169">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ecf63-170">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="ecf63-170">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="ecf63-171">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="ecf63-171">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="ecf63-172">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="ecf63-172">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="ecf63-173">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="ecf63-173">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="ecf63-174">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="ecf63-174">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="ecf63-175">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="ecf63-175">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="ecf63-176">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="ecf63-176">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="ecf63-177">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="ecf63-177">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> <dt>

[<span data-ttu-id="ecf63-178">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="ecf63-178">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="ecf63-179">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="ecf63-179">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="ecf63-180">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="ecf63-180">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





