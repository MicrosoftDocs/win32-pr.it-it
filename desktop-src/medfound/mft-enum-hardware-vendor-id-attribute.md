---
description: Specifica l'ID fornitore per un'istanza basata su hardware Microsoft Media Foundation.
ms.assetid: AA31639F-EF70-4454-AC61-60755CAA684A
title: MFT_ENUM_HARDWARE_VENDOR_ID_Attribute attributo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cff3a93abed968a26f8eead5be6a7d1872b9d4556b0d163632992cbcc21b1acd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973100"
---
# <a name="mft_enum_hardware_vendor_id_attribute-attribute"></a>Attributo ID FORNITORE \_ HARDWARE MFT ENUM \_ \_ \_ \_

Specifica l'ID fornitore per una trasformazione Microsoft Media Foundation basata su hardware (MFT).

## <a name="data-type"></a>Tipo di dati

**Wchar\***

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Per impostare questo attributo, chiamare [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Commenti

Questo attributo è informativo e facoltativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 app desktop \| app UWP\]<br/>                                          |
| Server minimo supportato<br/> | \[Windows Server 2012 app desktop \| app UWP\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mftransform.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFT hardware](hardware-mfts.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 




