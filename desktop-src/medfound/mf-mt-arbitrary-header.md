---
description: Dati specifici del tipo per un flusso binario in un file ASF (Advanced Systems Format).
ms.assetid: 45608dde-894b-4204-80dc-505f068fb158
title: MF_MT_ARBITRARY_HEADER attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d824aad4f76947786f991807d2f7b301703e3e356d2d1cfb416aa634d49f93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826521"
---
# <a name="mf_mt_arbitrary_header-attribute"></a>Attributo \_ MF MT \_ ARBITRARY \_ HEADER

Dati specifici del tipo per un flusso binario in un file ASF (Advanced Systems Format).

## <a name="data-type"></a>Tipo di dati

**[**MT \_ ARBITRARY \_ HEADER archiviato**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)** come **BYTE \[ \]**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Per impostare questo attributo, chiamare [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Commenti

I file ASF possono contenere flussi con dati binari. L'attributo \_ MF MT ARBITRARY HEADER nel tipo di supporto contiene una \_ struttura MT \_ [**\_ ARBITRARY \_ HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) che descrive il flusso.

Oltre all'attributo MF MT ARBITRARY HEADER, il tipo di supporto per un flusso binario \_ \_ \_ ASF contiene gli attributi seguenti:



| Attributo                                                 | Descrizione                                            |
|-----------------------------------------------------------|--------------------------------------------------------|
| [**MF \_ MT \_ MAJOR \_ TYPE**](mf-mt-major-type-attribute.md) | Il valore dell'attributo è **Binario MFMediaType. \_** |
| [FORMATO \_ ARBITRARIO MF MT \_ \_](mf-mt-arbitrary-format.md)   | Contiene dati di formato aggiuntivi.                       |



 

> [!Note]  
> Nell'SDK Windows Media Format, i flussi binari sono denominati flussi *arbitrari* o *flussi di dati arbitrari.*

 

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> </dl>

 

 




