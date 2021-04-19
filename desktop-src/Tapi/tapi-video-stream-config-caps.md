---
description: La \_ struttura di caps di configurazione del flusso video TAPI \_ \_ \_ è contenuta nella \_ struttura di caps di configurazione del flusso TAPI \_ \_ quando il membro CapsType è impostato sul membro VideoCap dell'Unione StreamConfigCapsType.
ms.assetid: 8812755a-50e8-4d8e-ab67-7a3a4b2a4a67
title: Struttura TAPI_VIDEO_STREAM_CONFIG_CAPS (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 525a35cb7c7332aa4e80fe8d5e2436e75e2d5c08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331775"
---
# <a name="tapi_video_stream_config_caps-structure"></a>\_ \_ \_ Struttura Caps di configurazione del flusso video TAPI \_

\[ Questa struttura non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

La struttura di **Caps di \_ \_ \_ configurazione \_ del flusso video TAPI** è contenuta nella struttura di caps di  [**\_ \_ configurazione \_ del flusso TAPI**](tapi-stream-config-caps.md) quando il membro CapsType è impostato sul membro **VideoCap** dell'Unione [**StreamConfigCapsType**](streamconfigcapstype.md) .

## <a name="syntax"></a>Sintassi


```C++
} TAPI_VIDEO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>Members

<dl> <dt>

**Descrizione**
</dt> <dd>

Descrizione intuitiva del tipo di configurazione del flusso audio da visualizzare agli utenti dell'applicazione.

</dd> <dt>

**VideoStandard**
</dt> <dd>

Viene usato il video standard.

</dd> <dt>

**InputSize**
</dt> <dd>

Dimensioni di input del frame.

</dd> <dt>

**MinCroppingSize**
</dt> <dd>

Dimensioni minime di ritaglio.

</dd> <dt>

**MaxCroppingSize**
</dt> <dd>

Dimensioni massime di ritaglio.

</dd> <dt>

**CropGranularityX**
</dt> <dd>

Granularità del ritaglio consentito lungo l'asse x.

</dd> <dt>

**CropGranularityY**
</dt> <dd>

Granularità del ritaglio consentito lungo l'asse y.

</dd> <dt>

**CropAlignX**
</dt> <dd>

Allineamento del ritaglio di asse x.

</dd> <dt>

**CropAlignY**
</dt> <dd>

Allineamento del ritaglio dell'asse y.

</dd> <dt>

**MinOutputSize**
</dt> <dd>

Dimensioni minime risultanti della finestra video.

</dd> <dt>

**MaxOutputSize**
</dt> <dd>

Dimensione massima risultante della finestra video.

</dd> <dt>

**OutputGranularityX**
</dt> <dd>

Granularità delle dimensioni di output lungo l'asse x.

</dd> <dt>

**OutputGranularityY**
</dt> <dd>

Granularità delle dimensioni di output lungo l'asse y.

</dd> <dt>

**StretchTapsX**
</dt> <dd>

Estendi lungo l'asse x.

</dd> <dt>

**StretchTapsY**
</dt> <dd>

Estendi lungo l'asse y.

</dd> <dt>

**ShrinkTapsX**
</dt> <dd>

Compatta lungo l'asse x.

</dd> <dt>

**ShrinkTapsY**
</dt> <dd>

Compatta lungo l'asse y.

</dd> <dt>

**MinFrameInterval**
</dt> <dd>

Intervallo minimo del fotogramma video.

</dd> <dt>

**MaxFrameInterval**
</dt> <dd>

Intervallo massimo di fotogrammi video.

</dd> <dt>

**MinBitsPerSecond**
</dt> <dd>

Bit minimi al secondo.

</dd> <dt>

**MaxBitsPerSecond**
</dt> <dd>

Numero massimo di bit al secondo.

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

 

 




