---
description: Specifica, in IMFTransform, la velocità di elaborazione massima di macroblocco, in macroblocchi al secondo, supportata dal codificatore hardware.
ms.assetid: 1AA41DE3-C37C-41BA-9549-5F12373DDB3B
title: Attributo MF_VIDEO_MAX_MB_PER_SEC (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbee009b50daee074241c11750e9d25240cda153
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308425"
---
# <a name="mf_video_max_mb_per_sec-attribute"></a>\_Attributo MF video \_ Max \_ MB \_ / \_ sec

Specifica, in [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform), la velocità di elaborazione massima di macroblocco, in macroblocchi al secondo, supportata dal codificatore hardware.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Attributo di sola lettura.

**Codificatori H. 264/AVC:**

Questo attributo è influenzato dalle proprietà seguenti:

-   [MF \_ \_ \_ Livello di video mt](mf-mt-video-level.md) (alias di [MF \_ mt \_ MPEG2 \_ Level](mf-mt-mpeg2-level-attribute.md))
-   [Codecapis \_ AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md)
-   [Codecapis \_ AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md)

Se è presente l'attributo di [ \_ \_ \_ livello video MF mt](mf-mt-video-level.md) , il codificatore deve restituire la velocità di elaborazione per la velocità in bit più elevata e la risoluzione supportata al livello specificato. Se l' \_ \_ \_ attributo di livello video MF MT non è presente, deve usare un livello predefinito pari a 4.

Se è stata impostata la proprietà [ \_ AVEncCommonQualityVsSpeed ICodecAPI di codecapite](../directshow/avenccommonqualityvsspeed-property.md) , il codificatore deve restituire la velocità di elaborazione corrispondente al valore impostato per questa proprietà. Se l' \_ attributo AVEncCommonQualityVsSpeed di CODEcapit non è presente, deve usare il valore predefinito 0 che dovrebbe essere la modalità di elaborazione più rapida.

Se la proprietà [ \_ AVEncMPVDefaultBPictureCount ICodecAPI di codecapi](../directshow/avencmpvdefaultbpicturecount-property.md) è stata impostata su un valore valido e supportato, il codificatore deve restituire la velocità di elaborazione corrispondente al valore impostato per questa proprietà. Se l' \_ attributo AVEncMPVDefaultBPictureCount di CODEcapit non è presen, t deve usare un valore predefinito di 0 B frame.

Solo i 28 bit inferiori devono essere usati da un'applicazione. I 4bits superiori sono riservati per un uso futuro. Le applicazioni devono ignorare i 4 bit superiori e MFTs devono impostare i 4 bit superiori su 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App \[ desktop di Windows 8.1 app \| UWP\]<br/>                                |
| Server minimo supportato<br/> | App desktop di Windows Server 2012 R2 \[ \| UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
