---
description: Contiene la casella di descrizione di esempio per un file MP4 o 3GP.
ms.assetid: ea157988-bd15-465c-bd6a-6d33cc1a0323
title: MF_MT_MPEG4_SAMPLE_DESCRIPTION attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c59827fa5d2ba6c6621c7e251cf319478fd621d24639e105dcd44863495b364
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741800"
---
# <a name="mf_mt_mpeg4_sample_description-attribute"></a>Attributo MF \_ MT \_ MPEG4 \_ SAMPLE \_ DESCRIPTION

Contiene la casella di descrizione di esempio per un file MP4 o 3GP.

## <a name="data-type"></a>Tipo di dati

**BYTE\[\]**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Per impostare questo attributo, chiamare [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="applies-to"></a>Si applica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Commenti

La casella di descrizione di esempio descrive la codifica usata per un flusso nel file.

L'origine file MPEG-4 imposta questo attributo sul tipo di supporto per ogni flusso. Il valore dell'attributo è i dati non elaborati nella casella della descrizione dell'esempio. Se l'origine file MPEG-4 può analizzare la descrizione dell'esempio, aggiunge anche i dettagli del formato al tipo di supporto. In caso contrario, l'applicazione o il decodificatore deve analizzare la descrizione di esempio dall'attributo \_ MF MT \_ MPEG4 \_ SAMPLE \_ DESCRIPTION.

Quando si imposta questo attributo nel sink MPEG-4 tramite il metodo [**IMFMediaTypeHandler::SetCurrentMediaType,**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) i dati per l'attributo MF MT MPEG4 SAMPLE DESCRIPTION non devono cambiare dopo l'invio di uno o più esempi al \_ \_ sink \_ \_ nell'interfaccia [**IMFStreamSink::P rocessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) del flusso corrispondente.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 R2 \[ \|\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi Media Foundation alfabetici](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




