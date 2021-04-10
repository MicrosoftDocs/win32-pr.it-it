---
description: Ottiene o imposta la velocità di decodifica dei video.
ms.assetid: 76F7013D-C172-4D31-93BC-EA3D186EB14C
title: Proprietà AVDecVideoFastDecodeMode (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 355c085731befedbcb9245a67870d9d609a92c6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125265"
---
# <a name="avdecvideofastdecodemode-property"></a>Proprietà AVDecVideoFastDecodeMode

Ottiene o imposta la velocità di decodifica dei video.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVDecVideoFastDecodeMode**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà può variare da 0 a 32, dove 0 indica la decodifica normale e 32 è la modalità di decodifica più veloce. Il comportamento esatto dipende dall'implementazione del decodificatore. Non tutti gli incrementi compresi tra 1 e 32 definiscono necessariamente una modalità distinta.

L'enumerazione [**eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode) contiene alcune modalità predefinite per questa proprietà.

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

 

 




