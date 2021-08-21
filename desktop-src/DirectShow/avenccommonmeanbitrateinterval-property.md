---
description: Specifica l'intervallo di tempo a cui si applica la velocità in bit media. Questa proprietà viene usata insieme alla proprietà AVEncCommonMeanBitRate.
ms.assetid: 3cf26f46-e8ac-448a-a031-800915cad1ef
title: Proprietà AVEncCommonMeanBitRateInterval (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5cbd463ea67e281183dccde937f16978634e4103670b0e82b90b96139da5296
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159797"
---
# <a name="avenccommonmeanbitrateinterval-property"></a>AVEncCommonMeanBitRateInterval - proprietà

Specifica l'intervallo di tempo a cui si applica la velocità in bit media. Questa proprietà viene usata insieme alla [**proprietà AVEncCommonMeanBitRate.**](avenccommonmeanbitrate-property.md)

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT64** (**VT \_ UI8**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncCommonMeanBitRateInterval**

## <a name="property-value"></a>Valore proprietà

Questa proprietà ha un intervallo lineare di valori. Per ottenere l'intervallo supportato, chiamare [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Commenti

Per la codifica VBR (Two-Pass Variable Bit Rate), il valore zero indica che l'intervallo di tempo è l'intera durata del contenuto. Per la codifica CBR (Single Pass Constant Bit Rate), il valore zero indica che il codificatore seleziona l'intervallo (in genere 0,5 secondi).

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

 

 




