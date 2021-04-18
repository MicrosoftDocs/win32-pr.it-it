---
title: Personalizzazione del flusso di ALE
description: È possibile personalizzare il filtro di rete a livello di applicazione dei livelli di applicazione (ALE) di Windows Filtering Platform (PAM) aggiungendo filtri con opzioni di classificazione specifiche.
ms.assetid: 123af237-cf42-410b-8a2f-c011cb5f4f19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9843a60719f424403139885f24f165c0dd936b
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104336450"
---
# <a name="ale-flow-customization"></a>Personalizzazione del flusso di ALE

È possibile personalizzare il filtro di rete a livello di applicazione dei livelli di applicazione (ALE) di Windows Filtering Platform (PAM) aggiungendo filtri con opzioni di classificazione specifiche.

## <a name="multicastbroadcast-traffic"></a>Traffico multicast/broadcast

Per bloccare il traffico in ingresso in base a stati broadcast o multicast in uscita, aggiungere un filtro che autorizza il multicast in uscita e il traffico broadcast e con l'opzione [**FWP \_ classificate \_ option \_ multicast \_ state**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) impostata sul **\_ valore FWP opzione \_ \_ Deny \_ multicast \_ state**.

## <a name="remote-peers"></a>Peer remoti

Per aggiungere pacchetti di risposta da peer diversi allo stesso flusso di ALE, aggiungere un filtro con l'opzione [**FWP \_ classificate \_ \_ Loose \_ source \_ mapping**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) opzione impostata su **FWP \_ opzione \_ \_ Abilita il \_ \_ \_ mapping del codice sorgente libero**.

Per un esempio di codice, vedere [utilizzo delle opzioni classifica](using-classify-options.md) .

## <a name="ale-flow-lifetime"></a>Durata del flusso ALE

Per modificare i valori di timeout di inattività per un flusso di ALE, aggiungere un filtro con l'opzione [**FWP \_ classificate option \_ \_ mcast \_ gettati \_ durata**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_classify_option0) e/o l'opzione di **\_ classificazione \_ \_ unicast \_ per la durata dell'opzione FWP classificate** sul valore di timeout di inattività desiderato.

Vedere [uso delle opzioni di classificazione](using-classify-options.md) per un esempio di codice.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Application Layer Enforcement (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Livelli ALE](ale-layers.md)
</dt> <dt>

[Filtro con stato ALE](ale-stateful-filtering.md)
</dt> <dt>

[Traffico di broadcast/multicast ALE](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[Riautorizzazione ALE](ale-re-authorization.md)
</dt> <dt>

[Uso delle opzioni di classificazione](using-classify-options.md)
</dt> </dl>

 

 




