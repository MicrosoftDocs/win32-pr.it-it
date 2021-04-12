---
title: Il modello di percorso audio sicuro (deprecato)
description: Il modello di percorso audio sicuro (deprecato)
ms.assetid: 8854411a-d917-497b-9c10-4c29bcb7832b
keywords:
- Windows Media Format SDK, Microsoft Secure Audio Path (SAP)
- Digital Rights Management (DRM), Microsoft Secure Audio Path (SAP)
- DRM (Digital Rights Management), Microsoft Secure Audio Path (SAP)
- Windows Media Format SDK, percorso audio sicuro (SAP)
- Digital Rights Management (DRM), percorso audio sicuro (SAP)
- DRM (Digital Rights Management), Secure Audio Path (SAP)
- Microsoft Secure Audio Path (SAP), modello
- Percorso audio sicuro (SAP), modello
- SAP (percorso audio sicuro), modello
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aee21d05113deb3c4e8d64141374c87da090f41c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395774"
---
# <a name="the-secure-audio-path-model-deprecated"></a><span data-ttu-id="d381c-112">Il modello di percorso audio sicuro (deprecato)</span><span class="sxs-lookup"><span data-stu-id="d381c-112">The Secure Audio Path Model (deprecated)</span></span>

<span data-ttu-id="d381c-113">Questa pagina documenta una funzionalità che verrà supportata con una soluzione tecnica diversa nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="d381c-113">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="d381c-114">Microsoft Secure Audio Path (SAP) è una funzionalità di Microsoft Windows® me e Microsoft Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d381c-114">Microsoft Secure Audio Path (SAP) is a feature of Microsoft Windows® Me and Microsoft Windows XP.</span></span> <span data-ttu-id="d381c-115">Il requisito per la riproduzione di un file audio solo tramite un percorso audio sicuro è specificato nella licenza DRM e viene applicato dai componenti client DRM.</span><span class="sxs-lookup"><span data-stu-id="d381c-115">The requirement that an audio file be played only through a secure audio path is specified in the DRM license and enforced by the DRM client components.</span></span> <span data-ttu-id="d381c-116">Non è stata aggiunta alcuna crittografia aggiuntiva per i file solo SAP quando sono inizialmente protetti.</span><span class="sxs-lookup"><span data-stu-id="d381c-116">There is no extra encryption added for SAP-only files when they are initially protected.</span></span> <span data-ttu-id="d381c-117">La crittografia SAP viene aggiunta automaticamente dai componenti DRM al momento della riproduzione, così come il processo di autenticazione per tutti i componenti software interessati dalla riproduzione.</span><span class="sxs-lookup"><span data-stu-id="d381c-117">The SAP encryption is added automatically by the DRM components at playback time, as is the authentication process for all software components involved in playback.</span></span> <span data-ttu-id="d381c-118">I lavori di SAP sono quindi completamente trasparenti per le applicazioni e questo è il motivo per cui non esiste alcun metodo o proprietà in Windows Media Format SDK per abilitare o disabilitare SAP.</span><span class="sxs-lookup"><span data-stu-id="d381c-118">The workings of SAP are therefore completely transparent to applications, and that is why there is no method or property in the Windows Media Format SDK for enabling or disabling SAP.</span></span> <span data-ttu-id="d381c-119">Se lo si desidera, quando si crea un file protetto un proprietario del contenuto può aggiungere un attributo di intestazione personalizzato denominato "DRMHeader. SAPRequired" per indicare a un server licenze di aggiungere il requisito SAP alla licenza.</span><span class="sxs-lookup"><span data-stu-id="d381c-119">If desired, when creating a protected file a content owner can add a custom header attribute called something like "DRMHeader.SAPRequired" in order to instruct a license server to add the SAP requirement to the license.</span></span> <span data-ttu-id="d381c-120">L'implementazione di tale schema è spetta al proprietario del contenuto e al servizio licenze.</span><span class="sxs-lookup"><span data-stu-id="d381c-120">The implementation of such a scheme is up to the content owner and the license service.</span></span>

<span data-ttu-id="d381c-121">Nel modello DRM corrente, se SAP non è applicato, quando viene riprodotta la musica digitale protetta, il contenuto crittografato passa al componente client DRM.</span><span class="sxs-lookup"><span data-stu-id="d381c-121">In the current DRM model, if SAP is not applied, when protected digital music is played, the encrypted content passes to the DRM client component.</span></span> <span data-ttu-id="d381c-122">Il client DRM verifica che l'applicazione e il componente DRM che incorporano Windows Media Format SDK siano validi.</span><span class="sxs-lookup"><span data-stu-id="d381c-122">The DRM client verifies that the application and the DRM component incorporating the Windows Media Format SDK are valid.</span></span> <span data-ttu-id="d381c-123">Se sono validi, il client DRM decrittografa il contenuto e lo invia all'applicazione, che quindi lo invia ai componenti audio di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="d381c-123">If they are valid, the DRM client decrypts the content and sends it to the application, which then sends it to the lower-level audio components.</span></span> <span data-ttu-id="d381c-124">A questo punto, la musica decrittografata è disponibile per le applicazioni in modalità utente e i plug-in e i driver in modalità kernel che possono intercettare i bit audio decrittografati.</span><span class="sxs-lookup"><span data-stu-id="d381c-124">At this point, the decrypted music is available to user mode applications and plug-ins and kernel mode drivers that can intercept the decrypted audio bits.</span></span>

<span data-ttu-id="d381c-125">Quando viene applicato il requisito del percorso audio protetto, il contenuto non viene decrittografato dall'applicazione, ma viene passato in uno stato crittografato ai componenti di livello inferiore, che sono stati autenticati da Microsoft come affidabili.</span><span class="sxs-lookup"><span data-stu-id="d381c-125">When the Secure Audio Path requirement is applied, the content is not decrypted by the application, but rather is passed in an encrypted state to lower level components, all of which have been authenticated by Microsoft as trustworthy.</span></span> <span data-ttu-id="d381c-126">Un componente audio attendibile è uno che non rende disponibile il contenuto audio per qualsiasi componente di sistema, ad eccezione di altri componenti attendibili specifici.</span><span class="sxs-lookup"><span data-stu-id="d381c-126">A trusted audio component is one that does not make the audio content available to any system component except other specific trusted components.</span></span> <span data-ttu-id="d381c-127">In questo modo, il contenuto digitale rimane protetto fino al livello del driver.</span><span class="sxs-lookup"><span data-stu-id="d381c-127">In this way, the digital content remains protected all the way down to the driver level.</span></span>

<span data-ttu-id="d381c-128">Il diagramma seguente mostra il modello corrente rispetto al modello di percorso audio protetto.</span><span class="sxs-lookup"><span data-stu-id="d381c-128">The following diagram displays the current model in comparison to the Secure Audio Path model.</span></span>

![diagramma del modello di percorso audio sicuro](images/sap.png)

 

 




