---
title: Traffico multicast/broadcast ALE
description: Tutto il traffico multicast e broadcast in ingresso ai livelli application layer enforcement (ALE) viene mappato a un flusso alE globale.
ms.assetid: b10b9758-8fce-4256-a25d-917e01336456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2849f7277cc9ada580bca22fa5a4fdf618d959d255b442607963047dd2a37bba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315611"
---
# <a name="ale-multicastbroadcast-traffic"></a>Traffico multicast/broadcast ALE

Tutto il traffico multicast e broadcast in ingresso ai livelli application layer enforcement (ALE) viene mappato a un flusso [ALE globale.](ale-stateful-filtering.md) Il traffico di risposta per i pacchetti multicast e broadcast in ingresso viene classificato al livello [**FWPM \_ LAYER \_ ALE \_ AUTH \_ CONNECT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) e per ogni risposta vengono creati flussi ALE separati.

Il traffico multicast e broadcast in uscita ai livelli ALE crea un flusso ALE di 4 secondi. Per impostazione predefinita, l'autorizzazione di un pacchetto ALE multicast o broadcast in uscita consente il traffico in ingresso, che sia unicast, multicast o broadcast, da qualsiasi indirizzo remoto per un massimo di 4 secondi. Tale flusso ALE può essere aggiornato o mantenuto attivo solo dal traffico in uscita successivo che corrisponde al flusso ALE.

> [!Note]  
> La durata di 4 secondi viene specificata dal callout [**predefinito FWPM \_ CALLOUT \_ SET OPTIONS \_ \_ AUTH CONNECT LAYER \_ \_ \_ V{4 \| 6}**](built-in-callout-identifiers.md). Per modificare la durata predefinita di 4 secondi, aggiungere un filtro che faccia riferimento al callout **FWPM \_ CALLOUT \_ SET OPTIONS \_ \_ AUTH CONNECT LAYER \_ \_ \_ V{4 \| 6}.** Per [altre informazioni, Flow ale.](ale-flow-customization.md)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazione del livello applicazione (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Livelli ALE](ale-layers.md)
</dt> <dt>

[Filtro con stato ALE](ale-stateful-filtering.md)
</dt> <dt>

[Riautorizzazione ALE](ale-re-authorization.md)
</dt> <dt>

[Personalizzazione dei Flow ale](ale-flow-customization.md)
</dt> </dl>

 

 




