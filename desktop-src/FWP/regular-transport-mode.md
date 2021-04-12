---
title: modalità di sicurezza trasporto
description: Lo scenario dei criteri IPsec in modalità trasporto richiede la protezione della modalità trasporto IPsec per tutto il traffico corrispondente.
ms.assetid: 303f7cdc-fb7a-4e5c-8291-cadcb45035cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfb927aff1b3f0e3c7fd13a192f0fcb18fc3ec45
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398937"
---
# <a name="transport-mode"></a>modalità di sicurezza trasporto

Lo scenario dei criteri IPsec in modalità trasporto richiede la protezione della modalità trasporto IPsec per tutto il traffico corrispondente. Qualsiasi traffico con testo non crittografato corrispondente viene eliminato fino a quando la negoziazione IKE o AuthIP non è stata completata correttamente. Se la negoziazione ha esito negativo, la connettività con l'indirizzo IP corrispondente rimarrà interrotta.

Un esempio di un possibile scenario della modalità di trasporto è "proteggere tutto il traffico dati unicast, tranne ICMP, usando la modalità di trasporto IPsec".

Per implementare questo esempio a livello di codice, utilizzare la seguente configurazione di Pam.

<dl>

**Ai \_ criteri di negoziazione FWPM layer \_ IKEEXT \_ V {4 \| 6} Setup mm**  

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

        

**A FWPM \_ Layer \_ IPSec \_ V {4 \| 6} installazione di QM e criteri di negoziazione em**  

1.  Aggiungere uno o entrambi i contesti del provider di criteri per la modalità di trasporto QM seguenti.  
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
    | Filter (proprietà)                                                   | Valore                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | **FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione** | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | **Action. Type**                                                   | \_ \_ terminazione CALLOUT azione FWP \_                             |
    | **Action. calloutKey**                                             | \_Trasporto in \_ ingresso IPSec di CALLOUT FWPM \_ \_ \_ V {4 \| 6}             |

        
2.  Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.
    | Filter (proprietà)                                                  | Valore                                                                     |
    |------------------------------------------------------------------|---------------------------------------------------------------------------|
    | **FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione** | NlatUnicast                                                               |
    | **FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**            | IPPROTO \_ ICMP {V6} queste costanti sono definite in Winsock2. h.<br/>    |
    | **Action. Type**                                                  | \_permesso azione \_ FWP                                                       |
    | **weight**                                                       | [**\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**](filter-weight-identifiers.md) |

        

**Al \_ trasporto in uscita FWPM layer \_ \_ \_ V {4 \| 6} Configurare le regole di filtro in uscita per pacchetto**  

1.  Aggiungere un filtro con le proprietà seguenti.
    | Filter (proprietà)                                                   | Valore                                              |
    |-------------------------------------------------------------------|----------------------------------------------------|
    | **FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione** | NlatUnicast                                        |
    | **Action. Type**                                                   | **\_ \_ terminazione CALLOUT azione FWP \_**              |
    | **Action. calloutKey**                                             | \_Trasporto in \_ uscita IPSec di CALLOUT FWPM \_ \_ \_ V {4 \| 6} |

        
2.  Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.
    | Filter (proprietà)                                                   | Valore                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | **FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione** | NlatUnicast                                                            |
    | **FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**             | IPPROTO \_ ICMP {V6} queste costanti sono definite in Winsock2. h.<br/> |
    | **Action. Type**                                                   | \_permesso azione \_ FWP                                                    |
    | **weight**                                                        | \_ \_ \_ esenzioni IKE per FWPM Weight Range \_                                   |

        

</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codice di esempio: utilizzo della modalità di trasporto](using-transport-mode.md)
</dt> <dt>

[**Filtraggio degli identificatori del livello**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**Tipi di contesto del provider**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_provider_context_type)
</dt> <dt>

[Condizioni di filtro](filtering-conditions.md)
</dt> <dt>

[**\_ACTION0 FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> <dt>

[**Identificatori di callout predefiniti**](built-in-callout-identifiers.md)
</dt> </dl>

 

