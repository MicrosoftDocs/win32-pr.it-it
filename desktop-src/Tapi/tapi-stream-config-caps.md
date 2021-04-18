---
description: La struttura di caps di configurazione del \_ flusso TAPI \_ \_ contiene informazioni sulla configurazione di flussi video o audio.
ms.assetid: 83b39751-b00f-4762-830b-13cafbcb1cfd
title: Struttura TAPI_STREAM_CONFIG_CAPS (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379ca481d3bebaf8ceb11bfc2dbdab6642ca20b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328901"
---
# <a name="tapi_stream_config_caps-structure"></a>\_Struttura di \_ Caps di configurazione del flusso TAPI \_

\[ Questa struttura non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

La struttura di **\_ \_ \_ Caps** di configurazione del flusso TAPI contiene informazioni sulla configurazione di flussi video o audio.

## <a name="syntax"></a>Sintassi


```C++
} TAPI_STREAM_CONFIG_CAPS, *PTAPI_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Members

<dl> <dt>

**CapsType**
</dt> <dd>

Definisce se il membro di Unione contiene informazioni video o audio.

</dd> <dt>

**VideoCap**
</dt> <dd>

Struttura [**di \_ \_ Caps di \_ configurazione \_ del flusso video TAPI**](tapi-video-stream-config-caps.md) che contiene le funzionalità del flusso video.

</dd> <dt>

**AudioCap**
</dt> <dd>

Struttura [**di \_ \_ Caps di \_ configurazione \_ del flusso audio TAPI**](tapi-audio-stream-config-caps.md) che contiene le funzionalità del flusso audio.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|------------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 3,1<br/>                                                       |
| Intestazione<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITFormatControl::GetStreamCaps**](itformatcontrol-getstreamcaps.md)
</dt> <dt>

[**StreamConfigCapsType**](streamconfigcapstype.md)
</dt> <dt>

[**\_ \_ \_ tappi di configurazione \_ flusso video TAPI**](tapi-video-stream-config-caps.md)
</dt> <dt>

[**\_ \_ \_ tappi di configurazione del flusso audio TAPI \_**](tapi-audio-stream-config-caps.md)
</dt> </dl>

 

 




