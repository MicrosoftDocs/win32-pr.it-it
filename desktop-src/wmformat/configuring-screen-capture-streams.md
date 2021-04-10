---
title: Configurazione di flussi di acquisizione schermo
description: Configurazione di flussi di acquisizione schermo
ms.assetid: 974e679f-0bf6-412b-9e80-43370de7605a
keywords:
- flussi, configurazione di flussi di acquisizione schermo
- codec, configurazione di flussi di acquisizione schermo
- flussi di acquisizione schermo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8200c4a6e733c2bb7f908b79cb73dbb2c3244dc4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956166"
---
# <a name="configuring-screen-capture-streams"></a>Configurazione di flussi di acquisizione schermo

I flussi che usano il codec Windows Media® video 9 screen sono configurati dalle applicazioni nello stesso modo dei normali flussi video. Tuttavia, se si imposta il livello di complessità video su 0, il writer ignorerà qualsiasi valore di qualità video impostato con [**IWMVideoMediaProps:: sequality**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setquality). Per altre informazioni, vedere [ottenere risultati soddisfacenti con il codec della schermata Windows Media video 9](getting-good-results-with-the-windows-media-video-9-screen-codec.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Configurazione di flussi**](configuring-streams.md)
</dt> <dt>

[**Configurazione comune a tutti i flussi**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurazione dei flussi video**](configuring-video-streams.md)
</dt> </dl>

 

 




