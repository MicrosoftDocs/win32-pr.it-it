---
title: Informazioni sull'allocazione delle risorse di streaming
description: Informazioni sull'allocazione delle risorse di streaming
ms.assetid: b09633c4-58f7-4e3e-bb4d-007845baaccf
keywords:
- Plug-in di Windows Media Player, DSP audio
- plug-in, audio DSP
- plug-in di elaborazione dei segnali digitali, risorse di streaming audio
- Plug-in DSP, risorse di streaming audio
- plug-in audio DSP, risorse di streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba82f150908e7b96f4e6e56c2161e1b2fdfe145
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116877"
---
# <a name="about-allocating-streaming-resources"></a>Informazioni sull'allocazione delle risorse di streaming

Il plug-in DSP di esempio generato dalla procedura guidata per il plug-in di Windows Media Player non richiede alcun buffer di flusso aggiuntivo. Tuttavia, potrebbe essere necessario allocare risorse di memoria per il plug-in DSP. Ad esempio, un plug-in che produce un effetto Echo richiederebbe un buffer secondario per creare il ritardo di tempo necessario.

L'interfaccia **IMediaObject** contiene due metodi per gestire questa situazione. Windows Media Player chiama **IMediaObject:: AllocateStreamingResources** per offrire la possibilità di creare buffer necessari. Windows Media Player in seguito chiama **IMediaObject:: FreeStreamingResources** per consentire di liberare la memoria allocata in precedenza. L'implementazione del plug-in DSP di esempio chiama anche **FreeStreamingResources** da *CProjectName*::**FinalRelease** per garantire che tutte le risorse vengano liberate prima che l'oggetto plug-in venga eliminato definitivamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di un plug-in DSP audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




