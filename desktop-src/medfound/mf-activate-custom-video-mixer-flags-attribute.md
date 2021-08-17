---
description: Specifica come creare un mixer personalizzato per il renderer video avanzato (EVR).
ms.assetid: 00e65718-885f-4e1f-9b06-66c7f5786851
title: MF_ACTIVATE_CUSTOM_VIDEO_MIXER_FLAGS attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd536328bf454a70b35376aca3b7c6a0cea9ec7e0e2408a05cd6d0e8da0854ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957091"
---
# <a name="mf_activate_custom_video_mixer_flags-attribute"></a>Attributo MF \_ ACTIVATE \_ CUSTOM VIDEO \_ \_ MIXER \_ FLAGS

Specifica come creare un mixer personalizzato per il renderer video avanzato (EVR).

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

È possibile impostare questo attributo sul [**puntatore IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) ottenuto dalla [**funzione MFCreateVideoRendererActivate.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) Il valore di questo attributo è un **OR** bit per bit dei valori seguenti.



| Valore                                      | Descrizione                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MF \_ ACTIVATE \_ CUSTOM \_ MIXER \_ ALLOWFAIL** | Se il [**metodo IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) non riesce a creare il mixer personalizzato dell'applicazione, usa invece il mixer EVR predefinito. Per impostazione predefinita, se [**l'oggetto IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) ha esito negativo quando tenta di creare il mixer personalizzato, il **metodo ActivateObject** ha esito negativo. |



 

Le applicazioni possono usare [**l'attributo \_ \_ \_ \_ \_ CLSID MF ACTIVATE CUSTOM VIDEO MIXER**](mf-activate-custom-video-mixer-clsid-attribute.md) per specificare un mixer personalizzato per l'EVR.

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

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Oggetti di attivazione](activation-objects.md)
</dt> </dl>

 

 




