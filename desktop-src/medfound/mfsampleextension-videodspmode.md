---
description: Indica se la stabilizzazione video è stata applicata a un fotogramma video.
ms.assetid: 13F877A3-7600-400F-9071-FE1B83027355
title: Attributo MFSampleExtension_VideoDSPMode (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 309d4b5b68455e78ba63074b9d8ec5e4cbde4fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310231"
---
# <a name="mfsampleextension_videodspmode-attribute"></a>\_Attributo VideoDSPMode di MFSampleExtension

Indica se la stabilizzazione video è stata applicata a un fotogramma video.

## <a name="data-type"></a>Tipo di dati

**MFVideoDSPMode** archiviato come **UInt32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Commenti

Il [**stabilizzazione video MFT**](video-stabilization-mft.md) imposta questo attributo sugli esempi di output che produce. Il valore dell'attributo è un valore di enumerazione [**MFVideoDSPMode**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) . Se il valore è **la \_ stabilizzazione MFVideoDSPMode**, il MFT applica la stabilizzazione dell'immagine al frame.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi di esempio](sample-attributes.md)
</dt> <dt>

[Esempi di supporti](media-samples.md)
</dt> <dt>

[**Stabilizzazione video MFT**](video-stabilization-mft.md)
</dt> </dl>

 

 




