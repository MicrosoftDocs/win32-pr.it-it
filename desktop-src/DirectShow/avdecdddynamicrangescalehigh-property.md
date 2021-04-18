---
description: Specifica il taglio di alto livello quando il decodificatore esegue il controllo dinamico degli intervalli su un flusso audio Dolby AC-3.
ms.assetid: 8771a5f9-878b-43fd-8eaa-0bfc276194aa
title: Proprietà AVDecDDDynamicRangeScaleHigh (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 521cd631d92db73f23c7018adeda9bd321d23c1a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482277"
---
# <a name="avdecdddynamicrangescalehigh-property"></a>Proprietà AVDecDDDynamicRangeScaleHigh

Specifica il taglio di alto livello quando il decodificatore esegue il controllo dinamico degli intervalli su un flusso audio Dolby AC-3.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVDecDDDynamicRangeScaleHigh**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà presenta l'intervallo seguente.



| Valore | Descrizione                                                    |
|-------|----------------------------------------------------------------|
| 0     | Nessuna compressione dell'intervallo dinamico. Mantenere l'intervallo dinamico completo. |
| 100   | Applicare la compressione dell'intervallo dinamico completo.                          |



 

## <a name="remarks"></a>Commenti

Questa proprietà si applica solo quando il valore della proprietà [**AVDecDDOperationalMode**](avdecddoperationalmode-property.md) è eAVDecDDOperationalMode \_ line.

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

 

 




