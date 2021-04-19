---
description: Il materiale seguente fornisce linee guida sull'uso di TAPI per scrivere applicazioni per le comunicazioni tra l'utente finale e il server. Queste informazioni sono inoltre estremamente rilevanti per i programmatori del provider di servizi.
ms.assetid: fb97aff7-910e-451f-b183-36324a459423
title: Applicazioni TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6836f33af120171016b080693ae7a8315f9b9d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317642"
---
# <a name="tapi-applications"></a><span data-ttu-id="ad3c1-104">Applicazioni TAPI</span><span class="sxs-lookup"><span data-stu-id="ad3c1-104">TAPI Applications</span></span>

<span data-ttu-id="ad3c1-105">Il materiale seguente fornisce linee guida sull'uso di TAPI per scrivere applicazioni per le comunicazioni tra l'utente finale e il server.</span><span class="sxs-lookup"><span data-stu-id="ad3c1-105">The following material provides guidelines on using TAPI to write end-user or server communications applications.</span></span> <span data-ttu-id="ad3c1-106">Queste informazioni sono inoltre estremamente rilevanti per i programmatori del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="ad3c1-106">This information is also highly relevant to service provider programmers.</span></span>

<span data-ttu-id="ad3c1-107">La prima decisione che un programmatore deve eseguire nell'uso di TAPI è il livello di servizio necessario.</span><span class="sxs-lookup"><span data-stu-id="ad3c1-107">The first decision a programmer needs to make in using TAPI is the level of service required.</span></span> <span data-ttu-id="ad3c1-108">Se, ad esempio, un'applicazione richiede una selezione di menu che può comporre un numero di telefono, probabilmente non è necessaria un'applicazione TAPI completa.</span><span class="sxs-lookup"><span data-stu-id="ad3c1-108">For example, if an application requires a menu selection that can dial a phone number, a full TAPI application is probably not required.</span></span> <span data-ttu-id="ad3c1-109">La telefonia assistita consente di abilitare questa opzione in modo rapido e semplice.</span><span class="sxs-lookup"><span data-stu-id="ad3c1-109">Assisted Telephony can enable this option quickly and simply.</span></span> <span data-ttu-id="ad3c1-110">Per ulteriori informazioni sulla distinzione tra le applicazioni TAPI complete e la telefonia assistita, vedere [livelli di servizio TAPI](tapi-levels-of-service.md) .</span><span class="sxs-lookup"><span data-stu-id="ad3c1-110">Please see [TAPI Levels of Service](tapi-levels-of-service.md) for more information on the distinction between full TAPI applications and Assisted Telephony.</span></span>

<span data-ttu-id="ad3c1-111">La seconda decisione importante è se usare TAPI 2. x, l'API basata su C o TAPI 3. x, basata su COM.</span><span class="sxs-lookup"><span data-stu-id="ad3c1-111">The second important decision is whether to use TAPI 2.x, the C-based API, or TAPI 3.x, which is based on COM.</span></span> <span data-ttu-id="ad3c1-112">Vedere [TAPI 3. x e TAPI 2. x](tapi-3-x-versus-tapi-2-x.md) per una descrizione delle considerazioni importanti per decidere quale usare.</span><span class="sxs-lookup"><span data-stu-id="ad3c1-112">Please see [TAPI 3.x vs. TAPI 2.x](tapi-3-x-versus-tapi-2-x.md) for a discussion of important considerations in deciding which one to use.</span></span>

<span data-ttu-id="ad3c1-113">Il diagramma seguente illustra i blocchi predefiniti di base di un'applicazione TAPI completa.</span><span class="sxs-lookup"><span data-stu-id="ad3c1-113">The following diagram illustrates the basic building blocks of a full TAPI application.</span></span> <span data-ttu-id="ad3c1-114">TAPI 2. x e TAPI 3. x sono entrambi trattati in queste sezioni.</span><span class="sxs-lookup"><span data-stu-id="ad3c1-114">TAPI 2.x and TAPI 3.x are both addressed in these sections.</span></span> <span data-ttu-id="ad3c1-115">Il materiale che è molto specifico per uno viene trattato nelle sezioni Panoramica per TAPI 2. x o TAPI 3. x.</span><span class="sxs-lookup"><span data-stu-id="ad3c1-115">Material that is highly specific to one is addressed in the overview sections for TAPI 2.x or TAPI 3.x.</span></span>

![blocchi predefiniti di un'applicazione TAPI](images/tapior3.png)

<span data-ttu-id="ad3c1-117">I collegamenti seguenti forniscono contenuto che corrisponde alle figure nell'immagine precedente:</span><span class="sxs-lookup"><span data-stu-id="ad3c1-117">The following links provide content that corresponds to the figures in the above image:</span></span>

| <span data-ttu-id="ad3c1-118">Figura</span><span class="sxs-lookup"><span data-stu-id="ad3c1-118">Figure</span></span> | <span data-ttu-id="ad3c1-119">Documentazione</span><span class="sxs-lookup"><span data-stu-id="ad3c1-119">Documentation</span></span>                                                                    |
|--------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ad3c1-120">1</span><span class="sxs-lookup"><span data-stu-id="ad3c1-120">1</span></span>      | [<span data-ttu-id="ad3c1-121">Inizializzazione TAPI</span><span class="sxs-lookup"><span data-stu-id="ad3c1-121">TAPI Initialization</span></span>](tapi-initialization.md)                                   |
| <span data-ttu-id="ad3c1-122">2</span><span class="sxs-lookup"><span data-stu-id="ad3c1-122">2</span></span>      | [<span data-ttu-id="ad3c1-123">Controllo della sessione</span><span class="sxs-lookup"><span data-stu-id="ad3c1-123">Session Control</span></span>](session-control.md)                                           |
| <span data-ttu-id="ad3c1-124">3</span><span class="sxs-lookup"><span data-stu-id="ad3c1-124">3</span></span>      | [<span data-ttu-id="ad3c1-125">Controllo dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="ad3c1-125">Device Control</span></span>](device-control.md)                                             |
| <span data-ttu-id="ad3c1-126">4</span><span class="sxs-lookup"><span data-stu-id="ad3c1-126">4</span></span>      | [<span data-ttu-id="ad3c1-127">Controllo multimediale</span><span class="sxs-lookup"><span data-stu-id="ad3c1-127">Media Control</span></span>](media-control.md)                                               |
| <span data-ttu-id="ad3c1-128">5</span><span class="sxs-lookup"><span data-stu-id="ad3c1-128">5</span></span>      | [<span data-ttu-id="ad3c1-129">Informazioni sui controlli Call Center</span><span class="sxs-lookup"><span data-stu-id="ad3c1-129">About Call Center Controls</span></span>](about-call-center-controls.md)                     |
| <span data-ttu-id="ad3c1-130">6</span><span class="sxs-lookup"><span data-stu-id="ad3c1-130">6</span></span>      | [<span data-ttu-id="ad3c1-131">Conferenza telefonica IP Rendezvous</span><span class="sxs-lookup"><span data-stu-id="ad3c1-131">Rendezvous IP Telephony Conferencing</span></span>](rendezvous-ip-telephony-conferencing.md) |
| <span data-ttu-id="ad3c1-132">7</span><span class="sxs-lookup"><span data-stu-id="ad3c1-132">7</span></span>      | [<span data-ttu-id="ad3c1-133">Arresto TAPI</span><span class="sxs-lookup"><span data-stu-id="ad3c1-133">TAPI Shutdown</span></span>](tapi-shutdown.md)                                               |



 

 

 



