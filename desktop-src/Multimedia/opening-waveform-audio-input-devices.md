---
title: Apertura Waveform-Audio di input
description: Apertura Waveform-Audio di input
ms.assetid: 46cdbce6-2433-433a-abd2-39e4146aa2e9
keywords:
- audio waveform, apertura di dispositivi di input
- interfaccia waveform-audio, apertura di dispositivi di input
- registrazione di audio waveform, apertura di dispositivi di input
- apertura di dispositivi di input audio waveform
- Funzione waveInOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e6391ca5bfe0690d2235504057865fb588f08d0359417ccbcc04b6a7e5eb082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802308"
---
# <a name="opening-waveform-audio-input-devices"></a>Apertura Waveform-Audio di input

Usare la [**funzione waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) per aprire un dispositivo di input audio waveform per la registrazione. Questa funzione apre il dispositivo associato all'identificatore di dispositivo specificato e restituisce un handle del dispositivo aperto scrivendo l'handle di un percorso di memoria specificato.

Alcuni computer multimediali hanno più dispositivi di input audio-waveform. A meno che non si sappia di voler aprire un dispositivo di input audio-forma d'onda specifico in un sistema, è consigliabile usare la costante WAVE MAPPER per l'identificatore di dispositivo quando si \_ apre un dispositivo. La [**funzione waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) sceglierà il dispositivo nel sistema più in grado di registrare nel formato dati specificato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione dell'audio Waveform](recording-waveform-audio.md)
</dt> </dl>

 

 