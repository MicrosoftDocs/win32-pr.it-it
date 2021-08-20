---
title: add iplisten
description: Specifica un indirizzo IPv4 o IPv6 da aggiungere all'elenco di ascolto IP.
ms.assetid: 38253818-c029-4a46-ab52-095cbfdeeaf4
keywords:
- aggiungere iplisten HTTP
topic_type:
- apiref
api_name:
- add iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2133a3f590c46c9e27b518d7621c158b86895961acb07670f6603e03513d1cc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014979"
---
# <a name="add-iplisten"></a>add iplisten

Specifica un indirizzo IPv4 o IPv6 da aggiungere all'elenco di ascolto IP.

``` syntax
add iplisten [ ipaddress=] IPAddress
 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="__ipaddress___IPAddress"></span><span id="__ipaddress___ipaddress"></span><span id="__ipADDRESS___IPADDRESS"></span>**\[ ipaddress= \]** *IPAddress*
</dt> <dd>

Specifica l'indirizzo IPv4 o IPv6 da aggiungere all'elenco di ascolto IP.

</dd> </dl>

## <a name="remarks"></a>Commenti

Aggiunge un nuovo indirizzo IP all'elenco di ascolto IP. Il numero di porta non è incluso. Questo elenco viene usato per definire l'ambito dell'elenco di indirizzi a cui viene eseguito il binding del servizio HTTP. "0.0.0.0" indica qualsiasi indirizzo IPv4 e "::" indica qualsiasi indirizzo IPv6.

## <a name="examples"></a>Esempio

**add iplisten ipaddress=fe80::1**

**add iplisten ipaddress=1.1.1.1**

**add iplisten ipaddress=0.0.0.0**

**add iplisten ipaddress=::**

 

 




