---
description: Determina se una determinata stringa host può essere risolta in un indirizzo IP.
ms.assetid: 83e52ca7-2ea0-419d-b09d-9301c1982b98
title: Funzione isResolvableEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isResolvableEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 580f5400b59a1142de90843e2be26790aef25a9311f7aa6f732aebeef606c701
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899171"
---
# <a name="isresolvableex-function"></a>Funzione isResolvableEx

Determina se una determinata stringa host può essere risolta in un indirizzo IP.

## <a name="parameters"></a>Parametri

<dl> <dt>

*Host* 
</dt> <dd>

Stringa contenente l'host HTTP fornito a FindProxyForUrl.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

TRUE se l'host è risolvibile in un indirizzo IPv4 o IPv6. in caso contrario, FALSE.

## <a name="examples"></a>Esempi

``` syntax
isResolvableEx(host);
    true if the hostname can be resolved to and IP address 
```

``` syntax
isResolvableEx(host); 
    false if the hostname cannot be resolved to an IP address 
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Definizioni dell'API helper proxy con supporto IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Estensioni IPv6 per il formato di file di configurazione automatica dello strumento di navigazione](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



