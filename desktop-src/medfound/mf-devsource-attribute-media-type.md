---
description: Specifica il formato di output di un dispositivo.
ms.assetid: 33a1b546-ece2-44ef-a1c0-5579c32be0bc
title: MF_DEVSOURCE_ATTRIBUTE_MEDIA_TYPE attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb4685f419658ecf77782a4cef770fd205119bb6cfd95523edb7fbbe001fd700
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105037"
---
# <a name="mf_devsource_attribute_media_type-attribute"></a>Attributo \_ MEDIA \_ \_ TYPE dell'ATTRIBUTO DEVSOURCE MF \_

Specifica il formato di output di un dispositivo.

## <a name="data-type"></a>Tipo di dati

**[**MFT \_ REGISTER \_ TYPE \_ INFO archiviato**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** come **BYTE \[ \]**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Per impostare questo attributo, chiamare [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Commenti

Questo attributo contiene una coppia di GUID: un tipo principale e un sottotipo. Questi GUID descrivono il formato di output predefinito del dispositivo. Il dispositivo potrebbe supportare formati di output aggiuntivi.

Ad esempio, se un dispositivo di acquisizione video restituisce un video RGB-32, il valore di questo attributo è `{ MFMediaType_Video, MFVideoFormat_RGB32 }` .

Questo attributo è un suggerimento per l'applicazione. Per ottenere il formato di output esatto, creare l'origine multimediale per il dispositivo e ottenere il descrittore di presentazione dell'origine multimediale.

Questo attributo viene impostato sugli oggetti di attivazione restituiti dalle funzioni seguenti:

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Acquisizione di audio/video](audio-video-capture.md)
</dt> <dt>

[Acquisisci attributi dispositivo](capture-device-attributes.md)
</dt> </dl>

 

 




