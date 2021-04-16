---
title: funzione glViewport (GL. h)
description: La funzione glViewport imposta il viewport.
ms.assetid: 11816b2f-ee18-42ef-a782-2e96699dd087
keywords:
- funzione glViewport OpenGL
topic_type:
- apiref
api_name:
- glViewport
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5e8eedb9c66211deda92ef6a84e8c1dd2073362
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104556678"
---
# <a name="glviewport-function"></a><span data-ttu-id="ee7b0-104">glViewport (funzione)</span><span class="sxs-lookup"><span data-stu-id="ee7b0-104">glViewport function</span></span>

<span data-ttu-id="ee7b0-105">La funzione **glViewport** imposta il viewport.</span><span class="sxs-lookup"><span data-stu-id="ee7b0-105">The **glViewport** function sets the viewport.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee7b0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ee7b0-106">Syntax</span></span>


```C++
void WINAPI glViewport(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="ee7b0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee7b0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee7b0-108">*x*</span><span class="sxs-lookup"><span data-stu-id="ee7b0-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="ee7b0-109">Angolo inferiore sinistro del rettangolo del viewport, in pixel.</span><span class="sxs-lookup"><span data-stu-id="ee7b0-109">The lower-left corner of the viewport rectangle, in pixels.</span></span> <span data-ttu-id="ee7b0-110">Il valore predefinito è (0,0).</span><span class="sxs-lookup"><span data-stu-id="ee7b0-110">The default is (0,0).</span></span>

</dd> <dt>

<span data-ttu-id="ee7b0-111">*y*</span><span class="sxs-lookup"><span data-stu-id="ee7b0-111">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="ee7b0-112">Angolo inferiore sinistro del rettangolo del viewport, in pixel.</span><span class="sxs-lookup"><span data-stu-id="ee7b0-112">The lower-left corner of the viewport rectangle, in pixels.</span></span> <span data-ttu-id="ee7b0-113">Il valore predefinito è (0,0).</span><span class="sxs-lookup"><span data-stu-id="ee7b0-113">The default is (0,0).</span></span>

</dd> <dt>

<span data-ttu-id="ee7b0-114">*width*</span><span class="sxs-lookup"><span data-stu-id="ee7b0-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="ee7b0-115">Larghezza del riquadro di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="ee7b0-115">The width of the viewport.</span></span> <span data-ttu-id="ee7b0-116">Quando un contesto OpenGL viene collegato per la prima volta a una finestra, la *larghezza* e l' *altezza* vengono impostate sulle dimensioni della finestra.</span><span class="sxs-lookup"><span data-stu-id="ee7b0-116">When an OpenGL context is first attached to a window, *width* and *height* are set to the dimensions of that window.</span></span>

</dd> <dt>

<span data-ttu-id="ee7b0-117">*height*</span><span class="sxs-lookup"><span data-stu-id="ee7b0-117">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="ee7b0-118">Altezza del riquadro di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="ee7b0-118">The height of the viewport.</span></span> <span data-ttu-id="ee7b0-119">Quando un contesto OpenGL viene collegato per la prima volta a una finestra, la *larghezza* e l' *altezza* vengono impostate sulle dimensioni della finestra.</span><span class="sxs-lookup"><span data-stu-id="ee7b0-119">When an OpenGL context is first attached to a window, *width* and *height* are set to the dimensions of that window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee7b0-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ee7b0-120">Return value</span></span>

<span data-ttu-id="ee7b0-121">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ee7b0-121">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ee7b0-122">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="ee7b0-122">Error codes</span></span>

<span data-ttu-id="ee7b0-123">I codici di errore seguenti possono essere recuperati dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="ee7b0-123">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="ee7b0-124">Nome</span><span class="sxs-lookup"><span data-stu-id="ee7b0-124">Name</span></span>                                                                                                  | <span data-ttu-id="ee7b0-125">Significato</span><span class="sxs-lookup"><span data-stu-id="ee7b0-125">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ee7b0-126"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ee7b0-126"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="ee7b0-127">La *larghezza* o l' *altezza* è negativa.</span><span class="sxs-lookup"><span data-stu-id="ee7b0-127">Either *width* or *height* was negative.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="ee7b0-128"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ee7b0-128"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="ee7b0-129">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="ee7b0-129">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ee7b0-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee7b0-130">Remarks</span></span>

<span data-ttu-id="ee7b0-131">La funzione **glViewport** specifica la trasformazione affine di *x* e *y* dalle coordinate del dispositivo normalizzate alle coordinate della finestra.</span><span class="sxs-lookup"><span data-stu-id="ee7b0-131">The **glViewport** function specifies the affine transformation of *x* and *y* from normalized device coordinates to window coordinates.</span></span> <span data-ttu-id="ee7b0-132">Let (*x*<sub>ND</sub> , *y*<sub>ND</sub> ) sono coordinate del dispositivo normalizzate.</span><span class="sxs-lookup"><span data-stu-id="ee7b0-132">Let (*x*<sub>nd</sub> , *y*<sub>nd</sub> ) be normalized device coordinates.</span></span> <span data-ttu-id="ee7b0-133">Le coordinate della finestra (*x*<sub>w</sub> , *y*<sub>w</sub> ) vengono quindi calcolate come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="ee7b0-133">The window coordinates (*x*<sub>w</sub> , *y*<sub>w</sub> ) are then computed as follows:</span></span>

![Equazione che mostra il calcolo delle coordinate della finestra.](images/view01.png)

<span data-ttu-id="ee7b0-135">La larghezza e l'altezza del viewport vengono automaticamente fissate a un intervallo che dipende dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="ee7b0-135">Viewport width and height are silently clamped to a range that depends on the implementation.</span></span> <span data-ttu-id="ee7b0-136">Viene eseguita una query su questo intervallo chiamando **glGet** con argomento GL \_ Max \_ viewport \_ Dim.</span><span class="sxs-lookup"><span data-stu-id="ee7b0-136">This range is queried by calling **glGet** with argument GL\_MAX\_VIEWPORT\_DIMS.</span></span>

<span data-ttu-id="ee7b0-137">Le funzioni seguenti consentono di recuperare informazioni correlate a **glViewport**:</span><span class="sxs-lookup"><span data-stu-id="ee7b0-137">The following functions retrieve information related to **glViewport**:</span></span>

<span data-ttu-id="ee7b0-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con viewport GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="ee7b0-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_VIEWPORT</span></span>

<span data-ttu-id="ee7b0-139">**glGet** con l'argomento \_ numero massimo di \_ finestre di visualizzazione \_ Dim</span><span class="sxs-lookup"><span data-stu-id="ee7b0-139">**glGet** with argument GL\_MAX\_VIEWPORT\_DIMS</span></span>

## <a name="requirements"></a><span data-ttu-id="ee7b0-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee7b0-140">Requirements</span></span>



| <span data-ttu-id="ee7b0-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee7b0-141">Requirement</span></span> | <span data-ttu-id="ee7b0-142">Valore</span><span class="sxs-lookup"><span data-stu-id="ee7b0-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee7b0-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee7b0-143">Minimum supported client</span></span><br/> | <span data-ttu-id="ee7b0-144">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ee7b0-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ee7b0-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ee7b0-145">Minimum supported server</span></span><br/> | <span data-ttu-id="ee7b0-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ee7b0-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ee7b0-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ee7b0-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee7b0-148"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee7b0-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="ee7b0-149">Libreria</span><span class="sxs-lookup"><span data-stu-id="ee7b0-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="ee7b0-150"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee7b0-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ee7b0-151">DLL</span><span class="sxs-lookup"><span data-stu-id="ee7b0-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee7b0-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee7b0-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee7b0-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee7b0-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee7b0-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="ee7b0-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="ee7b0-155">**glDepthRange**</span><span class="sxs-lookup"><span data-stu-id="ee7b0-155">**glDepthRange**</span></span>](gldepthrange.md)
</dt> </dl>

 

 





