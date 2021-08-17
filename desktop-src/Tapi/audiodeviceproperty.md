---
description: L'enumerazione AudioDeviceProperty viene usata dai metodi ITAudioDeviceControl::GetRange, ITAudioDeviceControl::Get e ITAudioDeviceControl::Set per indicare la proprietà indirizzata.
ms.assetid: 0ed9b75e-3c79-4e41-9883-63b85ebfae06
title: Enumerazione AudioDeviceProperty (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a634caa627f5d518e8783ce056e89a69931aa981466754a9d320f36787186f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117948793"
---
# <a name="audiodeviceproperty-enumeration"></a>Enumerazione AudioDeviceProperty

\[Questa enumerazione non è disponibile per l'uso in Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

L'enumerazione **AudioDeviceProperty** viene usata dai metodi [**ITAudioDeviceControl::GetRange**](itaudiodevicecontrol-getrange.md), [**ITAudioDeviceControl::Get**](itaudiodevicecontrol-get.md)e [**ITAudioDeviceControl::Set**](itaudiodevicecontrol-set.md) per indicare la proprietà da risolvere.

## <a name="syntax"></a>Sintassi


```C++
} AudioDeviceProperty;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**AudioDevice \_ DuplexMode**
</dt> <dd>

Indica che è in corso l'impostazione o il recupero della modalità duplex del dispositivo.

</dd> <dt>

<span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**AudioDevice \_ AutomaticGainControl**
</dt> <dd>

Indica che è in corso l'impostazione o il recupero del controllo automatico del guadagno del dispositivo.

</dd> <dt>

<span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**AudioDevice \_ AcousticEchoCancellation**
</dt> <dd>

Indica che le proprietà di annullamento dell'eco acustico del dispositivo vengono impostate o recuperate.

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
</dt> </dl>

 

 




