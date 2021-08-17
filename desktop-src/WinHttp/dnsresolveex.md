---
description: Risolvere una stringa host nel relativo indirizzo IP
ms.assetid: 32d70f10-803b-484d-a9e0-d4c61a8d897f
title: Funzione dnsResolveEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- dnsResolveEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: f0f0100367d4fad6d6e0b013e5d552f733086e6ddd5bc720779ef1fb5b65cdce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133224"
---
# <a name="dnsresolveex-function"></a>Funzione dnsResolveEx

Risolvere una stringa host nel relativo indirizzo IP

## <a name="parameters"></a>Parametri

<dl> <dt>

*Host* 
</dt> <dd>

Stringa contenente l'host HTTP fornito a FindProxyForUrl.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Stringa delimitata da punto e virgola contenente indirizzi IPv6 e IPv4 o una stringa vuota se l'host non è risolvibile.

## <a name="remarks"></a>Commenti

Gli implementatori di FindProxyforURLEx devono aggiungere codice che suddivide la stringa di indirizzi IP delimitati da punto e virgola in indirizzi separati.

## <a name="examples"></a>Esempi

``` syntax
dnsResolveEx("testmachine1");
    returns the string "fe80::380c:2e71:f5b9:a3b5%15;fe80::982d:a3b3:97ad:7dd0%9;2001:4898:28:7:982d:a3b3:97ad:7dd0;2001:4898:28:7:adfe:a643:8130:2fdc;fe80::5efe:10.70.92.74%13;3ffe:8311:ffff:f70f:0:5efe:10.70.92.74;10.70.92.74;3ffe:831f:4136:e37e:380c:2e71
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Definizioni dell'API helper proxy con supporto IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Estensioni IPv6 per il formato di file di configurazione automatica dello strumento di navigazione](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



