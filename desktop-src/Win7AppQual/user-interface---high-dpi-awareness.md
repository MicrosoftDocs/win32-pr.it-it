---
description: .
ms.assetid: 5b753340-366c-44b3-87e9-19c580f1c5d5
title: Interfaccia utente - Compatibilità DPI avanzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e93aeed452f421e8e38df8d6d75f6bbe1f97cc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319828"
---
# <a name="user-interface---high-dpi-awareness"></a><span data-ttu-id="945fb-103">Interfaccia utente - Compatibilità DPI avanzata</span><span class="sxs-lookup"><span data-stu-id="945fb-103">User Interface - High DPI Awareness</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="945fb-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="945fb-104">Affected Platforms</span></span>

 <span data-ttu-id="945fb-105">**Client** -Windows XP Windows \| Vista Windows \| 7</span><span class="sxs-lookup"><span data-stu-id="945fb-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="945fb-106">Effetto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="945fb-106">Feature Impact</span></span>

<span data-ttu-id="945fb-107">**Gravità** -medio</span><span class="sxs-lookup"><span data-stu-id="945fb-107">**Severity** - Medium</span></span>  
<span data-ttu-id="945fb-108">**Frequenza** -media</span><span class="sxs-lookup"><span data-stu-id="945fb-108">**Frequency** - Medium</span></span>  

## <a name="description"></a><span data-ttu-id="945fb-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="945fb-109">Description</span></span>

<span data-ttu-id="945fb-110">L'obiettivo è incoraggiare gli utenti finali a impostare gli schermi sulla risoluzione nativa e utilizzare DPI anziché la risoluzione dello schermo per modificare le dimensioni del testo e delle immagini visualizzate.</span><span class="sxs-lookup"><span data-stu-id="945fb-110">The goal is to encourage end users to set their displays to native resolution and use DPI rather than screen resolution to change the size of displayed text and images.</span></span> <span data-ttu-id="945fb-111">Windows 7 consente di rilevare automaticamente e configurare un valore DPI predefinito in installazioni pulite nei computer configurati dagli OEM usando le impostazioni DPI.</span><span class="sxs-lookup"><span data-stu-id="945fb-111">Windows 7 can auto-detect and configure a default DPI on clean installs on machines configured by their OEMs using DPI settings.</span></span> <span data-ttu-id="945fb-112">Sono disponibili strumenti che consentono di progettare applicazioni con compatibilità DPI elevata, in modo da garantire i risultati più leggibili.</span><span class="sxs-lookup"><span data-stu-id="945fb-112">There are tools you can use to help design applications that are high DPI aware in order to ensure the most readable results.</span></span>

<span data-ttu-id="945fb-113">Sono state aggiunte due nuove funzionalità DPI elevate a Windows 7:</span><span class="sxs-lookup"><span data-stu-id="945fb-113">We have added two new High DPI features to Windows 7:</span></span>

-   <span data-ttu-id="945fb-114">Impostazione DPI per utente (in precedenza per computer)</span><span class="sxs-lookup"><span data-stu-id="945fb-114">Per-user DPI setting (previously per machine)</span></span>
-   <span data-ttu-id="945fb-115">Modificare il valore DPI senza riavviare (la disconnessione/accesso è ancora necessaria)</span><span class="sxs-lookup"><span data-stu-id="945fb-115">Change DPI without rebooting (logoff/logon is still required)</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="945fb-116">Manifesto di effetto</span><span class="sxs-lookup"><span data-stu-id="945fb-116">Manifestation of Impact</span></span>

<span data-ttu-id="945fb-117">Le applicazioni che non gestiscono il case con valori DPI alti possono presentare artefatti visivi, tra cui:</span><span class="sxs-lookup"><span data-stu-id="945fb-117">Applications that do not handle the high DPI case are likely to exhibit visual artifacts, including:</span></span>

-   <span data-ttu-id="945fb-118">Ritaglio dell'interfaccia utente o del testo da altri elementi dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="945fb-118">Clipping of UI or text by other UI elements</span></span>
-   <span data-ttu-id="945fb-119">Dimensioni del carattere incoerenti</span><span class="sxs-lookup"><span data-stu-id="945fb-119">Inconsistent font sizes</span></span>
-   <span data-ttu-id="945fb-120">Interfacce utente non schermate</span><span class="sxs-lookup"><span data-stu-id="945fb-120">Off-screen UIs</span></span>
-   <span data-ttu-id="945fb-121">Sfocatura di testo o interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="945fb-121">Blurring of text or UI</span></span>
-   <span data-ttu-id="945fb-122">Trascinamento della selezione o altri input interrotti</span><span class="sxs-lookup"><span data-stu-id="945fb-122">Broken drag-and-drop or other inputs</span></span>
-   <span data-ttu-id="945fb-123">Rendering delle applicazioni DX a schermo intero parzialmente fuori dallo schermo</span><span class="sxs-lookup"><span data-stu-id="945fb-123">Rendering of full-screen DX applications partially off screen</span></span>

## <a name="solution"></a><span data-ttu-id="945fb-124">Soluzione</span><span class="sxs-lookup"><span data-stu-id="945fb-124">Solution</span></span>

<span data-ttu-id="945fb-125">Per rendere le applicazioni compatibili con DPI:</span><span class="sxs-lookup"><span data-stu-id="945fb-125">To make your applications DPI-aware:</span></span>

1.  <span data-ttu-id="945fb-126">Eseguire un test funzionale di alto livello, incluso l'installazione e la disinstallazione, nelle impostazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="945fb-126">Do a high-level functional test pass, including install and uninstall at the following settings:</span></span>

    | <span data-ttu-id="945fb-127">Impostazione</span><span class="sxs-lookup"><span data-stu-id="945fb-127">Setting</span></span>                                              | <span data-ttu-id="945fb-128">Elementi da cercare</span><span class="sxs-lookup"><span data-stu-id="945fb-128">What to look for</span></span>                                                                                                                                                      |
    |------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="945fb-129">1024x768 @ 120 DPI (125% in scala)</span><span class="sxs-lookup"><span data-stu-id="945fb-129">1024x768 @ 120 DPI (125% scaling)</span></span>                    | <span data-ttu-id="945fb-130">Si tratta di una risoluzione efficace di ~ 800x600, quindi cercare l'interfaccia utente ritagliata in caso di problemi di layout o schermo.</span><span class="sxs-lookup"><span data-stu-id="945fb-130">This is an effective resolution of ~800x600, so look for UI clipped off the screen or layout issues.</span></span> <span data-ttu-id="945fb-131">Cercare anche le bitmap scatti & icone.</span><span class="sxs-lookup"><span data-stu-id="945fb-131">Also look for pixilated bitmaps & icons.</span></span>                         |
    | <span data-ttu-id="945fb-132">@144dpi 1600x1200 (150% in scala)</span><span class="sxs-lookup"><span data-stu-id="945fb-132">1600x1200 @144 DPI (150% scaling)</span></span>                    | <span data-ttu-id="945fb-133">Interfaccia utente sfocata.</span><span class="sxs-lookup"><span data-stu-id="945fb-133">Blurry UI.</span></span> <span data-ttu-id="945fb-134">Verificare che tutte le operazioni del mouse funzionino, in particolare trascinare & operazioni di rilascio.</span><span class="sxs-lookup"><span data-stu-id="945fb-134">Verify that all mouse operations work, especially drag & drop operations.</span></span> <span data-ttu-id="945fb-135">Verificare inoltre che le modalità a schermo intero funzionino correttamente.</span><span class="sxs-lookup"><span data-stu-id="945fb-135">Also verify full-screen modes work properly.</span></span>                                     |
    | <span data-ttu-id="945fb-136">1600x1200 @ 144 DPI con virtualizzazione DPI disabilitata</span><span class="sxs-lookup"><span data-stu-id="945fb-136">1600x1200 @ 144 DPI with DPI Virtualization Disabled</span></span> | <span data-ttu-id="945fb-137">Spesso i pulsanti e l'interfaccia utente non vengono ridimensionati in relazione a testo di dimensioni maggiori & il ritaglio del testo è significativo.</span><span class="sxs-lookup"><span data-stu-id="945fb-137">Often buttons and UI won't scale in relation to larger text & there will be significant text clipping.</span></span> <span data-ttu-id="945fb-138">Individuare i problemi di layout in generale & & icone di scatti bitmats.</span><span class="sxs-lookup"><span data-stu-id="945fb-138">Look for layout issues in general & pixilated bitmats & icons.</span></span> |

    

     

2.  <span data-ttu-id="945fb-139">Annotare tutti i problemi rilevati, inclusi il percorso, la risoluzione dello schermo e le impostazioni DPI, nonché il comportamento dell'applicazione nelle altre configurazioni DPI/di risoluzione per completezza</span><span class="sxs-lookup"><span data-stu-id="945fb-139">Write down all the issues found, including location, screen resolution, and DPI settings, as well as how the application behaves in the other DPI/Resolution configurations for completeness</span></span>
3.  <span data-ttu-id="945fb-140">Controllare ogni problema per i problemi di codifica DPI comuni</span><span class="sxs-lookup"><span data-stu-id="945fb-140">Check each issue against the Common DPI Coding Issues</span></span>
4.  <span data-ttu-id="945fb-141">Valutare il costo di rendere la compatibilità dell'applicazione con DPI</span><span class="sxs-lookup"><span data-stu-id="945fb-141">Assess the cost of making the application fully DPI aware</span></span>
5.  <span data-ttu-id="945fb-142">Creare un elenco di asset DPI alti richiesti (ad esempio, pulsanti, icone)</span><span class="sxs-lookup"><span data-stu-id="945fb-142">Make a list of the High DPI assets required (for example, buttons, icons)</span></span>
6.  <span data-ttu-id="945fb-143">Risolvere e correggere l'elenco dei problemi DPI trovati nel passaggio 1</span><span class="sxs-lookup"><span data-stu-id="945fb-143">Work through and fix the list of DPI issues found in Step 1</span></span>
7.  <span data-ttu-id="945fb-144">Integrare i nuovi asset dal passaggio 5</span><span class="sxs-lookup"><span data-stu-id="945fb-144">Integrate the new assets from Step 5</span></span>
8.  <span data-ttu-id="945fb-145">Dichiarare la compatibilità dell'applicazione con DPI</span><span class="sxs-lookup"><span data-stu-id="945fb-145">Declare your application DPI Aware</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="945fb-146">Compatibilità, prestazioni, affidabilità e test di usabilità</span><span class="sxs-lookup"><span data-stu-id="945fb-146">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="945fb-147">Eseguire di nuovo la valutazione della consapevolezza DPI e verificare che i problemi siano corretti.</span><span class="sxs-lookup"><span data-stu-id="945fb-147">Re-run the DPI Awareness assessment and verify the issues are fixed.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="945fb-148">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="945fb-148">Links to Other Resources</span></span>

-   [<span data-ttu-id="945fb-149">Sviluppo di applicazioni desktop con DPI elevato in Windows</span><span class="sxs-lookup"><span data-stu-id="945fb-149">High DPI Desktop Application Development on Windows</span></span>](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   <span data-ttu-id="945fb-150">**Contattare per domande tecniche:**<disup@microsoft.com></span><span class="sxs-lookup"><span data-stu-id="945fb-150">**Contact for technical questions:** <disup@microsoft.com></span></span>

 

 
