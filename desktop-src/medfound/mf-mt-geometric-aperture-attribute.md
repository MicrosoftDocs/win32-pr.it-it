---
description: Definisce l'apertura geometrica per un tipo di supporto video.
ms.assetid: a2489ba1-f322-4b63-a479-0d9879c30a8c
title: Attributo MF_MT_GEOMETRIC_APERTURE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e194408dd8b6bf4a4dac717c7d41aaecbb06f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967038"
---
# <a name="mf_mt_geometric_aperture-attribute"></a>\_Attributo di \_ apertura geometrico MF mt \_

Definisce l'apertura geometrica per un tipo di supporto video.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

Il valore di questo attributo è una struttura [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .

Le proporzioni dell'immagine vengono calcolate in relazione all'apertura geometrica, usando la formula seguente: proporzioni immagine = (larghezza aperture geometrica/altezza diaframma geometrica) × proporzioni pixel.

Se questo attributo non è impostato, si presuppone che l'apertura geometrica sia l'intero frame video. Questo attributo deve essere impostato solo quando il tipo di supporto descrive uno standard video con un'area attiva definita.

Ad esempio, in NTSC Television il fotogramma video è 720 × 480 con un'area attiva di 704 × 480 e una percentuale di proporzioni di pixel 10:11. L'immagine risultante ha una proporzioni di (704/480) × (10/11) = 4:3.

> [!Note]  
> Il Presenter predefinito per il [renderer video avanzato](enhanced-video-renderer.md) (EVR) Mostra l'apertura geometrica del video, se specificato.

 

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="examples"></a>Esempio


```
HRESULT SetGeometricAperture(
    IMFMediaType *pMediaType, 
    const MFVideoArea& area
    )
{
    return pMediaType->SetBlob(
        MF_MT_GEOMETRIC_APERTURE, 
        (UINT8*)&area, 
        sizeof(MFVideoArea)
        );
}
```



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

[Attributi di Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Proporzioni immagine](picture-aspect-ratio.md)
</dt> <dt>

[Tipi di supporti video](video-media-types.md)
</dt> <dt>

[**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: seblob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**\_ \_ \_ apertura minima schermo \_ MF mt**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**\_apertura dell' \_ analisi della panoramica MF mt \_ \_**](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




