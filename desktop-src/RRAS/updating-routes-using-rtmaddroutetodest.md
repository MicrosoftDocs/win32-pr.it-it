---
title: Aggiornamento di route con RtmAddRouteToDest
description: Se il client non richiede efficienza durante l'aggiunta di una route, deve usare il metodo seguente per aggiornare le route.
ms.assetid: bfa914ea-5d54-4ce9-a97c-903c497d135b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c7972b2d5ec0996cafc1dd32a8a4056a6aeb0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955749"
---
# <a name="updating-routes-using-rtmaddroutetodest"></a>Aggiornamento di route con RtmAddRouteToDest

Se il client non richiede efficienza durante l'aggiunta di una route, deve usare il metodo seguente per aggiornare le route. Questo metodo è meno efficiente poiché richiede l'ottenimento di un handle per la route e il passaggio della struttura delle [**\_ \_ informazioni sulla route RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) da e verso gestione tabelle di routing. Questo metodo richiede inoltre più tempo. Poiché [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) non modifica direttamente la tabella di routing, l'utilizzo di questo metodo consente di rendere più semplice l'efficienza.

Per il codice di esempio che illustra come usare queste funzioni, vedere [aggiungere e aggiornare le route con RtmAddRouteToDest](add-and-update-routes-using-rtmaddroutetodest.md).

 

 




