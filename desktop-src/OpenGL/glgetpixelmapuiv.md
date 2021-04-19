---
title: funzione glGetPixelMapuiv (GL. h)
description: Le funzioni glGetPixelMapfv, glGetPixelMapuiv e glGetPixelMapusv restituiscono la mappa pixel specificata. | funzione glGetPixelMapuiv (GL. h)
ms.assetid: a49f5fd2-c350-4acc-8f61-ecb92b0164cc
keywords:
- funzione glGetPixelMapuiv OpenGL
topic_type:
- apiref
api_name:
- glGetPixelMapuiv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c017e7601e074c588aa534b6ea90aef79325ed4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321418"
---
# <a name="glgetpixelmapuiv-function"></a><span data-ttu-id="89e62-105">glGetPixelMapuiv (funzione)</span><span class="sxs-lookup"><span data-stu-id="89e62-105">glGetPixelMapuiv function</span></span>

<span data-ttu-id="89e62-106">Le funzioni [**glGetPixelMapfv**](glgetpixelmapfv.md), **glGetPixelMapuiv** e [**glGetPixelMapusv**](glgetpixelmapusv.md) restituiscono la mappa pixel specificata.</span><span class="sxs-lookup"><span data-stu-id="89e62-106">The [**glGetPixelMapfv**](glgetpixelmapfv.md), **glGetPixelMapuiv**, and [**glGetPixelMapusv**](glgetpixelmapusv.md) functions return the specified pixel map.</span></span>

## <a name="syntax"></a><span data-ttu-id="89e62-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89e62-107">Syntax</span></span>


```C++
void WINAPI glGetPixelMapuiv(
   GLenum map,
   GLuint *values
);
```



## <a name="parameters"></a><span data-ttu-id="89e62-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="89e62-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89e62-109">*map*</span><span class="sxs-lookup"><span data-stu-id="89e62-109">*map*</span></span> 
</dt> <dd>

<span data-ttu-id="89e62-110">Nome della mappa dei pixel da restituire.</span><span class="sxs-lookup"><span data-stu-id="89e62-110">The name of the pixel map to return.</span></span> <span data-ttu-id="89e62-111">I valori accettati sono GL \_ pixel \_ Map \_ i to \_ \_ i, GL \_ pixel \_ Map \_ S \_ to \_ S, GL \_ pixel \_ Map \_ i \_ to \_ R, GL \_ pixel \_ Map \_ i \_ to \_ g, GL \_ pixel \_ Map \_ i \_ a \_ b, GL \_ pixel \_ Map \_ i \_ to \_ a, GL \_ pixel \_ Map \_ r \_ to \_ r, GL \_ pixel map \_ \_ g \_ to \_ g, GL \_ pixel map \_ \_ B \_ to \_ b e \_ GL \_ pixel \_ \_ \_ Map a.</span><span class="sxs-lookup"><span data-stu-id="89e62-111">Accepted values are GL\_PIXEL\_MAP\_I\_TO\_I, GL\_PIXEL\_MAP\_S\_TO\_S, GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, GL\_PIXEL\_MAP\_I\_TO\_A, GL\_PIXEL\_MAP\_R\_TO\_R, GL\_PIXEL\_MAP\_G\_TO\_G, GL\_PIXEL\_MAP\_B\_TO\_B, and GL\_PIXEL\_MAP\_A\_TO\_A.</span></span>

</dd> <dt>

<span data-ttu-id="89e62-112">*valori*</span><span class="sxs-lookup"><span data-stu-id="89e62-112">*values*</span></span> 
</dt> <dd>

<span data-ttu-id="89e62-113">Restituisce il contenuto della mappa pixel.</span><span class="sxs-lookup"><span data-stu-id="89e62-113">Returns the pixel map contents.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89e62-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89e62-114">Return value</span></span>

<span data-ttu-id="89e62-115">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="89e62-115">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="89e62-116">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="89e62-116">Error codes</span></span>

<span data-ttu-id="89e62-117">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="89e62-117">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="89e62-118">Nome</span><span class="sxs-lookup"><span data-stu-id="89e62-118">Name</span></span>                                                                                                  | <span data-ttu-id="89e62-119">Significato</span><span class="sxs-lookup"><span data-stu-id="89e62-119">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="89e62-120"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="89e62-120"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="89e62-121">il *mapping* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="89e62-121">*map* was not an accepted value.</span></span><br/>                                                                                           |
| <dl> <span data-ttu-id="89e62-122"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="89e62-122"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="89e62-123">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="89e62-123">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="89e62-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="89e62-124">Remarks</span></span>

<span data-ttu-id="89e62-125">Per una descrizione dei valori accettabili per il parametro *Map* , vedere [**glPixelMap**](glpixelmap.md) .</span><span class="sxs-lookup"><span data-stu-id="89e62-125">See [**glPixelMap**](glpixelmap.md) for a description of the acceptable values for the *map* parameter.</span></span> <span data-ttu-id="89e62-126">La funzione **glGetPixelMap** restituisce in *valori* il contenuto della mappa pixel specificata in *Map*.</span><span class="sxs-lookup"><span data-stu-id="89e62-126">The **glGetPixelMap** function returns in *values* the contents of the pixel map specified in *map*.</span></span> <span data-ttu-id="89e62-127">Usare i mapping dei pixel durante l'esecuzione di [**glReadPixels**](glreadpixels.md), [**glDrawPixels**](gldrawpixels.md), [**glCopyPixels**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md)e [**glTexImage2D**](glteximage2d.md) per eseguire il mapping degli indici di colore, degli stencil, dei componenti dei colori e dei componenti di profondità ad altri valori.</span><span class="sxs-lookup"><span data-stu-id="89e62-127">Use pixel maps during the execution of [**glReadPixels**](glreadpixels.md), [**glDrawPixels**](gldrawpixels.md), [**glCopyPixels**](glcopypixels.md), [**glTexImage1D**](glteximage1d.md), and [**glTexImage2D**](glteximage2d.md) to map color indexes, stencil indexes, color components, and depth components to other values.</span></span>

<span data-ttu-id="89e62-128">I valori interi senza segno, se richiesti, vengono mappati linearmente dalla rappresentazione a virgola fissa o a virgola mobile interna, in modo che 1,0 sia mappata al valore integer rappresentabile più grande e 0,0 venga eseguito il mapping a zero.</span><span class="sxs-lookup"><span data-stu-id="89e62-128">Unsigned integer values, if requested, are linearly mapped from the internal fixed or floating-point representation such that 1.0 maps to the largest representable integer value, and 0.0 maps to zero.</span></span> <span data-ttu-id="89e62-129">I valori restituiti Unsigned Integer non sono definiti se il valore della mappa non è compreso nell'intervallo \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="89e62-129">Return unsigned integer values are undefined if the map value was not in the range \[0,1\].</span></span>

<span data-ttu-id="89e62-130">Per determinare la dimensione richiesta della *mappa*, chiamare [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con la costante simbolica appropriata.</span><span class="sxs-lookup"><span data-stu-id="89e62-130">To determine the required size of *map*, call [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with the appropriate symbolic constant.</span></span>

<span data-ttu-id="89e62-131">Se viene generato un errore, non viene apportata alcuna modifica al contenuto dei *valori*.</span><span class="sxs-lookup"><span data-stu-id="89e62-131">If an error is generated, no change is made to the contents of *values*.</span></span>

<span data-ttu-id="89e62-132">Le funzioni seguenti consentono di recuperare informazioni correlate a **glGetPixelMap**:</span><span class="sxs-lookup"><span data-stu-id="89e62-132">The following functions retrieve information related to **glGetPixelMap**:</span></span>

<span data-ttu-id="89e62-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ pixel \_ Map \_ i \_ to \_ i \_ size</span><span class="sxs-lookup"><span data-stu-id="89e62-133">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PIXEL\_MAP\_I\_TO\_I\_SIZE</span></span>

<span data-ttu-id="89e62-134">**glGet** con argomento \_ \_ di mapping GL pixel per la \_ \_ \_ \_ dimensione s</span><span class="sxs-lookup"><span data-stu-id="89e62-134">**glGet** with argument GL\_PIXEL\_MAP\_S\_TO\_S\_SIZE</span></span>

<span data-ttu-id="89e62-135">**glGet** con argomento GL \_ pixel \_ Map \_ I \_ to \_ R \_ size</span><span class="sxs-lookup"><span data-stu-id="89e62-135">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_R\_SIZE</span></span>

<span data-ttu-id="89e62-136">**glGet** con argomento GL \_ pixel \_ mapping \_ I \_ a \_ G \_ size</span><span class="sxs-lookup"><span data-stu-id="89e62-136">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_G\_SIZE</span></span>

<span data-ttu-id="89e62-137">**glGet** con argomento GL \_ pixel \_ Map \_ I \_ a \_ B \_ size</span><span class="sxs-lookup"><span data-stu-id="89e62-137">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_B\_SIZE</span></span>

<span data-ttu-id="89e62-138">**glGet** con argomento GL \_ pixel \_ mappa \_ I \_ a \_ una \_ dimensione</span><span class="sxs-lookup"><span data-stu-id="89e62-138">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_A\_SIZE</span></span>

<span data-ttu-id="89e62-139">**glGet** con argomento GL \_ pixel \_ Map \_ r \_ to \_ r \_ size</span><span class="sxs-lookup"><span data-stu-id="89e62-139">**glGet** with argument GL\_PIXEL\_MAP\_R\_TO\_R\_SIZE</span></span>

<span data-ttu-id="89e62-140">**glGet** con argomento GL \_ pixel \_ mappa \_ g \_ a \_ g \_ size</span><span class="sxs-lookup"><span data-stu-id="89e62-140">**glGet** with argument GL\_PIXEL\_MAP\_G\_TO\_G\_SIZE</span></span>

<span data-ttu-id="89e62-141">**glGet** con argomento GL \_ pixel \_ mappa \_ b \_ a \_ b \_ dimensioni</span><span class="sxs-lookup"><span data-stu-id="89e62-141">**glGet** with argument GL\_PIXEL\_MAP\_B\_TO\_B\_SIZE</span></span>

<span data-ttu-id="89e62-142">**glGet** con argomento GL \_ pixel \_ mappa \_ a \_ \_ una \_ dimensione</span><span class="sxs-lookup"><span data-stu-id="89e62-142">**glGet** with argument GL\_PIXEL\_MAP\_A\_TO\_A\_SIZE</span></span>

<span data-ttu-id="89e62-143">**glGet** con argomento \_ tabella di \_ mappa pixel max \_ \_</span><span class="sxs-lookup"><span data-stu-id="89e62-143">**glGet** with argument GL\_MAX\_PIXEL\_MAP\_TABLE</span></span>

## <a name="requirements"></a><span data-ttu-id="89e62-144">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89e62-144">Requirements</span></span>



| <span data-ttu-id="89e62-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="89e62-145">Requirement</span></span> | <span data-ttu-id="89e62-146">Valore</span><span class="sxs-lookup"><span data-stu-id="89e62-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89e62-147">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89e62-147">Minimum supported client</span></span><br/> | <span data-ttu-id="89e62-148">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="89e62-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="89e62-149">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89e62-149">Minimum supported server</span></span><br/> | <span data-ttu-id="89e62-150">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="89e62-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="89e62-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="89e62-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="89e62-152"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="89e62-152"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="89e62-153">Libreria</span><span class="sxs-lookup"><span data-stu-id="89e62-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="89e62-154"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="89e62-154"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="89e62-155">DLL</span><span class="sxs-lookup"><span data-stu-id="89e62-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89e62-156"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89e62-156"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89e62-157">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89e62-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89e62-158">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="89e62-158">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="89e62-159">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="89e62-159">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="89e62-160">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="89e62-160">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="89e62-161">**Remo**</span><span class="sxs-lookup"><span data-stu-id="89e62-161">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="89e62-162">**glGet**</span><span class="sxs-lookup"><span data-stu-id="89e62-162">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="89e62-163">**glPixelMap**</span><span class="sxs-lookup"><span data-stu-id="89e62-163">**glPixelMap**</span></span>](glpixelmap.md)
</dt> <dt>

[<span data-ttu-id="89e62-164">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="89e62-164">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="89e62-165">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="89e62-165">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="89e62-166">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="89e62-166">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="89e62-167">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="89e62-167">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





