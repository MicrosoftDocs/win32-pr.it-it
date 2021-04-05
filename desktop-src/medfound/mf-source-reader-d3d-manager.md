---
description: Contiene un puntatore al Gestione dispositivi Microsoft Direct3D per il lettore di origine.
ms.assetid: 507d350e-da0c-42d0-8a8d-77618ee5a1dd
title: Attributo MF_SOURCE_READER_D3D_MANAGER (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43bf0d49bb2744ff8219f8d15a6316f11875455c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882222"
---
# <a name="mf_source_reader_d3d_manager-attribute"></a>\_ \_ \_ Attributo gestione D3D del lettore di origine MF \_

Contiene un puntatore al Gestione dispositivi Microsoft [Direct3D](direct3d-device-manager.md) per il [lettore di origine](source-reader.md).

## <a name="data-type"></a>Tipo di dati

**IDirect3DDeviceManager9 \* o IMFDXGIDeviceManager \*** archiviato come **IUnknown \** _

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [_ *IMFAttributes:: getunknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Commenti

Il valore di questo attributo può essere un puntatore all'interfaccia [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) o a un [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager).

Usare questo attributo per fornire un dispositivo Direct3D per i decodificatori video caricati dal lettore di origine. Se si imposta questo attributo e il decodificatore supporta l'accelerazione video Microsoft DirectX (DXVA), il lettore di origine utilizzerà il dispositivo Direct3D per allocare i buffer video. Questi buffer sono compatibili con il processore video DXVA 2. Vedere [elaborazione video DXVA](dxva-video-processing.md).

Utilizzare questo attributo con le funzioni seguenti:

-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

Questo attributo viene in genere impostato se si utilizza il lettore di origine per ottenere i fotogrammi video decodificati e si utilizza Direct3D per visualizzare i frame. L'impostazione di questo attributo consente al decodificatore di utilizzare DXVA.

Non impostare questo attributo se:

-   Si usa il lettore di origine per elaborare solo l'audio e non il video.
-   Si sta ricevendo video compressi dal lettore di origine. In tal caso, il lettore di origine non crea un decodificatore.

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

[Lettore di origine](source-reader.md)
</dt> <dt>

[Attributi lettore di origine](source-reader-attributes.md)
</dt> </dl>

 

 




