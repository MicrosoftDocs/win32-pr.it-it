---
description: Indica se un frame video è interlacciato o progressivo.
ms.assetid: 3cb80e75-e803-493b-a22d-e485e77b5177
title: Attributo MFSampleExtension_Interlaced (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43a273b548192ac52da8604eb36fde5ec0e9fcf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309091"
---
# <a name="mfsampleextension_interlaced-attribute"></a>MFSampleExtension- \_ attributo interlacciato

Indica se un frame video è interlacciato o progressivo. Se **true**, il frame è interlacciato. Se **false**, il frame è progressivo. Se non impostato, il tipo di supporto descrive il interlacciamento. Questo attributo si applica agli esempi di supporti.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Commenti

Per contenuti video contenenti frame misti progressivi e interlacciati, impostare il tipo di supporto su interlacciato e utilizzare questo attributo in ogni frame per indicare se il frame è progressivo o interlacciato.

Per contenuto video completamente interlacciato, impostare il tipo di supporto su interlacciato e omettere questo attributo o impostarlo su **true** in ogni campione.

Per contenuti video completamente progressivi, impostare il tipo di supporto su progressive e omettere questo attributo o impostarlo su **false** in ogni esempio.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>                              |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[Attributi di esempio](sample-attributes.md)
</dt> <dt>

[Esempi di supporti](media-samples.md)
</dt> <dt>

[Interlacciamento video](video-interlacing.md)
</dt> </dl>

 

 




