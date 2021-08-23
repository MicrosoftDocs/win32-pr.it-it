---
title: modalità di sicurezza trasporto
description: Lo scenario dei criteri IPsec in modalità trasporto richiede la protezione in modalità trasporto IPsec per tutto il traffico corrispondente.
ms.assetid: 303f7cdc-fb7a-4e5c-8291-cadcb45035cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebfb6dad27340bfc72397307c58fddfe2bdf6eeadb65081faa0e1941de2c052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535891"
---
# <a name="transport-mode"></a>modalità di sicurezza trasporto

Lo scenario dei criteri IPsec in modalità trasporto richiede la protezione in modalità trasporto IPsec per tutto il traffico corrispondente. Qualsiasi traffico di testo non crittografato corrispondente viene eliminato fino al completamento della negoziazione IKE o AuthIP. Se la negoziazione non riesce, la connettività con l'indirizzo IP corrispondente rimarrà interrotta.

Un esempio di possibile scenario di modalità di trasporto è "Proteggere tutto il traffico dati unicast, ad eccezione di ICMP, usando la modalità di trasporto IPsec".

Per implementare questo esempio a livello di codice, usare la configurazione WFP seguente.

<dl>

**Al livello FWPM \_ \_ IKEEXT \_ V{4 \| 6} configurare i criteri di negoziazione MM**  

1.  Aggiungere uno o entrambi i contesti del provider di criteri MM seguenti.  
    -   Per IKE, un contesto del provider di criteri di tipo **FWPM \_ IPSEC \_ IKE \_ MM \_ CONTEXT**.
    -   Per AuthIP, un contesto del provider di criteri di tipo **FWPM \_ IPSEC \_ AUTHIP \_ MM \_ CONTEXT**.

    > [!Note]  
    > Verrà negoziato un modulo di keying comune e verranno applicati i criteri MM corrispondenti. AuthIP è il modulo di creazione chiavi preferito se sono supportati sia IKE che AuthIP.

     

2.  Per ognuno dei contesti aggiunti nel passaggio 1, aggiungere un filtro con le proprietà seguenti. 

    | Filter - proprietà        | Valore                                            |
    |------------------------|--------------------------------------------------|
    | Condizioni di filtro   | Vuoto. Tutto il traffico corrisponderà al filtro.        |
    | **providerContextKey** | GUID del contesto del provider MM aggiunto nel passaggio 1. |

        

**Al livello FWPM \_ \_ IPSEC \_ V{4 6} configurare i criteri di negoziazione \| QM ed EM**  

1.  Aggiungere uno o entrambi i contesti del provider di criteri della modalità trasporto QM seguenti.  
    -   Per IKE, un contesto del provider di criteri di tipo **FWPM \_ IPSEC \_ IKE \_ \_ QM TRANSPORT \_ CONTEXT**.
    -   Per AuthIP, un contesto del provider di criteri di tipo **FWPM \_ IPSEC \_ AUTHIP \_ QM \_ TRANSPORT \_ CONTEXT**. Questo contesto può contenere facoltativamente i criteri di negoziazione AuthIP Extended Mode (EM).

    > [!Note]  
    > Verrà negoziato un modulo di keying comune e verranno applicati i criteri QM corrispondenti. AuthIP è il modulo di creazione chiavi preferito se sono supportati sia IKE che AuthIP.

     

2.  Per ognuno dei contesti aggiunti nel passaggio 1, aggiungere un filtro con le proprietà seguenti. 

    | Filter - proprietà        | Valore                                            |
    |------------------------|--------------------------------------------------|
    | Condizioni di filtro   | Vuoto. Tutto il traffico corrisponderà al filtro.        |
    | **providerContextKey** | GUID del contesto del provider QM aggiunto nel passaggio 1. |

        

**A livello FWPM \_ \_ TRANSPORT INBOUND \_ \_ V{4 \| 6} configurare le regole di filtro in ingresso per pacchetto**  

1.  Aggiungere un filtro con le proprietà seguenti. 

    | Filter - proprietà                                                   | Valore                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | **FWPM \_ Condizione di \_ filtro CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | **action.type**                                                   | TERMINAZIONE \_ DEL \_ CALLOUT DELL'AZIONE \_ FWP                             |
    | **action.calloutKey**                                             | FWPM \_ CALLOUT \_ IPSEC \_ \_ INBOUND TRANSPORT \_ V{4 \| 6}             |

        
2.  Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.

    | Filter - proprietà                                                  | Valore                                                                     |
    |------------------------------------------------------------------|---------------------------------------------------------------------------|
    | **FWPM \_ Condizione di \_ filtro CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                               |
    | **FWPM \_ Condizione di \_ filtro CONDITION IP \_ PROTOCOL**            | IPPROTO \_ ICMP{V6}Queste costanti sono definite in winsock2.h.<br/>    |
    | **action.type**                                                  | AUTORIZZAZIONE \_ AZIONE FWP \_                                                       |
    | **weight**                                                       | [**ESENZIONI \_ \_ IKE PER L'INTERVALLO DI PESO \_ FWPM \_**](filter-weight-identifiers.md) |

        

**A livello FWPM \_ \_ TRANSPORT IN USCITA \_ \_ V{4 \| 6} configurare regole di filtro in uscita per pacchetto**  

1.  Aggiungere un filtro con le proprietà seguenti.

    | Filter - proprietà                                                   | Valore                                              |
    |-------------------------------------------------------------------|----------------------------------------------------|
    | **FWPM \_ Condizione di \_ filtro CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                        |
    | **action.type**                                                   | **TERMINAZIONE \_ DEL \_ CALLOUT DELL'AZIONE \_ FWP**              |
    | **action.calloutKey**                                             | FWPM \_ CALLOUT \_ IPSEC \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6} |

        
2.  Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.

    | Filter - proprietà                                                   | Valore                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | **FWPM \_ Condizione di \_ filtro CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                            |
    | **FWPM \_ Condizione di \_ filtro CONDITION IP \_ PROTOCOL**             | IPPROTO \_ ICMP{V6}Queste costanti sono definite in winsock2.h.<br/> |
    | **action.type**                                                   | AUTORIZZAZIONE \_ AZIONE FWP \_                                                    |
    | **weight**                                                        | ESENZIONI \_ \_ IKE PER L'INTERVALLO DI PESO \_ FWPM \_                                   |

        

</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codice di esempio: Uso della modalità trasporto](using-transport-mode.md)
</dt> <dt>

[**Filtro degli identificatori dei livelli**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**Tipi di contesto del provider**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> <dt>

[Condizioni di filtro](filtering-conditions.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[**Identificatori di callout predefiniti**](built-in-callout-identifiers.md)
</dt> </dl>

 

