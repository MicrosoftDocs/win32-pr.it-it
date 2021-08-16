---
description: Definisce l'apertura di visualizzazione, ovvero l'area di un fotogramma video che contiene dati di immagine validi.
ms.assetid: 86a7509b-c690-49c2-bbe4-8b02d64c307c
title: MF_MT_MINIMUM_DISPLAY_APERTURE attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97ff6dd226492c848bd2347ccc2bac17c2dd8824467e661e83be06d590f65c0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012941"
---
# <a name="mf_mt_minimum_display_aperture-attribute"></a>Attributo \_ MF MT \_ MINIMUM \_ DISPLAY \_ APERTURE

Definisce l'apertura di visualizzazione, ovvero l'area di un fotogramma video che contiene dati di immagine validi.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

Il valore dell'attributo è [**una struttura MFVideoArea.**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea)

L'apertura minima dello schermo è l'area che contiene la parte valida del segnale. I pixel all'esterno dell'apertura contengono dati non validi e non devono essere visualizzati.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop Di Vista \[ \| app UWP\]<br/>                              |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 \[ \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[Proporzioni immagine](picture-aspect-ratio.md)
</dt> <dt>

[Tipi di supporti video](video-media-types.md)
</dt> <dt>

[**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**APERTURA \_ GEOMETRICA MF MT \_ \_**](mf-mt-geometric-aperture-attribute.md)
</dt> <dt>

[**MF \_ MT \_ PAN \_ SCAN \_ APERTURE**](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




