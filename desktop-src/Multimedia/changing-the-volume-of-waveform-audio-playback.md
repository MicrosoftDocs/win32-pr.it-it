---
title: Modifica del volume della Waveform-Audio riproduzione
description: Modifica del volume della Waveform-Audio riproduzione
ms.assetid: 814daa35-7905-47a2-ab08-29f20493af1e
keywords:
- audio waveform, modifica del volume di riproduzione
- interfaccia audio-forma d'onda, modifica del volume di riproduzione
- audio waveform, volume di riproduzione
- interfaccia audio-forma d'onda, volume di riproduzione
- modifica del volume di riproduzione audio-forma d'onda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e59bca6dbc168d2c327c46e4d934d4abb3afa73cc8ef2cae8b1a6c283bd92c81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807991"
---
# <a name="changing-the-volume-of-waveform-audio-playback"></a>Modifica del volume della Waveform-Audio riproduzione

Windows fornisce le funzioni seguenti per eseguire query e impostare il livello di volume dei dispositivi di output audio-forma d'onda.



| Funzione                                     | Descrizione                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**waveOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume) | Recupera il livello di volume corrente del dispositivo di output audio-forma d'onda specificato. |
| [**waveOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume) | Imposta il livello di volume del dispositivo di output audio-forma d'onda specificato.              |



 

Non tutti i dispositivi audio waveform supportano le modifiche del volume. Alcuni dispositivi supportano il controllo dei singoli volumi nei canali sinistro e destro. Per informazioni su come determinare le funzionalità di controllo del volume dei dispositivi audio waveform, vedere [Dispositivi e tipi di dati.](devices-and-data-types.md)

Alcune applicazioni consentono all'utente di controllare il volume per tutti i dispositivi audio in un sistema. Molte applicazioni di questo tipo usano i servizi mixer audio. Per altre informazioni, vedere [Mixer audio.](audio-mixers.md) A meno che l'applicazione non sia in grado di controllare questo tipo di volume master, è necessario aprire un dispositivo audio prima di modificarne il volume. È anche necessario eseguire una query sul livello del volume prima di modificarlo e ripristinare il livello del volume al livello precedente appena possibile.

Il volume viene specificato in un valore doubleword. Quando il formato audio è stereo, i 16 bit superiori specificano il volume relativo del canale destro e i 16 bit inferiori specificano il volume relativo del canale sinistro. Per i dispositivi che non supportano il controllo del volume del canale sinistro e destro, i 16 bit inferiori specificano il livello del volume e i 16 bit superiori vengono ignorati.

I valori a livello di volume 0x0 (silenzio) a 0xFFFF (volume massimo) e vengono interpretati in modo logaritmico. L'aumento del volume percepito è lo stesso quando si aumenta il livello di volume da 0x5000 a 0x6000 mentre è da 0x4000 a 0x5000.

 

 