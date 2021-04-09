---
description: Contiene un puntatore agli attributi del flusso del flusso connesso su una trasformazione di Media Foundation basata su hardware.
ms.assetid: 7e14a02e-4cbf-45aa-a6f5-2c53b2437127
title: Attributo MFT_CONNECTED_STREAM_ATTRIBUTE (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b182cbed78f5f9851b621de72bf691bf698b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880606"
---
# <a name="mft_connected_stream_attribute-attribute"></a>\_ \_ Attributo attributo flusso connesso MFT \_

Contiene un puntatore agli attributi del flusso del flusso connesso su una trasformazione di Media Foundation basata su hardware.

## <a name="data-type"></a>Tipo di dati

**IMFAttributes \** _ archiviato come _*IUnknown \**_

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [_ *IMFAttributes:: getunknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Commenti

Le applicazioni in genere non utilizzano questo attributo.

Questo attributo viene usato per MFTs che fungono da proxy per un dispositivo hardware. Per informazioni dettagliate, vedere [hardware MFTS](hardware-mfts.md).

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

[MFT \_ connesso \_ al \_ \_ flusso HW](mft-connected-to-hw-stream.md)
</dt> <dt>

[MFTs hardware](hardware-mfts.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 




