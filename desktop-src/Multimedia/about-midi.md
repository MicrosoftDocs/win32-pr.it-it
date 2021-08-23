---
title: Informazioni su MIDI
description: Informazioni su MIDI
ms.assetid: 32030c98-e513-4ee3-bbd0-ba41fceadd57
keywords:
- Windows multimediali, Midi (Musical Instrument Digital Interface)
- multimedia,Musical Instrument Digital Interface (MIDI)
- audio multimediale, Interfaccia digitale dello strumento musicale (MIDI)
- audio, Interfaccia digitale dello strumento musicale (MIDI)
- Musical Instrument Digital Interface (MIDI), about
- MIDI (Musical Instrument Digital Interface),about
- MIDI (Musical Instrument Digital Interface), Media Control Interface (MCI)
- MIDI (Musical Instrument Digital Interface), Media Control Interface (MCI)
- MIDI (Musical Instrument Digital Interface), buffer di flusso
- MIDI (Musical Instrument Digital Interface), buffer di flusso
- Servizi MIDI (Musical Instrument Digital Interface), MIDI
- MIDI (Musical Instrument Digital Interface), servizi MIDI
- Media Control Interface (MCI), Musical Instrument Digital Interface (MIDI)
- MCI (Media Control Interface),Musical Instrument Digital Interface (MIDI)
- buffer di flusso, informazioni
- Servizi MIDI, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad1ce20164c42342c52defd27e7f3ccdfb0a44ec9a4e0a6679c1b190270fc62e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526691"
---
# <a name="about-midi"></a>Informazioni su MIDI

L'API (Application Programming Interface) Microsoft Win32 offre i metodi seguenti per l'utilizzo dei dati MIDI da parte delle applicazioni:

-   L'interfaccia MCI (Media Control Interface). Anche se il modo più semplice per riprodurre un file MIDI è usare la classe della finestra MCIWnd, è anche possibile usare i comandi MCI per creare un'interfaccia personalizzata per un dispositivo MIDI. Per altre informazioni sulla classe della finestra MCIWnd, vedere [McIWnd Window Class](mciwnd-window-class.md). Per altre informazioni su MCI, vedere [MCI](mci.md)o [Media Control Interface (MCI).](media-control-interface--mci.md)
-   [Buffer di flusso](stream-buffers.md). Questo formato consente a un'applicazione di modificare i buffer dei dati MIDI con timestamp per la riproduzione. I buffer di flusso sono utili per le applicazioni che richiedono un controllo più preciso sull'output rispetto alle offerte MCI.
-   [Servizi MIDI](midi-services.md). Le applicazioni che richiedono il controllo più preciso dei dati MIDI in genere usano questi servizi di basso livello.

Negli argomenti seguenti viene illustrato ognuno di questi metodi e viene fornita una panoramica di MIDI Mapper.

-   [The MIDI Mapper](the-midi-mapper.md)
-   [Media Control Interface (MCI)](media-control-interface--mci.md)
-   [Buffer di flusso](stream-buffers.md)
-   [Servizi MIDI](midi-services.md)
-   [Riproduzione di file MIDI](playing-midi-files.md)
-   [Registrazione dell'audio MIDI](recording-midi-audio.md)
-   [Elaborazione di dati MIDI da due origini MIDI](processing-midi-data-from-two-midi-sources.md)
-   [Creazione di file MIDI](creating-midi-files.md)

 

 




