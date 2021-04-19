---
description: Specifica l'ID endpoint per un dispositivo di acquisizione audio.
ms.assetid: a0d8b54b-7a05-4307-a756-a34bb22f1afd
title: Attributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1448dc753a8e3b8221fa040309d3f5b60c4879
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325960"
---
# <a name="mf_devsource_attribute_source_type_audcap_endpoint_id-attribute"></a>Attributo MF \_ DEVSOURCE \_ tipo di \_ origine attributo \_ \_ AUDCAP \_ endpoint \_ ID

Specifica l'ID endpoint per un dispositivo di acquisizione audio.

## <a name="data-type"></a>Tipo di dati

**WCHAR\***

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Per impostare questo attributo, chiamare [**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Commenti

Il valore dell'attributo è un ID endpoint. Questo attributo viene usato con le funzioni seguenti:

-   Può essere usato come input per le funzioni [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) e [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) . In questo contesto, l'attributo specifica il dispositivo di acquisizione audio per la funzione. È possibile ottenere l'ID endpoint per un determinato dispositivo chiamando il metodo [**IMMDevice:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) . Per ulteriori informazioni, vedere la documentazione principale sull'API audio.
-   Quando la funzione [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) enumera i dispositivi audio, gli oggetti attivazione restituiti contengono questo attributo. L'attributo viene utilizzato internamente dall'oggetto Activation durante la creazione dell'origine multimediale.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Acquisizione di audio/video](audio-video-capture.md)
</dt> <dt>

[Acquisisci attributi del dispositivo](capture-device-attributes.md)
</dt> </dl>

 

 
