---
description: L'elenco seguente contiene i membri CMSPCAllBase.
ms.assetid: a3193639-e0c4-4851-a879-551eca8023f9
title: Membri di CMSPCallBase
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ddae67d85a64a5a443727b3950054957c7f24f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231688"
---
# <a name="cmspcallbase-members"></a><span data-ttu-id="f1947-103">Membri di CMSPCallBase</span><span class="sxs-lookup"><span data-stu-id="f1947-103">CMSPCallBase Members</span></span>



| <span data-ttu-id="f1947-104">Tipo di membro</span><span class="sxs-lookup"><span data-stu-id="f1947-104">Member type</span></span>                   | <span data-ttu-id="f1947-105">Nome</span><span class="sxs-lookup"><span data-stu-id="f1947-105">Name</span></span>             | <span data-ttu-id="f1947-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1947-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1947-107">IUnknown</span><span class="sxs-lookup"><span data-stu-id="f1947-107">IUnknown</span></span>                      | <span data-ttu-id="f1947-108">\*\_pFTM m</span><span class="sxs-lookup"><span data-stu-id="f1947-108">\*m\_pFTM</span></span>        | <span data-ttu-id="f1947-109">Puntatore al marshaller a thread libero.</span><span class="sxs-lookup"><span data-stu-id="f1947-109">Pointer to the free threaded marshaller.</span></span>                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="f1947-110">CMSPAddress\*</span><span class="sxs-lookup"><span data-stu-id="f1947-110">CMSPAddress\*</span></span>                 | <span data-ttu-id="f1947-111">\*\_pMSPAddress m</span><span class="sxs-lookup"><span data-stu-id="f1947-111">\*m\_pMSPAddress</span></span> | <span data-ttu-id="f1947-112">Puntatore all'oggetto indirizzo MSP.</span><span class="sxs-lookup"><span data-stu-id="f1947-112">The pointer to the MSP address object.</span></span> <span data-ttu-id="f1947-113">Viene usato per ottenere i terminali predefiniti se l'applicazione non seleziona alcuna.</span><span class="sxs-lookup"><span data-stu-id="f1947-113">It is used to get the default terminals if the application doesn't select any.</span></span> <span data-ttu-id="f1947-114">Contiene anche un refcount (tramite [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref), non AddRef), in modo che l'indirizzo aggregato non venga tolto mentre la chiamata è ancora attiva, ma l'indirizzo di TAPI 3 non è AddRef'ed.</span><span class="sxs-lookup"><span data-stu-id="f1947-114">It also carries a refcount (via [**MSPAddressAddRef**](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref), not AddRef) so that the aggregated address will not go away while the call is still alive, but TAPI 3's address is not AddRef'ed.</span></span> |
| <span data-ttu-id="f1947-115">\_handle msp</span><span class="sxs-lookup"><span data-stu-id="f1947-115">MSP\_HANDLE</span></span>                   | <span data-ttu-id="f1947-116">\*\_htCall m</span><span class="sxs-lookup"><span data-stu-id="f1947-116">\*m\_htCall</span></span>      | <span data-ttu-id="f1947-117">Handle per chiamare TAPI3's.</span><span class="sxs-lookup"><span data-stu-id="f1947-117">The handle to TAPI3's call.</span></span> <span data-ttu-id="f1947-118">Utilizzato per attivare gli eventi di chiamata.</span><span class="sxs-lookup"><span data-stu-id="f1947-118">Used to fire call events.</span></span>                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="f1947-119">DWORD</span><span class="sxs-lookup"><span data-stu-id="f1947-119">DWORD</span></span>                         | <span data-ttu-id="f1947-120">\_dwMediaType m</span><span class="sxs-lookup"><span data-stu-id="f1947-120">m\_dwMediaType</span></span>   | <span data-ttu-id="f1947-121">Maschera di maschera dei tipi di supporto in questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="f1947-121">Bitmask of the media types on this call.</span></span>                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="f1947-122">CMSPArray <ITStream \*></span><span class="sxs-lookup"><span data-stu-id="f1947-122">CMSPArray <ITStream \*></span></span> | <span data-ttu-id="f1947-123">\_flussi m</span><span class="sxs-lookup"><span data-stu-id="f1947-123">m\_Streams</span></span>       | <span data-ttu-id="f1947-124">Elenco di oggetti Stream nella chiamata.</span><span class="sxs-lookup"><span data-stu-id="f1947-124">The list of stream objects in the call.</span></span>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="f1947-125">CMSPCritSection</span><span class="sxs-lookup"><span data-stu-id="f1947-125">CMSPCritSection</span></span>               | <span data-ttu-id="f1947-126">\_blocco m</span><span class="sxs-lookup"><span data-stu-id="f1947-126">m\_lock</span></span>          | <span data-ttu-id="f1947-127">Blocco che protegge gli elenchi di flussi.</span><span class="sxs-lookup"><span data-stu-id="f1947-127">The lock that protects the stream lists.</span></span>                                                                                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="f1947-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f1947-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1947-129">**CMSPCallBase**</span><span class="sxs-lookup"><span data-stu-id="f1947-129">**CMSPCallBase**</span></span>](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)
</dt> </dl>

 

 



