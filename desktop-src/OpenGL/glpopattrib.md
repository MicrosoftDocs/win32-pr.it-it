---
title: funzione glPopAttrib (GL. h)
description: Estrae lo stack dell'attributo.
ms.assetid: 6a11392c-d5af-47bb-a66a-691730a58260
keywords:
- funzione glPopAttrib OpenGL
topic_type:
- apiref
api_name:
- glPopAttrib
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2258b0f16e6f61e660384931abc394300a29516
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301794"
---
# <a name="glpopattrib-function"></a><span data-ttu-id="6865e-104">glPopAttrib (funzione)</span><span class="sxs-lookup"><span data-stu-id="6865e-104">glPopAttrib function</span></span>

<span data-ttu-id="6865e-105">Estrae lo stack dell'attributo.</span><span class="sxs-lookup"><span data-stu-id="6865e-105">Pops the attribute stack.</span></span>

## <a name="syntax"></a><span data-ttu-id="6865e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6865e-106">Syntax</span></span>


```C++
void WINAPI glPopAttrib(void);
```



## <a name="parameters"></a><span data-ttu-id="6865e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6865e-107">Parameters</span></span>

<span data-ttu-id="6865e-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="6865e-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6865e-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6865e-109">Return value</span></span>

<span data-ttu-id="6865e-110">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="6865e-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6865e-111">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="6865e-111">Error codes</span></span>

<span data-ttu-id="6865e-112">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="6865e-112">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6865e-113">Nome</span><span class="sxs-lookup"><span data-stu-id="6865e-113">Name</span></span>                                                                                                  | <span data-ttu-id="6865e-114">Significato</span><span class="sxs-lookup"><span data-stu-id="6865e-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6865e-115"><dt>**\_underflow dello stack GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6865e-115"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="6865e-116">La funzione è stata chiamata mentre lo stack dell'attributo è vuoto.</span><span class="sxs-lookup"><span data-stu-id="6865e-116">The function was called while the attribute stack was empty.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="6865e-117"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6865e-117"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="6865e-118">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="6865e-118">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6865e-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="6865e-119">Remarks</span></span>

<span data-ttu-id="6865e-120">La funzione [**glPushAttrib**](glpushattrib.md) accetta un argomento, una maschera che indica i gruppi di variabili di stato da salvare nello stack di attributi.</span><span class="sxs-lookup"><span data-stu-id="6865e-120">The [**glPushAttrib**](glpushattrib.md) function takes one argument, a mask that indicates which groups of state variables to save on the attribute stack.</span></span> <span data-ttu-id="6865e-121">Le costanti simboliche vengono utilizzate per impostare i bit nella maschera.</span><span class="sxs-lookup"><span data-stu-id="6865e-121">Symbolic constants are used to set bits in the mask.</span></span> <span data-ttu-id="6865e-122">Il parametro mask viene in genere costruito da **o** con alcune di queste costanti insieme.</span><span class="sxs-lookup"><span data-stu-id="6865e-122">The mask parameter is typically constructed by **OR** ing several of these constants together.</span></span> <span data-ttu-id="6865e-123">La maschera speciale GL \_ tutti \_ i \_ bit attrib può essere usata per salvare tutti gli Stati impilabili.</span><span class="sxs-lookup"><span data-stu-id="6865e-123">The special mask GL\_ALL\_ATTRIB\_BITS can be used to save all stackable states.</span></span>

<span data-ttu-id="6865e-124">La funzione **glPopAttrib** Ripristina i valori delle variabili di stato salvate con l'ultimo comando [**glPushAttrib**](glpushattrib.md) .</span><span class="sxs-lookup"><span data-stu-id="6865e-124">The **glPopAttrib** function restores the values of the state variables saved with the last [**glPushAttrib**](glpushattrib.md) command.</span></span> <span data-ttu-id="6865e-125">Quelli non salvati vengono lasciati invariati.</span><span class="sxs-lookup"><span data-stu-id="6865e-125">Those not saved are left unchanged.</span></span>

<span data-ttu-id="6865e-126">Non è possibile eseguire il push degli attributi in uno stack completo oppure per estrarre gli attributi da uno stack vuoto.</span><span class="sxs-lookup"><span data-stu-id="6865e-126">It is an error to push attributes onto a full stack, or to pop attributes off an empty stack.</span></span> <span data-ttu-id="6865e-127">In entrambi i casi, viene impostato il flag di errore e non viene apportata alcuna modifica allo stato OpenGL.</span><span class="sxs-lookup"><span data-stu-id="6865e-127">In either case, the error flag is set and no other change is made to the OpenGL state.</span></span>

<span data-ttu-id="6865e-128">Inizialmente, lo stack dell'attributo è vuoto.</span><span class="sxs-lookup"><span data-stu-id="6865e-128">Initially, the attribute stack is empty.</span></span>

<span data-ttu-id="6865e-129">Non tutti i valori per lo stato OpenGL possono essere salvati nello stack di attributi.</span><span class="sxs-lookup"><span data-stu-id="6865e-129">Not all values for the OpenGL state can be saved on the attribute stack.</span></span> <span data-ttu-id="6865e-130">Ad esempio, non è possibile salvare lo stato di pixel Pack e unpack, lo stato della modalità di rendering e lo stato di selezione e feedback.</span><span class="sxs-lookup"><span data-stu-id="6865e-130">For example, pixel pack and unpack state, render mode state, and select and feedback state cannot be saved.</span></span>

<span data-ttu-id="6865e-131">La profondità dello stack di attributi dipende dall'implementazione, ma deve essere almeno 16.</span><span class="sxs-lookup"><span data-stu-id="6865e-131">The depth of the attribute stack depends on the implementation, but it must be at least 16.</span></span>

<span data-ttu-id="6865e-132">Le funzioni seguenti recuperano informazioni relative a [**glPushAttrib**](glpushattrib.md) e **glPopAttrib**:</span><span class="sxs-lookup"><span data-stu-id="6865e-132">The following functions retrieve information related to [**glPushAttrib**](glpushattrib.md) and **glPopAttrib**:</span></span>

<span data-ttu-id="6865e-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ \_ profondità dello stack \_ attrib</span><span class="sxs-lookup"><span data-stu-id="6865e-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_ATTRIB\_STACK\_DEPTH</span></span>

<span data-ttu-id="6865e-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento \_ profondità massima \_ \_ dello stack \_ attrib</span><span class="sxs-lookup"><span data-stu-id="6865e-134">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_MAX\_ATTRIB\_STACK\_DEPTH</span></span>

## <a name="requirements"></a><span data-ttu-id="6865e-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6865e-135">Requirements</span></span>



| <span data-ttu-id="6865e-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="6865e-136">Requirement</span></span> | <span data-ttu-id="6865e-137">Valore</span><span class="sxs-lookup"><span data-stu-id="6865e-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6865e-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6865e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6865e-139">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6865e-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6865e-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6865e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6865e-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6865e-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6865e-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6865e-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="6865e-143"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6865e-143"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6865e-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="6865e-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="6865e-145"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6865e-145"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6865e-146">DLL</span><span class="sxs-lookup"><span data-stu-id="6865e-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6865e-147"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6865e-147"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6865e-148">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6865e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6865e-149">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6865e-149">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6865e-150">**Remo**</span><span class="sxs-lookup"><span data-stu-id="6865e-150">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6865e-151">**glGet**</span><span class="sxs-lookup"><span data-stu-id="6865e-151">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="6865e-152">**glGetClipPlane**</span><span class="sxs-lookup"><span data-stu-id="6865e-152">**glGetClipPlane**</span></span>](glgetclipplane.md)
</dt> <dt>

[<span data-ttu-id="6865e-153">**glGetError**</span><span class="sxs-lookup"><span data-stu-id="6865e-153">**glGetError**</span></span>](glgeterror.md)
</dt> <dt>

[<span data-ttu-id="6865e-154">**glGetLight**</span><span class="sxs-lookup"><span data-stu-id="6865e-154">**glGetLight**</span></span>](glgetlight.md)
</dt> <dt>

[<span data-ttu-id="6865e-155">**glGetMap**</span><span class="sxs-lookup"><span data-stu-id="6865e-155">**glGetMap**</span></span>](glgetmap.md)
</dt> <dt>

[<span data-ttu-id="6865e-156">**glGetMaterial**</span><span class="sxs-lookup"><span data-stu-id="6865e-156">**glGetMaterial**</span></span>](glgetmaterial.md)
</dt> <dt>

[<span data-ttu-id="6865e-157">**glGetPixelMap**</span><span class="sxs-lookup"><span data-stu-id="6865e-157">**glGetPixelMap**</span></span>](glgetpixelmap.md)
</dt> <dt>

[<span data-ttu-id="6865e-158">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="6865e-158">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md)
</dt> <dt>

[<span data-ttu-id="6865e-159">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="6865e-159">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="6865e-160">**glGetTexEnv**</span><span class="sxs-lookup"><span data-stu-id="6865e-160">**glGetTexEnv**</span></span>](glgettexenv.md)
</dt> <dt>

[<span data-ttu-id="6865e-161">**glGetTexGen**</span><span class="sxs-lookup"><span data-stu-id="6865e-161">**glGetTexGen**</span></span>](glgettexgen.md)
</dt> <dt>

[<span data-ttu-id="6865e-162">**glGetTexImage**</span><span class="sxs-lookup"><span data-stu-id="6865e-162">**glGetTexImage**</span></span>](glgetteximage.md)
</dt> <dt>

[<span data-ttu-id="6865e-163">**glGetTexLevelParameter**</span><span class="sxs-lookup"><span data-stu-id="6865e-163">**glGetTexLevelParameter**</span></span>](glgettexlevelparameter.md)
</dt> <dt>

[<span data-ttu-id="6865e-164">**glGetTexParameter**</span><span class="sxs-lookup"><span data-stu-id="6865e-164">**glGetTexParameter**</span></span>](glgettexparameter.md)
</dt> <dt>

[<span data-ttu-id="6865e-165">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="6865e-165">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





