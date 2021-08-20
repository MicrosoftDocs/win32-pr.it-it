---
title: Riproduzione a ciclo continuo (audio Waveform)
description: Riproduzione a ciclo continuo (audio Waveform)
ms.assetid: 8411290b-a3c5-4347-bee3-43c35188f736
keywords:
- audio waveform, audio a ciclo continuo
- interfaccia audio-forma d'onda, riproduzione di suoni a ciclo continuo
- audio waveform, riproduzione a ciclo continuo
- interfaccia audio waveform, riproduzione a ciclo continuo
- looping waveform-audio sounds
- riproduzione audio-forma d'onda a ciclo continuo
- Funzione waveOutWrite
- Funzione waveOutBreakLoop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d98732ccc0a1d75ad13a10dc881b66a3bb634beab03a95a86a9db5689890979
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139312"
---
# <a name="looping-playback"></a>Riproduzione a ciclo continuo

Il ciclo di un suono è controllato dai membri **dwLoops** e **dwFlags** nelle strutture [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) passate al dispositivo con la [**funzione waveOutWrite.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) Usare i **flag WHDR \_ BEGINLOOP** e **WHDR \_ ENDLOOP** nel membro **dwFlags** per specificare i blocchi di dati iniziale e finale per il ciclo.

Per eseguire il ciclo di un singolo blocco di dati, specificare entrambi i flag per lo stesso blocco. Per specificare il numero di cicli, usare il **membro dwLoops** nella struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) per il primo blocco del ciclo.

È possibile chiamare la [**funzione waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) per arrestare un suono a ciclo continuo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riproduzione Waveform-Audio file](playing-waveform-audio-files.md)
</dt> </dl>

 

 
