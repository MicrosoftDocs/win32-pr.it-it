---
title: Configurazione dell'acquisizione schermo Flussi
description: Configurazione dell'acquisizione schermo Flussi
ms.assetid: 974e679f-0bf6-412b-9e80-43370de7605a
keywords:
- flussi, configurazione di flussi di acquisizione schermo
- codec, configurazione di flussi di acquisizione schermo
- flussi di acquisizione dello schermo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0814525f57a540fe491bb1dd5425e4a0ecf4dc024a31ab0d2f468c3856921a8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119591801"
---
# <a name="configuring-screen-capture-streams"></a>Configurazione dell'acquisizione schermo Flussi

Flussi che usano il codec Windows Media® Video 9 Screen vengono configurati dalle applicazioni allo stesso modo dei normali flussi video. Tuttavia, se si imposta il livello di complessità video su 0, lo scrittore ignorerà qualsiasi valore di qualità video impostato con [**IWMVideoMediaProps::SetQuality**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setquality). Per altre informazioni, vedere [Getting Good Results with the Windows Media Video 9 Screen Codec](getting-good-results-with-the-windows-media-video-9-screen-codec.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione di Flussi**](configuring-streams.md)
</dt> <dt>

[**Configurazione comune a tutti Flussi**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurazione di video Flussi**](configuring-video-streams.md)
</dt> </dl>

 

 




