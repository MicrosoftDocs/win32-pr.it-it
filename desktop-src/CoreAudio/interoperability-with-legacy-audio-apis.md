---
description: Interoperabilità con le API audio legacy
ms.assetid: 34939f6d-a6e4-4f7a-afa3-b1fed52b471f
title: Interoperabilità con le API audio legacy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6b9a80b55695ffcfd3ac54e871f00ea27744d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966257"
---
# <a name="interoperability-with-legacy-audio-apis"></a>Interoperabilità con le API audio legacy

Molte applicazioni esistenti usano API audio legacy, ad esempio DirectSound, DirectShow e le funzioni multimediali di Windows. Con le sole modifiche minime, queste applicazioni possono essere ampliate per usare i [ruoli del dispositivo](device-roles.md), i controlli del volume di [sessione](session-volume-controls.md)e altre funzionalità delle API di base per audio in Windows Vista.

Come descritto in [componenti audio in modalità utente](user-mode-audio-components.md), le API di base dell'audio vengono usate come base per la compilazione di API audio di livello superiore. In Windows Vista, i dispositivi audio che accedono alle applicazioni tramite API audio legacy, ad esempio DirectSound e le funzioni Windows Media **waveOutXxx** e **waveInXxx** , sono in effetti [dispositivi di endpoint audio](audio-endpoint-devices.md) implementati dalle API di base audio. A causa delle limitazioni intrinseche nelle interfacce delle API audio legacy, un'applicazione può accedere ad alcune delle funzionalità dei dispositivi dell'endpoint audio tramite queste interfacce, ma non tutte. Le sezioni seguenti descrivono le tecniche per migliorare le applicazioni esistenti accedendo a funzionalità aggiuntive dei dispositivi dell'endpoint audio direttamente tramite le API di base di audio. Questi miglioramenti richiedono in genere solo modifiche minime al codice dell'applicazione esistente.

Le sezioni seguenti descrivono come incorporare le funzionalità delle API audio di base in applicazioni esistenti che usano le API audio legacy:

-   [Ruoli del dispositivo per le applicazioni DirectSound](device-roles-for-directsound-applications.md)
-   [Ruoli del dispositivo per le applicazioni DirectShow](device-roles-for-directshow-applications.md)
-   [Ruoli del dispositivo per applicazioni multimediali Windows legacy](device-roles-for-legacy-windows-multimedia-applications.md)
-   [Eventi audio per applicazioni audio legacy](audio-events-for-legacy-audio-applications.md)
-   [Suoni di notifica per le applicazioni audio legacy](notification-sounds-for-legacy-audio-applications.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ruoli del dispositivo](device-roles.md)
</dt> </dl>

 

 



