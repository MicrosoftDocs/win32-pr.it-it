---
description: Informazioni sui concetti e sulle funzionalità delle API audio principali di Windows Vista e su come usarle nella programmazione di applicazioni.
ms.assetid: 825c7cd7-dc66-47b6-a1b6-d10101daebb3
title: Guida alla programmazione audio di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f02e27206c70cca69abf263cfa49dfd439c480
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405874"
---
# <a name="core-audio-programming-guide"></a>Guida alla programmazione audio di base

Questa sezione della guida illustra i concetti e le funzionalità delle API audio di base di Windows Vista e descrive come usarle nella programmazione di applicazioni.

In questa sezione vengono trattati gli argomenti seguenti.



| Argomento                                                                                                                      | Descrizione                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Componenti audio in modalità utente](user-mode-audio-components.md)                                                               | Tramite le interfacce di basso livello nelle API audio di base, un client può accedere ai componenti di sistema che gestiscono e combinano flussi audio.                                                                        |
| [PuMA (Protected User Mode Audio)](protected-user-mode-audio--puma-.md)                                                   | Descrive gli aggiornamenti di PUMA (Protected User Mode Audio), il motore audio in modalità utente nell'ambiente protetto (PE), che offre un ambiente più sicuro per l'elaborazione e il rendering audio.              |
| [Dispositivi endpoint audio](audio-endpoint-devices.md)                                                                       | Un dispositivo endpoint audio è un'astrazione software che consente interazioni descrittive con dispositivi audio, ad esempio microfoni e altoparlanti.                                                              |
| [Sessioni audio](audio-sessions.md)                                                                                       | Una sessione audio è un'astrazione software che consente a un client di gestire una raccolta di flussi audio correlati come singola unità.                                                                           |
| [Controlli del volume](volume-controls.md)                                                                                     | Il sistema integra le impostazioni del volume basate su criteri con le impostazioni del volume dell'utente in modo logico e coerente.                                                                                      |
| [Gestione dei flussi](stream-management.md)                                                                                 | L'API della sessione audio di Windows (WASAPI) fornisce a un client un set completo di metodi per la creazione e la gestione dei flussi audio.                                                                             |
| [Topologie di dispositivi](device-topologies.md)                                                                                 | L'API DeviceTopology consente a un client di individuare i controlli audio che si trovano lungo i vari percorsi dati nell'hardware audio.                                                                          |
| [Uso dell'interfaccia IKsControl per accedere alle proprietà audio](using-the-ikscontrol-interface-to-access-audio-properties.md) | Un'applicazione audio specializzata potrebbe dover usare l'interfaccia IKsControl per accedere alle proprietà di un adattatore audio.                                                                                     |
| [Interoperabilità con LE API audio legacy](interoperability-with-legacy-audio-apis.md)                                     | Le funzionalità principali delle API audio principali in Windows Vista possono essere incorporate nelle applicazioni esistenti che usano DirectSound, DirectShow e le funzioni **waveOutXxx** e **waveInXxx** multimediali di Windows. |
| [Audio spaziale](spatial-sound.md)                                                                                         | Fornisce indicazioni per l'uso di Windows Sonic, la soluzione microsoft a livello di piattaforma per il supporto dell'audio spaziale in Xbox e Windows, abilitando segnali audio sia di surround che di elevazione (sopra o sotto il listener). |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[API audio di base](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



