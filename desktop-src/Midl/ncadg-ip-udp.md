---
title: attributo ncadg_ip_udp
description: La \_ \_ parola chiave UDP IP di ncadg identifica la versione del datagramma di TCP/IP come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.
ms.assetid: c9133fcc-6dc2-49da-9c6f-5ce3c51090d5
keywords:
- attributo ncadg_ip_udp MIDL
topic_type:
- apiref
api_name:
- ncadg_ip_udp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 173ccd0b81eb5fa7d84a6fa4d2821162b852303d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117639"
---
# <a name="ncadg_ip_udp-attribute"></a>\_ \_ attributo UDP IP ncadg

La parola chiave **\_ \_ UDP IP di ncadg** identifica la versione del datagramma di TCP/IP come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.

``` syntax
endpoint("ncadg_ip_udp:server-name[port-name]")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*nome server* 
</dt> <dd>

Specifica il nome o l'indirizzo Internet per il server, o host, computer. Il nome è una stringa di caratteri e può essere un nome di dominio completo. L'indirizzo Internet è una nota comune di indirizzo Internet.

</dd> <dt>

*nome porta* 
</dt> <dd>

Specifica un numero facoltativo a 16 bit. I valori minori di 1024 sono generalmente riservati. Se non viene specificato alcun valore, il servizio di mapping degli endpoint seleziona un valore valido per il *nome di porta* .

</dd> </dl>

## <a name="remarks"></a>Commenti

Si applicano le restrizioni seguenti ai protocolli di datagramma, [**ncadg \_ IPX**](ncadg-ipx.md) e **ncadg \_ IP \_ UDP**:

-   Non supportano i callback. Tutte le funzioni che utilizzano l'attributo di **\[** [**callback**](callback.md) **\]** avranno esito negativo.
-   Non supportano l'uso del costruttore del tipo di [**pipe**](pipe.md) .

La sintassi della stringa della porta di trasporto TCP/IP, come tutte le stringhe di porta, viene definita indipendentemente dalla specifica IDL. Il compilatore esegue alcune verifiche della sintassi, ma non garantisce che la specifica dell'endpoint sia corretta. È possibile che alcuni errori vengano segnalati in fase di esecuzione anziché in fase di compilazione.

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:rainier[1404]") 
]
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncadg_ip_udp:128.10.2.30[1404]") 
]
interface iface2
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

[**ncacn \_ le reti virtuali \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[Associazione stringa](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 