---
description: Configurazione della decodifica video
ms.assetid: 897b8e2d-9827-428d-91ae-632038c4c8c0
title: Configurazione della decodifica video (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f386e3dbb39d6296756f2fe8eec1b94c5533bff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305476"
---
# <a name="configuring-video-decoding-microsoft-media-foundation"></a>Configurazione della decodifica video (Microsoft Media Foundation)

La decodifica è essenzialmente l'opposto della codifica in termini di configurazione. Il decodificatore supporta pochissime proprietà e nessuno di essi è obbligatorio. Impostare il tipo di input sul tipo usato per l'output del decodificatore, inclusi i dati privati del codec. Impostare quindi l'output sul formato non compresso desiderato, impostare la struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) in modo che corrisponda alle dimensioni corrette del frame e avviare l'elaborazione degli esempi.

È necessario fornire al decodificatore un tipo di supporto che includa i dati privati del codec posizionati immediatamente dopo la struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) . Il decodificatore non è in grado di decodificare il contenuto senza questi dati. La convalida del formato eseguita dal decodificatore non convalida i dati privati. Se i dati privati del codec sono mancanti o errati, il decodificatore risponde come se il flusso di bit fosse danneggiato. Per altre informazioni, vedere [uso di dati privati di codec video](usingvideocodecprivatedata.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di dati privati del codec video](usingvideocodecprivatedata.md)
</dt> <dt>

[Uso dei video](workingwithvideo.md)
</dt> </dl>

 

 
