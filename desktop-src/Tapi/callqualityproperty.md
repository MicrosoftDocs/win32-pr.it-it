---
description: "L'enumerazione CallQualityProperty viene usata dai metodi ITCallQualityControl:: GetRange, ITCallQualityControl:: Get e ITCallQualityControl:: set per indicare la proprietà della qualità della chiamata da risolvere."
ms.assetid: d9a04cc4-9b7d-4b01-918f-e4938c172b8e
title: Enumerazione CallQualityProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2ca3af31e0b85a443bb34ac1992b3d3b5c89bfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329089"
---
# <a name="callqualityproperty-enumeration"></a>Enumerazione CallQualityProperty

\[ Questa enumerazione non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'enumerazione **CallQualityProperty** viene usata dai metodi [**ITCallQualityControl:: GetRange**](itcallqualitycontrol-getrange.md), [**ITCallQualityControl:: Get**](itcallqualitycontrol-get.md)e [**ITCallQualityControl:: set**](itcallqualitycontrol-set.md) per indicare la proprietà della qualità della chiamata da risolvere.

## <a name="syntax"></a>Sintassi


```C++
} CallQualityProperty;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="CallQuality_ControlInterval"></span><span id="callquality_controlinterval"></span><span id="CALLQUALITY_CONTROLINTERVAL"></span>**\_ControlInterval CallQuality**
</dt> <dd>

Intervallo di controllo.

</dd> <dt>

<span id="CallQuality_ConfBitrate"></span><span id="callquality_confbitrate"></span><span id="CALLQUALITY_CONFBITRATE"></span>**\_ConfBitrate CallQuality**
</dt> <dd>

Velocità in bit per la conferenza.

</dd> <dt>

<span id="CallQuality_MaxInputBitrate"></span><span id="callquality_maxinputbitrate"></span><span id="CALLQUALITY_MAXINPUTBITRATE"></span>**\_MaxInputBitrate CallQuality**
</dt> <dd>

Velocità in bit di input massima.

</dd> <dt>

<span id="CallQuality_CurrInputBitrate"></span><span id="callquality_currinputbitrate"></span><span id="CALLQUALITY_CURRINPUTBITRATE"></span>**\_CurrInputBitrate CallQuality**
</dt> <dd>

Velocità in bit di input corrente.

</dd> <dt>

<span id="CallQuality_MaxOutputBitrate"></span><span id="callquality_maxoutputbitrate"></span><span id="CALLQUALITY_MAXOUTPUTBITRATE"></span>**\_MaxOutputBitrate CallQuality**
</dt> <dd>

Velocità in bit di output massima.

</dd> <dt>

<span id="CallQuality_CurrOutputBitrate"></span><span id="callquality_curroutputbitrate"></span><span id="CALLQUALITY_CURROUTPUTBITRATE"></span>**\_CurrOutputBitrate CallQuality**
</dt> <dd>

Velocità in bit di output corrente.

</dd> <dt>

<span id="CallQuality_MaxCPULoad"></span><span id="callquality_maxcpuload"></span><span id="CALLQUALITY_MAXCPULOAD"></span>**\_MaxCPULoad CallQuality**
</dt> <dd>

Carico massimo della CPU.

</dd> <dt>

<span id="CallQuality_CurrCPULoad"></span><span id="callquality_currcpuload"></span><span id="CALLQUALITY_CURRCPULOAD"></span>**\_CurrCPULoad CallQuality**
</dt> <dd>

Carico corrente della CPU.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,1<br/>                                                       |
| Intestazione<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITCallQualityControl:: GetRange**](itcallqualitycontrol-getrange.md)
</dt> <dt>

[**ITCallQualityControl:: Get**](itcallqualitycontrol-get.md)
</dt> <dt>

[**ITCallQualityControl:: set**](itcallqualitycontrol-set.md)
</dt> </dl>

 

 




