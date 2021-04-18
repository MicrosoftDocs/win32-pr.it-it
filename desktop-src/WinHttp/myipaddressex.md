---
description: Trova tutti gli indirizzi IP per localhost.
ms.assetid: 47f7d03e-c1a1-4395-9889-01891208fe0f
title: myIPAddressEx (funzione)
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
ms.openlocfilehash: 88c205dbd5ce071a809cf87f4f97bb6d42120dcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314109"
---
# <a name="myipaddressex-function"></a>myIPAddressEx (funzione)

Trova tutti gli indirizzi IP per localhost.

## <a name="parameters"></a>Parametri

Questa funzione non ha parametri.

## <a name="return-value"></a>Valore restituito

Stringa delimitata da punto e virgola che contiene tutti gli indirizzi IP per localhost (IPv6 e/o IPv4) o una stringa vuota se non è possibile risolvere localhost in un indirizzo IP.

## <a name="remarks"></a>Commenti

Gli implementatori di FindProxyforURLEx devono aggiungere codice che suddivide la stringa di indirizzi IP delimitati da punto e virgola in indirizzi distinti.

## <a name="examples"></a>Esempi

``` syntax
myIpAddressEx();
    would return the string "fe80::380c:2e71:f5b9:a3b5%15;fe80::982d:a3b3:97ad:7dd0%9;2001:4898:28:7:982d:a3b3:97ad:7dd0;2001:4898:28:7:adfe:a643:8130:2fdc;fe80::5efe:10.70.92.74%13;3ffe:8311:ffff:f70f:0:5efe:10.70.92.74;10.70.92.74;3ffe:831f:4136:e37e:380c:2e71:f5b9:a3b5" 
    if you were running on that host.
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Definizioni API helper proxy compatibili con IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Estensioni IPv6 per il formato di file di configurazione automatica dello strumento di navigazione](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



