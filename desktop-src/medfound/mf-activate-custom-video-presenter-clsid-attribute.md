---
description: CLSID di un presentatore video personalizzato per il sink multimediale EVR (Enhanced Video Renderer).
ms.assetid: f035ee56-7582-45d3-bafe-dd9c821b6326
title: MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5afd39cf31cd0efaff4dc4d32756e1e27433d87fac643e4058897babd0f4f50f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877254"
---
# <a name="mf_activate_custom_video_presenter_clsid-attribute"></a>Attributo \_ \_ \_ \_ \_ CLSID MF ACTIVATE CUSTOM VIDEO PRESENTER

CLSID di un presentatore video personalizzato per il sink multimediale EVR (Enhanced Video Renderer).

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="remarks"></a>Commenti

Se si crea l'EVR tramite un oggetto attivazione, è possibile usare questo attributo per impostare un presentatore video personalizzato nell'EVR. Usare questo attributo come segue:

1.  Chiamare la [**funzione MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) per creare un oggetto attivazione per EVR. La funzione restituisce un puntatore [**all'interfaccia IMFActivate.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

2.  Impostare questo attributo sul puntatore [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) chiamando [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid). Il valore dell'attributo è il CLSID del presentatore video personalizzato dell'applicazione.

Se questo attributo è impostato, l'EVR chiama **CoCreateInstance** con il CLSID specificato per creare il presentatore video personalizzato. Il presentatore video deve esporre [**l'interfaccia IMFVideoPresenter.**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) Il presentatore viene creato come server COM in-process.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del renderer video avanzato](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[Oggetti di attivazione](activation-objects.md)
</dt> <dt>

[Come scrivere un presentatore EVR](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




