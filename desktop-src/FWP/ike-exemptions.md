---
title: Esenzioni IKE/AuthIP
description: Per il funzionamento Exchange internet key Exchange (IKE) e Authenticated Internet Protocol (AuthIP), è necessario esentare il traffico di rete dal filtro IPsec.
ms.assetid: 365bfebc-250a-440f-8056-ff9601daa030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2963c804c6bd63f191563566bcc99dcf9f0f4a74bb2c844a402adc856dbad3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069061"
---
# <a name="ikeauthip-exemptions"></a>Esenzioni IKE/AuthIP

I moduli di keying IPsec (Internet Protocol Security), IKE (Internet Key Exchange) e Authenticated Internet Protocol (AuthIP), per funzionare, devono esentare il traffico di rete dal filtro IPsec.

In Windows Filtering Platform (WFP) il Base Filtering Engine (BFE) aggiunge automaticamente i filtri di esenzione IKE e AuthIP quando viene aggiunto il primo filtro dei criteri IKE o AuthIP in modalità principale (MM) e li elimina quando viene eliminato l'ultimo filtro criteri IKE o AuthIP MM. In questo modo, i provider di criteri non devono gestire singolarmente le esenzioni di filtro IKE e AuthIP.

Un filtro dei criteri IKE MM è un filtro nel livello del motore [**FWPM \_ LAYER \_ IKEEXT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) che fa riferimento a un contesto del provider di tipo [**FWPM \_ IPSEC \_ IKE \_ MM \_ CONTEXT**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).

Un filtro criteri AuthIP MM è un filtro nel livello del motore [**FWPM \_ LAYER \_ IKEEXT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) che fa riferimento a un contesto del provider di tipo [**FWPM \_ IPSEC \_ AUTHIP \_ MM \_ CONTEXT**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).

Un filtro di esenzione IKE o AuthIP è un filtro nel livello del motore [**FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V{4 \| 6}**](management-filtering-layer-identifiers-.md) o **FWPM \_ LAYER OUTBOUND TRANSPORT \_ \_ \_ V{4 \| 6}** ponderato automaticamente nell'intervallo di peso [**FWPM \_ WEIGHT RANGE \_ \_ IKE \_ EXEMPTIONS.**](filter-weight-identifiers.md)

Le esenzioni IKE e AuthIP implementate da BFE sono le seguenti.

| Versione IP      | Porta                        | Esenzione                                                                                                                                                                                                                             |
|-----------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IPv4<br/> | UDP:500 UDP:4500<br/> | Consentire il traffico IKE e AuthIP a livello di trasporto in ingresso e a livello di trasporto in uscita. <br/> Consentire il traffico IKE e AuthIP ai livelli di ricezione/accettazione e connessione dell'ale, ma limitarlo al sistema locale.<br/> |
| IPv6<br/> | UDP:500<br/>          | Consentire il traffico IKE e AuthIP a livello di trasporto in ingresso e a livello di trasporto in uscita. <br/> Consentire il traffico IKE e AuthIP ai livelli di ricezione/accettazione e connessione dell'ale, ma limitarlo al sistema locale.<br/> |



 

I filtri di esenzione IKE e AuthIP sono aperti a tutti gli indirizzi. Per implementare un firewall con un controllo più granulare, i provider di criteri devono aggiungere filtri in un intervallo di peso superiore a [**FWPM \_ WEIGHT \_ RANGE \_ IKE \_ EXEMPTIONS**](filter-weight-identifiers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione IPsec](ipsec-configuration.md)
</dt> <dt>

[Assegnazione di pesi dei filtri](filter-weight-assignment.md)
</dt> </dl>

 

 





