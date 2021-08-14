---
description: Specifica se il sink sample-grabber usa l'orologio di presentazione per pianificare i campioni.
ms.assetid: 780ec4a6-8e14-4b81-9d50-82b2850c70ae
title: MF_SAMPLEGRABBERSINK_IGNORE_CLOCK attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d757b02a060b4e598ff42d3bd8b9ad7f38af41143c807647aa6f2b8528677cf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474424"
---
# <a name="mf_samplegrabbersink_ignore_clock-attribute"></a>Attributo MF \_ SAMPLEGRABBERSINK \_ IGNORE \_ CLOCK

Specifica se il sink sample-grabber usa l'orologio di presentazione per pianificare i campioni.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Commenti

È possibile impostare questo attributo nell'oggetto attivazione creato dalla [**funzione MFCreateSampleGrabberSinkActivate.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) Impostare l'attributo prima di chiamare [**il metodo IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) sull'oggetto attivazione.

Per impostazione predefinita, quando il sink sample-grabber riceve un esempio, attende fino all'ora di presentazione dell'esempio per richiamare il callback dell'applicazione. Se l'attributo MF SAMPLEGRABBERSINK IGNORE CLOCK è diverso da zero, il \_ \_ sink sample-grabber ignora il clock di presentazione e richiama il callback non appena riceve ogni \_ esempio.

Utilizzo consigliato:

-   Se si desidera elaborare gli esempi il più rapidamente possibile, impostare questo attributo su **TRUE.**
-   Se si desidera che le chiamate al metodo di callback siano sincronizzate con l'orologio, non impostare questo attributo o impostarlo su **FALSE.** È possibile ottenere campioni leggermente avanti rispetto all'orologio, pur rimanendo sincronizzati, impostando l'attributo [**MF \_ SAMPLEGRABBERSINK \_ SAMPLE TIME \_ \_ OFFSET.**](mf-samplegrabbersink-sample-time-offset-attribute.md)

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

[Media Foundation attributi](media-foundation-attributes.md)
</dt> </dl>

 

 




