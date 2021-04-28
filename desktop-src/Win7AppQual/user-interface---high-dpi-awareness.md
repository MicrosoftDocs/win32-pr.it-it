---
description: Interfaccia utente - Compatibilità DPI avanzata
ms.assetid: 5b753340-366c-44b3-87e9-19c580f1c5d5
title: Interfaccia utente - Compatibilità DPI avanzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 118b566d35f753a77f6cfd9706c2e69819f3fbaa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116069"
---
# <a name="user-interface---high-dpi-awareness"></a><span data-ttu-id="22517-103">Interfaccia utente - Compatibilità DPI avanzata</span><span class="sxs-lookup"><span data-stu-id="22517-103">User Interface - High DPI Awareness</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="22517-104">Piattaforme interessate</span><span class="sxs-lookup"><span data-stu-id="22517-104">Affected Platforms</span></span>

 <span data-ttu-id="22517-105">**Client** - Windows XP \| Windows Vista Windows \| 7</span><span class="sxs-lookup"><span data-stu-id="22517-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="22517-106">Impatto sulle funzionalità</span><span class="sxs-lookup"><span data-stu-id="22517-106">Feature Impact</span></span>

<span data-ttu-id="22517-107">**Gravità** - Media</span><span class="sxs-lookup"><span data-stu-id="22517-107">**Severity** - Medium</span></span>  
<span data-ttu-id="22517-108">**Frequenza** - Media</span><span class="sxs-lookup"><span data-stu-id="22517-108">**Frequency** - Medium</span></span>  

## <a name="description"></a><span data-ttu-id="22517-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22517-109">Description</span></span>

<span data-ttu-id="22517-110">L'obiettivo è quello di invitare gli utenti finali a impostare la risoluzione nativa e usare DPI anziché la risoluzione dello schermo per modificare le dimensioni del testo e delle immagini visualizzate.</span><span class="sxs-lookup"><span data-stu-id="22517-110">The goal is to encourage end users to set their displays to native resolution and use DPI rather than screen resolution to change the size of displayed text and images.</span></span> <span data-ttu-id="22517-111">Windows 7 può rilevare e configurare automaticamente un valore DPI predefinito nelle installazioni pulite nei computer configurati dagli OEM usando le impostazioni DPI.</span><span class="sxs-lookup"><span data-stu-id="22517-111">Windows 7 can auto-detect and configure a default DPI on clean installs on machines configured by their OEMs using DPI settings.</span></span> <span data-ttu-id="22517-112">Sono disponibili strumenti che è possibile usare per progettare applicazioni con valori DPI elevati per garantire risultati più leggibili.</span><span class="sxs-lookup"><span data-stu-id="22517-112">There are tools you can use to help design applications that are high DPI aware in order to ensure the most readable results.</span></span>

<span data-ttu-id="22517-113">Sono state aggiunte due nuove funzionalità high DPI a Windows 7:</span><span class="sxs-lookup"><span data-stu-id="22517-113">We have added two new High DPI features to Windows 7:</span></span>

-   <span data-ttu-id="22517-114">Impostazione DPI per utente (in precedenza per computer)</span><span class="sxs-lookup"><span data-stu-id="22517-114">Per-user DPI setting (previously per machine)</span></span>
-   <span data-ttu-id="22517-115">Modificare il valore DPI senza riavviare (la disconnessione/accesso è ancora necessaria)</span><span class="sxs-lookup"><span data-stu-id="22517-115">Change DPI without rebooting (logoff/logon is still required)</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="22517-116">Manifestazione di impatto</span><span class="sxs-lookup"><span data-stu-id="22517-116">Manifestation of Impact</span></span>

<span data-ttu-id="22517-117">È probabile che le applicazioni che non gestiscono il caso DPI elevato presentino artefatti visivi, tra cui:</span><span class="sxs-lookup"><span data-stu-id="22517-117">Applications that do not handle the high DPI case are likely to exhibit visual artifacts, including:</span></span>

-   <span data-ttu-id="22517-118">Ritaglio dell'interfaccia utente o del testo da altri elementi dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="22517-118">Clipping of UI or text by other UI elements</span></span>
-   <span data-ttu-id="22517-119">Dimensioni dei caratteri incoerenti</span><span class="sxs-lookup"><span data-stu-id="22517-119">Inconsistent font sizes</span></span>
-   <span data-ttu-id="22517-120">Off-screen UIs</span><span class="sxs-lookup"><span data-stu-id="22517-120">Off-screen UIs</span></span>
-   <span data-ttu-id="22517-121">Sfocatura del testo o dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="22517-121">Blurring of text or UI</span></span>
-   <span data-ttu-id="22517-122">Trascinamento della selezione interrotto o altri input</span><span class="sxs-lookup"><span data-stu-id="22517-122">Broken drag-and-drop or other inputs</span></span>
-   <span data-ttu-id="22517-123">Rendering di applicazioni DX a schermo intero parzialmente fuori schermo</span><span class="sxs-lookup"><span data-stu-id="22517-123">Rendering of full-screen DX applications partially off screen</span></span>

## <a name="solution"></a><span data-ttu-id="22517-124">Soluzione</span><span class="sxs-lookup"><span data-stu-id="22517-124">Solution</span></span>

<span data-ttu-id="22517-125">Per rendere le applicazioni in grado di riconoscere DPI:</span><span class="sxs-lookup"><span data-stu-id="22517-125">To make your applications DPI-aware:</span></span>

1.  <span data-ttu-id="22517-126">Eseguire un test funzionale di alto livello, inclusa l'installazione e la disinstallazione nelle impostazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="22517-126">Do a high-level functional test pass, including install and uninstall at the following settings:</span></span>

    | <span data-ttu-id="22517-127">Impostazione</span><span class="sxs-lookup"><span data-stu-id="22517-127">Setting</span></span>                                              | <span data-ttu-id="22517-128">Elementi da cercare</span><span class="sxs-lookup"><span data-stu-id="22517-128">What to look for</span></span>                                                                                                                                                      |
    |------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="22517-129">1024x768 @ 120 DPI (ridimensionamento del 125%)</span><span class="sxs-lookup"><span data-stu-id="22517-129">1024x768 @ 120 DPI (125% scaling)</span></span>                    | <span data-ttu-id="22517-130">Si tratta di una risoluzione efficace di ~800x600, quindi cercare i problemi di interfaccia utente tagliati fuori dalla schermata o dal layout.</span><span class="sxs-lookup"><span data-stu-id="22517-130">This is an effective resolution of ~800x600, so look for UI clipped off the screen or layout issues.</span></span> <span data-ttu-id="22517-131">Cercare anche bitmap con pixilated & icone.</span><span class="sxs-lookup"><span data-stu-id="22517-131">Also look for pixilated bitmaps & icons.</span></span>                         |
    | <span data-ttu-id="22517-132">1600 x 1200 @144 DPI (ridimensionamento del 150%)</span><span class="sxs-lookup"><span data-stu-id="22517-132">1600x1200 @144 DPI (150% scaling)</span></span>                    | <span data-ttu-id="22517-133">Interfaccia utente sfocata.</span><span class="sxs-lookup"><span data-stu-id="22517-133">Blurry UI.</span></span> <span data-ttu-id="22517-134">Verificare che tutte le operazioni del mouse funzionino, in particolare trascinare & di rilascio.</span><span class="sxs-lookup"><span data-stu-id="22517-134">Verify that all mouse operations work, especially drag & drop operations.</span></span> <span data-ttu-id="22517-135">Verificare anche che le modalità schermo intero funzionino correttamente.</span><span class="sxs-lookup"><span data-stu-id="22517-135">Also verify full-screen modes work properly.</span></span>                                     |
    | <span data-ttu-id="22517-136">1600x1200 @ 144 DPI con Virtualizzazione DPI disabilitata</span><span class="sxs-lookup"><span data-stu-id="22517-136">1600x1200 @ 144 DPI with DPI Virtualization Disabled</span></span> | <span data-ttu-id="22517-137">Spesso i pulsanti e l'interfaccia utente non vengono ridimensionati in relazione al testo più grande & sarà presente un ritaglio di testo significativo.</span><span class="sxs-lookup"><span data-stu-id="22517-137">Often buttons and UI won't scale in relation to larger text & there will be significant text clipping.</span></span> <span data-ttu-id="22517-138">Cercare i problemi di layout in generale & bitmat con pixilated & icone.</span><span class="sxs-lookup"><span data-stu-id="22517-138">Look for layout issues in general & pixilated bitmats & icons.</span></span> |

    

     

2.  <span data-ttu-id="22517-139">Annota tutti i problemi rilevati, tra cui la posizione, la risoluzione dello schermo e le impostazioni DPI, nonché il comportamento dell'applicazione nelle altre configurazioni DPI/Risoluzione per la completezza</span><span class="sxs-lookup"><span data-stu-id="22517-139">Write down all the issues found, including location, screen resolution, and DPI settings, as well as how the application behaves in the other DPI/Resolution configurations for completeness</span></span>
3.  <span data-ttu-id="22517-140">Verificare ogni problema in base ai problemi comuni di codifica DPI</span><span class="sxs-lookup"><span data-stu-id="22517-140">Check each issue against the Common DPI Coding Issues</span></span>
4.  <span data-ttu-id="22517-141">Valutare il costo per rendere l'applicazione completamente consapevole di DPI</span><span class="sxs-lookup"><span data-stu-id="22517-141">Assess the cost of making the application fully DPI aware</span></span>
5.  <span data-ttu-id="22517-142">Creare un elenco degli asset High DPI necessari (ad esempio, pulsanti, icone)</span><span class="sxs-lookup"><span data-stu-id="22517-142">Make a list of the High DPI assets required (for example, buttons, icons)</span></span>
6.  <span data-ttu-id="22517-143">Eseguire e correggere l'elenco dei problemi DPI rilevati nel passaggio 1</span><span class="sxs-lookup"><span data-stu-id="22517-143">Work through and fix the list of DPI issues found in Step 1</span></span>
7.  <span data-ttu-id="22517-144">Integrare i nuovi asset del passaggio 5</span><span class="sxs-lookup"><span data-stu-id="22517-144">Integrate the new assets from Step 5</span></span>
8.  <span data-ttu-id="22517-145">Dichiarare l'applicazione che è in grado di riconoscere DPI</span><span class="sxs-lookup"><span data-stu-id="22517-145">Declare your application DPI Aware</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="22517-146">Test di compatibilità, prestazioni, affidabilità e usabilità</span><span class="sxs-lookup"><span data-stu-id="22517-146">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="22517-147">Eseguire nuovamente la valutazione del riconoscimento DPI e verificare che i problemi siano stati risolti.</span><span class="sxs-lookup"><span data-stu-id="22517-147">Re-run the DPI Awareness assessment and verify the issues are fixed.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="22517-148">Collegamenti ad altre risorse</span><span class="sxs-lookup"><span data-stu-id="22517-148">Links to Other Resources</span></span>

-   [<span data-ttu-id="22517-149">Sviluppo di applicazioni desktop con valori DPI alti in Windows</span><span class="sxs-lookup"><span data-stu-id="22517-149">High DPI Desktop Application Development on Windows</span></span>](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   <span data-ttu-id="22517-150">**Per domande tecniche, contattare:**<disup@microsoft.com></span><span class="sxs-lookup"><span data-stu-id="22517-150">**Contact for technical questions:** <disup@microsoft.com></span></span>

 

 
