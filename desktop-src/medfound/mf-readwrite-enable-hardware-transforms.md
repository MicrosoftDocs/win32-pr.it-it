---
description: Consente al lettore di origine o al writer di sink di utilizzare le trasformazioni di Media Foundation basate su hardware (MFTs).
ms.assetid: 03f2fa76-b828-40b1-929d-60e7d5ab49bb
title: Attributo MF_READWRITE_ENABLE_HARDWARE_TRANSFORMS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 642be732a51f064d07e57609a886810f2a9c40b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347506"
---
# <a name="mf_readwrite_enable_hardware_transforms-attribute"></a>\_Attributo di \_ Abilitazione delle \_ \_ trasformazioni hardware MF ReadWrite

Consente al lettore di origine o al writer di sink di utilizzare le trasformazioni di Media Foundation basate su hardware (MFTs).

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il writer di origine e il writer di sink non utilizzano codificatori o codificatori hardware. Per abilitare l'uso di MFTs hardware, impostare questo attributo su **true** quando si crea il Reader di origine o il writer del sink.

Utilizzare questo attributo con le funzioni seguenti:

-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

Esiste un'eccezione per il comportamento predefinito. Il lettore di origine e il writer di sink utilizzano automaticamente MFTs registrati localmente nel processo del chiamante. Per registrare una MFT in locale, chiamare [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) o [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid). I MFTs hardware registrati localmente vengono usati anche se l'attributo **MF \_ ReadWrite \_ enable \_ hardware \_ Transformations** non è impostato.

Questo attributo non influisce sulla decodifica video con accelerazione hardware che usa l'accelerazione video DirectX (DXVA). Per abilitare la decodifica DXVA nel lettore di origine, impostare l'attributo di [ \_ \_ \_ \_ gestione D3D del lettore di origine MF](mf-source-reader-d3d-manager.md) .

Se questo attributo è **true**, non impostare l'attributo [MF \_ ReadWrite \_ Disable \_ Converters](mf-readwrite-disable-converters.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | App desktop di Windows Server 2008 R2 \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del writer di sink](sink-writer-attributes.md)
</dt> <dt>

[Attributi lettore di origine](source-reader-attributes.md)
</dt> </dl>

 

 




