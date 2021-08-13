---
title: ncacn_nb_ipx attributo
description: La parola chiave ncacn \_ nb ipx identifica \_ NetBIOS su IPX come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere usata nelle nuove applicazioni.
ms.assetid: 641471d4-eba4-4d4a-a3fe-1e40b3751e38
keywords:
- ncacn_nb_ipx attributo MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_ipx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c8be67485d86a6094e2a41c01d5e0cf78cdabe5e251a3ab9ae046a47ed05d6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642223"
---
# <a name="ncacn_nb_ipx-attribute"></a>ncacn \_ nb \_ ipx attribute

La **parola chiave ncacn \_ nb \_ ipx** identifica NetBIOS su IPX come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere usata nelle nuove applicazioni.

``` syntax
endpoint("ncacn_nb_ipx:[port-name]")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*port-name* 
</dt> <dd>

Specifica un valore facoltativo a 8 bit compreso tra 1 e 254. I valori minori di 0x20 sono riservati. Se il *valore port-name* non è specificato, il servizio di mapping degli endpoint seleziona il valore della porta.

</dd> </dl>

## <a name="remarks"></a>Commenti

La sintassi della stringa di porta NetBIOS, come tutte le stringhe di porta, è definita dall'implementazione del trasporto ed è indipendente dalla specifica IDL. Il compilatore MIDL esegue un controllo della sintassi limitato, ma non garantisce che la specifica dell'endpoint sia corretta. Alcune classi di errori possono essere segnalate in fase di esecuzione anziché in fase di compilazione.

> [!Note]  
> Questa famiglia di protocolli non è supportata in Windows XP.

 

## <a name="examples"></a>Esempi

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_nb_ipx:[100]") 
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

[**ncacn \_ ip \_ tcp**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ nb \_ tcp**](ncacn-nb-tcp.md)
</dt> <dt>

[**ncacn \_ nb \_ nb**](ncacn-nb-nb.md)
</dt> <dt>

[**ncacn \_ in \_ dsp**](ncacn-at-dsp.md)
</dt> <dt>

[**ncacn \_ spx**](ncacn-spx.md)
</dt> <dt>

[**ncacn \_ np**](ncacn-np.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**ncadg \_ ip \_ udp**](ncadg-ip-udp.md)
</dt> <dt>

[**ncadg \_ ipx**](ncadg-ipx.md)
</dt> <dt>

[**associazione di stringhe**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 