---
title: Informazioni di riferimento su Gestione compressione video
description: Informazioni di riferimento su Gestione compressione video
ms.assetid: dd678b24-62af-495f-bdd6-3082c1a753dd
keywords:
- Video per Windows (VFW), Gestione compressione video (VCM)
- VFW (Video per Windows),Gestione compressione video (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adffe57bd731736ed434dfdfa3c4ded4e643c66a0b5f9ea1c6085a71285e45c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804271"
---
# <a name="video-compression-manager-reference"></a>Informazioni di riferimento su Gestione compressione video

In questa sezione vengono descritte le funzioni, le strutture, i messaggi e le macro, associati a Gestione risorse virtuali. Questi elementi sono raggruppati nel modo seguente.

## <a name="compressor-installation-and-removal"></a>Installazione e rimozione di Unpressore

-   [**ICInstall**](/windows/desktop/api/Vfw/nf-vfw-icinstall)
-   [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [**ICOPEN**](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose)
-   [**ICRemove**](/windows/desktop/api/Vfw/nf-vfw-icremove)
-   [**ICOpenFunction**](/windows/desktop/api/Vfw/nf-vfw-icopenfunction)

## <a name="locating-and-opening-a-compressor"></a>Individuazione e apertura di un modello di compressione

-   [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [**ICOPEN**](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [**ICDecompressOpen**](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen)
-   [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [**ICClose**](/windows/desktop/api/Vfw/nf-vfw-icclose)

## <a name="selecting-compressors"></a>Selezione di compresse

-   [**ICCompressorSceglie**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)
-   [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree)
-   [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars)

## <a name="configuring-compressors"></a>Configurazione di Compressi

-   [**\_ICM Configurare**](icm-configure.md)
-   [**\_ICM GETSTATE**](icm-getstate.md)
-   [**\_ICM SETSTATE**](icm-setstate.md)
-   [**ICSendMessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage)

## <a name="compressor-information"></a>Informazioni sul compressore

-   [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [**\_ICM GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md)
-   [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat)
-   [**\_ICM GETDEFAULTQUALITY**](icm-getdefaultquality.md)
-   [**\_ICM Circa**](icm-about.md)

## <a name="single-image-compression"></a>Compressione a immagine singola

-   [**ICImageCompress**](/windows/desktop/api/Vfw/nf-vfw-icimagecompress)

## <a name="sequence-compression"></a>Compressione di sequenza

-   [**ICSeqCompressFrame**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe)
-   [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)
-   [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend)

## <a name="compvars"></a>COMPVARS

-   [**ICCompressorSceglie**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)

## <a name="image-data-compression"></a>Compressione dei dati delle immagini

-   [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress)
-   [**\_ICM \_COMPRIMI FORMATO \_ GET**](icm-compress-get-format.md)
-   [**\_ICM COMPRIMI \_ QUERY**](icm-compress-query.md)
-   [**\_ICM \_COMPRIMI GET \_ SIZE**](icm-compress-get-size.md)
-   [**\_ICM COMPRIMI \_ BEGIN**](icm-compress-begin.md)
-   [**\_ICM COMPRIMI \_ FINE**](icm-compress-end.md)

## <a name="compressor-monitoring"></a>Monitoraggio del conseore

-   [**ICSETSTATUSPROC**](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)

## <a name="decompressing-single-images"></a>Decompressione di singole immagini

-   [**ICImageDecompress**](/windows/desktop/api/Vfw/nf-vfw-icimagedecompress)

## <a name="decompressing-image-data"></a>Decompressione dei dati immagine

-   [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)
-   [**ICDecompressExBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin)
-   [**\_ICM DECOMPRESSEX \_ END**](icm-decompressex-end.md)
-   [**\_ICM DECOMPRESSIONE \_ DEL FORMATO \_ GET**](icm-decompress-get-format.md)
-   [**\_ICM DECOMPRIMERE \_ IL RIQUADRO GET \_**](icm-decompress-get-palette.md)
-   [**ICDecompressExQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)
-   [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress)
-   [**\_ICM DECOMPRESSIONE \_ BEGIN**](icm-decompress-begin.md)
-   [**\_ICM FINE \_ DECOMPRESSIONE**](icm-decompress-end.md)
-   [**\_ICM DECOMPRESSIONE \_ QUERY**](icm-decompress-query.md)

## <a name="using-hardware-drawing-capabilities"></a>Uso Hardware-Drawing funzionalità

-   [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin)
-   [**\_ICM DRAW \_ END**](icm-draw-end.md)
-   [**\_ICM SCARICAMENTO \_ DI DRAW**](icm-draw-flush.md)
-   [**\_ICM DRAW \_ QUERY**](icm-draw-query.md)
-   [**ICDrawSuggestFormat**](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat)
-   [**\_ICM INIZIO \_ DISEGNO**](icm-draw-start.md)
-   [**\_ICM DRAW \_ STOP**](icm-draw-stop.md)
-   [**\_ICM GETBUFFERSWANTED**](icm-getbufferswanted.md)
-   [**\_ICM DISEGNARE \_ L'OGGETTO**](icm-draw-realize.md)
-   [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw)
-   [**\_ICM GETTIME \_ DI DISEGNO**](icm-draw-gettime.md)
-   [**\_ICM DRAW \_ SETTIME**](icm-draw-settime.md)
-   [**\_ICM FINESTRA \_ DI DISEGNO**](icm-draw-window.md)
-   [**\_ICM DISEGNARE \_ L'OGGETTO**](icm-draw-realize.md)
-   [**\_ICM DISEGNARE \_ CHANGEPALETTE**](icm-draw-changepalette.md)
-   [**\_ICM DISEGNARE \_ RENDERBUFFER**](icm-draw-renderbuffer.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione compressione video](video-compression-manager.md)
</dt> </dl>

 

 




