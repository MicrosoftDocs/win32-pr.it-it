---
title: Funzionalità di Rights Management digitali
description: Funzionalità di Rights Management digitali
ms.assetid: c3c1e59f-8ff9-496c-8e63-0c1cf4ce7092
keywords:
- Windows Media Format SDK, funzionalità DRM
- Digital Rights Management (DRM), funzionalità
- DRM (Digital Rights Management), funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd9c30b350fdf430d5b20bbe112c5309ac9da4f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728010"
---
# <a name="digital-rights-management-features"></a><span data-ttu-id="5f06f-106">Funzionalità di Rights Management digitali</span><span class="sxs-lookup"><span data-stu-id="5f06f-106">Digital Rights Management Features</span></span>

<span data-ttu-id="5f06f-107">\[La funzionalità DRM di Windows Media è deprecata e non deve essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="5f06f-107">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="5f06f-108">In alternativa, usare [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]</span><span class="sxs-lookup"><span data-stu-id="5f06f-108">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="5f06f-109">Digital Rights Management (DRM) è una tecnologia che i proprietari di contenuti possono usare per proteggere i file multimediali digitali mediante la relativa crittografia con una chiave, ovvero una porzione di dati che blocca e sblocca il contenuto.</span><span class="sxs-lookup"><span data-stu-id="5f06f-109">Digital rights management (DRM) is a technology that content owners can use to protect digital media files by encrypting them with a key (a piece of data that locks and unlocks the content).</span></span> <span data-ttu-id="5f06f-110">Per riprodurre un file ASF protetto, un consumer deve ottenere una licenza separata contenente la chiave.</span><span class="sxs-lookup"><span data-stu-id="5f06f-110">To play a protected ASF file, a consumer must obtain a separate license containing the key.</span></span> <span data-ttu-id="5f06f-111">Ogni licenza contiene inoltre i diritti, determinati dal proprietario del contenuto o dall'emittente della licenza, che specificano come il consumer può utilizzare il file.</span><span class="sxs-lookup"><span data-stu-id="5f06f-111">Each license also contains rights, determined by the content owner or license issuer, which specify how the consumer can use the file.</span></span> <span data-ttu-id="5f06f-112">Grazie alla tecnologia DRM, i proprietari dei contenuti possono fornire canzoni, video e altri file multimediali digitali tramite Internet in un formato di file protetto e controllare l'uso del contenuto digitale.</span><span class="sxs-lookup"><span data-stu-id="5f06f-112">Using DRM technology, content owners can deliver songs, videos, and other digital media files over the Internet in a protected file format and control the use of their digital content.</span></span> <span data-ttu-id="5f06f-113">La tecnologia Microsoft DRM è supportata anche da Windows Media Rights Manager, Windows Media Encoder e Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5f06f-113">Microsoft DRM technology is also supported by the Windows Media Rights Manager, the Windows Media Encoder, and Windows Media Player.</span></span> <span data-ttu-id="5f06f-114">Per ulteriori informazioni generali sulla tecnologia DRM di Microsoft, visitare il [sito Web Microsoft Windows Media](https://support.microsoft.com/help/17946/windows-media).</span><span class="sxs-lookup"><span data-stu-id="5f06f-114">For more background information on Microsoft's DRM technology, see the [Microsoft Windows Media Web site](https://support.microsoft.com/help/17946/windows-media).</span></span>

> [!Note]  
> <span data-ttu-id="5f06f-115">Il DRM non è supportato dalla versione basata su x64 di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="5f06f-115">DRM is not supported by the x64-based version of this SDK.</span></span>

 

<span data-ttu-id="5f06f-116">Le sezioni seguenti illustrano le principali funzionalità correlate a DRM di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="5f06f-116">The following sections discuss the main DRM-related features of the Windows Media Format SDK.</span></span>



| <span data-ttu-id="5f06f-117">Sezione</span><span class="sxs-lookup"><span data-stu-id="5f06f-117">Section</span></span>                                                                                            | <span data-ttu-id="5f06f-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f06f-118">Description</span></span>                                                                                                                          |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f06f-119">Nozioni fondamentali su DRM</span><span class="sxs-lookup"><span data-stu-id="5f06f-119">DRM Basics</span></span>](drm-basics.md)                                                                       | <span data-ttu-id="5f06f-120">Viene fornita una breve panoramica della funzionalità DRM fornita da Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="5f06f-120">Provides a brief overview of the DRM functionality provided by the Windows Media Format SDK.</span></span>                                         |
| [<span data-ttu-id="5f06f-121">Versioni DRM</span><span class="sxs-lookup"><span data-stu-id="5f06f-121">DRM Versions</span></span>](drm-versions.md)                                                                   | <span data-ttu-id="5f06f-122">Descrive le principali differenze tra le versioni di protezione DRM disponibili per le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="5f06f-122">Describes the main differences between the versions of DRM protection available to applications.</span></span>                                     |
| [<span data-ttu-id="5f06f-123">DRM Live</span><span class="sxs-lookup"><span data-stu-id="5f06f-123">Live DRM</span></span>](live-drm.md)                                                                           | <span data-ttu-id="5f06f-124">Vengono descritti gli scenari resi possibili dalla protezione DRM "al volo".</span><span class="sxs-lookup"><span data-stu-id="5f06f-124">Describes the scenarios made possible by "on the fly" DRM protection.</span></span>                                                                |
| [<span data-ttu-id="5f06f-125">Individualizzazione DRM</span><span class="sxs-lookup"><span data-stu-id="5f06f-125">DRM Individualization</span></span>](drm-individualization.md)                                                 | <span data-ttu-id="5f06f-126">Descrive l'aggiornamento della sicurezza dell'applicazione che può essere richiesto dai proprietari del contenuto DRM o dalle autorità emittenti di licenze.</span><span class="sxs-lookup"><span data-stu-id="5f06f-126">Describes the application security upgrade that DRM content owners or license issuers can require.</span></span>                                   |
| [<span data-ttu-id="5f06f-127">Backup e ripristino di licenze DRM</span><span class="sxs-lookup"><span data-stu-id="5f06f-127">Backing Up and Restoring of DRM Licenses</span></span>](backing-up-and-restoring-of-drm-licenses.md)           | <span data-ttu-id="5f06f-128">Vengono descritti i vantaggi e gli svantaggi di consentire agli utenti di eseguire il backup e il ripristino delle licenze di contenuti.</span><span class="sxs-lookup"><span data-stu-id="5f06f-128">Describes the pros and cons of permitting users to back up and restore their content licenses.</span></span>                                       |
| [<span data-ttu-id="5f06f-129">Visualizzazione degli attributi DRM nell'editor di metadati</span><span class="sxs-lookup"><span data-stu-id="5f06f-129">Viewing DRM Attributes in the Metadata Editor</span></span>](viewing-drm-attributes-in-the-metadata-editor.md) | <span data-ttu-id="5f06f-130">Descrive le funzionalità di questo oggetto helper DRM e gli scenari in cui è stato progettato per supportare.</span><span class="sxs-lookup"><span data-stu-id="5f06f-130">Describes the capabilities of this DRM helper object and the scenarios it was designed to support.</span></span>                                   |
| [<span data-ttu-id="5f06f-131">Livelli di protezione dell'output</span><span class="sxs-lookup"><span data-stu-id="5f06f-131">Output Protection Levels</span></span>](output-protection-levels.md)                                           | <span data-ttu-id="5f06f-132">Viene descritto in che modo i livelli di protezione dell'output rendono più flessibili le licenze DRM versione 10.</span><span class="sxs-lookup"><span data-stu-id="5f06f-132">Describes how Output Protection Levels make DRM version 10 licenses more flexible.</span></span>                                                   |
| [<span data-ttu-id="5f06f-133">Revoca delle licenze</span><span class="sxs-lookup"><span data-stu-id="5f06f-133">License Revocation</span></span>](license-revocation.md)                                                       | <span data-ttu-id="5f06f-134">Descrive la revoca delle licenze.</span><span class="sxs-lookup"><span data-stu-id="5f06f-134">Describes license revocation.</span></span>                                                                                                        |
| [<span data-ttu-id="5f06f-135">Windows Media DRM 10 per i dispositivi di rete</span><span class="sxs-lookup"><span data-stu-id="5f06f-135">Windows Media DRM 10 for Network Devices</span></span>](windows-media-drm-10-for-network-devices.md)           | <span data-ttu-id="5f06f-136">Introduce Windows Media DRM 10 per i dispositivi di rete e la relativa implementazione in questo SDK.</span><span class="sxs-lookup"><span data-stu-id="5f06f-136">Introduces Windows Media DRM 10 for Network Devices and its implementation in this SDK.</span></span>                                              |
| [<span data-ttu-id="5f06f-137">Percorso audio protetto Microsoft</span><span class="sxs-lookup"><span data-stu-id="5f06f-137">Microsoft Secure Audio Path</span></span>](microsoft-secure-audio-path--deprecated.md)                         | <span data-ttu-id="5f06f-138">Viene descritta l'architettura Microsoft Secure Audio Path, che fornisce il livello massimo di protezione per il contenuto audio protetto.</span><span class="sxs-lookup"><span data-stu-id="5f06f-138">Describes the Microsoft Secure Audio Path architecture, which provides the highest degree of protection for protected audio content.</span></span> |
| [<span data-ttu-id="5f06f-139">Masterizzazione playlist</span><span class="sxs-lookup"><span data-stu-id="5f06f-139">Playlist Burning</span></span>](playlist-burning.md)                                                           | <span data-ttu-id="5f06f-140">Descrive la funzionalità di masterizzazione della playlist di DRM e il modo in cui è supportata in Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="5f06f-140">Describes the playlist-burning feature of DRM and how it is supported in the Windows Media Format SDK.</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="5f06f-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5f06f-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f06f-142">**Abilitazione del supporto DRM**</span><span class="sxs-lookup"><span data-stu-id="5f06f-142">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> <dt>

[<span data-ttu-id="5f06f-143">**Funzionalità**</span><span class="sxs-lookup"><span data-stu-id="5f06f-143">**Features**</span></span>](features.md)
</dt> </dl>

 

 