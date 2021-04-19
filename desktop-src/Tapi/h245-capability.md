---
description: L' \_ enumerazione della funzionalità h245 descrive il supporto del formato audio e video.
ms.assetid: 76aeb3a1-3233-4425-b9db-efacbedc309e
title: Enumerazione H245_CAPABILITY (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7a6f81f87480f221f87680d9cf086120deb2de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332823"
---
# <a name="h245_capability-enumeration"></a>\_Enumerazione della funzionalità h245

\[**H245 \_ La funzionalità** non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'enumerazione della **\_ funzionalità h245** descrive il supporto del formato audio e video.

## <a name="syntax"></a>Sintassi


```C++
} H245_CAPABILITY;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="HC_G711"></span><span id="hc_g711"></span>**\_G711 HC**
</dt> <dd>

Il protocollo audio G. 711 è supportato.

</dd> <dt>

<span id="HC_G723"></span><span id="hc_g723"></span>**\_G723 HC**
</dt> <dd>

Il protocollo audio G. 723 è supportato.

</dd> <dt>

<span id="HC_H263QCIF"></span><span id="hc_h263qcif"></span>**\_H263QCIF HC**
</dt> <dd>

Il protocollo video H. 263 è supportato.

</dd> <dt>

<span id="HC_H261QCIF"></span><span id="hc_h261qcif"></span>**\_H261QCIF HC**
</dt> <dd>

Il protocollo video H. 263 è supportato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|---------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,0 o versione successiva<br/>                                                 |
| Intestazione<br/>       | <dl> <dt>H323priv. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IH323LineEx::SetDefaultCapabilityPreferrence**](ih323lineex-setdefaultcapabilitypreferrence.md)
</dt> </dl>

 

 




