---
description: Enumerazione StreamQualityProperty usata dai metodi ITStreamQualityControl::GetRange, ITStreamQualityControl::Get e ITStreamQualityControl::Set per indicare la proprietà di qualità del flusso da risolvere.
ms.assetid: 28c9257f-6fbb-440f-9b84-c15a74229b5b
title: Enumerazione StreamQualityProperty (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea006b614522ffcab6f96e630df03087b78864ff7d7af6ddcd5c515bc090e821
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905751"
---
# <a name="streamqualityproperty-enumeration"></a>Enumerazione StreamQualityProperty

\[Questa enumerazione non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

Enumerazione **StreamQualityProperty** usata dai metodi [**ITStreamQualityControl::GetRange**](itstreamqualitycontrol-getrange.md), [**ITStreamQualityControl::Get**](itstreamqualitycontrol-get.md)e [**ITStreamQualityControl::Set**](itstreamqualitycontrol-set.md) per indicare la proprietà di qualità del flusso da risolvere.

## <a name="syntax"></a>Sintassi


```C++
} StreamQualityProperty;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="StreamQuality_MaxBitrate"></span><span id="streamquality_maxbitrate"></span><span id="STREAMQUALITY_MAXBITRATE"></span>**StreamQuality \_ MaxBitrate**
</dt> <dd>

Velocità in bit massima.

</dd> <dt>

<span id="StreamQuality_CurrBitrate"></span><span id="streamquality_currbitrate"></span><span id="STREAMQUALITY_CURRBITRATE"></span>**\_CurrBitrate di StreamQuality**
</dt> <dd>

Velocità in bit minima.

</dd> <dt>

<span id="StreamQuality_MinFrameInterval"></span><span id="streamquality_minframeinterval"></span><span id="STREAMQUALITY_MINFRAMEINTERVAL"></span>**StreamQuality \_ MinFrameInterval**
</dt> <dd>

Intervallo massimo di fotogrammi.

</dd> <dt>

<span id="StreamQuality_AvgFrameInterval"></span><span id="streamquality_avgframeinterval"></span><span id="STREAMQUALITY_AVGFRAMEINTERVAL"></span>**\_AvgFrameInterval di StreamQuality**
</dt> <dd>

Intervallo di fotogrammi minimo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.1<br/>                                                       |
| Intestazione<br/>       | <dl> <dt>Ipmsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITStreamQualityControl::GetRange**](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[**ITStreamQualityControl::Get**](itstreamqualitycontrol-get.md)
</dt> <dt>

[**ITStreamQualityControl::Set**](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




