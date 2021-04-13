---
description: Abilita l'elaborazione video avanzata da parte del lettore di origine, tra cui conversione dello spazio colore, deinterlacciamento, ridimensionamento video e conversione della frequenza dei fotogrammi.
ms.assetid: 1055CD55-4B25-4EEC-AF1B-C84C52287F8F
title: Attributo MF_SOURCE_READER_ENABLE_ADVANCED_VIDEO_PROCESSING (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6978239c5c1c466c78a310b38b5d10bd41f9e004
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525998"
---
# <a name="mf_source_reader_enable_advanced_video_processing-attribute"></a>MF \_ source \_ Reader \_ Abilita \_ l' \_ attributo Advanced video \_ Processing

Abilita l'elaborazione video avanzata da parte del [lettore di origine](source-reader.md), tra cui conversione dello spazio colore, deinterlacciamento, ridimensionamento video e conversione della frequenza dei fotogrammi.

## <a name="data-type"></a>Tipo di dati

**Bool** archiviato come **UInt32**

## <a name="remarks"></a>Commenti

Se questo attributo è **true**, il lettore di origine può inserire un processore video nella pipeline di elaborazione, che consente i tipi di conversione di formato seguenti:

-   Conversione dello spazio colore (YUV a RGB-32)
-   Deinterlacciamento
-   Ridimensionamento video
-   Conversione della frequenza di frame

Se questo attributo è **true**, è necessario che l'attributo [MF \_ ReadWrite \_ Disable \_ Converters](mf-readwrite-disable-converters.md) sia **impostato su false**.

Il lettore di origine cerca i processori video registrati nella categoria **MFT \_ categoria \_ \_ processore video** , inclusi MFTS registrati per il processo locale. Per ulteriori informazioni sulla registrazione locale di MFTs, vedere [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) . Il lettore di origine utilizza il processore transcodificatore video (XVP) se non viene trovato altro elaboratore video appropriato.

L'applicazione specifica il tipo di output desiderato chiamando [**IMFSourceReader:: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype). Quando il lettore di origine configura il processore video, tenta di trovare la corrispondenza con gli attributi seguenti del tipo di output:

-   Frequenza fotogrammi[( \_ \_ \_ frequenza del frame MF mt](mf-mt-frame-rate-attribute.md))
-   Dimensioni frame ([ \_ dimensioni del \_ frame \_ MF mt](mf-mt-frame-size-attribute.md))
-   Modalità interlacciata ([ \_ \_ \_ modalità di interpolazione MF mt](mf-mt-interlace-mode-attribute.md))
-   Proporzioni pixel (proporzioni del[ \_ pixel MF mt \_ \_ \_ ](mf-mt-pixel-aspect-ratio-attribute.md))
-   Sottotipo ([ \_ \_ sottotipo MF mt](mf-mt-subtype-attribute.md))

Questo attributo è simile all'attributo [di \_ \_ \_ \_ \_ elaborazione video dell'abilitazione del lettore di origine MF](mf-source-reader-enable-video-processing.md) , ma offre i vantaggi seguenti:

-   È supportata un'ampia gamma di conversioni di formato.
-   Le applicazioni possono registrare i propri convertitori.
-   Alcune conversioni possono essere eseguite nell'hardware usando la GPU.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 8 app \[ \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2012 \|\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lettore di origine](source-reader.md)
</dt> <dt>

[Attributi lettore di origine](source-reader-attributes.md)
</dt> </dl>

 

 




