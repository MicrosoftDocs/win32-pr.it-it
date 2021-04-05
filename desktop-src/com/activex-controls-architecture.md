---
title: Architettura di controlli ActiveX
description: La tecnologia controlli ActiveX si basa su una base di molti oggetti di livello inferiore e interfacce in OLE. Le interfacce esatte disponibili in un controllo variano in base alle relative funzionalità. In questa sezione vengono esaminate in dettaglio le funzionalità che possono essere fornite da un controllo.
ms.assetid: 42959a11-8bfb-4f7e-ba27-5dc1ed49cdaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d0592d774e1930623803d0769fb7890709a2f21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709553"
---
# <a name="activex-controls-architecture"></a><span data-ttu-id="a8bb0-105">Architettura di controlli ActiveX</span><span class="sxs-lookup"><span data-stu-id="a8bb0-105">ActiveX Controls Architecture</span></span>

<span data-ttu-id="a8bb0-106">La tecnologia controlli ActiveX si basa su una base di molti oggetti di livello inferiore e interfacce in OLE.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-106">ActiveX controls technology builds on a foundation of many lower-level objects and interfaces in OLE.</span></span> <span data-ttu-id="a8bb0-107">Le interfacce esatte disponibili in un controllo variano in base alle relative funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-107">The exact interfaces available on a control vary with its capabilities.</span></span> <span data-ttu-id="a8bb0-108">In questa sezione vengono esaminate in dettaglio le funzionalità che possono essere fornite da un controllo.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-108">This section takes a closer look at the capabilities a control might provide.</span></span>

<span data-ttu-id="a8bb0-109">I controlli ActiveX vengono utilizzati per fornire i blocchi predefiniti per la creazione di interfacce utente nelle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-109">ActiveX controls are used to provide the building blocks for creating user interfaces in applications.</span></span> <span data-ttu-id="a8bb0-110">Ad esempio, un pulsante che avvia un'azione nell'applicazione contenitore quando viene selezionato è un controllo semplice.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-110">For example, a button that initiates some action in the container application when it is clicked is a simple control.</span></span> <span data-ttu-id="a8bb0-111">Per fornire questi blocchi predefiniti dell'interfaccia utente sono necessari gli aspetti seguenti:</span><span class="sxs-lookup"><span data-stu-id="a8bb0-111">The following aspects are involved in providing these user interface building blocks:</span></span>

-   <span data-ttu-id="a8bb0-112">È possibile incorporare un controllo all'interno del client contenitore per supportare alcune attività dell'interfaccia utente all'interno del client.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-112">A control can be embedded within its container client to support some user interface activity within the client.</span></span> <span data-ttu-id="a8bb0-113">Pertanto, un controllo deve fornire una rappresentazione visiva di se stesso quando viene incorporato all'interno del contenitore e deve fornire un modo per salvarne lo stato, ad esempio i valori delle proprietà e la posizione all'interno del relativo contenitore.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-113">Thus, a control needs to provide a visual representation of itself when it is embedded within the container and needs to provide a way to save its state, for example, its property values and its position within its container.</span></span> <span data-ttu-id="a8bb0-114">Il client deve supportare un contenitore con oggetti incorporati.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-114">The client must support being a container with objects embedded in it.</span></span>
-   <span data-ttu-id="a8bb0-115">Attivando il controllo utilizzando una tastiera o un mouse, l'utente finale avvia un'azione nell'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-115">By activating the control using a keyboard or mouse, the end user initiates some action in the client application.</span></span> <span data-ttu-id="a8bb0-116">Pertanto, un controllo deve rispondere all'attività della tastiera e deve essere in grado di comunicare con il client in modo che possa inviare notifiche al contenitore delle attività e attivare gli eventi nel client.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-116">Thus, a control must respond to keyboard activity and must be able to communicate with its client so it can notify its container of its activities and trigger events in the client.</span></span>
-   <span data-ttu-id="a8bb0-117">Il client in genere fornisce anche un linguaggio di programmazione tramite il quale l'utente finale può avviare azioni fornite dalle proprietà e dai metodi del controllo.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-117">The client also typically provides a programming language through which the end user can initiate actions provided by the control's properties and methods.</span></span> <span data-ttu-id="a8bb0-118">In questo modo, un controllo deve supportare l'automazione e alcuni set di funzionalità in fase di progettazione rispetto a quelle di Runtime.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-118">Thus, a control must support automation and some set of design-time versus run-time features as well.</span></span>

<span data-ttu-id="a8bb0-119">Come conseguenza del suo ruolo nell'fornire blocchi predefiniti dell'interfaccia utente, un controllo in genere supporta le funzionalità nelle seguenti aree usando le tecnologie OLE come indicato:</span><span class="sxs-lookup"><span data-stu-id="a8bb0-119">As a result of its role in providing user interface building blocks, a control typically supports features in the following areas using OLE technologies as indicated:</span></span>

<dl> <dt>

<span data-ttu-id="a8bb0-120"><span id="Properties_and_methods"></span><span id="properties_and_methods"></span><span id="PROPERTIES_AND_METHODS"></span>Proprietà e metodi</span><span class="sxs-lookup"><span data-stu-id="a8bb0-120"><span id="Properties_and_methods"></span><span id="properties_and_methods"></span><span id="PROPERTIES_AND_METHODS"></span>Properties and methods</span></span>
</dt> <dd>

<span data-ttu-id="a8bb0-121">Analogamente a qualsiasi oggetto OLE, un controllo può offrire gran parte delle funzionalità tramite un set di interfacce in ingresso con proprietà e metodi.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-121">Like any OLE object, a control can provide much of its functionality through a set of incoming interfaces with properties and methods.</span></span> <span data-ttu-id="a8bb0-122">Il contenitore può fornire proprietà di ambiente aggiuntive e può supportare l'estensione delle proprietà del controllo tramite l'aggregazione.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-122">The container can supply additional ambient properties, and it can support extending the control's properties through aggregation.</span></span> <span data-ttu-id="a8bb0-123">Queste funzionalità restano in automazione OLE, pagine delle proprietà, oggetti collegabili e tecnologie di controllo ActiveX.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-123">These features rest on OLE automation, property pages, connectable objects, and ActiveX control technologies.</span></span>

</dd> <dt>

<span data-ttu-id="a8bb0-124"><span id="Events"></span><span id="events"></span><span id="EVENTS"></span>Eventi</span><span class="sxs-lookup"><span data-stu-id="a8bb0-124"><span id="Events"></span><span id="events"></span><span id="EVENTS"></span>Events</span></span>
</dt> <dd>

<span data-ttu-id="a8bb0-125">Oltre a fornire proprietà e metodi, un controllo ActiveX può anche fornire interfacce in uscita per notificare al client gli eventi.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-125">In addition to providing properties and methods, an ActiveX control can also provide outgoing interfaces to notify its client of events.</span></span> <span data-ttu-id="a8bb0-126">Il client deve supportare la gestione di questi eventi.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-126">The client must support handling of these events.</span></span> <span data-ttu-id="a8bb0-127">Queste funzionalità usano l'automazione OLE e gli oggetti collegabili.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-127">These features use OLE automation and connectable objects.</span></span>

</dd> <dt>

<span data-ttu-id="a8bb0-128"><span id="Visual_representation"></span><span id="visual_representation"></span><span id="VISUAL_REPRESENTATION"></span>Rappresentazione visiva</span><span class="sxs-lookup"><span data-stu-id="a8bb0-128"><span id="Visual_representation"></span><span id="visual_representation"></span><span id="VISUAL_REPRESENTATION"></span>Visual representation</span></span>
</dt> <dd>

<span data-ttu-id="a8bb0-129">Un controllo può supportare il posizionamento e la visualizzazione all'interno del relativo contenitore.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-129">A control can support positioning and displaying itself within its container.</span></span> <span data-ttu-id="a8bb0-130">Il contenitore posiziona il controllo e ne determina la dimensione.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-130">The container positions the control and determines its size.</span></span> <span data-ttu-id="a8bb0-131">Queste funzionalità utilizzano la tecnologia per documenti compositi, inclusa la tecnologia di trascinamento della selezione OLE.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-131">These features use compound document technology, including OLE drag and drop technology.</span></span>

</dd> <dt>

<span data-ttu-id="a8bb0-132"><span id="Keyboard_handling"></span><span id="keyboard_handling"></span><span id="KEYBOARD_HANDLING"></span>Gestione della tastiera</span><span class="sxs-lookup"><span data-stu-id="a8bb0-132"><span id="Keyboard_handling"></span><span id="keyboard_handling"></span><span id="KEYBOARD_HANDLING"></span>Keyboard handling</span></span>
</dt> <dd>

<span data-ttu-id="a8bb0-133">Un controllo può rispondere agli acceleratori della tastiera, in modo che l'utente finale possa avviare le azioni eseguite dal controllo.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-133">A control can respond to keyboard accelerators so the end-user can initiate actions performed by the control.</span></span> <span data-ttu-id="a8bb0-134">Il contenitore gestisce l'attività della tastiera per tutti i controlli incorporati.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-134">The container manages keyboard activity for all its embedded controls.</span></span> <span data-ttu-id="a8bb0-135">Queste funzionalità utilizzano le tecnologie di controllo e di documento composto.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-135">These features use control and compound document technologies.</span></span>

</dd> <dt>

<span data-ttu-id="a8bb0-136"><span id="Persistence"></span><span id="persistence"></span><span id="PERSISTENCE"></span>Persistenza</span><span class="sxs-lookup"><span data-stu-id="a8bb0-136"><span id="Persistence"></span><span id="persistence"></span><span id="PERSISTENCE"></span>Persistence</span></span>
</dt> <dd>

<span data-ttu-id="a8bb0-137">Un controllo può salvare il proprio stato.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-137">A control can save its state.</span></span> <span data-ttu-id="a8bb0-138">Il client gestisce la persistenza dei controlli incorporati.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-138">The client manages the persistence of its embedded controls.</span></span> <span data-ttu-id="a8bb0-139">Queste funzionalità utilizzano le tecnologie di archiviazione strutturata e di persistenza degli oggetti.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-139">These features use structured storage and object persistence technologies.</span></span>

</dd> <dt>

<span data-ttu-id="a8bb0-140"><span id="Registration_and_licensing"></span><span id="registration_and_licensing"></span><span id="REGISTRATION_AND_LICENSING"></span>Registrazione e licenze</span><span class="sxs-lookup"><span data-stu-id="a8bb0-140"><span id="Registration_and_licensing"></span><span id="registration_and_licensing"></span><span id="REGISTRATION_AND_LICENSING"></span>Registration and licensing</span></span>
</dt> <dd>

<span data-ttu-id="a8bb0-141">Un controllo in genere supporta la registrazione automatica e crea un set di voci del registro di sistema quando ne viene creata un'istanza.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-141">A control typically supports self-registration and creates a set of registry entries when it is instantiated.</span></span> <span data-ttu-id="a8bb0-142">Un controllo può anche essere concesso in licenza per impedire l'uso non autorizzato.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-142">A control can also be licensed to help prevent unauthorized use.</span></span>

</dd> </dl>

<span data-ttu-id="a8bb0-143">La maggior parte di queste funzionalità coinvolgono sia il controllo che il relativo contenitore client.</span><span class="sxs-lookup"><span data-stu-id="a8bb0-143">Most of these features involve both the control and its client container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8bb0-144">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a8bb0-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8bb0-145">Controlli ActiveX</span><span class="sxs-lookup"><span data-stu-id="a8bb0-145">ActiveX Controls</span></span>](activex-controls.md)
</dt> </dl>

 

 




