---
title: Informazioni sulla discontinuità
description: Informazioni sulla discontinuità
ms.assetid: 29210758-a1e6-47f2-9428-38f79623fbca
keywords:
- Windows Media Player plug-in audio, DSP audio
- plug-in, DSP audio
- plug-in di elaborazione del segnale digitale, discontinuità audio
- Plug-in DSP, discontinuità audio
- plug-in audio DSP, discontinuità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40de4c75c2d17699f0c72416873d64177e47d81761b27e5ffd465d89c9ecb9c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903571"
---
# <a name="about-discontinuity"></a>Informazioni sulla discontinuità

In qualsiasi momento, Windows Media Player segnalare un'interruzione nel flusso di input chiamando il metodo **IMediaObject::D iscontinuity.** Ciò si verifica regolarmente all'inizio e alla fine di un flusso e anche prima di ogni operazione di ricerca o quando il flusso di contenuto viene interrotto per qualsiasi motivo. Il plug-in DSP di esempio generato dalla procedura guidata Windows Media Player plug-in non deve gestire le discontinuità per i motivi seguenti:

-   Gli esempi PCM sono atomici, ovvero possono essere elaborati indipendentemente dagli altri campioni nel flusso. Alcuni formati video contengono dati che dipendono da fotogrammi chiave ed esempi compressi.
-   Il codice di esempio viene scritto per forzare sempre il client a elaborare tutto l'output prima che il plug-in accetti più input.

L'implementazione predefinita **di IMediaObject::D iscontinuity** restituisce semplicemente S \_ OK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di un plug-in DSP audio**](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




