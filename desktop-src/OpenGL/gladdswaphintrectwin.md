---
title: funzione glAddSwapHintRectWIN (GL. h)
description: La funzione di callback glAddSwapHintRectWIN specifica un set di rettangoli che devono essere copiati da SwapBuffers.
ms.assetid: f242e755-8e8a-471a-9884-47efa22a3de6
keywords:
- funzione glAddSwapHintRectWIN OpenGL
topic_type:
- apiref
api_name:
- glAddSwapHintRectWIN
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae3e10c2f51ff8d7c9763ff1dad7d09d800cd60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400711"
---
# <a name="gladdswaphintrectwin-function"></a><span data-ttu-id="a4e5e-104">glAddSwapHintRectWIN (funzione)</span><span class="sxs-lookup"><span data-stu-id="a4e5e-104">glAddSwapHintRectWIN function</span></span>

<span data-ttu-id="a4e5e-105">La funzione di callback **glAddSwapHintRectWIN** specifica un set di rettangoli che devono essere copiati da [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span><span class="sxs-lookup"><span data-stu-id="a4e5e-105">The **glAddSwapHintRectWIN** callback function specifies a set of rectangles that are to be copied by [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span></span>

## <a name="syntax"></a><span data-ttu-id="a4e5e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a4e5e-106">Syntax</span></span>


```C++
void WINAPI glAddSwapHintRectWIN(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a><span data-ttu-id="a4e5e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a4e5e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4e5e-108">*x*</span><span class="sxs-lookup"><span data-stu-id="a4e5e-108">*x*</span></span> 
</dt> <dd>

<span data-ttu-id="a4e5e-109">Coordinata *x*(in coordinate della finestra) dell'angolo inferiore sinistro del rettangolo dell'area dell'hint.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-109">The *x*-coordinate (in window coordinates) of the lower-left corner of the hint region rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="a4e5e-110">*y*</span><span class="sxs-lookup"><span data-stu-id="a4e5e-110">*y*</span></span> 
</dt> <dd>

<span data-ttu-id="a4e5e-111">Coordinata *y*(in coordinate della finestra) dell'angolo inferiore sinistro del rettangolo dell'area del suggerimento.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-111">The *y*-coordinate (in window coordinates) of the lower-left corner of the hint region rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="a4e5e-112">*width*</span><span class="sxs-lookup"><span data-stu-id="a4e5e-112">*width*</span></span> 
</dt> <dd>

<span data-ttu-id="a4e5e-113">Larghezza del rettangolo dell'area del suggerimento.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-113">The width of the hint region rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="a4e5e-114">*height*</span><span class="sxs-lookup"><span data-stu-id="a4e5e-114">*height*</span></span> 
</dt> <dd>

<span data-ttu-id="a4e5e-115">Altezza del rettangolo dell'area del suggerimento.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-115">The height of the hint region rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4e5e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a4e5e-116">Return value</span></span>

<span data-ttu-id="a4e5e-117">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4e5e-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="a4e5e-118">Remarks</span></span>

<span data-ttu-id="a4e5e-119">La funzione **glAddSwapHintRectWIN** accelera l'animazione riducendo la quantità di ridisegno tra i frame.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-119">The **glAddSwapHintRectWIN** function speeds up animation by reducing the amount of repainting between frames.</span></span> <span data-ttu-id="a4e5e-120">Con **glAddSwapHintRectWIN** è possibile specificare un set di aree rettangolari che si desidera copiare quando si chiama [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span><span class="sxs-lookup"><span data-stu-id="a4e5e-120">With **glAddSwapHintRectWIN**, you specify a set of rectangular areas that you want copied when you call [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).</span></span> <span data-ttu-id="a4e5e-121">Quando non si specifica alcun rettangolo con **glAddSwapHintRectWIN** prima di chiamare **SwapBuffers**, viene scambiato l'intero framebuffer.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-121">When you do not specify any rectangles with **glAddSwapHintRectWIN** before calling **SwapBuffers**, the entire framebuffer is swapped.</span></span> <span data-ttu-id="a4e5e-122">L'uso di **glAddSwapHintRectWIN** per copiare solo le parti modificate del buffer può migliorare significativamente le prestazioni di **SwapBuffers**, soprattutto quando **SwapBuffers** viene implementato nel software.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-122">Using **glAddSwapHintRectWIN** to copy only changed parts of the buffer can significantly increase the performance of **SwapBuffers**, especially when **SwapBuffers** is implemented in software.</span></span>

<span data-ttu-id="a4e5e-123">La funzione **glAddSwapHintRectWIN** aggiunge un rettangolo all'area del suggerimento.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-123">The **glAddSwapHintRectWIN** function adds a rectangle to the hint region.</span></span> <span data-ttu-id="a4e5e-124">Quando \_ \_ viene impostato il flag di copia di scambio PFD della struttura del formato pixel [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) , **SwapBuffers** usa quest'area per ritagliare la copia del buffer nascosto nel buffer anteriore.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-124">When the PFD\_SWAP\_COPY flag of the [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) pixel format structure is set, **SwapBuffers** uses this region to clip the copying of the back buffer to the front buffer.</span></span> <span data-ttu-id="a4e5e-125">Non viene specificata \_ \_ la copia di scambio PFD, che viene impostata da hardware idoneo.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-125">You don't specify PFD\_SWAP\_COPY; it is set by capable hardware.</span></span> <span data-ttu-id="a4e5e-126">L'area del suggerimento viene cancellata dopo ogni chiamata a **SwapBuffers**.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-126">The hint region is cleared after each call to **SwapBuffers**.</span></span> <span data-ttu-id="a4e5e-127">Con alcune configurazioni hardware, **SwapBuffers** può ignorare l'area del suggerimento ed scambiare l'intero buffer.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-127">With some hardware configurations, **SwapBuffers** can ignore the hint region and exchange the entire buffer.</span></span> <span data-ttu-id="a4e5e-128">**SwapBuffers** viene implementato dal sistema e non dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-128">**SwapBuffers** is implemented by the system, not by the application.</span></span>

<span data-ttu-id="a4e5e-129">OpenGL mantiene un'area di hint separata per ogni finestra.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-129">OpenGL maintains a separate hint region for each window.</span></span> <span data-ttu-id="a4e5e-130">Quando si chiama **glAddSwapHintRectWIN** in tutti i contesti di rendering associati a una finestra, i rettangoli di hint vengono combinati in una singola area.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-130">When you call **glAddSwapHintRectWIN** on any rendering contexts associated with a window, the hint rectangles are combined into a single region.</span></span>

<span data-ttu-id="a4e5e-131">Chiamare **glAddSwapHintRectWIN** con un rettangolo di delimitazione per ogni oggetto disegnato per un frame e per ogni rettangolo cancellato per cancellare gli oggetti frame precedenti.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-131">Call **glAddSwapHintRectWIN** with a bounding rectangle for each object drawn for a frame and for each rectangle cleared to erase previous frame objects.</span></span>

> [!Note]  
> <span data-ttu-id="a4e5e-132">La funzione **glAddSwapHintRectWIN** è una funzione di estensione che non fa parte della libreria OpenGL standard, ma fa parte dell' \_ estensione dell' \_ hint di scambio GL Win \_ .</span><span class="sxs-lookup"><span data-stu-id="a4e5e-132">The **glAddSwapHintRectWIN** function is an extension function that is not part of the standard OpenGL library but is part of the GL\_WIN\_swap\_hint extension.</span></span> <span data-ttu-id="a4e5e-133">Per verificare se l'implementazione di OpenGL supporta **glAddSwapHintRectWIN**, chiamare **glGetString**(GL \_ Extensions).</span><span class="sxs-lookup"><span data-stu-id="a4e5e-133">To check whether your implementation of OpenGL supports **glAddSwapHintRectWIN**, call **glGetString**(GL\_EXTENSIONS).</span></span> <span data-ttu-id="a4e5e-134">Se restituisce l'hint per lo \_ scambio di vittorie GL \_ \_ , **glAddSwapHintRectWIN** è supportato.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-134">If it returns GL\_WIN\_swap\_hint, **glAddSwapHintRectWIN** is supported.</span></span> <span data-ttu-id="a4e5e-135">Per ottenere l'indirizzo di una funzione di estensione, chiamare **wglGetProcAddress**.</span><span class="sxs-lookup"><span data-stu-id="a4e5e-135">To obtain the address of an extension function, call **wglGetProcAddress**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a4e5e-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a4e5e-136">Requirements</span></span>



| <span data-ttu-id="a4e5e-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4e5e-137">Requirement</span></span> | <span data-ttu-id="a4e5e-138">Valore</span><span class="sxs-lookup"><span data-stu-id="a4e5e-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="a4e5e-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4e5e-139">Minimum supported client</span></span><br/> | <span data-ttu-id="a4e5e-140">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a4e5e-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="a4e5e-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a4e5e-141">Minimum supported server</span></span><br/> | <span data-ttu-id="a4e5e-142">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a4e5e-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a4e5e-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a4e5e-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4e5e-144"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4e5e-144"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4e5e-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a4e5e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4e5e-146">**glGetString**</span><span class="sxs-lookup"><span data-stu-id="a4e5e-146">**glGetString**</span></span>](glgetstring.md)
</dt> <dt>

[<span data-ttu-id="a4e5e-147">**PIXELFORMATDESCRIPTOR**</span><span class="sxs-lookup"><span data-stu-id="a4e5e-147">**PIXELFORMATDESCRIPTOR**</span></span>](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)
</dt> <dt>

[<span data-ttu-id="a4e5e-148">**SwapBuffers**</span><span class="sxs-lookup"><span data-stu-id="a4e5e-148">**SwapBuffers**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)
</dt> <dt>

[<span data-ttu-id="a4e5e-149">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="a4e5e-149">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





