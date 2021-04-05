---
title: Flag di enumerazione
description: Flag di enumerazione
ms.assetid: d5677e3a-c0c1-4768-aae4-f6564a40ee99
keywords:
- Enumerazione
- Flag di enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1cbec08496ccd6338de77ebdddf76547a48258
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955479"
---
# <a name="enumeration-flags"></a><span data-ttu-id="2ee41-105">Flag di enumerazione</span><span class="sxs-lookup"><span data-stu-id="2ee41-105">Enumeration Flags</span></span>



| <span data-ttu-id="2ee41-106">Costante</span><span class="sxs-lookup"><span data-stu-id="2ee41-106">Constant</span></span>               | <span data-ttu-id="2ee41-107">Valore</span><span class="sxs-lookup"><span data-stu-id="2ee41-107">Value</span></span>      | <span data-ttu-id="2ee41-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ee41-108">Description</span></span>                                                                                                                                               |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ee41-109">\_inizio enum \_ RTM</span><span class="sxs-lookup"><span data-stu-id="2ee41-109">RTM\_ENUM\_START</span></span>       | <span data-ttu-id="2ee41-110">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ee41-110">0x00000000</span></span> | <span data-ttu-id="2ee41-111">Enumerare route o destinazioni a partire da 0/0.</span><span class="sxs-lookup"><span data-stu-id="2ee41-111">Enumerate routes or destinations starting at 0/0.</span></span>                                                                                                         |
| <span data-ttu-id="2ee41-112">\_enumerazione RTM \_ successiva</span><span class="sxs-lookup"><span data-stu-id="2ee41-112">RTM\_ENUM\_NEXT</span></span>        | <span data-ttu-id="2ee41-113">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2ee41-113">0x00000001</span></span> | <span data-ttu-id="2ee41-114">Enumera le route o le destinazioni a partire dalla lunghezza dell'indirizzo/maschera specificata (ad esempio, 10/8).</span><span class="sxs-lookup"><span data-stu-id="2ee41-114">Enumerate routes or destinations starting at the specified address/mask length (such as 10/8).</span></span> <span data-ttu-id="2ee41-115">L'enumerazione continua fino alla fine della tabella di routing.</span><span class="sxs-lookup"><span data-stu-id="2ee41-115">The enumeration continues to the end of the routing table.</span></span> |
| <span data-ttu-id="2ee41-116">\_intervallo enum \_ RTM</span><span class="sxs-lookup"><span data-stu-id="2ee41-116">RTM\_ENUM\_RANGE</span></span>       | <span data-ttu-id="2ee41-117">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2ee41-117">0x00000002</span></span> | <span data-ttu-id="2ee41-118">Enumera le route o le destinazioni nel sottoalbero specificato dalla lunghezza dell'indirizzo/maschera, ad esempio 10/8.</span><span class="sxs-lookup"><span data-stu-id="2ee41-118">Enumerate routes or destinations in the specified subtree specified by the address/mask length (such as 10/8).</span></span>                                            |
| <span data-ttu-id="2ee41-119">\_ \_ tutte le \_ DestS enum di RTM</span><span class="sxs-lookup"><span data-stu-id="2ee41-119">RTM\_ENUM\_ALL\_DESTS</span></span>  | <span data-ttu-id="2ee41-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ee41-120">0x00000000</span></span> | <span data-ttu-id="2ee41-121">Restituisce tutte le destinazioni.</span><span class="sxs-lookup"><span data-stu-id="2ee41-121">Return all destinations.</span></span>                                                                                                                                  |
| <span data-ttu-id="2ee41-122">\_DestS dell'enumerazione RTM \_ \_</span><span class="sxs-lookup"><span data-stu-id="2ee41-122">RTM\_ENUM\_OWN\_DESTS</span></span>  | <span data-ttu-id="2ee41-123">0x01000000</span><span class="sxs-lookup"><span data-stu-id="2ee41-123">0x01000000</span></span> | <span data-ttu-id="2ee41-124">Restituire solo le destinazioni di proprietà del client.</span><span class="sxs-lookup"><span data-stu-id="2ee41-124">Return only those destinations that the client owns.</span></span>                                                                                                      |
| <span data-ttu-id="2ee41-125">\_ \_ tutte le route di enum RTM \_</span><span class="sxs-lookup"><span data-stu-id="2ee41-125">RTM\_ENUM\_ALL\_ROUTES</span></span> | <span data-ttu-id="2ee41-126">0x00000000</span><span class="sxs-lookup"><span data-stu-id="2ee41-126">0x00000000</span></span> | <span data-ttu-id="2ee41-127">Restituisce tutte le route.</span><span class="sxs-lookup"><span data-stu-id="2ee41-127">Return all routes.</span></span>                                                                                                                                        |
| <span data-ttu-id="2ee41-128">\_ \_ route personalizzate enum \_ RTM</span><span class="sxs-lookup"><span data-stu-id="2ee41-128">RTM\_ENUM\_OWN\_ROUTES</span></span> | <span data-ttu-id="2ee41-129">0x00010000</span><span class="sxs-lookup"><span data-stu-id="2ee41-129">0x00010000</span></span> | <span data-ttu-id="2ee41-130">Restituisce solo le route di proprietà del client.</span><span class="sxs-lookup"><span data-stu-id="2ee41-130">Return only those routes that the client owns.</span></span>                                                                                                            |



 

 

 




