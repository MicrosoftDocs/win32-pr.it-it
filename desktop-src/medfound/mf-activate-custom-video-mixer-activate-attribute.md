---
description: Specifica un oggetto di attivazione che crea un mixer video personalizzato per il sink multimediale EVR (Enhanced Video Renderer).
ms.assetid: 60484f87-7588-4b52-93aa-ef8fad66d971
title: MF_ACTIVATE_CUSTOM_VIDEO_MIXER_ACTIVATE attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1966efe66efaba56c0206a9f6fac59aba30a1aea9d47100c4ce19a30af96a863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117877298"
---
# <a name="mf_activate_custom_video_mixer_activate-attribute"></a>MF \_ ACTIVATE CUSTOM VIDEO \_ \_ \_ MIXER ACTIVATE \_ attribute

Specifica un oggetto di attivazione che crea un mixer video personalizzato per il sink multimediale EVR (Enhanced Video Renderer).

## <a name="data-type"></a>Tipo di dati

**IUnknown\***

## <a name="remarks"></a>Commenti

Se si crea l'EVR tramite un oggetto di attivazione, è possibile usare questo attributo per impostare un mixer video personalizzato nell'EVR. Usare questo attributo come segue:

1.  Chiamare la [**funzione MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) per creare un oggetto di attivazione per l'EVR. La funzione restituisce un puntatore [**all'interfaccia IMFActivate.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
2.  Impostare questo attributo sul [**puntatore IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) chiamando [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown). Il valore dell'attributo è un puntatore a un oggetto di attivazione implementato dal chiamante. L'oggetto di attivazione del chiamante deve esporre **l'interfaccia IMFActivate.**

Se si imposta questo attributo, l'EVR chiama [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) per creare il mixer video personalizzato. Il mixer video deve esporre [**l'interfaccia IMFTransform.**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del renderer video avanzato](enhanced-video-renderer-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[Oggetti di attivazione](activation-objects.md)
</dt> </dl>

 

 




