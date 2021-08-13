---
description: Restituisce il numero di fotogrammi video ricevuti dal codificatore.
ms.assetid: 3de49105-3c74-4a52-9cac-465b4abfcbf5
title: Proprietà AVEncStatVideoTotalFrames (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 461708e9006db183992cf550bf7f98eeaeacbfe16c100675ab4992b54f0768d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663442"
---
# <a name="avencstatvideototalframes-property"></a>AVEncStatVideoTotalFrames - proprietà

Restituisce il numero di fotogrammi video ricevuti dal codificatore.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncStatVideoTotalFrames**

## <a name="remarks"></a>Commenti

Questa proprietà è disponibile dopo il completamento della codifica.

Il valore di questa proprietà è il numero totale di fotogrammi inviati al codificatore, inclusi quelli eliminati. Per ottenere il numero di fotogrammi codificati, leggere la [**proprietà AVEncStatVideoCodedFrames.**](avencstatvideocodedframes-property.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional app \[ desktop \| UWP\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 Server desktop apps UWP apps (App desktop UWP di Windows 2000 \[ \| Server)\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API Codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




