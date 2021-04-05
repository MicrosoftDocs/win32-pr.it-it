---
description: L'elenco seguente contiene i membri dell'indirizzo CMSP.
ms.assetid: ef15adef-1f4d-4bfc-8362-97fe1d118204
title: Membri di CMSPAddress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83213646427e7379b3eb2b45a0670f7908877175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885828"
---
# <a name="cmspaddress-members"></a><span data-ttu-id="67424-103">Membri di CMSPAddress</span><span class="sxs-lookup"><span data-stu-id="67424-103">CMSPAddress Members</span></span>



| <span data-ttu-id="67424-104">Tipi di membri</span><span class="sxs-lookup"><span data-stu-id="67424-104">Member types</span></span>                    | <span data-ttu-id="67424-105">Nome</span><span class="sxs-lookup"><span data-stu-id="67424-105">Name</span></span>                    | <span data-ttu-id="67424-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67424-106">Description</span></span>                                                                                      |
|---------------------------------|-------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67424-107">Iunknown</span><span class="sxs-lookup"><span data-stu-id="67424-107">Iunknown</span></span>                        | <span data-ttu-id="67424-108">\*\_pFTM m</span><span class="sxs-lookup"><span data-stu-id="67424-108">\*m\_pFTM</span></span>               | <span data-ttu-id="67424-109">Puntatore al marshaller a thread libero.</span><span class="sxs-lookup"><span data-stu-id="67424-109">Pointer to the free threaded marshaller.</span></span>                                                         |
| <span data-ttu-id="67424-110">HANDLE</span><span class="sxs-lookup"><span data-stu-id="67424-110">HANDLE</span></span>                          | <span data-ttu-id="67424-111">\_htEvent m</span><span class="sxs-lookup"><span data-stu-id="67424-111">m\_htEvent</span></span>              | <span data-ttu-id="67424-112">Handle per l'evento Tapi3.dll, che viene utilizzato per notificare a TAPI che il MSP desidera inviare dati.</span><span class="sxs-lookup"><span data-stu-id="67424-112">Handle to Tapi3.dll's event, which is used to notify TAPI that the MSP wants to send data to it.</span></span> |
| <span data-ttu-id="67424-113">\_voce elenco</span><span class="sxs-lookup"><span data-stu-id="67424-113">LIST\_ENTRY</span></span>                     | <span data-ttu-id="67424-114">\_evento m</span><span class="sxs-lookup"><span data-stu-id="67424-114">m\_EventList</span></span>            | <span data-ttu-id="67424-115">Elenco di eventi.</span><span class="sxs-lookup"><span data-stu-id="67424-115">List of events.</span></span>                                                                                  |
| <span data-ttu-id="67424-116">CMSPCritSection</span><span class="sxs-lookup"><span data-stu-id="67424-116">CMSPCritSection</span></span>                 | <span data-ttu-id="67424-117">\_EventDataLock m</span><span class="sxs-lookup"><span data-stu-id="67424-117">m\_EventDataLock</span></span>        | <span data-ttu-id="67424-118">Blocco che protegge i dati correlati alla gestione degli eventi con TAPI.</span><span class="sxs-lookup"><span data-stu-id="67424-118">The lock that protects the data related to event handling with TAPI.</span></span>                             |
| <span data-ttu-id="67424-119">ITTerminalManager</span><span class="sxs-lookup"><span data-stu-id="67424-119">ITTerminalManager</span></span>               | <span data-ttu-id="67424-120">\*\_pITTerminalManager m</span><span class="sxs-lookup"><span data-stu-id="67424-120">\*m\_pITTerminalManager</span></span> | <span data-ttu-id="67424-121">Puntatore all'oggetto di gestione terminal.</span><span class="sxs-lookup"><span data-stu-id="67424-121">The pointer to the Terminal Manager object.</span></span>                                                      |
| <span data-ttu-id="67424-122">CMSPArray <ITTerminal \*></span><span class="sxs-lookup"><span data-stu-id="67424-122">CMSPArray <ITTerminal \*></span></span> | <span data-ttu-id="67424-123">\_terminali m</span><span class="sxs-lookup"><span data-stu-id="67424-123">m\_Terminals</span></span>            | <span data-ttu-id="67424-124">Elenco di terminali statici che è possibile utilizzare per l'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="67424-124">The list of static terminals that can be used on the address.</span></span>                                    |
| <span data-ttu-id="67424-125">BOOL</span><span class="sxs-lookup"><span data-stu-id="67424-125">BOOL</span></span>                            | <span data-ttu-id="67424-126">\_fTerminalsUpToDate m</span><span class="sxs-lookup"><span data-stu-id="67424-126">m\_fTerminalsUpToDate</span></span>   | <span data-ttu-id="67424-127">Questo flag è **true** se l'elenco di terminali è aggiornato.</span><span class="sxs-lookup"><span data-stu-id="67424-127">This flag is **TRUE** if the terminal list is up to date.</span></span>                                        |
| <span data-ttu-id="67424-128">CMSPCritSection</span><span class="sxs-lookup"><span data-stu-id="67424-128">CMSPCritSection</span></span>                 | <span data-ttu-id="67424-129">\_TerminalDataLock m</span><span class="sxs-lookup"><span data-stu-id="67424-129">m\_TerminalDataLock</span></span>     | <span data-ttu-id="67424-130">Blocco che protegge i membri dati correlati al terminale.</span><span class="sxs-lookup"><span data-stu-id="67424-130">The lock that protects the terminal-related data members.</span></span>                                        |



 

 

 



