---
title: funzione glEnd (GL. h)
description: Le funzioni glBegin e glEnd delimitano i vertici di una primitiva o di un gruppo di primitive like. | funzione glEnd (GL. h)
ms.assetid: 040f8573-683c-4a8a-ae51-66abb0541ac4
keywords:
- funzione glEnd OpenGL
topic_type:
- apiref
api_name:
- glEnd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9bb41395b3ed2e38a64094506e07e2a69ad1d52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321343"
---
# <a name="glend-function"></a><span data-ttu-id="a73c7-105">funzione glEnd</span><span class="sxs-lookup"><span data-stu-id="a73c7-105">glEnd function</span></span>

<span data-ttu-id="a73c7-106">Le funzioni [**glBegin**](glbegin.md) e **glEnd** delimitano i vertici di una primitiva o di un gruppo di primitive like.</span><span class="sxs-lookup"><span data-stu-id="a73c7-106">The [**glBegin**](glbegin.md) and **glend** functions delimit the vertices of a primitive or a group of like primitives.</span></span>

## <a name="syntax"></a><span data-ttu-id="a73c7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a73c7-107">Syntax</span></span>


```C++
void WINAPI glEnd(void);
```



## <a name="parameters"></a><span data-ttu-id="a73c7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a73c7-108">Parameters</span></span>

<span data-ttu-id="a73c7-109">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="a73c7-109">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a73c7-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a73c7-110">Return value</span></span>

<span data-ttu-id="a73c7-111">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="a73c7-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a73c7-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="a73c7-112">Error codes</span></span>

<span data-ttu-id="a73c7-113">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="a73c7-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a73c7-114">Nome</span><span class="sxs-lookup"><span data-stu-id="a73c7-114">Name</span></span>                                                                                                  | <span data-ttu-id="a73c7-115">Significato</span><span class="sxs-lookup"><span data-stu-id="a73c7-115">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a73c7-116"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a73c7-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a73c7-117">Una funzione diversa da **glVertex**, **glColor**, **glIndex**, **glNormal**, **glTexCoord**, **glEvalCoord**, **GlEvalPoint**, **GlMaterial**, **glEdgeFlag**, **glCallList** o **glCallLists** è stata chiamata tra **glBegin** e l'oggetto **glEnd** corrispondente.</span><span class="sxs-lookup"><span data-stu-id="a73c7-117">A function other than **glVertex**, **glColor**, **glIndex**, **glNormal**, **glTexCoord**, **glEvalCoord**, **glEvalPoint**, **glMaterial**, **glEdgeFlag**, **glCallList**, or **glCallLists** was called between **glBegin** and the corresponding **glEnd**.</span></span> <span data-ttu-id="a73c7-118">La funzione **glEnd** è stata chiamata prima della chiamata del **glBegin** corrispondente oppure **glBegin** è stato chiamato all'interno di una sequenza **glBegin** / **glEnd** .</span><span class="sxs-lookup"><span data-stu-id="a73c7-118">The function **glEnd** was called before the corresponding **glBegin** was called, or **glBegin** was called within a **glBegin**/**glEnd** sequence.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="a73c7-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="a73c7-119">Remarks</span></span>

<span data-ttu-id="a73c7-120">Le funzioni [**glBegin**](glbegin.md) e **glEnd** delimitano i vertici che definiscono una primitiva o un gruppo di primitive like.</span><span class="sxs-lookup"><span data-stu-id="a73c7-120">The [**glBegin**](glbegin.md) and **glend** functions delimit the vertices that define a primitive or a group of like primitives.</span></span> <span data-ttu-id="a73c7-121">La funzione **glBegin** accetta un solo argomento che specifica quale delle dieci primitive i vertici compongono.</span><span class="sxs-lookup"><span data-stu-id="a73c7-121">The **glBegin** function accepts a single argument that specifies which of ten primitives the vertices compose.</span></span> <span data-ttu-id="a73c7-122">Accettando *n* come numero intero a partire da uno e *n* come numero totale di vertici specificati, le interpretazioni sono le seguenti:</span><span class="sxs-lookup"><span data-stu-id="a73c7-122">Taking *n* as an integer count starting at one, and *N* as the total number of vertices specified, the interpretations are as follows:</span></span>

-   <span data-ttu-id="a73c7-123">È possibile usare solo un subset di funzioni OpenGL tra **glBegin** e **glEnd**.</span><span class="sxs-lookup"><span data-stu-id="a73c7-123">You can use only a subset of OpenGL functions between **glBegin** and **glEnd**.</span></span> <span data-ttu-id="a73c7-124">Le funzioni che è possibile usare sono:</span><span class="sxs-lookup"><span data-stu-id="a73c7-124">The functions you can use are:</span></span>

    -   [<span data-ttu-id="a73c7-125">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="a73c7-125">**glVertex**</span></span>](glvertex-functions.md)
    -   [<span data-ttu-id="a73c7-126">**glColor**</span><span class="sxs-lookup"><span data-stu-id="a73c7-126">**glColor**</span></span>](glcolor-functions.md)
    -   [<span data-ttu-id="a73c7-127">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="a73c7-127">**glIndex**</span></span>](glindex-functions.md)
    -   [<span data-ttu-id="a73c7-128">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="a73c7-128">**glNormal**</span></span>](glnormal-functions.md)
    -   [<span data-ttu-id="a73c7-129">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="a73c7-129">**glTexCoord**</span></span>](gltexcoord-functions.md)
    -   [<span data-ttu-id="a73c7-130">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="a73c7-130">**glEvalCoord**</span></span>](glevalcoord-functions.md)
    -   [<span data-ttu-id="a73c7-131">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="a73c7-131">**glEvalPoint**</span></span>](glevalpoint.md)
    -   [<span data-ttu-id="a73c7-132">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="a73c7-132">**glMaterial**</span></span>](glmaterial-functions.md)
    -   [<span data-ttu-id="a73c7-133">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="a73c7-133">**glEdgeFlag**</span></span>](gledgeflag-functions.md)

    <span data-ttu-id="a73c7-134">È anche possibile usare [**glCallList**](glcalllist.md) o [**glCallLists**](glcalllists.md) per eseguire gli elenchi di visualizzazione che includono solo le funzioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="a73c7-134">You can also use [**glCallList**](glcalllist.md) or [**glCallLists**](glcalllists.md) to execute display lists that include only the preceding functions.</span></span> <span data-ttu-id="a73c7-135">Se viene chiamata una qualsiasi altra funzione OpenGL tra **glBegin** e **glEnd**, viene impostato il flag di errore e la funzione viene ignorata.</span><span class="sxs-lookup"><span data-stu-id="a73c7-135">If any other OpenGL function is called between **glBegin** and **glEnd**, the error flag is set and the function is ignored.</span></span>

-   <span data-ttu-id="a73c7-136">Indipendentemente dal valore scelto per la *modalità* in **glBegin**, non esiste alcun limite al numero di vertici che è possibile definire tra **glBegin** e **glEnd**.</span><span class="sxs-lookup"><span data-stu-id="a73c7-136">Regardless of the value chosen for *mode* in **glBegin**, there is no limit to the number of vertices you can define between **glBegin** and **glEnd**.</span></span> <span data-ttu-id="a73c7-137">Le linee, i triangoli, i quadrilateri e i poligoni specificati in un punto non completo non vengono disegnati.</span><span class="sxs-lookup"><span data-stu-id="a73c7-137">Lines, triangles, quadrilaterals, and polygons that are incompletely specified are not drawn.</span></span> <span data-ttu-id="a73c7-138">Risultati di specifica incompleti quando vengono forniti un numero troppo basso di vertici per specificare anche una singola primitiva o quando viene specificato un multiplo errato di vertici.</span><span class="sxs-lookup"><span data-stu-id="a73c7-138">Incomplete specification results when either too few vertices are provided to specify even a single primitive or when an incorrect multiple of vertices is specified.</span></span> <span data-ttu-id="a73c7-139">La primitiva incompleta viene ignorata; vengono disegnate le primitive complete.</span><span class="sxs-lookup"><span data-stu-id="a73c7-139">The incomplete primitive is ignored; the complete primitives are drawn.</span></span>
-   <span data-ttu-id="a73c7-140">La specifica minima dei vertici per ogni primitiva è la seguente:</span><span class="sxs-lookup"><span data-stu-id="a73c7-140">The minimum specification of vertices for each primitive is:</span></span> 

    | <span data-ttu-id="a73c7-141">Numero minimo di vertici</span><span class="sxs-lookup"><span data-stu-id="a73c7-141">Minimum number of vertices</span></span> | <span data-ttu-id="a73c7-142">Tipo di primitiva</span><span class="sxs-lookup"><span data-stu-id="a73c7-142">Type of primitive</span></span> |
    |----------------------------|-------------------|
    | <span data-ttu-id="a73c7-143">1</span><span class="sxs-lookup"><span data-stu-id="a73c7-143">1</span></span>                          | <span data-ttu-id="a73c7-144">point</span><span class="sxs-lookup"><span data-stu-id="a73c7-144">point</span></span>             |
    | <span data-ttu-id="a73c7-145">2</span><span class="sxs-lookup"><span data-stu-id="a73c7-145">2</span></span>                          | <span data-ttu-id="a73c7-146">line</span><span class="sxs-lookup"><span data-stu-id="a73c7-146">line</span></span>              |
    | <span data-ttu-id="a73c7-147">3</span><span class="sxs-lookup"><span data-stu-id="a73c7-147">3</span></span>                          | <span data-ttu-id="a73c7-148">triangolo</span><span class="sxs-lookup"><span data-stu-id="a73c7-148">triangle</span></span>          |
    | <span data-ttu-id="a73c7-149">4</span><span class="sxs-lookup"><span data-stu-id="a73c7-149">4</span></span>                          | <span data-ttu-id="a73c7-150">Quadrilatero</span><span class="sxs-lookup"><span data-stu-id="a73c7-150">quadrilateral</span></span>     |
    | <span data-ttu-id="a73c7-151">3</span><span class="sxs-lookup"><span data-stu-id="a73c7-151">3</span></span>                          | <span data-ttu-id="a73c7-152">polygon</span><span class="sxs-lookup"><span data-stu-id="a73c7-152">polygon</span></span>           |

    

     

-   <span data-ttu-id="a73c7-153">Le modalità che richiedono un determinato multiplo di vertici sono GL \_ Lines (2), GL \_ triangoli (3), GL \_ quad (4) e GL \_ Quad \_ Strip (2).</span><span class="sxs-lookup"><span data-stu-id="a73c7-153">Modes that require a certain multiple of vertices are GL\_LINES (2), GL\_TRIANGLES (3), GL\_QUADS (4), and GL\_QUAD\_STRIP (2).</span></span>

## <a name="requirements"></a><span data-ttu-id="a73c7-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a73c7-154">Requirements</span></span>



| <span data-ttu-id="a73c7-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="a73c7-155">Requirement</span></span> | <span data-ttu-id="a73c7-156">Valore</span><span class="sxs-lookup"><span data-stu-id="a73c7-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a73c7-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a73c7-157">Minimum supported client</span></span><br/> | <span data-ttu-id="a73c7-158">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a73c7-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a73c7-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a73c7-159">Minimum supported server</span></span><br/> | <span data-ttu-id="a73c7-160">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a73c7-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a73c7-161">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a73c7-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="a73c7-162"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a73c7-162"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a73c7-163">Libreria</span><span class="sxs-lookup"><span data-stu-id="a73c7-163">Library</span></span><br/>                  | <dl> <span data-ttu-id="a73c7-164"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a73c7-164"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a73c7-165">DLL</span><span class="sxs-lookup"><span data-stu-id="a73c7-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a73c7-166"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a73c7-166"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a73c7-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a73c7-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a73c7-168">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="a73c7-168">**glBegin**</span></span>](/windows/desktop/OpenGL/glbegin)
</dt> <dt>

[<span data-ttu-id="a73c7-169">**glCallLists**</span><span class="sxs-lookup"><span data-stu-id="a73c7-169">**glCallLists**</span></span>](glcalllists.md)
</dt> <dt>

[<span data-ttu-id="a73c7-170">**glColor**</span><span class="sxs-lookup"><span data-stu-id="a73c7-170">**glColor**</span></span>](glcolor-functions.md)
</dt> <dt>

[<span data-ttu-id="a73c7-171">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="a73c7-171">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="a73c7-172">**glEvalCoord**</span><span class="sxs-lookup"><span data-stu-id="a73c7-172">**glEvalCoord**</span></span>](glevalcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="a73c7-173">**glEvalPoint**</span><span class="sxs-lookup"><span data-stu-id="a73c7-173">**glEvalPoint**</span></span>](glevalpoint.md)
</dt> <dt>

[<span data-ttu-id="a73c7-174">**glIndex**</span><span class="sxs-lookup"><span data-stu-id="a73c7-174">**glIndex**</span></span>](glindex-functions.md)
</dt> <dt>

[<span data-ttu-id="a73c7-175">**glMaterial**</span><span class="sxs-lookup"><span data-stu-id="a73c7-175">**glMaterial**</span></span>](glmaterial-functions.md)
</dt> <dt>

[<span data-ttu-id="a73c7-176">**glNormal**</span><span class="sxs-lookup"><span data-stu-id="a73c7-176">**glNormal**</span></span>](glnormal-functions.md)
</dt> <dt>

[<span data-ttu-id="a73c7-177">**glTexCoord**</span><span class="sxs-lookup"><span data-stu-id="a73c7-177">**glTexCoord**</span></span>](gltexcoord-functions.md)
</dt> <dt>

[<span data-ttu-id="a73c7-178">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="a73c7-178">**glVertex**</span></span>](glvertex-functions.md)
</dt> </dl>

 

