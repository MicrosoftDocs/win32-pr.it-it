---
description: Contiene il collegamento simbolico per un driver di acquisizione video.
ms.assetid: 3d256dec-ec8c-4c62-883b-e2c292fd90eb
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd3b69899eb9df1973cb13611a822139ffda0e744c84137ff9d6094ed4a962d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104947"
---
# <a name="mf_devsource_attribute_source_type_vidcap_symbolic_link-attribute"></a>Attributo MF \_ DEVSOURCE \_ TIPO DI \_ ORIGINE \_ \_ VIDCAP \_ COLLEGAMENTO \_ SIMBOLICO

Contiene il collegamento simbolico per un driver di acquisizione video.

## <a name="data-type"></a>Tipo di dati

**Wchar\***

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Per impostare questo attributo, chiamare [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Commenti

Usare questo attributo come input per la [**funzione MFCreateDeviceSourceActivate.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)

Questo attributo viene inoltre impostato sugli oggetti di attivazione restituiti dalle funzioni seguenti:

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

Il collegamento simbolico deve essere considerato una stringa opaca. Il nome visualizzato leggibile per un dispositivo è contenuto nell'attributo [FRIENDLY \_ \_ \_ \_ NAME dell'ATTRIBUTO DEVSOURCE di MF.](mf-devsource-attribute-friendly-name.md)

L'attributo MF DEVSOURCE ATTRIBUTE SOURCE TYPE VIDCAP SYMBOLIC LINK può essere passato come valore dell'argomento DevicePath della \_ \_ funzione \_ \_ \_ \_ \_ [**SetupDiOpenDeviceInterface.**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea)

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

 

 
