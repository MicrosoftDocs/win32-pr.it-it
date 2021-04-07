---
description: Specifica l'incremento di basso livello quando il decodificatore esegue il controllo dinamico degli intervalli su un flusso audio Dolby AC-3.
ms.assetid: d723c825-f2f1-4ba0-a667-8285009764fd
title: Proprietà AVDecDDDynamicRangeScaleLow (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b68b1d4376d9ba15859be943ded23458fe16d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104049046"
---
# <a name="avdecdddynamicrangescalelow-property"></a>Proprietà AVDecDDDynamicRangeScaleLow

Specifica l'incremento di basso livello quando il decodificatore esegue il controllo dinamico degli intervalli su un flusso audio Dolby AC-3.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVDecDDDynamicRangeScaleLow**

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

 

 




