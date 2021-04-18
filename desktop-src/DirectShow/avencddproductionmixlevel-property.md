---
description: Specifica il livello di combinazione, in decibel (dB), in un flusso audio Dolby Digital. Questa proprietà si applica ai codificatori audio Dolby Digital.
ms.assetid: fcb16d02-af4f-4626-99ee-2831172e5280
title: Proprietà AVEncDDProductionMixLevel (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8a1726db6ab4841b4603a61bcfe39504742db42
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304226"
---
# <a name="avencddproductionmixlevel-property"></a>Proprietà AVEncDDProductionMixLevel

Specifica il livello di combinazione, in decibel (dB), in un flusso audio Dolby Digital. Questa proprietà si applica ai codificatori audio Dolby Digital.

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncDDProductionMixLevel**

## <a name="property-value"></a>Valore proprietà

Questa proprietà ha un intervallo lineare di valori. Per ottenere l'intervallo supportato, chiamare [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Commenti

Se si imposta questa proprietà, impostare la proprietà [**AVEncDDProductionInfoExists**](avencddproductioninfoexists-property.md) su **true**.

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

 

 




