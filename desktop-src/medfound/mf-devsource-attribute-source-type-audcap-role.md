---
description: Specifica il ruolo del dispositivo per un dispositivo di acquisizione audio.
ms.assetid: 4f2885b6-c771-4577-880d-5feea671432e
title: Attributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 148ae6697151698eef58d3c0148de3ed81822a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049716"
---
# <a name="mf_devsource_attribute_source_type_audcap_role-attribute"></a>\_Attributo del \_ \_ \_ \_ ruolo AUDCAP del tipo di origine dell'attributo \_ MF DEVSOURCE

Specifica il ruolo del dispositivo per un dispositivo di acquisizione audio.

## <a name="data-type"></a>Tipo di dati

**ERole** archiviato come **UInt32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

Il tipo di enumerazione **eRole** è documentato nella documentazione dell'API audio principale.

Il valore dell'attributo specifica un ruolo del dispositivo. Questo attributo viene utilizzato con le funzioni seguenti.

Questo attributo può essere usato come input per le funzioni [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) e [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) . Se viene specificato l'attributo, la funzione crea un'origine multimediale che usa il dispositivo di acquisizione audio predefinito per il ruolo del dispositivo specificato.

Questo attributo può essere usato anche come input per la funzione [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) . Se viene specificato l'attributo, l'enumerazione è limitata al ruolo del dispositivo specificato. Inoltre, ogni oggetto attivazione restituito dalla funzione **MFEnumDeviceSources** contiene questo attributo. L'attributo viene quindi usato internamente dall'oggetto attivazione quando crea l'origine multimediale.

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

 

 




