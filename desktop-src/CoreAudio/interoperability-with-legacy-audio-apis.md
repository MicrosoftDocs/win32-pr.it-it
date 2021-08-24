---
description: Interoperabilità con LE API audio legacy
ms.assetid: 34939f6d-a6e4-4f7a-afa3-b1fed52b471f
title: Interoperabilità con LE API audio legacy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f894c20785ebd49e50765ad67ba19056f5439bd5ab8c8fc7e0bcfbdd05fe04ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875431"
---
# <a name="interoperability-with-legacy-audio-apis"></a>Interoperabilità con LE API audio legacy

Molte applicazioni esistenti usano API audio legacy, ad esempio DirectSound, DirectShow e le Windows multimediali. Con solo piccole modifiche, queste applicazioni possono essere aumentate per usare i ruoli del [dispositivo,](device-roles.md)i controlli del [volume](session-volume-controls.md)di sessione e altre funzionalità delle API audio principali in Windows Vista.

Come descritto in [Componenti audio in](user-mode-audio-components.md)modalità utente, le API audio di base fungono da base per la compilazione delle API audio di livello superiore. In Windows Vista, i dispositivi audio a cui le applicazioni accedono tramite API audio legacy, ad esempio DirectSound e le funzioni **waveOutXxx** e **waveInXxx** dei supporti Windows, sono infatti dispositivi [endpoint audio](audio-endpoint-devices.md) implementati dalle API audio di base. A causa di limitazioni intrinseche nelle interfacce delle API audio legacy, un'applicazione può accedere ad alcune ma non a tutte le funzionalità dei dispositivi endpoint audio tramite queste interfacce. Le sezioni seguenti descrivono le tecniche per migliorare le applicazioni esistenti accedendo alle funzionalità aggiuntive dei dispositivi endpoint audio direttamente tramite le API audio di base. Questi miglioramenti richiedono in genere solo piccole modifiche al codice dell'applicazione esistente.

Le sezioni seguenti descrivono come incorporare le funzionalità delle API audio di base nelle applicazioni esistenti che usano API audio legacy:

-   [Ruoli del dispositivo per applicazioni DirectSound](device-roles-for-directsound-applications.md)
-   [Ruoli del dispositivo per DirectShow applicazioni](device-roles-for-directshow-applications.md)
-   [Ruoli del dispositivo per applicazioni multimediali Windows legacy](device-roles-for-legacy-windows-multimedia-applications.md)
-   [Eventi audio per applicazioni audio legacy](audio-events-for-legacy-audio-applications.md)
-   [Suoni di notifica per applicazioni audio legacy](notification-sounds-for-legacy-audio-applications.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ruoli del dispositivo](device-roles.md)
</dt> </dl>

 

 



