---
description: Configurazione della decodifica video
ms.assetid: 897b8e2d-9827-428d-91ae-632038c4c8c0
title: Configurazione della decodifica video (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7c49d42b47b4b6745731287e2b0bf0ee2d21c1eb503ed561274a5fb4cc8b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035339"
---
# <a name="configuring-video-decoding-microsoft-media-foundation"></a>Configurazione della decodifica video (Microsoft Media Foundation)

La decodifica è essenzialmente l'opposto della codifica in termini di configurazione. Il decodificatore supporta pochissime proprietà e nessuna di esse è necessaria. Impostare il tipo di input sul tipo usato per l'output del decodificatore (inclusi i dati privati del codec). Impostare quindi l'output sul formato non compresso desiderato, impostare la struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) in modo che rifletta le dimensioni dei fotogrammi appropriate e avviare l'elaborazione dei campioni.

È necessario fornire al decodificatore un tipo di supporto che includa i dati privati del codec posizionati immediatamente dopo la [**struttura VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) Il decodificatore non può decodificare il contenuto senza questi dati. La convalida del formato eseguita dal decodificatore non convalida i dati privati. Se i dati privati del codec sono mancanti o non corretti, il decodificatore risponde come se il flusso di bit fosse danneggiato. Per altre informazioni, vedere [Uso dei dati privati del codec video.](usingvideocodecprivatedata.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dei dati privati del codec video](usingvideocodecprivatedata.md)
</dt> <dt>

[Uso dei video](workingwithvideo.md)
</dt> </dl>

 

 
