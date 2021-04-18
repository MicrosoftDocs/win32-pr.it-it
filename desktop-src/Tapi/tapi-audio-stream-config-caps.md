---
description: La \_ struttura dei \_ tappi di configurazione del flusso audio TAPI \_ \_ è contenuta nella \_ struttura dei limiti di configurazione del flusso TAPI \_ \_ quando il membro CapsType è impostato sul membro AudioCap dell'Unione StreamConfigCapsType.
ms.assetid: 61575839-4604-4c8b-ae4d-fe796c3c5314
title: Struttura TAPI_AUDIO_STREAM_CONFIG_CAPS (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daec587a8e760bedd3ab9c6b3469ef8f70b72383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327488"
---
# <a name="tapi_audio_stream_config_caps-structure"></a>\_Struttura di \_ \_ Caps di configurazione del flusso audio TAPI \_

\[ Questa struttura non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

La struttura dei **\_ \_ \_ \_ tappi di configurazione del flusso audio TAPI** è contenuta nella struttura dei [**\_ \_ \_ limiti di configurazione del flusso TAPI**](tapi-stream-config-caps.md) quando il membro **CapsType** è impostato sul membro **AudioCap** dell'Unione [**StreamConfigCapsType**](streamconfigcapstype.md) .

## <a name="syntax"></a>Sintassi


```C++
} TAPI_AUDIO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Members

<dl> <dt>

**Descrizione**
</dt> <dd>

Descrizione intuitiva del tipo di configurazione del flusso audio da visualizzare agli utenti dell'applicazione.

</dd> <dt>

**MinimumChannels**
</dt> <dd>

Numero minimo di canali associati al flusso.

</dd> <dt>

**MaximumChannels**
</dt> <dd>

Numero massimo di canali associati al flusso.

</dd> <dt>

**ChannelsGranularity**
</dt> <dd>

Granularità del numero di canali.

</dd> <dt>

**MinimumBitsPerSample**
</dt> <dd>

Numero minimo di bit per campione.

</dd> <dt>

**MaximumBitsPerSample**
</dt> <dd>

Numero massimo di bit per campione.

</dd> <dt>

**BitsPerSampleGranularity**
</dt> <dd>

Granularità dei bit per i valori di esempio.

</dd> <dt>

**MinimumSampleFrequency**
</dt> <dd>

Frequenza di campionamento minima.

</dd> <dt>

**MaximumSampleFrequency**
</dt> <dd>

Frequenza massima di campionamento.

</dd> <dt>

**SampleFrequencyGranularity**
</dt> <dd>

Granularità dei valori della frequenza di campionamento.

</dd> <dt>

**MinimumAvgBytesPerSec**
</dt> <dd>

Media minima di byte al secondo.

</dd> <dt>

**MaximumAvgBytesPerSec**
</dt> <dd>

Numero massimo di byte media al secondo.

</dd> <dt>

**AvgBytesPerSecGranularity**
</dt> <dd>

Granularità dei valori di byte al secondo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,1<br/>                                                       |
| Intestazione<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ \_ tappi configurazione flusso TAPI \_**](tapi-stream-config-caps.md)
</dt> </dl>

 

 




