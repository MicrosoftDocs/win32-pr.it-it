---
description: L'oggetto PenInputPanel consente di aggiungere facilmente input penna sul posto alle applicazioni.
ms.assetid: ad63302e-b386-4b32-95bf-be1129839c33
title: Classe PenInputPanel (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PenInputPanel
- PenInputPanel.IPenInputPanel
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 0564f758d47e516873b8df5020f3f03a5bcb0727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319159"
---
# <a name="peninputpanel-class"></a><span data-ttu-id="83192-103">Classe PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="83192-103">PenInputPanel class</span></span>

<span data-ttu-id="83192-104">\[Deprecato.</span><span class="sxs-lookup"><span data-stu-id="83192-104">\[Deprecated.</span></span> <span data-ttu-id="83192-105">**PenInputPanel** è stato sostituito dal [Pannello di input di testo (tip)](text-input-panel-reference.md).\]</span><span class="sxs-lookup"><span data-stu-id="83192-105">**PenInputPanel** has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).\]</span></span>

<span data-ttu-id="83192-106">L'oggetto **PenInputPanel** consente di aggiungere facilmente input penna sul posto alle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="83192-106">The **PenInputPanel** object enables you to easily add in-place pen input to your applications.</span></span>

<span data-ttu-id="83192-107">L'oggetto **PenInputPanel** è disponibile come oggetto collegato che consente di aggiungere la funzionalità del pannello di input di Tablet PC ai controlli esistenti.</span><span class="sxs-lookup"><span data-stu-id="83192-107">The **PenInputPanel** object is available as an attachable object that allows you to add Tablet PC Input Panel functionality to existing controls.</span></span> <span data-ttu-id="83192-108">L'interfaccia utente è in gran parte obbligatoria dalla lingua di input corrente.</span><span class="sxs-lookup"><span data-stu-id="83192-108">The user interface is largely mandated by the current input language.</span></span> <span data-ttu-id="83192-109">È possibile scegliere il metodo di input predefinito per l'oggetto **PenInputPanel** , ovvero la grafia o la tastiera.</span><span class="sxs-lookup"><span data-stu-id="83192-109">You have the option of choosing the default input method for the **PenInputPanel** object, either handwriting or keyboard.</span></span> <span data-ttu-id="83192-110">L'utente finale può passare da un metodo di input all'altra usando i pulsanti dell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="83192-110">The end user can switch between input methods using buttons on the user interface.</span></span>

<span data-ttu-id="83192-111">**PenInputPanel** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="83192-111">**PenInputPanel** has these types of members:</span></span>

-   [<span data-ttu-id="83192-112">Enumerazioni</span><span class="sxs-lookup"><span data-stu-id="83192-112">Enumerations</span></span>](#enumerations)
-   [<span data-ttu-id="83192-113">Eventi</span><span class="sxs-lookup"><span data-stu-id="83192-113">Events</span></span>](#events)
-   [<span data-ttu-id="83192-114">Interfacce</span><span class="sxs-lookup"><span data-stu-id="83192-114">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="83192-115">Metodi</span><span class="sxs-lookup"><span data-stu-id="83192-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="83192-116">Proprietà</span><span class="sxs-lookup"><span data-stu-id="83192-116">Properties</span></span>](#properties)

### <a name="enumerations"></a><span data-ttu-id="83192-117">Enumerazioni</span><span class="sxs-lookup"><span data-stu-id="83192-117">Enumerations</span></span>

<span data-ttu-id="83192-118">La classe **PenInputPanel** presenta queste enumerazioni.</span><span class="sxs-lookup"><span data-stu-id="83192-118">The **PenInputPanel** class has these enumerations.</span></span>



| <span data-ttu-id="83192-119">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="83192-119">Enumeration</span></span>                    | <span data-ttu-id="83192-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83192-120">Description</span></span>                                                                               |
|:-------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83192-121">**PanelType**</span><span class="sxs-lookup"><span data-stu-id="83192-121">**PanelType**</span></span>](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) | <span data-ttu-id="83192-122">Definisce il tipo di input attualmente disponibile nell'oggetto **PenInputPanel** .</span><span class="sxs-lookup"><span data-stu-id="83192-122">Defines the type of input currently available in the **PenInputPanel** object.</span></span><br/> |



 

### <a name="events"></a><span data-ttu-id="83192-123">Eventi</span><span class="sxs-lookup"><span data-stu-id="83192-123">Events</span></span>

<span data-ttu-id="83192-124">La classe **PenInputPanel** presenta questi eventi.</span><span class="sxs-lookup"><span data-stu-id="83192-124">The **PenInputPanel** class has these events.</span></span>



| <span data-ttu-id="83192-125">Event</span><span class="sxs-lookup"><span data-stu-id="83192-125">Event</span></span>                                                  | <span data-ttu-id="83192-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83192-126">Description</span></span>                                                                                                                             |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83192-127">**InputFailed**</span><span class="sxs-lookup"><span data-stu-id="83192-127">**InputFailed**</span></span>](peninputpanel-inputfailed.md)       | <span data-ttu-id="83192-128">Si verifica quando lo stato attivo per l'input cambia prima che l'oggetto **PenInputPanel** fosse in grado di inserire l'input dell'utente nel controllo associato.</span><span class="sxs-lookup"><span data-stu-id="83192-128">Occurs when input focus changes before the **PenInputPanel** object was able to insert user input into the attached control.</span></span><br/> |
| [<span data-ttu-id="83192-129">**PanelChanged**</span><span class="sxs-lookup"><span data-stu-id="83192-129">**PanelChanged**</span></span>](peninputpanel-panelchanged.md)     | <span data-ttu-id="83192-130">Si verifica in seguito alla modifica dell'oggetto **PenInputPanel** tra layout.</span><span class="sxs-lookup"><span data-stu-id="83192-130">Occurs when the **PenInputPanel** object changes between layouts.</span></span><br/>                                                            |
| [<span data-ttu-id="83192-131">**PanelMoving**</span><span class="sxs-lookup"><span data-stu-id="83192-131">**PanelMoving**</span></span>](peninputpanel-panelmoving.md)       | <span data-ttu-id="83192-132">Si verifica quando l'oggetto **PenInputPanel** viene spostato.</span><span class="sxs-lookup"><span data-stu-id="83192-132">Occurs when the **PenInputPanel** object is moving.</span></span><br/>                                                                          |
| [<span data-ttu-id="83192-133">**VisibleChanged**</span><span class="sxs-lookup"><span data-stu-id="83192-133">**VisibleChanged**</span></span>](peninputpanel-visiblechanged.md) | <span data-ttu-id="83192-134">Si verifica quando l'oggetto **PenInputPanel** è stato visualizzato o nascosto.</span><span class="sxs-lookup"><span data-stu-id="83192-134">Occurs when the **PenInputPanel** object has shown or hidden itself.</span></span><br/>                                                         |



 

### <a name="interfaces"></a><span data-ttu-id="83192-135">Interfacce</span><span class="sxs-lookup"><span data-stu-id="83192-135">Interfaces</span></span>

<span data-ttu-id="83192-136">La classe **PenInputPanel** definisce queste interfacce.</span><span class="sxs-lookup"><span data-stu-id="83192-136">The **PenInputPanel** class defines these interfaces.</span></span>



| <span data-ttu-id="83192-137">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="83192-137">Interface</span></span>          | <span data-ttu-id="83192-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83192-138">Description</span></span>                                                             |
|:-------------------|:------------------------------------------------------------------------|
| <span data-ttu-id="83192-139">**IPenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="83192-139">**IPenInputPanel**</span></span> | <span data-ttu-id="83192-140">Questo oggetto implementa l'interfaccia com **IPenInputPanel** .</span><span class="sxs-lookup"><span data-stu-id="83192-140">This object implements the **IPenInputPanel** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="83192-141">Metodi</span><span class="sxs-lookup"><span data-stu-id="83192-141">Methods</span></span>

<span data-ttu-id="83192-142">La classe **PenInputPanel** presenta questi metodi.</span><span class="sxs-lookup"><span data-stu-id="83192-142">The **PenInputPanel** class has these methods.</span></span>



| <span data-ttu-id="83192-143">Metodo</span><span class="sxs-lookup"><span data-stu-id="83192-143">Method</span></span>                                                         | <span data-ttu-id="83192-144">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83192-144">Description</span></span>                                                                                                                                                                                             |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83192-145">**CommitPendingInput**</span><span class="sxs-lookup"><span data-stu-id="83192-145">**CommitPendingInput**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) | <span data-ttu-id="83192-146">Invia l'input penna raccolto al riconoscimento e invia il risultato del riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="83192-146">Sends collected ink to the recognizer and posts the recognition result.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="83192-147">**EnableTsf**</span><span class="sxs-lookup"><span data-stu-id="83192-147">**EnableTsf**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-enabletsf)                   | <span data-ttu-id="83192-148">Quando viene passato **true**, l'oggetto **PenInputPanel** tenta di inviare il testo al controllo collegato tramite il Framework di servizi di testo (TSF) e consente l'uso dell'interfaccia utente di correzione.</span><span class="sxs-lookup"><span data-stu-id="83192-148">When passed **TRUE**, the **PenInputPanel** attempts to send text to the attached control through the Text Services Framework (TSF) and enables the use of the correction user interface.</span></span><br/>    |
| [<span data-ttu-id="83192-149">**MoveTo**</span><span class="sxs-lookup"><span data-stu-id="83192-149">**MoveTo**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto)                         | <span data-ttu-id="83192-150">Imposta la posizione dell'oggetto **PenInputPanel** su una posizione dello schermo statica.</span><span class="sxs-lookup"><span data-stu-id="83192-150">Sets the position of the **PenInputPanel** object to a static screen position.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="83192-151">**Aggiorna**</span><span class="sxs-lookup"><span data-stu-id="83192-151">**Refresh**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)                       | <span data-ttu-id="83192-152">Aggiorna e ripristina le proprietà **PenInputPanel** basate sulle impostazioni del pannello di input di Tablet PC, posiziona automaticamente il pannello input penna e imposta l'interfaccia utente sul pannello predefinito.</span><span class="sxs-lookup"><span data-stu-id="83192-152">Updates and restores the **PenInputPanel** properties based on Tablet PC Input Panel settings, automatically positions the pen input panel and sets the user interface to the default panel.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="83192-153">Proprietà</span><span class="sxs-lookup"><span data-stu-id="83192-153">Properties</span></span>

<span data-ttu-id="83192-154">La classe **PenInputPanel** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="83192-154">The **PenInputPanel** class has these properties.</span></span>



| <span data-ttu-id="83192-155">Proprietà</span><span class="sxs-lookup"><span data-stu-id="83192-155">Property</span></span>                                                                  | <span data-ttu-id="83192-156">Tipo di accesso</span><span class="sxs-lookup"><span data-stu-id="83192-156">Access type</span></span>           | <span data-ttu-id="83192-157">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83192-157">Description</span></span>                                                                                                                                                                    |
|:--------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="83192-158">**AttachedEditWindow**</span><span class="sxs-lookup"><span data-stu-id="83192-158">**AttachedEditWindow**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow)<br/> | <span data-ttu-id="83192-159">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="83192-159">Read/write</span></span><br/> | <span data-ttu-id="83192-160">Ottiene o imposta l'handle della finestra del controllo a cui è associato l'oggetto **PenInputPanel** .</span><span class="sxs-lookup"><span data-stu-id="83192-160">Gets or sets the window handle of the control that the **PenInputPanel** object is attached to.</span></span><br/>                                                                     |
| [<span data-ttu-id="83192-161">**AutoShow**</span><span class="sxs-lookup"><span data-stu-id="83192-161">**AutoShow**</span></span>](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)<br/>                     | <span data-ttu-id="83192-162">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="83192-162">Read/write</span></span><br/> | <span data-ttu-id="83192-163">Ottiene o imposta un valore booleano che specifica se l'oggetto **PenInputPanel** viene visualizzato quando lo stato attivo viene impostato utilizzando la penna.</span><span class="sxs-lookup"><span data-stu-id="83192-163">Gets or sets a Boolean value that specifies whether the **PenInputPanel** object appears when focus is set using the pen.</span></span><br/>                                           |
| [<span data-ttu-id="83192-164">**Occupato**</span><span class="sxs-lookup"><span data-stu-id="83192-164">**Busy**</span></span>](/windows/desktop/api/Peninputpanel/nf-peninputpanel-ipeninputpanel-get_busy)<br/>                             | <span data-ttu-id="83192-165">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="83192-165">Read-only</span></span><br/>  | <span data-ttu-id="83192-166">Ottiene un valore booleano che specifica se l'oggetto **PenInputPanel** sta attualmente elaborando l'input penna.</span><span class="sxs-lookup"><span data-stu-id="83192-166">Gets a Boolean value that specifies whether the **PenInputPanel** object is currently processing ink.</span></span><br/>                                                               |
| [<span data-ttu-id="83192-167">**CurrentPanel**</span><span class="sxs-lookup"><span data-stu-id="83192-167">**CurrentPanel**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel)<br/>             | <span data-ttu-id="83192-168">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="83192-168">Read/write</span></span><br/> | <span data-ttu-id="83192-169">Ottiene o imposta il tipo di pannello attualmente utilizzato per l'input all'interno dell'oggetto **PenInputPanel** .</span><span class="sxs-lookup"><span data-stu-id="83192-169">Gets or sets which panel type is currently being used for input within the **PenInputPanel** object.</span></span><br/>                                                                |
| [<span data-ttu-id="83192-170">**DefaultPanel**</span><span class="sxs-lookup"><span data-stu-id="83192-170">**DefaultPanel**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_defaultpanel)<br/>             | <span data-ttu-id="83192-171">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="83192-171">Read/write</span></span><br/> | <span data-ttu-id="83192-172">Ottiene o imposta il tipo di pannello predefinito utilizzato per l'input all'interno dell'oggetto **PenInputPanel** .</span><span class="sxs-lookup"><span data-stu-id="83192-172">Gets or sets which panel type is the default panel type used for input within the **PenInputPanel** object.</span></span><br/>                                                         |
| [<span data-ttu-id="83192-173">**Factoid**</span><span class="sxs-lookup"><span data-stu-id="83192-173">**Factoid**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)<br/>                       | <span data-ttu-id="83192-174">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="83192-174">Read/write</span></span><br/> | <span data-ttu-id="83192-175">Ottiene o imposta il nome di stringa del controllo del controllo utilizzato per il riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="83192-175">Gets or sets the string name of the factoid used in recognition.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="83192-176">**Altezza**</span><span class="sxs-lookup"><span data-stu-id="83192-176">**Height**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_height)<br/>                         | <span data-ttu-id="83192-177">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="83192-177">Read-only</span></span><br/>  | <span data-ttu-id="83192-178">Ottiene l'altezza dell'oggetto **PenInputPanel** nelle coordinate del client.</span><span class="sxs-lookup"><span data-stu-id="83192-178">Gets the height of the **PenInputPanel** object in client coordinates.</span></span><br/>                                                                                              |
| [<span data-ttu-id="83192-179">**HorizontalOffset**</span><span class="sxs-lookup"><span data-stu-id="83192-179">**HorizontalOffset**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset)<br/>     | <span data-ttu-id="83192-180">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="83192-180">Read/write</span></span><br/> | <span data-ttu-id="83192-181">Ottiene o imposta l'offset tra il bordo sinistro dell'oggetto **PenInputPanel** e il bordo sinistro del controllo a cui è collegato.</span><span class="sxs-lookup"><span data-stu-id="83192-181">Gets or sets the offset between the left edge of the **PenInputPanel** object and the left edge of the control to which it is attached.</span></span><br/>                             |
| [<span data-ttu-id="83192-182">**Sinistra**</span><span class="sxs-lookup"><span data-stu-id="83192-182">**Left**</span></span>](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left)<br/>                             | <span data-ttu-id="83192-183">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="83192-183">Read-only</span></span><br/>  | <span data-ttu-id="83192-184">Ottiene la posizione orizzontale, o asse x, del bordo sinistro dell'oggetto **PenInputPanel** , in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="83192-184">Gets the horizontal, or x-axis, location of the left edge of the **PenInputPanel** object, in screen coordinates.</span></span><br/>                                                   |
| [<span data-ttu-id="83192-185">**In alto**</span><span class="sxs-lookup"><span data-stu-id="83192-185">**Top**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top)<br/>                               | <span data-ttu-id="83192-186">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="83192-186">Read-only</span></span><br/>  | <span data-ttu-id="83192-187">Ottiene l'asse verticale, o asse y, della posizione del bordo superiore dell'oggetto **PenInputPanel** , in coordinate dello schermo.</span><span class="sxs-lookup"><span data-stu-id="83192-187">Gets the vertical, or y-axis, location of the top edge of the **PenInputPanel** object, in screen coordinates.</span></span><br/>                                                      |
| [<span data-ttu-id="83192-188">**VerticalOffset**</span><span class="sxs-lookup"><span data-stu-id="83192-188">**VerticalOffset**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset)<br/>         | <span data-ttu-id="83192-189">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="83192-189">Read/write</span></span><br/> | <span data-ttu-id="83192-190">Ottiene o imposta l'offset tra il bordo orizzontale più vicino dell'oggetto **PenInputPanel** e il bordo orizzontale più vicino al controllo a cui è collegato.</span><span class="sxs-lookup"><span data-stu-id="83192-190">Gets or sets the offset between the closest horizontal edge of the **PenInputPanel** object and the closest horizontal edge of the control to which it is attached.</span></span><br/> |
| [<span data-ttu-id="83192-191">**Visible**</span><span class="sxs-lookup"><span data-stu-id="83192-191">**Visible**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_visible)<br/>                       | <span data-ttu-id="83192-192">Lettura/Scrittura</span><span class="sxs-lookup"><span data-stu-id="83192-192">Read/write</span></span><br/> | <span data-ttu-id="83192-193">Ottiene o imposta un valore che indica se l'oggetto **PenInputPanel** è visibile.</span><span class="sxs-lookup"><span data-stu-id="83192-193">Gets or sets a value that indicates whether the **PenInputPanel** object is visible.</span></span><br/>                                                                                |
| [<span data-ttu-id="83192-194">**Larghezza**</span><span class="sxs-lookup"><span data-stu-id="83192-194">**Width**</span></span>](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_width)<br/>                           | <span data-ttu-id="83192-195">Sola lettura</span><span class="sxs-lookup"><span data-stu-id="83192-195">Read-only</span></span><br/>  | <span data-ttu-id="83192-196">Ottiene la larghezza dell'oggetto **PenInputPanel** nelle coordinate del client.</span><span class="sxs-lookup"><span data-stu-id="83192-196">Gets the width of the **PenInputPanel** object in client coordinates.</span></span><br/>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="83192-197">Commenti</span><span class="sxs-lookup"><span data-stu-id="83192-197">Remarks</span></span>

<span data-ttu-id="83192-198">È possibile creare un'istanza di questo oggetto chiamando il metodo [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) in C++.</span><span class="sxs-lookup"><span data-stu-id="83192-198">This object can be instantiated by calling the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

## <a name="requirements"></a><span data-ttu-id="83192-199">Requisiti</span><span class="sxs-lookup"><span data-stu-id="83192-199">Requirements</span></span>



| <span data-ttu-id="83192-200">Requisito</span><span class="sxs-lookup"><span data-stu-id="83192-200">Requirement</span></span> | <span data-ttu-id="83192-201">Valore</span><span class="sxs-lookup"><span data-stu-id="83192-201">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83192-202">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83192-202">Minimum supported client</span></span><br/> | <span data-ttu-id="83192-203">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="83192-203">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="83192-204">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="83192-204">Minimum supported server</span></span><br/> | <span data-ttu-id="83192-205">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="83192-205">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="83192-206">Intestazione</span><span class="sxs-lookup"><span data-stu-id="83192-206">Header</span></span><br/>                   | <dl> <span data-ttu-id="83192-207"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="83192-207"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="83192-208">Libreria</span><span class="sxs-lookup"><span data-stu-id="83192-208">Library</span></span><br/>                  | <dl> <span data-ttu-id="83192-209"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83192-209"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="83192-210">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="83192-210">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83192-211">Programmazione del pannello di input usando la classe PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="83192-211">Programming the Input Panel Using the PenInputPanel Class</span></span>](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
