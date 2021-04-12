---
description: Specifica se un campione video contiene un solo campo o due campi con interfoliazione. Questo attributo si applica agli esempi di supporti.
ms.assetid: 550619be-2042-4a2c-9ad2-728474835255
title: Attributo MFSampleExtension_SingleField (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 217d7c43a9777982485ba350d259a59a518e26c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527925"
---
# <a name="mfsampleextension_singlefield-attribute"></a>\_Attributo SingleField di MFSampleExtension

Specifica se un campione video contiene un solo campo o due campi con interfoliazione. Questo attributo si applica agli esempi di supporti.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Commenti

Se il valore è **true**, l'esempio contiene un campo. Se il valore è **false** o l'attributo non è impostato, l'esempio contiene un frame completo. (Due campi se interlacciato o un frame progressivo).

Se il tipo di supporto è frame progressivi o campi con interfoliazione, questo attributo deve essere impostato su **false** o Left.

Se il tipo di supporto è Single Field, questo attributo deve essere **true**. Impostare l'attributo [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md) nell'esempio per indicare se si tratta del campo superiore o inferiore.

Attualmente il renderer video migliorato (EVR) non supporta il contenuto che passa tra i frame interlacciati e i singoli campi.

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

[Attributi di esempio](sample-attributes.md)
</dt> <dt>

[Esempi di supporti](media-samples.md)
</dt> <dt>

[Interlacciamento video](video-interlacing.md)
</dt> </dl>

 

 




