---
description: Questa sezione contiene le proprietà per il controllo InkPicture.
ms.assetid: d724c177-af57-4c99-94f2-c70904910b49
title: Proprietà InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ae8149098b34a70af5e088814e2a5258b0fa0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759527"
---
# <a name="inkpicture-properties"></a><span data-ttu-id="4ab98-103">Proprietà InkPicture</span><span class="sxs-lookup"><span data-stu-id="4ab98-103">InkPicture Properties</span></span>

<span data-ttu-id="4ab98-104">Questa sezione contiene le proprietà per il controllo InkPicture.</span><span class="sxs-lookup"><span data-stu-id="4ab98-104">This section contains Properties for the InkPicture Control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4ab98-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4ab98-105">Property</span></span></th>
<th><span data-ttu-id="4ab98-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ab98-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4ab98-107"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>Proprietà AutoRedraw</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-107"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_autoredraw"><strong>AutoRedraw Property</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-108">Ottiene o imposta un valore che specifica se il controllo <a href="inkpicture-control-reference.md">InkPicture</a> viene ridisegnato quando la finestra viene invalidata (se l'oggetto <a href="inkdisp-class.md"><strong>InkDisp</strong></a> attualmente associato al controllo InkPicture viene ridisegnato automaticamente quando la finestra associata a InkPicture riceve un messaggio di WM_PAINT).</span><span class="sxs-lookup"><span data-stu-id="4ab98-108">Gets or sets a value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control repaints when the window is invalidated (whether the <a href="inkdisp-class.md"><strong>InkDisp</strong></a> object currently associated with InkPicture control is automatically redrawn when the window associated with the InkPicture receives a WM_PAINT message).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ab98-109"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>BackColor</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-109"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_backcolor"><strong>BackColor</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-110">Ottiene o imposta il colore di sfondo per il controllo <a href="inkpicture-control-reference.md">InkPicture</a> .</span><span class="sxs-lookup"><span data-stu-id="4ab98-110">Gets or sets the background color for the <a href="inkpicture-control-reference.md">InkPicture</a> control.</span></span> <span data-ttu-id="4ab98-111">Il colore di sfondo predefinito è il colore di sfondo della finestra di sistema, in genere bianco.</span><span class="sxs-lookup"><span data-stu-id="4ab98-111">The default background color is the system window background color, which is typically white.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ab98-112"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>Proprietà CollectingInk</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-112"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectingink"><strong>CollectingInk Property</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-113">Ottiene il valore che specifica se il controllo <a href="inkpicture-control-reference.md">InkPicture</a> sta raccogliendo input penna (solo in fase di esecuzione).</span><span class="sxs-lookup"><span data-stu-id="4ab98-113">Gets the value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control is collecting ink (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ab98-114"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-114"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_collectionmode"><strong>CollectionMode</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-115">Ottiene o imposta la modalità di raccolta che determina se l'input penna, i movimenti o l'input penna e i movimenti vengono riconosciuti durante la scrittura da parte dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4ab98-115">Gets or sets the collection mode that determines whether ink, gestures, or ink and gestures are recognized as the user writes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ab98-116"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursors (proprietà)</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-116"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_cursors"><strong>Cursors Property</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-117">Ottiene la raccolta <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors</strong></a> disponibile per l'utilizzo nell'area Inking del controllo <a href="inkpicture-control-reference.md">InkPicture</a> .</span><span class="sxs-lookup"><span data-stu-id="4ab98-117">Gets the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursors"><strong>IInkCursors</strong></a> collection available for use in the <a href="inkpicture-control-reference.md">InkPicture</a> control's inking region.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ab98-118"><a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>CustomStrokes</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-118"><a href="/previous-versions/windows/desktop/legacy/ms703274(v=vs.85)"><strong>CustomStrokes</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-119">Ottiene la raccolta <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>IInkCustomStrokes</strong></a> da salvare in modo permanente con l'input penna (solo in fase di progettazione).</span><span class="sxs-lookup"><span data-stu-id="4ab98-119">Gets the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkcustomstrokes"><strong>IInkCustomStrokes</strong></a> collection to be persisted with the ink (design-time only).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ab98-120"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>Proprietà DefaultDrawingAttributes</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-120"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_defaultdrawingattributes"><strong>DefaultDrawingAttributes Property</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-121">Ottiene o imposta la raccolta <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes</strong></a> predefinita da utilizzare durante il disegno e la visualizzazione dell'input penna (solo in fase di esecuzione).</span><span class="sxs-lookup"><span data-stu-id="4ab98-121">Gets or sets the default <a href="inkdrawingattributes-class.md"><strong>InkDrawingAttributes</strong></a> collection to use when drawing and displaying ink (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ab98-122"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>Proprietà DesiredPacketDescription</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-122"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription"><strong>DesiredPacketDescription Property</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-123">Ottiene o imposta la descrizione del pacchetto del controllo <a href="inkpicture-control-reference.md">InkPicture</a> (solo in fase di esecuzione).</span><span class="sxs-lookup"><span data-stu-id="4ab98-123">Gets or sets the packet description of the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ab98-124"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>Proprietà DynamicRendering</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-124"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_dynamicrendering"><strong>DynamicRendering Property</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-125">Ottiene o imposta il valore che specifica se il controllo <a href="inkpicture-control-reference.md">InkPicture</a> esegue dinamicamente il rendering dell'input penna durante la raccolta.</span><span class="sxs-lookup"><span data-stu-id="4ab98-125">Gets or sets the value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control dynamically renders the ink as it is collected.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ab98-126"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-126"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode"><strong>EditingMode</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-127">Ottiene o imposta un valore che specifica se il controllo <a href="inkpicture-control-reference.md">InkPicture</a> è in modalità input penna, modalità di eliminazione o selezione/modifica.</span><span class="sxs-lookup"><span data-stu-id="4ab98-127">Gets or sets a value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control is in ink mode, deletion mode, or selecting/editing mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ab98-128"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Abilitato</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-128"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_enabled"><strong>Enabled</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-129">Ottiene o imposta un valore che determina se il controllo <a href="inkpicture-control-reference.md">InkPicture</a> può rispondere agli eventi generati dall'utente.</span><span class="sxs-lookup"><span data-stu-id="4ab98-129">Gets or sets a value that determines whether the <a href="inkpicture-control-reference.md">InkPicture</a> control can respond to user-generated events.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4ab98-130">Questa proprietà è equivalente alla proprietà <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="4ab98-130">This property is equivalent to the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a> property.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ab98-131"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-131"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_erasermode"><strong>EraserMode</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-132">Ottiene o imposta il valore che specifica se l'input penna è stato cancellato dal tratto o dal punto.</span><span class="sxs-lookup"><span data-stu-id="4ab98-132">Gets or sets the value that specifies whether ink is erased by stroke or by point.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ab98-133"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-133"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_eraserwidth"><strong>EraserWidth</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-134">Ottiene o imposta il valore che specifica la larghezza della descrizione della penna della gomma.</span><span class="sxs-lookup"><span data-stu-id="4ab98-134">Gets or sets the value that specifies the width of the eraser pen tip.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ab98-135"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>hWnd</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-135"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_hwnd"><strong>hWnd</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-136">Ottiene l'handle della finestra a cui è associato il controllo <a href="inkpicture-control-reference.md">InkPicture</a> .</span><span class="sxs-lookup"><span data-stu-id="4ab98-136">Gets the window handle to which the <a href="inkpicture-control-reference.md">InkPicture</a> control is bound.</span></span> <span data-ttu-id="4ab98-137">(solo in fase di esecuzione)</span><span class="sxs-lookup"><span data-stu-id="4ab98-137">(run time only)</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ab98-138"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Input penna</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-138"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink"><strong>Ink</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-139">Ottiene o imposta l'oggetto <a href="inkdisp-class.md"><strong>InkDisp</strong></a> associato al controllo <a href="inkpicture-control-reference.md">InkPicture</a> (solo in fase di esecuzione).</span><span class="sxs-lookup"><span data-stu-id="4ab98-139">Gets or sets the <a href="inkdisp-class.md"><strong>InkDisp</strong></a> object that is associated with the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ab98-140"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-140"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled"><strong>InkEnabled</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-141">Ottiene o imposta un valore che specifica se il controllo <a href="inkpicture-control-reference.md">InkPicture</a> raccoglie l'input penna, ovvero i pacchetti in aria, il cursore negli eventi di intervallo e così via.</span><span class="sxs-lookup"><span data-stu-id="4ab98-141">Gets or sets a value that specifies whether the <a href="inkpicture-control-reference.md">InkPicture</a> control collects pen input (in-air packets, cursor in range events, and so on).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ab98-142"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>Proprietà MarginX</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-142"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginx"><strong>MarginX Property</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-143">Ottiene o imposta il margine dell'asse x intorno al rettangolo della finestra nelle coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="4ab98-143">Gets or sets the x-axis margin around the window rectangle in screen coordinates.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ab98-144"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>Proprietà MarginY</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-144"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_marginy"><strong>MarginY Property</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-145">Ottiene o imposta il margine dell'asse y intorno al rettangolo della finestra nelle coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="4ab98-145">Gets or sets the y-axis margin around the window rectangle in screen coordinates.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ab98-146"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>Proprietà MouseIcon</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-146"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mouseicon"><strong>MouseIcon Property</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-147">Ottiene o imposta l'icona del mouse personalizzata corrente.</span><span class="sxs-lookup"><span data-stu-id="4ab98-147">Gets or sets the current custom mouse icon.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ab98-148"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>Proprietà MousePointer</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-148"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer"><strong>MousePointer Property</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-149">Ottiene o imposta un valore che indica il tipo di puntatore del mouse visualizzato quando il mouse si trova su una particolare parte del controllo <a href="inkpicture-control-reference.md">InkPicture</a> .</span><span class="sxs-lookup"><span data-stu-id="4ab98-149">Gets or sets a value that indicates the type of mouse pointer that appears when the mouse is over a particular part of the <a href="inkpicture-control-reference.md">InkPicture</a> control.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ab98-150"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Immagine</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-150"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_picture"><strong>Picture</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-151">Ottiene il file di grafica da visualizzare nel controllo <a href="inkpicture-control-reference.md">InkPicture</a> .</span><span class="sxs-lookup"><span data-stu-id="4ab98-151">Gets the graphics file to appear on the <a href="inkpicture-control-reference.md">InkPicture</a> control.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ab98-152"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Renderer (proprietà)</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-152"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_renderer"><strong>Renderer Property</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-153">Ottiene o imposta l'oggetto <a href="inkrenderer-class.md"><strong>InkRenderer</strong></a> utilizzato per creare l'input penna nel controllo <a href="inkpicture-control-reference.md">InkPicture</a> (solo in fase di esecuzione).</span><span class="sxs-lookup"><span data-stu-id="4ab98-153">Gets or sets the <a href="inkrenderer-class.md"><strong>InkRenderer</strong></a> object that is used to draw ink on the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ab98-154"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Selezione</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-154"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection"><strong>Selection</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-155">Ottiene la raccolta <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> attualmente selezionata all'interno del controllo <a href="inkpicture-control-reference.md">InkPicture</a> (solo in fase di esecuzione).</span><span class="sxs-lookup"><span data-stu-id="4ab98-155">Gets the <a href="/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)">InkStrokes</a> collection currently selected inside the <a href="inkpicture-control-reference.md">InkPicture</a> control (run time only).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ab98-156"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-156"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode"><strong>SizeMode</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-157">Ottiene o imposta il modo in cui il controllo gestisce il posizionamento e il ridimensionamento delle immagini.</span><span class="sxs-lookup"><span data-stu-id="4ab98-157">Gets or sets how the control handles image placement and sizing.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ab98-158"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>Proprietà SupportHighContrastInk</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-158"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastink"><strong>SupportHighContrastInk Property</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-159">Ottiene un valore che specifica se viene eseguito il rendering dell'input penna come un solo colore, color = COLOR_WINDOWTEXT (dalla chiamata GetSystemMetrics) quando il sistema è in modalità Contrasto elevato.</span><span class="sxs-lookup"><span data-stu-id="4ab98-159">Gets a value that specifies whether ink is rendered as just one color, Color = COLOR_WINDOWTEXT (from the GetSystemMetrics call) when the system is in High Contrast mode.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4ab98-160"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-160"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_supporthighcontrastselectionui"><strong>SupportHighContrastSelectionUI</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-161">Ottiene o imposta un valore che specifica se tutte le interfacce utente di selezione, ovvero i quadratini di selezione e gli handle di selezione, vengono disegnate con un contrasto elevato quando il sistema è in modalità Contrasto elevato.</span><span class="sxs-lookup"><span data-stu-id="4ab98-161">Gets or sets a value that specifies whether all selection user interfaces (selection bounding box and selection handles) are drawn in high contrast when the system is in High Contrast mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4ab98-162"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Proprietà Tablet</strong></a></span><span class="sxs-lookup"><span data-stu-id="4ab98-162"><a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_tablet"><strong>Tablet Property</strong></a></span></span></td>
<td><span data-ttu-id="4ab98-163">Ottiene l'oggetto <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet</strong></a> attualmente utilizzato dal controllo <a href="inkpicture-control-reference.md">InkPicture</a> per raccogliere input.</span><span class="sxs-lookup"><span data-stu-id="4ab98-163">Gets the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet"><strong>IInkTablet</strong></a> object that the <a href="inkpicture-control-reference.md">InkPicture</a> control is currently using to collect input.</span></span><br/></td>
</tr>
</tbody>
</table>



 

