---
description: Per un formato video 3D, specifica la visualizzazione a sinistra.
ms.assetid: 4F33BF2D-EB32-46B6-B071-F9130D404201
title: Attributo MF_MT_VIDEO_3D_FIRST_IS_LEFT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027d91509d772a9200cdfc0ac64cce15514aa5a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104401793"
---
# <a name="mf_mt_video_3d_first_is_left-attribute"></a>MF \_ mt \_ video \_ 3D \_ First \_ è l' \_ attributo Left

Per un formato video 3D, specifica la visualizzazione a sinistra.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Per video 3D, ogni esempio video contiene due visualizzazioni, che sono designate per la *prima visualizzazione* e la *seconda*. Il layout esatto delle visualizzazioni in memoria è indicato dall'attributo del [ \_ \_ \_ \_ Formato video 3D MF mt](mf-mt-video-3d-format.md) .



| Formato               | Prima visualizzazione              | Seconda visualizzazione               |
|----------------------|-------------------------|---------------------------|
| Compresso affiancato  | Metà sinistra del buffer | Metà destra del buffer  |
| Dall'alto verso il basso compresso | Metà superiore del buffer  | Metà inferiore del buffer |
| MultiView            | Indice buffer 0          | Indice buffer 1            |
| Visualizzazione di base            | Intero frame            | Non presente               |



 

Per impostazione predefinita, la prima visualizzazione è la visualizzazione a sinistra e la seconda visualizzazione è la vista corretta. Se le visualizzazioni a sinistra e a destra sono state scambiate, impostare la MF \_ mt \_ video \_ 3D \_ First \_ è \_ Left attribute su **false** nel tipo di supporto.

> [!Note]  
> Nel formato di *vista di base* (**MFVideo3DSampleFormat \_ BaseView**) viene mantenuta solo la visualizzazione di base, pertanto questo attributo non è applicabile.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




