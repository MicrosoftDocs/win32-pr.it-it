---
title: Visualizzazione o modifica del segnale musicale (deprecato)
description: Visualizzazione o modifica del segnale musicale (deprecato)
ms.assetid: 47150951-2ab5-4cbe-ae57-4ebd23943f1d
keywords:
- Windows Media Format SDK, Microsoft Secure Audio Path (SAP)
- Digital Rights Management (DRM), Microsoft Secure Audio Path (SAP)
- DRM (Digital Rights Management), Microsoft Secure Audio Path (SAP)
- Windows Media Format SDK, percorso audio sicuro (SAP)
- Digital Rights Management (DRM), percorso audio sicuro (SAP)
- DRM (Digital Rights Management), Secure Audio Path (SAP)
- Windows Media Format SDK, visualizzazione o modifica di segnali musicali
- Digital Rights Management (DRM), visualizzazione o modifica di segnali musicali
- DRM (Digital Rights Management), visualizzazione o modifica di segnali musicali
- Microsoft Secure Audio Path (SAP), Music Signal Viewing o Modifying
- Percorso audio sicuro (SAP), visualizzazione o modifica di segnali musicali
- SAP (percorso audio sicuro), visualizzazione o modifica di segnali musicali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 673038c9769301d2820cd73e4a090b5e4770fc4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298823"
---
# <a name="viewing-or-modifying-the-music-signal-deprecated"></a><span data-ttu-id="b46b6-115">Visualizzazione o modifica del segnale musicale (deprecato)</span><span class="sxs-lookup"><span data-stu-id="b46b6-115">Viewing or Modifying the Music Signal (deprecated)</span></span>

<span data-ttu-id="b46b6-116">Questa pagina documenta una funzionalità che verrà supportata con una soluzione tecnica diversa nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="b46b6-116">This page documents a feature that will be supported with a different technical solution in future versions of Windows.</span></span>

<span data-ttu-id="b46b6-117">Nel modello Microsoft Secure Audio Path (SAP), le applicazioni non possono modificare la musica protetta in alcun modo.</span><span class="sxs-lookup"><span data-stu-id="b46b6-117">In the Microsoft Secure Audio Path (SAP) model, applications cannot modify protected music in any way.</span></span> <span data-ttu-id="b46b6-118">Ad esempio, quando un'applicazione tenta di intercettare un segnale musicale, il segnale suona come un rumore casuale.</span><span class="sxs-lookup"><span data-stu-id="b46b6-118">For example, when an application attempts to intercept a music signal, the signal sounds like random noise.</span></span> <span data-ttu-id="b46b6-119">Di conseguenza, le applicazioni che in genere modificano i segnali, ad esempio un equalizzatore, non possono modificare il suono della musica.</span><span class="sxs-lookup"><span data-stu-id="b46b6-119">As a result, applications that normally modify signals (such as an equalizer) cannot change the sound of the music.</span></span>

<span data-ttu-id="b46b6-120">Alcune applicazioni visualizzano semplicemente un segnale musicale.</span><span class="sxs-lookup"><span data-stu-id="b46b6-120">Some applications merely view a music signal.</span></span> <span data-ttu-id="b46b6-121">Alcune applicazioni, ad esempio, visualizzano le spie lampeggianti nel tempo con il segnale musicale, ma non la modifica.</span><span class="sxs-lookup"><span data-stu-id="b46b6-121">For example, some applications display flashing lights in time with the music signal, but do not modify it.</span></span> <span data-ttu-id="b46b6-122">Per supportare le applicazioni che visualizzano i segnali, una piccola parte della musica viene decrittografata e passata in formato chiaro con il contenuto crittografato.</span><span class="sxs-lookup"><span data-stu-id="b46b6-122">To accommodate applications that view signals, a small part of the music is decrypted and passed in clear form with the encrypted content.</span></span> <span data-ttu-id="b46b6-123">Il segnale risultante è molto scarso (peggio la qualità del telefono) ma può essere sufficiente per le applicazioni che visualizzano i segnali.</span><span class="sxs-lookup"><span data-stu-id="b46b6-123">The resulting signal is very poor (worse than telephone quality) but can suffice for applications that view signals.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b46b6-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b46b6-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b46b6-125">**Percorso audio protetto Microsoft**</span><span class="sxs-lookup"><span data-stu-id="b46b6-125">**Microsoft Secure Audio Path**</span></span>](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




