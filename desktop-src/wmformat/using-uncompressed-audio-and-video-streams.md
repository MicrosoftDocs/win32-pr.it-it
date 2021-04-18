---
title: Uso di flussi audio e video non compressi
description: Uso di flussi audio e video non compressi
ms.assetid: 1a8fe604-bd99-4ba1-878f-8e1fd89483b3
keywords:
- flussi, configurazione di flussi audio e video non compressi
- codec, configurazione di flussi audio e video non compressi
- flussi video, non compressi
- flussi audio, non compressi
- flussi audio e video non compressi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00d81bd0a9f8c53751e404a0cfb0e55d57d4242
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299431"
---
# <a name="using-uncompressed-audio-and-video-streams"></a>Uso di flussi audio e video non compressi

Nella maggior parte dei casi, i supporti non compressi hanno requisiti di archiviazione e di distribuzione di grandi dimensioni, ma per alcuni scenari di riproduzione locali il livello di qualità è sufficientemente importante da garantire la mancata utilizzo della compressione.

Le impostazioni per un flusso multimediale non compresso devono riflettere le impostazioni del supporto di origine. Quando si configura un flusso non compresso, è necessario calcolare la velocità in bit del supporto e impostare il flusso in modo appropriato chiamando [**IWMStreamConfig:: bitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate). Poiché i flussi non compressi non possono essere usati per lo streaming, è sempre necessario impostare la finestra buffer per i flussi multimediali non compressi su zero chiamando [**IWMStreamConfig:: SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow).

I formati pixel seguenti sono supportati per i flussi video non compressi:

-   \_RGB555 WMMEDIASUBTYPE
-   \_RGB24 WMMEDIASUBTYPE
-   \_Rgb32 WMMEDIASUBTYPE
-   \_I420 WMMEDIASUBTYPE
-   \_IYUV WMMEDIASUBTYPE
-   \_YV12 WMMEDIASUBTYPE
-   \_YUY2 WMMEDIASUBTYPE
-   \_UYVY WMMEDIASUBTYPE
-   \_YVYU WMMEDIASUBTYPE

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione comune a tutti i flussi**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurazione di flussi audio**](configuring-audio-streams.md)
</dt> <dt>

[**Configurazione di flussi**](configuring-streams.md)
</dt> <dt>

[**Configurazione dei flussi video**](configuring-video-streams.md)
</dt> </dl>

 

 




