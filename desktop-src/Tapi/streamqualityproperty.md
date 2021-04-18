---
description: 'Enumerazione StreamQualityProperty usata dai metodi ITStreamQualityControl:: GetRange, ITStreamQualityControl:: Get e ITStreamQualityControl:: set per indicare la proprietà della qualità del flusso da risolvere.'
ms.assetid: 28c9257f-6fbb-440f-9b84-c15a74229b5b
title: Enumerazione StreamQualityProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f552641cd0847bb3ff8eec9d528a03171a78c2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333863"
---
# <a name="streamqualityproperty-enumeration"></a>Enumerazione StreamQualityProperty

\[ Questa enumerazione non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Enumerazione **StreamQualityProperty** usata dai metodi [**ITStreamQualityControl:: GetRange**](itstreamqualitycontrol-getrange.md), [**ITStreamQualityControl:: Get**](itstreamqualitycontrol-get.md)e [**ITStreamQualityControl:: set**](itstreamqualitycontrol-set.md) per indicare la proprietà della qualità del flusso da risolvere.

## <a name="syntax"></a>Sintassi


```C++
} StreamQualityProperty;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="StreamQuality_MaxBitrate"></span><span id="streamquality_maxbitrate"></span><span id="STREAMQUALITY_MAXBITRATE"></span>**\_MaxBitrate StreamQuality**
</dt> <dd>

Velocità in bit massima.

</dd> <dt>

<span id="StreamQuality_CurrBitrate"></span><span id="streamquality_currbitrate"></span><span id="STREAMQUALITY_CURRBITRATE"></span>**\_CurrBitrate StreamQuality**
</dt> <dd>

Velocità in bit minima.

</dd> <dt>

<span id="StreamQuality_MinFrameInterval"></span><span id="streamquality_minframeinterval"></span><span id="STREAMQUALITY_MINFRAMEINTERVAL"></span>**\_MinFrameInterval StreamQuality**
</dt> <dd>

Intervallo massimo di frame.

</dd> <dt>

<span id="StreamQuality_AvgFrameInterval"></span><span id="streamquality_avgframeinterval"></span><span id="STREAMQUALITY_AVGFRAMEINTERVAL"></span>**\_AvgFrameInterval StreamQuality**
</dt> <dd>

Intervallo minimo frame.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,1<br/>                                                       |
| Intestazione<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITStreamQualityControl:: GetRange**](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[**ITStreamQualityControl:: Get**](itstreamqualitycontrol-get.md)
</dt> <dt>

[**ITStreamQualityControl:: set**](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




