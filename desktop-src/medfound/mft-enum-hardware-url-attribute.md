---
description: Contiene il collegamento simbolico per una trasformazione Media Foundation basata su hardware (MFT).
ms.assetid: 7e153051-a167-4ff7-8178-b290d8a1345e
title: MFT_ENUM_HARDWARE_URL_Attribute attributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7119ea4bde7900087f706cb6fbc77c845721debab54dfa05b48f5c0094b1e29e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722587"
---
# <a name="mft_enum_hardware_url_attribute-attribute"></a>Attributo URL \_ hardware MFT ENUM \_ \_ \_

Contiene il collegamento simbolico per una trasformazione Media Foundation basata su hardware (MFT).

## <a name="data-type"></a>Tipo di dati

**Wchar\***

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Per impostare questo attributo, chiamare [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Commenti

Questo attributo è supportato da MFT basati su hardware. Il valore dell'attributo è il collegamento simbolico per il driver di dispositivo. Questo attributo viene impostato anche sui puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) allocati dalla [**funzione MFTEnumEx,**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) quando tali puntatori rappresentano MFT basati su hardware.

Il collegamento simbolico deve essere considerato una stringa opaca. Per ottenere il nome visualizzato per un dispositivo, eseguire una query [sull'attributo MFT \_ FRIENDLY \_ NAME.](mft-friendly-name-attribute.md)

Gli MFT software non devono avere questo attributo impostato.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

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

[MFT hardware](hardware-mfts.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 




