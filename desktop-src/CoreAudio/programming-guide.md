---
description: Guida per programmatori
ms.assetid: 825c7cd7-dc66-47b6-a1b6-d10101daebb3
title: Guida per programmatori audio Core
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb99369058983ebac7205053efdf967bbb8c36d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225758"
---
# <a name="core-audio-programming-guide"></a>Guida per programmatori audio Core

In questa sezione della guida vengono illustrati i concetti e le funzionalità delle principali API audio di Windows Vista e viene descritto come utilizzarli nella programmazione delle applicazioni.

In questa sezione vengono trattati gli argomenti seguenti.



| Argomento                                                                                                                      | Descrizione                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Componenti audio in modalità utente](user-mode-audio-components.md)                                                               | Attraverso le interfacce di basso livello nelle API di base audio, un client può accedere ai componenti di sistema che gestiscono e combinano i flussi audio.                                                                        |
| [Audio modalità utente protetto (PUMA)](protected-user-mode-audio--puma-.md)                                                   | Vengono descritti gli aggiornamenti dell'audio in modalità utente protetto (PUMA), il motore audio in modalità utente nell'ambiente protetto (PE), che fornisce un ambiente più sicuro per l'elaborazione e il rendering audio.              |
| [Dispositivi endpoint audio](audio-endpoint-devices.md)                                                                       | Un dispositivo endpoint audio è un'astrazione del software che consente interazioni intuitive con dispositivi audio come microfoni e altoparlanti.                                                              |
| [Sessioni audio](audio-sessions.md)                                                                                       | Una sessione audio è un'astrazione del software che consente a un client di gestire una raccolta di flussi audio correlati come una singola unità.                                                                           |
| [Controlli del volume](volume-controls.md)                                                                                     | Il sistema integra le impostazioni dei volumi basate su criteri con le impostazioni del volume dell'utente in modo logico e coerente.                                                                                      |
| [Gestione dei flussi](stream-management.md)                                                                                 | L'API di sessione audio di Windows (WASAPI) fornisce un client con un set completo di metodi per la creazione e la gestione di flussi audio.                                                                             |
| [Topologie del dispositivo](device-topologies.md)                                                                                 | L'API DeviceTopology consente a un client di individuare i controlli audio che si trovano lungo i vari percorsi dati nell'hardware audio.                                                                          |
| [Uso dell'interfaccia IKsControl per accedere alle proprietà audio](using-the-ikscontrol-interface-to-access-audio-properties.md) | Un'applicazione audio specializzata potrebbe dover utilizzare l'interfaccia IKsControl per accedere alle proprietà di una scheda audio.                                                                                     |
| [Interoperabilità con le API audio legacy](interoperability-with-legacy-audio-apis.md)                                     | Le funzionalità principali delle API audio di base di Windows Vista possono essere incorporate in applicazioni esistenti che utilizzano le funzioni DirectSound, DirectShow e Windows Multimedia **waveOutXxx** e **waveInXxx** . |
| [Audio spaziale](spatial-sound.md)                                                                                         | Vengono fornite informazioni aggiuntive per l'utilizzo di Windows Sonic, la soluzione a livello di piattaforma Microsoft per il supporto di suoni spaziali in Xbox e Windows, che consente l'uso di segnali audio sia per l'elevazione (sopra o sotto il listener). |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API audio Core](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



