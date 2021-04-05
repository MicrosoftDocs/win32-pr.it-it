---
title: Destinazioni
description: Una destinazione nella tabella di routing è una voce di rete rappresentata da un indirizzo di rete e un network mask.
ms.assetid: 115d86e3-f933-4601-af10-abaab287b509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c0c758720824284147c2f35be004622157edb3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856278"
---
# <a name="destinations"></a><span data-ttu-id="51dbc-103">Destinazioni</span><span class="sxs-lookup"><span data-stu-id="51dbc-103">Destinations</span></span>

<span data-ttu-id="51dbc-104">Una destinazione nella tabella di routing è una voce di rete rappresentata da un indirizzo di rete e un network mask.</span><span class="sxs-lookup"><span data-stu-id="51dbc-104">A destination in the routing table is a network entry represented by a network address and a network mask.</span></span>

<span data-ttu-id="51dbc-105">Una voce di destinazione nella tabella di routing include:</span><span class="sxs-lookup"><span data-stu-id="51dbc-105">A destination entry in the routing table includes:</span></span>

-   <span data-ttu-id="51dbc-106">Indirizzo, espresso come indirizzo di rete e network mask.</span><span class="sxs-lookup"><span data-stu-id="51dbc-106">The address, expressed as a network address and network mask.</span></span>
-   <span data-ttu-id="51dbc-107">Elenco di route per la destinazione.</span><span class="sxs-lookup"><span data-stu-id="51dbc-107">A list of routes to the destination.</span></span>
-   <span data-ttu-id="51dbc-108">Elenco di slot del puntatore opaco.</span><span class="sxs-lookup"><span data-stu-id="51dbc-108">A list of opaque pointer slots.</span></span>
-   <span data-ttu-id="51dbc-109">Visualizzazioni in cui questa destinazione è valida.</span><span class="sxs-lookup"><span data-stu-id="51dbc-109">The views in which this destination is valid.</span></span> <span data-ttu-id="51dbc-110">La destinazione contiene una struttura per ogni visualizzazione che contiene le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="51dbc-110">The destination contains a structure for each view that contains the following information:</span></span>
    -   <span data-ttu-id="51dbc-111">Identificatore per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="51dbc-111">An identifier for the view.</span></span>
    -   <span data-ttu-id="51dbc-112">Puntatore al percorso migliore della destinazione in questa visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="51dbc-112">A pointer to the best route to the destination in this view.</span></span>
    -   <span data-ttu-id="51dbc-113">Proprietario della route migliore in questa visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="51dbc-113">The owner of the best route in this view.</span></span>
    -   <span data-ttu-id="51dbc-114">Flag associati alla route migliore in questa visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="51dbc-114">Flags associated with the best route in this view.</span></span>
    -   <span data-ttu-id="51dbc-115">Handle per tutte le route in uno stato di attesa in questa visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="51dbc-115">Handle to any routes that are in a hold-down state in this view.</span></span>

 

 




