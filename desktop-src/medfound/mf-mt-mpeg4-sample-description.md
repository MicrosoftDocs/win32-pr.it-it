---
description: Contiene la casella di descrizione dell'esempio per un file MP4 o 3GP.
ms.assetid: ea157988-bd15-465c-bd6a-6d33cc1a0323
title: Attributo MF_MT_MPEG4_SAMPLE_DESCRIPTION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4620ae0b50a2c6f2dae7663aab0c49f13bc5a162
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884189"
---
# <a name="mf_mt_mpeg4_sample_description-attribute"></a>\_Attributo della \_ \_ Descrizione dell'esempio MF mt MPEG4 \_

Contiene la casella di descrizione dell'esempio per un file MP4 o 3GP.

## <a name="data-type"></a>Tipo di dati

**BYTE\[\]**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Commenti

Nella casella Descrizione esempio viene descritta la codifica utilizzata per un flusso nel file.

L'origine file MPEG-4 imposta questo attributo sul tipo di supporto per ogni flusso. Il valore dell'attributo è costituito dai dati non elaborati nella casella Descrizione esempio. Se l'origine file MPEG-4 è in grado di analizzare la descrizione dell'esempio, aggiunge anche i dettagli del formato al tipo di supporto. In caso contrario, l'applicazione o il decodificatore deve analizzare la descrizione dell'esempio dall' \_ attributo MF mt \_ MPEG4 \_ Sample \_ Description.

Quando si imposta questo attributo sul sink MPEG-4 tramite il metodo [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) , i dati per l'attributo MF \_ mt \_ MPEG4 \_ Sample \_ Description non devono essere modificati dopo che uno o più campioni sono stati inviati al sink sull'interfaccia [**IMFStreamSink::P rocesssample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) del flusso corrispondente.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App desktop di Windows Server 2008 R2 \[ \| UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




