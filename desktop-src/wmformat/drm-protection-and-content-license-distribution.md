---
title: Protezione DRM e distribuzione delle licenze di contenuti
description: Protezione DRM e distribuzione delle licenze di contenuti
ms.assetid: 147fef8c-7298-450d-a1a9-345c03c49bec
keywords:
- Windows Media Format SDK, protezione del contenuto DRM
- Windows Media Format SDK, licenze DRM
- ASF (Advanced Systems Format), protezione del contenuto DRM
- ASF (Advanced Systems Format), protezione del contenuto DRM
- ASF (Advanced Systems Format), distribuzione di licenze DRM
- ASF (Advanced Systems Format), distribuzione di licenze DRM
- Digital Rights Management (DRM), protezione del contenuto
- DRM (Digital Rights Management), protezione del contenuto
- Digital Rights Management (DRM), distribuzione di licenze
- DRM (Digital Rights Management), distribuzione di licenze
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25af13947828885d70f3e0fd9fe8bf035eb8c5e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332564"
---
# <a name="drm-protection-and-content-license-distribution"></a><span data-ttu-id="2a1eb-113">Protezione DRM e distribuzione delle licenze di contenuti</span><span class="sxs-lookup"><span data-stu-id="2a1eb-113">DRM Protection and Content License Distribution</span></span>

<span data-ttu-id="2a1eb-114">Sul lato della creazione, Digital Rights Management tecnologia implica due processi principali: (1) proteggere il contenuto e (2) fornire le licenze per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="2a1eb-114">On the creation side, digital rights management technology involves two main processes: (1) protecting the content and (2) providing licenses for the content.</span></span> <span data-ttu-id="2a1eb-115">La protezione di un file comporta essenzialmente la crittografia del contenuto e l'inclusione di un URL nell'intestazione del file che specifica dove è possibile ottenere una licenza per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="2a1eb-115">Protecting a file basically involves encrypting the content, and including a URL in the file header that specifies where a license for the content may be obtained.</span></span> <span data-ttu-id="2a1eb-116">Per proteggere i file con e quindi distribuire i file in altri computer o dispositivi, è possibile usare Windows Media Format SDK o Windows Media Rights Manager SDK per proteggere il file.</span><span class="sxs-lookup"><span data-stu-id="2a1eb-116">If you want to protect files with and then distribute the files to other computers or devices, you can use either the Windows Media Format SDK or the Windows Media Rights Manager SDK to protect the file.</span></span> <span data-ttu-id="2a1eb-117">Per gli scenari di DRM Live, è necessario usare Windows Media Format SDK per proteggere il contenuto mentre viene codificato.</span><span class="sxs-lookup"><span data-stu-id="2a1eb-117">For live-DRM scenarios, you must use the Windows Media Format SDK to protect the content as it is being encoded.</span></span>

<span data-ttu-id="2a1eb-118">Per creare ed emettere licenze per il contenuto protetto, è possibile creare una soluzione personalizzata usando gli oggetti di Windows Media Rights Manager SDK oppure è possibile usare un servizio eseguito da terze parti.</span><span class="sxs-lookup"><span data-stu-id="2a1eb-118">To create and issue licenses for protected content, you can create your own custom solution using the objects of the Windows Media Rights Manager SDK, or you can use a service run by a third party.</span></span>

<span data-ttu-id="2a1eb-119">Indipendentemente dal metodo utilizzato, i file protetti creati conterranno, nell'oggetto intestazione DRM, un URL che indica alle applicazioni client dove ottenere una licenza per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="2a1eb-119">Whichever method you use, the protected files that you create will contain, in the DRM header object, a URL that tells client applications where to obtain a license for the content.</span></span>

> [!Note]  
> <span data-ttu-id="2a1eb-120">Windows Media Format SDK non fornisce supporto per la creazione o l'emissione di licenze.</span><span class="sxs-lookup"><span data-stu-id="2a1eb-120">The Windows Media Format SDK does not provide support for creating or issuing licenses.</span></span>

 

<span data-ttu-id="2a1eb-121">Sul lato riproduzione, un'applicazione abilitata per DRM deve essere in grado di ottenere le licenze per il contenuto protetto, di decrittografare il contenuto usando la chiave contenuta nella licenza e di applicare le restrizioni di licenza, ad esempio il numero di volte in cui un file può essere riprodotto o se il file può essere copiato in un altro dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2a1eb-121">On the playback side, a DRM-enabled application must be able to obtain licenses for protected content, to decrypt that content using the key contained in the license, and to enforce the license restrictions, such as the number of times a file may be played, or whether the file can be copied to another device.</span></span> <span data-ttu-id="2a1eb-122">Windows Media Format SDK fornisce tutto il supporto necessario per creare un'applicazione di riproduzione DRM completamente abilitata.</span><span class="sxs-lookup"><span data-stu-id="2a1eb-122">The Windows Media Format SDK provides all the support required to create a fully enabled DRM playback application.</span></span>

> [!Note]  
> <span data-ttu-id="2a1eb-123">Il DRM non è supportato dalla versione basata su x64 di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="2a1eb-123">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2a1eb-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2a1eb-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a1eb-125">**Funzionalità di Rights Management digitali**</span><span class="sxs-lookup"><span data-stu-id="2a1eb-125">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="2a1eb-126">**Abilitazione del supporto DRM**</span><span class="sxs-lookup"><span data-stu-id="2a1eb-126">**Enabling DRM Support**</span></span>](enabling-drm-support.md)
</dt> </dl>

 

 




