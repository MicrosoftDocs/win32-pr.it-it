---
title: Modifica della frequenza di pitch e playback
description: Modifica della frequenza di pitch e playback
ms.assetid: f0f5249b-ae2a-4f17-80ee-575f9f7963a7
keywords:
- audio Waveform, pitch
- waveform-interfaccia audio, pitch
- audio Waveform, velocità di riproduzione
- waveform-interfaccia audio, velocità di riproduzione
- audio Waveform, modifica del pitch
- waveform-interfaccia audio, modifica del passo
- audio Waveform, modifica della velocità di riproduzione
- waveform-interfaccia audio, modifica della velocità di riproduzione
- modifica della frequenza di riproduzione audio
- modifica della forma d'onda-audio pitch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99eec4e29ec1c38cddb5a5f92f27643e2c9c3e6c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473123"
---
# <a name="changing-pitch-and-playback-rate"></a>Modifica della frequenza di pitch e playback

Alcuni dispositivi di output audio e della forma d'onda possono variare il pitch e la velocità di riproduzione dei dati audio della forma d'onda. Non tutti i dispositivi Waveform-Audio supportano le variazioni della velocità di riproduzione e del pitch. Per informazioni su come determinare se una particolare periferica waveform-audio supporta le modifiche alla frequenza di Pitch and playback, vedere [dispositivi e tipi di dati](devices-and-data-types.md).

Di seguito sono riportate le differenze tra la variazione del pitch e della frequenza di riproduzione:

-   La modifica della velocità di riproduzione viene eseguita dal driver di dispositivo e non richiede hardware specializzato. La frequenza di campionamento non viene modificata, ma il driver esegue l'interpolazione ignorando o sintetizzando gli esempi. Se, ad esempio, la velocità di riproduzione viene modificata in base a un fattore di due, il driver ignora tutti gli altri esempi.
-   Per modificare il pitch è necessario hardware specializzato. La frequenza di riproduzione e la frequenza di campionamento non vengono modificate.

Windows fornisce le funzioni seguenti per eseguire query e impostare frequenze di velocità di riproduzione e pitch di forma d'onda audio.



| Funzione                                                 | Descrizione                                                                 |
|----------------------------------------------------------|-----------------------------------------------------------------------------|
| [**waveOutGetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)               | Recupera il pitch per il dispositivo di output dell'audio e della forma d'onda specificato.         |
| [**waveOutGetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate) | Recupera la velocità di riproduzione per il dispositivo di output dell'audio e della forma d'onda specificato. |
| [**waveOutSetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)               | Imposta il pitch per il dispositivo di output dell'audio e della forma d'onda specificato.              |
| [**waveOutSetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate) | Imposta la velocità di riproduzione per il dispositivo di output dell'audio e della forma d'onda specificato.      |



 

Le frequenze di pitch e playback vengono modificate da un fattore specificato con un numero a virgola fissa compresso in un valore parola doppia. I 16 bit superiori specificano la parte intera del numero; i 16 bit inferiori specificano la parte frazionaria. Ad esempio, il valore 1,5 viene rappresentato come 0x00018000L. Il valore 0,75 è rappresentato come 0x0000C000L. Il valore 1,0 (0x00010000) indica che il pitch o la velocità di riproduzione è invariata.

 

 