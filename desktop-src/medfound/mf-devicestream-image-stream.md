---
description: Specifica se un flusso in un'origine di acquisizione video è un flusso di immagini non ancorate.
ms.assetid: 52251A45-3603-41C7-A869-7F6319BD337F
title: MF_DEVICESTREAM_IMAGE_STREAM attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a42ec0ea6ac8f89c7b35e5ae137c92aaf62006b9b06be689bb7203626f36b7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118244764"
---
# <a name="mf_devicestream_image_stream-attribute"></a>Attributo \_ MF DEVICESTREAM \_ IMAGE \_ STREAM

Specifica se un flusso in un'origine di acquisizione video è un flusso di immagini non ancorate.

## <a name="data-type"></a>Tipo di dati

**BOOL** archiviato come **UINT32**

## <a name="remarks"></a>Commenti

Alcune videocamere espongono un flusso di immagini fisse che produce immagini ad alta risoluzione. Il flusso di immagini potrebbe produrre immagini non compresse o immagini JPEG. Se la fotocamera ha un flusso di immagini, l'origine multimediale per il dispositivo di acquisizione imposta questo attributo su **TRUE** nel flusso dell'immagine.

Per ottenere questo attributo, eseguire le operazioni seguenti:

1.  Eseguire una query sull'origine multimediale per [**l'interfaccia IMFMediaSourceEx.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex)
2.  Chiamare [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) per ottenere un [**puntatore IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) per il flusso.
3.  Chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) per ottenere l'attributo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                         |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




