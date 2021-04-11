---
title: Istanza di gestione tabelle di routing
description: Un'istanza è una tabella separata utilizzata da Gestione tabelle di routing per mantenere le informazioni di routing su un subset di interfacce.
ms.assetid: a17233fc-2c40-4d00-8a6b-86f08fef5690
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d209f254bb9111c786bde6635b43895604785d5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044616"
---
# <a name="routing-table-manager-instance"></a><span data-ttu-id="a5b1b-103">Istanza di gestione tabelle di routing</span><span class="sxs-lookup"><span data-stu-id="a5b1b-103">Routing Table Manager Instance</span></span>

<span data-ttu-id="a5b1b-104">Un'istanza è una tabella separata utilizzata da Gestione tabelle di routing per mantenere le informazioni di routing su un subset di interfacce.</span><span class="sxs-lookup"><span data-stu-id="a5b1b-104">An instance is a separate table that the routing table manager uses to maintain routing information about a subset of interfaces.</span></span> <span data-ttu-id="a5b1b-105">Le istanze vengono in genere utilizzate per consentire a un router fisico di fungere da un set di router virtuali, ovvero un router virtuale per ogni rete logica.</span><span class="sxs-lookup"><span data-stu-id="a5b1b-105">Instances are typically used to enable a physical router to act as a set of virtual routers – one virtual router per logical network.</span></span>

<span data-ttu-id="a5b1b-106">Attualmente, gestione tabelle di routing supporta solo un'istanza (identificata come zero, l'impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="a5b1b-106">Currently, the routing table manager supports only one instance (identified as zero, the default).</span></span> <span data-ttu-id="a5b1b-107">Il client può eseguire la registrazione con altre istanze, ma nessun router virtuale, eccetto quello predefinito, viene riconosciuto o utilizzato da Gestione router.</span><span class="sxs-lookup"><span data-stu-id="a5b1b-107">The client can register with other instances, but no virtual router except the default one is recognized or used by the router manager.</span></span>

 

 




