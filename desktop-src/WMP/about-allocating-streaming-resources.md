---
title: Informazioni sull'allocazione di risorse di streaming
description: Informazioni sull'allocazione di risorse di streaming
ms.assetid: b09633c4-58f7-4e3e-bb4d-007845baaccf
keywords:
- Windows Media Player plug-in audio, DSP audio
- plug-in, DSP audio
- plug-in di elaborazione dei segnali digitali, risorse di streaming audio
- plug-in DSP, risorse di streaming audio
- plug-in DSP audio, risorse di streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f815fe9875f2e93e140b577da6e00dd7c684c1fedbad13234ecfbf87ca84ddb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903731"
---
# <a name="about-allocating-streaming-resources"></a>Informazioni sull'allocazione di risorse di streaming

Il plug-in DSP di esempio generato dalla Windows Media Player guidata plug-in non richiede buffer di streaming aggiuntivi. Tuttavia, potrebbe essere necessario allocare risorse di memoria per il plug-in DSP. Ad esempio, un plug-in che produce un effetto echo richiederebbe un buffer secondario per creare il ritardo di tempo necessario.

**L'interfaccia IMediaObject** contiene due metodi per gestire questa situazione. Windows Media Player chiama **IMediaObject::AllocateStreamingResources** per offrire la possibilità di creare i buffer necessari. Windows Media Player successivamente chiama **IMediaObject::FreeStreamingResources** per consentire di liberare la memoria allocata in precedenza. L'implementazione del plug-in DSP di esempio chiama anche **FreeStreamingResources** da *CProjectName*::**FinalRelease** per garantire che tutte le risorse siano liberate prima che l'oggetto plug-in venga eliminato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di un plug-in DSP audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




