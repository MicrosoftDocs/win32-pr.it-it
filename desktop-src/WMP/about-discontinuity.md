---
title: Informazioni sulla discontinuità
description: Informazioni sulla discontinuità
ms.assetid: 29210758-a1e6-47f2-9428-38f79623fbca
keywords:
- Plug-in di Windows Media Player, DSP audio
- plug-in, audio DSP
- plug-in di elaborazione dei segnali digitali, discontinuità audio
- Plug-in DSP, discontinuità audio
- plug-in DSP audio, discontinuità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0448220d4616122b3c99670357bbbd78de11c392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395415"
---
# <a name="about-discontinuity"></a>Informazioni sulla discontinuità

In qualsiasi momento, Windows Media Player può segnalare un'interruzione nel flusso di input chiamando il metodo **IMediaObject::D di continuità** . Questo problema si verifica regolarmente all'inizio e alla fine di un flusso e anche prima di ogni operazione di ricerca o quando il contenuto del flusso viene interrotto per qualsiasi motivo. Il plug-in DSP di esempio generato dalla procedura guidata plug-in di Windows Media Player non deve gestire le discontinuità per i motivi seguenti:

-   Gli esempi di PCM sono atomici, ovvero possono essere elaborati indipendentemente dagli altri esempi nel flusso. Alcuni formati video contengono dati che dipendono da fotogrammi chiave ed esempi compressi.
-   Il codice di esempio viene scritto per forzare sempre il client a elaborare tutti gli output prima che il plug-in accetti un maggior numero di input.

L'implementazione predefinita di **IMediaObject::D la continuità** restituisce semplicemente S \_ OK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di un plug-in DSP audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




