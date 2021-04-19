---
description: Definisce l'apertura di visualizzazione, ovvero l'area di un frame video che contiene dati di immagine validi.
ms.assetid: 86a7509b-c690-49c2-bbe4-8b02d64c307c
title: Attributo MF_MT_MINIMUM_DISPLAY_APERTURE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d13252378422081044d7f2cb21e5a31098702a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307505"
---
# <a name="mf_mt_minimum_display_aperture-attribute"></a>\_ \_ \_ Attributo apertura minima schermo MF mt \_

Definisce l'apertura di visualizzazione, ovvero l'area di un frame video che contiene dati di immagine validi.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

Il valore dell'attributo è una struttura [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .

Il diaframma di visualizzazione minimo è l'area che contiene la parte valida del segnale. I pixel al di fuori dell'apertura contengono dati non validi e non devono essere visualizzati.

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

[Attributi del tipo di supporto](media-type-attributes.md)
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

[**\_ \_ apertura geometrica MF mt \_**](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[**\_apertura dell' \_ analisi della panoramica MF mt \_ \_**](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




