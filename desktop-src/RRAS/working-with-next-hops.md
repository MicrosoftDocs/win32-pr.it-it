---
title: Uso degli hop successivi
description: L'API RTMv2 consente ai client di usare l'elenco degli hop successivi associati a route e destinazioni.
ms.assetid: ef474091-48fe-48e5-b476-73d77dbcbec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f629bb5f43298c2cada3759ea3ab9c7bb71f0ca47a3c4158028d923646662c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024711"
---
# <a name="working-with-next-hops"></a>Uso degli hop successivi

L'API RTMv2 consente ai client di usare l'elenco degli hop successivi associati a route e destinazioni. I client possono aggiungere o aggiornare un hop successivo chiamando [**RtmAddNextHop.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop) I client possono eliminare un hop successivo [**usando RtmDeleteNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop). I client possono cercare hop successivi chiamando [**RtmFindNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop).

I client possono anche aggiornare direttamente l'hop successivo. A tale scopo, il client deve prima bloccare l'hop successivo con [**la funzione RtmLockNextHop.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop) Il client può quindi usare il puntatore diretto alla struttura [**RTM \_ NEXTHOP \_ INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) del gestore tabelle di routing per apportare le modifiche necessarie. Infine, il client può sbloccare l'hop successivo.

> [!Note]  
> I campi indirizzo hop successivo e indice dell'interfaccia nell'hop successivo identificano in modo univoco l'hop successivo e non devono essere modificati.

 

 

 




