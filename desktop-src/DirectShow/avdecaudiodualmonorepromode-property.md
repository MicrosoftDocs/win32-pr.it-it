---
description: Specifica il modo in cui il decodificatore riproduce l'audio mono doppio.
ms.assetid: 3ef1f52c-13b2-4d9f-99fe-3317846be8a0
title: Proprietà AVDecAudioDualMonoReproMode (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9151ed6b996ec4ab92791221b7fb4c920913c818eac4a079ee6f40d04591a9db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917061"
---
# <a name="avdecaudiodualmonorepromode-property"></a>AVDecAudioDualMonoReproMode - proprietà

Specifica il modo in cui il decodificatore riproduce l'audio mono doppio.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVDecAudioDualMonoReproMode**

## <a name="property-value"></a>Valore proprietà

Il valore di questa proprietà è un membro [**dell'enumerazione eAVDecAudioDualMonoReproMode.**](/windows/desktop/api/codecapi/ne-codecapi-eavdecaudiodualmonorepromode)

## <a name="remarks"></a>Commenti

Queste proprietà si applicano solo quando il flusso di bit di input del decodificatore contiene audio mono doppio. Per testare questa condizione, ottenere il valore della [proprietà AVDecAudioDualMono.](avdecaudiodualmono-property.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[ app desktop \| UWP\]<br/>                     |
| Server minimo supportato<br/> | app \[ desktop UWP di Windows 2000 Server \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API Codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




