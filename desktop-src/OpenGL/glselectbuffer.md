---
title: funzione glSelectBuffer (GL. h)
description: La funzione glSelectBuffer stabilisce un buffer per i valori della modalità di selezione.
ms.assetid: b5c64364-1f47-4281-96b5-95c3f5c8e753
keywords:
- funzione glSelectBuffer OpenGL
topic_type:
- apiref
api_name:
- glSelectBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efa5b97abad6575de77a760c72e3eb05e90461c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740039"
---
# <a name="glselectbuffer-function"></a><span data-ttu-id="9137f-104">glSelectBuffer (funzione)</span><span class="sxs-lookup"><span data-stu-id="9137f-104">glSelectBuffer function</span></span>

<span data-ttu-id="9137f-105">La funzione **glSelectBuffer** stabilisce un buffer per i valori della modalità di selezione.</span><span class="sxs-lookup"><span data-stu-id="9137f-105">The **glSelectBuffer** function establishes a buffer for selection mode values.</span></span>

## <a name="syntax"></a><span data-ttu-id="9137f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9137f-106">Syntax</span></span>


```C++
void WINAPI glSelectBuffer(
   GLsizei size,
   GLuint  *buffer
);
```



## <a name="parameters"></a><span data-ttu-id="9137f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9137f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9137f-108">*size*</span><span class="sxs-lookup"><span data-stu-id="9137f-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="9137f-109">Dimensione del *buffer*.</span><span class="sxs-lookup"><span data-stu-id="9137f-109">The size of *buffer*.</span></span>

</dd> <dt>

<span data-ttu-id="9137f-110">*buffer*</span><span class="sxs-lookup"><span data-stu-id="9137f-110">*buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="9137f-111">Restituisce i dati di selezione.</span><span class="sxs-lookup"><span data-stu-id="9137f-111">Returns the selection data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9137f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9137f-112">Return value</span></span>

<span data-ttu-id="9137f-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="9137f-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9137f-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="9137f-114">Error codes</span></span>

<span data-ttu-id="9137f-115">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="9137f-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="9137f-116">Nome</span><span class="sxs-lookup"><span data-stu-id="9137f-116">Name</span></span>                                                                                                  | <span data-ttu-id="9137f-117">Significato</span><span class="sxs-lookup"><span data-stu-id="9137f-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9137f-118"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9137f-118"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="9137f-119">la *dimensione* è negativa.</span><span class="sxs-lookup"><span data-stu-id="9137f-119">*size* was negative.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="9137f-120"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9137f-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9137f-121">La funzione è stata chiamata mentre la modalità di rendering era GL \_ Select.</span><span class="sxs-lookup"><span data-stu-id="9137f-121">The function was called while the render mode was GL\_SELECT.</span></span><br/>                                                              |
| <dl> <span data-ttu-id="9137f-122"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9137f-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="9137f-123">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="9137f-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="9137f-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="9137f-124">Remarks</span></span>

<span data-ttu-id="9137f-125">La funzione **glSelectBuffer** ha due parametri: *buffer* è un puntatore a una matrice di interi senza segno e *size* indica la dimensione della matrice.</span><span class="sxs-lookup"><span data-stu-id="9137f-125">The **glSelectBuffer** function has two parameters: *buffer* is a pointer to an array of unsigned integers, and *size* indicates the size of the array.</span></span> <span data-ttu-id="9137f-126">Il parametro *buffer* restituisce i valori dallo stack dei nomi (vedere [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)) quando la modalità di rendering è GL \_ Select (vedere [**glRenderMode**](glrendermode.md)).</span><span class="sxs-lookup"><span data-stu-id="9137f-126">The *buffer* parameter returns values from the name stack (see [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)) when the rendering mode is GL\_SELECT (see [**glRenderMode**](glrendermode.md)).</span></span> <span data-ttu-id="9137f-127">La funzione **glSelectBuffer** deve essere eseguita prima dell'abilitazione della modalità di selezione e non deve essere eseguita mentre la modalità di rendering è GL \_ Select.</span><span class="sxs-lookup"><span data-stu-id="9137f-127">The **glSelectBuffer** function must be issued before selection mode is enabled, and it must not be issued while the rendering mode is GL\_SELECT.</span></span>

<span data-ttu-id="9137f-128">La selezione viene utilizzata da un programmatore per determinare quali primitive vengono disegnate in una determinata area di una finestra.</span><span class="sxs-lookup"><span data-stu-id="9137f-128">Selection is used by a programmer to determine which primitives are drawn into some region of a window.</span></span> <span data-ttu-id="9137f-129">L'area è definita dalle matrici Modelview e Perspective correnti.</span><span class="sxs-lookup"><span data-stu-id="9137f-129">The region is defined by the current modelview and perspective matrices.</span></span>

<span data-ttu-id="9137f-130">In modalità di selezione non viene prodotto alcun frammento di pixel dalla rasterizzazione.</span><span class="sxs-lookup"><span data-stu-id="9137f-130">In selection mode, no pixel fragments are produced from rasterization.</span></span> <span data-ttu-id="9137f-131">Al contrario, se una primitiva interseca il volume di ritaglio definito dal tronco di visualizzazione e i piani di ritaglio definiti dall'utente, questa primitiva causa un riscontro della selezione.</span><span class="sxs-lookup"><span data-stu-id="9137f-131">Instead, if a primitive intersects the clip volume defined by the viewing frustum and the user-defined clipping planes, this primitive causes a selection hit.</span></span> <span data-ttu-id="9137f-132">Con i poligoni, non si verifica alcun hit se il poligono viene raccolto. Quando viene apportata una modifica allo stack dei nomi o quando viene chiamato [**glRenderMode**](glrendermode.md) , un record di hit viene copiato nel *buffer* se si verificano dei riscontri dall'ultimo evento di questo tipo (una modifica dello stack del nome o una chiamata **glRenderMode** ).</span><span class="sxs-lookup"><span data-stu-id="9137f-132">(With polygons, no hit occurs if the polygon is culled.) When a change is made to the name stack, or when [**glRenderMode**](glrendermode.md) is called, a hit record is copied to *buffer* if any hits have occurred since the last such event (either a name stack change or a **glRenderMode** call).</span></span> <span data-ttu-id="9137f-133">Il record di hit è costituito dal numero di nomi nello stack dei nomi al momento dell'evento. seguito dai valori minimo e massimo di profondità di tutti i vertici raggiunti dall'evento precedente; seguito dal contenuto dello stack dei nomi, il nome inferiore prima.</span><span class="sxs-lookup"><span data-stu-id="9137f-133">The hit record consists of the number of names in the name stack at the time of the event; followed by the minimum and maximum depth values of all vertices that hit since the previous event; followed by the name stack contents, bottom name first.</span></span>

<span data-ttu-id="9137f-134">Viene eseguito il mapping dei valori di profondità restituiti in modo che il valore di Unsigned Integer più grande corrisponda alla profondità della coordinata finestra 1,0 e zero corrisponda alla 0,0 profondità della coordinata</span><span class="sxs-lookup"><span data-stu-id="9137f-134">Returned depth values are mapped such that the largest unsigned integer value corresponds to window coordinate depth 1.0, and zero corresponds to window coordinate depth 0.0.</span></span>

<span data-ttu-id="9137f-135">Un indice interno nel *buffer* viene reimpostato su zero ogni volta che viene immessa la modalità di selezione.</span><span class="sxs-lookup"><span data-stu-id="9137f-135">An internal index into *buffer* is reset to zero whenever selection mode is entered.</span></span> <span data-ttu-id="9137f-136">Ogni volta che un record di hit viene copiato nel *buffer*, l'indice viene incrementato in modo che punti alla cella appena oltre la fine del blocco di namesthat è, alla cella successiva disponibile.</span><span class="sxs-lookup"><span data-stu-id="9137f-136">Each time a hit record is copied into *buffer*, the index is incremented to point to the cell just past the end of the block of namesthat is, to the next available cell.</span></span> <span data-ttu-id="9137f-137">Se il record di hit supera il numero di posizioni rimanenti nel *buffer*, la quantità di dati che è possibile adattare viene copiata e viene impostato il flag di overflow.</span><span class="sxs-lookup"><span data-stu-id="9137f-137">If the hit record is larger than the number of remaining locations in *buffer*, as much data as can fit is copied, and the overflow flag is set.</span></span> <span data-ttu-id="9137f-138">Se lo stack dei nomi è vuoto quando viene copiato un record di hit, il record è costituito da zero seguito dai valori minimo e massimo di profondità.</span><span class="sxs-lookup"><span data-stu-id="9137f-138">If the name stack is empty when a hit record is copied, that record consists of zero followed by the minimum and maximum depth values.</span></span>

<span data-ttu-id="9137f-139">La modalità di selezione è stata chiusa chiamando **glRenderMode** con un argomento diverso da GL \_ Select.</span><span class="sxs-lookup"><span data-stu-id="9137f-139">Selection mode is exited by calling **glRenderMode** with an argument other than GL\_SELECT.</span></span> <span data-ttu-id="9137f-140">Quando **glRenderMode** viene chiamato mentre la modalità di rendering è GL \_ Select, restituisce il numero di record di hit copiati nel *buffer*, reimposta il flag di overflow e il puntatore del buffer di selezione e inizializza lo stack dei nomi come vuoto.</span><span class="sxs-lookup"><span data-stu-id="9137f-140">Whenever **glRenderMode** is called while the render mode is GL\_SELECT, it returns the number of hit records copied to *buffer*, resets the overflow flag and the selection buffer pointer, and initializes the name stack to be empty.</span></span> <span data-ttu-id="9137f-141">Se è stato impostato il bit di overflow quando è stato chiamato **glRenderMode** , viene restituito un numero di record di hit negativo.</span><span class="sxs-lookup"><span data-stu-id="9137f-141">If the overflow bit was set when **glRenderMode** was called, a negative hit record count is returned.</span></span>

<span data-ttu-id="9137f-142">Il contenuto del *buffer* non è definito fino a quando non viene chiamato [**glRenderMode**](glrendermode.md) con un argomento diverso da GL \_ Select.</span><span class="sxs-lookup"><span data-stu-id="9137f-142">The contents of *buffer* are undefined until [**glRenderMode**](glrendermode.md) is called with an argument other than GL\_SELECT.</span></span>

<span data-ttu-id="9137f-143">Le  / primitive e le chiamate a [**glRasterPos**](glrasterpos-functions.md) di glBegin **glEnd** possono causare riscontri.</span><span class="sxs-lookup"><span data-stu-id="9137f-143">The **glBegin**/**glEnd** primitives and calls to [**glRasterPos**](glrasterpos-functions.md) can result in hits.</span></span>

<span data-ttu-id="9137f-144">La funzione seguente recupera le informazioni correlate a **glSelectBuffer**:</span><span class="sxs-lookup"><span data-stu-id="9137f-144">The following function retrieves information related to **glSelectBuffer**:</span></span>

<span data-ttu-id="9137f-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ \_ profondità dello stack nome GL \_</span><span class="sxs-lookup"><span data-stu-id="9137f-145">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_NAME\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="9137f-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9137f-146">Requirements</span></span>



| <span data-ttu-id="9137f-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="9137f-147">Requirement</span></span> | <span data-ttu-id="9137f-148">Valore</span><span class="sxs-lookup"><span data-stu-id="9137f-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9137f-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9137f-149">Minimum supported client</span></span><br/> | <span data-ttu-id="9137f-150">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9137f-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9137f-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9137f-151">Minimum supported server</span></span><br/> | <span data-ttu-id="9137f-152">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9137f-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9137f-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9137f-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="9137f-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="9137f-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="9137f-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="9137f-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="9137f-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9137f-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9137f-157">DLL</span><span class="sxs-lookup"><span data-stu-id="9137f-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9137f-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9137f-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9137f-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9137f-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9137f-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="9137f-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="9137f-161">**Remo**</span><span class="sxs-lookup"><span data-stu-id="9137f-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="9137f-162">**glFeedbackBuffer**</span><span class="sxs-lookup"><span data-stu-id="9137f-162">**glFeedbackBuffer**</span></span>](glfeedbackbuffer.md)
</dt> <dt>

[<span data-ttu-id="9137f-163">**glInitNames**</span><span class="sxs-lookup"><span data-stu-id="9137f-163">**glInitNames**</span></span>](glinitnames.md)
</dt> <dt>

[<span data-ttu-id="9137f-164">**glLoadName**</span><span class="sxs-lookup"><span data-stu-id="9137f-164">**glLoadName**</span></span>](glloadname.md)
</dt> <dt>

[<span data-ttu-id="9137f-165">**glPushName**</span><span class="sxs-lookup"><span data-stu-id="9137f-165">**glPushName**</span></span>](glpushname.md)
</dt> <dt>

[<span data-ttu-id="9137f-166">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="9137f-166">**glRenderMode**</span></span>](glrendermode.md)
</dt> </dl>

 

 





