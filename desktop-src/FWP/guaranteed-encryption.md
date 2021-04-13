---
title: Crittografia garantita
description: Lo scenario dei criteri IPsec di crittografia garantita richiede la crittografia IPsec per tutto il traffico corrispondente. Questo criterio deve essere specificato insieme a una delle opzioni dei criteri della modalità di trasporto.
ms.assetid: 68758f0c-f134-4b7a-820a-313e2a82f280
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7120e9cb794b6010e16dd5f61accb07ca0ab9cb8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398976"
---
# <a name="guaranteed-encryption"></a>Crittografia garantita

Lo scenario dei criteri IPsec di crittografia garantita richiede la crittografia IPsec per tutto il traffico corrispondente. Questo criterio deve essere specificato insieme a una delle opzioni dei criteri della modalità di trasporto.

La crittografia garantita viene in genere usata per crittografare il traffico sensibile per ogni singola applicazione.

Un esempio di uno scenario di crittografia garantita è "proteggere tutto il traffico dati unicast, tranne ICMP, usando la modalità di trasporto IPsec, abilitare l'individuazione della negoziazione e richiedere la crittografia garantita per tutto il traffico unicast corrispondente alla porta TCP locale 5555".

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

1.  Aggiungere uno o entrambi i contesti del provider di criteri per la modalità di trasporto QM seguenti e impostare il flag di [**\_ criteri IPSec \_ \_ ND \_ Secure**](/windows/desktop/api/Ipsectypes/ns-ipsectypes-ipsec_transport_policy0) flag.  
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
    | Filter (proprietà)                                               | Valore                                                                                              |
    |---------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
    | \_Condizione di \_ \_ filtro del \_ tipo di indirizzo locale IP della condizione FWPM \_ | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type)                                      |
    | **Action. Type**                                               | **\_ \_ terminazione CALLOUT azione FWP \_**                                                              |
    | **Action. calloutKey**                                         | **\_Trasporto in \_ ingresso IPSec di CALLOUT FWPM \_ \_ \_ V {4 \| 6}**                                              |
    | **rawContext**                                                | [**sicurezza della connessione per il \_ \_ \_ \_ salvataggio permanente in ingresso IPSec \_ del contesto FWPM \_**](filter-context-identifiers.md) |

        
2.  Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti.
    | Filter (proprietà)                                                   | Valore                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione** | NlatUnicast                                                                |
    | **FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**             | **IPPROTO \_ ICMP {V6}** queste costanti sono definite in Winsock2. h.<br/> |
    | **Action. Type**                                                   | **\_permesso azione \_ FWP**                                                    |
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

        
3.  Aggiungere un filtro con le proprietà seguenti. Questo filtro consentirà solo le connessioni in ingresso alla porta TCP 5555, se crittografate.
    | Filter (proprietà)                                                   | Valore                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | **FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione** | NlatUnicast                                                                                           |
    | **FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**             | **IPPROTO \_ TCP** questa costante è definita in Winsock2. h.<br/>                                    |
    | **FWPM \_ Condizione di filtro della \_ \_ \_ porta locale IP della condizione**          | 5555                                                                                                  |
    | **Action. Type**                                                   | **\_ \_ terminazione CALLOUT azione FWP \_**                                                                 |
    | **Action. calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSec in \_ ingresso \_ avvio \_ sicuro \_ V {4 \| 6}**                                          |
    | **rawContext**                                                    | [**per la connessione a FWPM \_ Context \_ ale è richiesta la \_ \_ \_ \_ \_ crittografia IPSec**](filter-context-identifiers.md) |

        

**A FWPM \_ Layer \_ ale \_ auth \_ Connect \_ V {4 \| 6} Configurare le regole di filtro in uscita per connessione**

-   Aggiungere un filtro con le proprietà seguenti. Questo filtro consente solo le connessioni in uscita dalla porta TCP 5555, se crittografate.
    | Filter (proprietà)                                                   | Valore                                                                                                 |
    |-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
    | **FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione** | NlatUnicast                                                                                           |
    | **FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**             | **IPPROTO \_ TCP** questa costante è definita in Winsock2. h.<br/>                                    |
    | **FWPM \_ Condizione di filtro della \_ \_ \_ porta locale IP della condizione**          | 5555                                                                                                  |
    | **Action. Type**                                                   | **\_ \_ terminazione CALLOUT azione FWP \_**                                                                 |
    | **Action. calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSec \_ ale \_ Connect \_ V {4 \| 6}**                                                       |
    | **rawContext**                                                    | [**per la connessione a FWPM \_ Context \_ ale è richiesta la \_ \_ \_ \_ \_ crittografia IPSec**](filter-context-identifiers.md) |

      

  
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

 

