---
description: Contiene un puntatore agli attributi del flusso connesso in una trasformazione Media Foundation (MFT) basata su hardware.
ms.assetid: 7e14a02e-4cbf-45aa-a6f5-2c53b2437127
title: MFT_CONNECTED_STREAM_ATTRIBUTE attributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2289b8f1e8d5d751f7aa69564b8bbd26d865b43efedb474529147385b1851bb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722567"
---
# <a name="mft_connected_stream_attribute-attribute"></a>Attributo MFT \_ CONNECTED \_ STREAM \_ ATTRIBUTE

Contiene un puntatore agli attributi del flusso connesso in una trasformazione Media Foundation (MFT) basata su hardware.

## <a name="data-type"></a>Tipo di dati

**IMFAttributes \* *_ archiviato come _* IUnknown\***

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Commenti

Le applicazioni in genere non usano questo attributo.

Questo attributo viene usato per i file MFT che fungono da proxy per un dispositivo hardware. Per informazioni dettagliate, vedere [MFT hardware.](hardware-mfts.md)

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

[MFT \_ CONNESSO \_ A \_ HW \_ STREAM](mft-connected-to-hw-stream.md)
</dt> <dt>

[MFT hardware](hardware-mfts.md)
</dt> <dt>

[Attributi di trasformazione](transform-attributes.md)
</dt> </dl>

 

 




