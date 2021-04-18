---
description: Contiene il valore Merit di un codec hardware.
ms.assetid: 1df40a42-4c02-473f-a87f-2ae2d42e4f4e
title: Attributo MFT_CODEC_MERIT_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74745244824bc766d0f7c1e691cb5f176d1da6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309081"
---
# <a name="mft_codec_merit_attribute-attribute"></a>\_Attributo attributo \_ Merit \_ codec MFT

Contiene il valore Merit di un codec hardware.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

Questo attributo viene impostato sull'oggetto Activation per una trasformazione Media Foundation (MFT) che rappresenta un codec hardware. Il valore dell'attributo è il valore Merit del codec.

Questo attributo controlla l'ordine in cui la funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) enumera i codec, se è impostato il flag di **\_ enumerazione MFT \_ \_ SORTANDFILTER** flag. MFTs con un valore Merit compare più in alto nell'elenco rispetto ad altri MFTs.

Questo attributo non contiene un valore attendibile. Per verificare il valore di Merit effettivo del codec, chiamare la funzione [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) .

Se il valore dell'attributo di \_ \_ attributo Merit codec MFT \_ non corrisponde al valore Merit recuperato da [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit), il metodo [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) ha esito negativo e restituisce il **\_ \_ \_ \_ merito del codec MF e non valido**.

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

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 




