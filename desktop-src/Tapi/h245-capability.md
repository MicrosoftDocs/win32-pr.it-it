---
description: L'enumerazione H245 CAPABILITY descrive il supporto dei formati \_ audio e video.
ms.assetid: 76aeb3a1-3233-4425-b9db-efacbedc309e
title: H245_CAPABILITY enumerazione (H323priv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1666eb918748696263247f00f0d0e17ac9424e6c4bf85c5574f866bb10e28be1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140554"
---
# <a name="h245_capability-enumeration"></a>Enumerazione CAPABILITY H245 \_

\[**H245 \_ CAPABILITY** non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

**L'enumerazione H245 \_ CAPABILITY** descrive il supporto dei formati audio e video.

## <a name="syntax"></a>Sintassi


```C++
} H245_CAPABILITY;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="HC_G711"></span><span id="hc_g711"></span>**HC \_ G711**
</dt> <dd>

Il protocollo audio G.711 è supportato.

</dd> <dt>

<span id="HC_G723"></span><span id="hc_g723"></span>**HC \_ G723**
</dt> <dd>

Il protocollo audio G.723 è supportato.

</dd> <dt>

<span id="HC_H263QCIF"></span><span id="hc_h263qcif"></span>**HC \_ H263QCIF**
</dt> <dd>

Il protocollo video H.263 è supportato.

</dd> <dt>

<span id="HC_H261QCIF"></span><span id="hc_h261qcif"></span>**HC \_ H261QCIF**
</dt> <dd>

Il protocollo video H.263 è supportato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>H323priv.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IH323LineEx::SetDefaultCapabilityPreferrence**](ih323lineex-setdefaultcapabilitypreferrence.md)
</dt> </dl>

 

 




