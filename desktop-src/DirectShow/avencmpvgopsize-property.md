---
description: Specifica il numero massimo di immagini da un'intestazione GOP (Group-of-Pictures) all'intestazione GOP successiva.
ms.assetid: 90433df4-5a96-4bc2-a780-93306abcb0a4
title: Proprietà AVEncMPVGOPSize (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7c82ae5c613bb3e78069be3f39f652d840e19c5d62d095fe020f4186bf975f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119258451"
---
# <a name="avencmpvgopsize-property"></a>AVEncMPVGOPSize - proprietà

Specifica il numero massimo di immagini da un'intestazione GOP (Group-of-Pictures) all'intestazione GOP successiva.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncMPVGOPSize**

## <a name="property-value"></a>Valore proprietà

I codificatori possono implementare questa proprietà come set enumerato o come intervallo lineare.

## <a name="remarks"></a>Commenti

Impostare questa proprietà prima di avviare una registrazione.

**Si applica a Windows 8:** Le dimensioni GOP codificate devono essere inferiori o uguali al numero specificato tramite questa proprietà, in modo da mantenere lo stesso modello di frame B impostato da [CODECAPI \_ AVEncMPVDefaultBPictureCount](avencmpvdefaultbpicturecount-property.md) in tutto il GOP o a causa della modifica della scena. Ad esempio, quando il numero di fotogrammi B in un GOP è 2 e le dimensioni GOP sono 11, il codificatore produrrà dimensioni GOP di 10 fotogrammi o meno. Quando si verifica una modifica della scena nel mezzo di un GOP, il codificatore potrebbe anche inserire un fotogramma chiave e produrre GOP più piccolo.

La dimensione GOP 0 dipende dal codificatore e i codificatori possono scegliere dimensioni GOP diverse in base all'implementazione, alla qualità e alle prestazioni. In questo caso, i codificatori devono rispettare le dimensioni GOP e troncare i frame B.

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

 

 




