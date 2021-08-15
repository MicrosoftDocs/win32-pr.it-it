---
description: L'enumerazione AudioSettingsProperty viene usata dai metodi ITAudioSettings::GetRange, ITAudioSettings::Get e ITAudioSettings::Set per indicare la proprietà dell'impostazione audio da risolvere.
ms.assetid: b91c8213-f102-4ebb-ad8a-e43709b3daad
title: Enumerazione AudioSettingsProperty (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b15cfb5a0211f02ac333ba75e47b5e4cbd5c44865b4a18c2f19ea3a8769dde3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118871531"
---
# <a name="audiosettingsproperty-enumeration"></a>Enumerazione AudioSettingsProperty

\[Questa enumerazione non è disponibile per l'uso in Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

L'enumerazione **AudioSettingsProperty** viene usata dai metodi [**ITAudioSettings::GetRange**](itaudiosettings-getrange.md), [**ITAudioSettings::Get**](itaudiosettings-get.md)e [**ITAudioSettings::Set**](itaudiosettings-set.md) per indicare la proprietà dell'impostazione audio da risolvere.

## <a name="syntax"></a>Sintassi


```C++
} AudioSettingsProperty;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**AudioSettings \_ SignalLevel**
</dt> <dd>

Proprietà delle impostazioni del segnale.

</dd> <dt>

<span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**AudioSettings \_ SilenceThreshold**
</dt> <dd>

Proprietà Soglia di silenzio.

</dd> <dt>

<span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**AudioSettings \_ Volume**
</dt> <dd>

Proprietà volume.

</dd> <dt>

<span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**AudioSettings \_ Balance**
</dt> <dd>

Proprietà Balance.

</dd> <dt>

<span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**AudioSettings \_ Loudness**
</dt> <dd>

Proprietà Loudness.

</dd> <dt>

<span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**AudioSettings \_ Treble**
</dt> <dd>

Proprietà Treble.

</dd> <dt>

<span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**AudioSettings \_ Inno**
</dt> <dd>

Proprietà Disassociato.

</dd> <dt>

<span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**AudioSettings \_ Mono**
</dt> <dd>

Proprietà monaurale.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.1<br/>                                                       |
| Intestazione<br/>       | <dl> <dt>Ipmsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITAudioSettings::GetRange**](itaudiosettings-getrange.md)
</dt> <dt>

[**ITAudioSettings::Get**](itaudiosettings-get.md)
</dt> <dt>

[**ITAudioSettings::Set**](itaudiosettings-set.md)
</dt> </dl>

 

 




