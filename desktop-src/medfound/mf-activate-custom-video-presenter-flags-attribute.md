---
description: Specifica come creare un presentatore personalizzato per il renderer video avanzato (EVR).
ms.assetid: 40893e13-bf2e-4424-ae43-2b253fc0b622
title: MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb223224b7dc01dbfcbfe43962201e4c40871d2d7d1a2be0e5cf78ebcac21430
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723668"
---
# <a name="mf_activate_custom_video_presenter_flags-attribute"></a>Attributo MF \_ ACTIVATE \_ CUSTOM VIDEO \_ \_ PRESENTER \_ FLAGS

Specifica come creare un presentatore personalizzato per il renderer video avanzato (EVR).

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

È possibile impostare questo attributo sul [**puntatore IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) ottenuto dalla [**funzione MFCreateVideoRendererActivate.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) Il valore di questo attributo è **un'operazione OR** bit per bit dei valori seguenti.



| Valore                                          | Descrizione                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MF \_ ACTIVATE \_ CUSTOM \_ PRESENTER \_ ALLOWFAIL** | Se il [**metodo IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) non riesce a creare il presentatore personalizzato dell'applicazione, usa invece il presentatore EVR predefinito. Per impostazione predefinita, se [**l'oggetto IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) ha esito negativo quando tenta di creare il presentatore personalizzato, il **metodo ActivateObject** ha esito negativo. |



 

Le applicazioni possono usare [**l'attributo \_ \_ \_ \_ \_ CLSID MF ACTIVATE CUSTOM VIDEO PRESENTER**](mf-activate-custom-video-presenter-clsid-attribute.md) per specificare un presentatore personalizzato per EVR.

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

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Oggetti di attivazione](activation-objects.md)
</dt> <dt>

[Come scrivere un presentatore EVR](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




