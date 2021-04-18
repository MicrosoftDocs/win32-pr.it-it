---
description: Handle per la finestra di ritaglio video.
ms.assetid: 883bc7cf-f52f-4cb5-a942-b42b429b17a9
title: Attributo MF_ACTIVATE_VIDEO_WINDOW (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a23253c0cd1e4ae90659838acbb58056f770419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314552"
---
# <a name="mf_activate_video_window-attribute"></a>\_Attributo attivazione \_ \_ finestra video MF

Handle per la finestra di ritaglio video.

## <a name="data-type"></a>Tipo di dati

**UINT64**

Considera come **DWORD \_ ptr** (**HWND**).

## <a name="remarks"></a>Commenti

Questo attributo si applica all'oggetto attivazione per il renderer video avanzato (EVR). Il valore viene impostato automaticamente quando si chiama [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) per creare l'oggetto attivazione di EVR.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi renderer video avanzati](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes:: UINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[Oggetti attivazione](activation-objects.md)
</dt> </dl>

 

 




