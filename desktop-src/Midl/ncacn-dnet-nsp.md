---
title: ncacn_dnet_nsp attributo
description: La parola chiave ncacn \_ dnet \_ nsp identifica DECnet come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere usata nelle nuove applicazioni.
ms.assetid: 797251c1-c5d3-416b-8bc7-5b83bb7027e6
keywords:
- ncacn_dnet_nsp attributo MIDL
topic_type:
- apiref
api_name:
- ncacn_dnet_nsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4fa7448ff9d0cf3946ad3d0293ade19a5c2c0c407ca157d79c2c425f4a8ef6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642762"
---
# <a name="ncacn_dnet_nsp-attribute"></a>ncacn \_ dnet \_ nsp attribute

La **parola chiave ncacn \_ dnet \_ nsp** identifica DECnet come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere usata nelle nuove applicazioni.

``` syntax
endpoint("ncacn_dnet_nsp:server-name[port-name]")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*server-name* 
</dt> <dd>

Specifica il nome o l'indirizzo Internet per il server o l'host del computer. Il nome è una stringa di caratteri.

</dd> <dt>

*port-name* 
</dt> <dd>

Specifica un nome di oggetto DECnet o un numero di oggetto. Il nome dell'oggetto può essere costituito da un massimo di 16 caratteri. I numeri di oggetto possono essere preceduti dal cancelletto ( \# ).

</dd> </dl>

## <a name="remarks"></a>Commenti

La sintassi della stringa di porta del trasporto DECnet, come tutte le stringhe di porta, è definita indipendentemente dalla specifica IDL. Il compilatore esegue un controllo della sintassi, ma non garantisce che la specifica dell'endpoint sia corretta. Alcuni errori possono essere segnalati in fase di esecuzione anziché in fase di compilazione.

> [!Note]  
> Questa famiglia di protocolli non è supportata in Windows XP.

 

## <a name="examples"></a>Esempi

``` syntax
[   
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[RPC0034501]") 
interface iface
{
    // Interface definition statements.
}

[
    uuid(12345678-1234-1234-1234-123456789ABC), 
    version(1.1), 
    endpoint("ncacn_dnet_nsp:node[#41]") 
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

[**associazione di stringhe**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 