---
title: Flag di notifica delle modifiche
description: Flag di notifica delle modifiche
ms.assetid: 1f1aef71-a2b7-49ad-a0bc-f61f10b701c9
keywords:
- Modifica
- Flag di notifica delle modifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e6d3015be29c84b6b93b47b373d05f96f4388b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330292"
---
# <a name="change-notification-flags"></a><span data-ttu-id="f32a0-105">Flag di notifica delle modifiche</span><span class="sxs-lookup"><span data-stu-id="f32a0-105">Change Notification Flags</span></span>



| <span data-ttu-id="f32a0-106">Costante</span><span class="sxs-lookup"><span data-stu-id="f32a0-106">Constant</span></span>                         | <span data-ttu-id="f32a0-107">Valore</span><span class="sxs-lookup"><span data-stu-id="f32a0-107">Value</span></span>      | <span data-ttu-id="f32a0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f32a0-108">Description</span></span>                                                                                                                                                           |
|----------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f32a0-109">\_tipi di \_ modifiche RTM num \_</span><span class="sxs-lookup"><span data-stu-id="f32a0-109">RTM\_NUM\_CHANGE\_TYPES</span></span>          | <span data-ttu-id="f32a0-110">3</span><span class="sxs-lookup"><span data-stu-id="f32a0-110">3</span></span>          | <span data-ttu-id="f32a0-111">Specifica il numero di tipi di modifiche attualmente utilizzati da Gestione tabelle di routing.</span><span class="sxs-lookup"><span data-stu-id="f32a0-111">Specifies the number of change types that are currently used by the routing table manager.</span></span>                                                                            |
| <span data-ttu-id="f32a0-112">\_tipo di modifica RTM \_ \_ All</span><span class="sxs-lookup"><span data-stu-id="f32a0-112">RTM\_CHANGE\_TYPE\_ALL</span></span>           | <span data-ttu-id="f32a0-113">0x0001</span><span class="sxs-lookup"><span data-stu-id="f32a0-113">0x0001</span></span>     | <span data-ttu-id="f32a0-114">Notifica al client qualsiasi modifica a una destinazione.</span><span class="sxs-lookup"><span data-stu-id="f32a0-114">Notifies the client of any change to a destination.</span></span>                                                                                                                   |
| <span data-ttu-id="f32a0-115">\_tipo di modifica RTM \_ \_ migliore</span><span class="sxs-lookup"><span data-stu-id="f32a0-115">RTM\_CHANGE\_TYPE\_BEST</span></span>          | <span data-ttu-id="f32a0-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="f32a0-116">0x0002</span></span>     | <span data-ttu-id="f32a0-117">Notifica al client le modifiche apportate alla route migliore o quando viene modificata la route migliore.</span><span class="sxs-lookup"><span data-stu-id="f32a0-117">Notifies the client of changes to the best route, or when the best route changes.</span></span>                                                                                     |
| <span data-ttu-id="f32a0-118">\_avanzamento del \_ tipo di modifica RTM \_</span><span class="sxs-lookup"><span data-stu-id="f32a0-118">RTM\_CHANGE\_TYPE\_FORWARDING</span></span>    | <span data-ttu-id="f32a0-119">0x0004</span><span class="sxs-lookup"><span data-stu-id="f32a0-119">0x0004</span></span>     | <span data-ttu-id="f32a0-120">Notifica al client eventuali modifiche della route migliori che interessano l'inoltro, ad esempio le modifiche all'hop successivo.</span><span class="sxs-lookup"><span data-stu-id="f32a0-120">Notifies the client of any best route changes that affect forwarding (such as next hop changes).</span></span>                                                                      |
| <span data-ttu-id="f32a0-121">\_ \_ solo \_ \_ DestS contrassegnato per la notifica RTM</span><span class="sxs-lookup"><span data-stu-id="f32a0-121">RTM\_NOTIFY\_ONLY\_MARKED\_DESTS</span></span> | <span data-ttu-id="f32a0-122">0x00010000</span><span class="sxs-lookup"><span data-stu-id="f32a0-122">0x00010000</span></span> | <span data-ttu-id="f32a0-123">Notifica al client le modifiche apportate alle destinazioni contrassegnate dal client.</span><span class="sxs-lookup"><span data-stu-id="f32a0-123">Notifies the client of changes to destinations that the client has marked.</span></span> <span data-ttu-id="f32a0-124">Se questo flag non è specificato, vengono inviati i messaggi di notifica delle modifiche per tutte le destinazioni.</span><span class="sxs-lookup"><span data-stu-id="f32a0-124">If this flag is not specified, change notification messages for all destinations are sent.</span></span> |



 

 

 




