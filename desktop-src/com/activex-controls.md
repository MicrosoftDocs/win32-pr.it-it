---
title: Controlli ActiveX
description: Controlli ActiveX
ms.assetid: e491b66c-d6ba-4476-8413-7a9e41c05e8d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b75aabfbf2b81b4a4d3a45a1868a6eebf6fd4e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399748"
---
# <a name="activex-controls"></a><span data-ttu-id="793f3-103">Controlli ActiveX</span><span class="sxs-lookup"><span data-stu-id="793f3-103">ActiveX Controls</span></span>

<span data-ttu-id="793f3-104">La tecnologia dei controlli ActiveX si basa su una base costituita da COM, oggetti collegabili, documenti composti, pagine delle proprietà, automazione OLE, persistenza degli oggetti e oggetti di tipo carattere e immagine forniti dal sistema.</span><span class="sxs-lookup"><span data-stu-id="793f3-104">ActiveX controls technology rests on a foundation consisting of COM, connectable objects, compound documents, property pages, OLE automation, object persistence, and system-provided font and picture objects.</span></span> <span data-ttu-id="793f3-105">Come riepilogato di seguito, ognuna di queste tecnologie di base svolge un ruolo nei controlli.</span><span class="sxs-lookup"><span data-stu-id="793f3-105">As summarized below, each of these core technologies plays a role in controls.</span></span>

<dl> <dt>

<span data-ttu-id="793f3-106"><span id="COM"></span><span id="com"></span>COM</span><span class="sxs-lookup"><span data-stu-id="793f3-106"><span id="COM"></span><span id="com"></span>COM</span></span>
</dt> <dd>

<span data-ttu-id="793f3-107">Un controllo è essenzialmente un oggetto COM che espone l'interfaccia [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , tramite la quale i client possono ottenere i puntatori alle altre interfacce.</span><span class="sxs-lookup"><span data-stu-id="793f3-107">A control is essentially a COM object that exposes the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, through which clients can obtain pointers to its other interfaces.</span></span> <span data-ttu-id="793f3-108">I controlli possono supportare le licenze tramite [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) e la registrazione automatica.</span><span class="sxs-lookup"><span data-stu-id="793f3-108">Controls can support licensing through [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) and self-registration.</span></span> <span data-ttu-id="793f3-109">Per ulteriori informazioni su COM, sulle licenze e sulla registrazione automatica, vedere [la Component Object Model](the-component-object-model.md) .</span><span class="sxs-lookup"><span data-stu-id="793f3-109">See [The Component Object Model](the-component-object-model.md) for more information on COM, licensing, and self-registration.</span></span>

</dd> <dt>

<span data-ttu-id="793f3-110"><span id="Connectable_objects"></span><span id="connectable_objects"></span><span id="CONNECTABLE_OBJECTS"></span>Oggetti collegabili</span><span class="sxs-lookup"><span data-stu-id="793f3-110"><span id="Connectable_objects"></span><span id="connectable_objects"></span><span id="CONNECTABLE_OBJECTS"></span>Connectable objects</span></span>
</dt> <dd>

<span data-ttu-id="793f3-111">I controlli possono supportare le interfacce in uscita tramite oggetti collegabili, in modo che il controllo possa comunicare con il client.</span><span class="sxs-lookup"><span data-stu-id="793f3-111">Controls can support outgoing interfaces through connectable objects so that the control can communicate with its client.</span></span> <span data-ttu-id="793f3-112">Un'interfaccia in uscita, ad esempio, può attivare un'azione nel client, può notificare al client una modifica nel controllo o richiedere l'autorizzazione al client prima che il controllo esegua un'azione.</span><span class="sxs-lookup"><span data-stu-id="793f3-112">For example, an outgoing interface can trigger an action in the client, can notify the client of some change in the control, or can request permission from the client before the control takes some action.</span></span> <span data-ttu-id="793f3-113">Per ulteriori informazioni sul funzionamento degli oggetti collegabili, vedere [eventi in com e oggetti collegabili](events-in-com-and-connectable-objects.md) .</span><span class="sxs-lookup"><span data-stu-id="793f3-113">See [Events in COM and Connectable Objects](events-in-com-and-connectable-objects.md) for more information on how connectable objects work.</span></span>

</dd> <dt>

<span data-ttu-id="793f3-114"><span id="Uniform_data_transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Trasferimento dati uniforme</span><span class="sxs-lookup"><span data-stu-id="793f3-114"><span id="Uniform_data_transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Uniform data transfer</span></span>
</dt> <dd>

<span data-ttu-id="793f3-115">I controlli possono supportare il trascinamento e l'eliminazione in un contenitore con supporto dal relativo contenitore.</span><span class="sxs-lookup"><span data-stu-id="793f3-115">Controls can support being dragged and dropped within a container with help from their container.</span></span> <span data-ttu-id="793f3-116">Per ulteriori informazioni sul trascinamento della selezione, vedere [**IOleInPlaceObjectWindowless:: GetDropTarget**](/windows/desktop/api/OCIdl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget) .</span><span class="sxs-lookup"><span data-stu-id="793f3-116">See [**IOleInPlaceObjectWindowless::GetDropTarget**](/windows/desktop/api/OCIdl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget) for more information on drag and drop.</span></span>

</dd> <dt>

<span data-ttu-id="793f3-117"><span id="Compound_documents"></span><span id="compound_documents"></span><span id="COMPOUND_DOCUMENTS"></span>Documenti composti</span><span class="sxs-lookup"><span data-stu-id="793f3-117"><span id="Compound_documents"></span><span id="compound_documents"></span><span id="COMPOUND_DOCUMENTS"></span>Compound documents</span></span>
</dt> <dd>

<span data-ttu-id="793f3-118">Un controllo può essere un oggetto attivo sul posto che può essere incorporato in un client contenitore.</span><span class="sxs-lookup"><span data-stu-id="793f3-118">A control can be an in-place active object that can be embedded in a containing client.</span></span> <span data-ttu-id="793f3-119">Un utente finale attiva il controllo per avviare un'azione nell'applicazione contenitore.</span><span class="sxs-lookup"><span data-stu-id="793f3-119">An end-user activates the control to initiate an action in the container application.</span></span> <span data-ttu-id="793f3-120">Per ulteriori informazioni sull'attivazione sul posto e altre interfacce per documenti compositi, vedere [documenti composti](compound-documents.md) .</span><span class="sxs-lookup"><span data-stu-id="793f3-120">See [Compound Documents](compound-documents.md) for more information on in-place activation and other compound document interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="793f3-121"><span id="Property_pages"></span><span id="property_pages"></span><span id="PROPERTY_PAGES"></span>Pagine delle proprietà</span><span class="sxs-lookup"><span data-stu-id="793f3-121"><span id="Property_pages"></span><span id="property_pages"></span><span id="PROPERTY_PAGES"></span>Property pages</span></span>
</dt> <dd>

<span data-ttu-id="793f3-122">I controlli possono fornire pagine delle proprietà in modo che gli utenti finali possano visualizzare e modificare le proprietà del controllo.</span><span class="sxs-lookup"><span data-stu-id="793f3-122">Controls can provide property pages so end users can view and change the control's properties.</span></span> <span data-ttu-id="793f3-123">Per ulteriori informazioni sul funzionamento delle pagine delle proprietà, vedere pagine delle proprietà [e finestre](property-pages-and-property-sheets.md) delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="793f3-123">See [Property Pages and Property Sheets](property-pages-and-property-sheets.md) for more information on how property pages work.</span></span>

</dd> <dt>

<span data-ttu-id="793f3-124"><span id="OLE_automation"></span><span id="ole_automation"></span><span id="OLE_AUTOMATION"></span>Automazione OLE</span><span class="sxs-lookup"><span data-stu-id="793f3-124"><span id="OLE_automation"></span><span id="ole_automation"></span><span id="OLE_AUTOMATION"></span>OLE automation</span></span>
</dt> <dd>

<span data-ttu-id="793f3-125">I controlli possono garantire la programmabilità tramite l'automazione OLE, in modo che i client possano sfruttare le funzionalità del controllo tramite un linguaggio di programmazione fornito dal client.</span><span class="sxs-lookup"><span data-stu-id="793f3-125">Controls can provide programmability through OLE automation so clients can take advantage of the control's features through a programming language supplied by the client.</span></span> <span data-ttu-id="793f3-126">Per ulteriori informazioni sull'automazione OLE, vedere la sezione automazione OLE.</span><span class="sxs-lookup"><span data-stu-id="793f3-126">See the OLE Automation section for more information on OLE automation.</span></span>

</dd> <dt>

<span data-ttu-id="793f3-127"><span id="Persistent_storage"></span><span id="persistent_storage"></span><span id="PERSISTENT_STORAGE"></span>Archiviazione permanente</span><span class="sxs-lookup"><span data-stu-id="793f3-127"><span id="Persistent_storage"></span><span id="persistent_storage"></span><span id="PERSISTENT_STORAGE"></span>Persistent storage</span></span>
</dt> <dd>

<span data-ttu-id="793f3-128">Un controllo può implementare una o più interfacce di persistenza per supportare la persistenza dello stato.</span><span class="sxs-lookup"><span data-stu-id="793f3-128">A control can implement one or more of several persistence interfaces to support persistence of its state.</span></span> <span data-ttu-id="793f3-129">L'implementatore del controllo deve decidere quali tipi di persistenza sono più importanti e implementare le interfacce di persistenza appropriate.</span><span class="sxs-lookup"><span data-stu-id="793f3-129">The control implementer must decide what kinds of persistence are most important and implement the appropriate persistence interfaces.</span></span> <span data-ttu-id="793f3-130">Il client decide quale interfaccia si preferisce usare.</span><span class="sxs-lookup"><span data-stu-id="793f3-130">The client decides which interface it prefers to use.</span></span> <span data-ttu-id="793f3-131">Per ulteriori informazioni su tutte le interfacce di persistenza, vedere [la Component Object Model](the-component-object-model.md) .</span><span class="sxs-lookup"><span data-stu-id="793f3-131">See [The Component Object Model](the-component-object-model.md) for more information on all the persistence interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="793f3-132"><span id="Font_and_picture_objects"></span><span id="font_and_picture_objects"></span><span id="FONT_AND_PICTURE_OBJECTS"></span>Oggetti Font e Picture</span><span class="sxs-lookup"><span data-stu-id="793f3-132"><span id="Font_and_picture_objects"></span><span id="font_and_picture_objects"></span><span id="FONT_AND_PICTURE_OBJECTS"></span>Font and picture objects</span></span>
</dt> <dd>

<span data-ttu-id="793f3-133">I controlli possono usare questi oggetti forniti dal sistema per fornire una rappresentazione visiva autonoma all'interno del client.</span><span class="sxs-lookup"><span data-stu-id="793f3-133">Controls can use these system provided objects to provide a visual representation of themselves within the client.</span></span> <span data-ttu-id="793f3-134">L'oggetto Font implementa diverse interfacce, tra cui [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) e [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp).</span><span class="sxs-lookup"><span data-stu-id="793f3-134">The font object implements several interfaces, including [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) and [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp).</span></span> <span data-ttu-id="793f3-135">Un oggetto Font può essere creato con [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect).</span><span class="sxs-lookup"><span data-stu-id="793f3-135">A font object can be created with [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect).</span></span> <span data-ttu-id="793f3-136">L'oggetto immagine implementa inoltre diverse interfacce, tra cui [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) e [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp).</span><span class="sxs-lookup"><span data-stu-id="793f3-136">The picture object also implements several interfaces, including [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) and [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp).</span></span> <span data-ttu-id="793f3-137">Un oggetto immagine può essere creato usando [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect) e può essere caricato da un flusso con [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture).</span><span class="sxs-lookup"><span data-stu-id="793f3-137">A picture object can be created using [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect) and can loaded from a stream with [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture).</span></span>

</dd> </dl>

<span data-ttu-id="793f3-138">È importante comprendere che queste funzionalità possono essere utilizzate in qualsiasi oggetto OLE.</span><span class="sxs-lookup"><span data-stu-id="793f3-138">It is important to understand that these features can be used in any OLE object.</span></span> <span data-ttu-id="793f3-139">Non è necessario implementare un controllo per poter utilizzare queste funzionalità.</span><span class="sxs-lookup"><span data-stu-id="793f3-139">One does not need to implement a control in order to use these features.</span></span> <span data-ttu-id="793f3-140">Inoltre, l'unica interfaccia necessaria su un controllo è IUnknown.</span><span class="sxs-lookup"><span data-stu-id="793f3-140">Also, the only required interface on a control is IUnknown.</span></span> <span data-ttu-id="793f3-141">Il controllo supporta facoltativamente altre interfacce basate sulla necessità di supportare le funzionalità correlate.</span><span class="sxs-lookup"><span data-stu-id="793f3-141">The control optionally supports other interfaces based on the need to support the related features.</span></span>

<span data-ttu-id="793f3-142">Oltre a queste funzionalità, le interfacce e le funzioni seguenti sono specifiche della tecnologia dei controlli: [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol), [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite), [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)e [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor).</span><span class="sxs-lookup"><span data-stu-id="793f3-142">In addition to these features, the following interfaces and functions are specific to controls technology: [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol), [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite), [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), and [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor).</span></span> <span data-ttu-id="793f3-143">Anche i controlli sono specifici di un set di standard per le proprietà e i metodi che possono essere supportati da un controllo o da un contenitore di controlli.</span><span class="sxs-lookup"><span data-stu-id="793f3-143">Also specific to controls are a set of standards for properties and methods that a control or a control container can support.</span></span>

> [!Note]  
> <span data-ttu-id="793f3-144">La libreria di sistema OleAut32.dll contiene le implementazioni delle funzioni ([**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe), [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect), [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect), [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture)e [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)).</span><span class="sxs-lookup"><span data-stu-id="793f3-144">The system library OleAut32.dll contains implementations of the functions ([**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe), [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect), [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect), [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture), and [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)).</span></span> <span data-ttu-id="793f3-145">Inoltre, OleAut32.dll contiene le implementazioni degli oggetti di tipo carattere e immagine standard, nonché una libreria dei tipi per tutte le interfacce utilizzate con i controlli, nonché le strutture di dati e i tipi di dati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="793f3-145">In addition, OleAut32.dll contains the implementations of the standard font and picture objects, as well as a type library for all the interfaces used with controls as well as the additional data structures and data types.</span></span>

 

<span data-ttu-id="793f3-146">Per altre informazioni, vedere i seguenti argomenti:</span><span class="sxs-lookup"><span data-stu-id="793f3-146">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="793f3-147">Architettura di controlli ActiveX</span><span class="sxs-lookup"><span data-stu-id="793f3-147">ActiveX Controls Architecture</span></span>](activex-controls-architecture.md)
-   [<span data-ttu-id="793f3-148">Interfacce di controlli ActiveX</span><span class="sxs-lookup"><span data-stu-id="793f3-148">ActiveX Controls Interfaces</span></span>](activex-controls-interfaces.md)
-   [<span data-ttu-id="793f3-149">Proprietà e metodi</span><span class="sxs-lookup"><span data-stu-id="793f3-149">Properties and Methods</span></span>](properties-and-methods.md)
-   [<span data-ttu-id="793f3-150">Eventi di controllo</span><span class="sxs-lookup"><span data-stu-id="793f3-150">Control Events</span></span>](control-events.md)
-   [<span data-ttu-id="793f3-151">Rappresentazione visiva</span><span class="sxs-lookup"><span data-stu-id="793f3-151">Visual Representation</span></span>](visual-representation.md)
-   [<span data-ttu-id="793f3-152">Gestione della tastiera per i controlli</span><span class="sxs-lookup"><span data-stu-id="793f3-152">Keyboard Handling for Controls</span></span>](keyboard-handling-for-controls.md)
-   [<span data-ttu-id="793f3-153">Persistenza</span><span class="sxs-lookup"><span data-stu-id="793f3-153">Persistence</span></span>](persistence.md)
-   [<span data-ttu-id="793f3-154">Registrazione e licenze</span><span class="sxs-lookup"><span data-stu-id="793f3-154">Registration and Licensing</span></span>](registration-and-licensing.md)

## <a name="related-topics"></a><span data-ttu-id="793f3-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="793f3-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="793f3-156">Linee guida per il controllo ActiveX e il controllo del contenitore</span><span class="sxs-lookup"><span data-stu-id="793f3-156">ActiveX Control and Control Container Guidelines</span></span>](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 