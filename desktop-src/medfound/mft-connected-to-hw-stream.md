---
description: Specifica se una trasformazione di Media Foundation basata su hardware è connessa a un'altra MFT basata su hardware.
ms.assetid: 9166c43f-d2ae-4dc7-84e9-02146b67efe2
title: Attributo MFT_CONNECTED_TO_HW_STREAM (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d5a3e8e4da74b3d581dd5ae4a53a03dc2b0fd67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309080"
---
# <a name="mft_connected_to_hw_stream-attribute"></a>MFT \_ connesso \_ all' \_ \_ attributo del flusso HW

Specifica se una trasformazione di Media Foundation basata su hardware è connessa a un'altra MFT basata su hardware.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

Le applicazioni in genere non utilizzano questo attributo.

Questo attributo viene utilizzato con MFTs basato su hardware. Quando due MFTs hardware sono connessi all'interno di una topologia, il caricatore della topologia imposta questo attributo su **true** negli oggetti seguenti:

-   Il flusso di output del MFT upstream
-   Flusso di input della MFT downstream

Per ottenere l'archivio di attributi per il flusso di output, il caricatore della topologia chiama [**IMFTransform:: GetOutputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) nella MFT upstream. Per ottenere l'archivio di attributi per il flusso di input, il caricatore della topologia chiama [**IMFTransform:: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) nella MFT downstream.

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

 

 




