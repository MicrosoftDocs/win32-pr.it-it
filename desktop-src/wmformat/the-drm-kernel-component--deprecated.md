---
title: Componente kernel DRM (deprecato)
description: Componente kernel DRM (deprecato)
ms.assetid: 016899fb-6d0a-4529-8649-5e8f29c89253
keywords:
- Windows Media Format SDK, Microsoft Secure Audio Path (SAP)
- Digital Rights Management (DRM), Microsoft Secure Audio Path (SAP)
- DRM (Digital Rights Management), Microsoft Secure Audio Path (SAP)
- Windows Media Format SDK, percorso audio sicuro (SAP)
- Digital Rights Management (DRM), percorso audio sicuro (SAP)
- DRM (Digital Rights Management), Secure Audio Path (SAP)
- Windows Media Format SDK, componente kernel DRM
- Digital Rights Management (DRM), componente kernel
- DRM (Digital Rights Management), componente kernel
- Microsoft Secure Audio Path (SAP), componente kernel DRM
- Secure Audio Path (SAP), componente kernel DRM
- SAP (Secure Audio Path), componente kernel DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacc0074fdf390ca478ed41b59188ad42ec193c1
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104047576"
---
# <a name="the-drm-kernel-component-deprecated"></a><span data-ttu-id="4a493-115">Componente kernel DRM (deprecato)</span><span class="sxs-lookup"><span data-stu-id="4a493-115">The DRM Kernel Component (deprecated)</span></span>

<span data-ttu-id="4a493-116">Questa pagina documenta una funzionalità che verrà supportata con una soluzione tecnica diversa nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="4a493-116">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="4a493-117">Nel modello Microsoft Secure Audio Path (SAP) il componente kernel DRM fornisce due funzionalità di base che proteggono l'integrità della musica crittografata.</span><span class="sxs-lookup"><span data-stu-id="4a493-117">In the Microsoft Secure Audio Path (SAP) model, the DRM kernel component provides two basic features that protect the integrity of encrypted music.</span></span>

<span data-ttu-id="4a493-118">In primo luogo, il componente client DRM e il componente kernel DRM sono in comunicazione quando viene riprodotto un file musicale.</span><span class="sxs-lookup"><span data-stu-id="4a493-118">First, the DRM client component and the DRM kernel component are in communication when a music file is played.</span></span> <span data-ttu-id="4a493-119">Questa comunicazione tra i componenti impedisce a chiunque di manomettere il segnale crittografato o di inserire informazioni false.</span><span class="sxs-lookup"><span data-stu-id="4a493-119">This communication between components prevents anyone from tampering with the encrypted signal or from inserting false information.</span></span>

<span data-ttu-id="4a493-120">In secondo luogo, il componente kernel DRM non decrittografa il segnale musicale finché non vengono autenticati tutti i componenti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="4a493-120">Second, the DRM kernel component does not decrypt the music signal until all remaining components are authenticated.</span></span> <span data-ttu-id="4a493-121">Ovvero, prima di decrittografare il contenuto e passarlo al componente di sistema successivo, il componente kernel DRM controlla ogni componente che rimane nel percorso alla scheda audio (ogni componente che può accedere al contenuto) e verifica che questi componenti siano firmati con un certificato di Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4a493-121">That is, before decrypting content and passing it to the next system component, the DRM kernel component checks each component that remains in the path to the sound card (each component that can access the content) and verifies that these components are signed with a certificate from Microsoft.</span></span> <span data-ttu-id="4a493-122">Un componente non firmato potrebbe indicare un componente sospetto o un driver dannoso.</span><span class="sxs-lookup"><span data-stu-id="4a493-122">An unsigned component might indicate a suspicious component or a malicious driver.</span></span> <span data-ttu-id="4a493-123">Pertanto, quando il componente kernel DRM convalida i componenti rimanenti, se il test ha esito negativo, il segnale viene interrotto e non può essere riprodotto.</span><span class="sxs-lookup"><span data-stu-id="4a493-123">So, when the DRM kernel component validates remaining components, if any component fails this test, the signal is halted and cannot be played.</span></span> <span data-ttu-id="4a493-124">In caso contrario, se tutti i componenti passano la convalida, il componente kernel DRM decrittografa la musica e la passa al componente successivo.</span><span class="sxs-lookup"><span data-stu-id="4a493-124">Otherwise, if all components pass validation, the DRM kernel component decrypts the music and passes it to the next component.</span></span>

<span data-ttu-id="4a493-125">Microsoft firma digitalmente i driver che passano i test Windows® Hardware Quality Lab (WHQL) per garantire agli utenti che utilizzano i driver di qualità più elevata.</span><span class="sxs-lookup"><span data-stu-id="4a493-125">Microsoft digitally signs drivers that pass the Windows® Hardware Quality Lab (WHQL) tests to assure users that they are using the highest-quality drivers.</span></span> <span data-ttu-id="4a493-126">Questa pratica è standard e garantisce l'autenticità dei componenti perché la firma non può essere falsificata, né può essere modificata senza eliminare definitivamente la firma.</span><span class="sxs-lookup"><span data-stu-id="4a493-126">This practice is standard and guarantees the authenticity of components because the signature cannot be forged, nor can the code be modified without destroying the signature.</span></span> <span data-ttu-id="4a493-127">I driver certificati per il percorso audio sicuro devono proteggere i dati audio che elaborano dall'accesso da parte di componenti non attendibili.</span><span class="sxs-lookup"><span data-stu-id="4a493-127">Drivers that are certified for Secure Audio Path must protect the audio data they process from access by untrusted components.</span></span> 

<span data-ttu-id="4a493-128">I driver inclusi in Windows Millennium Edition e Windows XP vengono aggiornati per il percorso audio protetto e firmati.</span><span class="sxs-lookup"><span data-stu-id="4a493-128">Drivers included with Windows Millennium Edition and Windows XP are updated for Secure Audio Path and signed.</span></span> <span data-ttu-id="4a493-129">I driver non firmati per l'utilizzo con Windows me o Windows XP non possono riprodurre musica protetta.</span><span class="sxs-lookup"><span data-stu-id="4a493-129">Drivers that are not signed for use with Windows Me or Windows XP cannot play protected music.</span></span> <span data-ttu-id="4a493-130">I produttori di driver possono riemettere le versioni aggiornate dei driver firmati da WHQL e pubblicarli in Internet per il download da parte degli utenti.</span><span class="sxs-lookup"><span data-stu-id="4a493-130">Driver manufacturers can reissue updated versions of their drivers that are signed by WHQL, and publish them on the Internet for consumers to download.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a493-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4a493-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a493-132">**Percorso audio protetto Microsoft**</span><span class="sxs-lookup"><span data-stu-id="4a493-132">**Microsoft Secure Audio Path**</span></span>](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




