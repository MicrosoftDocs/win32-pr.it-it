---
title: Traffico di broadcast/multicast ALE
description: Viene eseguito il mapping di tutto il traffico in ingresso multicast e broadcast a livello di applicazione (ALE) a un flusso di ALE globale.
ms.assetid: b10b9758-8fce-4256-a25d-917e01336456
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30b56a6e2a27a209baf66d34948b704ae321644
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329708"
---
# <a name="ale-multicastbroadcast-traffic"></a>Traffico di broadcast/multicast ALE

Viene eseguito il mapping di tutto il traffico in ingresso multicast e broadcast a livello di applicazione (ALE) a un [flusso di ale](ale-stateful-filtering.md)globale. Il traffico di risposta per i pacchetti multicast e broadcast in ingresso è Classificato al livello [**FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) e vengono creati flussi ale distinti per ogni risposta.

Il traffico multicast e broadcast in uscita a livello di ALE crea un flusso ALE di 4 secondi. Per impostazione predefinita, l'autorizzazione di un pacchetto multicast o broadcast in uscita consentirà il traffico in ingresso, sia unicast, multicast o broadcast, da qualsiasi indirizzo remoto per un massimo di 4 secondi. Questo flusso di ALE può essere aggiornato o mantenuto attivo solo dal traffico in uscita successivo corrispondente al flusso ALE.

> [!Note]  
> Il ciclo di vita di 4 secondi viene specificato dalle opzioni di callout FWPM del callout predefinite di [**\_ \_ \_ \_ auth \_ Connect \_ Layer \_ V {4 \| 6}**](built-in-callout-identifiers.md). Per modificare la durata predefinita di 4 secondi, aggiungere un filtro che faccia riferimento **alle \_ Opzioni del set di callout FWPM autenticazione di \_ \_ \_ \_ \_ livello \_ V {4 \| 6}** callout. Per ulteriori informazioni, vedere [personalizzazione del flusso di ale](ale-flow-customization.md) .

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Application Layer Enforcement (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[Livelli ALE](ale-layers.md)
</dt> <dt>

[Filtro con stato ALE](ale-stateful-filtering.md)
</dt> <dt>

[Riautorizzazione ALE](ale-re-authorization.md)
</dt> <dt>

[Personalizzazione del flusso di ALE](ale-flow-customization.md)
</dt> </dl>

 

 




