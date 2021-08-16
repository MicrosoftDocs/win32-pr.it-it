---
description: Specifica, in IMFTransform, la velocità massima di elaborazione dei macroblock, in blocchi di macro al secondo, supportata dal codificatore hardware.
ms.assetid: 1AA41DE3-C37C-41BA-9549-5F12373DDB3B
title: MF_VIDEO_MAX_MB_PER_SEC attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c76e6a44a6e0993f9cf6410a0092708da767f92815fc98020dd2f4d88359370
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739239"
---
# <a name="mf_video_max_mb_per_sec-attribute"></a>Attributo MF \_ VIDEO MAX MB PER \_ \_ \_ \_ SEC

Specifica, in [**IMFTransform,**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)la frequenza massima di elaborazione dei macroblock, in blocchi di macro al secondo, supportata dal codificatore hardware.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Attributo di sola lettura.

**Codificatori H.264/AVC:**

Questo attributo è interessato dalle proprietà seguenti:

-   [MF \_ MT \_ VIDEO \_ LEVEL](mf-mt-video-level.md) (alias di [MF MT \_ \_ MPEG2 \_ LEVEL)](mf-mt-mpeg2-level-attribute.md)
-   [CODECAPI \_ AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md)
-   [CODECAPI \_ AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md)

Se è [presente l'attributo \_ MF MT \_ VIDEO \_ LEVEL,](mf-mt-video-level.md) il codificatore deve restituire la velocità di elaborazione per la velocità in bit e la risoluzione più alte supportate al livello specificato. Se l'attributo MF MT VIDEO LEVEL non è \_ \_ \_ presente, deve usare un livello predefinito di 4.

Se la [proprietà CODECAPI \_ AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) ICodecAPI è stata impostata, il codificatore deve restituire la velocità di elaborazione corrispondente al valore impostato per questa proprietà. Se l'attributo CODECAPI AVEncCommonQualityVsSpeed non è presente, deve usare il valore predefinito 0, che dovrebbe essere la modalità di elaborazione più \_ veloce.

Se la proprietà ICodecAPI [CODECAPI \_ AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md) è stata impostata su un valore valido e supportato, il codificatore deve restituire la velocità di elaborazione corrispondente al valore impostato per questa proprietà. Se l'attributo CODECAPI AVEncMPVDefaultBPictureCount non è presen, deve usare un valore predefinito di \_ 0 frame B.

Solo i 28 bit inferiori devono essere usati da un'applicazione. I 4 bit superiori sono riservati per un uso futuro. Le applicazioni devono ignorare i 4 bit superiori e i bit MFT devono impostare i 4 bit superiori su 0.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 app desktop \| app UWP\]<br/>                                |
| Server minimo supportato<br/> | Windows Server 2012 App desktop R2 \[ \| app UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
