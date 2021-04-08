---
description: Specifica il modo in cui il decodificatore riproduce audio mono doppio.
ms.assetid: 3ef1f52c-13b2-4d9f-99fe-3317846be8a0
title: Proprietà AVDecAudioDualMonoReproMode (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71ebe7e003b2dc4b6eebc30901525ffb918a9a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747082"
---
# <a name="avdecaudiodualmonorepromode-property"></a>Proprietà AVDecAudioDualMonoReproMode

Specifica il modo in cui il decodificatore riproduce audio mono doppio.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVDecAudioDualMonoReproMode**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un membro dell'enumerazione [**eAVDecAudioDualMonoReproMode**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode) .

## <a name="remarks"></a>Commenti

Questa proprietà si applica solo quando il flusso di bit di input del decodificatore contiene audio mono doppio. Per verificare questa condizione, ottenere il valore della proprietà [AVDecAudioDualMono](avdecaudiodualmono-property.md) .

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

 

 




