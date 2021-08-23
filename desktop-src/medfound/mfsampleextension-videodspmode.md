---
description: Indica se la stabilizzazione video è stata applicata a un fotogramma video.
ms.assetid: 13F877A3-7600-400F-9071-FE1B83027355
title: MFSampleExtension_VideoDSPMode attributo (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95776fd7b8e130b9538e98843ca72d69980978b6f954747fadca939b8d3c5922
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554931"
---
# <a name="mfsampleextension_videodspmode-attribute"></a>Attributo MFSampleExtension \_ VideoDSPMode

Indica se la stabilizzazione video è stata applicata a un fotogramma video.

## <a name="data-type"></a>Tipo di dati

**MFVideoDSPMode** archiviato come **UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Si applica a

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>Commenti

Il [**Stabilizzazione video MFT**](video-stabilization-mft.md) imposta questo attributo sugli esempi di output prodotti. Il valore dell'attributo è un [**valore di enumerazione MFVideoDSPMode.**](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mfvideodspmode) Se il valore è **MFVideoDSPMode \_ Stabilization**, significa che mFT ha applicato la stabilizzazione dell'immagine al frame.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                    |
| Intestazione<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi di esempio](sample-attributes.md)
</dt> <dt>

[Esempi di supporti](media-samples.md)
</dt> <dt>

[**Stabilizzazione video MFT**](video-stabilization-mft.md)
</dt> </dl>

 

 




