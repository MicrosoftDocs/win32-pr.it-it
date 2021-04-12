---
description: Rappresenta la gestione dei mapping dall'input penna alla finestra di visualizzazione. Usare l'oggetto InkRenderer per visualizzare l'input penna in una finestra. È anche possibile usarlo per riposizionare e ridimensionare il tratto.
ms.assetid: 66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7
title: Classe InkRenderer (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkRenderer
- InkRenderer.IInkRenderer
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 5d29448e2f8ae98c4e15d6c3a51747257d20c62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234081"
---
# <a name="inkrenderer-class"></a><span data-ttu-id="496f5-105">Classe InkRenderer</span><span class="sxs-lookup"><span data-stu-id="496f5-105">InkRenderer class</span></span>

<span data-ttu-id="496f5-106">Rappresenta la gestione dei mapping dall'input penna alla finestra di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="496f5-106">Represents the management of mappings from ink to the display window.</span></span> <span data-ttu-id="496f5-107">Usare l'oggetto **InkRenderer** per visualizzare l'input penna in una finestra.</span><span class="sxs-lookup"><span data-stu-id="496f5-107">Use the **InkRenderer** object to display ink in a window.</span></span> <span data-ttu-id="496f5-108">È anche possibile usarlo per riposizionare e ridimensionare il tratto.</span><span class="sxs-lookup"><span data-stu-id="496f5-108">You can also use it to reposition and resize stroke.</span></span>

<span data-ttu-id="496f5-109">**InkRenderer** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="496f5-109">**InkRenderer** has these types of members:</span></span>

-   [<span data-ttu-id="496f5-110">Interfacce</span><span class="sxs-lookup"><span data-stu-id="496f5-110">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="496f5-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="496f5-111">Methods</span></span>](#methods)

### <a name="interfaces"></a><span data-ttu-id="496f5-112">Interfacce</span><span class="sxs-lookup"><span data-stu-id="496f5-112">Interfaces</span></span>

<span data-ttu-id="496f5-113">La classe **InkRenderer** definisce queste interfacce.</span><span class="sxs-lookup"><span data-stu-id="496f5-113">The **InkRenderer** class defines these interfaces.</span></span>



| <span data-ttu-id="496f5-114">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="496f5-114">Interface</span></span>        | <span data-ttu-id="496f5-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="496f5-115">Description</span></span>                                                           |
|:-----------------|:----------------------------------------------------------------------|
| <span data-ttu-id="496f5-116">**IInkRenderer**</span><span class="sxs-lookup"><span data-stu-id="496f5-116">**IInkRenderer**</span></span> | <span data-ttu-id="496f5-117">Questo oggetto implementa l'interfaccia com **IInkRenderer** .</span><span class="sxs-lookup"><span data-stu-id="496f5-117">This object implements the **IInkRenderer** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="496f5-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="496f5-118">Methods</span></span>

<span data-ttu-id="496f5-119">La classe **InkRenderer** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="496f5-119">The **InkRenderer** class has these methods.</span></span>



| <span data-ttu-id="496f5-120">Metodo</span><span class="sxs-lookup"><span data-stu-id="496f5-120">Method</span></span>                                                                     | <span data-ttu-id="496f5-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="496f5-121">Description</span></span>                                                                                                                                              |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="496f5-122">**Disegna**</span><span class="sxs-lookup"><span data-stu-id="496f5-122">**Draw**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw)                                           | <span data-ttu-id="496f5-123">Disegna tratti in un contesto di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="496f5-123">Draws strokes on a device context.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="496f5-124">**DrawStroke**</span><span class="sxs-lookup"><span data-stu-id="496f5-124">**DrawStroke**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)                               | <span data-ttu-id="496f5-125">Disegna un tratto nel contesto di dispositivo Windows specificato.</span><span class="sxs-lookup"><span data-stu-id="496f5-125">Draws a stroke on the specified windows device context.</span></span><br/>                                                                                       |
| [<span data-ttu-id="496f5-126">**GetObjectTransform**</span><span class="sxs-lookup"><span data-stu-id="496f5-126">**GetObjectTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getobjecttransform)               | <span data-ttu-id="496f5-127">Recupera la trasformazione oggetto utilizzata per eseguire il rendering dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="496f5-127">Retrieves the object transform that was used to render ink.</span></span><br/>                                                                                   |
| [<span data-ttu-id="496f5-128">**GetViewTransform**</span><span class="sxs-lookup"><span data-stu-id="496f5-128">**GetViewTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-getviewtransform)                   | <span data-ttu-id="496f5-129">Recupera la trasformazione di visualizzazione utilizzata per eseguire il rendering dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="496f5-129">Retrieves the view transform that is used to render ink.</span></span><br/>                                                                                      |
| [<span data-ttu-id="496f5-130">**InkSpaceToPixel**</span><span class="sxs-lookup"><span data-stu-id="496f5-130">**InkSpaceToPixel**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixel)                     | <span data-ttu-id="496f5-131">Converte una posizione nelle coordinate dello spazio input penna in uno spazio in pixel.</span><span class="sxs-lookup"><span data-stu-id="496f5-131">Converts a location in ink space coordinates to be in pixel space.</span></span><br/>                                                                            |
| [<span data-ttu-id="496f5-132">**InkSpaceToPixelFromPoints**</span><span class="sxs-lookup"><span data-stu-id="496f5-132">**InkSpaceToPixelFromPoints**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-inkspacetopixelfrompoints) | <span data-ttu-id="496f5-133">Converte una matrice di punti nelle coordinate dello spazio input penna nello spazio pixel.</span><span class="sxs-lookup"><span data-stu-id="496f5-133">Converts an array of points in ink space coordinates to pixel space.</span></span><br/>                                                                          |
| [<span data-ttu-id="496f5-134">**Measure**</span><span class="sxs-lookup"><span data-stu-id="496f5-134">**Measure**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-measure)                                     | <span data-ttu-id="496f5-135">Calcola il rettangolo nel contesto di dispositivo che conterrebbe una raccolta di tratti se sono stati disegnati con l'oggetto **InkRenderer** .</span><span class="sxs-lookup"><span data-stu-id="496f5-135">Calculates the rectangle on the device context that would contain a collection of strokes if they were drawn with the **InkRenderer** object.</span></span><br/> |
| [<span data-ttu-id="496f5-136">**MeasureStroke**</span><span class="sxs-lookup"><span data-stu-id="496f5-136">**MeasureStroke**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkrenderer-measurestroke)                         | <span data-ttu-id="496f5-137">Calcola il rettangolo nel contesto di dispositivo che conterrebbe un tratto se sono stati disegnati con l'oggetto **InkRenderer** .</span><span class="sxs-lookup"><span data-stu-id="496f5-137">Calculates the rectangle on the device context that would contain a stroke if they were drawn with the **InkRenderer** object.</span></span><br/>                |
| [<span data-ttu-id="496f5-138">**Spostare**</span><span class="sxs-lookup"><span data-stu-id="496f5-138">**Move**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-move)                                           | <span data-ttu-id="496f5-139">Applica una conversione alla trasformazione visualizzazione nelle coordinate dello spazio di input penna.</span><span class="sxs-lookup"><span data-stu-id="496f5-139">Applies a translation to the view transform in ink space coordinates.</span></span><br/>                                                                         |
| [<span data-ttu-id="496f5-140">**PixelToInkSpace**</span><span class="sxs-lookup"><span data-stu-id="496f5-140">**PixelToInkSpace**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspace)                     | <span data-ttu-id="496f5-141">Converte una posizione in coordinate pixel nello spazio di input penna.</span><span class="sxs-lookup"><span data-stu-id="496f5-141">Converts a location in pixel coordinates to be in ink space.</span></span><br/>                                                                                  |
| [<span data-ttu-id="496f5-142">**PixelToInkSpaceFromPoints**</span><span class="sxs-lookup"><span data-stu-id="496f5-142">**PixelToInkSpaceFromPoints**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-pixeltoinkspacefrompoints) | <span data-ttu-id="496f5-143">Converte una matrice di punti in coordinate dello spazio in pixel nello spazio di input penna.</span><span class="sxs-lookup"><span data-stu-id="496f5-143">Converts an array of points in pixel space coordinates to ink space.</span></span><br/>                                                                          |
| [<span data-ttu-id="496f5-144">**Ruota**</span><span class="sxs-lookup"><span data-stu-id="496f5-144">**Rotate**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-rotate)                                       | <span data-ttu-id="496f5-145">Applica una rotazione alla trasformazione della vista.</span><span class="sxs-lookup"><span data-stu-id="496f5-145">Applies a rotation to the view transform.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="496f5-146">**ScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="496f5-146">**ScaleTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-scaletransform)                       | <span data-ttu-id="496f5-147">Ridimensiona la trasformazione della vista nella dimensione X e Y.</span><span class="sxs-lookup"><span data-stu-id="496f5-147">Scales the view transform in the X and Y dimension.</span></span><br/>                                                                                           |
| [<span data-ttu-id="496f5-148">**SetObjectTransform**</span><span class="sxs-lookup"><span data-stu-id="496f5-148">**SetObjectTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform)               | <span data-ttu-id="496f5-149">Imposta la trasformazione oggetto utilizzata per eseguire il rendering dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="496f5-149">Sets the object transform that is used to render ink.</span></span><br/>                                                                                         |
| [<span data-ttu-id="496f5-150">**SetViewTransform**</span><span class="sxs-lookup"><span data-stu-id="496f5-150">**SetViewTransform**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform)                   | <span data-ttu-id="496f5-151">Imposta la trasformazione visualizzazione utilizzata per eseguire il rendering dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="496f5-151">Sets the view transform that is used to render ink.</span></span><br/>                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="496f5-152">Commenti</span><span class="sxs-lookup"><span data-stu-id="496f5-152">Remarks</span></span>

<span data-ttu-id="496f5-153">La stampa viene eseguita anche tramite l'oggetto **InkRenderer** .</span><span class="sxs-lookup"><span data-stu-id="496f5-153">Printing is also done through the **InkRenderer** object.</span></span>

<span data-ttu-id="496f5-154">È possibile creare un'istanza di questo oggetto chiamando il metodo [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.</span><span class="sxs-lookup"><span data-stu-id="496f5-154">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

## <a name="requirements"></a><span data-ttu-id="496f5-155">Requisiti</span><span class="sxs-lookup"><span data-stu-id="496f5-155">Requirements</span></span>



| <span data-ttu-id="496f5-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="496f5-156">Requirement</span></span> | <span data-ttu-id="496f5-157">Valore</span><span class="sxs-lookup"><span data-stu-id="496f5-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="496f5-158">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="496f5-158">Minimum supported client</span></span><br/> | <span data-ttu-id="496f5-159">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="496f5-159">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="496f5-160">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="496f5-160">Minimum supported server</span></span><br/> | <span data-ttu-id="496f5-161">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="496f5-161">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="496f5-162">Intestazione</span><span class="sxs-lookup"><span data-stu-id="496f5-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="496f5-163"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="496f5-163"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="496f5-164">Libreria</span><span class="sxs-lookup"><span data-stu-id="496f5-164">Library</span></span><br/>                  | <dl> <span data-ttu-id="496f5-165"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="496f5-165"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="496f5-166">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="496f5-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="496f5-167">**Renderer (proprietà)**</span><span class="sxs-lookup"><span data-stu-id="496f5-167">**Renderer Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_renderer)
</dt> <dt>

[<span data-ttu-id="496f5-168">**Classe InkDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="496f5-168">**InkDrawingAttributes Class**</span></span>](inkdrawingattributes-class.md)
</dt> <dt>

[<span data-ttu-id="496f5-169">**Interfaccia IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="496f5-169">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

<span data-ttu-id="496f5-170">[Raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="496f5-170">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> </dl>

 

