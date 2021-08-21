---
description: La struttura TAPI STREAM CONFIG CAPS contiene informazioni di configurazione del flusso \_ video o \_ \_ audio.
ms.assetid: 83b39751-b00f-4762-830b-13cafbcb1cfd
title: TAPI_STREAM_CONFIG_CAPS struttura (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbbb3b3ec72cc99810311cc510e36c2adc8242e2b3d98b321fd8bc8c6a9ab4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002649"
---
# <a name="tapi_stream_config_caps-structure"></a>Struttura TAPI \_ STREAM \_ CONFIG \_ CAPS

\[Questa struttura non è disponibile per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API client RTC offre funzionalità simili.\]

La **struttura TAPI \_ STREAM CONFIG \_ \_ CAPS** contiene informazioni di configurazione del flusso video o audio.

## <a name="syntax"></a>Sintassi


```C++
} TAPI_STREAM_CONFIG_CAPS, *PTAPI_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Members

<dl> <dt>

**CapsType**
</dt> <dd>

Definisce se il membro dell'unione contiene informazioni video o audio.

</dd> <dt>

**VideoCap**
</dt> <dd>

Struttura [**TAPI \_ VIDEO STREAM \_ CONFIG \_ \_ CAPS**](tapi-video-stream-config-caps.md) contenente le funzionalità del flusso video.

</dd> <dt>

**AudioCap**
</dt> <dd>

Struttura [**TAPI \_ AUDIO STREAM \_ CONFIG \_ \_ CAPS**](tapi-audio-stream-config-caps.md) contenente le funzionalità del flusso audio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3.1<br/>                                                       |
| Intestazione<br/>       | <dl> <dt>Ipmsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITFormatControl::GetStreamCaps**](itformatcontrol-getstreamcaps.md)
</dt> <dt>

[**StreamConfigCapsType**](streamconfigcapstype.md)
</dt> <dt>

[**TAPI \_ VIDEO \_ STREAM \_ CONFIG \_ CAPS**](tapi-video-stream-config-caps.md)
</dt> <dt>

[**TAPI \_ AUDIO \_ STREAM \_ CONFIG \_ CAPS**](tapi-audio-stream-config-caps.md)
</dt> </dl>

 

 




