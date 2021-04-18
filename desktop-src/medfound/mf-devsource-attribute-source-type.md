---
description: Specifica un tipo di dispositivi, ad esempio acquisizione audio o acquisizione video.
ms.assetid: c6c05267-1c93-48e2-b463-b5a1514f1b7b
title: Attributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3445c74b1a77472bad564f6988f9ae2f4696fef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307970"
---
# <a name="mf_devsource_attribute_source_type-attribute"></a>\_Attributo del \_ tipo di origine dell'attributo MF DEVSOURCE \_ \_

Specifica un tipo di dispositivo, ad esempio acquisizione audio o acquisizione video.

## <a name="data-type"></a>Tipo di dati

**GUID**

Per questo attributo sono definiti i valori seguenti:



| Valore                                                                                                                                                                                                                                                                 | Significato                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_audcap_guid"></span><dl> <dt>**\_tipo di origine dell'attributo MF DEVSOURCE \_ \_ \_ \_ AUDCAP \_ GUID**</dt> </dl> | Dispositivo di acquisizione audio.<br/> |
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_vidcap_guid"></span><dl> <dt>**\_tipo di origine dell'attributo MF DEVSOURCE \_ \_ \_ \_ VidCap \_ GUID**</dt> </dl> | Dispositivo di acquisizione video.<br/> |



 

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).

Per impostare questo attributo, chiamare [**IMFAttributes:: Seguid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Commenti

Utilizzare questo attributo come input per le funzioni seguenti:

-   [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)
-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

Inoltre, questo attributo viene impostato sugli oggetti di attivazione restituiti dalla funzione [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) .

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Acquisizione di audio/video](audio-video-capture.md)
</dt> <dt>

[Acquisisci attributi del dispositivo](capture-device-attributes.md)
</dt> </dl>

 

 




