---
description: Specifica la categoria per una trasformazione Media Foundation (MFT).
ms.assetid: cebd64ea-b20f-4ccc-805f-0deab3096bc3
title: Attributo MF_TRANSFORM_CATEGORY_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3c64fd5e19bba10646957e7c247294b6d82a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226371"
---
# <a name="mf_transform_category_attribute-attribute"></a>\_Attributo dell' \_ \_ attributo Category di MF Transform

Specifica la categoria per una trasformazione Media Foundation (MFT).

## <a name="data-type"></a>Tipo di dati

**GUID**

Per un elenco di valori possibili, vedere [**la \_ categoria MFT**](mft-category.md).

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetGuid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).

Per impostare questo attributo, chiamare [**IMFAttributes:: Seguid**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Commenti

Questo attributo viene impostato sui puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) restituiti dalla funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | App desktop di Windows Server 2008 R2 \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 




