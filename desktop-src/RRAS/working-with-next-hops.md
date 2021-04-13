---
title: Utilizzo degli hop successivi
description: L'API RTMv2 consente ai client di usare l'elenco degli hop successivi associati alle route e alle destinazioni.
ms.assetid: ef474091-48fe-48e5-b476-73d77dbcbec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d20a812fd272afafd2cd8eb1d6fb93d97530a2a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396723"
---
# <a name="working-with-next-hops"></a>Utilizzo degli hop successivi

L'API RTMv2 consente ai client di usare l'elenco degli hop successivi associati alle route e alle destinazioni. I client possono aggiungere o aggiornare un hop successivo chiamando [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop). I client possono eliminare un hop successivo usando [**RtmDeleteNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop). I client possono cercare hop successivi chiamando [**RtmFindNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop).

I client possono anche aggiornare direttamente l'hop successivo. A tale scopo, il client deve prima bloccare l'hop successivo con la funzione [**RtmLockNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop) . Il client può quindi utilizzare il puntatore diretto alla struttura delle [**\_ \_ informazioni RTM NEXTHOP**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) di gestione tabelle di routing per apportare le modifiche necessarie. Infine, il client può sbloccare l'hop successivo.

> [!Note]  
> I campi indirizzo hop successivo e indice interfaccia nell'hop successivo identificano in modo univoco l'hop successivo e non devono essere modificati.

 

 

 




