---
title: Guida di riferimento a Gestione compressione video
description: Guida di riferimento a Gestione compressione video
ms.assetid: dd678b24-62af-495f-bdd6-3082c1a753dd
keywords:
- Video per Windows (VFW), Video Compression Manager (VCM)
- VFW (video per Windows), Gestione compressione video (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801df7ecdf0f6468762c2742235d4ef627f5aee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221122"
---
# <a name="video-compression-manager-reference"></a>Guida di riferimento a Gestione compressione video

Questa sezione descrive le funzioni, le strutture, i messaggi e le macro associate a VCM. Questi elementi vengono raggruppati come indicato di seguito.

## <a name="compressor-installation-and-removal"></a>Installazione e rimozione del compressore

-   [**ICInstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall)
-   [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [**ICOPEN**](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose)
-   [**ICRemove**](/windows/desktop/api/Vfw/nf-vfw-icremove)
-   [**ICOpenFunction**](/windows/desktop/api/Vfw/nf-vfw-icopenfunction)

## <a name="locating-and-opening-a-compressor"></a>Individuazione e apertura di un compressore

-   [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [**ICOPEN**](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen)
-   [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose)

## <a name="selecting-compressors"></a>Selezione di comprimeri

-   [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)
-   [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree)
-   [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars)

## <a name="configuring-compressors"></a>Configurazione di compressatori

-   [**configurazione di ICM \_**](icm-configure.md)
-   [**STATO di ICM \_**](icm-getstate.md)
-   [**\_stato MCI**](icm-setstate.md)
-   [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage)

## <a name="compressor-information"></a>Informazioni sul compressore

-   [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [**\_GETDEFAULTKEYFRAMERATE ICM**](icm-getdefaultkeyframerate.md)
-   [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat)
-   [**\_GETDEFAULTQUALITY ICM**](icm-getdefaultquality.md)
-   [**ICM \_ su**](icm-about.md)

## <a name="single-image-compression"></a>Compressione di immagini singole

-   [**ICImageCompress**](/windows/desktop/api/Vfw/nf-vfw-icimagecompress)

## <a name="sequence-compression"></a>Compressione sequenza

-   [**ICSeqCompressFrame**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe)
-   [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)
-   [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend)

## <a name="compvars"></a>COMPVARS

-   [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)

## <a name="image-data-compression"></a>Compressione dati immagine

-   [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress)
-   [**\_formato MCI compress \_ get \_**](icm-compress-get-format.md)
-   [**\_query di compressione ICM \_**](icm-compress-query.md)
-   [**\_ \_ dimensioni Get della compressione ICM \_**](icm-compress-get-size.md)
-   [**\_inizio compressione \_ ICM**](icm-compress-begin.md)
-   [**\_fine compressione \_ MCI**](icm-compress-end.md)

## <a name="compressor-monitoring"></a>Monitoraggio compressore

-   [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)

## <a name="decompressing-single-images"></a>Decompressione di immagini singole

-   [**ICImageDecompress**](/windows/desktop/api/Vfw/nf-vfw-icimagedecompress)

## <a name="decompressing-image-data"></a>Decompressione dei dati dell'immagine

-   [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)
-   [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin)
-   [**\_fine DECOMPRESSEX \_ ICM**](icm-decompressex-end.md)
-   [**\_formato di \_ ottenimento di MCI decompresso \_**](icm-decompress-get-format.md)
-   [**\_tavolozza Decomprimi MCI \_ get \_**](icm-decompress-get-palette.md)
-   [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)
-   [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress)
-   [**\_inizio decompressione ICM \_**](icm-decompress-begin.md)
-   [**\_fine Decomprimi MCI \_**](icm-decompress-end.md)
-   [**\_query di decompressione ICM \_**](icm-decompress-query.md)

## <a name="using-hardware-drawing-capabilities"></a>Uso delle funzionalità di Hardware-Drawing

-   [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin)
-   [**\_fine di disegnato ICM \_**](icm-draw-end.md)
-   [**\_ \_ SCARICAmento ICM**](icm-draw-flush.md)
-   [**\_query di estrazione ICM \_**](icm-draw-query.md)
-   [**ICDrawSuggestFormat**](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat)
-   [**\_inizio estrazione \_ ICM**](icm-draw-start.md)
-   [**\_arresto di disegnato ICM \_**](icm-draw-stop.md)
-   [**\_GETBUFFERSWANTED ICM**](icm-getbufferswanted.md)
-   [**\_progetto ICM \_ realizzato**](icm-draw-realize.md)
-   [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw)
-   [**\_tempo di elaborazione ICM \_**](icm-draw-gettime.md)
-   [**\_tempo di elaborazione ICM \_**](icm-draw-settime.md)
-   [**\_finestra di disegni ICM \_**](icm-draw-window.md)
-   [**\_progetto ICM \_ realizzato**](icm-draw-realize.md)
-   [**\_CHANGEPALETTE di disegni ICM \_**](icm-draw-changepalette.md)
-   [**\_RENDERBUFFER di disegni ICM \_**](icm-draw-renderbuffer.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione compressione video](video-compression-manager.md)
</dt> </dl>

 

 




