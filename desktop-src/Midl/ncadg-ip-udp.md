---
title: ncadg_ip_udp attributo
description: La parola chiave ncadg \_ ip udp identifica la versione del \_ datagramma di TCP/IP come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere usata nelle nuove applicazioni.
ms.assetid: c9133fcc-6dc2-49da-9c6f-5ce3c51090d5
keywords:
- ncadg_ip_udp attributo MIDL
topic_type:
- apiref
api_name:
- ncadg_ip_udp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f91db32fd7636f956e64dafc0db15efb520e643b435995dd977db7a631a20c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067061"
---
# <a name="ncadg_ip_udp-attribute"></a>Attributo ncadg \_ ip \_ udp

La **parola chiave ncadg \_ ip \_ udp** identifica la versione del datagramma di TCP/IP come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere usata nelle nuove applicazioni.

``` syntax
endpoint("ncadg_ip_udp:server-name[port-name]")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*nome-server* 
</dt> <dd>

Specifica il nome o l'indirizzo Internet per il server, o host, computer. Il nome è una stringa di caratteri e può essere un nome di dominio completo. L'indirizzo Internet è una notazione di indirizzo Internet comune.

</dd> <dt>

*port-name* 
</dt> <dd>

Specifica un numero a 16 bit facoltativo. I valori minori di 1024 sono in genere riservati. Se non viene specificato alcun valore, il servizio di mapping degli endpoint seleziona un valore *di nome di porta* valido.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le restrizioni seguenti si applicano ai protocolli di datagramma, [**ncadg \_ ipx**](ncadg-ipx.md) e **ncadg \_ ip \_ udp:**

-   Non supportano i callback. Tutte le funzioni che usano **\[** [**l'attributo di callback**](callback.md) **\]** avranno esito negativo.
-   Non supportano l'uso del costruttore [**del tipo di pipe.**](pipe.md)

La sintassi della stringa della porta di trasporto TCP/IP, come tutte le stringhe di porta, è definita indipendentemente dalla specifica IDL. Il compilatore esegue alcuni controlli della sintassi, ma non garantisce che la specifica dell'endpoint sia corretta. Alcuni errori possono essere segnalati in fase di esecuzione anziché in fase di compilazione.

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

[**Endpoint**](endpoint.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ at \_ dsp**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ dnet \_ nsp**](ncacn-dnet-nsp.md)
</dt> <dt>

[**ncacn \_ ip \_ tcp**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ nb \_ ipx**](ncacn-nb-ipx.md)
</dt> <dt>

[**ncacn \_ spx**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ nb \_ nb**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ nb \_ tcp**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ vns \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[Associazione di stringhe](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 