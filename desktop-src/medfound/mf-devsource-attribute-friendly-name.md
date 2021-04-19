---
description: Specifica il nome visualizzato per un dispositivo.
ms.assetid: 3f6c7faf-2ecd-4510-adc2-252c3619d70f
title: Attributo MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab0d2bb3c0e75d547e1249a83261b7c804743ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307972"
---
# <a name="mf_devsource_attribute_friendly_name-attribute"></a>\_Attributo del \_ \_ nome descrittivo dell'attributo MF DEVSOURCE \_

Specifica il nome visualizzato per un dispositivo. Il *nome visualizzato* è una stringa leggibile, adatta per la visualizzazione in un'interfaccia utente.

## <a name="data-type"></a>Tipo di dati

**WCHAR \** _

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [_ *IMFAttributes:: GetString* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Per impostare questo attributo, chiamare [**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Commenti

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

 

 




