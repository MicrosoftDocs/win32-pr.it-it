---
title: Attributo ncalrpc
description: La parola chiave ncalrpc identifica la comunicazione interprocesso locale come famiglia di protocolli per l'endpoint. Questa parola chiave è uno dei nomi di famiglia di protocolli validi che devono essere usati con l'attributo \ endpoint\.
ms.assetid: 0009f794-5c14-4484-9023-cb20c7030dc5
keywords:
- Attributo ncalrpc MIDL
topic_type:
- apiref
api_name:
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481f005a741c6a815572f5861755f52d5921bae89e8bb2d8a3ef757a0fc42d9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067001"
---
# <a name="ncalrpc-attribute"></a>Attributo ncalrpc

La **parola chiave ncalrpc** identifica la comunicazione interprocesso locale come famiglia di protocolli per l'endpoint. Questa parola chiave è uno dei nomi di famiglia di protocolli validi che devono essere usati con **\[** [**l'attributo endpoint.**](endpoint.md) **\]**

``` syntax
endpoint("ncalrpc:[port-name]")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*port-name* 
</dt> <dd>

Stringa di caratteri che specifica la porta di comunicazione (un'applicazione, un servizio o un'istanza di un servizio) utilizzata da un client per effettuare chiamate interprocesso a un server. La stringa può contenere fino a 53 caratteri e non deve contenere alcuna barra rovesciata ( \\ ). Il nome del computer non deve essere usato con la **parola chiave ncalrpc.**

</dd> </dl>

## <a name="remarks"></a>Commenti

La sintassi della stringa di porta interprocess-communication locale, come tutte le stringhe di porta, è definita dall'implementazione del trasporto ed è indipendente dalla specifica IDL. Il compilatore MIDL esegue un controllo della sintassi limitato, ma non garantisce che la specifica dell'endpoint sia corretta. Alcune classi di errori possono essere segnalate in fase di esecuzione anziché in fase di compilazione.

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncalrpc:[myapplicationname]") 
] 
interface iface
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

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ vns \_ spp**](ncacn-vns-spp.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[Associazione di stringhe](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 