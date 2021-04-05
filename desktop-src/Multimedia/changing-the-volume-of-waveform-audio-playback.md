---
title: Modifica del volume della riproduzione Waveform-Audio
description: Modifica del volume della riproduzione Waveform-Audio
ms.assetid: 814daa35-7905-47a2-ab08-29f20493af1e
keywords:
- audio della forma d'onda, modifica del volume di riproduzione
- waveform-interfaccia audio, modifica del volume di riproduzione
- audio Waveform, volume di riproduzione
- waveform-interfaccia audio, volume di riproduzione
- modifica del volume della riproduzione audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89f972b5bd8e6f0d4a0d7d5964f164429c5632b0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727314"
---
# <a name="changing-the-volume-of-waveform-audio-playback"></a>Modifica del volume della riproduzione Waveform-Audio

Windows fornisce le funzioni seguenti per eseguire query e impostare il livello di volume dei dispositivi di output dell'audio e della forma d'onda.



| Funzione                                     | Descrizione                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**waveOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume) | Recupera il livello del volume corrente del dispositivo di output dell'audio e della forma d'onda specificato. |
| [**waveOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume) | Imposta il livello del volume del dispositivo di output dell'audio e della forma d'onda specificato.              |



 

Non tutti i dispositivi Waveform-Audio supportano le modifiche del volume. Alcuni dispositivi supportano il controllo del volume singolo sui canali sinistro e destro. Per informazioni su come determinare le funzionalità di controllo del volume dei dispositivi audio e della forma d'onda, vedere [dispositivi e tipi di dati](devices-and-data-types.md).

Alcune applicazioni consentono all'utente di controllare il volume per tutti i dispositivi audio in un sistema. In molte applicazioni di questo tipo vengono utilizzati i servizi mixer audio. per ulteriori informazioni, vedere [mixer audio](audio-mixers.md). A meno che l'applicazione non sia in grado di eseguire questo tipo di controllo del volume principale, è necessario aprire un dispositivo audio prima di modificarne il volume. È anche necessario eseguire una query sul livello del volume prima di modificarlo e ripristinare il livello del volume precedente il prima possibile.

Il volume è specificato in un valore parola doppia. Quando il formato audio è stereo, i 16 bit superiori specificano il volume relativo del canale destro e i 16 bit inferiori specificano il volume relativo del canale sinistro. Per i dispositivi che non supportano il controllo del volume del canale sinistro e destro, i 16 bit inferiori specificano il livello del volume e i 16 bit superiori vengono ignorati.

I valori a livello di volume variano da 0x0 (silenzioso) a 0xFFFF (volume massimo) e vengono interpretati come logaritmicamente. L'aumento del volume percepito è lo stesso quando si aumenta il livello di volume da 0x5000 a 0x6000, come da 0x4000 a 0x5000.

 

 