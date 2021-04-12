---
title: Esenzioni IKE/AuthIP
description: Protocollo IKE (IKE) e Authenticated Internet Protocol (AuthIP), per funzionare, è necessario esentare il traffico di rete dal filtro IPsec.
ms.assetid: 365bfebc-250a-440f-8056-ff9601daa030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58a6d00ddd337d56c3c00a34b6949213be6ee26
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104398636"
---
# <a name="ikeauthip-exemptions"></a>Esenzioni IKE/AuthIP

I moduli di chiave Internet Protocol Security (IPsec), protocollo IKE (IKE) e Authenticated Internet Protocol (AuthIP), per funzionare, devono esentare il traffico di rete dal filtro IPsec.

In Windows Filtering Platform (WFP) il motore di filtro di base (BFE) aggiunge automaticamente i filtri di esenzione IKE e AuthIP quando viene aggiunto il primo filtro dei criteri della modalità principale IKE o AuthIP e li elimina quando viene eliminato l'ultimo filtro dei criteri IKE o AuthIP MM. In questo modo, i provider di criteri non devono gestire singolarmente le esenzioni di filtro IKE e AuthIP.

Un filtro dei criteri IKE MM è un filtro nel livello [**FWPM \_ livello motore \_ IKEEXT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) che fa riferimento a un contesto del provider di tipo [**FWPM \_ IPSec \_ IKE \_ mm \_ context**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).

Un filtro dei criteri AuthIP MM è un filtro nel livello del motore [**FWPM \_ livello \_ IKEEXT \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) che fa riferimento a un contesto del provider di tipo FWPM il [**\_ \_ \_ \_ contesto di AuthIP mm di IPSec**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type).

Un filtro di esenzione IKE o AuthIP è un filtro nel livello motore [**FWPM \_ del \_ trasporto in \_ ingresso \_ v {4 \| 6}**](management-filtering-layer-identifiers-.md) o **FWPM \_ Layer in \_ uscita del \_ trasporto \_ v {4 \| 6}** ponderato in modo automatico nell'intervallo di ponderazione del FWPM di [**\_ ponderazione \_ \_ IKE \_**](filter-weight-identifiers.md) .

Di seguito sono riportate le esenzioni IKE e AuthIP implementate da BFE.

| Versione IP      | Porta                        | Esenzione                                                                                                                                                                                                                             |
|-----------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IPv4<br/> | UDP: 500 UDP: 4500<br/> | Consentire il traffico IKE e AuthIP al livello di trasporto in ingresso e al livello di trasporto in uscita. <br/> Consentire il traffico IKE e AuthIP ai livelli di ricezione/accettazione e connessione di ALE, ma limitarlo al sistema locale.<br/> |
| IPv6<br/> | UDP: 500<br/>          | Consentire il traffico IKE e AuthIP al livello di trasporto in ingresso e al livello di trasporto in uscita. <br/> Consentire il traffico IKE e AuthIP ai livelli di ricezione/accettazione e connessione di ALE, ma limitarlo al sistema locale.<br/> |



 

I filtri di esenzione IKE e AuthIP sono aperti a tutti gli indirizzi. Per implementare un firewall con un controllo più granulare, i provider di criteri devono aggiungere filtri in un intervallo di ponderazione superiore alle [**\_ \_ \_ \_ esenzioni IKE dell'intervallo di FWPM ponderato**](filter-weight-identifiers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione IPsec](ipsec-configuration.md)
</dt> <dt>

[Assegnazione di pesi dei filtri](filter-weight-assignment.md)
</dt> </dl>

 

 





