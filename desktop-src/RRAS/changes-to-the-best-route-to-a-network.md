---
title: Modifiche alla route migliore a una rete
description: Una modifica apportata a uno dei valori seguenti per la route migliore a una determinata rete di destinazione determina la generazione di un messaggio di notifica inviato a ogni client registrato e ai server d'inoltro.
ms.assetid: 2864af0f-e05a-48d7-a78d-57cc9ac42246
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35b8c43483dbd69f5407f9859d5943e515e8825d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298623"
---
# <a name="changes-to-the-best-route-to-a-network"></a><span data-ttu-id="03d31-103">Modifiche alla route migliore a una rete</span><span class="sxs-lookup"><span data-stu-id="03d31-103">Changes to the Best Route to a Network</span></span>

<span data-ttu-id="03d31-104">**Windows Server 2003:** Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="03d31-104">**Windows Server 2003:** This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="03d31-105">Le nuove applicazioni devono usare l'API di Routing Table Manager versione 2.</span><span class="sxs-lookup"><span data-stu-id="03d31-105">New applications should use the Routing Table Manager Version 2 API.</span></span>

<span data-ttu-id="03d31-106">Una modifica apportata a uno dei valori seguenti per la route migliore a una determinata rete di destinazione determina la generazione di un messaggio di notifica inviato a ogni client registrato e ai server d'inoltro:</span><span class="sxs-lookup"><span data-stu-id="03d31-106">A change in any of the following values for the best route to a given destination network causes the routing table manager to generate a notification message sent to each registered client and to the forwarders:</span></span>

-   <span data-ttu-id="03d31-107">Identificatore di protocollo</span><span class="sxs-lookup"><span data-stu-id="03d31-107">Protocol identifier</span></span>
-   <span data-ttu-id="03d31-108">Indice dell'interfaccia</span><span class="sxs-lookup"><span data-stu-id="03d31-108">Interface index</span></span>
-   <span data-ttu-id="03d31-109">Indirizzo del router hop successivo</span><span class="sxs-lookup"><span data-stu-id="03d31-109">Address of next-hop router</span></span>
-   <span data-ttu-id="03d31-110">Dati specifici della famiglia di protocolli che includono metriche di route</span><span class="sxs-lookup"><span data-stu-id="03d31-110">Protocol family-specific data that includes route metrics</span></span>

<span data-ttu-id="03d31-111">Una modifica nell'identificatore del protocollo, nell'indice dell'interfaccia o nell'indirizzo del router di hop successivo si verifica quando viene aggiunta una nuova voce di route migliore o quando la voce di route migliore corrente viene eliminata o obsoleta e lascia un'altra route come nuova route migliore.</span><span class="sxs-lookup"><span data-stu-id="03d31-111">A change in protocol identifier, interface index, or next-hop router address occurs when a new, better-route entry is added, or when the current best-route entry is deleted or aged out, and leaves another route as the new best route.</span></span>

 

 




