---
title: Uso delle risorse di streaming
description: Uso delle risorse di streaming
ms.assetid: 0258ad24-f1b9-4cb3-921c-068072fd2dbb
keywords:
- Plug-in di Windows Media Player, risorse di streaming di esempio Echo
- plug-in, risorse di streaming di esempio Echo
- plug-in di elaborazione dei segnali digitali, risorse di streaming di esempio Echo
- Plug-in DSP, risorse di streaming di esempio Echo
- Esempio di plug-in Echo DSP, risorse di streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a1df8cc221f3d75c8333b3ffd41a144d28bed7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298909"
---
# <a name="working-with-streaming-resources"></a>Uso delle risorse di streaming

Il progetto di plug-in audio DSP di esempio generato dalla procedura guidata per il plug-in di Windows Media Player non richiede l'allocazione di risorse di flusso da parte del plug-in. L'esempio Echo, tuttavia, richiede un buffer separato per conservare i dati audio per un determinato periodo di tempo per creare l'effetto ritardo. Il buffer è gestito da due metodi: **IMediaObject:: AllocateStreamingResources**, che crea il buffer e **IMediaObject:: FreeStreamingResources**, che rilascia il buffer. I metodi **IMediaObject** vengono implementati in Echo. cpp.

Nelle sezioni seguenti vengono fornite ulteriori informazioni sulla gestione dei buffer:

-   [Variabili per gestire il buffer di ritardo](variables-to-manage-the-delay-buffer.md)
-   [Implementazione di IMediaObject:: AllocateStreamingResources](implementing-imediaobject--allocatestreamingresources.md)
-   [Implementazione di IMediaObject:: FreeStreamingResources](implementing-imediaobject--freestreamingresources.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempio Echo**](the-echo-sample.md)
</dt> </dl>

 

 




