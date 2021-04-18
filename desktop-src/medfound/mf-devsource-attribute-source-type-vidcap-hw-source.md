---
description: Specifica se un'origine di acquisizione video è un dispositivo hardware o software.
ms.assetid: 4a886124-54f1-4cd1-a22b-552e8c8d556f
title: Attributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_HW_SOURCE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e816e668267a23e67e7450b81a32cde454315bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309567"
---
# <a name="mf_devsource_attribute_source_type_vidcap_hw_source-attribute"></a>\_Tipo di \_ origine attributo MF DEVSOURCE \_ \_ \_ VidCap \_ \_ attributo Source HW

Specifica se un'origine di acquisizione video è un dispositivo hardware o software.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

Se il valore è **true**, l'origine di acquisizione è un dispositivo hardware. Se il valore è **false**, si tratta di un dispositivo software. Il valore predefinito è **false**.

Questo attributo viene impostato sugli oggetti di attivazione restituiti dalle funzioni seguenti:

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

L'attributo si applica solo ai dispositivi di acquisizione video.

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

 

 




