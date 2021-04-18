---
description: Specifica il parametro di quantizzazione (QP) per la codifica video.
ms.assetid: 9E3B5E2D-3583-4C89-BC2A-4AC3C5545673
title: Proprietà CODECAPI_AVEncVideoEncodeQP (codecapit. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec6c746f2f3c902ca416097571abaf5953956cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305490"
---
# <a name="codecapi_avencvideoencodeqp-property"></a>Proprietà AVEncVideoEncodeQP di codecapi \_

Specifica il parametro di quantizzazione (QP) per la codifica video.

## <a name="data-type"></a>Tipo di dati

**ULONGLONG** (VT \_ UI8)

## <a name="property-guid"></a>GUID proprietà

**Codecapis \_ AVEncVideoEncodeQP**

## <a name="property-value"></a>Valore proprietà

Set di campi a 4 16 bit utilizzato per specificare il frame query al secondo nella codifica Fixed-QP.

I campi sono:

-   BITS 0-15: QP predefinito
-   BITS 16-31: QP usato per I frame I
-   BITS 32-47: QP usato per i frame P
-   BITS 48-63: QP usato per i frame B

## <a name="remarks"></a>Commenti

Questa proprietà viene usata anche con [codificatori della fotocamera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).

Per garantire un utilizzo coerente tra codificatori diversi, è necessario presupporre che i codificatori considerino solo il QP predefinito e possano ignorare i valori QP per le immagini I/P/B.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                     |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Codecapis. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[**ICodecAPI**](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

