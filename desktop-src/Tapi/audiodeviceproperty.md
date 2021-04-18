---
description: "L'enumerazione AudioDeviceProperty viene usata dai metodi ITAudioDeviceControl:: GetRange, ITAudioDeviceControl:: Get e ITAudioDeviceControl:: set per indicare la proprietà da risolvere."
ms.assetid: 0ed9b75e-3c79-4e41-9883-63b85ebfae06
title: Enumerazione AudioDeviceProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab807759bfb316858be41ea9bb4b78d795ee1a1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328738"
---
# <a name="audiodeviceproperty-enumeration"></a>Enumerazione AudioDeviceProperty

\[ Questa enumerazione non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'enumerazione **AudioDeviceProperty** viene usata dai metodi [**ITAudioDeviceControl:: GetRange**](itaudiodevicecontrol-getrange.md), [**ITAudioDeviceControl:: Get**](itaudiodevicecontrol-get.md)e [**ITAudioDeviceControl:: set**](itaudiodevicecontrol-set.md) per indicare la proprietà da risolvere.

## <a name="syntax"></a>Sintassi


```C++
} AudioDeviceProperty;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**\_DuplexMode AudioDevice**
</dt> <dd>

Indica che è in corso l'impostazione o il recupero della modalità duplex del dispositivo.

</dd> <dt>

<span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**\_AutomaticGainControl AudioDevice**
</dt> <dd>

Indica che è in corso l'impostazione o il recupero del controllo del guadagno automatico del dispositivo.

</dd> <dt>

<span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**\_AcousticEchoCancellation AudioDevice**
</dt> <dd>

Indica che le proprietà di annullamento Echo acustico del dispositivo vengono impostate o recuperate.

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
</dt> </dl>

 

 




