---
description: L'enumerazione TAPIControlFlags viene usata da diversi metodi per indicare se una determinata proprietà viene controllata automaticamente o manualmente.
ms.assetid: 48259444-bf7b-4f0e-9068-2bdf89dde694
title: Enumerazione TAPIControlFlags (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07cc3e931c69a408d996fa28e6002b6c53c9df87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331772"
---
# <a name="tapicontrolflags-enumeration"></a>Enumerazione TAPIControlFlags

\[ Questa enumerazione non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'enumerazione **TAPIControlFlags** viene usata da diversi metodi per indicare se una determinata proprietà viene controllata automaticamente o manualmente.

## <a name="syntax"></a>Sintassi


```C++
} TAPIControlFlags;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="TAPIControl_Flags_None"></span><span id="tapicontrol_flags_none"></span><span id="TAPICONTROL_FLAGS_NONE"></span>**\_Flag TAPIControl \_ None**
</dt> <dd>

TAPI non ha flag di controllo per la proprietà.

</dd> <dt>

<span id="TAPIControl_Flags_Auto"></span><span id="tapicontrol_flags_auto"></span><span id="TAPICONTROL_FLAGS_AUTO"></span>**\_Flag TAPIControl \_ automatici**
</dt> <dd>

La proprietà viene controllata automaticamente.

</dd> <dt>

<span id="TAPIControl_Flags_Manual"></span><span id="tapicontrol_flags_manual"></span><span id="TAPICONTROL_FLAGS_MANUAL"></span>**\_Manuale flag \_ TAPIControl**
</dt> <dd>

La proprietà viene controllata manualmente.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,1<br/>                                                       |
| Intestazione<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITAudioDeviceControl:: GetRange**](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[**ITAudioDeviceControl:: Get**](itaudiodevicecontrol-get.md)
</dt> <dt>

[**ITAudioDeviceControl:: set**](itaudiodevicecontrol-set.md)
</dt> <dt>

[**ITAudioSettings:: GetRange**](itaudiosettings-getrange.md)
</dt> <dt>

[**ITAudioSettings:: Get**](itaudiosettings-get.md)
</dt> <dt>

[**ITAudioSettings:: set**](itaudiosettings-set.md)
</dt> <dt>

[**ITCallQualityControl:: GetRange**](itcallqualitycontrol-getrange.md)
</dt> <dt>

[**ITCallQualityControl:: Get**](itcallqualitycontrol-get.md)
</dt> <dt>

[**ITCallQualityControl:: set**](itcallqualitycontrol-set.md)
</dt> <dt>

[**ITStreamQualityControl:: GetRange**](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[**ITStreamQualityControl:: Get**](itstreamqualitycontrol-get.md)
</dt> <dt>

[**ITStreamQualityControl:: set**](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




