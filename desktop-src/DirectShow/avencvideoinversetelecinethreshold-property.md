---
description: Imposta la soglia in corrispondenza della quale il codificatore considera ridondante un campo video.
ms.assetid: db6c2f0e-f451-4d2d-984f-b507083e8358
title: Proprietà AVEncVideoInverseTelecineThreshold (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3427a8ff1491277c2e36640560acf728c0ef7208
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745658"
---
# <a name="avencvideoinversetelecinethreshold-property"></a>Proprietà AVEncVideoInverseTelecineThreshold

Imposta la soglia in corrispondenza della quale il codificatore considera ridondante un campo video.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncVideoInverseTelecineThreshold**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà presenta l'intervallo seguente.



| Valore | Descrizione                                                    |
|-------|----------------------------------------------------------------|
| 0     | È meno probabile che il codificatore prenda in considerazione i campi video ridondanti. |
| 100   | È più probabile che il codificatore prenda in considerazione i campi video ridondanti. |



 

## <a name="remarks"></a>Commenti

Impostare questa proprietà se il codificatore esegue una telecine inversa con un'origine video analoga.

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

 

 




