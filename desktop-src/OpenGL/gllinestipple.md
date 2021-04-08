---
title: funzione glLineStipple (GL. h)
description: La funzione glLineStipple specifica il modello di riga stipple.
ms.assetid: 256d968c-9e72-4aec-9faf-afe70f1087a8
keywords:
- funzione glLineStipple OpenGL
topic_type:
- apiref
api_name:
- glLineStipple
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b47202b25c0779a3daa0bd801900b1d29e0b37b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739799"
---
# <a name="gllinestipple-function"></a><span data-ttu-id="3545d-104">glLineStipple (funzione)</span><span class="sxs-lookup"><span data-stu-id="3545d-104">glLineStipple function</span></span>

<span data-ttu-id="3545d-105">La funzione **glLineStipple** specifica il modello di riga stipple.</span><span class="sxs-lookup"><span data-stu-id="3545d-105">The **glLineStipple** function specifies the line stipple pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="3545d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3545d-106">Syntax</span></span>


```C++
void WINAPI glLineStipple(
   GLint    factor,
   GLushort pattern
);
```



## <a name="parameters"></a><span data-ttu-id="3545d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3545d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3545d-108">*Factor*</span><span class="sxs-lookup"><span data-stu-id="3545d-108">*factor*</span></span> 
</dt> <dd>

<span data-ttu-id="3545d-109">Moltiplicatore per ogni bit nello schema stipple della riga.</span><span class="sxs-lookup"><span data-stu-id="3545d-109">A multiplier for each bit in the line stipple pattern.</span></span> <span data-ttu-id="3545d-110">Se *Factor* è 3, ad esempio, ogni bit del modello verrà usato tre volte prima del bit successivo nel modello.</span><span class="sxs-lookup"><span data-stu-id="3545d-110">If *factor* is 3, for example, each bit in the pattern will be used three times before the next bit in the pattern is used.</span></span> <span data-ttu-id="3545d-111">Il parametro *Factor* viene bloccato nell'intervallo \[ 1, 256 e il \] valore predefinito è uno.</span><span class="sxs-lookup"><span data-stu-id="3545d-111">The *factor* parameter is clamped to the range \[1, 256\] and defaults to one.</span></span>

</dd> <dt>

<span data-ttu-id="3545d-112">*pattern*</span><span class="sxs-lookup"><span data-stu-id="3545d-112">*pattern*</span></span> 
</dt> <dd>

<span data-ttu-id="3545d-113">Intero a 16 bit il cui modello di bit determina quali frammenti di una linea verranno disegnati quando la riga viene rasterizzata.</span><span class="sxs-lookup"><span data-stu-id="3545d-113">A 16-bit integer whose bit pattern determines which fragments of a line will be drawn when the line is rasterized.</span></span> <span data-ttu-id="3545d-114">Viene usato per primo il bit zero e il criterio predefinito è tutti quelli.</span><span class="sxs-lookup"><span data-stu-id="3545d-114">Bit zero is used first, and the default pattern is all ones.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3545d-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3545d-115">Return value</span></span>

<span data-ttu-id="3545d-116">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="3545d-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3545d-117">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="3545d-117">Error codes</span></span>

<span data-ttu-id="3545d-118">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="3545d-118">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="3545d-119">Nome</span><span class="sxs-lookup"><span data-stu-id="3545d-119">Name</span></span>                                                                                                  | <span data-ttu-id="3545d-120">Significato</span><span class="sxs-lookup"><span data-stu-id="3545d-120">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3545d-121"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3545d-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="3545d-122">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="3545d-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3545d-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="3545d-123">Remarks</span></span>

<span data-ttu-id="3545d-124">La funzione **glLineStipple** specifica il modello di riga stipple.</span><span class="sxs-lookup"><span data-stu-id="3545d-124">The **glLineStipple** function specifies the line stipple pattern.</span></span> <span data-ttu-id="3545d-125">Line punteggiatura maschera alcuni frammenti prodotti dalla rasterizzazione; questi frammenti non verranno disegnati.</span><span class="sxs-lookup"><span data-stu-id="3545d-125">Line stippling masks out certain fragments produced by rasterization; those fragments will not be drawn.</span></span> <span data-ttu-id="3545d-126">La maschera viene eseguita utilizzando tre parametri, ovvero *il modello di pattern stipple* a 16 bit, il *fattore* di ripetizione del conteggio e *un contatore di* stipple Integer.</span><span class="sxs-lookup"><span data-stu-id="3545d-126">The masking is achieved by using three parameters: the 16-bit line stipple pattern *pattern*, the repeat count *factor*, and an integer stipple counter *s*.</span></span>

<span data-ttu-id="3545d-127">Counter *s* viene reimpostato su zero ogni volta che viene chiamato [**glBegin**](glbegin.md) e prima che venga generato ogni segmento di riga di una sequenza **glBegin**(GL \_ Lines)/**glEnd** .</span><span class="sxs-lookup"><span data-stu-id="3545d-127">Counter *s* is reset to zero whenever [**glBegin**](glbegin.md) is called, and before each line segment of a **glBegin**(GL\_LINES)/**glEnd** sequence is generated.</span></span> <span data-ttu-id="3545d-128">Viene incrementato dopo la generazione di ogni frammento di un segmento di linea con alias di larghezza unità o dopo che sono stati generati *i* frammenti di un segmento di linea *i* /o.</span><span class="sxs-lookup"><span data-stu-id="3545d-128">It is incremented after each fragment of a unit width aliased line segment is generated, or after each *i* fragments of an *i* width line segment are generated.</span></span> <span data-ttu-id="3545d-129">I frammenti di *i* associati ai conteggi *vengono* mascherati se il mod 16 dei bitdel *modello*  /  è zero.</span><span class="sxs-lookup"><span data-stu-id="3545d-129">The *i* fragments associated with count *s* are masked out if *pattern* bit (*s* / *factor*) mod 16 is zero.</span></span> <span data-ttu-id="3545d-130">In caso contrario, questi frammenti vengono inviati al framebuffer.</span><span class="sxs-lookup"><span data-stu-id="3545d-130">Otherwise these fragments are sent to the framebuffer.</span></span> <span data-ttu-id="3545d-131">Bit zero del *modello* è il bit meno significativo.</span><span class="sxs-lookup"><span data-stu-id="3545d-131">Bit zero of *pattern* is the least significant bit.</span></span>

<span data-ttu-id="3545d-132">Le linee con anti-aliasing vengono considerate come una sequenza di rettangoli con *larghezza* 1 a scopo di punteggiatura.</span><span class="sxs-lookup"><span data-stu-id="3545d-132">Antialiased lines are treated as a sequence of 1x *width* rectangles for purposes of stippling.</span></span> <span data-ttu-id="3545d-133">Il rettangolo *s* è rasterizzato o non basato sulla regola del frammento descritta per le righe con alias. conta i rettangoli anziché i gruppi di frammenti.</span><span class="sxs-lookup"><span data-stu-id="3545d-133">Rectangle *s* is rasterized or not based on the fragment rule described for aliased lines; it counts rectangles rather than groups of fragments.</span></span>

<span data-ttu-id="3545d-134">La riga punteggiatura è abilitata o disabilitata usando [**glEnable**](glenable.md) e **glDisable** con l'argomento GL \_ line \_ stipple.</span><span class="sxs-lookup"><span data-stu-id="3545d-134">Line stippling is enabled or disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_LINE\_STIPPLE.</span></span> <span data-ttu-id="3545d-135">Se abilitata, il modello di stipple di riga viene applicato come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="3545d-135">When enabled, the line stipple pattern is applied as described above.</span></span> <span data-ttu-id="3545d-136">Quando è disabilitato, è come se il modello fosse tutti quelli.</span><span class="sxs-lookup"><span data-stu-id="3545d-136">When disabled, it is as if the pattern were all ones.</span></span> <span data-ttu-id="3545d-137">Inizialmente, la riga punteggiatura è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="3545d-137">Initially, line stippling is disabled.</span></span>

<span data-ttu-id="3545d-138">Le funzioni seguenti consentono di recuperare informazioni correlate a **glLineStipple**:</span><span class="sxs-lookup"><span data-stu-id="3545d-138">The following functions retrieve information related to **glLineStipple**:</span></span>

<span data-ttu-id="3545d-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ modello di \_ stipple \_ linea GL</span><span class="sxs-lookup"><span data-stu-id="3545d-139">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LINE\_STIPPLE\_PATTERN</span></span>

<span data-ttu-id="3545d-140">**glGet** con argomento della \_ riga GL \_ stipple \_ Repeat</span><span class="sxs-lookup"><span data-stu-id="3545d-140">**glGet** with argument GL\_LINE\_STIPPLE\_REPEAT</span></span>

<span data-ttu-id="3545d-141">[**glIsEnabled**](glisenabled.md) con argomento GL \_ line \_ stipple</span><span class="sxs-lookup"><span data-stu-id="3545d-141">[**glIsEnabled**](glisenabled.md) with argument GL\_LINE\_STIPPLE</span></span>

## <a name="requirements"></a><span data-ttu-id="3545d-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3545d-142">Requirements</span></span>



| <span data-ttu-id="3545d-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="3545d-143">Requirement</span></span> | <span data-ttu-id="3545d-144">Valore</span><span class="sxs-lookup"><span data-stu-id="3545d-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3545d-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3545d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="3545d-146">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3545d-146">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3545d-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3545d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="3545d-148">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3545d-148">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3545d-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3545d-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="3545d-150"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="3545d-150"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="3545d-151">Libreria</span><span class="sxs-lookup"><span data-stu-id="3545d-151">Library</span></span><br/>                  | <dl> <span data-ttu-id="3545d-152"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3545d-152"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="3545d-153">DLL</span><span class="sxs-lookup"><span data-stu-id="3545d-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3545d-154"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3545d-154"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3545d-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3545d-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3545d-156">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="3545d-156">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="3545d-157">**Remo**</span><span class="sxs-lookup"><span data-stu-id="3545d-157">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="3545d-158">**glLineWidth**</span><span class="sxs-lookup"><span data-stu-id="3545d-158">**glLineWidth**</span></span>](gllinewidth.md)
</dt> <dt>

[<span data-ttu-id="3545d-159">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="3545d-159">**glPolygonStipple**</span></span>](glpolygonstipple.md)
</dt> </dl>

 

 





