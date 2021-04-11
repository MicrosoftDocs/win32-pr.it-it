---
title: Individualizzazione DRM
description: Individualizzazione DRM
ms.assetid: 8f129bc1-3db9-4b41-9d60-daff037237ff
keywords:
- Windows Media Format SDK, individualizzazione DRM
- Digital Rights Management (DRM), individualizzazione
- DRM (Digital Rights Management), individualizzazione
- individualizzazione di DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 217be5cb5c1c7abef882c28961439baa93011c29
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329148"
---
# <a name="drm-individualization"></a><span data-ttu-id="774d4-107">Individualizzazione DRM</span><span class="sxs-lookup"><span data-stu-id="774d4-107">DRM Individualization</span></span>

<span data-ttu-id="774d4-108">I proprietari di contenuti protetti possono richiedere agli utenti di aggiornare alcuni componenti di Digital Rights Management (DRM) inclusi in Windows Media Format SDK prima di accedere al contenuto.</span><span class="sxs-lookup"><span data-stu-id="774d4-108">Owners of protected content may require users to upgrade some of the digital rights management (DRM) components included in the Windows Media Format SDK before accessing their content.</span></span> <span data-ttu-id="774d4-109">Se un utente accetta l'aggiornamento, una versione personalizzata di un file di protezione (uno univoco per il proprio computer) verrà scaricata da un sito Web Microsoft.</span><span class="sxs-lookup"><span data-stu-id="774d4-109">If a user accepts the upgrade, an individualized version of a security file (one unique to their computer) will be downloaded from a Microsoft Web site.</span></span> <span data-ttu-id="774d4-110">Se l'utente rifiuta l'aggiornamento, non sarà in grado di accedere al contenuto; Tuttavia, saranno comunque in grado di accedere al contenuto non protetto e ai contenuti protetti che non richiedono l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="774d4-110">If the user declines the upgrade, they will not be able to access the content; however, they will still be able to access unprotected content and protected content that does not require the upgrade.</span></span> <span data-ttu-id="774d4-111">L'esecuzione di un aggiornamento della sicurezza consente di aumentare il livello di protezione offerto da DRM.</span><span class="sxs-lookup"><span data-stu-id="774d4-111">Performing a security upgrade helps increase the level of protection offered by DRM.</span></span>

<span data-ttu-id="774d4-112">L'individualizzazione può essere eseguita in fase di installazione o quando un'applicazione rileva un file ASF protetto che la richiede.</span><span class="sxs-lookup"><span data-stu-id="774d4-112">Individualization can be done either at setup time or when an application first encounters a protected ASF file that requires it.</span></span> <span data-ttu-id="774d4-113">Poiché questo processo modifica i componenti di sistema di un utente, l'applicazione deve inviare una notifica all'utente e ottenere il consenso informato prima di eseguire l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="774d4-113">Because this process modifies a user's system components, the application must notify the user and obtain their informed consent before performing the upgrade.</span></span> <span data-ttu-id="774d4-114">In Microsoft Windows Media Player, ad esempio, viene visualizzata una finestra di dialogo con il testo seguente:</span><span class="sxs-lookup"><span data-stu-id="774d4-114">Microsoft Windows Media Player, for example, shows a dialog box with the following text:</span></span>

<span data-ttu-id="774d4-115">**Aggiornamento della sicurezza obbligatorio**</span><span class="sxs-lookup"><span data-stu-id="774d4-115">**Security Upgrade Required**</span></span>

<span data-ttu-id="774d4-116">**Il proprietario del contenuto protetto a cui si sta tentando di accedere richiede prima di tutto l'aggiornamento di alcuni componenti di Microsoft Digital Rights Management (DRM) nel computer.**</span><span class="sxs-lookup"><span data-stu-id="774d4-116">**The owner of the protected content you are trying to access requires you to first upgrade some of the Microsoft digital rights management (DRM) components on your computer.**</span></span>

<span data-ttu-id="774d4-117">**Fare clic su OK per aggiornare i componenti di DRM.**</span><span class="sxs-lookup"><span data-stu-id="774d4-117">**Click OK to upgrade your DRM components.**</span></span>

<span data-ttu-id="774d4-118">**Dettagli**</span><span class="sxs-lookup"><span data-stu-id="774d4-118">**Details:**</span></span>

<span data-ttu-id="774d4-119">**Quando si fa clic su OK, un identificatore univoco e un file di protezione DRM vengono inviati a un servizio Microsoft su Internet. Il file viene sostituito con una versione personalizzata che contiene l'identificatore univoco. Questo aumenta il livello di protezione fornito da DRM.**</span><span class="sxs-lookup"><span data-stu-id="774d4-119">**When you click OK, a unique identifier and a DRM security file are sent to a Microsoft service on the Internet. The file is replaced with a customized version that contains your unique identifier. This increases the level of protection provided by DRM.**</span></span>

<span data-ttu-id="774d4-120">Qualsiasi applicazione che supporta l'individualizzazione deve usare la stessa formulazione o la stessa parola.</span><span class="sxs-lookup"><span data-stu-id="774d4-120">Any application that supports individualization should use the same or similar wording.</span></span> <span data-ttu-id="774d4-121">Per ulteriori informazioni sull'informativa sulla privacy di Microsoft, vedere la sezione [informativa sulla privacy](privacy-statement.md) di questa documentazione.</span><span class="sxs-lookup"><span data-stu-id="774d4-121">For more information on Microsoft's Privacy Policy, see the [Privacy Statement](privacy-statement.md) section of this documentation.</span></span>

> [!Note]  
> <span data-ttu-id="774d4-122">Il DRM non è supportato dalla versione basata su x64 di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="774d4-122">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="774d4-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="774d4-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="774d4-124">**Funzionalità di Rights Management digitali**</span><span class="sxs-lookup"><span data-stu-id="774d4-124">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="774d4-125">**Applicazioni DRM individualizzazione**</span><span class="sxs-lookup"><span data-stu-id="774d4-125">**Individualizing DRM Applications**</span></span>](individualizing-drm-applications.md)
</dt> </dl>

 

 




