---
description: Per un formato video 3D, specifica quale visualizzazione è la visualizzazione di base.
ms.assetid: 11555BA0-D9BE-4239-A857-C9EEE86A8520
title: Attributo MF_MT_VIDEO_3D_LEFT_IS_BASE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8f5ece66db7de19cd77d7e686d9665ad239c6d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316442"
---
# <a name="mf_mt_video_3d_left_is_base-attribute"></a>MF \_ mt \_ video \_ 3D \_ Left \_ è l' \_ attributo di base

Per un formato video 3D, specifica quale visualizzazione è la visualizzazione di base.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Per impostazione predefinita, la visualizzazione a sinistra in una sequenza video 3D è la visualizzazione di base. Se la visualizzazione a destra è la visualizzazione di base, impostare questo attributo su **false**.

Per convertire il video stereoscopico in 2D, lasciare la visualizzazione di base ed eliminare l'altra visualizzazione.

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

 

 




