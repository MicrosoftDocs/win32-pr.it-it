---
description: Specifica il numero massimo di fotogrammi che verranno memorizzati nel buffer dall'origine di acquisizione video.
ms.assetid: af30606b-f1a0-4fbf-a831-05ed891f5d53
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_MAX_BUFFERS attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba50ad5489d08ba0fc986d56bef8d57c547fa0146a3bbb58290bca43009cc5af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973820"
---
# <a name="mf_devsource_attribute_source_type_vidcap_max_buffers-attribute"></a>Attributo MF \_ DEVSOURCE \_ ATTRIBUTE SOURCE TYPE \_ \_ \_ VIDCAP \_ MAX \_ BUFFERS attribute

Specifica il numero massimo di fotogrammi che verranno memorizzati nel buffer dall'origine di acquisizione video.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Commenti

Per impostazione predefinita, l'origine dell'acquisizione video buffera un massimo di un fotogramma alla volta. È possibile aumentare il limite del buffer impostando questo attributo.

Il modo corretto per impostare questo attributo dipende dalla funzione usata per creare l'origine multimediale:

-   [**MFCreateDeviceSource:**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)impostare l'attributo tramite il *parametro pAttributes* della funzione.
-   [**MFCreateDeviceSourceActivate:**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)imposta l'attributo tramite il *parametro pAttributes* della funzione.
-   [**MFEnumDeviceSources:**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)imposta l'attributo sul [**puntatore IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) restituito dalla funzione. Impostare l'attributo prima di [**chiamare IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

L'attributo si applica solo ai dispositivi di acquisizione video.

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

[Acquisire gli attributi del dispositivo](capture-device-attributes.md)
</dt> </dl>

 

 




