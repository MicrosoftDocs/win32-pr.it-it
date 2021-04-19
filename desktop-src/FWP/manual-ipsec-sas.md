---
title: SA manuale
description: Lo scenario di criteri IPsec dell'associazione di sicurezza manuale consente ai chiamanti di ignorare i moduli di chiavi IPSec predefiniti (IKE e AuthIP) specificando direttamente le associazioni di sicurezza IPsec per proteggere il traffico di rete.
ms.assetid: 2bcc0b40-ca43-43c6-b1e4-b64426ef7ff4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beeef4486e3a07dea2e83d924c2354a3dabca241
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314574"
---
# <a name="manual-sa"></a>SA manuale

Lo scenario di criteri IPsec dell'associazione di sicurezza manuale consente ai chiamanti di ignorare i moduli di chiavi IPSec predefiniti (IKE e AuthIP) specificando direttamente le associazioni di sicurezza IPsec per proteggere il traffico di rete.

Un esempio di uno scenario SA manuale è "aggiungere una coppia di SA IPsec per proteggere il traffico dati unicast tra gli indirizzi IP 1.1.1.1 & 2.2.2.2, tranne ICMP, usando la modalità di trasporto IPsec".

> [!Note]  
> La procedura seguente deve essere eseguita su entrambi i computer con indirizzi IP impostati in modo appropriato.

 

Per implementare questo esempio a livello di codice, utilizzare la seguente configurazione di Pam.

<dl>

**Al \_ trasporto in ingresso FWPM layer \_ \_ \_ V {4 \| 6} Configurare le regole di filtro in ingresso per pacchetto**  

1.  Aggiungere un filtro con le proprietà seguenti. 

    | Filter (proprietà)                                                   | Valore                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | **FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione** | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | **\_ \_ \_ indirizzo IP locale \_ della condizione FWPM**                           | Indirizzo locale appropriato (1.1.1.1 o 2.2.2.2).           |
    | **\_ \_ \_ indirizzo IP remoto \_ della condizione FWPM**                          | Indirizzo remoto appropriato (1.1.1.1 o 2.2.2.2).          |
    | **Action. Type**                                                   | **\_ \_ terminazione CALLOUT azione FWP \_**                         |
    | **Action. calloutKey**                                             | **\_Trasporto in \_ ingresso IPSec di CALLOUT FWPM \_ \_ \_ V {4 \| 6}**         |

        
2.  Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti. 

    | Filter (proprietà)                                                   | Valore                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione** | NlatUnicast                                                                |
    | **FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**             | **IPPROTO \_ ICMP {V6}** queste costanti sono definite in Winsock2. h.<br/> |
    | **Action. Type**                                                   | **\_permesso azione \_ FWP**                                                    |
    | **weight**                                                        | [**\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**](filter-weight-identifiers.md)  |

        

**Al \_ trasporto in uscita FWPM layer \_ \_ \_ V {4 \| 6} Configurare le regole di filtro in uscita per pacchetto**  

1.  Aggiungere un filtro con le proprietà seguenti. 

    | Filter (proprietà)                                                   | Valore                                                  |
    |-------------------------------------------------------------------|--------------------------------------------------------|
    | **FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione** | NlatUnicast                                            |
    | **FWPM \_ Condizione di filtro degli \_ \_ \_ indirizzi locali IP della condizione**       | Indirizzo locale appropriato (1.1.1.1 o 2.2.2.2).    |
    | **FWPM \_ Condizione di filtro \_ \_ \_ indirizzo remoto IP condizione**      | Indirizzo remoto appropriato (1.1.1.1 o 2.2.2.2).   |
    | **Action. Type**                                                   | **\_ \_ terminazione CALLOUT azione FWP \_**                  |
    | **Action. calloutKey**                                             | **\_Trasporto in \_ uscita IPSec di CALLOUT FWPM \_ \_ \_ V {4 \| 6}** |

        
2.  Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti. 

    | Filter (proprietà)                                                   | Valore                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condizione di filtro \_ \_ del \_ \_ tipo di indirizzo locale IP della condizione** | NlatUnicast                                                                |
    | **FWPM \_ Condizione di filtro \_ \_ protocollo IP condizione**             | **IPPROTO \_ ICMP {V6}** queste costanti sono definite in Winsock2. h.<br/> |
    | **Action. Type**                                                   | **\_permesso azione \_ FWP**                                                    |
    | **weight**                                                        | **\_ \_ \_ esenzioni IKE per FWPM Weight Range \_**                                   |

        

**Configurare associazioni di sicurezza in ingresso e in uscita**

1.  Chiamare [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)con il parametro *outboundTraffic* che contiene gli indirizzi IP come 1.1.1.1 & 2.2.2.2 e **ipsecFilterId** come LUID del filtro di callout IPSec del livello trasporto in uscita aggiunto in precedenza.
2.  Chiamare [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)con il parametro *ID* contenente l'ID di contesto restituito da [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)e il parametro *getSpi* contenente gli indirizzi IP come 1.1.1.1 & 2.2.2.2 e **ipsecFilterId** come LUID del filtro di callout IPSec a livello trasporto in ingresso aggiunto in precedenza. Il valore SPI restituito deve essere usato come SA SPI in ingresso dal computer locale e come SA in uscita dal computer remoto corrispondente. Per scambiare i valori SPI, è necessario che entrambi i computer usino un certo mezzo fuori banda.
3.  Chiamare [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0), con il parametro *ID* contenente l'ID di contesto restituito da [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)e il parametro *INBOUNDBUNDLE* che descrive le proprietà del bundle SA in ingresso (ad esempio, l'associazione SA, il tipo di trasformazione, i tipi di algoritmo, le chiavi e così via).
4.  Chiamare [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0), con il parametro *ID* contenente l'ID di contesto restituito da [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)e il parametro *OUTBOUNDBUNDLE* che descrive le proprietà del bundle SA in uscita (ad esempio, l'associazione SA in uscita, il tipo di trasformazione, i tipi di algoritmo, le chiavi e così via).

  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codice di esempio: digitazione manuale SA](manual-sa-keying.md)
</dt> <dt>

[**Identificatori di callout predefiniti**](built-in-callout-identifiers.md)
</dt> <dt>

[**Filtraggio degli identificatori del livello**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**\_ACTION0 FWPM**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> </dl>

 

