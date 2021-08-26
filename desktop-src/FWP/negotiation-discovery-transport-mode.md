---
title: Modalità di trasporto individuazione negoziazione
description: Lo scenario dei criteri IPsec modalità trasporto individuazione negoziazione richiede la protezione in modalità trasporto IPsec per tutto il traffico in ingresso corrispondente e richiede la protezione IPsec per la corrispondenza del traffico in uscita.
ms.assetid: c08d9d03-7d77-43c2-8468-964b498b45f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990a7f84e20d081933ffa0def9800ff7610a3a0e3a6d01dd3b45fe7c99729ca9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102141"
---
# <a name="negotiation-discovery-transport-mode"></a>Modalità di trasporto individuazione negoziazione

Lo scenario dei criteri IPsec modalità trasporto individuazione negoziazione richiede la protezione in modalità trasporto IPsec per tutto il traffico in ingresso corrispondente e richiede la protezione IPsec per la corrispondenza del traffico in uscita. Pertanto, alle connessioni in uscita è consentito il fallback in testo non crittografato, mentre le connessioni in ingresso non lo sono.

Con questo criterio, quando il computer host tenta una nuova connessione in uscita e non esiste alcuna firma di accesso condiviso IPsec esistente corrispondente al traffico, l'host invia contemporaneamente i pacchetti in testo non crittografato e avvia una negoziazione IKE o AuthIP. Se la negoziazione ha esito positivo, la connessione viene aggiornata a protetta da IPsec. In caso contrario, la connessione rimane in testo non crittografato. Dopo aver protetto IPsec, non è mai possibile eseguire il downgrade di una connessione in testo non crittografato.

La modalità di trasporto individuazione negoziazione viene in genere usata in ambienti che includono computer con capacità IPsec e non IPsec.

Un esempio di un possibile scenario di modalità trasporto individuazione negoziazione è "Proteggere tutto il traffico dati unicast, ad eccezione di ICMP, usando la modalità di trasporto IPsec e abilitare l'individuazione della negoziazione".

Per implementare questo esempio a livello di codice, usare la configurazione wfp seguente.

<dl>

**In FWPM \_ LAYER \_ IKEEXT \_ V{4 \| 6} configurare i criteri di negoziazione MM**  

1.  Aggiungere uno o entrambi i contesti del provider di criteri MM seguenti.  
    -   Per IKE, un contesto del provider di criteri di tipo **FWPM \_ IPSEC \_ IKE \_ MM \_ CONTEXT**.
    -   Per AuthIP, contesto del provider di criteri di tipo **FWPM \_ IPSEC \_ AUTHIP \_ MM \_ CONTEXT**.

    > [!Note]  
    > Verrà negoziato un modulo di keying comune e verranno applicati i criteri MM corrispondenti. AuthIP è il modulo di keying preferito se sono supportati sia IKE che AuthIP.

     

2.  Per ognuno dei contesti aggiunti nel passaggio 1, aggiungere un filtro con le proprietà seguenti. 

    | Proprietà Filter        | Valore                                            |
    |------------------------|--------------------------------------------------|
    | Condizioni di filtro   | Vuoto. Tutto il traffico corrisponderà al filtro.        |
    | **providerContextKey** | GUID del contesto del provider MM aggiunto nel passaggio 1. |

        

**In FWPM \_ LAYER \_ IPSEC \_ V{4 6} configurare i criteri di negoziazione \| QM ed EM**  

1.  Aggiungere uno o entrambi i contesti del provider di criteri della modalità di trasporto QM seguenti e impostare il flag [**IPSEC \_ POLICY FLAG \_ \_ ND \_ SECURE.**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0)  
    -   Per IKE, contesto del provider di criteri di tipo FWPM \_ IPSEC \_ IKE \_ QM \_ TRANSPORT \_ CONTEXT.
    -   Per AuthIP, contesto del provider di criteri di tipo FWPM \_ IPSEC \_ AUTHIP \_ QM \_ TRANSPORT \_ CONTEXT. Questo contesto può contenere facoltativamente i criteri di negoziazione AuthIP Extended Mode (EM).

    > [!Note]  
    > Verrà negoziato un modulo di keying comune e verranno applicati i criteri QM corrispondenti. AuthIP è il modulo di keying preferito se sono supportati sia IKE che AuthIP.

     

2.  Per ognuno dei contesti aggiunti nel passaggio 1, aggiungere un filtro con le proprietà seguenti. 

    | Proprietà Filter        | Valore                                            |
    |------------------------|--------------------------------------------------|
    | Condizioni di filtro   | Vuoto. Tutto il traffico corrisponderà al filtro.        |
    | **providerContextKey** | GUID del contesto del provider QM aggiunto nel passaggio 1. |

        

**In FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V{4 \| 6} configurare le regole di filtro in ingresso per pacchetto**  

1.  Aggiungere un filtro con le proprietà seguenti. 

    | Proprietà Filter                                                   | Valore                                                                                              |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | **FWPM \_ Condizione \_ di filtro CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | **action.type**                                                   | **CALLOUT AZIONE FWP \_ \_ CHE \_ TERMINA**                                                              |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ \_ INBOUND TRANSPORT \_ V{4 \| 6}**                                              |
    | **rawContext**                                                    | [**FWPM \_ CONTEXT \_ IPSEC \_ INBOUND \_ PERSIST \_ CONNECTION \_ SECURITY**](filter-context-identifiers.md) |

        
2.  Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.

    | Proprietà Filter                                                   | Valore                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condizione \_ di filtro CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                                |
    | **FWPM \_ Condizione \_ di filtro \_ PROTOCOLLO IP** CONDIZIONE             | **IPPROTO \_ ICMP{V6}** Queste costanti sono definite in winsock2.h.<br/> |
    | **action.type**                                                   | **AUTORIZZAZIONE \_ ALL'AZIONE \_ FWP**                                                    |
    | **weight**                                                        | [**ESENZIONI \_ \_ IKE PER L'INTERVALLO DI PESO \_ FWPM \_**](filter-weight-identifiers.md)  |

        

**In FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6} configurare regole di filtro in uscita per pacchetto**  

1.  Aggiungere un filtro con le proprietà seguenti.

    | Proprietà Filter                                                   | Valore                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | **FWPM \_ Condizione \_ di filtro CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                                               |
    | **action.type**                                                   | **CALLOUT AZIONE FWP \_ \_ CHE \_ TERMINA**                                                     |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6}**                                    |
    | **rawContext**                                                    | [**INDIVIDUAZIONE NEGOZIAZIONE \_ \_ IN USCITA IPSEC \_ CONTESTO \_ \_ FWPM**](filter-context-identifiers.md) |

        
2.  Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.

    | Proprietà Filter                                                   | Valore                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condizione \_ di filtro CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                                |
    | **FWPM \_ Condizione \_ di filtro \_ PROTOCOLLO IP** CONDIZIONE             | **IPPROTO \_ ICMP{V6}** Queste costanti sono definite in winsock2.h.<br/> |
    | **action.type**                                                   | **AUTORIZZAZIONE \_ ALL'AZIONE \_ FWP**                                                    |
    | **weight**                                                        | **ESENZIONI \_ \_ IKE PER L'INTERVALLO DI PESO \_ FWPM \_**                                   |

        

**In FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6} configurare le regole di filtro per connessione in ingresso**  

1.  Aggiungere un filtro con le proprietà seguenti. Questo filtro consentirà i tentativi di connessione in ingresso solo se sono protetti da IPsec. 

    | Proprietà Filter                                                   | Valore                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | **FWPM \_ Condizione \_ di filtro CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                  |
    | **action.type**                                                   | **CALLOUT AZIONE FWP \_ \_ CHE \_ TERMINA**                        |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ IN INGRESSO INITIATE \_ \_ SECURE \_ V{4 \| 6}** |

        
2.  Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.

    | Proprietà Filter                                                   | Valore                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condizione di \_ filtro CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                                |
    | **FWPM \_ Condizione di \_ filtro CONDITION IP \_ PROTOCOL**             | **IPPROTO \_ ICMP{V6}** Queste costanti sono definite in winsock2.h.<br/> |
    | **action.type**                                                   | **AUTORIZZAZIONE \_ AZIONE FWP \_**                                                    |
    | **weight**                                                        | **ESENZIONI \_ \_ IKE PER L'INTERVALLO DI PESO \_ FWPM \_**                                   |

        

</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codice di esempio: Uso della modalità trasporto](using-transport-mode.md)
</dt> <dt>

[Livelli ALE](ale-layers.md)
</dt> <dt>

[**Identificatori di callout predefiniti**](built-in-callout-identifiers.md)
</dt> <dt>

[Condizioni di filtro](filtering-conditions.md)
</dt> <dt>

[**Filtro degli identificatori dei livelli**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[**TIPO DI CONTESTO DEL PROVIDER FWPM \_ \_ \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

