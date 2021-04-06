---
title: funzione glCullFace (GL. h)
description: La funzione glCullFace specifica se i facet front-end o back-facet possono essere rivolti.
ms.assetid: 53bf05b5-a68b-4d96-b4e7-2878a0a86a13
keywords:
- funzione glCullFace OpenGL
topic_type:
- apiref
api_name:
- glCullFace
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c20370e0fa8bcf746d1b835ee45725f76158fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963871"
---
# <a name="glcullface-function"></a><span data-ttu-id="ca816-104">glCullFace (funzione)</span><span class="sxs-lookup"><span data-stu-id="ca816-104">glCullFace function</span></span>

<span data-ttu-id="ca816-105">La funzione **glCullFace** specifica se i facet front-end o back-facet possono essere rivolti.</span><span class="sxs-lookup"><span data-stu-id="ca816-105">The **glCullFace** function specifies whether front-facing or back-facing facets can be culled.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca816-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca816-106">Syntax</span></span>


```C++
void WINAPI glCullFace(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="ca816-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca816-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca816-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="ca816-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="ca816-109">Specifica se i facet front-end o back-facing sono candidati per l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="ca816-109">Specifies whether front-facing or back-facing facets are candidates for culling.</span></span> <span data-ttu-id="ca816-110">Vengono accettate le costanti simboliche GL \_ Front, GL \_ back e GL \_ front \_ e \_ back.</span><span class="sxs-lookup"><span data-stu-id="ca816-110">The symbolic constants GL\_FRONT, GL\_BACK, and GL\_FRONT\_AND\_BACK are accepted.</span></span> <span data-ttu-id="ca816-111">Il valore predefinito è GL \_ back.</span><span class="sxs-lookup"><span data-stu-id="ca816-111">The default value is GL\_BACK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca816-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca816-112">Return value</span></span>

<span data-ttu-id="ca816-113">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ca816-113">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ca816-114">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ca816-114">Error codes</span></span>

<span data-ttu-id="ca816-115">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="ca816-115">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ca816-116">Nome</span><span class="sxs-lookup"><span data-stu-id="ca816-116">Name</span></span>                                                                                                  | <span data-ttu-id="ca816-117">Significato</span><span class="sxs-lookup"><span data-stu-id="ca816-117">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ca816-118"><dt>**\_enumerazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ca816-118"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="ca816-119">la *modalità* non è un valore accettato.</span><span class="sxs-lookup"><span data-stu-id="ca816-119">*mode* was not an accepted value.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="ca816-120"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ca816-120"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ca816-121">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ca816-121">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ca816-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="ca816-122">Remarks</span></span>

<span data-ttu-id="ca816-123">La funzione **glCullFace** specifica se i facet front-end o back-facet vengono abbattuti (come specificato dalla *modalità*) quando è abilitata l'eliminazione dei facet.</span><span class="sxs-lookup"><span data-stu-id="ca816-123">The **glCullFace** function specifies whether front-facing or back-facing facets are culled (as specified by *mode*) when facet culling is enabled.</span></span> <span data-ttu-id="ca816-124">È possibile abilitare e disabilitare l'abbattimento dei facet usando [**glEnable**](glenable.md) e [**glDisable**](gldisable.md) con la \_ faccia di abbattimento GL dell'argomento \_ .</span><span class="sxs-lookup"><span data-stu-id="ca816-124">You enable and disable facet culling using [**glEnable**](glenable.md) and [**glDisable**](gldisable.md) with the argument GL\_CULL\_FACE.</span></span> <span data-ttu-id="ca816-125">I facet includono triangoli, quadrilateri, poligoni e rettangoli.</span><span class="sxs-lookup"><span data-stu-id="ca816-125">Facets include triangles, quadrilaterals, polygons, and rectangles.</span></span>

<span data-ttu-id="ca816-126">La funzione [**glFrontFace**](glfrontface.md) specifica quale dei facet in senso orario e in senso antiorario sono rivolti verso il lato anteriore e posteriore.</span><span class="sxs-lookup"><span data-stu-id="ca816-126">The [**glFrontFace**](glfrontface.md) function specifies which of the clockwise and counterclockwise facets are front-facing and back-facing.</span></span>

<span data-ttu-id="ca816-127">Se la *modalità* è GL \_ front \_ e \_ back, non viene disegnato alcun facet, ma vengono disegnate altre primitive, ad esempio punti e linee.</span><span class="sxs-lookup"><span data-stu-id="ca816-127">If *mode* is GL\_FRONT\_AND\_BACK, no facets are drawn, but other primitives, such as points and lines, are drawn.</span></span>

<span data-ttu-id="ca816-128">Le funzioni seguenti consentono di recuperare informazioni correlate a **glCullFace**:</span><span class="sxs-lookup"><span data-stu-id="ca816-128">The following functions retrieve information related to **glCullFace**:</span></span>

<span data-ttu-id="ca816-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con la \_ modalità della \_ faccia abbattimento GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="ca816-129">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_CULL\_FACE\_MODE</span></span>

<span data-ttu-id="ca816-130">[**glIsEnabled**](glisenabled.md) con l'argomento relativo alla selezione degli \_ argomenti GL \_</span><span class="sxs-lookup"><span data-stu-id="ca816-130">[**glIsEnabled**](glisenabled.md) with argument GL\_CULL\_FACE</span></span>

## <a name="requirements"></a><span data-ttu-id="ca816-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca816-131">Requirements</span></span>



| <span data-ttu-id="ca816-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca816-132">Requirement</span></span> | <span data-ttu-id="ca816-133">Valore</span><span class="sxs-lookup"><span data-stu-id="ca816-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca816-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca816-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ca816-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ca816-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ca816-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca816-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ca816-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ca816-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ca816-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca816-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca816-139"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca816-139"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ca816-140">Libreria</span><span class="sxs-lookup"><span data-stu-id="ca816-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="ca816-141"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca816-141"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ca816-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ca816-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca816-143"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca816-143"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca816-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca816-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca816-145">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ca816-145">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ca816-146">**glDisable**</span><span class="sxs-lookup"><span data-stu-id="ca816-146">**glDisable**</span></span>](gldisable.md)
</dt> <dt>

[<span data-ttu-id="ca816-147">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="ca816-147">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="ca816-148">**Remo**</span><span class="sxs-lookup"><span data-stu-id="ca816-148">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="ca816-149">**glFrontFace**</span><span class="sxs-lookup"><span data-stu-id="ca816-149">**glFrontFace**</span></span>](glfrontface.md)
</dt> <dt>

[<span data-ttu-id="ca816-150">**glGet**</span><span class="sxs-lookup"><span data-stu-id="ca816-150">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="ca816-151">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="ca816-151">**glIsEnabled**</span></span>](glisenabled.md)
</dt> </dl>

 

 





