---
description: Specifica il nome visualizzato per un dispositivo.
ms.assetid: 3f6c7faf-2ecd-4510-adc2-252c3619d70f
title: MF_DEVSOURCE_ATTRIBUTE_FRIENDLY_NAME attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e90e019b37b251ad8ec00efbd3bd0395659b96c6dd2e3a1cad247ea17ace3ece
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973830"
---
# <a name="mf_devsource_attribute_friendly_name-attribute"></a>Attributo NOME \_ DESCRITTIVO \_ DELL'ATTRIBUTO DEVSOURCE \_ MF \_

Specifica il nome visualizzato per un dispositivo. Il *nome visualizzato* è una stringa leggibile, adatta per la visualizzazione in un'interfaccia utente.

## <a name="data-type"></a>Tipo di dati

**Wchar\***

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Per impostare questo attributo, chiamare [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Commenti

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

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Acquisizione di audio/video](audio-video-capture.md)
</dt> <dt>

[Acquisire gli attributi del dispositivo](capture-device-attributes.md)
</dt> </dl>

 

 




