---
description: "L'enumerazione AudioSettingsProperty viene usata dai metodi ITAudioSettings:: GetRange, ITAudioSettings:: Get e ITAudioSettings:: set per indicare la proprietà dell'impostazione audio da risolvere."
ms.assetid: b91c8213-f102-4ebb-ad8a-e43709b3daad
title: Enumerazione AudioSettingsProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759e3ca9d9559c35c64c117b9b84b1cee4a1fad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328735"
---
# <a name="audiosettingsproperty-enumeration"></a>Enumerazione AudioSettingsProperty

\[ Questa enumerazione non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

L'enumerazione **AudioSettingsProperty** viene usata dai metodi [**ITAudioSettings:: GetRange**](itaudiosettings-getrange.md), [**ITAudioSettings:: Get**](itaudiosettings-get.md)e [**ITAudioSettings:: set**](itaudiosettings-set.md) per indicare la proprietà dell'impostazione audio da risolvere.

## <a name="syntax"></a>Sintassi


```C++
} AudioSettingsProperty;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**\_SignalLevel AudioSettings**
</dt> <dd>

Proprietà delle impostazioni del segnale.

</dd> <dt>

<span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**\_SilenceThreshold AudioSettings**
</dt> <dd>

Proprietà soglia di inattività.

</dd> <dt>

<span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**\_Volume AudioSettings**
</dt> <dd>

Proprietà del volume.

</dd> <dt>

<span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**\_Bilanciamento AudioSettings**
</dt> <dd>

Proprietà Balance.

</dd> <dt>

<span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**\_Sonorità AudioSettings**
</dt> <dd>

Proprietà di sonorità.

</dd> <dt>

<span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**AudioSettings \_ acuti**
</dt> <dd>

Proprietà Treble.

</dd> <dt>

<span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**AudioSettings \_ Bass**
</dt> <dd>

Proprietà Bass.

</dd> <dt>

<span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**\_Mono AudioSettings**
</dt> <dd>

Proprietà mono.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,1<br/>                                                       |
| Intestazione<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITAudioSettings:: GetRange**](itaudiosettings-getrange.md)
</dt> <dt>

[**ITAudioSettings:: Get**](itaudiosettings-get.md)
</dt> <dt>

[**ITAudioSettings:: set**](itaudiosettings-set.md)
</dt> </dl>

 

 




