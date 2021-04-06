---
title: Riferimento onda audio
description: Questa sezione elenca le funzioni, le strutture e i messaggi associati all'audio della forma d'onda, documentati in riferimenti multimediali. Questi elementi vengono raggruppati come indicato di seguito.
ms.assetid: 723953f7-b38e-4f24-8d54-9849e013011d
keywords:
- Multimedia di Windows, informazioni di riferimento su audio Waveform
- informazioni di riferimento su Multimedia, onda audio
- audio multimediale, riferimento alla forma d'onda
- audio, riferimento alla forma d'onda
- Multimedia di Windows, audio Waveform
- Multimedia, audio Waveform
- audio multimediale, forma d'onda
- audio, forma d'onda
- audio Waveform, riferimento
- Guida di riferimento all'audio della forma d'onda, informazioni
- informazioni di riferimento su wavefore audio, about
- riferimento audio per la forma d'onda, dispositivi ausiliari
- informazioni di riferimento per audio wavefore, dispositivi ausiliari
- riferimento audio Waveform, riproduzione
- informazioni di riferimento sull'audio wavefore, riproduzione
- riferimento audio per la forma d'onda, errori
- informazioni di riferimento sull'audio wavefore, errori
- riferimento audio per la forma d'onda, apertura
- informazioni di riferimento sull'audio wavefore, apertura
- riferimento audio per la forma d'onda, chiusura
- informazioni di riferimento per wavefore audio, chiusura
- riferimento audio Waveform, pitch
- informazioni di riferimento su wavefore audio, pitch
- riferimento audio Waveform, volume
- informazioni di riferimento sull'audio wavefore, volume
- riferimento audio Waveform, messaggi
- informazioni di riferimento sull'audio wavefore, messaggi
- riferimento audio Waveform, posizione corrente
- informazioni di riferimento sull'audio wavefore, posizione corrente
- riferimento audio per la forma d'onda, registrazione
- informazioni di riferimento sull'audio di wavefore, registrazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74b37984b2d3fab5dad1ea0df4f1f62dfa1855e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046654"
---
# <a name="waveform-audio-reference"></a>Riferimento onda audio

Questa sezione elenca le funzioni, le strutture e i messaggi associati all'audio della forma d'onda, documentati in [riferimenti multimediali](multimedia-reference.md). Questi elementi vengono raggruppati come indicato di seguito.

## <a name="auxiliary-devices"></a>Dispositivi ausiliari

-   [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)
-   [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)
-   [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)
-   [**auxGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume)
-   [**auxOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-auxoutmessage)
-   [**auxSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume)

## <a name="easy-playback"></a>Facile riproduzione

-   [**PlaySound**](/previous-versions//dd743680(v=vs.85))
-   [**sndPlaySound**](/previous-versions//dd798676(v=vs.85))

## <a name="errors"></a>Errors

-   [**waveInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)
-   [**waveOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext)

## <a name="opening-and-closing"></a>Apertura e chiusura

-   [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat)
-   [**\_Wim \_ chiusura di mm**](mm-wim-close.md)
-   [**\_Wim \_ aperto mm**](mm-wim-open.md)
-   [**MM \_ WOM \_ Close**](mm-wom-close.md)
-   [**MM \_ WOM \_ aperto**](mm-wom-open.md)
-   [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat)
-   [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)
-   [**waveInClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)
-   [**waveInProc**](/previous-versions//dd743849(v=vs.85))
-   [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen)
-   [**waveOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose)
-   [**waveOutProc**](/previous-versions//dd743869(v=vs.85))
-   [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)
-   [**chiusura di WIM \_**](wim-close.md)
-   [**WIM \_ aperto**](wim-open.md)
-   [**chiusura di WOM \_**](wom-close.md)
-   [**WOM \_ aperto**](wom-open.md)

## <a name="pitch"></a>Tonalità

-   [**waveOutGetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)
-   [**waveOutSetPitch**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)

## <a name="playback-rate"></a>Velocità di riproduzione

-   [**waveOutGetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate)
-   [**waveOutSetPlaybackRate**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate)

## <a name="playback-progress"></a>Stato riproduzione

-   [**MM \_ WOM \_ completato**](mm-wom-done.md)
-   [**waveOutBreakLoop**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop)
-   [**waveOutPause**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)
-   [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)
-   [**waveOutRestart**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart)
-   [**WOM \_ completato**](wom-done.md)

## <a name="playing"></a>Playing

-   [**MM \_ WOM \_ completato**](mm-wom-done.md)
-   [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)
-   [**waveOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)
-   [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader)
-   [**waveOutWrite**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite)
-   [**WOM \_ completato**](wom-done.md)

## <a name="querying-a-device"></a>Esecuzione di query su un dispositivo

-   [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)
-   [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)
-   [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)
-   [**WAVEOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)
-   [**waveOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps)
-   [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs)

## <a name="recording"></a>Registrazione

-   [**\_dati WIM \_ mm**](mm-wim-data.md)
-   [**waveInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer)
-   [**waveInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)
-   [**waveInReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)
-   [**waveInStart**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)
-   [**waveInStop**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)
-   [**waveInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)
-   [**\_dati WIM**](wim-data.md)

## <a name="retrieving-device-identifiers"></a>Recupero degli identificatori del dispositivo

-   [**waveInGetID**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetid)
-   [**waveOutGetID**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetid)

## <a name="retrieving-the-current-position"></a>Recupero della posizione corrente

-   [**waveInGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetposition)
-   [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition)

## <a name="sending-custom-messages"></a>Invio di messaggi personalizzati

-   [**waveInMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveinmessage)
-   [**waveOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)

## <a name="volume"></a>Volume

-   [**waveOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume)
-   [**waveOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Audio Waveform](waveform-audio.md)
</dt> </dl>

 

 