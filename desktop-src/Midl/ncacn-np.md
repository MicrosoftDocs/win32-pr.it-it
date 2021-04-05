---
title: attributo ncacn_np
description: La \_ parola chiave ncacn NP identifica le named pipe come famiglia di protocolli per l'endpoint.
ms.assetid: 02961bb8-faf0-42e5-b134-dd2983e6d146
keywords:
- attributo ncacn_np MIDL
topic_type:
- apiref
api_name:
- ncacn_np
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84634e6bb5d2b634439be767ad44749291cffe11
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726735"
---
# <a name="ncacn_np-attribute"></a>\_attributo NP ncacn

La parola chiave **ncacn \_ NP** identifica le named pipe come famiglia di protocolli per l'endpoint.

``` syntax
endpoint("ncacn_np:server-name[\\pipe\\pipe-name]")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*nome server* 
</dt> <dd>

facoltativo. Specifica il nome del server. I caratteri barra rovesciata sono facoltativi.

</dd> <dt>

*Nome pipe* 
</dt> <dd>

Specifica un nome di pipe valido. Un nome di pipe valido è una stringa contenente gli identificatori separati da una barra rovesciata. Il primo identificatore deve essere [**pipe**](pipe.md). Ogni identificatore deve essere separato da due caratteri di barra rovesciata.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un server crea un'istanza di un named pipe che è quindi disponibile per tutti i client. Quando un client tenta di connettersi, l'istanza esistente è associata a tale client. Prima che un altro client possa connettersi, il server deve creare un'altra istanza del named pipe. Se un client tenta di eseguire l'associazione al server prima della creazione della nuova istanza, la chiamata di binding, [**errore in RpcBindingFromStringBinding**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding), potrebbe non riuscire e il server RPC del messaggio di errore è \_ \_ \_ troppo \_ occupato. Pertanto, è necessario assicurarsi che l'applicazione client gestisca il caso in cui il server è troppo occupato per accettare una connessione. Il client deve riprovare automaticamente, richiedere all'utente una linea di condotta o non riuscire normalmente.

La sintassi della stringa della porta named pipe, come tutte le stringhe di porta, viene definita dall'implementazione del trasporto ed è indipendente dalla specifica IDL. Il compilatore MIDL esegue un controllo della sintassi limitato, ma non garantisce che la specifica dell'endpoint sia corretta. Alcune classi di errori possono essere segnalate in fase di esecuzione anziché in fase di compilazione.

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_np:[\\pipe\\stove\\hat]") 
] 
interface iface1
{
    // Interface definition statements.
}

[
    uuid(87654321-4000-2006-0000-20000000001b), 
    version(1.1), 
    endpoint("ncacn_np:\\\\myotherserver[\\pipe\\corncob]") 
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

[**ncacn \_ le reti virtuali \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[**\_UDP IP \_ ncadg**](ncadg-ip-udp.md)
</dt> <dt>

[**Associazione stringa**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 