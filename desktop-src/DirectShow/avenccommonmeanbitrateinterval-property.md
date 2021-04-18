---
description: Specifica l'intervallo di tempo in base al quale viene applicata la velocità in bit media. Questa proprietà viene utilizzata insieme alla proprietà AVEncCommonMeanBitRate.
ms.assetid: 3cf26f46-e8ac-448a-a031-800915cad1ef
title: Proprietà AVEncCommonMeanBitRateInterval (codecapis. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ffee31b0ac54d195051f1cc973d2fdcb058f202
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482524"
---
# <a name="avenccommonmeanbitrateinterval-property"></a>Proprietà AVEncCommonMeanBitRateInterval

Specifica l'intervallo di tempo in base al quale viene applicata la velocità in bit media. Questa proprietà viene utilizzata insieme alla proprietà [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) .

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UInt64** (**VT \_ UI8**)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncCommonMeanBitRateInterval**

## <a name="property-value"></a>Valore proprietà

Questa proprietà ha un intervallo lineare di valori. Per ottenere l'intervallo supportato, chiamare [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Commenti

Per la codifica con velocità in bit variabile (VBR) a due passaggi, il valore zero indica che l'intervallo di tempo è l'intera durata del contenuto. Per la codifica CBR (constant bit rate) a passaggio singolo, il valore zero indica che il codificatore seleziona l'intervallo (in genere 0,5 secondi).

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

 

 




