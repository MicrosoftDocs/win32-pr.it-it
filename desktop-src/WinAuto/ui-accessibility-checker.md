---
title: Strumenti di accessibilità-AccChecker (controllo di accessibilità dell'interfaccia utente)
description: Descrive AccChecker (controllo dell'accessibilità dell'interfaccia utente), uno strumento per testare l'automazione interfaccia utente di un'applicazione o l'implementazione di Microsoft Active Accessibility (MSAA).
ms.assetid: 92155984-356A-4774-A99D-35B15A3BB704
keywords:
- Strumento di verifica dell'accessibilità dell'interfaccia utente
- AccChecker
- Implementazione di automazione interfaccia utente, test
- Implementazione di UIA, test
- Implementazione di Microsoft Active Accessibility, test
- Implementazione di MSAA, test
- test di automazione interfaccia utente
- test di UIA
- test di Microsoft Active Accessibility
- test di MSAA
- Strumenti di test di UIA
- Strumenti di test di automazione interfaccia utente
- Strumenti di test MSAA
- Strumenti di test di Microsoft Active Accessibility
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d2b85436735bfa08f8fc73cf4e465b11d71630
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "106299467"
---
# <a name="accessibility-tools---accchecker-ui-accessibility-checker"></a><span data-ttu-id="45fe7-117">Strumenti di accessibilità-AccChecker (controllo di accessibilità dell'interfaccia utente)</span><span class="sxs-lookup"><span data-stu-id="45fe7-117">Accessibility tools - AccChecker (UI Accessibility Checker)</span></span>

<span data-ttu-id="45fe7-118">**AccChecker** (UI Accessibility Checker) verifica che i requisiti di accessibilità dell'interfaccia utente chiave siano soddisfatti nella progettazione e nell'implementazione di automazione interfaccia utente (UIA) o Microsoft Active ACCESSIBILITY (MSAA) indipendentemente dal framework dell'interfaccia utente sottostante.</span><span class="sxs-lookup"><span data-stu-id="45fe7-118">**AccChecker** (UI Accessibility Checker) verifies that key UI accessibility requirements are met in the design and implementation of UI Automation (UIA) or Microsoft Active Accessibility (MSAA) regardless of the underlying UI framework.</span></span> <span data-ttu-id="45fe7-119">**AccChecker** include anche un set di verifiche di accessibilità Web.</span><span class="sxs-lookup"><span data-stu-id="45fe7-119">**AccChecker** also includes a set of web accessibility verifications.</span></span>

<span data-ttu-id="45fe7-120">**AccChecker** offre i seguenti livelli di funzionalità:</span><span class="sxs-lookup"><span data-stu-id="45fe7-120">**AccChecker** provides the following levels of functionality:</span></span>

- <span data-ttu-id="45fe7-121">Applicazione GUI Windows che supporta il test manuale, la registrazione di messaggi e la generazione dell'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="45fe7-121">A Windows GUI application that supports manual testing, message logging, and suppression generation.</span></span>
- <span data-ttu-id="45fe7-122">API da usare nei framework di test automatizzati.</span><span class="sxs-lookup"><span data-stu-id="45fe7-122">An API for use in automated testing frameworks.</span></span>
- <span data-ttu-id="45fe7-123">Applicazione console che supporta le automazioni di test non gestite per gli scenari in cui non è possibile usare l'API gestita **AccChecker** .</span><span class="sxs-lookup"><span data-stu-id="45fe7-123">A console application that supports unmanaged test automations for scenarios where the **AccChecker** managed API can't be used.</span></span>

<span data-ttu-id="45fe7-124">Tutti i livelli di funzionalità di **AccChecker** forniscono routine per la verifica dell'accesso a livello di codice di Microsoft Active Accessibility, della generazione di eventi a livello di codice, del layout di controllo e della navigazione</span><span class="sxs-lookup"><span data-stu-id="45fe7-124">All levels of **AccChecker** functionality provide routines for verifying Microsoft Active Accessibility programmatic access, programmatic event generation, control layout, and keyboard navigation.</span></span> <span data-ttu-id="45fe7-125">**AccChecker** fornisce anche un servizio di trascrizione di base per la lettura dello schermo.</span><span class="sxs-lookup"><span data-stu-id="45fe7-125">**AccChecker** also provides a basic screen reader transcription service.</span></span>

<span data-ttu-id="45fe7-126">**AccChecker** viene installato con Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="45fe7-126">**AccChecker** is installed with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="45fe7-127">Si trova nella \\ cartella bin \\ < *versione* > \\ <  > \\ della piattaforma AccChecker del percorso di installazione di SDK.</span><span class="sxs-lookup"><span data-stu-id="45fe7-127">It is located in the \\bin\\<*version*>\\<*platform*>\\AccChecker folder of the SDK installation path.</span></span>

> [!NOTE]
> <span data-ttu-id="45fe7-128">**AccChecker** è uno strumento legacy.</span><span class="sxs-lookup"><span data-stu-id="45fe7-128">**AccChecker** is a legacy tool.</span></span> <span data-ttu-id="45fe7-129">È invece consigliabile usare [informazioni dettagliate sull'accessibilità](https://accessibilityinsights.io/) .</span><span class="sxs-lookup"><span data-stu-id="45fe7-129">We recommend using [Accessibility Insights](https://accessibilityinsights.io/) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="45fe7-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="45fe7-130">Requirements</span></span>

<span data-ttu-id="45fe7-131">Richiede .NET Framework 2,0 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="45fe7-131">Requires .NET Framework 2.0 or later.</span></span>

<span data-ttu-id="45fe7-132">**AccChecker** può essere usato per esaminare i dati di accessibilità nei sistemi che non dispongono di automazione interfaccia utente Microsoft, ma è possibile esaminare solo le proprietà di Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="45fe7-132">**AccChecker** can be used to examine accessibility data on systems that don't have Microsoft UI Automation, but can only examine the Microsoft Active Accessibility properties.</span></span> <span data-ttu-id="45fe7-133">Per esaminare l'automazione dell'interfaccia utente, è necessario che l'automazione interfaccia utente sia presente nel sistema.</span><span class="sxs-lookup"><span data-stu-id="45fe7-133">To examine UI Automation, UI Automation must be present on the system.</span></span> <span data-ttu-id="45fe7-134">Per ulteriori informazioni, vedere la sezione "requisiti" di [automazione interfaccia utente](entry-uiauto-win32.md).</span><span class="sxs-lookup"><span data-stu-id="45fe7-134">For more information, see the "Requirements" section of [UI Automation](entry-uiauto-win32.md).</span></span>

<span data-ttu-id="45fe7-135">**AccChecker** viene installato come parte del set di strumenti completo in Windows SDK, ma non viene distribuito come download di exe separato.</span><span class="sxs-lookup"><span data-stu-id="45fe7-135">**AccChecker** is installed as part of the overall set of tools in theWindows SDK, it is not distributed as a separate exe download.</span></span> <span data-ttu-id="45fe7-136">Il Windows SDK include tutti gli strumenti correlati all'accessibilità descritti in questa sezione.</span><span class="sxs-lookup"><span data-stu-id="45fe7-136">The Windows SDK includes all of the accessibility-related tools documented in this section.</span></span> [<span data-ttu-id="45fe7-137">Ottenere il Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="45fe7-137">Get the Windows SDK.</span></span>](https://developer.microsoft.com/) <span data-ttu-id="45fe7-138">È anche disponibile un archivio di download dell'SDK collegato da tale pagina, se è necessaria una versione precedente.</span><span class="sxs-lookup"><span data-stu-id="45fe7-138">(There's also an SDK download archive linked from that page, if you need a previous version.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="45fe7-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="45fe7-139">Related topics</span></span>

- [<span data-ttu-id="45fe7-140">Accessible Event Watcher</span><span class="sxs-lookup"><span data-stu-id="45fe7-140">Accessible Event Watcher</span></span>](accessible-event-watcher.md)
- [<span data-ttu-id="45fe7-141">Controllare</span><span class="sxs-lookup"><span data-stu-id="45fe7-141">Inspect</span></span>](inspect-objects.md)
- [<span data-ttu-id="45fe7-142">Strumenti di test</span><span class="sxs-lookup"><span data-stu-id="45fe7-142">Testing Tools</span></span>](testing-tools.md)
- [<span data-ttu-id="45fe7-143">Verifica dell'automazione dell'interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="45fe7-143">UI Automation Verify</span></span>](ui-automation-verify.md)
