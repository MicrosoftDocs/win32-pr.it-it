---
description: Uso del sink di supporto EVR
ms.assetid: cd98266a-bc62-43da-b4d7-3561447d634f
title: Uso del sink di supporto EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84f8c666e88b495ad2d2e53fb1de10364f91636f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320798"
---
# <a name="using-the-evr-media-sink"></a>Uso del sink di supporto EVR

Il sink multimediale EVR (Enhanced video renderer) può essere usato come componente autonomo. Più spesso, tuttavia, un'applicazione creerà il sink del supporto EVR all'interno di una topologia e quindi utilizzerà la sessione multimediale per controllare la riproduzione.

Esistono due modi per creare il sink di supporto EVR:

-   La funzione [**MFCreateVideoRenderer**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) crea il sink multimediale.

-   La funzione [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) crea un oggetto Activation per il sink multimediale.

Il sink del supporto EVR inizialmente ha un sink di flusso, che corrisponde al flusso di riferimento. Per aggiungere nuovi sink di flusso, chiamare [**IMFMediaSink:: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Renderer video migliorato](enhanced-video-renderer.md)
</dt> <dt>

[Sink di supporti](media-sinks.md)
</dt> </dl>

 

 



