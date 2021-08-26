---
description: Specifica la categoria di dispositivi per un dispositivo di acquisizione video.
ms.assetid: 008ff9df-ebe0-4efd-a62c-24f4a4239ebd
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_CATEGORY attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 140a9055bdc8081d5cdea1931b199dcd00f537e73051f30790f036be4af57fb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060791"
---
# <a name="mf_devsource_attribute_source_type_vidcap_category-attribute"></a>Attributo MF \_ DEVSOURCE \_ ATTRIBUTE SOURCE TYPE \_ \_ \_ VIDCAP \_ CATEGORY

Specifica la categoria di dispositivi per un dispositivo di acquisizione video.

## <a name="data-type"></a>Tipo di dati

**GUID**

Viene definito il valore seguente.



| Valore                                                                                                                                                                                                                                                             | Significato                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="CLSID_VideoInputDeviceCategory"></span><span id="clsid_videoinputdevicecategory"></span><span id="CLSID_VIDEOINPUTDEVICECATEGORY"></span><dl> <dt>**CLSID \_ VideoInputDeviceCategory**</dt> </dl> | Dispositivo di acquisizione video.<br/> |



 

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).

Per impostare questo attributo, chiamare [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Commenti

Usare questo attributo come input per la [**funzione MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) durante l'enumerazione dei dispositivi di acquisizione video.

Inoltre, questo attributo viene impostato sugli oggetti di attivazione restituiti dalle funzioni seguenti:

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

L'attributo si applica solo ai dispositivi di acquisizione video.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Acquisizione di audio/video](audio-video-capture.md)
</dt> <dt>

[Acquisire gli attributi del dispositivo](capture-device-attributes.md)
</dt> </dl>

 

 




