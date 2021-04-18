---
title: Formati di input video
description: Formati di input video
ms.assetid: 0f1ec15d-328e-4c07-bf58-fd4ecb483549
keywords:
- Windows Media Format SDK, formati di input video
- ASF (Advanced Systems Format), formati di input video
- ASF (Advanced Systems Format), formati di input video
- formati di input video
- Windows Media Format SDK, formati video
- ASF (Advanced Systems Format), formati video
- ASF (Advanced Systems Format), formati video
- formati video
- Windows Media Video 9 codec, formati di input video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5113ee3cbd9c9235104f858968db20ebc29e3a
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "106299525"
---
# <a name="video-input-formats"></a>Formati di input video

Il writer accetta i formati video seguenti come input da comprimere usando il codec Windows Media Video 9:

-   \_IYUV WMMEDIASUBTYPE
-   \_I420 WMMEDIASUBTYPE
-   \_YV12 WMMEDIASUBTYPE
-   \_YUY2 WMMEDIASUBTYPE
-   \_UYVY WMMEDIASUBTYPE
-   \_YVYU WMMEDIASUBTYPE
-   \_YVU9 WMMEDIASUBTYPE
-   \_Rgb32 WMMEDIASUBTYPE
-   \_RGB24 WMMEDIASUBTYPE
-   \_RGB565 WMMEDIASUBTYPE
-   \_RGB555 WMMEDIASUBTYPE
-   \_RGB8 WMMEDIASUBTYPE

Usare sempre [**IWMWriter:: GetInputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformatcount) e [**IWMWriter:: GetInputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputformat) per enumerare i formati di input disponibili e ottenere l'oggetto proprietà supporto di input per il formato desiderato. È necessario modificare gli oggetti proprietà del supporto di input video per riflettere le dimensioni del frame e la frequenza dei fotogrammi del supporto di input.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Identificatori del tipo di supporto**](media-type-identifiers.md)
</dt> <dt>

[**Tipi di supporto**](media-types.md)
</dt> </dl>

 

 




