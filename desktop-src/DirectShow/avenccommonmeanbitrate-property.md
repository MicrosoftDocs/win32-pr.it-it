---
description: Specifica la velocità in bit codificata media, in bit al secondo. Questa proprietà si applica solo alle modalità di codifica CBR (Constant Bit Rate) e VBR (Variable Bit Rate).
ms.assetid: 8519685a-4f5b-44af-ad46-09eba7a198c6
title: Proprietà AVEncCommonMeanBitRate (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05c1db672b09e257959a409182288cdfbfd271d0679335c9d9e14048c1e31781
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983781"
---
# <a name="avenccommonmeanbitrate-property"></a>AVEncCommonMeanBitRate - proprietà

Specifica la velocità in bit codificata media, in bit al secondo. Questa proprietà si applica solo alle modalità di codifica CBR (Constant Bit Rate) e VBR (Variable Bit Rate).

Si tratta di una proprietà di lettura/scrittura.

## <a name="data-type"></a>Tipo di dati

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID proprietà

**CODECAPI \_ AVEncCommonMeanBitRate**

## <a name="property-value"></a>Valore proprietà

I codificatori possono implementare questa proprietà come set enumerato o come intervallo lineare.

## <a name="remarks"></a>Commenti

Questa proprietà viene usata anche con codificatori [di fotocamera H.264 UVC 1.5.](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)

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

 

