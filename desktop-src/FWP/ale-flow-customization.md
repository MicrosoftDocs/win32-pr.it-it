---
title: Personalizzazione Flow ale
description: I filtri di rete nei livelli Application Layer Enforcement (ALE) di Windows Filtering Platform (WFP) possono essere personalizzati aggiungendo filtri con opzioni di classificazione specifiche.
ms.assetid: 123af237-cf42-410b-8a2f-c011cb5f4f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe42a6df32bc69ba454226eb113cb43756224daaf752c3925f1f2d3bacd7650
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951370"
---
# <a name="ale-flow-customization"></a>Personalizzazione Flow ale

I filtri di rete nei livelli Application Layer Enforcement (ALE) di Windows Filtering Platform (WFP) possono essere personalizzati aggiungendo filtri con opzioni di classificazione specifiche.

## <a name="multicastbroadcast-traffic"></a>Traffico multicast/broadcast

Per bloccare il traffico in ingresso in base agli stati multicast o broadcast in uscita, aggiungere un filtro che autorizza il traffico multicast e broadcast in uscita e con l'opzione [**FWP \_ CLASSIFY \_ OPTION \_ MULTICAST \_ STATE**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) impostata su **FWP \_ OPTION VALUE \_ DENY \_ \_ MULTICAST \_ STATE**.

## <a name="remote-peers"></a>Peer remoti

Per aggiungere pacchetti di risposta da peer diversi allo stesso flusso ALE, aggiungere un filtro con l'opzione [**FWP \_ CLASSIFY \_ OPTION LOOSE SOURCE \_ \_ \_ MAPPING**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) impostata su **FWP OPTION VALUE ENABLE \_ LOOSE SOURCE \_ \_ \_ \_ \_ MAPPING**.

Per [l'esempio di codice, vedere](using-classify-options.md) Uso delle opzioni di classificazione.

## <a name="ale-flow-lifetime"></a>Durata Flow ale

Per modificare i valori di timeout di inattività per un flusso ALE, aggiungere un filtro con l'opzione [**FWP \_ CLASSIFY \_ OPTION \_ MCAST \_ BCAST \_ LIFETIME**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) e/o l'opzione **FWP \_ CLASSIFY \_ OPTION \_ UNICAST \_ LIFETIME** impostata sul valore di timeout di inattività desiderato.

Per [un esempio di codice, vedere Uso delle opzioni](using-classify-options.md) di classificazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazione a livello di applicazione (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Livelli ALE](ale-layers.md)
</dt> <dt>

[Filtro con stato ALE](ale-stateful-filtering.md)
</dt> <dt>

[Traffico multicast/broadcast ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Riautorizzazione ALE](ale-re-authorization.md)
</dt> <dt>

[Uso delle opzioni di classificazione](using-classify-options.md)
</dt> </dl>

 

 




