---
description: Ottiene la versione del motore di elaborazione WPAD.
ms.assetid: f9e9a867-d491-4d46-bbd8-c0c3d8d5b3d6
title: getClientVersion (funzione)
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
ms.openlocfilehash: e0bcf439c8a282e42a28126824ffb70630a341e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882874"
---
# <a name="getclientversion-function"></a>getClientVersion (funzione)

Ottiene la versione del motore di elaborazione WPAD.

## <a name="parameters"></a>Parametri

<dl> <dt>

*IpAddress* 
</dt> <dd>

Stringa delimitata da punto e virgola contenente indirizzi IP.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Elenco di indirizzi IP delimitati da punti e virgola o una stringa vuota se non è possibile ordinare l'elenco di indirizzi IP.

## <a name="remarks"></a>Commenti

Attualmente questa funzione restituisce la versione 1,0.

Microsoft ha aggiunto questa funzione per consentire agli amministratori IT di aggiornare gli script WPAD per l'uso di versioni diverse del motore di elaborazione WPAD senza causare interruzioni della distribuzione esistente. Se ad esempio Microsoft ha aggiunto una funzione alla versione 2,0 del motore WPAD, gli amministratori possono verificare la versione prima di tentare di chiamare tale funzione. Questo consente di usare lo script con il client che esegue le versioni 1,0 e 2,0 del motore WPAD.

## <a name="examples"></a>Esempi

``` syntax
getClientVersion();
    returns the appropriate versions number of the WPAD engine.
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Definizioni API helper proxy compatibili con IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Estensioni IPv6 per il formato di file di configurazione automatica dello strumento di navigazione](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



