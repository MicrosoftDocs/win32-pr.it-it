---
title: funzione glHint (GL. h)
description: La funzione glHint specifica hint specifici dell'implementazione.
ms.assetid: 6d03e107-321a-45ee-9ce7-25fa9cab32d9
keywords:
- funzione glHint OpenGL
topic_type:
- apiref
api_name:
- glHint
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2772c76868c741660486184e5ab51bd193d3667a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119303"
---
# <a name="glhint-function"></a><span data-ttu-id="7fc39-104">glHint (funzione)</span><span class="sxs-lookup"><span data-stu-id="7fc39-104">glHint function</span></span>

<span data-ttu-id="7fc39-105">La funzione **glHint** specifica hint specifici dell'implementazione.</span><span class="sxs-lookup"><span data-stu-id="7fc39-105">The **glHint** function specifies implementation-specific hints.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fc39-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7fc39-106">Syntax</span></span>


```C++
void WINAPI glHint(
   GLenum target,
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="7fc39-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7fc39-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fc39-108">*target*</span><span class="sxs-lookup"><span data-stu-id="7fc39-108">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="7fc39-109">Costante simbolica che indica il comportamento da controllare.</span><span class="sxs-lookup"><span data-stu-id="7fc39-109">A symbolic constant indicating the behavior to be controlled.</span></span> <span data-ttu-id="7fc39-110">Vengono accettate le costanti simboliche seguenti, insieme alla semantica suggerita.</span><span class="sxs-lookup"><span data-stu-id="7fc39-110">The following symbolic constants, along with suggested semantics, are accepted.</span></span>



| <span data-ttu-id="7fc39-111">Valore</span><span class="sxs-lookup"><span data-stu-id="7fc39-111">Value</span></span>                                                                                                                                                                                                              | <span data-ttu-id="7fc39-112">Significato</span><span class="sxs-lookup"><span data-stu-id="7fc39-112">Meaning</span></span>                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_HINT"></span><span id="gl_fog_hint"></span><dl> <span data-ttu-id="7fc39-113"><dt>**\_hint di nebbia GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7fc39-113"><dt>**GL\_FOG\_HINT**</dt></span></span> </dl>                                                           | <span data-ttu-id="7fc39-114">Indica l'accuratezza del calcolo di nebbia.</span><span class="sxs-lookup"><span data-stu-id="7fc39-114">Indicates the accuracy of fog calculation.</span></span> <span data-ttu-id="7fc39-115">Se il calcolo della nebbia per pixel non è supportato in modo efficiente dall'implementazione di OpenGL, l'hinting GL \_ dont \_ care o GL più \_ veloci possono determinare un calcolo per vertice degli effetti di nebbia.</span><span class="sxs-lookup"><span data-stu-id="7fc39-115">If per-pixel fog calculation is not efficiently supported by the OpenGL implementation, hinting GL\_DONT\_CARE or GL\_FASTEST can result in per-vertex calculation of fog effects.</span></span><br/>                                                                          |
| <span id="GL_LINE_SMOOTH_HINT"></span><span id="gl_line_smooth_hint"></span><dl> <span data-ttu-id="7fc39-116"><dt>**\_ \_ hint uniforme linea \_ GL**</dt></span><span class="sxs-lookup"><span data-stu-id="7fc39-116"><dt>**GL\_LINE\_SMOOTH\_HINT**</dt></span></span> </dl>                                  | <span data-ttu-id="7fc39-117">Indica la qualità di campionamento delle linee con antialias.</span><span class="sxs-lookup"><span data-stu-id="7fc39-117">Indicates the sampling quality of antialiased lines.</span></span> <span data-ttu-id="7fc39-118">L'hinting GL \_ più gradevole può comportare la generazione di più frammenti di pixel durante la rasterizzazione, se viene applicata una funzione di filtro di dimensioni maggiori.</span><span class="sxs-lookup"><span data-stu-id="7fc39-118">Hinting GL\_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.</span></span><br/>                                                                                                               |
| <span id="GL_PERSPECTIVE_CORRECTION_HINT"></span><span id="gl_perspective_correction_hint"></span><dl> <span data-ttu-id="7fc39-119"><dt>**HINT per la \_ correzione della prospettiva GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7fc39-119"><dt>**GL\_PERSPECTIVE\_CORRECTION\_HINT**</dt></span></span> </dl> | <span data-ttu-id="7fc39-120">Indica la qualità del colore e l'interpolazione delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="7fc39-120">Indicates the quality of color and texture coordinate interpolation.</span></span> <span data-ttu-id="7fc39-121">Se l'interpolazione dei parametri con correzione della prospettiva non è supportata in modo efficiente dall'implementazione di OpenGL, l'hinting GL \_ dont \_ care o GL \_ più veloci possono produrre un'interpolazione lineare semplice di colori e/o coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="7fc39-121">If perspective-corrected parameter interpolation is not efficiently supported by the OpenGL implementation, hinting GL\_DONT\_CARE or GL\_FASTEST can result in simple linear interpolation of colors and/or texture coordinates.</span></span><br/> |
| <span id="GL_POINT_SMOOTH_HINT"></span><span id="gl_point_smooth_hint"></span><dl> <span data-ttu-id="7fc39-122"><dt>**\_ \_ Suggerimento smussato del punto GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7fc39-122"><dt>**GL\_POINT\_SMOOTH\_HINT**</dt></span></span> </dl>                               | <span data-ttu-id="7fc39-123">Indica la qualità di campionamento dei punti antialias.</span><span class="sxs-lookup"><span data-stu-id="7fc39-123">Indicates the sampling quality of antialiased points.</span></span> <span data-ttu-id="7fc39-124">L'hinting GL \_ più gradevole può comportare la generazione di più frammenti di pixel durante la rasterizzazione, se viene applicata una funzione di filtro di dimensioni maggiori.</span><span class="sxs-lookup"><span data-stu-id="7fc39-124">Hinting GL\_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.</span></span><br/>                                                                                                              |
| <span id="GL_POLYGON_SMOOTH_HINT"></span><span id="gl_polygon_smooth_hint"></span><dl> <span data-ttu-id="7fc39-125"><dt>**\_hint Smooth poligono GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7fc39-125"><dt>**GL\_POLYGON\_SMOOTH\_HINT**</dt></span></span> </dl>                         | <span data-ttu-id="7fc39-126">Indica la qualità di campionamento dei poligoni con antialias.</span><span class="sxs-lookup"><span data-stu-id="7fc39-126">Indicates the sampling quality of antialiased polygons.</span></span> <span data-ttu-id="7fc39-127">L'hinting GL \_ più gradevole può comportare la generazione di più frammenti di pixel durante la rasterizzazione, se viene applicata una funzione di filtro di dimensioni maggiori.</span><span class="sxs-lookup"><span data-stu-id="7fc39-127">Hinting GL\_NICEST can result in more pixel fragments being generated during rasterization, if a larger filter function is applied.</span></span><br/>                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="7fc39-128">*mode*</span><span class="sxs-lookup"><span data-stu-id="7fc39-128">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="7fc39-129">Costante simbolica che indica il comportamento desiderato.</span><span class="sxs-lookup"><span data-stu-id="7fc39-129">A symbolic constant indicating the desired behavior.</span></span> <span data-ttu-id="7fc39-130">Vengono accettate le seguenti costanti simboliche.</span><span class="sxs-lookup"><span data-stu-id="7fc39-130">The following symbolic constants are accepted.</span></span>



| <span data-ttu-id="7fc39-131">Valore</span><span class="sxs-lookup"><span data-stu-id="7fc39-131">Value</span></span>                                                                                                                                                       | <span data-ttu-id="7fc39-132">Significato</span><span class="sxs-lookup"><span data-stu-id="7fc39-132">Meaning</span></span>                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="GL_FASTEST"></span><span id="gl_fastest"></span><dl> <span data-ttu-id="7fc39-133"><dt>**CONTABILITÀ più \_ veloce**</dt></span><span class="sxs-lookup"><span data-stu-id="7fc39-133"><dt>**GL\_FASTEST**</dt></span></span> </dl>        | <span data-ttu-id="7fc39-134">È consigliabile scegliere l'opzione più efficiente.</span><span class="sxs-lookup"><span data-stu-id="7fc39-134">The most efficient option should be chosen.</span></span><br/>                    |
| <span id="GL_NICEST"></span><span id="gl_nicest"></span><dl> <span data-ttu-id="7fc39-135"><dt>**GL più \_ bello**</dt></span><span class="sxs-lookup"><span data-stu-id="7fc39-135"><dt>**GL\_NICEST**</dt></span></span> </dl>           | <span data-ttu-id="7fc39-136">È consigliabile scegliere l'opzione più corretta, o di qualità più elevata.</span><span class="sxs-lookup"><span data-stu-id="7fc39-136">The most correct, or highest quality, option should be chosen.</span></span><br/> |
| <span id="GL_DONT_CARE"></span><span id="gl_dont_care"></span><dl> <span data-ttu-id="7fc39-137"><dt>**GL \_ dont \_ care**</dt></span><span class="sxs-lookup"><span data-stu-id="7fc39-137"><dt>**GL\_DONT\_CARE**</dt></span></span> </dl> | <span data-ttu-id="7fc39-138">Il client non ha preferenze.</span><span class="sxs-lookup"><span data-stu-id="7fc39-138">The client doesn't have a preference.</span></span><br/>                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fc39-139">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7fc39-139">Return value</span></span>

<span data-ttu-id="7fc39-140">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="7fc39-140">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7fc39-141">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="7fc39-141">Error codes</span></span>

<span data-ttu-id="7fc39-142">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="7fc39-142">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="7fc39-143">Nome</span><span class="sxs-lookup"><span data-stu-id="7fc39-143">Name</span></span>                                                                                                  | <span data-ttu-id="7fc39-144">Significato</span><span class="sxs-lookup"><span data-stu-id="7fc39-144">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7fc39-145"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7fc39-145"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="7fc39-146">la *destinazione* o la *modalità* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="7fc39-146">*target* or *mode* was not an accepted value.</span></span><br/>                                                                              |
| <dl> <span data-ttu-id="7fc39-147"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7fc39-147"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="7fc39-148">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="7fc39-148">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="7fc39-149">Commenti</span><span class="sxs-lookup"><span data-stu-id="7fc39-149">Remarks</span></span>

<span data-ttu-id="7fc39-150">Quando è disponibile spazio per l'interpretazione, è possibile controllare alcuni aspetti del comportamento di OpenGL con hint.</span><span class="sxs-lookup"><span data-stu-id="7fc39-150">When there is room for interpretation, you can control certain aspects of OpenGL behavior with hints.</span></span> <span data-ttu-id="7fc39-151">È possibile specificare un hint con due argomenti.</span><span class="sxs-lookup"><span data-stu-id="7fc39-151">You specify a hint with two arguments.</span></span> <span data-ttu-id="7fc39-152">Il parametro di *destinazione* è una costante simbolica che indica il comportamento da controllare e la *modalità* è un'altra costante simbolica che indica il comportamento desiderato.</span><span class="sxs-lookup"><span data-stu-id="7fc39-152">The *target* parameter is a symbolic constant indicating the behavior to be controlled, and *mode* is another symbolic constant indicating the desired behavior.</span></span>

<span data-ttu-id="7fc39-153">Sebbene gli aspetti di implementazione che è possibile suggerire siano ben definiti, l'interpretazione degli hint dipende dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="7fc39-153">Though the implementation aspects that can be hinted are well defined, the interpretation of the hints depends on the implementation.</span></span>

<span data-ttu-id="7fc39-154">La funzione **glHint** può essere ignorata.</span><span class="sxs-lookup"><span data-stu-id="7fc39-154">The **glHint** function can be ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fc39-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7fc39-155">Requirements</span></span>



| <span data-ttu-id="7fc39-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fc39-156">Requirement</span></span> | <span data-ttu-id="7fc39-157">Valore</span><span class="sxs-lookup"><span data-stu-id="7fc39-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fc39-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7fc39-158">Minimum supported client</span></span><br/> | <span data-ttu-id="7fc39-159">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7fc39-159">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7fc39-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7fc39-160">Minimum supported server</span></span><br/> | <span data-ttu-id="7fc39-161">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7fc39-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7fc39-162">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7fc39-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fc39-163"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fc39-163"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="7fc39-164">Libreria</span><span class="sxs-lookup"><span data-stu-id="7fc39-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="7fc39-165"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7fc39-165"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="7fc39-166">DLL</span><span class="sxs-lookup"><span data-stu-id="7fc39-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fc39-167"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fc39-167"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fc39-168">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7fc39-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fc39-169">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="7fc39-169">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="7fc39-170">**Remo**</span><span class="sxs-lookup"><span data-stu-id="7fc39-170">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





