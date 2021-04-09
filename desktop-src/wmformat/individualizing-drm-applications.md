---
title: Applicazioni DRM individualizzazione
description: Applicazioni DRM individualizzazione
ms.assetid: 8d87c663-bc54-4928-9eee-d09c358e61f8
keywords:
- Windows Media Format SDK, applicazioni DRM individualizzazione
- Windows Media Format SDK, applicazione individualizzazione
- ASF (Advanced Systems Format), applicazioni DRM individualizzazione
- ASF (Advanced Systems Format), individualizzazione DRM Applications
- ASF (Advanced Systems Format), individualizzazione dell'applicazione
- ASF (Advanced Systems Format), individualizzazione applicazione
- Digital Rights Management (DRM), applicazioni individualizzazione
- DRM (Digital Rights Management), applicazioni individualizzazione
- Digital Rights Management (DRM), applicazione individualizzazione
- DRM (Digital Rights Management), individualizzazione dell'applicazione
- individualizzazione applicazione
- applicazioni DRM individualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c3fc0166332c52e39fc0882238fa9009aa0cc1
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "103956258"
---
# <a name="individualizing-drm-applications"></a><span data-ttu-id="c879b-115">Applicazioni DRM individualizzazione</span><span class="sxs-lookup"><span data-stu-id="c879b-115">Individualizing DRM Applications</span></span>

<span data-ttu-id="c879b-116">Per aumentare la sicurezza, il componente DRM delle applicazioni può essere *personalizzato*.</span><span class="sxs-lookup"><span data-stu-id="c879b-116">To increase security, the DRM component of applications can be *individualized*.</span></span> <span data-ttu-id="c879b-117">Un'applicazione personalizzata è una che ha ricevuto un aggiornamento ai componenti DRM che lo differenzia da tutte le altre copie della stessa applicazione.</span><span class="sxs-lookup"><span data-stu-id="c879b-117">An individualized application is one that has received an upgrade to its DRM components that differentiates it from all other copies of the same application.</span></span> <span data-ttu-id="c879b-118">I proprietari del contenuto possono richiedere che i file protetti vengano riprodotti solo in un'applicazione che è stata individualmente.</span><span class="sxs-lookup"><span data-stu-id="c879b-118">Content owners can require that their protected files be played only on an application that has been individualized.</span></span>

<span data-ttu-id="c879b-119">Il processo di individualizzazione viene avviato quando l'applicazione contatta il servizio di individualizzazione Microsoft, che quindi installa un aggiornamento della sicurezza nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c879b-119">The individualization process starts when the application contacts the Microsoft Individualization Service, which then installs a security upgrade on the user's computer.</span></span> <span data-ttu-id="c879b-120">Poiché il servizio di individualizzazione gestisce le informazioni dell'utente, è necessario visualizzare l'informativa sulla privacy di Microsoft o fornire un collegamento a tale pagina nel sito Web Microsoft: <https://privacy.microsoft.com/privacystatement> .</span><span class="sxs-lookup"><span data-stu-id="c879b-120">Because the Individualization Service handles information from the user, you must display the Microsoft privacy policy or provide a link to that page at the Microsoft Web site: <https://privacy.microsoft.com/privacystatement>.</span></span>

<span data-ttu-id="c879b-121">L'individualizzazione può essere eseguita in modi diversi.</span><span class="sxs-lookup"><span data-stu-id="c879b-121">Individualization can be accomplished in different ways.</span></span> <span data-ttu-id="c879b-122">Ad esempio, l'individualizzazione può essere eseguita quando un utente riproduce un file protetto.</span><span class="sxs-lookup"><span data-stu-id="c879b-122">For example, individualization can take place when a user plays a protected file.</span></span> <span data-ttu-id="c879b-123">La richiesta di licenza viene inviata al [*servizio Windows Media License*](wmformat-glossary.md), che controlla il certificato dell'applicazione che richiede la [*licenza*](wmformat-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="c879b-123">The license request is sent to the [*Windows Media License Service*](wmformat-glossary.md), which inspects the certificate of the application requesting the [*license*](wmformat-glossary.md).</span></span> <span data-ttu-id="c879b-124">Se il componente DRM dell'applicazione non è stato individualizzato, il servizio licenze Windows Media rifiuta di emettere la licenza, perché si tratta dei criteri del servizio licenze Windows Media per emettere licenze solo per i giocatori individuali.</span><span class="sxs-lookup"><span data-stu-id="c879b-124">If the DRM component of the application has not been individualized, Windows Media License Service refuses to issue the license, because it is the policy of Windows Media License Service to issue licenses only to individualized players.</span></span> <span data-ttu-id="c879b-125">L'applicazione può quindi notificare all'utente che l'applicazione deve essere aggiornata.</span><span class="sxs-lookup"><span data-stu-id="c879b-125">The application can then notify the user that the application must be upgraded.</span></span> <span data-ttu-id="c879b-126">Se l'utente acconsente, viene fornito un aggiornamento della sicurezza per individuare il componente DRM dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c879b-126">If the user agrees, a security upgrade is provided to individualize the DRM component of the application.</span></span>

<span data-ttu-id="c879b-127">Per migliorare l'esperienza utente, è possibile avviare il processo di individualizzazione come passaggio di aggiornamento della sicurezza durante l'installazione. l'utente non viene quindi interrotto per ottenere un aggiornamento della sicurezza durante il tentativo di riprodurre un file protetto.</span><span class="sxs-lookup"><span data-stu-id="c879b-127">For a better user experience, you can initiate the individualization process as a security upgrade step during setup; then the user is not interrupted to get a security upgrade while trying to play a protected file.</span></span> <span data-ttu-id="c879b-128">È anche possibile incoraggiare attivamente l'individualizzazione aggiungendo un comando o un pulsante di menu di **aggiornamento della sicurezza** all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c879b-128">You can also actively encourage individualization by adding a **Security Upgrade** menu command or button to the application.</span></span>

> [!Note]  
> <span data-ttu-id="c879b-129">Il DRM non è supportato dalla versione basata su x64 di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="c879b-129">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c879b-130">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c879b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c879b-131">**Funzionalità di Rights Management digitali**</span><span class="sxs-lookup"><span data-stu-id="c879b-131">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="c879b-132">**Abilitazione del supporto DRM**</span><span class="sxs-lookup"><span data-stu-id="c879b-132">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




