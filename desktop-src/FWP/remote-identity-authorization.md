---
title: Autorizzazione dell'identità remota
description: Lo scenario dei criteri IPsec per l'autorizzazione dell'identità remota richiede che le connessioni in ingresso provengono da un set specifico di entità di sicurezza remote specificate in un elenco di controllo di accesso (ACL) del descrittore di sicurezza Windows.
ms.assetid: 4d9f83d6-6f56-4416-8c35-d0260f9e888c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c426f0d153d45d3699020bb723b15d75d84df4662fd0bb61d66513c2af24fe31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075381"
---
# <a name="remote-identity-authorization"></a>Autorizzazione dell'identità remota

Lo scenario dei criteri IPsec per l'autorizzazione dell'identità remota richiede che le connessioni in ingresso provengono da un set specifico di entità di sicurezza remote specificate in un elenco di controllo di accesso (ACL) del descrittore di sicurezza Windows. Se l'identità remota (come determinato da IPsec) non corrisponde al set di identità consentite, la connessione verrà eliminata. Questo criterio deve essere specificato insieme a una delle opzioni dei criteri della modalità di trasporto.

Se AuthIP è abilitato, è possibile specificare due descrittori di sicurezza, uno corrispondente alla modalità principale AuthIP e l'altro corrispondente alla modalità estesa AuthIP.

Un esempio di un possibile scenario di modalità trasporto individuazione negoziazione è "Proteggere tutto il traffico dati unicast, ad eccezione di ICMP, usando la modalità di trasporto IPsec, abilitare l'individuazione della negoziazione e limitare l'accesso in ingresso alle identità remote consentite in base al descrittore di sicurezza SD1 (corrispondente alla modalità principale IKE/AuthIP) e al descrittore di sicurezza SD2 (corrispondente alla modalità estesa AuthIP), per tutto il traffico unicast corrispondente alla porta locale TCP 5555".

Per implementare questo esempio a livello di codice, usare la configurazione wfp seguente.

<dl>

**Al livello FWPM \_ \_ IKEEXT \_ V{4 6} configurare i criteri di \| negoziazione MM**  

1.  Aggiungere uno o entrambi i contesti del provider di criteri MM seguenti.  
    -   Per IKE, un contesto del provider di criteri di tipo **FWPM \_ IPSEC \_ IKE \_ MM \_ CONTEXT**.
    -   Per AuthIP, un contesto del provider di criteri di tipo **FWPM \_ IPSEC \_ AUTHIP \_ MM \_ CONTEXT**.

    > [!Note]  
    > Verrà negoziato un modulo di keying comune e verranno applicati i criteri MM corrispondenti. AuthIP è il modulo di keying preferito se sono supportati sia IKE che AuthIP.

     

2.  Per ognuno dei contesti aggiunti nel passaggio 1, aggiungere un filtro con le proprietà seguenti. 

    | Proprietà Filter        | Valore                                            |
    |------------------------|--------------------------------------------------|
    | Condizioni di filtro   | Vuoto. Tutto il traffico corrisponderà al filtro.        |
    | **providerContextKey** | GUID del contesto del provider MM aggiunto nel passaggio 1. |

        

**Al livello FWPM \_ \_ IPSEC \_ V{4 6} configurare i criteri \| di negoziazione QM ed EM**  

1.  Aggiungere uno o entrambi i contesti del provider di criteri della modalità di trasporto QM seguenti e impostare il flag [**IPSEC \_ POLICY FLAG \_ \_ ND \_ SECURE.**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0)  
    -   Per IKE, un contesto del provider di criteri di tipo **FWPM \_ IPSEC \_ IKE \_ QM \_ TRANSPORT \_ CONTEXT**.
    -   Per AuthIP, contesto del provider di criteri di tipo **\_ FWPM IPSEC \_ AUTHIP \_ QM \_ TRANSPORT \_ CONTEXT** che contiene i criteri di negoziazione AuthIP Extended Mode (EM).

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
    | **action.type**                                                   | AUTORIZZAZIONE \_ ALL'AZIONE \_ FWP                                                        |
    | **weight**                                                        | [**ESENZIONI \_ \_ IKE PER L'INTERVALLO DI PESO \_ FWPM \_**](filter-weight-identifiers.md)  |

        

**In FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6} configurare le regole di filtro in uscita per pacchetto**  

1.  Aggiungere un filtro con le proprietà seguenti. 

    | Proprietà Filter                                                   | Valore                                                                                     |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
    | **FWPM \_ Condizione \_ di filtro CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                                               |
    | **action.type**                                                   | **CALLOUT AZIONE FWP \_ \_ CHE \_ TERMINA**                                                     |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6}**                                    |
    | **rawContext**                                                    | [**INDIVIDUAZIONE NEGOZIAZIONE \_ \_ IN USCITA IPSEC \_ CONTESTO \_ \_ FWPM**](filter-context-identifiers.md) |

        
2.  Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti. 

    | Proprietà Filter                                                   | Valore                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | **FWPM \_ Condizione \_ di filtro CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                            |
    | **FWPM \_ Condizione \_ di filtro \_ PROTOCOLLO IP** CONDIZIONE             | IPPROTO \_ ICMP{V6}Queste costanti sono definite in winsock2.h.<br/> |
    | **action.type**                                                   | **AUTORIZZAZIONE \_ ALL'AZIONE \_ FWP**                                                |
    | **weight**                                                        | **ESENZIONI \_ \_ IKE PER L'INTERVALLO DI PESO \_ FWPM \_**                               |

        

**In FWPM \_ LAYER \_ ALE \_ AUTH \_ RECV \_ ACCEPT \_ V{4 \| 6} setup inbound per connection filtering rules**  

1.  Aggiungere un filtro con le proprietà seguenti. Questo filtro consentirà i tentativi di connessione in ingresso solo se sono protetti da IPsec. 

    | Proprietà Filter                                                   | Valore                                                        |
    |-------------------------------------------------------------------|--------------------------------------------------------------|
    | **FWPM \_ Condizione \_ di filtro CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                  |
    | **action.type**                                                   | **CALLOUT AZIONE FWP \_ \_ CHE \_ TERMINA**                        |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ IN INGRESSO INITIATE \_ \_ SECURE \_ V{4 \| 6}** |

        
2.  Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti. 

    | Proprietà Filter                                                   | Valore                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condizione \_ di filtro CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                                |
    | **FWPM \_ Condizione \_ di filtro \_ PROTOCOLLO IP** CONDIZIONE             | **IPPROTO \_ ICMP{V6}** Queste costanti sono definite in winsock2.h.<br/> |
    | **action.type**                                                   | **AUTORIZZAZIONE \_ ALL'AZIONE \_ FWP**                                                    |
    | **weight**                                                        | **ESENZIONI \_ \_ IKE PER L'INTERVALLO DI PESO \_ FWPM \_**                                   |

        
3.  Aggiungere un filtro con le proprietà seguenti. Questo filtro consente le connessioni in ingresso alla porta TCP 5555 se le identità remote corrispondenti sono consentite sia da SD1 che da SD2. 

    | Proprietà Filter                                                   | Valore                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | **FWPM \_ Condizione \_ di filtro CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                        |
    | **FWPM \_ Condizione \_ di filtro \_ PROTOCOLLO IP** CONDIZIONE             | **IPPROTO \_ TCP** Questa costante è definita in winsock2.h.<br/> |
    | **FWPM \_ Condizione \_ di filtro CONDITION IP LOCAL \_ \_ PORT**          | 5555                                                               |
    | **FWPM CONDITION ALE REMOTE MACHINE ID (ID MACCHINA REMOTA \_ FWPM CONDITION \_ \_ ALE) \_ \_**                     | SD1                                                                |
    | **ID UTENTE \_ REMOTO FWPM CONDITION \_ ALE \_ \_ \_**                        | SD2                                                                |
    | **action.type**                                                   | **CALLOUT AZIONE FWP \_ \_ CHE \_ TERMINA**                              |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ IN INGRESSO INITIATE \_ \_ SECURE \_ V{4 \| 6}**       |

        
4.  Aggiungere un filtro con le proprietà seguenti. Questo filtro blocca tutte le altre connessioni in ingresso alla porta TCP 5555 che non corrispondono al filtro precedente. 

    | Proprietà Filter                                                   | Valore                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | **FWPM \_ Condizione \_ di filtro CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                        |
    | **FWPM \_ Condizione \_ di filtro \_ PROTOCOLLO IP** CONDIZIONE             | **IPPROTO \_ TCP** Questa costante è definita in winsock2.h.<br/> |
    | **FWPM \_ Condizione \_ di filtro CONDITION IP LOCAL \_ \_ PORT**          | 5555                                                               |
    | **action.type**                                                   | **BLOCCO DI \_ AZIONE \_ FWP**                                             |

        

</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codice di esempio: Uso della modalità di trasporto](using-transport-mode.md)
</dt> <dt>

[Livelli ALE](ale-layers.md)
</dt> <dt>

[**Identificatori callout predefiniti**](built-in-callout-identifiers.md)
</dt> <dt>

[Condizioni di filtro](filtering-conditions.md)
</dt> <dt>

[**Filtro degli identificatori di livello**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[**TIPO DI CONTESTO DEL PROVIDER FWPM \_ \_ \_**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> </dl>

 

