---
description: Specifica l'ID endpoint per un dispositivo di acquisizione audio.
ms.assetid: a0d8b54b-7a05-4307-a756-a34bb22f1afd
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6baafd2aa1bdfc3f4959b877963faff5df9aabe57c672555edb98f4cded8b1ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113951"
---
# <a name="mf_devsource_attribute_source_type_audcap_endpoint_id-attribute"></a>Attributo MF \_ DEVSOURCE \_ ATTRIBUTE SOURCE TYPE \_ \_ \_ AUDCAP \_ ENDPOINT \_ ID

Specifica l'ID endpoint per un dispositivo di acquisizione audio.

## <a name="data-type"></a>Tipo di dati

**Wchar\***

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Per impostare questo attributo, chiamare [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Commenti

Il valore dell'attributo è un ID endpoint. Questo attributo viene usato con le funzioni seguenti:

-   Può essere usato come input per le [**funzioni MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) e [**MFCreateDeviceSourceActivate.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) In questo contesto, l'attributo specifica il dispositivo di acquisizione audio per la funzione. È possibile ottenere l'ID endpoint per un determinato dispositivo chiamando il [**metodo IMMDevice::GetId.**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) Per altre informazioni, vedere la documentazione dell'API Audio core.
-   Quando la [**funzione MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) enumera i dispositivi audio, gli oggetti di attivazione restituiti contengono questo attributo. L'attributo viene usato internamente dall'oggetto di attivazione quando crea l'origine multimediale.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Acquisizione di audio/video](audio-video-capture.md)
</dt> <dt>

[Acquisire gli attributi del dispositivo](capture-device-attributes.md)
</dt> </dl>

 

 
