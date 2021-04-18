---
description: Ordina un elenco di indirizzi IP.
ms.assetid: 1266d6f3-e9f5-4e6b-9431-7329df156f0a
title: sortIpAddressList (funzione)
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
ms.openlocfilehash: 600d87a58248aafdef5b0a8a7f284f4094c95780
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305582"
---
# <a name="sortipaddresslist-function"></a>sortIpAddressList (funzione)

Ordina un elenco di indirizzi IP.

## <a name="parameters"></a>Parametri

<dl> <dt>

*IpAddress* 
</dt> <dd>

Stringa delimitata da punto e virgola contenente indirizzi IP.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Elenco di indirizzi IP delimitati da punti e virgola o una stringa vuota se non è possibile ordinare l'elenco di indirizzi IP.

## <a name="remarks"></a>Commenti

Gli implementatori di FindProxyforURLEx devono aggiungere codice che suddivide la stringa di indirizzi IP delimitati da punto e virgola in indirizzi distinti.

## <a name="examples"></a>Esempi

``` syntax
sortIpAddressList(2001:4898:28:3:201:2ff:feea:fc14; 
                  157.59.139.22; 
                  fe80::5efe:157.59.139.22");
    returns "fe80::5efe:157.59.139.22;2001:4898:28:3:201:2ff:feea:fc14;157.59.139.22" 
    A list of sorted IP addresses. If there both IPv6 and IPv4 IP addresses are passed as input to this function, then the sorted IPv6 addresses are followed by sorted IPv4 addresses
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Definizioni API helper proxy compatibili con IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Estensioni IPv6 per il formato di file di configurazione automatica dello strumento di navigazione](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



