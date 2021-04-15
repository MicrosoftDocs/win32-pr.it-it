---
description: Consente l'elaborazione video da parte del lettore di origine.
ms.assetid: b1ec1c0e-8042-4486-822f-eb106577c0b1
title: Attributo MF_SOURCE_READER_ENABLE_VIDEO_PROCESSING (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfcbb076d5f42e784277dbd78101b473ec33905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484805"
---
# <a name="mf_source_reader_enable_video_processing-attribute"></a>MF \_ source \_ Reader \_ Abilita \_ l' \_ attributo elaborazione video

Consente l'elaborazione video da parte del [lettore di origine](source-reader.md).

## <a name="data-type"></a>Tipo di dati

**UINT32**



| Valore                                                                                                                                                                | Significato                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="Nonzero"></span><span id="nonzero"></span><span id="NONZERO"></span><dl> <dt>**Diverso da zero**</dt> </dl> | Abilitare l'elaborazione video.<br/>            |
| <span id="Zero"></span><span id="zero"></span><span id="ZERO"></span><dl> <dt>**Zero**</dt> </dl>             | Disabilitare l'elaborazione video. Valore predefinito.<br/> |



 

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

Se questo attributo è **true** (diverso da zero), il lettore di origine può eseguire l'elaborazione video limitata seguente nei fotogrammi video non compressi:

-   Conversione da YUV a RGB-32.
-   Deinterlacciamento.

Queste operazioni vengono eseguite nel software e non sono ottimizzate per la riproduzione. Questa funzionalità è destinata alle applicazioni che elaborano un numero ridotto di frame, ad esempio per creare un'anteprima video, o applicazioni che non decodificano i frame in tempo reale. L'operazione di deinterlacciamento esegue l'interpolazione dei dati da un singolo campo, in modo da avere un valore loss.

Evitare questa impostazione se si utilizza Direct3D per visualizzare i fotogrammi video, perché la GPU offre in genere migliori funzionalità di elaborazione video.

Se questo attributo è **true**, i seguenti attributi devono essere **false**:

-   [\_ \_ Gestione D3D del lettore di origine MF \_ \_](mf-source-reader-d3d-manager.md)
-   [MF \_ ReadWrite \_ Disabilita \_ convertitori](mf-readwrite-disable-converters.md)

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

 

 




