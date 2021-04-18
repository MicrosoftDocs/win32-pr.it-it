---
title: attributo ncacn_ip_tcp
description: La \_ \_ parola chiave TCP IP ncacn identifica TCP/IP come famiglia di protocolli per l'endpoint.
ms.assetid: 8142c667-9a5f-4066-a36d-1bb5ce551d21
keywords:
- attributo ncacn_ip_tcp MIDL
topic_type:
- apiref
api_name:
- ncacn_ip_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adb57951e862ebcdfa6889aae170bfdf5a14f96
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299776"
---
# <a name="ncacn_ip_tcp-attribute"></a>\_ \_ attributo TCP IP ncacn

La parola chiave **\_ \_ TCP IP ncacn** identifica TCP/IP come famiglia di protocolli per l'endpoint.

``` syntax
endpoint("ncacn_ip_tcp:server-name[port-name]")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*nome server* 
</dt> <dd>

Specifica il nome o l'indirizzo Internet per il server, o host, computer. Il nome è una stringa di caratteri. L'indirizzo Internet è una nota comune di indirizzo Internet.

</dd> <dt>

*nome porta* 
</dt> <dd>

Specifica un numero facoltativo a 16 bit. I valori minori di 1024 sono generalmente riservati. Se non viene specificato alcun valore, il servizio di mapping degli endpoint seleziona un valore valido per il *nome di porta* .

</dd> </dl>

## <a name="remarks"></a>Commenti

La sintassi della stringa della porta di trasporto TCP/IP, come tutte le stringhe di porta, viene definita indipendentemente dalla specifica IDL. Il compilatore esegue alcune verifiche della sintassi, ma non garantisce che la specifica dell'endpoint sia corretta. È possibile che alcuni errori vengano segnalati in fase di esecuzione anziché in fase di compilazione.

## <a name="examples"></a>Esempi

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_ip_tcp:rainier[1404]") 
]
interface iface
{
    // Interface definition statements.
}

 
endpoint("ncacn_ip_tcp:128.10.2.30[1404]")
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[**endpoint**](endpoint.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ NB \_ TCP**](ncacn-nb-tcp.md)
</dt> <dt>

[**\_NP ncacn**](ncacn-np.md)
</dt> <dt>

[**\_SPX ncacn**](ncacn-spx.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**Associazione stringa**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 