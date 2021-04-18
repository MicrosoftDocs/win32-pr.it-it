---
description: Specifica le caratteristiche precedenti dell'origine multimediale.
ms.assetid: 9779f350-60d5-4129-bada-0c4a58f93e6a
title: Attributo MF_EVENT_SOURCE_CHARACTERISTICS_OLD (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb19505643de064e3aa54abc9e37649ecd97ff9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309563"
---
# <a name="mf_event_source_characteristics_old-attribute"></a>\_Caratteristiche dell' \_ origine evento MF \_ \_ attributo obsoleto

Specifica le caratteristiche precedenti dell'origine multimediale. I dati dell'attributo sono un **operatore OR** bit per bit di flag dell'enumerazione delle [**\_ caratteristiche MFMEDIASOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Questo attributo viene utilizzato con l'evento [MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) .

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi dell'evento](event-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> </dl>

 

 




