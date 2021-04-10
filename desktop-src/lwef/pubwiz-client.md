---
title: Progettazione Client-Side
description: Lo script nelle pagine HTML sul lato server comunica con il client della procedura guidata per l'ordine di stampa online in cui è ospitato. Questa comunicazione viene eseguita tramite i metodi e le proprietà a cui accede l'oggetto Window. External.
ms.assetid: fa76ccee-0b94-41b5-8cc8-eb7e1818dbed
keywords:
- pubblicazione guidata, progettazione lato client
- finestra. External, pubblicazione guidata
- procedure guidate di pubblicazione, finestra. esterno
- procedure guidate di pubblicazione, considerazioni sulla progettazione
- procedure guidate di pubblicazione, ordinamento guidato stampa online
- Ordinamento guidato stampa online, progettazione lato client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f794ee5f576077e0523f9a21101205ec789d4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963059"
---
# <a name="client-side-design"></a><span data-ttu-id="41c9c-110">Progettazione Client-Side</span><span class="sxs-lookup"><span data-stu-id="41c9c-110">Client-Side Design</span></span>

<span data-ttu-id="41c9c-111">Lo script nelle pagine HTML sul lato server comunica con il client della procedura guidata per l'ordine di stampa online in cui è ospitato.</span><span class="sxs-lookup"><span data-stu-id="41c9c-111">Script in server-side HTML pages communicates with the Online Print Ordering Wizard client in which it is hosted.</span></span> <span data-ttu-id="41c9c-112">Questa comunicazione viene eseguita tramite i metodi e le proprietà a cui accede l'oggetto **Window. External** .</span><span class="sxs-lookup"><span data-stu-id="41c9c-112">This communication is accomplished through methods and properties accessed by the **window.external** object.</span></span>

<span data-ttu-id="41c9c-113">In questo documento sono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="41c9c-113">The following topics are covered in this document.</span></span>

-   [<span data-ttu-id="41c9c-114">Metodi e proprietà</span><span class="sxs-lookup"><span data-stu-id="41c9c-114">Methods and Properties</span></span>](#methods-and-properties)
-   [<span data-ttu-id="41c9c-115">Considerazioni sulla progettazione</span><span class="sxs-lookup"><span data-stu-id="41c9c-115">Design Considerations</span></span>](#design-considerations)
-   [<span data-ttu-id="41c9c-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="41c9c-116">Related topics</span></span>](#related-topics)

## <a name="methods-and-properties"></a><span data-ttu-id="41c9c-117">Metodi e proprietà</span><span class="sxs-lookup"><span data-stu-id="41c9c-117">Methods and Properties</span></span>

<span data-ttu-id="41c9c-118">I metodi e le proprietà seguenti sono disponibili tramite l'oggetto **Window. External** .</span><span class="sxs-lookup"><span data-stu-id="41c9c-118">The following methods and properties are available through the **window.external** object.</span></span>

-   [<span data-ttu-id="41c9c-119">**FinalBack**</span><span class="sxs-lookup"><span data-stu-id="41c9c-119">**FinalBack**</span></span>](/windows/desktop/shell/iwebwizardhost-finalback)
-   [<span data-ttu-id="41c9c-120">**FinalNext**</span><span class="sxs-lookup"><span data-stu-id="41c9c-120">**FinalNext**</span></span>](/windows/desktop/shell/iwebwizardhost-finalnext)
-   [<span data-ttu-id="41c9c-121">**Annulla**</span><span class="sxs-lookup"><span data-stu-id="41c9c-121">**Cancel**</span></span>](/windows/desktop/shell/iwebwizardhost-cancel)
-   [<span data-ttu-id="41c9c-122">**PassportAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="41c9c-122">**PassportAuthenticate**</span></span>](/windows/desktop/shell/inewwdevents-passportauthenticate)
-   [<span data-ttu-id="41c9c-123">**SetHeaderText**</span><span class="sxs-lookup"><span data-stu-id="41c9c-123">**SetHeaderText**</span></span>](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [<span data-ttu-id="41c9c-124">**SetWizardButtons**</span><span class="sxs-lookup"><span data-stu-id="41c9c-124">**SetWizardButtons**</span></span>](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   <span data-ttu-id="41c9c-125">[**Didascalia**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="41c9c-125">[**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span></span>
-   [<span data-ttu-id="41c9c-126">**Proprietà**</span><span class="sxs-lookup"><span data-stu-id="41c9c-126">**Property**</span></span>](/windows/desktop/shell/iwebwizardhost-property)

<span data-ttu-id="41c9c-127">Lo script della pagina lato server chiama questi metodi per notificare al client gli eventi durante la procedura di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="41c9c-127">The server-side page's script calls these methods to notify the client of events during the publishing procedure.</span></span> <span data-ttu-id="41c9c-128">Si osservi ora [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback) come esempio.</span><span class="sxs-lookup"><span data-stu-id="41c9c-128">Let's look at [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback) as an example.</span></span> <span data-ttu-id="41c9c-129">Quando viene visualizzata la prima pagina HTML sul lato server, la procedura guidata include le informazioni sugli handle per le pagine della procedura guidata precedenti e successive alle pagine HTML ospitate.</span><span class="sxs-lookup"><span data-stu-id="41c9c-129">When the wizard displays the first server-side HTML page, it does so armed with knowledge of the handles for the wizard pages preceding and following the hosted HTML pages.</span></span> <span data-ttu-id="41c9c-130">A questo punto dell'esempio, l'utente, seduto alla prima pagina HTML, fa clic sul pulsante **indietro** .</span><span class="sxs-lookup"><span data-stu-id="41c9c-130">At this point in our example, the user, sitting at that first HTML page, clicks the **Back** button.</span></span> <span data-ttu-id="41c9c-131">La procedura guidata invia una notifica di questo evento al server.</span><span class="sxs-lookup"><span data-stu-id="41c9c-131">The wizard sends a notification of this event to the server.</span></span> <span data-ttu-id="41c9c-132">Alla ricezione di questo messaggio, lo script sul lato server fa riferimento al relativo gestore **onback** per questo evento, che, poiché questa è la prima pagina HTML, chiama il metodo **FinalBack** .</span><span class="sxs-lookup"><span data-stu-id="41c9c-132">On receipt of this message, the server-side script refers to its **OnBack** handler for this event, which, as this is the first HTML page, calls the **FinalBack** method.</span></span> <span data-ttu-id="41c9c-133">In questo modo verrà visualizzata la pagina della procedura guidata prima di accedere all'interfaccia utente sul lato server.</span><span class="sxs-lookup"><span data-stu-id="41c9c-133">This causes the wizard to navigate to the wizard page displayed before entering the server-side UI.</span></span>

<span data-ttu-id="41c9c-134">Per una descrizione completa di questi metodi e proprietà, vedere la documentazione relativa agli oggetti [**WebWizardHost**](/windows/desktop/shell/webwizardhost) e [**NewWDEvents**](/windows/desktop/shell/newwdevents) .</span><span class="sxs-lookup"><span data-stu-id="41c9c-134">For a complete discussion of these methods and properties, see the documentation for the [**WebWizardHost**](/windows/desktop/shell/webwizardhost) and [**NewWDEvents**](/windows/desktop/shell/newwdevents) objects.</span></span>

## <a name="design-considerations"></a><span data-ttu-id="41c9c-135">Considerazioni sulla progettazione</span><span class="sxs-lookup"><span data-stu-id="41c9c-135">Design Considerations</span></span>

<span data-ttu-id="41c9c-136">Il codice HTML che crea ogni pagina sul lato server viene visualizzato normalmente nel riquadro della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="41c9c-136">HTML making up each server-side page is displayed normally in the wizard pane.</span></span> <span data-ttu-id="41c9c-137">Quando si progettano queste pagine, tenere presente che non è possibile ridimensionare una finestra della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="41c9c-137">When designing these pages, bear in mind that a wizard window cannot be resized.</span></span> <span data-ttu-id="41c9c-138">Le pagine devono pertanto essere costruite e dimensionate in modo che le barre di scorrimento vengano evitate quando possibile per fornire all'utente una navigazione uniforme nella procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="41c9c-138">Pages should therefore be constructed and sized so that scroll bars are avoided whenever possible to provide the user with smooth navigation through the wizard.</span></span>

<span data-ttu-id="41c9c-139">Ogni pagina HTML deve anche fornire un gestore per gli eventi **onback**, **OnNext** e **OnCancel** .</span><span class="sxs-lookup"><span data-stu-id="41c9c-139">Each HTML page must also provide a handler for **OnBack**, **OnNext**, and **OnCancel** events.</span></span> <span data-ttu-id="41c9c-140">Il gestore **OnNext** gestirà anche l'evento **Finish** .</span><span class="sxs-lookup"><span data-stu-id="41c9c-140">The **OnNext** handler will also handle the **Finish** event.</span></span> <span data-ttu-id="41c9c-141">Una pagina che non implementa una funzione **onback** viene considerata non valida e comporterà la visualizzazione di una pagina di errore.</span><span class="sxs-lookup"><span data-stu-id="41c9c-141">A page that does not implement an **OnBack** function is considered invalid and will cause an error page to be displayed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41c9c-142">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="41c9c-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41c9c-143">**WebWizardHost**</span><span class="sxs-lookup"><span data-stu-id="41c9c-143">**WebWizardHost**</span></span>](/windows/desktop/shell/webwizardhost)
</dt> <dt>

[<span data-ttu-id="41c9c-144">**NewWDEvents**</span><span class="sxs-lookup"><span data-stu-id="41c9c-144">**NewWDEvents**</span></span>](/windows/desktop/shell/newwdevents)
</dt> <dt>

[<span data-ttu-id="41c9c-145">Progettazione lato server</span><span class="sxs-lookup"><span data-stu-id="41c9c-145">Server-Side Design</span></span>](pubwiz-server.md)
</dt> </dl>

 

 