---
description: Per un formato video 3D, specifica quale visualizzazione è la visualizzazione di base.
ms.assetid: 11555BA0-D9BE-4239-A857-C9EEE86A8520
title: MF_MT_VIDEO_3D_LEFT_IS_BASE attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb03bc12d32b96abc52999ef6a3b21580c4ac1c59125a076b9eb1d620e0bd362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741593"
---
# <a name="mf_mt_video_3d_left_is_base-attribute"></a>Attributo MF \_ MT \_ VIDEO \_ 3D \_ LEFT IS \_ \_ BASE

Per un formato video 3D, specifica quale visualizzazione è la visualizzazione di base.

## <a name="data-type"></a>Tipo di dati

**BOOL** archiviato come **UINT32**

## <a name="remarks"></a>Commenti

Per impostazione predefinita, la visualizzazione a sinistra in una sequenza video 3D è la visualizzazione di base. Se la visualizzazione a destra è la visualizzazione di base, impostare questo attributo su **FALSE.**

Per convertire video stereoscopici in 2D, mantenere la visualizzazione di base ed eliminare l'altra visualizzazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                  |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                        |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




