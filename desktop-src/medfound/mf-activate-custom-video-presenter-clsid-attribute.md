---
description: CLSID di un presentatore video personalizzato per il sink multimediale Enhanced video renderer (EVR).
ms.assetid: f035ee56-7582-45d3-bafe-dd9c821b6326
title: Attributo MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0eb913a56671d5d2ac8d27c785e1cc1fbfc51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307987"
---
# <a name="mf_activate_custom_video_presenter_clsid-attribute"></a>\_Attributo CLSID per l'attivazione del \_ \_ \_ prolatore video personalizzato \_

CLSID di un presentatore video personalizzato per il sink multimediale Enhanced video renderer (EVR).

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="remarks"></a>Commenti

Se si sta creando EVR tramite un oggetto Activation, è possibile usare questo attributo per impostare un presentatore video personalizzato in EVR. Usare questo attributo come indicato di seguito:

1.  Chiamare la funzione [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) per creare un oggetto Activation per il EVR. La funzione restituisce un puntatore all'interfaccia [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .

2.  Impostare questo attribue sul puntatore [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) chiamando [**IMFAttributes:: Seguid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid). Il valore dell'attributo è il CLSID del Presenter video personalizzato dell'applicazione.

Se questo attributo è impostato, EVR chiama **CoCreateInstance** con il CLSID specificato per creare il presentatore video personalizzato. Il presentatore video deve esporre l'interfaccia [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) . Il Presenter viene creato come un server COM in-process.

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

[**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes:: Seguid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[Oggetti attivazione](activation-objects.md)
</dt> <dt>

[Come scrivere un presentatore EVR](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




