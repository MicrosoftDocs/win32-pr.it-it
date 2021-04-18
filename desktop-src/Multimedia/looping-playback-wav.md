---
title: Riproduzione di cicli (audio Waveform)
description: Riproduzione di cicli (audio Waveform)
ms.assetid: 8411290b-a3c5-4347-bee3-43c35188f736
keywords:
- audio della forma d'onda, suoni di loop
- waveform-interfaccia audio, loop suoni
- audio della forma d'onda, riproduzione a cicli
- waveform-interfaccia audio, riproduzione a ciclo
- loop della forma d'onda-suoni audio
- esecuzione del loop della forma d'onda-riproduzione audio
- waveOutWrite (funzione)
- waveOutBreakLoop (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c233799e2d4faf8107b4a2a68a261b544ec1274
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2021
ms.locfileid: "106334032"
---
# <a name="looping-playback"></a>Riproduzione di cicli

Il ciclo di un suono è controllato dai membri **dwLoops** e **DwFlags** nelle strutture [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) passate al dispositivo con la funzione [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite) . Usare i flag **WHDR \_ BEGINLOOP** e **WHDR \_ EndLoop** nel membro **dwFlags** per specificare i blocchi di dati iniziali e finali per il ciclo.

Per eseguire il ciclo di un singolo blocco di dati, specificare entrambi i flag per lo stesso blocco. Per specificare il numero di cicli, usare il membro **dwLoops** nella struttura [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) per il primo blocco del ciclo.

È possibile chiamare la funzione [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop) per arrestare un suono di ciclo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riproduzione di file di Waveform-Audio](playing-waveform-audio-files.md)
</dt> </dl>

 

 
