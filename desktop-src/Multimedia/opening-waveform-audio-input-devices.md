---
title: Apertura di dispositivi di input Waveform-Audio
description: Apertura di dispositivi di input Waveform-Audio
ms.assetid: 46cdbce6-2433-433a-abd2-39e4146aa2e9
keywords:
- audio Waveform, apertura di dispositivi di input
- waveform-interfaccia audio, apertura di dispositivi di input
- registrazione audio della forma d'onda, apertura di dispositivi di input
- apertura della forma d'onda-dispositivi di input audio
- waveInOpen (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92b7f49b9d170ceb8ebce287025ce0e0c1c5530
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299676"
---
# <a name="opening-waveform-audio-input-devices"></a>Apertura di dispositivi di input Waveform-Audio

Usare la funzione [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) per aprire un dispositivo di input della forma d'onda-audio per la registrazione. Questa funzione apre il dispositivo associato all'identificatore di dispositivo specificato e restituisce un handle del dispositivo aperto scrivendo l'handle di una posizione di memoria specificata.

Alcuni computer multimediali hanno più dispositivi di input audio e di forma d'onda. A meno che non si sia certi di voler aprire un dispositivo di input della forma d'onda specifico in un sistema, è necessario usare la \_ costante di mapper wave per l'identificatore del dispositivo quando si apre un dispositivo. La funzione [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) sceglierà il dispositivo nel sistema più idoneo per la registrazione nel formato dati specificato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione dell'audio della forma d'onda](recording-waveform-audio.md)
</dt> </dl>

 

 