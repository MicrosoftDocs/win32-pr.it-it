---
description: 'Metodi virtuali puri CMSPCallBase: questi metodi devono essere sottoposti a override dalle classi derivate.'
ms.assetid: 2ea9d35a-c87e-44f4-8dc6-618251c81fe4
title: Metodi virtuali puri CMSPCallBase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8da8530ab3dae737bf1407f00d5d4a415a1437e3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094459"
---
# <a name="cmspcallbase-pure-virtual-methods"></a><span data-ttu-id="6a814-103">Metodi virtuali puri CMSPCallBase</span><span class="sxs-lookup"><span data-stu-id="6a814-103">CMSPCallBase Pure Virtual Methods</span></span>

<span data-ttu-id="6a814-104">Questi metodi devono essere sottoposti a override dalle classi derivate.</span><span class="sxs-lookup"><span data-stu-id="6a814-104">These methods must be overridden by derived classes.</span></span>



| <span data-ttu-id="6a814-105">Metodi virtuali puri CMSPCallBase</span><span class="sxs-lookup"><span data-stu-id="6a814-105">CMSPCallBase pure virtual methods</span></span>                                 | <span data-ttu-id="6a814-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a814-106">Description</span></span>                                                                                                                             |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a814-107">**MSPCallAddRef**</span><span class="sxs-lookup"><span data-stu-id="6a814-107">**MSPCallAddRef**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcalladdref)               | <span data-ttu-id="6a814-108">Metodo AddRef privato per l'oggetto di chiamata.</span><span class="sxs-lookup"><span data-stu-id="6a814-108">Private AddRef method for the call object.</span></span>                                                                                              |
| [<span data-ttu-id="6a814-109">**MSPCallRelease**</span><span class="sxs-lookup"><span data-stu-id="6a814-109">**MSPCallRelease**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-mspcallrelease)             | <span data-ttu-id="6a814-110">Metodo Release privato per l'oggetto di chiamata.</span><span class="sxs-lookup"><span data-stu-id="6a814-110">Private Release method for the call object.</span></span>                                                                                             |
| [<span data-ttu-id="6a814-111">**Init**</span><span class="sxs-lookup"><span data-stu-id="6a814-111">**Init**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-init)                                 | <span data-ttu-id="6a814-112">Chiamato dall'oggetto indirizzo MSP (nel metodo [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) per inizializzare l'oggetto chiamata MSP.</span><span class="sxs-lookup"><span data-stu-id="6a814-112">Called by the MSP address object (in the method [**CreateMSPCall**](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)) to initialize the MSP call object.</span></span> |
| [<span data-ttu-id="6a814-113">**Arresto**</span><span class="sxs-lookup"><span data-stu-id="6a814-113">**ShutDown**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-shutdown)                         | <span data-ttu-id="6a814-114">Chiamato dall'oggetto indirizzo MSP per arrestare la chiamata.</span><span class="sxs-lookup"><span data-stu-id="6a814-114">Called by the MSP address object to shut down the call..</span></span>                                                                                |
| [<span data-ttu-id="6a814-115">**InternalCreateStream**</span><span class="sxs-lookup"><span data-stu-id="6a814-115">**InternalCreateStream**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) | <span data-ttu-id="6a814-116">Chiamato da [**CreateStream per**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) creare un oggetto flusso.</span><span class="sxs-lookup"><span data-stu-id="6a814-116">Called by [**CreateStream**](/windows/win32/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream) to create a stream object.</span></span>                                               |
| [<span data-ttu-id="6a814-117">**CreateStreamObject**</span><span class="sxs-lookup"><span data-stu-id="6a814-117">**CreateStreamObject**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-createstreamobject)     | <span data-ttu-id="6a814-118">Chiamato da [**InternalCreateStream per**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) creare un oggetto flusso.</span><span class="sxs-lookup"><span data-stu-id="6a814-118">Called by [**InternalCreateStream**](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-internalcreatestream) to create a stream object.</span></span>                                  |
| [<span data-ttu-id="6a814-119">**RemoveStream**</span><span class="sxs-lookup"><span data-stu-id="6a814-119">**RemoveStream**</span></span>](/windows/desktop/api/Mspcall/nf-mspcall-cmspcallbase-removestream)                 | <span data-ttu-id="6a814-120">Chiamato dall'applicazione per rimuovere un flusso dalla chiamata</span><span class="sxs-lookup"><span data-stu-id="6a814-120">Called by the application to remove a stream from the call</span></span>                                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="6a814-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6a814-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a814-122">**CMSPCallBase**</span><span class="sxs-lookup"><span data-stu-id="6a814-122">**CMSPCallBase**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 
