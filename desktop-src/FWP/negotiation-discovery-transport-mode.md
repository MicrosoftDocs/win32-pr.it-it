---
title: Modalità trasporto individuazione negoziazione
description: Lo scenario dei criteri IPsec della modalità trasporto di individuazione negoziazione richiede la protezione della modalità trasporto IPsec per tutto il traffico in ingresso corrispondente e richiede la protezione IPsec per il traffico in uscita corrispondente.
ms.assetid: c08d9d03-7d77-43c2-8468-964b498b45f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9477d18f2fe478f5c885c071f47d0bf2baaad8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872354"
---
# <a name="negotiation-discovery-transport-mode"></a>Modalità trasporto individuazione negoziazione

Lo scenario dei criteri IPsec della modalità trasporto di individuazione negoziazione richiede la protezione della modalità trasporto IPsec per tutto il traffico in ingresso corrispondente e richiede la protezione IPsec per il traffico in uscita corrispondente. Pertanto, le connessioni in uscita possono eseguire il fallback al testo non crittografato mentre le connessioni in ingresso non lo sono.

Con questi criteri, quando il computer host tenta una nuova connessione in uscita e non esiste una SA IPsec esistente corrispondente al traffico, l'host invia contemporaneamente i pacchetti in testo non crittografato e avvia una negoziazione IKE o AuthIP. Se la negoziazione ha esito positivo, la connessione viene aggiornata a protetta da IPsec. In caso contrario, la connessione rimane in testo non crittografato. Una volta protetto da IPsec, una connessione non può mai essere sottoposto a downgrade a testo non crittografato.

La modalità di trasporto per l'individuazione della negoziazione viene in genere utilizzata in ambienti che includono sia computer idonei per IPsec che non IPsec.

Un esempio di possibile scenario di modalità trasporto di individuazione negoziazione è "proteggere tutto il traffico dati unicast, tranne ICMP, usando la modalità di trasporto IPsec e abilitare l'individuazione della negoziazione".

Per implementare questo esempio a livello di codice, utilizzare la seguente configurazione di Pam.

<dl>

**Al \_ livello FWPM \_ IKEEXT \_ V {4 \| 6} impostare i criteri di negoziazione mm**  

1.  Aggiungere uno o entrambi i contesti di provider di criteri MM seguenti.  
    -   Per IKE, un contesto del provider di criteri di tipo **FWPM \_ IPSec \_ IKE \_ mm \_ context**.
    -   Per AuthIP, un contesto del provider di criteri di tipo **FWPM \_ IPSec \_ AuthIP \_ mm \_ context**.

    > [!Note]  
    > Verrà negoziato un modulo di trasparenza comune e verranno applicati i criteri di MM corrispondenti. AuthIP è il modulo di chiavi preferito se sono supportati sia IKE che AuthIP.

     

2.  Per ognuno dei contesti aggiunti nel passaggio 1, aggiungere un filtro con le proprietà seguenti. 
    | Filter (proprietà)        | Valore                                            |
    |------------------------|--------------------------------------------------|
    | Condizioni di filtro   | Vuoto. Tutto il traffico corrisponderà al filtro.        |
    | **providerContextKey** | GUID del contesto del provider MM aggiunto nel passaggio 1. |

        

**In FWPM \_ Layer \_ IPSec \_ V {4 \| 6} configurare i criteri di negoziazione di mq e em**  

1.  Aggiungere uno o entrambi i contesti del provider di criteri per la modalità di trasporto QM seguenti e impostare il flag di [**\_ criteri IPSec \_ \_ ND \_ Secure**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.  
    -   Per IKE, un contesto del provider di criteri di tipo FWPM \_ IPSec \_ IKE \_ \_ trasporto \_ context.
    -   Per AuthIP, un contesto del provider di criteri di tipo FWPM \_ IPSec \_ AuthIP \_ mq \_ \_ context. Questo contesto può facoltativamente contenere i criteri di negoziazione della modalità estesa AuthIP (EM).

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
    | **Action. Type**                                                   | **\_permesso azione \_ FWP**                                                    |
    | **weight**                                                        | [**\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**](filter-weight-identifiers.md)  |

        

**Al \_ trasporto in uscita FWPM layer \_ \_ \_ V {4 \| 6} Configurare le regole di filtro per pacchetto in uscita**  

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

        

**At FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ Accept \_ V {4 \| 6} Configurare le regole di filtro in ingresso per connessione**  

1.  Aggiungere un filtro con le proprietà seguenti. Questo filtro consente solo i tentativi di connessione in ingresso se sono protetti da IPsec. 
    | Filter (proprietà)                                                   | Valore                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | **FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione** | NlatUnicast                                                  |
    | **Action. Type**                                                   | **\_ \_ terminazione CALLOUT azione FWP \_**                        |
    | **Action. calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSec in \_ ingresso \_ avvio \_ sicuro \_ V {4 \| 6}** |

        
2.  Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.
    | Filter (proprietà)                                                   | Valore                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione** | NlatUnicast                                                                |
    | **FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**             | **IPPROTO \_ ICMP {V6}** queste costanti sono definite in Winsock2. h.<br/> |
    | **Action. Type**                                                   | **\_permesso azione \_ FWP**                                                    |
    | **weight**                                                        | **\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**                                   |

        

</dl>

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

 

