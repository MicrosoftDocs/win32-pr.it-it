---
title: funzione glScissor (GL. h)
description: La funzione glScissor definisce la casella a forbice.
ms.assetid: c06a1d20-bf7b-4283-b0fe-8bd80bece4ce
keywords:
- funzione glScissor OpenGL
topic_type:
- apiref
api_name:
- glScissor
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e18559bb30260dcb4285980d8dc75642a7c9ec6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479132"
---
# <a name="glscissor-function"></a><span data-ttu-id="6bba5-104">glScissor (funzione)</span><span class="sxs-lookup"><span data-stu-id="6bba5-104">glScissor function</span></span>

<span data-ttu-id="6bba5-105">La funzione **glScissor** definisce la casella a forbice.</span><span class="sxs-lookup"><span data-stu-id="6bba5-105">The **glScissor** function defines the scissor box.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bba5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6bba5-106">Syntax</span></span>


```C++
void WINAPI glScissor(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="6bba5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6bba5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bba5-108">*x*</span><span class="sxs-lookup"><span data-stu-id="6bba5-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="6bba5-109">Coordinata x (asse verticale) dell'angolo inferiore sinistro della casella a forbice.</span><span class="sxs-lookup"><span data-stu-id="6bba5-109">The x (vertical axis) coordinate for the lower-left corner of the scissor box.</span></span>

</dd> <dt>

<span data-ttu-id="6bba5-110">*y*</span><span class="sxs-lookup"><span data-stu-id="6bba5-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="6bba5-111">Coordinata y (asse orizzontale) per l'angolo inferiore sinistro della casella a forbice.</span><span class="sxs-lookup"><span data-stu-id="6bba5-111">The y (horizontal axis) coordinate for the lower-left corner of the scissor box.</span></span> <span data-ttu-id="6bba5-112">Insieme, x e y specificano l'angolo inferiore sinistro della casella a forbice.</span><span class="sxs-lookup"><span data-stu-id="6bba5-112">Together, x and y specify the lower-left corner of the scissor box.</span></span> <span data-ttu-id="6bba5-113">Inizialmente (0,0).</span><span class="sxs-lookup"><span data-stu-id="6bba5-113">Initially (0,0).</span></span>

</dd> <dt>

<span data-ttu-id="6bba5-114">*width*</span><span class="sxs-lookup"><span data-stu-id="6bba5-114">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="6bba5-115">Larghezza della casella a forbice.</span><span class="sxs-lookup"><span data-stu-id="6bba5-115">The width of the scissor box.</span></span>

</dd> <dt>

<span data-ttu-id="6bba5-116">*height*</span><span class="sxs-lookup"><span data-stu-id="6bba5-116">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="6bba5-117">Altezza della casella a forbice.</span><span class="sxs-lookup"><span data-stu-id="6bba5-117">The height of the scissor box.</span></span> <span data-ttu-id="6bba5-118">Quando un contesto OpenGL viene collegato per la *prima volta* a una finestra, la *larghezza* e l' *altezza* vengono impostate sulle dimensioni della finestra.</span><span class="sxs-lookup"><span data-stu-id="6bba5-118">When an OpenGL context is *first* attached to a window, *width* and *height* are set to the dimensions of that window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bba5-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6bba5-119">Return value</span></span>

<span data-ttu-id="6bba5-120">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="6bba5-120">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6bba5-121">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="6bba5-121">Error codes</span></span>

<span data-ttu-id="6bba5-122">Il codice di errore seguente può essere recuperato dalla funzione [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="6bba5-122">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="6bba5-123">Nome</span><span class="sxs-lookup"><span data-stu-id="6bba5-123">Name</span></span>                                                                                                  | <span data-ttu-id="6bba5-124">Significato</span><span class="sxs-lookup"><span data-stu-id="6bba5-124">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6bba5-125"><dt>**\_valore GL non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6bba5-125"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="6bba5-126">La *larghezza* o l' *altezza* è negativa.</span><span class="sxs-lookup"><span data-stu-id="6bba5-126">Either *width* or *height* was negative.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="6bba5-127"><dt>**\_operazione GL non valida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6bba5-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="6bba5-128">La funzione è stata chiamata tra una chiamata a [**glBegin**](glbegin.md) e la chiamata corrispondente a [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="6bba5-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="6bba5-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="6bba5-129">Remarks</span></span>

<span data-ttu-id="6bba5-130">La funzione **glScissor** definisce un rettangolo, denominato casella Scissor, nelle coordinate della finestra.</span><span class="sxs-lookup"><span data-stu-id="6bba5-130">The **glScissor** function defines a rectangle, called the scissor box, in window coordinates.</span></span> <span data-ttu-id="6bba5-131">I primi due parametri, *x* e *y*, specificano l'angolo inferiore sinistro della casella.</span><span class="sxs-lookup"><span data-stu-id="6bba5-131">The first two parameters, *x* and *y*, specify the lower-left corner of the box.</span></span> <span data-ttu-id="6bba5-132">I parametri *Width* e *Height* specificano la larghezza e l'altezza della casella.</span><span class="sxs-lookup"><span data-stu-id="6bba5-132">The *width* and *height* parameters specify the width and height of the box.</span></span>

<span data-ttu-id="6bba5-133">Il test a forbice viene abilitato e disabilitato usando [**glEnable**](glenable.md) e **glDisable** con l'argomento \_ test a forbice GL \_ .</span><span class="sxs-lookup"><span data-stu-id="6bba5-133">The scissor test is enabled and disabled using [**glEnable**](glenable.md) and **glDisable** with argument GL\_SCISSOR\_TEST.</span></span> <span data-ttu-id="6bba5-134">Mentre il test di scissor è abilitato, è possibile modificare solo i pixel che si trovano all'interno della casella di forbice disegnando comandi.</span><span class="sxs-lookup"><span data-stu-id="6bba5-134">While the scissor test is enabled, only pixels that lie within the scissor box can be modified by drawing commands.</span></span> <span data-ttu-id="6bba5-135">Le coordinate della finestra hanno valori integer negli angoli condivisi dei pixel del framebuffer, quindi **glScissor**(0, 0, 1, 1) consente di modificare solo il pixel inferiore sinistro della finestra e **glScissor**(0, 0, 0, 0) non consente la modifica a tutti i pixel nella finestra.</span><span class="sxs-lookup"><span data-stu-id="6bba5-135">Window coordinates have integer values at the shared corners of framebuffer pixels, so **glScissor**(0,0,1,1) allows only the lower-left pixel in the window to be modified, and **glScissor**(0,0,0,0) disallows modification to all pixels in the window.</span></span>

<span data-ttu-id="6bba5-136">Quando il test di scissor è disabilitato, è come se la casella Scissor includa l'intera finestra.</span><span class="sxs-lookup"><span data-stu-id="6bba5-136">When the scissor test is disabled, it is as though the scissor box includes the entire window.</span></span>

<span data-ttu-id="6bba5-137">Le funzioni seguenti consentono di recuperare informazioni correlate a **glScissor**:</span><span class="sxs-lookup"><span data-stu-id="6bba5-137">The following functions retrieve information related to **glScissor**:</span></span>

<span data-ttu-id="6bba5-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argomento GL \_ Scissor \_ Box</span><span class="sxs-lookup"><span data-stu-id="6bba5-138">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_SCISSOR\_BOX</span></span>

<span data-ttu-id="6bba5-139">[**glIsEnabled**](glisenabled.md) con test della \_ forbice GL argomento \_</span><span class="sxs-lookup"><span data-stu-id="6bba5-139">[**glIsEnabled**](glisenabled.md) with argument GL\_SCISSOR\_TEST</span></span>

## <a name="requirements"></a><span data-ttu-id="6bba5-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6bba5-140">Requirements</span></span>



| <span data-ttu-id="6bba5-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bba5-141">Requirement</span></span> | <span data-ttu-id="6bba5-142">Valore</span><span class="sxs-lookup"><span data-stu-id="6bba5-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6bba5-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6bba5-143">Minimum supported client</span></span><br/> | <span data-ttu-id="6bba5-144">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6bba5-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6bba5-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6bba5-145">Minimum supported server</span></span><br/> | <span data-ttu-id="6bba5-146">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6bba5-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6bba5-147">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6bba5-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bba5-148"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bba5-148"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6bba5-149">Libreria</span><span class="sxs-lookup"><span data-stu-id="6bba5-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="6bba5-150"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6bba5-150"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6bba5-151">DLL</span><span class="sxs-lookup"><span data-stu-id="6bba5-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6bba5-152"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bba5-152"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bba5-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6bba5-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bba5-154">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6bba5-154">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6bba5-155">**glEnable**</span><span class="sxs-lookup"><span data-stu-id="6bba5-155">**glEnable**</span></span>](glenable.md)
</dt> <dt>

[<span data-ttu-id="6bba5-156">**Remo**</span><span class="sxs-lookup"><span data-stu-id="6bba5-156">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="6bba5-157">**glIsEnabled**</span><span class="sxs-lookup"><span data-stu-id="6bba5-157">**glIsEnabled**</span></span>](glisenabled.md)
</dt> <dt>

[<span data-ttu-id="6bba5-158">**glViewport**</span><span class="sxs-lookup"><span data-stu-id="6bba5-158">**glViewport**</span></span>](glviewport.md)
</dt> </dl>

 

 





