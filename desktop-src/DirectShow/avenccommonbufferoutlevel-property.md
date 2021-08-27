---
description: Specifica il livello finale del buffer di codifica, in bit, alla fine del processo di codifica. Questa proprietà si applica solo alle modalità di codifica CBR (Constant Bit Rate) e VBR (Variable Bit Rate).
ms.assetid: d5bcdf54-061a-436b-8b1a-61ef7d7c90bf
title: Proprietà AVEncCommonBufferOutLevel (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77159af0f328dcc6003c21bfa91544070d121e9aad4f8f42caf02853c218926e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103501"
---
# <a name="avenccommonbufferoutlevel-property"></a>AVEncCommonBufferOutLevel - proprietà

Specifica il livello finale del buffer di codifica, in bit, alla fine del processo di codifica. Questa proprietà si applica solo alle modalità di codifica CBR (Constant Bit Rate) e VBR (Variable Bit Rate).

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncCommonBufferOutLevel**

## <a name="property-value"></a>Valore proprietà

Questa proprietà ha un intervallo lineare di valori. Per ottenere l'intervallo supportato, chiamare [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Commenti

La proprietà è disponibile solo se la durata della codifica è definita in anticipo, usando la proprietà [**AVEncVideoNoOfFieldsToEncode**](avencvideonooffieldstoencode-property.md) o [**AVEncAudioIntervalToEncode.**](avencaudiointervaltoencode-property.md)

Per i video MPEG, questa proprietà definisce la completezza del verificatore del buffer video (VBV) alla fine del processo di codifica. Supporta la concatenazione dei flussi durante la codifica.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional app \[ desktop \| app UWP\]<br/>                     |
| Server minimo supportato<br/> | Windows 2000 App desktop UWP per le app \[ desktop di 2000 \| Server\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà API codec](codec-api-properties.md)
</dt> <dt>

[**Interfaccia ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




