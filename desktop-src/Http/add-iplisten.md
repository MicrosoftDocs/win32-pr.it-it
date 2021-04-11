---
title: add iplisten
description: Specifica un indirizzo IPv4 o IPv6 da aggiungere all'elenco di ascolto IP.
ms.assetid: 38253818-c029-4a46-ab52-095cbfdeeaf4
keywords:
- Aggiungi iplisten HTTP
topic_type:
- apiref
api_name:
- add iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6090d3044be134035edb5f1f42a9790859d0301d
ms.sourcegitcommit: 243954e695c6ab5372b2935b095c3cd0b1202e16
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "103956241"
---
# <a name="add-iplisten"></a>add iplisten

Specifica un indirizzo IPv4 o IPv6 da aggiungere all'elenco di ascolto IP.

``` syntax
add iplisten [ ipaddress=] IPAddress
 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="__ipaddress___IPAddress"></span><span id="__ipaddress___ipaddress"></span><span id="__ipADDRESS___IPADDRESS"></span>**\[ IPAddress = \]** *IPAddress*
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

 

 




