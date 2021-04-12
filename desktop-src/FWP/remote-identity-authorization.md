---
title: Autorizzazione identità remota
description: Lo scenario dei criteri IPsec di autorizzazione dell'identità remota richiede che le connessioni in ingresso provengano da un set specifico di entità di sicurezza remote specificate in un elenco di controllo di accesso (ACL) di Windows Security Descriptor (SD).
ms.assetid: 4d9f83d6-6f56-4416-8c35-d0260f9e888c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44022c9696dec25e709d9ab1e374ada295893ed
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398874"
---
# <a name="remote-identity-authorization"></a>Autorizzazione identità remota

Lo scenario dei criteri IPsec di autorizzazione dell'identità remota richiede che le connessioni in ingresso provengano da un set specifico di entità di sicurezza remote specificate in un elenco di controllo di accesso (ACL) di Windows Security Descriptor (SD). Se l'identità remota (come determinato da IPsec) non corrisponde al set di identità consentite, la connessione verrà eliminata. Questo criterio deve essere specificato insieme a una delle opzioni dei criteri della modalità di trasporto.

Se AuthIP è abilitato, è possibile specificare due descrittori di sicurezza, uno corrispondente alla modalità principale AuthIP e l'altro corrispondente alla modalità estesa AuthIP.

Un esempio di un possibile scenario di modalità di trasporto per l'individuazione della negoziazione è "proteggere tutto il traffico dati unicast, ad eccezione di ICMP, uso della modalità di trasporto IPsec, abilitazione dell'individuazione della negoziazione e limitazione dell'accesso in ingresso alle identità remote consentite in base al descrittore di sicurezza SD1 (corrispondente alla modalità principale IKE/AuthIP) e al descrittore di sicurezza SD2 (corrispondente alla modalità estesa AuthIP), per tutto il traffico unicast corrispondente alla porta TCP locale 5555".

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

1.  Aggiungere uno o entrambi i contesti del provider di criteri per la modalità di trasporto QM seguenti e impostare il flag di [**\_ criteri IPSec \_ \_ ND \_ Secure**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.  
    -   Per IKE, un contesto del provider di criteri di tipo **FWPM \_ IPSec \_ IKE \_ \_ trasporto \_ context**.
    -   Per AuthIP, un contesto del provider di criteri di tipo **FWPM \_ IPSec \_ AuthIP \_ QM del \_ \_ contesto di trasporto** che contiene i criteri di negoziazione della modalità estesa (em) AuthIP.

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
    | Filter (proprietà)                                                   | Valore                                                                  |
    |-------------------------------------------------------------------|------------------------------------------------------------------------|
    | **FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione** | NlatUnicast                                                            |
    | **FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**             | IPPROTO \_ ICMP {V6} queste costanti sono definite in Winsock2. h.<br/> |
    | **Action. Type**                                                   | **\_permesso azione \_ FWP**                                                |
    | **weight**                                                        | **\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**                               |

        

**A FWPM \_ Layer \_ ale \_ auth \_ ricezione \_ accetta \_ V {4 \| 6} Configurare le regole di filtro in ingresso per connessione**  

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

        
3.  Aggiungere un filtro con le proprietà seguenti. Questo filtro consente le connessioni in ingresso alla porta TCP 5555 se le identità Remote corrispondenti sono consentite sia da SD1 che da SD2. 
    | Filter (proprietà)                                                   | Valore                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | **FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione** | NlatUnicast                                                        |
    | **FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**             | **IPPROTO \_ TCP** questa costante è definita in Winsock2. h.<br/> |
    | **FWPM \_ Condizione di filtro della \_ \_ \_ porta locale IP della condizione**          | 5555                                                               |
    | **\_ \_ \_ \_ ID computer remoto ale Condition \_ FWPM**                     | SD1                                                                |
    | **\_ \_ \_ \_ ID utente remoto di FWPM Condition ale \_**                        | SD2                                                                |
    | **Action. Type**                                                   | **\_ \_ terminazione CALLOUT azione FWP \_**                              |
    | **Action. calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSec in \_ ingresso \_ avvio \_ sicuro \_ V {4 \| 6}**       |

        
4.  Aggiungere un filtro con le proprietà seguenti. Questo filtro bloccherà qualsiasi altra connessione in ingresso alla porta TCP 5555 che non corrisponde al filtro precedente. 
    | Filter (proprietà)                                                   | Valore                                                              |
    |-------------------------------------------------------------------|--------------------------------------------------------------------|
    | **FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione** | NlatUnicast                                                        |
    | **FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**             | **IPPROTO \_ TCP** questa costante è definita in Winsock2. h.<br/> |
    | **FWPM \_ Condizione di filtro della \_ \_ \_ porta locale IP della condizione**          | 5555                                                               |
    | **Action. Type**                                                   | **\_blocco azione \_ FWP**                                             |

        

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

 

