---
description: Determina se un indirizzo IP si trova in una subnet specifica.
ms.assetid: 2fbfad9c-86b1-44c3-860b-a5c98ac6c2e9
title: Funzione isInNetEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- isInNetEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3a91555370bada5c4bb9257918d0920ac71ac5475c08201f30bf1fbbb4b95c1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114464"
---
# <a name="isinnetex-function"></a>Funzione isInNetEx

Determina se un indirizzo IP si trova in una subnet specifica.

## <a name="parameters"></a>Parametri

<dl> <dt>

*Ipaddress* 
</dt> <dd>

Stringa contenente gli indirizzi IPv6/IPv4.

</dd> <dt>

*IPprefix* 
</dt> <dd>

Stringa contenente il prefisso IP delimitato da due punti con i primi n bit specificati nel campo di bit (ad esempio 3ffe:8311:ffff::/48 o 123.112.0.0/16).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

TRUE se l'host si trova nella stessa subnet. in caso contrario, FALSE.

Restituisce ANCHE FALSE se il prefisso non è nel formato corretto o se nel confronto vengono usati indirizzi e prefissi di tipi diversi, ad esempio un prefisso IPv4 e un indirizzo IPv6.

## <a name="examples"></a>Esempi

``` syntax
isInNetEx(host, "198.95.249.79/32");
    true if the IP address of host matches exactly 198.95.249.79
```

``` syntax
isInNetEx(host, "198.95.0.0/16");
    true if the IP address of the host matches 198.95.*.*
```

``` syntax
isInNetEx(host, "3ffe:8311:ffff::/48");
    true if the IP address of the host matches 3ffe:8311:fff:*:*:*:*:*
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Definizioni dell'API helper proxy con supporto IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Estensioni IPv6 per il formato di file di configurazione automatica dello strumento di navigazione](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



