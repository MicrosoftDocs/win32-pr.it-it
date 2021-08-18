---
description: Ottiene la versione del motore di elaborazione WPAD.
ms.assetid: f9e9a867-d491-4d46-bbd8-c0c3d8d5b3d6
title: Funzione getClientVersion
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
ms.openlocfilehash: 33aeb4bd59730c48407220fede0cec0a606614f4a9692cd0e9852d56757a7f9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133214"
---
# <a name="getclientversion-function"></a>Funzione getClientVersion

Ottiene la versione del motore di elaborazione WPAD.

## <a name="parameters"></a>Parametri

<dl> <dt>

*IpAddressList* 
</dt> <dd>

Stringa delimitata da punto e virgola contenente gli indirizzi IP.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Elenco di indirizzi IP delimitati da punti e virgola ordinati o una stringa vuota se non è possibile ordinare l'elenco di indirizzi IP.

## <a name="remarks"></a>Commenti

Attualmente questa funzione restituisce la versione 1.0.

Microsoft ha aggiunto questa funzione per consentire agli amministratori IT di aggiornare gli script WPAD in modo da usare versioni diverse del motore di elaborazione WPAD senza causare interruzioni della distribuzione esistente. Ad esempio, se Microsoft ha aggiunto una funzione alla versione 2.0 del motore WPAD, gli amministratori possono controllare la versione prima di tentare di chiamare tale funzione. In questo modo, lo script può funzionare con il client che esegue le versioni 1.0 e 2.0 del motore WPAD.

## <a name="examples"></a>Esempi

``` syntax
getClientVersion();
    returns the appropriate versions number of the WPAD engine.
```

## <a name="see-also"></a>Vedere anche

<dl> <dt>

[Definizioni dell'API helper proxy con supporto IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Estensioni IPv6 per il formato di file di configurazione automatica dello strumento di navigazione](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



