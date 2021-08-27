---
description: Specifica il livello di qualità per la codifica.
ms.assetid: 2c7f3836-2392-47c6-9a56-d5a9b52560ff
title: Proprietà AVEncCommonQuality (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99202391e919fa1da9028a15a57154834feddd3039160b9b0562a713fe59ddaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087671"
---
# <a name="avenccommonquality-property"></a>AVEncCommonQuality - proprietà

Specifica il livello di qualità per la codifica.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncCommonQuality**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà ha l'intervallo seguente.



| Valore | Descrizione                           |
|-------|---------------------------------------|
| 0     | Qualità minima, dimensioni di output inferiori. |
| 100   | Qualità massima, dimensioni di output maggiori.  |



 

## <a name="remarks"></a>Commenti

Questa proprietà controlla il livello di qualità quando il codificatore non usa una velocità in bit vincolata. La [**proprietà AVEncCommonRateControlMode**](avenccommonratecontrolmode-property.md) determina se la velocità in bit è vincolata.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[ app desktop app \| UWP\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 App desktop UWP per le app \[ desktop di 2000 \| Server\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




