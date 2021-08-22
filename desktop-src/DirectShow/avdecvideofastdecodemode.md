---
description: Ottiene o imposta la velocità di decodifica video.
ms.assetid: 76F7013D-C172-4D31-93BC-EA3D186EB14C
title: Proprietà AVDecVideoFastDecodeMode (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f36cd765754e73924caae401495e597ec69828ed62f08466884b10365517d17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503140"
---
# <a name="avdecvideofastdecodemode-property"></a>AVDecVideoFastDecodeMode - proprietà

Ottiene o imposta la velocità di decodifica video.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVDecVideoFastDecodeMode**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà può essere compreso tra 0 e 32, dove 0 indica la decodifica normale e 32 è la modalità di decodifica più veloce. Il comportamento esatto dipende dall'implementazione del decodificatore. Non ogni incremento compreso tra 1 e 32 definisce necessariamente una modalità distinta.

[**L'enumerazione eAVFastDecodeMode**](/windows/desktop/api/codecapi/ne-codecapi-eavfastdecodemode) contiene alcune modalità predefinite per questa proprietà.

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

 

 




