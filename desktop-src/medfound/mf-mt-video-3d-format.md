---
description: Per un tipo di supporto video, specifica la modalità di archiviazione dei fotogrammi video 3D in memoria.
ms.assetid: 880DF017-5841-4C0A-82AF-F092DEF5406B
title: MF_MT_VIDEO_3D_FORMAT attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4100a605ecc7e8fe1c171b02341822972061363e7cd1b322162291dbd75b2c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692070"
---
# <a name="mf_mt_video_3d_format-attribute"></a>Attributo \_ MF MT \_ VIDEO \_ 3D \_ FORMAT

Per un tipo di supporto video, specifica la modalità di archiviazione dei fotogrammi video 3D in memoria.

## <a name="data-type"></a>Tipo di dati

**MFVideo3DFormat archiviato** come **UINT32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un membro [**dell'enumerazione MFVideo3DFormat.**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) L'attributo si applica solo se [l'attributo \_ MF MT \_ VIDEO \_ 3D](mf-mt-video-3d.md) è **TRUE.**

Questo attributo è obbligatorio per i formati video 3D non compressi. È facoltativo per i video 3D compressi. Un'origine multimediale che recapita fotogrammi codificati potrebbe essere in grado di impostare l'attributo in base alle informazioni nel contenitore di file. In caso contrario, l'attributo deve essere impostato dal decodificatore nel tipo di supporto di output del decodificatore.

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

 

 




