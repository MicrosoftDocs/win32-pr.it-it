---
description: Specifica se un flusso di immagini ASF è un tipo JPEG degradabile.
ms.assetid: e29d0893-8561-4a8c-99e2-168186becd82
title: Attributo MF_MT_IMAGE_LOSS_TOLERANT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eea33f9f5f49725d164bd26ba21b9602bffef2b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879390"
---
# <a name="mf_mt_image_loss_tolerant-attribute"></a>\_Attributo a \_ \_ tolleranza di perdita immagine MF mt \_

Specifica se un flusso di immagini ASF è un tipo JPEG degradabile.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="applies-to"></a>Si applica a

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Commenti

Questo attributo si applica al tipo di supporto per i flussi di immagine in ASF. Se il valore è **true**, il flusso è un tipo di immagine JPEG degradabile. In caso contrario, il flusso è un tipo di immagine JFIF. Per ulteriori informazioni su questi tipi di flusso, vedere la specifica ASF.

Oltre all' \_ attributo MF mt \_ Image \_ Loss \_ tolerance, il tipo di supporto per un flusso di immagini ASF contiene gli attributi seguenti:



| Attributo                                                 | Descrizione                                |
|-----------------------------------------------------------|--------------------------------------------|
| [**\_ \_ tipo principale MF \_ mt**](mf-mt-major-type-attribute.md) | Contiene il valore **MFMediaType \_ Image**. |
| [**\_dimensioni del \_ frame MF mt \_**](mf-mt-frame-size-attribute.md) | Restituisce le dimensioni dell'immagine in pixel.            |



 

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

 

 




