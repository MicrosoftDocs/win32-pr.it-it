---
description: Specifica il formato di output di un dispositivo.
ms.assetid: 33a1b546-ece2-44ef-a1c0-5579c32be0bc
title: Attributo MF_DEVSOURCE_ATTRIBUTE_MEDIA_TYPE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a05283f33fa3b3bf4b9e339b830c2ae6a948ea82
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320669"
---
# <a name="mf_devsource_attribute_media_type-attribute"></a>\_Attributo del \_ \_ tipo di supporto attributo MF DEVSOURCE \_

Specifica il formato di output di un dispositivo.

## <a name="data-type"></a>Tipo di dati

**[**MFT \_ Registra \_ \_ informazioni sul tipo**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** archiviate come **byte \[ \]**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)SetAttribute.

## <a name="remarks"></a>Commenti

Questo attributo contiene una coppia di GUID: un tipo principale e un sottotipo. Questi GUID descrivono il formato di output predefinito del dispositivo. Il dispositivo potrebbe supportare formati di output aggiuntivi.

Se, ad esempio, un dispositivo di acquisizione video restituisce un video RGB-32, il valore di questo attributo è `{ MFMediaType_Video, MFVideoFormat_RGB32 }` .

Questo attributo è un suggerimento per l'applicazione. Per ottenere il formato di output esatto, creare l'origine multimediale per il dispositivo e ottenere il descrittore di presentazione dell'origine multimediale.

Questo attributo viene impostato sugli oggetti di attivazione restituiti dalle funzioni seguenti:

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

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

 

 




