---
description: Specifica se la modalità Pan/Scan è abilitata.
ms.assetid: 9e8746c6-13a4-4cf7-9748-82223d9529fa
title: Attributo MF_MT_PAN_SCAN_ENABLED (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b347c898ce827ff37796a9698e843f6321db8a1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528753"
---
# <a name="mf_mt_pan_scan_enabled-attribute"></a>\_ \_ \_ \_ Attributo abilitata per l'analisi della panoramica MF mt

Specifica se la modalità Pan/Scan è abilitata.

## <a name="data-type"></a>Tipo di dati

**UINT32**

Considera come valore booleano.

## <a name="remarks"></a>Commenti

Se questo attributo è **true**, verrà visualizzata solo l'area di Pan/Scan del video. L'area di Pan/Scan è specificata dall'attributo di [**\_ \_ \_ \_ apertura della Panoramica di MF mt**](mf-mt-pan-scan-aperture-attribute.md) .

Se questo attributo è **false** o non impostato, verrà visualizzata l'intera apertura di visualizzazione del video. L'apertura di visualizzazione è specificata dall'attributo di [**\_ \_ \_ \_ apertura della visualizzazione minima MF mt**](mf-mt-minimum-display-aperture-attribute.md) .

Se si imposta questo attributo su **true**, impostare anche il valore dell'attributo [**MF \_ mt \_ Pan \_ Scan \_ aperture**](mf-mt-pan-scan-aperture-attribute.md) .

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

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[Proporzioni immagine](picture-aspect-ratio.md)
</dt> </dl>

 

 




