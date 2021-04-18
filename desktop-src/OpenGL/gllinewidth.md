---
title: funzione glLineWidth (GL. h)
description: La funzione glLineWidth specifica la larghezza delle linee rasterizzate.
ms.assetid: 13a69fd7-5eee-42ec-bd05-5bd3c838d4d7
keywords:
- funzione glLineWidth OpenGL
topic_type:
- apiref
api_name:
- glLineWidth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa4cecafc9e5d8e0f55c6e9d0dbfe49924d54f14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302712"
---
# <a name="gllinewidth-function"></a><span data-ttu-id="45aa2-104">glLineWidth (funzione)</span><span class="sxs-lookup"><span data-stu-id="45aa2-104">glLineWidth function</span></span>

<span data-ttu-id="45aa2-105">La funzione **glLineWidth** specifica la larghezza delle linee rasterizzate.</span><span class="sxs-lookup"><span data-stu-id="45aa2-105">The **glLineWidth** function specifies the width of rasterized lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="45aa2-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="45aa2-106">Syntax</span></span>


```C++
void WINAPI glLineWidth(
   GLfloat width
);
```



## <a name="parameters"></a><span data-ttu-id="45aa2-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="45aa2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45aa2-108">*width*</span><span class="sxs-lookup"><span data-stu-id="45aa2-108">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="45aa2-109">Larghezza delle linee rasterizzate.</span><span class="sxs-lookup"><span data-stu-id="45aa2-109">The width of rasterized lines.</span></span> <span data-ttu-id="45aa2-110">Il valore predefinito è 1,0.</span><span class="sxs-lookup"><span data-stu-id="45aa2-110">The default is 1.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45aa2-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="45aa2-111">Return value</span></span>

<span data-ttu-id="45aa2-112">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="45aa2-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="45aa2-113">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="45aa2-113">Error codes</span></span>

<span data-ttu-id="45aa2-114">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="45aa2-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="45aa2-115">Nome</span><span class="sxs-lookup"><span data-stu-id="45aa2-115">Name</span></span>                                                                                                  | <span data-ttu-id="45aa2-116">Significato</span><span class="sxs-lookup"><span data-stu-id="45aa2-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="45aa2-117"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="45aa2-117"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="45aa2-118">la *larghezza* era minore o uguale a zero.</span><span class="sxs-lookup"><span data-stu-id="45aa2-118">*width* was less than or equal to zero.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="45aa2-119"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="45aa2-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="45aa2-120">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="45aa2-120">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="45aa2-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="45aa2-121">Remarks</span></span>

<span data-ttu-id="45aa2-122">La funzione **glLineWidth** specifica la larghezza rasterizzata delle righe con alias e con alias.</span><span class="sxs-lookup"><span data-stu-id="45aa2-122">The **glLineWidth** function specifies the rasterized width of both aliased and antialiased lines.</span></span> <span data-ttu-id="45aa2-123">L'uso di una lunghezza di riga diversa da 1,0 ha effetti diversi, a seconda che sia abilitata l'anti-aliasing della linea.</span><span class="sxs-lookup"><span data-stu-id="45aa2-123">Using a line width other than 1.0 has different effects, depending on whether line antialiasing is enabled.</span></span> <span data-ttu-id="45aa2-124">L'anti-aliasing della linea viene controllato chiamando [**glEnable**](glenable.md) e **glDisable** con l'argomento GL \_ line \_ Smooth.</span><span class="sxs-lookup"><span data-stu-id="45aa2-124">Line antialiasing is controlled by calling [**glEnable**](glenable.md) and **glDisable** with argument GL\_LINE\_SMOOTH.</span></span>

<span data-ttu-id="45aa2-125">Se l'anti-aliasing della riga è disabilitato, la larghezza effettiva viene determinata dall'arrotondamento della larghezza fornita all'intero più vicino.</span><span class="sxs-lookup"><span data-stu-id="45aa2-125">If line antialiasing is disabled, the actual width is determined by rounding the supplied width to the nearest integer.</span></span> <span data-ttu-id="45aa2-126">Se l'arrotondamento ha come risultato il valore 0,0, è come se la lunghezza della linea fosse 1,0) Se \| ?</span><span class="sxs-lookup"><span data-stu-id="45aa2-126">(If the rounding results in the value 0.0, it is as if the line width were 1.0) If \| ?</span></span> <span data-ttu-id="45aa2-127">x \|  =  \| ?</span><span class="sxs-lookup"><span data-stu-id="45aa2-127">x \| = \| ?</span></span> <span data-ttu-id="45aa2-128">y \| , *i* pixel vengono compilati in ogni colonna rasterizzata, dove  è il valore arrotondato della *larghezza*.</span><span class="sxs-lookup"><span data-stu-id="45aa2-128">y \|, *i* pixels are filled in each column that is rasterized, where *i* is the rounded value of *width*.</span></span> <span data-ttu-id="45aa2-129">In caso contrario, *i* pixel vengono compilati in ogni riga rasterizzata.</span><span class="sxs-lookup"><span data-stu-id="45aa2-129">Otherwise, *i* pixels are filled in each row that is rasterized.</span></span>

<span data-ttu-id="45aa2-130">Se l'anti-aliasing è abilitato, la rasterizzazione delle righe produce un frammento per ogni quadrato di pixel che interseca l'area che si trova all'interno del rettangolo con larghezza uguale alla lunghezza riga corrente, lunghezza uguale alla lunghezza effettiva della linea e centrata sul segmento di linea matematico.</span><span class="sxs-lookup"><span data-stu-id="45aa2-130">If antialiasing is enabled, line rasterization produces a fragment for each pixel square that intersects the region lying within the rectangle having width equal to the current line width, length equal to the actual length of the line, and centered on the mathematical line segment.</span></span> <span data-ttu-id="45aa2-131">Il valore di code coverage per ogni frammento è l'area delle coordinate della finestra dell'intersezione dell'area rettangolare con il quadrato pixel corrispondente.</span><span class="sxs-lookup"><span data-stu-id="45aa2-131">The coverage value for each fragment is the window coordinate area of the intersection of the rectangular region with the corresponding pixel square.</span></span> <span data-ttu-id="45aa2-132">Questo valore viene salvato e utilizzato nel passaggio di rasterizzazione finale.</span><span class="sxs-lookup"><span data-stu-id="45aa2-132">This value is saved and used in the final rasterization step.</span></span>

<span data-ttu-id="45aa2-133">Non è possibile supportare tutte le larghezze quando è abilitato l'anti-aliasing della riga.</span><span class="sxs-lookup"><span data-stu-id="45aa2-133">Not all widths can be supported when line antialiasing is enabled.</span></span> <span data-ttu-id="45aa2-134">Se viene richiesta una larghezza non supportata, viene utilizzata la larghezza supportata più vicina.</span><span class="sxs-lookup"><span data-stu-id="45aa2-134">If an unsupported width is requested, the nearest supported width is used.</span></span> <span data-ttu-id="45aa2-135">È garantita solo la larghezza 1,0; altre dipendono dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="45aa2-135">Only width 1.0 is guaranteed to be supported; others depend on the implementation.</span></span> <span data-ttu-id="45aa2-136">È possibile eseguire una query sull'intervallo di larghezze supportate e sulla differenza di dimensione tra le larghezze supportate all'interno dell'intervallo chiamando **glGet** con gli argomenti \_ linea di lunghezza riga GL \_ \_ e \_ \_ granularità di lunghezza linea GL \_ .</span><span class="sxs-lookup"><span data-stu-id="45aa2-136">The range of supported widths and the size difference between supported widths within the range can be queried by calling **glGet** with arguments GL\_LINE\_WIDTH\_RANGE and GL\_LINE\_WIDTH\_GRANULARITY.</span></span>

<span data-ttu-id="45aa2-137">La lunghezza riga specificata da **glLineWidth** viene sempre restituita quando \_ viene eseguita una query sulla lunghezza della riga GL \_ .</span><span class="sxs-lookup"><span data-stu-id="45aa2-137">The line width specified by **glLineWidth** is always returned when GL\_LINE\_WIDTH is queried.</span></span> <span data-ttu-id="45aa2-138">Il bloccaggio e l'arrotondamento per le linee con alias e con alias non hanno effetto sul valore specificato.</span><span class="sxs-lookup"><span data-stu-id="45aa2-138">Clamping and rounding for aliased and antialiased lines have no effect on the specified value.</span></span>

<span data-ttu-id="45aa2-139">La lunghezza della linea non con alias può essere fissata a un valore massimo dipendente dall'implementazione.</span><span class="sxs-lookup"><span data-stu-id="45aa2-139">Non-antialiased line width may be clamped to an implementation-dependent maximum.</span></span> <span data-ttu-id="45aa2-140">Sebbene non sia possibile eseguire query su questo valore massimo, il valore non deve essere minore del valore massimo per le righe con alias, arrotondato al valore intero più vicino.</span><span class="sxs-lookup"><span data-stu-id="45aa2-140">Although this maximum cannot be queried, it must be no less than the maximum value for antialiased lines, rounded to the nearest integer value.</span></span>

<span data-ttu-id="45aa2-141">Le funzioni seguenti consentono di recuperare informazioni correlate a **glLineWidth**:</span><span class="sxs-lookup"><span data-stu-id="45aa2-141">The following functions retrieve information related to **glLineWidth**:</span></span>

<span data-ttu-id="45aa2-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con \_ lunghezza riga argomento \_ GL</span><span class="sxs-lookup"><span data-stu-id="45aa2-142">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LINE\_WIDTH</span></span>

<span data-ttu-id="45aa2-143">**glGet** con argomento di \_ lunghezza riga linea GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="45aa2-143">**glGet** with argument GL\_LINE\_WIDTH\_RANGE</span></span>

<span data-ttu-id="45aa2-144">**glGet** con \_ \_ granularità di lunghezza riga argomento GL \_</span><span class="sxs-lookup"><span data-stu-id="45aa2-144">**glGet** with argument GL\_LINE\_WIDTH\_GRANULARITY</span></span>

<span data-ttu-id="45aa2-145">[**glIsEnabled**](glisenabled.md) con argomento GL \_ line \_ Smooth</span><span class="sxs-lookup"><span data-stu-id="45aa2-145">[**glIsEnabled**](glisenabled.md) with argument GL\_LINE\_SMOOTH</span></span>

## <a name="requirements"></a><span data-ttu-id="45aa2-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45aa2-146">Requirements</span></span>



| <span data-ttu-id="45aa2-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="45aa2-147">Requirement</span></span> | <span data-ttu-id="45aa2-148">Valore</span><span class="sxs-lookup"><span data-stu-id="45aa2-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45aa2-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45aa2-149">Minimum supported client</span></span><br/> | <span data-ttu-id="45aa2-150">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="45aa2-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="45aa2-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="45aa2-151">Minimum supported server</span></span><br/> | <span data-ttu-id="45aa2-152">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="45aa2-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="45aa2-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="45aa2-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="45aa2-154"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="45aa2-154"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="45aa2-155">Libreria</span><span class="sxs-lookup"><span data-stu-id="45aa2-155">Library</span></span><br/>                  | <dl> <span data-ttu-id="45aa2-156"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="45aa2-156"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="45aa2-157">DLL</span><span class="sxs-lookup"><span data-stu-id="45aa2-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45aa2-158"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45aa2-158"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45aa2-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="45aa2-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45aa2-160">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="45aa2-160">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="45aa2-161">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="45aa2-161">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="45aa2-162">**Remo**</span><span class="sxs-lookup"><span data-stu-id="45aa2-162">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="45aa2-163">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="45aa2-163">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





