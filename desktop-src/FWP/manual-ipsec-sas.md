---
title: Firma di accesso condiviso manuale
description: Lo scenario dei criteri IPsec dell'associazione di sicurezza manuale (SA) consente ai chiamanti di ignorare i moduli di chiave IPsec predefiniti (IKE e AuthIP) specificando direttamente le SA IPsec per proteggere qualsiasi traffico di rete.
ms.assetid: 2bcc0b40-ca43-43c6-b1e4-b64426ef7ff4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cdb3d7c67d9cfa513cbdff846c02fd6ba61ebf031672fb86887bc01c90455b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083321"
---
# <a name="manual-sa"></a>Firma di accesso condiviso manuale

Lo scenario dei criteri IPsec dell'associazione di sicurezza manuale (SA) consente ai chiamanti di ignorare i moduli di chiave IPsec predefiniti (IKE e AuthIP) specificando direttamente le SA IPsec per proteggere qualsiasi traffico di rete.

Un esempio di un possibile scenario di firma di accesso condiviso manuale è "Aggiungere una coppia di SA IPsec per proteggere tutto il traffico dati unicast tra gli indirizzi IP 1.1.1.1 & 2.2.2.2, ad eccezione di ICMP, usando la modalità di trasporto IPsec".

> [!Note]  
> I passaggi seguenti devono essere eseguiti in entrambi i computer con indirizzi IP impostati in modo appropriato.

 

Per implementare questo esempio a livello di codice, usare la configurazione wfp seguente.

<dl>

**In FWPM \_ LAYER \_ INBOUND \_ TRANSPORT \_ V{4 \| 6} configurare le regole di filtro in ingresso per pacchetto**  

1.  Aggiungere un filtro con le proprietà seguenti. 

    | Proprietà Filter                                                   | Valore                                                         |
    |-------------------------------------------------------------------|---------------------------------------------------------------|
    | **FWPM \_ Condizione \_ di filtro CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | [NlatUnicast](/windows/win32/api/nldef/ne-nldef-nl_address_type) |
    | **INDIRIZZO IP LOCALE DELLA CONDIZIONE FWPM \_ \_ \_ \_**                           | Indirizzo locale appropriato (1.1.1.1 o 2.2.2.2).           |
    | **INDIRIZZO REMOTO IP DELLA CONDIZIONE FWPM \_ \_ \_ \_**                          | Indirizzo remoto appropriato (1.1.1.1 o 2.2.2.2).          |
    | **action.type**                                                   | **CALLOUT AZIONE FWP \_ \_ CHE \_ TERMINA**                         |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ \_ INBOUND TRANSPORT \_ V{4 \| 6}**         |

        
2.  Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti. 

    | Proprietà Filter                                                   | Valore                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condizione \_ di filtro CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                                |
    | **FWPM \_ Condizione \_ di filtro \_ PROTOCOLLO IP** CONDIZIONE             | **IPPROTO \_ ICMP{V6}** Queste costanti sono definite in winsock2.h.<br/> |
    | **action.type**                                                   | **AUTORIZZAZIONE \_ ALL'AZIONE \_ FWP**                                                    |
    | **weight**                                                        | [**ESENZIONI \_ \_ IKE PER L'INTERVALLO DI PESO \_ FWPM \_**](filter-weight-identifiers.md)  |

        

**In FWPM \_ LAYER \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6} configurare le regole di filtro in uscita per pacchetto**  

1.  Aggiungere un filtro con le proprietà seguenti. 

    | Proprietà Filter                                                   | Valore                                                  |
    |-------------------------------------------------------------------|--------------------------------------------------------|
    | **FWPM \_ Condizione \_ di filtro CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                            |
    | **FWPM \_ Condizione \_ di filtro CONDITION IP LOCAL \_ \_ ADDRESS**       | Indirizzo locale appropriato (1.1.1.1 o 2.2.2.2).    |
    | **FWPM \_ Condizione \_ di filtro CONDITION IP REMOTE \_ \_ ADDRESS**      | Indirizzo remoto appropriato (1.1.1.1 o 2.2.2.2).   |
    | **action.type**                                                   | **CALLOUT AZIONE FWP \_ \_ CHE \_ TERMINA**                  |
    | **action.calloutKey**                                             | **FWPM \_ CALLOUT \_ IPSEC \_ OUTBOUND TRANSPORT \_ \_ V{4 \| 6}** |

        
2.  Esentare il traffico ICMP da IPsec aggiungendo un filtro con le proprietà seguenti. 

    | Proprietà Filter                                                   | Valore                                                                      |
    |-------------------------------------------------------------------|----------------------------------------------------------------------------|
    | **FWPM \_ Condizione \_ di filtro CONDITION IP LOCAL ADDRESS \_ \_ \_ TYPE** | NlatUnicast                                                                |
    | **FWPM \_ Condizione \_ di filtro \_ PROTOCOLLO IP** CONDIZIONE             | **IPPROTO \_ ICMP{V6}** Queste costanti sono definite in winsock2.h.<br/> |
    | **action.type**                                                   | **AUTORIZZAZIONE \_ ALL'AZIONE \_ FWP**                                                    |
    | **weight**                                                        | **ESENZIONI \_ \_ IKE PER L'INTERVALLO DI PESO \_ FWPM \_**                                   |

        

**Configurare le associazioni di sicurezza in ingresso e in uscita**

1.  Chiamare [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)con il parametro *outboundTraffic* contenente gli indirizzi IP come 1.1.1.1 & 2.2.2.2 e **ipsecFilterId** come LUID del filtro callout IPsec del livello di trasporto in uscita aggiunto in precedenza.
2.  Chiamare [**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)con il parametro *id* contenente l'ID di contesto restituito da [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)e il parametro *getSpi* contenente gli indirizzi IP come 1.1.1.1 & 2.2.2.2 e **ipsecFilterId** come LUID del filtro callout IPsec del livello di trasporto in ingresso aggiunto in precedenza. Il valore SPI restituito deve essere usato come SPI sa in ingresso dal computer locale e come SPI sa in uscita dal computer remoto corrispondente. Entrambi i computer devono usare alcuni mezzi fuori banda per scambiare i valori SPI.
3.  Chiamare [**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)con il parametro *id* contenente l'ID di contesto restituito da [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)e il parametro *inboundBundle* che descrive le proprietà dell'aggregazione sa in ingresso ,ad esempio l'SPI sa in ingresso, il tipo di trasformazione, i tipi di algoritmo, le chiavi e così via.
4.  Chiamare [**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)con il parametro *id* contenente l'ID di contesto restituito da [**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)e il parametro *outboundBundle* che descrive le proprietà dell'aggregazione sa in uscita, ad esempio spi sa in uscita, tipo di trasformazione, tipi di algoritmo, chiavi e così via.

  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Codice di esempio: Keying SA manuale](manual-sa-keying.md)
</dt> <dt>

[**Identificatori callout predefiniti**](built-in-callout-identifiers.md)
</dt> <dt>

[**Filtro degli identificatori di livello**](management-filtering-layer-identifiers-.md)
</dt> <dt>

[**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0)
</dt> </dl>

 

