---
description: Specifica il numero massimo di frame che l'origine di acquisizione video registrerà nel buffer.
ms.assetid: af30606b-f1a0-4fbf-a831-05ed891f5d53
title: Attributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_MAX_BUFFERS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa927d28b49da0eb0a0be40c3137f1cd9acf79b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307971"
---
# <a name="mf_devsource_attribute_source_type_vidcap_max_buffers-attribute"></a>\_Attributo MF DEVSOURCE \_ tipo di origine attributo \_ \_ \_ VidCap \_ Max \_ buffers

Specifica il numero massimo di frame che l'origine di acquisizione video registrerà nel buffer.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, l'origine di acquisizione video memorizza nel buffer un massimo di un frame alla volta. È possibile aumentare il limite del buffer impostando questo attributo.

Il modo corretto per impostare questo attributo dipende dalla funzione usata per creare l'origine multimediale:

-   [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource): impostare l'attributo tramite il parametro *pAttributes* della funzione.
-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate): impostare l'attributo tramite il parametro *pAttributes* della funzione.
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources): impostare l'attributo sul puntatore [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) restituito dalla funzione. Impostare l'attributo prima di chiamare [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

L'attributo si applica solo ai dispositivi di acquisizione video.

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

 

 




