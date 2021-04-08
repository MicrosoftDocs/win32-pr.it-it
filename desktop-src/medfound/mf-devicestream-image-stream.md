---
description: Specifica se un flusso in un'origine di acquisizione video è un flusso di immagini fisse.
ms.assetid: 52251A45-3603-41C7-A869-7F6319BD337F
title: Attributo MF_DEVICESTREAM_IMAGE_STREAM (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 382ce587574d6ec46509a460dfb964e23dd416d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752447"
---
# <a name="mf_devicestream_image_stream-attribute"></a>\_ \_ Attributo flusso di immagine MF DEVICESTREAM \_

Specifica se un flusso in un'origine di acquisizione video è un flusso di immagini fisse.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Alcune fotocamere video espongono un flusso di immagini ancora che produce immagini ad alta risoluzione. Il flusso di immagini potrebbe produrre immagini non compresse o immagini JPEG. Se la fotocamera ha un flusso di immagini, l'origine multimediale per il dispositivo di acquisizione imposta questo attributo su **true** nel flusso di immagini.

Per ottenere questo attributo, procedere come segue:

1.  Eseguire una query sull'origine multimediale per l'interfaccia [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .
2.  Chiamare [**IMFMediaSourceEx:: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) per ottenere un puntatore [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) per il flusso.
3.  Chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) per ottenere l'attributo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




