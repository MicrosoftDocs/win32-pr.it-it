---
title: attributo ncalrpc
description: La parola chiave ncalrpc identifica la comunicazione interprocesso locale come famiglia di protocolli per l'endpoint. Questa parola chiave è uno dei nomi di famiglia di protocollo validi che devono essere usati con l'attributo \ endpoint \.
ms.assetid: 0009f794-5c14-4484-9023-cb20c7030dc5
keywords:
- attributo MIDL di ncalrpc
topic_type:
- apiref
api_name:
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f20ae9e347303288868eeb16758736047fecc1b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963049"
---
# <a name="ncalrpc-attribute"></a>attributo ncalrpc

La parola chiave **ncalrpc** identifica la comunicazione interprocesso locale come famiglia di protocolli per l'endpoint. Questa parola chiave è uno dei nomi di famiglia di protocollo validi che devono essere utilizzati con l' **\[** [](endpoint.md) **\]** attributo endpoint.

``` syntax
endpoint("ncalrpc:[port-name]")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*nome porta* 
</dt> <dd>

Stringa di caratteri che specifica la porta di comunicazione (un'applicazione, un servizio o un'istanza di un servizio) che un client utilizza per eseguire chiamate interprocesso a un server. La stringa può contenere un massimo di 53 caratteri e non deve contenere una barra rovesciata ( \) caratteri. Il nome del computer non deve essere utilizzato con la parola chiave **ncalrpc** .

</dd> </dl>

## <a name="remarks"></a>Commenti

La sintassi della stringa di porta di comunicazione interprocesso locale, come tutte le stringhe di porta, è definita dall'implementazione del trasporto ed è indipendente dalla specifica IDL. Il compilatore MIDL esegue un controllo della sintassi limitato, ma non garantisce che la specifica dell'endpoint sia corretta. Alcune classi di errori possono essere segnalate in fase di esecuzione anziché in fase di compilazione.

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

[**\_UDP IP \_ ncadg**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ IPX**](ncadg-ipx.md)
</dt> <dt>

[Associazione stringa](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 