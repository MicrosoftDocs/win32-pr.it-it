---
description: Specifica se un flusso di immagini ASF è un tipo JPEG degradabile.
ms.assetid: e29d0893-8561-4a8c-99e2-168186becd82
title: MF_MT_IMAGE_LOSS_TOLERANT attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fdf5b2633586cf4b73279a636119ac4770a5321d6bc22b5b961fa85881019b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035169"
---
# <a name="mf_mt_image_loss_tolerant-attribute"></a>Attributo MF \_ MT \_ IMAGE LOSS \_ \_ TOLERANT

Specifica se un flusso di immagini ASF è un tipo JPEG degradabile.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Si applica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Commenti

Questo attributo si applica al tipo di supporto per i flussi di immagini in ASF. Se il valore è **TRUE,** il flusso è un tipo di immagine JPEG degradabile. In caso contrario, il flusso è un tipo di immagine JFIF. Per altre informazioni su questi tipi di flusso, vedere la specifica ASF.

Oltre all'attributo MF \_ MT \_ IMAGE LOSS TOLERANT, il tipo di supporto per un flusso di immagine \_ \_ ASF contiene gli attributi seguenti:



| Attributo                                                 | Descrizione                                |
|-----------------------------------------------------------|--------------------------------------------|
| [**MF \_ MT \_ MAJOR \_ TYPE**](mf-mt-major-type-attribute.md) | Contiene il valore **MFMediaType \_ Image**. |
| [**DIMENSIONI \_ DEL FRAME MT \_ \_ MF**](mf-mt-frame-size-attribute.md) | Fornisce le dimensioni dell'immagine in pixel.            |



 

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 R2 \[ \|\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




