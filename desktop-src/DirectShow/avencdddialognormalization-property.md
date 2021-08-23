---
description: Specifica il livello di normalizzazione del dialogo, in decibel (dB), in un flusso audio Dolby Digital. Questa proprietà si applica ai codificatori audio Dolby Digital.
ms.assetid: c347f8b2-5132-45d6-af66-43d3c409b0d7
title: Proprietà AVEncDDDialogNormalization (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f050147b0de889c9bb12f4e66964f16b8705c4883fa66c0f5cbba9c82338c30f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690191"
---
# <a name="avencdddialognormalization-property"></a>AVEncDDDialogNormalization - proprietà

Specifica il livello di normalizzazione del dialogo, in decibel (dB), in un flusso audio Dolby Digital. Questa proprietà si applica ai codificatori audio Dolby Digital.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncDDDialogNormalization**

## <a name="property-value"></a>Valore proprietà

Questa proprietà ha un intervallo lineare di valori. Per ottenere l'intervallo supportato, chiamare [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

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

 

 




