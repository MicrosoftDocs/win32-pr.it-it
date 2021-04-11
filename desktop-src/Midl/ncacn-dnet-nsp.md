---
title: attributo ncacn_dnet_nsp
description: La \_ \_ parola chiave ncacn DNET NSP identifica DECnet come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.
ms.assetid: 797251c1-c5d3-416b-8bc7-5b83bb7027e6
keywords:
- attributo ncacn_dnet_nsp MIDL
topic_type:
- apiref
api_name:
- ncacn_dnet_nsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6312aff15d3bdef85d1e37829d669ce1faa5fbb4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117714"
---
# <a name="ncacn_dnet_nsp-attribute"></a>ncacn \_ DNET- \_ attributo NSP

La parola chiave **ncacn \_ DNET \_ NSP** identifica DECnet come famiglia di protocolli per l'endpoint. Questa famiglia di protocolli è obsoleta e non deve essere utilizzata nelle nuove applicazioni.

``` syntax
endpoint("ncacn_dnet_nsp:server-name[port-name]")
```

## <a name="parameters"></a>Parametri

<dl> <dt>

*nome server* 
</dt> <dd>

Specifica il nome o l'indirizzo Internet per il server, o host, computer. Il nome è una stringa di caratteri.

</dd> <dt>

*nome porta* 
</dt> <dd>

Specifica un nome di oggetto o un numero di oggetto DECnet. Il nome dell'oggetto può essere composto da un massimo di 16 caratteri. I numeri degli oggetti possono essere preceduti dal simbolo di cancelletto ( \# ).

</dd> </dl>

## <a name="remarks"></a>Commenti

La sintassi della stringa della porta di trasporto DECnet, come tutte le stringhe di porta, viene definita indipendentemente dalla specifica IDL. Il compilatore esegue alcune verifiche della sintassi, ma non garantisce che la specifica dell'endpoint sia corretta. È possibile che alcuni errori vengano segnalati in fase di esecuzione anziché in fase di compilazione.

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

[**endpoint**](endpoint.md)
</dt> <dt>

[**Associazione stringa**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 