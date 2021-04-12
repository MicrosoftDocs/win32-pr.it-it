---
title: Riferimento MIDI
description: Riferimento MIDI
ms.assetid: 6229a4a7-be42-4e2a-af9d-695c4759a4ef
keywords:
- Multimedia di Windows, Musical Instrument Digital Interface (MIDI)
- Multimedia, Musical Instrument Digital Interface (MIDI)
- audio multimediale, MIDI (Musical Instrument Digital Interface)
- audio, Musical Instrument Digital Interface (MIDI)
- Windows Multimedia, riferimento MIDI
- Multimedia, riferimento MIDI
- audio multimediale, riferimento MIDI
- audio, riferimento MIDI
- MIDI (Musical Instrument Digital Interface), riferimento
- MIDI (Musical Instrument Digital Interface), riferimento
- informazioni di riferimento su MIDI, informazioni
- Riferimento MIDI, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c21542867faf1e09d68dc4fc81a50d25f56b5c5e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398971"
---
# <a name="midi-reference"></a>Riferimento MIDI

Questa sezione descrive le funzioni, le macro, i messaggi e le strutture associati al MIDI (Musical Instrument Digital Interface). Questi elementi vengono raggruppati come indicato di seguito.

## <a name="allocating-and-managing-buffers"></a>Allocazione e gestione dei buffer

-   [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)
-   [**midiInAddBuffer**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)
-   [**midiInPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)
-   [**midiInUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)
-   [**midiOutPrepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)
-   [**midiOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader)

## <a name="callback-functions"></a>Funzioni di callback

-   [**MidiInProc**](/previous-versions//dd798460(v=vs.85))
-   [**MidiOutProc**](/previous-versions//dd798478(v=vs.85))

## <a name="device-capabilities"></a>Funzionalità del dispositivo

-   [**MIDIINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps)
-   [**midiInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)
-   [**midiInGetID**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetid)
-   [**midiInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)
-   [**MIDIOUTCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps)
-   [**midiOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps)
-   [**midiOutGetID**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetid)
-   [**midiOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs)
-   [**MIDISTRMBUFFVER**](/windows/win32/api/mmeapi/ns-mmeapi-midistrmbuffver)

## <a name="error-processing"></a>Errore di elaborazione

-   [**midiInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext)
-   [**midiOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext)
-   [**\_errore MIM**](mim-error.md)
-   [**\_LONGERROR MIM**](mim-longerror.md)
-   [**\_errore MIM \_ mm**](mm-mim-error.md)
-   [**\_LONGERROR MIM \_ mm**](mm-mim-longerror.md)

## <a name="managing-midi-streams"></a>Gestione dei flussi MIDI

-   [**midiStreamClose**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)
-   [**midiStreamOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)
-   [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [**midiStreamPause**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition)
-   [**midiStreamProperty**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty)
-   [**midiStreamRestart**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [**midiStreamStop**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)

## <a name="opening-and-closing-devices"></a>Apertura e chiusura di dispositivi

-   [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)
-   [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)
-   [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose)
-   [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)
-   [**\_chiusura MIM**](mim-close.md)
-   [**MIM \_ aperto**](mim-open.md)
-   [**MM \_ di \_ chiusura MIM**](mm-mim-close.md)
-   [**\_apertura MIM \_ mm**](mm-mim-open.md)
-   [**MM \_ \_ chiusura MOM**](mm-mom-close.md)
-   [**MM- \_ MOM \_ aperto**](mm-mom-open.md)
-   [**\_chiusura MOM**](mom-close.md)
-   [**MOM \_ aperto**](mom-open.md)

## <a name="output-devices"></a>Dispositivi di output

-   [Matrice di matrici](keyarray.md)
-   [**midiOutCacheDrumPatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches)
-   [**midiOutCachePatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)
-   [**midiOutGetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume)
-   [**midiOutSetVolume**](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume)
-   [PATCHARRAY](patcharray.md)

## <a name="playing-a-message-or-messages"></a>Riproduzione di un messaggio o di messaggi

-   [**\_EVENTPARM MEVT**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm)
-   [**MEVT \_ eventType**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype)
-   [**MIDIEVENT**](/windows/win32/api/mmeapi/ns-mmeapi-midievent)
-   [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)
-   [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)
-   [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg)
-   [**midiStreamOut**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [**midiStreamPause**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [**midiStreamRestart**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [**midiStreamStop**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)
-   [**MM \_ MOM \_ completato**](mm-mom-done.md)
-   [**MM \_ \_ POSITIONCB MOM**](mm-mom-positioncb.md)
-   [**MOM \_ completato**](mom-done.md)
-   [**\_POSITIONCB MOM**](mom-positioncb.md)

## <a name="recording"></a>Registrazione

-   [**midiConnect**](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect)
-   [**midiDisconnect**](/windows/win32/api/mmeapi/nf-mmeapi-mididisconnect)
-   [**midiInReset**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)
-   [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)
-   [**midiInStop**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)
-   [**MIDIPROPTEMPO**](/windows/win32/api/mmeapi/ns-mmeapi-midiproptempo)
-   [**MIDIPROPTIMEDIV**](/windows/win32/api/mmeapi/ns-mmeapi-midiproptimediv)
-   [**\_dati MIM**](mim-data.md)
-   [**\_LONGDATA MIM**](mim-longdata.md)
-   [**\_MOREDATA MIM**](mim-moredata.md)
-   [**\_dati MIM \_ mm**](mm-mim-data.md)
-   [**\_MOREDATA MIM \_ mm**](mm-mim-moredata.md)
-   [**\_LONGDATA MIM \_ mm**](mm-mim-longdata.md)

## <a name="sending-messages-to-devices"></a>Invio di messaggi ai dispositivi

-   [**midiInMessage**](/windows/win32/api/mmeapi/nf-mmeapi-midiinmessage)
-   [**midiOutMessage**](/windows/win32/api/mmeapi/nf-mmeapi-midioutmessage)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[MIDI (Musical Instrument Digital Interface)](musical-instrument-digital-interface--midi.md)
</dt> </dl>

 

 