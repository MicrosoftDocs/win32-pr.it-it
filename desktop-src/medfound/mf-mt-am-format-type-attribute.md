---
description: Contiene un GUID DirectShow formato per un tipo di supporto.
ms.assetid: dc532791-39e1-4acb-9e62-21d8f25be870
title: MF_MT_AM_FORMAT_TYPE attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eff59e148f7532cc07e47acf033de91b5eaeb8969f0c39376850738fd54e758e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973630"
---
# <a name="mf_mt_am_format_type-attribute"></a>Attributo \_ MF MT \_ AM \_ FORMAT \_ TYPE

Contiene un GUID DirectShow formato per un tipo di supporto.

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="remarks"></a>Commenti

Questo attributo può essere impostato quando un DirectShow tipo di supporto viene convertito in un Media Foundation tipo di supporto. L'attributo indica il tipo di DirectShow originale. Il valore corrisponde al membro formattype della struttura [**AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)

Per un formato audio, [**l'attributo \_ MF MT \_ USER \_ DATA**](mf-mt-user-data-attribute.md) potrebbe contenere il blocco di formato originale, se il DirectShow non è stato riconosciuto.

Non impostare questo attributo su un tipo di supporto a meno che non si converta una struttura DirectShow formato.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                     |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del tipo di supporto](media-type-attributes.md)
</dt> <dt>

[Conversioni di tipi di supporti](media-type-conversions.md)
</dt> <dt>

[Tipi di supporti](media-types.md)
</dt> <dt>

[**IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**MFCreateMediaTypeFromRepresentation**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatypefromrepresentation)
</dt> </dl>

 

 
