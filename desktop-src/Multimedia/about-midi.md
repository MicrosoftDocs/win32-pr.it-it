---
title: Informazioni su MIDI
description: Informazioni su MIDI
ms.assetid: 32030c98-e513-4ee3-bbd0-ba41fceadd57
keywords:
- Multimedia di Windows, Musical Instrument Digital Interface (MIDI)
- Multimedia, Musical Instrument Digital Interface (MIDI)
- audio multimediale, MIDI (Musical Instrument Digital Interface)
- audio, Musical Instrument Digital Interface (MIDI)
- MIDI (Musical Instrument Digital Interface), informazioni
- MIDI (Musical Instrument Digital Interface), informazioni
- MIDI (Musical Instrument Digital Interface), MCI (Media Control Interface)
- MIDI (strumento musicale digitale), MCI (Media Control Interface)
- MIDI (Musical Instrument Digital Interface), buffer di flusso
- MIDI (Musical Instrument Digital Interface), buffer di flusso
- MIDI (Musical Instrument Digital Interface), servizi MIDI
- MIDI (Musical Instrument Digital Interface), servizi MIDI
- Interfaccia di controllo multimediale (MCI), Musical Instrument Digital Interface (MIDI)
- MCI (Media Control Interface), Musical Instrument Digital Interface (MIDI)
- buffer di flusso, informazioni
- Servizi MIDI, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c476807f750f9e90788377588f6c9af96561aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708926"
---
# <a name="about-midi"></a>Informazioni su MIDI

Il Application Programming Interface Microsoft Win32 (API) fornisce i metodi seguenti per l'utilizzo dei dati MIDI da parte delle applicazioni:

-   L'interfaccia di controllo multimediale (MCI). Sebbene il modo più semplice per riprodurre un file MIDI consiste nell'usare la classe della finestra MCIWnd, è anche possibile usare i comandi MCI per creare un'interfaccia personalizzata per un dispositivo MIDI. Per ulteriori informazioni sulla classe della finestra MCIWnd, vedere [classe della finestra MCIWnd](mciwnd-window-class.md). Per ulteriori informazioni su MCI, vedere [MCI](mci.md)o [MCI (Media Control Interface)](media-control-interface--mci.md).
-   [Buffer di flusso](stream-buffers.md). Questo formato consente a un'applicazione di modificare buffer di dati MIDI timestamp per la riproduzione. I buffer di flusso sono utili per le applicazioni che richiedono un controllo più preciso sull'output rispetto alle offerte MCI.
-   [Servizi MIDI](midi-services.md). Le applicazioni che richiedono il controllo più preciso dei dati MIDI utilizzano in genere questi servizi di basso livello.

Negli argomenti seguenti vengono descritti ognuno di questi metodi e viene fornita una panoramica del mapper di MIDI.

-   [Mapper MIDI](the-midi-mapper.md)
-   [Interfaccia di controllo multimediale (MCI)](media-control-interface--mci.md)
-   [Buffer di flusso](stream-buffers.md)
-   [Servizi MIDI](midi-services.md)
-   [Riproduzione di file MIDI](playing-midi-files.md)
-   [Registrazione audio MIDI](recording-midi-audio.md)
-   [Elaborazione di dati MIDI da due origini MIDI](processing-midi-data-from-two-midi-sources.md)
-   [Creazione di file MIDI](creating-midi-files.md)

 

 




