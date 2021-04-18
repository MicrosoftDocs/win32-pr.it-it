---
description: Indica il numero di buffer non compressi richiesti dal sink multimediale EVR (Enhanced video renderer) per la deinterlacciamento.
ms.assetid: b62bff64-153f-4028-a546-250419dc4152
title: Attributo MF_SA_REQUIRED_SAMPLE_COUNT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe7d47370cd4877a0f9722d443bc6bb3f7bdeb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314029"
---
# <a name="mf_sa_required_sample_count-attribute"></a>\_ \_ \_ Attributo count di esempio \_ obbligatorio MF SA

Indica il numero di buffer non compressi richiesti dal sink multimediale EVR (Enhanced video renderer) per la deinterlacciamento.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Si tratta di un attributo a livello di flusso. Per ottenere l'attributo da EVR, eseguire le operazioni seguenti:

1.  Chiamare [**IMFMediaSink:: GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) per ottenere il sink del flusso.
2.  Eseguire una query sul sink di flusso per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
3.  Chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Internamente, il mixer fornisce questo attributo a EVR. Per ottenere l'attributo dal mixer, chiamare [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes).

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>                                    |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Attributi di Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 




