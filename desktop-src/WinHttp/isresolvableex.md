---
description: Determina se una determinata stringa host può essere risolta in un indirizzo IP.
ms.assetid: 83e52ca7-2ea0-419d-b09d-9301c1982b98
title: isResolvableEx (funzione)
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
ms.openlocfilehash: 1172aaed93a9fc6cede5ae5393c5dd430613a466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317011"
---
# <a name="isresolvableex-function"></a>isResolvableEx (funzione)

Determina se una determinata stringa host può essere risolta in un indirizzo IP.

## <a name="parameters"></a>Parametri

<dl> <dt>

*host* 
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

[Definizioni API helper proxy compatibili con IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Estensioni IPv6 per il formato di file di configurazione automatica dello strumento di navigazione](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



