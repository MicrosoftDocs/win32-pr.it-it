---
title: Modifica del passo e della velocità di riproduzione
description: Modifica del passo e della velocità di riproduzione
ms.assetid: f0f5249b-ae2a-4f17-80ee-575f9f7963a7
keywords:
- audio waveform, pitch
- interfaccia waveform-audio, pitch
- audio waveform, velocità di riproduzione
- interfaccia waveform-audio, velocità di riproduzione
- audio della forma d'onda, modifica del passo
- interfaccia waveform-audio, modifica del passo
- audio waveform, modifica della velocità di riproduzione
- interfaccia waveform-audio, modifica della velocità di riproduzione
- modifica della frequenza di riproduzione waveform-audio
- modifica del passo waveform-audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 006788c286476434a7ca2a3d5b79dbd6c4d8af431d74ffb4a00e03a7357777f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941279"
---
# <a name="changing-pitch-and-playback-rate"></a>Modifica del passo e della velocità di riproduzione

Alcuni dispositivi di output waveform-audio possono variare il passo e la velocità di riproduzione dei dati waveform-audio. Non tutti i dispositivi waveform-audio supportano le modifiche di frequenza di riproduzione e passo. Per informazioni su come determinare se un particolare dispositivo audio-forma d'onda supporta le modifiche della velocità di riproduzione e di presentazione, vedere [Dispositivi e tipi di dati](devices-and-data-types.md).

Le differenze tra la modifica del passo e la velocità di riproduzione sono le seguenti:

-   La modifica della velocità di riproduzione viene eseguita dal driver di dispositivo e non richiede hardware specializzato. La frequenza di campionamento non viene modificata, ma il driver interpola ignorando o sintetizzando i campioni. Ad esempio, se la velocità di riproduzione viene modificata di un fattore di due, il driver ignora ogni altro campione.
-   La modifica del passo richiede hardware specializzato. La velocità di riproduzione e la frequenza di campionamento non vengono modificate.

Windows fornisce le funzioni seguenti per eseguire query e impostare le frequenze di riproduzione e del passo audio della forma d'onda.



| Funzione                                                 | Descrizione                                                                 |
|----------------------------------------------------------|-----------------------------------------------------------------------------|
| [**waveOutGetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)               | Recupera l'altezza per il dispositivo di output waveform-audio specificato.         |
| [**waveOutGetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate) | Recupera la velocità di riproduzione per il dispositivo di output waveform-audio specificato. |
| [**waveOutSetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)               | Imposta il passo per il dispositivo di output waveform-audio specificato.              |
| [**waveOutSetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate) | Imposta la velocità di riproduzione per il dispositivo di output waveform-audio specificato.      |



 

Le frequenze di intonazione e riproduzione vengono modificate da un fattore specificato con un numero a virgola fissa imballato in un valore doubleword. I 16 bit superiori specificano la parte intera del numero. i 16 bit inferiori specificano la parte frazionaria. Ad esempio, il valore 1,5 è rappresentato come 0x00018000L. Il valore 0,75 è rappresentato come 0x0000C000L. Un valore pari a 1,0 (0x00010000) indica che il passo o la velocità di riproduzione rimane invariata.

 

 