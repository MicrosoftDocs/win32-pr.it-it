---
title: ncacn_ip_tcp attributo
description: La parola chiave ncacn \_ ip tcp identifica TCP/IP come famiglia di protocolli per \_ l'endpoint.
ms.assetid: 8142c667-9a5f-4066-a36d-1bb5ce551d21
keywords:
- ncacn_ip_tcp attributo MIDL
topic_type:
- apiref
api_name:
- ncacn_ip_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c34ba0a872af79245469818121761a38d356316b53a31743f9ebf2cd66f72325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642231"
---
# <a name="ncacn_ip_tcp-attribute"></a>Attributo tcp ip ncacn \_ \_

La **parola chiave ncacn \_ ip \_ tcp** identifica TCP/IP come famiglia di protocolli per l'endpoint.

``` syntax
endpoint("ncacn_ip_tcp:server-name[port-name]")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*server-name* 
</dt> <dd>

Specifica il nome o l'indirizzo Internet per il server o l'host del computer. Il nome è una stringa di caratteri. L'indirizzo Internet è una notazione di indirizzi Internet comune.

</dd> <dt>

*port-name* 
</dt> <dd>

Specifica un numero facoltativo a 16 bit. I valori minori di 1024 sono in genere riservati. Se non viene specificato alcun valore, il servizio di mapping degli endpoint seleziona un valore *di nome porta* valido.

</dd> </dl>

## <a name="remarks"></a>Commenti

La sintassi della stringa di porta del trasporto TCP/IP, come tutte le stringhe di porta, è definita indipendentemente dalla specifica IDL. Il compilatore esegue un controllo della sintassi, ma non garantisce che la specifica dell'endpoint sia corretta. Alcuni errori possono essere segnalati in fase di esecuzione anziché in fase di compilazione.

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

[**Endpoint**](endpoint.md)
</dt> <dt>

[File di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**ncacn \_ nb \_ tcp**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncacn \_ spx**](ncacn-spx.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**associazione di stringhe**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 