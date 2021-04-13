---
title: Nozioni fondamentali su DRM
description: Nozioni fondamentali su DRM
ms.assetid: f36da29d-5f9d-441d-8061-eb50331a8e7a
keywords:
- Windows Media Format SDK, nozioni fondamentali su DRM
- Digital Rights Management (DRM), informazioni
- DRM (Digital Rights Management), informazioni
- Digital Rights Management (DRM), protezione del contenuto
- DRM (Digital Rights Management), protezione del contenuto
- Digital Rights Management (DRM), creazione di pacchetti di contenuto
- DRM (Digital Rights Management), contenuto del pacchetto
- Digital Rights Management (DRM), lettura di contenuto protetto
- DRM (Digital Rights Management), lettura di contenuto protetto
- protezione del contenuto
- creazione di pacchetti di contenuto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c210fceb69174147dcb36a3e97b5591c2654a566
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396854"
---
# <a name="drm-basics"></a><span data-ttu-id="f8af6-114">Nozioni fondamentali su DRM</span><span class="sxs-lookup"><span data-stu-id="f8af6-114">DRM Basics</span></span>

<span data-ttu-id="f8af6-115">Le tecnologie DRM di Windows Media sono piuttosto semplici dal punto di vista di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="f8af6-115">The Windows Media DRM technologies are fairly simple from the perspective of the Windows Media Format SDK.</span></span> <span data-ttu-id="f8af6-116">I componenti dell'SDK possono essere usati per proteggere il contenuto e per riprodurre contenuti protetti.</span><span class="sxs-lookup"><span data-stu-id="f8af6-116">Components of the SDK can be used to protect content and to play protected content.</span></span>

## <a name="protecting-content"></a><span data-ttu-id="f8af6-117">Protezione del contenuto</span><span class="sxs-lookup"><span data-stu-id="f8af6-117">Protecting Content</span></span>

<span data-ttu-id="f8af6-118">La protezione del contenuto (detto anche contenuto del packaging) implica la crittografia della sezione di dati del file e include alcune informazioni nell'intestazione del file che consente ai giocatori di decrittografare il contenuto.</span><span class="sxs-lookup"><span data-stu-id="f8af6-118">Protecting content (also called packaging content) involves encrypting the data section of the file and including some information in the file header that enables players to decrypt the content.</span></span>

<span data-ttu-id="f8af6-119">Per crittografare il contenuto, è necessaria una chiave, ovvero un valore utilizzato per il seeding degli algoritmi di crittografia.</span><span class="sxs-lookup"><span data-stu-id="f8af6-119">To encrypt the content, you need a key, which is a value used to seed the encryption algorithms.</span></span> <span data-ttu-id="f8af6-120">Una chiave è costituita da due parti: un valore di inizializzazione chiave (o chiave privata) e un identificatore di chiave (o chiave pubblica).</span><span class="sxs-lookup"><span data-stu-id="f8af6-120">A key is made up of two pieces: a key seed (or private key), and a key identifier (or public key).</span></span> <span data-ttu-id="f8af6-121">Il valore di inizializzazione chiave è il valore Secret con cui si codifica il contenuto.</span><span class="sxs-lookup"><span data-stu-id="f8af6-121">The key seed is the secret value with which you encode content.</span></span> <span data-ttu-id="f8af6-122">L'identificatore di chiave è un valore pubblico incluso nell'intestazione di un file protetto.</span><span class="sxs-lookup"><span data-stu-id="f8af6-122">The key identifier is a public value that is included in the header of a protected file.</span></span>

<span data-ttu-id="f8af6-123">Quando un file è protetto, non può essere decrittografato senza una licenza.</span><span class="sxs-lookup"><span data-stu-id="f8af6-123">When a file is protected, it cannot be decrypted without a license.</span></span> <span data-ttu-id="f8af6-124">Una licenza include informazioni che specificano le condizioni per l'utilizzo del contenuto protetto.</span><span class="sxs-lookup"><span data-stu-id="f8af6-124">A license includes information that specifies the terms of use for the protected content.</span></span> <span data-ttu-id="f8af6-125">Le condizioni di licenza vengono stabilite dal proprietario del contenuto e possono essere personalizzate per soddisfare diverse esigenze.</span><span class="sxs-lookup"><span data-stu-id="f8af6-125">The terms of a license are decided by the content owner and can be customized to meet a variety of needs.</span></span> <span data-ttu-id="f8af6-126">Parte del processo di creazione del pacchetto di un file consiste nell'includere l'URL di una pagina Web in cui gli utenti possono acquisire una licenza per accedere al contenuto.</span><span class="sxs-lookup"><span data-stu-id="f8af6-126">Part of the process of packaging a file is to include the URL of a Web page where users can acquire a license to access the content.</span></span>

## <a name="reading-protected-content"></a><span data-ttu-id="f8af6-127">Lettura del contenuto protetto</span><span class="sxs-lookup"><span data-stu-id="f8af6-127">Reading Protected Content</span></span>

<span data-ttu-id="f8af6-128">Per leggere il contenuto protetto, una licenza per il contenuto deve risiedere nel computer client.</span><span class="sxs-lookup"><span data-stu-id="f8af6-128">To read protected content, a license for the content must reside on the client computer.</span></span> <span data-ttu-id="f8af6-129">Alcune restrizioni di licenza vengono controllate internamente dai componenti DRM di Windows Media Format SDK, mentre altre devono essere applicate dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="f8af6-129">Some license restrictions are checked internally by the DRM components of the Windows Media Format SDK, while others must be enforced by your application.</span></span>

<span data-ttu-id="f8af6-130">È possibile utilizzare gli oggetti di Windows Media Format SDK per consentire all'utente di acquisire licenze per il contenuto e di eseguire altre attività amministrative, ad esempio l'aggiornamento dei componenti DRM e il backup delle licenze.</span><span class="sxs-lookup"><span data-stu-id="f8af6-130">You can use the objects of the Windows Media Format SDK to assist the user in acquiring licenses for content and to perform other administrative tasks, such as updating DRM components and backing up licenses.</span></span>

> [!Note]  
> <span data-ttu-id="f8af6-131">Il DRM non è supportato dalla versione basata su x64 di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="f8af6-131">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f8af6-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f8af6-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8af6-133">**Funzionalità di Rights Management digitali**</span><span class="sxs-lookup"><span data-stu-id="f8af6-133">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="f8af6-134">**Abilitazione del supporto DRM**</span><span class="sxs-lookup"><span data-stu-id="f8af6-134">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




