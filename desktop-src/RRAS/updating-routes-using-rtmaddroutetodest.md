---
title: Aggiornamento delle route tramite RtmAddRouteToDest
description: Se il client non richiede efficienza durante l'aggiunta di una route, deve usare il metodo di aggiornamento delle route seguente.
ms.assetid: bfa914ea-5d54-4ce9-a97c-903c497d135b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3212a74637fa4de51f3b05f80f84bace1c0c57ba570e5025adb796da933b24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025331"
---
# <a name="updating-routes-using-rtmaddroutetodest"></a>Aggiornamento delle route tramite RtmAddRouteToDest

Se il client non richiede efficienza durante l'aggiunta di una route, deve usare il metodo di aggiornamento delle route seguente. Questo metodo è meno efficiente perché richiede l'acquisizione di un handle per la route e il passaggio della struttura [**RTM \_ ROUTE \_ INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) da e verso il gestore tabelle di routing. Questo metodo richiede anche più tempo. Poiché [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) non modifica direttamente la tabella di routing, l'uso di questo metodo commercia l'efficienza per semplicità.

Per il codice di esempio che illustra come usare queste funzioni, vedere Aggiungere e [aggiornare route tramite RtmAddRouteToDest.](add-and-update-routes-using-rtmaddroutetodest.md)

 

 




