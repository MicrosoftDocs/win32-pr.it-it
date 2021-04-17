---
title: Modalità di trasporto individuazione negoziazione in modalità limite
description: La modalità trasporto per l'individuazione della negoziazione in modalità limite IPsec richiede la protezione della modalità trasporto IPsec per tutto il traffico corrispondente.
ms.assetid: 36ae74b3-30f5-49bd-8855-6f3c0fb04d70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9f4168eee38165125c2455bc80dae29c1c6794
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473083"
---
# <a name="negotiation-discovery-transport-mode-in-boundary-mode"></a>Modalità di trasporto individuazione negoziazione in modalità limite

La modalità trasporto per l'individuazione della negoziazione in modalità limite IPsec richiede la protezione della modalità trasporto IPsec per tutto il traffico corrispondente. Se la negoziazione IKE/AuthIP ha esito negativo, le connessioni in ingresso e in uscita possono eseguire il fallback a testo non crittografato.

Questo criterio IPsec viene in genere usato nei computer a cui è possibile accedere sia da computer che supportano IPsec che da computer non IPsec.

Un esempio di scenario della modalità di trasporto per l'individuazione delle negoziazioni è "proteggere tutto il traffico dati unicast, tranne ICMP, usando la modalità di trasporto IPsec e abilitare l'individuazione della negoziazione in modalità limite".

Per implementare questo esempio a livello di codice, utilizzare la seguente configurazione di Pam.

<dl>

**Ai \_ criteri di negoziazione FWPM layer \_ IKEEXT \_ V {4 \| 6} Setup mm**  

1.  Aggiungere uno o entrambi i contesti di provider di criteri MM seguenti.  
    -   Per IKE, un contesto del provider di criteri di tipo FWPM \_ IPSec \_ IKE \_ mm \_ context.
    -   Per AuthIP, un contesto del provider di criteri di tipo FWPM \_ IPSec \_ AuthIP \_ mm \_ context.

    > [!Note]  
    > Verrà negoziato un modulo di trasparenza comune e verranno applicati i criteri di MM corrispondenti. AuthIP è il modulo di chiavi preferito se sono supportati sia IKE che AuthIP.

     

2.  Per ognuno dei contesti aggiunti nel passaggio 1, aggiungere un filtro con le proprietà seguenti.
    | Filter (proprietà)        | Valore                                            |
    |------------------------|--------------------------------------------------|
    | Condizioni di filtro   | Vuoto. Tutto il traffico corrisponderà al filtro.        |
    | **providerContextKey** | GUID del contesto del provider MM aggiunto nel passaggio 1. |

        

**A FWPM \_ Layer \_ IPSec \_ V {4 \| 6} installazione di QM e criteri di negoziazione em**  

1.  Aggiungere uno o entrambi i contesti del provider di criteri per la modalità trasporto QM seguenti e impostare il flag del [**\_ criterio IPSec \_ \_ ND \_ limite**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) .  
    -   Per IKE, un contesto del provider di criteri di tipo **FWPM \_ IPSec \_ IKE \_ \_ trasporto \_ context**.
    -   Per AuthIP, un contesto del provider di criteri di tipo **FWPM \_ IPSec \_ AuthIP \_ mq \_ \_ context**. Questo contesto può facoltativamente contenere i criteri di negoziazione della modalità estesa AuthIP (EM).

    > [!Note]  
    > Verrà negoziato un modulo di trasparenza comune e verranno applicati i criteri di QM corrispondenti. AuthIP è il modulo di chiavi preferito se sono supportati sia IKE che AuthIP.

     

2.  Per ognuno dei contesti aggiunti nel passaggio 1, aggiungere un filtro con le proprietà seguenti.
    | Filter (proprietà)        | Valore                                            |
    |------------------------|--------------------------------------------------|
    | Condizioni di filtro   | Vuoto. Tutto il traffico corrisponderà al filtro.        |
    | **providerContextKey** | GUID del contesto del provider QM aggiunto nel passaggio 1. |

        

**Al \_ trasporto in ingresso FWPM layer \_ \_ \_ V {4 \| 6} Configurare le regole di filtro in ingresso per pacchetto**  

1.  Aggiungere un filtro con le proprietà seguenti. 
    | Filter (proprietà)                                                   | Valore                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | **FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione** | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | **Action. Type**                                                   | **\_ \_ terminazione CALLOUT azione FWP \_**                                                              |
    | **Action. calloutKey**                                             | **\_Trasporto in \_ ingresso IPSec di CALLOUT FWPM \_ \_ \_ V {4 \| 6}**                                              |
    | **rawContext**                                                    | [**sicurezza della connessione per il \_ \_ \_ \_ salvataggio permanente in ingresso IPSec \_ del contesto FWPM \_**](filter-context-identifiers.md) |

        
2.  Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.
    | Filter (proprietà)                                                   | Valore                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione** | NlatUnicast                                                                |
    | **FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**             | **IPPROTO \_ ICMP {V6}** queste costanti sono definite in Winsock2. h.<br/> |
    | **Action. Type**                                                   | \_permesso azione \_ FWP                                                        |
    | **weight**                                                        | [**\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**](filter-weight-identifiers.md)  |

        

**Al \_ trasporto in uscita FWPM layer \_ \_ \_ V {4 \| 6} Configurare le regole di filtro in uscita per pacchetto**  

1.  Aggiungere un filtro con le proprietà seguenti.
    | Filter (proprietà)                                                   | Valore                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | **FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione** | NlatUnicast                                                                               |
    | **Action. Type**                                                   | **\_ \_ terminazione CALLOUT azione FWP \_**                                                     |
    | **Action. calloutKey**                                             | **\_Trasporto in \_ uscita IPSec di CALLOUT FWPM \_ \_ \_ V {4 \| 6}**                                    |
    | **rawContext**                                                    | [**\_ \_ \_ \_ individuazione negoziazioni in uscita IPSec del contesto FWPM \_**](filter-context-identifiers.md) |

        
2.  Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.
    | Filter (proprietà)                                                   | Valore                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione** | NlatUnicast                                                                |
    | **FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**             | **IPPROTO \_ ICMP {V6}** queste costanti sono definite in Winsock2. h.<br/> |
    | **Action. Type**                                                   | **\_permesso azione \_ FWP**                                                    |
    | **weight**                                                        | **\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**                                   |

        

</dl>

> [!Note]  
> A differenza della modalità di trasporto per l'individuazione della negoziazione, per la modalità di trasporto di individuazione della negoziazione nei criteri della modalità limite non è necessario aggiungere un filtro a **livello di FWPM \_ livello \_ ale \_ \_ ricezione \_ accetta \_ V {4 \| 6}** livelli perché questo criterio consente connessioni non protette in ingresso non protette.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codice di esempio: utilizzo della modalità di trasporto](using-transport-mode.md)
</dt> <dt>

[Livelli ALE](ale-layers.md)
</dt> <dt>

[**Identificatori di callout predefiniti**](built-in-callout-identifiers.md)
</dt> <dt>

[Condizioni di filtro](filtering-conditions.md)
</dt> <dt>

[**Filtraggio degli identificatori del livello**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**\_ACTION0 FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[**\_tipo di \_ contesto del provider FWPM \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

