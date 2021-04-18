---
description: Restituisce il numero di fotogrammi video ricevuti dal codificatore.
ms.assetid: 3de49105-3c74-4a52-9cac-465b4abfcbf5
title: Proprietà AVEncStatVideoTotalFrames (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d76adda51e6d16676a2a957fd16a5aac2a15691e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303874"
---
# <a name="avencstatvideototalframes-property"></a>Proprietà AVEncStatVideoTotalFrames

Restituisce il numero di fotogrammi video ricevuti dal codificatore.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncStatVideoTotalFrames**

## <a name="remarks"></a>Commenti

Questa proprietà è disponibile al termine della codifica.

Il valore di questa proprietà è il numero totale di frame inviati al codificatore, inclusi i frame eliminati. Per ottenere il numero di frame codificati, leggere la proprietà [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md) .

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

 

 




