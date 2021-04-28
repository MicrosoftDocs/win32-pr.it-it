---
description: "Classe InkDisp: rappresenta i tratti raccolti dell'input penna all'interno di uno spazio input penna."
ms.assetid: f942d6a3-f303-49df-a128-de9760b508ef
title: Classe InkDisp (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDisp
- InkDisp.IInkDisp
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: e4214d6b03e5823bd5012017e418066763c8132c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109989"
---
# <a name="inkdisp-class"></a><span data-ttu-id="03b92-103">Classe InkDisp</span><span class="sxs-lookup"><span data-stu-id="03b92-103">InkDisp class</span></span>

<span data-ttu-id="03b92-104">Rappresenta i tratti raccolti dell'input penna all'interno di uno spazio input penna.</span><span class="sxs-lookup"><span data-stu-id="03b92-104">Represents the collected strokes of ink within an ink space.</span></span>

<span data-ttu-id="03b92-105">**InkDisp** ha questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="03b92-105">**InkDisp** has these types of members:</span></span>

-   [<span data-ttu-id="03b92-106">Eventi</span><span class="sxs-lookup"><span data-stu-id="03b92-106">Events</span></span>](#events)
-   [<span data-ttu-id="03b92-107">Interfacce</span><span class="sxs-lookup"><span data-stu-id="03b92-107">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="03b92-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="03b92-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="03b92-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="03b92-109">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="03b92-110">Eventi</span><span class="sxs-lookup"><span data-stu-id="03b92-110">Events</span></span>

<span data-ttu-id="03b92-111">La **classe InkDisp** include questi eventi.</span><span class="sxs-lookup"><span data-stu-id="03b92-111">The **InkDisp** class has these events.</span></span>



| <span data-ttu-id="03b92-112">Event</span><span class="sxs-lookup"><span data-stu-id="03b92-112">Event</span></span>                                    | <span data-ttu-id="03b92-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03b92-113">Description</span></span>                                                             |
|:-----------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="03b92-114">**InkAdded**</span><span class="sxs-lookup"><span data-stu-id="03b92-114">**InkAdded**</span></span>](inkdisp-inkadded.md)     | <span data-ttu-id="03b92-115">Si verifica quando un tratto viene aggiunto **all'oggetto InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="03b92-115">Occurs when a stroke is added to the **InkDisp** object.</span></span><br/>     |
| [<span data-ttu-id="03b92-116">**InkDeleted**</span><span class="sxs-lookup"><span data-stu-id="03b92-116">**InkDeleted**</span></span>](inkdisp-inkdeleted.md) | <span data-ttu-id="03b92-117">Si verifica quando un tratto viene eliminato **dall'oggetto InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="03b92-117">Occurs when a stroke is deleted from the **InkDisp** object.</span></span><br/> |



 

### <a name="interfaces"></a><span data-ttu-id="03b92-118">Interfacce</span><span class="sxs-lookup"><span data-stu-id="03b92-118">Interfaces</span></span>

<span data-ttu-id="03b92-119">La **classe InkDisp** definisce queste interfacce.</span><span class="sxs-lookup"><span data-stu-id="03b92-119">The **InkDisp** class defines these interfaces.</span></span>



| <span data-ttu-id="03b92-120">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="03b92-120">Interface</span></span>    | <span data-ttu-id="03b92-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03b92-121">Description</span></span>                                                       |
|:-------------|:------------------------------------------------------------------|
| <span data-ttu-id="03b92-122">**IInkDisp**</span><span class="sxs-lookup"><span data-stu-id="03b92-122">**IInkDisp**</span></span> | <span data-ttu-id="03b92-123">Questo oggetto implementa **l'interfaccia COM IInkDisp.**</span><span class="sxs-lookup"><span data-stu-id="03b92-123">This object implements the **IInkDisp** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="03b92-124">Metodi</span><span class="sxs-lookup"><span data-stu-id="03b92-124">Methods</span></span>

<span data-ttu-id="03b92-125">La **classe InkDisp** include questi metodi.</span><span class="sxs-lookup"><span data-stu-id="03b92-125">The **InkDisp** class has these methods.</span></span>



| <span data-ttu-id="03b92-126">Metodo</span><span class="sxs-lookup"><span data-stu-id="03b92-126">Method</span></span>                                                                   | <span data-ttu-id="03b92-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03b92-127">Description</span></span>                                                                                                                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03b92-128">**AddStrokesAtRectangle**</span><span class="sxs-lookup"><span data-stu-id="03b92-128">**AddStrokesAtRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-addstrokesatrectangle)           | <span data-ttu-id="03b92-129">Inserisce una raccolta di tratti **nell'oggetto InkDisp** in corrispondenza del rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="03b92-129">Inserts a stroke collection into the **InkDisp** object at the specified rectangle.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="03b92-130">**CanPaste**</span><span class="sxs-lookup"><span data-stu-id="03b92-130">**CanPaste**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                     | <span data-ttu-id="03b92-131">Indica se [**L'oggetto IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) può essere convertito in un **oggetto InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="03b92-131">Indicates whether the [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) can be converted to an **InkDisp** object.</span></span><br/>                                                                                       |
| [<span data-ttu-id="03b92-132">**Clip**</span><span class="sxs-lookup"><span data-stu-id="03b92-132">**Clip**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-clip)                                      | <span data-ttu-id="03b92-133">Rimuove parti di un tratto o di una raccolta di tratti esterni a un rettangolo.</span><span class="sxs-lookup"><span data-stu-id="03b92-133">Removes portions of a stroke or collection of strokes that are outside a rectangle.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="03b92-134">**ClipboardCopy**</span><span class="sxs-lookup"><span data-stu-id="03b92-134">**ClipboardCopy**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                           | <span data-ttu-id="03b92-135">Copia la [raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) negli Appunti.</span><span class="sxs-lookup"><span data-stu-id="03b92-135">Copies the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection to the Clipboard.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="03b92-136">**ClipboardCopyWithRectangle**</span><span class="sxs-lookup"><span data-stu-id="03b92-136">**ClipboardCopyWithRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopywithrectangle) | <span data-ttu-id="03b92-137">Copia negli [**Appunti gli oggetti IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) contenuti nel rettangolo noto.</span><span class="sxs-lookup"><span data-stu-id="03b92-137">Copies the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects that are contained within the known rectangle to the Clipboard.</span></span><br/>                                                               |
| [<span data-ttu-id="03b92-138">**AppuntiPaste**</span><span class="sxs-lookup"><span data-stu-id="03b92-138">**ClipboardPaste**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                         | <span data-ttu-id="03b92-139">Copia [**l'oggetto IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) dagli Appunti all'oggetto **InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="03b92-139">Copies the [**IDataObject**](/windows/desktop/api/objidl/nn-objidl-idataobject) from the Clipboard to the **InkDisp** object.</span></span><br/>                                                                                               |
| [<span data-ttu-id="03b92-140">**Clone**</span><span class="sxs-lookup"><span data-stu-id="03b92-140">**Clone**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clone)                                           | <span data-ttu-id="03b92-141">Crea un oggetto **InkDisp** duplicato.</span><span class="sxs-lookup"><span data-stu-id="03b92-141">Creates a duplicate **InkDisp** object.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="03b92-142">**CreateStroke**</span><span class="sxs-lookup"><span data-stu-id="03b92-142">**CreateStroke**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstroke)                             | <span data-ttu-id="03b92-143">Crea un tratto dai punti o dai dati del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="03b92-143">Creates a stroke from points or packet data.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="03b92-144">**CreateStrokes**</span><span class="sxs-lookup"><span data-stu-id="03b92-144">**CreateStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-createstrokes)                           | <span data-ttu-id="03b92-145">Crea una [raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) per questo **oggetto InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="03b92-145">Creates an [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection for this **InkDisp** object.</span></span><br/>                                                                                                |
| [<span data-ttu-id="03b92-146">**DeleteStroke**</span><span class="sxs-lookup"><span data-stu-id="03b92-146">**DeleteStroke**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestroke)                             | <span data-ttu-id="03b92-147">Elimina un tratto **dall'oggetto InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="03b92-147">Deletes a stroke from the **InkDisp** object.</span></span><br/>                                                                                                                                             |
| [<span data-ttu-id="03b92-148">**Elimina sequenze**</span><span class="sxs-lookup"><span data-stu-id="03b92-148">**DeleteStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-deletestrokes)                           | <span data-ttu-id="03b92-149">Elimina i tratti **dall'oggetto InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="03b92-149">Deletes strokes from the **InkDisp** object.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="03b92-150">**Metodo ExtractStrokes**</span><span class="sxs-lookup"><span data-stu-id="03b92-150">**ExtractStrokes Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractstrokes)                  | <span data-ttu-id="03b92-151">Estrae i tratti **dall'oggetto InkDisp** e restituisce un nuovo **oggetto InkDisp** contenente i tratti estratti.</span><span class="sxs-lookup"><span data-stu-id="03b92-151">Extracts strokes from the **InkDisp** object and returns a new **InkDisp** object containing the extracted strokes.</span></span><br/>                                                                       |
| [<span data-ttu-id="03b92-152">**Metodo ExtractWithRectangle**</span><span class="sxs-lookup"><span data-stu-id="03b92-152">**ExtractWithRectangle Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-extractwithrectangle)      | <span data-ttu-id="03b92-153">Taglia o copia i tratti da un oggetto **Classe InkDisp** esistente e li incolla in un nuovo oggetto **Classe InkDisp,** usando il rettangolo noto per determinare quali tratti estrarre.</span><span class="sxs-lookup"><span data-stu-id="03b92-153">Cuts or copies strokes from an existing **InkDisp Class** object and pastes them into a new **InkDisp Class** object, by using the known rectangle to determine which strokes to extract.</span></span><br/> |
| [<span data-ttu-id="03b92-154">**GetBoundingBox**</span><span class="sxs-lookup"><span data-stu-id="03b92-154">**GetBoundingBox**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-getboundingbox)                  | <span data-ttu-id="03b92-155">Recupera il rettangolo di selezione di tutti i tratti **nell'oggetto InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="03b92-155">Retrieves the bounding box of all of the strokes in the **InkDisp** object.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="03b92-156">**HitTestCircle**</span><span class="sxs-lookup"><span data-stu-id="03b92-156">**HitTestCircle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestcircle)                   | <span data-ttu-id="03b92-157">Recupera la raccolta [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) completamente all'interno o intersecata da un cerchio noto.</span><span class="sxs-lookup"><span data-stu-id="03b92-157">Retrieves the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection that are either completely inside or intersected by a known circle.</span></span><br/>                                                  |
| [<span data-ttu-id="03b92-158">**HitTestWithLasso**</span><span class="sxs-lookup"><span data-stu-id="03b92-158">**HitTestWithLasso**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithlasso)              | <span data-ttu-id="03b92-159">Recupera i tratti all'interno di un'area di selezione della polilinea.</span><span class="sxs-lookup"><span data-stu-id="03b92-159">Retrieves the strokes within a polyline selection area.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="03b92-160">**HitTestWithRectangle**</span><span class="sxs-lookup"><span data-stu-id="03b92-160">**HitTestWithRectangle**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-hittestwithrectangle)        | <span data-ttu-id="03b92-161">Recupera i tratti contenuti in un rettangolo specificato.</span><span class="sxs-lookup"><span data-stu-id="03b92-161">Retrieves the strokes that are contained within a specified rectangle.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="03b92-162">**Caricamento**</span><span class="sxs-lookup"><span data-stu-id="03b92-162">**Load**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-load)                                             | <span data-ttu-id="03b92-163">Popola un nuovo **oggetto InkDisp** con dati binari noti.</span><span class="sxs-lookup"><span data-stu-id="03b92-163">Populates a new **InkDisp** object with known binary data.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="03b92-164">**NearestPoint**</span><span class="sxs-lookup"><span data-stu-id="03b92-164">**NearestPoint**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-nearestpoint)                             | <span data-ttu-id="03b92-165">Recupera [**IInkStrokeDisp all'interno**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) dell'oggetto **InkDisp** più vicino a un punto noto, fornendo facoltativamente informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="03b92-165">Retrieves the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) within the **InkDisp** object that is nearest to a known point, optionally providing additional information.</span></span><br/>                       |
| [<span data-ttu-id="03b92-166">**Salva**</span><span class="sxs-lookup"><span data-stu-id="03b92-166">**Save**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-save)                                             | <span data-ttu-id="03b92-167">Converte l'input penna in un formato specificato e restituisce i dati binari.</span><span class="sxs-lookup"><span data-stu-id="03b92-167">Converts the ink to a specified format and returns the binary data.</span></span><br/>                                                                                                                       |



 

### <a name="properties"></a><span data-ttu-id="03b92-168">Proprietà</span><span class="sxs-lookup"><span data-stu-id="03b92-168">Properties</span></span>

<span data-ttu-id="03b92-169">La **classe InkDisp** ha queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="03b92-169">The **InkDisp** class has these properties.</span></span>



| <span data-ttu-id="03b92-170">Proprietà</span><span class="sxs-lookup"><span data-stu-id="03b92-170">Property</span></span>                                                                           | <span data-ttu-id="03b92-171">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="03b92-171">Access type</span></span>           | <span data-ttu-id="03b92-172">Descrizione</span><span class="sxs-lookup"><span data-stu-id="03b92-172">Description</span></span>                                                                                                                             |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="03b92-173">**CustomStrokes**</span><span class="sxs-lookup"><span data-stu-id="03b92-173">**CustomStrokes**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes)<br/>                          | <span data-ttu-id="03b92-174">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="03b92-174">Read-only</span></span><br/>  | <span data-ttu-id="03b92-175">Ottiene la [**raccolta IInkCustomStrokes**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) da rendere persistente con l'input penna.</span><span class="sxs-lookup"><span data-stu-id="03b92-175">Gets the [**IInkCustomStrokes**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes) collection to be persisted with the ink.</span></span><br/>                             |
| [<span data-ttu-id="03b92-176">**Sporco**</span><span class="sxs-lookup"><span data-stu-id="03b92-176">**Dirty**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_dirty)<br/>                                          | <span data-ttu-id="03b92-177">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="03b92-177">Read/write</span></span><br/> | <span data-ttu-id="03b92-178">Ottiene o imposta il valore che indica se un **oggetto InkDisp** è stato modificato dall'ultimo salvataggio dell'input penna.</span><span class="sxs-lookup"><span data-stu-id="03b92-178">Gets or sets the value that indicates whether an **InkDisp** object has been modified since the last time the ink was saved.</span></span><br/> |
| [<span data-ttu-id="03b92-179">**ExtendedProperties**</span><span class="sxs-lookup"><span data-stu-id="03b92-179">**ExtendedProperties**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_extendedproperties)<br/> | <span data-ttu-id="03b92-180">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="03b92-180">Read-only</span></span><br/>  | <span data-ttu-id="03b92-181">Ottiene la raccolta di dati definiti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="03b92-181">Gets the collection of application-defined data.</span></span><br/>                                                                             |
| [<span data-ttu-id="03b92-182">**Tratti**</span><span class="sxs-lookup"><span data-stu-id="03b92-182">**Strokes**</span></span>](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes)<br/>                           | <span data-ttu-id="03b92-183">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="03b92-183">Read-only</span></span><br/>  | <span data-ttu-id="03b92-184">Ottiene la [raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) contenuta nell'oggetto **InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="03b92-184">Gets the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection contained in the **InkDisp** object.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="03b92-185">Commenti</span><span class="sxs-lookup"><span data-stu-id="03b92-185">Remarks</span></span>

<span data-ttu-id="03b92-186">È possibile creare un'istanza di questo oggetto chiamando il [**metodo CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.</span><span class="sxs-lookup"><span data-stu-id="03b92-186">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

> [!Note]  
> <span data-ttu-id="03b92-187">La prima creazione di un'istanza di questo oggetto comporta anche la creazione di un'istanza di GDI+.</span><span class="sxs-lookup"><span data-stu-id="03b92-187">The first instantiation of this object causes GDI+ to be instantiated as well.</span></span> <span data-ttu-id="03b92-188">Un effetto collaterale è che se si usa un singolo oggetto input penna in un ciclo e lo si crea ed elimina all'interno del ciclo, si creerà più volte un'istanza di GDI+.</span><span class="sxs-lookup"><span data-stu-id="03b92-188">A side-effect is that if you are using a single ink object in a loop and create and destroy it within the loop, you will cause GDI+ to be instantiated over and over.</span></span> <span data-ttu-id="03b92-189">Ciò può causare una riduzione delle prestazioni nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="03b92-189">This can cause a performance degradation in your application.</span></span> <span data-ttu-id="03b92-190">Per evitare questo problema, mantenere sempre una singola istanza di un oggetto input penna mentre l'applicazione usa l'input penna.</span><span class="sxs-lookup"><span data-stu-id="03b92-190">To prevent this, keep a single instance of an ink object at all times while your application is using ink.</span></span>

 

<span data-ttu-id="03b92-191">Un **oggetto InkDisp** è un contenitore di dati del tratto (punto).</span><span class="sxs-lookup"><span data-stu-id="03b92-191">An **InkDisp** object is a container of stroke (point) data.</span></span> <span data-ttu-id="03b92-192">I dati del tratto, o i punti raccolti dalla penna, vengono inseriti in un **oggetto InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="03b92-192">The stroke data, or the points collected by the pen, are put into an **InkDisp** object.</span></span> <span data-ttu-id="03b92-193">La [**proprietà Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) contiene i dati per tutti i tratti all'interno dell'oggetto **InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="03b92-193">The [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) property contains the data for all strokes within the **InkDisp** object.</span></span>

<span data-ttu-id="03b92-194">[**L'oggetto InkCollector,**](inkcollector-class.md) [**l'oggetto InkOverlay**](inkoverlay-class.md) e il controllo [InkPicture](inkpicture-control-reference.md) raccolgono i punti dal dispositivo di input e li inserisce in **un oggetto InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="03b92-194">The [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, and [InkPicture](inkpicture-control-reference.md) control collects points from the input device and puts them into an **InkDisp** object.</span></span> <span data-ttu-id="03b92-195">Questi oggetti fungono essenzialmente da origine che distribuisce l'input penna in uno o più oggetti **InkDisp** diversi, che fungono da contenitori che contengono l'input penna distribuito.</span><span class="sxs-lookup"><span data-stu-id="03b92-195">These objects essentially act as the source that distributes ink into one or many different **InkDisp** objects, which act as containers that hold the distributed ink.</span></span>

<span data-ttu-id="03b92-196">Lo spazio input penna è uno spazio delle coordinate virtuali a cui vengono mappate le coordinate del contesto della tablet.</span><span class="sxs-lookup"><span data-stu-id="03b92-196">The ink space is a virtual coordinate space to which the coordinates of the tablet context are mapped.</span></span> <span data-ttu-id="03b92-197">Questo spazio è fisso in un sistema di coordinate HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="03b92-197">This space is fixed to a HIMETRIC coordinate system.</span></span> <span data-ttu-id="03b92-198">Nelle coordinate dello spazio input penna, uno spostamento da 0 a 1 equivale a 1 unità HIMETRIC.</span><span class="sxs-lookup"><span data-stu-id="03b92-198">In ink space coordinates, a move from 0 to 1 equals 1 HIMETRIC unit.</span></span> <span data-ttu-id="03b92-199">Questo mapping semplifica la relazione tra più **oggetti InkDisp.**</span><span class="sxs-lookup"><span data-stu-id="03b92-199">This mapping makes it easy to relate multiple **InkDisp** objects.</span></span>

<span data-ttu-id="03b92-200">[**L'oggetto InkRenderer**](inkrenderer-class.md) gestisce i mapping tra input penna e finestra di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="03b92-200">The [**InkRenderer**](inkrenderer-class.md) object manages the mappings between ink and the display window.</span></span>

## <a name="requirements"></a><span data-ttu-id="03b92-201">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03b92-201">Requirements</span></span>



| <span data-ttu-id="03b92-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="03b92-202">Requirement</span></span> | <span data-ttu-id="03b92-203">Valore</span><span class="sxs-lookup"><span data-stu-id="03b92-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03b92-204">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03b92-204">Minimum supported client</span></span><br/> | <span data-ttu-id="03b92-205">Solo app desktop Windows XP Tablet PC \[ Edition\]</span><span class="sxs-lookup"><span data-stu-id="03b92-205">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="03b92-206">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03b92-206">Minimum supported server</span></span><br/> | <span data-ttu-id="03b92-207">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="03b92-207">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="03b92-208">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03b92-208">Header</span></span><br/>                   | <dl> <span data-ttu-id="03b92-209"><dt>Msinkaut.h (richiede anche Msinkaut \_ i.c)</dt></span><span class="sxs-lookup"><span data-stu-id="03b92-209"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="03b92-210">Libreria</span><span class="sxs-lookup"><span data-stu-id="03b92-210">Library</span></span><br/>                  | <dl> <span data-ttu-id="03b92-211"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03b92-211"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="03b92-212">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03b92-212">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03b92-213">**Interfaccia IInkStrokeDisp**</span><span class="sxs-lookup"><span data-stu-id="03b92-213">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> <dt>

<span data-ttu-id="03b92-214">[Raccolta InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="03b92-214">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="03b92-215">**Interfaccia IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="03b92-215">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

