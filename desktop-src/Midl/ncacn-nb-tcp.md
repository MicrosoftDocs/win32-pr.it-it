---
title: attributo ncacn_nb_tcp
description: La \_ \_ parola chiave ncacn NB TCP viene utilizzata per identificare TCP su NetBIOS come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.
ms.assetid: 3633842c-d1f5-46d9-866e-e54f31415ea5
keywords:
- attributo ncacn_nb_tcp MIDL
topic_type:
- apiref
api_name:
- ncacn_nb_tcp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d59a544c592643cffcb282ba8a0f3fdab48c03fd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337294"
---
# <a name="ncacn_nb_tcp-attribute"></a>ncacn \_ NB- \_ attributo TCP

La parola chiave **ncacn \_ NB \_ TCP** viene utilizzata per identificare TCP su NetBIOS come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.

``` syntax
endpoint("ncacn_nb_tcp:[port-name]")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*nome porta* 
</dt> <dd>

Specifica un valore facoltativo a 8 bit compreso tra 1 e 254. I valori minori di 0x20 sono riservati. Se non si specifica il valore di *nome porta* , il servizio di mapping degli endpoint seleziona il valore di porta.

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
    endpoint("ncacn_nb_tcp:[100]") 
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

[**\_TCP IP \_ ncacn**](ncacn-ip-tcp.md)
</dt> <dt>

[**ncacn \_ NB \_ NB**](ncacn-nb-nb.md)
</dt> <dt>

[**\_NP ncacn**](ncacn-np.md)
</dt> <dt>

[**\_SPX ncacn**](ncacn-spx.md)
</dt> <dt>

[**ncalrpc**](ncalrpc.md)
</dt> <dt>

[**Associazione stringa**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 