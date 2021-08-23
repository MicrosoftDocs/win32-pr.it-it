---
title: Riferimento onda audio
description: In questa sezione sono elencate le funzioni, le strutture e i messaggi associati all'audio waveform, documentati in Informazioni di riferimento multimediali. Questi elementi sono raggruppati come indicato di seguito.
ms.assetid: 723953f7-b38e-4f24-8d54-9849e013011d
keywords:
- Windows multimediale, informazioni di riferimento audio waveform
- informazioni di riferimento su audio multimediale e waveform
- audio multimediale, informazioni di riferimento sulla forma d'onda
- informazioni di riferimento su audio, forma d'onda
- Windows multimediale, audio waveform
- multimediali, audio waveform
- audio multimediale, forma d'onda
- audio, forma d'onda
- audio della forma d'onda, riferimento
- informazioni di riferimento sull'audio della forma d'onda, informazioni su
- informazioni di riferimento per l'audio wavefore, informazioni su
- informazioni di riferimento audio waveform, dispositivi ausiliari
- informazioni di riferimento per l'audio wavefore, i dispositivi ausiliari
- informazioni di riferimento per l'audio della forma d'onda, riproduzione
- informazioni di riferimento per l'audio wavefore, la riproduzione
- riferimento audio waveform,errori
- informazioni di riferimento per l'audio wavefore, errori
- informazioni di riferimento per l'audio della forma d'onda, apertura
- informazioni di riferimento per l'audio wavefore, apertura
- informazioni di riferimento audio sulla forma d'onda, chiusura
- informazioni di riferimento per l'audio wavefore, chiusura
- informazioni di riferimento per l'audio della forma d'onda, pitch
- informazioni di riferimento per l'audio wavefore, pitch
- riferimento audio forma d'onda,volume
- informazioni di riferimento per l'audio wavefore, volume
- informazioni di riferimento audio waveform, messaggi
- informazioni di riferimento per l'audio wavefore, messaggi
- riferimento audio forma d'onda,posizione corrente
- riferimento per l'audio wavefore, posizione corrente
- informazioni di riferimento per l'audio della forma d'onda, registrazione
- informazioni di riferimento per l'audio wavefore, registrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fd83f843de130d247749acfc87a67c60948871bb8cd878f9aa180fcd385fb13
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687421"
---
# <a name="waveform-audio-reference"></a>Riferimento onda audio

In questa sezione sono elencate le funzioni, le strutture e i messaggi associati all'audio waveform, documentati in [Riferimenti multimediali](multimedia-reference.md). Questi elementi sono raggruppati come indicato di seguito.

## <a name="auxiliary-devices"></a>Dispositivi ausiliari

-   [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)
-   [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)
-   [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)
-   [**auxGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume)
-   [**auxOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-auxoutmessage)
-   [**auxSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume)

## <a name="easy-playback"></a>Riproduzione semplice

-   [**Playsound**](/previous-versions//dd743680(v=vs.85))
-   [**sndPlaySound**](/previous-versions//dd798676(v=vs.85))

## <a name="errors"></a>Errors

-   [**waveInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)
-   [**waveOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext)

## <a name="opening-and-closing"></a>Apertura e chiusura

-   [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat)
-   [**CHIUSURA \_ DI MM WIM \_**](mm-wim-close.md)
-   [**MM \_ WIM \_ OPEN**](mm-wim-open.md)
-   [**CHIUSURA \_ DI MM WOM \_**](mm-wom-close.md)
-   [**MM \_ WOM \_ OPEN**](mm-wom-open.md)
-   [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat)
-   [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)
-   [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)
-   [**waveInProc**](/previous-versions//dd743849(v=vs.85))
-   [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen)
-   [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose)
-   [**waveOutProc**](/previous-versions//dd743869(v=vs.85))
-   [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)
-   [**WIM \_ CLOSE**](wim-close.md)
-   [**WIM \_ OPEN**](wim-open.md)
-   [**CHIUSURA \_ DI WOM**](wom-close.md)
-   [**WOM \_ OPEN**](wom-open.md)

## <a name="pitch"></a>Tonalità

-   [**waveOutGetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)
-   [**waveOutSetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)

## <a name="playback-rate"></a>Velocità di riproduzione

-   [**waveOutGetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate)
-   [**waveOutSetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate)

## <a name="playback-progress"></a>Stato di riproduzione

-   [**MM \_ WOM \_ DONE**](mm-wom-done.md)
-   [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop)
-   [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)
-   [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)
-   [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart)
-   [**WOM \_ DONE**](wom-done.md)

## <a name="playing"></a>Playing

-   [**MM \_ WOM \_ DONE**](mm-wom-done.md)
-   [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)
-   [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)
-   [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader)
-   [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite)
-   [**WOM \_ DONE**](wom-done.md)

## <a name="querying-a-device"></a>Esecuzione di query su un dispositivo

-   [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)
-   [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)
-   [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)
-   [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)
-   [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps)
-   [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs)

## <a name="recording"></a>Registrazione

-   [**DATI \_ DI MM WIM \_**](mm-wim-data.md)
-   [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer)
-   [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)
-   [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)
-   [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)
-   [**waveInStop**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)
-   [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)
-   [**DATI \_ WIM**](wim-data.md)

## <a name="retrieving-device-identifiers"></a>Recupero di identificatori di dispositivo

-   [**waveInGetID**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetid)
-   [**waveOutGetID**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetid)

## <a name="retrieving-the-current-position"></a>Recupero della posizione corrente

-   [**waveInGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetposition)
-   [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition)

## <a name="sending-custom-messages"></a>Invio di messaggi personalizzati

-   [**waveInMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveinmessage)
-   [**WaveOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)

## <a name="volume"></a>Volume

-   [**waveOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume)
-   [**waveOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Waveform Audio](waveform-audio.md)
</dt> </dl>

 

 