---
description: Contiene il collegamento simbolico per un driver di acquisizione video.
ms.assetid: 3d256dec-ec8c-4c62-883b-e2c292fd90eb
title: Attributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48e1c854ee070713462676482cc04690c2bdde2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130722"
---
# <a name="mf_devsource_attribute_source_type_vidcap_symbolic_link-attribute"></a>Attributo MF \_ DEVSOURCE \_ tipo di \_ origine attributo \_ \_ VidCap \_ collegamento simbolico \_

Contiene il collegamento simbolico per un driver di acquisizione video.

## <a name="data-type"></a>Tipo di dati

**WCHAR \** _

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [_ *IMFAttributes:: GetString* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Per impostare questo attributo, chiamare [**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Commenti

Utilizzare questo attributo come input per la funzione [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) .

Inoltre, questo attributo viene impostato sugli oggetti di attivazione restituiti dalle funzioni seguenti:

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

Il collegamento simbolico deve essere considerato una stringa opaca. Il nome visualizzato leggibile per un dispositivo è contenuto nell'attributo del [ \_ \_ \_ \_ nome descrittivo dell'attributo MF DEVSOURCE](mf-devsource-attribute-friendly-name.md) .

\_ \_ \_ \_ È possibile passare l'attributo di collegamento simbolico VidCap del tipo di origine dell'attributo MF DEVSOURCE \_ \_ \_ come valore dell'argomento DevicePath della funzione [**SetupDiOpenDeviceInterface**](/windows/win32/api/setupapi/nf-setupapi-setupdiopendeviceinterfacea) .

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

 

 
