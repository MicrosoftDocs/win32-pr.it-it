---
description: Per un tipo di supporto video, specifica il modo in cui vengono archiviati i frame video 3D in memoria.
ms.assetid: 880DF017-5841-4C0A-82AF-F092DEF5406B
title: Attributo MF_MT_VIDEO_3D_FORMAT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f2b12f907edb2875b3b121607509288787c8e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316443"
---
# <a name="mf_mt_video_3d_format-attribute"></a>\_ \_ \_ Attributo formato 3D video MF mt \_

Per un tipo di supporto video, specifica il modo in cui vengono archiviati i frame video 3D in memoria.

## <a name="data-type"></a>Tipo di dati

**MFVideo3DFormat** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un membro dell'enumerazione [**MFVideo3DFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) . L'attributo si applica solo se l'attributo del [ \_ \_ video \_ 3D MF mt](mf-mt-video-3d.md) è **true**.

Questo attributo è necessario per i formati video 3D non compressi. È facoltativo per i video compressi 3D. Un'origine multimediale che fornisce frame codificati potrebbe essere in grado di impostare l'attributo, in base alle informazioni contenute nel contenitore di file. In caso contrario, l'attributo deve essere impostato dal decodificatore nel tipo di supporto di output del decodificatore.

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

 

 




