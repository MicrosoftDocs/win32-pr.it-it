---
description: Specifica il parametro di quantizzazione (QP) usato per codificare un campione video.
ms.assetid: F7C4FEFC-FEE7-4614-BC90-4F9D5D878F49
title: Attributo MFSampleExtension_VideoEncodeQP (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721f5df00ff24b307daed2ccbcbf61a04b129db2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310230"
---
# <a name="mfsampleextension_videoencodeqp-attribute"></a>\_Attributo VideoEncodeQP di MFSampleExtension

Specifica il parametro di quantizzazione (QP) usato per codificare un campione video.

## <a name="data-type"></a>Tipo di dati

**UINT64**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Commenti

Il [**codificatore video H. 264**](h-264-video-encoder.md) imposta questo attributo sugli esempi di output generati.

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

 

 




