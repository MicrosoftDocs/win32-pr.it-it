---
description: Specifica il numero massimo di immagini da un'intestazione GOP (Group-of-Pictures) all'intestazione GOP successiva.
ms.assetid: 90433df4-5a96-4bc2-a780-93306abcb0a4
title: Proprietà AVEncMPVGOPSize (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c8907d0992153039b1af9a9a0e82ee5782b525d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104049022"
---
# <a name="avencmpvgopsize-property"></a>Proprietà AVEncMPVGOPSize

Specifica il numero massimo di immagini da un'intestazione GOP (Group-of-Pictures) all'intestazione GOP successiva.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncMPVGOPSize**

## <a name="property-value"></a>Valore proprietà

I codificatori possono implementare questa proprietà come un set enumerato o come intervallo lineare.

## <a name="remarks"></a>Commenti

Impostare questa proprietà prima di avviare una registrazione.

**Si applica a Windows 8:** La dimensione del GOP codificata deve essere minore o uguale al numero specificato tramite questa proprietà, in modo da tenere lo stesso modello di frame B impostato da [CODEcapit \_ AVEncMPVDefaultBPictureCount](avencmpvdefaultbpicturecount-property.md) in tutto il GOP o a causa di una modifica della scena. Ad esempio, quando il numero di fotogrammi B in un GOP viene specificato come 2 e le dimensioni del GOP sono 11, il codificatore deve produrre dimensioni GOP di 10 fotogrammi o meno. Quando la modifica della scena viene eseguita al centro di un GOP, il codificatore può anche inserire il fotogramma chiave e produrre un GOP più piccolo.

La dimensione GOP 0 è dipendente dal codificatore e i codificatori possono scegliere Dimensioni GOP diverse in base all'implementazione, alla qualità e alle prestazioni. I codificatori devono rispettare le dimensioni GOP e troncare i frame B in questo caso.

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

 

 




