---
description: Specifica la velocità in bit massima, in bit al secondo. Questa proprietà si applica solo alle modalità di codifica CBR (Constant Bit Rate) e VBR (Variable Bit Rate).
ms.assetid: 053fdad0-dc5f-4af1-84a6-bb7c0dac7e79
title: Proprietà AVEncCommonMaxBitRate (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0981a8f3fea67fa6e3dc4564ef2d2777af130bc02079050e63f571d7199e626
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159830"
---
# <a name="avenccommonmaxbitrate-property"></a>AVEncCommonMaxBitRate - proprietà

Specifica la velocità in bit massima, in bit al secondo. Questa proprietà si applica solo alle modalità di codifica CBR (Constant Bit Rate) e VBR (Variable Bit Rate).

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncCommonMaxBitRate**

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

 

 




