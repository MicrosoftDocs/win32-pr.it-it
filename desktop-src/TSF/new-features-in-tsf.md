---
title: Nuove funzionalità in TSF
description: Con il rilascio di Microsoft WindowsXP Service Pack1, il Framework di servizi di testo (TSF) dispone di numerose nuove funzionalità.
ms.assetid: d69fec9a-9304-45af-806a-dcc476c95759
keywords:
- Framework servizi di testo (TSF), nuove funzionalità
- TSF (Text Services Framework), nuove funzionalità
- Servizi di testo, nuove funzionalità
- Applicazioni abilitate per TSF, nuove funzionalità
- Framework servizi di testo (TSF), supporto avanzato
- TSF (Text Services Framework), supporto avanzato
- Servizi di testo, supporto avanzato
- Applicazioni abilitate per TSF, supporto avanzato
- Framework servizi di testo (TSF), Rich Edit
- TSF (Text Services Framework), Rich Edit
- Servizi di testo, Rich Edit
- Applicazioni abilitate per TSF, Rich Edit
- Modifica avanzata
- Framework servizi di testo (TSF), sicurezza
- TSF (Framework di servizi di testo), sicurezza
- Servizi di testo, sicurezza
- Applicazioni abilitate per TSF, sicurezza
- sicurezza per TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7a345087304be638be93fa352845cdd468bf15
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399117"
---
# <a name="new-features-in-tsf"></a><span data-ttu-id="1e308-121">Nuove funzionalità in TSF</span><span class="sxs-lookup"><span data-stu-id="1e308-121">New Features in TSF</span></span>

<span data-ttu-id="1e308-122">Con il rilascio di Microsoft WindowsXP Service Pack1, il Framework di servizi di testo (TSF) dispone di numerose nuove funzionalità.</span><span class="sxs-lookup"><span data-stu-id="1e308-122">With the release of Microsoft WindowsXP Service Pack1, Text Services Framework (TSF) has several new features.</span></span>

## <a name="extended-support-of-advanced-text-services"></a><span data-ttu-id="1e308-123">Supporto esteso dei servizi di testo avanzati</span><span class="sxs-lookup"><span data-stu-id="1e308-123">Extended Support of Advanced Text Services</span></span>

<span data-ttu-id="1e308-124">È stato aggiunto il supporto a TSF e Windows per fornire un'interfaccia utente coerente per tutte le applicazioni sul desktop.</span><span class="sxs-lookup"><span data-stu-id="1e308-124">Support has been added to TSF and Windows to provide a consistent user interface for all applications across the desktop.</span></span> <span data-ttu-id="1e308-125">Questo nuovo supporto Abilita le applicazioni o i controlli legacy che non sono a conoscenza di TSF per sfruttare gratuitamente alcuni servizi di testo avanzati.</span><span class="sxs-lookup"><span data-stu-id="1e308-125">This new support enables legacy applications or controls that are not aware of TSF to take advantage of some advanced text services for free.</span></span> <span data-ttu-id="1e308-126">Ad esempio, è ora possibile usare la dettatura vocale e la grafia per immettere il testo in un documento in qualsiasi applicazione.</span><span class="sxs-lookup"><span data-stu-id="1e308-126">For example, speech dictation and handwriting can now be used to enter text into a document in any application.</span></span>

<span data-ttu-id="1e308-127">Questa nuova funzionalità è disponibile solo per il servizio WindowsXP Pack1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="1e308-127">This new feature is available only for WindowsXP Service Pack1 or later.</span></span> <span data-ttu-id="1e308-128">È disattivata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="1e308-128">It is turned off by default.</span></span> <span data-ttu-id="1e308-129">Per abilitarla, fare clic sulla casella di controllo nella scheda nuovo **Avanzate** della parte **servizi di testo e lingue di input** del pannello di controllo **Opzioni internazionali e della lingua** .</span><span class="sxs-lookup"><span data-stu-id="1e308-129">To enable it, click the check box in the new **Advanced** tab in the **Text Services and Input Languages** portion of the **Regional and Language Options** control panel.</span></span>

![supporto delle applicazioni non compatibili nel pannello di controllo TSF](images/advanced-text-services.gif)

## <a name="rich-edit-support"></a><span data-ttu-id="1e308-131">Supporto Rich Edit</span><span class="sxs-lookup"><span data-stu-id="1e308-131">Rich Edit Support</span></span>

<span data-ttu-id="1e308-132">[Microsoft® Rich Edit](../controls/rich-edit-controls.md) La versione 4,1, usata dalle applicazioni per visualizzare e modificare il testo con una formattazione speciale per caratteri e paragrafi, ora espone la funzionalità TSF.</span><span class="sxs-lookup"><span data-stu-id="1e308-132">[Microsoft® Rich Edit](../controls/rich-edit-controls.md) Version 4.1, used by applications to view and edit text with special character and paragraph formatting, now exposes TSF functionality.</span></span> <span data-ttu-id="1e308-133">Per impostazione predefinita, questo supporto è disattivato.</span><span class="sxs-lookup"><span data-stu-id="1e308-133">By default this support is turned off.</span></span> <span data-ttu-id="1e308-134">Per abilitare TSF in Rich Edit, un'applicazione host invia un messaggio di finestra speciale al controllo Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="1e308-134">To enable TSF in Rich Edit, a hosting application sends a special window message to the Rich Edit control.</span></span>

## <a name="security-improvements"></a><span data-ttu-id="1e308-135">Miglioramenti alla sicurezza</span><span class="sxs-lookup"><span data-stu-id="1e308-135">Security Improvements</span></span>

<span data-ttu-id="1e308-136">La sicurezza e l'affidabilità di TSF sono state notevolmente migliorate, per ridurre la probabilità che un programma ostile possa accedere allo stack, all'heap o ad altre posizioni di memoria sicure.</span><span class="sxs-lookup"><span data-stu-id="1e308-136">The security and robustness of TSF have been substantially improved, to reduce the likelihood of a hostile program being able to access the stack, heap, or other secure memory locations.</span></span> <span data-ttu-id="1e308-137">È stata migliorata anche la sicurezza delle applicazioni di esempio Software Development Kit (SDK) e dei servizi di testo.</span><span class="sxs-lookup"><span data-stu-id="1e308-137">The security of software development kit (SDK) sample applications and text services has also been improved.</span></span>

 

 