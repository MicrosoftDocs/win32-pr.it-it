---
description: L'elenco seguente contiene i membri CMSPStream.
ms.assetid: 792a29ac-ebbb-4bb2-bebf-fbf870b18e84
title: Membri di CMSPStream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dacee41ff95cdf16c7cd50c2e39017d9dfa7e83c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131719"
---
# <a name="cmspstream-members"></a><span data-ttu-id="e49eb-103">Membri di CMSPStream</span><span class="sxs-lookup"><span data-stu-id="e49eb-103">CMSPStream Members</span></span>



| <span data-ttu-id="e49eb-104">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="e49eb-104">Member type</span></span>                     | <span data-ttu-id="e49eb-105">Nome</span><span class="sxs-lookup"><span data-stu-id="e49eb-105">Name</span></span>                | <span data-ttu-id="e49eb-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e49eb-106">Description</span></span>                                                                                                                                |
|---------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e49eb-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="e49eb-107">IUnknown</span></span>                        | <span data-ttu-id="e49eb-108">\*\_pFTM m</span><span class="sxs-lookup"><span data-stu-id="e49eb-108">\*m\_pFTM</span></span>           | <span data-ttu-id="e49eb-109">Puntatore al marshaller a thread libero.</span><span class="sxs-lookup"><span data-stu-id="e49eb-109">Pointer to the free threaded marshaller.</span></span>                                                                                                   |
| <span data-ttu-id="e49eb-110">DWORD</span><span class="sxs-lookup"><span data-stu-id="e49eb-110">DWORD</span></span>                           | <span data-ttu-id="e49eb-111">\_dwState m</span><span class="sxs-lookup"><span data-stu-id="e49eb-111">m\_dwState</span></span>          | <span data-ttu-id="e49eb-112">Stato corrente del flusso.</span><span class="sxs-lookup"><span data-stu-id="e49eb-112">The current state of the stream.</span></span>                                                                                                           |
| <span data-ttu-id="e49eb-113">HANDLE</span><span class="sxs-lookup"><span data-stu-id="e49eb-113">HANDLE</span></span>                          | <span data-ttu-id="e49eb-114">\_hAddress m</span><span class="sxs-lookup"><span data-stu-id="e49eb-114">m\_hAddress</span></span>         | <span data-ttu-id="e49eb-115">Indirizzo in cui viene utilizzato il flusso.</span><span class="sxs-lookup"><span data-stu-id="e49eb-115">The address on which this stream is being used.</span></span>                                                                                            |
| <span data-ttu-id="e49eb-116">DWORD</span><span class="sxs-lookup"><span data-stu-id="e49eb-116">DWORD</span></span>                           | <span data-ttu-id="e49eb-117">\_dwMediaType m</span><span class="sxs-lookup"><span data-stu-id="e49eb-117">m\_dwMediaType</span></span>      | <span data-ttu-id="e49eb-118">Il [**tipo di supporto**](tapimediatype--constants.md) di questo flusso (audio, video e così via).</span><span class="sxs-lookup"><span data-stu-id="e49eb-118">The [**media type**](tapimediatype--constants.md) of this stream (audio, video, etc.).</span></span>                                                    |
| <span data-ttu-id="e49eb-119">direzione del terminale \_</span><span class="sxs-lookup"><span data-stu-id="e49eb-119">TERMINAL\_DIRECTION</span></span>             | <span data-ttu-id="e49eb-120">\_direzione m</span><span class="sxs-lookup"><span data-stu-id="e49eb-120">m\_Direction</span></span>        | <span data-ttu-id="e49eb-121">[**Direzione**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) del flusso (in entrata o in uscita).</span><span class="sxs-lookup"><span data-stu-id="e49eb-121">The [**direction**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) of this stream (incoming or outgoing).</span></span>                                                         |
| <span data-ttu-id="e49eb-122">CMSPCallBase</span><span class="sxs-lookup"><span data-stu-id="e49eb-122">CMSPCallBase</span></span>                    | <span data-ttu-id="e49eb-123">\*\_pMSPCall m</span><span class="sxs-lookup"><span data-stu-id="e49eb-123">\*m\_pMSPCall</span></span>       | <span data-ttu-id="e49eb-124">Puntatore all'oggetto chiamata.</span><span class="sxs-lookup"><span data-stu-id="e49eb-124">Pointer to the call object.</span></span>                                                                                                                |
| <span data-ttu-id="e49eb-125">IGraphBuilder</span><span class="sxs-lookup"><span data-stu-id="e49eb-125">IGraphBuilder</span></span>                   | <span data-ttu-id="e49eb-126">\*\_pIGraphBuilder m</span><span class="sxs-lookup"><span data-stu-id="e49eb-126">\*m\_pIGraphBuilder</span></span> | <span data-ttu-id="e49eb-127">Puntatore a interfacce di oggetti Graph.</span><span class="sxs-lookup"><span data-stu-id="e49eb-127">Pointer to graph object interfaces.</span></span>                                                                                                        |
| <span data-ttu-id="e49eb-128">IMediaControl</span><span class="sxs-lookup"><span data-stu-id="e49eb-128">IMediaControl</span></span>                   | <span data-ttu-id="e49eb-129">\*\_pIMediaControl m</span><span class="sxs-lookup"><span data-stu-id="e49eb-129">\*m\_pIMediaControl</span></span> | <span data-ttu-id="e49eb-130">Puntatore all'interfaccia del controllo multimediale.</span><span class="sxs-lookup"><span data-stu-id="e49eb-130">Pointer to the media control interface.</span></span>                                                                                                    |
| <span data-ttu-id="e49eb-131">CMSPArray <ITTerminal \*></span><span class="sxs-lookup"><span data-stu-id="e49eb-131">CMSPArray <ITTerminal \*></span></span> | <span data-ttu-id="e49eb-132">\_terminali m</span><span class="sxs-lookup"><span data-stu-id="e49eb-132">m\_Terminals</span></span>        | <span data-ttu-id="e49eb-133">Elenco di terminali nel flusso.</span><span class="sxs-lookup"><span data-stu-id="e49eb-133">The list of terminals on the stream.</span></span>                                                                                                       |
| <span data-ttu-id="e49eb-134">CMSPCritSection</span><span class="sxs-lookup"><span data-stu-id="e49eb-134">CMSPCritSection</span></span>                 | <span data-ttu-id="e49eb-135">\_blocco m</span><span class="sxs-lookup"><span data-stu-id="e49eb-135">m\_lock</span></span>             | <span data-ttu-id="e49eb-136">Blocco che protegge l'oggetto flusso.</span><span class="sxs-lookup"><span data-stu-id="e49eb-136">The lock that protects the stream object.</span></span> <span data-ttu-id="e49eb-137">L'oggetto Stream non deve mai acquisire il blocco e quindi chiamare un metodo MSPCall che potrebbe bloccarsi.</span><span class="sxs-lookup"><span data-stu-id="e49eb-137">The stream object should never acquire the lock and then call an MSPCall method that might lock.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e49eb-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e49eb-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e49eb-139">**CMSPStream**</span><span class="sxs-lookup"><span data-stu-id="e49eb-139">**CMSPStream**</span></span>](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)
</dt> </dl>

 

 



