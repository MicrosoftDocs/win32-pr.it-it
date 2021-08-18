---
description: Specifica il tipo di immagine restituita da un codificatore video.
ms.assetid: 18A47033-3EAC-46C3-94AB-6ED20732F63C
title: MFSampleExtension_VideoEncodePictureType attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3be87284be3b605e3af70d64df98e5d762aa7cc353bb83b5f61a110d1242ae1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973170"
---
# <a name="mfsampleextension_videoencodepicturetype-attribute"></a>Attributo MFSampleExtension \_ VideoEncodePictureType

Specifica il tipo di immagine restituita da un codificatore video.

## <a name="data-type"></a>Tipo di dati

**eAVEncH264PictureType \_ B** archiviato come **UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Si applica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Commenti

[**H.264 Video Encoder imposta**](h-264-video-encoder.md) questo attributo sugli esempi di output generati. Il valore dell'attributo è un membro [**dell'enumerazione eAVEncH264PictureType.**](/windows/desktop/api/codecapi/ne-codecapi-eavench264picturetype)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                  |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Codificatore video H.264**](h-264-video-encoder.md)
</dt> <dt>

[Attributi di esempio](sample-attributes.md)
</dt> <dt>

[Esempi di supporti](media-samples.md)
</dt> </dl>

 

 




