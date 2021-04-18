---
title: Visualizza flag
description: Usare i flag di visualizzazione per controllare le viste delle tabelle di routing.
ms.assetid: 836e3400-0dca-4a21-9a5c-7da357ed72ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5192bf3e1acaa91412d8ae7e06d035e54af1ece6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298803"
---
# <a name="view-flags"></a><span data-ttu-id="6c4fa-103">Visualizza flag</span><span class="sxs-lookup"><span data-stu-id="6c4fa-103">View Flags</span></span>

<span data-ttu-id="6c4fa-104">Usare i flag di visualizzazione per controllare le viste delle tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-104">Use the View Flags to control routing table views.</span></span>



| <span data-ttu-id="6c4fa-105">Costante</span><span class="sxs-lookup"><span data-stu-id="6c4fa-105">Constant</span></span>                 | <span data-ttu-id="6c4fa-106">Valore</span><span class="sxs-lookup"><span data-stu-id="6c4fa-106">Value</span></span>      | <span data-ttu-id="6c4fa-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c4fa-107">Description</span></span>                                                      |
|--------------------------|------------|------------------------------------------------------------------|
| <span data-ttu-id="6c4fa-108">\_dimensioni massime \_ Indirizzo RTM \_</span><span class="sxs-lookup"><span data-stu-id="6c4fa-108">RTM\_MAX \_ADDRESS\_SIZE</span></span> | <span data-ttu-id="6c4fa-109">16</span><span class="sxs-lookup"><span data-stu-id="6c4fa-109">16</span></span>         | <span data-ttu-id="6c4fa-110">Dimensioni massime degli indirizzi per una famiglia di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-110">Max address size for an address family.</span></span>                          |
| <span data-ttu-id="6c4fa-111">\_visualizzazioni massime RTM \_</span><span class="sxs-lookup"><span data-stu-id="6c4fa-111">RTM\_MAX\_VIEWS</span></span>          | <span data-ttu-id="6c4fa-112">32</span><span class="sxs-lookup"><span data-stu-id="6c4fa-112">32</span></span>         | <span data-ttu-id="6c4fa-113">Numero massimo di visualizzazioni che possono essere attive nella tabella di routing.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-113">Maximum number of views that can be active in the routing table.</span></span> |
| <span data-ttu-id="6c4fa-114">\_ID vista \_ RTM \_ UCAST</span><span class="sxs-lookup"><span data-stu-id="6c4fa-114">RTM\_VIEW\_ID\_UCAST</span></span>     | <span data-ttu-id="6c4fa-115">0</span><span class="sxs-lookup"><span data-stu-id="6c4fa-115">0</span></span>          | <span data-ttu-id="6c4fa-116">Specifica una visualizzazione unicast.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-116">Specifies a unicast view.</span></span>                                        |
| <span data-ttu-id="6c4fa-117">\_ID vista \_ RTM \_ mcast</span><span class="sxs-lookup"><span data-stu-id="6c4fa-117">RTM\_VIEW\_ID\_MCAST</span></span>     | <span data-ttu-id="6c4fa-118">1</span><span class="sxs-lookup"><span data-stu-id="6c4fa-118">1</span></span>          | <span data-ttu-id="6c4fa-119">Specifica una visualizzazione multicast.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-119">Specifies a multicast view.</span></span>                                      |
| <span data-ttu-id="6c4fa-120">\_dimensioni della \_ maschera di visualizzazione RTM \_</span><span class="sxs-lookup"><span data-stu-id="6c4fa-120">RTM\_VIEW\_MASK\_SIZE</span></span>    | <span data-ttu-id="6c4fa-121">0x20</span><span class="sxs-lookup"><span data-stu-id="6c4fa-121">0x20</span></span>       | <span data-ttu-id="6c4fa-122">Specifica il numero massimo di visualizzazioni che è possibile configurare.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-122">Specifies the maximum number of views that can be configured.</span></span>    |
| <span data-ttu-id="6c4fa-123">\_maschera di visualizzazione RTM \_ \_ None</span><span class="sxs-lookup"><span data-stu-id="6c4fa-123">RTM\_VIEW\_MASK\_NONE</span></span>    | <span data-ttu-id="6c4fa-124">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c4fa-124">0x00000000</span></span> | <span data-ttu-id="6c4fa-125">Restituisce informazioni indipendentemente dalla visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-125">Returns information regardless of the view.</span></span>                      |
| <span data-ttu-id="6c4fa-126">\_maschera di visualizzazione RTM \_ \_ any</span><span class="sxs-lookup"><span data-stu-id="6c4fa-126">RTM\_VIEW\_MASK\_ANY</span></span>     | <span data-ttu-id="6c4fa-127">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6c4fa-127">0x00000000</span></span> | <span data-ttu-id="6c4fa-128">Restituisce le destinazioni da tutte le visualizzazioni.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-128">Returns destinations from all views.</span></span> <span data-ttu-id="6c4fa-129">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-129">This is the default value.</span></span>  |
| <span data-ttu-id="6c4fa-130">\_maschera di visualizzazione RTM \_ \_ UCAST</span><span class="sxs-lookup"><span data-stu-id="6c4fa-130">RTM\_VIEW\_MASK\_UCAST</span></span>   | <span data-ttu-id="6c4fa-131">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6c4fa-131">0x00000001</span></span> | <span data-ttu-id="6c4fa-132">Restituisce le destinazioni dalla visualizzazione unicast.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-132">Returns destinations from the unicast view.</span></span>                      |
| <span data-ttu-id="6c4fa-133">\_maschera di visualizzazione RTM \_ \_ mcast</span><span class="sxs-lookup"><span data-stu-id="6c4fa-133">RTM\_VIEW\_MASK\_MCAST</span></span>   | <span data-ttu-id="6c4fa-134">0x00000002</span><span class="sxs-lookup"><span data-stu-id="6c4fa-134">0x00000002</span></span> | <span data-ttu-id="6c4fa-135">Restituisce le destinazioni dalla visualizzazione multicast.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-135">Returns destinations from the multicast view.</span></span>                    |
| <span data-ttu-id="6c4fa-136">\_maschera di visualizzazione RTM \_ \_ All</span><span class="sxs-lookup"><span data-stu-id="6c4fa-136">RTM\_VIEW\_MASK\_ALL</span></span>     | <span data-ttu-id="6c4fa-137">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="6c4fa-137">0xFFFFFFFF</span></span> | <span data-ttu-id="6c4fa-138">Restituisce informazioni da tutte le visualizzazioni.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-138">Returns information from all views.</span></span>                              |



 

 

 




