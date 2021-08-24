---
description: Specifica la priorità di basso livello quando il decodificatore esegue il controllo dinamico dell'intervallo in un flusso audio Dolby AC-3.
ms.assetid: d723c825-f2f1-4ba0-a667-8285009764fd
title: Proprietà AVDecDDDynamicRangeScaleLow (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91773eb20f3d0714223877acba4f26b01503202fc87f9f7b97dcde60ab99512e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586741"
---
# <a name="avdecdddynamicrangescalelow-property"></a>AVDecDDDynamicRangeScaleLow - proprietà

Specifica la priorità di basso livello quando il decodificatore esegue il controllo dinamico dell'intervallo in un flusso audio Dolby AC-3.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVDecDDDynamicRangeScaleLow**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà ha l'intervallo seguente.



| Valore | Descrizione                                                    |
|-------|----------------------------------------------------------------|
| 0     | Nessuna compressione di intervallo dinamico. Mantenere l'intervallo dinamico completo. |
| 100   | Applicare la compressione a intervalli dinamici completi.                          |



 

## <a name="remarks"></a>Commenti

Questa proprietà si applica solo quando il valore della proprietà [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) è eAVDecDDOperationalMode \_ LINE.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[ app desktop \| UWP\]<br/>                     |
| Server minimo supportato<br/> | Windows app desktop di Windows 2000 Server \[ \| app UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API Codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




