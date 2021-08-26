---
description: Ottiene la configurazione del parlante per i canali audio nel flusso di bit audio.
ms.assetid: ec13bb55-47af-4d79-9560-d297bce8e236
title: Proprietà AVAudioChannelConfig (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba9c497305292abeb34b86a7989fb05fbb872c898d10743ebd93b3982089e00
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983791"
---
# <a name="avaudiochannelconfig-property"></a>AVAudioChannelConfig - proprietà

Ottiene la configurazione del parlante per i canali audio nel flusso di bit audio.

Questa proprietà è di sola lettura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVAudioChannelConfig**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un'operazione OR bit per bit dei membri [**dell'enumerazione eAVAudioChannelConfig.**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig)

## <a name="remarks"></a>Commenti

Il numero di canali include il canale LFE (Low Frequency Effect), se presente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[ app desktop \| UWP\]<br/>                     |
| Server minimo supportato<br/> | app \[ desktop UWP di Windows 2000 Server \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API Codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




