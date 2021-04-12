---
description: Rappresenta gli attributi applicati all'input penna quando viene disegnata.
ms.assetid: 10ca7ae5-28dd-42a2-98d9-852d4de5869d
title: Classe InkDrawingAttributes (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDrawingAttributes
- InkDrawingAttributes.IInkDrawingAttributes
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 64a45c33e7aa17b381875ac8e8e8d054af2bf086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347906"
---
# <a name="inkdrawingattributes-class"></a><span data-ttu-id="85ac2-103">Classe InkDrawingAttributes</span><span class="sxs-lookup"><span data-stu-id="85ac2-103">InkDrawingAttributes class</span></span>

<span data-ttu-id="85ac2-104">Rappresenta gli attributi applicati all'input penna quando viene disegnata.</span><span class="sxs-lookup"><span data-stu-id="85ac2-104">Represents the attributes that are applied to ink when it is drawn.</span></span>

<span data-ttu-id="85ac2-105">**InkDrawingAttributes** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="85ac2-105">**InkDrawingAttributes** has these types of members:</span></span>

-   [<span data-ttu-id="85ac2-106">Interfacce</span><span class="sxs-lookup"><span data-stu-id="85ac2-106">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="85ac2-107">Metodi</span><span class="sxs-lookup"><span data-stu-id="85ac2-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="85ac2-108">Proprietà</span><span class="sxs-lookup"><span data-stu-id="85ac2-108">Properties</span></span>](#properties)

### <a name="interfaces"></a><span data-ttu-id="85ac2-109">Interfacce</span><span class="sxs-lookup"><span data-stu-id="85ac2-109">Interfaces</span></span>

<span data-ttu-id="85ac2-110">La classe **InkDrawingAttributes** definisce queste interfacce.</span><span class="sxs-lookup"><span data-stu-id="85ac2-110">The **InkDrawingAttributes** class defines these interfaces.</span></span>



| <span data-ttu-id="85ac2-111">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="85ac2-111">Interface</span></span>                 | <span data-ttu-id="85ac2-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85ac2-112">Description</span></span>                                                                    |
|:--------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="85ac2-113">**IInkDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="85ac2-113">**IInkDrawingAttributes**</span></span> | <span data-ttu-id="85ac2-114">Questo oggetto implementa l'interfaccia com **IInkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="85ac2-114">This object implements the **IInkDrawingAttributes** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="85ac2-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="85ac2-115">Methods</span></span>

<span data-ttu-id="85ac2-116">La classe **InkDrawingAttributes** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="85ac2-116">The **InkDrawingAttributes** class has these methods.</span></span>



| <span data-ttu-id="85ac2-117">Metodo</span><span class="sxs-lookup"><span data-stu-id="85ac2-117">Method</span></span>                         | <span data-ttu-id="85ac2-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85ac2-118">Description</span></span>                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85ac2-119">**Clone**</span><span class="sxs-lookup"><span data-stu-id="85ac2-119">**Clone**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone) | <span data-ttu-id="85ac2-120">Crea un oggetto [**InkDisp**](inkdisp-class.md), **InkDrawingAttributes** o [**InkRecognizerContext**](inkrecognizercontext-class.md) duplicato.</span><span class="sxs-lookup"><span data-stu-id="85ac2-120">Creates a duplicate [**InkDisp**](inkdisp-class.md), **InkDrawingAttributes**, or [**InkRecognizerContext**](inkrecognizercontext-class.md) object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="85ac2-121">Proprietà</span><span class="sxs-lookup"><span data-stu-id="85ac2-121">Properties</span></span>

<span data-ttu-id="85ac2-122">La classe **InkDrawingAttributes** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="85ac2-122">The **InkDrawingAttributes** class has these properties.</span></span>



| <span data-ttu-id="85ac2-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="85ac2-123">Property</span></span>                                                                           | <span data-ttu-id="85ac2-124">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="85ac2-124">Access type</span></span>           | <span data-ttu-id="85ac2-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85ac2-125">Description</span></span>                                                                                                                                                                      |
|:-----------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85ac2-126">**Antialias**</span><span class="sxs-lookup"><span data-stu-id="85ac2-126">**AntiAliased**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_antialiased)<br/>                 | <span data-ttu-id="85ac2-127">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="85ac2-127">Read/write</span></span><br/> | <span data-ttu-id="85ac2-128">Ottiene o imposta il valore che specifica se i colori di primo piano e di sfondo lungo il bordo dell'input penna vengono combinati per aumentare la smussatura di un tratto di input penna.</span><span class="sxs-lookup"><span data-stu-id="85ac2-128">Gets or sets the value that specifies whether the foreground and background colors along the edge of the ink are blended to increase the smoothness of an ink stroke.</span></span><br/> |
| [<span data-ttu-id="85ac2-129">**Colore**</span><span class="sxs-lookup"><span data-stu-id="85ac2-129">**Color**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color)<br/>                             | <span data-ttu-id="85ac2-130">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="85ac2-130">Read/write</span></span><br/> | <span data-ttu-id="85ac2-131">Ottiene o imposta il colore dell'input penna creato con questo oggetto **InkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="85ac2-131">Gets or sets the color of the ink drawn with this **InkDrawingAttributes** object.</span></span><br/>                                                                                    |
| [<span data-ttu-id="85ac2-132">**ExtendedProperties**</span><span class="sxs-lookup"><span data-stu-id="85ac2-132">**ExtendedProperties**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | <span data-ttu-id="85ac2-133">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="85ac2-133">Read-only</span></span><br/>  | <span data-ttu-id="85ac2-134">Ottiene la raccolta di dati definiti dall'applicazione archiviati nell'oggetto **InkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="85ac2-134">Gets the collection of application-defined data that is stored in the **InkDrawingAttributes** object.</span></span><br/>                                                                |
| [<span data-ttu-id="85ac2-135">**FitToCurve**</span><span class="sxs-lookup"><span data-stu-id="85ac2-135">**FitToCurve**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve)<br/>                   | <span data-ttu-id="85ac2-136">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="85ac2-136">Read/write</span></span><br/> | <span data-ttu-id="85ac2-137">Ottiene o imposta il valore che specifica se viene eseguito il rendering dell'input penna come una serie di curve anziché come linee tra i punti di esempio della penna.</span><span class="sxs-lookup"><span data-stu-id="85ac2-137">Gets or sets the value that specifies whether ink is rendered as a series of curves instead of as lines between pen sample points.</span></span><br/>                                    |
| [<span data-ttu-id="85ac2-138">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="85ac2-138">**Height**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height)<br/>                           | <span data-ttu-id="85ac2-139">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="85ac2-139">Read/write</span></span><br/> | <span data-ttu-id="85ac2-140">Ottiene o imposta l'altezza della penna quando si disegna l'input penna con questo oggetto **InkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="85ac2-140">Gets or sets the height of the pen when drawing ink with this **InkDrawingAttributes** object.</span></span><br/>                                                                        |
| [<span data-ttu-id="85ac2-141">**IgnorePressure**</span><span class="sxs-lookup"><span data-stu-id="85ac2-141">**IgnorePressure**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_ignorepressure)<br/>           | <span data-ttu-id="85ac2-142">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="85ac2-142">Read/write</span></span><br/> | <span data-ttu-id="85ac2-143">Ottiene o imposta il valore che specifica se l'input penna automatico diventa più ampio con una maggiore pressione della punta della penna sulla superficie del tablet.</span><span class="sxs-lookup"><span data-stu-id="85ac2-143">Gets or sets the value that specifies whether drawn ink automatically becomes wider with increased pressure of the pen tip on the tablet surface.</span></span><br/>                     |
| [<span data-ttu-id="85ac2-144">**PenTip**</span><span class="sxs-lookup"><span data-stu-id="85ac2-144">**PenTip**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip)<br/>                           | <span data-ttu-id="85ac2-145">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="85ac2-145">Read/write</span></span><br/> | <span data-ttu-id="85ac2-146">Ottiene o imposta la punta della penna da usare (palla o rettangolo) quando si disegna l'input penna con questo oggetto **InkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="85ac2-146">Gets or sets the pen tip to use (ball or rectangle) when drawing ink with this **InkDrawingAttributes** object.</span></span><br/>                                                       |
| [<span data-ttu-id="85ac2-147">**RasterOperation**</span><span class="sxs-lookup"><span data-stu-id="85ac2-147">**RasterOperation**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_rasteroperation)<br/>         | <span data-ttu-id="85ac2-148">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="85ac2-148">Read/write</span></span><br/> | <span data-ttu-id="85ac2-149">Ottiene o imposta il modo in cui il colore della penna interagisce con i colori di sfondo esistenti sullo schermo quando viene disegnato l'input penna.</span><span class="sxs-lookup"><span data-stu-id="85ac2-149">Gets or sets how the pen color interacts with the existing background colors on the display when the ink is drawn.</span></span><br/>                                                    |
| [<span data-ttu-id="85ac2-150">**Trasparenza**</span><span class="sxs-lookup"><span data-stu-id="85ac2-150">**Transparency**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_transparency)<br/>               | <span data-ttu-id="85ac2-151">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="85ac2-151">Read/write</span></span><br/> | <span data-ttu-id="85ac2-152">Ottiene o imposta il valore di trasparenza dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="85ac2-152">Gets or sets the transparency value of drawn ink.</span></span> <span data-ttu-id="85ac2-153">I valori sono compresi tra zero (completamente opaco) e 255 (completamente trasparente).</span><span class="sxs-lookup"><span data-stu-id="85ac2-153">Values range from zero (totally opaque) to 255 (totally transparent).</span></span><br/>                                               |
| [<span data-ttu-id="85ac2-154">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="85ac2-154">**Width**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)<br/>                             | <span data-ttu-id="85ac2-155">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="85ac2-155">Read/write</span></span><br/> | <span data-ttu-id="85ac2-156">Ottiene o imposta la larghezza della penna durante il disegno dell'input penna con questo oggetto **InkDrawingAttributes** .</span><span class="sxs-lookup"><span data-stu-id="85ac2-156">Gets or sets the width of the pen when drawing ink with this **InkDrawingAttributes** object.</span></span><br/>                                                                         |



 

## <a name="remarks"></a><span data-ttu-id="85ac2-157">Commenti</span><span class="sxs-lookup"><span data-stu-id="85ac2-157">Remarks</span></span>

<span data-ttu-id="85ac2-158">È possibile creare un'istanza di questo oggetto chiamando il metodo [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.</span><span class="sxs-lookup"><span data-stu-id="85ac2-158">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

<span data-ttu-id="85ac2-159">Questi attributi di disegno possono essere associati a un tratto o a un cursore e specificare impostazioni quali il colore, la larghezza e la trasparenza.</span><span class="sxs-lookup"><span data-stu-id="85ac2-159">These drawing attributes can be associated with a stroke or a cursor and specify settings such as color, width, and transparency.</span></span>

<span data-ttu-id="85ac2-160">Per specificare gli attributi di disegno di un tratto, utilizzare la proprietà [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) dell'oggetto [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="85ac2-160">To specify the drawing attributes of a stroke, use the [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) property of the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span> <span data-ttu-id="85ac2-161">Per specificare gli attributi di disegno di tutti i tratti all'interno di una raccolta di tratti, chiamare il metodo [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) della raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="85ac2-161">To specify the drawing attributes of all of the strokes within a collection of strokes, call the [**ModifyDrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes) method of the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

<span data-ttu-id="85ac2-162">Ogni oggetto [**InkCollector**](inkcollector-class.md) , oggetto [**InkOverlay**](inkoverlay-class.md) e controllo [InkPicture](inkpicture-control-reference.md) può specificare un set diverso di attributi di disegno per lo stesso cursore.</span><span class="sxs-lookup"><span data-stu-id="85ac2-162">Each [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, and [InkPicture](inkpicture-control-reference.md) control can specify a different set of drawing attributes for the same cursor.</span></span> <span data-ttu-id="85ac2-163">Utilizzare la proprietà [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) dell'oggetto [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) per ottenere o impostare gli attributi di disegno di un cursore.</span><span class="sxs-lookup"><span data-stu-id="85ac2-163">Use the [**DrawingAttributes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes) property of the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object to get or set the drawing attributes of a cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="85ac2-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85ac2-164">Requirements</span></span>



| <span data-ttu-id="85ac2-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="85ac2-165">Requirement</span></span> | <span data-ttu-id="85ac2-166">Valore</span><span class="sxs-lookup"><span data-stu-id="85ac2-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85ac2-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85ac2-167">Minimum supported client</span></span><br/> | <span data-ttu-id="85ac2-168">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="85ac2-168">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="85ac2-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85ac2-169">Minimum supported server</span></span><br/> | <span data-ttu-id="85ac2-170">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="85ac2-170">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="85ac2-171">Intestazione</span><span class="sxs-lookup"><span data-stu-id="85ac2-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="85ac2-172"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="85ac2-172"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="85ac2-173">Libreria</span><span class="sxs-lookup"><span data-stu-id="85ac2-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="85ac2-174"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85ac2-174"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="85ac2-175">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85ac2-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85ac2-176">**DrawingAttributes (proprietà)**</span><span class="sxs-lookup"><span data-stu-id="85ac2-176">**DrawingAttributes Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_drawingattributes)
</dt> <dt>

<span data-ttu-id="85ac2-177">**DrawingAttributes (proprietà)**</span><span class="sxs-lookup"><span data-stu-id="85ac2-177">**DrawingAttributes Property**</span></span>
</dt> <dt>

<span data-ttu-id="85ac2-178">**DrawingAttributes (proprietà)**</span><span class="sxs-lookup"><span data-stu-id="85ac2-178">**DrawingAttributes Property**</span></span>
</dt> <dt>

[<span data-ttu-id="85ac2-179">**Proprietà DefaultDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="85ac2-179">**DefaultDrawingAttributes Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_defaultdrawingattributes)
</dt> <dt>

<span data-ttu-id="85ac2-180">**Proprietà DefaultDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="85ac2-180">**DefaultDrawingAttributes Property**</span></span>
</dt> <dt>

<span data-ttu-id="85ac2-181">**Proprietà DefaultDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="85ac2-181">**DefaultDrawingAttributes Property**</span></span>
</dt> <dt>

[<span data-ttu-id="85ac2-182">**Metodo ModifyDrawingAttributes**</span><span class="sxs-lookup"><span data-stu-id="85ac2-182">**ModifyDrawingAttributes Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-modifydrawingattributes)
</dt> <dt>

[<span data-ttu-id="85ac2-183">**Interfaccia IInkCursor**</span><span class="sxs-lookup"><span data-stu-id="85ac2-183">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="85ac2-184">**Classe InkDisp**</span><span class="sxs-lookup"><span data-stu-id="85ac2-184">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> <dt>

[<span data-ttu-id="85ac2-185">**Interfaccia IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="85ac2-185">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

