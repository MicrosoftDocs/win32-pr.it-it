---
title: show sslcert
description: Elenca i binding del certificato server SSL e i criteri dei certificati client corrispondenti per un indirizzo IP e una porta.
ms.assetid: 8e20f55e-a357-4f9c-a24e-e234607c3196
keywords:
- Mostra HTTP sslcert
topic_type:
- apiref
api_name:
- show sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71c2faf370066f5ce8d5ce6a20b173a74d0f645
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "104335060"
---
# <a name="show-sslcert"></a>show sslcert

Elenca i binding del certificato server SSL e i criteri dei certificati client corrispondenti per un indirizzo IP e una porta.

``` syntax
show sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport = \] * * * indirizzo IP: porta*
</dt> <dd>

Specifica l'indirizzo IPv4 o IPv6 e la porta per cui verranno visualizzate le associazioni di certificati SSL. Se non si specifica un ipport, vengono elencati tutti i binding.

</dd> </dl>

## <a name="examples"></a>Esempio

**Mostra sslcert ipport = \[ FE80:: 1 \] : 443**

**show sslcert ipport=1.1.1.1:443**

**show sslcert ipport=0.0.0.0:443**

**Mostra sslcert ipport = \[ :: \] : 443**

 

 




