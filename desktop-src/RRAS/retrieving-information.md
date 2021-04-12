---
title: Recupero di informazioni
description: RTMv2 consente a un client di recuperare le informazioni a cui fa riferimento un determinato handle usando le funzioni RtmGetEntityInfo, RtmGetDestInfo, RtmGetRouteInfo e RtmGetNextHopInfo.
ms.assetid: a3fc2020-eac4-40a1-9a6e-6eaa2bcc582c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058a87c9463011aec55b0c6c8c0574ff1e013f23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221026"
---
# <a name="retrieving-information"></a>Recupero di informazioni

RTMv2 consente a un client di recuperare le informazioni a cui fa riferimento un determinato handle usando le funzioni [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)e [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) .

Queste chiamate di funzione hanno funzioni corrispondenti ([**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo), [**RtmReleaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)) per rilasciare gli handle associati alla struttura di informazioni restituita da Gestione tabelle di routing.

> [!Note]  
> Le informazioni per i client sono disponibili solo nell'istanza corrente e nella famiglia di indirizzi.

 

Per il codice di esempio che illustra come usare queste funzioni, vedere [cercare la route migliore](search-for-the-best-route.md).

## <a name="using-rtmgetexactmatchroute-and-rtmgetexactmatchdestination"></a>Uso di RtmGetExactMatchRoute e RtmGetExactMatchDestination

Le funzioni [**RtmGetExactMatchRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) e [**RtmGetExactMatchDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) vengono usate dai client per trovare una route o una destinazione specifica. Queste funzioni risparmiano tempo eseguendo le operazioni di confronto per il client.

Ad esempio, quando RIP Aggiorna una route, RIP deve conservare le informazioni della metrica obsolete. RIP cerca la route e le relative informazioni. Quindi, RIP può copiare le informazioni e aggiornare la route.

## <a name="using-rtmgetmostspecificdestination"></a>Uso di RtmGetMostSpecificDestination

La funzione [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination) viene usata per individuare la destinazione che corrisponde maggiormente al prefisso di rete specificato.

Ad esempio, il gestore del gruppo multicast usa questa funzione per eseguire un controllo RPF (Reverse-Path-inoltring) su un singolo indirizzo. La funzione può essere usata anche per trovare l'hop successivo locale per un determinato hop successivo remoto.

Per il codice di esempio che illustra come usare queste funzioni, vedere [cercare le route usando un albero del prefisso](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) e [cercare la route migliore](search-for-the-best-route.md).

## <a name="using-rtmgetlessspecificdestination"></a>Uso di RtmGetLessSpecificDestination

La funzione [**RtmGetLessSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination) viene usata per individuare la destinazione che rappresenta la corrispondenza migliore successiva per il prefisso di rete specificato. Questa funzione può essere chiamata ripetutamente per restituire la successiva corrispondenza meno specifica successiva, fino a quando non sono presenti altre destinazioni corrispondenti.

Questa funzione viene chiamata dopo una chiamata a [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination).

Per il codice di esempio che illustra come usare queste funzioni, vedere [cercare le route usando un albero del prefisso](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md).

## <a name="using-rtmisbestroute"></a>Uso di RtmIsBestRoute

La funzione [**RtmIsBestRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute) consente a un client di determinare rapidamente se una determinata route è la migliore route a una destinazione. Ad esempio, un client potrebbe dover archiviare una route specifica solo se è la route migliore. Pertanto, il client può chiamare questa funzione, invece di enumerare tutte le route e di eseguire il confronto.

 

 




