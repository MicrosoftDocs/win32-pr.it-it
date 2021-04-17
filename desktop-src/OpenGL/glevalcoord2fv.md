---
title: funzione glEvalCoord2fv (GL. h)
description: La funzione glEvalCoord2fv valuta i mapping bidimensionali abilitati.
ms.assetid: fff786b4-a9e1-4f3e-a62e-36e89bc9c35d
keywords:
- funzione glEvalCoord2fv OpenGL
topic_type:
- apiref
api_name:
- glEvalCoord2fv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e277b0b71361588f8a9835ec3b8891b49f9482a
ms.sourcegitcommit: 7ef31bf778e76ce4196205d4c4c632fbdc649805
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104568024"
---
# <a name="glevalcoord2fv-function"></a><span data-ttu-id="62f67-104">glEvalCoord2fv (funzione)</span><span class="sxs-lookup"><span data-stu-id="62f67-104">glEvalCoord2fv function</span></span>

<span data-ttu-id="62f67-105">La funzione **glEvalCoord2fv** valuta i mapping bidimensionali abilitati.</span><span class="sxs-lookup"><span data-stu-id="62f67-105">The **glEvalCoord2fv** function evaluates enabled two-dimensional maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="62f67-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62f67-106">Syntax</span></span>


```C++
void WINAPI glEvalCoord2fv(
   const GLfloat *u
);
```



## <a name="parameters"></a><span data-ttu-id="62f67-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="62f67-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62f67-108">*u*</span><span class="sxs-lookup"><span data-stu-id="62f67-108">*u*</span></span> 
</dt> <dd>

<span data-ttu-id="62f67-109">Puntatore a una matrice che contiene la coordinata di dominio *u*.</span><span class="sxs-lookup"><span data-stu-id="62f67-109">A pointer to an array containing the domain coordinate *u*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62f67-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62f67-110">Return value</span></span>

<span data-ttu-id="62f67-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="62f67-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62f67-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="62f67-112">Remarks</span></span>

<span data-ttu-id="62f67-113">La funzione **glEvalCoord2fv** valuta le mappe bidimensionali abilitate usando due valori di dominio, *u* e *v*.</span><span class="sxs-lookup"><span data-stu-id="62f67-113">The **glEvalCoord2fv** function evaluates enabled two-dimensional maps using two domain values, *u* and *v*.</span></span> <span data-ttu-id="62f67-114">Definire Maps con [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="62f67-114">Define maps with [**glMap1**](glmap1.md).</span></span> <span data-ttu-id="62f67-115">Abilitarli o disabilitarli con [**glEnable**](glenable.md) e [**glDisable**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="62f67-115">Enable or disable them with [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="62f67-116">Quando viene eseguita una delle funzioni **glEvalCoord** , vengono valutate tutte le mappe attualmente abilitate della dimensione indicata.</span><span class="sxs-lookup"><span data-stu-id="62f67-116">When one of the **glEvalCoord** functions is issued, all currently enabled maps of the indicated dimension are evaluated.</span></span> <span data-ttu-id="62f67-117">Quindi, per ogni mappa abilitata, è come se la funzione OpenGL corrispondente venisse eseguita con il valore calcolato.</span><span class="sxs-lookup"><span data-stu-id="62f67-117">Then, for each enabled map, it is as if the corresponding OpenGL function were issued with the computed value.</span></span> <span data-ttu-id="62f67-118">Ovvero, se \_ \_ è abilitato l'indice GL MAPPA1 o GL \_ map2 \_ , viene simulata una funzione [**glIndex**](glindex-functions.md) .</span><span class="sxs-lookup"><span data-stu-id="62f67-118">That is, if GL\_MAP1\_INDEX or GL\_MAP2\_INDEX is enabled, a [**glIndex**](glindex-functions.md) function is simulated.</span></span> <span data-ttu-id="62f67-119">Se GL \_ Mappa1 \_ Color \_ 4 o GL \_ map2 \_ Color \_ 4 è abilitato, viene simulata una funzione **glcolor** .</span><span class="sxs-lookup"><span data-stu-id="62f67-119">If GL\_MAP1\_COLOR\_4 or GL\_MAP2\_COLOR\_4 is enabled, a **glcolor** function is simulated.</span></span> <span data-ttu-id="62f67-120">Se GL \_ Mappa1 \_ Normal o GL \_ map2 \_ Normal è abilitato, viene prodotto un vettore normale e, se è presente una \_ MAPPA1 \_ trama \_ Coord \_ 1, GL \_ Mappa1 \_ trama \_ Coord \_ 2, GL \_ Mappa1 \_ texture \_ Coord \_ 3, GL \_ Mappa1 \_ texture \_ Coord \_ 4, GL \_ map2 \_ texture \_ Coord \_ 1, GL \_ map2 \_ texture \_ Coord \_ 2, GL \_ map2 \_ texture \_ Coord \_ 3 e GL \_ map2 \_ texture \_ Coord \_ 4 è abilitato, viene simulata una funzione [**glTexCoord**](gltexcoord-functions.md) appropriata.</span><span class="sxs-lookup"><span data-stu-id="62f67-120">If GL\_MAP1\_NORMAL or GL\_MAP2\_NORMAL is enabled, a normal vector is produced, and if any of GL\_MAP1\_TEXTURE\_COORD\_1, GL\_MAP1\_TEXTURE\_COORD\_2, GL\_MAP1\_TEXTURE\_COORD\_3, GL\_MAP1\_TEXTURE\_COORD\_4, GL\_MAP2\_TEXTURE\_COORD\_1, GL\_MAP2\_TEXTURE\_COORD\_2, GL\_MAP2\_TEXTURE\_COORD\_3, and GL\_MAP2\_TEXTURE\_COORD\_4 is enabled, then an appropriate [**glTexCoord**](gltexcoord-functions.md) function is simulated.</span></span>

<span data-ttu-id="62f67-121">OpenGL usa i valori valutati anziché i valori correnti per le valutazioni abilitate e i valori correnti in caso contrario, per le coordinate di colore, indice dei colori, normale e trama.</span><span class="sxs-lookup"><span data-stu-id="62f67-121">OpenGL uses evaluated values instead of current values for those evaluations that are enabled, and current values otherwise, for color, color index, normal, and texture coordinates.</span></span> <span data-ttu-id="62f67-122">Tuttavia, i valori valutati non aggiornano i valori correnti.</span><span class="sxs-lookup"><span data-stu-id="62f67-122">However, the evaluated values do not update the current values.</span></span> <span data-ttu-id="62f67-123">Pertanto, se le funzioni [**glVertex**](glvertex-functions.md) sono intercalate con le funzioni **glEvalCoord** , le coordinate di colore, normali e di trama associate alle funzioni **glVertex** non sono interessate dai valori generati dalle funzioni **glEvalCoord** , ma solo dalle funzioni [**glColor**](glcolor-functions.md) [**, glIndex,**](glindex-functions.md) [**glNormal**](glnormal-functions.md)e [**glTexCoord**](gltexcoord-functions.md) più recenti.</span><span class="sxs-lookup"><span data-stu-id="62f67-123">Thus, if [**glVertex**](glvertex-functions.md) functions are interspersed with **glEvalCoord** functions, the color, normal, and texture coordinates associated with the **glVertex** functions are not affected by the values generated by the **glEvalCoord** functions, but only by the most recent [**glColor**](glcolor-functions.md), [**glIndex**](glindex-functions.md), [**glNormal**](glnormal-functions.md), and [**glTexCoord**](gltexcoord-functions.md) functions.</span></span>

<span data-ttu-id="62f67-124">Se è abilitata la generazione automatica normale, **glEvalCoord2fv** chiama [**glEnable**](glenable.md) con argomento GL \_ auto \_ Normal per generare le normalità della superficie in modo analitico, indipendentemente dal contenuto o abilitando la \_ \_ mappa normale GL map2.</span><span class="sxs-lookup"><span data-stu-id="62f67-124">If automatic normal generation is enabled, **glEvalCoord2fv** calls [**glEnable**](glenable.md) with argument GL\_AUTO\_NORMAL to generate surface normals analytically, regardless of the contents or enabling of the GL\_MAP2\_NORMAL map.</span></span> <span data-ttu-id="62f67-125">Let</span><span class="sxs-lookup"><span data-stu-id="62f67-125">Let</span></span>

![Equazione che mostra un valore di prodotto incrociato per una mappa m.](images/evlcrd01.png)

<span data-ttu-id="62f67-127">Il normale **n** generato è</span><span class="sxs-lookup"><span data-stu-id="62f67-127">The generated normal **n** is</span></span>

![Equazione che mostra la n normale generata per la mappa.](images/evlcrd02.png)

<span data-ttu-id="62f67-129">Le funzioni seguenti consentono di recuperare informazioni correlate alla funzione **glEvalCoord2fv** :</span><span class="sxs-lookup"><span data-stu-id="62f67-129">The following functions retrieve information related to the **glEvalCoord2fv** function:</span></span>

<span data-ttu-id="62f67-130">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="62f67-130">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_3</span></span>

<span data-ttu-id="62f67-131">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="62f67-131">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_VERTEX\_4</span></span>

<span data-ttu-id="62f67-132">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ index</span><span class="sxs-lookup"><span data-stu-id="62f67-132">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_INDEX</span></span>

<span data-ttu-id="62f67-133">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ Color \_ 4</span><span class="sxs-lookup"><span data-stu-id="62f67-133">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_COLOR\_4</span></span>

<span data-ttu-id="62f67-134">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ Normal</span><span class="sxs-lookup"><span data-stu-id="62f67-134">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_NORMAL</span></span>

<span data-ttu-id="62f67-135">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="62f67-135">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="62f67-136">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="62f67-136">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="62f67-137">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 3</span><span class="sxs-lookup"><span data-stu-id="62f67-137">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="62f67-138">[**glIsEnabled**](glisenabled.md) con argomento GL \_ Mappa1 \_ trama \_ Coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="62f67-138">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP1\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="62f67-139">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="62f67-139">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_3</span></span>

<span data-ttu-id="62f67-140">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ Vertex \_ 4</span><span class="sxs-lookup"><span data-stu-id="62f67-140">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_VERTEX\_4</span></span>

<span data-ttu-id="62f67-141">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ index</span><span class="sxs-lookup"><span data-stu-id="62f67-141">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_INDEX</span></span>

<span data-ttu-id="62f67-142">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ Color \_ 4</span><span class="sxs-lookup"><span data-stu-id="62f67-142">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_COLOR\_4</span></span>

<span data-ttu-id="62f67-143">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ Normal</span><span class="sxs-lookup"><span data-stu-id="62f67-143">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_NORMAL</span></span>

<span data-ttu-id="62f67-144">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ trama \_ Coord \_ 1</span><span class="sxs-lookup"><span data-stu-id="62f67-144">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_1</span></span>

<span data-ttu-id="62f67-145">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ trama \_ Coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="62f67-145">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_2</span></span>

<span data-ttu-id="62f67-146">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ trama \_ Coord \_ 3</span><span class="sxs-lookup"><span data-stu-id="62f67-146">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_3</span></span>

<span data-ttu-id="62f67-147">[**glIsEnabled**](glisenabled.md) con argomento GL \_ map2 \_ trama \_ Coord \_ 4</span><span class="sxs-lookup"><span data-stu-id="62f67-147">[**glIsEnabled**](glisenabled.md) with argument GL\_MAP2\_TEXTURE\_COORD\_4</span></span>

<span data-ttu-id="62f67-148">[**glIsEnabled**](glisenabled.md) con argomento GL \_ auto \_ Normal</span><span class="sxs-lookup"><span data-stu-id="62f67-148">[**glIsEnabled**](glisenabled.md) with argument GL\_AUTO\_NORMAL</span></span>

## <a name="requirements"></a><span data-ttu-id="62f67-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62f67-149">Requirements</span></span>



| <span data-ttu-id="62f67-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="62f67-150">Requirement</span></span> | <span data-ttu-id="62f67-151">Valore</span><span class="sxs-lookup"><span data-stu-id="62f67-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62f67-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62f67-152">Minimum supported client</span></span><br/> | <span data-ttu-id="62f67-153">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="62f67-153">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="62f67-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="62f67-154">Minimum supported server</span></span><br/> | <span data-ttu-id="62f67-155">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="62f67-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="62f67-156">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62f67-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="62f67-157"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="62f67-157"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="62f67-158">Libreria</span><span class="sxs-lookup"><span data-stu-id="62f67-158">Library</span></span><br/>                  | <dl> <span data-ttu-id="62f67-159"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62f67-159"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="62f67-160">DLL</span><span class="sxs-lookup"><span data-stu-id="62f67-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62f67-161"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62f67-161"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62f67-162">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62f67-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62f67-163">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="62f67-163">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="62f67-164">**glColor**</span><span class="sxs-lookup"><span data-stu-id="62f67-164">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="62f67-165">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="62f67-165">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="62f67-166">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="62f67-166">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="62f67-167">**Remo**</span><span class="sxs-lookup"><span data-stu-id="62f67-167">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="62f67-168">**glEvalMesh**</span><span class="sxs-lookup"><span data-stu-id="62f67-168">**glEvalMesh**</span></span>](glevalmesh-functions.md)
</dt> <dt>

[<span data-ttu-id="62f67-169">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="62f67-169">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="62f67-170">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="62f67-170">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="62f67-171">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="62f67-171">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="62f67-172">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="62f67-172">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="62f67-173">**glMap1**</span><span class="sxs-lookup"><span data-stu-id="62f67-173">**glMap1**</span></span>](glmap1.md)
</dt> <dt>

[<span data-ttu-id="62f67-174">**glMap2**</span><span class="sxs-lookup"><span data-stu-id="62f67-174">**glMap2**</span></span>](glmap2.md)
</dt> <dt>

[<span data-ttu-id="62f67-175">**glMapGrid**</span><span class="sxs-lookup"><span data-stu-id="62f67-175">**glMapGrid**</span></span>](glmapgrid-functions.md)
</dt> <dt>

[<span data-ttu-id="62f67-176">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="62f67-176">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="62f67-177">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="62f67-177">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="62f67-178">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="62f67-178">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

 





