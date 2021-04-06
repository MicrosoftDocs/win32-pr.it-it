---
title: delete iplisten
description: Specifica un indirizzo IPv4 o IPv6 da eliminare dall'elenco di ascolto IP.
ms.assetid: 1d0935a5-77de-4fdf-8d3b-88c8578bd5c7
keywords:
- Elimina HTTP iplisten
topic_type:
- apiref
api_name:
- delete iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed7356d8dea3b4313a46c7d7906de15b7389edc
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "104045969"
---
# <a name="delete-iplisten"></a>delete iplisten

Specifica un indirizzo IPv4 o IPv6 da eliminare dall'elenco di ascolto IP.

``` syntax
delete iplisten [ address=] IPAddress
 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[ Address = \]** *IPAddress*
</dt> <dd>

Specifica l'indirizzo IPv4 o IPv6 da eliminare dall'elenco di ascolto IP.

</dd> </dl>

## <a name="remarks"></a>Commenti

Elimina un indirizzo IP nell'elenco di ascolto IP. Il numero di porta non è incluso. Questo elenco viene usato per definire l'ambito dell'elenco di indirizzi a cui viene eseguito il binding del servizio HTTP. "0.0.0.0" indica qualsiasi indirizzo IPv4 e "::" indica qualsiasi indirizzo IPv6.

## <a name="examples"></a>Esempio

**Elimina indirizzo iplisten = FE80:: 1**

**Elimina indirizzo iplisten = 1.1.1.1**

**Elimina indirizzo iplisten = 0.0.0.0**

**Elimina indirizzo iplisten =::**

 

 




