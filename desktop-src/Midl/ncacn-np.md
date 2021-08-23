---
title: ncacn_np attributo
description: La parola chiave np ncacn \_ identifica le named pipe come famiglia di protocolli per l'endpoint.
ms.assetid: 02961bb8-faf0-42e5-b134-dd2983e6d146
keywords:
- ncacn_np attributo MIDL
topic_type:
- apiref
api_name:
- ncacn_np
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7acf294241c1d38b2067ba54e315fc3240e5bb6eca81a6b12012f8dec457a8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013759"
---
# <a name="ncacn_np-attribute"></a>Attributo \_ np ncacn

La **parola chiave \_ np ncacn** identifica le named pipe come famiglia di protocolli per l'endpoint.

``` syntax
endpoint("ncacn_np:server-name[\\pipe\\pipe-name]")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*server-name* 
</dt> <dd>

facoltativo. Specifica il nome del server. I caratteri barra rovesciata sono facoltativi.

</dd> <dt>

*pipe-name* 
</dt> <dd>

Specifica un nome di pipe valido. Un nome di pipe valido è una stringa contenente identificatori separati da caratteri barra rovesciata. Il primo identificatore deve essere [**pipe**](pipe.md). Ogni identificatore deve essere separato da due barre rovesciate.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un server crea un'istanza di un named pipe che è quindi disponibile per qualsiasi client. Quando un client tenta di connettersi, l'istanza esistente viene associata a tale client. Prima che un altro client possa connettersi, il server deve creare un'altra istanza del named pipe. Se un client tenta di eseguire l'associazione al server prima della creazione della nuova istanza, la chiamata di associazione [**RpcBindingFromStringBinding**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingfromstringbinding)potrebbe non riuscire con il messaggio di errore RPC \_ S SERVER TOO \_ \_ \_ BUSY. È quindi necessario assicurarsi che l'applicazione client gestisca il caso in cui il server è troppo occupato per accettare una connessione. Il client deve riprovare automaticamente, richiedere all'utente un corso di azione o non riuscire correttamente.

La sintassi della stringa di porta named pipe, come tutte le stringhe di porta, è definita dall'implementazione del trasporto ed è indipendente dalla specifica IDL. Il compilatore MIDL esegue un controllo della sintassi limitato, ma non garantisce che la specifica dell'endpoint sia corretta. Alcune classi di errori possono essere segnalate in fase di esecuzione anziché in fase di compilazione.

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

[**Endpoint**](endpoint.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ in \_ dsp**](ncacn-at-dsp.md)
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

[**ncacn \_ vns \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[**associazione di stringhe**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 