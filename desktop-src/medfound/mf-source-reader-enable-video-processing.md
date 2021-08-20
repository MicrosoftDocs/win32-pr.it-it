---
description: Abilita l'elaborazione video da parte del lettore di origine.
ms.assetid: b1ec1c0e-8042-4486-822f-eb106577c0b1
title: MF_SOURCE_READER_ENABLE_VIDEO_PROCESSING attributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 259bc463953fdd3e69ddec9fb479921632f97bbe658747aa0e051eb4e78a14c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117691476"
---
# <a name="mf_source_reader_enable_video_processing-attribute"></a>Attributo MF \_ SOURCE READER ENABLE VIDEO \_ \_ \_ \_ PROCESSING

Abilita l'elaborazione video da [parte del lettore di origine.](source-reader.md)

## <a name="data-type"></a>Tipo di dati

**UINT32**



| Valore                                                                                                                                                                | Significato                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="Nonzero"></span><span id="nonzero"></span><span id="NONZERO"></span><dl> <dt>**Diverso da zero**</dt> </dl> | Abilitare l'elaborazione video.<br/>            |
| <span id="Zero"></span><span id="zero"></span><span id="ZERO"></span><dl> <dt>**Zero**</dt> </dl>             | Disabilitare l'elaborazione video. Valore predefinito.<br/> |



 

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Commenti

Se questo attributo è **TRUE** (diverso da zero), il lettore di origine può eseguire l'elaborazione video limitata seguente su fotogrammi video non compressi:

-   Conversione da YUV a RGB-32.
-   Deinterlacciamento.

Queste operazioni vengono eseguite nel software e non sono ottimizzate per la riproduzione. Questa funzionalità è destinata alle applicazioni che elaborano un numero ridotto di fotogrammi, ad esempio per creare un'anteprima video, o alle applicazioni che non decodificano i fotogrammi in tempo reale. L'operazione di dinterlace interpola i dati da un singolo campo, pertanto è una perdita.

Evitare questa impostazione se si usa Direct3D per visualizzare i fotogrammi video, perché la GPU offre in genere funzionalità di elaborazione video migliori.

Se questo attributo è **TRUE,** gli attributi seguenti devono essere **FALSE**:

-   [MF \_ SOURCE \_ READER \_ D3D \_ MANAGER](mf-source-reader-d3d-manager.md)
-   [MF \_ READWRITE \_ DISABLE \_ CONVERTERS](mf-readwrite-disable-converters.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 R2 \[ \| app UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lettore di origine](source-reader.md)
</dt> <dt>

[Attributi del lettore di origine](source-reader-attributes.md)
</dt> </dl>

 

 




