---
title: Abilitazione della sincronizzazione con Windows Media Player
description: Abilitazione della sincronizzazione con Windows Media Player
ms.assetid: a312dfef-ac48-4c58-a59a-b277f5386419
keywords:
- Windows Media Gestione dispositivi, sincronizzazione con Windows Media Player
- Gestione dispositivi, sincronizzazione con Windows Media Player
- Guida per programmatori, sincronizzazione con Windows Media Player
- provider di servizi, sincronizzazione con Windows Media Player
- creazione di provider di servizi, sincronizzazione con Windows Media Player
- sincronizzazione con Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b621be3b17d42368bc859081f47bc29bb2cfc667
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298987"
---
# <a name="enabling-synchronization-with-windows-media-player"></a><span data-ttu-id="caf8f-109">Abilitazione della sincronizzazione con Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="caf8f-109">Enabling Synchronization with Windows Media Player</span></span>

<span data-ttu-id="caf8f-110">È possibile consentire a un dispositivo di partecipare alla sincronizzazione automatica con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="caf8f-110">You can enable a device to participate in automatic synchronization with Windows Media Player.</span></span> <span data-ttu-id="caf8f-111">Con la sincronizzazione automatica, quando un dispositivo sincronizzato definito dall'utente si connette al computer, Windows Media Player scaricherà, aggiornerà o eliminerà automaticamente i file dal dispositivo senza richiedere input utente aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="caf8f-111">Automatic synchronization means that when a user-designated synchronized device connects to the computer, Windows Media Player will automatically download, update, or delete files from the device without requiring any additional user input.</span></span>

<span data-ttu-id="caf8f-112">Per impostazione predefinita, i dispositivi seguenti sono sincronizzati con Windows Media Player:</span><span class="sxs-lookup"><span data-stu-id="caf8f-112">By default the following devices are synchronized with Windows Media Player:</span></span>

-   <span data-ttu-id="caf8f-113">Dispositivi MTP</span><span class="sxs-lookup"><span data-stu-id="caf8f-113">MTP devices</span></span>
-   <span data-ttu-id="caf8f-114">Dispositivi di archiviazione di massa</span><span class="sxs-lookup"><span data-stu-id="caf8f-114">Mass-storage devices</span></span>
-   <span data-ttu-id="caf8f-115">Dispositivi Windows CE (Windows Media Player 10 mobile e versioni successive)</span><span class="sxs-lookup"><span data-stu-id="caf8f-115">Windows CE devices (Windows Media Player 10 Mobile and later)</span></span>

<span data-ttu-id="caf8f-116">Per qualsiasi altro dispositivo da sincronizzare con Media Player di Windows, devono essere soddisfatti i requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="caf8f-116">For any other device to synchronize with Windows Media Player, the following requirements must met:</span></span>

-   <span data-ttu-id="caf8f-117">Il dispositivo deve annunciare un'interfaccia del dispositivo PAP {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE}</span><span class="sxs-lookup"><span data-stu-id="caf8f-117">The device must advertise a PAP device interface that is {F33FDC04-D1AC-4E8E-9A30-19BBD4B108AE}</span></span>
-   <span data-ttu-id="caf8f-118">Gli oggetti dispositivo restituiti dal provider di servizi devono supportare l'interfaccia **IMDSPDevice3** .</span><span class="sxs-lookup"><span data-stu-id="caf8f-118">The device objects returned by service provider must support the **IMDSPDevice3** interface.</span></span>
-   <span data-ttu-id="caf8f-119">Il parametro UseExtendedWmdm del dispositivo deve essere impostato su un valore **DWORD** pari a 1.</span><span class="sxs-lookup"><span data-stu-id="caf8f-119">The device parameter UseExtendedWmdm must be set to a **DWORD** value of 1.</span></span> <span data-ttu-id="caf8f-120">Per ulteriori informazioni, vedere [parametri del dispositivo](device-parameters.md) .</span><span class="sxs-lookup"><span data-stu-id="caf8f-120">See [Device Parameters](device-parameters.md) for more information.</span></span>
-   <span data-ttu-id="caf8f-121">Il provider di servizi deve implementare le interfacce seguenti:</span><span class="sxs-lookup"><span data-stu-id="caf8f-121">The service provider should implement the following interfaces:</span></span>

    [<span data-ttu-id="caf8f-122">**IMDSPDevice3**</span><span class="sxs-lookup"><span data-stu-id="caf8f-122">**IMDSPDevice3**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice3)

    [<span data-ttu-id="caf8f-123">**IMDSPObject2**</span><span class="sxs-lookup"><span data-stu-id="caf8f-123">**IMDSPObject2**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)

    [<span data-ttu-id="caf8f-124">**IMDSPStorage4**</span><span class="sxs-lookup"><span data-stu-id="caf8f-124">**IMDSPStorage4**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage4)

## <a name="related-topics"></a><span data-ttu-id="caf8f-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="caf8f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="caf8f-126">**Creazione di un provider di servizi**</span><span class="sxs-lookup"><span data-stu-id="caf8f-126">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> <dt>

[<span data-ttu-id="caf8f-127">**Parametri del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="caf8f-127">**Device Parameters**</span></span>](device-parameters.md)
</dt> </dl>

 

 




