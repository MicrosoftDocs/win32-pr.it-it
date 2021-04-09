---
title: Gestione degli handle
description: Gestione tabelle di routing mantiene un conteggio dei riferimenti per tutte le informazioni che gestisce.
ms.assetid: bcd02881-b021-414f-8a40-14baac5baac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24653dd98db9b0427e5a3bee3f2f6613a68ce41
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955564"
---
# <a name="managing-handles"></a>Gestione degli handle

Gestione tabelle di routing mantiene un conteggio dei riferimenti per tutte le informazioni che gestisce. In questo modo si impedisce al gestore tabelle di routing di tornare a un client qualsiasi handle alla memoria che è stata liberata. Ogni volta che un handle viene restituito al chiamante, come handle esplicito o come parte di una struttura di informazioni, ad esempio [**le \_ \_ informazioni di destinazione RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_dest_info), il conteggio dei riferimenti per l'oggetto che corrisponde all'handle viene incrementato. Quando viene rilasciato l'handle o la struttura delle informazioni, il conteggio dei riferimenti appropriato viene decrementato. Quando il conteggio dei riferimenti diventa zero, l'oggetto viene liberato.

Le funzioni [**RtmGetDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo), [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) e [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) restituiscono strutture di informazioni. Queste funzioni corrispondono rispettivamente alle funzioni [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) e [**RtmRelaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo) .

> [!Note]  
> La funzione [**RtmReleaseChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasechangeddests) deve essere usata per rilasciare gli handle restituiti da una chiamata a [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests). Non usare [**RtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests) per le strutture di destinazione modificate.

 

Se un client deve contenere un handle specifico in una struttura di informazioni mentre rilascia il resto, il client può chiamare [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) con tale handle prima di rilasciare la struttura delle informazioni. L'handle può quindi essere rilasciato da una chiamata alle funzioni [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) e [**RtmRelaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo) .

 

 




