---
title: Recupero di informazioni
description: RTMv2 consente a un client di recuperare le informazioni a cui fa riferimento un determinato handle usando le funzioni RtmGetEntityInfo, RtmGetDestInfo, RtmGetRouteInfo e RtmGetNextHopInfo.
ms.assetid: a3fc2020-eac4-40a1-9a6e-6eaa2bcc582c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51958fccc8a07e8846705945d9210f4259dfd89b1e3cefccd65d57dd0f033757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028021"
---
# <a name="retrieving-information"></a>Recupero di informazioni

RTMv2 consente a un client di recuperare le informazioni a cui fa riferimento un determinato handle usando le funzioni [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)e [**RtmGetNextHopInfo.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo)

Queste chiamate di funzione hanno funzioni corrispondenti ([**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo), [**RtmReleaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)) per rilasciare gli handle associati alla struttura di informazioni restituita dal gestore tabelle di routing.

> [!Note]  
> Le informazioni per i client sono disponibili solo nell'istanza corrente e nella famiglia di indirizzi.

 

Per il codice di esempio che illustra come usare queste funzioni, vedere [Cercare la route migliore](search-for-the-best-route.md).

## <a name="using-rtmgetexactmatchroute-and-rtmgetexactmatchdestination"></a>Uso di RtmGetExactMatchRoute e RtmGetExactMatchDestination

Le [**funzioni RtmGetExactMatchRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) e [**RtmGetExactMatchDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) vengono usate dai client per trovare una route o una destinazione specifica. Queste funzioni risparmiano tempo eseguendo il lavoro di confronto per il client.

Ad esempio, quando RIP aggiorna una route, RIP deve mantenere le informazioni sulle metriche precedenti. RIP cerca la route e le relative informazioni. Rip può quindi copiare le informazioni e aggiornare la route.

## <a name="using-rtmgetmostspecificdestination"></a>Uso di RtmGetMostSpecificDestination

La [**funzione RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination) viene usata per individuare la destinazione più adatta al prefisso di rete specificato.

Ad esempio, il gestore di gruppi multicast usa questa funzione per eseguire un controllo RPF (Reverse Path Forwarding) su un singolo indirizzo. La funzione può essere usata anche per trovare l'hop successivo locale per un hop successivo remoto specificato.

Per il codice di esempio che illustra come usare queste funzioni, vedere [Cercare](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) route usando un albero dei prefissi e [Cercare la route migliore.](search-for-the-best-route.md)

## <a name="using-rtmgetlessspecificdestination"></a>Uso di RtmGetLessSpecificDestination

La [**funzione RtmGetLessSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination) viene usata per individuare la destinazione che rappresenta la corrispondenza migliore per il prefisso di rete specificato. Questa funzione può essere chiamata ripetutamente per restituire la successiva corrispondenza successiva meno specifica, fino a quando non vi sono più destinazioni corrispondenti.

Questa funzione viene chiamata dopo una chiamata a [**RtmGetMostSpecificDestination.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination)

Per il codice di esempio che illustra come usare queste funzioni, vedere [Cercare route tramite un albero dei prefissi](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md).

## <a name="using-rtmisbestroute"></a>Uso di RtmIsBestRoute

La [**funzione RtmIsBestRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute) consente a un client di determinare rapidamente se una route specifica è la route migliore per una destinazione. Ad esempio, un client potrebbe dover archiviare una route specifica solo se è la route migliore. Pertanto, il client può chiamare questa funzione, anziché enumerare tutte le route ed eseguire il confronto stesso.

 

 




