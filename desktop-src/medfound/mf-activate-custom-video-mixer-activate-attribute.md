---
description: Specifica un oggetto attivazione che consente di creare un mixer video personalizzato per il sink multimediale EVR (Enhanced video renderer).
ms.assetid: 60484f87-7588-4b52-93aa-ef8fad66d971
title: Attributo MF_ACTIVATE_CUSTOM_VIDEO_MIXER_ACTIVATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6268f3630b013235f3d365e0b8ab0578c9dd3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130727"
---
# <a name="mf_activate_custom_video_mixer_activate-attribute"></a>Attiva \_ l' \_ \_ \_ attributo Activate del mixer video personalizzato \_ MF

Specifica un oggetto attivazione che consente di creare un mixer video personalizzato per il sink multimediale EVR (Enhanced video renderer).

## <a name="data-type"></a>Tipo di dati

**IUnknown \** _

## <a name="remarks"></a>Commenti

Se si sta creando EVR tramite un oggetto Activation, è possibile usare questo attributo per impostare un mixer video personalizzato in EVR. Usare questo attributo come indicato di seguito:

1.  Chiamare la funzione [_ *MFCreateVideoRendererActivate* *](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) per creare un oggetto Activation per il EVR. La funzione restituisce un puntatore all'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .
2.  Impostare questo attributo sul puntatore [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) chiamando [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown). Il valore dell'attributo è un puntatore a un oggetto di attivazione implementato dal chiamante. L'oggetto attivazione del chiamante deve esporre l'interfaccia **IMFActivate** .

Se si imposta questo attributo, EVR chiama [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) per creare il mixer video personalizzato. Il mixer video deve esporre l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .

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

[**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[**IMFAttributes:: Unknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[Oggetti attivazione](activation-objects.md)
</dt> </dl>

 

 




