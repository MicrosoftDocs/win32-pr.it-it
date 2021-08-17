---
description: La struttura TAPI AUDIO STREAM CONFIG CAPS è contenuta nella struttura TAPI STREAM CONFIG CAPS quando il membro CapsType è impostato sul membro AudioCap dell'unione \_ \_ \_ \_ \_ \_ \_ StreamConfigCapsType.
ms.assetid: 61575839-4604-4c8b-ae4d-fe796c3c5314
title: TAPI_AUDIO_STREAM_CONFIG_CAPS struttura (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51fc4777e6d174f7d4aaeac9bbd3f6d467123275b4030c9fa21363223584e8b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118861220"
---
# <a name="tapi_audio_stream_config_caps-structure"></a>Struttura TAPI \_ AUDIO \_ STREAM CONFIG \_ \_ CAPS

\[Questa struttura non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client rtc offre funzionalità simili.\]

La struttura TAPI AUDIO STREAM CONFIG CAPS è contenuta nella struttura [**\_ TAPI STREAM \_ CONFIG \_**](tapi-stream-config-caps.md) **\_ \_ \_ \_ CAPS** quando il membro **CapsType** è impostato sul membro **AudioCap** dell'unione [**StreamConfigCapsType.**](streamconfigcapstype.md)

## <a name="syntax"></a>Sintassi


```C++
} TAPI_AUDIO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Members

<dl> <dt>

**Descrizione**
</dt> <dd>

Descrizione descrittiva del tipo di configurazione del flusso audio per la visualizzazione agli utenti dell'applicazione.

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

Granularità dei bit per ogni valore di esempio.

</dd> <dt>

**MinimumSampleFrequency**
</dt> <dd>

Frequenza di campionamento minima.

</dd> <dt>

**MaximumSampleFrequency**
</dt> <dd>

Frequenza di campionamento massima.

</dd> <dt>

**SampleFrequencyGranularity**
</dt> <dd>

Granularità dei valori della frequenza di campionamento.

</dd> <dt>

**MinimumAvgBytesPerSec**
</dt> <dd>

Byte medi minimi al secondo.

</dd> <dt>

**MaximumAvgBytesPerSec**
</dt> <dd>

Numero massimo di byte medi al secondo.

</dd> <dt>

**AvgBytesPerSecGranularity**
</dt> <dd>

Granularità dei valori di byte al secondo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.1<br/>                                                       |
| Intestazione<br/>       | <dl> <dt>Ipmsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TAPI \_ STREAM \_ CONFIG \_ CAPS**](tapi-stream-config-caps.md)
</dt> </dl>

 

 




