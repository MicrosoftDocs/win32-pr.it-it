---
title: Progettazione Server-Side
description: Le funzioni lato server comunicano con la creazione guidata client tramite l'oggetto Windows. External. Lo script lato server fornisce queste funzioni per rispondere agli eventi della procedura guidata e per recuperare informazioni sulla procedura guidata.
ms.assetid: 7cc8b814-f230-4326-a9df-a491ed35483e
keywords:
- pubblicazione guidata, progettazione lato server
- finestra. External, pubblicazione guidata
- procedure guidate di pubblicazione, finestra. esterno
- procedure guidate di pubblicazione, funzioni script di spostamento
- script, pubblicazione guidata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20b3b218bbca297be446016335d90fe717a88bba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963089"
---
# <a name="server-side-design"></a><span data-ttu-id="e7171-109">Progettazione Server-Side</span><span class="sxs-lookup"><span data-stu-id="e7171-109">Server-Side Design</span></span>

<span data-ttu-id="e7171-110">Le funzioni lato server comunicano con la creazione guidata client tramite l'oggetto **Windows. External** .</span><span class="sxs-lookup"><span data-stu-id="e7171-110">Server-side functions communicate with the client wizard through the **windows.external** object.</span></span> <span data-ttu-id="e7171-111">Lo script lato server fornisce queste funzioni per rispondere agli eventi della procedura guidata e per recuperare informazioni sulla procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="e7171-111">Server-side script provides these functions to respond to wizard events and to retrieve information about the wizard.</span></span>

<span data-ttu-id="e7171-112">In questo documento sono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="e7171-112">The following topics are covered in this document.</span></span>

-   [<span data-ttu-id="e7171-113">Implementazione di funzioni script di spostamento</span><span class="sxs-lookup"><span data-stu-id="e7171-113">Implementing Navigation Script Functions</span></span>](#implementing-navigation-script-functions)
    -   [<span data-ttu-id="e7171-114">Onback ()</span><span class="sxs-lookup"><span data-stu-id="e7171-114">OnBack()</span></span>](#onback)
    -   [<span data-ttu-id="e7171-115">OnNext ()</span><span class="sxs-lookup"><span data-stu-id="e7171-115">OnNext()</span></span>](#onnext)
    -   [<span data-ttu-id="e7171-116">OnCancel ()</span><span class="sxs-lookup"><span data-stu-id="e7171-116">OnCancel()</span></span>](#oncancel)
-   [<span data-ttu-id="e7171-117">Altri metodi e proprietà</span><span class="sxs-lookup"><span data-stu-id="e7171-117">Other Methods and Properties</span></span>](#other-methods-and-properties)
    -   [<span data-ttu-id="e7171-118">Metodi</span><span class="sxs-lookup"><span data-stu-id="e7171-118">Methods</span></span>](#methods)
    -   [<span data-ttu-id="e7171-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e7171-119">Properties</span></span>](#properties)
-   [<span data-ttu-id="e7171-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e7171-120">Related topics</span></span>](#related-topics)

## <a name="implementing-navigation-script-functions"></a><span data-ttu-id="e7171-121">Implementazione di funzioni script di spostamento</span><span class="sxs-lookup"><span data-stu-id="e7171-121">Implementing Navigation Script Functions</span></span>

<span data-ttu-id="e7171-122">Script sul lato server in ogni pagina HTML risponde ai pulsanti di spostamento tramite le funzioni per **onback**, **OnNext** e **OnCancel**.</span><span class="sxs-lookup"><span data-stu-id="e7171-122">Server-side script in each HTML page responds to navigation buttons through functions for **OnBack**, **OnNext**, and **OnCancel**.</span></span> <span data-ttu-id="e7171-123">Queste funzioni devono essere accessibili tramite **\_ lo script IHTMLDocument:: Get** nel client e non accettano parametri.</span><span class="sxs-lookup"><span data-stu-id="e7171-123">These functions must be accessible through **IHTMLDocument::get\_Script** on the client and take no parameters.</span></span>

### <a name="onback"></a><span data-ttu-id="e7171-124">Onback ()</span><span class="sxs-lookup"><span data-stu-id="e7171-124">OnBack()</span></span>

-   <span data-ttu-id="e7171-125">Risponde quando l'utente fa clic **nuovamente** nella procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="e7171-125">Responds when the user clicks **Back** in the wizard.</span></span>
-   <span data-ttu-id="e7171-126">Se la pagina del lato server corrente è la prima pagina sul lato server, chiamare **Window. External. FinalBack** per indicare al client di passare alla pagina del lato client precedente.</span><span class="sxs-lookup"><span data-stu-id="e7171-126">If the current server-side page is the first server-side page, call **window.external.FinalBack** to instruct the client to navigate to the previous client-side page.</span></span>
-   <span data-ttu-id="e7171-127">Se la pagina del lato server corrente non è la prima pagina sul lato server, passare alla pagina precedente sul lato server.</span><span class="sxs-lookup"><span data-stu-id="e7171-127">If the current server-side page is not the first server-side page, navigate to the previous server-side page.</span></span>
-   <span data-ttu-id="e7171-128">Questa funzione deve essere implementata per ogni pagina.</span><span class="sxs-lookup"><span data-stu-id="e7171-128">This function must be implemented for each page.</span></span> <span data-ttu-id="e7171-129">Le pagine che non riescono a eseguire questa operazione vengono considerate non valide e visualizzano una pagina di errore.</span><span class="sxs-lookup"><span data-stu-id="e7171-129">Any page that fails to do so is considered invalid and displays an error page.</span></span>

### <a name="onnext"></a><span data-ttu-id="e7171-130">OnNext ()</span><span class="sxs-lookup"><span data-stu-id="e7171-130">OnNext()</span></span>

-   <span data-ttu-id="e7171-131">Risponde quando l'utente fa clic su **Avanti** nella procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="e7171-131">Responds when the user clicks **Next** in the wizard.</span></span>
-   <span data-ttu-id="e7171-132">Se la pagina del lato server corrente è l'ultima pagina sul lato server, chiamare **Window. External. FinalNext** per indicare al client di passare alla pagina successiva sul lato client o completare la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="e7171-132">If the current server-side page is the last server-side page, call **window.external.FinalNext** to instruct the client to navigate to the next client-side page or to complete the wizard.</span></span>
-   <span data-ttu-id="e7171-133">Se la pagina del lato server corrente non è l'ultima pagina sul lato server, passare alla pagina successiva sul lato server.</span><span class="sxs-lookup"><span data-stu-id="e7171-133">If the current server-side page is not the last server-side page, navigate to the next server-side page.</span></span>

### <a name="oncancel"></a><span data-ttu-id="e7171-134">OnCancel ()</span><span class="sxs-lookup"><span data-stu-id="e7171-134">OnCancel()</span></span>

-   <span data-ttu-id="e7171-135">Risponde quando l'utente fa clic su **Annulla** nella procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="e7171-135">Responds when the user clicks **Cancel** in the wizard.</span></span>
-   <span data-ttu-id="e7171-136">L'interfaccia utente deve essere progettata in modo che l'utente possa essere annullata in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="e7171-136">The UI should be designed so the user can cancel at any time.</span></span>
-   <span data-ttu-id="e7171-137">Una volta elaborate le elaborazioni nella funzione **OnCancel** , il client chiude la procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="e7171-137">Once any processing in the **OnCancel** function is processed, the client closes the wizard.</span></span>

## <a name="other-methods-and-properties"></a><span data-ttu-id="e7171-138">Altri metodi e proprietà</span><span class="sxs-lookup"><span data-stu-id="e7171-138">Other Methods and Properties</span></span>

<span data-ttu-id="e7171-139">È possibile accedere alle funzioni implementate dal client tramite **Windows. External**, così come sono proprietà.</span><span class="sxs-lookup"><span data-stu-id="e7171-139">Client-implemented functions are accessed through **windows.external**, as are properties.</span></span> <span data-ttu-id="e7171-140">I servizi disponibili sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e7171-140">Available services are as follows:</span></span>

### <a name="methods"></a><span data-ttu-id="e7171-141">Metodi</span><span class="sxs-lookup"><span data-stu-id="e7171-141">Methods</span></span>

-   [<span data-ttu-id="e7171-142">**SetHeaderText**</span><span class="sxs-lookup"><span data-stu-id="e7171-142">**SetHeaderText**</span></span>](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [<span data-ttu-id="e7171-143">**SetWizardButtons**</span><span class="sxs-lookup"><span data-stu-id="e7171-143">**SetWizardButtons**</span></span>](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [<span data-ttu-id="e7171-144">**PassportAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="e7171-144">**PassportAuthenticate**</span></span>](/windows/desktop/shell/inewwdevents-passportauthenticate)

### <a name="properties"></a><span data-ttu-id="e7171-145">Proprietà</span><span class="sxs-lookup"><span data-stu-id="e7171-145">Properties</span></span>

-   <span data-ttu-id="e7171-146">[**Didascalia**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e7171-146">[**Caption**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))</span></span>
-   [<span data-ttu-id="e7171-147">**Proprietà**</span><span class="sxs-lookup"><span data-stu-id="e7171-147">**Property**</span></span>](/windows/desktop/shell/iwebwizardhost-property)

<span data-ttu-id="e7171-148">Nell'esempio di codice riportato di seguito viene illustrato il codice sul lato server per una semplice pagina della procedura guidata che implementa la pagina di errore del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="e7171-148">The following code sample shows server-side code for a simple wizard page which implements the web service's error page.</span></span>


```
<html>
    <head>
        <script language="JavaScript">
            function window.onload()
            {
                window.external.SetWizardButtons(1, 0, 0);    
                <!-- Back button enabled -->
            }

            function window.onback()
            {
                window.external.FinalBack();
            }
        </script>
    </head>
.
.
.
</html>
                    
```



## <a name="related-topics"></a><span data-ttu-id="e7171-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e7171-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7171-150">Progettazione lato client</span><span class="sxs-lookup"><span data-stu-id="e7171-150">Client-Side Design</span></span>](pubwiz-client.md)
</dt> <dt>

[<span data-ttu-id="e7171-151">Registrazione di un servizio</span><span class="sxs-lookup"><span data-stu-id="e7171-151">Registering a Service</span></span>](pubwiz-reg.md)
</dt> </dl>

 

 