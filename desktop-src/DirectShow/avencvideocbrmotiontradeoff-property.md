---
description: Specifica il compromesso tra movimento e immagini fisse. Questa proprietà si applica solo alla modalità di controllo CBR (Constant Bit Rate).
ms.assetid: e657e971-4624-4c87-ad51-6bf0cd1f9246
title: Proprietà AVEncVideoCBRMotionOff (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d3db1f310de6468b57d469fbf699919ab86429e7242344622ca498b9e59f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057941"
---
# <a name="avencvideocbrmotiontradeoff-property"></a>AVEncVideoCBRMotionOff - proprietà

Specifica il compromesso tra movimento e immagini fisse. Questa proprietà si applica solo alla modalità di controllo CBR (Constant Bit Rate).

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncVideoCBRMotionOff**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà ha l'intervallo seguente.



| Valore | Descrizione               |
|-------|---------------------------|
| 0     | Ottimizzare le immagini fisse |
| 100   | Ottimizzare il movimento.      |



 

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

 

 




