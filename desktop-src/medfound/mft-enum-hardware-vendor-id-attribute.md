---
description: Specifica l'ID fornitore per un Microsoft Media Foundation basato su hardware.
ms.assetid: AA31639F-EF70-4454-AC61-60755CAA684A
title: Attributo MFT_ENUM_HARDWARE_VENDOR_ID_Attribute
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c4d92585936e52cbb0b9b65201a5de0d3a02b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309078"
---
# <a name="mft_enum_hardware_vendor_id_attribute-attribute"></a>\_ \_ \_ \_ Attributo attributo ID fornitore hardware MFT enum \_

Specifica l'ID fornitore per una trasformazione di Microsoft Media Foundation basata su hardware (MFT).

## <a name="data-type"></a>Tipo di dati

**WCHAR \** _

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [_ *IMFAttributes:: GetString* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Per impostare questo attributo, chiamare [**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Commenti

Questo attributo è informativo e facoltativo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                          |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Mftransform. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFTs hardware](hardware-mfts.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 




