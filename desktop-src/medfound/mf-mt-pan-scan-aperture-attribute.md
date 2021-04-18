---
description: Definisce l'apertura di Pan/Scan, ovvero la 4&\# 215; 3 area del video che deve essere visualizzata in modalità Pan/Scan.
ms.assetid: faa577fd-6572-46b9-9c6c-f91c47832cb5
title: Attributo MF_MT_PAN_SCAN_APERTURE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a798ba96315126daab94ba92e8791bfeac77db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308466"
---
# <a name="mf_mt_pan_scan_aperture-attribute"></a>\_Attributo di \_ apertura della panoramica dell' \_ analisi MF mt \_

Definisce l'apertura di Pan/Scan, ovvero l'area di 4 × 3 del video che deve essere visualizzata in modalità Pan/Scan.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

Il valore dell'attributo è una struttura [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .

Questo attributo viene usato per ritagliare un video widescreen in proporzioni di 4:3. L'apertura di Pan/Scan viene usata solo in modalità Pan/Scan, che è abilitata impostando l'attributo [**MF \_ mt \_ Pan \_ Scan \_ Enabled**](mf-mt-pan-scan-enabled-attribute.md) su **true**.

Se la modalità Pan/Scan non è abilitata, usare l'apertura di visualizzazione, specificata dall'attributo di [**\_ \_ \_ \_ apertura della visualizzazione minima MF mt**](mf-mt-minimum-display-aperture-attribute.md) .

Se questo attributo non è impostato, si presuppone che l'apertura di Pan/Scan sia l'intero frame video.

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

[**\_ \_ \_ apertura minima schermo \_ MF mt**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**\_ \_ Analisi panoramica MF \_ mt \_ abilitata**](mf-mt-pan-scan-enabled-attribute.md)
</dt> </dl>

 

 




