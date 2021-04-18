---
description: Specifica il tipo di immagine restituito da un codificatore video.
ms.assetid: 18A47033-3EAC-46C3-94AB-6ED20732F63C
title: Attributo MFSampleExtension_VideoEncodePictureType (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bfe0df0e4f3163e7c8c0581c5c7c2a854555eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309086"
---
# <a name="mfsampleextension_videoencodepicturetype-attribute"></a>\_Attributo VideoEncodePictureType di MFSampleExtension

Specifica il tipo di immagine restituito da un codificatore video.

## <a name="data-type"></a>Tipo di dati

**eAVEncH264PictureType \_ B** archiviato come **UInt32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Commenti

Il [**codificatore video H. 264**](h-264-video-encoder.md) imposta questo attributo sugli esempi di output generati. Il valore dell'attributo è un membro dell'enumerazione [**eAVEncH264PictureType**](/windows/desktop/api/codecapi/ne-codecapi-eavench264picturetype) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Codificatore video H. 264**](h-264-video-encoder.md)
</dt> <dt>

[Attributi di esempio](sample-attributes.md)
</dt> <dt>

[Esempi di supporti](media-samples.md)
</dt> </dl>

 

 




