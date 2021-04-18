---
description: Specifica se il sink Sample-Grabber usa il clock di presentazione per pianificare gli esempi.
ms.assetid: 780ec4a6-8e14-4b81-9d50-82b2850c70ae
title: Attributo MF_SAMPLEGRABBERSINK_IGNORE_CLOCK (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ad5476779d958bdbf94af554d889dd8d174ca3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314028"
---
# <a name="mf_samplegrabbersink_ignore_clock-attribute"></a>\_ \_ Attributo Clock MF SAMPLEGRABBERSINK ignore \_

Specifica se il sink Sample-Grabber usa il clock di presentazione per pianificare gli esempi.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

È possibile impostare questo attributo sull'oggetto attivazione creato dalla funzione [**MFCreateSampleGrabberSinkActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) . Impostare l'attributo prima di chiamare il metodo [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) sull'oggetto Activation.

Per impostazione predefinita, quando il sink Sample-Grabber riceve un campione, attende che l'ora di presentazione dell'esempio richiami il callback dell'applicazione. Se l' \_ \_ attributo Clock MF SAMPLEGRABBERSINK ignore \_ è diverso da zero, il sink Sample-Grabber ignora il clock di presentazione e richiama il callback non appena riceve ogni campione.

Utilizzo consigliato:

-   Se si desidera elaborare i campioni il più rapidamente possibile, impostare questo attributo su **true**.
-   Se si desidera che le chiamate al metodo di callback siano sincronizzate con il clock, non impostare questo attributo o impostarlo su **false**. È possibile ottenere campioni leggermente più avanti rispetto al clock, rimanendo comunque sincronizzati, impostando l'attributo di [**\_ offset dell'ora di \_ esempio \_ \_ MF SAMPLEGRABBERSINK**](mf-samplegrabbersink-sample-time-offset-attribute.md) .

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

[Attributi di Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 




