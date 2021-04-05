---
description: Specifica come creare un mixer personalizzato per il renderer video avanzato (EVR).
ms.assetid: 00e65718-885f-4e1f-9b06-66c7f5786851
title: Attributo MF_ACTIVATE_CUSTOM_VIDEO_MIXER_FLAGS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b17a0063b7ef4b6a1cbb5993ea2fb7af2a4a678
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757868"
---
# <a name="mf_activate_custom_video_mixer_flags-attribute"></a>Attributo per l' \_ attivazione di \_ \_ \_ flag mixer video personalizzati \_

Specifica come creare un mixer personalizzato per il renderer video avanzato (EVR).

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

È possibile impostare questo attributo sul puntatore [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) ottenuto dalla funzione [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) . Il valore di questo attributo è un **or** bit per bit dei valori seguenti.



| Valore                                      | Descrizione                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ \_ ALLOWFAIL mixer personalizzato MF \_ Activate** | Se il metodo [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) non riesce a creare il mixer personalizzato dell'applicazione, USA invece il mixer EVR predefinito. Per impostazione predefinita, se l'oggetto [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) ha esito negativo quando tenta di creare il mixer personalizzato, il metodo **ActivateObject** ha esito negativo. |



 

Le applicazioni possono usare l'attributo [**MF \_ Activate \_ Custom \_ video \_ mixer \_ CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md) per specificare un mixer personalizzato per la EVR.

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

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Oggetti attivazione](activation-objects.md)
</dt> </dl>

 

 




