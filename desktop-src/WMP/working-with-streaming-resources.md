---
title: Uso delle risorse di streaming
description: Uso delle risorse di streaming
ms.assetid: 0258ad24-f1b9-4cb3-921c-068072fd2dbb
keywords:
- Windows Media Player plug-in, Echo sample streaming resources (Risorse di streaming di esempio Echo)
- plug-in, risorse di streaming di esempio Echo
- plug-in di elaborazione dei segnali digitali, risorse di streaming di esempio Echo
- Plug-in DSP, risorse di streaming di esempio Echo
- Esempio di plug-in Echo DSP, risorse di streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 268dc57bfad71f8ee46a3b934e671e478ca6a78a6b05fc30b7123e7b3f7f6ba0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118567170"
---
# <a name="working-with-streaming-resources"></a>Uso delle risorse di streaming

Il progetto di plug-in DSP audio di esempio generato dalla creazione guidata plug-in Windows Media Player non richiede l'allocazione di risorse di streaming da parte del plug-in. L'esempio Echo, tuttavia, richiede un buffer separato per contenere i dati audio per un periodo di tempo per creare l'effetto di ritardo. Il buffer è gestito da due metodi: **IMediaObject::AllocateStreamingResources**, che crea il buffer, e **IMediaObject::FreeStreamingResources**, che rilascia il buffer. I **metodi IMediaObject** vengono implementati in Echo.cpp.

Le sezioni seguenti forniscono altre informazioni sulla gestione dei buffer:

-   [Variabili per gestire il buffer di ritardo](variables-to-manage-the-delay-buffer.md)
-   [Implementazione di IMediaObject::AllocateStreamingResources](implementing-imediaobject--allocatestreamingresources.md)
-   [Implementazione di IMediaObject::FreeStreamingResources](implementing-imediaobject--freestreamingresources.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempio echo**](the-echo-sample.md)
</dt> </dl>

 

 




