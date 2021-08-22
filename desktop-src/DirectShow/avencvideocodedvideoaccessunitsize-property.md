---
description: Specifica le dimensioni in byte delle unità di accesso video. Questa proprietà si applica solo alle modalità di controllo VBR (Variable Bit Rate).
ms.assetid: bb46b171-d70a-4e01-88c4-321a210a0220
title: Proprietà AVEncVideoCodedVideoAccessUnitSize (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcce45dbd232226aa5e0013cbead8e4ff2d8d82b5362d1d6a43cf45c2d030407
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663167"
---
# <a name="avencvideocodedvideoaccessunitsize-property"></a>AVEncVideoCodedVideoAccessUnitSize - proprietà

Specifica le dimensioni in byte delle unità di accesso video. Questa proprietà si applica solo alle modalità di controllo VBR (Variable Bit Rate).

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncVideoCodedVideoAccessUnitSize**

## <a name="property-value"></a>Valore proprietà

Questa proprietà viene restituita come intervallo di valori. Per ottenere l'intervallo supportato, chiamare [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional app \[ desktop \| UWP\]<br/>                     |
| Server minimo supportato<br/> | app \[ desktop UWP di Windows 2000 Server \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà dell'API Codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




