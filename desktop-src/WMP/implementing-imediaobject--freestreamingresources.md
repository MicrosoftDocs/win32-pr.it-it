---
title: Implementazione di IMediaObject FreeStreamingResources
description: Implementazione di IMediaObject FreeStreamingResources
ms.assetid: 970dd10b-a7a0-4ba0-97e3-725d5c914500
keywords:
- Plug-in di Windows Media Player, risorse di streaming di esempio Echo
- plug-in, risorse di streaming di esempio Echo
- plug-in di elaborazione dei segnali digitali, risorse di streaming di esempio Echo
- Plug-in DSP, risorse di streaming di esempio Echo
- Esempio di plug-in Echo DSP, risorse di streaming
- Esempio di plug-in Echo DSP, rilascio della memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31a293cfc68caf43496d031426de2441c9c1d05
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855802"
---
# <a name="implementing-imediaobjectfreestreamingresources"></a>Implementazione di IMediaObject:: FreeStreamingResources

È importante che il codice rilasci qualsiasi memoria allocata prima che l'oggetto plug-in venga eliminato definitivamente. Windows Media Player chiama **FreeStreamingResources** per consentire di eseguire questa operazione. Per garantire la sicurezza, l'esempio creato dalla procedura guidata per il plug-in include una chiamata a **FreeStreamingResources** nel metodo **FinalRelease** per garantire che la memoria venga liberata. Per l'esempio Echo è necessario aggiungere il codice seguente a **FreeStreamingResources** :


```
// Test whether a buffer exists.
if (m_pbDelayBuffer)
{
    delete m_pbDelayBuffer;
    m_pbDelayBuffer = NULL;
    m_pbDelayPointer = NULL;
    m_cbDelayBuffer = 0;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso delle risorse di streaming**](working-with-streaming-resources.md)
</dt> </dl>

 

 




