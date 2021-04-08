---
description: Specifica la frequenza dei fotogrammi nel flusso di output del codificatore, in frame al secondo.
ms.assetid: 72e16c7d-977e-4269-9576-afc789e31826
title: Proprietà AVEncVideoOutputFrameRate (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4cb675c266d146936a3402934e51486ded5b02
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746231"
---
# <a name="avencvideooutputframerate-property"></a>Proprietà AVEncVideoOutputFrameRate

Specifica la frequenza dei fotogrammi nel flusso di output del codificatore, in frame al secondo.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt64** (**VT \_ UI8**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncVideoOutputFrameRate**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un rapporto che definisce la frequenza dei fotogrammi. I 32 bit superiori contengono il numeratore e i 32 bit inferiori contengono il denominatore. La tabella seguente mostra le frequenze dei fotogrammi comuni, in frame al secondo.



| Frequenza dei fotogrammi | Proporzioni      |
|------------|------------|
| 23,97      | 24000/1001 |
| 24         | 24/1       |
| 25         | 25/1       |
| 29,97      | 30000/1001 |
| 30         | 30/1       |
| 50         | 50/1       |
| 59,94      | 60000/1001 |
| 60         | 60/1       |



 

## <a name="remarks"></a>Commenti

Le applicazioni possono impostare questa proprietà per specificare la frequenza dei fotogrammi di output. I codificatori possono inoltre restituire questa proprietà come funzionalità. A seconda del codificatore, il valore potrebbe essere limitato alla frequenza dei fotogrammi di input. In caso contrario, il codificatore è in grado di convertire internamente la frequenza dei fotogrammi. Vedere [**Proprietà AVEncVideoOutputFrameRateConversion**](avencvideooutputframerateconversion-property.md).

Questa proprietà viene usata anche con [codificatori della fotocamera H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).

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

 

