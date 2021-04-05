---
title: attributo ncacn_vns_spp
description: La \_ \_ parola chiave ncacn le reti virtuali spp identifica Banyan VINES SPP come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.
ms.assetid: a2aff0a6-2e7e-43e4-a180-f1ddd0456843
keywords:
- attributo ncacn_vns_spp MIDL
topic_type:
- apiref
api_name:
- ncacn_vns_spp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e72cd17ae65fbffc2cef280f15d12ba0ddbdbe
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726079"
---
# <a name="ncacn_vns_spp-attribute"></a>\_attributo ncacn le reti virtuali \_ spp

La parola chiave **ncacn \_ le reti virtuali \_ spp** identifica Banyan VINES SPP come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.

``` syntax
endpoint("ncacn_vns_spp:server-name[port-address]")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*nome server* 
</dt> <dd>

Specifica il nome StreetTalk del server. Il nome è nel formato item@group @organization . L'elemento può contenere un massimo di 31 caratteri e il gruppo e l'organizzazione possono avere un massimo di 15 caratteri.

</dd> <dt>

*nome porta* 
</dt> <dd>

Specifica una porta Banyan VINES SPP. L'intervallo valido per gli endpoint statici è 250-511.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per usare il protocollo di trasporto **ncacn \_ le reti virtuali \_ spp** nelle applicazioni distribuite in esecuzione su Windows 2000, è necessario installare il software Banyan Enterprise client appropriato. Al termine dell'installazione, aprire il **Pannello di controllo**, scegliere **configurazione e Aggiungi**, quindi selezionare **servizio \| \| servizi RPC di Banyan per Banyan**. Il supporto per i client a 16 bit richiede il software VINES appropriato. Per ulteriori informazioni sul prodotto Enterprise Client di Banyan e sul software a 16 bit Vines, contattare Banyan.

La sintassi della stringa di porta del trasporto del Banyan VINES, come tutte le stringhe di porta, viene definita indipendentemente dalla specifica IDL. Il compilatore esegue alcune verifiche della sintassi, ma non garantisce che la specifica dell'endpoint sia corretta. È possibile che alcuni errori vengano segnalati in fase di esecuzione anziché in fase di compilazione.

> [!Note]  
> Questa famiglia di protocolli non è supportata in Windows XP.

 

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_vns_spp:printer@sdkgrp@company[260]")
]
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**endpoint**](endpoint.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ in \_ DSP**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ DNET \_ NSP**](ncacn-dnet-nsp.md)
</dt> <dt>

[**\_TCP IP \_ ncacn**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ NB \_ IPX**](ncacn-nb-ipx.md)
</dt> <dt>

[**\_SPX ncacn**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ NB \_ NB**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ NB \_ TCP**](ncacn-nb-tcp.md)
</dt> <dt>

[**\_NP ncacn**](ncacn-np.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[**\_UDP IP \_ ncadg**](ncadg-ip-udp.md)
</dt> <dt>

[Associazione stringa](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 