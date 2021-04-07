---
title: delete sslcert
description: Elimina i binding del certificato server SSL e i criteri dei certificati client corrispondenti per un indirizzo IP e una porta.
ms.assetid: 2adea7a8-f31f-4c02-8279-7d452e36cd9b
keywords:
- Elimina HTTP sslcert
topic_type:
- apiref
api_name:
- delete sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7672df5eee1634c41ff153435edcbecc58c2595
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "103719003"
---
# <a name="delete-sslcert"></a>delete sslcert

Elimina i binding del certificato server SSL e i criteri dei certificati client corrispondenti per un indirizzo IP e una porta.

``` syntax
delete sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport = \] * * * indirizzo IP: porta*
</dt> <dd>

Specifica l'indirizzo IPv4 o IPv6 e la porta per cui verranno eliminati i binding del certificato SSL.

</dd> </dl>

## <a name="examples"></a>Esempio

**delete sslcert ipport=1.1.1.1:443**

**delete sslcert ipport=0.0.0.0:443**

**Elimina sslcert ipport = \[ :: \] : 443**

 

 




