---
description: Per un formato video 3D, specifica quale visualizzazione è la visualizzazione a sinistra.
ms.assetid: 4F33BF2D-EB32-46B6-B071-F9130D404201
title: MF_MT_VIDEO_3D_FIRST_IS_LEFT attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19b7deed122f3de419455abf54bfcc18ad50ef199d87afa8bcaad8d34000a011
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876802"
---
# <a name="mf_mt_video_3d_first_is_left-attribute"></a>Attributo \_ MF MT \_ VIDEO \_ 3D \_ FIRST IS \_ \_ LEFT

Per un formato video 3D, specifica quale visualizzazione è la visualizzazione a sinistra.

## <a name="data-type"></a>Tipo di dati

**BOOL** archiviato come **UINT32**

## <a name="remarks"></a>Commenti

Per i video 3D, ogni esempio di video contiene due visualizzazioni, ovvero la prima *e* *la seconda visualizzazione.* Il layout esatto delle viste in memoria è indicato dall'attributo [ \_ MF MT \_ VIDEO \_ 3D \_ FORMAT.](mf-mt-video-3d-format.md)



| Formato               | Prima visualizzazione              | Seconda visualizzazione               |
|----------------------|-------------------------|---------------------------|
| Pacchetto side-by-side  | Metà sinistra del buffer | Metà destra del buffer  |
| Imballato dall'alto verso il basso | Metà superiore del buffer  | Metà inferiore del buffer |
| Multiview            | Indice buffer 0          | Indice buffer 1            |
| Visualizzazione di base            | Intero frame            | Non presente               |



 

Per impostazione predefinita, la prima è la visualizzazione a sinistra e la seconda è la visualizzazione a destra. Se le visualizzazioni sinistra e destra vengono scambiate, impostare l'attributo MF \_ MT \_ VIDEO \_ 3D \_ FIRST IS LEFT su \_ FALSE nel tipo di \_ supporto. 

> [!Note]  
> Nel *formato di* visualizzazione di base (**MFVideo3DSampleFormat \_ BaseView**), viene mantenuta solo la visualizzazione di base, pertanto questo attributo non è applicabile.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                  |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




