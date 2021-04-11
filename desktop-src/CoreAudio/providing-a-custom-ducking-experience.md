---
description: Un'applicazione può rifiutare esplicitamente l'esperienza di ducking predefinita gestita dal sistema e sostituirla con un'implementazione personalizzata.
ms.assetid: 18290d05-b114-476b-8365-6bbb5fe6cffc
title: Fornire un comportamento di ducking personalizzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4051dc7b79f698f10d007beaafa97e90d79f3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127426"
---
# <a name="providing-a-custom-ducking-behavior"></a>Fornire un comportamento di ducking personalizzato

Un'applicazione può rifiutare esplicitamente l' [esperienza di ducking predefinita](stream-attenuation.md) gestita dal sistema e sostituirla con un'implementazione personalizzata.

Un'applicazione può offrire un'esperienza di ducking personalizzata. Ad esempio, Windows Media Player fornisce una propria esperienza di ducking sospendendo il flusso multimediale corrente durante una sessione di comunicazione e riprendendo la riproduzione quando la sessione viene chiusa. Con Windows SDK esempi è inclusa un'applicazione multimediale di esempio che implementa ducking; Per ulteriori informazioni, vedere [DuckingMediaPlayer](duckingmediaplayer.md). Per simulare l'esperienza di apertura e chiusura dei flussi di comunicazione e la generazione di eventi ducking, vedere [DuckingCaptureSample](duckingcapturesample.md), che è anche incluso in Windows SDK esempi.

Un'applicazione multimediale che riproduce i suoni da attenuare deve essere in grado di riconoscere i flussi di comunicazione, quando vengono aperti e chiusi nel sistema. È possibile fornire l'implementazione personalizzata usando MediaFoundation, DirectShow o DirectSound, che usano le API di base di audio. Un client WASAPI diretto può anche eseguire l'override della gestione predefinita se sa quando inizia e termina la sessione di comunicazione.

**Per offrire un'esperienza di ducking personalizzata, un client WASAPI deve eseguire le attività seguenti:**

1.  Registrarsi per ricevere eventi ducking da *ducking Manager*, un componente del sistema audio che gestisce le notifiche relative alle modifiche del flusso di comunicazione. Per altre informazioni, [ottenere eventi ducking](handling-audio-ducking-events-from-communication-devices.md).
    > [!Note]  
    > Se il client viene registrato per ricevere notifiche di ducking, il Manager di ducking Disabilita il comportamento predefinito fornito dal sistema. Se il comportamento predefinito è disabilitato esplicitamente (vedere [disabilitazione dell'esperienza di ducking predefinita](disabling-the-ducking-experience.md)) e il client non fornisce un comportamento di sostituzione, l'applicazione non ha alcun comportamento di ducking.

     

2.  Ascolta le notifiche degli eventi Duck inviate da ducking Manager ed Esegui il comportamento di ducking desiderato. Per altre informazioni sull'implementazione di un comportamento di ducking, vedere [considerazioni sull'implementazione per le notifiche di ducking](handling-audio-ducking-events-from-communication-devices.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di un dispositivo di comunicazione](using-the-communication-device.md)
</dt> <dt>

[Esperienza di ducking predefinita](stream-attenuation.md)
</dt> <dt>

[Disabilitazione dell'esperienza di ducking predefinita](disabling-the-ducking-experience.md)
</dt> <dt>

[Considerazioni sull'implementazione per le notifiche di ducking](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Recupero di eventi ducking](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



