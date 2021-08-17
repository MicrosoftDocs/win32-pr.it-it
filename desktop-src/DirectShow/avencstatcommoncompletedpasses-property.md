---
description: Specifica il numero di passaggi di codifica completati. Questa proprietà si applica solo alla codifica multipass.
ms.assetid: 19286f26-96f1-429c-9d6a-5e9b98597cd2
title: Proprietà AVEncStatCommonCompletedPasses (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5950a8f013dc697b0e8178e65610971776c0bd7bba233a58d164c05080f966f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119275871"
---
# <a name="avencstatcommoncompletedpasses-property"></a>AVEncStatCommonCompletedPasses - proprietà

Specifica il numero di passaggi di codifica completati. Questa proprietà si applica solo alla codifica multipass.

Questa proprietà è di sola lettura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncStatCommonCompletedPasses**

## <a name="property-value"></a>Valore proprietà

Questa proprietà ha un intervallo lineare di valori. Per ottenere l'intervallo supportato, chiamare [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

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

 

 




