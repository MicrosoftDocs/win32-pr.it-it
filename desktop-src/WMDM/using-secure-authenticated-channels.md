---
title: Uso di canali con autenticazione sicura
description: Uso di canali con autenticazione sicura
ms.assetid: ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7
keywords:
- Windows Media Gestione dispositivi, autenticazione
- Gestione dispositivi, autenticazione
- applicazioni desktop, autenticazione
- provider di servizi, autenticazione
- Guida per programmatori, autenticazione
- autenticazione
- Windows Media Gestione dispositivi, comunicazione protetta
- Gestione dispositivi, comunicazione protetta
- applicazioni desktop, comunicazione protetta
- provider di servizi, comunicazione protetta
- Guida per programmatori, comunicazione sicura
- comunicazione protetta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f88c271cecc2e9252a3f7af0540beef3dc57d2b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044343"
---
# <a name="using-secure-authenticated-channels"></a><span data-ttu-id="dc236-115">Uso di canali con autenticazione sicura</span><span class="sxs-lookup"><span data-stu-id="dc236-115">Using Secure Authenticated Channels</span></span>

<span data-ttu-id="dc236-116">Windows Media Gestione dispositivi consente l'autenticazione e la comunicazione sicura tra i componenti fornendo due classi helper, [CSecureChannelClient](csecurechannelclient-class.md) (per le applicazioni) e [CSecureChannelServer](csecurechannelserver-class.md) (per i provider di servizi) e un'interfaccia, [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (per entrambi).</span><span class="sxs-lookup"><span data-stu-id="dc236-116">Windows Media Device Manager enables authentication and secure communication between components by providing two helper classes, [CSecureChannelClient](csecurechannelclient-class.md) (for applications) and [CSecureChannelServer](csecurechannelserver-class.md) (for service providers), and one interface, [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (for both).</span></span> <span data-ttu-id="dc236-117">Insieme costituiscono un'API per l'uso di canali con autenticazione sicura (SAC).</span><span class="sxs-lookup"><span data-stu-id="dc236-117">Together these make up an API for the use of secure authenticated channels (SAC).</span></span> <span data-ttu-id="dc236-118">SAC gestisce le tre attività seguenti per i provider di servizi o le applicazioni che usano Windows Media Gestione dispositivi:</span><span class="sxs-lookup"><span data-stu-id="dc236-118">SAC handles the following three tasks for service providers or applications using Windows Media Device Manager:</span></span>

-   [<span data-ttu-id="dc236-119">Autenticazione componenti</span><span class="sxs-lookup"><span data-stu-id="dc236-119">Component Authentication</span></span>](component-authentication.md)
-   [<span data-ttu-id="dc236-120">Crittografia e decrittografia</span><span class="sxs-lookup"><span data-stu-id="dc236-120">Encryption and Decryption</span></span>](encryption-and-decryption.md)
-   [<span data-ttu-id="dc236-121">Autenticazione del messaggio</span><span class="sxs-lookup"><span data-stu-id="dc236-121">Message Authentication</span></span>](message-authentication.md)

<span data-ttu-id="dc236-122">Un'applicazione o un provider di servizi deve gestire l'autenticazione, la crittografia e la decrittografia di componenti. l'autenticazione del messaggio è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="dc236-122">An application or service provider must handle component authentication, encryption, and decryption; message authentication is optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc236-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dc236-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc236-124">**Attività comuni per le applicazioni e i provider di servizi**</span><span class="sxs-lookup"><span data-stu-id="dc236-124">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




