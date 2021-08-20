---
title: delete iplisten
description: Specifica un indirizzo IPv4 o IPv6 da eliminare dall'elenco di ascolto IP.
ms.assetid: 1d0935a5-77de-4fdf-8d3b-88c8578bd5c7
keywords:
- delete iplisten HTTP
topic_type:
- apiref
api_name:
- delete iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42dbe9716ae19fdbbfb8f147b0f5f7f5a592adbf7b241c2f4e4548e0ee7e6e7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014869"
---
# <a name="delete-iplisten"></a>delete iplisten

Specifica un indirizzo IPv4 o IPv6 da eliminare dall'elenco di ascolto IP.

``` syntax
delete iplisten [ address=] IPAddress
 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[ address= \]** *IPAddress*
</dt> <dd>

Specifica l'indirizzo IPv4 o IPv6 da eliminare dall'elenco di ascolto IP.

</dd> </dl>

## <a name="remarks"></a>Commenti

Elimina un indirizzo IP nell'elenco di ascolto IP. Il numero di porta non è incluso. Questo elenco viene usato per definire l'ambito dell'elenco di indirizzi a cui viene eseguito il binding del servizio HTTP. "0.0.0.0" indica qualsiasi indirizzo IPv4 e "::" indica qualsiasi indirizzo IPv6.

## <a name="examples"></a>Esempio

**delete iplisten address=fe80::1**

**delete iplisten address=1.1.1.1**

**delete iplisten address=0.0.0.0**

**delete iplisten address=::**

 

 




