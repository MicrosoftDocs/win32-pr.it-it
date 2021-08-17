---
description: L'enumerazione TAPIControlFlags viene usata da diversi metodi per indicare se una determinata proprietà viene controllata automaticamente o manualmente.
ms.assetid: 48259444-bf7b-4f0e-9068-2bdf89dde694
title: Enumerazione TAPIControlFlags (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 278cc2328335409d4ffcc95ea136826d121acd57776f98aaad947c8fb9ee5d93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139804"
---
# <a name="tapicontrolflags-enumeration"></a>Enumerazione TAPIControlFlags

\[Questa enumerazione non è disponibile per l'uso in Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

**L'enumerazione TAPIControlFlags** viene usata da diversi metodi per indicare se una determinata proprietà viene controllata automaticamente o manualmente.

## <a name="syntax"></a>Sintassi


```C++
} TAPIControlFlags;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="TAPIControl_Flags_None"></span><span id="tapicontrol_flags_none"></span><span id="TAPICONTROL_FLAGS_NONE"></span>**TAPIControl \_ Flag \_ Nessuno**
</dt> <dd>

TAPI non dispone di flag di controllo per la proprietà .

</dd> <dt>

<span id="TAPIControl_Flags_Auto"></span><span id="tapicontrol_flags_auto"></span><span id="TAPICONTROL_FLAGS_AUTO"></span>**TAPIControl \_ Flags \_ Auto**
</dt> <dd>

La proprietà viene controllata automaticamente.

</dd> <dt>

<span id="TAPIControl_Flags_Manual"></span><span id="tapicontrol_flags_manual"></span><span id="TAPICONTROL_FLAGS_MANUAL"></span>**TAPIControl \_ Flags \_ Manual**
</dt> <dd>

La proprietà viene controllata manualmente.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.1<br/>                                                       |
| Intestazione<br/>       | <dl> <dt>Ipmsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITAudioDeviceControl::GetRange**](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[**ITAudioDeviceControl::Get**](itaudiodevicecontrol-get.md)
</dt> <dt>

[**ITAudioDeviceControl::Set**](itaudiodevicecontrol-set.md)
</dt> <dt>

[**ITAudioSettings::GetRange**](itaudiosettings-getrange.md)
</dt> <dt>

[**ITAudioSettings::Get**](itaudiosettings-get.md)
</dt> <dt>

[**ITAudioSettings::Set**](itaudiosettings-set.md)
</dt> <dt>

[**ITCallQualityControl::GetRange**](itcallqualitycontrol-getrange.md)
</dt> <dt>

[**ITCallQualityControl::Get**](itcallqualitycontrol-get.md)
</dt> <dt>

[**ITCallQualityControl::Set**](itcallqualitycontrol-set.md)
</dt> <dt>

[**ITStreamQualityControl::GetRange**](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[**ITStreamQualityControl::Get**](itstreamqualitycontrol-get.md)
</dt> <dt>

[**ITStreamQualityControl::Set**](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




