---
description: Un'applicazione può rifiutare esplicitamente l'esperienza di gestione predefinita gestita dal sistema e sostituirla con un'implementazione personalizzata.
ms.assetid: 18290d05-b114-476b-8365-6bbb5fe6cffc
title: Fornire un comportamento personalizzato per l'accodamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72cf4bb254b97a6a9d6b5c9d415d48a2c95f528f20efbf2ffbe4782ae5980400
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406369"
---
# <a name="providing-a-custom-ducking-behavior"></a>Fornire un comportamento personalizzato per l'accodamento

Un'applicazione può rifiutare esplicitamente [l'esperienza di gestione](stream-attenuation.md) predefinita gestita dal sistema e sostituirla con un'implementazione personalizzata.

Un'applicazione può offrire un'esperienza di "papera personalizzata". Ad esempio, Windows Media Player la propria esperienza di accodamento sosendo il flusso multimediale corrente durante una sessione di comunicazione e riprendendo la riproduzione alla chiusura della sessione. Un'applicazione multimediale di esempio che implementa l'endosezione è inclusa Windows sdk di esempio; Per altre informazioni, vedere [La creazione di un oggettoMediaPlayer.](duckingmediaplayer.md) Per simulare l'esperienza di apertura e chiusura dei flussi di comunicazione e la generazione di eventi di atrofia, vedere [l'esempio DiaascaptureSample,](duckingcapturesample.md)incluso anche con Windows SDK.

Un'applicazione multimediale che riproduce suoni da attenuare deve essere a conoscenza dei flussi di comunicazione, quando vengono aperti e chiusi nel sistema. L'implementazione personalizzata può essere fornita usando MediaFoundation, DirectShow o DirectSound, che usano le API audio di base. Un client WASAPI diretto può anche eseguire l'override della gestione predefinita se sa quando viene avviata e terminata la sessione di comunicazione.

**Per offrire un'esperienza di azzeramento personalizzata, un client WASAPI deve eseguire le attività seguenti:**

1.  Eseguire la registrazione per ricevere gli eventi di inasamento dal gestore di *notifiche,* un componente del sistema audio che gestisce le notifiche correlate alle modifiche del flusso di comunicazione. Per altre informazioni, [vedere Getting Ducking Events](handling-audio-ducking-events-from-communication-devices.md).
    > [!Note]  
    > Se il client viene registrato per la ricezione di notifiche di inassamento, il gestore di notifiche disabilita il comportamento predefinito fornito dal sistema. Se il comportamento predefinito è disabilitato in modo esplicplicato (vedere Disabilitazione dell'esperienza di gestione [predefinita)](disabling-the-ducking-experience.md)e il client non fornisce un comportamento sostitutivo, l'applicazione non sperimenta alcun comportamento di insodettamento.

     

2.  Restare in ascolto delle notifiche degli eventi di antartide inviate dal responsabile dell'endosezione ed eseguire il comportamento desiderato. Per altre informazioni sull'implementazione di un comportamento di disaccodamento, vedere Considerazioni sull'implementazione [per l'applicazione di notifiche.](handling-audio-ducking-events-from-communication-devices.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di un dispositivo di comunicazione](using-the-communication-device.md)
</dt> <dt>

[Esperienza di analisi predefinita](stream-attenuation.md)
</dt> <dt>

[Disabilitazione dell'esperienza di analisi predefinita](disabling-the-ducking-experience.md)
</dt> <dt>

[Considerazioni sull'implementazione per l'accodamento delle notifiche](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Recupero di eventi di antartide](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



