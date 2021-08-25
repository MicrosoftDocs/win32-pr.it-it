---
description: Uso del sink multimediale EVR
ms.assetid: cd98266a-bc62-43da-b4d7-3561447d634f
title: Uso del sink multimediale EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ced80b4f9ee17093a00436a26f3f142281907597191791712fd6900520926ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826291"
---
# <a name="using-the-evr-media-sink"></a>Uso del sink multimediale EVR

Il sink multimediale EVR (Enhanced Video Renderer) può essere usato come componente autonomo. Più spesso, tuttavia, un'applicazione creerà il sink multimediale EVR all'interno di una topologia e quindi userà la sessione multimediale per controllare la riproduzione.

Esistono due modi per creare il sink multimediale EVR:

-   La [**funzione MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) crea il sink multimediale.

-   La [**funzione MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) crea un oggetto di attivazione per il sink multimediale.

Il sink multimediale EVR ha inizialmente un sink di flusso, che corrisponde al flusso di riferimento. Per aggiungere nuovi sink di flusso, chiamare [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Renderer video avanzato](enhanced-video-renderer.md)
</dt> <dt>

[Sink di supporti](media-sinks.md)
</dt> </dl>

 

 



