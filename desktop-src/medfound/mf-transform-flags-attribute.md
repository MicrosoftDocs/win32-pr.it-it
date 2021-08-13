---
description: Contiene flag per un Media Foundation di attivazione MFT (Media Foundation Transform).
ms.assetid: de377132-19b0-4c8c-882e-193c31420739
title: MF_TRANSFORM_FLAGS_Attribute attributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d54d8775cb58980e0b5b4a8557ae4a3e8082b045eb3e87330841f75dfd057774
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739229"
---
# <a name="mf_transform_flags_attribute-attribute"></a>Attributo MF \_ TRANSFORM \_ FLAGS \_

Contiene flag per un Media Foundation di attivazione MFT (Media Foundation Transform).

## <a name="data-type"></a>Tipo di dati

**UINT32**

Il valore è **un'operazione OR** bit per bit di flag [**\_ dell'enumerazione MFT \_ ENUM \_ FLAG.**](/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag)

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Commenti

Questo attributo viene impostato sui [**puntatori IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) restituiti dalla [**funzione MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) L'attributo contiene flag che descrivono l'MFT.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 R2 \[ \| app UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 
