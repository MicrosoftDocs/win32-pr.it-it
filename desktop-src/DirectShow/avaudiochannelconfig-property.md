---
description: Ottiene la configurazione dell'altoparlante per i canali audio nel flusso di bit audio.
ms.assetid: ec13bb55-47af-4d79-9560-d297bce8e236
title: Proprietà AVAudioChannelConfig (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52ee1bc7897d92f7efa1b6d351d2f73c32867529
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048944"
---
# <a name="avaudiochannelconfig-property"></a>Proprietà AVAudioChannelConfig

Ottiene la configurazione dell'altoparlante per i canali audio nel flusso di bit audio.

Questa proprietà è di sola lettura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVAudioChannelConfig**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un operatore OR bit per bit dei membri dell'enumerazione [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig) .

## <a name="remarks"></a>Commenti

Il numero di canali include il canale LFE (Low Frequency Effect), se presente.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App UWP di Windows 2000 Professional \[ desktop apps \|\]<br/>                     |
| Server minimo supportato<br/> | App desktop di Windows 2000 Server \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




