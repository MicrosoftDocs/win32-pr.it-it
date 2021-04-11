---
description: Contiene il collegamento simbolico per una trasformazione di Media Foundation basata su hardware (MFT).
ms.assetid: 7e153051-a167-4ff7-8178-b290d8a1345e
title: Attributo MFT_ENUM_HARDWARE_URL_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 539aa1ecbf8bf322e7397a50bb16175dbcca806f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226911"
---
# <a name="mft_enum_hardware_url_attribute-attribute"></a>\_ \_ \_ Attributo attributo URL dell' \_ enumerazione MFT

Contiene il collegamento simbolico per una trasformazione di Media Foundation basata su hardware (MFT).

## <a name="data-type"></a>Tipo di dati

**WCHAR \** _

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [_ *IMFAttributes:: GetString* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Per impostare questo attributo, chiamare [**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Commenti

Questo attributo è supportato da MFTs basato su hardware. Il valore dell'attributo è il collegamento simbolico per il driver di dispositivo. Questo attributo viene inoltre impostato sui puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) allocati dalla funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , quando tali puntatori rappresentano MFTS basati su hardware.

Il collegamento simbolico deve essere considerato una stringa opaca. Per ottenere il nome visualizzato per un dispositivo, eseguire una query sull'attributo [ \_ \_ nome descrittivo di MFT](mft-friendly-name-attribute.md) .

Per il software MFTs non deve essere impostato questo attributo.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

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

[MFTs hardware](hardware-mfts.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 




