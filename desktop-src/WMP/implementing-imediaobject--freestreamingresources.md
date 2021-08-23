---
title: Implementazione di IMediaObject FreeStreamingResources
description: Implementazione di IMediaObject FreeStreamingResources
ms.assetid: 970dd10b-a7a0-4ba0-97e3-725d5c914500
keywords:
- Windows Media Player plug-in, risorse di streaming di esempio Echo
- plug-in, risorse di streaming di esempio Echo
- plug-in di elaborazione del segnale digitale, risorse di streaming di esempio Echo
- Plug-in DSP, risorse di streaming di esempio Echo
- Esempio di plug-in Echo DSP, risorse di streaming
- Esempio di plug-in Echo DSP, rilascio della memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30da5f92ec8420ccc90f74256003aae02664a57a8ffad3470901f672cf37aa73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119617321"
---
# <a name="implementing-imediaobjectfreestreamingresources"></a>Implementazione di IMediaObject::FreeStreamingResources

È importante che il codice rilasci qualsiasi memoria allocata prima che l'oggetto plug-in venga eliminato. Windows Media Player chiama **FreeStreamingResources** per consentire questa operazione. Per motivi di sicurezza, l'esempio creato dalla procedura guidata del plug-in include una chiamata a **FreeStreamingResources** nel **metodo FinalRelease** per assicurarsi che la memoria sia liberata. È necessario aggiungere il codice seguente a **FreeStreamingResources per** l'esempio Echo:


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

 

 




